---
title: Ce este nou sau schimbat în Operațiunile de proiect, septembrie 2021 pentru scenariile stocate/bazate pe producție
description: Acest articol oferă informații despre actualizările de calitate care sunt disponibile în versiunea din septembrie 2021 a Operațiunilor de proiect pentru scenariile stocate/bazate pe producție.
author: andchoi
ms.date: 11/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: andchoi
ms.openlocfilehash: 1e99471b4338209c1f7fe411084d1745d74b2d2c
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916533"
---
# <a name="whats-new-or-changed-in-project-operations-september-2021-for-stockedproduction-based-scenarios"></a>Ce este nou sau schimbat în Operațiunile de proiect, septembrie 2021 pentru scenariile stocate/bazate pe producție

_**Se aplică la:** Project Operations pentru scenariile bazate pe stocuri/producție_

Acest articol se aplică următoarelor componente și versiuni ale Microsoft Dynamics 365 Project Operations:

- Management de proiect și contabilitate într-un mediu Dynamics 365 Finance versiunea 10.0.21
 
## <a name="quality-updates"></a>Actualizări de calitate

| Zonă de caracteristici | Număr de referință | Actualizare de calitate |
|---|---|---|
| Management de proiect și contabilitate | [412077](https://fix.lcs.dynamics.com/Issue/Details/?bugId=412077) | Dacă rolului de manager de achiziții i se oferă acces la o singură entitate juridică, acesta obține și acces la toate proiectele din toate entitățile juridice. |
| Management de proiect și contabilitate | [537214](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537214) | O problemă de rotunjire a taxei pe valoarea adăugată (TVA) apare în timp ce o notă de credit este decontată cu o factură de proiect originală. |
| Management de proiect și contabilitate | [538002](https://fix.lcs.dynamics.com/Issue/Details/?bugId=538002) | Utilizați un buget de proiect alternativ pentru verificarea bugetului. |
| Management de proiect și contabilitate | [546265](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546265) | The **Pret de vanzare ora** grupul de preț nu este calculat pe structura defalcării lucrărilor pentru ofertele de proiecte. |
| Management de proiect și contabilitate | [555604](https://fix.lcs.dynamics.com/Issue/Details/?bugId=555604) | Eliminarea estimării eșuează atunci când **Activați moneda contractului de proiect pentru calcularea estimării** caracteristica este activată. |
| Management de proiect și contabilitate | [563523](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563523) | Factorizarea taxei pe vânzări în funcție de cantitate este adăugată la valoarea prețului de vânzare atunci când taxa de utilizare este utilizată în grupul de taxe pe vânzări din jurnalul de cheltuieli de proiect. |
| Management de proiect și contabilitate | [564701](https://fix.lcs.dynamics.com/Issue/Details/?bugId=564701) | Taxa condiționată nu este calculată corect pentru ultima plată atunci când reținerea furnizorului și plata anticipată sunt aplicate facturilor pentru comenzile de achiziție. |
| Management de proiect și contabilitate | [565642](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565642) | Urmărirea ajustării nu funcționează pentru jurnalele de sold de început. |
| Management de proiect și contabilitate | [568814](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568814) | **Alocarea revizuirii bugetului proiectului pe perioadă** este împărțit în toate perioadele bugetare. Când alocarea este trimisă, înregistrarea nu este șters. |
| Management de proiect și contabilitate | [569250](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569250) | Înregistrările de lucru în curs (WIP) în registrul general au o sumă incorectă. |
| Management de proiect și contabilitate | [570731](https://fix.lcs.dynamics.com/Issue/Details/?bugId=570371) | Aprobarea jurnalului de oră al proiectului nu funcționează. |
| Management de proiect și contabilitate | [571391](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571391) | Prețul de vânzare pentru ajustarea proiectului nu este actualizat cu costuri indirecte atunci când limita de finanțare este nemarcată. |
| Management de proiect și contabilitate | [575831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575831) | O cerință de articol nu poate fi creată atunci când antetul tabelului de vânzări este facturat și comanda de achiziție de rezervă pentru liniile existente a fost finalizată. |
| Management de proiect și contabilitate | [578036](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578036) | Suma de reținere pentru o regulă de facturare care are o etapă pentru un proiect diferit nu este publicată în ID-ul de proiect corespunzător care a fost selectat pentru reper. În schimb, este postat cu primul proiect. |
| Management de proiect și contabilitate | [578327](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578327) | Când selectezi **Set de dimensiuni financiare** la o propunere de factură, apare următoarea eroare: „Imposibil de difuzat obiectul de tip „Dynamics.AX .Application.FormIntControl' pentru a tasta 'Dynamics.AX .Application.FormStringControl'." |
| Management de proiect și contabilitate | [581167](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581167) | The **Factura de proiect** raportul omite rânduri. |
| Management de proiect și contabilitate | [581489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581489) | Apare o eroare atunci când calculați controlul costurilor pentru un proiect de investiții. |
| Management de proiect și contabilitate | [590357](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590357) | The **ProjTable:: InitFromCustTable - canDeletePostalAddress** metoda cauzează o problemă de performanță. |
| Management de proiect și contabilitate | [592493](https://fix.lcs.dynamics.com/Issue/Details/?bugId=592493) | Mesajul de eroare ar trebui să fie mai clar decât „Eroare neașteptată”. |
| Management de proiect și contabilitate | [598810](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598810) | Încărcarea facturii Proiect procesează și înregistrează oferta de factură în lot, chiar dacă liniile de factură nu au fost generate. |
| Management de proiect și contabilitate | [574282](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574282) | O problemă de rotunjire apare atunci când cheia de configurare a licenței din sectorul public este dezactivată. Un cost sau un preț de vânzare incorect este generat în orele de pontaj pentru contractele care au mai multe surse de întemeiere. |
| Management de proiect și contabilitate | [577598](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577598) | Prețul de vânzare al proiectului pentru o comandă de achiziție de proiect facturată este calculat incorect atunci când modelul prețului de vânzare este **Raportul de contribuție**. |
| Management de proiect și contabilitate | [580784](https://fix.lcs.dynamics.com/Issue/Details/?bugId=580784) | Sistemul nu ia în considerare zilele active intermediare atunci când calculează rata efectivă de muncă pentru un angajat. |
| Management de proiect și contabilitate | [584054](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584054) | Apare o eroare de postare pe foaia de pontaj intercompanie din cauza următoarei erori de validare: „Niciun partener comercial nu este configurat pentru entitate juridică”. |
| Management de proiect și contabilitate | [586303](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586303) | Descrierea dintr-o comandă de achiziție care are o categorie de cheltuieli nu este preluată în lista de tranzacții de proiect publicată. |
| Management de proiect și contabilitate | [590349](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590349) | Există o conversie incorectă în jurnalele de articole care sunt postate într-un proiect. |
| Management de proiect și contabilitate | [557294](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557294) | Puteți confirma o comandă de cumpărare chiar dacă limita de finanțare a fost depășită. |
| Management de proiect și contabilitate | [574162](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574162) | The **Rectificare/Anulare factura** secțiunea de pe o factură cu text liber dispare atunci când este selectat un ID de proiect. |
| Management de proiect și contabilitate | [575425](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575425) | Există probleme de performanță atunci când o propunere de factură de proiect este postată dintr-o comandă de vânzare de proiect care include un articol stocat. |
| Management de proiect și contabilitate | [575939](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575939) | Facturile de achiziție pentru proiecte nu pot fi încărcate deoarece apare următoarea eroare: „Funcția AccDistProcessorProjectExtension.createForProjectRevenueLine a fost apelată incorect”. |
| Management de proiect și contabilitate | [578970](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578970) | Actualizare pentru crearea de joburi lot de estimare a proiectului pentru a sprijini executarea mai multor subsarcini. |
| Management de proiect și contabilitate | [584519](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584519) | Starea unei foi de pontaj nu poate fi actualizată la **Proiect** când fluxul de lucru este blocat într-o **Anulat** stat. |
| Management de proiect și contabilitate | [584757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584757) | Sumele de reținere nu sunt calculate în propunerea de factură cu nota de credit dacă există mai multe rânduri. |
| Management de proiect și contabilitate | [586034](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586034) | Când încercați să modificați suma de pe o factură generată dintr-o comandă de achiziție, apare următoarea eroare: „Tranzacțiile pe voucher nu se echilibrează conform XX/XX/XXXX. (monedă contabilă: 0,00 - monedă de raportare: 0,01).” |
| Management de proiect și contabilitate | [588714](https://fix.lcs.dynamics.com/Issue/Details/?bugId=588714) | Există o problemă de performanță atunci când o propunere de factură de proiect este postată în modul lot, din cauza unirii cu **GeneralJournalAccountEntry**. |
| Management de proiect și contabilitate | [588851](https://fix.lcs.dynamics.com/Issue/Details/?bugId=588851) | Există probleme de performanță atunci când o foaie de pontaj este postată. |
| Management de proiect și contabilitate | [590535](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590535) | Ierarhia estimărilor de cost a structurii de defalcare a muncii nu este aliniată corect după ce toate sarcinile sunt extinse sau după ce o singură sarcină este extinsă manual. |
| Management de proiect și contabilitate | [593663](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593663) | Șablonul Excel pentru oferta de proiect nu poate fi adăugat la **Deschideți în Excel** meniul. |
| Management de proiect și contabilitate | [596669](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596669) | Numărul scutit de taxe pentru o entitate juridică nu este inclus pe factura de proiect tipărită. |
| Management de proiect și contabilitate | [597563](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597563) | Nu se actualizează date financiare în eroarea unității de inventar atunci când un proiect este ajustat în raport cu liniile de credit. |
| Management de proiect și contabilitate | [598109](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598109) | După ce aplicați KB 461935, nu puteți posta estimări dacă treceți la secvențe de numere continue. |
| Management de proiect și contabilitate | [598688](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598688) | **TimeEntryDataManager** provoacă aplicația mobilă pentru foaia de pontaj proiect pentru Android a nu mai răspunde. |
| Management de proiect și contabilitate | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | Valoarea WIP inversată dintr-o înregistrare a facturii diferă de valoarea WIP postată inițial din momentul introducerii. |
| Management de proiect și contabilitate | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | În cazurile de reținere aplicată, tranzacțiile pe un voucher nu se echilibrează atunci când sunt înregistrate veniturile facturate pentru un proiect. |
| Management de proiect și contabilitate | [603320](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603320) | Cand **Îmbunătățirea performanței în planificarea resurselor proiectului** caracteristica este activată, valorile zecimale sunt rotunjite incorect pentru disponibilitatea resurselor și capacitatea. |
| Management de proiect și contabilitate | [607324](https://fix.lcs.dynamics.com/Issue/Details/?bugId=607324) | Cand **Creați estimări de proiect folosind mai multe sarcini lot** caracteristica este activată, crearea estimărilor într-un lot care are mai multe subsarcini funcționează numai pentru perioada curentă. |
| Deplasări și cheltuieli | [551911](https://fix.lcs.dynamics.com/Issue/Details/?bugId=551911) | O politică de solicitare de călătorie este ignorată, iar fluxul de lucru este aprobat fără erori. |
| Deplasări și cheltuieli | [563752](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563752) | <p>Aplicația Mobile Expense nu salvează următoarele informații pe linia de cheltuieli:</p><ul><li>ID-ul proiectului</li><li>Dacă cheltuiala este facturabilă</li><li>Numărul activității</li></ul> |
| Deplasări și cheltuieli | [569458](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569458) | The **Chitanțe atașate** câmpul este setat la **da** chiar dacă nicio chitanță nu este atașată liniei de cheltuieli. |
| Deplasări și cheltuieli | [571334](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571334) | Apare o eroare când schimbați categoria de cheltuieli în **Personal**. |
| Deplasări și cheltuieli | [572783](https://fix.lcs.dynamics.com/Issue/Details/?bugId=572783) | Nu puteți atașa o chitanță și modifica cheltuielile părintelui după ce o tranzacție cu cardul de credit este împărțită într-o cheltuială personală. |
| Deplasări și cheltuieli | [574252](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574252) | Politica de cheltuieli pentru tranzacțiile între companii care au un ID de proiect nu funcționează corect. |
| Deplasări și cheltuieli | [574489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574489) | Informațiile despre data publicată lipsesc pentru rapoartele de cheltuieli publicate. |
| Deplasări și cheltuieli | [574504](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574504) | Există probleme legate de metoda de plată în aplicația mobilă Expense. |
| Deplasări și cheltuieli | [584799](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584799) | O solicitare de călătorie creată pentru un lucrător poate fi utilizată pentru raportul de cheltuieli al altui lucrător înainte de data delegatului. |
| Deplasări și cheltuieli | [586023](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586023) | Când creați o cheltuială, modificările la valorile dimensiunii financiare nu sunt actualizate corect la nivel de distribuție contabilă în **Managementul cheltuielilor** spațiu de lucru. |
| Deplasări și cheltuieli | [586081](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586081) | Starea de aprobare a liniei principale de cheltuieli nu este sincronizată cu starea de aprobare a fluxului de lucru detaliat. |
| Deplasări și cheltuieli | [590544](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590544) | Apare o eroare dacă publicați un raport de cheltuieli și recuperarea taxelor este activată. |
| Deplasări și cheltuieli | [564851](https://fix.lcs.dynamics.com/Issue/Details/?bugId=564851) | Un delegat nu poate șterge documentele de cheltuieli pentru un angajat revocat. |
| Deplasări și cheltuieli | [587306](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587306) | Ștergerea unei linii de cheltuieli durează mai mult decât se aștepta și afectează performanța. |
| Deplasări și cheltuieli | [600455](https://fix.lcs.dynamics.com/Issue/Details/?bugId=600455) | **TrvExpTrans** provoacă un orfan **TaxUncommitted** înregistrare, pentru că numai **SourceDocumentLine** este șters. |
| Deplasări și cheltuieli | [609918](https://fix.lcs.dynamics.com/Issue/Details/?bugId=609918) | **ReleaseUpdateDB72_Expense.updateTrvExpTransProjTransId()** nu onorează **trvExpTrans.ReferenceDataAreaId** pentru a crea noua secvență de numere. |

## <a name="regulatory-updates"></a>Actualizări de reglementare

Pentru informații despre actualizările de reglementare pentru aplicațiile Finance and Operations, consultați [Actualizări de reglementare](/dynamics365/finance/localizations/regulatory-updates). De asemenea, vă puteți conecta la Microsoft Dynamics Lifecycle Services (LCS) și utilizați instrumentul de căutare a problemelor pentru a vedea actualizările de reglementare planificate. Căutarea problemelor vă permite să căutați după țară sau regiune, tip de caracteristică și versiune.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
