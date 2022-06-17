---
title: Impactul real pentru un proiect intern
description: Acest articol oferă informații despre impactul asupra tabelului Actuals la diferite evenimente pentru un proiect intern în Microsoft Dynamics 365 Project Operations.
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
ms.openlocfilehash: de05714c079fe121ef68e28b1acb82c24bce095e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921363"
---
# <a name="actuals-impact-for-an-internal-project"></a>Impactul real pentru un proiect intern

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Următorul tabel listează datele reale ale diferitelor tipuri de tranzacții care sunt create la diferite evenimente într-un proiect intern.

| Eveniment | Cost real | Exemplu |
|---|---|---|
| Timpul este creat. | Nu se aplică | <p>Bob Kozack, de la unitatea organizațională Fabrikam din SUA, care are o rată de cost de 100 de dolari SUA (100 USD) pe oră, lucrează la un proiect care se numește „Instalare Arm la Adatum”. Acest proiect este mapat la o metodă de facturare cu preț fix pe linia contractului. Iată un exemplu de intrare de timp de la Bob Kozak:</p><p>Bob Kozack - 8 ore</p> |
| Timpul este transmis. | Nu se aplică | Este creată o linie de jurnal de cost pentru înregistrarea timpului. Rata de cost implicită este introdusă în înregistrarea jurnalului. |
| Ora este rechemată înainte de a fi aprobată. | Nu se aplică | |
| Ora este aprobată. | Este creat un cost real. | <p>Un nou real care este creat:</p><ul><li>**Cost real:** Bob Kozack, 8 ore, USD 800</li></ul> |
| Aprobarea timpului este anulată. | <p>Starea de ajustare a costului inițial real este actualizată la **Ajustat**.</p><p>Este creat un cost real de inversare care are o stare de ajustare de **Nereglabil**.</p> | <p>Actual existent care este actualizat:</p><ul><li>**Cost real:** Bob Kozack, 8 ore, USD 800, *Ajustat*</li></ul><p>Un nou real creat pentru a inversa impactul financiar anterior:</p><ul><li>**Cost real:** Bob Kozack, (8 ore), (800 USD), *Nereglabil*</li></ul> |
| Ora este rechemată după ce este aprobată. | <p>Starea de ajustare a costului inițial real este actualizată la **Ajustat**.</p><p>Este creat un cost real de inversare care are o stare de ajustare de **Nereglabil**.</p> | <p>Actual existent care este actualizat:</p><ul><li>**Cost real:** Bob Kozack, 8 ore, USD 800, *Ajustat*</li></ul><p>Un nou real creat pentru a inversa impactul financiar anterior:</p><ul><li>**Cost real:** Bob Kozack, (8 ore), (800 USD), *Nereglabil*</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
