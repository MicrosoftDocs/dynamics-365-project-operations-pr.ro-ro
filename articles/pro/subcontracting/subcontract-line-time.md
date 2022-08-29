---
title: Linii de subcontract pentru timp
description: Acest articol explică cum să înregistrați liniile de subcontractare pentru timp și să înregistrați achiziția de timp de la furnizori.
author: rumant
ms.date: 08/05/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 8e9619dc713fde3127f552234e4a7427d99be683
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/11/2022
ms.locfileid: "9262105"
---
# <a name="subcontract-lines-for-time"></a>Linii de subcontract pentru timp

_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_

Un subcontract în Dynamics 365 Project Operations poate avea o linie de subcontract pentru timp. Liniile de subcontract pentru timp îi permit unui manager de proiect să cumpere timp al resurselor de la furnizori pentru a avea personal pentru sarcinile proiectului și pentru a avea resurse pentru cerințe.

Parcurgeți pașii următori pentru a crea o linie de subcontract pentru timp în Project Operations.

1. În panoul de navigare, selectați **Subcontracte** și deschideți un subcontract.
2. Pe fila **Linii de subcontract**, selectați **Nou** pentru a crea o nouă linie de subcontract.
3. Pe pagina **Creare rapidă**, în câmpul **Clasa tranzacției**, selectați **Timp**.
4. Introduceți restul de informații pentru câmp și apoi selectați **Salvare**.

  Următorul tabel oferă informații despre câmpurile de pe pagina **Linie de subcontract** și pagina **Creare rapidă**.

| **Câmp** | **Descriere** | **Impact funcțional** |
| --- | --- | --- |
| Nume | Numele liniei de subcontractare pentru identificare. | Aceasta va fi afișată ca prima coloană din toate căutările bazate pe reperele liniilor de subcontractare. |
| Descriere | O scurtă descriere a serviciilor care sunt achiziționate pe linia de subcontract. |Fără |
| Tip linie |   Acest câmp are valoarea implicită **Bazat pe cantitate**.| Fără |
| Metodă de facturare | Acesta este un set de opțiuni care reprezintă cele două modele principale de contractare susținute de Project Operations: **Preț fix** și **Timp și material**. | Pe baza metodei de facturare selectate, o planificare de facturare bazat pe o etapă importantă este pus la dispoziție pentru liniile de subcontractare cu metoda de facturare cu Preț fix. |
| Clasă de tranzacții | Valoarea implicită este **Timp**. | Acest lucru indică faptul că linia de subcontractare este utilizată pentru a înregistra o achiziție de timp subcontractant. |
| Rol | Selectați rolul resurselor de subcontractare al căror timp este achiziționat. | Rolul îndeplinit de resursele subcontractului determină costul achiziției. |
| Început solicitat | Introduceți data la care resursele subcontractorului sunt necesare pentru a începe să funcționeze. | Acesta este utilizat pentru a alege o listă de prețuri a proiectelor din listele de prețuri ale proiectului atașate subcontractului. Costul rolului de pe linia de subcontractare provine din acea listă de prețuri. |
| Final solicitat | Introduceți data la care se termină atribuirea resursei subcontractorului. | Aceasta va fi utilizată pentru a afișa avertismente atunci când un manager de proiect trage din capacitatea pentru cerințele de resurse care apar după această dată. |
| Cantitate comandată | Introduceți numărul de ore pentru rolul achiziționat de la furnizor. | Aceasta va fi utilizată pentru a afișa avertismente atunci când un manager de proiect trage în exces din capacitatea pentru cerințele de resurse. |
| Grup de unități | Valoarea implicită este **Grupul de unități de timp**, care nu poate fi modificat. | Fără|
| Unitate | Valoarea implicită pentru acest câmp este unitatea de bază a orelor de la **Grupul de unități de timp**. Puteți modifica această valoare pentru a cumpăra orice unitate din **Grup de unități de timp**, precum ziua sau săptămâna. | Combinația dintre **Rol** și **Unitate** va fi folosit ca implicit sau calculat pentru prețul unitar pentru linia de subcontractare. |
| Preț unitar | Prețul unitar implicit utilizează combinația dintre **Rol** și **Unitate** din lista de prețuri a proiectului pentru data **Început solicitat** a liniei de subcontractare. | Când lista de prețuri aplicabilă a proiectului are prețul stabilit într-o unitate diferită de unitatea de pe linia de subcontract, sistemul folosește conversia de unități pentru a calcula prețul unitar. |
| Subtotal |    Acesta este un câmp de numai citire care este calculat ca Cantitate x Preț unitar, dacă sunt introduse atât cantitatea, cât și prețul unitar. Dacă fie câmpul Cantitate, fie câmpul Preț unitar, sau ambele sunt goale, puteți introduce o valoare în câmp. | Fără|
| Impozit pe vânzări |   Introduceți valoarea impozitului pe vânzări. |Fără |
| Sumă totală | Valoarea totală a liniei de subcontract, inclusiv taxele. Acest câmp este calculat ca Subtotal + Impozit pe vânzări.|Fără |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
