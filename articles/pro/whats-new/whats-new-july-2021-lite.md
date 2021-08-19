---
title: Noutăți în iulie 2021 - implementare simplificată Project Operations
description: Acest subiect oferă informații despre actualizările de calitate disponibile în versiunea Project Operations de implementare simplificată din iulie 2021.
author: sigitac
ms.date: 07/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 8cff4c37e1c2df29041ef86cdcf05afa6093f890565a855024202e87fd533ea5
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/06/2021
ms.locfileid: "7009231"
---
# <a name="whats-new-july-2021---project-operations-lite-deployment"></a>Noutăți în iulie 2021 - implementare simplificată Project Operations

_Se aplică pentru: implementare simplificată - înțelegere la emiterea facturii proforme_

Acest subiect se aplică următoarelor componente și versiuni Dynamics 365 Project Operations:

  - Project Operations în mediul Dataverse versiunea 4.12.0.148 sau 4.12.0.152.

## <a name="quality-updates"></a>Actualizări de calitate
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
| General                       | 2376405              | S-a remediat problema de actualizare bazată pe editor (Actualizarea de calitate este disponibilă în versiunea 4.12.0.152)                                                                                                                     |
