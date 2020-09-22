---
title: Configurați costurile standard pentru forța de muncă și cheltuieli
description: Acest subiect explică modul de stabilire a costurilor standard pentru forța de muncă și pentru cheltuielile unui proiect.
author: KimANelson
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.assetid: fa7c024f-4b18-4d29-9fd4-9c430cd83fad
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f3e796cc03aeaa28938c56ce37d5075755248dfa
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754837"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a>Configurați costurile standard pentru forța de muncă și cheltuieli

[!include [task guide banner](../../includes/task-guide-banner.md)]

Acest subiect explică modul de stabilire a costurilor standard pentru forța de muncă și pentru cheltuielile unui proiect. Această sarcină utilizează setul de date USSI.

1. În panoul de navigare, accesați **Module > Management de proiect și contabilitate > Configurare > Prețuri > Preț de cost (oră)**.
2. Selectați **Nou**.
3. În câmpul **Data efectivă**, introduceți o dată.
4. În câmpul **Preț de cost**, introduceți un număr. Puteți seta un preț de cost standard pentru categoria de proiect sau puteți seta un preț de cost în funcție de numărul lucrătorului, numărul proiectului, categoria, data sau orice combinație a acestora. Prețul de cost aplicat este prețul de cost cu cel mai înalt nivel de detaliere.  
5. Selectați **Salvare**.
6. În panoul de navigare, accesați **Module > Management de proiect și contabilitate > Configurare > Prețuri > Prețul de vânzări (oră)**.
7. Selectați **Nou**.
8. În câmpul **Data efectivă**, introduceți o dată.
9. În câmpul **Valid pentru**, selectați o opțiune.
10. În câmpul **Preț**, introduceți un număr. Puteți configura un preț de vânzare standard pentru tranzacțiile per oră sau pentru o categorie de proiect. De asemenea, puteți seta prețurile de vânzare după numărul lucrătorului, numărul proiectului, categoria, data tranzacției sau orice combinație a acestora. Prețul real de vânzare, care se aplică atunci când un lucrător introduce o tranzacție în jurnalul pe oră, este prețul de vânzare cu cel mai înalt nivel de detaliere. De exemplu, dacă sunt stabilite atât un preț general de vânzare, cât și un preț de vânzare specific lucrătorului, se folosește prețul de vânzare specific lucrătorului.  
11. Selectați **Salvare**.
12. Închideți pagina.
13. În panoul de navigare, accesați **Module > Management de proiect și contabilitate > Configurare > Prețuri > Preț de cost (cheltuieli)**.
14. Selectați **Nou**.
15. În câmpul **Data efectivă**, introduceți o dată.
16. În câmpul **Preț de cost**, introduceți un număr. Pot fi completate mai multe câmpuri, dar acesta este minimul necesar pentru salvarea înregistrării.  
17. Selectați **Salvare**.
18. În panoul de navigare, accesați **Module > Management de proiect și contabilitate > Configurare > Prețuri > Prețul de vânzări (cheltuieli)**.
19. Selectați **Nou**.
20. În câmpul **Data efectivă**, introduceți o dată.
21. În câmpul **Valid pentru**, selectați o opțiune.
22. În câmpul **Preț**, introduceți un număr. Prețul real de vânzare, care se aplică atunci când un lucrător introduce tranzacții în jurnalul de cheltuieli, este prețul de vânzare cu cel mai înalt nivel de detaliere. De exemplu, dacă sunt stabilite atât un preț general de vânzare, cât și un preț de vânzare specific lucrătorului, se folosește prețul de vânzare specific lucrătorului.  
23. Selectați **Salvare**.

