---
title: Comenzi de achiziție pentru un proiect
description: Acest articol descrie diferitele metode pe care le puteți utiliza pentru a crea comenzi de achiziție pentru un proiect. Metoda pe care o utilizați depinde de scopul comenzii de cumpărare, și de când sunt consumate și taxate într-un proiect articolele achiziționate.
author: Yowelle
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5de28f3844b802a980c811411cae75549c697538f89e8c3d2495ea171a188524
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/06/2021
ms.locfileid: "7009006"
---
# <a name="purchase-orders-for-a-project"></a>Comenzi de achiziție pentru un proiect

[!include [banner](../includes/banner.md)]

Acest articol descrie diferitele metode pe care le puteți utiliza pentru a crea comenzi de achiziție pentru un proiect. Metoda pe care o utilizați depinde de scopul comenzii de cumpărare, și de când sunt consumate și taxate într-un proiect articolele achiziționate.

### <a name="methods-for-creating-a-purchase-order"></a>Metode de creare a unei comenzi de achiziție

Puteți utiliza una dintre următoarele metode pentru a crea o comandă de achiziție în managementul de proiect și contabilitate. Scopul comenzii de achiziție determină când este consumată comanda de achiziție și, prin urmare, când sunt taxate articolele către un proiect.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Metodă</th>
<th>Scop</th>
<th>Consumul de articole</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Creați o comandă de achiziție direct dintr-un proiect.</td>
<td>Utilizați această metodă pentru a achiziționa articole de la un furnizor extern pentru consum în cadrul unui proiect. Puteți crea comanda de cumpărare în două moduri:
<ul>
<li>Din proiectul în sine. În acest caz, proiectul este deja definit pentru comanda de cumpărare.</li>
<li>Navigând la comanda de achiziție a proiectului. Trebuie să selectați atât furnizorul, cât și proiectul pentru a crea comanda de achiziție.</li>
</ul></td>
<td>Articolele sunt consumate atunci când factura furnizorului este actualizată.</td>
</tr>
<tr class="even">
<td>Creați o comandă de cumpărare dintr-o comandă de vânzare.</td>
<td>Utilizați această metodă pentru a achiziționa articole atunci când creați o comandă de vânzare dintr-un proiect.</td>
<td>Articolele sunt consumate atunci când comanda de vânzare este facturată către client.</td>
</tr>
<tr class="odd">
<td>Creați o comandă de cumpărare dintr-o cerință de articol.</td>
<td>Utilizați această metodă pentru a achiziționa articole atunci când creați o cerință de articol dintr-un proiect.</td>
<td>Articolele sunt consumate la actualizarea bonului de ambalare pentru cerința articolului.</td>
</tr>
</tbody>
</table>

> [!NOTE] 
> Când actualizați factura furnizorului sau bonul de ambalare, vi se solicită să actualizați bonul de ambalare pentru cerința articolului.

Pentru mai multe informații, consultați [Primiți articole din comanda de achiziție din cerința articolului](tasks/receive-items-purchase-order-item-requirement.md).



[!INCLUDE[footer-include](../includes/footer-banner.md)]