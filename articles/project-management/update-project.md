---
title: Actualizarea unui proiect
description: Acest subiect furnizează informații despre actualizarea proiectelor în Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 27444b072bdf7de55d6b38c30c1ea5fe66ed46ac
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286398"
---
# <a name="update-a-project"></a>Actualizarea unui proiect

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Mai jos este un rezumat al câmpurilor care pot fi actualizate pe un proiect după ce a fost creat și orice implicații aplicabile ale actualizărilor.

## <a name="project-detail-fields"></a>Câmpuri de detaliu ale proiectului

- **Nume**: titlul proiectului.
- **Descriere**: o prezentare generală a proiectului.
- **Client**: Compania căreia îi va fi livrat proiectul.
- **Șablon de calendar**: orele de lucru ale proiectului. Când câmpul este schimbat, întreaga planificare este recalculată.
- **Monedă**: moneda pentru proiect. Acest câmp implicit se bazează pe moneda definită în unitatea contractantă. Când unitatea contractantă este actualizată, câmpul este, de asemenea, actualizat.
- **Unitate contractantă**: unitatea organizațională care reprezintă grupul de firme sau divizia care este principalul responsabil cu câștigarea vânzării și cu gestionarea livrării de lucrări și servicii către client. 
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