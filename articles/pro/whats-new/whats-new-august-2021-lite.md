---
title: Noutăți în august 2021 - implementare Project Operations lite
description: Acest articol oferă informații despre actualizările de calitate disponibile în versiunea din august 2021 a implementării Project Operations lite.
author: sigitac
ms.date: 08/10/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 84318a26d97355fe56794e1d1532576cde4af661
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922053"
---
# <a name="whats-new-august-2021---project-operations-lite-deployment"></a>Noutăți în august 2021 - implementare Project Operations lite

_Se aplică pentru: implementare simplificată - înțelegere la emiterea facturii proforme_

Acest articol se aplică la următoarele Dynamics 365 Project Operations componente si versiuni:

  - Project Operations pe mediul Dataverse versiunea 4.13.0.152

## <a name="features-included-in-this-release"></a>Caracteristicile incluse în această versiune

Următoarele caracteristici sunt incluse în această versiune:

- **Seturi de aprobare**: Seturile de aprobare grupează cererile de timp, cheltuieli sau solicitări de aprobare a utilizării materialelor în subseturi mai mici de operațiuni. Această grupare permite procesarea aprobărilor într-o ordine specifică după proiect și permite reîncercarea și secvențierea. Gruparea cererilor îmbunătățește fiabilitatea și trasabilitatea procesării aprobării pentru volume mari de aprobări. Pentru informații suplimentare, consultați [Seturi de aprobări](../../approvals/approval-sets.md).

## <a name="quality-updates"></a>Actualizări de calitate

### <a name="project-operations-on-dataverse"></a>Project Operations pe Dataverse

| **Zonă de caracteristici** | **Număr de referință** | **Actualizare de calitate** |
| --- | --- | --- |
| Facturarea și stabilirea prețurilor | 2295625 | Numele jalonului trebuie copiat din planificarea facturării în detaliul liniei de facturare. |
| Facturarea și stabilirea prețurilor | 2316323 | Reducerea nu ar trebui să poată fi modificată pe o factură proforma în Project Operations pentru scenarii bazate pe resurse. |
| Managementul oportunităților | 2338619 | Regulile de business **Oportunitate** și **Ofertă** trebuie invocate numai pe pagini. |
| Gestionarea resurselor | 2316523 | Folosirea de **Trimitere cerere** dintr-o cerință de resursă care are un rol atașat nu ar trebui să afișeze o eroare. |
| Gestionarea resurselor | 2326885 | Crearea unei cerințe de resurse printr-un proiect nu ar trebui să afișeze o eroare. |
| Timp și cheltuieli | 2335584 | Fluxuri de activități depreciate în înregistrarea de timp. |
| Timp și cheltuieli | 2336884 | Butonul de înregistrare de timp **Copiere săptămână** nu trebuie să funcționeze doar pentru utilizatorul curent. |
