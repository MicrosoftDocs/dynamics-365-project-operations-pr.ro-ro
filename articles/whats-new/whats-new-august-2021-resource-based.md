---
title: Noutăți august 2021 - Project Operations pentru scenarii bazate pe resurse/fără stocuri
description: Acest subiect oferă informații despre actualizările de calitate disponibile în versiunea Project Operations din august 2021 pentru scenarii bazate pe resurse/fără stocuri.
author: sigitac
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 26861472d3af20c58b3d01142b834d535cf99715
ms.sourcegitcommit: 083e3d219cd5126eecb74debb1b70b361680b1f6
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 09/18/2021
ms.locfileid: "7501386"
---
# <a name="whats-new-august-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Noutăți august 2021 - Project Operations pentru scenarii bazate pe resurse/fără stocuri

*Se aplică la: Project Operations pentru scenarii bazate pe resurse/fără stoc*

Acest subiect se aplică următoarelor componente și versiuni Dynamics 365 Project Operations:

   - Project Operations în mediul Microsoft Dataverse versiunea 4.13.0.152.
   - Management de proiect și contabilitate în mediul Dynamics 365 Finance versiunea 10.0.20.

## <a name="features-included-in-this-release"></a>Caracteristicile incluse în această versiune

Următoarele caracteristici sunt incluse în această versiune:

- **Seturi de aprobare**: Seturile de aprobare grupează cererile de timp, cheltuieli sau solicitări de aprobare a utilizării materialelor în subseturi mai mici de operațiuni. Această grupare permite procesarea aprobărilor într-o ordine specifică după proiect și permite reîncercarea și secvențierea. Gruparea cererilor îmbunătățește fiabilitatea și trasabilitatea procesării aprobării pentru volume mari de aprobări. Pentru informații suplimentare, consultați [Seturi de aprobări](../approvals/approval-sets.md).

## <a name="project-operations-dual-write-maps-updates"></a>Actualizări de hărți Project Operations cu scriere duală

Nu există actualizări pentru hărțile cu dublă scriere Project Operations în această versiune.

Pentru o listă actuală și versiuni ale hărților cu scriere duală Project Operations, consultați [Versiuni de hartă cu scriere duală Project Operations](../environment/resource-dual-write-maps.md).

Rulați întotdeauna cea mai recentă versiune a hărții în mediul dvs. și activați toate hărțile de tabel aferente pe măsură ce vă actualizați soluția Dataverse în Project Operations și versiunea de soluție financiară. Este posibil ca anumite caracteristici și capabilități să nu funcționeze corect dacă cea mai recentă versiune a hărții nu este activată. Puteți vedea versiunea activă a hărții pe pagina **Scriere duală** în coloana **Versiune**. Activați o nouă versiune a hărții selectând **Versiunile hărții tabel**, selectând cea mai recentă versiune și apoi salvând versiunea selectată. Dacă ați personalizat o hartă a tabelului predefinită, aplicați din nou modificările. Pentru mai multe informații, consultați: [Gestionarea ciclului de viață al aplicațiilor](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Dacă întâmpinați o problemă în lansarea hărții, urmați instrucțiunile din secțiunea [Problemă legată de coloanele lipsă în tabel pe hărți](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) din Ghidul de depanare pentru scriere duală.

## <a name="quality-updates"></a>Actualizări de calitate

### <a name="project-operations-on-dataverse"></a>Project Operations pe Dataverse

| **Zonă de caracteristici** | **Număr de referință** | **Actualizare de calitate** |
| --- | --- | --- |
| Facturarea și stabilirea prețurilor | 2295625 | Numele jalonului trebuie copiat din planificarea facturării în detaliul liniei de facturare. |
| Facturarea și stabilirea prețurilor | 2316323 | Reducerea nu ar trebui să poată fi modificată pe o factură proforma în Project Operations pentru scenarii bazate pe resurse. |
| Managementul oportunităților | 2338619 | Regulile de business **Oportunitate** și **Ofertă** trebuie invocate numai pe pagini. |
| Gestionarea resurselor | 2316523 | Folosirea de **Trimitere cerere** dintr-o cerință de resursă care are un rol atașat nu ar trebui să afișeze o eroare. |
| Gestionarea resurselor | 2326885 | Crearea unei cerințe de resurse printr-un proiect nu ar trebui să afișeze o eroare. |
| Timp și cheltuieli | 2335584 | Fluxuri de activități depreciate în înregistrarea de timp. |
| Timp și cheltuieli | 2336884 | Butonul de înregistrare de timp **Copiere săptămână** nu trebuie să funcționeze doar pentru utilizatorul curent. |


### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Management de proiect și contabilitate pe Dynamics 365 Finance

| Zonă de caracteristici | Număr de referință | Actualizare de calitate |
| --- | --- | --- |
| Deplasări și cheltuieli | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Se înregistrează valori incorecte de tranzacții ale vânzătorului și de taxe de vânzare când se creează o cheltuială dintr-o tranzacție cu un card de credit. |
| Deplasări și cheltuieli | [4620366](https://fix.lcs.dynamics.com/Issue/Details?kb=4620366&amp;bugId=579485&amp;dbType=3&amp;qc=e864789bd95505ea624c537d585bf113c2de60b97c88439d44693dbd85aa8e92) | Decontarea greșită sunt liniile create la generarea jurnalului de plăți. |
| Deplasări și cheltuieli | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Se postează valori incorecte de taxe de vânzare când se creează o cheltuială dintr-o tranzacție cu un card de credit. |
| Deplasări și cheltuieli | [4621765](https://fix.lcs.dynamics.com/Issue/Details?kb=4621765&amp;bugId=587306&amp;dbType=3&amp;qc=6fbfad0123d4e95eaf8d5a5a2f6c354577c991b7905c852ab02d1f94e728a876) | Ștergerea unei linii de cheltuieli ar putea dura mult. |
| Contabilitatea proiectelor | [4623737](https://fix.lcs.dynamics.com/Issue/Details?kb=4623737&amp;bugId=598109&amp;dbType=3&amp;qc=4101fc5865201e21815299f2ff11ae46d5d5370510868df86c25ee09a8ca1a0c) | Sistemul nu acceptă configurarea secvențierii numerice continue atunci când postați o estimare după aplicarea KB 4619395. |
| Contabilitatea proiectelor | [4623332](https://fix.lcs.dynamics.com/Issue/Details?kb=4623332&amp;bugId=586034&amp;dbType=3&amp;qc=2f64bb1977c4a9c9dd2ce9de7e72230b86eca14b6295c5bbfb614ea97ad81caf) | Este posibil ca postarea facturilor furnizorului să eșueze cu mesajul de eroare „Tranzacțiile pe cupon nu se echilibrează conform 17/05/2021. (monedă contabilă: 0,00 - monedă de raportare: 0,01) " |
