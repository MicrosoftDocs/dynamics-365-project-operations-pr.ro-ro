---
title: Activați și revizuiți o ofertă de proiect
description: Acest articol oferă informații despre activarea și revizuirea cotațiilor în Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: e71102078832ac7d5f8e5edb40cc484df927eda4
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410377"
---
# <a name="activate-and-revise-a-project-quote"></a>Activați și revizuiți o ofertă de proiect

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Capacitățile de activare și revizuire vă ajută să urmăriți versiunea pentru cotațiile bazate pe proiecte în timpul fazelor de estimare și negociere. Când o versiune nefinalizată a unei cotații este activată, aceasta devine doar pentru citire.

Capacitățile de activare și revizuire vă permit să efectuați următoarele sarcini:

- Câștigă sau pierde ghilimele numai după activare.
- Revizuiți o ofertă fie pentru a modifica oferta existentă, fie pentru a crea o versiune nouă.

> [!NOTE]
> După ce funcția de activare și revizuire a ghilimelor este activată, aceasta nu poate fi dezactivată.

Pentru a activa capacitatea de a activa și revizui cotațiile bazate pe proiecte, urmați acești pași.

1. Mergi la **Setări** \> **Parametrii**.
1. Deschide **Parametrii** record.
1. În panoul de acțiuni, pe **Controlul caracteristicilor** filă, selectați **Activați activarea și revizuirea cotațiilor**.
1. În caseta de dialog de confirmare, selectați **OK**.
1. După câteva momente, reîmprospătați browserul. Capacitățile de activare și revizuire ar trebui să fie acum disponibile. Veți ști că aceste capabilități au fost activate dacă **Activați activarea și revizuirea cotațiilor** butonul nu mai apare în panoul de acțiuni.

## <a name="activating-a-quote"></a>Activarea unei cotații

După ce funcția de activare și revizuire a ghilimelor este activată, **Închideți citatul ca câștigat** și **Închide citatul ca pierdut** butoanele din panoul de acțiuni nu sunt disponibile pentru ofertele de proiect nefinalizate. Sunt disponibile numai după activarea unei cotații.

Activarea reprezintă etapa din procesul de cotație în care doriți să preveniți mai multe modificări ale cotației. În această etapă, oferta este trimisă spre revizuire internă sau către client.

The **Închideți citatul ca câștigat** și **Închide citatul ca pierdut** butoanele din panoul de acțiuni sunt disponibile pentru cotațiile activate. În funcție de rezultatul evaluării interne sau ale clienților, puteți folosi unul dintre aceste butoane pentru a închide o cotație activată. Puteți efectua negocieri și modificări asupra cotațiilor activate selectând **Revizuiește citatul**.

## <a name="revising-a-quote"></a>Revizuirea unui citat

Dacă trebuie să faceți modificări la o ofertă activată, selectați **Revizuiește citatul**. Citatul este închis, iar **revizuit** este folosit codul motiv. Se creează apoi o nouă cotație care are același ID și un număr de revizuire incrementat. Toate detaliile din oferta originală sunt copiate în noul citat. Noul cotație este în stare de proiect și poate fi editată după cum este necesar.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
