---
title: Dezinstalare Dynamics 365 Project Operations
description: Acest subiect oferă informații despre cum să dezinstalați Dynamics 365 Project Operations.
author: stsporen
ms.date: 11/09/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: e2600c770477ad32cebb66f33a8ca31502a6da3d
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8575871"
---
# <a name="uninstall-dynamics-365-project-operations"></a>Dezinstalare Dynamics 365 Project Operations 

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

Pentru a dezinstala Dynamics 365 Project Operations, trebuie să vi se atribuie rolul de Administrator.

1. Accesați **Setări** > **Soluții**.

    ![Pagina setări.](./media/uninstall-proj-ops-solutions.png)
  
2. Eliminați soluțiile în ordinea exactă în care sunt enumerate în tabelul următor. 

    | Pas | Nume Soluție                                    | Notă                                                                                         |
    |------|----------------------------------------------------|----------------------------------------------------------------------------------------------|
    | 1 | msdyn_ProjectServiceUpgrade_managed.cab            | Dacă nu ați găsit, omiteți această soluție.                                                            |
    | 2 | ProjectOperations_Anchor                           | Dacă nu ați găsit, omiteți această soluție.                                                            |
    | 3 | Dynamics365ProjectOperationsDualWriteEntityMaps    | Dacă nu ați găsit, omiteți această soluție.                                                            |
    | 4 | Dynamics365ProjectOperationsDualWrite              | Dacă nu ați găsit, omiteți această soluție.                                                            |
    | 5 | ProjectService                                     | Fără note suplimentare.                                                                         |
    | 6 | ProjectServiceCore_Patch                           | Fără note suplimentare.                                                                         |
    | 7 | ProjectServiceCore                                 | Fără note suplimentare.                                                                         |
    | 8 | ProjectServiceDeprecatedComponents                 | Dacă nu ați găsit, omiteți această soluție.                                                            |
    | 9 | FieldServiceCommon                                 | Necesar pentru scriere duală cu Dynamics 365 Finance sau Dynamics 365 Supply Chain Management.   |
    | 10 | msdyn_AssetCommon                                  | Necesar pentru scriere duală cu Dynamics 365 Finance sau Dynamics 365 Supply Chain Management.   |
    | 11 | msdyn_TESA_Anchor                                  | Necesar pentru Dynamics 365 Field Service.                                                     |
    | 12 | msdyn_TESA_Patch                                   | Necesar pentru Dynamics 365 Field Service.                                                     |
    | 13 | msdyn_TESA                                         | Necesar pentru Dynamics 365 Field Service.                                                     |
    | 14 | ResourceSchedulingControls                         | Necesar pentru Dynamics 365 Field Service.                                                     |
    | 15 | MicrosoftDynamicsScheduling3_CumulativePatch       | Necesar pentru Dynamics 365 Field Service.                                                     |
    | 16 | MicrosoftDynamicsScheduling_Patch_xx               | Necesar pentru Dynamics 365 Field Service.                                                     |
    | 17 | MicrosoftDynamicsScheduling                        | Necesar pentru Dynamics 365 Field Service.                                                     |
    | 18 | Dynamics365FinanceAndOperationsAnchor              | Dacă nu ați găsit, omiteți această soluție.                                                            |
    | 19 | Dynamics365Notes                                   | Dacă nu ați găsit, omiteți această soluție.                                                            |
    | 20 | Dynamics365FinanceAndOperationsDualWriteEntityMaps | Dacă nu ați găsit, omiteți această soluție.                                                            |
    | 21 | DualWriteCore                                      | Dacă nu ați găsit, omiteți această soluție.                                                            |
    | 22 | Dynamics365AssetManagementApp                      | Dacă nu ați găsit, omiteți această soluție.                                                            |
    | 23 | Dynamics365AssetManagement                         | Dacă nu ați găsit, omiteți această soluție.                                                            |
    | 24 | Dynamics365SupplyChainExtended                     | Dacă nu ați găsit, omiteți această soluție.                                                            |
    | 25 | Dynamics365FinanceExtended                         | Dacă nu ați găsit, omiteți această soluție.                                                            |
    | 26 | HCMCommon                                          | Dacă nu ați găsit, omiteți această soluție.                                                            |
    | 27 | Dynamics365FinanceAndOperationsCommon              | Dacă nu ați găsit, omiteți această soluție.                                                            |
    | 28 | Grup                                              | Dacă nu ați găsit, omiteți această soluție.                                                            |
    | 29 | Dynamics365Company                                 | Dacă nu ați găsit, omiteți această soluție.                                                            |
    | 30 | CurrencyExchangeRates                              | Dacă nu ați găsit, omiteți această soluție.                                                            |
    | 31 | AssetCommon                                        | Dacă nu ați găsit, omiteți această soluție.                                                            |
