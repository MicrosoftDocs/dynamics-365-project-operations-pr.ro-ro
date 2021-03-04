---
title: Vizualizați utilizarea taxabilă pentru o resursă
description: Acest subiect furnizează informații despre vizualizarea utilizării resurselor.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 4516c562e7eaf35c5fef638183967eef5a033b11
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146408"
---
# <a name="view-chargeable-utilization-for-resources"></a>Vizualizați utilizarea taxabilă pentru o resursă

[!include [banner](../includes/psa-now-project-operations.md)]
 
**Vizualizarea utilizării** pe pagina **Utilizarea resurselor Project Service** afișează utilizarea taxabilă pentru fiecare resursă care se poate rezerva. Întrucât vizualizarea se bazează pe tabloul de planificare, astfel încât veți găsi multe din aceleași funcții.

> ![Captură ecran pentru Vizualizarea utilizării](media/FAQ-utilization-1.png)
 

Calculul de utilizare taxabilă funcționează după cum urmează:

   Utilizare taxabilă = (ore efective taxabile)/(capacitate resursă)

Celulele reprezintă utilizarea taxabilă calculată pentru perioada selectată (zile, săptămâni sau luni).

Culorile din fiecare celulă arată utilizarea taxabilă pentru o resursă în comparație cu utilizarea taxabilă țintă a acestora. 

Utilizarea țintă poate fi setată fie pe rolul implicit al resursei, fie pe resursa individuală în sine. Calculul privește individual mai întâi ținta, apoi rolul implicit al resursei.

## <a name="set-target-on-a-resource"></a>Setați țintă pe o resursă

1. Accesați **Resurse** \> **Resurse**. 
2. Selectați o resursă pentru a deschide înregistrarea. 
3. În fila **Project Service**, puteți seta utilizarea țintă a resursei.

> ![Captură de ecran a utilizării filei Project Service pentru a seta utilizarea țintă](media/FAQ-utilization-2.png)
 
## <a name="set-target-utilization-on-a-role"></a>Setați utilizarea țintă pe un rol

1. Accesați **Resurse** \> **Roluri de resursă**. 
2. Selectați un rol și deschideți înregistrarea. 
3. Setați utilizarea țintei pentru rol.

> ![Captură de ecran a utilizării Rolurilor resursei pentru a seta utilizarea țintă](media/FAQ-utilization-3.png)
 
## <a name="calculate-chargeable-utilization-for-a-resource"></a>Calculați utilizarea taxabilă pentru o resursă

Pentru a calcula utilizarea taxabilă pentru o resursă, va trebui să întruniți câteva cerințe preliminare. 

### <a name="set-default-role-for-individual-resource"></a>Setați rolul implicit pentru resursa individuală

În primul rând, utilizarea țintă trebuie să fi setată fie pe resursa individuală, fie pe rolurile resursei. Dacă utilizați rolurile resursei pentru obiective, fiecare resursă individuală trebuie să aibă un rol implicit. 

1. Pentru a seta acest lucru, accesați **Resurse** \> **Resurse**. 
2. Selectați o resursă, deschideți înregistrarea, apoi selectați fila **Project service**. 
3. În grila **Rol resursă**, asigurați-vă că există un rol pentru resursă și **Este implicit** este setat la **Da**.
 
### <a name="change-billing-type-for-resource-role"></a>Modificați tipul de facturare pentru rolul de resursă

Rolurile de resursă trebuie setate pentru a avea un tip de facturare **Taxabil**. 

1. Accesați **Resurse** \> **Roluri de resursă**. 
2. Deschideți înregistrarea pe care doriți să o acualizați, apoi setați implicit tipul de facturare pe **Taxabil**.

### <a name="set-working-hours-for-resource-role"></a>Setați orele lucrătroare pentru rolul resursei
 
Resursa trebuie să aibă ore de lucru pentru capacitatea de calcul. 

1. Accesați **Resurse** \> **Resurse**. 
2. Selectați o resursă pentru a deschide înregistrarea, apoi selectați **Afișați orele de lucru**. 
3. Puteți actualiza în bloc lista de resurse aplicând un **șablon de ore de lucru** din vizualizarea **Listă de resurse**.

## <a name="troubleshooting-chargeable-actual-hours"></a>Depanarea orelor efective taxabile

Orele efective taxabile provin din entitatea **Valori reale**. Valorile reale cu un tip de facturare **Taxabil** sunt incluse în calcul și din acest motiv trebuie să aveți proiecte în cazul în care valorile reale sunt taxabile.

Dacă nu vedeți utilizarea taxabilă, aici sunt câteva aspecte care pot fi verificate:

- Resursa are ore de lucru definite pentru capacitate.
- Resursa are fie o țintă de utilizare definită individual, fie un rol implicit atribuit. Rolul are o țintă de utilizare definită pentru el.
- Valorile reale au un tip de facturare **Taxabil** pentru perioada pentru care estimați un calcul de utilizare. Verificați următoarele dacă vedeți valorile actuale cu alte tipuri de facturare decât contra cost:

  - Rolul utilizat pe valorile reale are un tip de facturare implicit sau altul decât facturabil.
  - Rolul din linia contractului subadiacentă proiectului a fost setat pe non-taxabil.
  - Proiectul nu are o linie a contractului asociată.

