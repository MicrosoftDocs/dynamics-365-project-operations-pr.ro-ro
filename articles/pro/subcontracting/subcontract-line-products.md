---
title: Linii de subcontract pentru produse
description: Acest subiect explică modul de înregistrare a liniilor de subcontract pentru produse și utilizarea diferitelor câmpuri pentru înregistrarea achizițiilor de produse de la furnizori.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c0ddc39638ae9830eacc57f3e1def75aa36e6553
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323701"
---
# <a name="subcontract-lines-for-products"></a>Linii de subcontract pentru produse

[!include [banner](../../includes/dataverse-preview.md)]

_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_

Un subcontract în Dynamics 365 Project Operations poate avea o linie de subcontract pentru produse. Aceste linii îi permit unui manager de proiect să achiziționeze produse de la furnizori, pe care să le poată utiliza apoi în sarcinile proiectului.

Parcurgeți pașii următori pentru a crea o linie de subcontract pentru produse în Project Operations.

1. Pe pagina de navigare, selectați **Subcontracte**, apoi deschideți subcontractul cu care doriți să lucrați. 
2. Pe fila **Linii de subcontract**, selectați **+ Nou** pentru a crea o nouă linie de subcontract.
3. Pe pagina **Creare rapidă** pagina, în câmpul **Clasa tranzacției**, selectați **Material** și introduceți sau selectați informațiile de câmp necesare. 
4. Selectați **Salvare**.

Următorul tabel oferă informații despre câmpurile de pe pagina **Detaliile liniei de subcontract** și pagina **Creare rapidă**, deoarece acestea sunt relevante pentru achiziționarea de produse.

| Câmp | Descriere |
| ----- | ----------- |
| Nume | Numele liniei de subcontract. |
| Descriere | O scurtă descriere a produselor care sunt comandate pe linia de subcontract. |
| Tip linie | Valoarea implicită a acestui câmp este **Bazat pe cantitate**. |
| Metodă de facturare |  Metoda de facturare a liniei de subcontract. Pentru metodele de facturare cu preț fix este disponibil un program de facturare bazat pe jaloane. |
| Clasă de tranzacții | Valoarea implicită a acestui câmp este **Timp**. Pentru a crea linii de subcontract pentru achiziționarea de produse, în câmpul **Clasa tranzacției** selectați **Material**. Această selecție indică faptul că linia de subcontract este utilizată pentru a înregistra o achiziție de produse de utilizat în proiecte. |
| Selectare produs | Selectați dacă produsul achiziționat este ținut în catalogul de produse sau este un produs din afara catalogului. |
| Produs | Selectați un produs activ din catalog. Acest câmp este disponibil numai când **Selectare produs** este setat la **Existent**. |
| Produs din afara catalogului | Introduceți numele produsului din afara catalogului. Acest câmp este disponibil numai când **Selectare produs** este setat la **Din afara catalogului**.  |
| Dată de livrare solicitată | Selectați data de livrare necesară pentru produse. Această dată este, de asemenea, utilizată pentru a alege o listă de prețuri a proiectelor din listele de prețuri ale proiectului atașate subcontractului. Costul produsului pe linia de subcontract capătă apoi valoarea implicită din lista de prețuri respectivă. |
| Data de livrare contractată | Selectați data la care s-a convenit contractual livrarea produselor.  |
| Cantitate comandată | Introduceți cantitatea de produs achiziționată de la furnizor. Dacă un manager de proiect ia prea mult din această cantitate, va apărea un avertisment. |
| Grup de unități | Această valoare este implicită numai pentru produsele din catalog. Când sunt selectate atât **Produs**, cât și **Data de livrare solicitată**, sistemul alege lista de prețuri aplicabilă în funcție de data livrării. Sunt interogate articolele aferente din lista de prețuri pentru produsul care se potrivește. Valorile pentru unitate și pentru grupul de unități primesc valori implicite din înregistrarea articolului din lista de prețuri. |
| Unitate | Această valoare este setată implicit la setarea unității din înregistrarea articolului din lista de prețuri. Puteți schimba acest lucru cu o altă unitate, după cum este necesar. Combinația de produs și unitate este utilizată pentru a seta implicit prețul unitar pe linia de subcontract pentru produsele din catalog existente. |
| Preț unitar | Prețul unitar este implicit, utilizând combinația de produs și unitate din articolele din lista de prețuri, aferente listei de prețuri a proiectului aplicabile pentru data de livrare solicitată din linia de subcontract.  |
| Subtotal | Acest câmp numai citire este calculat drept Cantitate x Preț unitar dacă ambele câmpuri au valori introduse. Dacă fie câmpul **Cantitate**, fie câmpul **Preț unitar**, sau ambele sunt goale, puteți introduce manual o valoare.  |
| Impozit pe vânzări | Introduceți valoarea impozitului pe vânzări. |
| Sumă totală | Acest câmp calculat arată valoarea totală din linia de subcontract după includerea taxelor. Valoarea din acest câmp este calculată ca subtotal + taxă. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
