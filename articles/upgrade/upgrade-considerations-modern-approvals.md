---
title: Considerații de actualizare pentru aprobările moderne
description: Subiectul acoperă punctele pe care administratorii ar trebui să le ia în considerare atunci când activează funcționalitatea Aprobari moderne.
author: stsporen
ms.date: 01/31/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: a3757f057a801318feccde9be3e49c7b40fa8fcb
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8578401"
---
# <a name="upgrade-considerations-for-modern-approvals"></a>Considerații de actualizare pentru aprobările moderne 

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Ca parte a lansării Wave 1 din aprilie 2022, funcționalitatea aprobări moderne va fi activată în mod implicit. Această funcționalitate îmbunătățește fiabilitatea logicii de aprobare și vă asigură că puteți determina motivul în care logica de aprobare eșuează.

Ca parte a acestei modificări, modificările de stare pentru aprobările proiectelor sunt actualizate. Starea merge acum direct de la **Trimis** la **Aprobat**. **In asteptarea** nu mai este un statut pentru aprobări. Pentru a determina dacă o aprobare este în așteptare, verificați dacă aprobarea face parte dintr-un set de aprobare și examinați starea setului de aprobare atașat.

## <a name="before-you-upgrade"></a>Înainte de a face upgrade

Înainte de a face upgrade la aprobări moderne, asigurați-vă că nu aveți aprobări în așteptare. Modern Approvals nu folosește **In asteptarea** stare. Prin urmare, orice aprobări care sunt încă marcate ca **In asteptarea** după upgrade nu va fi procesat.

## <a name="after-you-upgrade"></a>După ce faci upgrade

După ce faceți upgrade la Modern Approvals, un administrator trebuie să valideze că fluxul cloud care procesează aprobările a fost activat.

1. Conectați la [flow.microsoft.com](https://flow.microsoft.com)
2. În partea dreaptă sus a paginii, comutați mediul în mediul pe care l-ați actualizat.
3. Selectați **Soluții** pentru a enumera soluțiile care sunt instalate în mediu.
4. În lista de soluții, selectați **Operațiuni de proiect** sau **Serviciul de proiect**.
5. Schimbați filtrul de la **Toate** la **Cloud Flows**.
6. Verificați că **Serviciu de proiect – Programează în mod recurent seturi de aprobare a proiectelor** opțiunea este setată la **Pe**. Dacă nu este, selectați fluxul, apoi selectați **Aprinde**.
7. Verificați dacă procesarea are loc la fiecare cinci minute, examinând **Joburi de sistem** lista în **Setări** zonă.

## <a name="short-term-rollback"></a>Rollback pe termen scurt

Dacă nu puteți prelua modificările sau dacă întâmpinați o problemă gravă cu această funcție, puteți reveni temporar la fluxul de aprobare inițial, parcurgând următorii pași:
1. Conectați-vă la mediul dvs. și verificați că nu există aprobări în așteptare.
2. Mergi la **Setări** > **Parametrii proiectului**.
3. Selectați **Controlul caracteristicilor** și apoi selectați **Aprobari moderne** pentru a dezactiva caracteristica.

## <a name="removing-the-feature-flag"></a>Eliminarea steagului caracteristicii

În actualizarea Wave 2 din octombrie 2022, capacitatea de a dezactiva această funcție va fi eliminată.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
