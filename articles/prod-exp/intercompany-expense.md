---
title: Cheltuieli între companii
description: Acest subiect oferă informații despre modul de utilizare a cheltuielilor inter-companii pentru a aloca cheltuielile unui lucrător persoanei juridice pentru care a fost efectuată munca.
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
ms.openlocfilehash: 553ddbe622210169db8de4aa506dcf1ea1e9d5ef
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960847"
---
# <a name="intercompany-expenses"></a>Cheltuieli între companii

Un lucrător care este angajat de o entitate juridică într-o organizație ar putea efectua lucrări pentru o altă entitate juridică din aceeași organizație. Puteți utiliza cheltuielile inter-companii pentru pentru a aloca cheltuielile lucrătorului persoanei juridice pentru care a fost efectuată munca. Persoana juridică care angajează lucrătorul se numește persoana juridică care împrumută. Persoana juridică pentru care lucrătorul efectuează cheltuieli se numește persoana juridică care împrumută. 

Înainte ca un lucrător să poată crea și trimite cheltuieli inter-companii, trebuie să activați liniile de cheltuieli inter-companii. Accesând persoana juridică care împrumută, pe pagina **Parametrii de gestionare a cheltuielilor**, selectați **Permiteți liniile de cheltuieli inter-companii**. 

## <a name="tax-posting-for-intercompany-expenses"></a>Înregistrare fiscală pentru cheltuieli între companii

[!include [banner](../includes/banner.md)]

Înainte de a putea utiliza grupuri de impozite care sunt asociate cu persoana juridică care împrumută (sursă) în locul entității juridice împrumutate (de destinație) în raportul dvs. de cheltuieli, trebuie să activați funcționalitatea în secțiunea de configurare a impozitului pe vânzări din registrul general. Cand **Persoană juridică pentru înregistrarea impozitelor inter-companii** parametrul este setat la **Sursă** și **Aplicați regulile de impozitare a impozitului pe vânzări** este setat pe **Nu**, se utilizează o combinația de impozite pentru persoana juridică care împrumută. Când același parametru este setat la **Destinaţie**, va fi utilizată combinația fiscală pentru împrumutarea entității juridice. Pentru persoanele juridice din Statele Unite, când parametrul este setat la **Sursă**, câmpul **Impozit pe vânzări de primit** trebuie configurat și pe noua pagină **Grupuri de înregistrare a registrului**. Motorul contabil va utiliza informațiile din acest câmp pentru înregistrarea contabilă referitoare la impozite.   
Comportamentul este consecvent pentru liniile de cheltuieli postate cu sau fără un proiect.  


[!INCLUDE[footer-include](../includes/footer-banner.md)]