---
title: Crearea unei soluții pentru dimensiunile de tarifare particularizate
description: Acest subiect oferă informații despre cum să creați soluții pentru dimensiuni de preț particularizate.
author: Rumant
manager: tfehr
ms.date: 11/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 441501dff23d16960381b3f9fb4b2cceba2b3ba5
ms.sourcegitcommit: 869bde007805ef255f61b03937e4a44aeef61df9
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 11/12/2020
ms.locfileid: "4514015"
---
# <a name="create-a-solution-for-custom-pricing-dimensions"></a>Crearea unei soluții pentru dimensiunile de tarifare particularizate

 _**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_ 

>[!IMPORTANT]
>Toate modificările dimensiunii de preț personalizate ar trebui să fie într-o soluție separată. Această bună practică importantă permite flexibilitatea de a actualiza sau elimina modificările după este necesar, ajută la reutilizarea activității dvs. și facilitează portarea acestor modificări în alte instanțe. După ce faceți toate modificările necesare, exportați această soluție ca soluție **Gestionată** și apoi importați-o în alte instanțe pentru reutilizare.

## <a name="create-a-solution-for-custom-pricing-dimensions"></a>Crearea unei soluții pentru dimensiunile de tarifare particularizate

1.  Selectați **Setări** > **Soluții**, apoi selectați **Nou**.
2.  Denumiți soluția, *<your organization name> dimensiunile prețurilor*.
3. Introduceți restul de informații solicitate și apoi selectați **Salvare**.

  ![Crearea de soluții pentru dimensiunea de preț particularizată](./media/Creation-of-custom-pricing-dimension-solution.png)
 
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>Adăugați toate entitățile necesare și componentele corelate la Soluția de dimensiune de preț

Adăugați următoarele entități Project Service la soluția dvs. de stabilire a prețurilor pentru a efectua modificări importante ale schemei în soluția de stabilire a prețurilor. După ce ați finalizat această procedură, entitățile vor recunoaște noile dimensiuni de stabilire a prețurilor.

1.  Selectați **Setări** > **Soluții** și apoi faceți dublu clic pe **<*numele organizației dvs.*> dimensiuni de tarifare**.
2.  În Explorator soluții, în panoul de navigare din stânga, selectați **Adăugare existentă** > **Entități**.
3.  În caseta de dialog **Componente soluție**, selectați următoarele entități:
 
   - **Real**
   - **Resursă ce se poate rezerva**
   - **Linie estimată**
   - **Activitate de proiect**
   - **Detaliu linie factură**
   - **Linie de jurnal**
   - **Detaliu linie contract pentru proiect**
   - **Membru echipă de proiect**
   - **Detaliu linie de ofertă**
   - **Adaos de preț pentru rol**
   - **Preț pentru rol**
   - **Intrare de timp**
 
   ![Adăugați entități existente soluția de dimensiuni de tarifare particularizată](./media/Existing-entities-to-PD-solution.png)
 
 4. Pentru fiecare entitate, revedeți componentele care se adaugă și lista finală a activelor entității pentru fiecare entitate. 

   >[!NOTE]
   > Includeți toate formularele și vizualizările pentru fiecare dintre entitățile selectate.

  ![Entități adăugate](./media/solution-component-selection.png)


5.  Când vi se solicită să includeți entități dependente pentru entitățile selectate, selectați **Nu, nu includeți componentele necesare.**

    ![Inclusiv entități dependente](./media/Do-not-include-required.png)