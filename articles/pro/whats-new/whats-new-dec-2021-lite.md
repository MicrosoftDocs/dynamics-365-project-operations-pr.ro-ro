---
title: Ce este nou Decembrie 2021 - Implementarea Project Operations Lite
description: Acest subiect oferă informații despre actualizările de calitate care sunt disponibile în versiunea din decembrie 2021 a implementării Project Operations lite.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 0432e2d4970c352e91cca589987bbdace57c6eaf
ms.sourcegitcommit: 9d20e7738cce195d344f5925a115741a1ce3ca36
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 12/21/2021
ms.locfileid: "7942992"
---
# <a name="whats-new-december-2021---project-operations-lite-deployment"></a>Ce este nou Decembrie 2021 - Implementarea Project Operations Lite

_Se aplică pentru: implementare simplificată - înțelegere la emiterea facturii proforme_

Acest subiect se aplică următoarelor componente și versiuni ale Microsoft Dynamics 365 Project Operations:

- Operațiuni de proiect în a Dataverse versiunea de mediu 4.27.0.195, 4.27.0.242


## <a name="features-included-in-this-release"></a>Caracteristicile incluse în această versiune

### <a name="subcontract-management"></a>Managementul subcontractelor 

- [Subcontractarea membrilor echipei de proiect](../subcontracting/subcontracting-project-team-members.md) : Un manager de proiect poate crea membri de echipă numiți sau generici cu subcontracte și linii de subcontractare pentru a afecta personalul și estimarea.
- [Opțiuni de subcontractare pentru membrii echipei de proiect](../subcontracting/subcon-options.md) : Când face alegeri de personal pentru membrii echipei de proiect numiți sau generici, managerul de proiect poate revizui subcontractele existente sau poate crea subcontracte noi pentru unul sau mai mulți membri ai echipei de proiect. 
- [Estimarea costurilor alocărilor de resurse subcontractate](../subcontracting/costing-subcon-ra.md) : Estimarea costului proiectului va ține cont de alocările de resurse subcontractate și le va costa folosind listele de prețuri de achiziție asociate subcontractelor. 
- [Configurați Schedule Board pentru a afișa lucrătorii contractuali și capacitatea subcontractată](../subcontracting/configure-sb-subcon.md) : Tabloul de planificare din Operațiunile de proiect poate fi configurat acum pentru a căuta și a sugera tipul de lucrător contractual de resurse rezervabile și capacitatea subcontractată împreună cu angajații. Această configurație poate fi aplicată atunci când se caută resurse în contextul personalului pentru o anumită cerință de proiect sau când se caută în afara contextului unei cerințe de proiect.
- [Angajarea unui proiect cu lucrători contractuali și capacitate subcontractată](../subcontracting/staffing-cw.md) : Lucrătorii contractuali pot fi acum rezervați pentru proiecte care profită de experiențele consiliului de planificare.
- [Înregistrarea timpului, a cheltuielilor și a utilizării materialelor pe proiecte pentru componentele subcontractate](../subcontracting/recording-subcon-actuals.md) : Lucrătorii contractuali pot înregistra timpul și cheltuielile, iar membrii echipei de proiect pot, de asemenea, să înregistreze utilizarea materialelor achiziționate folosind un subcontract pentru un proiect. Acest lucru va avea ca rezultat înregistrarea costurilor precise pentru proiectele care utilizează capacitatea sau materialele achiziționate.
- [Tranziții de stat pe un subcontract](../subcontracting/subcon-states.md) : Subcontractele pot fi confirmate pentru a finaliza negocierea cu vânzătorul, închise pentru a indica finalizarea livrării sau anulate pentru a indica rezilierea contractului cu vânzătorul înainte de finalizarea livrării.

### <a name="task-planning"></a>Planificarea sarcinilor
- Depanare îmbunătățită pentru administratorii de sistem. Când un utilizator nu poate deschide un proiect, administratorul poate examina erorile care nu sunt legate de licență generate de Project pentru web în [Jurnalele de programare a proiectelor](../../project-management/schedule-api-logs.md).
- [Utilizați liste de verificare a sarcinilor în Microsoft Project pentru web](https://support.microsoft.com/en-us/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c). În Microsoft Project pentru web, puteți adăuga o listă de verificare la o sarcină pentru a urmări anumite elemente.

## <a name="quality-updates"></a>Actualizări de calitate

| **Zonă de caracteristici** | **Număr de referință** | **Actualizare de calitate** |
| --- | --- | --- |
| Planificare și urmărire | 2392596 | API-urile Schedule permit acum actualizări ale **Efort rămas**, **finalizat**, și **% Complet** câmpuri. |
| Planificare și urmărire | 2478497 | Programați API-uri **Numărul activității** și **ID-ul sarcinii** câmpurile pot fi goale la introducere, deoarece sistemul le va popula folosind numerotarea automată.|
| Timp și cheltuială | 2468135 | Numărul de reîncercări de aprobare este redus de la cinci la trei. |
| Timp și cheltuială | 2468188 | S-a rezolvat problema cu textul jurnalului care depășește lungimea maximă în fișierul **notetext** atributul **adnotare** entitate. |
