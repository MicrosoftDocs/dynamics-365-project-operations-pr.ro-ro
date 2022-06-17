---
title: Închiderea unei oferte - simplificat
description: Acest articol oferă informații despre închiderea unei cotații în Operațiuni de proiect.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: e3a199843f379dc53d63372f91e8be2e1bcbf4e9
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916947"
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