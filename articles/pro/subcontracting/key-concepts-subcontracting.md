---
title: Concepte cheie în subcontractare
description: Acest articol explică câteva concepte cheie care se aplică subcontractării în Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 08/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 0ac84d132a2d62528d97ed3776a78062a589a380
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927711"
---
# <a name="key-concepts-in-subcontracting"></a>Concepte cheie în subcontractare

[!include [banner](../../includes/dataverse-preview.md)]

_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_

Articolul explică câteva concepte cheie de care ar trebui să le cunoașteți înainte de a începe să utilizați funcționalitatea de subcontractare din Microsoft Dynamics 365 Project Operations.

## <a name="contracting-unit-on-the-subcontract"></a>Unitatea contractantă în subcontract

Unitatea contractantă reprezintă divizia sau practica ce deține livrarea proiectului eventual. Unitatea contractantă este, de asemenea, divizia care intră în relația contractuală cu furnizorul.

## <a name="purchase-currency"></a>Moneda de cumpărare

În Project Operations, moneda de cumpărare este moneda în care este creat subcontractul. Este, de asemenea, moneda în care sunt înregistrate costurile subcontractorului pentru un proiect. Moneda de cumpărare poate diferi de moneda proiectului, iar moneda proiectului poate, la rândul său, să difere de moneda de vânzare.

## <a name="billing-methods-on-subcontract-lines"></a>Metode de facturare pe liniile de subcontractare

Pentru proiecte, de obicei există modele de contractare cu taxă fixă și bazate pe consum. Project Operations acceptă aceste metode de facturare în contextele de vânzare și cumpărare. Pentru o achiziție, metodele de facturare funcționează în felul următor:

- **Timp și material** - Când o linie de subcontractare folosește metoda de facturare **Timp și material**, costul timpului este înregistrat la proiect pe măsură ce subcontractorii lucrează la acel proiect și înregistrează timpul. Aceste tranzacții de cost de la subcontractori sunt apoi corelate cu elementele de linie de pe facturile furnizorului. În acest model, managerii de proiect care utilizează Project Operations pot potrivi și verifica liniile de facturare ale furnizorului cu timpul subcontractantului care este înregistrat și aprobat. După finalizarea verificării, costurile anterioare care au fost înregistrate după aprobare sunt inversate și costurile noi care se bazează pe factura de la furnizor sunt create în proiect.
- **Preț fix** - În acest model de contractare cu taxă fixă, facturile furnizor se bazează pe repere fixe. Cu toate acestea, resursele subcontractorilor pot raporta și timpul. Timpul este apoi revizuit și aprobat de managerul de proiect. Când este aprobat, Project Operations creează valori reale de costuri temporare pentru proiect. După ce furnizorul trimite o factură pentru o etapă de referință, managerul de proiect poate compara costurile înregistrate anterior cu datele de referință. Când verificarea se finalizează, costurile reale sunt inversate și este înregistrat costul bazat pe jaloane.

## <a name="project-price-lists-on-subcontracts"></a>Liste de prețuri proiect în subcontracte

Listele de prețuri de proiecte sunt liste de prețuri utilizate pentru a configura prețurile de achiziție pentru timp, cheltuieli și alte componente legate de proiect. Pot exista mai multe liste de prețuri, fiecare dintre acestea putând avea subcontractul său propriu cu o dată efectivă în Project Operations. Project Operations nu acceptă suprapunerea datelor efective pe listele de prețuri de proiect pentru un subcontract.

## <a name="transaction-classes-on-subcontracts"></a>Clase de tranzacții pentru subcontracte

Project Operations acceptă patru tipuri de clase de tranzacții:

- Timp
- Cheltuială
- Material
- Taxă

Costurile de achiziție pot fi estimate și suportate numai pentru clasele de tranzacții **Timp**, **Cheltuieli** și **Material**. **Taxă** este o clasă de tranzacții doar pentru venituri și nu este disponibilă în conținutul achiziției.

## <a name="purchase-pricing-dimensions"></a>Dimensiunile de preț de achiziție

Dimensiunile prețurilor permit să decideți care atribute se utilizează pentru a configura prețul de achiziție și pentru valorile implicite ale tranzacțiilor de timp. În ceea ce privește achizițiile, Project Operations acceptă doar seturi fixe de dimensiuni pentru a configura prețul de achiziție și valorile implicite. Pentru configurarea prețului de cumpărare și valorilor implicit pentru liniile de subcontractare și tranzacțiile de timp de subcontractare, atributele sunt **Rol** și **Resurse ce se pot rezerva**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
