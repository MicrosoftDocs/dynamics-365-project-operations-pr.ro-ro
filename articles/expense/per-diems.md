---
title: Diurne
description: Acest subiect oferă informații despre regulile per diem care sunt utilizate în gestionarea cheltuielilor.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 8d723b49e9556401c364b323cf58eaaf44906275
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128523"
---
# <a name="per-diems"></a>Diurne

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_


O diurnă este o indemnizație care se plătește unui lucrător care călătorește pentru muncă. În gestionarea cheltuielilor, puteți crea reguli pentru diurnă pentru diferite situații de călătorie. Tarifele diurnei se pot baza pe perioada anului, locația călătoriei sau ambele. Când creați o regulă de diurnă, puteți specifica că un procent din rata diemului va fi reținut dacă un lucrător primește mese sau servicii gratuite. De asemenea, puteți seta un număr minim și maxim de ore pe care le poate aplica tariful diurnei pentru călătoria unui lucrător.

## <a name="configuration"></a>Configurație 

1. Pentru a adăuga locații pentru diurnp, accesați **Configurare** > **Calcule și coduri** > **Locații diurnă**.
2. Pentru fiecare dintre locațiile adăugate mai sus, selectați o diurnă zilnică și o monedă valabile între o anumită dată de începere și de sfârșit pentru hotel, mese și alte cheltuieli. Ratele diurnei și valutele sunt configurate în **Configurare** > **Calcule și coduri** > **Diurne**.
3. Pe pagina **Locații diurnă**, configurați nivelurile de diurnă. Nivelurile de tarifare a diurnei vă permit să definiți procentul împărțirii unei diurne pentru hotel, masă și alte cheltuieli. 
4. Pentru a specifica reducerea procentuală a mesei pentru micul dejun, prânz sau cină, actualizați câmpurile de pe pagina **Parametrii de gestionare a cheltuielilor** pe fila **Diurnă**. 
    
## <a name="submit-expenses-using-per-diem"></a>Trimiteți cheltuielile folosind diurna
Pentru a trimite cheltuieli cu diurnele, utilizați categoria de cheltuieli **Diurnă** atunci când creați un raport de cheltuieli. Introduceți **Diurnă data de la**, **Diurnă data până la**, și **Locație diurnă**. Suma va fi calculată pe baza ratelor diurnei pentru locația selectată, iar reducerea mesei va fi calculată pe baza nivelurilor tarifelor diurne.
