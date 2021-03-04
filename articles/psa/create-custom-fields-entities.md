---
title: Crearea câmpurilor și entităților particularizate
description: Acest subiect explică modul de creare a seturilor de opțiuni și a entităților în soluția proprie în platforma Power Apps platform.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: b9e32c8871a8986ba827f742baf4e4d5cd9dd235
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144878"
---
# <a name="create-custom-fields-and-entities"></a>Crearea câmpurilor și entităților particularizate 

[!include [banner](../includes/psa-now-project-operations.md)]

Parcurgeți pașii următori în orice moment în care doriți să creați un set de opțiuni sau o entitate particularizat(ă) pe platforma Power Apps.  
Procedurile din acest subiect trebuie parcurse folosind interfața web a Project Service Automation (PSA).

> [!IMPORTANT]
> Vă recomandăm să efectuați toate modificările de dimensiune de tarifare particularizate într-o soluție separată. Această bună practică importantă oferă flexibilitate în viitor pentru a actualiza sau elimina modificările după este necesar, va ajuta la reutilizarea activității dvs. și facilitează portarea acestor modificări într-o altă instanță. După ce ați făcut toate modificările necesare, exportați această soluție ca **Soluție gestionată** și importați-o în alte instanțe pentru a reutiliza configurația dvs. de tarifare.

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Creați câmpuri particularizate și seturi de opțiuni în soluția de dimensiune de tarifare

O dimensiune de tarifare poate fi un set de opțiuni sau o entitate. Ambele trebuie să fie create în soluția dvs. de tarifare. Pașii din această procedură explică modul de creare a dimensiunilor bazate pe entități și a dimensiunilor bazate pe seturi de opțiuni.

### <a name="entity-based-dimensions"></a>Dimensiuni bazate pe entități

1. În PSA, selectați **Setări** > **Soluții** și apoi faceți clic dublu pe **\<your organization name> dimensiuni de preț**.
2. În Explorator soluții, în panoul de navigare din stânga, selectați **Entități**.
3. Faceți clic pe **Nou** pentru a crea o nouă entitate denumită **Titlu standard**. Introduceți restul de informații solicitate și apoi faceți clic pe **Salvare**.

> ![Definiție entitate titlu standard](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a>Dimensiuni bazate pe seturi de opțiuni 
Aveți posibilitatea să creați două dimensiuni bazate pe seturi de opțiuni. Utilizați **Locația de lucru resursă** pentru a urmări prețul lucrărilor cu locația **Acasă** și **Local** și utilizați **Ore de lucru resursă** cu valorile **Obișnuite** și **Ore suplimentare** pentru a aplica un marcaj la terminarea lucrărilor.


1. În PSA, selectați **Setări** > **Soluții** și apoi faceți clic dublu pe  **\<your organization name> dimensiuni de preț**. 
2. În Explorator soluții, în panoul de navigare din stânga, selectați **Seturi de opțiuni**. 
3. Faceți clic pe **Nou** pentru a crea un set de opțiuni nou, introduceți restul de informații solicitate, apoi faceți clic pe **Salvare**.

> ![Dimensiunea de tarifare bazată pe set de opțiuni denumită Locația de lucru resursă ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![Dimensiunea de tarifare bazată pe set de opțiuni denumită Ore de lucru resursă ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a>Crearea de date pentru dimensiunile bazate pe entități

Aveți posibilitatea să creați manual date pentru dimensiunile bazate pe entități sau utilizând apelurile de import sau de service Microsoft Excel. Utilizați pașii din această procedură pentru a crea două titluri standard, **Inginer sisteme** și **Inginer sisteme senior** din dimensiunea bazată pe entitate **Titlu standard**. Dacă datele pe care doriți să le creați sunt mici, ca în exemplul următor, aveți posibilitatea să utilizați un formular standard.

1. În PSA, faceți clic pe **Găsire complexă**. Selectați entitatea **Titlu standard**, apoi faceți clic pe **Rezultate**. Toate rândurile din entitatea **Titlu standard** vor fi afișate.
2. Faceți clic pe **Nou**. În câmpul **Nume**, introduceți „Inginer sisteme” și apoi faceți clic pe **Salvare**.
3. Închideţi formularul. 
4. Repetați pașii 1-3 pentru a crea un alt titlu standard pentru „Inginer sisteme senior”.

> ![Date eșantion pentru entitatea Titlu standard ](media/ST-data.png)


