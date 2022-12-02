---
title: Noutăți sau modificări în Project Operations, octombrie 2021 pentru scenarii bazate pe stoc/producție
description: Acest articol oferă informații despre actualizările de calitate care sunt disponibile în versiunea din octombrie 2021 a Project Operations pentru scenarii bazate pe stoc/producție.
author: andchoi
ms.date: 11/17/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: andchoi
ms.openlocfilehash: aa36199c9e7b0a70307c5e9fb163d82554f6be16
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029958"
---
# <a name="whats-new-or-changed-in-project-operations-october-2021-for-stockedproduction-based-scenarios"></a>Noutăți sau modificări în Project Operations, octombrie 2021 pentru scenarii bazate pe stoc/producție

_**Se aplică la:** Project Operations pentru scenariile bazate pe stocuri/producție_

Acest articol se aplică următoarelor componente și versiuni de Microsoft Dynamics 365 Project Operations:

- Management de proiect și contabilitate într-un mediu Dynamics 365 Finance, versiunea 10.0.22
 
## <a name="quality-updates"></a>Actualizări de calitate

| Zonă de caracteristici | Număr de referință | Actualizare de calitate |
|--------------|------------------|----------------|
| Management de proiect și contabilitate | [557017](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557017) | Lucrările de proiect în curs (WIP) și sumele veniturilor acumulate nu sunt inversate corect atunci când este înregistrată o factură de client intercompanie. |
| Management de proiect și contabilitate | [558232](https://fix.lcs.dynamics.com/Issue/Details/?bugId=558232) | Funcționalitatea **Prevenirea închiderii proiectului dacă există tranzacții deschise** nu funcționează. |
| Management de proiect și contabilitate | [559271](https://fix.lcs.dynamics.com/Issue/Details/?bugId=559271) | Clasificarea de facturare pe o factură cu text liber nu completează automat dimensiunile din proiecte atunci când această funcționalitate este activată. |
| Management de proiect și contabilitate | [574013](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574013) | În scenariile non-intercompanie, WIP și sumele veniturilor acumulate nu sunt inversate corect atunci când factura de proiect este înregistrată. |
| Management de proiect și contabilitate | [577857](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577857) | Valorile de debit și credit sunt schimbate atunci când add-in-ul Microsoft Excel este utilizat cu jurnalul de cheltuieli ale proiectului și **Tip de cont de contrapartidă** câmpul este setat la **Proiect**. |
| Management de proiect și contabilitate | [577972](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577972) | Suma care este publicată în tranzacțiile de proiect este supraevaluată pe o comandă de achiziție de proiect care include articole stocate și care are sume de taxe nedeductibile atunci când **UseTax** este marcat. |
| Management de proiect și contabilitate | [581216](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581216) | Sistemul împarte suma între rapoartele de profit și pierdere ale proiectului și rapoartele WIP ale proiectului. |
| Management de proiect și contabilitate | [582065](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582065) | Inventarul disponibil este incorect după ce o cerință de articol returnat parțial este ajustată. |
| Management de proiect și contabilitate | [582682](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582682) | Numele resurselor sunt duplicate în Project Operations atunci când sunt editate în Microsoft Project. |
| Management de proiect și contabilitate | [583873](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583873) | Rapoartele de cheltuieli intercompanii care au costuri de plată intercompanii în așteptare pentru facturarea furnizorului sunt înregistrate mai întâi la tipul de publicare **Cost WIP al proiectului**. Cu toate acestea, în timpul procesării, costurile legate de estimare sunt înregistrate în tipul de publicare **Cost proiect** în loc de cel așteptat **Cost intercompanii**. |
| Management de proiect și contabilitate | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | Rezultatele reținerii furnizorului în tranzacțiile de cheltuieli ale proiectului nu sunt afișate. |
| Management de proiect și contabilitate | [587453](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587453) | Foaia de pontaj trebuie să rotunjească suma tranzacției în moneda tranzacției la un număr specificat de zecimale pe toate distribuțiile contabile și înregistrările generale de alocare de jurnal. |
| Management de proiect și contabilitate | [589409](https://fix.lcs.dynamics.com/Issue/Details/?bugId=589409) | Cantitățile necesare pentru articole din proiect sunt actualizate automat când comenzile planificate sunt confirmate. |
| Management de proiect și contabilitate | [590206](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590206) | Numărul voucherului, soldul furnizorului de tip tranzacție și numărul contului nu pot fi inversate pe factura de plată anticipată a unei comenzi de achiziție. |
| Management de proiect și contabilitate | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | Factura furnizorului intercompanii este întreruptă atunci când integrarea facturii furnizorului este activată. |
| Management de proiect și contabilitate | [593335](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593335) | Când creați un jurnal de cheltuieli pentru proiect, suma costului este afișată în câmpul **Credit**. |
| Management de proiect și contabilitate | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | Condițiile de plată de pe facturile de proiect nu funcționează conform așteptărilor. |
| Management de proiect și contabilitate | [593565](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593565) | Bonurile de pontaj pot fi reutilizate atunci când secvența de numere este configurată ca fiind continuă. |
| Management de proiect și contabilitate | [593652](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593652) | FRANȚA: Logica **Suma de retenție manuală** nu se potrivește cu logica **Suma de retenție automată** din propunerea de facturare a contractului de proiect. |
| Management de proiect și contabilitate | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | Când reținerea furnizorului este eliberată, publicarea voucherului are rânduri suplimentare incorecte. |
| Management de proiect și contabilitate | [596650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596650) | Cand câmpul **Dată factură** de pe pagina **Crearea unei propuneri de factură** este schimbată, poate apărea următoarea eroare: „Referința obiectului nu este setată la o instanță a unui obiect”. |
| Management de proiect și contabilitate | [597679](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597679) | Apare o eroare când încercați să aprobați o foaie de pontaj de la fluxul de lucru **TSLine** și există o politică de pontaj pentru sâmbătă și duminică. |
| Management de proiect și contabilitate | [597801](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597801) | Tipul de articol al proiectului soldului inițial este exclus din **Rezumatele tranzacțiilor pentru propunerea de factură** atunci când se calculează totalul facturii propunerii de factură. |
| Management de proiect și contabilitate | [597886](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597886) | Dacă costul de consum pe o comandă de producție de proiect este 0 (zero), apare următoarea eroare când încercați să estimați: „S-a încercat împărțirea la zero”. |
| Management de proiect și contabilitate | [598706](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598706) | Aplicația Project Timesheet Mobile pentru Android nu mai răspunde. Problema este legată de **TimeEntryDataManager ArgumentNullException**. |
| Management de proiect și contabilitate | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | Jurnalul de integrare Project Operations eșuează atunci când îl publicați, deoarece unui cont îi lipsesc dimensiuni. Cu toate acestea, contul căruia îi lipsesc dimensiunile nu este contul în care postați. |
| Management de proiect și contabilitate | [598929](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598929) | Filtrul **ToDate** în căutări nu este șters atunci când este eliminat din caseta de dialog **Selectare** de pe pagina **Cost publicare**. |
| Management de proiect și contabilitate | [599757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=599757) | **Resetați toată distribuția** eșuează și afișează o eroare pentru foile de pontaj care sunt create pentru un proiect de tipul **Numai timp**. |
| Management de proiect și contabilitate | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | Fila **Project** nu poate fi editată pe o factură de furnizor în așteptare atunci când categoria de achiziție este atribuită articolului. |
| Management de proiect și contabilitate | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | Panoul de navigare lipsește dacă nu sunteți conectat la Project Operations Dataverse. |
| Management de proiect și contabilitate | [546467](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546467) | Pentru tranzacțiile de ajustare a proiectelor între companii, există probleme în compania de destinație. |
| Management de proiect și contabilitate | [563579](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563579) | Costurile angajate pentru un proiect calculează cantitatea greșită și prețul de cost în cazul în care comanda de achiziție a fost procesată de **Procesul de sfârșit de an al comenzii de cumpărare** în registrul general. |
| Management de proiect și contabilitate | [581454](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581454) | Când o comandă de producție de proiect care are comenzi de calitate este raportată ca finalizată, apare următoarea eroare: „Nicio tranzacție virtuală marcată cu tranzacție de inventar”. |
| Management de proiect și contabilitate | [596408](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596408) | Când se înregistrează o factură pentru conturi de plată aferentă unui proiect, apare următoarea eroare: „Textul enumerat Project – cost – articol nu există”. |
| Management de proiect și contabilitate | [597237](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597237) | Costurile indirecte se dublează atunci când acumulați manual venituri. |
| Management de proiect și contabilitate | [601198](https://fix.lcs.dynamics.com/Issue/Details/?bugId=601198) | Acumularea veniturilor și înregistrarea WIP nu generează tranzacții. |
| Management de proiect și contabilitate | [602095](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602095) | Activarea prețului în așteptare eșuează pentru un articol de cost standard atunci când există o comandă de achiziție de proiect primită. |
| Management de proiect și contabilitate | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | Valoarea inversată WIP de la o publicare de factură diferă de valoarea WIP inițială înregistrată de la o intrare de timp. |
| Management de proiect și contabilitate | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Există o problemă de publicare pentru veniturile facturate de proiect în cazurile de reținere aplicată în care tranzacțiile pe voucher nu se echilibrează. |
| Management de proiect și contabilitate | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | Crearea unei estimări după publicarea unei propuneri de factură blochează importul liniilor de corecție în Project Operations. |
| Management de proiect și contabilitate | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | Nu ar trebui să fie posibilă modificarea unei înregistrări facturate integral. |
| Management de proiect și contabilitate | [611389](https://fix.lcs.dynamics.com/Issue/Details/?bugId=611389) | Când sunt utilizate taxe automate, factura intercompanii a clientului pentru o foaie de pontaj nu poate fi postată și este afișat un mesaj de eroare. |
| Management de proiect și contabilitate | [612991](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612991) | Adresa unui subproiect nu este corect actualizată. |
| Management de proiect și contabilitate | [613418](https://fix.lcs.dynamics.com/Issue/Details/?bugId=613418) | Prețul de cost pentru cerințele articolului este actualizat cu prețul de achiziție pentru comenzile de achiziție consolidate. |
| Management de proiect și contabilitate | [614145](https://fix.lcs.dynamics.com/Issue/Details/?bugId=614145) | Costul postat nu este corect după actualizarea prețului de achiziție și parametrul **Activare gestionare modificări** este activat. |
| Deplasări și cheltuieli | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Toate cheltuielile utilizatorilor pot fi văzute atunci când căutați o categorie în aplicația mobilă Cheltuieli. |
| Deplasări și cheltuieli | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | Sumele incorecte pentru tranzacțiile furnizorilor și tranzacțiile cu impozitul pe vânzări sunt înregistrate dintr-o cheltuială care a fost creată dintr-o tranzacție cu cardul de credit. |
| Deplasări și cheltuieli | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | Un mesaj de avertizare irelevant este afișat când reîmprospătați paginile raportului de cheltuieli. |
| Deplasări și cheltuieli | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | Aprobatorul interimar greșit este utilizat când ștergeți un aprobator interimar și apoi retrimiteți prin fluxul de lucru. |
| Deplasări și cheltuieli | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | Apare o eroare de postare legată de configurarea kilometrajului. |
| Deplasări și cheltuieli | [620773](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620773) | Distribuția nu actualizează entitatea juridică atunci când o tranzacție neatașată este adăugată din nou la raportul de cheltuieli pentru o cheltuială intercompanie. |

### <a name="regulatory-updates"></a>Actualizări de reglementare

Pentru informații despre actualizările de reglementare pentru aplicații de finanțe și operațiuni, consultați [Actualizări de reglementare](/dynamics365/finance/localizations/regulatory-updates). De asemenea, vă puteți conecta la Microsoft Dynamics Lifecycle Services (LCS) și puteți utiliza instrumentul de Căutare a problemelor pentru a vedea actualizările de reglementare planificate. Căutarea problemelor vă permite să căutați, în funcție de țară sau regiune, tipul de funcție și eliberare.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
