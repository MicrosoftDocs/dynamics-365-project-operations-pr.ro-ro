---
title: Impactul real în timpul etapei de pre-vânzare a unui angajament
description: Acest articol oferă informații despre impactul asupra tabelului Realități la diferite evenimente în timp ce o implicare este în stadiul de pre-vânzare în Microsoft Dynamics 365 Project Operations.
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
# <a name="actuals-impact-during-the-pre-sales-stage-of-an-engagement"></a>Impactul real în timpul etapei de pre-vânzare a unui angajament

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Următorul tabel listează datele reale ale diferitelor tipuri de tranzacții care sunt create la diferite evenimente în timpul etapei de pre-vânzare a unui angajament de proiect.

| Eveniment | Cost real | Exemplu |
|---|---|---|
| Timpul este creat. | Nu se aplică | <p>Bob Kozack, de la unitatea organizațională Fabrikam din SUA, care are o rată de cost de 100 de dolari SUA (100 USD) pe oră, lucrează la un proiect care se numește „Instalare Arm la Adatum”. Acest proiect este mapat la o metodă de facturare cu preț fix pe linia contractului. Iată un exemplu de intrare de timp de la Bob Kozak:</p><p>Bob Kozack - 8 ore</p> |
| Timpul este transmis. | Nu se aplică | Este creată o linie de jurnal de cost pentru înregistrarea timpului. Rata de cost implicită este introdusă în înregistrarea jurnalului. |
| Ora este rechemată înainte de a fi aprobată. | Nu se aplică | |
| Ora este aprobată. | Este creat un cost real. | <p>Un nou real care este creat:</p><ul><li>**Cost real:** Bob Kozack, 8 ore, USD 800</li></ul> |
| Aprobarea timpului este anulată. | <p>Starea de ajustare a costului inițial real este actualizată la **Ajustat**.</p><p>Este creat un cost real de inversare care are o stare de ajustare de **Nereglabil**.</p> | <p>Actual existent care este actualizat:</p><ul><li>**Cost real:** Bob Kozack, 8 ore, USD 800, *Ajustat*</li></ul><p>Un nou real creat pentru a inversa impactul financiar anterior:</p><ul><li>**Cost real:** Bob Kozack, (8 ore), (800 USD), *Nereglabil*</li></ul> |
| Ora este rechemată după ce este aprobată. | <p>Starea de ajustare a costului inițial real este actualizată la **Ajustat**.</p><p>Este creat un cost real de inversare care are o stare de ajustare de **Nereglabil**.</p> | <p>Actual existent care este actualizat:</p><ul><li>**Cost real:** Bob Kozack, 8 ore, USD 800, *Ajustat*</li></ul><p>Un nou real creat pentru a inversa impactul financiar anterior:</p><ul><li>**Cost real:** Bob Kozack, (8 ore), (800 USD), *Nereglabil*</li></ul> |
| Cotația este câștigată și se creează un contract. | <p>Starea de ajustare a vechilor costuri reale este actualizată la **Ajustat**.</p><p>Sunt create costurile reale de inversare care au o stare de ajustare de **Nereglabil**.</p><p>Noile costuri reale sunt create după reevaluarea regulilor contractuale.</p> | <p>Actual existent care este actualizat:</p><ul><li>**Cost real:** Bob Kozack, 8 ore, USD 800, *Ajustat*</li></ul><p>Un nou real creat pentru a inversa impactul financiar anterior:</p><ul><li>**Cost real:** Bob Kozack, (8 ore), (800 USD), *Nereglabil*</li></ul><p>Noi date reale care sunt create pentru impactul financiar reevaluat atunci când cotația este câștigată și este creat contractul:</p><ul><li>**Cost real:** Bob Kozack, 8 ore, USD 800</li><li>**Vânzări reale nefacturate:** Bob Kozack, 8 ore, USD 1,600</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
