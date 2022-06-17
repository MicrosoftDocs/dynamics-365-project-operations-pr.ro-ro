---
title: Tarifare pentru Catalog de produse
description: Acest articol oferă informații despre cum funcționează prețurile din catalogul de produse Dynamics 365 Project Service Automation (PSA).
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 61d35a9ce16bb58abc66edab5e21dd83d607184e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913405"
---
# <a name="product-catalog-pricing"></a>Tarifare pentru Catalog de produse 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


Listele de preț și entitățile element listă de prețuri acceptă stabilirea prețului catalogului de produse. În cea mai mare parte, această funcționalitate este utilizată pentru liniile bazate pe catalog pe oferte de proiect și contracte de proiect.

Pentru liniile bazate pe proiect, un contract reprezintă afacerea după ce a fost câștigat. Pentru că de obicei procesul de negociere precede câștigul, stabilirea prețului care este atașat ofertei este mereu copiat așa cum este la o nouă listă de prețuri și atașată contractului. Această nouă listă de prețuri nu poate fi schimbată în afara domeniului de aplicare al contractului. Această limitare ajută la protejarea grilei tarifare care a fost negociată de orice modificări de prețuri care pot avea loc în lista de prețuri principală.

Produsele trebuie să fie configurate astfel încât să aibă cost implicit și liste de prețuri în catalogul de produse. Trebuie să utilizați prețul de listă, costul standard și costul actual pentru a configura costul implicit și prețul de listă. Prețurile de listă implicite sunt utilizate pe o linie de ofertă sau pe o linie de contract de proiect numai când sistemul nu găsește o linie de listă de prețuri pentru acel produs în lista de prețuri a produsului pentru ofertă sau contractul de proiect.

Prețul de cost al liniilor de catalog de produse poate fi modificat între oferte. Această capacitate este importantă, pentru că dacă nu urmăriți cu acuratețe costurile, nu puteți determina profiturile operaționale pe angajamente de proiect. În mod implicit, costul standard al produsului este utilizat ca preț de cost. Cu toate acestea, prețul implicit de cost poate fi actualizat pe linia de ofertă dacă există un preț de cost diferit pentru acea ofertă.

## <a name="price-list-items"></a>Element listă de prețuri

Puteți adăuga produse dintr-un catalog de produse la diferite liste de prețuri. Liniile de listă de prețuri pentru produse se referă întotdeauna la o anumită unitate. Prețurile pentru un produs pe elementele listei de prețuri pot fi configurate ca o valoare monetară. Alternativ, acesta poate fi configurat ca o funcție a prețului listei, costului curent sau costului standard.

PSA acceptă diverse opțiuni de rotunjire atunci când prețurile sunt configurate ca o funcție a prețului de listă, costului standard sau costului curent. În plus față de a profita de mai multe metode de stabilire a prețurilor și opțiuni de rotunjire, puteți asocia liste de reduceri cu elemente de listă de prețuri. 

> ![Adăugarea produselor dintr-un catalog la liste de prețuri diferite.](media/basic-guide-16.png)

Atunci când creați o nouă listă de prețuri particularizate pentru o ofertă selectând **Creați prețuri particularizate** pe pagina **Ofertă de proiect**, PSA face o copie a listei de prețuri și câmpul **Entitate** pe antetul noii liste de prețuri este setată la **Entitate de vânzări**. Numele listei de prețuri noi este anexat cu numele ofertei și cu un marcaj temporal. De asemenea, puteți utiliza numele listei de prețuri noi și numele ofertei în fluxuri de lucru particularizate pentru a declanșa revizuire suplimentară și aprobări pentru ofertele care utilizează prețuri particularizate.

 
## <a name="default-product-price-list"></a>Listă de prețuri de produs implicită
Fiecare înregistrare client are un câmp **Câmp de listă de prețuri implicit**, unde aveți posibilitatea să specificați o listă de prețuri care corespunde cu valuta clientului. În PSA, o valoare implicită nu este introdusă automat în acest câmp. Atunci când există un acord de tarifare particularizat cu un anumit client, aveți posibilitatea să utilizați acest câmp pentru a asocia o listă de prețuri cu acel client.

Entitățile de oportunitate, ofertă și contract de proiect utilizează următoarea ordine pentru a introduce listele de prețuri de produs implicite. Aceeași ordine este utilizată pentru listele de prețuri de proiect.

1.  Ofertă
2.  Oportunitate
3.  Client
4.  Setări globale pentru PSA

În mod implicit, câmpul **Produs** din linia de ofertă listează toate produsele active din lista de prețuri de produs a ofertei. Dacă un produs a fost inactivat sau dacă este o schiță de produs, aceasta nu este listată, chiar dacă este în lista de prețuri. 

Linii de catalog de produse sunt adăugate ca linii de factură pe prima factură care este creat pentru un contract de proiect. Pe o schiță de factură, aceste linii de factură pot fi șterse. În acest caz, liniile vor apărea pe o factură ulterioară până când sunt facturate sau până când factura este trimisă clientului. În PSA, nu se poate factura o cantitate parțială a unei linii de factură de produs. Când liniile de produs din contractul de proiect sunt facturate, se creează date reale. Cu toate acestea, aceste date reale nu sunt legate de entitatea de proiect corelată. Cu alte cuvinte, liniile de contract de proiect bazate pe produse sunt independente de orice utilizare bazată pe proiect. PSA nu urmărește consumul de materiale pe proiecte.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
