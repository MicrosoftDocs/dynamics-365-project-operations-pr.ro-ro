---
title: Definiți politicile de cheltuieli
description: Puteți defini politicile de cheltuieli pe care lucrătorii dvs. trebuie să le urmeze atunci când introduc și depun rapoarte de cheltuieli și cereri de călătorie.
author: suvaidya
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: d29b1a9c1a935b933f403f78279b74577d11089007ce1d1090c361075822263a
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986371"
---
# <a name="define-expense-policies"></a>Definiți politicile de cheltuieli

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Puteți defini politicile pe care lucrătorii dvs. trebuie să le urmeze atunci când introduc și depun rapoarte de cheltuieli și cereri de călătorie.         
Implementarea politicilor de cheltuieli vă poate ajuta să gestionați eficient cheltuielile.         

De exemplu, puteți seta o politică pentru cheltuielile hoteliere din New York, care prevede că cheltuielile pe noapte nu pot depăși USD 250.       
Dacă un lucrător depune un raport de cheltuieli sau o cerere de călătorie în cazul în care tariful camerei depășește această sumă, sistemul va notifica         
Lucrătorului că suma poliței pentru cheltuială a fost depășită. Puteți configura mesajul pe care muncitorul îl va primi atunci când        
definiți politica.      
        
Puteți defini trei tipuri de politici:         
        
- **Avertizare**: Permite lucrătorului să depună un raport de cheltuieli sau o cerere de călătorie, dar cheltuielile vor fi marcate pentru toți aprobatorii și         
  pentru raportare ulterioară.        

- **Eroare**: Solicită lucrătorului să revizuiască cheltuiala pentru a se conforma politicii înainte de a trimite raportul de cheltuieli sau cererea de călătorie.        
 
 - **Justificare**: Solicită lucrătorului sau unui manager să introducă o justificare pentru depășirea sumei poliței înainte de a trimite raportul de cheltuieli sau cererea de călătorie.        

## <a name="policy-tips"></a>Sfaturi de politică
Iată câteva sugestii care vă pot ajuta atunci când creați noi politici pentru gestionarea cheltuielilor: 

- Politicile intră în vigoare, ceea ce înseamnă că o politică nu va intra în vigoare dacă este creată cu o dată după data la care s-a produs cheltuiala. De exemplu, creați astăzi o nouă politică pentru a impune o cheltuială maximă de masă de $50. Orice cheltuieli existente introduse începând de ieri nu vor fi comparate cu această politică.
- Când creați o politică pentru o categorie de cheltuieli care poate fi detaliată, luați în considerare adăugarea unei condiții pentru tipul de linie de cheltuieli. Este posibil ca unele politici, cum ar fi solicitarea unei chitanțe, să nu aibă sens pentru liniile detaliate. În această situație, politica se aplică numai liniei de antet sau unei linii ne-detaliate. 
- Politicile de gestionare a cheltuielilor sunt evaluate în mod implicit în raport cu entitatea sursă. Pentru scenariile între companii, puteți seta politica care urmează să fie evaluată în raport cu entitatea de destinație (entitatea care împrumută). Pentru a rula politicile împotriva entității de destinație, activați caracteristica **Evaluați politica de cheltuieli împotriva împrumutului entității juridice** în spațiul de lucru **Gestionarea caracteristicilor**.

## <a name="when-to-evaluate-policies"></a>Când se evaluează politicile

În parametrii de gestionare a cheltuielilor, puteți selecta să evaluați politicile de gestionare a cheltuielilor atunci când este salvată o linie sau când este trimis un raport de cheltuieli. Dacă alegeți să evaluați când este salvată o linie, utilizatorii vor avea o vizibilitate mai timpurie a ceea ce trebuie să facă pentru a completa raportul de cheltuieli dintr-o dată. În caz contrar, puteți întârzia evaluarea politicii și puteți economisi timp validând la final, în timpul trimiterii la fluxul de lucru.


[!INCLUDE[footer-include](../includes/footer-banner.md)]