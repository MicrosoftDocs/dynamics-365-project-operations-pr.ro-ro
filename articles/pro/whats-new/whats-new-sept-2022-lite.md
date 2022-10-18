---
title: Noutăți septembrie 2022 - implementare simplificată Project Operations
description: Acest articol oferă informații despre actualizările de calitate care sunt disponibile în versiunea Microsoft din septembrie 2022 Dynamics 365 Project Operations implementare simplă.
author: ramagadu
ms.date: 09/28/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: a02ac7a69489bc7974eb0e63c11fa5de74795b78
ms.sourcegitcommit: b3a70bc4f2850cff5c2b7114cff7bd61ec298143
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/06/2022
ms.locfileid: "9634868"
---
# <a name="whats-new-september-2022---project-operations-lite-deployment"></a>Noutăți septembrie 2022 - implementare simplificată Project Operations

_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_

Acest articol se aplică următoarelor componente și versiuni ale Microsoft Dynamics 365 Project Operations:

- Operațiuni de proiect în a Dataverse versiunea de mediu 4.46.0.60

## <a name="features-included-in-this-release"></a>Caracteristicile incluse în această versiune

| Zonă de caracteristici | Numele caracteristicii | Mai multe informații |
| --- | --- | --- |
| Managementul oportunităților | **Revizuirea și activarea cotațiilor**<br>Project Operations oferă suport deplin al procesului de vânzări. Ofertele de proiect pot fi activate pentru a reprezenta o stare în care oferta este doar pentru citire și este în curs de revizuire. Citatele activate pot fi revizuite pentru a crea ghilimele noi care au un număr de revizuire incrementat. Cotațiile de proiecte activate sau revizuirile de cotații pot fi închise ca câștigate sau pierdute. | [Activarea și revizuirea unei oferte de proiect](/dynamics365/project-operations/sales/activation-and-revision) |
| Facturarea și stabilirea prețurilor | **Prețul agnostic de fus orar este implicit**<br>Project Operations a introdus conceptul unei date agnostice de fus orar pe toate datele reale ale proiectului. Un domeniu nou, **Data tranzacției**, este acum disponibil pe liniile jurnalului și pe valorile reale și va fi folosit pentru a stoca data la care a avut loc tranzacția, dar fără a converti data respectivă în Ora universală coordonată. Această dată va fi utilizată pentru procesele din aval, cum ar fi stabilirea implicită a prețurilor și crearea facturii. | <p>[Determinați ratele de cost pentru estimările și valorile reale bazate pe proiecte](/dynamics365/project-operations/pro/pricing-costing/cost-price-resolution-sales)</p><p>[Determinați prețurile de vânzare pentru estimări și valori reale bazate pe proiecte](/dynamics365/project-operations/pro/pricing-costing/sales-price-resolution-sales)</p> |
| Facturarea și stabilirea prețurilor | **Prețurile efective de date în operațiunile de proiect**<br>Depășirile de preț efective în funcție de dată oferă o modalitate de a modifica sau de a modifica prețurile specifice din lista de prețuri. | [Prețurile efective de date](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Timp și cheltuială | **Aprobator global**<br>Această caracteristică permite furnizorul independent de software (ISV) și aprobarea centralizată, indiferent de statutul proiectului sau membru al echipei din proiect. | [Securitate și aprobări](/dynamics365/project-operations/approvals/approvals-security) |
|Planificare și urmărire de proiect|**Utilizați API-urile de planificare a proiectelor pentru a efectua operațiuni cu entități de planificare** </br> </br>API-ul de editare a conturului de atribuire a resurselor le permite dezvoltatorilor să specifice în mod programatic efortul unui desemnat al sarcinii în orice interval de date acceptat pentru o planificare mai granulară a efortului în etape.|[Utilizați API-urile de planificare a proiectelor pentru a efectua operațiuni cu entități de planificare](/dynamics365/project-operations/project-management/schedule-api-preview)|

## <a name="quality-updates"></a>Actualizări de calitate

| Zonă de caracteristici | Număr de referință | Actualizare de calitate |
| --- | --- | --- |
| Facturarea și stabilirea prețurilor | 2754422 | Estimările de materiale și cheltuieli nu ajung la Dynamics 365 Finance atunci când proiectele sunt copiate în Dataverse. |
| Timp și cheltuială | 2787409 | Un autorizator nevalid poate aproba o intrare de timp non-proiect. |
| Managementul oportunităților | 2788907 | Mesaj de eroare actualizat privind validarea unicității pentru liniile de comandă care includ indicatoare. |
| Timp și cheltuială | 2842253 | Gestionarea excepțiilor nulă pentru aprobarea timpului. |
| Facturarea și stabilirea prețurilor | 2844181 | Eșecul de a obține ID-ul de corelare blochează crearea facturii. |
| Facturarea și stabilirea prețurilor | 2876628 | QLD, CLD - Rezoluția estimată a listei de prețuri ar trebui să utilizeze câmpurile vechi ale intervalului de date ale listei de prețuri. |
| Subcontractare | 2893222 | Dacă nu este specificat niciun rol pentru o linie de subcontractare, ar trebui să fie posibilă selectarea acelei linii pe un membru al echipei pentru orice rol. |
