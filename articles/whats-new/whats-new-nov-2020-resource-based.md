---
title: Ce este nou în noiembrie 2020 - Project Operations pentru scenarii de resurse/care nu sunt bazate pe stoc
description: Acest subiect oferă informații despre actualizările de calitate disponibile în lansarea din noiembrie 2020 Project Operations pentru scenarii bazate pe resurse/care nu sunt bazate pe stoc.
author: sigitac
manager: Annbe
ms.date: 10/30/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: f8e9bce6612e617785264470b7946ffc4795a621
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291859"
---
# <a name="whats-new-november-2020---project-operations-for-resourcenon-stocked-based-scenarios"></a>Ce este nou în noiembrie 2020 - Project Operations pentru scenarii de resurse/care nu sunt bazate pe stoc

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

Acest subiect se aplică următoarelor componente și versiuni Dynamics 365 Project Operations:

- Project Operations pe mediu CDS versiunea 4.4.0.70
- Management de proiect și contabilitate în Dynamics 365 Finance versiunea mediului 10.0.14

## <a name="updates-to-project-operations-for-resource-non-stocked-based-scenarios"></a>Actualizări la Project Operations pentru scenarii de resurse/care nu sunt bazate pe stoc

### <a name="project-operations-on-cds"></a>Project Operations pe CDS

| Zonă de caracteristici                 | Număr de referință | Actualizare de calitate                                                                                                                                                                    |
|------------------------------|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   Managementul oportunităților       | 2036993          | Linia estimativă și liniile contractului de atribuire a resurselor sunt actualizate la ofertele câștigătoare atunci când tipul de linie a cotației este **Toate activitățile**.                                                 |
| Facturarea și stabilirea prețurilor          | 2070392          | Liniile contractului de proiect de pe factură cresc de fiecare dată când este selectat **Reîmprospătați tranzacțiile de facturi**.                                                                         |
| Planificarea unui proiect             | 2043336          | Imposibil de șters o înregistrare de membru al echipei de proiect.                                                                                                                                  |
| Planificarea unui proiect             | 2046013          | Comportament neconcordant pentru coloanele etichetei Estimări în timpul încărcării față de schimbarea tipului de fază temporală.                                                                                   |
| Planificarea unui proiect             | 2046647          | Orele de început și de sfârșit sunt oprite cu o oră când cerințele de resurse sunt generate de membrii echipei de proiect.                                                                      |
| Planificarea unui proiect             | 2053879          | (Conform lansării CDS viitoare) PublishUnassignedAssignments întrerupe o încercare de salvare a unei sarcini atunci când eroarea „Valoarea trecută pentru ConditionOperator.In este goală”.                       |
| Planificarea unui proiect             | 2055501          | Lăsarea **Data de începere a proiectului** goală provoacă o eroare în planificare.                                                                                                      |
| Planificarea unui proiect             | 2066817          | Nu se poate crea o resursă generică utilizând selectorul de persoane de pe fila **Activități**.                                                                                                   |
| Planificarea unui proiect             | 2067034          | Butonul **Vizualizare detalii** nu este disponibil pe pagina **Detalii despre activitate**.                                                                                                       |
| Gestionarea resurselor          | 2046667          | Membrii echipei generice nu sunt șterși chiar și după ce toate resursele sunt îndeplinite.                                                                                                    |
| Intrare de timp și cheltuială rapidă | 2047499          | Butonul **Nou** de pe pagina de introducere a timpului deschide pagina **Semnătură de e-mail nouă**.                                                                                               |
| Intrare de timp și cheltuială rapidă | 2059859          | Fereastra pop-up neașteptată se deschide la crearea unei intrări de cheltuieli.                                                                                                                         |
| Altceva                        | 2044181          | (Dezinstalarea comenzii de achiziție)   când încercați să dezinstalați soluțiile de bază ale serviciului msdyn_ProjectServiceCore_Patch și msdyn Project Service apare eroarea „Înregistrarea nu este disponibilă”.  |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Management de proiect și contabilitate în Dynamics 365 Finance

| Zonă de caracteristici        | Număr de referință | Actualizare de calitate                                                                                                                                                            |
|---------------------|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Recunoașterea veniturilor | [451662](https://fix.lcs.dynamics.com/Issue/Details/?bugId=451662)           | Procentul estimat de proiect finalizat este greșit atunci când contractul folosește o monedă străină și procentul de progres al lucrării pentru metoda completă.                     |
| Recunoașterea veniturilor | [469894](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469894)           | Imposibil de publicat estimări cu metoda de finalizare **Costul actual**.                                                                                                    |
| Recunoașterea veniturilor | [485439](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485439)           | Eliminarea eșuează din cauza unei erori de dezechilibru a voucherului atunci când moneda companiei și moneda tranzacției sunt diferite.                                              |
| Gestionarea cheltuielilor  | [456882](https://fix.lcs.dynamics.com/Issue/Details/?bugId=456822)           | Pentru utilizatorii care nu sunt administratori, valorile de căutare pentru coloanele de linie de cheltuieli, cum ar fi **ID-ul proiectului** și **Categoria de cheltuieli** nu se afișează corect în cadrul conectorului de date. |
| Gestionarea cheltuielilor  | [469300](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469300)           | Valoarea implicită a proprietății de linie nu este afișată pentru categoriile de cheltuieli.                                                                                                         |
| Gestionarea cheltuielilor  | [469302](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469302)           | Integrarea cheltuielilor trebuie să includă proprietatea liniei din raportul de cheltuieli.                                                                                             |
| Facturare           | [462499](https://fix.lcs.dynamics.com/Issue/Details/?bugId=462499)           | Nu se pot posta propuneri de facturare a proiectului din cauza unui mesaj de eroare care spune că combinația FD nu a fost validată.                                                    |
| Facturare           | [470614](https://fix.lcs.dynamics.com/Issue/Details/?bugId=470614)           | Nu pot vizualiza tranzacțiile din pagina de detalii   **factură**.                                                                                                              |
| Facturare           | [480070](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480070)           | Liniile de propunere de factură pot fi șterse.                                                                                                                                  |
| Contabilitatea proiectului  | [470293](https://fix.lcs.dynamics.com/Issue/Details/?bugId=470293)           | Elementele de meniu **Prognoză** nu sunt vizibile pe pagina listei **Proiecte**.                                                                                                   |
| Contabilitatea proiectului  | [475873](https://fix.lcs.dynamics.com/Issue/Details/?bugId=475873)           | Nu se poate deschide **Declarația proiectului**   > **Tranzacții și prognoză**.                                                                                                       |
| Contabilitatea proiectului  | [475879](https://fix.lcs.dynamics.com/Issue/Details/?bugId=475879)           | **Ajustați contabilitatea** nu este activat pentru tranzacțiile de proiect facturate.                                                                                                  |
| Contabilitatea proiectului  | [480962](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480962)           | Detaliile contabile nu sunt incluse în tabelul **ProjCDSActualsImport** când este publicat jurnalul **Integrare**.                                                  |
| Contabilitatea proiectului  | [482558](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482558)           | Intrarea de prognoză a proiectului este dublată când eliminați și apoi citiți o alocare de resurse.                                                                            |
| Contabilitatea proiectului  | [502019](https://fix.lcs.dynamics.com/Issue/Details/?bugId=502019)           | Selectarea unui link ID proiect nu deschide adresa URL a linkului profund CDS.                                                                                                         |
| Contabilitatea proiectului  | [505458](https://fix.lcs.dynamics.com/Issue/Details/?bugId=505458)           | Nu se poate actualiza data de începere a unei activități din CDS.                                                                                                                           |
| Contabilitatea proiectului  | [510041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510041)           | Activând funcția, mai multe linii contractuale nu sunt posibile fără integrarea CDS.                                                                                   |

### <a name="regulatory-updates"></a>Actualizări de reglementare
Pentru informații despre actualizările de reglementare pentru aplicații Finance and Operations, vezi [Actualizări de reglementare](https://docs.microsoft.com/dynamics365/finance/localizations/regulatory-updates). De asemenea, vă puteți conecta la LCS și puteți vizualiza actualizările de reglementare planificate folosind instrumentul de căutare a problemelor. Căutarea problemelor vă permite să căutați în funcție de țară, tipul de funcție și eliberare.


[!INCLUDE[footer-include](../includes/footer-banner.md)]