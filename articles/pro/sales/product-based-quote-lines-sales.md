---
title: Prezentare generală a liniilor de oferte bazate pe produs - simplificat
description: Acest subiect oferă informații despre lucrul cu linii de ofertă bazate pe produs.
author: rumant
ms.date: 10/30/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: 8b904f9abd3d2505c5397906f63a5ae8ff4be41b
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369841"
---
# <a name="product-based-quote-lines-overview---lite"></a>Prezentare generală a liniilor de oferte bazate pe produs - simplificat

_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_

Aveți posibilitatea să creați linii de ofertă bazate pe produse în Dynamics 365 Project Operations. Liniile de ofertă bazate pe produse pot fi adăugate manual sau pot fi elemente din catalogul de produse.

## <a name="product-catalog"></a>Catalog de produse

Fiecare produs din catalogul de produse are o unitate implicită și un grup de unități. Dacă mai multe produse partajează același set de atribute, puteți crea o familie de produse care partajează, de asemenea, aceste atribute. 

De exemplu, o companie vinde licențe de abonament pentru mai multe feluri de software. Toate software-ul de abonament are următoarele două atribute:

- Numărul de utilizatori
- Durata unui abonament măsurată în luni

Pentru a întreține acest tip de catalog, creați o familie de produse numită **Software de abonament** și adăugați numărul de utilizatori și durata abonamentului ca atribute. Apoi, puteți adăuga produse individuale la familia de produse **Software de abonament**.

## <a name="add-product-catalog-items-to-a-project-quote"></a>Adăugați elemente din catalogul de produse la o ofertă de proiect

Paginile **Ofertă de proiect** și **Contractul de proiect** au secțiuni pentru linii pe bază de proiect și linii pe bază de produs. Pentru linii pe bază de produs, lista verticală din linia ofertei sau din linia de contract de proiect include toate produsele și unitățile din lista de prețuri a produsului. De asemenea, aveți posibilitatea să adăugați produse care nu fac parte din lista de prețuri a produsului.

În plus, puteți selecta produse din alte liste de prețuri sau direct din catalogul de produse. Când selectați produse direct dintr-un catalog de produse, lista de prețuri implicită a acelui produs este utilizată pentru a obține prețul de vânzare al produsului. Dacă nu este setată o listă de prețuri implicită, prețul este setat la zero (0).

Când o linie de ofertă se bazează pe un catalog de produse, aveți posibilitatea să înlocuiți prețul de vânzare direct în linia de ofertă. O linie de ofertă în câmpul **Prețuri** cu două valori disponibile:

- **Înlocuire stabilire preț**
- **Utilizare valoare implicită**

Dacă selectați **Înlocuiți prețurile**, prețul implicit nu este setat. În schimb, trebuie să introduceți un preț pentru produs în linia de ofertă. Dacă selectați **Utilizare implicit**, se folosește prețul de vânzare implicit și câmpul este blocat pentru editare.

Prețurile de vânzare implicite sunt introduse pe liniile bazate pe produs ale unei oferte. Câmpul **Stabilire preț** este atunci configurat la **Înlocuire preț** astfel încât puteți edita prețul implicit pe liniile de ofertă. Aceasta este o suprascriere specifică Project Operations la comportamentul liniilor bazate pe produs în Dynamics 365 Sales.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]