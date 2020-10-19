---
title: Tip de implementare
description: Acest subiect oferă informații pentru a vă ajuta să determinați tipul corect de implementare a operațiunilor de proiect pentru compania dvs.
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: c3cf378caae4510482a8ee6771bf2e6decfe3b48
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949028"
---
# <a name="deployment-types"></a>Tip de implementare

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

> [!IMPORTANT]
> După ce ați achiziționat licența, începeți aici pentru a determina cel mai bun model de implementare a operațiunilor de proiect Dynamics 365 Project Operations folosind [Flux de instalare ghidat](https://aka.ms/provisionprojectoperations).
> După ce ați terminat fluxul de instalare ghidat, veți fi direcționat către portalul de management corect pentru a finaliza instalarea. Consultați detaliile de implementare de mai jos pentru a finaliza instalarea.


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a>Clienții existenți ai Dynamics utilizând Dynamics 365 Project Service Automation
Project Operations include capabilitățile livrate împreună cu Project Service Automation. O cale de actualizare va fi lansată pentru acești clienți în viitor.

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a>Clienții existenți ai Dynamics 365 Finance care utilizează managementul proiectului și contabilitatea 

Clienții existenți ai Finanțelor care utilizează funcționalitatea de gestionare a proiectelor și contabilitate pot utiliza în continuare acest lucru așa cum este. Consultați [Project Operations pentru scenarii cu stocuri/comenzi de producție](#pma).

Project Operations acceptă mai multe opțiuni de implementare pentru a se potrivi cerințelor dvs. Indiferent dacă sunteți un client Dynamics 365 nou sau existent, Project Operations vă poate sprijini nevoile.

[Chestionarul de implementare](https://aka.ms/provisionprojectoperations) de la noi vă va ajuta să determinați implementarea corectă. Rezultatele vă vor ghida către unul dintre următoarele tipuri de implementare:

- [Implementare simplificată - facturare de la ofertă și până la proforma](#lite)
- [Project Operations pentru resurse/scenarii fără stoc](#integrated)
- [Project Operations pentru scenarii cu stocuri/comenzi de producție](#pma)

Project Operations acceptă scenarii de stocare/comandă de producție și scenarii ne-stocate/bazate pe resurse în același mediu prin configurații la nivel de entitate juridică. De exemplu, Contoso poate valorifica capacitățile de stocare/comandă de producție din unitatea de producție din SUA (entitate juridică = Contoso Manufacturing United States) și capacitățile ne-stocate/bazate pe resurse în unitatea de service Contoso Robotics Arms din Regatul Unit (entitate juridică = Contoso Robotics Regatul Unit).

## <a name="a-namelitelite-deployment---deal-to-proforma-invoicing"></a><a name="lite"><a/>Implementare simplificată - facturare de la ofertă și până la proforma
Implementarea simplă include următoarele funcții:

- Planificarea proiectului utilizând Microsoft Project pentru web
- Prețuri multidimensionale
- Gestionare unificată a resurselor
- Urmărirea timpului
- Cheltuieli de bază
- Propunere de factură

### <a name="deployment-steps"></a>Pași de implementare:
Determinați cel mai bun model de implementare a Project Operations utilizând [Chestionar de implementare](https://aka.ms/provisionprojectoperations).

Pentru această desfășurare, consultați [Înscrieți-vă pentru abonamente de previzualizare](lite-preview-subscription-sign-up.md) și [Furnizarea accesului la un mediu nou](lite-deployment.md). 


## <a name="a-nameintegratedproject-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"><a/>Project Operations pentru resurse/scenarii fără stoc
Project Operations pentru resurse/scenarii ne-stocate includ următoarele capacități:
  
- Planificarea proiectului utilizând Microsoft Project pentru web
- Prețuri multidimensionale
- Gestionare unificată a resurselor
- Urmărirea timpului
- Cheltuieli de bază
- Cheltuieli complete
- Chitanță OCR
- Facturare completă
- Recunoașterea veniturilor

### <a name="deployment-steps"></a>Pași de implementare:
Determinați cel mai bun model de implementare a Project Operations utilizând [Chestionar de implementare](https://aka.ms/provisionprojectoperations).

Pentru această desfășurare, consultați [Înscrieți-vă pentru abonamente de previzualizare](resource-sign-up-preview-subscription.md) și [Furnizarea accesului la un mediu nou](resource-provision-new-environment.md). 


## <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a>Project Operations pentru scenarii cu stocuri/comenzi de producție

- Planificarea proiectelor utilizând WBS
- Gestionarea de resurse
- Urmărirea timpului
- Cheltuieli complete
- Chitanță OCR
- Facturare completă
- Recunoașterea veniturilor
- Comenzi de producție
- Materiale de asistență

### <a name="deployment-steps"></a>Pași de implementare:
Determinați cel mai bun model de implementare a Project Operations utilizând [Chestionar de implementare](https://aka.ms/provisionprojectoperations).

Pentru această desfășurare, consultați [Înscrieți-vă pentru abonamente de previzualizare](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) și [Furnizarea accesului la un mediu nou](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json). 



