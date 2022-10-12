---
title: Ce este nou în septembrie 2022 - Project Operations pentru scenarii de resurse/care nu sunt bazate pe stoc
description: Acest articol oferă informații despre actualizările de calitate care sunt disponibile în versiunea Microsoft din septembrie 2022 Dynamics 365 Project Operations pentru scenarii bazate pe resurse/neaprovizionate.
author: ramagadu
ms.date: 09/28/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: ef8b4dd98d64dac1e2420f8e6a104258f126f112
ms.sourcegitcommit: a2d720ac6d7ddb20a0967fe87992a376b2478208
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/04/2022
ms.locfileid: "9621349"
---
# <a name="whats-new-september-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Ce este nou în septembrie 2022 - Project Operations pentru scenarii de resurse/care nu sunt bazate pe stoc

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

Acest articol se aplică următoarelor componente și versiuni ale Microsoft Dynamics 365 Project Operations:

- Operațiuni de proiect în a Dataverse versiunea de mediu 4.46.0.60
- Management de proiect și contabilitate într-un mediu Dynamics 365 Finance versiunea 10.0.29

## <a name="features-included-in-this-release"></a>Caracteristicile incluse în această versiune

| Zonă de caracteristici | Numele caracteristicii | Mai multe informații |
| --- | --- | --- |
| Managementul oportunităților | **Revizuirea și activarea cotațiilor**<br>Project Operations oferă suport deplin al procesului de vânzări. Ofertele de proiect pot fi activate pentru a reprezenta o stare în care oferta este doar pentru citire și este în curs de revizuire. Citatele activate pot fi revizuite pentru a crea ghilimele noi care au un număr de revizuire incrementat. Cotațiile de proiecte activate sau revizuirile de cotații pot fi închise ca câștigate sau pierdute. | [Activarea și revizuirea unei oferte de proiect](/dynamics365/project-operations/sales/activation-and-revision) |
| Facturarea și stabilirea prețurilor | **Prețul agnostic al fusului orar este implicit**<br>Project Operations a introdus conceptul unei date agnostice de fus orar pe toate datele reale ale proiectului. Un domeniu nou, **Data tranzacției**, este acum disponibil pe liniile jurnalului și pe valorile reale și va fi folosit pentru a stoca data la care a avut loc tranzacția, dar fără a converti data respectivă în Ora universală coordonată. Această dată va fi utilizată pentru procesele din aval, cum ar fi stabilirea implicită a prețurilor și crearea facturii. | <p>[Determinați ratele de cost pentru estimările și valorile reale bazate pe proiecte](/dynamics365/project-operations/pricing-costing/cost-price-resolution)</p><p>[Determinați prețurile de vânzare pentru estimări și valori reale bazate pe proiecte](/dynamics365/project-operations/pricing-costing/sales-price-resolution)</p> |
| Facturarea și stabilirea prețurilor | **Prețurile efective de date în operațiunile de proiect**<br>Depășirile de preț efective în funcție de dată oferă o modalitate de a modifica sau de a modifica prețurile specifice din lista de prețuri. | [Prețurile efective de date](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Subcontractare | **Subcontractare și reconciliere facturi furnizor**<br>Această caracteristică permite clienților să creeze subcontracte pentru a achiziționa timp de resurse, categorii de cheltuieli și materiale care sunt utilizate pentru lucrul la proiect. De asemenea, permite clienților să înregistreze, în aplicațiile financiare și operaționale, facturile furnizorilor care vor fi disponibile pentru managerii de proiect în Dataverse pentru verificare. | <p>[Managementul subcontractelor](/dynamics365/project-operations/pro/subcontracting/managing-subcontracts-overview)</p><p>[Crearea facturilor de furnizor](/dynamics365/project-operations/procurement/vendor-invoicing-concept-and-creation)</p> |
| Timp și cheltuială | **Aprobator global**<br>Această caracteristică permite furnizorul independent de software (ISV) și aprobarea centralizată, indiferent de statutul de membru al proiectului sau al echipei din proiect. | [Securitate și aprobări](/dynamics365/project-operations/approvals/approvals-security) |
| Gestionarea cheltuielilor | **Posibilitatea de a înregistra datoria de cheltuieli în moneda vânzătorului**<br>Această caracteristică permite ca rapoartele de cheltuieli să fie postate într-o monedă a furnizorului pentru metoda de plată în numerar. | [Posibilitatea de a înregistra datoria de cheltuieli în moneda vânzătorului](/dynamics365/project-operations/expense/posting-expense-reports#enable-the-ability-to-post-expense-liability-in-vendor-currency-for-cash-payment-method-feature) |
| Achiziții de proiecte | **Plătiți atunci când plătiți plățile furnizorului**<br>Această caracteristică permite ca funcția Plătește atunci când este plătită (PWP) să fie utilizată cu medii fără stoc de Operațiuni de proiect. Permite blocarea/reținerea plăților vânzătorului, pe baza termenilor de păstrare, până când plata este primită de la client. | [Plătiți atunci când plătiți plățile furnizorului](/dynamics365/project-operations/procurement/pay-when-paid) |
| Achiziții de proiecte | **Cereri de achiziție de proiecte**<br>Această caracteristică permite utilizatorilor să creeze comenzi de achiziție legate de proiecte în entitățile juridice în care este activată Operațiunile de proiect pe integrarea Dynamics 365 Customer Engagement. Comenzile de achiziție ale proiectului pot fi utilizate pentru a înregistra achizițiile de materiale nestocizate în raport cu proiectul de către personalul departamentului de achiziții. Comenzile de achiziție pentru proiecte nu vor fi sincronizate cu Dataverse. Cu toate acestea, puteți utiliza o entitate virtuală pentru a afișa liniile de comandă de achiziție ale Proiectului Dataverse pentru informații despre managerul de proiect. Costul facturii furnizorului legat de proiect este integrat cu entitatea Project Actuals în Dataverse. Costul proiectului este înregistrat în registrul secundar al proiectului utilizând jurnalul de integrare a operațiunilor de proiect. | |

## <a name="project-operations-dual-write-maps-updates"></a>Actualizări de hărți Project Operations cu scriere duală

Următorul tabel prezintă hărțile cu dublă scriere care au fost modificate sau adăugate în versiunea din septembrie 2022 a Project Operations.

| Maparea entității | Versiune actualizată | Comentarii |
| -------------- | ------------------- | ------------|
| Integrare valori reale Project Operations (msdyn_actuals) | 1.0.0.15 | Această hartă acceptă procesarea subcontractelor reale cu Operațiuni de proiect pentru scenarii bazate pe resurse. |
| Entitatea privind exportul facturilor de la furnizori în proiectul de integrare Project Operations (msdyn_projectvendorinvoices) | 1.0.0.2 | Această hartă acceptă procesarea subcontractelor reale cu Operațiuni de proiect pentru scenarii bazate pe resurse. |
| Entitatea privind exportul liniilor de factură de la furnizori în proiectul de integrare Project operations (msdyn_projectvendorinvoicelines) | 1.0.0.5 | Această hartă acceptă procesarea subcontractelor reale cu Operațiuni de proiect pentru scenarii bazate pe resurse. |

Rulați întotdeauna cea mai recentă versiune a hărții în mediul dvs. și activați toate hărțile de tabel asociate pe măsură ce actualizați operațiunile de proiect Dataverse soluție și versiunea soluției financiare. Este posibil ca unele funcții și capabilități să nu funcționeze corect dacă cea mai recentă versiune a hărții nu este activată. Puteți vizualiza versiunea activă a hărții în coloana **Versiune** de pe pagina **Scriere duală**. Pentru a activa o nouă versiune a hărții selectați **Versiuni ale hărții cu tabele**, selectați cea mai recentă versiune și apoi salvați versiunea selectată. Dacă ați personalizat o hartă a tabelului out-of-box, aplicați din nou modificările. Pentru mai multe informații, consultați: [Gestionarea ciclului de viață al aplicațiilor](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Dacă întâmpinați o problemă când porniți harta, urmați instrucțiunile din [Problemă cu coloanele din tabel lipsă pe hărți](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) secțiunea din ghidul de depanare cu scriere dublă.

## <a name="quality-updates"></a>Actualizări de calitate

### <a name="project-operations-on-dataverse"></a>Project Operations pe Dataverse

| Zonă de caracteristici | Număr de referință | Actualizare de calitate |
| --- | --- | --- |
| Facturarea și stabilirea prețurilor | 2754422 | Estimările de materiale și cheltuieli nu ajung la Finanțe atunci când proiectele sunt copiate Dataverse. |
| Timp și cheltuială | 2787409 | Un autorizator nevalid poate aproba o intrare de timp non-proiect. |
| Managementul oportunităților | 2788907 | Mesaj de eroare actualizat privind validarea unicității pentru liniile de comandă care includ indicatoare. |
| Timp și cheltuială | 2842253 | Gestionarea excepțiilor nulă pentru aprobarea timpului. |
| Facturarea și stabilirea prețurilor | 2844181 | Eșecul de a obține ID-ul de corelare blochează crearea facturii. |
| Facturarea și stabilirea prețurilor | 2876628 | QLD, CLD - Rezoluția estimată a listei de prețuri ar trebui să utilizeze câmpurile vechi ale intervalului de date ale listei de prețuri. |
| Subcontractare | 2893222 | Dacă nu este specificat niciun rol pentru o linie de subcontractare, ar trebui să fie posibilă selectarea acelei linii pe un membru al echipei pentru orice rol. |

### <a name="project-management-and-accounting-in-finance"></a>Management de proiect si contabilitate in Finante

Pentru informații despre remedierea erorilor care sunt incluse în această actualizare, conectați-vă la Microsoft Dynamics Lifecycle Services și vizualizați [articol KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=726559).

## <a name="features-turned-on-by-default-in-upcoming-release"></a>Funcțiile sunt activate în mod prestabilit în versiunea viitoare

Următorul tabel listează caracteristicile care sunt activate implicit în versiunea 10.0.30. Majoritatea funcțiilor care au fost activate automat pot fi dezactivate în [Managementul caracteristicilor](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview). În viitor, unele funcții care au fost activate automat ar putea fi eliminate din Gestionarea caracteristicilor și devin obligatorii. Această modificare asigură că clienții folosesc funcționalitatea actuală, astfel încât îmbunătățirile se pot construi pe funcționalitatea curentă pe măsură ce sunt adăugate. Funcțiile nu vor fi niciodată activate automat în mai puțin de un an, cu excepția cazului în care se consideră că sunt esențiale.

| Numele caracteristicii | Activați data | Funcție adăugată | Stare caracteristică | Modul |
| --- | --- | --- |--- |--- |
| Activați operația asincronă atunci când utilizatorul trebuie să comute între operațiunile de sincronizare și asincrone | 21 Octombrie 2022 | 9 aprilie 2021 | Activat implicit | Gestionarea cheltuielilor |
| Este necesară evaluarea politicii de cheltuieli pentru încasări | 21 Octombrie 2022 | 20 decembrie 2021 | Activat implicit | Gestionarea cheltuielilor |
| Vizualizare listă a rapoartelor de cheltuieli create prin delegarea lucrătorilor | 21 Octombrie 2022 | 19 februarie 2020 | Activat implicit | Gestionarea cheltuielilor |
| Calcul total al kilometrajului de către exercițiu financiar | 21 Octombrie 2022 | 10 mai 2022 | Activat implicit | Gestionarea cheltuielilor |
