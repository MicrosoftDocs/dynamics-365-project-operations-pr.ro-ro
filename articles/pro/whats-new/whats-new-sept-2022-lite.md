---
title: Noutăți septembrie 2022 - implementare simplificată Project Operations
description: Acest articol oferă informații despre actualizările de calitate care sunt disponibile în versiunea din septembrie 2022 de implementare a Microsoft Dynamics 365 Project Operations lite.
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

Acest articol se aplică următoarelor componente și versiuni de Microsoft Dynamics 365 Project Operations:

- Project Operations într-un mediu Dataverse versiunea 4.46.0.60

## <a name="features-included-in-this-release"></a>Caracteristicile incluse în această versiune

| Zonă de caracteristici | Denumire funcție | Mai multe informații |
| --- | --- | --- |
| Managementul oportunităților | **Revizuirea și activarea ofertelor**<br>Project Operations oferă suport deplin al procesului de vânzări. Ofertele de proiect pot fi activate pentru a reprezenta o stare în care oferta este doar pentru citire și este în curs de revizuire. Ofertele activate pot fi revizuite pentru a crea oferte noi care au un număr de revizuire incrementat. Ofertele de proiect activate sau revizuirile de oferte pot fi închise sub formă de câștigate sau pierdute. | [Activarea și revizuirea unei oferte de proiect](/dynamics365/project-operations/sales/activation-and-revision) |
| Facturarea și stabilirea prețurilor | **Prețul agnostic pentru fusul orar este implicit**<br>Project Operations a introdus conceptul unei date agnostice de fus orar pe toate valorile reale ale proiectului. Un câmp nou, **Dată tranzacție** este acum disponibil pe liniile jurnalului și pe valorile reale și va fi folosit pentru a stoca data la care a avut loc tranzacția, dar fără a converti data respectivă în Ora universală coordonată. Această dată va fi utilizată pentru procesele din aval, cum ar fi stabilirea implicită a prețurilor și crearea facturii. | <p>[Stabilirea ratelor de cost pentru estimările și valorile reale bazate pe proiect](/dynamics365/project-operations/pro/pricing-costing/cost-price-resolution-sales)</p><p>[Stabilirea prețurilor de vânzare pentru estimări și valori reale bazate pe proiect](/dynamics365/project-operations/pro/pricing-costing/sales-price-resolution-sales)</p> |
| Facturarea și stabilirea prețurilor | **Înlocuirile de prețu cu dată efectivă în Project Operations**<br>Înlocuirile de preț cu dată efectivă oferă o modalitate de a înlocui sau modifica anumite prețuri din lista de prețuri. | [Înlocuiri de preț cu dată efectivă](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Timp și cheltuială | **Aprobator global**<br>Această caracteristică autorizează furnizorul independent de software (ISV) și aprobarea centralizată, indiferent de statutul proiectului sau al membrului echipei în proiect. | [Securitate și aprobări](/dynamics365/project-operations/approvals/approvals-security) |
|Planificare și urmărire de proiect|**Utilizați API-urile de planificare a proiectelor pentru a efectua operațiuni cu entități de planificare** </br> </br>API-ul de editare a conturului de atribuire a resurselor le permite dezvoltatorilor să specifice în mod programatic efortul unui desemnat al sarcinii în orice interval de date acceptat pentru o planificare mai granulară a efortului în etape de timp.|[Utilizați API-urile de planificare a proiectelor pentru a efectua operațiuni cu entități de planificare](/dynamics365/project-operations/project-management/schedule-api-preview)|

## <a name="quality-updates"></a>Actualizări de calitate

| Zonă de caracteristici | Număr de referință | Actualizare de calitate |
| --- | --- | --- |
| Facturarea și stabilirea prețurilor | 2754422 | Estimările de materiale și cheltuieli nu ajung la Dynamics 365 Finance atunci când proiectele sunt copiate în Dataverse. |
| Timp și cheltuială | 2787409 | Un aprobator nevalid poate aproba o intrare de timp non-proiect. |
| Managementul oportunităților | 2788907 | Mesaj de eroare actualizat privind validarea unicității pentru liniile de comandă care includ indicatoare. |
| Timp și cheltuială | 2842253 | Gestionarea excepțiilor nule pentru aprobarea timpului. |
| Facturarea și stabilirea prețurilor | 2844181 | Eșecul de a obține ID-ul de corelare blochează crearea facturii. |
| Facturarea și stabilirea prețurilor | 2876628 | QLD, CLD - Rezoluția estimată a listei de prețuri ar trebui să utilizeze câmpurile vechi ale intervalului de date ale listei de prețuri. |
| Subcontractare | 2893222 | Dacă nu este specificat niciun rol pentru o linie de subcontractare, ar trebui să fie posibilă selectarea acelei linii pe un membru al echipei pentru orice rol. |
