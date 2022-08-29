---
title: Înregistrarea timpului, cheltuielilor și consumului materialelor pentru componentele subcontractate
description: Acest articol explică modul în care timpul, cheltuielile și utilizarea materialelor înregistrate pe proiecte din componentele subcontractate sunt urmărite de Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 89fbbfcd1535660e92d0cc80beb91029331e990f
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261155"
---
# <a name="recording-time-expenses-and-material-usage-on-projects-for-subcontracted-components"></a>Înregistrarea timpului, a cheltuielilor și a utilizării materialelor pe proiecte pentru componentele subcontractate

_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_

Acest articol explică modul în care timpul, cheltuielile și utilizarea materialelor înregistrate pe proiecte din componentele subcontractate sunt urmărite de Microsoft Dynamics 365 Project Operations.

## <a name="costing-for-subcontractor-time-on-projects"></a>Costuri pentru timpul subcontractantului pe proiecte
În operațiunile de proiect, lucrătorii contractuali pot înregistra timp pentru proiecte într-un mod similar cu angajații. Când introduceți timp pentru proiecte și/sau sarcini de proiect, un lucrător contractual poate selecta o anumită linie de subcontractare și de subcontractare.

Când timpul transmis de lucrătorii contractuali este aprobat, costul proiectului este înregistrat utilizând rata costului unitar care este stabilit pentru resursa respectivă de lucrător contractual în **Prețurile de rol** secțiunea din lista de prețuri de achiziție din subcontract.

## <a name="costing-for-subcontracted-expenses-on-projects"></a>Costuri pentru cheltuielile subcontractate pe proiecte
Când introduceți cheltuielile efectuate pentru proiecte, puteți selecta o linie de subcontractare și subcontractare în înregistrarea de cheltuieli. 

Când această înregistrare a cheltuielilor este depusă și aprobată, costul cheltuielilor este înregistrat în proiect pe baza costului unitar care este stabilit pentru acea categorie de tranzacție în **Preturi de categorie** secțiunea din lista de prețuri de achiziție din subcontract.

## <a name="costing-for-subcontracted-materials-on-projects"></a>Costuri pentru materialele subcontractate pe proiecte
Când introduceți utilizarea materialului pe proiecte, puteți selecta o linie de subcontractare și subcontractare în jurnalul de utilizare a materialului. Când registrul de utilizare a materialului este depus și aprobat, costul materialului este înregistrat în proiect pe baza costului unitar care este stabilit pentru acel produs în **Articole din lista de preturi** secțiunea listei de prețuri de subcontractare.

Utilizarea materialului poate fi înregistrată și pentru produsele de înscriere pe proiecte. Acest tip de utilizare a materialului poate fi, de asemenea, legat de o linie de subcontractare și de subcontractare. Când înregistrați utilizarea materialului pentru produsele de scriere, trebuie să introduceți costul pe unitate al produsului de scriere. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
