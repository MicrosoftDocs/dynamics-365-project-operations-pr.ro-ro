---
title: Gestionarea listelor de prețuri de vânzări și achiziții în Project Operations
description: Acest articol oferă informații care vă vor ajuta să creați și să mențineți date despre furnizori și liste de prețuri de achiziție pentru subcontractare.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3cd883fed8a59f1c54c39e2d051b9748833ba692
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261903"
---
# <a name="vendor-and-purchase-price-list-management-in-project-operations"></a>Gestionarea listelor de prețuri de vânzări și achiziții în Project Operations


_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_

## <a name="vendors-in-project-operations"></a>Furnizori în Project Operations

În Microsoft Dynamics 365 Project Operations, conturile de furnizor au un tip de relație **Vânzător** sau **Furnizor**. Puteți selecta doar o înregistrare de cont care are unul dintre aceste tipuri de relații ca furnizor pentru un subcontract.

Puteți asocia una sau mai multe liste de prețuri de achiziție cu o înregistrare de furnizor. Totuși, fiecare listă de prețuri de achiziție care este asociată cu o înregistrare a furnizorului ar trebui să aibă o dată de intrare în vigoare distinctă. Project Operations nu acceptă suprapunerea intrării în vigoare a datelor pe listele de prețuri de achiziție.

În mod implicit, următoarele câmpuri și concepte dintr-o înregistrare furnizor sunt utilizate pentru orice subcontract creat pentru furnizor:

- Termeni de plată
- Facturare către contact
- Persoană principală de contact

    > [!NOTE]
    > În mod implicit, contactul principal al furnizorului este utilizat ca manager de cont furnizor al subcontractului.

- Monedă
- Liste de prețuri de achiziție curente

## <a name="purchase-price-lists-in-project-operations"></a>Liste de prețuri achiziție în Project Operations

O listă de prețuri unde câmpul **Contextul** este setat la **Cumpărare** și este considerat o listă de prețuri de achiziție. Listele de prețuri de achiziție pot fi definite pentru a reprezenta un catalog de tarife de achiziție pentru timp, cheltuieli și materiale. Listele de prețuri de achiziție seamănă cu listele de prețuri și de vânzare din Project Operations. Următoarele concepte se aplică listelor de prețuri de achiziție în același mod în care se aplică listelor de costuri și prețuri de vânzare:

- **Data de intrare în vigoare** - Listele de prețuri de achiziție au dată de intrare în vigoare. Perioada de vigoare este reprezentată de câmpurile pentru data de începere și data de sfârșit de pe fiecare listă de prețuri. Timpul dintre data de începere și data de încheiere este perioada de efect a datei.
- **Monedă** - Moneda din antetul listei de prețuri este utilizată ca moneda în care sunt exprimate prețurile de cumpărare pentru forță de muncă, categorii de cheltuieli și produse din catalog.
- **Unitate de timp implicită** - Unitatea de timp implicită exprimă prețurile forței de muncă pentru achiziții. Câmpul unității de timp dintr-o listă de prețuri este utilizat numai pentru a furniza o valoare implicită. Această valoare poate fi modificată pe rândurile de prețuri ale rolurilor individuale.

Listele de prețuri de achiziție pot fi atașate la înregistrările furnizorilor ca asocieri cunoscute sub numele de liste de prețuri ale proiectelor. Aceste liste de prețuri sunt utilizate pentru a introduce prețuri implicite pe liniile de subcontractare. În mod implicit, atunci când mai multe liste de prețuri de achiziție sunt atașate la o înregistrare de furnizor, cea mai actuală listă de prețuri este utilizată pentru subcontractele create pentru furnizor. Numai listele de prețuri în care câmpul **Contextul** este setat la **Cumpărare** pot fi atașate la înregistrările furnizorilor.

### <a name="subcontract-specific-purchase-price-lists"></a>Liste de prețuri de achiziție specifice subcontractelor

Listele de prețuri de achiziție pot fi totodată atașate la subcontracte ca asocieri cunoscute sub numele de liste de prețuri ale proiectelor. Aceste liste de prețuri sunt utilizate pentru a introduce prețuri implicite pe liniile de subcontractare. În mod implicit, atunci când mai multe liste de prețuri de achiziție sunt atașate unui subcontract, fiecare trebuie să aibă o eficiență de dată distinctă. Project Operations nu acceptă listele de prețuri de achiziție care au date de efectivitate suprapuse. Numai listele de prețuri în care câmpul **Contextul** este setat la **Cumpărare** pot fi atașate la subcontracte.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
