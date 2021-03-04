---
title: Prezentare generală a facturării între companii
description: Acest subiect oferă informații și exemple despre facturarea între companii pentru proiecte.
author: sigitac
manager: tfehr
ms.date: 11/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 670b5d15ecf1ef7dcc034064e625814cbe6d54b0
ms.sourcegitcommit: addbe0647619413e85e7cde80f6a21db95ab623e
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 11/20/2020
ms.locfileid: "4595535"
---
# <a name="intercompany-invoicing-overview"></a>Prezentare generală a facturării între companii

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

Organizația dvs. ar putea avea mai multe divizii, filiale și alte entități juridice care își transferă produse și servicii reciproc pentru proiecte. Entitatea juridică care furnizează serviciul sau produsul se numește *entitate juridică de creditare*. Entitatea juridică care primește serviciul sau produsul se numește *entitate juridică de împrumut*.

Următoarea ilustrație prezintă un scenariu tipic în care două entități juridice, Contoso Robotics USA (entitatea juridică care împrumută) și Contoso Robotics UK (entitatea juridică care împrumută) împart resurse pentru a livra un proiect pentru client, Adventure works. Pentru acest scenariu, Contoso Robotics SUA este contractat pentru livrarea lucrărilor către Adventure Works.

![Facturare între companii](./media/IntercompanyScenario.png) 

Dynamics 365 Project Operations utilizează următorul flux pentru a procesa tranzacții între companii:

1. Resursele de la entitatea juridică care acordă împrumuturi înregistrează tranzacțiile între timp sau cheltuieli între companii prin rezervarea timpului și cheltuielilor pentru proiectele din entitatea juridică care împrumută.
2. Costurile de timp și cheltuieli sunt înregistrate în societatea de creditare utilizând lista de prețuri de cost unitare a companiei de împrumut.
3. Tranzacțiile de vânzare nefacturate între companii sunt înregistrate în societatea de creditare utilizând lista de prețuri de cost unitare a companiei de împrumut.
4. Veniturile necontabilizate se înregistrează în compania împrumutată utilizând lista de prețuri de vânzare a contractului de proiect. Clientul poate fi facturat atunci când se înregistrează venituri nefacturate. Clientul nu trebuie să aștepte până la finalizarea procesării facturilor între companii.
5. Facturile clienților între companii sunt create periodic în cadrul companiei de creditare. Facturile sunt create manual sau utilizând un proces automat automat. Se poate crea o singură factură pentru fiecare entitate juridică care împrumută sau se pot crea facturi separate prin proiect.
6. Atunci când factura clientului între companii este înregistrată în entitatea juridică de creditare, se creează factura de vânzător în așteptare corespunzătoare în entitatea juridică de împrumut. Costurile din factura furnizorului în așteptare vor fi înregistrate în caseta de proiect la înregistrarea facturii.

Următoarea diagramă ilustrează facturarea între companii, în ceea ce privește evenimentele contabile și înregistrările preconizate în registrul general.

![Flux între companii](./media/IntercompanyFlow.png)

## <a name="additional-resources"></a>Resurse suplimentare

- [Configurarea facturării între companii](configure-intercompany-invoicing.md)
- [Înregistrarea tranzacțiilor între companii](create-intercompany-transactions.md)
- [Crearea de facturi de client și furnizor între companii](create-intercompany-customer-vendor-invoices.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]