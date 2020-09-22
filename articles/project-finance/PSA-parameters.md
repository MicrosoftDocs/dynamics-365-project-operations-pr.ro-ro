---
title: Parametri de integrare Project Service Automation
description: Acest subiect explică modul de configurare a modului în care sunt introduse datele implicite la integrare Microsoft Dynamics 365 for Project Service Automation cu Microsoft Dynamics 365 Finance.
author: KimANelson
manager: AnnBe
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: ade812ac-2f8f-4761-a474-0fd7246967df
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 9e46823f8bd3aef2ba9be271560c3a532be8ef0d
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754735"
---
# <a name="project-service-automation-integration-parameters"></a>Parametri de integrare Project Service Automation

[!include[banner](../includes/banner.md)]

Pe pagina **Parametrii de integrare a Project Service Automation**, puteți configura modul în care sunt introduse datele implicite când integrați Dynamics 365 Project Service Automation cu Dynamics 365 Finance. Pentru ca proiectele să fie sincronizate cu succes de la Project Service Automation la Finance, trebuie să configurați următoarele câmpuri.

Pentru a deschide pagina **Parametrii de integrare a Project Service Automation**, accesați **Management de proiect și contabilitate** \> **Configurare** \> **Dynamics 365 for Project Service Automation parametri de integrare**. 

> [!NOTE]
> - Integrarea sarcinilor proiectului, categoriile tranzacțiilor de cheltuieli, estimările orelor, estimările cheltuielilor și blocarea funcționalității sunt disponibile în versiunea 8.0.
> - Integrarea datelor reale este disponibilă din cu versiunea 8.0.1 sau mai nouă.


| Tabulator                    | Câmp                | Descriere |
|------------------------|----------------------|-------------|
| General                | Tip de proiect implicit | Selectați tipul implicit de proiect. Când proiectele sunt sincronizate din Project Service Automation, această valoare este utilizată dacă nu ați furnizat o valoare implicită în șablonul de integrare. În timpul sincronizării, câmpul **Tipul proiectului** de proiecte noi este setat la această valoare. Cu toate acestea, valoarea poate fi actualizată atunci când liniile contractului de proiect sunt sincronizate cu Project Service Automation. |
|                        | Categoria de timp        | Selectați categoria de timp implicită. Această valoare este utilizată atunci când estimările orelor sunt sincronizate de la Project Service Automation. Când estimările orelor și efectele orelor sunt sincronizate de la Project Service Automation, câmpul **Categorie** previziunilor orelor de proiect în Finanțe este setat la această valoare. |
|                        | Categorie taxă         | Selectați categoria de taxă implicită. Această valoare este utilizată atunci când datele de taxe sunt sincronizate de la Project Service Automation. Când estimările taxelor sunt sincronizate de la Project Service Automation, câmpul **Categorie** previziunilor tranzacțiilor de taxe în Finanțe este setat la această valoare. |
| Setările implicite ale grupului de proiect | Tip de proiect         | Clic **Nou** pentru a adăuga un rând în care puteți selecta tipul de proiect pentru care setați grupul de proiect implicit. Un anumit tip de proiect poate fi selectat o singură dată în configurație. |
|                        | Grupul de proiect        | Selectați grupul de proiect implicit pentru tipul de proiect selectat. Când noile proiecte sunt sincronizate de la Project Service Automation, câmpul **Grup de proiect** este setat la valoarea implicită pentru tipul de proiect dacă nu ați furnizat o valoare implicită în șablonul de integrare. |
| Tip implicit de facturare  | Tip de facturare         | Clic **Nou** pentru a adăuga un rând în care puteți selecta tipul de facturare pentru care setați linia implicită de proprietate. Un anumit tip de facturare poate fi selectat o singură dată în configurație. |
|                        | Proprietate de linie        | Selectați linia de proprietate implcită pentru tipul de facturare selectat. Atunci când estimările orelor noi, estimările cheltuielilor noi sau noile date reale sunt sincronizate din Project Service Automation, câmpul **Proprietate de linie** este setat la valoarea implicită pentru tipul de facturare. |
| Blocarea funcționalității  | Nu se aplică       | Selectați funcționalitatea de dezactivat în Finanțe pentru proiecte și contracte care au provenit din Project Service Automation. De exemplu, puteți dezactiva capacitatea de a edita contracte și proiecte, de a crea structuri de repartizare a lucrărilor și de a introduce fișe de timp în Finanțe. Câmpurile legate de contabilitate vor continua să fie activate, chiar dacă acestea nu sunt disponibile prin setarea parametrilor. În mod implicit, toate funcționalitățile sunt activate. |
