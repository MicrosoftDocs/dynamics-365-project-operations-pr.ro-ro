---
title: Noutăți sau modificări în Project Operations, mai 2021, pentru scenarii bazate pe stocuri/producție
description: Acest subiect oferă informații despre actualizările de calitate disponibile în versiunea Project Operations din mai 2021 pentru scenarii bazate pe stocuri/producție.
author: andchoi
ms.date: 07/01/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: andchoi
ms.openlocfilehash: c4f58842c33ec5f45a6cd9ea4bd0e73b0aa693b7cecf63bfa8889a5671840d7b
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/06/2021
ms.locfileid: "6991141"
---
# <a name="whats-new-or-changed-in-project-operations-may-2021-for-stockedproduction-based-scenarios"></a>Noutăți sau modificări în Project Operations, mai 2021, pentru scenarii bazate pe stocuri/producție

_ **Se aplică la:** Project Operations pentru scenariile bazate pe stocuri/producție

Acest subiect se aplică următoarelor componente și versiuni Dynamics 365 Project Operations:

- Management de proiect și contabilitate în Dynamics 365 Finance versiunea mediului 10.0.19
 
### <a name="quality-updates"></a>Actualizări de calitate
                                                                                                                                                                                  
| Zonă de caracteristici                      | Număr de referință| Actualizare de calitate                                                                                                                                                                          |
|-----------------------------------|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Management de proiect și contabilitate | [529751](https://fix.lcs.dynamics.com/Issue/Details/?bugId=529751) | Importul eșuează când validările entității sunt dezactivate pentru liniile de jurnal ale elementelor proiectului.                                                                                                                                                   |
| Management de proiect și contabilitate | [550565](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550565) | Există o problemă de performanță cu raportul conturilor WIP legat de căutarea **GeneralJournalEntry**.                                                                                                                                  |
| Management de proiect și contabilitate | [539044](https://fix.lcs.dynamics.com/Issue/Details/?bugId=539044) | Dimensiunile financiare lipsesc în proiectul WIP.                                                                                                                                                                                                    |
| Management de proiect și contabilitate | [540903](https://fix.lcs.dynamics.com/Issue/Details/?bugId=540903) | Postarea unei propuneri de facturare eșuează deoarece **ProjBudgetAllocationLineIdSales** greșit este atribuit la **ProjBudgetReductionHistory**.                                                                                                                           |
| Management de proiect și contabilitate | [547090](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547090) | După importul fișierului XML, jurnalul general afișează numere de voucher incorecte.                                                                                                                                                              |
| Management de proiect și contabilitate | [552160](https://fix.lcs.dynamics.com/Issue/Details/?bugId=552160) | Apare o eroare la șablonul structurii detaliate a proiectului.                                                                                                                                                                                          |
| Management de proiect și contabilitate | [552976](https://fix.lcs.dynamics.com/Issue/Details/?bugId=552976) | **Notele formularului** și **Configurarea formularului** nu sunt vizibile în configurarea managementului de proiect în entitățile juridice de finanțare atunci când sunt integrate în Project Operations.                                                                                                             |
| Management de proiect și contabilitate | [553313](https://fix.lcs.dynamics.com/Issue/Details/?bugId=553313) | Anularea unei comenzi de vânzări între companii eșuează cu următoarea eroare: „Nu se poate edita o înregistrare în liniile comenzii de cumpărare (PurchLine). A apărut un conflict de actualizare din cauza unui alt proces de utilizator care a șters înregistrarea sau a schimbat unul sau mai multe câmpuri din înregistrare.” |
| Management de proiect și contabilitate | [553775](https://fix.lcs.dynamics.com/Issue/Details/?bugId=553775) | Ajustarea tranzacției proiectului creează o dimensiune financiară greșită pentru costul proiectului.                                                                                                                                                          |
| Management de proiect și contabilitate | [556751](https://fix.lcs.dynamics.com/Issue/Details/?bugId=556751) | Factura furnizorului are o solicitare suplimentară atunci când procesează o comandă de achiziție conectată la un proiect.                                                                                                                                                 |
| Management de proiect și contabilitate | [557925](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557925) | Liniile din orar nu pot fi aprobate și apare următoarea eroare „Condiția de activare pentru fluxul de lucru nu este validă. Raportați această problemă administratorului de sistem.”                                                                          |
| Management de proiect și contabilitate | [559266](https://fix.lcs.dynamics.com/Issue/Details/?bugId=559266) | Dacă primiți eroarea „Nu se poate modifica contractul de proiect deoarece există o tranzacție pentru proiectul asociat XXXXXX”, puteți schimba în continuare contractul la nivel de proiect.                                                                           |
| Management de proiect și contabilitate | [560432](https://fix.lcs.dynamics.com/Issue/Details/?bugId=560432) | Dacă primiți eroarea „Cantitatea nu poate fi facturată, deoarece tranzacțiile cu inventar cu starea Dedus sunt insuficiente”, o factură a comenzii de achiziție nu poate fi înregistrată după executarea recalculării inventarului.                             |
| Management de proiect și contabilitate | [562013](https://fix.lcs.dynamics.com/Issue/Details/?bugId=562013) | Când fluxul de lucru Solicitare resurse este activat, există probleme de performanță atunci când se încearcă deschiderea paginilor de control al disponibilității resurselor proiectului.                                                                                                               |
| Management de proiect și contabilitate | [488320](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488320) | Starea facturii se modifică în **Netarifabil** după ce adăugați o regulă de facturare pentru a specifica un alt proiect la contractul de proiect.                                                                                                                                |
| Management de proiect și contabilitate | [515219](https://fix.lcs.dynamics.com/Issue/Details/?bugId=515219) | Apare o eroare atunci când eliminați o factură de plată anticipată dintr-o comandă de achiziție a proiectului și este activat parametrul **Costul ulterior avansului în raport cu proiectul**.                                                                                                        |
| Management de proiect și contabilitate | [526439](https://fix.lcs.dynamics.com/Issue/Details/?bugId=526439) | Când postați o factură de comandă de achiziție a proiectului, apare o eroare deoarece lipsește marcarea automată a articolelor.                                                                                                                            |
| Management de proiect și contabilitate | [527970](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527970) | În descrierea implicită TVA-ul nu este completat atunci când tipul de postare este același cu taxa de vânzare pentru voucherele de factură pentru proiect.                                                                                                                                           |
| Management de proiect și contabilitate | [530352](https://fix.lcs.dynamics.com/Issue/Details/?bugId=530352) | O comandă de achiziție a proiectului va afișa o eroare dacă ștergeți comanda de vânzare cerută pentru articolul anulat.                                                                                                                                 |
| Management de proiect și contabilitate | [530651](https://fix.lcs.dynamics.com/Issue/Details/?bugId=530651) | Când bifați și debifați comenzile de achiziție cerute pentru elementul de proiect, referințele se pierd.                                                                                                                                                               |
| Management de proiect și contabilitate | [533023](https://fix.lcs.dynamics.com/Issue/Details/?bugId=533023) | Există o problemă cu valoarea implicită a cantității reduse la imprimarea unei liste de selectare pentru cerințele articolului de proiect.                                                                                                                                                 |
| Management de proiect și contabilitate | [535493](https://fix.lcs.dynamics.com/Issue/Details/?bugId=535493) | Prețul de vânzare calculat nu este corect dacă există o livrare excesivă.                                                                                                                                                                                 |
| Management de proiect și contabilitate | [541329](https://fix.lcs.dynamics.com/Issue/Details/?bugId=541329) | Datoria greșită este înregistrată atunci când reținerea este eliberată fără o cantitate de factură pe o propunere de factură.                                                                                                                                                |
| Management de proiect și contabilitate | [541997](https://fix.lcs.dynamics.com/Issue/Details/?bugId=541997) | Când generați o perioadă pe orar, prima perioadă apare ca săptămâna 53.                                                                                                                                                                         |
| Management de proiect și contabilitate | [542043](https://fix.lcs.dynamics.com/Issue/Details/?bugId=542043) | Tipurile implicite de proiect în parametrii de integrare Dynamics 365 Project Service Automation ar trebui să fie Timp și Material și Preț fix.                                                                                                         |
| Management de proiect și contabilitate | [543096](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543096) | Ștergerea unei propuneri de facturare cu reguli de facturare generează postări.                                                                                                                                                                              |
| Management de proiect și contabilitate | [543463](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543463) | Estimarea finală a procesului de eliminare utilizând metoda procentuală completă nu poate fi eliminată deoarece sistemul nu recunoaște veniturile.                                                                                                                                      |
| Management de proiect și contabilitate | [543938](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543938) | Când postați o estimare de proiect, înregistrarea estimării de post nu este creată.                                                                                                                                                                            |
| Management de proiect și contabilitate | [546885](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546885) | Contul principal al unei facturi de vânzător în așteptare nu este găsit în timpul facturării între companii.                                                                                                                                                               |
| Management de proiect și contabilitate | [547885](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547885) | Dacă un contract include cerințe privind articolele, nu puteți adăuga a doua sursă de finanțare.                                                                                                                                                         |
| Management de proiect și contabilitate | [550379](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550379) | Sistemul creează revizuiri la bugetul proiectului pentru toate proiectele atunci când utilizați **Proiect** > **Buget** > **Revizuiri** > **Nou** > **Import**.                                                                                                                         |
| Management de proiect și contabilitate | [550577](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550577) |  Dacă modificați o tranzacție cu diferite tranzacții și valute contabile, postarea și înregistrările din registrul general sunt incorecte.                                                                                                                                       |
| Management de proiect și contabilitate | [557049](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557049) | Costul angajat este supraevaluat cu impozite nedeductibile.                                                                                                                                                                                   |
| Management de proiect și contabilitate | [557376](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557376) | Nu se preia nicio dimensiune atunci când creați o factură de postare pentru o tranzacție.                                                                                                                                                                  |
| Management de proiect și contabilitate | [559416](https://fix.lcs.dynamics.com/Issue/Details/?bugId=559416) | Metoda **PurchTotals.purchNewTotalAmount()** este aplicată atunci când creați o factură de furnizor în așteptare care nu este legată de o comandă de achiziție, ceea ce duce la o problemă de performanță.                                                                                   |
| Management de proiect și contabilitate | [563694](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563694) | Coloanele **Buget consumat** și **Buget rămas** coloanele afișează sume incorecte la soldurile bugetului proiectului.                                                                                                                                                |
| Management de proiect și contabilitate | [565089](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565089) | O tranzacție este postată de două ori când se utilizează facturarea bazată pe sarcini în Dataverse cu Project Operations.                                                                                                                                         |
| Management de proiect și contabilitate | [566869](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566869) | Procentul complet pentru recunoașterea veniturilor este incorect atunci când se utilizează Project Operations.                                                                                                                                                  |
| Management de proiect și contabilitate | [568107](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568107) | Acumularea de venituri este dublată atunci când utilizați o factură de furnizor în așteptare într-un scenariu integrat Project Operations.                                                                                                                                          |
| Management de proiect și contabilitate | [569736](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569736) | Postarea unui orar al proiectului creează tranzacții duplicat.                                                                                                                                                                        |
| Management de proiect și contabilitate | [569819](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569819) | Apare o eroare când postați jurnalul de consum de articole față de comanda de lucru.                                                                                                                                  |
| Management de proiect și contabilitate | [571197](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571197) | O comandă de producție a proiectului nu poate fi finalizată din cauza următoarei erori, „Referința obiectului nu este setată la o instanță a unui obiect.”                                                                                                                           |
| Management de proiect și contabilitate | [572370](https://fix.lcs.dynamics.com/Issue/Details/?bugId=572370) | Jurnalul de integrare nu poate fi postat dacă regula profilului veniturilor este setată la **Configurarea grupului**.                                                                                                                                                           |
| Management de proiect și contabilitate | [573596](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573596) | O factură de achiziție nu poate fi postată pentru o comandă de achiziție a proiectului care are linii cu mai multe unități de măsură.                                                                                                                                             |
| Management de proiect și contabilitate | [573637](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573637) | Dimensiunea financiară implicită pentru un proiect nu poate fi actualizată folosind entitatea de date **Proiecte V2**.                                                                                                                                                          |
| Management de proiect și contabilitate | [573886](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573886) | Nu se poate crea o notă de credit pentru o comandă de vânzare a proiectului atunci când taxa este într-o monedă diferită de moneda companiei.                                                                                                                     |
| Management de proiect și contabilitate | [574104](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574104) | Există o problemă la crearea unei propuneri de facturare cu peste 100 de reguli de facturare.                                                                                                                                                                  |
| Management de proiect și contabilitate | [577211](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577211) | Procesul de creare a lotului estimat de proiect durează prea mult.                                                                                                                                                                      |
| Management de proiect și contabilitate | [577785](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577785) | Când rulați funcționalitatea **Populați resursele proiectului în toate companiile**, apare următoarea eroare „Numele obiectului ResRollupCalendar nu este valid.”                                                                                                                                   |
| Management de proiect și contabilitate | [582329](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582329) | Când ștergeți un contract, se șterge și adresa asociată clientului.                                                                                                                                                                    |
| Deplasări și cheltuieli                  | [514930](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514930) | Condiția fluxului de lucru pentru aprobarea raportului de cheltuieli nu este evaluată corect.                                                                                                                                                                           |
| Deplasări și cheltuieli                  | [519304](https://fix.lcs.dynamics.com/Issue/Details/?bugId=519304) | Politica privind raportul de cheltuieli nu evaluează corect ID-ul proiectului.                                                                                                                                                                                   |
| Deplasări și cheltuieli                  | [522463](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522463) | Acțiunea **Împărțire la personal** pentru tranzacțiile de cheltuieli între companii nu funcționează corect.                                                                                                                                                                |
| Deplasări și cheltuieli                  | [534702](https://fix.lcs.dynamics.com/Issue/Details/?bugId=534702) | Justificările din linia raportului de cheltuieli sunt uneori șterse atunci când anumite cereri de călătorie sunt șterse. Acest lucru se întâmplă atunci când recID-ul raportului de cheltuieli și cererea de călătorie sunt aceleași.                                                            |
| Deplasări și cheltuieli                  | [544368](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544368) | Există o problemă în aplicația mobilă Cheltuieli atunci când câmpul **ID proiect** este obligatoriu în politicile raportului de cheltuieli.                                                                                                                                                |
| Deplasări și cheltuieli                  | [545331](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545331) | Când încercați să editați o cheltuială între companii care este asociată cu un proiect, apare următorul mesaj de eroare, „Referința obiectului nu este setată la o instanță a unui obiect.”                                                                           |
| Deplasări și cheltuieli                  | [548659](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548659) | După postarea raportului de cheltuieli, moneda și suma greșite sunt afișate în registrul de bancă.                                                                                                                                                                |
| Deplasări și cheltuieli                  | [555462](https://fix.lcs.dynamics.com/Issue/Details/?bugId=5355462) | Costul angajat pentru un proiect nu este eliberat după închiderea unei cereri de călătorie cu un cost angajat.                                                                                                                                              |
| Deplasări și cheltuieli                  | [558336](https://fix.lcs.dynamics.com/Issue/Details/?bugId=558336) | Au fost aduse îmbunătățiri caracteristicii Ștergeți tranzacțiile cu cardul de credit.                                                                                                                                                                                           |
| Deplasări și cheltuieli                  | [525070](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525070) | Impozitul pe vânzări inclus într-un raport de cheltuieli nu este calculat în mod consecvent atunci când este specificată o altă monedă de raportare pentru o persoană juridică.                                                                                                         |
| Deplasări și cheltuieli                  | [527779](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527779) | Performanța este afectată atunci când se adaugă o nouă cheltuială de călătorie în numerar.                                                                                                                                                                                         |
| Deplasări și cheltuieli                  | [537841](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537841) | Regulile politicii de cheltuieli nu sunt declanșate într-un raport de cheltuieli.                                                                                                                                                                                            |
| Deplasări și cheltuieli                  | [566386](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566386) | Încărcarea unei noi categorii partajate folosind Data Management Framework elimină toate subcategoriile pentru toate categoriile partajate.                                                                                                                         |
| Deplasări și cheltuieli                  | [574131](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574131) | Când creați o linie de cheltuieli și apoi selectați o categorie, se afișează următorul mesaj de eroare: „Combinația grupului de taxe pe vânzări DOM și a grupului de taxe pe vânzări articol STD nu este validă.”                                                                  |
| Deplasări și cheltuieli                  | [574900](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574900) | Există probleme de sincronizare în aplicația mobilă Cheltuieli. 

### <a name="regulatory-updates"></a>Actualizări de reglementare
Pentru informații despre actualizările de reglementare pentru aplicații Finance and Operations, vezi [Actualizări de reglementare](/dynamics365/finance/localizations/regulatory-updates). De asemenea, vă puteți conecta la Lifecycle Services (LCS) și puteți vizualiza actualizările de reglementare planificate folosind instrumentul de căutare a problemelor. Căutarea problemelor vă permite să căutați în funcție de țară, tipul de funcție și eliberare.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]