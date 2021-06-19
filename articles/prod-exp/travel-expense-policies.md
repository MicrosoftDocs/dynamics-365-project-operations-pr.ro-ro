---
title: Configurarea politicilor de cheltuieli
description: Puteți configura politicile de cheltuieli pe care lucrătorii dvs. trebuie să le urmeze atunci când introduc și depun rapoarte de cheltuieși și cereri de călătorie în Microsoft Dynamics 365 Finance.
author: suvaidya
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fa4f628a918e6e099a723ed05994f63d6ad847f5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005761"
---
# <a name="set-up-expense-policies"></a>Configurarea politicilor de cheltuieli

Puteți defini politicile pe care lucrătorii dvs. trebuie să le urmeze atunci când introduc și depun rapoarte de cheltuieli și cereri de călătorie.         
Implementarea politicilor de cheltuieli vă poate ajuta să gestionați eficient cheltuielile.         

De exemplu, puteți seta o politică pentru cheltuielile hoteliere din New York, care prevede că cheltuielile pe noapte nu pot depăși USD 250.       
Dacă un lucrător depune un raport de cheltuieli sau o cerere de călătorie în care tariful camerei depășește această sumă, sistemul va notifica        
Lucrătorului că suma poliței pentru cheltuială a fost depășită. Puteți configura mesajul pe care muncitorul îl va primi atunci când        
definiți politica.      
        
Puteți defini trei tipuri de politici:         
        
- Avertizare - Permite lucrătorului să depună un raport de cheltuieli sau o cerere de călătorie, dar cheltuielile vor fi marcate pentru toți aprobatorii și        
  pentru raportare ulterioară.        

- Eroare - Solicită lucrătorului să revizuiască cheltuiala pentru a se conforma politicii înainte de a trimite raportul de cheltuieli sau cererea de călătorie.       
 
 - Justificare - Solicită lucrătorului sau unui manager să introducă o justificare pentru depășirea sumei poliței înainte de a trimite raportul de cheltuieli sau cererea de călătorie.        

## <a name="policy-tips"></a>Sfaturi de politică
Iată câteva sugestii care vă pot ajuta atunci când creați noi politici pentru gestionarea cheltuielilor. 
* Politicile sunt cu dată efectivă și nu vor intra în vigoare dacă politica este creată cu o dată după data la care s-a produs cheltuiala. De exemplu, dacă creați o politică nouă astăzi pentru a impune o cheltuială maximă de masă de $50, atunci orice cheltuieli existente introduse începând de ieri nu vor fi comparate cu această politică.
* Când creați o politică pentru o categorie de cheltuieli care poate fi detaliată, luați în considerare adăugarea unei condiții pentru tipul de linie de cheltuieli. Unele politici, cum ar fi solicitarea unei chitanțe, pot să nu aibă sens pentru liniile detaliate și ar trebui să fie aplicate numai liniei antetului sau unei linii nedefinite. 
* Politicile de gestionare a cheltuielilor sunt evaluate în mod implicit în raport cu entitatea sursă. Pentru scenariile între companii, puteți seta politica care urmează să fie evaluată în raport cu entitatea de destinație (entitatea care împrumută). Pentru a rula politicile împotriva entității de destinație, activați caracteristica „Evaluați politica de cheltuieli împotriva împrumutului entității juridice” în spațiul de lucru **Gestionarea caracteristicilor**.

## <a name="when-to-evaluate-policies"></a>Când se evaluează politicile

În parametrii de gestionare a cheltuielilor, există opțiunea ca fie să evaluați politicile de gestionare a cheltuielilor atunci când este salvată o linie, sau când este trimis un raport de cheltuieli. Dacă alegeți să evaluați când este salvată o linie, aceasta asigură că utilizatorii vor avea o vizibilitate mai timpurie a ceea ce trebuie să facă pentru a completa raportul de cheltuieli dintr-o dată. În caz contrar, puteți întârzia evaluarea politicii și puteți economisi timp dacă aveți validare la final, în timpul trimiterii la fluxul de lucru.


[!INCLUDE[footer-include](../includes/footer-banner.md)]