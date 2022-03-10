---
title: Copierea ofertelor bazate pe proiect
description: Acest subiect furnizează informații despre cum să copiați ofertele bazate pe proiect în Project Operations.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 247f9d33bc2e7b0bcbeae8114bb436ed237efce660d0840e58d536d2a290639e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/06/2021
ms.locfileid: "6992176"
---
# <a name="copy-project-based-quotes"></a>Copierea ofertelor bazate pe proiect

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Puteți crea cu ușurință o nouă ofertă de proiect copiind una existentă. 

- Pentru a copia o ofertă de proiect, pe pagina listei **Oferte de proiect** sau pagina de detalii **Oferta proiectului**, selectați oferta proiectului pe care doriți să o copiați, apoi selectați **Copiați**.

Aceasta va deschide o pagină de dialog în care puteți introduce parametrii copiei. Următorul tabel listează câmpurile care sunt incluse în pagina de dialog. În funcție de valorile selectate, procesul de copiere se poate modifica.

| **Câmp** | **Descriere** | **Impactul din aval** |
| --- | --- | --- |
| Subiect | Introduceți subiectul relevant sau numele ofertei țintă. Când se deschide dialogul, sistemul îl va seta la subiectul ofertei sursă cu **-copie** anexat la acesta. | |
| Client potențial | Trimitere la compania clientului sau la înregistrarea contului. Când se deschide caseta de dialog, sistemul îl va seta la contul din oferta sursă. | Acest câmp este clientul principal din ofertă. |
| Unitate contractantă | Unitatea organizației care este responsabilă pentru livrarea proiectului/proiectelor asociate acestei tranzacții.
Când se deschide caseta de dialog, sistemul îl va seta la unitatea contractantă a ofertei sursă. | Unitatea contractantă este divizia companiei care va executa proiectele după încheierea tranzacției. Fiecare unitate contractantă are o monedă. Moneda este utilizată pentru a raporta costurile estimate și reale suportate în timpul execuției proiectului. |
| Monedă | Aceasta este moneda în care este calculată tranzacția. Când se deschide caseta de dialog, sistemul îl va seta la moneda ofertei sursă. Acest lucru poate fi modificat și dacă este modificat, câmpul **Preț copiere** este întotdeauna setat la **Nu**. Acest lucru se datorează faptului că listele de prețuri din ofertele sursă nu mai sunt relevante. | Moneda este utilizată pentru a stabili implicit o listă de prețuri, pentru a construi o estimare financiară pe oferta și, în cele din urmă, pentru a factura clientul atunci când tranzacția este câștigată. |
| Dată de livrare solicitată | Aceasta este data livrării solicitată de client. | Aceasta este utilizată ca dată de încheiere la crearea datelor de facturare pe o anumită frecvență. |
| Copiați prețul | O valoare Da/Nu indică dacă prețul din oferta trebuie copiat din oferta sursă. | Dacă **Da** este selectat, referințele pentru lista de prețuri a proiectului și lista de prețuri pentru produse sunt copiate din oferta sursă în oferta țintă. Dacă **Nu** este selectat, listele de prețuri sunt restabilite pe baza celor mai recente liste de prețuri care au fost configurate pe parametrii contului sau proiectului. |

Când selectați **OK** pe pagina de dialog, sistemul creează o copie a ofertei de proiect pe baza parametrilor selectați în dialog. Se deschide noua ofertă de proiect. 

> [!NOTE]
> Următoarele informații nu sunt copiate de la sursa la cota țintă:
>
> - Planificări factură
> - Ofertă și clienți de linie de ofertă
> - Referința proiectului pe liniile de ofertă bazate pe proiect - Informații despre bugetul clienților
>
>Deoarece aceste informații sunt foarte specifice fiecărei oferte, aceste câmpuri și înregistrări nu sunt copiate. Se copiază liniile de ofertă pentru proiecte și produse, estimările privind detaliile liniei de ofertă și valorile care nu trebuie depășite la nivelul ofertelor. Valoarea implicită a prețului și a costului depinde de opțiunea **Preț copiere** selectată pe pagina de dialog **Copiați parametrii**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]