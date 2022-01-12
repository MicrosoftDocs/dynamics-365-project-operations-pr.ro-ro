---
title: Timpul de înregistrare, cheltuielile și utilizarea materialelor pentru componentele subcontractate
description: Acest subiect explică modul în care timpul, cheltuielile și utilizarea materialelor înregistrate pe proiecte din componentele subcontractate este urmărită de Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: 04c78dd48367c3720b8f5ad5d924ed106da6a128
ms.sourcegitcommit: 04dc8d952e6da3ab3eb2a20131c6f7cee6040876
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 12/10/2021
ms.locfileid: "7903744"
---
# <a name="recording-time-expenses-and-material-usage-on-projects-for-subcontracted-components"></a>Înregistrarea timpului, a cheltuielilor și a utilizării materialelor pe proiecte pentru componentele subcontractate

[!include [banner](../../includes/dataverse-preview.md)]

_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_

Acest subiect explică modul în care timpul, cheltuielile și utilizarea materialelor înregistrate pe proiecte din componentele subcontractate este urmărită de Microsoft Dynamics 365 Project Operations.

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
