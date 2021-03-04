---
title: Linii de oferte bazate pe produs
description: Acest subiect oferă informații despre linii de ofertă pe bază de produs.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: a5b52e74994a40b20353d85d1d9bcd59d435cd0b
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/10/2021
ms.locfileid: "5151268"
---
# <a name="product-based-quote-lines"></a>Linii de oferte bazate pe produs

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


Aveți posibilitatea să creați linii de ofertă bazate pe produse în Dynamics 365 Project Service Automation. Liniile de ofertă bazate pe produse pot fi linii din afara catalogului sau pot fi elemente din catalogul de produse.

## <a name="product-catalog"></a>Catalog de produse

Produsele dintr-un catalog de produse Dynamics 365 au o unitate și un grup de unități implicite. Dacă mai multe produse partajează același set de atribute, puteți crea o familie de produse care are, de asemenea, aceste atribute. Toate produsele dintr-o familie de produse moștenesc același set de atribute.

De exemplu, o companie vinde licențe de abonament pentru o varietate de software. Toate software-ul de abonament are următoarele două atribute:

- Număr de utilizatori 
- Durata abonamentului (în luni)

O modalitate bună de a menține acest tip de catalog este de a crea o familie de produse care este denumită **Software de abonament** și care are **Număr de utilizatori** și **Durata abonamentului** ca atribute. Apoi, puteți adăuga produse individuale, cum ar fi **Dynamics 365 Sales** sau **Dynamics 365 Field Service** la familia de produse **Software de abonament**.

## <a name="adding-product-catalog-items-to-a-project-quote"></a>Adăugarea elementelor din catalogul de produse la o ofertă de proiect

Oferta de proiect și paginile contractului de proiect au secțiuni pentru două tipuri de linii: linii pe bază de proiect și linii pe bază de produs. Pentru liniile bazate pe produse, Dynamics 365 este utilizat pentru a adăuga elemente dintr-un catalog de produse la o ofertă. Lista verticală din linia ofertei sau din linia de contract de proiect include toate produsele și unitățile din lista de prețuri a produsului care este atașată la ofertă sau la contractul de proiect. De asemenea, aveți posibilitatea să adăugați produse care nu fac parte din lista de prețuri a produsului citat.

În plus, puteți selecta produse din alte liste de prețuri sau puteți selecta produse direct din catalogul de produse. Când selectați produse direct dintr-un catalog de produse, lista de prețuri implicită a acelui produs este utilizată pentru a obține prețul de vânzare al produsului. Dacă nu este setată o listă de prețuri implicită, prețul este setat la 0 (zero).

Dacă o linie de ofertă se bazează pe un catalog de produse, aveți posibilitatea să înlocuiți prețul de vânzare direct în linia de ofertă. Rețineți că o linie de ofertă în Dynamics 365 are un câmp de **Prețuri**. Sunt disponibile două valori:

- Înlocuire stabilire preț  
- Utilizați valoarea implicită

Dacă setați acest câmp pentru **Înlocuire stabilire preț**, Dynamics 365 nu configurează un preț implicit. Trebuie să introduceți un preț pentru produs în linia de ofertă. Dacă setați acest câmp pentru a **Utiliza implicit**, Dynamics 365 utilizează prețul implicit de vânzare și blochează câmpul pentru a preveni editarea.

După ce instalați PSA, prețurile de vânzare implicite sunt introduse pe liniile bazate pe produs pe o ofertă. Câmpul **Stabilire preț** este atunci configurat la **Înlocuire stabilire preț** astfel încât puteți edita prețul implicit pe liniile de ofertă.

> ![Configurare înlocuire stabilire preț](media/basic-guide-10.png)
 
## <a name="quantity-factors-for-products"></a>Factori de cantitate pentru produse

PSA utilizează factori de cantitate pentru a asista vânzarea de produse pe bază de abonament. Pentru produsele bazate pe abonament, cantitatea din linia de contract de ofertă sau de proiect este exprimată ca număr de luni de utilizare.

De obicei, prețul software-ului de abonament este stocat în catalogul ca prețul pe utilizator pe lună. Cu toate acestea, puteți utiliza alte descrieri de timp în schimb. În timpul procesului de vânzări, prețul de pe linia de ofertă este, de obicei, prețul per utilizator, pe lună, care a fost negociat și actualizat de către agentul de vânzări IT. Fiecare afacere are un număr diferit de utilizatori și un număr diferit de luni de abonament. Cantitatea utilizată pentru a calcula suma liniei de ofertă este un produs al numărului de utilizatori și numărul de luni de abonament.

Pentru a sprijini acest tip de vânzare, PSA a introdus conceptul de factori de cantitate. Factorii de cantitate se bazează pe atributele produsului în Dynamics 365. Când configurați proprietăți specifice pentru un produs, PSA vă permite să semnalizați un subset al acelor proprietăți sau toate proprietățile, ca factori de cantitate.

PSA validează că numai proprietățile numerice sau proprietățile produsului care au un tip de date numerice sunt marcate ca factori de cantitate. Când un produs pentru care sunt configurate factori de cantitate este adăugat la o linie de ofertă câmpul **Cantitate** din linia de ofertă devine un câmp doar în citire. După ce introduceți valori pentru proprietățile produsului care sunt factori de cantitate, PSA calculează cantitatea liniei de ofertă.

De exemplu, Dynamics 365 poate avea următoarele proprietăți: 

- **Nr. de utilizatori** - numărul de utilizatori 
- **Nr. de luni** - numărul de luni de abonament
- **Produs SKU** 

Proprietățile **Nr. de utilizatori** și **Nr. de luni** pot fi marcate ca factori de cantitate prin editarea proprietăților de linie de produs. 

> ![Semnalizarea Nr. de utilizatori și Nr. de luni ca factori de calitate](media/basic-guide-11.png)
 


[!INCLUDE[footer-include](../includes/footer-banner.md)]