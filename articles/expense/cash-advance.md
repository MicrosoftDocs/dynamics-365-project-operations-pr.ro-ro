---
title: Avans în numerar
description: Acest subiect oferă informații despre avansuri de numerar.
author: suvaidya
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 209fe0b8a79b2c0689c458c423664cb292da249b
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908488"
---
# <a name="cash-advance"></a>Avans în numerar

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

Un avans în numerar permite angajaților să împrumute bani de la compania lor înainte de a suporta cheltuieli. Atunci când un avans de numerar solicitat este aprobat și plătit, angajatul poate folosi banii pentru cheltuielile de afaceri pe care ar putea să le suporte. 

## <a name="create-and-submit-a-cash-advance-request"></a>Creați și trimiteți o cerere de avans în numerar

1. Sub **Cheltuielile mele**, selectați **Avansuri de numerar** > **Nou** pentru a crea un nou avans de numerar. 
2. Pe pagina **Nouă solicitare de avans în numerar**, introduceți scopul cheltuielilor și selectați locația în care va fi efectuată cheltuiala.
3. Introduceți suma și moneda solicitate, apoi selectați **Salvare**. 
4. Când sunteți gata să depuneți cererea de avans în numerar, pe pagina **Cerere de avans în numerar**, selectați **Flux de lucru** > **Trimite**.

## <a name="modify-a-cash-advance-request"></a>Modificați o solicitare de avans în numerar

Puteți modifica o solicitare de avans în numerar dacă nu a fost trimisă spre aprobare.

1. Sub **Cheltuielile mele: avansuri în numerar** localizați și selectați avansul de numerar pe care doriți să îl modificați.
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

Când creați și trimiteți un raport de cheltuieli pentru avansul în numerar pe care l-ați primit deja, cheltuielile vor fi ajustate automat în funcție de acel avans. Dacă avansul dvs. de numerar este mai mare decât suma cheltuită, trebuie să returnați soldul companiei utilizând categoria de cheltuieli **Returnează numerar**. Dacă avansul în numerar plătit de companie este mai mic decât suma pe care ați cheltuit-o, compania trebuie să vă ramburseze soldul. 

### <a name="example"></a>Exemplu
Aveți de gând să călătoriți pentru o conferință de la Seattle la New York. Creați o solicitare de avans în numerar pentru 3000,00 USD, deoarece ați estimat că costul biletului de conferință, zborurilor, hotelului, meselor și taxiului va fi aproximativ această sumă. Nu veți fi plătit decât dacă managerul dvs. a aprobat această solicitare. După ce managerul dvs. aprobă, avansul de numerar solicitat este plătit ca 3000,00 USD în contul dvs. bancar. Apoi participați la conferință. După finalizarea călătoriei dvs., constatați că cheltuielile totale au fost doar de 2790,00 USD. Selectați **Numerar** în câmpul **Modalitate de plată** și vă trimite cheltuiala pentru 2790,00 USD. Valoarea cheltuielilor trimise este ajustată automat în funcție de avansul în numerar al 3000,00 USD care v-a fost împrumutat. Acum datorați companiei un sold de 210,00 USD (3000,00-2790,00), pe care îl puteți restitui companiei folosind categoria de cheltuieli **Returnează numerar**. 
