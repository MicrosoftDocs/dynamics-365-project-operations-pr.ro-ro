---
title: Configurați kilometrajul utilizând nivelurile de rată a kilometrajului
description: Acest articol oferă informații despre ratele de kilometraj și nivelurile de rate de kilometri.
author: suvaidya
ms.date: 05/20/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 03ca18c8fef6228f2ba553ebe50447beda5a857c
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930149"
---
# <a name="set-up-mileage-using-mileage-rate-tiers"></a>Configurați kilometrajul utilizând nivelurile de rată a kilometrajului

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

Când se raportează o cheltuială și categoria de cheltuieli selectată este **Kilometraj**, suma pentru acea linie de cheltuieli este calculată în conformitate cu suma *rata pe kilometraj*. Această sumă este determinată prin utilizarea nivelurilor de kilometraj definite sau, dacă nu sunt stabilite niveluri ale ratei de kilometraj, urmând o rată standard a kilometrajului. 

Nivelurile de rată a kilometrajului pot fi configurate accesând **Managementul cheltuielilor** > **Configurare** > **General** > **Categorii de cheltuieli** > **Kilometraj** > **Configurare categorie**.

După actualizarea la 10.0.18, dacă organizația dvs. folosește categoria de cheltuieli de kilometraj, luați în considerare activarea caracteristicii de kilometraj după examinarea modificărilor de proiectare de mai jos. 

Noul design al nivelurilor ratei de kilometraj influențează modul în care valoarea în câmpul **Cantitate** este procesat. Înainte de lansarea din 10.0.18, valoarea în câmpul **Cantitate** a fost considerat a fi limita inferioară. Când acumularea a depășit acea valoare, a fost utilizată rata corespunzătoare.  Începând cu 10.0.18, valoarea în câmpul **Cantitate** este considerat limita superioară. Rata corespunzătoare este utilizată atunci când acumularea de kilometri este mai mică decât valoarea din câmpul **Cantitate**.  Noul model pentru nivelurile de kilometraj ajută la consecvența nivelurilor de kilometraj și la o utilizare mai bună.   

Toate rapoartele de cheltuieli aprobate vor fi recalculate în timpul înregistrării conform noului design.

## <a name="example"></a>Exemplu
 
### <a name="before-version-10018"></a>Înainte de versiunea 10.0.18
Cu două niveluri de rată de kilometraj, câmpul **Cantitate** din fiecare nivel reprezintă limita inferioară de kilometraj. În prezent, nivelul 1 are o valoare de zero (0) și o rată de 0,45, iar nivelul doi are o valoare de 1000 și o rată de 0,25. Dacă mile sau kilometri acumulați depășesc valoarea din câmp, se utilizează rata corelată. Dacă nu există nicio linie cu cantitate zero, sistemul utilizează rata de kilometraj care este definită în gestionarea cheltuielilor. 
 
Dacă un angajat depune un raport de cheltuieli cu 1.500 de mile, cele două linii de kilometraj din raportul de cheltuieli afișat ar fi: 1000 (rata 0,45) + 500 (rata 0,25) = 575,00.

### <a name="after-version-10018"></a>După versiunea 10.0.18
În 10.0.18, câmpul **Cantitate** din fiecare nivel reprezintă limita superioară a nivelului. În prezent, nivelul 1 are o valoare de 999 și o rată de 0,45, iar nivelul doi are o valoare de 999.999.999,00 și o rată de 0,25. Dacă mile sau kilometri acumulați depășesc valoarea din câmpul **Cantitate**, se utilizează rata corelată. Dacă toate limitele superioare sunt depășite, sistemul utilizează rata de kilometraj care este definită în gestionarea cheltuielilor. 
 
Pentru a calcula corect același scenariu, configurarea nivelului trebuie modificată. Câmpul **Cantitate** din primul nivel are o valoare de 999,00 și o valoare de 999.999.999,00 în nivelul doi. Dacă un angajat depășește cantitatea totală de mile sau kilometri în primul nivel, sistemul utilizează rata de kilometraj definită în gestionarea cheltuielilor. 
  
Dacă un angajat depune un raport de cheltuieli cu 1.500 de mile, cele două linii de kilometraj din raportul de cheltuieli afișat ar fi: 1000 (rata 0,45) + 500 (rata 0,25) = 575

## <a name="enable-the-mileage-amount-calculation-for-multiple-mileage-tiers-with-same-rate-feature"></a>Activați calculul cantității de kilometraj pentru mai multe niveluri de kilometraj cu aceeași caracteristică de tarif

Caracteristica **Calculul cantității de kilometraj pentru mai multe niveluri de kilometraj cu aceeași caracteristică de tarif** îmbunătățește calculul ratei de kilometraj. Parcurgeți pașii următori pentru a activa această caracteristică.

1. Accesați **Spații de lucru** > **Gestionare caracteristică**. 
2. În listă, localizați și selectați **Calculul valorii kilometrajului pentru mai multe niveluri de kilometraj cu aceeași rată**, apoi selectați **Activați acum**.

După ce activați caracteristica, resetați nivelurile de kilometraj pentru a reflecta corect valoarea câmpului **Cantitate**. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
