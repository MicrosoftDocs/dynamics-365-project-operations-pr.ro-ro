---
title: Închideți o ofertă
description: Acest subiect furnizează informații despre închiderea ofertelor în Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3c429fa14b4b95420c67a91a6a59af7db2660f68
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898906"
---
# <a name="close-a-quote"></a>Închideți o ofertă

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

O ofertă de proiect poate fi închisă drept câștigată sau pierdută. Deoarece funcțiile Activare și Revizuire nu sunt acceptate pe ghilimele din Microsoft Dynamics 365 Project Operations, puteți închide o versiune preliminară.

## <a name="close-a-quote-as-won"></a>Închideți o ofertă drept Câștigată

Închiderea unei oferte de proiect ca Câștigat va seta starea cotației la **Închis** și motiv stare la **Câștigat**. Închiderea ofertelor îl face doar în citire și creează un proiect de contract de proiect cu toate informațiile despre ofertă. Deoarece o ofertă închisă nu poate fi redeschisă, înainte de a închide o ofertă, un dialog de confirmare vă va confirma modificările.

Contractul de proiect creat dintr-o ofertă de proiect este, de asemenea, disponibil în modulul de management al proiectului și contabilitate al Project Operations. Dacă un contract de proiect nu este asociat cu un proiect pe niciuna dintre liniile sale, acest contract de proiect este pus la dispoziție ca contract de proiect inactiv și devine activ de îndată ce un proiect este asociat cu cel puțin una dintre liniile sale de contract.

Dacă oferta este atașată unei oportunități, orice alte oferte ale proiectului cu ocazia se închid automat ca Pierdute.

### <a name="financial-impact-of-closing-a-quote-as-won"></a>Impactul financiar al închiderii unei oferte drept câștigată

Dacă au existat date reale pentru timpul înregistrat pe un proiect în timp ce acesta este încă atașat la o schiță de ofertă, se înregistrează doar costul timpului sau cheltuielilor. După închiderea unei oferte ca câștigat, aplicația va refactoriza costurile prin inversarea costurilor mai vechi și recrearea costurilor noi. Aplicația va procesa aceste costuri reale pe baza metodei de facturare a liniei contractului de proiect asociat. În cazul în care costurile reale fac referire la o linie contractuală de timp și materiale, sistemul va crea în mod automat cifre de vânzări corespondente nefacturate pentru momentul în care se închide oferta și se creează contractul de proiect. În cazul în care costurile reale se referă la o linie contractuală cu preț fix, aplicația va înceta să reproceseze costurile reale pe baza regulilor de facturare împărțite pentru clienții contractului de proiect.

Toate datele reale reprocesate sunt disponibile în modulul de management și contabilitate a proiectului pentru ca contabilul proiectului să le poată revizui, actualiza și posta în registrul general. 

## <a name="close-a-quote-as-lost"></a>Închideți o ofertă ca Pierdută

Închiderea unei oferte de proiect drept Pierdut va seta starea cotației la **Închis** și motiv stare la **Pierdut**. Închiderea ofertei îl face doar în citire. Deoarece o ofertă închisă nu poate fi redeschisă și înainte de a închide o ofertă, un dialog de confirmare vă va confirma modificările.

Dacă oferta de proiect care este închisă ca Pierdută are un proiect la care se face referire pe oricare dintre liniile sale, acel proiect este de asemenea marcat ca Închis și orice rezervare de resurse din acea zi înainte este anulată.

> [!NOTE]
> În Project Operations, închiderea unei cotații ca Câștigat sau Pierdut nu va avea un impact asupra stării oportunității, care va rămâne deschisă până când va fi închisă manual.
