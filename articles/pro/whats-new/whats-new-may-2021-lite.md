---
title: Noutăți mai 2021 - implementare simplificată Project Operations
description: Acest subiect oferă informații despre actualizările de calitate disponibile în versiunea din mai 2021 a implementării simplificate Project Operations.
author: sigitac
ms.date: 05/17/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 14ff7f1f7374ffe885c511fd693cda5b7023c5beb53adb45042ddda1e932c93d
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/06/2021
ms.locfileid: "7005991"
---
# <a name="whats-new-may-2021---project-operations-lite-deployment"></a>Noutăți mai 2021 - implementare simplificată Project Operations

_Se aplică pentru: implementare simplificată - înțelegere la emiterea facturii proforme_

Acest subiect se aplică următoarelor componente și versiuni Dynamics 365 Project Operations:

   - Project Operations pe mediul Dataverse versiunea 4.10.0.186.

## <a name="features-included-in-this-release"></a>Caracteristicile incluse în această versiune

Următoarele caracteristici sunt incluse în această versiune:

- [Moduri de planificare](../../project-management/scheduling-modes.md): Managerii de proiect pot defini acum dacă un proiect ar trebui să fie gestionat utilizând o durată fixă, munca fixă sau modul de planificare a unităților fixe.

## <a name="quality-updates"></a>Actualizări de calitate

| **Zonă de caracteristici** | **Număr de referință** | **Actualizare de calitate** |
| --- | --- | --- |
| Facturarea și stabilirea prețurilor | 2224568 | S-a adăugat logică pentru a permite particularizări care implică invocarea insertului de confirmare a facturii. |
| Facturarea și stabilirea prețurilor | 2101098 | Am îmbunătățit logica câmpurilor implicite pentru a factura proforma. Aceste câmpuri includ, **Adresa de facturare**, **Nume de facturare** și **Termeni de plată**. Câmpurile sunt acum implicite din înregistrarea clientului contractului de proiect corespunzător. |
| Facturarea și stabilirea prețurilor | 2021413 | Actualizat câmpurile **Cost actual** și **Vânzări** de pe entitatea **Activitate** să includă valorile vânzărilor din cheltuielile nefacturate și facturate pe activități. |
| Facturarea și stabilirea prețurilor | 2182110 | La copierea unui contract de proiect, ID-ul liniei contractului este regenerat în contractul de proiect de destinație pentru a se asigura că este unic. |
| Managementul oportunităților | 2186741 | S-au adăugat validări pentru a asigura că câmpul **Origine** și tipul tranzacției nu poate fi actualizat la detaliile existente despre linia de ofertă. |
| Managementul oportunităților | 2191353 | Crearea jaloanelor nu trebuie permisă pe o linie contractuală de timp și material. |
| Managementul oportunităților | 2216956 | S-au rezolvat problemele cu **Actualizați prețurile**. |
| Planificare și urmărire | 2182979 | Funcția de copiere a proiectului a fost îmbunătățită pentru a se asigura ca liniile de estimare a cheltuielilor sunt copiate din proiectul original. |
| Planificare și urmărire | 2184144 | Funcția de copiere a proiectului a fost îmbunătățită pentru a se asigura că numele poziției resursei este copiat din proiectul original. |
| Planificare și urmărire | 2184799 | Controlul a fost strâns când se copiază un proiect pentru a asigura că data estimată de începere nu poate fi modificare în timp ce copierea este în curs. |
| Planificare și urmărire | 2185134 | În timpul copierii unui proiect, data estimată de începere a proiectului de destinație este setată la data de astăzi. |
| Planificare și urmărire | 2196373 | Asigurați-vă că înregistrările managerului de proiect și ale membrilor echipei nu sunt duplicate în echipa proiectului când se copiază un proiect. |
| Planificare și urmărire | 2211833 | Alocările resurselor sunt copiate din sarcina proiectului sursă în proiectul destinație. |
| Planificare și urmărire | 2186541 | S-au rezolvat problemele din grila **Estimări** la gruparea după **Resurse**. |
| Planificare și urmărire | 2166906 | Categoria de tranzacție dintr-o activitate trebuie copiată în entitatea **Alocarea resurselor**. |
| Gestionarea de resurse | 2125362 | S-au rezolvat problemele legate de crearea unui membru generic al echipei folosind metoda de alocare bazată pe ore. |
| Timp și cheltuială | 2113603 | S-a remediat problema legată de particularizare prin eliminarea atributelor din pagina **Intrare de timp**. Sistemul verifică acum dacă atributul există pe pagină înainte de a accesa atributul utilizând un script. |
| Timp și cheltuială | 2204377 | Fișele de timp copiate trebuie să se afișeze automat atunci când selectați **Copiați săptămâna**. |
| Timp și cheltuială | 2209059 | Câmpul **Stare** este editabil pentru intrări de timp Dynamics 365 Field Service. |
