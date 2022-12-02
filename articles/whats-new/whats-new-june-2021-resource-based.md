---
title: Noutăți iunie 2021 - Project Operations pentru scenarii bazate pe stocuri/producție
description: Acest articol oferă informații despre actualizările de calitate disponibile în versiunea Project Operations din iunie 2021 pentru scenarii bazate pe resurse/care nu există pe stoc.
author: sigitac
ms.date: 06/14/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: fd745107fa6d50882ebea302d3d2ae0de21b79ad
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028278"
---
# <a name="whats-new-june-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Noutăți iunie 2021 - Project Operations pentru scenarii bazate pe stocuri/producție

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

Acest articol se aplică următoarelor componente și versiuni Dynamics 365 Project Operations:

- Project Operations pe mediul Dynamics 365 Dataverse versiunea 4.11.0.156 sau 4.11.0.164.
- Management de proiect și contabilitate în medii de aplicații pentru finanțe și operațiuni versiunea 10.0.19.

## <a name="features-included-in-this-release"></a>Caracteristicile incluse în această versiune

Următoarele caracteristici sunt incluse în această versiune:

- Abilitatea de a șterge [Linii de propunere de factură de proiect pentru scenarii de ajustare](../invoicing/correct-project-invoice-proposals.md).
- Liniile de cheltuieli detaliate reflectă numele subcategoriilor în raportul de cheltuieli [Rapoarte de cheltuieli reinventate - caracteristici noi](../expense/expense-reports-reimagined.md#new-features).
- Metoda de plată este disponibilă în noul panou de cheltuieli atunci când creați o nouă cheltuială.
- Disponibilitatea generală a API-urilor de planificare proiect. Această nouă funcționalitate permite clienților să efectueze în mod programatic operațiuni de creare, actualizare și ștergere pe sarcini de proiect, alocări de resurse, dependențe de sarcini și înregistrări ale membrilor echipei de proiect. Pentru mai multe informații, consultați [Utilizați API-urile de planificare a proiectului pentru a efectua operațiuni cu entitățile de planificare](../project-management/schedule-api-preview.md).

## <a name="project-operations-dual-write-maps-updates"></a>Actualizări de hărți Project Operations cu scriere duală

Nu există actualizări pentru hărțile cu dublă scriere Project Operations în această versiune. 

Pentru o listă actuală și versiuni ale hărților cu scriere duală Project Operations, consultați [Versiuni de hartă cu scriere duală Project Operations](../environment/resource-dual-write-maps.md).

Rulați întotdeauna cea mai recentă versiune a hărții în mediul dvs. și activați toate hărțile de tabel aferente pe măsură ce vă actualizați soluția Project Operations Dataverse și versiunea de soluție pentru finanțe și operațiuni. Este posibil ca anumite caracteristici și capabilități să nu funcționeze corect dacă cea mai recentă versiune a hărții nu este activată. Puteți vedea versiunea activă a hărții pe pagina **Scriere duală** în coloana **Versiune**. Activați o nouă versiune a hărții selectând **Versiunile hărții tabel**, selectând cea mai recentă versiune și apoi salvând versiunea selectată. Dacă ați personalizat o hartă a tabelului predefinită, aplicați din nou modificările. Pentru mai multe informații, consultați: [Gestionarea ciclului de viață al aplicațiilor](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Dacă întâmpinați o problemă în lansarea hărții, urmați instrucțiunile din secțiunea [Problemă legată de coloanele lipsă în tabel pe hărți](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) din Ghidul de depanare pentru scriere duală.

## <a name="quality-updates"></a>Actualizări de calitate

### <a name="project-operations-on-dataverse"></a>Project Operations pe Dataverse

| **Zonă de caracteristici** | **Număr de referință** | **Actualizare de calitate** |
| --- | --- | --- |
| Facturarea și stabilirea prețurilor | 2281417 | S-a rezolvat problema referitoare la eșecul acțiunii de creare automată a facturilor prin programul de facturare. |
| Facturarea și stabilirea prețurilor | 2287835 | Performanță îmbunătățită de confirmare a facturii. |
| Managementul oportunităților | 2222555 | Încărcarea estimărilor materiale trebuie să fie corect copiată pentru a cita detaliile liniei atunci când se utilizează **Import din estimarea proiectului**. |
| Managementul oportunităților | 2223427 | Personalizările sunt acum permise pentru acțiune, **GenerateRetainersFromRetainerScheduleOptions**. |
| Managementul oportunităților | 2277528 | Calculul valorii de referință a facturării fixe pentru liniile contractului de proiect cu mai mulți clienți. |
| Planificare și urmărire de proiect | 2226110 | S-a rezolvat problema intermitentă cu funcția **Generați cerința** în grila **Echipă de proiect**. |
| Planificare și urmărire de proiect | 2208109 | Utilizatorii nu pot crea un proiect într-o monedă cu sarcini conexe într-o altă monedă. |
| Planificare și urmărire de proiect | 2258228 | Lista câmpurilor permise să se modifice cu entitățile **Planificare** care utilizează API-ul Planificare a fost actualizată. |
| Planificare și urmărire de proiect | 2293989 | Setările regionale și lingvistice corecte trebuie transmise către grila **Sarcini de proiect**. |
| Gestionarea de resurse | 2220493 | S-a remediat experiența utilizatorului în grila **Sarcină** atunci când marcați rapid o cerere de resursă ca fiind completă. |
| Gestionarea de resurse | 2330496 | S-a remediat problema de încărcare **Tablou de planificare**. (Actualizarea de calitate este disponibilă în versiunea 4.11.0.164) |
| Timp și cheltuială | 2194431 | Grila **Intrare de timp** trebuie să onoreze începutul săptămânii așa cum este stabilit în **Setările sistemului**. |
| Timp și cheltuială | 2277311 | După ce ștergeți valoarea dintr-o celulă din grila **Intrare de timp**, cursorul rămâne în grilă. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Management de proiect și contabilitate în Dynamics 365 Finance

| Zonă de caracteristici | Număr de referință | Actualizare de calitate |
| --- | --- | --- |
| Management de proiect și contabilitate | [552976](https://fix.lcs.dynamics.com/Issue/Details/?bugId=552976) | **Notele formularului** și **Configurarea formularului** nu sunt vizibile în **Configurarea managementului de proiect** în entitățile juridice de finanțare atunci când sunt integrate în Project Operations. |
| Management de proiect și contabilitate | [527970](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527970) | În descrierea implicită, TVA-ul nu este completat atunci când **Tip de postare** = **Taxă de vânzare** pentru voucherele de factură pentru proiect. |
| Management de proiect și contabilitate | [565089](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565089) | Tranzacțiile duble sunt postate când se utilizează facturarea bazată pe sarcini în Dataverse cu integrare Project Operations. |
| Management de proiect și contabilitate | [566869](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566869) | Procentul complet pentru recunoașterea veniturilor este incorect atunci când se utilizează integrarea Project Operations. |
| Management de proiect și contabilitate | [568107](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568107) | Acumularea de venituri este dublată pe o factură de furnizor în așteptare într-un scenariu integrat Project Operations. |
| Management de proiect și contabilitate | [572370](https://fix.lcs.dynamics.com/Issue/Details/?bugId=572370) | Jurnalul de integrare nu poate fi postat dacă regula profilului veniturilor este setată la Configurarea **Grupului**. |
| Management de proiect și contabilitate | [573596](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573596) | O factură de achiziție nu poate fi postată pentru comenzi de achiziție a proiectului care are linii cu mai multe unități de măsură. |
| Management de proiect și contabilitate | [573637](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573637) | Dimensiunea financiară implicită pentru un proiect nu poate fi actualizată folosind entitatea de date proiecte **V2**. |
| Management de proiect și contabilitate | [577211](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577211) | Procesul de creare a lotului estimat de proiect durează prea mult. |
| Management de proiect și contabilitate | [582329](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582329) | Când ștergeți un contract, se șterge și adresa asociată clientului. |
| Deplasări și cheltuieli | [514930](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514930) | Condiția fluxului de lucru pentru aprobarea raportului de cheltuieli nu este evaluată corect. |
| Deplasări și cheltuieli | [519304](https://fix.lcs.dynamics.com/Issue/Details/?bugId=519304) | Politica privind raportul de cheltuieli nu evaluează corect ID-ul proiectului. |
| Deplasări și cheltuieli | [522463](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522463) | Acțiunea **Împărțire la personal pentru tranzacțiile de cheltuieli între companii** nu funcționează corect. |
| Deplasări și cheltuieli | [534702](https://fix.lcs.dynamics.com/Issue/Details/?bugId=534702) | Justificările din linia raportului de cheltuieli sunt șterse accidental atunci când anumite cereri de călătorie sunt șterse. Acest lucru se întâmplă atunci când recID-ul raportului de cheltuieli și cererea de călătorie sunt aceleași. |
| Deplasări și cheltuieli | [544368](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544368) | Există o problemă în aplicația mobilă Cheltuieli atunci când câmpul **ID proiect** este obligatoriu în politicile raportului de cheltuieli. |
| Deplasări și cheltuieli | [545331](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545331) | Cheltuielile între companii care sunt asociate cu un proiect nu pot fi editate. În schimb, următorul mesaj de eroare afișează „Referința obiectului nu este setată la o instanță a unui obiect.” |
| Deplasări și cheltuieli | [548659](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548659) | După înregistrarea raportului de cheltuieli, moneda și suma greșite sunt afișate în registrul de bancă. |
| Deplasări și cheltuieli | [558336](https://fix.lcs.dynamics.com/Issue/Details/?bugId=558336) | Au fost aduse îmbunătățiri caracteristicii *Ștergeți tranzacțiile cu cardul de credit*.  |
| Deplasări și cheltuieli | [525070](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525070) | Impozitul pe vânzări inclus într-un raport de cheltuieli nu este calculat în mod consecvent atunci când este specificată o altă monedă de raportare pentru o persoană juridică. |
| Deplasări și cheltuieli | [527779](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527779) | Performanța este afectată atunci când se adaugă o nouă cheltuială de călătorie în numerar. |
| Deplasări și cheltuieli | [537841](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537841) | Regulile politicii de cheltuieli nu sunt declanșate într-un raport de cheltuieli. |
| Deplasări și cheltuieli | [566386](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566386) | Încărcarea unei noi categorii partajate folosind Data Management Framework elimină toate subcategoriile pentru toate categoriile partajate. |
| Deplasări și cheltuieli | [574131](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574131) | Când creați o linie de cheltuieli și apoi selectați o categorie, se afișează următorul mesaj de eroare: „Combinația grupului de taxe pe vânzări DOM și a grupului de taxe pe vânzări articol STD nu este validă.” |
| Deplasări și cheltuieli | [574900](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574900) | Există probleme de sincronizare în aplicația mobilă Cheltuieli. |
