---
title: Avansuri și contracte bazate pe garanții - simplificat
description: Acest subiect furnizează informații despre modele de contractare și avansuri pe bază de onorariu în Project Operations.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 912b235af5e561349fdfb481e5f5b7c5514669c3
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/31/2020
ms.locfileid: "4180882"
---
# <a name="advances-and-retainer-based-contracts---lite"></a>Avansuri și contracte bazate pe garanții - simplificat


_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_

Dynamics 365 Project Operations acceptă contracte bazate pe onorarii. Un contract bazat pe onorariu este un set negociat de plăți distribuite în mod egal pentru care clientul va fi facturat pe toată durata unui proiect. Acest tip de contract este de obicei utilizat pentru modele de facturare bazate pe timp și materiale sau consum, în cazul în care este nevoie să ofere clientului o factură previzibilă și un program de plată. Veniturile efective acumulate în fiecare perioadă sunt reconciliate cu plata primită de la client la începutul perioadei. În conformitate cu conceptul modelului de facturare Timp și Material, valorile veniturilor acumulate în fiecare perioadă pot varia în funcție de costurile suportate. Dacă veniturile acumulate sunt mai mari decât suma primită la începutul perioadei, compania de livrare a proiectului ar putea:

- Facturați clientul numai pentru excedent 
- Amânați reconcilierea veniturilor cu următoarea perioadă de facturare și efectuați o ultimă factură la sfârșitul proiectului pentru orice venit rămas neconciliat

Principala diferență între un model de contractare bazat pe garanție și un model de contract cu preț fix în Project Operations este că în modelul contractului cu preț fix, suma facturii nu este legată sau legată de costurile suportate. Facturarea urmează o abordare bazată pe reper, care este aliniată la costurile suportate pentru acea perioadă. Într-un contract bazat pe garanții, veniturile care pot fi facturate sunt înregistrate pe baza metodei de facturare pe linia contractului. Atunci când metoda de facturare este în timp și semnificativă, venitul facturabil este legat de costurile suportate într-o anumită perioadă și poate varia de la o perioadă la alta. Cu toate acestea, clientului i se facturează numai suma pe reținerea periodică. Sistemul folosește o altă factură la sfârșitul perioadei pentru a concilia veniturile facturabile înregistrate în perioada respectivă cu suma pentru care a fost facturat clientul la începutul perioadei.

Avantajul acestei metode constă în faptul că costurile clientului devin previzibile în programul de reținere, spre deosebire de un model tipic de timp și material. Organizația care livrează proiectul are, de asemenea, un spațiu pentru acoperirea riscului de recuperare a costurilor suportate din cauza oricăror creșteri de domeniu pe care un model de preț fix nu le-ar fi permis.

În plus față de un program periodic bazat pe reținere, Project Operations pot înregistra un avans unic de la un client și pot concilia acest lucru cu diferitele componente ale costului proiectului.

Sistemul de reținere din Project Operations nu este disponibil pentru utilizare până când nu este facturat clientului. Acest lucru este indicat de următoarele câmpuri de pe subgrilă pentru avansuri și onorarii.

| Câmp | Descriere | Impactul din aval |
| --- | --- | --- |
| Sumă disponibilă | Suma disponibilă pentru a fi utilizată în înregistrarea de onorariu sau avans. | Până când nu se facturează avansul sau onorariul, acesta nu este disponibil pentru a fi utilizat, ceea ce înseamnă că suma disponibilă va fi zero. |
| Sumă utilizată | Suma care este deja utilizată pe onorariu sau avans. | Un avans sau un onorariu poate fi parțial împăcat pe o factură cu costurile efective care vor avea o parte marcată ca fiind deja utilizată sau consumată. Restul sumei avansului sau onorariului este disponibil pentru a se reconcilia pe o factură viitoare cu costurile reale. |
