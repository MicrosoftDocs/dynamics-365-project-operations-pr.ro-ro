---
title: Înregistrarea utilizării materialelor pentru proiecte și activitățile proiectului
description: Acest subiect oferă informații despre cum să conectați utilizarea materialului la proiecte și sarcinile proiectului.
author: rumant
ms.date: 03/31/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 60aed9aa82eeb0339e71b0171719e765a63d91e7
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579689"
---
# <a name="record-material-usage-on-projects-and-project-tasks"></a>Înregistrarea utilizării materialelor pentru proiecte și activitățile proiectului

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Pe măsură ce o echipă de proiect lucrează prin sarcini la un proiect, consumă sau utilizează materiale. Un jurnal de utilizare a materialului oferă o modalitate de a înregistra această utilizare, astfel încât să poată fi aprobată de managerul de proiect și eventual facturată către client. 

Pentru a înregistra utilizarea catalogului sau a materialelor din afara catalogului și a le trimite aprobatorului, urmați acești pași: 

1. În panoul de navigare, selectați **Utilizarea materialului**, apoi selectați **Nou**.
2. Pe pagina **Utilizare material nou**, introduceți informațiile necesare de utilizare a materialului, apoi selectați **Salvare**.

Următorul tabel oferă informații despre câmpurile de pe pagina **Jurnal de utilizare a materialelor**. 

| **Câmp** | **Descriere** | **Impactul din aval** |
| --- | --- | --- |
| Descriere | O descriere a utilizării specifice a materialului. | Nu există niciun impact în aval pentru acest câmp. |
| Data | Data la care se așteaptă utilizarea materialului. | Nu există niciun impact în aval pentru acest câmp. |
| Project | O listă de proiecte active. | Selectarea unui proiect pentru un jurnal de utilizare a materialelor are impact asupra câmpului **Sarcină** pentru a afișa numai acele sarcini care sunt în proiect. |
| Activitate | O listă de sarcini pentru proiect, inclusiv sarcini de rezumat și nod frunză. | Selectarea unei sarcini pentru un jurnal de utilizare a materialelor afectează costul materialului real și vânzările reale de material pentru o activitate. Dacă acest câmp este gol, costul corespunzător de utilizare a materialului și vânzările sunt urmărite și sintetizate numai la nivel de proiect. |
| Selectare produs | Specificați dacă această utilizare a materialului este pentru un produs **Existent** (de catalog) un produs **Din afara catalogului**. | Acest câmp determină tipul de produs. |
| Produs | ID-ul produsului din catalogul de produse. Când selectați un ID de produs, câmpul **Selectare Produs** se actualizează automat la **Produs existent**. ID-ul este utilizat pentru a prelua prețurile de cost și de vânzare din lista de prețuri. | Nu există niciun impact în aval pentru acest câmp. |
| Descriere produs din afara catalogului/introdus manual | Un câmp text pentru a introduce numele produsului. Acest câmp este disponibil când selectați un produs **Completat manual** în câmpul **Selectare Produs**.| Nu există niciun impact în aval pentru acest câmp. |
| Resursă ce se poate rezerva| Resursa care a folosit acest material pentru proiect. Valoarea implicită pentru acest câmp este resursa rezervabilă a utilizatorului conectat, dar poate fi modificată pentru a înregistra utilizarea în numele altor membri din echipa proiectului. | Nu există niciun impact în aval pentru acest câmp. |
| Grup de unități | Valoarea implicită din acest câmp provine din grupul de unități configurat ca implicit pentru produsul din catalog. Puteți actualiza acest câmp pentru a selecta un alt grup de unități. | Nu există niciun impact în aval pentru acest câmp. |
| Unitate | Valoarea implicită din acest câmp este unitatea implicită a produsului selectat. Puteți actualiza acest câmp pentru a selecta o altă unitate. | Schimbarea unității are ca rezultat un preț unitar și un cost implicit diferit. |
| Cantitate | Cantitatea de produs care a fost utilizată în proiect sau în sarcina proiectului. | Nu există niciun impact în aval pentru acest câmp. |
| Cost unitar | Costul unitar al produsului selectat și combinația de unități, așa cum este stabilit în lista de prețuri de cost aplicabilă. | Costul unitar este întotdeauna afișat în moneda costului proiectului. Dacă nu există un cost unitar pentru combinația de produs și unitate din lista de prețuri, costul unitar va fi implicit 0,00. |
| Cost total | Valoarea costului care este calculată ca un \*cost unitar al cantității.| Valoarea costului este întotdeauna afișat în moneda costului proiectului. |


## <a name="submit-material-usage-for-review-and-approval"></a>Trimiteți utilizarea materialului pentru examinare și aprobare 
După ce vă capturați toată utilizarea materialului și sunteți gata să îl trimiteți la aprobare, trebuie să trimiteți informațiile de utilizare pentru revizuire.

1. Accesați **Jurnal de utilizare a materialelor** și selectați una sau mai multe intrări. Sau selectați toate înregistrările de utilizare a materialului utilizând caseta de selectare din antet.
2. Selectați **Remitere**. Sistemul procesează intrările selectate și apoi creează cereri de aprobare a utilizării materialelor.

## <a name="recall-a-material-usage-log"></a>Retrageți un jurnal de utilizare de material

Când este necesar, puteți retrage o utilizare a materialului trimisă. Timpul necesar pentru a retrage o intrare de utilizare a materialului depinde de etapa de aprobare.  Dacă aprobatorul nu a aprobat încă înregistrarea, retragerea poate avea loc imediat. Cu toate acestea, dacă înregistrarea a fost deja aprobată, aprobatorului i se cere să aprobe retragerea și să inverseze tranzacțiile.

1. Accesați **Utilizarea materialului** și, în lista jurnalelor de utilizare a materialelor, selectați utilizarea materialului pe care doriți să o retrageți.
2. Selectați **Retragere**. Dacă intrarea de utilizare a materialului nu a fost încă aprobată, sistemul o retrage imediat. Dacă înregistrarea materialului a fost deja aprobată, se creează o cerere de retragere pentru a notifica aprobatorul că doriți să retrageți utilizarea materialului. Aprobatorul va confirma apoi că se poate face inversarea, iar intrarea va fi returnată.

## <a name="delete-a-material-usage-log"></a>Ștergeți un jurnal de utilizare de material

Puteți șterge jurnalele de utilizare a materialelor care nu au fost trimise. Pentru a șterge un jurnal de utilizare a materialului care a fost deja trimis, trebuie mai întâi să îl retrageți.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
