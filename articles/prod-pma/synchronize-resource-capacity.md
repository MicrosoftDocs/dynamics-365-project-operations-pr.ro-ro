---
title: Sincronizarea capacității resurselor
description: Acest articol oferă informații despre cum să sincronizați capacitatea unei resurse între calendare și proiecte.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2b684833ffae83b7cedfc73ee96a8aa8ddd4ec57
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920719"
---
# <a name="synchronize-resource-capacity"></a>Sincronizarea capacității resurselor

[!include [banner](../includes/banner.md)]

Procesele de sincronizare a resurselor contribuie la garantarea faptului că informațiile pentru calendar și calendarul de bază se transferă în planificarea resurselor proiectului. Când calendarul este modificat, procesele fac actualizările necesare pentru planificarea resurselor proiectului. Procesele contribuie, de asemenea, la îmbunătățirea performanței, deoarece informațiile despre resurse ale calendarului sunt sincronizate în avans. Prin urmare, actualizările informațiilor de planificare a resurselor apar mai rapid. Vă recomandăm să planificați procesele ca un lot în loc de unul câte unul. În caz contrar, există riscul ca cineva să uite datele inclusive în care informațiile au fost sincronizate ultima dată. Dacă datele inclusive nu sunt utilizate, pot apărea lacune în timpul sincronizării datei.

![Sincronizare calendar.](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a>Cumulări de sincronizare a capacității resursei

Procesul de sincronizare este conceput pentru a sincroniza toate informațiile din calendarul resurselor. Aceste informații includ informații de bază despre calendar despre orice modificare a tabelului de capacitate a calendarului de resurse al proiectului. Dacă în proiect sunt adăugate resurse noi, sincronizarea ajută la garantarea disponibilității informațiilor de calendar actualizate. Această sincronizare se poate face oricând.

Vă recomandăm să utilizați un lot. Opțiunile sunt disponibile în timpul sincronizării rezervărilor de capacitate.

1. Selectați **Management de proiect și contabilitate** &gt; **Periodic** &gt; **Sincronizarea capacității** &gt; **Cumulare sincronizare resurse de capacitate**.
2. Setați opțiunile în tabelul următor.

    | Opțiune      | Descriere |
    |-------------|-------------|
    | Codul perioadei | Opțional, selectați codul intervalului de dată pentru registrul general pentru a seta datele de început și de sfârșit pentru procesul de sincronizare pentru cumulările de capacitate a resurselor. |
    | Data de început  | Introduceți data de începere pentru procesul de sincronizare pentru cumulările de capacitate a resurselor. |
    | Dată de sfârșit    | Introduceți data de încheiere pentru procesul de sincronizare pentru cumulările de capacitate a resurselor. |

[![Proces de sincronizare.](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]