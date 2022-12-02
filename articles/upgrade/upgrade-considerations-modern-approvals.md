---
title: Considerații privind upgrade-ul pentru Aprobări moderne
description: Articolul acoperă punctele pe care administratorii ar trebui să le ia în considerare atunci când activează funcționalitatea Aprobări moderne.
author: stsporen
ms.date: 01/31/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 44a933c92d4ef8dff40f20200d74c4bbdf8caa76
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931759"
---
# <a name="upgrade-considerations-for-modern-approvals"></a>Considerații privind upgrade-ul pentru Aprobări moderne 

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Ca parte a lansării Valului 1 din aprilie 2022, funcționalitatea Aprobări moderne va fi activată în mod implicit. Această funcționalitate îmbunătățește fiabilitatea logicii de aprobare și vă asigură că puteți stabili motivul dacă logica de aprobare eșuează.

Ca parte a acestei modificări, modificările de stare pentru aprobările proiectelor sunt actualizate. Starea merge acum direct de la **Trimis** la **Aprobat**. **În așteptare** nu mai este o stare pentru aprobări. Pentru a determina dacă o aprobare este în așteptare, verificați dacă aprobarea face parte dintr-un set de aprobare și examinați starea setului de aprobare atașat.

## <a name="before-you-upgrade"></a>Înainte de a face upgrade

Înainte de a face upgrade la Aprobări moderne, asigurați-vă că nu aveți aprobări în așteptare. Aprobări moderne nu utilizează starea **În așteptare**. Prin urmare, orice aprobări care sunt încă marcate ca **În așteptare** după upgrade nu vor fi procesate.

## <a name="after-you-upgrade"></a>După ce faceți upgrade

După ce faceți upgrade la Aprobări Moderne, un administrator trebuie să valideze că fluxul cloud care procesează aprobările a fost activat.

1. Conectați-vă la [flow.microsoft.com](https://flow.microsoft.com)
2. În partea dreaptă sus a paginii, comutați mediul la mediul pe care l-ați actualizat.
3. Selectați **Soluții** pentru a enumera soluțiile care sunt instalate în mediu.
4. În lista de soluții, selectați **Project Operations** sau **Project Service**.
5. Schimbați filtrul de la **Toate** la **Fluxuri Cloud**.
6. Verificați dacă opțiunea **Project Service – Programare recurentă a seturilor de aprobare a proiectelor** este setată ca **Activată**. Dacă nu este activată, selectați fluxul, apoi selectați **Activare**.
7. Verificați dacă procesarea are loc la fiecare cinci minute, examinând lista **Procese de sistem** în zona **Setări**.

## <a name="short-term-rollback"></a>Revenire pe termen scurt

Dacă nu puteți prelua modificările sau dacă întâmpinați o problemă gravă cu această funcție, puteți reveni temporar la fluxul de aprobare inițial, parcurgând următorii pași:
1. Conectați-vă la mediul dvs. și verificați că nu există aprobări în așteptare.
2. Accesați **Setări** > **Parametri proiect**.
3. Selectați **Control funcții** și apoi selectați **Aprobări moderne** pentru a dezactiva funcția.

## <a name="removing-the-feature-flag"></a>Eliminarea marcajului funcției

În actualizarea Valul 2 din octombrie 2022, capacitatea de a dezactiva această funcție va fi eliminată.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
