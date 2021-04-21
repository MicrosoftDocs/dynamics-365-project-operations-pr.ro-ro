---
title: Avans în numerar
description: Acest subiect oferă informații despre avansuri de numerar.
author: suvaidya
manager: AnnBe
ms.date: 03/25/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 5ac8956720deac9e9c9191cefb870a7fbbeedcca
ms.sourcegitcommit: 9ebf7dd501898053bfa824f732adabf3f273613b
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 03/26/2021
ms.locfileid: "5715575"
---
# <a name="cash-advance"></a>Avans în numerar

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

Un avans în numerar permite angajaților să împrumute bani de la compania lor înainte de a suporta cheltuieli. Atunci când un avans de numerar solicitat este aprobat și plătit, angajatul poate folosi banii pentru cheltuielile de afaceri pe care ar putea să le suporte. 

## <a name="create-and-submit-a-cash-advance-request"></a>Creați și trimiteți o cerere de avans în numerar
Pentru a crea un nou avans de numerar și a trimite o solicitare de avans în numerar, procedați în felul următor: 

1. La secțiunea **Cheltuielile mele**, selectați **Avansuri de numerar** > **Nou**. 
2. Pe pagina **Nouă solicitare de avans în numerar**, introduceți scopul cheltuielilor și selectați locația în care va fi efectuată cheltuiala.
3. Introduceți suma și moneda solicitate, apoi selectați **Salvare**. 
4. Când sunteți gata să depuneți cererea de avans în numerar, pe pagina **Cerere de avans în numerar**, selectați **Flux de lucru** > **Trimite**.

## <a name="modify-a-cash-advance-request"></a>Modificați o solicitare de avans în numerar

Puteți modifica o solicitare de avans în numerar dacă nu a fost trimisă spre aprobare.

1. La secțiunea **Cheltuielile mele: avansuri de numerar** localizați și selectați avansul de numerar pe care doriți să îl editați.
2. Selectați **Editați** și faceți modificările necesare la solicitarea de avans în numerar. 
3. Selectați **Salvați și închideți**.


## <a name="view-cash-advance-requests"></a>Vizualizați solicitările de avans de numerar
Puteți consulta lista tuturor avansurilor în numerar care sunt în proiect, trimise, în revizuire sau plătite sub **Cheltuielile mele: avansuri în numerar**. 

## <a name="approve-cash-advance-requests"></a>Aprobați solicitările de avans de numerar

Managerii sau utilizatorii configurați ca aprobatori în fluxul de lucru vor putea aproba avansurile de numerar care le-au fost supuse spre examinare. 

1. Pentru a aproba un avans de numerar, în conformitate cu **Procesează avansuri de numerar**, selectați **Avansuri de numerar pentru recenzia mea**.
2. Selectați avansul de numerar pe care trebuie să îl examinați și selectați **Aprobare**.  

## <a name="pay-cash-advances"></a>Plătiți avansuri în numerar 
Următoarea procedură este de obicei finalizată de un contabil sau un utilizator cu permisiuni de contabilitate.

1. Pentru a înregistra avansuri de numerar aprobate, selectați **Avansuri de numerar aprobate**, apoi selectați **Plătiți și transferați**.  
2. Furnizați detaliile jurnalului pentru avansurile de numerar, apoi selectați **OK**. 

## <a name="submit-an-expense-report-against-a-paid-cash-advance"></a>Trimiteți un raport de cheltuieli cu un avans de numerar plătit 

Când creați și trimiteți un raport de cheltuieli pentru avansul de numerar pe care l-ați primit deja, cheltuielile vor fi ajustate automat în funcție de acel avans. Dacă avansul dvs. de numerar este mai mare decât suma cheltuită, trebuie să returnați soldul companiei utilizând categoria de cheltuieli **Returnează numerar**. Dacă avansul de numerar plătit de companie este mai mic decât suma pe care ați cheltuit-o, compania trebuie să vă ramburseze soldul. 

### <a name="select-cash-advances-that-apply-to-your-expenses"></a>Selectați avansuri în numerar care se aplică cheltuielilor dvs
Înainte de a trimite un raport de cheltuieli, puteți selecta avansul de numerar care se aliniază cu tranzacțiile de cheltuieli din raport. Pentru a utiliza această funcționalitate, următoarele două caracteristici trebuie activate din spațiul de lucru **Managementul caracteristicilor**:

  - Rapoarte de cheltuieli reimaginate
  - Capacitatea de a mapa avansurile de numerar la liniile de cheltuieli
 
 Când aceste caracteristici sunt activate:
 
  - Puteți adăuga unul sau mai multe avansuri de numerar pentru fiecare linie de cheltuieli.
  - Soldul disponibil al unui avans de numerar este vizibil în timp real atunci când se salvează un raport de cheltuieli. Acest lucru vă permite să procesați tranzacții de cheltuieli și să returnați tranzacții în numerar în același timp.
  - Puteți selecta mai multe avansuri de numerar pentru o tranzacție de cheltuieli.
  - Datele de reconciliere a avansului de numerar sunt disponibile utilizând o interogare. 
 
Dacă nu utilizați aceste caracteristici, funcționalitatea va rămâne aceeași, cu avansurile de numerar existente reduse automat după depunerea unei cheltuieli.

### <a name="example"></a>Exemplu 
Aveți de gând să faceți o deplasare de la Seattle la New York pentru o conferință. Creați o solicitare de avans de numerar pentru suma de 3000,00 USD pe baza costului estimat al biletului, zborurilor, hotelului, meselor și taxiurilor pentru conferință. Nu vi se va plăti decât dacă managerul dvs. aprobă această solicitare. După ce managerul dvs. aprobă, avansul de numerar solicitat este plătit ca 3000,00 USD în contul dvs. bancar. Apoi participați la conferință. După finalizarea călătoriei dvs., constatați că cheltuielile totale au fost doar de 2790,00 USD. Selectați **Numerar** în câmpul **Modalitate de plată** și trimiteți cheltuielile pentru suma de 2790,00 USD. Valoarea cheltuielilor trimise este ajustată automat în funcție de avansul în numerar al 3000,00 USD care v-a fost împrumutat. În acest moment aveți o datorie de 210,00 USD (3000,00 - 2790,00), pe care îl puteți restitui companiei folosind categoria de cheltuieli **Returnați numerar**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
