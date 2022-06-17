---
title: Creați și actualizați un proiect
description: Acest articol oferă informații despre actualizarea proiectelor Operațiuni de proiect.
author: ruhercul
ms.date: 10/20/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: dcb822a726f94a7e8e8621dc7a04f9051168d361
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911105"
---
# <a name="create-and-update-a-project"></a>Creați și actualizați un proiect

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Următorul este un rezumat al câmpurilor care pot fi actualizate pe un proiect după ce acesta a fost creat. Aceasta include, de asemenea, orice implicații aplicabile bazate pe aceste actualizări.

## <a name="project-detail-fields"></a>Câmpuri de detaliu ale proiectului

- **Nume**: titlul proiectului.
- **Descriere**: o prezentare generală a proiectului.
- **Client**: Compania căreia îi va fi livrat proiectul.
- **Șablon de calendar**: orele de lucru ale proiectului. Când câmpul este schimbat, întreaga planificare este recalculată.
- **Monedă**: moneda pentru proiect. Valoarea implicită pentru acest câmp se bazează pe moneda definită în unitatea contractantă. Când unitatea contractantă este actualizată, câmpul este, de asemenea, actualizat.
- **Unitate contractantă**: unitatea organizațională care reprezintă grupul de firme sau divizia care este principalul responsabil cu câștigarea vânzării și cu gestionarea livrării de lucrări și servicii către client.  Când unitatea organizațională a managerului de proiect nu este definită, acest câmp este implicit la valoarea definită în parametrii proiectului.
- **Manager de proiect**: membru al echipei de proiect care are autoritatea de a revizui și aproba intrările și cheltuielile de timp.

## <a name="estimate-fields"></a>Câmpuri de estimare

- **Data estimată de începere**: data la care va începe proiectul. Când acest câmp este actualizat, orice sarcini din proiect se vor muta proporțional cu data de începere nouă.
- **Data de finalizare**: data la care proiectul este programat să se încheie.
- **Efort**: efortul estimat al proiectului. Când sarcinile sunt adăugate la proiect, acest câmp nu mai poate fi modificat.
- **Costul estimat al forței de muncă**: costul estimat al forței de muncă al proiectului. Când costurile cu forța de muncă sunt adăugate la proiect, acest câmp nu mai poate fi modificat.
- **Cheltuieli estimate**: cheltuielile estimate ale proiectului. Când cheltuielile sunt adăugate la proiect, acest câmp nu mai poate fi modificat.

## <a name="project-actual-fields"></a>Proiectați câmpurile reale
- **Start efectiv**: data la care a început proiectul.
- **Finalizare efectivă**: pentru a fi actualizat la finalizarea unui proiect.

## <a name="project-status-fields"></a>Câmpuri de stare proiect

- **Starea generală a proiectului**: starea generală a proiectului oferită de managerul de proiect.
- **Comentarii**: o narațiune privind starea actuală a proiectului oferită de managerul de proiect.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
