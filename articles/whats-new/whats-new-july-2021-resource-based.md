---
title: Noutăți iulie 2021 - Project Operations pentru scenarii bazate pe stocuri/producție
description: Acest subiect oferă informații despre actualizările de calitate disponibile în versiunea Project Operations din iulie 2021 pentru scenarii bazate pe stocuri/producție.
author: sigitac
ms.date: 07/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5dbf9c7158ce7d9e568e270791e7e7aaf8ce731d
ms.sourcegitcommit: 3abf1e67938d91bd826b025ae3187cd313f556b9
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 07/07/2021
ms.locfileid: "6433533"
---
# <a name="whats-new-july-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Noutăți iulie 2021 - Project Operations pentru scenarii bazate pe stocuri/producție

*Se aplică la: Project Operations pentru scenarii bazate pe resurse/fără stoc*

Acest subiect se aplică următoarelor componente și versiuni Dynamics 365 Project Operations:

   - Project Operations în mediul Microsoft Dataverse versiunea 4.12.0.148.
   - Management de proiect și contabilitate în mediul Dynamics 365 Finance versiunea 10.0.20.

## <a name="features-included-in-this-release"></a>Caracteristicile incluse în această versiune

Următoarele caracteristici sunt incluse în această versiune:

- Abilitatea administratorilor de a vizualiza jurnalele PSS și jurnalele Setări operațiuni din meniul de setări. Jurnalele sunt stocate timp de 90 de zile.

## <a name="project-operations-dual-write-maps-updates"></a>Actualizări de hărți Project Operations cu scriere duală

Nu există actualizări pentru hărțile cu dublă scriere Project Operations în această versiune.

Pentru o listă actuală și versiuni ale hărților cu scriere duală Project Operations, consultați [Versiuni de hartă cu scriere duală Project Operations](../environment/resource-dual-write-maps.md).

Rulați întotdeauna cea mai recentă versiune a hărții în mediul dvs. și activați toate hărțile de tabel aferente pe măsură ce vă actualizați soluția Dataverse în Project Operations și versiunea de soluție financiară. Este posibil ca anumite caracteristici și capabilități să nu funcționeze corect dacă cea mai recentă versiune a hărții nu este activată. Puteți vedea versiunea activă a hărții pe pagina **Scriere duală** în coloana **Versiune**. Activați o nouă versiune a hărții selectând **Versiunile hărții tabel**, selectând cea mai recentă versiune și apoi salvând versiunea selectată. Dacă ați personalizat o hartă a tabelului predefinită, aplicați din nou modificările. Pentru mai multe informații, consultați: [Gestionarea ciclului de viață al aplicațiilor](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Dacă întâmpinați o problemă în lansarea hărții, urmați instrucțiunile din secțiunea [Problemă legată de coloanele lipsă în tabel pe hărți](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) din Ghidul de depanare pentru scriere duală.

## <a name="quality-updates"></a>Actualizări de calitate

### <a name="project-operations-on-dataverse"></a>Project Operations pe Dataverse

| **Zonă de caracteristici**              | **Număr de referință** | **Actualizare de calitate**                                                                                                                                                                                             |
|-------------------------------|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Facturarea și stabilirea prețurilor           | 2224046              | Câmpul **Clasa tranzacției** este editabil pe fila **Detalii despre linia de ofertă**, dar este blocat dacă lucrați de pe pagina **Detalii despre linia de ofertă**.                                                                     |
| Facturarea și stabilirea prețurilor           | 2224400              | Acțiunea **Închidere ofertă cu starea Câștigat** eșuează atunci când o ofertă nu are repere de dată.                                                                                                                                    |
| Facturarea și stabilirea prețurilor           | 2234089              | Când introduceți manual o descriere a produsului, aceasta este ștearsă după ce introduceți o cantitate pentru o estimare a materialului.                                                                                                                         |
| Facturarea și stabilirea prețurilor           | 2234100              | Grila **Configurare facturare activități** nu include coloana **Material** și valoarea ei pe fila **Facturare activități** din proiect.                                                                                                       |
| Facturarea și stabilirea prețurilor           | 2277409              | ID-ul produsului nu este disponibil pe detaliile liniei de contract pentru o linie de tip material.                                                                                                                                        |
| Facturarea și stabilirea prețurilor           | 2281728              | Crearea unei linii de contract reevaluează inutil datele reale, provocând creșteri semnificative ale volumului de date, ceea ce afectează performanța.                                                                                |
| Facturarea și stabilirea prețurilor           | 2298668              | Liniile din jurnal asociate cu o cheltuială retrasă și ștearsă nu sunt eliminate.                                                                                                                                     |
| Facturarea și stabilirea prețurilor           | 2300192              | Atunci când mai mulți utilizatori editează o factură, este posibil să se creeze un nou detaliu de linie de factură pe o factură confirmată.                                                                                   |
| Facturarea și stabilirea prețurilor           | 2301569              | Facturile nu pot fi corectate dacă s-a aplicat o sumă de siguranță \$0.                                                                                                                                        |
| Facturarea și stabilirea prețurilor           | 2307965              | Apare o eroare dacă se creează un preț de categorie cu valori lipsă.                                                                                                                           |
| Facturarea și stabilirea prețurilor           | 2326870              | Apare o eroare în **Microsoft.Dynamics.ProjectService.Plugins.PostInvoiceLineDelete** dacă valoarea **producttypecode** este nulă.                                                                            |
| Facturarea și stabilirea prețurilor           | 2332732              | Apare o eroare dacă se creează o etapă a liniei de contract fără o linie de comandă.                                                                                                                |
| Planificare și urmărire de proiect | 2181094              | API-ul de planificare a proiectului acceptă acum jurnalele PSS și jurnalele setului de operațiuni, care sunt stocate timp de 90 de zile.                                                                                                                  |
| Planificare și urmărire de proiect | 2254201              | Eticheta **Mod de planificare** este actualizată cu detalii care descriu logica implicită.                                                                                                                                      |
| Planificare și urmărire de proiect | 2300252              | Memoria cache de răspuns **openProject** este actualizată și include proprietarul tokenului în cheia cache, **URL-ul de bază** și **Segment URL** astfel încât **Solicitare URL** să poată fi întotdeauna recreat dacă se modifică **URL-ul de bază**. |
| Planificare și urmărire de proiect | 2301312              | **msdyn_membershipstatus** a fost eliminat din vizualizarea **Membru echipă de proiect**.                                                                                                                                        |
| Planificare și urmărire de proiect | 2302759              | Produsele sunt preluate inutil pe filele **Atribuiri de resurse**, **Estimări** și **Estimări de cheltuieli**.                                                                                                        |
| Planificare și urmărire de proiect | 2308050              | **CopyProject** eșuează și afișează eroarea „Nu s-a reușit obținerea tokenului pentru a comunica cu serviciul de la distanță”.                                                                                                                           |
| Planificare și urmărire de proiect | 2322650              | Vizualizarea **Lista sarcinilor proiectului** a fost actualizată pentru a afișa în mod implicit data sarcinii.                                                                                                            |
| Planificare și urmărire de proiect | 2327266              | **CopyProject** generează eroarea „Cheia nu a fost găsită în dicționar” la copierea estimărilor.                                                                                                      |
| Planificare și urmărire de proiect | 2328123              | **CopyProject** generează eroarea „Nu s-a reușit obținerea tokenului pentru a comunica cu serviciul de la distanță”.                                                                                                                          |
| Planificare și urmărire de proiect | 2336258              | **CopyProject** copiază incorect numele pozițiilor resurselor.                                                                                                                                                 |
| Facturarea și stabilirea prețurilor           | 2224476              | Câmpul **Resursă rezervabilă** nu este setat implicit corect pentru utilizatorul conectat de pe pagina **Utilizare material**.                                                                                                            |
| Gestionarea de resurse           | 2277249              | Apare o eroare atunci când este actualizată o cerință de resurse care nu este bazată pe proiect.                                                                                                            |
| Gestionarea de resurse           | 2323869              | Utilizarea resurselor nu recunoaște corect resursele filtrate.                                                                                                                                             |
| Timp și cheltuială              | 2176538              | Operatorii de filtru incorecte sunt aplicați la comanda **Intrare de timp**.                                                                                                                                                   |
| Timp și cheltuială              | 2177462              | Ștergerea unei intrări de timp în grilă nu actualizează starea butonului **Trimitere**, **Retragere**, **Ștergere**, și **Editare intrare** așa cum era de așteptat.                                                                                        |
| Timp și cheltuială              | 2299985              | **TimeEntriesImportFromResourceAssignment** nu păstrează ora de început/sfârșit de la contururile atribuirii.                                                                                                  |
| Timp și cheltuială              | 2318426              | După trimiterea unei intrări de timp, câmpurile blocate pot fi în continuare editate.                                                                                                                                   |
| Timp și cheltuială              | 2323749              | Apare o eroare atunci când se creează o cheltuială din fila **Corelate** a unei resurse rezervabile.                                                                                                      |
| Timp și cheltuială              | 2327678              | Când creați o intrare de timp din fila **Corelate** a unei resurse rezervabile, resursa principală nu este trecută la comanda de intrare de timp.                                                                            |
| General                       | 2296857              | Urmărirea progresului pentru operațiuni lungi în curs.                                                                                                                                                                        |
| General                       | 2253682              | Soluția de scriere duală Project Operations nu ar trebui instalată atunci când nucleul de scriere duală este instalat într-un mediu fără soluția de orchestrare cu scriere duală.                                                |
| General                       | 2316420              | Asigurarea accesului de bază la Project Service eșuează dacă se schimbă unitatea de business a utilizatorului aplicației.                                                                                                                     |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Management de proiect și contabilitate pe Dynamics 365 Finance

| Zonă de caracteristici                      | Număr de referință | Actualizare de calitate                                                                                                                                                                                                                                                                                                                |
|-----------------------------------|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Management de proiect și contabilitate | 4620267          | Nu puteți personaliza formularele pentru a adăuga un câmp **Scop** pe paginile **Tranzacție de proiect postată**, **Crearea propunerii de factură** și **Propunere de factură**.                                                                                                                                                                                         |
| Management de proiect și contabilitate | 4613449          | Când selectați un ID de contract de proiect în Finanțe, mediul integrat Project Operations deschide pagina pentru a crea o nouă înregistrare în loc să deschidă pagina pentru contracte de proiect existente.                                                                                                                                           |
| Management de proiect și contabilitate | 4614445          | În implementarea scenariului integrat Project Operations, nu puteți edita câmpul **Grup de taxe pe vânzări de articole** din propunerea de facturare importată din etapizare. Grupul de taxe pe vânzări de articole ar trebui să poată fi editabil pentru o propunere de factură deschisă de toate tipurile de tranzacții, inclusiv pentru cont, ore, cheltuieli, taxe și articole. |
| Management de proiect și contabilitate |                  | O propunere de factură care rezultă dintr-o corecție negativă a tranzacției în timp nu poate fi postată.                                                                                                                                                                                                                                              |
| Management de proiect și contabilitate |                  | Liniile de propunere de factură sunt duplicate din cauza mai multor instanțe ale procesului periodic **Import din etapizare** care rulează în același timp.                                                                                                                                                                                                                |

