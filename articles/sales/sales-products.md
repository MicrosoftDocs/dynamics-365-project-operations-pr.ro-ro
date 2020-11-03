---
title: Produse
description: Acest subiect oferă informații despre catalogul de produse pe care îl puteți utiliza pentru a oferi clienților informații despre produsele și prețurile oferite de organizația dvs.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 7116659c646b323667e3c92cb3f6de99184f5ae6
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082893"
---
# <a name="products"></a>Produse

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Produsele sunt coloana vertebrală a afacerii dumneavoastră. Catalogul de produse din Dynamics 365 Sales Professional este o colecție de produse cu informații despre prețurile lor. Ajutați agenții de vânzări să crească vânzările, creând rapid un catalog de produse.

## <a name="add-a-product"></a>Adăugarea unui produs

1.  Asigurați-vă că aveți funcția Sales Manager Professional sau un rol de administrator de sistem pentru a putea adăuga produse în Dynamics 365 Sales Professional.
2.  În harta site-ului, sub **Configurare** , selectați **Produse**.
3.  Selectați **Adăugați produs** și completați următoarele informații:

    -  **Nume**
    -  **ID produs**
    -  **Principal** : selectați o familie de produse principale pentru produs. În cazul în care creați un produs secundar într-o familie de produse, numele familiei de produse principale este populat aici. Acest lucru nu poate fi schimbat după ce înregistrarea este salvată.
    -  **Valid de la**/**Valid până la** : definiți perioada de valabilitate a produsului selectând o dată **Valid de la** și **Valid până la**.
    -  **Grup de unități** : selectați un grup de unități. Un grup de unități este o colecție de diverse unități în care este vândut un produs și definește modul în care sunt grupate elementele individuale în cantități mai mari. De exemplu, dacă adăugați semințe ca produs, este posibil să fie creat un grup de unități numit „Semințe” și să îi fie definită unitatea principală ca „pachet.”
    -  **Unitate implicită** : selectați unitatea cea mai comună în care se va vinde produsul. Unitățile sunt cantitățile sau măsurătorile în care vă vindeți produsele. De exemplu, dacă adăugați semințe ca produs, le puteți vinde în pachete, cutii, sau pungi. Fiecare dintre acestea devine o unitate de produs. În cazul în care semințele se vând în principal în pachete, selectați pachet ca unitate.
    -  **Listă de prețuri implicită** : dacă acesta este un produs nou, acest câmp este doar în citire. Înainte de a selecta o listă de prețuri implicită, trebuie să completați toate câmpurile obligatorii și apoi să salvați înregistrarea. Deși lista de prețuri implicită nu este obligatorie, după salvarea înregistrării de produs se recomandă setarea unei liste de prețuri implicite pentru fiecare produs. Apoi, dacă o înregistrare client nu conține o listă de prețuri, Vânzări poate utiliza lista de prețuri implicită pentru a genera oferte, comenzi și facturi.
    -  **Zecimale acceptate** : introduceți un număr întreg între 0 și 5. Dacă produsul nu poate fi împărțit în cantități fracționare, introduceți 0. Precizia câmpului **Cantitate** în înregistrarea ofertei, comenzii sau facturii produs este validată în raport cu valoarea din acest câmp în cazul în care produsul nu are o listă de prețuri asociată.
    -  **Subiect** : asociați acst produs cu un subiect. Utilizaţi subiectele pentru a clasifica produsele dvs. şi pentru a filtra rapoarte.

4.  Selectați **Salvare**.
5.  Pe fila **Detalii adiționale** , în secțiunea **Elemente de listă de prețuri** , selectați **Mai multe comenzi** , iar apoi selectați **Adăugați nou element listă de prețuri**.
7.  Pe fila **Detalii adiționale** , în secțiunea **Relație de produs** , selectați pictograma **Mai multe comenzi** și apoi selectați **Adăugați relație nouă de produs.**
8.  În formularul **Relație nouă produs** , introduceți următoarele detalii, iar pe bara de comandă, selectați **Salvare și închidere** :

    -   **Produs corelat** : selectați un produs pe care doriți să îl adăugați ca produs conex la înregistrarea de produs existentă la care lucrați.
    -   **Tip de relație de vânzări** : Selectați dacă doriți să adăugați produsul ca vânzare suplimentară, vânzare încrucișată, accesoriu sau produs substituent.
    -   **Direcție** :Selectați dacă relația dintre produse va fi unidirecțională sau bidirecțională. Când selectați unidirecțională, produsul pe care îl selectați în **Produs asociat** va fi afișat ca o recomandare pentru produsul existent, dar nu invers.

9.  În formularul de produs, selectați **Salvare**.

## <a name="import-products"></a>Import produse

Puteți utiliza șabloane de import pentru a introduce vrac date despre produse în Dynamics 365 Sales.

## <a name="revise-a-product"></a>Revizuirea unui produs

Păstrați actualizat inventarul produselor revizuind rapid proprietățile pentru produse, după caz, și republicând informațiile, astfel încât agenții de vânzări să poată vedea ultimele modificări la inventar.

1.  Asigurați-vă că aveți unul dintre următoarele roluri de securitate sau permisiuni echivalente: Administrator de sistem, Expert logistică sistem, Manager de vânzări, Vicepreședinte de vânzări, Vicepreședinte de marketing sau Președinte - director de firmă.
2.  În harta site-ului, selectați **Produse**.
3.  Deschideți un produs, pe care doriți să îl modificați și, pe bara de comenzi, selectați **Revizuire**.
4.  În caseta de dialog **Confirmați revizuirea** , selectați **Confirmați**. Acest lucru va schimba starea produsului la **În curs de revizuire**.
5.  După ce terminați modificările, din bara de comenzi selectați **Publicare**.

    > [!TIP]
    > Pentru a anula modificările și a continua cu ultima versiune activă a produsului, selectați **Revenire**. Acest lucru modifică starea produsului înapoi la **Activ**.

## <a name="clone-a-product"></a>Clonarea unui produs 

Atunci când creați un produs, economisiți timp clonând unul deja existent. Acest lucru creează o copie a înregistrării originale cu toate detaliile cu excepția numelui și ID-ului.

1.  Asigurați-vă că aveți unul dintre următoarele roluri de securitate sau permisiuni echivalente: Administrator de sistem, Expert logistică sistem, Manager de vânzări, Vicepreședinte de vânzări, Vicepreședinte de marketing sau Președinte - director de firmă.
2.  În harta site-ului, selectați **Produse**.
3.  Selectați o înregistrare de produs, pe care doriți să o clonați și, pe bara de comenzi, selectați **Clonare**. Apare o casetă de dialog de confirmare.
4.  Selectați **Confirmare**.

Se deschide o nouă înregistrare de produs cu aceleași detalii ca înregistrarea originală, cu excepția numelui și ID-ului.

## <a name="retire-a-product"></a>Retragerea unui produs 

Dacă organizația dvs. nu mai vinde un produs, retrageți produsul, pentru a nu mai fi disponibil agenților de vânzări.

1.  Asigurați-vă că aveți rolul de administrator de sistem sau Sales Professional Manager sau permisiuni echivalente.
2.  În harta site-ului, selectați **Produse**.
3.  Deschideți un produs, pe care doriți să îl retrageți și, pe bara de comenzi, selectați **Retragere**.
4.  În caseta de dialog **Confirmați retragerea** , selectați **Confirmați**.


## <a name="delete-a-product"></a>Ștergerea unui produs

Pentru a opri vânzarea unui produs, ștergeți-l.

> [!IMPORTANT]
> Nu puteți recupera o înregistrare ștearsă.

1.  Asigurați-vă că aveți rolul de administrator de sistem sau Sales Professional Manager sau permisiuni echivalente.
2.  În harta site-ului, selectați **Produse**.
3.  Selectați o înregistrare de produs pe care doriți să o ștergeți și, pe bara de comenzi, selectați **Ștergere**.
4.  În caseta de dialog **Confirmare ștergere** , selectați **Continuare**.
 
 ## <a name="quantity-factors-for-products"></a>Factori de cantitate pentru produse

Factori de cantitate acceptă vânzarea de produse pe bază de abonament. Pentru produsele bazate pe abonament, cantitatea din linia de contract de ofertă sau de proiect este exprimată ca număr de luni de utilizare.

De obicei, prețul software-ului de abonament este stocat în catalogul ca prețul pe utilizator pe lună. Cu toate acestea, puteți utiliza alte descrieri de timp în schimb. În timpul procesului de vânzări, prețul de pe linia de ofertă este, de obicei, prețul per utilizator, pe lună, care a fost negociat și actualizat de către agentul de vânzări IT. Fiecare afacere are un număr diferit de utilizatori și un număr diferit de luni de abonament. Cantitatea utilizată pentru a calcula suma liniei de ofertă este un produs al numărului de utilizatori și numărul de luni de abonament.

Factorii de cantitate se bazează pe atributele produsului. Când configurați proprietăți specifice pentru un produs, puteți semnaliza un subset al acelor proprietăți sau toate proprietățile, ca factori de cantitate.

Sistemul validează că numai proprietățile numerice sau proprietățile produsului care au un tip de date numerice sunt marcate ca factori de cantitate. Când un produs pentru care sunt configurate factori de cantitate este adăugat la o linie de ofertă câmpul **Cantitate** din linia de ofertă devine un câmp doar în citire. După ce introduceți valori pentru proprietățile produsului care sunt factori de cantitate, este calculată cantitatea liniei de ofertă.

De exemplu, dacă există următoarele proprietăți: 

- **Nr. de utilizatori** : numărul de utilizatori 
- **Nr. de luni** : numărul de luni de abonament
- **Produs SKU** 

Proprietățile **Nr. de utilizatori** și **Nr. de luni** pot fi marcate ca factori de cantitate prin editarea proprietăților de linie de produs. 
