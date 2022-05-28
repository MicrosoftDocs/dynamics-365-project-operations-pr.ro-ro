---
title: Ce este nou în martie 2022 - Project Operations pentru scenarii bazate pe resurse/ne-stocate
description: Acest subiect oferă informații despre actualizările de calitate care sunt disponibile în ediția din martie 2022 a Project Operations pentru scenarii bazate pe resurse/nestoc.
author: sigitac
ms.date: 03/31/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: afd5149cda909b5367e7f12382423179d7e19267
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8600757"
---
# <a name="whats-new-march-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Ce este nou în martie 2022 - Project Operations pentru scenarii bazate pe resurse/ne-stocate

*Se aplică la: Project Operations pentru scenarii bazate pe resurse/fără stoc*

Acest subiect se aplică următoarelor componente și versiuni ale Microsoft Dynamics 365 Project Operations:

- Operațiuni de proiect în a Dataverse versiunea de mediu 4.30.0.99
- Management de proiect și contabilitate într-un mediu Dynamics 365 Finance versiunea 10.0.25

## <a name="features-included-in-this-release"></a>Caracteristicile incluse în această versiune

Diurnele sunt acum acceptate în noul și reimaginat spațiu de lucru modern pentru cheltuieli. Companiile care utilizează diurne pot activa această funcție pentru a oferi utilizatorilor o modalitate ușoară de a trimite și de a fi rambursați pentru cheltuielile cu diurnă. Pentru mai multe informații, vezi [Cheltuieli diurne](../expense/per-diem-expenses.md).

## <a name="project-operations-dual-write-maps-updates"></a>Actualizări de hărți Project Operations cu scriere duală

Următoarea listă arată hărțile cu dublă scriere care au fost modificate sau adăugate în versiunea Project Operations martie 2022.

| **Maparea entității** | **Versiune actualizată** | **Comentarii** |
| --- | --- | --- |
| Proiect Operations integrare proiect furnizor linie factură export entitate msdyn\_ proiectevendorinvoicelines | 1.0.0.3 | Mapările au fost actualizate pentru a se alinia cu entitatea linie de factură a furnizorului din Dataverse. <br>Nu activați versiunea de cartografiere 1.0.0.4. Va fi gata de utilizare în combinație cu mediul Finance versiunea 10.0.26 în următoarea actualizare lunară. |

Rulați întotdeauna cea mai recentă versiune a hărții în mediul dvs. și activați toate hărțile de tabel asociate pe măsură ce actualizați operațiunile de proiect Dataverse soluție și versiunea soluției financiare. Este posibil ca unele funcții și capabilități să nu funcționeze corect dacă cea mai recentă versiune a hărții nu este activată. Puteți vizualiza versiunea activă a hărții în coloana **Versiune** de pe pagina **Scriere duală**. Pentru a activa o nouă versiune a hărții selectați **Versiuni ale hărții cu tabele**, selectați cea mai recentă versiune și apoi salvați versiunea selectată. Dacă ați personalizat o hartă a tabelului out-of-box, aplicați din nou modificările. Pentru mai multe informații, consultați: [Gestionarea ciclului de viață al aplicațiilor](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Dacă întâmpinați o problemă când porniți harta, urmați instrucțiunile din [Problemă cu coloanele din tabel lipsă pe hărți](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) secțiunea din ghidul de depanare cu scriere duală.

## <a name="quality-updates"></a>Actualizări de calitate

### <a name="project-operations-on-dataverse"></a>Project Operations pe Dataverse

| Zonă de caracteristici | Număr de referință | Actualizare de calitate |
| --- | --- | --- |
| Timp și cheltuieli | 2388011 | Afișați comentariile de respingere celor care trimit datele de timp în timpul aprobării în bloc. |
| Planificarea și urmărirea proiectului | 2495294 | Detaliile proiectului nu trebuie să fie editabile pe **Detalii despre sarcină** pagină. |
| Facturarea și stabilirea prețurilor | 2499605 | Etapele contractului care sunt create din reperele de cotație sunt marcate incorect ca doar pentru citire. |
| Planificarea și urmărirea proiectului | 2506050 | Setul de operații rămâne în așteptare timp de o oră dacă nu există nicio modificare de salvat. Setul este apoi marcat fals ca **A eșuat**, în timp ce ar trebui finalizat imediat. |
| Facturarea și stabilirea prețurilor | 2507401 | Unitățile de contractare implicite sunt introduse incorect în proiecte din cauza memorării în cache incorecte. |
| Facturarea și stabilirea prețurilor | 2541660 | **Validarea creării comenzii de vânzare** în dublă scriere ar trebui să fie doar pentru comenzi bazate pe proiecte. |
| Facturarea și stabilirea prețurilor | 2552745 | Taxele nu sunt împărțite între clienții care au stabilit reguli de facturare divizate. |
| Facturarea și stabilirea prețurilor | 2558859 | Mesaje de eroare îmbunătățite la configurarea dimensiunilor de preț. |
| Facturarea și stabilirea prețurilor | 2558933 | **Import din estimări de proiect** eșuează când **msdyn\_ proiect** este adăugată ca dimensiune a prețului. |
| Facturarea și stabilirea prețurilor | 2559101 | Ștergerea parametrilor de proiect nu este blocată și provoacă probleme. |
| Managementul oportunităților | 2570390 | Pluginul cu dublă scriere forțează tipul de cont pe cotații, comenzi și oportunități să fie **Client**, chiar și atunci când acel tip de cont nu este corect. |
| Facturarea și stabilirea prețurilor | 2586097 | Costurile efective facturate divizate nu sunt inversate atunci când un proiect este eliminat dintr-o linie de contract de proiect. |
| Facturarea și stabilirea prețurilor | 2589619 | Taxa pe materialul înscris este propagată în efectivele de vânzări nefacturate și pe factură. |
| Managementul oportunităților | 2594015 | O cotație nu poate fi închisă ca câștigată pentru clienții care au **Net60** termeni de plată. |
| Planificarea și urmărirea proiectului | 2595841 | În Project for the Web, utilizatorii primesc un mesaj de eroare despre o lipsă **msdyn\_ actualstart** când creează o nouă cerere de resursă. |
| Timp și cheltuială | 2602511 | The **Respins de** se afișează câmpul pentru intrările de timp **Sistem** în loc de un utilizator numit ca respingător. |
| Timp și cheltuială | 2602528 | Un aprobator de proiect poate aproba timpul pentru proiectele în care nu sunt listate ca aprobare. |
| Facturarea și stabilirea prețurilor | 2608550 | O factură de corectare poate fi confirmată chiar dacă nu există modificări la original. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Management de proiect și contabilitate pe Dynamics 365 Finance

| Zonă de caracteristici | Număr de referință | Actualizare de calitate |
| --- | --- | --- |
| Management de proiect și contabilitate | [606759](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606759) | Există o nepotrivire între finanțare și operațiunile de proiect în durata permisă a **ID categorie** camp. |
| Management de proiect și contabilitate | [617806](https://fix.lcs.dynamics.com/Issue/Details/?bugId=617806) | Proiectele cu preț fix nu pot fi eliminate atunci când **Facturare pe cont** câmpul este setat la **Profit și pierdere** si **Procent finalizat** este utilizat principiul. |
| Management de proiect și contabilitate | [620979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620979) | Un grup implicit de taxe pe vânzări incorect este introdus din configurarea proiectului pe liniile de cheltuieli din jurnalul de integrare Operațiuni de proiect. |
| Management de proiect și contabilitate | [623014](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623014) | Nu puteți edita dimensiunile antetului propunerii de factură de proiect într-o implementare integrată cu Operațiuni de proiect. |
| Management de proiect și contabilitate | [624283](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624283) | Facturile furnizorilor intercompanii nu trebuie să fie integrate cu Dataverse. |
| Management de proiect și contabilitate | [634156](https://fix.lcs.dynamics.com/Issue/Details/?bugId=634156) | Există o nepotrivire între moneda soldurilor clienților și moneda de raportare. |
| Management de proiect și contabilitate | [641612](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641612) | Puteți posta o factură de proiect chiar dacă clientul este în așteptare pentru toate facturile. |
| Management de proiect și contabilitate | [642945](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642945) | The **Ștergeți toate liniile** Butonul lipsește din propunerile de factură de proiect care au **Antet** și **Linii** vederi. |
| Management de proiect și contabilitate | [637760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=637760) | Când înregistrați o factură de furnizor, apare următoarea eroare: „Data contabilă a facturii trebuie să fie în același an contabil cu comanda achiziționată aferentă. Rulați procesul de încheiere a anului comenzii de achiziție sau modificați data în anul contabil curent." |
| Deplasări și cheltuieli | [604128](https://fix.lcs.dynamics.com/Issue/Details/?bugId=604128) | Costul angajat pentru un proiect nu este eliberat după ce costul angajat al cererii de călătorie este eliberat. |
| Deplasări și cheltuieli | [620803](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620803) | Următoarea eroare apare atunci când trimiteți un raport de cheltuieli: „Stack Trace: Compania nu există”. |
| Deplasări și cheltuieli | [622465](https://fix.lcs.dynamics.com/Issue/Details/?bugId=622465) | Implicit **ID proiect** nu este înscris în rapoartele de cheltuieli atunci când **Necesită activitate pentru jurnal** parametrul este selectat în proiect. |
| Deplasări și cheltuieli | [626781](https://fix.lcs.dynamics.com/Issue/Details/?bugId=626781) | The **Cheltuieli postate** butonul nu funcționează corect în Operațiuni de proiect pentru scenarii de resurse/ne-aprovizionate. |
| Deplasări și cheltuieli | [635348](https://fix.lcs.dynamics.com/Issue/Details/?bugId=635348) | Există o problemă cu **Tarif pe milă** pentru un raport de cheltuieli cu kilometrajul care include pasagerii. |
| Deplasări și cheltuieli | [638019](https://fix.lcs.dynamics.com/Issue/Details/?bugId=638019) | Ratele de kilometraj de cheltuieli pentru angajați nu sunt totalizate corect atunci când două tipuri diferite de vehicule sunt utilizate în **Nivelurile ratei de kilometraj** categorie de cheltuieli. |
| Deplasări și cheltuieli | [641272](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641272) | Căutarea pentru **Proiect** câmpul de pe o linie de solicitare de călătorie nu returnează lista corectă de proiecte. |
| Deplasări și cheltuieli | [645905](https://fix.lcs.dynamics.com/Issue/Details/?bugId=645905) | **Kilometraj în revizuire** afișează un avertisment pe rapoartele de cheltuieli. |
| Deplasări și cheltuieli | [647819](https://fix.lcs.dynamics.com/Issue/Details/?bugId=647819) | Serviciul de recunoaștere optică a caracterelor pentru chitanță (OCR) nu funcționează din cauza unei probleme cu adresa URL a serviciului OCR de cheltuieli. |
| Deplasări și cheltuieli | [648684](https://fix.lcs.dynamics.com/Issue/Details/?bugId=648684) | Cand **Abilitatea de a detalia rapid cheltuielile recurente** caracteristica este activată, sumele de pe liniile de detaliere din rapoartele de cheltuieli modifică sumele de fiecare dată când **Detaliază** pagina este deschisă. |
| Deplasări și cheltuieli | [651899](https://fix.lcs.dynamics.com/Issue/Details/?bugId=651899) | Nu puteți șterge un raport de cheltuieli atunci când lista intermediară are mai mulți aprobatori. |

## <a name="removed-and-deprecated-features"></a>Funcții eliminate și depreciate

The [Caracteristici eliminate sau depreciate în Operațiuni de proiect](removed-depreciated-features-project.md) subiectul descrie caracteristici pentru care au fost eliminate sau depreciate Dynamics 365 Project Operations.

- O caracteristică eliminat nu mai este disponibilă în produs.
- O funcție învechită nu este în dezvoltare activă și ar putea fi eliminată într-o actualizare viitoare.

Un anunț de depreciere va apărea în [Caracteristici eliminate sau depreciate în Operațiuni de proiect](removed-depreciated-features-project.md) subiect cu 12 luni înainte ca orice caracteristică să fie eliminată din produs.

Pentru modificările nerespective care afectează doar timpul de compilare, dar sunt compatibile binar cu mediile sandbox și de producție, timpul de depreciere va fi mai mic de 12 luni. De obicei, aceste modificări sunt actualizări funcționale care trebuie făcute compilatorului.
