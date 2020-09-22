---
title: Ce este nou în Project Service Automation versiunea actualizată 13, V3
description: Acest subiect oferă informații despre ceea ce este nou și schimbat în Project Service Automation versiunea 13, V3.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: c6f6a5b6-b5bb-467c-b7c7-7fb962504c6d
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 5f1b6b3879c94a77ab62082aad1e470a3ba66552
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754745"
---
# <a name="project-service-automation-v3-update-release-13"></a>Project Service Automation V3, versiunea actualizată 13
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
     - Remediat: Butoane suplimentare pentru **Oportunitate nouă**, **Ofertă**, **Linie de comandă** și **Adaugă produs** sunt vizibile în comenzile pentru Oportunități, Oferte, Produse pentru Comandă și sub-rețeaua Linii bazate pe proiect.


