---
title: Cereri de călătorie
description: Acest subiect oferă informații despre cereri de călătorie.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 0261405abb9305d7f6abcde9cb90d9b184868580
ms.sourcegitcommit: a0f80d024a5d3112a39781815bd31d0c05ddaf6f
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 09/30/2020
ms.locfileid: "3906296"
---
# <a name="travel-requisitions"></a>Cereri de călătorie

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

O cerere de călătorie enumeră cheltuielile care vor fi suportate în scopul călătoriei. O cerere de călătorie este trimisă spre examinare și poate fi utilizată pentru autorizarea cheltuielilor.

Este posibil să vi se solicite să depuneți o cerere de călătorie înainte de a suporta orice cheltuială care este percepută organizației. Această cerință se aplică, indiferent dacă încărcați cheltuieli pe un card de credit corporativ, cheltuiți numerar pe care l-ați primit dintr-un avans de numerar sau suportați cheltuieli din buzunar care vor fi rambursate de organizație.

Cererile de călătorie și politicile pot fi utilizate pentru a ajuta la gestionarea cheltuielilor organizației. De exemplu, dacă organizația dvs. lucrează la un proiect cu preț fix care necesită călătorie, cheltuielile de călătorie ale membrilor echipei proiectului trebuie să se încadreze în bugetul proiectului. Solicitând aprobarea cheltuielilor de călătorie înainte de a fi suportate, organizația se poate asigura că proiectul rămâne în limita bugetului.

## <a name="configuration"></a>Configurație 

Cerințele de călătorie pot fi configurate ca „obligatorii” prin activarea parametrului „Pre-autorizarea călătoriei este obligatorie” în parametrii de gestionare a cheltuielilor. 

## <a name="create-and-submit-a-travel-requisition"></a>Creați și trimiteți o cerere de călătorie

1. Accesați **Cheltuielile mele: Cerere de călătorie**, și selectați **Cerere nouă de călătorie**.
2. Introduceți un scop și o destinație pentru solicitare.
3. În câmpul  **Descrierea călătoriei**, introduceți orice informații suplimentare. 
4. Pentru fiecare dintre cheltuielile așteptate, cum ar fi zborul, mesele sau închirierea de mașini, creați un element rând pentru cheltuieli. Includeți data estimată, suma estimată și moneda pentru fiecare cheltuială. 
5. După ce ați terminat de adăugat cheltuielile preconizate, selectați **Salvați**.
6. Când sunteți gata să trimiteți cererea de călătorie, selectați **Flux de lucru** > **Trimite**.

Puteți vedea cererile de călătorie aprobate în secțiunea **Cheltuielile mele: cererea de călătorie**. 

## <a name="view-available-travel-requisitions"></a>Vizualizați cererile de călătorie disponibile

Puteți vedea cererile dvs. de călătorie aprobate în secțiunea **Cheltuielile mele: cereri de călătorie**.

## <a name="approve-travel-requisitions"></a>Aprobați cereri de călătorie

Selectați cerința de călătorie pe care doriți să o aprobați, apoi selectați **Flux de lucru** > **Aprobare**.  

## <a name="submit-an-expense-report-using-your-approved-travel-requisition"></a>Trimiteți un raport de cheltuieli utilizând cererea de călătorie aprobată

1. Creați un nou raport de cheltuieli și în antetul raportului de cheltuieli și selectați din lista cererilor de călătorie aprobate **Mapați la Cerere de călătorie**.
2. Câmpul **Suma cererii de călătorie** este actualizat automat în antetul raportului de cheltuieli.
3. Adăugați fiecare cheltuială efectuată pentru călătorie. Dacă este activat câmpul **Pre-autorizat**, suma reconciliată și suma autorizată pentru categoria de cheltuieli specifice vor fi actualizate.

> [!NOTE]
> Când mapați un raport de cheltuieli la o cerere de călătorie aprobată, suma tranzacției nu poate fi mai mare decât suma autorizată. 
