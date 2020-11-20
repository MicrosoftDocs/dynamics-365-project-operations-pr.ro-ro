---
title: Închiderea unei oferte - simplificat
description: Acest subiect furnizează informații despre închiderea unei oferte în Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5ad206232d616cdbdc83e2a17b9177cfb98ffda9
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/30/2020
ms.locfileid: "4175726"
---
# <a name="close-a-quote---lite"></a>Închiderea unei oferte - simplificat

_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_

O ofertă de proiect poate fi închisă drept câștigată sau pierdută. Operațiunile de activare și revizuire asupra ofertelor nu sunt acceptate în Microsoft Dynamics 365 Project Operations, așa că o schiță de ofertă poate fi închisă.

## <a name="close-a-quote-as-won"></a>Închideți o ofertă drept Câștigată

Închiderea unei oferte de proiect drept Câștigată va închide oferta cu starea setată la Închisă și motivul de stare setat la Câștigat. Închiderea ofertei face oferta de proiect doar în citire și creează o schiță de contract de proiect care conține informațiile despre ofertă. Deoarece o ofertă închisă nu poate fi redeschisă, un dialog de confirmare Există un dialog de confirmare înainte de efectuarea modificărilor, deoarece o ofertă închisă nu poate fi redeschisă și modificările sunt ireversibile.

Dacă oferta este atașată unei oportunități, orice alte oferte ale proiectului cu ocazia se închid automat ca Pierdute.

### <a name="financial-impact-of-closing-a-quote-as-won"></a>Impactul financiar al închiderii unei oferte drept câștigată

Dacă au existat date reale pentru timpul înregistrat pe un proiect în timp ce acesta este încă atașat la o schiță de ofertă, se înregistrează doar costul timpului sau cheltuielilor. După închiderea unei oferte ca câștigat, aplicația va refactoriza costurile prin inversarea costurilor mai vechi și recrearea costurilor noi. Aplicația va procesa aceste costuri reale pe baza metodei de facturare a liniei contractului de proiect asociat. În cazul în care costurile reale fac referire la o linie contractuală de timp și materiale, sistemul va crea în mod automat cifre de vânzări corespondente nefacturate pentru momentul în care se închide oferta și se creează contractul de proiect. În cazul în care costurile reale se referă la o linie contractuală cu preț fix, aplicația va înceta să reproceseze costurile reale pe baza regulilor de facturare împărțite pentru clienții contractului de proiect.

## <a name="closing-a-quote-as-lost"></a>Închiderea unei oferte drept pierdută:

Închiderea unei oferte de proiect drept Pierdut va seta starea cotației la Închis și motiv stare la Pierdut. Închiderea ofertei face ca oferta de proiect să fie doar în citire. Deoarece o ofertă închisă nu poate fi redeschisă și înainte de a închide o ofertă, un dialog de confirmare vă va confirma modificările.

Dacă oferta de proiect care este închisă ca Pierdută are un proiect la care se face referire pe oricare dintre liniile sale, acel proiect este de asemenea marcat ca Închis și orice rezervare de resurse din acea zi înainte este anulată.

> [!NOTE]
> În Project Operations, închiderea unei cotații ca Câștigat sau Pierdut nu va avea un impact asupra stării oportunității, care va rămâne deschisă până când va fi închisă manual.
