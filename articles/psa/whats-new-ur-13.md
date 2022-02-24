---
title: Ce este nou sau schimbat în Project Service Automation versiunea actualizată 13, V3
description: Acest subiect oferă informații despre ceea ce este nou și schimbat în Project Service Automation versiunea 13, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 7287054c470a44ed1fdc243018ec935fe21a6c4f
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147263"
---
# <a name="project-service-automation-update-release-13-v3"></a>Project Service Automation, versiunea actualizată 13, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Suntem încântați să anunțăm cea mai recentă actualizare pentru aplicația Dynamics 365 Project Service Automation (PSA). Această versiune include câteva îmbunătățiri importante ale calității, performanței și utilizabilității. Această versiune este compatibilă cu Dynamics 365 9.x. Pentru a actualiza această versiune, accesați Centrul de administrare pentru Dynamics 365 online și accesați pagina cu soluții pentru a instala actualizarea. Pentru informații suplimentare, consultați: [Instalarea, actualizarea sau eliminarea unei soluții preferate](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Acest subiect listează caracteristicile și corecțiile care sunt noi sau modificate pentru Project Service Automation V3, versiunea actualizată 13. Această versiune are un număr de V3.10.3.18 și este disponibilă în următoarea planificare:

- **Disponibilitate generală (autoactualizare):** noiembrie 2019
- **Auto-actualizare:** decembrie 2019


## <a name="update-release-13"></a>Lansarea de actualizări 13 

### <a name="bug-fixes"></a>Remedieri de erori

- Timp și cheltuială

     - Remediat: funcționalitatea de căutare pe pagina **Aprobarea cheltuielilor** nu funcționează atunci când căutați după scopul cheltuielii.

- Gestionarea de resurse

     - Remediat: Numerele de reconciliere au fost actualizate pentru a fi justificate corect.
     - Remediat: Resurse denumite nu pot fi atribuite sarcinilor prin intermediul filei **Planificare**.

- Gestionare de proiect

     - Remediat: excepție de referință nulă la atribuirea unui membru al echipei atunci când din **Tipul tranzacției** lipsesc informațiile de configurare pentru **Unitate** și **DefaultGroup**.

- Sales

     - Remediat: înregistrările de tipul de tranzacție duplicat returnează o eroare atunci când sunt create înregistrările de prețuri de rol.
     - Reparat: butoane suplimentare pentru **Oportunitate nouă**, **Ofertă**, **Linie de comandă** și **Adăugați produs** sunt vizibile în comenzile pentru Oportunități, Oferte, Produse de comandă și subgrila Linii bazate pe proiecte.


