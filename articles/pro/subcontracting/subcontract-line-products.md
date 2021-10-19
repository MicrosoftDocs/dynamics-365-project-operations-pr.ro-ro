---
title: Linii de subcontract pentru produse
description: Acest subiect explică modul de înregistrare a liniilor de subcontract pentru produse și utilizarea diferitelor câmpuri pentru înregistrarea achizițiilor de produse de la furnizori.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cda2db2b6beafb943738b35857d091f7ad17390d
ms.sourcegitcommit: d507a75a19c992a9421e4f3605162a2faa84a445
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 09/27/2021
ms.locfileid: "7558562"
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

| Câmp | Descriere | Impact funcțional|
| ----- | ----------- | ----------- |
| Nume | Numele liniei de subcontractare pentru identificare. |Aceasta va fi afișată ca prima coloană din toate căutările bazate pe reperele liniilor de subcontractare.
| Descriere | O scurtă descriere a produselor care sunt comandate pe linia de subcontract. | Fără |
| Tip linie | Acest câmp are valoarea implicită **Bazat pe cantitate**. |Fără |
| Metodă de facturare | Acesta este un set de opțiuni care reprezintă cele două modele principale de contractare susținute de Project Operations: **Preț fix** și **Timp și material**. | Pe baza metodei de facturare selectate, o planificare de facturare bazat pe o etapă importantă este pus la dispoziție pentru liniile de subcontractare cu metoda de facturare cu Preț fix. |
| Clasă de tranzacții |Acest câmp are valoarea implicită de  **Timp**. Pentru a crea linii de subcontractare pentru achiziționarea de produse, setați câmpul  **Clasa tranzacției**  la  **Material**.  | Acest lucru indică faptul că linia de subcontractare este utilizată pentru a înregistra achiziția de produse care urmează să fie utilizate în proiecte. |
| Selectare produs | Selectați dacă produsul achiziționat este ținut în catalogul de produse sau este un produs din afara catalogului. |Fără |
| Produs | Selectați un produs activ din catalog. Acest câmp este disponibil numai când **Selectare produs** este setat la **Existent**. |Combinația dintre **Produs** și **Unitate** va fi folosit ca implicit sau calculat pentru prețul unitar pentru linia de subcontractare.
| Produs din afara catalogului | Introduceți numele produsului din afara catalogului. Acest câmp este disponibil numai când **Selectare produs** este setat la **Din afara catalogului**.  |Prețul de achiziție nu va fi completat automat pentru produsele în afara catalogului.|
| Dată de livrare solicitată | Introduceți data de livrare necesară pentru produse.| Această dată este, de asemenea, utilizată pentru a alege o listă de prețuri a proiectelor din listele de prețuri ale proiectului atașate subcontractului. Costul produsului pe linia de subcontract capătă apoi valoarea implicită din lista de prețuri respectivă. |
| Data de livrare contractată | Introduceți data la care produsele sunt convenite contractual să fie livrate.  |Fără|
| Cantitate comandată | Introduceți cantitatea de produs achiziționată de la furnizor.| Aceasta va fi utilizată pentru a afișa avertismente atunci când un manager de proiect trage în exces din această cantitate.|
| Grup de unități | Această valoare este implicită numai pentru produsele din catalog. |Când sunt selectate atât **Produs**, cât și **Data de livrare solicitată**, sistemul alege lista de prețuri aplicabilă în funcție de data livrării. Sunt interogate articolele aferente din lista de prețuri pentru produsul care se potrivește. Valorile pentru unitate și pentru grupul de unități primesc valori implicite din înregistrarea articolului din lista de prețuri. |
| Unitate | Această valoare implicită este unitatea configurată în înregistrarea elementului din lista de prețuri. Puteți schimba acest lucru cu o altă unitate, după cum este necesar.| Combinația de produs și unitate este utilizată pentru a seta implicit prețul unitar pe linia de subcontract pentru produsele din catalog existente. |
| Preț unitar | Prețul unitar este implicit, utilizând combinația de produs și unitate din articolele din lista de prețuri, aferente listei de prețuri a proiectului aplicabile pentru data de livrare solicitată din linia de subcontract.  |Fără |
| Subtotal | Acest câmp numai citire este calculat drept Cantitate x Preț unitar dacă ambele câmpuri au valori introduse. Dacă fie câmpul **Cantitate**, fie câmpul **Preț unitar**, sau ambele sunt goale, puteți introduce manual o valoare.  |Fără |
| Impozit pe vânzări | Introduceți valoarea impozitului pe vânzări. |Fără |
| Sumă totală | Acest câmp calculat arată valoarea totală din linia de subcontract după includerea taxelor. Valoarea din acest câmp este calculată ca Subtotal + impozit. |Fără |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
