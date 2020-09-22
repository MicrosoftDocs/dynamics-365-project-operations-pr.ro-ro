---
title: Creare intrări de timp
description: Acest subiect oferă informații despre modul de creare a intrărilor de timp.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 05/20/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 90f6450b-e0c4-4d86-b8f5-ffb1a2b1e38a
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: ae3af7d62d93884c7fa9881394b7129daeb8bf7e
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754788"
---
# <a name="create-time-entries"></a>Creare intrări de timp

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

În versiunile anterioare de Dynamics 365 Project Service Automation, intrările de timp erau introduse săptămânal. În versiunea 3 a Project Service Automation, intrările de timp sunt introduse zilnic. Cu toate acestea, după ce au fost create câteva intrări de timp, aveți posibilitatea să le creați sau să le copiați în vrac.

## <a name="create-a-time-entry"></a>Creați o intrare de timp

Urmați acești pași pentru a crea o intrare de timp.

1. În pagina **Intrări timp**, selectați **Nou**.
2. În caseta de dialog **Creare rapidă: intrare timp**, introduceți durata intrării de timp în minute, ore sau zile. Durata trebuie introdusă în formatul următor: *x* minute, *x* ore sau *x* zile. Orele și zilele pot fi introduse și ca valori zecimale, de exemplu, *x.x* ore sau *x.x* zile.
3. Selectați tipul de intrare de timp și proiectul în care introduceți intrarea de timp.
4. În câmpul **Activitate proiect**, găsiți activitatea pentru această intrare de timp.

    > [!NOTE]
    > Dacă creați o intrare de timp pentru o activitate care nu este atribuită unui utilizator, în câmpul **activitate proiect**, selectați butonul **Căutare**, selectați **Schimbare vizualizare**, apoi selectați **Toate activitățile de proiect active** pentru a lista toate activitățile.

5. Introduceți o descriere, dacă este necesară o descriere, apoi selectați **Salvare și închidere**.

După ce intrarea de timp este creată și salvată, o puteți edita în grila de intrare de timp. Grila de intrare de timp acceptă două formate:

- Aveți posibilitatea să introduceți intrările de timp în format **hh:mm**. Acest format este apoi convertit în ore și fracții.
- Aveți posibilitatea să introduceți direct ore și fracții.

Rețineți că fracțiunile unei ore nu sunt minute. Prin urmare, 1,5 ore reprezintă 1 oră și 30 de minute. Aceeași regulă se aplică fracțiunilor unei zile. O zi este de 24 de ore, iar 0,5 zile reprezintă 12 ore.

## <a name="bulk-create-time-entries"></a>Creare în bloc de intrări de timp

După ce au fost create câteva înregistrări de timp, le puteți copia pentru a crea în bloc înregistrări de timp suplimentare.

1. În pagina **Intrări timp**, selectați **Copiere săptămână**.
2. În grupul de câmpuri **De la perioada**, în câmpurile **Data de început** și **Data de sfârșit**, definiți intervalul de date din care să copiați înregistrările de timp.
3. În grupul de câmpuri **Până la perioada**, în câmpul **Data de început**, specificați data pentru care să creați înregistrări de timp.
4. Selectați **Copiere** pentru a crea o copie a intrărilor de timp care corespund zilei săptămânii indicate în grupul de câmpuri **Până la perioada**. De exemplu, înregistrarea de timp pentru ziua de luni de săptămâna trecută este copiată pentru lunea săptămânii indicate în grupul de câmpuri **Până la perioada**.

## <a name="import-data-for-time-entries"></a>Importați date pentru intrările de timp

Aveți posibilitatea să importați date din rezervările și activitățile de proiect. Când importați date, aveți posibilitatea să specificați intervalul de date al rezervărilor de importat și apoi să selectați în mod explicit rezervările care ar trebui create ca intrări de timp **Schiță**.

## <a name="group-by-sort-search-and-filter-capabilities"></a>Grupați după, sortați, căutați și filtrați capacități

Aveți posibilitatea să grupați și să filtrați intrările de timp după dimensiunile specificate în coloane. În câmpul **Grupare după**, selectați dimensiunea de utilizat pentru filtrarea intrărilor de timp. De asemenea, aveți posibilitatea să sortați înregistrările de intrări de timp în ordine crescătoare sau descrescătoare utilizând săgeata de sortare de pe titlurile coloanelor. În plus, aveți posibilitatea să afișați sau să ascundeți intrările selectând butonul **Filtru** de pe titlurile coloanelor, apoi, în caseta **Căutare**, introduceți textul care ar trebui utilizat pentru a căuta intrările de timp după numele proiectului, activitatea proiectului, intrarea de timp sau resursă.
