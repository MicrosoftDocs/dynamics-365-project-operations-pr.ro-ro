---
title: Linii de subcontract pentru categoriile de cheltuieli
description: Acest subiect explică modul de înregistrare a liniilor de subcontract pentru cheltuieli și utilizarea câmpurilor pentru înregistrarea achizițiilor de timp de la furnizori.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0c32bf2ac54de98a921d338e436ecd089e68a759
ms.sourcegitcommit: cd4e81f129681a12f2efe63ec2bb14e611cf88ba
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 09/20/2021
ms.locfileid: "7506114"
---
#  <a name="subcontract-lines-for-expense-categories"></a>Linii de subcontract pentru categoriile de cheltuieli

[!include [banner](../../includes/dataverse-preview.md)]

_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_

Un subcontract în Dynamics 365 Project Operations poate avea o linie pentru categorii de cheltuieli. Liniile de subcontract pentru categoriile de cheltuieli îi permit unui manager de proiect să achiziționeze categorii de servicii sau produse de la furnizori pe care le pot percepe unui proiect.

Parcurgeți pașii următori pentru a crea o linie de subcontract pentru categorii de cheltuieli în Project Operations.

1. În panoul de navigare, selectați **Subcontracte**, apoi deschideți subcontractul cu care doriți să lucrați.
2. Pe fila **Linii de subcontract**, selectați **Nou** pentru a crea oNouă linie.
3. Pe pagina **Creare rapidă** pagina, în câmpul **Clasa tranzacției**, selectați **Cheltuială** și introduceți sau selectați orice altă informație de câmp necesară.

Următorul tabel oferă informații despre câmpurile de pe pagina de detalii pentru **Linia de subcontract** și pagina **Creare rapidă**.

| **Câmp** | **Descriere** | **Impact funcțional** |
| --- | --- | --- |
| Nume | Numele liniei de subcontractare pentru identificare. | Aceasta va fi afișată ca prima coloană din toate căutările bazate pe reperele liniilor de subcontractare. |
| Descriere | O scurtă descriere a categoriilor de cheltuieli care sunt achiziționate pe linia de subcontractare. | Fără |
|Tip linie | Acest câmp are valoarea implicită de  **Bazat pe cantitate**. |Fără |
| Metodă de facturare | Acesta este un set de opțiuni care reprezintă cele două modele principale de contractare susținute de Project Operations: **Preț fix** și **Timp și material**. | O planificare de facturare bazat pe o etapă importantă este pusă la dispoziție pentru liniile de subcontractare dacă este selectată metoda de facturare cu Preț fix. |
| Clasă de tranzacții | Acest câmp are valoarea implicită de  **Timp**. Pentru a crea linii de subcontract pentru achiziționarea de produse, setați câmpul  **Clasa tranzacției**  la  **Cheltuială**.  | Acest lucru indică faptul că linia de subcontractare este utilizată pentru a înregistra achiziția unei categorii de cheltuieli care urmează să fie utilizate în proiecte. |
| Categorie tranzacție | Afișează o listă a categoriilor de tranzacții active din sistem. |Fără |
| Început solicitat | Introduceți data la care categoriile de achiziții trebuie să fie disponibile de la furnizor. | Începutul solicitat este utilizat pentru a alege o listă de prețuri a proiectelor din listele de prețuri ale proiectului atașate subcontractului. Costul categoriei de pe linia de subcontractare provine din acea listă de prețuri. |
| Final solicitat | Introduceți data la care categoriile de achiziții nu ar mai fi necesare. | Aceasta va fi utilizată pentru a afișa avertismente atunci când un manager de proiect asociază această linie de subcontractare cu estimări specifice de cheltuieli ale proiectului care sunt necesare după această dată. |
| Cantitate comandată | Cantitatea categoriei achiziționate de la furnizor. | Aceasta va fi utilizată pentru a afișa avertismente atunci când un manager de proiect trage în exces din această cantitate.|
| Grup de unități | Valoarea implicită se bazează pe grupul de unități implicit care este configurat pentru categoria selectată. |Fără |
| Unitate | Implicitul se bazează pe unitatea implicită configurată pentru categoria selectată.  | Combinația dintre **Categorie** și **Unitate** va fi folosit ca implicit sau calculat pentru prețul unitar pentru linia de subcontractare.  |
| Preț unitar | Valoarea implicită folosește combinația dintre **Categorie** și **Unitate** din categoria prețuri aferente listei de prețuri a proiectului, care este aplicabilă pentru începutul solicitat al liniei de subcontractare. |Fără |
| Subtotal | Acesta este un câmp de numai citire care este calculat ca Cantitate X Preț unitar, dacă sunt introduse atât cantitatea, cât și prețul unitar. Dacă unul sau ambele câmpuri sunt necompletate, puteți introduce o valoare în acest câmp. |Fără |
| Impozit pe vânzări | Introduceți valoarea impozitului pe vânzări. |Fără |
| Sumă totală | Valoarea totală a liniei de subcontract, inclusiv taxele. Acest câmp este calculat ca Subtotal + Impozit pe vânzări. |Fără |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
