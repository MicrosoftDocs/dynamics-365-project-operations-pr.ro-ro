---
title: Ce este nou în ianuarie 2021 - Project Operations pentru scenarii bazate pe resurse/ne-stocate
description: Acest subiect oferă informații despre actualizările de calitate disponibile în lansarea din ianuarie 2021 a Project Operations pentru scenarii bazate pe resurse/ne-stocate.
author: sigitac
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: c600c30acd5e07e6370459928e33033a6ba418d6
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 05/10/2021
ms.locfileid: "5995771"
---
# <a name="whats-new-january-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Ce este nou în ianuarie 2021 - Project Operations pentru scenarii bazate pe resurse/ne-stocate

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_


Acest subiect se aplică următoarelor componente și versiuni Dynamics 365 Project Operations:

  - Project Operations pe mediul Dataverse versiunea 4.6.0.154
  - Management de proiect și contabilitate în Dynamics 365 Finance versiunea mediului 10.0.16

## <a name="quality-updates"></a>Actualizări de calitate

### <a name="project-operations-on-dataverse"></a>Project Operations pe Dataverse

| **Zonă de caracteristici** | **Număr de referință** | **Actualizare de calitate** |
| --- | --- | --- |
| **Implementare și configurare** | 2106818 | S-a remediat redenumirea resursei web care provoca probleme legate de personalizarea unei pagini. |
| **Facturare și stabilirea prețurilor** | 2091908 | S-a remediat vizibilitatea opțiunilor **Blocare prețuri** și **Folosiți prețurile actuale** pe pagina **Factură** când Project Operations este instalat împreună cu Dynamics 365 Field Service. |
| **Facturare și stabilirea prețurilor** | 2103058 | S-a reîmprospătat **Totaluri proiect** pentru a gestiona valorile nule pentru costul real al unei sarcini. |
| **Facturare și stabilirea prețurilor** | 2116100 | Mesaje de eroare îmbunătățite utilizate cu funcționalitatea, **Corectați intrările la valori reale**. |
| **Facturare și stabilirea prețurilor** | 2116129 | S-a îmbunătățit vizibilitatea la estimările de cheltuieli pe fila **Estimări** de pe pagina **Proiecte**. |
| **Facturare și stabilirea prețurilor** | 2119112 | S-au remediat agregările de vânzările reale și costuri real atunci când sunt utilizate cursuri de schimb diferite. |
| **Facturare și stabilirea prețurilor** | 2134705 | S-a remediat eroarea „Nu se poate citi proprietatea **ObținețiȘirResursă** a nedefinit" când pagina **Factură** este deschisă și Field Service este instalat. |
| **Managementul oportunităților** | 2022195 | Grila de facturare bazată pe sarcini de pe pagina **Proiect** include o pictogramă care indică faptul că există linie de contract sau de ofertă asociată sarcinii respective. |
| **Managementul oportunităților** | 2029135 | S-a remediat eroarea procesului comercial care apare atunci când un utilizator încearcă să deschidă o linie de factură pe o factură confirmată care are o sumă în avans facturată. |
| **Managementul oportunităților** | 2040713 | S-a remediat eroarea de script care apare la crearea unei facturi dintr-un contract și Field Service este instalat. |
| **Planificarea și urmărirea proiectului** | 2090202 | Reguli comerciale marcate care nu mai sunt folosite ca **Depreciate**. |
| **Timp și cheltuială** | 2091249 | Controale mai stricte pentru ca utilizatorii să poată modifica sarcina la o intrare de timp aprobată sau trimisă. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Management de proiect și contabilitate în Dynamics 365 Finance

| **Zonă de caracteristici** | **Număr de referință** | **Actualizare de calitate** |
| --- | --- | --- |
| **Management de proiect și contabilitate** | [478667](https://fix.lcs.dynamics.com/Issue/Details/?bugId=478667) | Sumă contractuală incorectă pe pagina **În cont** pentru un proiect cu preț fix cu mai multe surse de finanțare. |
| **Management de proiect și contabilitate** | [480260](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480260) | Substituentul **PropunereFacturare.PSAnfRefProjId** nu afișează ID-ul proiectului pentru fluxul de lucru, **Examinați propunerile de facturare ale proiectului**. |
| **Management de proiect și contabilitate** | [481227](https://fix.lcs.dynamics.com/Issue/Details/?bugId=481227) | Data eronată de reducere a numerarului este utilizată la înregistrarea propunerilor de facturare pentru proiect. |
| **Management de proiect și contabilitate** | [482558](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482558) | Eliminarea și citirea alocărilor de resursele în Project Operations dublează intrările de prognoză ale proiectului în Finanțe. |
| **Management de proiect și contabilitate** | [484468](https://fix.lcs.dynamics.com/Issue/Details/?bugId=484468) | În Project Operations, nu puteți crea estimări de proiect în Dataverse fără a avea o linie de contract asociată proiectului proiect. |
| **Management de proiect și contabilitate** | [485871](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485871) | Dimensiunea financiară la o tranzacție de cheltuieli pentru proiect nu este sincronizată cu voucherul aferent și distribuția contabilă a raportului de cheltuieli când costurile sunt înregistrate în Sold. |
| **Management de proiect și contabilitate** | [488382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488382) | Filtrul pentru **Starea facturii** la tranzacțiile de proiect înregistrate pentru proiecte cu preț fix nu funcționează. |
| **Management de proiect și contabilitate** | [491941](https://fix.lcs.dynamics.com/Issue/Details/?bugId=491941) | Eliminarea inversă a estimării nu funcționează în secțiunea **Periodic**. |
| **Management de proiect și contabilitate** | [509989](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509989) | Liniile de propunere de facturare poti fi șterse în Project Operations când este integrat cu Dataverse. |
| **Management de proiect și contabilitate** | [510041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510041) | Previne activarea caracteristicii liniilor de contract multiple fără integrarea Dataverse. |
| **Management de proiect și contabilitate** | [510527](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510527) | Atunci când facturarea în cont este egală cu profitul și pierderea, veniturile facturate sunt listate ca zero pe pagina de Estimări. |
| **Management de proiect și contabilitate** | [514167](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514167) | Corecțiile facturilor nu funcționează în medii integrate. |
| **Management de proiect și contabilitate** | [514364](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514364) | La înregistrarea valorilor de vâznări WIP în facturarea proiectelor inter-companii, se selectrează contul greșit. |
| **Management de proiect și contabilitate** | [514385](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514385) | În Project Operations, dependențele de sarcini estimate în Dataverse nu pot fi actualizate. |
| **Management de proiect și contabilitate** | [515258](https://fix.lcs.dynamics.com/Issue/Details/?bugId=515258) | Ștergerea repetată a jurnalelor de integrare Project Operations în Finanțe duce la pierderea datelor. |
| **Management de proiect și contabilitate** | [519716](https://fix.lcs.dynamics.com/Issue/Details/?bugId=519716) | Următoarea eroare apare atunci când se postează o propunere de facturare a proiectului, „Tranzacția nu se compensează în raportarea monedei atunci când factura de avans dedusă este adăugată”. |
| **Management de proiect și contabilitate** | [521807](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521807) | ID-ul proiectului greșit este inclus în deduceri după actualizarea contractului implicit de proiect în Project Operations. |
| **Management de proiect și contabilitate** | [522799](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522799) | Estimarea și recunoașterea veniturilor nu pot fi finalizate atunci când este activat Project Operations. |
| **Management de proiect și contabilitate** | [527319](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527319) | În Project Operations, eliminarea unui proiect dintr-un contract nu resetează proiectul implicit din contract. |
| **Management de proiect și contabilitate** | [528212](https://fix.lcs.dynamics.com/Issue/Details/?bugId=528212) | În Project Operations, pe o factură inter-companii, liniile de cheltuieli greșite apar în lista **Adăugați linie**. |
| **Deplasări și cheltuieli** | [515334](https://fix.lcs.dynamics.com/Issue/Details/?bugId=515334) | Liniile de cheltuieli nu pot fi înregistrate, deoarece configurarea orei lipsește pe linia de contract. |
| **Deplasări și cheltuieli** | [437673](https://fix.lcs.dynamics.com/Issue/Details/?bugId=437673) | Când validarea proiectului/categoriilor este obligatorie, categoriile de cheltuieli asociate proiectului nu sunt vizibile în raportul de cheltuieli. |
| **Deplasări și cheltuieli** | [441256](https://fix.lcs.dynamics.com/Issue/Details/?bugId=441256) | Soldul avansului de numerar nu este actualizat când un raport de cheltuieli este înregistrat pe linie. |
| **Deplasări și cheltuieli** | [465396](https://fix.lcs.dynamics.com/Issue/Details/?bugId=465396) | Operațiunea **Actualizați informațiile de plată** eșuează după inversarea decontărilor în care a fost decontată o factură cu două sau mai multe tranzacții de plată. |
| **Deplasări și cheltuieli** | [472892](https://fix.lcs.dynamics.com/Issue/Details/?bugId=472892) | Există o problemă cu calcularea reducerii mesei din ultima zi pentru categoria de cheltuieli diurne. |
| **Deplasări și cheltuieli** | [477714](https://fix.lcs.dynamics.com/Issue/Details/?bugId=477714) | Raportul **Tip de cheltuieli pe angajat** nu afișează cheltuieli detaliate dacă prima conexiune a unui utilizator a fost în limba es-MX. |
| **Deplasări și cheltuieli** | [487516](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487516) | Plata furnizorului pentru o factură de raport de cheltuieli folosește un cont rezumativ greșit pentru înregistrarea decontării. |
| **Deplasări și cheltuieli** | [487531](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487531) | Când un raport de cheltuieli este postat cu funcțiile **Permiteți gruparea tranzacțiilor pe baza contului de plată compensată** și **Corectarea datei contabile la înregistrare** activat, datele contabile nu sunt grupate pe tabelul **Distribuția contabilă**, care are impact asupra înregistrărilor impozitului pe vânzări. |
| **Deplasări și cheltuieli** | [488292](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488292) | Cartografierea subcategoriei de cheltuielilor este eliminată atunci când Utilizarea în caseta de selectare pentru cheltuieli este debifată și apoi selectată din nou. |
| **Deplasări și cheltuieli** | [506175](https://fix.lcs.dynamics.com/Issue/Details/?bugId=506175) | Raportul de cheltuieli inter-companii nu poate fi creat dacă ID-ul proiectului este adăugat la nivelul antetului. |
| **Deplasări și cheltuieli** | [509491](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509491) | Există o problemă cu plățile cheltuielilor când valoarea cheltuielilor este mai mare decât suma în avans. |
| **Deplasări și cheltuieli** | [509556](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509556) | Câmpul **ID-ul proiectului** dintr-un raport de cheltuieli inter-companii este gol dacă rolul de utilizator este atribuit unei anumite organizații. |
| **Deplasări și cheltuieli** | [518186](https://fix.lcs.dynamics.com/Issue/Details/?bugId=518186) | Categoria de cheltuieli este blocată la adăugarea unei noi linii de cheltuieli. |
| **Deplasări și cheltuieli** | [520914](https://fix.lcs.dynamics.com/Issue/Details/?bugId=520914) | Detalierea liniilor de raportare a cheltuielilor care sunt deja divizate are ca rezultat un voucher înregistrat incomplet Conturi de debit\Registru general. Din cauza duplicării **CHELTDEPLTRANS.LINIEDOCUMENTSURSĂ**, Exploratorul sursei contabile este, de asemenea, defect. |
| **Deplasări și cheltuieli** | [521768](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521768) | Indicele adăugat în tabelul **LINIERECHIZIȚIEDEPL** pentru care clientul are duplicate, are ca rezultat o eroare în timpul actualizării. |
| **Deplasări și cheltuieli** | [525106](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525106) | În Project Operations, timpul cu sarcini inter companii în Dataverse nu poate fi creat sau aprobat. |

## <a name="regulatory-updates"></a>Actualizări de reglementare

Pentru informații despre actualizările de reglementare pentru aplicații Finance and Operations, vezi [Actualizări de reglementare](/dynamics365/finance/localizations/regulatory-updates). De asemenea, vă puteți conecta la LCS și puteți vizualiza actualizările de reglementare planificate folosind instrumentul de căutare a problemelor. Căutarea problemelor vă permite să căutați în funcție de țară, tipul de funcție și eliberare.


[!INCLUDE[footer-include](../includes/footer-banner.md)]