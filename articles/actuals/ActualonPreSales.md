---
title: Impactul datelor reale în timpul etapei de pre-vânzare a unui angajament
description: Acest articol oferă informații despre impactul asupra tabelului Valori reale la diferite evenimente din timpul fazei de pre-vânzare a unui angajament în Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 02/22/2022
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: d03d6ac2154806189d0d9d0b232bb317f51071ba
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922375"
---
# <a name="actuals-impact-during-the-pre-sales-stage-of-an-engagement"></a>Impactul datelor reale în timpul etapei de pre-vânzare a unui angajament

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Următorul tabel enumeră datele reale ale diferitelor tipuri de tranzacții care sunt create la diferite evenimente pe parcursul fazei de pre-vânzare a unui angajament de proiect.

| Eveniment | Cost real | Exemplu |
|---|---|---|
| Timpul este creat. | Nu se aplică | <p>Bob Kozack, de la unitatea organizațională Fabrikam din S.U.A., care are o rată de cost de 100 de dolari S.U.A. (100 USD) pe oră, lucrează la un proiect care se numește „Instalare Arm la Adatum”. Acest proiect este mapat la o metodă de facturare cu preț fix pe linia de contract. Iată un exemplu de intrare de timp de la Bob Kozak:</p><p>Bob Kozack - 8 ore</p> |
| Timpul este transmis. | Nu se aplică | Se creează o linie de jurnal de cost pentru intrarea de timp. Rata de cost implicită este introdusă în intrarea jurnal. |
| Intrarea de timp este retrasă înainte de a fi aprobată. | Nu se aplică | |
| Timpul este aprobat. | Este creat un cost real. | <p>Noua valoare reală care este creată:</p><ul><li>**Cost real:** Bob Kozack, 8 ore, 800 USD</li></ul> |
| Aprobarea timpului este anulată. | <p>Starea de ajustare a costului real inițial este actualizată la **Ajustat**.</p><p>Este creat un cost real de inversare care are o stare de ajustare de **Nereglabil**.</p> | <p>Valoarea reală existentă care este actualizată:</p><ul><li>**Cost real:** Bob Kozack, 8 ore, 800 USD, *Ajustat*</li></ul><p>Noua valoare reală care este creată pentru a inversa impactul financiar anterior:</p><ul><li>**Cost real:** Bob Kozack, (8 ore), (800 USD), *Nereglabil*</li></ul> |
| Intrarea de timp este retrasă după aprobare. | <p>Starea de ajustare a costului real inițial este actualizată la **Ajustat**.</p><p>Este creat un cost real de inversare care are o stare de ajustare de **Nereglabil**.</p> | <p>Valoarea reală existentă care este actualizată:</p><ul><li>**Cost real:** Bob Kozack, 8 ore, 800 USD, *Ajustat*</li></ul><p>Noua valoare reală care este creată pentru a inversa impactul financiar anterior:</p><ul><li>**Cost real:** Bob Kozack, (8 ore), (800 USD), *Nereglabil*</li></ul> |
| Oferta este câștigată și se creează un contract. | <p>Starea de ajustare a vechiului cost real este actualizată la **Ajustat**.</p><p>Sunt create valori reale pentru un cost de inversare care au ca stare de ajustare **Nereglabil**.</p><p>Noi valori reale pentru cost sunt create după reevaluarea regulilor contractuale.</p> | <p>Valoarea reală existentă care este actualizată:</p><ul><li>**Cost real:** Bob Kozack, 8 ore, 800 USD, *Ajustat*</li></ul><p>Noua valoare reală care este creată pentru a inversa impactul financiar anterior:</p><ul><li>**Cost real:** Bob Kozack, (8 ore), (800 USD), *Nereglabil*</li></ul><p>Noi date reale care sunt create pentru impactul financiar reevaluat atunci când oferta este câștigată și contractul este creat:</p><ul><li>**Cost real:** Bob Kozack, 8 ore, 800 USD</li><li>**Vânzări reale nefacturate:** Bob Kozack, 8 ore, 1.600 USD</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
