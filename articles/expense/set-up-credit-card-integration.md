---
title: Configurarea integrării cardului de credit
description: Acest subiect explică cum să importați și să mențineți tranzacțiile cu cardul de credit legate de cheltuieli.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 483775e1334a281026dbfaf214d06d235255f13e
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896836"
---
# <a name="set-up-credit-card-integration"></a>Configurarea integrării cardului de credit

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Tranzacțiile legate de cheltuieli cu cardul de credit pot fi configurate astfel încât să fie importate automat într-un program recurent. Alternativ, tranzacțiile pot fi importate manual, după cum sunt necesare. Tranzacțiile cu cardul de credit sunt importate prin intermediul entității de date privind tranzacțiile cu cardul de credit.

## <a name="import-credit-card-transactions"></a>Importați tranzacții cu cardul de credit

1. Pe pagina **Tranzacții cu cardul de credit**, selectați **Tranzacții de import**. Dacă deschideți gestionarea datelor pentru prima dată, sistemul trebuie să actualizeze lista entităților de date înainte de a putea continua.
2. În câmpul **Nume**, introduceți o descriere unică a lucrării de import.
3. În câmpul **Format de date sursă**, selectați formatul fișierului care conține tranzacțiile cu cardul de credit de importat.
4. Selectați **Încărcare**, apoi găsiți și selectați fișierul de importat.
5. După ce fișierul a fost încărcat, validați maparea fișierului tranzacției cu cardul de credit și coloanele entității de date privind tranzacțiile cu cardul de credit, selectând linkul **Vizualizare hartă** pe dală. Dacă există erori de mapare sau dacă trebuie să modificați maparea, efectuați modificările de mapare fie din fila **Vizualizare mapare** sau fila **Detalii de mapare**.
6. Pentru a automatiza tranzacțiile cu cardul de credit, selectați **Creați o operațiune de date recurente**. Puteți seta apoi recurența care definește cât de des ar trebui importate tranzacțiile cu cardul de credit. Când ați terminat, selectați **OK**.
7. Pentru a importa fișierul selectat acum, selectați **Import**.
8. Dacă apar erori în timpul importului, puteți vizualiza jurnalul de execuție sau datele de etapizare pentru a vedea erorile pe care trebuie să le remediați pentru a garanta un import reușit.

> [!NOTE]
> Dacă trebuie să importați mai mult de un format de fișier, trebuie să creați lucrări de import separate pentru fiecare tip de format.

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a>Reatribuiți tranzacțiile cu cardul de credit pentru angajații reziliați

După ce o înregistrare a angajatului este terminată, contul Active Directory Domain Services (AD DS) al angajatului este dezactivat. Cu toate acestea, ar putea exista tranzacții active cu cardul de credit care trebuie în continuare cheltuite și rambursate. De la pagina **Tranzacții cu cardul de credit**, puteți reatribui angajatul pentru orice tranzacție cu cardul de credit în cazul în care angajatul asociat a fost reziliat.

Selectați una sau mai multe tranzacții cu cardul de credit, apoi selectați **Reatribuiți tranzacțiile**. Apoi puteți selecta un alt angajat căruia să îi atribuiți tranzacțiile cu cardul de credit. După ce tranzacțiile cu cardul de credit au fost realocate, acestea pot fi selectate pentru un raport de cheltuieli și plătite prin procesul obișnuit de rambursare a raportului de cheltuieli.
