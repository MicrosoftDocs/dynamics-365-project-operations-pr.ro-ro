---
title: Linii de subcontract pentru timp
description: Acest subiect explică modul de înregistrare a liniilor de subcontract pentru timp și înregistrarea achizițiilor de timp de la furnizori.
author: rumant
ms.date: 08/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 10ebe0fcc86b4652ac01e28108361df1f768b61d
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323881"
---
# <a name="subcontract-lines-for-time"></a>Linii de subcontract pentru timp

[!include [banner](../../includes/dataverse-preview.md)]

_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_

Un subcontract în Dynamics 365 Project Operations poate avea o linie de subcontract pentru timp. Liniile de subcontract pentru timp îi permit unui manager de proiect să cumpere timp al resurselor de la furnizori pentru a avea personal pentru sarcinile proiectului și pentru a avea resurse pentru cerințe.

Parcurgeți pașii următori pentru a crea o linie de subcontract pentru timp în Project Operations.

1. În panoul de navigare, selectați **Subcontracte** și deschideți un subcontract.
2. Pe fila **Linii de subcontract**, selectați **Nou** pentru a crea o nouă linie de subcontract.
3. Pe pagina **Creare rapidă**, în câmpul **Clasa tranzacției**, selectați **Timp**.
4. Introduceți restul de informații pentru câmp și apoi selectați **Salvare**.

  Următorul tabel oferă informații despre câmpurile de pe pagina **Linie de subcontract** și pagina **Creare rapidă**.

| **Câmp** | **Descriere** |
| --- | --- |
| Nume | Numele liniei de subcontract. |
| Descriere | O scurtă descriere a serviciilor care sunt achiziționate pe linia de subcontract. | 
| Tip linie | Acest câmp este o valoare implicită.  |
| Metodă de facturare | Selectați metoda de facturare. Pe baza metodei de facturare a liniei de subcontract la care se face referire, este pus la dispoziție un program de facturare bazat pe jaloane pentru metoda de facturare cu preț fix. |
| Clasă de tranzacții | Acest câmp este o valoare implicită care indică dacă linia de subcontract este utilizată pentru a înregistra o achiziție de timp de la subcontractant. |
| Rol | Rolul resurselor din subcontract al căror timp este achiziționat. Rolul atribuit resurselor din subcontract determină costul achiziției. |
| Început solicitat | Data la trebuie să înceapă să lucreze resursele subcontractantului. Data solicitată este utilizată pentru a alege o listă de prețuri a proiectelor din listele de prețuri ale proiectului atașate subcontractului. Costul rolului de pe linia de subcontract capătă apoi valoarea implicită din lista de prețuri respectivă. |
| Sfârșit solicitat | Data la care se încheie alocarea resurselor subcontractantului. Această dată este utilizată pentru a afișa avertismente atunci când un manager de proiect trage din această capacitate pentru cerințele de resurse care apar după această dată. |
| Cantitate comandată | Numărul de ore de roluri achiziționate de la furnizor. Această valoare este utilizată pentru a afișa avertismente atunci când un manager de proiect trage prea mult din această capacitate pentru cerințele de resurse. |
| Grup de unități | Această valoare a câmpului este în mod implicit grupul de unități de timp și nu poate fi modificată.  |
| Unitate | Acest câmp este în mod implicit unitatea de bază de ore din grupul de unități de timp. Puteți modifica această valoare pentru a cumpăra orice unitate din grupul de unități de timp, cum ar fi ziua sau săptămâna. Combinația de rol și unitate este folosită pentru a calcula prețul unitar pentru linia de subcontract. |
| Preț unitar | Prețul unitar este implicit și derivă din utilizând combinația de rol și unitate din lista de prețuri a proiectului aplicabilă pentru data de livrare solicitată din linia de subcontract. Când lista de prețuri aplicabilă a proiectului are prețul stabilit într-o unitate diferită de unitatea de pe linia de subcontract, sistemul folosește conversia de unități pentru a calcula prețul unitar. |
| Subtotal | Acest câmp numai în citire este calculat automat drept **Cantitate x Preț unitar** dacă sunt introduse atât valorile pentru cantitate, cât și pentru prețul unitar. Dacă fie câmpul Cantitate, fie câmpul Preț unitar, sau ambele sunt goale, puteți introduce o valoare în câmp. |
| Impozit pe vânzări |  Introduceți valoarea impozitului pe vânzări. |
| Sumă totală | Valoarea totală a liniei de subcontract, după includerea taxelor. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
