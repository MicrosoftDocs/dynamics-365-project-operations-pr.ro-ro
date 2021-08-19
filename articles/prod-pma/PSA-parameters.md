---
title: Parametri de integrare Project Service Automation
description: Acest subiect explică modul de configurare a modului în care sunt introduse datele implicite la integrare Microsoft Dynamics 365 for Project Service Automation cu Microsoft Dynamics 365 Finance.
author: ruhercul
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: ruhercul
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: b58f34cb74be531a98518100158f39d74f136afc34444468d666cd4e9394af6f
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/06/2021
ms.locfileid: "7005856"
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


[!INCLUDE[footer-include](../includes/footer-banner.md)]