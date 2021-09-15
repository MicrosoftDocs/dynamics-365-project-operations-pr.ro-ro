---
title: Subcontractarea în versiunea lansată pentru acces timpuriu în luna octombrie 2021
description: Acest subiect oferă o prezentare generală a capabilităților de subcontractare din Project Operations, care fac parte din versiunea de acces timpuriu din octombrie 2021.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 21ec8355487b5e69fc5b68b11dca029e6dc04f3c
ms.sourcegitcommit: c7f891adb5c81654c01d00c6b39beed403058eb1
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/14/2021
ms.locfileid: "7383710"
---
# <a name="subcontracting-in-october-2021-early-access-release"></a>Subcontractarea în versiunea lansată pentru acces timpuriu în luna octombrie 2021

[!include [banner](../../includes/dataverse-preview.md)]

_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_

Acest subiect oferă o prezentare generală a capabilităților de subcontractare din Dynamics 365 Project Operations, care fac parte din versiunea de acces timpuriu din octombrie 2021. Acest set de caracteristici nu este pregătit pentru producție sau medii live, prin urmare aceste caracteristici vor rămâne în versiunea de acces timpuriu până la lansarea întregului set de caracteristici. Vă recomandăm insistent să nu utilizați setul de caracteristici de subcontractare pentru scenarii de producție live până nu este eliminat bannerul de previzualizare. 

Următoarea listă oferă o schiță a ceea ce este disponibil în prezent în versiunea de acces timpuriu din octombrie 2021:

1. Managerul de proiect creează un subcontract cu un furnizor. În mod implicit, listele de prețuri atașate la înregistrarea furnizorului sunt utilizate pentru subcontract. Contul de furnizor are un tip de relație **Vânzător** sau **Furnizor**.

2. Managerul de proiect poate detalia toate achizițiile ca elemente de linie pe subcontract. Liniile de subcontract pot fi pentru timp, cheltuieli sau produse. Clasa de tranzacție care a liniei de subcontract stabilește pentru ce este linia.

3. Managerul de cont al furnizorului și managerul de proiect pot itera subcontractul. Prețurile pot fi ajustate în listele de prețuri de achiziție atașate subcontractului.

4. În acest moment sau mai târziu în proces, dacă linia de subcontract este pentru timp, managerul contului de furnizor asociază persoanele de contact ale furnizorului cu fiecare linie de subcontract. Această asociere oferă informații managerului de proiect care lucrează la subcontract. Când o persoană de contact a furnizorului este asociată cu o linie de subcontract, sistemul creează automat o resursă ce se poate rezerva din contact, dacă o resursă ce se poate rezerva nu există deja.

5. Metoda de facturare pe fiecare linie de subcontract poate fi **Preț fix** sau **Timp și material**. Pentru liniile de subcontract cu preț fix, se configurează o planificare de facturare bazată pe jaloane.

Pașii rămași din fluxul de business pentru subcontractare, descriși în Prezentarea generală, nu sunt momentan disponibili. Pe măsură ce se adaugă noi funcționalități, acest subiect va fi actualizat. 

Următoarea ilustrație reprezintă versiunea Acces timpuriu subcontractare, în contrast cu procesul complet de business.

![Fluxul procesului de subcontractare](../media/SubcontractingEAFlow.png)  


## <a name="quantity-based-and-work-based-subcontract-lines-early-access-release"></a>Linii de subcontract bazate pe cantitate și linii de subcontract bazate pe muncă în versiunea cu acces timpuriu
În versiunea de acces timpuriu din octombrie 2021, sunt acceptate numai linii de subcontract bazate pe cantități. Acest lucru înseamnă că o linie de subcontract poate fi utilizată pentru a cumpăra timp, cheltuieli sau materiale de la un furnizor, dar nu un întreg corp de activități. Mai înseamnă și că întreaga cantitate achiziționată (unități de timp, cheltuieli sau cantitatea de materiale) de pe o linie de subcontract poate fi utilizată pentru orice proiect din sistem.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
