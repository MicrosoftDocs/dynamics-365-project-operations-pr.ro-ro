---
title: Noutăți în iunie 2022 - implementare simplificată Project Operations
description: Acest articol oferă informații despre actualizările de calitate care sunt disponibile în versiunea din iunie 2022 a Microsoft Dynamics 365 Project Operations implementare simplă.
author: sigitac
ms.date: 06/03/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 8313288ecf7ff1350cd82c62d3d0c291d8a3ded4
ms.sourcegitcommit: 7772d72a7c96a44ffb23369f8ffb436813449239
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/20/2022
ms.locfileid: "9031208"
---
# <a name="whats-new-june-2022---project-operations-lite-deployment"></a>Noutăți în iunie 2022 - implementare simplificată Project Operations

_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_

Acest articol se aplică următoarelor componente și versiuni ale Microsoft Dynamics 365 Project Operations:

- Operațiuni de proiect în a Dataverse versiunea de mediu 4.43.0.77 sau 4.43.0.119

## <a name="quality-updates"></a>Actualizări de calitate

| Zonă de caracteristici | Număr de referință | Actualizare de calitate |
| --- | --- | --- |
| Subcontractare | 2708885 | S-a remediat mesajul de eroare care apare atunci când un utilizator creează o înregistrare antet de rezervare a resurselor rezervabile în care nu este completată nicio resursă rezervabilă. |
| Planificarea și urmărirea proiectului | 2629441 | S-a corectat logica de declanșare a fluxului de lucru pentru a ajuta la prevenirea unei bucle infinite atunci când sarcinile proiectului sunt actualizate. |
| Timp și cheltuieli | 2641209 | Importurile de intrări de timp din teme/rezervări trebuie să păstreze o referință de resurse care poate fi rezervată. |
| Planificarea și urmărirea proiectului | 2651148 | Antetul documentului de proiect trebuie protejat.|
| Planificarea și urmărirea proiectului | 2653145 | S-au adăugat validări pentru a se asigura că nu poate fi creată o înregistrare de proiect care are caractere nevalide în numele său. |
| Timp și cheltuieli | 2654710 | S-a corectat filtrarea pe **Aprobari** pagină. |
| Facturarea și stabilirea prețurilor | 2667805 | S-au adăugat validări pentru a preveni crearea de vânzări efective facturate dacă nu există susținerea vânzărilor reale nefacturate. |
| Facturarea și stabilirea prețurilor | 2668378 | Au fost adăugate validări pentru a împiedica adăugarea unei dimensiuni de preț personalizate, cu excepția cazului în care sunt completate un nume logic și un nume de câmp. |
| Timp și cheltuieli | 2700428 | S-a îmbunătățit logica aprobărilor pentru a se asigura că alte seturi de aprobare pentru proiect pot fi procesate chiar dacă unul dintre seturile de aprobare este blocat în joburile de sistem. |