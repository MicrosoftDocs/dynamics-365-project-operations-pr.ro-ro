---
title: Dezactivarea listelor de prețuri
description: Acest subiect explică cum să dezactivați sau să eliminați listele de prețuri neutilizate sau vechi.
author: rumant
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Professional Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: aca58eed2a0ee5e108d40636529802a7feec5b8dd060ba6c0eabc6d0b92b2e2f
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/06/2021
ms.locfileid: "6997666"
---
# <a name="deactivate-price-lists"></a>Dezactivarea listelor de prețuri 

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Pentru a elimina listele de prețuri vechi sau neutilizate din Dynamics 365 Project Operations, trebuie să parcurgeți doi pași. 

1. Eliminați sau ștergeți lista de prețuri din anumite pagini.
2. Dezactivați sau ștergeți lista de prețuri din listele de prețuri active de pe pagina **Liste de prețuri**.

>[!IMPORTANT]
> Trebuie să parcurgeți ambii pași pentru a elimina complet o listă de prețuri. Numai efectuarea pasului 2, care este ștergerea sau dezactivarea directă a listei de prețuri din vizualizarea Listelor de preț active, nu este suficientă. De asemenea, trebuie să ștergeți asocierea acestei liste de prețuri din toate locurile menționate la pasul 1.

## <a name="delete-the-price-list-from-specific-pages"></a>Ștergeți lista de prețuri din anumite pagini
1. Pentru a șterge o listă de prețuri din Project Operations, accesați următoarele pagini:  

      - Pagina **Parametri liste de prețuri** > fila **Liste de prețuri**
      - Pagina **Unitate organizațională** > grila **Liste de prețuri**
      - Pagina **Cont** > grila **Liste de prețuri ale proiectului**
      - Pagina **Oferte proiect** > grila **Liste de prețuri ale proiectului**: Acest lucru se aplică tuturor ofertelor de proiect active.
      - Pagina **Contracte proiect** > grila **Liste de prețuri ale proiectului**: Acest lucru se aplică tuturor contractelor de proiect active.

 2. Pentru fiecare pagină, trebuie să selectați lista de prețuri pe care doriți să o ștergeți, apoi să selectați **Ștergere**. 
 
## <a name="delete-or-deactivate-the-price-list-from-the-price-lists-page"></a>Ștergeți sau dezactivați lista de prețuri din pagina Liste de prețuri
 
1. Pentru a șterge o listă de prețuri din listele de prețuri active, accesați **Vânzări** > **Clienți** > **Liste de prețuri**. 
2. Selectați lista de prețuri pe care doriți să o ștergeți și apoi selectați **Ștergere**. Dacă lista de prețuri face trimitere la orice tranzacții existente, nu o veți putea șterge. Dacă se întâmplă acest lucru, puteți dezactiva lista de prețuri, astfel încât să nu apară în nicio vizualizare. 
3. Pentru a dezactiva lista de prețuri, selectați din nou lista de prețuri, apoi selectați **Dezactivare**.   
