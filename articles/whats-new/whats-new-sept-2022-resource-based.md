---
title: Ce este nou în septembrie 2022 - Project Operations pentru scenarii de resurse/care nu sunt bazate pe stoc
description: Acest articol oferă informații despre actualizările de calitate care sunt disponibile în versiunea de Microsoft Dynamics 365 Project Operations din septembrie 2022 pentru scenarii bazate pe resurse/care nu există pe stoc.
author: ramagadu
ms.date: 09/28/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 04b5f2f8223cdc80028860dd880dde314be244eb
ms.sourcegitcommit: b3a70bc4f2850cff5c2b7114cff7bd61ec298143
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/06/2022
ms.locfileid: "9634821"
---
# <a name="whats-new-september-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Ce este nou în septembrie 2022 - Project Operations pentru scenarii de resurse/care nu sunt bazate pe stoc

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

Acest articol se aplică următoarelor componente și versiuni de Microsoft Dynamics 365 Project Operations:

- Project Operations într-un mediu Dataverse versiunea 4.46.0.60
- Management de proiect și contabilitate într-un mediu Dynamics 365 Finance, versiunea 10.0.29

## <a name="features-included-in-this-release"></a>Caracteristicile incluse în această versiune

| Zonă de caracteristici | Denumire funcție | Mai multe informații |
| --- | --- | --- |
| Managementul oportunităților | **Revizuirea și activarea ofertelor**<br>Project Operations oferă suport deplin al procesului de vânzări. Ofertele de proiect pot fi activate pentru a reprezenta o stare în care oferta este doar pentru citire și este în curs de revizuire. Ofertele activate pot fi revizuite pentru a crea oferte noi care au un număr de revizuire incrementat. Ofertele de proiect activate sau revizuirile de oferte pot fi închise sub formă de câștigate sau pierdute. | [Activarea și revizuirea unei oferte de proiect](/dynamics365/project-operations/sales/activation-and-revision) |
| Facturarea și stabilirea prețurilor | **Prețul agnostic pentru fusul orar este implicit**<br>Project Operations a introdus conceptul unei date agnostice de fus orar pe toate valorile reale ale proiectului. Un câmp nou, **Dată tranzacție** este acum disponibil pe liniile jurnalului și pe valorile reale și va fi folosit pentru a stoca data la care a avut loc tranzacția, dar fără a converti data respectivă în Ora universală coordonată. Această dată va fi utilizată pentru procesele din aval, cum ar fi stabilirea implicită a prețurilor și crearea facturii. | <p>[Stabilirea ratelor de cost pentru estimările și valorile reale bazate pe proiect](/dynamics365/project-operations/pricing-costing/cost-price-resolution)</p><p>[Stabilirea prețurilor de vânzare pentru estimări și valori reale bazate pe proiect](/dynamics365/project-operations/pricing-costing/sales-price-resolution)</p> |
| Facturarea și stabilirea prețurilor | **Înlocuirile de prețu cu dată efectivă în Project Operations**<br>Înlocuirile de preț cu dată efectivă oferă o modalitate de a înlocui sau modifica anumite prețuri din lista de prețuri. | [Înlocuiri de preț cu dată efectivă](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Subcontractare | **Subcontractare și reconciliere facturi de furnizor**<br>Această caracteristică permite clienților să creeze subcontracte pentru a achiziționa timp de resurse, categorii de cheltuieli și materiale care sunt utilizate pentru lucrul la proiect. De asemenea, permite clienților să înregistreze, în aplicațiile financiare și operaționale, facturile furnizorilor care vor fi disponibile pentru managerii de proiect în Dataverse pentru verificare. | <p>[Gestionarea subcontractării](/dynamics365/project-operations/pro/subcontracting/managing-subcontracts-overview)</p><p>[Crearea facturilor de furnizor](/dynamics365/project-operations/procurement/vendor-invoicing-concept-and-creation)</p> |
| Timp și cheltuială | **Aprobator global**<br>Această caracteristică autorizează furnizorul independent de software (ISV) și aprobarea centralizată, indiferent de statutul proiectului sau al membrului echipei în proiect. | [Securitate și aprobări](/dynamics365/project-operations/approvals/approvals-security) |
| Gestionarea cheltuielilor | **Posibilitatea de a înregistra datoria de cheltuieli în moneda vânzătorului**<br>Această caracteristică permite ca rapoartele de cheltuieli să fie postate într-o monedă a furnizorului pentru metoda de plată în numerar. | [Posibilitatea de a înregistra datoria de cheltuieli în moneda vânzătorului](/dynamics365/project-operations/expense/posting-expense-reports#enable-the-ability-to-post-expense-liability-in-vendor-currency-for-cash-payment-method-feature) |
| Achiziții de proiecte | **Plățile de la furnizor cu plată la plată**<br>Această caracteristică permite ca funcția Plătește atunci când este plătită (PWP) să fie utilizată cu medii Project Operations care nu există pe stoc. Permite blocarea/reținerea plăților vânzătorului, pe baza termenilor de reținere, până când plata este primită de la client. | [Plățile de la furnizor cu plată la plată](/dynamics365/project-operations/procurement/pay-when-paid) |
| Achiziții de proiecte | **Cereri de achiziție de proiecte**<br>Această caracteristică permite utilizatorilor să creeze comenzi de achiziție legate de proiecte în entități juridice în care este activată integrarea Project Operations on Dynamics 365 Customer Engagement. Comenzile de achiziție ale proiectului pot fi utilizate pentru a înregistra achizițiile de materiale care nu există pe stoc în raport cu proiectul de către personalul Departamentului de achiziții. Comenzile de achiziție pentru proiecte nu vor fi sincronizate cu Dataverse. Cu toate acestea, puteți utiliza o entitate virtuală pentru a afișa liniile de comandă de achiziție ale Proiectului în Dataverse pentru informații despre managerul de proiect. Costul facturii furnizorului aferent proiectului este integrat cu entitatea Valori reale ale proiectului în Dataverse. Costul proiectului este înregistrat în registrul secundar al proiectului utilizând Jurnalul de integrare din Project Operations. | |
|Planificare și urmărire de proiect|**Utilizați API-urile de planificare a proiectelor pentru a efectua operațiuni cu entități de planificare** </br> </br>API-ul de editare a conturului de atribuire a resurselor le permite dezvoltatorilor să specifice în mod programatic efortul unui desemnat al sarcinii în orice interval de date acceptat pentru o planificare mai granulară a efortului în etape de timp.|[Utilizați API-urile de planificare a proiectelor pentru a efectua operațiuni cu entități de planificare](/dynamics365/project-operations/project-management/schedule-api-preview)|

## <a name="project-operations-dual-write-maps-updates"></a>Actualizări de hărți Project Operations cu scriere duală

Următorul tabel prezintă hărțile cu scriere duală care au fost modificate sau adăugate în Project Operations, versiunea septembrie 2022.

| Maparea entității | Versiune actualizată | Comentarii |
| -------------- | ------------------- | ------------|
| Integrare valori reale Project Operations (msdyn_actuals) | 1.0.0.15 | Această hartă acceptă procesarea subcontractelor reale cu Project Operations pentru scenarii bazate pe resurse. |
| Entitatea privind exportul facturilor de la furnizori în proiectul de integrare Project Operations (msdyn_projectvendorinvoices) | 1.0.0.2 | Această hartă acceptă procesarea subcontractelor reale cu Project Operations pentru scenarii bazate pe resurse. |
| Entitatea privind exportul liniilor de factură de la furnizori în proiectul de integrare Project operations (msdyn_projectvendorinvoicelines) | 1.0.0.5 | Această hartă acceptă procesarea subcontractelor reale cu Project Operations pentru scenarii bazate pe resurse. |

Rulați întotdeauna cea mai recentă versiune a hărții în mediul dvs. și activați toate hărțile de tabel aferente pe măsură ce vă actualizați soluția Project Operations Dataverse și versiunea de soluție Finance. Este posibil ca unele caracteristici și capabilități să nu funcționeze corect dacă cea mai recentă versiune a hărții nu este activată. Puteți vizualiza versiunea activă a hărții în coloana **Versiune** de pe pagina **Scriere duală**. Pentru a activa o nouă versiune a hărții selectați **Versiuni ale hărții cu tabele**, selectați cea mai recentă versiune și apoi salvați versiunea selectată. Dacă ați personalizat o hartă predefinită a tabelului, aplicați din nou modificările. Pentru mai multe informații, consultați: [Gestionarea ciclului de viață al aplicațiilor](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Dacă întâmpinați o problemă când porniți harta, urmați instrucțiunile din secțiunea [Problema coloanelor din tabel lipsă pe hărți](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) a ghidului de depanare Dual-write.

## <a name="quality-updates"></a>Actualizări de calitate

### <a name="project-operations-on-dataverse"></a>Project Operations pe Dataverse

| Zonă de caracteristici | Număr de referință | Actualizare de calitate |
| --- | --- | --- |
| Facturarea și stabilirea prețurilor | 2754422 | Estimările de materiale și cheltuieli nu ajung la Finance atunci când proiectele sunt copiate în Dataverse. |
| Timp și cheltuială | 2787409 | Un aprobator nevalid poate aproba o intrare de timp non-proiect. |
| Managementul oportunităților | 2788907 | Mesaj de eroare actualizat privind validarea unicității pentru liniile de comandă care includ indicatoare. |
| Timp și cheltuială | 2842253 | Gestionarea excepțiilor nule pentru aprobarea timpului. |
| Facturarea și stabilirea prețurilor | 2844181 | Eșecul de a obține ID-ul de corelare blochează crearea facturii. |
| Facturarea și stabilirea prețurilor | 2876628 | QLD, CLD - Rezoluția estimată a listei de prețuri ar trebui să utilizeze câmpurile vechi ale intervalului de date ale listei de prețuri. |
| Subcontractare | 2893222 | Dacă nu este specificat niciun rol pentru o linie de subcontractare, ar trebui să fie posibilă selectarea acelei linii pe un membru al echipei pentru orice rol. |

### <a name="project-management-and-accounting-in-finance"></a>Management de proiect și contabilitate în Finance

Pentru informații despre remedierile erorilor care sunt incluse în această actualizare, autentificați-vă în Microsoft Dynamics Lifecycle Services (LCS) și vizualizați [Articolul KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=726559).

## <a name="features-turned-on-by-default-in-upcoming-release"></a>Funcțiile activate în mod implicit în versiunea viitoare

Următorul tabel listează funcțiile care sunt activate implicit în versiunea 10.0.30. Majoritatea funcțiilor care au fost activate automat pot fi dezactivate în [Managementul caracteristicilor](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview). În viitor, unele funcții care au fost activate automat ar putea fi eliminate din Gestionarea caracteristicilor și devin obligatorii. Această modificare asigură utilizarea de către clienți a funcționalității actuale, astfel încât îmbunătățirile se pot construi pe funcționalitatea curentă pe măsură ce sunt adăugate. Funcțiile nu vor fi niciodată activate automat în mai puțin de un an, cu excepția cazului în care se consideră că sunt esențiale.

| Denumire funcție | Activare dată | Funcție adăugată | Stare caracteristică | Modul |
| --- | --- | --- |--- |--- |
| Activați operațiunea asincronă atunci când utilizatorul trebuie să comute între operațiunile de sincronizare și cele asincrone | 21 Octombrie 2022 | 9 aprilie 2021 | Activată în mod implicit | Gestionarea cheltuielilor |
| Este necesară evaluarea politicii de cheltuieli pentru încasări | 21 Octombrie 2022 | 20 decembrie 2021 | Activată în mod implicit | Gestionarea cheltuielilor |
| Vizualizare listă a rapoartelor de cheltuieli create prin delegarea lucrătorilor | 21 Octombrie 2022 | 19 februarie 2020 | Activată în mod implicit | Gestionarea cheltuielilor |
| Calculul total de kilometraj pe an fiscal | 21 Octombrie 2022 | 10 mai 2022 | Activată în mod implicit | Gestionarea cheltuielilor |
