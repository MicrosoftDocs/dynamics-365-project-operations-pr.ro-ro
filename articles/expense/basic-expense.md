---
title: Intrare cheltuieli (simplificată)
description: Acest articol oferă informații despre cum să lucrați cu intrarea de cheltuieli într-o implementare simplificată.
author: stsporen
ms.date: 11/19/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: b69cc4ec0a4b51cd1d27f8b8a4a94248ae884797
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8917959"
---
# <a name="expense-entry-lite"></a>Intrare cheltuieli (simplificată)

_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_

Gestionarea cheltuielilor de bază sau simplă este capacitatea de a înregistra cheltuieli simple. Puteți înregistra cheltuielile pentru un proiect, iar apoi aprobatorul de proiect le va revizui și aproba.

Pentru mai multe informații despre capacitățile de cheltuieli din Dynamics 365 Project Operations, consultați [Prezentare generală a cheltuielilor](expense-overview.md).

## <a name="capture-a-basic-expense"></a>Captează o cheltuială de bază

Vă puteți captura cheltuielile, astfel încât să le puteți trimite aprobatorului.

1. Accesați **Cheltuieli** și selectați **Nou**.
2. Pe pagina **Cheltuieli noi**, introduceți informațiile necesare despre cheltuieli, apoi selectați **Salvați**.

## <a name="submit-a-basic-expense"></a>Remite o cheltuială de bază

După ce ați terminat de capturat toate cheltuielile și sunteți gata să le aprobați, trebuie să le trimiteți.

1. Accesați **Cheltuieli** și selectați o cheltuială. Sau selectați toate cheltuielile folosind caseta de selectare din antet.
2. Selectați **Remitere**. Sistemul procesează intrările selectate și apoi creează cereri de aprobare a cheltuielilor.

## <a name="add-an-attachment"></a>Adăugați o atașare

Este posibil să trebuiască să furnizați aprobatorului documentație suplimentară despre cheltuielile dvs. Puteți atașa o chitanță în cronologia înregistrării cheltuielilor. Selectați **Editați** iar în secțiunea **Cronologie**, apoi selectați pictograma agrafă pentru a atașa chitanța.

## <a name="recall-a-basic-expense"></a>Retrageți o cheltuială de bază

Când trimiteți o cheltuială din greșeală, o puteți retrage. Timpul necesar pentru recuperarea unei înregistrări de cheltuieli depinde de etapa de aprobare a acesteia.  Dacă aprobatorul nu a aprobat încă înregistrarea, retragerea poate avea loc imediat. Cu toate acestea, dacă înregistrarea a fost deja aprobată, aprobatorului i se cere să aprobe retragerea și să inverseze tranzacțiile.

1. Accesați **Cheltuieli**, apoi, în lista de cheltuieli, selectați cheltuiala de retras.
2. Selectați **Retragere**. Dacă înregistrarea cheltuielilor nu a fost încă aprobată, sistemul o retrage imediat. Dacă înregistrarea cheltuielilor a fost deja aprobată, se creează o cerere de retragere pentru a notifica aprobatorului că doriți să inversați cheltuielile. Aprobatorul va confirma apoi că se poate face inversarea, iar intrarea va fi returnată.

## <a name="delete-a-basic-expense"></a>Șterge o cheltuială de bază

Cheltuielile care nu au fost încă trimise pot fi șterse. Pentru a șterge o cheltuială care a fost deja trimisă, trebuie mai întâi să o retrageți.

## <a name="see-also"></a>Consultați și

- [Prezentare generală a aprobărilor](../approvals/approvals-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]