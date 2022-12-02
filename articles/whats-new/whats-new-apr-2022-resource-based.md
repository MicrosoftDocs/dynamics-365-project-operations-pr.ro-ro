---
title: Ce este nou în aprilie 2022 - Project Operations pentru scenarii de resurse/care nu sunt bazate pe stoc
description: Acest articol oferă informații despre actualizările de calitate care sunt disponibile în versiunea de Microsoft Dynamics 365 Project Operations din aprilie 2022 pentru scenarii bazate pe resurse/care nu există pe stoc.
author: sigitac
ms.date: 04/08/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 999006b2c2fe2b31d6e47910a3f1a55cab415f0e
ms.sourcegitcommit: 5c971b15295046b3c92ff6638dd1352129f1c390
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 07/01/2022
ms.locfileid: "9110899"
---
# <a name="whats-new-april-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Ce este nou în aprilie 2022 - Project Operations pentru scenarii de resurse/care nu sunt bazate pe stoc

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

Acest articol se aplică următoarelor componente și versiuni de Microsoft Dynamics 365 Project Operations:

- Project Operations într-un mediu Dataverse versiunea 4.41.0.45
- Management de proiect și contabilitate într-un mediu Dynamics 365 Finance, versiunea 10.0.26

## <a name="features-included-in-this-release"></a>Caracteristicile incluse în această versiune

Categoriile de achiziții pot fi utilizate în comenzile de achiziție ale proiectelor și în facturile furnizorilor în așteptare. Pentru mai multe informații, consultați [Utilizarea categoriilor de achiziții cu comenzile de achiziție de proiect și facturile furnizorilor în așteptare](../procurement/configure-procurement-categories.md).

## <a name="project-operations-dual-write-maps-updates"></a>Actualizări de hărți Project Operations cu scriere duală

Următorul tabel prezintă hărțile cu scriere duală care au fost modificate sau adăugate în Project Operations, versiunea martie 2022.

| Maparea entității | Versiune actualizată | Comentarii |
| -------------- | ------------------- | ------------|
| Entitatea msdyn\_projectvendorinvoicelines privind exportul liniei de facturare de furnizor în proiectul de integrare Project Operations | 1.0.0.4 | Această hartă acceptă utilizarea categoriilor de achiziții cu comenzile de achiziție și facturile furnizorilor în așteptare. |

Rulați întotdeauna cea mai recentă versiune a hărții în mediul dvs. și activați toate hărțile de tabel aferente pe măsură ce vă actualizați soluția Project Operations Dataverse și versiunea de soluție Finance. Este posibil ca unele caracteristici și capabilități să nu funcționeze corect dacă cea mai recentă versiune a hărții nu este activată. Puteți vizualiza versiunea activă a hărții în coloana **Versiune** de pe pagina **Scriere duală**. Pentru a activa o nouă versiune a hărții selectați **Versiuni ale hărții cu tabele**, selectați cea mai recentă versiune și apoi salvați versiunea selectată. Dacă ați personalizat o hartă predefinită a tabelului, aplicați din nou modificările. Pentru mai multe informații, consultați: [Gestionarea ciclului de viață al aplicațiilor](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Dacă întâmpinați o problemă când porniți harta, urmați instrucțiunile din secțiunea [Problema coloanelor din tabel lipsă pe hărți](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) a ghidului de depanare Dual-write.

## <a name="quality-updates"></a>Actualizări de calitate

### <a name="project-operations-on-dataverse"></a>Project Operations pe Dataverse

| Zonă de caracteristici | Număr de referință | Actualizare de calitate |
| ------------ | ---------------- | -------------- |
| Timp și cheltuieli | 2573900 | Caracteristica **Aprobare modernă** trebuie să fie activată în mod implicit. |
| Facturarea și stabilirea prețurilor | 2603313 | S-a remediat o eroare de înregistrare duplicat care a împiedicat adăugarea liniilor de ofertă și de contract care au un produs. |
| Implementare și configurare | 2611368 | Clienții trebuie să poată adăuga până la cinci entități personalizate la soluție folosind proiectantul de aplicații modern. |
| Timp și cheltuieli | 2628285 | S-a remediat o problemă care afecta capacitatea de a seta categoria corectă de resurse în timpul importului de intrare de timp. |
| Managementul oportunităților| 2628815 | Actualizați limita de caractere din descrierea detaliată a liniei de ofertă pentru a se potrivi cu limita de caractere a subiectului sarcinii, astfel încât importul să aibă succes pentru sarcinile în care subiectul este mai lung de 100 de caractere. |
| Timp și cheltuieli| 2629547 | Câmpul **Trimis de** al aprobărilor de proiect trebuie să indice utilizatorul care a transmis înregistrarea. |
| Timp și cheltuieli| 2629865 | Câmpul **Categorie de copiere** privind sarcinile atunci când proiectele sunt copiate. |
| Timp și cheltuieli| 2636463 | S-au remediat filtrele privind aprobările în formularele moderne de aprobări. |
| Planificarea și urmărirea proiectului | 2648300 | S-a rezolvat o problemă care împiedică schimbarea proprietarului proiectului. |
| Facturarea și stabilirea prețurilor | 2563000 | Nu trebuie permise linii de jurnal pentru o vânzare nefacturată în care moneda diferă de moneda contractului. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Management de proiect și contabilitate în Dynamics 365 Finance

Pentru informații despre remedierile erorilor care sunt incluse în această actualizare, conectați-vă la Microsoft Dynamics Lifecycle Services (LCS) și vizualizați [Articolul KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864).
