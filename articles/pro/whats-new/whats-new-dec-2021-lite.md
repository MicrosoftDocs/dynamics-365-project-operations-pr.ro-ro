---
title: Noutăți decembrie 2021 - implementare Project Operations lite
description: Acest articol oferă informații despre actualizările de calitate care sunt disponibile în versiunea din septembrie 2021 de implementare a Project Operations lite.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 301acc5be76fb0318d6298820b62ae5bb05efac3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914095"
---
# <a name="whats-new-december-2021---project-operations-lite-deployment"></a>Noutăți decembrie 2021 - implementare Project Operations lite

_Se aplică pentru: implementare simplificată - înțelegere la emiterea facturii proforme_

Acest articol se aplică următoarelor componente și versiuni de Microsoft Dynamics 365 Project Operations:

- Project Operations într-un mediu Dataverse versiunea 4.27.0.195, 4.27.0.242, 4.27.0.244


## <a name="features-included-in-this-release"></a>Caracteristicile incluse în această versiune

### <a name="subcontract-management"></a>Gestionarea subcontractării 

- [Subcontractarea membrilor echipei de proiect](../subcontracting/subcontracting-project-team-members.md): Un manager de proiect poate crea membri de echipă numiți sau generici cu subcontracte și linii de subcontractare pentru a efectua încadrarea și estimarea.
- [Opțiuni de subcontractare pentru membrii echipei de proiect](../subcontracting/subcon-options.md): Când face alegeri de încadrare pentru membrii echipei de proiect numiți sau generici, managerul de proiect poate revizui subcontractele existente sau poate crea subcontracte noi pentru unul sau mai mulți membri ai echipei de proiect. 
- [Estimarea costurilor alocărilor de resurse subcontractate](../subcontracting/costing-subcon-ra.md): Estimarea costului proiectului va ține cont de alocările de resurse subcontractate și le va calcula folosind listele de prețuri de achiziție asociate subcontractelor. 
- [Configurați Tabloul de planificare pentru a afișa lucrătorii contractuali și capacitatea subcontractată](../subcontracting/configure-sb-subcon.md): Tabloul de planificare din Project Operations poate fi acum configurat pentru a căuta și sugera tipul de lucrător contractual de resurse rezervabile și capacitatea subcontractată alături de angajați. Această configurație poate fi aplicată atunci când se caută resurse în contextul încadrării pentru o anumită cerință de proiect sau când se caută în afara contextului unei cerințe de proiect.
- [Încadrarea de lucrători contractuali și capacitate subcontractată pentru un proiect](../subcontracting/staffing-cw.md): Lucrătorii contractuali pot fi acum rezervați pentru proiecte care se folosesc de experiențele tabloului de planificare.
- [Înregistrarea timpului, a cheltuielilor și a utilizării materialelor pe proiecte pentru componentele subcontractate](../subcontracting/recording-subcon-actuals.md): Lucrătorii contractuali pot înregistra timpul și cheltuielile, iar membrii echipei de proiect pot, de asemenea, să înregistreze utilizarea materialelor achiziționate folosind un subcontract pentru un proiect. Acest lucru va avea ca rezultat înregistrarea costurilor precise pentru proiectele care utilizează capacitatea sau materialele achiziționate.
- [Tranziții de stare pe un subcontract](../subcontracting/subcon-states.md): Subcontractele pot fi confirmate pentru a finaliza negocierea cu vânzătorul, închise pentru a indica finalizarea livrării sau anulate pentru a indica rezilierea contractului cu vânzătorul înainte de finalizarea livrării.

### <a name="task-planning"></a>Planificarea sarcinilor
- Depanare îmbunătățită pentru administratorii de sistem. Când un utilizator nu poate deschide un proiect, administratorul poate examina erorile care nu sunt legate de licență generate de Project for the web în [Jurnalele de programare a proiectelor](../../project-management/schedule-api-logs.md).
- [Utilizați liste de verificare a sarcinilor în Microsoft Project for the web](https://support.microsoft.com/en-us/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c). În Microsoft Project for the web, puteți adăuga o listă de verificare la o sarcină pentru a urmări anumite elemente.

## <a name="quality-updates"></a>Actualizări de calitate

| **Zonă de caracteristici** | **Număr de referință** | **Actualizare de calitate** |
| --- | --- | --- |
| Planificare și urmărire | 2392596 | API-urile Planificare permit acum actualizări ale câmpurilor **Efort rămas**, **Efort depus** și **Finalizat %**. |
| Planificare și urmărire | 2478497 | Programați API-uri câmpurile **Număr activitate** și **ID activitate** pot fi goale la introducere, deoarece sistemul le va popula folosind numerotarea automată.|
| Timp și cheltuială | 2468135 | Numărul de reîncercări de aprobare este redus de la cinci la trei. |
| Timp și cheltuială | 2468188 | S-a rezolvat problema legată de textul jurnalului care depășește lungimea maximă în atributul **notetext** al entității **adnotare**. |
