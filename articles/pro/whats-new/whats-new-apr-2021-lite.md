---
title: Noutăți aprilie 2021 - implementare simplificată Project Operations
description: Acest subiect oferă informații despre actualizările de calitate disponibile în versiunea din aprilie 2021 a implementării simplificate Project Operations.
author: sigitac
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 8c85e0230840753bc1d28a46b065bce002446f5d8c62da9666d58bc9d2a68af8
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/06/2021
ms.locfileid: "7009411"
---
# <a name="whats-new-april-2021---project-operations-lite-deployment"></a>Noutăți aprilie 2021 - implementare simplificată Project Operations

_Se aplică pentru: implementare simplificată - înțelegere la emiterea facturii proforme_

Acest subiect se aplică următoarelor componente și versiuni Dynamics 365 Project Operations:

  - Project Operations pe mediul Dataverse versiunea 4.9.0.221 

## <a name="features-included-in-this-release"></a>Caracteristicile incluse în această versiune

Următoarele caracteristici sunt incluse în această versiune:

- Materiale ne-stocate pentru proiecte. Capabilitățile cheie includ:
  - Estimarea și prețul materialelor ne-stocate în timpul ciclului de vânzări pentru un proiect. Pentru mai multe informații, consultați [Configurați rate de cost și vânzări pentru produse de catalog - simplificat](../pricing-costing/set-up-cost-sales-rates-catalog-products.md).
  - Urmărirea utilizării materialelor ne-stocate în timpul livrării proiectului. Pentru informații suplimentare, consultați [Înregistrarea utilizării materialelor pentru proiecte și activitățile proiectului](../../material/material-usage-log.md).
  - Facturarea costurilor materiale ne stocate utilizate. Pentru mai multe informații, consultați [Gestionați restanțele de facturare - simplificat](../proforma-invoicing/manage-billing-backlog-sales.md#product-billing-backlog).
  - API-uri noi în Dynamics 365 Dataverse permite crearea, actualizarea și ștergerea operațiunilor cu **Planificarea entităților**. Pentru mai multe informații, consultați [Utilizați API-uri de programare pentru a efectua operațiuni cu entități de planificare](../../project-management/schedule-api-preview.md).

## <a name="quality-updates"></a>Actualizări de calitate

| **Zonă de caracteristici** | **Număr de referință** | **Actualizare de calitate** |
| --- | --- | --- |
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
