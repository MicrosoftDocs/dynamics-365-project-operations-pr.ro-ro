---
title: Importul și menținerea tranzacțiilor cu cardul de credit
description: Acest subiect explică cum să importați și să mențineți tranzacțiile cu cardul de credit legate de cheltuieli. Aceste tranzacții pot fi configurate astfel încât să fie importate automat într-o planificare recurentă sau să poată fi importate manual, după cum sunt necesare.
author: KimANelson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvPbsMainDataLines
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: suvaidya
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 6cec15e436bc699e361577c970dd5845c6c68908
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082949"
---
# <a name="import-and-maintain-credit-card-transactions"></a>Importul și menținerea tranzacțiilor cu cardul de credit

[!include [banner](../includes/banner.md)]

Tranzacțiile legate de cheltuieli cu cardul de credit pot fi configurate astfel încât să fie importate automat într-un program recurent. Alternativ, tranzacțiile pot fi importate manual, după cum sunt necesare. Tranzacțiile cu cardul de credit sunt importate prin intermediul entității de date privind tranzacțiile cu cardul de credit.

Pentru mai multe informații despre entitățile de date, consultați [Entități de date](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities).

## <a name="import-credit-card-transactions"></a>Importați tranzacții cu cardul de credit

1. Pe pagina **Tranzacții cu cardul de credit** , selectați **Tranzacții de import**. Dacă deschideți gestionarea datelor pentru prima dată, sistemul trebuie să actualizeze lista entităților de date înainte de a putea continua.
2. În câmpul **Nume** , introduceți o descriere unică a lucrării de import.
3. În câmpul **Format de date sursă** , selectați formatul fișierului care conține tranzacțiile cu cardul de credit de importat.
4. Selectați **Încărcare** , apoi găsiți și selectați fișierul de importat.
5. După ce fișierul a fost încărcat, validați maparea fișierului tranzacției cu cardul de credit și coloanele entității de date privind tranzacțiile cu cardul de credit, selectând linkul **Vizualizare hartă** pe dală. Dacă există erori de mapare sau dacă trebuie să modificați maparea, efectuați modificările de mapare fie din fila **Vizualizare mapare** sau fila **Detalii de mapare**.
6. Pentru a automatiza tranzacțiile cu cardul de credit, selectați **Creați o operațiune de date recurente**. Puteți seta apoi recurența care definește cât de des ar trebui importate tranzacțiile cu cardul de credit. Când ați terminat, selectați **OK**.
7. Pentru a importa fișierul selectat acum, selectați **Import**.
8. Dacă apar erori în timpul importului, puteți vizualiza jurnalul de execuție sau datele de etapizare pentru a vedea erorile pe care trebuie să le remediați pentru a garanta un import reușit.

> [!NOTE]
> Dacă trebuie să importați mai mult de un format de fișier, trebuie să creați lucrări de import separate pentru fiecare tip de format.

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a>Reatribuiți tranzacțiile cu cardul de credit pentru angajații reziliați

După ce o înregistrare a angajatului este terminată, contul Active Directory Domain Services (AD DS) al angajatului este dezactivat. Cu toate acestea, ar putea exista tranzacții active cu cardul de credit care trebuie în continuare cheltuite și rambursate. De la pagina **Tranzacții cu cardul de credit** , puteți reatribui angajatul pentru orice tranzacție cu cardul de credit în cazul în care angajatul asociat a fost reziliat.

Selectați una sau mai multe tranzacții cu cardul de credit, apoi selectați **Reatribuiți tranzacțiile**. Apoi puteți selecta un alt angajat căruia să îi atribuiți tranzacțiile cu cardul de credit. După ce tranzacțiile cu cardul de credit au fost realocate, acestea pot fi selectate pentru un raport de cheltuieli și plătite prin procesul obișnuit de rambursare a raportului de cheltuieli.
