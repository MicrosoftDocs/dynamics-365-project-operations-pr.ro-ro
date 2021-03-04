---
title: Antet/rezumat de oportunitate
description: Acest subiect oferă informații despre oferte bazate pe proiecte și liniile de oportunitate bazate pe proiecte.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1344e21d58fbc28198468146f9cea9cf00572d7d
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181242"
---
# <a name="opportunity-settings"></a>Setări de oportunitate

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_


Antetul sau rezumatul Oportunitate captează informațiile generale despre o afacere bazată pe proiect care se aplică tuturor liniilor unei oportunități bazate pe proiect.

Oportunitățile bazate pe proiecte în Dynamics 365 Project Operations sunt extensii de oportunități în Dynamics 365 Sales. Aceste extensii oferă funcționalități suplimentare specifice și necesare pentru oportunități bazate pe proiecte. Aceste extensii pot include câmpuri noi și acțiuni panglică disponibile în oportunități bazate pe proiecte. Este posibil să găsiți câteva câmpuri, funcționalitate și logică implicită care sunt disponibile în Vânzări nu sunt disponibile în Project Operations.

Următorul tabel include câmpurile dintr-o oportunitate bazată pe proiect, care sunt fie unice pentru Project Operations, fie au unele modificări importante în comportament din oportunitățile în vânzări.

| **Câmp** | **Locaţie** | **Descriere** | **Impactul din aval** |
| --- | --- | --- | --- |
| Tip | Fila General (ascuns) | Acest câmp set de opțiuni are următoarele opțiuni:</br>- Bazat pe muncă (disponibil numai cu Project Operations)</br>- Pe bază de element (disponibil numai atunci când sunt instalate Project Operations și Vânzări)</br>- Serviciu bazat pe întreținere (disponibil când este instalat Field Service) | Când utilizați Project Operations, această valoare a câmpului este setată automat la **Bazat pe muncă** care clasifică oportunitatea ca fiind bazată pe proiect. O oportunitate ar trebui să fie bazată pe proiect pentru a permite toate extensiile și funcționalitățile specifice proiectului în procesul de vânzare din aval pentru această ofertă. |
| Firmă proprietară | Fila General | Aceasta este compania sau entitatea juridică care va livra proiectul pentru client. | Aceste informații despre câmp vor fi copiate în câmpul corespunzător din Oferta de proiect care este creată din această oportunitate. |
| Contact | Fila General | Trimitere la persoana de contact principală a clientului pentru această tranzacție. | |
| Cont | Fila General | Trimitere la compania clientului sau la înregistrarea contului. | |
| Manager de cont | Fila General | Numele managerului de cont pentru această oportunitate bazată pe proiect. | Managerul de cont este responsabil pentru gestionarea relației cu clientul prin finalizarea acestui proiect. Pe baza înregistrării resursei rezervabile legată de Managerul de cont, unitatea contractantă este implicită. |
| Unitate contractantă | Fila General | Unitatea organizației care este responsabilă pentru livrarea proiectului sau proiectelor asociate acestei tranzacții. | Unitatea contractantă este divizia companiei care va finaliza proiectele după încheierea tranzacției. Fiecare unitate contractantă are o monedă, iar această monedă este utilizată pentru a raporta costurile estimate și reale suportate în timpul proiectului. |

Pentru toate celelalte câmpuri și secțiuni de pe fila **Rezumat** a oportunității, consultați [Creați sau editați oportunități (Vânzări și Hub de vânzări)](https://docs.microsoft.com/dynamics365/sales-enterprise/create-edit-opportunity-sales).


[!INCLUDE[footer-include](../includes/footer-banner.md)]