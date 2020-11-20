---
title: Crearea de entități și câmpuri particularizate ca dimensiuni de preț
description: Acest subiect oferă informații despre cum să creați seturi de opțiuni personalizate sau entități.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 616bcd5758b434b45bd06aa1a026f32efc8b7f99
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130908"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a>Crearea de entități și câmpuri particularizate ca dimensiuni de preț

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Parcurgeți pașii următori în orice moment în care doriți să creați un set de opțiuni sau o entitate particularizat(ă).

> [!IMPORTANT]
> Vă recomandăm să efectuați toate modificările de dimensiune de tarifare particularizate într-o soluție separată. Această bună practică importantă oferă flexibilitate în viitor pentru a actualiza sau elimina modificările după este necesar, va ajuta la reutilizarea activității dvs. și facilitează portarea acestor modificări într-o altă instanță. După ce ați făcut toate modificările necesare, exportați această soluție ca **Soluție gestionată** și importați-o în alte instanțe pentru a reutiliza configurația dvs. de tarifare.


## <a name="create-a-custom-solution-for-pricing-dimensions"></a>Crearea unei soluții particularizate pentru dimensiunile de tarifare
1. Accesați **Setări** > **Soluții** și apoi selectați **Nou** pentru a crea o soluție nouă. 
2. Denumiți soluția, **\<your organization name> dimensiunile de preț**, introduceți informațiile necesare rămase și apoi selectați **Salvați**.
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Creați câmpuri particularizate și seturi de opțiuni în soluția de dimensiune de tarifare

O dimensiune de tarifare poate fi un set de opțiuni sau o entitate. Ambele trebuie să fie create în soluția dvs. de tarifare. Pașii din această procedură explică modul de creare a dimensiunilor bazate pe entități și a dimensiunilor bazate pe seturi de opțiuni.

### <a name="entity-based-dimensions"></a>Dimensiuni bazate pe entități

1. Accesați **Setări** > **Soluții**, apoi faceți dublu clic pe **\<your organization name> dimensiunile prețurilor**.
2. În Explorator soluții, în panoul de navigare din stânga, selectați **Entități**.
3. Selectați **Nou** pentru a crea o nouă entitate denumită **Titlu standard**. 
4. Introduceți restul de informații solicitate și apoi selectați **Salvare**.


### <a name="option-set-based-dimensions"></a>Dimensiuni bazate pe seturi de opțiuni 
Aveți posibilitatea să creați două dimensiuni bazate pe seturi de opțiuni. Utilizați **Locația de lucru resursă** pentru a urmări prețul lucrărilor cu locația **Acasă** și **Local** și utilizați **Ore de lucru resursă** cu valorile **Obișnuite** și **Ore suplimentare** pentru a aplica un marcaj la terminarea lucrărilor.


1. Accesați **Setări** > **Soluții**, apoi faceți dublu clic pe  **\<your organization name> dimensiunile prețurilor**. 
2. În Explorator soluții, în panoul de navigare din stânga, selectați **Seturi de opțiuni**. 
3. Selectați **Nou** pentru a crea un set de opțiuni nou, introduceți restul de informații solicitate, apoi selectați **Salvare**.

## <a name="create-data-for-entity-based-dimensions"></a>Crearea de date pentru dimensiunile bazate pe entități

Aveți posibilitatea să creați manual date pentru dimensiunile bazate pe entități sau utilizând apelurile de import sau de service Microsoft Excel. Utilizați pașii din această procedură pentru a crea două titluri standard, **Inginer sisteme** și **Inginer sisteme senior** din dimensiunea bazată pe entitate **Titlu standard**. Dacă datele pe care doriți să le creați sunt mici, ca în exemplul următor, aveți posibilitatea să utilizați un formular standard.

1. Selectați **Găsire avansată**, selectați entitatea **Titlu standard**, apoi selectați **Rezultate**. Toate rândurile din entitatea **Titlu standard** vor fi afișate.
2. Selectați **Nou** și pe câmpul **Nume**, introduceți „Inginer de sistem” și apoi selectați **Salvare**.
3. Închideți formularul. 
4. Repetați pașii 1-3 pentru a crea un alt titlu standard pentru „Inginer sisteme senior”.

## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>Adăugați toate entitățile necesare și componentele corelate la Soluția de dimensiune de tarifare
Va trebui să adăugați următoarele entități la soluția dvs. de tarifare. Utilizați pașii din această procedură pentru a face unele modificări importante ale schemei în soluția de tarifare, astfel încât entitățile să devină conștiente de noile dimensiuni de tarifare.

1. Selectați **Setări** > **Soluții** și faceți clic dublu pe **\<your organization name> dimensiuni de preț**. 
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


> [!NOTE]
> Asigurați-vă că includeți toate formularele și vizualizările pentru fiecare dintre entitățile selectate.

4. Când vi se solicită să includeți orice entități dependente pentru entitățile selectate mai sus, selectați **Nu**.

