---
title: Crearea de entități și câmpuri particularizate ca dimensiuni de preț
description: Acest subiect oferă informații despre cum să creați seturi de opțiuni personalizate sau entități.
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 4912087d7a19f5f342beff94723acd6131ce2dd8
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580701"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a>Crearea de entități și câmpuri particularizate ca dimensiuni de preț

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Parcurgeți pașii următori când doriți să creați un set de opțiuni sau o entitate particularizat(ă) pentru a o utiliza drept dimensiune de preț. Pentru mai multe informații, consultați [Prezentare generală a dimensiunii de preț](pricing-dimensions-overview.md).  

> [!IMPORTANT]
> Vă recomandăm să efectuați toate modificările de dimensiune de tarifare particularizate într-o soluție separată. Această bună practică importantă oferă flexibilitate în viitor pentru actualizarea sau eliminarea modificărilor, după cum este necesar. Acest lucru vă va ajuta, de asemenea, la reutilizarea muncii dvs. și va facilita portarea acestor modificări într-o altă instanță După ce ați făcut toate modificările necesare, exportați această soluție ca **Soluție gestionată** și importați-o în alte instanțe pentru a reutiliza configurarea prețurilor.

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Creați câmpuri particularizate și seturi de opțiuni în soluția de dimensiune de tarifare

O dimensiune de tarifare poate fi un set de opțiuni sau o entitate. Ambele trebuie să fie create în soluția dvs. de tarifare. Pașii din această procedură explică modul de creare a dimensiunilor bazate pe entități și a dimensiunilor bazate pe seturi de opțiuni.

### <a name="entity-based-dimensions"></a>Dimensiuni bazate pe entități
Pentru a crea dimensiuni bazate pe entități, urmați acești pași:

1. Accesați **Setări** > **Soluții**, apoi faceți dublu clic pe **\<your organization name> dimensiunile prețurilor**.
2. În Explorator soluții, în panoul de navigare din stânga, selectați **Entități**.
3. Selectați **Nou** pentru a crea o nouă entitate denumită **Titlu standard**. 
4. Introduceți restul de informații solicitate și apoi selectați **Salvare**.

> ![Definiție entitate titlu standard.](media/Standard-Title-entity-definition.png)

### <a name="option-set-based-dimensions"></a>Dimensiuni bazate pe seturi de opțiuni 
Aveți posibilitatea să creați două dimensiuni bazate pe seturi de opțiuni. 

- Utilizați **Locația de lucru a resurselor** pentru a urmări locația de lucru **Acasă** și **La fața locului**. 
- Utilizați **Resurse Program de lucru** cu valori **Regulat** și **Ore suplimentare** pentru a aplica un adaos când lucrarea este finalizată.

Următorul grafic oferă o vizualizare a dimensiunii **Locația de lucru a resurselor**. 

> ![Dimensiunea de tarifare bazată pe set de opțiuni denumită Locația de lucru resursă.](media/Option-set-PD-called-Resource-Work-Location.png)

Următorul grafic oferă o vizualizare a dimensiunii **Ore de lucru resursă**. 

> ![Dimensiunea de tarifare bazată pe set de opțiuni denumită Ore de lucru resursă.](media/Option-set-PD-called-Resource-Work-Hours.png)

1. Accesați **Setări** > **Soluții**, apoi faceți dublu clic pe  **\<your organization name> dimensiunile prețurilor**. 
2. În Explorator soluții, în panoul de navigare din stânga, selectați  **Seturi de opțiuni**. 
3. Selectați **Nou** pentru a crea un set de opțiuni nou, introduceți restul de informații solicitate, apoi selectați **Salvare**.

## <a name="create-data-for-entity-based-dimensions"></a>Crearea de date pentru dimensiunile bazate pe entități

Aveți posibilitatea să creați manual date pentru dimensiunile bazate pe entități sau utilizând apelurile de import sau de service Microsoft Excel. Utilizați pașii din această procedură pentru a crea două titluri standard, **Inginer sisteme** și **Inginer sisteme senior** din dimensiunea bazată pe entitate **Titlu standard**. Dacă datele pe care doriți să le creați sunt mici, ca în exemplul următor, aveți posibilitatea să utilizați un formular standard.

1. Selectați **Găsire complexă**.
2. Selectați entitatea **Titlu standard**, apoi selectați **Rezultate**. Toate rândurile din entitatea **Titlu standard** vor fi afișate.
3. Selectați **Nou** și pe câmpul **Nume**, introduceți „Inginer de sistem” și apoi selectați **Salvare**.
4. Închideți pagina. 
5. Repetați pașii 1-3 pentru a crea un alt titlu standard pentru „Inginer sisteme senior”.

> ![Date eșantion pentru entitatea Titlu standard.](media/ST-data.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]