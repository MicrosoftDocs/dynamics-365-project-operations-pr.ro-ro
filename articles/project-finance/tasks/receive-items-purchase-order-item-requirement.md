---
title: Primiți articole din comanda de achiziție din cerința articolului
description: Acest subiect explică modul de primire a articolelor dintr-o comandă de achiziție dintr-o cerință de articol.
author: KimANelson
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.assetid: c61e3a5e-da3d-4f4c-87fa-03dea19f6936
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c5ed287aa24aff647ef1dc625f9e9f5f086ee662
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754681"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a>Primiți articole din comanda de achiziție din cerința articolului

[!include [task guide banner](../../includes/task-guide-banner.md)]

Acest subiect explică modul de primire a articolelor dintr-o comandă de achiziție dintr-o cerință de articol.

Utilizând o cerință de articol în loc de o tranzacție de articol, puteți planifica livrarea chiar înainte ca articolul să fie utilizat efectiv, să creați o comandă de achiziție, să includeți articolul în cadrul acordului comercial și să includeți cerința articolului în planificarea producției. 

Această sarcină utilizează setul de date USSI.

1. În panoul de navigare, accesați **Module > Management de proiect și contabilitate > Proiecte > Toate proiectele**.
2. În listă, selectați linkul din rândul doriți.
3. În panoul de acțiuni, selectați **Plan**.
4. Selectați **Cerințele articolului**.
5. Selectați **Nou**.
6. În noul rând, introduceți sau selectați o valoare în câmpul **Numărul de articol**.
7. În câmpul **Cantitate**, introduceți un număr.
8. Selectați **Salvare**.
9. În panoul de acțiuni, selectați **Gestionare**.
10. Selectați **Funcții**.
11. Selectați **Creați comanda de achiziție**.
12. Selectați caseta de selectare **Includeți tot**.
13. În câmpul **Cont distribuitor**, introduceți sau selectați o valoare.
14. Selectați **OK**.
15. În panoul de navigare, selectați **Module > Conturi furnizori > Comenzi de achiziție > Toate comenzile de achiziție**.
16. În listă, selectați linkul din rândul doriți.
17. În panoul de acțiuni, selectați **Achiziție**.
18. Selectați **Confirmare**.
19. În panoul de acțiuni, selectați **Primiți**.
20. Selectați **Chitanță de produs**.
21. În câmpul **Chitanță de produs**, tastați o valoare.
22. Selectați **OK**.

