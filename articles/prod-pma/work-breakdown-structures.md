---
title: Prezentare generală a structurilor detaliate ale proiectului
description: O structură detaliată a proiectului (WBS) este o descriere a lucrului care va fi făcut pentru un proiect. Este o ierarhie a sarcinilor care reprezintă înțelegerea echipei de proiect cu privire la compoziția muncii și la dimensiunea, costul și durata fiecărei componente sau sarcini.
author: Yowelle
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjWorkBreakdownStructure
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23861
ms.assetid: 241a0464-0056-4a69-b468-0afbe2d5f3ae
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 713e38f4218b980c4256e433e90c12adccd70e11
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012241"
---
# <a name="work-breakdown-structures-overview"></a>Prezentare generală a structurilor detaliate ale proiectului

[!include [banner](../includes/banner.md)]

O structură detaliată a proiectului (WBS) este o descriere a lucrului care va fi făcut pentru un proiect. Este o ierarhie a sarcinilor care reprezintă înțelegerea echipei de proiect cu privire la compoziția muncii și la dimensiunea, costul și durata fiecărei componente sau sarcini. Un WBS are trei scopuri majore:

-   Descrieți defalcarea sau compoziția muncii în sarcini.
-   Planificați munca proiectului.
-   Estimează costul fiecărei sarcini.

Gradul de detaliu într-o WBS depinde de nivelul de acuratețe care este necesar în estimări și de nivelul de urmărire care este necesar pentru aceste estimări. Proiectele care au o toleranță foarte scăzută pentru derapaje în planificare sau cost necesită, de obicei, un WBS mai detaliată și necesită, de asemenea, o urmărire diligentă a progresului și costurilor lucrărilor față de WBS. Acest tip de proiect este comun în industria construcțiilor și ingineriei. 

În schimb, proiectele din industrii precum media și publicitatea, software-ul și infrastructura IT tind să fie unice, iar productivitatea este relativă la experiența și competența individului care îndeplinește sarcina. Prin urmare, aceste industrii folosesc un WBS pentru a obține o aproximare a dimensiunii unui proiect, nu pentru a urmări în detaliu progresul proiectului respectiv. 

Construirea unui WBS este un proces intensiv care se face de obicei pe o perioadă lungă de timp și care necesită colaborare și informații de la o mare varietate de oameni. Acest subiect descrie modul în care puteți utiliza îmbunătățirile WBS pentru a satisface cerințele dvs. pentru estimări și urmărire.

## <a name="prerequisites-for-creating-a-wbs"></a>Cerințe preliminare pentru crearea unui WBS
Pentru a crea un WBS, trebuie să puteți crea un program de lucru și să estimați costul lucrului.

### <a name="prerequisites-for-creating-a-work-schedule"></a>Cerințe preliminare pentru crearea unui program de lucru

Pentru a utiliza capacitățile complete de programare ale caracteristicilor WBS, finalizați următoarea configurare:

1.  Configurați un calendar implicit și un calendar de proiect:
    1.  Faceți clic pe **Gestionarea proiectului și contabilitate** &gt; **Configurare** &gt; **Gestionarea proiectului și parametri de contabilitate** &gt; **Planificare**. În câmpul **Calendar de lucru implicit**, specificați un calendar implicit. Acesta va fi calendarul de lucru implicit pentru orice proiect nou creat.
    2.  Puteți modifica calendarul implicit pentru un anumit proiect. Faceți clic pe pagina de detalii a proiectului și apoi pe FastTab **Echipa proiectului și planificare**, actualizați câmpul **Calendarul de planificare** selectând un alt calendar.

2.  Configurați zilele și orele de lucru standard. Calendarul pe care l-ați setat ca calendar de lucru pentru proiectul dvs. va fi utilizat în WBS pentru a determina următoarele informații:

-   Zile lucrătoare și sărbători
-   Numărul de ore de lucru într-o zi

Pentru a configura zilele și orele de lucru pentru un calendar sau pentru a crea un calendar nou, faceți clic pe **Administrarea organizației** &gt; **Comun** &gt; **Calendare**.

### <a name="prerequisites-for-estimating-the-cost-of-work"></a>Condiții preliminare pentru estimarea costului de lucru

Pentru a utiliza capacitățile complete de estimare a costurilor WBS, ar trebui să configurați costurile și prețurile de vânzare pentru lucrători, categoriile de muncă, cheltuielile și taxele și articolele.

-   Pentru a configura costul și prețul de vânzare pentru categoriile de forță de muncă, cheltuieli și taxe, faceți clic pe **Management de proiect și contabilitate** &gt; **Configurare** &gt; **Prețuri**.
-   Pentru a configura costul și prețul de vânzare al articolelor, utilizați pagina **Acorduri comerciale** pentru fiecare element de pe pagina de listă **Produse lansate** în Gestionarea informațiilor despre produs.

## <a name="creating-a-wbs"></a>Crearea unui WBS
Crearea unui WBS implică trei activități:

1.  **Descompunerea lucrului** - Creați o defalcare a lucrului în bucăți sau sarcini gestionabile.
2.  **Program de lucru** - Estimați timpul necesar pentru finalizarea unei sarcini, setați interdependențele sarcinii și selectați datele de începere și de încheiere pentru sarcini.
3.  **Estimarea costurilor** - Estimarea costurilor pentru fiecare sarcină.

Următoarele secțiuni discută despre modul în care capabilitățile WBS pot ajuta la fiecare dintre aceste activități.

### <a name="work-decomposition"></a>Descompunerea muncii

Crearea unei defalcări sau descompuneri a muncii este de obicei primul pas în procesul de creare a unui WBS. Funcționalitatea WBS acceptă următoarele construcții de bază pentru defalcarea sau descompunerea lucrărilor. 

**Activitate rădăcină de proiect** Activitatea rădăcină de proiect este activitatea de rezumat de nivel superior pentru un proiect. Toate celelalte activități de proiect create sub acesta. Numele activității rădăcină este mereu setat la numele proiectului. Efortul, datele și durata nodului rădăcină rezumă valorile pentru sarcinile de sub sarcina rădăcină. Nu puteți modifica proprietățile nodului rădăcină sau să îl ștergeți.

**Sumar sau activități de container** O activitate de rezumat este o activitate care are sub-activități sau activități constitutive sub ea. O activitate rezumat nu are niciun efort de lucru sau cost propriu. În schimb, efortul de lucru și costul unei sarcini de sinteză sunt suma efortului de muncă și costul sarcinilor sale constitutive. Cea mai timpurie dată de început a activităților de membru este utilizată la data de început a activității de rezumat și cea mai târzie dată de final a sarcinilor de membru este utilizată la data de final. Puteți modifica numele unei activități de rezumat, dar nu puteți modifica proprietățile de planificare pentru efort, date și durată. Dacă ștergeți o activitate rezumat, ștergeți și toate activitățile sale membru. 

**Activități nod frunză** O activitate de nod frunză reprezintă cel mai granular pachet de lucru din proiect. Un nod frunză are un efort estimat, un număr planificat de resurse, o dată de început și de sfârșit planificată și durata. 

Puteți finaliza următoarele operațiuni ierarhice pentru a permite crearea unei ierarhii de lucru sau descompunere pentru un proiect. 

**Activitate nouă** Orice activitate nouă pe care o creați este adăugată automat sub nodul rădăcină și un număr WBS este atribuit automat activității. Numărul WBS reprezintă nivelul activității în ierarhie. Pentru activități în primul nivel sub activitatea rădăcină de proiect, se utilizează o schemă de numerotare de 1, 2, 3 și așa mai departe. Pentru activități care sunt sub primul nivel sub nodul rădăcină de proiect, se utilizează o schemă de numerotare de 1.1, 1.2, 1.3 și așa mai departe. Pentru fiecare nivel adăugat sub un nivel anterior, se adaugă o nouă serie de puncte de numere. 

În prezent, nu puteți personaliza numerotarea WBS. 

**Activitate de indentare** Când indentați o activitate, aceasta devine un fiu al activității care o precede. Numărul WBS al noii activități secundare este recalculat automat pe baza numărului WBS al noului său principal. Activitatea principală este acum un rezumat sau o activitate de recipient și, prin urmare, devine o acumulare a sarcinilor sale constitutive. 

> [!NOTE] 
> Când indentați activități sub o activitate care a fost un nod frunză înainte de operația de indentare, sarcina rezumativă recent creată își pierde propriile date, efort și numărul de resurse. Acum folosește un rezumat al valorilor noilor sale sarcini membre. 

**Activitate de identare negativă** Când identați negativ o activitate, nu mai este o activitate de membru a părintelui său. Numărul WBS al acestei activități este recalculat automat pentru a reflecta noul nivel al activității în ierarhie. Efortul, costul și datele activității părinte anterioare sunt recalculate astfel încât să excludă această activitate. 

**Mutați în sus și Mutați în jos** Când faceți clic pe **Mutați în sus** și **Mutați în jos**, schimbați poziția unei sarcini în ierarhia părintelui acesteia. Poziția unei activități nu afectează efortul activității, costul, datele sau durata. Cu toate acestea, numărul WBS al acestei activități este recalculat automat pentru a reflecta noua poziție a activității.

### <a name="schedule-estimation"></a>Estimarea planificării

Estimarea planificării este de obicei al doilea pas în crearea unui WBS. Ca cea mai bună practică, ar trebui să finalizați estimarea planificării după ce creați activitățile. Pagina **Structura detaliată a proiectului** din Finance are două secțiuni. Panoul superior este destinat estimării programului, iar panoul inferior include o filă **Costuri și venituri estimate** pe care o puteți utiliza pentru estimarea costurilor. 
**Dependențe de activități** Într-un WBS, puteți crea o relație predecesor între activități. Când atribuiți activități predecesoare unei activități, acea activitate poate să înceapă numai după ce toate activitățile predecesoare au fost terminate. Data de început planificată a activității este setată automat la cea mai recentă dată a tuturor predecesorilor săi. 

**Planificarea activităților** Următorii factori determină programarea activităților nodului frunză:

-   Predecesori
-   Efort
-   Numărul de resurse
-   Datele de sfârşit şi de început

Data de început a unei activități nod frunză care nu are predecesori este setată automat la data de început a planificării proiectului. Durata unei activități nod frunză se calculează întotdeauna ca numărul de zile lucrătoare dintre datele sale de început și de sfârșit. 

*<strong><em>Reguli de planificare</em></strong>* Când asistența de planificare automată este activată, următoarele reguli se aplică planificării sarcinilor pentru activitățile nodului frunză:

-   Datele de început și de sfârșit ale unei activități trebuie să fie întotdeauna zile lucrătoare, conform calendarului de planificare a proiectului.
-   Data de început a unei activități care are predecesori este setată automat la cea mai recentă dată de sfârșit a predecesorilor săi.
-   Efortul pentru o activitate este calculat automat după cum urmează:

Numărul de persoane x durata x numărul de ore într-o zi standard de lucru în calendarul de proiect. 

În unele cazuri, ați putea dori să vă abateți de la aceste reguli. Puteți dezactiva programarea automată pentru a împiedica Finance să seteze sau să corecteze automat orice proprietăți ale activităților nodului frunze. Când introduceți informații pentru o activitate care provoacă o încălcare a oricăror reguli de planificare, este afișată o pictogramă de eroare de planificare pentru activitate. Dacă nu doriți să fie afișate erori de planificare, faceți clic pe **Sunt afișate erorile de planificare** pentru a dezactiva caracteristica. 

> [!NOTE] 
> Valorile pentru un rezumat sau o sarcină de container continuă să fie calculate ca suma valorilor sarcinilor constitutive, indiferent dacă asistența de planificare automată este activată sau dezactivată. 

**Remedierea erorilor de planificare** Când asistența de planificare automată este activată, este posibil ca erorile de planificare să nu apară. Cu toate acestea, dacă dezactivați asistența de planificare automată și apoi o reporniți mai târziu, pictogramele de eroare de planificare pot apărea în WBS. 

**Remedierea erorilor de planificare după activitate** Când faceți dublu clic pe pictograma eroare de planificare pentru o anumită activitate, o casetă de dialog afișează toate erorile de planificare pentru acea activitate. Puteți decide ce erori de planificare să remediați pentru activitate. 

**Remedierea tuturor erorilor de planificare** Dacă doriți ca Finance să remedieze toate erorile de planificare din WBS, în panoul de acțiuni, faceți clic pe **Remediați toate discrepanțele de planificare**. 

> [!NOTE] 
> Această caracteristică poate provoca modificări semnificative ale WBS. Erorile sunt corectate în următoarea ordine:

1.  Efortul estimat pentru toate sarcinile este modificat astfel încât să fie egal cu capacitatea definită în calendarul proiectului.
2.  Data de începere a fiecărei sarcini este modificată astfel încât sarcina să înceapă după finalizarea tuturor sarcinilor sale predecesoare.
3.  Data de începere a fiecărei sarcini este modificată pentru a elimina golurile din datele de începere a sarcinilor predecesoare.

### <a name="cost-estimation"></a>Estimarea costurilor

După cum sa menționat mai devreme în acest document, introduceți estimarea costurilor pentru fiecare sarcină de nod frunză folosind fila **Costuri și venituri estimate** din panoul inferior al paginii **Structura detaliată a proiectului**. 

> [!NOTE] 
> Nu puteți modifica estimarea costurilor pentru un rezumat sau o sarcină de recipient. Estimarea costurilor pentru o sarcină sumară este egală cu suma estimării costurilor sarcinilor nodului frunză. Costul total estimat pentru fiecare sarcină este calculat ca suma sumelor costurilor estimate pentru următoarele tipuri de tranzacții:

-   Lucrare
-   Element sau material
-   Cheltuieli

Un tip de tranzacție **Taxă** este utilizat pentru a estima venitul bazat pe taxe. Acest tip de tranzacție nu are o componentă de cost și, prin urmare, nu este luat în considerare atunci când sunt estimate costurile. 

Un tip de tranzacție **În cont** este utilizat pentru înregistrarea valorii de vânzare contractate într-un tip de proiect cu valoare fixă. De asemenea, acest tip de tranzacție nu este luat în considerare atunci când sunt estimate costurile. 

Când estimați costurile pentru forță de muncă, materiale și cheltuieli pentru fiecare sarcină, trebuie să atribuiți o categorie de proiect la costul estimat. 

**Estimarea costurilor forței de muncă** Pentru fiecare sarcină de nod frunză, atribuiți un efort de lucru în ore și o categorie implicită. Prin urmare, când configurați un program pentru o sarcină, estimarea costului forței de muncă pentru acea sarcină este adăugată automat în categoria implicită pentru forță de muncă. Această estimare a costurilor este afișată pe fila **Costuri și venituri estimate** din grila **Detalii despre linie** pentru acea sarcină. Dacă aveți nevoie de mai multe estimări ale costului forței de muncă, le puteți adăuga în această filă. Dacă măriți sau micșorați numărul de ore pentru estimarea costului forței de muncă, programul sarcinii este recalculat automat. 

Fila **Estimarea cheltuielilor și a costurilor materiale** **Costuri și venituri estimate** vă permite, de asemenea, să estimați cheltuielile și costurile materiale pentru o sarcină, dacă aveți nevoie de estimări. 

Costul și prețul de vânzare pentru fiecare linie de estimare a forței de muncă sau a cheltuielilor se bazează pe configurarea definită pentru fiecare categorie în tabelele de prețuri de la **Management de proiect și contabilitate** &gt; **Configurare** &gt; **Preț**. Pentru elemente, costul și prețul de vânzare sunt adăugate în mod implicit din acordurile de element sau comerț de pe pagina de listă **Proiecte lansate** din Gestionarea informațiilor de proiect.

## <a name="tracking-progress-on-the-wbs"></a>Urmărirea progresului pe WBS
Unele industrii urmăresc progresul unui proiect împotriva unui WBS la un nivel foarte granular, în timp ce altele urmăresc progresul la un nivel superior al WBS. Această secțiune descrie modul în care puteți utiliza urmărirea WBS pentru cerințele proiectului. 

Finanța are trei vizualizări pentru WBS-ul unui proiect: vizualizarea Planificare, vizualizarea Urmărire efort și vizualizarea Urmărirea costurilor.

### <a name="planning-view"></a>Vizualizare planificare

Vizualizarea Planificare afișează estimarea planificată sau de bază a informațiilor privind programul și costurile. Deși nu există caracteristici pentru urmărirea versiunii și a liniei de bază pentru un proiect WBS, valorile din această vizualizare sunt destinate să reprezinte versiunea de bază. Secțiunile de estimare a programării și estimarea costurilor din acest subiect descriu această vizualizare și modul în care este utilizată pentru a crea un WBS.

### <a name="effort-tracking-view"></a>Vizualizarea Urmărire efort

Vizualizarea Urmărire efort afișează urmărirea progresului pentru activități în WBS. Compară orele de efort efectiv acumulate pentru o sarcină cu orele de efort planificate. Următoarele formule furnizează valorile din vizualizarea Urmărire efort:

-   Procentaj de progres = efort efectiv până în prezent ÷ efortul planificat pentru activitate
-   Efort rămas (cunoscut și sub denumirea de estimare până la finalizare \[ETC\]) = Efort planificat - Efort efectiv până în prezent
-   Estimare la (EAC) finalizat = efortul rămas + efortul real până în prezent
-   Varianța preconizată a efortului = efortul planificat – EAC

Vizualizarea Urmărire efort afișează o proiecție a varianței efortului pentru sarcină, pe baza faptului că EAC este mai mult sau mai puțin decât efortul planificat:

-   În cazul în care EAC este mai mult decât efortul planificat, activitatea este proiectată să dureze mai mult timp decât a fost planificat inițial și este în urmă.
-   În cazul în care EAC este mai puțin decât efortul planificat, activitatea este proiectată să dureze mai puțin timp decât a fost planificat inițial și este înainte.

**Reproiectarea efortului de către managerul de proiect** Ocazional, managerul de proiect sau o altă persoană care urmărește progresul unui proiect va trebui să revizuiască estimările inițiale pentru o sarcină. Sarcina s-ar putea mișca mai repede sau mai lent decât se anticipase inițial din diverse motive. De exemplu, domeniul de aplicare a fost redus sau lucrătorii au mai puțină experiență decât au planificat inițial. Proiecțiile sunt percepția unui manager de proiect asupra estimărilor, pe baza stării actuale a unui proiect. În general, nu ar trebui să modificați numerele de referință, deoarece linia de bază a proiectului reprezintă un document ca sursă publicată pentru planificarea proiectului și estimarea de cost aprobate de toți participanții direct interesați. 

Există două modalități prin care manageri de proiect pot modifica efortul asupra activităților:

-   Modificați efortul rămas care este setat automat pentru a actualiza efortul rămas efectiv asupra sarcinii.
-   Modificați procentul de progres care este configurat automat să actualizeze progresul efectiv asupra activității.

Ambele aceste abordări cauzează o recalculare a activității ETC, EAC și procentajul de progres, precum și varianța de efort proiectată pentru activitate. EAC, ETC, și procentul de progres cu privire la activitățile de sinteză sunt, de asemenea, recalculate, și varianța lor de efort proiectată este actualizată. 

**Efort modificat asupra sarcinilor rezumative** Puteți modifica efortul pentru rezumat sau sarcini de recipient. Indiferent dacă modificați aceste valori utilizând efortul rămas sau procentajul de progres pe activitățile de rezumat, calculele au loc automat în următoarea ordine:

1.  Se calculează EAC, ETC. și procentajul de progres al activității.
2.  Noul EAC este distribuit spre activitățile secundare în aceeași proporție cum a fost suma EAC originală.
3.  Se calculează noul EAC pentru fiecare sarcină de nod frunză.
4.  Efortul rămas și procentul de progres sunt recalculate pentru toate sarcinile copilului afectat, pe baza noii valori EAC. Varianța efortului sarcinilor este, de asemenea, recalculată.
5.  EAC al sarcinilor sumare este, de asemenea, recalculat din nodurile frunze.

Clic pe **Extindeți la nivel** în vizualizarea Efort de urmărire pentru a seta nivelul la care să urmăriți și să vă mențineți WBS. WBS este extins automat la acel nivel în vizualizarea Urmărire efort ori de câte ori îl deschideți.

### <a name="cost-tracking-view"></a>Vizualizare urmărire cost

Vizualizarea Urmărirea costurilor afișează urmărirea consumului de costuri pentru o sarcină. În această perspectivă, costul real care a fost cheltuit pentru o sarcină până în prezent este comparat cu costul planificat pentru sarcină. Următoarele formule furnizează valorile din vizualizarea Urmărire cost:

-   Procent din costul consumat = cost real până în prezent ÷ costul planificat pentru activitate
-   Cost pentru a finaliza (CTC) = cost planificat - cost real până în prezent
-   Estimare la final (EAC) = CTC + costul real până în prezent
-   Varianța costurilor proiectate = cost planificat – EAC

Vizualizarea Urmărire cost afișează o proiecție a varianței costului pentru sarcină, pe baza faptului că EAC este mai mult sau mai puțin decât costul planificat:

-   În cazul în care EAC este mai mult decât costul planificat, activitatea este proiectată să utilizeze mai mulți bani decât a fost planificat inițial și a depășit bugetul.
-   În cazul în care EAC este mai puțin decât costul planificat, activitatea este proiectată să utilizeze mai puțini bani decât a fost planificat inițial și este sub buget.

**Reproiectarea costului de către managerul de proiect** Managerii de proiect trebuie să utilizeze CTC pentru a revizui estimarea inițială a costurilor pentru o sarcină. Managerul de proiect poate modifica valoarea CTC la costul necesar pentru finalizarea sarcinii. Dacă modificați valoarea CTC, CTC-ul sarcinii, EAC și procentul din costul consumat și variația costurilor proiectate pentru o sarcină sunt recalculate. EAC, ETC, și procentul de cost consumat pe activitățile de sinteză sunt, de asemenea, recalculate, și varianța lor de cost proiectată este actualizată. 

> [!NOTE] 
> Când revizuiți efortul pentru o sarcină WBS în vizualizarea Urmărire efort, CTC-ul sarcinii, EAC, procentul costului consumat și varianța costurilor proiectate sunt recalculate în vizualizarea Urmărire costuri. Cu toate acestea, revizuirile costurilor nu afectează valorile din vizualizarea Urmărire efort, deoarece costul pe tip de tranzacție (forță de muncă, material sau cheltuială) sau categoria de proiect nu este revizuit. 

**Revizuirea proiecției pentru costuri pe sarcini de rezumat** Puteți revizui costurile pentru activitățile de sinteză, iar calculele au loc automat în următoarea ordine:

1.  EAC, CTC și procentul din costul consumat pentru sarcină sunt recalculate.
2.  Noul EAC este distribuit în jos, activităților secundare în aceeași proporție ca EAC-ul original pe activități.
3.  Se calculează noul EAC pentru fiecare sarcină.
4.  CTS și procentul din costul consumat sunt recalculate pentru sarcinile copilului afectat, pe baza valorii EAC. Varianța costului sarcinilor este, de asemenea, recalculată.
5.  EAC pentru toate sarcinile de sinteză este recalculat pe baza acestei modificări.

Clic pe **Extindeți la nivel** în vizualizarea Cost de urmărire pentru a seta nivelul la care să urmăriți și să vă mențineți WBS. WBS este extins la acel nivel în vizualizarea Urmărire cost ori de câte ori îl deschideți.

### <a name="earned-value-management"></a>Managementul valorii câștigate

Puteți utiliza metoda valorii câștigate (EVM) pentru a urmări progresul unui proiect. Puteți vizualiza valorile câștigate în Centrul de roluri al managerului de proiect. Componenta graficului valorii câștigate arată valorile în etape ale valorii planificate și ale costului real. Valoarea câștigată de la data curentă este afișată ca punct. Datele pe etape pentru valoarea câștigată nu sunt disponibile momentan. 

Faza de timp pe graficul valorii câștigate este afișată în funcție de săptămână sau de lună. Această secțiune descrie cei trei piloni ai EVM: valoarea planificată, valoarea câștigată și costul real. 

**Valoare planificată** Teoria EVM afirmă că graficul valoric planificat reprezintă rata la care echipa proiectului a planificat să câștige valoare pe proiect. 

Finance utilizează regula câștigului 0:100 atunci când reprezintă grafic valoarea planificată. Conform acestei reguli, valoarea sarcinii este înregistrată în sarcină de la data sa de încheiere. Nicio valoare nu este publicată până când sarcina este finalizată 100%. 

În Managementul și contabilitatea proiectului, introduceți data de încheiere a nodurilor frunze și costul planificat pentru aceasta. Când graficul valorii planificate este afișat pe săptămâni, valoarea planificată este rezumată pe săptămână pentru toate sarcinile nodului frunză pe durata proiectului. 

**Valoare câștigată** Teoria EVM afirmă că graficul valoric câștigat reprezintă rata la care echipa proiectului câștigă efectiv valoare pe proiect. 

Finance utilizează regula câștigului 0:100 atunci când reprezentările sale grafice au câștigat valoare. Conform acestei reguli, valoarea sarcinii este înregistrată în sarcină de la data sa de încheiere. Nicio valoare nu este publicată până când sarcina este finalizată 100%. 

Când se calculează valoarea câștigată, se ia în considerare procentul de progres al fiecărei sarcini. În conformitate cu regula câștigului 0: 100, numai sarcinile care sunt finalizate într-o anumită perioadă sunt luate în considerare pentru calcularea valorii câștigate de la sfârșitul perioadei respective. Valoarea câștigată pe proiect este calculată pentru toate sarcinile care au fost finalizate la crearea graficului. 

> [!NOTE] 
> În prezent, sistemul de urmărire WBS nu are structuri de date pentru a stoca procentele istorice de progres pe fiecare sarcină. Prin urmare, valoarea câștigată poate fi raportată numai din momentul procesării cubului. Procesați cubul în mod regulat pentru a actualiza datele despre valoarea câștigată care sunt afișate în Centrul de roluri. 

**Cost actual** Teoria EVM afirmă că reprezentarea grafică reală a costurilor reprezintă rata la care sunt cheltuiți banii pentru proiect. 

Tranzacțiile care sunt înregistrate într-un proiect sunt utilizate pentru a trasa linia de cost reală. Costurile sunt sintetizate după dată. Aceste date sunt apoi utilizate pentru a grafica costurile reale pe săptămână sau pe lună pe graficul valorii câștigate.

### <a name="how-to-use-the-concepts-of-planned-value-earned-value-and-actual-cost"></a>Cum se utilizează conceptele de valoare planificată, valoarea câștigată și costul real

**Planifică varianța** În timpul planificării, creați o prognoză pentru lucrul pe o cronologie. Prin urmare, valoarea planificată este rata la care planificatorii de proiecte au considerat că ar fi finalizată lucrarea la proiect. După ce un proiect este în desfășurare, lucrările sunt finalizate și proiectul câștigă valoare. Comparând valoarea planificată cu valoarea câștigată, puteți vedea cum progresează munca la un proiect. Rezultatul acestei comparații se numește varianță de program. 

Dacă valoarea planificată pentru o perioadă este mai mare decât valoarea câștigată, cantitatea de muncă care a fost făcută la un proiect este mai mică decât cea planificată. Prin urmare, proiectul este în întârziere. Deoarece valoarea planificată și valoarea câștigată sunt exprimate în termeni monetari, timpul de întârziere al proiectului primește și o valoare monetară. 

Dacă valoarea planificată pentru o perioadă este mai mică decât valoarea câștigată, cantitatea de muncă care a fost făcută la un proiect este mai mare decât cea planificată. Prin urmare, proiectul este în avansul planificării. Acest timp necesar are, de asemenea, o valoare monetară.

**Variația costurilor** Deoarece valoarea câștigată folosește prețul de cost ca multiplicator, valoarea câștigată indică costul muncii efectuate la un proiect. Pe măsură ce un proiect progresează, jurnalul de tranzacții oferă o evidență a banilor cheltuiți efectiv pentru acel proiect. Comparând valoarea câștigată cu costul real, puteți vedea suma de bani cheltuită față de valoarea câștigată. Rezultatul acestei comparații se numește varianță de cost. 

Dacă costul real cheltuit pentru o perioadă este mai mare decât valoarea câștigată, s-au cheltuit mai mulți bani decât câștigați. Prin urmare, proiectul depășește bugetul. 

Dacă costul real cheltuit pentru o perioadă este mai mică decât valoarea câștigată, s-au câștigat mai mulți bani decât s-au cheltuit. Prin urmare, proiectul este sub buget.

## <a name="wbs-templates"></a>Șabloane WBS
Puteți utiliza funcționalitatea șabloanelor WBS pentru a crea șabloane standard pentru proiecte. Dacă proiectele pe care le oferă compania dvs. implică o mulțime de muncă repetabilă, ar trebui să luați în considerare crearea unui șablon WBS. 

Puteți crea un șablon WBS din WBS al unui proiect existent, astfel încât cunoștințele și cele mai bune practici pe care le-ați adunat în timpul planificării acelui proiect să poată fi reutilizate în proiecte similare în viitor. Cu toate acestea, uneori, s-ar putea să nu aibă sens să salvați întregul WBS ca șablon. Prin urmare, puteți crea și șabloane din părți ale WBS pentru un proiect.

### <a name="saving-a-projects-wbs-as-a-template"></a>Salvarea WBS-ului unui proiect ca șablon

După ce creați un șablon, îl puteți importa în WBS-ul unui nou proiect sub nodul rădăcină sau în orice activitate din WBS-ul proiectului.

### <a name="importing-a-wbs-template-into-a-projects-wbs"></a>Importarea unui șablon WBS în WBS-ul unui proiect

Când importați activități, activitățile din șablon sunt organizate pe baza datei de începere a activității în care sunt importate. În timpul importului, relațiile predecesoare pe activitățile șablon sunt utilizate pentru a calcula datele de începere pentru activitățile importate. Calendarul de lucru standard al proiectului de destinație este aplicat pentru a calcula datele de încheiere ale sarcinilor importate, astfel încât să se păstreze zilele de lucru și orele de lucru standard care sunt definite în calendarul de lucru al proiectului curent. 

Sumele costurilor și prețurile de vânzare pe liniile de estimare sunt aplicate pentru a garanta că prețurile specifice proiectului sau contractului de proiect au date valabile.

### <a name="differences-between-a-projects-wbs-and-a-wbs-template"></a>Diferențele dintre șablonul WBS al unui proiect și un șablon WBS

-   Activitățile din șabloanele WBS nu au date de începere și date de încheiere.

Zilele lucrătoare și cele nelucrătoare nu sunt setate pentru șabloanele WBS.

-   Șabloanele WBS folosesc întotdeauna calendarul de planificare care este configurat ca calendar implicit pentru toate proiectele.

Calendarul de programare implicit este utilizat numai pentru a afla orele într-o zi de lucru standard.

-   Relațiile anterioare nu sunt copiate într-un șablon WBS.

Deoarece șabloanele WBS nu au date, logica datei de început care se bazează pe data de încheiere a predecesorului nu este necesară.

-   O linie de estimare a costului forței de muncă este creată automat atunci când o activitate este creată într-un șablon WBS. Prețul de vânzare și valoarea costului sunt copiate de la lucrătorul selectat.

Cheltuielile și costurile articolelor pot fi create manual, la fel cum se poate face pe WBS-ul unui proiect.

-   Erorile de planificare sunt afișate atunci când există abateri de la următoarea formulă:

Efort = Număr de resurse × Durată × Număr de ore într-o zi de lucru standard 

Puteți corecta toate erorile de planificare în același timp, făcând clic pe **Remediați toate erorile de planificare**. 

Alternativ, puteți corecta erorile de planificare individual făcând clic pe pictograma de avertizare pentru fiecare activitate.





[!INCLUDE[footer-include](../includes/footer-banner.md)]