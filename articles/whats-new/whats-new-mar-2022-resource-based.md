---
title: Ce este nou în martie 2022 - Project Operations pentru scenarii bazate pe resurse/ne-stocate
description: Acest articol oferă informații despre actualizările de calitate care sunt disponibile în lansarea din martie 2022 a Project Operations pentru scenarii bazate pe resurse/care nu există pe stoc.
author: sigitac
ms.date: 03/31/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 986d0652ed502873085259fef5ad40aba99c278d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910921"
---
# <a name="whats-new-march-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Ce este nou în martie 2022 - Project Operations pentru scenarii bazate pe resurse/ne-stocate

*Se aplică la: Project Operations pentru scenarii bazate pe resurse/fără stoc*

Acest articol se aplică următoarelor componente și versiuni de Microsoft Dynamics 365 Project Operations:

- Project Operations într-un mediu Dataverse versiunea 4.30.0.99
- Management de proiect și contabilitate într-un mediu Dynamics 365 Finance, versiunea 10.0.25

## <a name="features-included-in-this-release"></a>Caracteristicile incluse în această versiune

Diurnele sunt acum acceptate în spațiul de lucru modern pentru cheltuieli nou și reimaginat. Companiile care utilizează diurne pot activa această funcție pentru a oferi utilizatorilor o modalitate ușoară de a trimite și de a fi rambursați pentru cheltuielile diurne. Pentru informații suplimentare, consultați [Cheltuieli de diurnă](../expense/per-diem-expenses.md).

## <a name="project-operations-dual-write-maps-updates"></a>Actualizări de hărți Project Operations cu scriere duală

Următoarea listă prezintă hărțile cu scriere duală care au fost modificate sau adăugate în Project Operations, versiunea martie 2022.

| **Maparea entității** | **Versiune actualizată** | **Comentarii** |
| --- | --- | --- |
| Entitatea msdyn\_projectvendorinvoicelines privind exportul liniei de facturare de furnizor în proiectul de integrare Project Operations | 1.0.0.3 | Mapările au fost actualizate pentru a se alinia cu entitatea linie de facturare de furnizor în Dataverse. <br>Nu activați versiunea de mapare 1.0.0.4. Va fi gata de utilizare în combinație cu mediul Finance, versiunea 10.0.26, în următoarea actualizare lunară. |

Rulați întotdeauna cea mai recentă versiune a hărții în mediul dvs. și activați toate hărțile de tabel aferente pe măsură ce vă actualizați soluția Project Operations Dataverse și versiunea de soluție Finance. Este posibil ca unele caracteristici și capabilități să nu funcționeze corect dacă cea mai recentă versiune a hărții nu este activată. Puteți vizualiza versiunea activă a hărții în coloana **Versiune** de pe pagina **Scriere duală**. Pentru a activa o nouă versiune a hărții selectați **Versiuni ale hărții cu tabele**, selectați cea mai recentă versiune și apoi salvați versiunea selectată. Dacă ați personalizat o hartă predefinită a tabelului, aplicați din nou modificările. Pentru mai multe informații, consultați: [Gestionarea ciclului de viață al aplicațiilor](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Dacă întâmpinați o problemă când porniți harta, urmați instrucțiunile din secțiunea [Problema coloanelor din tabel lipsă pe hărți](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) a ghidului de depanare Dual-write.

## <a name="quality-updates"></a>Actualizări de calitate

### <a name="project-operations-on-dataverse"></a>Project Operations pe Dataverse

| Zonă de caracteristici | Număr de referință | Actualizare de calitate |
| --- | --- | --- |
| Timp și cheltuieli | 2388011 | Afișați comentariile de respingere celor care trimit înregistrările de timp în timpul aprobării în bloc. |
| Planificarea și urmărirea proiectului | 2495294 | Detaliile proiectului nu trebuie să fie editabile pe pagina **Detalii sarcină**. |
| Facturarea și stabilirea prețurilor | 2499605 | Etapele contractuale care sunt create din reperele de cotație sunt marcate incorect ca doar pentru citire. |
| Planificarea și urmărirea proiectului | 2506050 | Setul de operațiuni rămâne în așteptare timp de o oră dacă nu există nicio modificare de salvat. Setul este apoi marcat fals ca **Eșuat**, în timp ce ar trebui finalizat imediat. |
| Facturarea și stabilirea prețurilor | 2507401 | Unitățile de contractare implicite sunt introduse incorect în proiecte din cauza memorării incorecte în cache. |
| Facturarea și stabilirea prețurilor | 2541660 | **Validarea creării comenzii de vânzare** în scriere duală ar trebui să fie doar pentru comenzi bazate pe proiecte. |
| Facturarea și stabilirea prețurilor | 2552745 | Impozitul nu este împărțit între clienții care au stabilit reguli de facturare divizate. |
| Facturarea și stabilirea prețurilor | 2558859 | Mesaje de eroare îmbunătățite atunci când sunt configurați parametrii de preț. |
| Facturarea și stabilirea prețurilor | 2558933 | **Import din estimări de proiect** eșuează când **msdyn\_proiect** este adăugată ca dimensiune a prețului. |
| Facturarea și stabilirea prețurilor | 2559101 | Ștergerea parametrilor de proiect nu este blocată și provoacă probleme. |
| Managementul oportunităților | 2570390 | Pluginul cu scriere duală obligă ca tipul de cont pe oferte, comenzi și oportunități să fie **Client**, chiar și atunci când acel tip de cont nu este corect. |
| Facturarea și stabilirea prețurilor | 2586097 | Costurile reale facturate împărțite nu sunt inversate atunci când un proiect este eliminat dintr-o linie de contract de proiect. |
| Facturarea și stabilirea prețurilor | 2589619 | Impozitul pe materialul din afara catalogului este propagat la valorile reale de vânzări nefacturate și la factură. |
| Managementul oportunităților | 2594015 | O ofertă nu poate fi închisă ca fiind câștigată pentru clienții care au termeni de plată **Net60**. |
| Planificarea și urmărirea proiectului | 2595841 | În Project for the Web, utilizatorii primesc un mesaj de eroare despre o lipsă **msdyn\_actualstart** când creează o nouă cerere de resursă. |
| Timp și cheltuială | 2602511 | Câmpul **Respins de** pentru intrările de timp afișează **Sistem** în loc de un utilizator numit ca respingător. |
| Timp și cheltuială | 2602528 | Un aprobator de proiect poate aproba timpul pentru proiectele în care nu sunt listate ca aprobator. |
| Facturarea și stabilirea prețurilor | 2608550 | O factură de corectare poate fi confirmată chiar dacă nu există modificări ale originalului |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Management de proiect și contabilitate în Dynamics 365 Finance

| Zonă de caracteristici | Număr de referință | Actualizare de calitate |
| --- | --- | --- |
| Management de proiect și contabilitate | [606759](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606759) | Există o nepotrivire între Finance și Project Operations în durata permisă a câmpului **ID categorie**. |
| Management de proiect și contabilitate | [617806](https://fix.lcs.dynamics.com/Issue/Details/?bugId=617806) | Proiectele cu preț fix nu pot fi eliminate atunci când câmpul **Facturare pe cont** este setat la **Profit și pierdere** și este utilizat principiul **Procent finalizat**. |
| Management de proiect și contabilitate | [620979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620979) | Un grup implicit de taxe pe vânzări incorect este introdus din configurarea proiectului pe liniile de cheltuieli din jurnalul de integrare Project Operations. |
| Management de proiect și contabilitate | [623014](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623014) | Nu puteți edita dimensiunile antetului propunerii de factură de proiect într-o implementare integrată cu Project Operations. |
| Management de proiect și contabilitate | [624283](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624283) | Facturile furnizorilor intercompanii nu trebuie să fie integrate cu Dataverse. |
| Management de proiect și contabilitate | [634156](https://fix.lcs.dynamics.com/Issue/Details/?bugId=634156) | Există o nepotrivire între moneda soldurilor clienților și moneda de raportare. |
| Management de proiect și contabilitate | [641612](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641612) | Puteți publica o factură de proiect chiar dacă clientul este în așteptare pentru toate facturile. |
| Management de proiect și contabilitate | [642945](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642945) | Butonul **Ștergeți toate liniile** lipsește din propunerile de factură de proiect care au vizualizări pentru **Antet** și **Linii**. |
| Management de proiect și contabilitate | [637760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=637760) | Când înregistrați o factură de furnizor, apare următoarea eroare: „Data contabilă a facturii trebuie să fie în același an contabil cu comanda achiziționată aferentă. Rulați procesul de încheiere a anului comenzii de achiziție sau modificați data în anul contabil curent." |
| Deplasări și cheltuieli | [604128](https://fix.lcs.dynamics.com/Issue/Details/?bugId=604128) | Costul angajat pentru un proiect nu este eliberat după ce costul angajat al cererii de călătorie este eliberat. |
| Deplasări și cheltuieli | [620803](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620803) | Următoarea eroare apare atunci când trimiteți un raport de cheltuieli: „Trasare stivă: Compania nu există”. |
| Deplasări și cheltuieli | [622465](https://fix.lcs.dynamics.com/Issue/Details/?bugId=622465) | Câmpul implicit **ID proiect** nu este înscris în rapoartele de cheltuieli atunci când parametrul **Necesită activitate pentru jurnal** este selectat în proiect. |
| Deplasări și cheltuieli | [626781](https://fix.lcs.dynamics.com/Issue/Details/?bugId=626781) | Butonul **Publicare Cheltuieli** nu funcționează corect în Project Operations pentru scenarii de resurse/care nu există pe stoc. |
| Deplasări și cheltuieli | [635348](https://fix.lcs.dynamics.com/Issue/Details/?bugId=635348) | Există o problemă legată de **Tarif pe milă** pentru un raport de cheltuieli de kilometraj care include pasagerii. |
| Deplasări și cheltuieli | [638019](https://fix.lcs.dynamics.com/Issue/Details/?bugId=638019) | Ratele de kilometraj de cheltuieli pentru angajați nu sunt totalizate corect atunci când două tipuri diferite de vehicule sunt utilizate în categoria de cheltuieli **Nivelurile ratei de kilometraj**. |
| Deplasări și cheltuieli | [641272](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641272) | Căutarea pentru câmpul **Proiect** de pe o linie de solicitare de călătorie nu returnează lista corectă de proiecte. |
| Deplasări și cheltuieli | [645905](https://fix.lcs.dynamics.com/Issue/Details/?bugId=645905) | **Kilometraj în revizuire** afișează un avertisment pe rapoartele de cheltuieli. |
| Deplasări și cheltuieli | [647819](https://fix.lcs.dynamics.com/Issue/Details/?bugId=647819) | Serviciul de recunoaștere optică a caracterelor (OCR) a chitanței nu funcționează din cauza unei probleme cu adresa URL a serviciului OCR de cheltuieli. |
| Deplasări și cheltuieli | [648684](https://fix.lcs.dynamics.com/Issue/Details/?bugId=648684) | Cand caracteristica **Abilitatea de a detalia rapid cheltuielile recurente** este activată, sumele de pe liniile de detaliere din rapoartele de cheltuieli modifică sumele de fiecare dată când pagina **Detaliere** este deschisă. |
| Deplasări și cheltuieli | [651899](https://fix.lcs.dynamics.com/Issue/Details/?bugId=651899) | Nu puteți șterge un raport de cheltuieli atunci când lista intermediară are mai mulți aprobatori. |

## <a name="removed-and-deprecated-features"></a>Caracteristici eliminate și perimate

Articolul [Caracteristici eliminate sau perimate în Project Operations](removed-depreciated-features-project.md) descrie funcțiile care au fost eliminate sau perimate pentru Dynamics 365 Project Operations.

- O caracteristică eliminat nu mai este disponibilă în produs.
- O caracteristică perimată nu este în dezvoltare activă și ar putea fi eliminată într-o actualizare viitoare.

Un anunț de perimare va apărea în articolul [Caracteristici eliminate sau perimate în Project Operations](removed-depreciated-features-project.md) cu 12 luni înainte ca orice caracteristică să fie eliminată din produs.

Pentru modificările nerespective care afectează doar timpul de compilare, dar sunt compatibile binar cu mediile sandbox și de producție, timpul de perimare va fi mai mic de 12 luni. De obicei, aceste modificări sunt actualizări funcționale care trebuie făcute compilatorului.
