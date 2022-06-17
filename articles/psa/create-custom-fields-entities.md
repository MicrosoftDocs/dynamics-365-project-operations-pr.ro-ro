---
title: Crearea câmpurilor și entităților particularizate
description: Acest articol explică cum să creați seturi de opțiuni și entități în propria soluție în Power Apps platformă.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 3b6f675d604f3b6a6f2465c413ceff3d16815e12
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926929"
---
# <a name="create-custom-fields-and-entities"></a>Crearea câmpurilor și entităților particularizate 

[!include [banner](../includes/psa-now-project-operations.md)]

Parcurgeți pașii următori în orice moment în care doriți să creați un set de opțiuni sau o entitate particularizat(ă) pe platforma Power Apps.  
Procedurile din acest articol trebuie finalizate folosind interfața web a Project Service Automation (PSA).

> [!IMPORTANT]
> Vă recomandăm să efectuați toate modificările de dimensiune de tarifare particularizate într-o soluție separată. Această bună practică importantă oferă flexibilitate în viitor pentru a actualiza sau elimina modificările după este necesar, va ajuta la reutilizarea activității dvs. și facilitează portarea acestor modificări într-o altă instanță. După ce ați făcut toate modificările necesare, exportați această soluție ca **Soluție gestionată** și importați-o în alte instanțe pentru a reutiliza configurația dvs. de tarifare.

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Creați câmpuri particularizate și seturi de opțiuni în soluția de dimensiune de tarifare

O dimensiune de tarifare poate fi un set de opțiuni sau o entitate. Ambele trebuie să fie create în soluția dvs. de tarifare. Pașii din această procedură explică modul de creare a dimensiunilor bazate pe entități și a dimensiunilor bazate pe seturi de opțiuni.

### <a name="entity-based-dimensions"></a>Dimensiuni bazate pe entități

1. În PSA, selectați **Setări** > **Soluții** și apoi faceți clic dublu pe **\<your organization name> dimensiuni de preț**.
2. În Explorator soluții, în panoul de navigare din stânga, selectați **Entități**.
3. Faceți clic pe **Nou** pentru a crea o nouă entitate denumită **Titlu standard**. Introduceți restul de informații solicitate și apoi faceți clic pe **Salvare**.

> ![Definiție entitate titlu standard.](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a>Dimensiuni bazate pe seturi de opțiuni 
Aveți posibilitatea să creați două dimensiuni bazate pe seturi de opțiuni. Utilizați **Locația de lucru resursă** pentru a urmări prețul lucrărilor cu locația **Acasă** și **Local** și utilizați **Ore de lucru resursă** cu valorile **Obișnuite** și **Ore suplimentare** pentru a aplica un marcaj la terminarea lucrărilor.


1. În PSA, selectați **Setări** > **Soluții** și apoi faceți clic dublu pe  **\<your organization name> dimensiuni de preț**. 
2. În Explorator soluții, în panoul de navigare din stânga, selectați **Seturi de opțiuni**. 
3. Faceți clic pe **Nou** pentru a crea un set de opțiuni nou, introduceți restul de informații solicitate, apoi faceți clic pe **Salvare**.

> ![Dimensiunea de tarifare bazată pe set de opțiuni denumită Locația de lucru resursă.](media/Option-set-PD-called-Resource-Work-Location.png)

> ![Dimensiunea de tarifare bazată pe set de opțiuni denumită Ore de lucru resursă.](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a>Crearea de date pentru dimensiunile bazate pe entități

Aveți posibilitatea să creați manual date pentru dimensiunile bazate pe entități sau utilizând apelurile de import sau de service Microsoft Excel. Utilizați pașii din această procedură pentru a crea două titluri standard, **Inginer sisteme** și **Inginer sisteme senior** din dimensiunea bazată pe entitate **Titlu standard**. Dacă datele pe care doriți să le creați sunt mici, ca în exemplul următor, aveți posibilitatea să utilizați un formular standard.

1. În PSA, faceți clic pe **Găsire complexă**. Selectați entitatea **Titlu standard**, apoi faceți clic pe **Rezultate**. Toate rândurile din entitatea **Titlu standard** vor fi afișate.
2. Faceți clic pe **Nou**. În câmpul **Nume**, introduceți „Inginer sisteme” și apoi faceți clic pe **Salvare**.
3. Închideţi formularul. 
4. Repetați pașii 1-3 pentru a crea un alt titlu standard pentru „Inginer sisteme senior”.

> ![Date eșantion pentru entitatea Titlu standard.](media/ST-data.png)




[!INCLUDE[footer-include](../includes/footer-banner.md)]
