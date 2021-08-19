---
title: Contracte de proiect
description: Acest subiect oferă exemple de contracte de proiect pe care le puteți crea pentru diferite tipuri de proiecte și surse de finanțare și modul în care puteți gestiona contracte și factura clienții proiectului.
author: Yowelle
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectContractsListPage, ProjProjectsListPage
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1b92668c38071e8b1afdee9a79fd4a25190248ada30380bfb79054a6dc587f95
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/06/2021
ms.locfileid: "7001041"
---
# <a name="project-contracts"></a>Contracte de proiect

[!include [banner](../includes/banner.md)]

Acest articol furnizează exemple de contracte de proiect pe care le puteți crea pentru diferite tipuri de proiecte și surse de finanțare și modul în care puteți gestiona contracte și factura clienții proiectului.

Tipul de proiect pe care îl creați pentru un contract de proiect determină metoda utilizată pentru a factura clienții proiectului. Puteți modifica un contract de proiect și proiectul aferent, dar nu puteți modifica tipul de proiect. 

Utilizând un contract de proiect, puteți factura unul sau mai multe proiecte în același timp. De asemenea, contractul de proiect garantează o procedură de facturare consecventă pentru fiecare subproiect dintr-o structură de proiect. 

Fiecare proiect care va fi facturat trebuie să fie asociat cu un contract de proiect. Setările pentru un contract de proiect se aplică tuturor proiectelor și subproiectelor care sunt asociate cu acel contract de proiect. 

Un contract de proiect poate specifica una sau mai multe surse de finanțare. Prin urmare, puteți împărți facturarea între mai mulți finanțatori, setați limite de finanțare astfel încât sursele de finanțare să nu fie facturate mai mult decât o sumă specificată și să configurați reguli de finanțare pentru perceperea cheltuielilor.

## <a name="funding-for-project-contracts"></a>Finanțarea contractelor de proiect
Unele contracte de proiect specifică faptul că mai multe părți împart responsabilitatea pentru finanțarea costurilor proiectului. Iată câteva exemple:

-   Un client mare care are mai multe divizii solicită ca finanțarea unui proiect să fie împărțită pe divizii.
-   Compania dvs. împarte costurile unui proiect mare cu o organizație externă.
-   Un proiect rutier este cofinanțat de două municipalități.
-   Un proiect de pod este finanțat de o subvenție guvernamentală și de o corporație privată.

În Dynamics 365 Finance, puteți împărți facturarea pentru o singură tranzacție sau un întreg proiect între mai mulți clienți, subvenții sau organizații. 

În proiectele care au mai mulți finanțatori, toate părțile care contribuie la finanțarea unui proiect avansat de finanțare sunt numite surse de finanțare. După ce un client, o organizație sau o bursă este definit ca sursă de finanțare, acesta poate fi atribuit uneia sau mai multor reguli de finanțare. Regulile de finanțare conțin criteriile care determină modul în care taxele sunt alocate diferitelor surse de finanțare pentru un proiect. 

Deoarece articolele stocate, cum ar fi cele care apar în cererile de achiziție și comenzile de cumpărare, nu pot fi împărțite, suma costului nu poate fi împărțită între mai multe surse de finanțare în momentul distribuției. Prin urmare, valoarea sursei de finanțare rămâne 0 (zero) până la publicarea emisiunii de inventar. Când este înregistrată problema inventarului, suma costului este distribuită conform regulilor de distribuire a contului pentru proiect.

Iată câțiva pași pe care îi puteți face pentru a facilita împărțirea facturării între mai multe surse de finanțare:

-   Specificați că toate tranzacțiile introduse pentru un proiect utilizează aceeași monedă de vânzare ca și contractul de proiect.
-   Stabiliți limite de finanțare, astfel încât o sursă de finanțare să nu fie facturată mai mult decât o sumă specificată pentru un proiect.
-   Configurați regulile de finanțare și limitele de finanțare pentru fiecare lucrător, articol, categorie, grup de categorii și tip de tranzacție (sau pentru toate tipurile de tranzacții).
-   Selectați datele opționale de începere și de încheiere pentru a defini perioada în care fiecare regulă de finanțare este valabilă.
-   Specificați procentul de care este responsabilă fiecare sursă de finanțare.
-   Specificați ce sursă de finanțare este responsabilă pentru rotunjirea diferențelor cauzate de calculele alocării finanțării.
-   Stabiliți reguli care determină modul în care costurile proiectului sunt facturate clienților externi și taxate către organizațiile interne.
-   Înregistrați tranzacțiile într-un cont de finanțare în așteptare până când se poate obține finanțare suplimentară sau până când decideți să suportați costurile pe plan intern.

Pentru a determina ce grup fiscal se asociază cu o tranzacție, proiectul este căutat pentru o atribuire de grup fiscal. Dacă nu a fost efectuată nicio atribuire de grup fiscal la nivelul proiectului, se caută contractul de proiect.

### <a name="example-multiple-funding-sources-simple"></a>Exemplu: mai multe surse de finanțare (simple)

Tabelul următor oferă scenarii pentru gestionarea alocării finanțării între mai multe surse de finanțare. Aceste scenarii se bazează pe următoarele ipoteze:

-   Setările prioritare sunt luate în considerare în alocarea fondurilor înainte de aplicarea altor criterii de regulă de finanțare.
-   Nu a fost specificat niciun interval de date pentru a defini perioada când regula de finanțare este valabilă.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Scenariu</strong></td>
<td><strong>Sursă de finanțare</strong></td>
<td><strong>Procentul de alocare</strong></td>
<td><strong>Prioritate de alocare</strong></td>
</tr>
<tr class="even">
<td>Doriți să alocați costurile unei surse de finanțare până la epuizarea fondurilor sale, alocați costurile unei a doua surse de finanțare până la epuizarea fondurilor sale și, în cele din urmă, alocați costurile rămase la o a treia sursă de finanțare.</td>
<td><ul>
<li>Sursă de　finanțare　1</li>
<li>Sursă de　finanțare　2</li>
<li>Sursă de　finanțare　3</li>
</ul></td>
<td><ul>
<li>100%</li>
<li>100%</li>
<li>100%</li>
</ul></td>
<td><ul>
<li>1</li>
<li>2</li>
<li>3</li>
</ul></td>
</tr>
<tr class="odd">
<td>Doriți să alocați 75% din costuri unei surse de finanțare și 25% unei alte surse de finanțare. Când oricare dintre aceste surse de finanțare este epuizată, doriți să plătiți costurile rămase dintr-o a treia sursă de finanțare.</td>
<td><ul>
<li>Sursă de　finanțare　1</li>
<li>Sursă de　finanțare　2</li>
<li>Sursă de　finanțare　3</li>
</ul></td>
<td><ul>
<li>75%</li>
<li>25%</li>
<li>100%</li>
</ul></td>
<td><ul>
<li>1</li>
<li>1</li>
<li>2</li>
</ul></td>
</tr>
<tr class="even">
<td>Doriți să alocați 75% din costuri unei surse de finanțare și 25% unei alte surse de finanțare. Când oricare dintre aceste surse de finanțare este epuizată, doriți să împărțiți costurile rămase între o a treia sursă de finanțare și o a patra sursă de finanțare.</td>
<td><ul>
<li>Sursă de　finanțare　1</li>
<li>Sursă de　finanțare　2</li>
<li>Sursă de　finanțare　3</li>
<li>Sursă de　finanțare　4</li>
</ul></td>
<td><ul>
<li>75%</li>
<li>25%</li>
<li>50%</li>
<li>50%</li>
</ul></td>
<td><ul>
<li>1</li>
<li>1</li>
<li>2</li>
<li>2</li>
</ul></td>
</tr>
<tr class="odd">
<td>Doriți să alocați primii 25% din costuri unei surse de finanțare și restul unei a doua surse de finanțare.</td>
<td><ul>
<li>Sursă de　finanțare　1</li>
<li>Sursă de　finanțare　2</li>
</ul></td>
<td><ul>
<li>25%</li>
<li>100%</li>
</ul></td>
<td><ul>
<li>1</li>
<li>2</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="example-multiple-funding-sources-complex"></a>Exemplu: mai multe surse de finanțare (complexe)

Aveți trei surse de finanțare pe care doriți să le utilizați în următoarea ordine:

1.  Utilizați sursa de finanțare 2 și sursa de finanțare 3 în mod egal până când sursa de finanțare 2 este epuizată.
2.  Continuați să utilizați sursa de finanțare 3 până când aceasta este epuizată.
3.  Utilizați sursa de finanțare 1 după ce sursa de finanțare 3 este epuizată.

Pentru a realiza acest obiectiv, trebuie să faceți următoarele:

-   Stabiliți limite de finanțare pentru sursa de finanțare 2 și sursa de finanțare 3, pentru sumele respective.
-   Creați următoarele reguli de finanțare:
    -   Regula 1 (Prioritatea1): Alocați 50% din tranzacții la sursa de finanțare 2 și 50% la sursa de finanțare 3.
    -   Regula 2 (Prioritatea 2): Alocați 100% din tranzacții sursei de finanțare 3.
    -   Regula 3 (Prioritatea 3): Alocați 100% din tranzacții sursei de finanțare 1.

Această configurare funcționează deoarece tranzacțiile sunt verificate în raport cu regulile și limitele pentru a determina dacă oricare dintre acestea se aplică tranzacției. Dacă nu se aplică reguli sau limite specifice tranzacției, se aplică regula Toate tranzacțiile. Regula Toate tranzacțiile corespunde tuturor tranzacțiilor. 

Dacă se găsește o regulă care se potrivește cu o tranzacție, procentul care a fost alocat în regula respectivă se aplică mai întâi, dar numai după ce meciurile sunt verificate în raport cu orice limite care au fost stabilite. Dacă a fost atinsă o limită și fondurile unei surse de finanțare sunt epuizate, regula de finanțare care este asociată cu limita de finanțare este ignorată, iar programul verifică următoarea regulă care se aplică. 

În unele cazuri, numai o parte a unei tranzacții poate fi alocată conform unei reguli. Acest lucru se poate întâmpla deoarece o limită este atinsă atunci când tranzacția este alocată. În acest caz, numai o anumită sumă este alocată în conformitate cu regula respectivă, cum ar fi 50 la sută pentru fiecare sursă de finanțare. Acesta este cazul în regula 1, care este descrisă mai devreme în această secțiune. Restul este alocat în conformitate cu următoarea regulă din secvență. 

Tabelul următor examinează acest scenariu în detaliu.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Focus</strong></td>
<td><strong>Detalii</strong></td>
</tr>
<tr class="even">
<td>Reguli de finanțare</td>
<td><ul>
<li>Regula 1 (Prioritatea 1): Toate tranzacțiile. Alocați sursa de finanțare 2 la 50% și sursa de finanțare 3 la 50%.</li>
<li>Regula 2 (Prioritatea 2): Toate tranzacțiile. Alocați sursa de finanțare 3 la 100%.</li>
<li>Regula 3 (Prioritatea 2): Toate tranzacțiile. Alocați sursa de finanțare 1 la 100%.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Limite de finanțare</td>
<td><ul>
<li>Sursa de finanțare 1 limită = 10.000</li>
<li>Limita sursei 2 de finanțare = 500.00</li>
<li>Limita sursei 3 de finanțare = 750.00</li>
</ul></td>
</tr>
<tr class="even">
<td>Tranzacție 1</td>
<td><strong>Suma tranzacției:</strong> 100.00<strong>Finanțare:</strong> Tranzacția este plătită numai conform regulii 1, deoarece tranzacția este plătită integral după aplicarea regulii 1. Tranzacția este finanțată în mod egal între sursa de finanțare 2 și sursa de finanțare 3.
<ul>
<li>Sursa de finanțare 2: 50.00</li>
<li>Sursa de finanțare 3: 50.00</li>
</ul></td>
</tr>
<tr class="odd">
<td>Tranzacție 2</td>
<td><strong>Suma tranzacției:</strong> 5.000.00<strong>Finanțare:</strong> Tranzacția este plătită în conformitate cu toate cele trei reguli. <strong>Regula 1</strong>
<ul>
<li>Sursa de finanțare 2: 450.00</li>
<li>Sursa de finanțare 3: 450.00</li>
</ul>
<strong>Regula 2</strong>
<ul>
<li>Sursa de finanțare 3: 250.00 (= 750.00 – 50.00 – 450.00)</li>
</ul>
<strong>Regula 3</strong>
<ul>
<li>Sursă de finanțare 1: 3.850.00 (= 5.000.00 – 450.00 – 450.00 – 250.00)</li>
</ul></td>
</tr>
<tr class="even">
<td>Totalul fondurilor distribuite pentru fiecare sursă de finanțare</td>
<td><ul>
<li>Sursa de finanțare 1: 3.850.00</li>
<li>Sursa de finanțare 2: 500.00</li>
<li>Sursa de finanțare 3: 750.00</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="billing-rules"></a>Regulile de facturare
Când negociați un contract de proiect cu un client, definiți cum și când puteți factura clientul pentru munca la un proiect. După ce configurați contractul de proiect și proiectul, puteți seta reguli de facturare pentru proiect. Regulile de facturare se bazează pe termenii proiectului specificați în contractul de proiect. Regulile de facturare pe care le puteți crea depind de termenii contractului de proiect și de tipul de proiect, cum ar fi Timpul și materialul sau Prețul fix, pe care le asociați cu regula de facturare. Puteți crea mai multe reguli de facturare pentru un contract de proiect. De asemenea, puteți atribui o regulă de facturare mai multor proiecte care sunt asociate cu același contract de proiect și care au condiții de facturare similare. 

Puteți configura următoarele tipuri de reguli de facturare:

-   **Unitatea de livrare** - Facturați un client atunci când finalizați o unitate de livrare. Definiți unitățile de livrare în contract.
-   **Progres** - Facturați un client atunci când finalizați un procent specificat din proiect. Puteți configura o regulă de facturare pentru a calcula automat procentul de muncă finalizată sau puteți calcula manual procentul de muncă finalizată și suma de facturare a clientului.
-   **Jalon** - Facturați un client pentru suma totală a unui proiect de referință la atingerea acestuia.
-   **Taxă** - Facturați un client pentru serviciile dvs. plus o taxă de administrare, care este de obicei un procent din costul serviciilor.
-   **Timp și material** - Facturați un client pentru valoarea timpului și a materialelor utilizate pentru un proiect.

Pentru toate tipurile de reguli de facturare, puteți specifica un procent de păstrare care se deduce din facturile clienților până când un proiect ajunge la o etapă convenită. Procentul de păstrare a plăților este specificat în contractul de proiect. Suma se calculează pe baza și se scade din valoarea totală a liniilor dintr-o factură de client. 

Pentru regulile de facturare **Timp și material** și **Progres**, puteți atribui categorii taxabile. Categoriile taxabile indică tranzacțiile care ar trebui incluse în facturile clienților. 

Când sunteți gata să facturați clientul, suma de facturat pentru proiect este calculată pe baza regulilor de facturare și se generează o propunere de facturare a proiectului. 

Următoarele secțiuni oferă exemple care arată cum să configurați și să gestionați regulile de facturare pentru un proiect.

### <a name="example-create-a-billing-rule-that-is-based-on-the-number-of-units-delivered"></a>Exemplu: creați o regulă de facturare care se bazează pe numărul de unități livrate

Organizația dvs. încheie un acord pentru a furniza în total cinci sesiuni de instruire angajaților unui client la un cost de 10.000 pe sesiune de instruire. Facturați clientul după fiecare sesiune de instruire. 

Când configurați regulile de facturare pentru contract, utilizați următoarele valori:

-   Unitatea de livrare este o sesiune de antrenament.
-   Prețul unitar este de 10.000 pe sesiune de antrenament.
-   Numărul total de unități este de cinci sesiuni de antrenament.

După ce ați finalizat o sesiune de instruire, puteți crea o factură pentru 10.000, pentru prima unitate care a fost livrată și puteți trimite factura către client.

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-manual-calculation"></a>Exemplu: creați o regulă de facturare care se bazează pe un procent specificat de finalizare a proiectului (calcul manual)

Organizația dvs., o firmă de consultanță software, încheie un acord cu un client pentru a dezvolta o parte a unui produs pe care acesta îl dezvoltă. Organizația dvs. este de acord să livreze codul software pe o perioadă de șase luni. Clientul este de acord să plătească organizației dvs. un total de 100.000 pentru lucrări. Creați o regulă de facturare pentru a factura clientul pe baza procentajului de muncă finalizat pe proiect, așa cum se specifică în contract.

-   La sfârșitul primei luni, vă întâlniți cu clientul pentru a determina procentul de muncă finalizată. După ce dvs. și clientul examinați proiectul, decideți că proiectul este finalizat cu 15%.
-   Creați o factură pentru 15.000 (15 la sută din 100.000) și o trimiteți clientului.

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-automatic-calculation"></a>Exemplu: creați o regulă de facturare care se bazează pe un procent specificat de finalizare a proiectului (calcul automat)

Organizația dvs., o firmă de dezvoltare software, este de acord să dezvolte un pachet de contabilitate a salariilor pentru un client pentru 30.000. Clientul este de acord să plătească organizației dvs. pe baza procentului de lucru finalizat. Estimați că costurile proiectului sunt de 20.000. Contractul de proiect specifică categoriile de lucrări pe care le utilizați în procesul de facturare. Configurați reguli de facturare care calculează automat sumele facturii pentru procentul de muncă finalizat pentru fiecare categorie. Configurați un buget pentru fiecare categorie:

-   **Dezvoltare** - Cost de 15.000 și venituri de 20.000
-   **Instalare** - Cost de 5.000 și venituri de 10.000

Când creați o factură pentru client pentru prima dată, suma facturii este calculată automat pe baza următoarelor informații:

-   După o lună, lucrătorul din proiect transmite o foaie de timp pentru proiect. Costul orelor lucrătorului este de 5.000 pentru dezvoltare și 1.000 pentru instalare. Lucrările de dezvoltare sunt finalizate cu 33% (5.000 de costuri reale/15.000 de costuri bugetare), iar lucrările de instalare sunt finalizate cu 20% (1.000 de costuri reale/5.000 de costuri bugetare).
-   Suma facturii de 8.667 este calculată automat (33% din 20.000 + 20% din 10.000).
-   Creați o factură pentru 8.667 și o trimiteți clientului.

### <a name="example-create-a-billing-rule-that-is-based-on-agreed-upon-milestones"></a>Exemplu: creați o regulă de facturare bazată pe repere convenite

Organizația dvs., o firmă de consultanță în management, este de acord să efectueze cercetări de piață pentru un produs de consum pe care clientul intenționează să îl vândă. Clientul este de acord să utilizeze serviciile dvs. pentru o perioadă de trei luni, începând cu luna martie, și este de acord să plătească organizației dvs. 50.000. Proiectul are trei jaloane:

-   Etapa 1: Colectați date despre consumatori - 31 martie
-   Etapa 2: Analizați datele consumatorilor - 30 aprilie
-   Etapa 3: Prezentați o propunere de viabilitate a produsului - 31 mai

Clientul este de acord să plătească organizației dvs. 10.000 pentru primul jalon, 20.000 pentru al doilea jalon și 20.000 pentru al treilea jalon. 

Când configurați contractul de proiect, sunteți de acord să facturați clientul pe baza etapei care a fost finalizată. Configurarea regulii de facturare include următorii pași:

-   Definiți etapele proiectului.
-   Definiți suma de facturat clientului la finalizarea fiecărei etape.

Când prima etapă este finalizată la 31 martie, marcați etapa ca fiind finalizată, apoi creați o factură pentru 10.000 și o trimiteți clientului. Nu puteți crea o factură pentru o etapă de referință până când nu ați marcat această etapă ca fiind finalizată.

### <a name="example-create-a-billing-rule-that-is-based-on-services-plus-a-management-fee"></a>Exemplu: creați o regulă de facturare care se bazează pe servicii plus o taxă de administrare

Organizația dvs., o firmă de consultanță în management, este de acord să efectueze studii de piață pentru a evalua viabilitatea unui produs pe care clientul, o companie de retail, îl dezvoltă. Termenii acordului specifică faptul că veți furniza serviciile primilor dvs. trei consultanți în management, care vor efectua cercetările în funcție de timp și materiale. Clientul este de acord să plătească 100 pe oră, plus o taxă de administrare de 10% pentru orele de consultanță care sunt taxate pentru proiect. 

Când configurați contractul de proiect, creați o regulă de facturare pentru a adăuga o taxă de administrare de 10% la orele de consultanță care sunt taxate proiectului. 

Atunci când creați o factură pentru client, clientul primește o taxă de administrare de 10% plus costul orelor de consultanță. De exemplu, dacă cei trei consultanți au lucrat în total 200 de ore la proiect, se creează o factură pentru 22.000 pe baza următorului calcul:

-   200 de ore la 100 pe oră = 20.000
-   10% comision de administrare = 2.000
-   Suma totală a facturii = 22.000

Dacă taxele sunt impozabile pentru un client și selectați un grup de taxe pe vânzări în contractul de proiect, grupul de taxe pe vânzări este introdus automat într-o regulă de facturare pentru taxe.

### <a name="example-create-a-billing-rule-for-the-value-of-time-and-materials"></a>Exemplu: creați o regulă de facturare pentru valoarea timpului și a materialelor

Organizația dvs., o firmă de consultanță software, este de acord să ofere cinci consultanți tehnici pentru a lucra la un proiect de dezvoltare software pentru un client pentru următoarele șase luni. Clientul este de acord să plătească 150 pentru fiecare oră de consultanță, plus costul materialelor de birou. Organizația dvs. trimite o factură către client la sfârșitul fiecărei luni. 

Când stabiliți contractul de proiect, sunteți de acord să facturați lunar clientului timpul și materialele aferente proiectului. Creați o regulă de facturare care include următoarele informații:

-   Perioada contractului este de șase luni.
-   Timpul de consultare este calculat la o rată de 150 pe oră.
-   Materialele de birou sunt facturate la cost, iar costul total al proiectului nu trebuie să depășească 10.000.
-   Creați o factură pentru client la sfârșitul fiecărei luni calendaristice în timpul proiectului.

În prima lună, în total 800 de ore sunt înregistrate de consultanți în cadrul proiectului. Costul materialelor de birou care sunt taxate pentru proiect este de 2.000. Prin urmare, la sfârșitul lunii, creați o factură pentru 122.000, care este calculată ca 800 de ore la 150 pe oră, plus 2.000 pentru rechizite de birou.





[!INCLUDE[footer-include](../includes/footer-banner.md)]