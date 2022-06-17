---
title: Ce este nou sau schimbat în Operațiunile de proiect, octombrie 2021 pentru scenariile stocate/bazate pe producție
description: Acest articol oferă informații despre actualizările de calitate disponibile în ediția din octombrie 2021 a Project Operations pentru scenariile stocate/bazate pe producție.
author: andchoi
ms.date: 11/17/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: andchoi
ms.openlocfilehash: ba88268e74269c774b41396a8b6574e5bab477b9
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8933691"
---
# <a name="whats-new-or-changed-in-project-operations-october-2021-for-stockedproduction-based-scenarios"></a>Ce este nou sau schimbat în Operațiunile de proiect, octombrie 2021 pentru scenariile stocate/bazate pe producție

_**Se aplică la:** Project Operations pentru scenariile bazate pe stocuri/producție_

Acest articol se aplică următoarelor componente și versiuni ale Microsoft Dynamics 365 Project Operations:

- Management de proiect și contabilitate într-un mediu Dynamics 365 Finance versiunea 10.0.22
 
## <a name="quality-updates"></a>Actualizări de calitate

| Zonă de caracteristici | Număr de referință | Actualizare de calitate |
|--------------|------------------|----------------|
| Management de proiect și contabilitate | [557017](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557017) | Lucrările de proiect în curs (WIP) și sumele veniturilor acumulate nu sunt inversate corect atunci când este înregistrată o factură de client intercompanie. |
| Management de proiect și contabilitate | [558232](https://fix.lcs.dynamics.com/Issue/Details/?bugId=558232) | The **Preveniți închiderea proiectului dacă există tranzacții deschise** funcționalitatea nu funcționează. |
| Management de proiect și contabilitate | [559271](https://fix.lcs.dynamics.com/Issue/Details/?bugId=559271) | Clasificarea de facturare pe o factură cu text liber nu completează automat dimensiunile din proiecte atunci când această funcționalitate este activată. |
| Management de proiect și contabilitate | [574013](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574013) | În scenariile non-intercompany, WIP și sumele veniturilor acumulate nu sunt inversate corect atunci când factura de proiect este înregistrată. |
| Management de proiect și contabilitate | [577857](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577857) | Valorile de debit și credit sunt schimbate atunci când Microsoft Excel add-in-ul este utilizat cu jurnalul de cheltuieli ale proiectului și **Tip de cont compensat** câmpul este setat la **Proiect**. |
| Management de proiect și contabilitate | [577972](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577972) | Suma care este înregistrată în tranzacțiile de proiect este supraevaluată pe o comandă de achiziție de proiect care include articole stocate și care are sume de taxe nedeductibile atunci când **UseTax** este marcat. |
| Management de proiect și contabilitate | [581216](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581216) | Sistemul împarte suma între rapoartele de profit și pierdere ale proiectului și rapoartele WIP ale proiectului. |
| Management de proiect și contabilitate | [582065](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582065) | Inventarul disponibil este incorect după ce o cerință de articol returnat parțial este ajustată. |
| Management de proiect și contabilitate | [582682](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582682) | Numele resurselor sunt duplicate în Operațiuni de proiect atunci când sunt editate în Microsoft Project. |
| Management de proiect și contabilitate | [583873](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583873) | Rapoartele de cheltuieli intercompanii care au costuri intercompanii de plătitori în așteptarea facturii furnizorului sunt mai întâi înregistrate în **Costul WIP al proiectului** tip de postare. Cu toate acestea, în timpul procesării, costurile aferente estimării sunt înregistrate în **Costul proiectului** tipul de postare în loc de cel așteptat **Costul intercompanii** tip de postare. |
| Management de proiect și contabilitate | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | Rezultatele reținerii furnizorului în tranzacțiile de cheltuieli ale proiectului nu sunt afișate. |
| Management de proiect și contabilitate | [587453](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587453) | Foaia de pontaj trebuie să rotunjească suma tranzacției în moneda tranzacției la un anumit număr de zecimale pe toate distribuțiile contabile și înregistrările generale de alocare a jurnalului. |
| Management de proiect și contabilitate | [589409](https://fix.lcs.dynamics.com/Issue/Details/?bugId=589409) | Cantitățile necesare pentru articolele proiectului sunt actualizate automat când comenzile planificate sunt confirmate. |
| Management de proiect și contabilitate | [590206](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590206) | Numărul voucherului, soldul furnizorului tip tranzacție și numărul contului nu pot fi inversate pe factura de plată anticipată a unei comenzi de achiziție. |
| Management de proiect și contabilitate | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | Factura furnizorului intercompanii este întreruptă atunci când integrarea facturii furnizorului este activată. |
| Management de proiect și contabilitate | [593335](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593335) | Când creați un jurnal de cheltuieli pentru proiect, suma costului este afișată în **Credit** camp. |
| Management de proiect și contabilitate | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | Condițiile de plată de pe facturile de proiect nu funcționează conform așteptărilor. |
| Management de proiect și contabilitate | [593565](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593565) | Bonurile de pontaj pot fi reutilizate atunci când secvența de numere este configurată ca continuă. |
| Management de proiect și contabilitate | [593652](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593652) | FRANTA: The **Suma de retenție manuală** logica nu se potrivește cu **Suma de retenție automată** logica din propunerea de facturare a contractului de proiect. |
| Management de proiect și contabilitate | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | Când reținerea furnizorului este eliberată, înregistrarea voucherului are rânduri suplimentare incorecte. |
| Management de proiect și contabilitate | [596650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596650) | Cand **Data facturii** câmp de pe **Creați o propunere de factură** pagina este schimbată, poate apărea următoarea eroare: „Referința obiectului nu este setată la o instanță a unui obiect”. |
| Management de proiect și contabilitate | [597679](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597679) | Apare o eroare când încercați să aprobați o foaie de pontaj de la **TSLine** flux de lucru și există o politică de pontaj pentru sâmbătă și duminică. |
| Management de proiect și contabilitate | [597801](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597801) | Tipul de articol al proiectului soldului de început este exclus din **Rezumatele tranzacțiilor pentru propunerea de factură** când se calculează totalul facturii propunerii de factură. |
| Management de proiect și contabilitate | [597886](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597886) | Dacă costul de consum pe o comandă de producție de proiect este 0 (zero), atunci când încercați să estimați, apare următoarea eroare: „S-a încercat împărțirea la zero”. |
| Management de proiect și contabilitate | [598706](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598706) | Aplicația mobilă Project Timesheet pentru Android nu mai răspunde. Problema este legată de **TimeEntryDataManager ArgumentNullException**. |
| Management de proiect și contabilitate | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | Jurnalul de integrare Project Operations eșuează atunci când îl publicați, deoarece unui cont îi lipsesc dimensiuni. Cu toate acestea, contul căruia îi lipsesc parametrii nu este contul în care postați. |
| Management de proiect și contabilitate | [598929](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598929) | The **Până în prezent** filtrul în căutări nu este șters când este eliminat din **Selectați** caseta de dialog pe **Cost post** pagină. |
| Management de proiect și contabilitate | [599757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=599757) | **Resetați toată distribuția** eșuează și afișează o eroare pentru foile de pontaj care sunt create pentru un proiect al **Numai timp** tip. |
| Management de proiect și contabilitate | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | The **Proiect** fila nu este editabilă pe o factură de furnizor în așteptare atunci când categoria de achiziție este atribuită articolului. |
| Management de proiect și contabilitate | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | Panoul de navigare lipsește dacă nu sunteți conectat la Project Operations Dataverse. |
| Management de proiect și contabilitate | [546467](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546467) | Pentru tranzacțiile de ajustare a proiectelor între companii, există probleme în compania de destinație. |
| Management de proiect și contabilitate | [563579](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563579) | Costurile angajate pentru un proiect calculează cantitatea și prețul de cost greșit dacă comanda de cumpărare a fost procesată de **Procesul de sfârșit de an al comenzii de achiziție** în Cartea mare. |
| Management de proiect și contabilitate | [581454](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581454) | Când o comandă de producție de proiect care are comenzi de calitate este raportată ca finalizată, apare următoarea eroare: „Nici o tranzacție virtuală marcată cu tranzacție de inventar”. |
| Management de proiect și contabilitate | [596408](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596408) | Când se înregistrează o factură aferentă unui proiect Conturi de plătit, apare următoarea eroare: „Textul enumerat Proiect - cost - articol nu există”. |
| Management de proiect și contabilitate | [597237](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597237) | Costurile indirecte se dublează atunci când acumulezi manual venituri. |
| Management de proiect și contabilitate | [601198](https://fix.lcs.dynamics.com/Issue/Details/?bugId=601198) | Acumularea veniturilor și înregistrarea WIP nu generează tranzacții. |
| Management de proiect și contabilitate | [602095](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602095) | Activarea prețului în așteptare eșuează pentru un articol de cost standard atunci când există o comandă de achiziție de proiect primită. |
| Management de proiect și contabilitate | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | Valoarea WIP inversată dintr-o înregistrare a facturii diferă de valoarea WIP inițială înregistrată de la o intrare de timp. |
| Management de proiect și contabilitate | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Există o problemă de înregistrare pentru veniturile facturate de proiect în cazurile de reținere aplicată în care tranzacțiile pe bon nu se echilibrează. |
| Management de proiect și contabilitate | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | Crearea unei estimări după înregistrarea unei propuneri de factură blochează importul liniilor de corecție în Operațiuni de proiect. |
| Management de proiect și contabilitate | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | Modificarea unei înregistrări de reper facturată integral nu ar trebui să fie posibilă. |
| Management de proiect și contabilitate | [611389](https://fix.lcs.dynamics.com/Issue/Details/?bugId=611389) | Când sunt utilizate taxe automate, factura intercompanii a clientului pentru o foaie de pontaj nu poate fi postată și este afișat un mesaj de eroare. |
| Management de proiect și contabilitate | [612991](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612991) | Adresa unui subproiect nu este corect actualizată. |
| Management de proiect și contabilitate | [613418](https://fix.lcs.dynamics.com/Issue/Details/?bugId=613418) | Prețul de cost pentru cerințele articolului este actualizat cu prețul de achiziție pentru comenzile de achiziție consolidate. |
| Management de proiect și contabilitate | [614145](https://fix.lcs.dynamics.com/Issue/Details/?bugId=614145) | Costul postat nu este corect după actualizarea prețului de achiziție și a parametrului **Activați gestionarea modificărilor** este activat. |
| Deplasări și cheltuieli | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Toate cheltuielile utilizatorilor pot fi văzute atunci când căutați o categorie în aplicația mobilă Cheltuieli. |
| Deplasări și cheltuieli | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | Sumele incorecte pentru tranzacțiile furnizorilor și tranzacțiile cu impozitul pe vânzări sunt înregistrate dintr-o cheltuială care a fost creată dintr-o tranzacție cu cardul de credit. |
| Deplasări și cheltuieli | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | Un mesaj de avertizare irelevant este afișat când reîmprospătați paginile raportului de cheltuieli. |
| Deplasări și cheltuieli | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | Aprobatorul interimar greșit este utilizat atunci când ștergeți un autorizator interimar și apoi retrimiteți prin fluxul de lucru. |
| Deplasări și cheltuieli | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | Apare o eroare de postare legată de configurarea kilometrajului. |
| Deplasări și cheltuieli | [620773](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620773) | Distribuția nu actualizează entitatea juridică atunci când o tranzacție neatașată este adăugată din nou la raportul de cheltuieli pentru o cheltuială intercompanie. |

### <a name="regulatory-updates"></a>Actualizări de reglementare

Pentru informații despre actualizările de reglementare pentru aplicațiile Finance and Operations, consultați [Actualizări de reglementare](/dynamics365/finance/localizations/regulatory-updates). De asemenea, vă puteți conecta la Microsoft Dynamics Lifecycle Services (LCS) și utilizați instrumentul de căutare a problemelor pentru a vedea actualizările de reglementare planificate. Căutarea problemelor vă permite să căutați după țară sau regiune, tip de caracteristică și versiune.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
