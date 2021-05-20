---
title: Ce este nou sau schimbat în Project Service Automation versiunea actualizată 26, V3
description: Acest subiect listează caracteristicile și corecțiile care sunt disponibile în Project Service Automation V3, versiunea actualizată 26, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/12/2021
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
ms.openlocfilehash: 669b3ca4601bdac483db4e1d7f55a8bf5b3d9661
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948839"
---
# <a name="project-service-automation-update-release-26-v3"></a>Project Service Automation, versiunea actualizată 26, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Suntem încântați să anunțăm cea mai recentă actualizare pentru aplicația Project Service Automation pentru Dynamics 365. Această versiune include câteva îmbunătățiri importante ale calității, performanței și utilizabilității. Această versiune este compatibilă cu Dynamics 365 9.x. Pentru a actualiza această versiune, accesați Centrul de administrare pentru Dynamics 365, pagina de soluții online pentru a instala actualizarea. Pentru informații suplimentare, consultați: [Instalarea, actualizarea sau eliminarea unei soluții preferate](/power-platform/admin/install-remove-preferred-solution).

Acest subiect listează caracteristicile și corecțiile care sunt noi sau modificate pentru Project Service Automation, versiunea actualizată 26, V3. Această versiune are un număr de versiune V3.10.44.59 și este în general disponibilă printr-o actualizare automată în decembrie 2020.

## <a name="update-release-26"></a>Lansarea de actualizări 26

### <a name="bug-fixes"></a>Remedieri de erori

**Timp și cheltuială**

S-au remediat următoarele probleme:

- Utilizatorii pot modifica sarcina la o intrare de timp care a fost aprobată/trimisă.
- Eroare „Referință obiect neconfigurat” la salvarea timpului de intrare.
- Importarea intrării de timp din alocările de resurse creează intrări de timp cu valorile incorecte DateTime.
- Când Project Service Automation și aplicația Field Service sunt ambele instalate, butonul **Nou** se afișează de două ori pe bara de comandă pentru intrările de timp în aplicația Field Service.
- Actualizările de celule **Permiteți unitate** și **Grup de unități** funcționează acum pe grila **Estimări de cheltuieli**.
- Formularul **Actualizare editare intrare timp** include **Cronologie**.
- Aprobarea timpului pentru intrările de timp care nu fac parte din proiect blochează sistemul atunci când caută un rol de aprobator de proiect.

**Gestionarea resurselor**

S-au remediat următoarele probleme:

- S-a adăugat validarea în insertul **PostProjectCreate** pentru a verifica o cerință principală înainte de a crea una.
- Formularul de creare rapidă **Membru al echipei de proiect** aruncă o excepție de referință nulă dacă câmpurile sunt eliminate din formular.
- Generarea cerințelor pentru 12 ore peste 1 an va eșua.
- S-a îmbunătățit excepția de referință nulă a mesajului de eroare în timpul creării cerințelor de resurse.

**Gestionare de proiect**

S-au remediat următoarele probleme:

- Validare îmbunătățită pentru a aborda excepția de referință nulă generată în insertul **PreProjectUpdate**.
- Proiectele publicate de programul de completare desktop Microsoft Project șterg atribuțiile neatribuite.
- S-a adăugat o nouă validare atunci când referința proiectului unei sarcini este invalidă din cauza excepției de referință nulă din insertul **PreValidateProjectTaskUpdate**.
- Grila membrilor echipei nu afișează sarcini distincte în înregistrarea membrilor echipei.
- S-au adăugat noi mesaje de validare și eroare din cauza excepției de referință nulă în insertul **PreProjectTaskDelete**.

**Sales**

S-au remediat următoarele probleme:

- Atunci când selectați o linie bazată pe proiect în ofertă sau contract, butonul **Sugestie** ar trebui să fie vizibil numai atunci când selectați o linie bazată pe produs asociată unui produs existent.
- Scindează privilegiul **Create_Product** din privilegiul **Create_ProjectContract**.
- Ștergerea unei linii de facturare provoacă eșecul referinței nule pe **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]