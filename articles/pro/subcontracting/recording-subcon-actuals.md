---
title: Înregistrarea timpului, cheltuielilor și consumului materialelor pentru componentele subcontractate
description: Acest articol explică modul în care timpul, cheltuielile și utilizarea materialelor înregistrate pe proiecte din componentele subcontractate sunt urmărite de Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b82c14412cfb0405040902a2329c3b6692422d89
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522529"
---
# <a name="recording-time-expenses-and-material-usage-on-projects-for-subcontracted-components"></a>Înregistrarea timpului, a cheltuielilor și a utilizării materialelor pe proiecte pentru componentele subcontractate

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Acest articol explică modul în care timpul, cheltuielile și utilizarea materialelor înregistrate pe proiecte din componentele subcontractate sunt urmărite de Microsoft Dynamics 365 Project Operations.

## <a name="costing-for-subcontractor-time-on-projects"></a>Costuri pentru timpul subcontractantului pe proiecte
În Project Operations, lucrătorii contractuali pot înregistra timp pe proiecte într-un mod similar cu angajații. La introducerea timpului pe proiecte și/sau sarcini de proiecte, un lucrător contractual poate selecta un anumit subcontract și o anumită linie de subcontract.

Când timpul transmis de lucrătorii contractuali este aprobat, costul proiectului este înregistrat utilizând rata costului unitar care este stabilită pentru resursa respectivă de lucrător contractual în secțiunea **Prețuri de rol** din lista de prețuri de achiziție din subcontract.

## <a name="costing-for-subcontracted-expenses-on-projects"></a>Calcularea prețurilor pentru cheltuieli subcontractate pe proiecte
Când introduceți cheltuielile efectuate pentru proiecte, puteți selecta un subcontract și o linie de subcontractare în înregistrarea de cheltuieli. 

Când această intrare de cheltuieli este transmisă și aprobată, costul pentru cheltuieli este înregistrat în proiect pe baza costului unitar care este stabilit pentru categoria de tranzacție în secțiunea **Prețuri categorii** din lista de prețuri de achiziție din subcontract.

## <a name="costing-for-subcontracted-materials-on-projects"></a>Calcularea prețurilor pentru materiale subcontractate pe proiecte
Când introduceți utilizarea materialelor pe proiecte, puteți selecta un subcontract și o linie de subcontractare în înregistrarea de utilizare a materialelor. Când înregistrarea de utilizare a materialelor este transmisă și aprobată, costul pentru materiale este înregistrat în proiect pe baza costului unitar care este stabilit pentru acel produs în secțiunea **Articole din lista de prețuri** a listei de prețuri din subcontract.

Utilizarea materialelor poate fi înregistrată și pentru produsele din afara catalogului pe proiecte. Acest tip de utilizare a materialelor poate fi, de asemenea, legat de un subcontract și o linie de subcontractare. Când înregistrați utilizarea materialelor pentru produsele din afara catalogului, trebuie să introduceți costul unitar al produsului din afara catalogului. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
