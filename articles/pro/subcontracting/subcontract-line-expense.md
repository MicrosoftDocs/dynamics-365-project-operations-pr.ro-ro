---
title: Linii de subcontract pentru categoriile de cheltuieli
description: Acest subiect explică modul de înregistrare a liniilor de subcontract pentru cheltuieli și utilizarea câmpurilor pentru înregistrarea achizițiilor de timp de la furnizori.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9e8e7bb66063dab6db1ac8da1753913aee0ef3fc
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323836"
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

| **Câmp** |  **Descriere** |
| ----------| ---------------- |
| Nume | Numele liniei de subcontract. |
| Descriere | O scurtă descriere a serviciilor sau produselor care sunt achiziționate în linia de subcontract. |
| Tip linie | Acest câmp are valoarea implicită **Bazat pe cantitate**.  |
| Metodă de facturare | Metoda de facturare a liniei de subcontract. Pe baza metodei de facturare a liniei, este disponibil un program de facturare bazat pe jaloane pentru metoda de facturare cu preț fix.  |
| Clasă de tranzacții | Acest câmp are valoarea implicită **Timp**. Pentru a crea linii de subcontract pentru achiziționarea de produse, setați câmpul **Clasa tranzacției** la **Cheltuială**. Această valoare de câmp indică faptul că linia de subcontract este utilizată pentru a înregistra o achiziție de categorie de produse sau servicii de utilizat în proiecte. |
| Categorie tranzacție | Selectați categoria de tranzacție. |
| Început solicitat | Data la care categoriile de achiziții trebuie să fie disponibile de la furnizor. Data solicitată este utilizată pentru a alege o listă de prețuri a proiectelor din listele de prețuri ale proiectului atașate subcontractului. Costul categoriei pe linia de subcontract capătă apoi valoarea implicită din lista de prețuri respectivă. |
| Sfârșit solicitat | Data la care categoriile de achiziții nu mai sunt necesare. Această dată apelează un avertisment atunci când un manager de proiect asociază această linie de subcontract cu estimări de cheltuieli specifice pentru proiectele care sunt datate după această dată. |
| Cantitate comandată | Cantitatea de categorie achiziționată de la furnizor. Când un manager de proiect ia prea mult din cantitatea achiziționată, va apărea un avertisment.  |
| Grup de unități | Valoarea implicită a acestui câmp se bazează pe grupul de unități implicit configurat pentru categoria selectată. |
| Unitate | Valoarea implicită a acestui câmp se bazează pe grupul de unități implicit configurat pentru categoria selectată. Combinația de categorie și unitate este utilizată pentru a seta implicit prețul unitar pe linia de subcontract. |
| Preț unitar | Valoarea de câmp pentru prețul unitar preia valoarea implicită din combinația de categorie și unitate din prețurile categoriilor aferente listei de prețuri a proiectului, aplicabile pentru data de început solicitată din linia de subcontract.  |
| Subtotal | Acest câmp numai în citire este calculat automat ca preț unitar al cantității dacă sunt introduse atât valorile cantității, cât și prețul unitar. Dacă oricare dintre câmpuri sau ambele câmpuri sunt goale, puteți introduce manual o valoare în acest câmp.  |
| Impozit pe vânzări | Introduceți valoarea impozitului pe vânzări.  |
| Sumă totală | Valoarea totală a liniei de subcontract, inclusiv taxele. Acest câmp este calculat ca subtotal + impozit pe vânzări.  |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
