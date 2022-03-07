---
title: Închiderea unei oferte - simplificat
description: Acest subiect furnizează informații despre închiderea unei oferte în Project Operations.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 8ae5e14220ffecab5bcfa016d8d18e6ccfbc5b04be9a4e66cee26f8885125d31
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994336"
---
# <a name="close-a-quote---lite"></a>Închiderea unei oferte - simplificat

_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_

O ofertă de proiect poate fi închisă drept câștigată sau pierdută. O ciornă a ofertei poate fi închisă deoarece operațiunile de activare și revizuire a cotațiilor nu sunt acceptate în Microsoft Dynamics 365 Project Operations.

## <a name="close-a-quote-as-won"></a>Închideți o ofertă drept Câștigată

Când închideți o ofertă de proiect drept Câștigat, starea este setată pe Închis și motivul pentru această stare este Câștigat. Închiderea ofertei face oferta de proiect doar în citire și creează o schiță de contract de proiect care conține informațiile despre ofertă. Deoarece o ofertă închisă nu poate fi redeschisă, un dialog de confirmare vă va confirma modificările.

Dacă oferta este atașată unei oportunități, orice alte oferte ale proiectului cu ocazia se închid automat ca Pierdute.

### <a name="financial-impact-of-closing-a-quote-as-won"></a>Impactul financiar al închiderii unei oferte drept câștigată

Dacă există date reale de timp pentru un proiect în timp ce este încă atașat la cironă de ofertă, se înregistrează doar costul timpului sau cheltuielilor. După închiderea unei oferte ca câștigat, aplicația va refactoriza costurile prin inversarea costurilor mai vechi și recrearea costurilor noi. Aplicația va procesa aceste costuri reale pe baza metodei de facturare a liniei contractului de proiect asociat. În cazul în care valorile reale ale costurilor fac referire la o linie de contract de timp și materiale, sunt create valorile reale de vânzare neînregistrate în contabilitate corespunzătoare pentru momentul când se închid ofertele și se creează contractul de proiect. În cazul în care valorile reale ale costurilor fac referire la o linie de contract cu preț fix, aplicația va înceta să reproceseze valorile reale ale costurilor care se bazează pe regulile de facturare divizată pentru clienții contractului de proiect.

## <a name="closing-a-quote-as-lost"></a>Închiderea unei oferte drept pierdută:

Când închideți o ofertă de proiect ca Pierdut, starea este setată pe Închis și motivul pentru această stare este Pierdut. Închiderea ofertei face ca oferta de proiect să fie doar în citire. Deoarece o ofertă închisă nu poate fi redeschisă și înainte de a închide o ofertă, un dialog de confirmare vă va confirma modificările.

Dacă oferta proiectului care este închisă ca Pierdut face referire la un proiect pe oricare dintre liniile sale, și respectivul proiect va fi marcat ca Închis. Orice rezervare de resurse începând cu ziua respectivă este anulată.

> [!NOTE]
> În Project Operations, închiderea unei cotații ca Câștigat sau Pierdut nu va avea un impact asupra stării oportunității, care va rămâne deschisă până când va fi închisă manual.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]