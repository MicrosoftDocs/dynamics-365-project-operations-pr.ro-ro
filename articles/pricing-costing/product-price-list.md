---
title: Liste de prețuri pentru produse
description: Acest subiect oferă informații despre listele de prețuri din prețurile de catalog utilizate pentru ofertele de proiecte și contracte.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 8bfd4eaa6f4bcbbdf398683a25a3b0079cfedd535ef32d383993883607f7ef5a
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/06/2021
ms.locfileid: "6999241"
---
# <a name="product-price-lists"></a>Liste de prețuri pentru produse

_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_

 În Project Operations, **Listele de prețuri ale produselor** și entitățile de articole din lista de prețuri conexe acceptă funcționalitatea pentru stabilirea prețurilor produselor pe linii de ofertă și contract pe bază de produse. Pentru produsele utilizate în proiecte, sunt utilizate înregistrările articolelor din lista de prețuri pentru listele de prețuri ale proiectelor. 

Produsele trebuie să fie configurate astfel încât să aibă cost implicit și liste de prețuri în catalogul de produse. Utilizați prețul de listă, costul standard și costul actual pentru a configura costul implicit și prețul de listă. Prețurile de listă implicite sunt utilizate pe o linie de ofertă sau pe o linie de contract de proiect numai când sistemul nu găsește o linie de listă de prețuri pentru acel produs în lista de prețuri a produsului pentru ofertă sau contractul de proiect.

Prețul de cost al liniilor de catalog de produse poate fi modificat între oferte. Această capacitate este importantă, pentru că dacă nu urmăriți cu acuratețe costurile, nu puteți determina profiturile operaționale pe angajamente de proiect. În mod implicit, costul standard al produsului este utilizat ca preț de cost. Cu toate acestea, prețul implicit de cost poate fi actualizat pe linia de ofertă dacă există un preț de cost diferit pentru acea ofertă.

## <a name="price-list-items"></a>Element listă de prețuri

Puteți adăuga produse dintr-un catalog de produse la diferite liste de prețuri. Liniile de listă de prețuri pentru produse se referă întotdeauna la o anumită unitate. Prețurile pentru un produs pe elementele listei de prețuri pot fi configurate ca o valoare monetară. Alternativ, acesta poate fi configurat ca o funcție a prețului listei, costului curent sau costului standard.

Funcționalitatea de prețuri acceptă diverse opțiuni de rotunjire atunci când prețurile produselor sunt configurate ca o funcție a prețului de listă, costului standard sau costului curent. În plus față de a profita de mai multe metode de stabilire a prețurilor și opțiuni de rotunjire, puteți asocia liste de reduceri cu elemente de listă de prețuri. 

 
## <a name="default-product-price-list"></a>Listă de prețuri de produs implicită
Fiecare înregistrare client are un câmp **Câmp de listă de prețuri implicit**, unde aveți posibilitatea să specificați o listă de prețuri care corespunde cu valuta clientului. O valoare implicită nu este introdusă automat în acest câmp. Atunci când există un acord de tarifare particularizat cu un anumit client, aveți posibilitatea să utilizați acest câmp pentru a asocia o listă de prețuri cu acel client.

Entitățile de oportunitate, ofertă și contract de proiect utilizează următoarea ordine pentru a introduce listele de prețuri de produs implicite. Aceeași ordine este utilizată pentru listele de prețuri de proiect.

1.  Ofertă
2.  Oportunitate
3.  Client
4.  Setări globale 

În mod implicit, câmpul **Produs** din linia de ofertă listează toate produsele active din lista de prețuri de produs a ofertei. Dacă un produs a fost inactivat sau dacă este o schiță de produs, aceasta nu este listată, chiar dacă este în lista de prețuri. 

Linii de catalog de produse sunt adăugate ca linii de factură pe prima factură care este creat pentru un contract de proiect. Pe o schiță de factură, aceste linii de factură pot fi șterse. În acest caz, liniile vor apărea pe o factură ulterioară până când sunt facturate sau până când factura este trimisă clientului. Nu se poate factura o cantitate parțială a unei linii de factură de produs. Când liniile de produs din contractul de proiect sunt facturate, se creează date reale. Cu toate acestea, aceste date reale nu sunt legate de entitatea de proiect corelată. Cu alte cuvinte, liniile de contract de proiect bazate pe produse sunt independente de orice utilizare bazată pe proiect. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
