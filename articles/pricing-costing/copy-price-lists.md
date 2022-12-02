---
title: Copierea listelor de prețuri
description: Acest articol furnizează informații despre cum să copiați listele de prețuri în Project Operations.
author: rumant
ms.date: 10/13/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3fce3a362fe6326e362c3f77054c10281a9c146c
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921179"
---
# <a name="copy-price-lists"></a>Copierea listelor de prețuri

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Puteți crea copii ale listelor de prețuri în Dynamics 365 Project Operations. De exemplu, puteți crea liste de prețuri pentru anul viitor folosind o listă de prețuri din anul curent.  Sau, puteți copia o listă de prețuri pentru tarifele facturilor și prețurile de vânzare din listele de prețuri pentru costuri. 

Pentru a face o copie a listei de prețuri, parcurgeți pașii următori.

1. Deschideți lista de prețuri pentru care doriți să faceți o copie și selectați **Copie**.
2. Introduceți orice informații necesare pentru a copia lista de prețuri. Tabelul următor prezintă considerații de care trebuie să țineți cont atunci când introduceți informații.

| Câmp | Descriere | Impactul din aval |
| --- | --- | --- |
| Nume | Numele listei de prețuri sursă cu adăugare **-copie**. | Lista de prețuri include această valoare pe toate paginile de liste și opțiuni verticale. |
| Context | Introduceți contextul dorit pentru lista de prețuri țintă. | O listă de prețuri care are contextul setat la **Cost** este utilizată pentru a căuta prețul pentru estimări ale costurilor și costuri reale. O listă de prețuri care are contextul setat la **Vânzări** este utilizată pentru a căuta prețul pentru estimări ale vânzări și vânzări reale. Numai listele de prețuri care au contextul setat la **Vânzări** pot fi atașate la o listă de prețuri a proiectului pentru un client, oferte sau un contract. |
| Data de început | Data de începere a perioadei în care lista de prețuri este efectivă. | Împreună cu **Data de sfârșit**, acest câmp este utilizat pentru a determina care listă de prețuri este aplicabilă pentru o anumită estimare sau linie reală. |
| Data de sfârșit | Data de sfârșit a perioadei în care lista de prețuri este efectivă. | Împreună cu **Data de început**, acest câmp este utilizat pentru a determina care listă de prețuri este aplicabilă pentru o anumită estimare sau linie reală. |
| Monedă | Moneda listei de prețuri sursă. Aceasta poate fi modificată. | Când acest lucru este modificat, toate liniile de preț rezultate pentru muncă, cheltuieli și articole din catalogul de produse sunt convertite în moneda listei de prețuri țintă în timpul copierii. |
| Unitate de timp | Moneda listei de prețuri sursă. Aceasta poate fi modificată. | Când acest lucru este modificat, toate liniile de preț rezultate pentru muncă sunt convertite în unitatea listei de prețuri țintă în timpul copierii. Se utilizează conversia din setarea unității pentru unitatea de timp a listei de prețuri sursă și unitatea de timp a listei de prețuri țintă. |
| Descriere | O descriere a listei de prețuri sursă cu adăugare **-copie**. Acesta este un câmp text și vă permite să aveți o descriere pe mai multe linii a listei de prețuri. | Acest câmp este afișat în vizualizări **Asociate** pe lista de prețuri din diferite entități care au liste de prețuri conexe. |

3. Salvați lista de prețuri. 

## <a name="update-a-price-list-by-applying-a-mark-up-to-all-the-prices"></a>Actualizați o listă de prețuri aplicând o marcare la toate prețurile

1. Pe filele **Rol**, **Categorie** și filele **Element din lista de prețuri** unei liste de prețuri, puteți selecta **Actualizați prețurile** pentru a aplica un adaos pentru toate prețurile din subgrilă. 
2. În pagina de dialog care se deschide, introduceți o marcare. De asemenea, puteți introduce un procent de majorare negativ pentru a reduce prețurile cu un anumit procent. 
3. Selectați **OK** pe pagina de dialog și apoi verificați dacă prețurile din subgrilă reflectă modificările pe care le-ați făcut.


[!INCLUDE[footer-include](../includes/footer-banner.md)]