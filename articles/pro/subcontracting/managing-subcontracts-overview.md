---
title: Gestionarea subcontractelor în Project Operations
description: Acest subiect oferă o prezentare generală a procesului integral de gestionare a subcontractelor în Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6ffceb0886fdc841ea01a099243cf4eeb43e5374a18414576f3639a3e50857fd
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994246"
---
# <a name="subcontract-management-in-project-operations"></a>Gestionarea subcontractelor în Project Operations

[!include [banner](../../includes/dataverse-preview.md)]

_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_

Subcontractarea în Microsoft Dynamics 365 Project Operations acceptă următorul flux de business.

![Fluxul procesului de subcontractare](../media/SubcontractingProcessFlow.png)

Iată o descriere pas cu pas a procesului de subcontractare.

1. Managerul de proiect creează un subcontract cu un furnizor. În mod implicit, listele de prețuri atașate la înregistrarea furnizorului sunt utilizate pentru subcontract. Contul de furnizor are un tip de relație **Vânzător** sau **Furnizor**.
2. Managerul de proiect poate detalia toate achizițiile ca elemente de linie pe subcontract. Liniile de subcontract pot fi pentru timp, cheltuieli sau produse. Clasa de tranzacție care este selectată pe fiecare linie de subcontract determină pentru ce este linia.
3. Managerul de cont al furnizorului și managerul de proiect pot itera subcontractul. Prețurile pot fi ajustate în listele de prețuri de achiziție atașate subcontractului.
4. În acest moment sau mai târziu în proces, dacă linia de subcontract este pentru timp, managerul contului de furnizor asociază persoanele de contact cu fiecare linie de subcontract. Această asociere oferă informații managerului de proiect care lucrează la subcontract. Când o persoană de contact este asociată cu o linie de subcontract, sistemul creează automat o resursă ce se poate rezerva din contact, dacă o resursă ce se poate rezerva nu există deja.
5. Metoda de facturare pe fiecare linie de subcontract poate fi **Preț fix** sau **Timp și material**. Pentru liniile de subcontract cu preț fix, puteți configura un program de facturare bazat pe jaloane.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
