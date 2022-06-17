---
title: Flux de lucru pentru gestionarea cheltuielilor
description: Acest articol explică cum puteți utiliza sistemul de flux de lucru în Microsoft Dynamics 365 Finanțe, pentru a stabili un proces de revizuire pentru rapoartele de cheltuieli în Gestionarea cheltuielilor.
author: ShylaThompson
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: johnmichalak
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 71efc89d9167ef1ee546c67c123efeb37125cc02
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929735"
---
# <a name="expense-management-workflow"></a>Flux de lucru pentru gestionarea cheltuielilor

Puteți utiliza sistemul fluxului de lucru pentru a stabili un proces de revizuire a rapoartelor de cheltuieli în gestionarea cheltuielilor. Puteți configura un flux de lucru care utilizează următoarele criterii pentru a determina cine aprobă rapoartele de cheltuieli:

- Ierarhia raportării angajaților și limitele de aprobare predefinite
- Aprobare pe mai multe niveluri care acceptă aprobatorii intermediari și un aprobator final
- Dimensiunile financiare și responsabilitatea proiectului
- Atribuirea pentru anumiți utilizatori sau grupuri de utilizatori

Aprobările fluxului de lucru pot fi create pentru rapoarte de cheltuieli, cereri de călătorie, avansuri de numerar și recuperarea taxei pe valoarea adăugată (TVA).

**Exemplu**

Următorul proces este un exemplu al fluxului de lucru de gestionare a cheltuielilor pentru un raport de cheltuieli.

1. Un angajat creează și salvează un raport de cheltuieli.
2. Angajatul transmite raportul de cheltuieli pentru aprobare. Aprobatorul este identificat pe baza regulilor care au fost definite atunci când a fost configurat fluxul de lucru.
3. Aprobatorul primește o notificare că un raport de cheltuieli este pregătit pentru aprobare. Aprobatorul examinează raportul de cheltuieli și verifică dacă sunt îndeplinite următoarele condiții:

    - Cheltuielile nu încalcă nicio politică de cheltuieli. Dacă o cheltuială încalcă o politică, aprobatorul verifică dacă raportul de cheltuieli include o justificare validă pentru afaceri.
    - Chitanțele electronice sunt atașate la raportul de cheltuieli.

4. Aprobatorul aprobă raportul de cheltuieli.
5. Raportul de cheltuieli este atribuit coordonatorului de conturi de furnizori pentru postare.
6. Unul dintre pașii următori are loc, în funcție de configurarea de postare automată:

    - Dacă este configurată postarea automată, raportul de cheltuieli este procesat pentru plată, iar starea raportului de cheltuieli este actualizată.
    - Dacă postarea automată nu este configurată, coordonatorul conturilor de furnizori verifică dacă toate chitanțele originale au fost depuse și că chitanțele sunt aliniate cu cheltuielile din raportul de cheltuieli. Toate codurile fiscale care sunt introduse în raportul de cheltuieli trebuie, de asemenea, verificate pentru corectitudine.

După verificarea acestor cerințe, raportul de cheltuieli este postat.

După postarea raportului de cheltuieli, plata este autorizată pentru raportul de cheltuieli, iar angajatul este rambursat.


[!INCLUDE[footer-include](../includes/footer-banner.md)]