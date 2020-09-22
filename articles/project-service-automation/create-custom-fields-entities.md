---
title: Crearea câmpurilor și entităților particularizate
description: Acest subiect explică modul de creare a seturilor de opțiuni și a entităților în soluția proprie în platforma Power Apps platform.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/26/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: fb160bfd-e037-4a21-a968-3ff2e6e16481
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 7ee30e3bb6b8034ef226e2e9181195685355011f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754811"
---
# <a name="create-custom-fields-and-entities"></a>Crearea câmpurilor și entităților particularizate 

Parcurgeți pașii următori în orice moment în care doriți să creați un set de opțiuni sau o entitate particularizat(ă) pe platforma Power Apps.  
Procedurile din acest subiect trebuie parcurse folosind interfața web a Project Service Automation (PSA).

> [!IMPORTANT]
> Vă recomandăm să efectuați toate modificările de dimensiune de tarifare particularizate într-o soluție separată. Această bună practică importantă oferă flexibilitate în viitor pentru a actualiza sau elimina modificările după este necesar, va ajuta la reutilizarea activității dvs. și facilitează portarea acestor modificări într-o altă instanță. După ce ați făcut toate modificările necesare, exportați această soluție ca **Soluție gestionată** și importați-o în alte instanțe pentru a reutiliza configurația dvs. de tarifare.


## <a name="create-a-custom-solution-for-pricing-dimensions"></a>Crearea unei soluții particularizate pentru dimensiunile de tarifare
1. În PSA, faceți clic pe **Setări** > **Soluții**, apoi faceți clic pe **Nou** pentru a crea o soluție nouă. 
2. Denumiți soluția, **\<numele organizației dvs. > dimensiuni de tarifare**, introduceți restul de informații solicitate, apoi faceți clic pe **Salvare.**

> ![Crearea unei soluții particularizate pentru dimensiunile de tarifare](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Creați câmpuri particularizate și seturi de opțiuni în soluția de dimensiune de tarifare

O dimensiune de tarifare poate fi un set de opțiuni sau o entitate. Ambele trebuie să fie create în soluția dvs. de tarifare. Pașii din această procedură explică modul de creare a dimensiunilor bazate pe entități și a dimensiunilor bazate pe seturi de opțiuni.

### <a name="entity-based-dimensions"></a>Dimensiuni bazate pe entități

1. În PSA, faceți clic pe **Setări** > **Soluții**, apoi faceți dublu clic pe **\<numele organizației dvs.> dimensiunile prețurilor**.
2. În Explorator soluții, în panoul de navigare din stânga, selectați **Entități**.
3. Faceți clic pe **Nou** pentru a crea o nouă entitate denumită **Titlu standard**. Introduceți restul de informații solicitate și apoi faceți clic pe **Salvare**.

> ![Definiție entitate titlu standard](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a>Dimensiuni bazate pe seturi de opțiuni 
Aveți posibilitatea să creați două dimensiuni bazate pe seturi de opțiuni. Utilizați **Locația de lucru resursă** pentru a urmări prețul lucrărilor cu locația **Acasă** și **Local** și utilizați **Ore de lucru resursă** cu valorile **Obișnuite** și **Ore suplimentare** pentru a aplica un marcaj la terminarea lucrărilor.


1. În PSA, faceți clic pe **Setări** > **Soluții**, apoi faceți dublu clic pe **\<numele organizației dvs. > dimensiuni de tarifare**. 
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

## <a name="add-all-required-psa-entities-and-related-components-to-the-pricing-dimension-solution"></a>Adăugați toate entitățile PSA necesare și componentele corelate la Soluția de dimensiune de tarifare
Va trebui să adăugați următoarele entități Project Service la soluția dvs. de tarifare. Utilizați pașii din această procedură pentru a face unele modificări importante ale schemei în soluția de tarifare, astfel încât entitățile să devină conștiente de noile dimensiuni de tarifare.

1. În PSA, faceți clic pe **Setări** > **Soluții**, apoi faceți dublu clic pe **\<numele organizației dvs.> dimensiunile prețurilor**. 
2. În Explorator soluții, în panoul de navigare din stânga, selectați **Adăugare existentă** > **Entități**.
3. În caseta de dialog **Componente soluție**, selectați următoarele entități:

- Real
- Resursă ce se poate rezerva
- Linie estimată
- Detaliu linie factură
- Linie de jurnal
- Detaliu linie contract pentru proiect
- Membru echipă de proiect
- Detaliu linie de ofertă
- Adaos de preț pentru rol
- Preț pentru rol 
- Intrare de timp 

> ![Adăugați entități existente la soluția de dimensiuni de tarifare](media/Existing-entities-to-PD-solution.png)

> ![Selectare componente soluție](media/Dimension-Components.png)

> [!NOTE]
> Asigurați-vă că includeți toate formularele și vizualizările pentru fiecare dintre entitățile selectate.

4. Când vi se solicită să includeți orice entități dependente pentru entitățile selectate mai sus, faceți clic pe **Nu**.

> ![Nu includeți toate componentele corelate](media/Do-not-include-required.png)


