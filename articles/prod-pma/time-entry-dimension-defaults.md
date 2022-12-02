---
title: Valori implicite pentru dimensiunile financiare pentru înregistrările de timp ale proiectului
description: Acest articol oferă informații despre modul în care dimensiunile financiare implicite sunt aplicate intrărilor de timp.
author: stsporen
ms.date: 01/24/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 9863738a2d6d0e001961554043939f62f65d9ce5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916579"
---
# <a name="defaulting-financial-dimensions-for-project-time-entries"></a>Valori implicite pentru dimensiunile financiare pentru înregistrările de timp ale proiectului

[!include [banner](../includes/banner.md)]

Când utilizați dimensiuni financiare pentru intrările de timp ale proiectului, valoarea implicită a dimensiunii este evaluată în următoarea ordine:

1. Resursă
2. Project
3. Sursă de finanțare

De exemplu, dacă dimensiunea implicită este specificată pe o resursă, valoarea implicită este aplicată peste valoarea implicită care este specificată pentru proiect. De asemenea, dacă dimensiunea implicită este specificată într-un proiect, valoarea implicită este aplicată peste valoarea implicită care este specificată pentru sursa de finanțare.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
