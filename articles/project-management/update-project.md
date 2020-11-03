---
title: Actualizarea unui proiect
description: Acest subiect furnizează informații despre actualizarea proiectelor în Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 5c9cd0c7c6886bd454c5f2ef2ae7f20d1707293f
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082651"
---
# <a name="update-a-project"></a>Actualizarea unui proiect

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Mai jos este un rezumat al câmpurilor care pot fi actualizate pe un proiect după ce a fost creat și orice implicații aplicabile ale actualizărilor.

## <a name="project-detail-fields"></a>Câmpuri de detaliu ale proiectului

- **Nume** : titlul proiectului.
- **Descriere** : o prezentare generală a proiectului.
- **Client** : Compania căreia îi va fi livrat proiectul.
- **Șablon de calendar** : orele de lucru ale proiectului. Când câmpul este schimbat, întreaga planificare este recalculată.
- **Monedă** : moneda pentru proiect. Acest câmp implicit se bazează pe moneda definită în unitatea contractantă. Când unitatea contractantă este actualizată, câmpul este, de asemenea, actualizat.
- **Unitate contractantă** : unitatea organizațională care reprezintă grupul de firme sau divizia care este principalul responsabil cu câștigarea vânzării și cu gestionarea livrării de lucrări și servicii către client. 
- **Manager de proiect** : membru al echipei de proiect care are autoritatea de a revizui și aproba intrările și cheltuielile de timp.

## <a name="estimate-fields"></a>Câmpuri de estimare

- **Data estimată de începere** : data la care va începe proiectul. Când acest câmp este actualizat, orice sarcini din proiect se vor muta proporțional cu data de începere nouă.
- **Data de finalizare** : data la care proiectul este programat să se încheie.
- **Efort** : efortul estimat al proiectului. Când sarcinile sunt adăugate la proiect, acest câmp nu mai poate fi modificat.
- **Costul estimat al forței de muncă** : costul estimat al forței de muncă al proiectului. Când costurile cu forța de muncă sunt adăugate la proiect, acest câmp nu mai poate fi modificat.
- **Cheltuieli estimate** : cheltuielile estimate ale proiectului. Când cheltuielile sunt adăugate la proiect, acest câmp nu mai poate fi modificat.

## <a name="project-actual-fields"></a>Proiectați câmpurile reale
- **Start efectiv** : data la care a început proiectul.
- **Finalizare efectivă** : pentru a fi actualizat la finalizarea unui proiect.

## <a name="project-status-fields"></a>Câmpuri de stare proiect

- **Starea generală a proiectului** : starea generală a proiectului oferită de managerul de proiect.
- **Comentarii** : o narațiune privind starea actuală a proiectului oferită de managerul de proiect.

