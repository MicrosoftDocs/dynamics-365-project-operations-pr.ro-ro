---
title: Configurarea integrării cardului de credit
description: Acest articol explică cum să lucrați cu tranzacțiile cu cardul de credit legate de cheltuieli.
author: suvaidya
ms.date: 11/17/2021
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4d32754548af67bdd5b9f7345f6363bd6193b36d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924510"
---
# <a name="set-up-credit-card-integration"></a>Configurarea integrării cardului de credit

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Tranzacțiile legate de cheltuieli cu cardul de credit pot fi configurate astfel încât să fie importate automat într-un program recurent. Alternativ, tranzacțiile pot fi importate manual, după cum sunt necesare. Tranzacțiile cu cardul de credit sunt importate prin intermediul entității de date privind tranzacțiile cu cardul de credit.

## <a name="import-credit-card-transactions"></a>Importați tranzacții cu cardul de credit

Pentru a importa tranzacții cu cardul de credit, urmați acești pași:

1. Pe pagina **Tranzacții cu cardul de credit**, selectați **Tranzacții de import**. Dacă deschideți gestionarea datelor pentru prima dată, sistemul trebuie să actualizeze lista de entități de date înainte de a putea continua.
2. În câmpul **Nume**, introduceți o descriere unică pentru operațiunea de import.
3. În câmpul **Format de date sursă**, selectați formatul fișierului care conține tranzacțiile cu cardul de credit de importat.
4. Selectați **Încărcare**, apoi găsiți și selectați fișierul de importat.
5. După ce fișierul a fost încărcat, validați maparea fișierului tranzacției cu cardul de credit și coloanele entității de date privind tranzacțiile cu cardul de credit, selectând linkul **Vizualizare hartă** pe dală. Dacă există erori de mapare sau dacă trebuie să modificați maparea, efectuați modificările de mapare fie din fila **Vizualizare mapare** sau fila **Detalii de mapare**.
6. Pentru a automatiza tranzacțiile cu cardul de credit, selectați **Creați o operațiune de date recurente**. Puteți seta apoi recurența care definește cât de des ar trebui importate tranzacțiile cu cardul de credit. Când ați terminat, selectați **O.K**.
7. Pentru a importa fișierul selectat acum, selectați **Import**.
8. Dacă apar erori în timpul importului, puteți vizualiza jurnalul de execuție sau datele de etapizare pentru a vedea erorile pe care trebuie să le remediați pentru a vă asigura importul cu succes.

> [!NOTE]
> Dacă trebuie să importați mai mult de un format de fișier, trebuie să creați operațiuni de import separate pentru fiecare tip de format.

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a>Reatribuiți tranzacțiile cu cardul de credit pentru angajații reziliați

După ce o înregistrare a angajatului este încheiată, contul Active Directory Domain Services (AD DS) al angajatului este dezactivat. Cu toate acestea, ar putea exista tranzacții active cu cardul de credit care trebuie în continuare cheltuite și rambursate. Pe pagina **Tranzacții cu cardul de credit**, puteți reatribui angajatul pentru orice tranzacție cu cardul de credit în cazul în care angajatul asociat a fost reziliat.

Selectați una sau mai multe tranzacții cu cardul de credit, apoi selectați **Reatribuiți tranzacțiile**. Apoi puteți selecta un alt angajat căruia să îi atribuiți tranzacțiile cu cardul de credit. După ce tranzacțiile cu cardul de credit au fost realocate, acestea pot fi selectate pentru un raport de cheltuieli și plătite prin procesul obișnuit de rambursare a raportului de cheltuieli.

## <a name="delete-credit-card-transactions"></a>Ștergeți tranzacțiile cu cardul de credit 

Uneori, după importul tranzacțiilor cu cardul de credit, este posibil să fie necesară ștergerea anumitor tranzacții. Acest lucru se poate datora faptului că tranzacțiile sunt duplicate sau pentru că datele nu sunt exacte. Administratorii pot utiliza caracteristica **„Ștergeți tranzacțiile cu cardul de credit”** pentru a selecta și șterge tranzacțiile cu cardul de credit care sunt **nu este atașat** la un raport de cheltuieli. 

1. Accesați **Sarcini periodice** > **Ștergeți tranzacțiile cu cardul de credit**.
2. Selectați **Filtru** și furnizați informații pentru a identifica înregistrările de inclus.
3. Selectați **OK** pentru a șterge înregistrările. 

## <a name="storing-credit-card-numbers"></a>Stocarea numerelor de card de credit

Sunt disponibile trei opțiuni pentru stocarea numerelor de card de credit. Numerele cardurilor de credit sunt stocate pe **Parametrii de management al cheltuielilor** pagină.

- **Preveniți introducerea numărului de card** – Numerele cardurilor de credit nu sunt stocate.
- **Numere de card hash (stocareazã ultimele patru cifre)** – Ultimele patru cifre ale numerelor cardului de credit sunt stocate într-un format criptat.
- **Păstrați numere de card** – Numerele cardurilor de credit sunt stocate într-un format necriptat. Această opțiune nu respectă standardul de securitate a datelor (DSS) pentru industria cardurilor de plată (PCI). Prin urmare, pentru a menține organizația în conformitate cu reglementările PCI DSS, administratorii organizației ar trebui să aleagă fie să nu stocheze numerele cardurilor de credit, fie să stocheze numerele de card hash.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
