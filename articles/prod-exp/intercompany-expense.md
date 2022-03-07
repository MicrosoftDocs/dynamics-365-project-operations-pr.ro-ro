---
title: Cheltuieli între companii
description: Acest subiect oferă informații despre modul de utilizare a cheltuielilor inter-companii pentru a aloca cheltuielile unui lucrător persoanei juridice pentru care a fost efectuată munca.
author: Surya Vaidyanathan
ms.date: 07/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 80ef42bf5274ff9a5c50e6dcb93995cfbbda40a66d7471f29ebf056086320640
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/06/2021
ms.locfileid: "7001221"
---
# <a name="intercompany-expenses"></a>Cheltuieli între companii

Un lucrător care este angajat de o entitate juridică într-o organizație ar putea efectua lucrări pentru o altă entitate juridică din aceeași organizație. Puteți utiliza cheltuielile inter-companii pentru pentru a aloca cheltuielile lucrătorului persoanei juridice pentru care a fost efectuată munca. Persoana juridică care angajează lucrătorul se numește persoana juridică care împrumută. Persoana juridică pentru care lucrătorul efectuează cheltuieli se numește persoana juridică care împrumută. 

Înainte ca un lucrător să poată crea și trimite cheltuieli inter-companii, trebuie să activați liniile de cheltuieli inter-companii. Accesând persoana juridică care împrumută, pe pagina **Parametrii de gestionare a cheltuielilor**, selectați **Permiteți liniile de cheltuieli inter-companii**. 

## <a name="tax-posting-for-intercompany-expenses"></a>Înregistrare fiscală pentru cheltuieli între companii

[!include [banner](../includes/banner.md)]

Înainte de a putea utiliza grupuri de impozite care sunt asociate cu persoana juridică care împrumută (sursă) în locul entității juridice împrumutate (de destinație) în raportul dvs. de cheltuieli, trebuie să activați funcționalitatea în secțiunea de configurare a impozitului pe vânzări din registrul general. Cand **Persoană juridică pentru înregistrarea impozitelor inter-companii** parametrul este setat la **Sursă** și **Aplicați regulile de impozitare a impozitului pe vânzări** este setat pe **Nu**, se utilizează o combinația de impozite pentru persoana juridică care împrumută. Când același parametru este setat la **Destinaţie**, va fi utilizată combinația fiscală pentru împrumutarea entității juridice. Pentru persoanele juridice din Statele Unite, când parametrul este setat la **Sursă**, câmpul **Impozit pe vânzări de primit** trebuie configurat și pe noua pagină **Grupuri de înregistrare a registrului**. Motorul contabil va utiliza informațiile din acest câmp pentru înregistrarea contabilă referitoare la impozite.   
Comportamentul este consecvent pentru liniile de cheltuieli postate cu sau fără un proiect.  

## <a name="new-expense-expression-builder"></a>Nou constructor de expresii de cheltuieli

Noul constructor de expresii de cheltuieli abordează probleme cu scenariile de cheltuieli între companii care utilizează proiecte. Această caracteristică asigură faptul că, atunci când creați o cheltuială între companii, politica de cheltuieli este corect validată în raport cu proiectul selectat pe linia de cheltuieli și că raportul de cheltuieli poate fi trimis cu succes.

Pentru ca funcția constructor de expresii de cheltuieli să funcționeze, trebuie să fie activată. În plus, ar trebui configurată politica de cheltuieli care are un ID de proiect.

Dacă ați configurat deja politici care validează ID-ul proiectului pe linia de cheltuieli, aceste politici trebuie să fie retrase. Apoi puteți activa caracteristica și să reconfigurați politicile.

Pentru a activa caracteristica, urmați pașii de mai jos.

1. Accesați **Spații de lucru** \> **Gestionare caracteristică**.
2. În listă, selectați **Noul constructor de expresii de cheltuieli pentru a aborda probleme cu scenariile de cheltuieli inter-companii care utilizează proiecte**. Selectați apoi **Activați acum**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
