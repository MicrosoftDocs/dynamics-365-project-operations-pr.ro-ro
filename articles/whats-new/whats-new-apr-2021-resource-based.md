---
title: Ce este nou în aprilie 2021 - Project Operations pentru scenarii de resurse/care nu sunt bazate pe stoc
description: Acest subiect oferă informații despre actualizările de calitate disponibile în versiunea din aprilie 2021 a Project Operations pentru scenarii bazate pe resurse/fără stoc.
author: sigitac
manager: tfehr
ms.date: 04/05/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 359d39898ed60c7253b122cb884465fbd9605e0c
ms.sourcegitcommit: 8ff9fe396db6dec581c21cd6bb9acc2691c815b0
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 04/07/2021
ms.locfileid: "5868008"
---
# <a name="whats-new-april-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Ce este nou în aprilie 2021 - Project Operations pentru scenarii de resurse/care nu sunt bazate pe stoc

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

Acest subiect se aplică următoarelor componente și versiuni Dynamics 365 Project Operations:

- Project Operations pe mediul Dataverse versiunea 4.9.0.221
- Management de proiect și contabilitate în Dynamics 365 Finance versiunea mediului 10.0.17

## <a name="features-included-in-this-release"></a>Caracteristicile incluse în această versiune

Următoarele caracteristici sunt incluse în această versiune:

- Materiale ne-stocate pentru proiecte. Capabilitățile cheie includ:
  - Estimarea și prețul materialelor ne-stocate în timpul ciclului de vânzări pentru un proiect. Pentru mai multe informații, consultați [Configurați rate de cost și vânzări pentru produse de catalog - simplificat](../pro/pricing-costing/set-up-cost-sales-rates-catalog-products.md).
  - Urmărirea utilizării materialelor ne-stocate în timpul livrării proiectului. Pentru informații suplimentare, consultați [Înregistrarea utilizării materialelor pentru proiecte și activitățile proiectului](../material/material-usage-log.md).
  - Facturarea costurilor materiale ne stocate utilizate. Pentru mai multe informații, consultați [Gestionați restanțele de facturare](../proforma-invoicing/manage-billing-backlog.md).
- Facturare bazată pe sarcini: s-a adăugat capacitatea de a asocia sarcinile proiectului cu liniile contractuale ale proiectului, supunându-le astfel aceleiași metode de facturare, frecvența facturării și clienților ca cele de pe linia contractului. Această asociație asigură facturarea, contabilitatea, estimarea veniturilor și recunoașterea corecte pentru a funcționa în conformitate cu această configurare a sarcinilor proiectului.
- API-uri noi în Dynamics 365 Dataverse permite crearea, actualizarea și ștergerea operațiunilor cu **Planificarea entităților**. Pentru mai multe informații, consultați [Utilizați API-uri de programare pentru a efectua operațiuni cu entități de planificare](../project-management/schedule-api-preview.md).

## <a name="quality-updates"></a>Actualizări de calitate

### <a name="project-operations-in-dynamics-365-dataverse"></a>Project Operations în Dynamics 365 Dataverse

| **Zonă de caracteristici** | **Număr de referință** | **Actualizare de calitate** |
| --- | --- | --- |
| Facturarea și stabilirea prețurilor | 2124532 | Butonul **Factura corectă** este afișat pe o factură proforma atunci când suma de reținere sau suma de reținere aplicată este prezentă pe factura originală. Butonul este afișat numai pentru medii cu versiunea financiară 10.0.19 sau mai recentă. |
| Facturarea și stabilirea prețurilor | 2224568 | S-a adăugat logică pentru a permite particularizări care implică invocarea insertului de confirmare a facturii. |
| Facturarea și stabilirea prețurilor | 2101098 | Am îmbunătățit logica câmpurilor implicite pentru a factura proforma: **Adresa de facturare**, **Nume Facturare către**, și **Termeni de plată** acum implicit din înregistrarea clientului contractului de proiect corespunzător. |
| Facturarea și stabilirea prețurilor | 2021413 | Actualizat câmpurile **Costul actual** și **Vânzări** de pe entitatea **Activitate** să includă valorile vânzărilor din cheltuielile nefacturate și facturate pe activități. |
| Facturarea și stabilirea prețurilor | 2182110 | La copierea unui contract de proiect, ID-ul liniei contractului este regenerat în contractul de proiect de destinație pentru a se asigura că este unic. |
| Managementul oportunităților | 2186741 | S-au adăugat validări pentru a asigura că câmpurile **Origine** și **Tipul tranzacției** nu pot fi actualizate la detaliile existente despre linia de ofertă. |
| Managementul oportunităților | 2191353 | Jaloanele nu trebuie create pe o linie contractuală de timp și material. |
| Managementul oportunităților | 2216956 | S-au rezolvat problemele cu **Actualizați prețurile**. |
| Planificare și urmărire | 2182979 | Funcția de copiere a proiectului a fost îmbunătățită pentru a se asigura că liniile de estimare a cheltuielilor sunt copiate din proiectul original. |
| Planificare și urmărire | 2184144 | Funcția de copiere a proiectului a fost îmbunătățită pentru a se asigura că numele poziției resursei este copiat din proiectul original. |
| Planificare și urmărire | 2184799 | Copiere proiect: control strâns pentru a se asigura că data estimată de începere nu poate fi modificată în timp ce copierea este în curs. |
| Planificare și urmărire | 2185134 | Copie proiect: Data estimată de începere a proiectului este setată la data de astăzi. |
| Planificare și urmărire | 2196373 | Copie proiect: asigurați-vă că înregistrările managerului de proiect și ale membrilor echipei nu sunt duplicate în echipa proiectului. |
| Planificare și urmărire | 2211833 | Copierea proiectului: Alocările resurselor sunt copiate din sarcina proiectului sursă în proiectul destinație. |
| Planificare și urmărire | 2186541 | S-au rezolvat problemele din grila **Estimări** la gruparea după resurse. |
| Planificare și urmărire | 2166906 | Categoria tranzacției dintr-o activitate trebuie copiată în entitatea **Alocarea resurselor**. |
| Gestionarea de resurse | 2125362 | S-au rezolvat problemele legate de crearea unui membru generic al echipei folosind o metodă de alocare bazată pe ore. |
| Timp și cheltuială | 2113603 | S-a remediat problema legată de personalizare prin eliminarea atributelor din pagina **Intrare în timp**. Sistemul verifică acum dacă atributul există pe pagină înainte de a le accesa utilizând un script. |
| Timp și cheltuială | 2204377 | Fișele de timp copiate trebuie să se afișeze automat atunci când selectați **Copiați săptămâna** în timpul intrării în timp. |
| Timp și cheltuială | 2209059 | Câmpul **Stare** poate fi editat pentru intrări de timp Dynamics 365 Field Service. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Management de proiect și contabilitate în Dynamics 365 Finance

| **Zonă de caracteristici** | **Număr de referință** | **Actualizare de calitate** |
| --- | --- | --- |
| Management de proiect și contabilitate | [491941](https://fix.lcs.dynamics.com/Issue/Details/?bugId=491941) | Eliminarea inversă a estimării nu funcționează în **Periodic**.  |
| Management de proiect și contabilitate | [509773](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509773) | Caracteristica **Ajustare contabilă** creează o problemă cu conturile de registru care au **Nu permiteți introducerea manuală** selectată. |
| Management de proiect și contabilitate | [510728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=5109728) | S-a adăugat logica de afaceri pentru procesarea facturilor de corecție, inclusiv suma de rezervă sau suma de rezervă aplicată. |
| Management de proiect și contabilitate | [514364](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514364) | WIP-înregistrarea valorii vânzărilor în facturarea proiectelor inter-companii alege un cont neașteptat. |
| Management de proiect și contabilitate | [521807](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521807) | Când lucrați cu agenții de reținere în Project Operations, modificarea proiectului implicit pe un contract după facturarea plăților în avans cauzează probleme ulterioare cu deduceri primite. |
| Management de proiect și contabilitate | [527319](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527319) | În Project Operations, eliminarea unui proiect dintr-un contract ar trebui să reseteze proiectul implicit al contractului, dacă este necesar. |
| Management de proiect și contabilitate | [528212](https://fix.lcs.dynamics.com/Issue/Details/?bugId=528212) | În Project Operations, liniile de cheltuieli greșite apar în lista **Adăugați linie** pe factura între companii. |
| Management de proiect și contabilitate | [543968](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543968) | În Project Operations, pagina **Contract de achiziție** nu este vizibilă în entitățile juridice financiare care sunt integrate cu Project Operations. |
| Management de proiect și contabilitate | [545878](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545878) | Din cauza unei erori de integrare Dataverse, nu puteți converti o ofertă în câștigat în Project Operations. |
| Management de proiect și contabilitate | [547440](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547440) | **ProjCDSProjectContractEntity** poate seta adresa facturii sursă de finanțare de la un alt client.  |
| Management de proiect și contabilitate | [557376](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557376) | În Project Operations, nu sunt selectate dimensiuni atunci când creați o factură de înregistrare pentru o tranzacție. |
| Călătorii și cheltuială | [441256](https://fix.lcs.dynamics.com/Issue/Details/?bugId=441256) | Soldul avansului de numerar nu este actualizat pentru un raport de cheltuieli, dacă este aprobat și înregistrat rând cu rând. |
| Deplasări și cheltuieli | [482041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482041) | Impozitele pentru rapoartele de cheltuieli între companii detaliate nu sunt calculate corect. |
| Deplasări și cheltuieli | [483469](https://fix.lcs.dynamics.com/Issue/Details/?bugId=483469) | Câmpurile suplimentare legate de proiecte sunt afișate în pagina **Rapoarte de cheltuieli între companii** reimaginată. |
| Deplasări și cheltuieli | [486592](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486592) | Apare un mesaj de eroare incorect pe chitanțele antetului rapoartelor de cheltuieli. |
| Deplasări și cheltuieli | [487971](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487971) | Un raport de cheltuieli este înregistrat incorect într-un scenariu între companii dacă taxa de vânzări este înregistrată entității juridice de destinație. |
| Deplasări și cheltuieli | [505696](https://fix.lcs.dynamics.com/Issue/Details/?bugId=505696) | Datele de trimitere a rapoartelor nu sunt tipărite în rapoartele de cheltuieli aprobate. |
| Deplasări și cheltuieli | [508726](https://fix.lcs.dynamics.com/Issue/Details/?bugId=508726) | Câmpurile **Data aprobării** și **Data respinsă** nu sunt completate după aprobarea unei cheltuieli. |
| Deplasări și cheltuieli | [509913](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509913) | O cerere de călătorie creată pentru un lucrător poate fi utilizată pentru raportul de cheltuieli al altui lucrător. |
| Deplasări și cheltuieli | [518186](https://fix.lcs.dynamics.com/Issue/Details/?bugId=518186) | Categoriile de cheltuieli sunt blocate la adăugarea unei noi linii de cheltuieli. |
| Deplasări și cheltuieli | [520914](https://fix.lcs.dynamics.com/Issue/Details/?bugId=520914) | Detalierea unui rând de raport de cheltuieli deja împărțit duce la o înregistrare incompletă a voucherului Conturi furnizori\Registru general și împiedică Exploratorul sursei contabile deoarece **TRVEXPTRANS.SOURCEDOCUMENTLINE** este duplicat. |
| Deplasări și cheltuieli | [521943](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521943) | Politica de solicitare a călătoriei nu funcționează conform așteptărilor. |
| Deplasări și cheltuieli | [522567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522567) | Numele contului furnizorului nu apare pe tranzacțiile de proiect afișate pentru rapoartele de cheltuieli. |
| Deplasări și cheltuieli | [525106](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525106) | În Project Operations, nu puteți aproba timpul cu o sarcină pentru un proiect inter-companie. |
| Deplasări și cheltuieli | [526336](https://fix.lcs.dynamics.com/Issue/Details/?bugId=526336) | Categoria de returnare a avansului de numerar nu actualizează soldurile anticipate de numerar atunci când sunt înregistrate. |
| Deplasări și cheltuieli | [527218](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527218) | Prețul de vânzare este calculat incorect pe rapoartele de cheltuieli care au fost create într-o monedă străină folosind tranzacții cu cardul de credit importate și care sunt asociate cu un proiect. |
| Deplasări și cheltuieli | [542927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=542927) | A dezinstalat entitatea de date **TrvRequisitionLine** și indexul unic asociat. |
| Deplasări și cheltuieli | [543239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543239) | S-au adăugat instrumente la generați **SOURCEDOCUMENTLINE**. |
| Deplasări și cheltuieli | [544323](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544323) | Jurnalul subregistru greșit este arătat într-un scenariu între companii dacă taxa de vânzări este înregistrată entității juridice de destinație. |
| Deplasări și cheltuieli | [546877](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546877) | În Project Operations, estimările cheltuielilor nu sunt șterse din Finanțe atunci când sunt șterse din Dataverse. |
| Deplasări și cheltuieli | [550575](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550575) | Când o categorie de cheltuieli este o categorie care nu face parte din proiect, dimensiunile financiare selectate pe pagina **Cheltuieli** nu sunt copiate în raportul de cheltuieli. |
