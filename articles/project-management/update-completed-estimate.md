---
title: Actualizarea costului estimat la finalizare
description: Acest subiect oferă informații despre actualizarea proiecției efortului asupra unui proiect.
author: ruhercul
manager: AnnBe
ms.date: 09/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 42824cc4cfc2b934f69d319944fe7ee43183955c
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897781"
---
# <a name="update-estimate-at-completion"></a>Actualizarea costului estimat la finalizare

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Este un lucru obișnuit ca un manager de proiect să revizuiască estimările inițiale ale unei activități. Reproiectările proiectului reprezintă percepția estimativă a unui manager de proiect, dat fiind starea actuală a proiectului. Cu toate acestea, nu recomandăm ca managerii de proiect să modifice numerele de referință, pentru că referința proiectului reprezintă sursa stabilită de adevăr pentru planificarea proiectului și estimarea de cost și toți participanții direct interesați ai proiectului s-au pus de acord în această privință.

Există două modalități prin care un manager de proiect poate reproiecta efortul asupra activităților:

- Suprascrie estimarea implicită pentru a finaliza (ETC) cu o nouă estimare a efortului efectiv rămase pe activitate. 
- Suprascrie procentul progresului implicit cu o nouă estimare a progresului real asupra activității.

Fiecare dintre aceste abordări cauzează o recalculare a activității ETC, estimarea la realizare (EAC) și procentajul de progres, precum și varianța de efort proiectată pentru o activitate. EAC, ETC, și procentul de progres cu privire la activitățile de sinteză sunt recalculate, și produce o nouă proiecție a varianței efortului.
