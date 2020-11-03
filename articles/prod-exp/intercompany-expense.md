---
title: Cheltuieli între companii
description: Un lucrător care este angajat de o entitate juridică într-o organizație ar putea efectua lucrări pentru o altă entitate juridică din aceeași organizație. În această situație, puteți utiliza caracteristica de cheltuieli între companii pentru a aloca cheltuielile lucrătorului persoanei juridice pentru care a fost efectuată lucrarea.
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0967f23e4e1f8e0431c55d4d54554e7e90e2451c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082947"
---
# <a name="intercompany-expenses"></a>Cheltuieli între companii

[!include [banner](../includes/banner.md)]

Un lucrător care este angajat de o entitate juridică într-o organizație ar putea efectua lucrări pentru o altă entitate juridică din aceeași organizație. În această situație, puteți utiliza caracteristica de cheltuieli între companii pentru a aloca cheltuielile lucrătorului persoanei juridice pentru care a fost efectuată lucrarea. Persoana juridică care angajează lucrătorul se numește persoana juridică care împrumută. Persoana juridică pentru care lucrătorul efectuează cheltuieli se numește persoana juridică care împrumută. 

Înainte ca un lucrător să poată crea și depune cheltuieli pentru munca efectuată pentru o altă entitate juridică, în entitatea juridică care împrumută, pe pagina **Parametrii de gestionare a cheltuielilor** , selectați opțiunea **Permiteți liniile de cheltuieli între companii**. 

## <a name="tax-posting-for-intercompany-expenses"></a>Înregistrare fiscală pentru cheltuieli între companii

[!include [banner](../includes/banner.md)]

Dacă doriți să utilizați grupuri de impozite care sunt asociate cu persoana juridică de împrumut (sursă) în locul entității juridice de împrumut (de destinație) în raportul dvs. de cheltuieli, va trebui să configurați acest lucru în setul de impozitare pe contabilitate. Când parametrul contabil general, **Persoană juridică pentru înregistrarea impozitelor între companii** este setat la **Sursă** și **Aplicați regulile de impozitare a impozitului pe vânzări** este setat la **Nu** , va fi utilizată combinația de impozite pentru persoana juridică care împrumută. Când același parametru este setat la **Destinaţie** , va fi utilizată combinația fiscală pentru împrumutarea entității juridice. Pentru persoanele juridice din Statele Unite, când parametrul este setat la **Sursă** , câmpul **Impozit pe vânzări de primit** trebuie configurat și pe noua pagină **Grupuri de înregistrare a registrului**. Motorul contabil va utiliza informațiile din acest câmp pentru înregistrarea contabilă legată de impozite.   
Comportamentul este consecvent pentru liniile de cheltuieli postate cu sau fără un proiect.  
