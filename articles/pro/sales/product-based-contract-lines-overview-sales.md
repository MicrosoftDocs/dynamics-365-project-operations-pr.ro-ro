---
title: Prezentare generală a liniilor de contract bazate pe produs - simplificat
description: Acest subiect oferă informații despre linii de contract pe bază de produs.
author: rumant
ms.date: 10/07/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 8006e90e0d4fdf02042f26b261775a92f87f47ca
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8598227"
---
# <a name="product-based-contract-lines-overview---lite"></a>Prezentare generală a liniilor de contract bazate pe produs - simplificat

_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_

Aveți posibilitatea să creați linii de contract bazate pe produse în Dynamics 365 Project Operations. Liniile de contract bazate pe produse pot fi linii create manual sau pot fi elemente din catalogul de produse.

## <a name="product-catalog"></a>Catalog de produse

Produsele din catalogul de produse au o unitate și un grup de unități implicite. Dacă mai multe produse partajează același set de atribute, puteți crea o familie de produse care are, de asemenea, aceste atribute. Toate produsele dintr-o familie de produse moștenesc același set de atribute.

De exemplu, o companie vinde licențe de abonament pentru mai multe feluri de software. Toate software-ul de abonament are următoarele două atribute:

- Numărul de utilizatori
- Durata abonamentului (în luni)

Pentru a menține acest tip de catalog, creați o familie de produse denumită **Abonament de software**. Adăugați atributele, **Număr de utilizatori** și **Durata abonamentului** la familia de produse. Apoi, adăugați produse individuale la familia de produse **Abonament de software**.

## <a name="add-product-catalog-items-to-a-project-contract"></a>Adăugați elementele catalogului de produse la un contract de proiect

Contractele de proiecte au secțiuni pentru două tipuri de linii, pe bază de proiect și pe bază de produs. Liniile bazate pe produse includ toate produsele și unitățile din lista de prețuri a produselor din contract. Pot fi adăugate produse care nu fac parte dintr-o listă de prețuri de produse de contract.

Puteți selecta produse din alte liste de prețuri sau direct din catalogul de produse. Când selectați produse direct dintr-un catalog de produse, lista de prețuri implicită a acelui produs este utilizată pentru a obține prețul de vânzare al produsului. Dacă nu este setată o listă de prețuri implicită, prețul este setat la 0 (zero).

Dacă o linie de contract se bazează pe un catalog de produse, aveți posibilitatea să înlocuiți prețul de vânzare direct în linie. O linie contractuală are câmpul **Prețuri** cu cele două valori:

- **Înlocuire stabilire preț**
- **Utilizați valoarea implicită**

Dacă configurați câmpul **Prețuri** la **Înlocuire preț**, prețul implicit nu este configurat. Introduceți un preț pentru produsul de pe linia de contract. Dacă setați câmpul la **Utilizare implicit**, se folosește prețul de vânzare implicit și câmpul nu poate fi editat.

După ce instalați Project Operations, prețurile de vânzare implicite sunt introduse pe liniile bazate pe produs pe un contract. Câmpul **Stabilire preț** este atunci configurat la **Înlocuire preț** astfel încât puteți edita prețul implicit pe liniile de contract. Aceasta este o suprascriere specifică Project Operations la comportamentul liniilor bazate pe produse în Dynamics 365 Sales.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]