---
title: Creare soluții particularizate pentru dimensiunile de tarifare
description: Acest subiect explică cum să creați o soluție personalizată atunci când creați dimensiuni de tarifare personalizate.
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
ms.openlocfilehash: 3e437fce5b9f1fb330a713788e24100a4fe02948
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082805"
---
# <a name="create-custom-solutions-for-pricing-dimensions"></a>Creare soluții particularizate pentru dimensiunile de tarifare

> [!IMPORTANT]
> Toate modificările dimensiunii de preț personalizate ar trebui să fie într-o soluție separată. Această bună practică importantă oferă flexibilitate în viitor pentru a actualiza sau elimina modificările după este necesar, va ajuta la reutilizarea activității dvs. și facilitează portarea acestor modificări într-o altă instanță. După ce faceți modificările necesare, exportați această soluție ca **Soluție gestionată** și importați-o în alte instanțe pentru a reutiliza configurația dvs. de tarifare.

1. Selectați **Setări** > **Soluții** , apoi selectați **Nou**. 
2. Denumiți soluția, **\<your organization name> dimensiunile de preț** , introduceți informațiile necesare rămase și apoi selectați **Salvați**.

> ![Crearea unei soluții particularizate pentru dimensiunile de tarifare](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>Adăugați toate entitățile necesare și componentele corelate la Soluția de dimensiune de preț
Va trebui să adăugați următoarele entități Project Service la soluția dvs. de tarifare. Completați pașii din această procedură pentru a face unele modificări importante ale schemei în soluția de tarifare, astfel încât entitățile să devină conștiente de noile dimensiuni de tarifare.

1. Selectați **Setări** > **Soluții** și apoi faceți clic dublu pe **\<your organization name> dimensiuni de preț**. 
2. În Explorator soluții, în panoul de navigare din stânga, selectați **Adăugare existentă** > **Entități**.
3. În caseta de dialog **Componente soluție** , selectați următoarele entități:

- Real
- Resursă ce se poate rezerva
- Linie estimată
- Activitate de proiect
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

4. Când vi se solicită să includeți orice entități dependente pentru entitățile selectate, selectați **Nu**.

> ![Nu includeți toate componentele corelate](media/Do-not-include-required.png)


