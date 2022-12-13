---
title: Detalii antet pentru contractele de proiect
description: Acest articol oferă informații despre câmpurile și informații despre contractele de proiect din Operațiuni de proiect.
author: rumant
ms.date: 03/08/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f648113f54257e2c303cb2729e282d70f818d838
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824924"
---
# <a name="header-details-for-project-contracts"></a>Detalii antet pentru contractele de proiect

_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_

Acest articol oferă informații despre câmpurile care se aplică întregului contract de proiect, inclusiv setările care au impact asupra tuturor liniilor de contract. Sunt incluse, de asemenea, informații despre contract care sunt rezumate pe toate elementele rând pentru a genera KPI-urile contractului de proiect.

Următorul tabel listează câmpurile unui contract de proiect care sunt unice pentru Dynamics 365 Project Operations sau au unele schimbări importante în comportament de la comenzile de vânzări în Dynamics 365 Sales.

| Câmp | Locație | Descriere | Impactul din aval |
| --- | --- | --- | --- |
| Tip | Fila **Rezumat** (ascuns) | Acesta este un câmp de set de opțiuni cu următoarele opțiuni:</br>- **Pe bază de muncă** (disponibil numai când este instalat Project Operations)</br>- **Pe bază de element** (disponibil numai atunci când sunt instalate Project Operations și Vânzări)</br>- **Pe bază de serviciu de întreținere** (Disponibil când este instalat Dynamics 365 Field Service) | În Project Operations, valoarea acestui câmp este implicită **Bazat pe muncă** și clasifică contractul ca fiind un contract bazat pe proiecte. Un contract ar trebui să fie bazat pe proiect pentru a permite toate funcțiile și extensiile specifice proiectului. |
| Client potențial | Fila **Rezumat** | Referința la compania clienților sau la înregistrarea contului. Când un contract este creat dintr-o ofertă, acest câmp este copiat din câmpul corespunzător de pe înregistrarea ofertei. | Moneda din oferta de proiectul este implicită în funcție de moneda clientului. Acest lucru se poate schimba înainte ca contractul să fie salvat. |
| Manager de cont | Fila **Rezumat** | Numele Managerului de cont pentru această tranzacție. Când un contract este creat dintr-o ofertă, acest câmp este copiat din câmpul corespunzător de pe înregistrarea ofertei. | Managerul de cont este responsabil pentru gestionarea relației cu clientul prin finalizarea proiectului. Pe baza înregistrării resursei rezervabile legată de Managerul de cont, unitatea contractantă este implicită pe contractul de proiect. |
| Unitate contractantă | Fila **Rezumat** | Unitatea organizației responsabilă pentru livrarea proiectelor asociate acestui contract. Când un contract este creat dintr-o ofertă, acest câmp este copiat din câmpul corespunzător de pe înregistrarea ofertei. | Unitatea contractantă este divizia companiei care execută proiectele. Fiecare unitate contractantă are o monedă, iar această monedă este utilizată pentru a raporta costurile estimate și reale suportate în timpul proiectului. |
| Listă de prețuri produse | Fila **Rezumat** | Această listă de prețuri este utilizată pentru stabilirea prețurilor implicite pe liniile de contract bazate pe produse. Lista derulantă de opțiuni pentru acest câmp afișează o listă de liste de prețuri în care moneda listei de prețuri se potrivește cu moneda din contract. Când un contract este creat dintr-o ofertă, acest câmp este copiat din câmpul corespunzător de pe înregistrarea ofertei. Pe contractul de proiect, acest câmp este implicit din înregistrarea de cont, dar poate fi modificat. | Nu există nicio relevanță în aval pentru acest câmp. |
| Monedă | Fila **Rezumat** | Moneda utilizată pentru a raporta valoarea acestei oferte și moneda în care va fi facturat clientul. Când un contract este creat dintr-o ofertă, acest câmp este copiat din câmpul corespunzător de pe înregistrarea ofertei. Pe contractul de proiect, acest câmp este implicit din înregistrarea de cont, dar poate fi modificat. | După salvarea unui contract, acest câmp nu mai poate fi modificat. Acest câmp este utilizat pentru ca pe ofertă să fie produsul implicit și listele de preț de contract. Pe contract este utilizată moneda care să corespundă celei de pe lista de prețuri. |
| Limită de nedepășire | Fila **Rezumat** | Acest câmp indică limita negociată pentru valoarea finală pe care clientul a fost de acord pentru această tranzacție. | Limita superioară este evaluată în timpul execuției și se aplică tuturor elementelor rând și proiectelor asociate acestei oferte. |
| Dată de livrare solicitată | Fila **Rezumat** | Când un contract este creat dintr-o ofertă de proiect, acest câmp este copiat din câmpul corespunzător de pe oferta de proiect. | Această dată este utilizată ca dată de încheiere pentru a genera planificări de facturare. |

Următoarele KPI sunt disponibile pe fila **Executarea contractului** unui contract de proiect. 

>[!NOTE]
>Toate sumele de pe fila **Performanță contract** sunt exprimate în moneda implicită a mediului.

| Câmp | Locație | Descriere |
| --- | --- | --- |
| Valoare contract | Prezentarea generală a contractului | Valoarea totală a contractului de proiect.|
| Volum facturat | Prezentarea generală a contractului | Suma sumelor de pe toate facturile aferente acestui contract.|
| Cost achitat | Prezentarea generală a contractului | Suma tuturor costurilor reale înregistrate la toate proiectele care sunt mapate la contract. |
| Marjă brută | Prezentarea generală a contractului | Suma facturată - Cost suportat până în prezent / Suma facturată |
| Marjă estimată | Prezentarea generală a contractului | (Valoarea contractului - Costuri estimate) / Valoarea contractului Costuri estimate = Suma tuturor costurilor estimate pentru toate proiectele mapate la contract.|
| Valoare contract | Linii bazate pe proiect | Valoarea liniei de contract. |
| Sumă facturată | Linii bazate pe proiect | Pentru linia contractuală cu preț fix: Suma sumelor pentru toate cifrele de referință ale vânzărilor facturate față de această linie contractuală pe diverse facturi create pentru acest contract. Pentru linia contractuală de timp și material: Suma sumelor pentru toate cifrele tarifabile ale vânzărilor facturate față de această linie contractuală pe diverse facturi create pentru acest contract. |
| Cost achitat | Linii bazate pe proiect | Suma tuturor costurilor reale înregistrate la toate proiectele care sunt mapate la linia de contract. |
| Marjă brută | Linii bazate pe proiect | (Suma facturată - Cost suportat până în prezent) / Suma facturată |
| Marjă estimată | Linii bazate pe proiect | (Valoarea liniei contractului în moneda de bază - Costuri estimate pentru linia contractului în moneda de bază) / Valoarea liniei contractului în moneda de bază |
| Cost achitat | Detaliu al unei linii bazate pe proiecte | Timp: suma cantității de timp pentru costurile reale de timp înregistrate pentru acest rol în proiectul mapat la linia de contract. Cheltuieli: suma cantității de timp pentru toate costurile reale de timp înregistrate pentru această categorie în proiectul mapat la linia de contract. |
| Cantitate înregistrată | Detaliu al unei linii bazate pe proiecte | Timp: cantitatea totală de timp din costul timpului real pentru un rol din proiect care este mapat la această linie de contract. Cheltuieli: toate cantitățile pentru această categorie de cheltuială pe costurile cheltuielilor reale pe proiect sunt mapate la această linie de contract. |
| Volum facturat | Detaliu al unei linii bazate pe proiecte | Pentru o linie contractuală cu preț fix, acest câmp este lăsat necompletat la nivelul detaliilor și este afișat numai la nivelul liniei contractuale. Pentru o linie contractuală de timp și material, calculele sunt finalizate la nivel de detalii. Detaliile arată suma sumei pe toate liniile de venituri facturate din această linie contractuală care se plătesc. |
| Cantitate facturată | Detaliu al unei linii bazate pe proiecte | Pentru o linie contractuală cu preț fix, acest câmp este lăsat necompletat la nivelul detaliilor și este afișat numai la nivelul liniei contractuale. Pentru o linie contractuală de timp și material, calculele sunt finalizate la nivel de detalii pentru timp și cheltuieli. Timp: suma sumei orelor pe toate liniile de venituri facturate pentru acest rol din această linie contractuală care sunt tarifabile. Cheltuieli: toate cantitățile pentru această categorie de cheltuială pe costurile cheltuielilor reale pe proiect sunt mapate la această linie de contract. |
| Valoare contract | Linii bazate pe produs | Valoarea liniei contractuale a acestei linii contractuale bazate pe produse. |
| Volum facturat | Linii bazate pe produs | Suma sumelor de pe toate liniile de facturare față de această linie de contract pe produs pe diverse facturi care sunt create pentru acest contract. |
| Cost achitat | Linii bazate pe produs | Suma tuturor costurilor reale înregistrate pentru linia de contract bazată pe produs. |
| Marjă brută | Linii bazate pe proiect | Suma facturată - Cost suportat până în prezent / Suma facturată |
| Marjă estimată | Linii bazate pe produs | (Valoarea liniei contractului - Costuri estimate pentru linia contractului) / Valoarea liniei contractului |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
