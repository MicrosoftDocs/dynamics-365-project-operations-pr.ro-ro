---
title: Ce este nou sau schimbat în Project Service Automation versiunea actualizată 20, V3
description: Acest articol listează caracteristicile și corecțiile care sunt disponibile în Project Service Automation V3, versiunea de actualizare 20, V3
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/12/2020
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 7265f4999ee9c584450efcf444621c00acd65920
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913083"
---
# <a name="project-service-automation-update-release-20-v3"></a>Project Service Automation, versiunea actualizată 20, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Suntem încântați să anunțăm cea mai recentă actualizare pentru aplicația Project Service Automation pentru Dynamics 365. Această versiune include câteva îmbunătățiri importante ale calității, performanței și utilizabilității. Această versiune este compatibilă cu Dynamics 365 9.x. Pentru a actualiza această versiune, accesați Centrul de administrare pentru Dynamics 365, pagina de soluții online pentru a instala actualizarea. Pentru informații suplimentare, consultați: [Instalarea, actualizarea sau eliminarea unei soluții preferate](/power-platform/admin/install-remove-preferred-solution).

Acest articol listează caracteristicile și corecțiile care sunt noi sau modificate pentru Project Service Automation V3, versiunea de actualizare 20. Această versiune are un număr de versiune V 3.10.31.37 și este disponibil în general printr-o autoactualizare în iunie 2020.

## <a name="update-release-20"></a>Lansarea de actualizări 20

### <a name="bug-fixes"></a>Remedieri de erori

**Gestionare de proiect**

S-au remediat următoarele probleme:

- Importarea membrilor echipei de proiect cu o metodă de alocare care necesită ore are ca rezultat un mesaj de eroare neclar atunci când orele specificate sunt zero.
- Utilizatorii primesc o eroare incorectă atunci când numărul maxim de caractere a fost introdus în câmpul **Descriere** pentru o sarcină de proiect.
- Pagina **Microsoft Dynamics 365 Project Service Automation de descărcare a programului de completare** redirecționează către pagina de descărcare în limba engleză atunci când setările de limbă ale utilizatorului sunt setate la japoneză.
- Când apare o eroare de server, eticheta de sincronizare de pe fila **Planificare** din formularul **Proiecte** rămâne uneori.
- Actualizările de sarcini redundante sunt trimise serverului atunci când o sarcină este modificată.

**Sales**

S-au remediat următoarele probleme:

- Pe formularul **Contract**, dublul clic pe **Creați factură** creează două facturi pentru o singură înregistrare de date reale.
- În Internet Explorer 11, utilizatorii nu pot crea intrări de cheltuieli.
- Inversarea costurilor și inversarea Cifrelor reale din vânzările nefacturate nu sunt legate.
- Butonul **Reîmprospătați valorile reale** de pe formularul **Proiect** nu reîmprospătează **Activitate ore efective**.
- Insertul **PreValidateProjectTeamMemberCreate** poate crea resurse generice duplicate care se pot rezerva când atributul **msdyn_isgenericresourceprojectscoped** este setat la **Fals**.
- **Recalcularea** șterge costurile exigibile pentru detaliile liniei de ofertă bazate pe produse și detaliile liniei contractului.
- În scenarii specifice, insertul **PostEstimateLineUpdate** afișează o eroare de excepție nulă.
- Durata fazei de timp pe **Graficul analizei rentabilității** nu se potrivește cu durata costurilor din detaliul liniei de ofertă la preț fix.
- Valorile grupului unitar și ale unităților nu implicit corect pentru categoriile de cheltuieli din **Detalii linie contract** și formulare **Detalii despre linie de ofertă**.
- Listele **Preț cost unitate organizațională** permit suprapunerea efectivității datei.
- Utilizatorii nu au voie să schimbe **OrgUnit** când tipul de comandă nu este bazat pe lucru, deoarece va duce la o eroare nulă de excepție de referință.
- Când încercați să navigați din formularul **Detalii despre linie de ofertă**, înapoi la fila **Oferta**, formularul reîmprospătează și afișează fila **Rezumat**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
