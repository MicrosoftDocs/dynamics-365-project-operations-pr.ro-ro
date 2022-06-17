---
title: Determinarea tipului de implementare
description: Acest articol oferă informații pentru a vă ajuta să determinați tipul corect de implementare a operațiunilor de proiect pentru compania dvs.
author: stsporen
ms.date: 03/15/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 592c1bfdaf5ea6bdbf6c67bc5b82dd5cf979b367
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912209"
---
# <a name="determine-your-deployment-type"></a>Determinarea tipului de implementare

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

> [!IMPORTANT]
> După ce ați achiziționat licența, începeți aici pentru a determina cel mai bun model de implementare a Dynamics 365 Project Operations folosind [Flux de instalare ghidat](https://aka.ms/provisionprojectoperations).
> După ce ați terminat fluxul de instalare ghidat, veți fi direcționat către portalul de management corect pentru a finaliza instalarea. Consultați detaliile de implementare pentru a finaliza instalarea.


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a>Clienții existenți ai Dynamics utilizând Dynamics 365 Project Service Automation
Project Operations include capabilitățile livrate împreună cu Project Service Automation. O cale de actualizare va fi lansată pentru acești clienți în versiunea 1 de lansare 2021.

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a>Clienții existenți ai Dynamics 365 Finance care folosesc managementul proiectelor și contabilitatea 

Clienții existenți ai Finanțelor care utilizează funcționalitatea de gestionare a proiectelor și contabilitate pot continua să o utilizeze așa cum este. Consultați [Project Operations pentru scenarii cu stocuri/comenzi de producție](#pma).


## <a name="deployment-regions"></a>Regiuni de implementare
Pentru a determina ce regiuni acceptă implementarea Project Operations, consultați [Raport de disponibilitate geografică pentru Dynamics 365 și Power Platform](https://dynamics.microsoft.com/en-us/geographic-availability/). Selectați **Vizualizați raportul**, și extindeți **Dynamics 365> Aplicații pentru operațiuni > Dynamics 365 Project Operations** pentru a vizualiza regiunile acceptate.

## <a name="deployment-types"></a>Tip de implementare
Project Operations acceptă mai multe opțiuni de implementare pentru a se potrivi cerințelor dvs. Indiferent dacă sunteți un client Dynamics 365 nou sau existent, Project Operations vă poate sprijini nevoile.

[Chestionarul de implementare](https://aka.ms/provisionprojectoperations) de la noi vă va ajuta să determinați implementarea corectă. Rezultatele vă vor ghida către unul dintre următoarele tipuri de implementare:

- [Implementare simplificată - facturare de la ofertă și până la proforma](#lite)
- [Project Operations pentru resurse/scenarii fără stoc](#integrated)
- [Project Operations pentru scenarii cu stocuri/comenzi de producție](#pma)

Project Operations acceptă scenarii de stocare/comandă de producție și scenarii ne-stocate/bazate pe resurse în același mediu prin configurații la nivel de entitate juridică. De exemplu, Contoso poate utiliza capacitățile de stocare/comandă de producție în unitatea lor de producție din SUA (entitate juridică = Contoso Manufacturing United States). Contoso poate utiliza capabilitățile non-stocate/bazate pe resurse în unitatea lor de service Contoso Robotics Arms din Regatul Unit (entitate juridică = Contoso Robotics Regatul Unit).

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a>Implementare simplificată - facturare de la ofertă și până la proforma

Implementarea simplă include următoarele funcții:

- Proces de vânzări pentru proiecte care extinde experiențele aplicației Dynamics 365 Sales
- Planificarea proiectului utilizând Microsoft Project pentru web
- Prețuri multidimensionale
- Gestionare unificată a resurselor
- Urmărirea timpului
- Cheltuieli de bază
- Facturare proformă pentru revizuirea și modificările managerului de proiect 

#### <a name="deployment-steps"></a>Pași de implementare
Determinați cel mai bun model de implementare a Project Operations utilizând [Chestionar de implementare](https://aka.ms/provisionprojectoperations).

Pentru această desfășurare, consultați [Înscrieți-vă pentru abonamente de previzualizare](lite-preview-subscription-sign-up.md) și [Furnizarea accesului la un mediu nou](lite-deployment.md). 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a>Project Operations pentru resurse/scenarii fără stoc
Project Operations pentru resurse/scenarii ne-stocate includ următoarele capacități:
 
- Proces de vânzări pentru proiecte care extinde aplicația Dynamics 365 Sales
- Planificarea proiectului utilizând Microsoft Project pentru web
- Prețuri multidimensionale
- Gestionare unificată a resurselor
- Urmărirea timpului
- Cheltuieli de bază
- Cheltuieli complete
- Chitanță OCR
- Facturare Proforma și orientată către clienți 
- Recunoașterea veniturilor pentru proiecte

#### <a name="deployment-steps"></a>Pași de implementare
Determinați cel mai bun model de implementare a Project Operations utilizând [Chestionar de implementare](https://aka.ms/provisionprojectoperations).

Pentru această desfășurare, consultați [Înscrieți-vă pentru abonamente de previzualizare](resource-sign-up-preview-subscription.md) și [Furnizarea accesului la un mediu nou](resource-provision-new-environment.md). 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a>Project Operations pentru scenarii cu stocuri/comenzi de producție

- Planificarea proiectelor utilizând WBS
- Gestionarea resurselor
- Urmărirea timpului
- Cheltuieli complete
- Chitanță OCR
- Facturare completă
- Recunoașterea veniturilor
- Comenzi de producție
- Suport material stocat cu inventar

#### <a name="deployment-steps"></a>Pași de implementare
Determinați cel mai bun model de implementare a Project Operations utilizând [Chestionar de implementare](https://aka.ms/provisionprojectoperations).

Pentru această desfășurare, consultați [Înscrieți-vă pentru abonamente de previzualizare](/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=%2fdynamics365%2ffinance%2ftoc.json) și [Furnizarea accesului la un mediu nou](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=%2fdynamics365%2ffinance%2ftoc.json). 



[!INCLUDE[footer-include](../includes/footer-banner.md)]