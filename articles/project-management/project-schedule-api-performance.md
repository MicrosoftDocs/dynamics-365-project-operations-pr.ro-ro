---
title: Performanța API-ului de planificare a proiectelor
description: Acest articol oferă informații despre standardele de performanță ale API-urilor de planificare a proiectului și identifică cele mai bune practici pentru o utilizare optimă.
author: ruhercul
ms.date: 11/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1ee1bd8e4412ee1d10f445628c5dc87cc9fa91d3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911197"
---
# <a name="project-schedule-api-performance"></a>Performanța API-ului de planificare a proiectelor

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stoc, implementare Lite - facturare de la ofertă și până la proforma, Project for the web_

Acest articol oferă informații despre standardele de performanță ale interfețelor de programare a aplicațiilor (API) pentru planificarea proiectului și identifică cele mai bune practici pentru optimizarea utilizării.

## <a name="project-scheduling-service"></a>Serviciu de planificare a proiectului
Serviciul de planificare a proiectelor este un serviciu multi-entități găzduite care rulează în Microsoft Azure. Este conceput pentru a îmbunătăți interacțiunea, oferind o experiență rapidă și fluidă atunci când utilizatorii lucrează la proiecte. Această îmbunătățire se realizează prin acceptarea cererilor de modificare, procesarea acestora și apoi returnarea imediată a rezultatului. Serviciul persistă în mod asincron în Dataverse și nu blochează utilizatorii să efectueze alte operațiuni.

API-urile de planificare a proiectului se bazează pe Serviciul de planificare a proiectelor pentru a rula solicitări care sunt descrise mai detaliat în secțiunile ulterioare ale acestui articol.

API-urile de planificare a proiectului sunt concepute pentru a funcționa cu următoarele entități cu structură de detaliată a lucrărilor (WBS):

  - Project
  - Activitate proiect
  - Dependență de activitate proiect
  - Membru echipă de proiect
  - Atribuire de resurse
  
Sunt acceptate atât câmpurile predefinite, cât și câmpurile personalizate. Dacă nu se specifică altfel, sunt acceptate toate operațiunile comune, cum ar fi crearea, actualizarea și ștergerea. Pentru mai multe informații, consultați [Utilizați API-urile de planificare a proiectului și entitățile de planificare](schedule-api-preview.md).

Ca parte a API-urilor de planificare a proiectului, a fost adăugat un model de unitate de lucru. Acest model este cunoscut sub numele de OperationSet și poate fi utilizat atunci când mai multe cereri trebuie procesate într-o singură tranzacție.

Următoarea ilustrație arată fluxul pe care îl va experimenta un partener atunci când este utilizată această funcție.

![Dataverse și fluxul serviciului de planificare proiect.](./media/dataverse-project-scheduling-service-flow.png)

**Pasul 1**: Un client efectuează un apel API către un punct final OData (Open Data Protocol) în Dataverse pentru a crea un OperationSet.

**Pasul 2** : După ce noul OperationSet este creat, este returnată o valoare **OperationSetId**.

**Pasul 3** : Clientul utilizează valoarea **OperationSetId** pentru a face o altă solicitare API de planificare a proiectului. Rezultatul este o solicitare de creare, actualizare sau ștergere pentru o entitate de planificare. Când se face această solicitare, se face validarea metadatelor. Dacă validarea eșuează, cererea este terminată și este returnată o eroare.

**Pașii 4a–4c**: Acești pași reprezintă faza ACCEPTARE. Clientul apelează API **ExecuteOperationSetV1**, care trimite toate modificările către Serviciul de planificare a proiectelor într-un singur lot. Serviciul de planificare a proiectelor rulează propriile validări la solicitările din lot. Orice eșec de validare anulează lotul și returnează o excepție apelantului. Dacă lotul este acceptat cu succes de către Serviciul de planificare a proiectelor, starea OperationSet este actualizată pentru a reflecta faptul că OperationSet este procesată de către Serviciul de planificare a proiectelor.

**Pasul 5**: Acest pas reprezintă faza PERSISTĂ. Serviciul de planificare a proiectelor scrie asincron lotul în Dataverse într-o tranzacție. Dacă operația de scriere are succes, OperationSet este marcat ca **Efectuat**. Orice erori derulează înapoi tranzacția și lotul, iar OperationSet este marcat ca **Eșuat**.

## <a name="performance-methodology"></a>Metodologia performanței
Timpul de execuție este definit ca timpul de la apel până la API **ExecuteOperationSetV1** până când Serviciul de planificare a proiectelor a terminat de scris către Dataverse. Toate operațiunile rulează combinate de 2.200 de ori, iar măsurătorile timpului de execuție P99 sunt raportate. Sunt măsurate operațiunile cu o singură înregistrare și operațiunile în vrac.

Pentru o operație cu o singură înregistrare, OperationSet conține o singură solicitare. Pentru operațiunile în bloc, conține 20, 50 sau 100 de solicitări. Fiecare dimensiune în vrac este raportată separat.

Aceste operațiuni rulează pe o implementare UR 15 Project Operations Lite în America de Nord.

## <a name="results"></a>Rezultate
### <a name="create-operations"></a>Creați operațiuni
#### <a name="single-record-create-operations"></a>Operațiuni de creare a unei singure înregistrări
Următorul tabel prezintă timpii de execuție pentru crearea unei singure înregistrări. Timpii sunt în secunde.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">Tip&nbsp;&nbsp;&nbsp;înregistrare</th>
    <th class="tg-0lax" colspan="2">Timp</th>
  </tr>
  <tr>
    <th class="tg-0lax">Câmpuri obligatorii</th>
    <th class="tg-0lax">Toate câmpurile acceptate</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Project</td>
    <td class="tg-0lax">2.5</td>
    <td class="tg-0lax">3.78</td>
  </tr>
  <tr>
    <td class="tg-0lax">Activitate</td>
    <td class="tg-0lax">8.82</td>
    <td class="tg-0lax">9.34</td>
  </tr>
  <tr>
    <td class="tg-0lax">Atribuire</td>
    <td class="tg-0lax">9.19</td>
    <td class="tg-0lax">9.19</td>
  </tr>
  <tr>
    <td class="tg-0lax">Membru echipă</td>
    <td class="tg-0lax">0.84</td>
    <td class="tg-0lax">4.2</td>
  </tr>
  <tr>
    <td class="tg-0lax">Dependență</td>
    <td class="tg-0lax">8.84</td>
    <td class="tg-0lax">8.84</td>
  </tr>
</tbody>
</table>

#### <a name="bulk-create-operations"></a>Operațiuni de creare în bloc
Următorul tabel prezintă timpii de execuție pentru crearea multor înregistrări. Mai exact, Microsoft a măsurat timpii de execuție pentru crearea a 20, 50 și 100 de înregistrări într-un singur OperationSet. Timpii sunt în secunde.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="3">Tip&nbsp;&nbsp;&nbsp;înregistrare</th>
    <th class="tg-0lax" colspan="6">Timp</th>
  </tr>
  <tr>
    <th class="tg-0lax" colspan="2">20 de înregistrări</th>
    <th class="tg-0lax" colspan="2">50 de înregistrări</th>
    <th class="tg-0lax" colspan="2">100 de înregistrări</th>
  </tr>
  <tr>
    <th class="tg-0lax">Câmpuri obligatorii</th>
    <th class="tg-0lax">Toate câmpurile acceptate</th>
    <th class="tg-0lax">Câmpuri obligatorii</th>
    <th class="tg-0lax">Toate câmpurile acceptate</th>
    <th class="tg-0lax">Câmpuri obligatorii</th>
    <th class="tg-0lax">Toate câmpurile acceptate</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Activitate</td>
    <td class="tg-0lax">19.92</td>
    <td class="tg-0lax">38.35</td>
    <td class="tg-0lax">36.67</td>
    <td class="tg-0lax">99.13</td>
    <td class="tg-0lax">116.77</td>
    <td class="tg-0lax">174.06</td>
  </tr>
  <tr>
    <td class="tg-0lax">Atribuire</td>
    <td class="tg-0lax">13.94</td>
    <td class="tg-0lax">13.94</td>
    <td class="tg-0lax">43.95</td>
    <td class="tg-0lax">43.95</td>
    <td class="tg-0lax">69.38</td>
    <td class="tg-0lax">69.38</td>
  </tr>
  <tr>
    <td class="tg-0lax">Dependență</td>
    <td class="tg-0lax">30.04</td>
    <td class="tg-0lax">30.04</td>
    <td class="tg-0lax">77.82</td>
    <td class="tg-0lax">77.82</td>
    <td class="tg-0lax">176.89</td>
    <td class="tg-0lax">176.89</td>
  </tr>
</tbody>
</table>

> [!NOTE] 
> Operațiuni de creare în bloc pe entitățile **Proiect** și **Membru al echipei** nu sunt incluse în acest tabel, deoarece timpul de rulare pentru acele operațiuni seamănă cu timpul de rulare când API-ul pentru crearea unei singure înregistrări este apelat de mai multe ori. Aceste API-uri sunt rulate imediat în Dataverse.

Următoarea ilustrație prezintă un grafic al timpilor de execuție pentru entitățile **Activitate**, **Misiune** și **Dependenţă** când sunt create 20, 50 și 100 de înregistrări și sunt utilizate toate câmpurile acceptate.

![Creați un grafic al timpului de execuție a înregistrării.](./media/create-record-execution-time.png)

### <a name="update-operations"></a>Actualizați operațiuni
#### <a name="single-record-update-operations"></a>Operațiuni de actualizare a unei singure înregistrări
Următorul tabel prezintă timpii de execuție pentru actualizarea unei singure înregistrări. Timpii sunt în secunde.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">Tip&nbsp;&nbsp;&nbsp;înregistrare</th>
    <th class="tg-0lax" colspan="2">Timp</th>
  </tr>
  <tr>
    <th class="tg-0lax">Câmpuri obligatorii </th>
    <th class="tg-0lax">Toate câmpurile acceptate</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Project</td>
    <td class="tg-0lax">9.53</td>
    <td class="tg-0lax">13.91</td>
  </tr>
  <tr>
    <td class="tg-0lax">Activitate</td>
    <td class="tg-0lax">8.82</td>
    <td class="tg-0lax">9.91</td>
  </tr>
  <tr>
    <td class="tg-0lax">Membru echipă</td>
    <td class="tg-0lax">9</td>
    <td class="tg-0lax">8.96</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> Operațiuni de actualizare pe entitățile **Atribuții de resurse** și **Dependența sarcinilor proiectului** nu sunt acceptate.

#### <a name="bulk-update-operations"></a>Operațiuni de actualizare în bloc
Următorul tabel prezintă timpii de execuție pentru actualizarea multor înregistrări. Mai exact, Microsoft a măsurat timpii de execuție pentru actualizarea a 20, 50 și 100 de înregistrări într-un singur OperationSet. Timpii sunt în secunde.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="3">Tip&nbsp;&nbsp;&nbsp;înregistrare</th>
    <th class="tg-0lax" colspan="6">Timp</th>
  </tr>
  <tr>
    <th class="tg-0lax" colspan="2">20 de înregistrări</th>
    <th class="tg-0lax" colspan="2">50 de înregistrări</th>
    <th class="tg-0lax" colspan="2">100 de înregistrări</th>
  </tr>
  <tr>
    <th class="tg-0lax">Câmpuri obligatorii</th>
    <th class="tg-0lax">Toate câmpurile acceptate</th>
    <th class="tg-0lax">Câmpuri obligatorii</th>
    <th class="tg-0lax">Toate câmpurile acceptate</th>
    <th class="tg-0lax">Câmpuri obligatorii</th>
    <th class="tg-0lax">Toate câmpurile acceptate</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Activitate</td>
    <td class="tg-0lax">8.91</td>
    <td class="tg-0lax">38.71</td>
    <td class="tg-0lax">20.92</td>
    <td class="tg-0lax">87.13</td>
    <td class="tg-0lax">36.68</td>
    <td class="tg-0lax">190.34</td>
  </tr>
  <tr>
    <td class="tg-0lax">Membru echipă</td>
    <td class="tg-0lax">20.52</td>
    <td class="tg-0lax">26.06</td>
    <td class="tg-0lax">41.93</td>
    <td class="tg-0lax">44.51</td>
    <td class="tg-0lax">38.63</td>
    <td class="tg-0lax">66.53</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> Operațiuni de actualizare pe entitățile **Atribuții de resurse** și **Dependența sarcinilor proiectului** nu sunt acceptate.

Următoarea ilustrație prezintă un grafic al timpilor de execuție pentru entitățile Activitate, și Membru al echipei când sunt actualizate 20, 50 și 100 de înregistrări și sunt utilizate toate câmpurile acceptate.

![Actualizați un grafic al timpului de execuție a înregistrării.](./media/update-record-execution-time.png)

### <a name="delete-operations"></a>Ștergeți operațiuni
#### <a name="single-record-delete-operations"></a>Operațiuni de ștergere a unei singure înregistrări
Următorul tabel prezintă timpii de execuție pentru ștergerea unei singure înregistrări. Timpii sunt în secunde.

| Tip de înregistrare | Timp  |
|-------------|-------|
| Activitate        | 20.12 |
| Atribuire  | 10.86 |
| Membru echipă | 12.52 |
| Dependență  | 20.89 |

> [!NOTE]
> Ștergeți operațiunile de pe entitatea **Proiect** nu sunt acceptate.

#### <a name="bulk-delete-operations"></a>Operațiuni de ștergere în bloc
Următorul tabel prezintă timpii de execuție pentru ștergerea multor înregistrări. Mai exact, Microsoft a măsurat timpii de execuție pentru ștergerea a 20, 50 și 100 de înregistrări într-un singur OperationSet. Timpii sunt în secunde.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">Tip&nbsp;&nbsp;&nbsp;înregistrare</th>
    <th class="tg-0lax" colspan="3">Timp</th>
  </tr>
  <tr>
    <th class="tg-0lax">20 de înregistrări</th>
    <th class="tg-0lax">50 de înregistrări</th>
    <th class="tg-0lax">100 de înregistrări</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Activitate</td>
    <td class="tg-0lax">20.91</td>
    <td class="tg-0lax">67.43</td>
    <td class="tg-0lax">71.96</td>
  </tr>
  <tr>
    <td class="tg-0lax">Atribuire</td>
    <td class="tg-0lax">11.75</td>
    <td class="tg-0lax">25.79</td>
    <td class="tg-0lax">47.66</td>
  </tr>
  <tr>
    <td class="tg-0lax">Membru echipă</td>
    <td class="tg-0lax">9.78</td>
    <td class="tg-0lax">39.73</td>
    <td class="tg-0lax">24.33</td>
  </tr>
  <tr>
    <td class="tg-0lax">Dependență</td>
    <td class="tg-0lax">24.61</td>
    <td class="tg-0lax">54.9</td>
    <td class="tg-0lax">109.16</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> Ștergeți operațiunile de pe entitatea **Proiect** nu sunt acceptate.

Următoarea ilustrație prezintă un grafic al timpilor de execuție pentru entitățile **Activitate**, **Atribuire**, **Membru de echipă** și **Dependență** când sunt șterse 20, 50 și 100 de înregistrări.

![Ștergeți un grafic al timpului de execuție a înregistrării.](./media/delete-record-execution-time.png)

## <a name="observations"></a>Observații
Pentru fiecare operațiune de înregistrare, API-ul **ExecuteOperationSet** durează aproximativ 800 de milisecunde pentru a trimite o solicitare către Serviciul de planificare a proiectelor. Serviciul de planificare a proiectelor durează apoi aproximativ cinci secunde pentru a procesa sarcina utilă și a apela Dataverse. Restul timpului de execuție este petrecut rulând logica de afaceri și scriend date în baza de date în Dataverse.

Când sunt create, actualizate sau șterse 100 de înregistrări, API-ul **ExecuteOperationSet** durează aproximativ trei secunde pentru a trimite cererea către Serviciul de planificare a proiectelor. Serviciul de planificare a proiectelor durează apoi aproximativ cinci secunde pentru a procesa solicitările și a apela Dataverse. Operațiunile în vrac trebuie să plătească o **Taxă de Serviciu de planificare a proiectelor** o singură dată, pentru toate înregistrările din OperationSet. Prin urmare, operațiunile în bloc au un timp mediu de execuție semnificativ mai mic decât operațiunile cu o singură înregistrare.

## <a name="scenarios"></a>Scenarii
Următorul tabel arată timpii de execuție când API-urile de planificare a proiectului sunt utilizate pentru a realiza scenarii specifice. Timpii sunt în secunde.

| Scenariu                                                                   | Timp  |
|----------------------------------------------------------------------------|-------|
| Creați un proiect care are 40 de activități.                                      | 36.01 |
| Creați un proiect care are 40 de activități și 20 de dependențe.                  | 38.11 |
| Creați un proiect care are 40 de activități și 30 de atribuiri.                   | 60.17 |
| Creați un proiect care are 40 de activități, 20 de dependențe și 30 de atribuiri. | 60.27 |

## <a name="best-practices"></a>Cele mai bune practici
Pe baza rezultatelor scenariului precedent, API-urile funcționează mai bine în următoarele condiții:

  - Grupați cât mai multe operațiuni împreună. Durata medie de rulare pentru operațiunile în bloc este mai bună decât durata medie de rulare pentru operațiuni cu o singură înregistrare. Cu cât numărul de OperationSets utilizate este mai mic, cu atât timpul mediu de execuție va fi mai rapid.
  - Setați numai atributele minime necesare pentru a vă îndeplini scenariul. Fiți selectiv cu privire la tipurile de câmpuri neobligatorii incluse într-o solicitare OperationSet. Câmpurile care conțin chei străine sau câmpuri de cumul vor afecta negativ performanța.
