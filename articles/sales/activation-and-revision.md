---
title: Activarea și revizuirea unei oferte de proiect
description: Acest articol oferă informații despre activarea și revizuirea ofertelor în Microsoft Dynamics 365 Project Operations.
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
# <a name="activate-and-revise-a-project-quote"></a>Activarea și revizuirea unei oferte de proiect

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Capacitățile de activare și revizuire vă ajută să urmăriți versiunea pentru ofertele bazate pe proiecte în timpul fazelor de estimare și negociere. Când o versiune nefinalizată a unei oferte este activată, aceasta devine doar pentru citire.

Capacitățile de activare și revizuire vă permit să efectuați următoarele sarcini:

- Câștigați sau pierdeți oferte numai după activare.
- Revizuiți o ofertă fie pentru a modifica oferta existentă, fie pentru a crea o versiune nouă.

> [!NOTE]
> După ce funcția de activare și revizuire a ofertelor este activată, aceasta nu poate fi dezactivată.

Pentru a activa capacitatea de a activa și revizui ofertele bazate pe proiecte, urmați acești pași.

1. Accesați **Setări** \> **Parametri**.
1. Deschideți înregistrarea **Parametri**.
1. În panoul de acțiuni, pe fila **Control funcții**, selectați **Permitere activare și revizuire oferte**.
1. În caseta de dialog de confirmare, selectați **OK**.
1. După câteva momente, reîmprospătați browserul. Capacitățile de activare și revizuire ar trebui să fie acum disponibile. Veți ști că aceste capabilități au fost activate dacă butonul **Permitere activare și revizuire pentru oferte** nu mai apare în Panoul de acțiuni.

## <a name="activating-a-quote"></a>Activarea uneioferte

După ce funcția de activare și revizuire a ofertelor este activată, butoanele **Închidere ofertă ca fiind câștigată** și **Închidere ofertă ca fiind pierdută** din Panoul de acțiuni nu sunt disponibile pentru ofertele de proiect nefinalizate. Sunt disponibile numai după activarea unei oferte.

Activarea reprezintă etapa din procesul de oferte în care doriți să preveniți mai multe modificări ale ofertei. În această etapă, oferta este trimisă spre revizuire internă sau către client.

Butoanele **Închidere ofetă ca fiind câștigată** și **Închidere ofertă ca fiind pierdută** din Panoul de acțiuni sunt disponibile pentru ofertele activate. În funcție de rezultatul evaluării interne sau a clienților, puteți folosi unul dintre aceste butoane pentru a închide o ofertă activată. Puteți efectua negocieri și modificări asupra ofertelor activate selectând **Revizuire ofertă**.

## <a name="revising-a-quote"></a>Revizuirea unei oferte

Dacă trebuie să faceți modificări la o ofertă activată, selectați **Revizuire ofertă**. Oferta este închisă, iar codul motivului **revizuit** este folosit. Se creează apoi o nouă ofertă care are același ID și un număr de revizuire incrementat. Toate detaliile din oferta originală sunt copiate în noua ofertă. Noua ofertă este în stare de proiect și poate fi editatădupă cum este necesar.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
