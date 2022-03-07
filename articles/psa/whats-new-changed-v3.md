---
title: Ce este nou sau modificat în Project Service Automation versiunea 3
description: Acest subiect oferă informații despre ceea ce este nou și schimbat în Project Service Automation versiunea 3.
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
ms.topic: article
author: JohnPBurrows
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 0c198a0fd293008b73422f3f60ea023f918e0ddc
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082758"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3"></a>Ce este nou sau modificat în Project Service Automation versiunea 3
[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Acest subiect oferă informații despre modificările la interfața cu utilizatorul (UI), funcționalitatea și terminologia în Project Service Automation între versiunea 2 sau versiunea 1 și versiunea 3.

## <a name="project-scheduling"></a>Planificarea proiectelor
Planificarea de proiect, care a fost cunoscută sub numele de structura detaliată a proiectului (WBS) în versiunile anterioare, a fost redenumit Planificare și este accesat făcând clic pe fila **Planificare**. 

![Planificarea proiectului](media/psa-schedule-01.png)

Planificarea are acum o nouă suprafață de interacțiune care este atât modernă cât și accesibilă. Cu toate acestea, motorul de planificare de bază Project Service Automation nu s-a schimbat. Butoanele de control din panglica grila de planificare vă permit să interacționați cu planificarea similară cu versiunea anterioară de Project Service Automation. Modificările suplimentare ale planificării includ:

- **Diagramă Gantt** - diagrama Gantt nu mai este prezentă. O nouă vizualizare Gantt se va întoarce într-o actualizare viitoare.
- **Anteturi de coloană** - puteți ascunde anteturi de coloană în grilă făcând clic pe indicatorul de jos de lângă titlul coloanei. 
- **Coloane** - puteți afișa coloanele ascunse făcând clic pe **Adăugare coloană**. 
- **Categorie de tranzacții** - o căutare **Categorie de tranzacții** a fost adăugată la grila de planificare și este afișată în mod implicit. 
 
## <a name="project-templates"></a>Șabloane de proiect
S-au făcut următoarele modificări la funcționalitatea de șablon de proiect.

### <a name="create-a-project-template"></a>Crearea unui șablon de proiect 
Aveți posibilitatea să creați un șablon de proiect în versiunea 3 similară cu versiuni anterioare ale Project Service Automation. Șablonul poate conține numai o planificare, iar planificarea poate include roluri, dar nu sunt necesare. Dacă planificarea are roluri, acestea pot fi numai pentru resurse generice. Aveți posibilitatea să generați cerințe de resurse pentru resurse generice, dar acestea nu pot fi rezervate cu resurse reale în șablon. Nu puteți rezerva o resursă reală unei echipe dintr-un șablon. 

### <a name="create-a-template-from-an-existing-template"></a>Crearea unui șablon pe baza unui șablon existent
Atunci când creați un șablon de proiect nou dintr-un șablon existent în Project Service Automation versiunea 3, se întâmplă următoarele: 

- Planificarea proiectului sursă este copiată în șablon. 
- Resursele generice sunt copiate în echipă și toate atribuirile de resurse generice sunt copiate peste. Cerințele pentru resursele generice nu sunt copiate peste. 

### <a name="create-a-template-from-an-existing-project"></a>Crearea unui șablon pe baza unui proiect existent
Atunci când creați un șablon de proiect nou dintr-un proiect existent, se întâmplă următoarele: 

- Planificarea proiectului sursă este copiată în șablon. 
- Resursele generice sunt copiate în echipă și toate atribuirile de resurse generice se păstrează. Cerințele pentru resursele generice nu sunt copiate peste.    
- Resursele denumite, ambele atribuite sau neatribuite sunt eliminate din echipă și înlocuite cu resurse generice.
- Dacă sunt prezente, informațiile despre clienți sunt eliminate. 
- Dacă există, trimiterile la oferte și contracte sunt eliminate. 

### <a name="create-a-project-from-a-template"></a>Creați un proiect dintr-un șablon
Atunci când creați un proiect nou dintr-un șablon în Project Service Automation versiunea 3, se întâmplă următoarele:

- Planificarea, echipa și rolurile sunt copiate în noul proiect.   
- Data de începere este fie data de copiere, fie data selectată de utilizator.   
- Pentru orice membri ai echipei generice cu cerințe de resurse în șablon, cerințele nu sunt copiate sau generate automat. Va trebui să le generați. 

## <a name="copy-a-project"></a>Copiați un proiect
Atunci când copiați un proiect în Project Service Automation versiunea 3, se întâmplă următoarele: 

- Data estimată de începere este copiată, dar poate fi schimbată.  
- Sunt copiate planificarea și activitățile proiectului. 
- Resursele generice și atribuirile lor sunt copiate. Cerințele pentru resursele generice nu sunt copiate. Va trebui să le generați din nou. 
- Resursele reale și atribuirile lor nu sunt copiate. În schimb, ele sunt înlocuite de resurse generice. 
- Datele reale nu sunt copiate în noul proiect. 

## <a name="move-a-scheduled-project"></a>Mutarea unui proiect planificat
Când mutați planificarea de proiect existent înainte, se întâmplă următoarele: 

- Datele de activitate sunt mutate automat pentru a corespunde perioadei de deplasare. 
- Resursele generice atribuite rămân atribuite.   
- Dacă sunt generate înainte de mutarea proiectului, cerințele pentru resursa generică rămân aceleași și nu sunt automat generate din nou. Va trebui să le generați din nou pentru a reflecta noile atribuiri din cauza mutării de activități. 
- Atribuirile de resurse reale se modifică pentru a corespunde cu mutarea datei de activitate. Rezervările la resurse reale nu se modifică. Va trebui să modificați rezervările utilizând vizualizarea reconciliere. 
- Resursele de echipă cu rezervări, dar fără misiuni nu se modifică. 
- Datele reale nu se mută. 

## <a name="estimates"></a>Estimări
Estimările au fost împărțite în două file, **Atribuire de resurse** și **Estimări**. Fila **Atribuire resurse** conține estimările efortului și afișează atribuirile de resurse pentru activități într-o vizualizare pe etape. Puteți edita estimările pe baza a ceea ce a generat motorul de planificare.

![Fila Atribuiri resurse afișează estimările de efort și atribuirile de resurse pentru activități](media/resource-assignments-tab-02.png)

Fila **Estimări** afișează sumele de cost și vânzări pentru atribuirile de resurse. Sumele sunt doar în citire. Costul și prețurile de vânzare sunt acum conduse din atribuirile membrului echipei pe planificare. Acest lucru înseamnă că, dacă aveți o activitate fără nici o atribuire, aceasta va apărea sub pachetul neatribuit. Acest lucru înseamnă, de asemenea, că fără **rol**, care este o dimensiune implicită de tarifare, nu va exista nici un cost estimat sau vânzări dacă aveți un client sau un contract/ofertă asociate cu proiectul. 

![Fila estimări afișează sumele de cost și de vânzări](media/estimates-tab-03.png)
  
Categorie este, de asemenea, acceptată pe activități în vizualizarea de planificare. Gruparea după categorie în vizualizarea treptată a estimărilor va oferi o experiență mai bună, în special atunci când aveți, de asemenea, estimări ale cheltuielilor în proiect. Estimările de cheltuieli sunt introduse utilizând o grilă pe o filă separată. 

Estimările de cheltuieli pot fi introduse în grila de pe fila **Estimări de cheltuieli**. 

![Fila estimări de cheltuieli afișează grila cu estimări de cheltuieli](media/expense-estimates-tab-04.png)

## <a name="resource-management"></a>Gestionarea resurselor
În Project Service Automation versiunea 3, cu noul utilizator Unified Client și modificări în relația dintre rezervări și atribuiri, echiparea cu personal a unui proiect cu resurse generice sau reale s-a schimbat dramatic de la versiunea 2 și versiunea 1. Cu toate acestea, conceptele de resurse care pot fi rezervate, atât **reale**, cât și **generice** rămân aceleași, la fel ca membrii echipei, cerințele, misiunile și rezervările.   

![Utilizarea selectorului de resurse](media/resource-management-05.png)

### <a name="assign-a-real-bookable-resource"></a>Atribuiți o resursă reală care se poate rezerva 
În versiunea 3 de Project Service Automation, rezervările și sarcinile de sarcini nu sunt la fel de strâns legate între versiunile anterioare ale Project Service Automation. Puteți utiliza grila de echipă pentru a rezerva un membru **real** al echipei, similar cu cel de pe piață.

Utilizând selectorul de resurse din planificare, aveți posibilitatea să selectați membrul echipei creat în vizualizarea echipă și apoi să-l atribuiți la activități. Puteți continua să le atribuiți sarcini, chiar și după rezervările lor. Utilizați fila **Reconciliere** pentru a reconcilia membrii echipei care au diferențe în rezervări și atribuiri.

Selectorul de resurse va afișa membrii echipei pentru proiect. De asemenea, puteți utiliza selectorul de resurse pentru a căuta și a vizualiza alte resurse care se pot rezerva care nu fac parte din echipa de proiect. Le puteți atribui o activitate și vor deveni parte a echipei de proiect. Va trebui să le rezervați utilizând **Panoul de planificare** sau fila **Reconciliere**.

### <a name="assign-a-generic-bookable-resource-on-a-task-and-project-team-and-then-fulfill-with-a-real-resource-via-schedule-board"></a>Atribuiți unei activități o resursă generică care se poate rezerva pe o echipă de activități și proiect și apoi să îndeplinească cu o resursă reală prin intermediul Panoului de planificare 
În Project Service Automation versiunea 3, funcționalitatea generare echipă nu este utilizată pentru resurse generice. În schimb, aveți posibilitatea să creați și să atribuiți direct o resursă generică din planificare tastând numele poziției resursei generice în celula de resurse a planificării. Sau, aveți posibilitatea să selectați pictograma resursei din celulă și apoi, utilizând selectorul de resurse, tastați numele resursei generice pe care doriți să o creați. Acest lucru va deschide un panou de creare rapidă, care vă permite să setați rolul și unitatea de organizație membru al echipei de resurse generice. După ce creați resursa, aceasta este atribuită activității și aveți posibilitatea să continuați să atribuiți acea resursă generică altor activități din planificare.    
 
Când ați atribuit resursa tuturor activităților potrivite, puteți genera o solicitare de resurse și apoi să o îndepliniți rezervând direct cu **Panoul de planificare** sau trimițând o solicitare de resursă. De asemenea, puteți adăuga resurse generice direct la grila de membru al echipei. 

Resursele generice sunt adăugate la echipa de proiect fără cerințe de resurse și cu datele de început/sfârșit ale proiectului până când se generează cerința de resurse. Pentru a genera o cerință, selectați resursa generică și faceți clic pe **Generare**. Linkul de cerință se afișează acum, iar orele necesare vor fi populate cu orele atribuite. Aveți posibilitatea să faceți clic pe link pentru a deschide și actualiza cerința.
  
Când rezervarea este completă și complet îndeplinită de o resursă denumită, resursa generic este înlocuită cu resursa denumită și atribuirea pe planificare este actualizată cu resursa denumită. 

Resursele propuse pentru cerințe sunt acum stocate pe o filă în loc de o secțiune separată.

### <a name="multiple-named-resources-fulfilling-a-generic-resource"></a>Mai multe resurse numite care îndeplinesc o resursă generică
Atunci când o cerință este îndeplinită cu mai multe resurse, resursa generică rămâne în echipă și atribuită activității. Membrii echipei numite care sunt rezervați nu sunt desemnați ca parte a poziției. Managerul de proiect poate atribui activitatea necesară resurselor reale.  Vizualizarea **Reconciliere** oferă o defalcare a rezervărilor în mai multe resurse pentru mai multe misiuni de activitate. Acest lucru nu se face în mod automat, deoarece în scenarii mai complicate, ar fi unul în cazul în care aveți un pachet de sarcini care alcătuiesc cerința, intenția modului în care managerul de proiect vrea să atribuie, trebuie să fie asumată. Deoarece sistemul nu poate înțelege intenția, ipotezele vor fi probabil diferite de cele preconizate și se va produce un rezultat incorect sau imprevizibil. Rezultatul previzibil este că resursa generică rămâne atribuit până când managerul de proiect atribuie în mod deliberat resurse utilizând vizualizarea **Reconciliere**.

### <a name="reconciliation"></a>Reconciliere
Fila **Reconciliere** afișează rezervări și toate atribuirile pentru fiecare membru al echipei de proiect. Vizualizarea arată ore în celule, ceea ce poate reprezenta repere în timp, de la luni la zile. Această vizualizare îi ajută managerii de proiect să reconcilieze rezervările membrilor echipei și sarcinile lor pentru echipa lor de proiect. Acest lucru este util deoarece rezervările și atribuirile de activități nu sunt strâns cuplate, ceea ce permite o mai mare flexibilitate la planificarea unui proiect. 

![Fila Reconciliere afișează rezervări și toate atribuirile pentru membrii echipei de proiect.](media/resource-reconciliation-tab-06.png)

Pentru fiecare resursă, vizualizarea ia diferența dintre rezervările unui membru al echipei și un cumul de atribuirile lor de activități și arată următoarele două diferențe care pot apărea cu rezervările și atribuirile într-un proiect: 

- **Deficit de rezervare** - deficitul de rezervare apare atunci când o resursă are mai multe atribuiri decât rezervări. Deoarece această capacitate nu a fost rezervată, un manager de proiect poate corecta această condiție prin extinderea rezervărilor resursei pentru a acoperi deficitul. 
- **Rezervări în exces** - rezervarea în exces apare atunci când o resursă a fost rezervată proiectului, dar nu a fost atribuită activităților.  Această apariție poate fi una acceptabilă dacă, de exemplu, resursa a fost rezervată înainte să apară atribuirea de activități. Cu toate acestea, în alte cazuri, resursa nu poate fi planificată pentru a fi atribuită, și MP ar trebui să ia în considerare anularea rezervările resursei pentru a permite capacității să fie utilizate pentru un alt proiect. 

Când aveți atribuiri de sarcini pentru o resursă fără rezervări (o lipsă de rezervări), puteți selecta lipsa agregată de rezervări și să faceți clic pe **Extindeți rezervarea**. De aici, puteți vizualiza rezervarea necesară pentru a aborda deficitul resursei și disponibilitatea acestora. 
 
## <a name="time-and-expense"></a>Timp și cheltuială
Această secțiune furnizează informații despre modificările în timp, cheltuieli și aprobare în versiunea 3 a Project Service Automation. Ca parte a soluției Dynamics 365 Project Service Automation, caracteristica de **Intrare de timp** a fost reîmprospătată pentru a profita de structura Interfață unificată. Aceasta permite livrarea unei interfețe a utilizatorului consistente, uniforme, care urmărește un design receptiv pentru vizualizare optimă pe orice mărime de ecran sau dispozitiv. 

### <a name="landing-page"></a>Pagină de destinație
Experiența de intrare de timp particularizată non-extensibilă a fost perimată în versiunea 3. În schimb, există acum o experiență de rețea extensibilă și accesibilă. Puteți accesa funcționalitatea de intrare în timp utilizând harta site-ului din stânga. Cu această modificare, nu veți mai putea să introduceți ora pentru o săptămână la rând. În schimb, va trebui să creați o intrare de timp pentru fiecare zi în grilă. După ce au fost create câteva intrări de timp, utilizatorii pot crea în bloc intrările de timp cu funcția **Copiere** explicată mai târziu în acest subiect. 

![Pagina de destinație a intrării de timp](media/time-entry-landing-page-07.png)
 
### <a name="create-new-time-entries"></a>Creați noi intrări de timp 
Faceți clic pe **Nou** în panglică pentru a deschide o pagină de creare rapidă pentru intrarea de timp unde introduceți durata în minute, ore sau zile. Pentru a face acest lucru, începeți să tastați o, m sau z împreună cu cantitatea.  

![Creare rapidă intrare de timp](media/quick-create-time-entry-08.png)

Câmpurile căutare sunt susținute de vizualizări de sistem. De exemplu, după ce introduceți informații despre proiect, câmpul **Activitatea de proiect** este setată implicit la vizualizarea **Activitățile mele de proiect deschise**. Pentru a crea intrări de timp pentru activități care nu sunt atribuite utilizatorului, faceți clic pe **Modificare vizualizare** pe câmpul căutare și selectați **Toate activitățile active de proiect**. După ce intrarea de timp a fost creată și este afișatăîn grilă, aveți posibilitatea să editați orice valori de linie direct în grilă.  

### <a name="bulk-createcopy"></a>Creare/Copiere în bloc 
După ce au fost create câteva înregistrări de timp, puteți utiliza funcționalitatea de copiere pentru a crea în bloc entități de timp adiționale. Faceți clic pe **Copiere** pentru a deschide dialogul **Copiere**. În **De la perioada: data de început**, setați intervalul de date din care trebuie copiate intervalele de timp. În **La perioadă: data de început**, specificați data pentru care trebuie create intrările de timp. Faceți clic pe **Copiere** pentru a copia intrările de timp în ziua corespunzătoare a săptămânii indicată în **La perioada**. De exemplu, înregistrarea de timp pentru luni de săptămâna trecută va fi copiată pentru lunea săptămânii indicate în **La perioada**. 

![Copiați intrările de timp în bloc](media/bulk-copy-time-entry-09.png)
 
### <a name="import-data"></a>Importați date 
Atribuirile și schimbul urmează același model UI, care permite utilizatorului să precizeze intervalul de date de la momentul în care rezervările trebuie importate. Apoi trebuie să alegeți explicit rezervările care ar trebui copiate în intrările de timp **Schiță**. În versiunea 3, nu mai puteți vedea modelul de intrări de timp **Sugerat** pe grilă și calendar.  

### <a name="change-in-calendar-control"></a>Modificarea controlului calendarului
În versiunea 3, ne-am mutat departe de controlul calendar personalizat și acum utilizăm UC calendar pentru a afișa intrările de timp pentru săptămână. Cu acest calendar, puteți vizualiza ziua, săptămâna și luna. 

> [!NOTE]
> O limitare în calendar este că acest control nu acceptă acțiuni pe elemente de calendar individuale. De exemplu, nu veți avea posibilitatea să selectați unul sau mai multe elemente de calendar și să trimiteți sau să ștergeți acele elemente. Făcând clic pe un element de calendar se va deschide pagina **Entitate de intrare de timp** pentru acțiuni suplimentare. 

### <a name="extensibility"></a>Extensibilitate
**Capturați date pe câmpuri particularizate doar în entități de intrări de timp și cheltuieli** - intrarea de timp utilizează o grilă editabilă, o grilă doar citire și controale de calendar din platformă. Toate aceste controale sunt native și, prin urmare, vor accepta particularizări. În Project Service Automation versiunea 3, puteți adăuga câmpuri particularizate suplimentare, să configurați câmpuri de căutare și să le copiați de rezervă cu vizualizări particularizate. De asemenea, puteți seta logica de business particularizată pe baza valorilor selectate în câmpuri particularizate.  

**Capturați date pe câmpuri particularizate în intrarea de timp și cheltuieli și propagați-le prin entități care acceptă fluxul de trimitere și aprobare** - procesarea tipică a intrărilor de timp este afișată în diagrama următoare.

![Procesarea fluxului de intrare de timp](media/process-time-entries-10.png)

Dacă cerințele de afaceri stipulează că entitățile de timp și cheltuieli trebuie să captureze dimensiunile de preț particularizate și să propagați valorile care sunt setate de o resursă de marcă de timp și de intrare în dimensiunea de preț particularizat prin toate entitățile din graficul anterior, consultați [Configurați câmpuri particularizate ca dimensiuni de preț](set-up-pricing-dimensions.md)

Pentru a accepta cerințe de afaceri în cazul în care entități de timp și cheltuieli trebuie să surprindă dimensiuni particularizate non-tarifare și propaga valorile, puteți utiliza setarea dimensiunilor de stabilire a prețurilor și exprima dimensiunile particularizate ca dimensiuni de stabilire a prețurilor, fără nici un cost sau rată de facturare. Un alt scenariu ar fi să adăugați un câmp particularizat la fiecare dintre entități, utilizând același nume de câmp în toate entitățile. Plug-in-uri particularizate pot fi create pentru a lega înregistrările din entitățile care participă la fluxul de remitere/aprobare utilizând entitatea de tranzacții de origine și tranzacții de conexiune.  

### <a name="delegate-time-and-expense-entry"></a>Delegați intrarea de timp și cheltuială
Platforma Common Data Service nu acceptă ca un utilizator să se dea drept altul, ceea ce înseamnă că în versiunea 3 a Project Service Automation nu există suport pentru intrarea de timp și cheltuială delegate. Cu toate acestea, partenerii și clienții au utilizat o soluție pentru a permite suport pentru experiențele de intrare de timp delegate în versiunea 3. Aceasta este doar o soluție temporară și nu o soluție completă, deci este important să înțelegeți limitările și să utilizați această abordare numai dacă limitările sunt acceptabile. 

> [!IMPORTANT]
> Aceste informații ar trebui să fie considerate doar indicații sugerate pentru implementarea personalizată de către un partener/client. Echipa de produs nu va oferi suport formal pentru această funcționalitate prin oricare dintre canalele noastre de asistență.

### <a name="customization-details"></a>Detalii de particularizare 
Particularizarea vă permite să adăugați **Resurse care pot fi rezervate** pentru a crea și edita experiențele, ceea ce va permite unui utilizator să acționeze ca delegat modificând **Resursa rezervare** la un alt utilizator pentru care intrările de timp și cheltuieli trebuie să fi înregistrate. Următorii pași acoperă delegarea de intrare de timp. Aceleași informații se aplică delegării de intrare de cheltuială. 
 
1.  Asigurați-vă că utilizatorul delegat are acces de securitate global la proiecte și activități de proiect. 
1.  Deoarece **Resursa care se poate rezerva**, care este un câmp în entitatea **Intrare de timp** nu este expusă pe pagina **Creare rapidă**, trebuie să o adăugați.

    -sau-

    Creați o vizualizare particularizată care include coloana **Resursă ce se poate rezerva** pentru a vizualiza numai intrările de timp create pentru resursă. Publicați particularizările de pe proiectantul modulului aplicației pentru ca această vizualizare să apară sub **Vizualizare selector** pe pagina **Intrări de timp**. Există două inserturi care se ocupă de setarea managerului pentru intrările de timp non-proiect:

    - PreValidateTimeEntryCreate
    - PreValidateTimeEntryUpdate
 
1. Creați un insert nou pentru a suprascrie câmpul **Manager** la managerul utilizatorului atribuit în câmpul **Resursă care se poate rezerva**. Utilizați aceeași **Etapă de execuție** ca insert extraordinar (OOB) (pre-validare) și utilizați o **Comandă de executare** care este mai mare decât inserturile OOB (mai mare decât 1). Acest lucru va asigura că insertul personalizat este executat după inserturi OOB.  
 
### <a name="end-user-experience"></a>Experiența utilizatorului final
1.  Atunci când creați o intrare de timp pe pagina de creare rapidă, introduceți Proiectul și Detaliile activității de proiect și apoi alegeți utilizatorul pe câmpul **Resursă care se poate rezerva** pentru care trebuie înregistrate intrările de timp. 
2.  În mod implicit, acest câmp trece implicit la utilizatorul conectat, cu toate acestea, dat fiind că utilizatorul a depășit acest câmp, intrarea de timp este acum creată pentru **Resursa care se poate rezerva** selectată.
3.  Când remiteți intrările de timp pe care le-ați creat pentru aceste înregistrări, intrările vor fi plasate în coadă pentru aprobator în proiect așa cum este preconizat. 
4.  Când retrageți intrările de timp create pentru celălalt utilizator, intrările de timp vor fi returnate la o stare de **Schiță** cu câmpul **Resursă care se poate rezerva** setată la celălalt utilizator. 
5.  Opțional, aveți posibilitatea să comutați la vizualizarea particularizată pentru a filtra intrările de timp create pentru celălalt utilizator. 
 
### <a name="limitations"></a>Limitări
Funcționalitatea **Copiere** și **Import** funcționează numai în contextul utilizatorului care este conectat. Acest lucru înseamnă că nu este posibil să copiați sau să importați intrări de timp care sunt create pentru utilizatorul care este conectat ca resursa care poate fi rezervată.

Intrările de timp care nu sunt pentru un proiect vor fi rutate pentru aprobare managerului resursei care se poate rezerva numai dacă se finalizează pasul 4 din secțiunea **Detalii de particularizare** de mai sus. În caz contrar, intrările de timp non-proiect pentru celălalt utilizator va fi rutate incorect la managerul utilizatorului conectat. 

### <a name="other-changes"></a>Alte modificări 
Funcționalitatea **Rezervări și activități** a fost ștearsă. 

## <a name="multidimensional-pricing"></a>Prețuri multidimensionale
Pentru a maximiza flexibilitatea și a îndeplini cerințele de business diferite, versiunea 3 a Project Service Automation acceptă aplicarea discretă a seturilor de dimensiune a prețurilor la ratele de cost și de facturare. Valorile de dimensiuni pot fi setate ca implicite și apoi propagate în procesul de cost și de stabilire a prețurilor de la crearea de profiluri de resurse la intrarea de timp la datele reale de proiect. Configurația și modificarea specifice clientului utilizează infrastructura de personalizare standard.

Project Service Automation se livrează cu un set implicit de dimensiuni de stabilire a prețurilor și roluri și unități de resurse, și permite stabilirea de prețuri și costuri pentru fiecare combinație de rol și unitate organizațională.

Pentru clienții de Project Service Automation care doresc să continue să utilizeze aceste câmpuri predefinite ca dimensiuni de preț în versiunea 3, nu va exista nici o schimbare observabilă. Puteți continua să utilizați Project Service Automation ca de obicei. În cazul în care, cu toate acestea, trebuie să stabiliți prețul sau costul pentru resursele adiționale utilizând alte atribute suplimentare, versiunea 3 permite adăugarea propriilor dimensiuni de preț personalizat la Project Service Automation. Extinderea dimensiunilor de tarifare particularizate este o experiență de configurare complicată. 

## <a name="quotes-and-contracts"></a>Oferte și contracte
În versiunea 3 a Project Service Automation, aspectele de configurare și de gestionare pentru ghilimele și contracte s-au modificat. Următoarele secțiuni furnizează informații mai detaliate.

### <a name="set-up-chargeability-options"></a>Configurați opțiunile de posibilitate de tarifare
În versiunile 1 și 2, configurarea posibilității de tarifare pentru roluri și categorii pentru oferte și contracte specifice a fost realizată utilizând vizualizarea **Posibilitate de tarifare** care era în partea de sus a navigației unei linii de ofertă sau a unei linii de contract. Aici era locul în care puteați stabili și prețurile pentru acele roluri și categorii de Cheltuieli.

Începând cu versiunea 3, configurarea opțiunilor de posibilitate de tarifare după rol și categorie de cheltuială se va face la nivel de ofertă sau linie de contract. Configurarea prețurilor este separată de configurarea posibilității de tarifare. Veți putea găsi **Roluri taxabile** și **Categorii taxabile** ca file pe **Linia de ofertă** și paginile  **Linie de contract** fără a fi nevoie să utilizați navigarea de sus.

![Roluri tarifabile](media/chargeable-12.png)
 
Configurarea Rolurilor taxabile și a Categoriilor de taxare utilizează, de asemenea, controlul de grilă editabil predefinit. Pentru fiecare rol și categorie, opțiunile acceptate pentru tipul de facturare în timpul fazei de ofertare și contractare rămân neschimbate față de versiunile anterioare ca **Tarifabil** și **Netarifabil**. **Gratuitate** nu este un tip acceptat în timpul fazei de ofertare sau de contractare. **Gratuitate** este acceptată numai în timpul aprobării de timp sau cheltuială.  
 
### <a name="create-and-edit-custom-pricing-for-a-project-service-automation-quote-and-project-contract"></a>Crearea și editarea prețurilor particularizate pentru o ofertă Project Service Automation și un contract de proiect
În versiunile 1 și 2, utilizând lista de prețuri particularizate pentru anumite oferte și contracte s-a făcut utilizând **Editați prețurile** pe vizualizarea **Posibilitatea de tarifare**. Vizualizarea **Posibilitatea de tarifare** a fost localizată în navigarea de sus a unei linii de ofertă sau a unei linii de contract. Tot aici puteați configura opțiunile de posibilitate de tarifare pentru roluri și sau categorii de cheltuială.

Începând cu versiunea 3, crearea și utilizarea unei liste de prețuri particularizate de proiect pe o ofertă Project Service Automation și un contract de proiect Project Service Automation a fost separată de configurarea posibilității de tarifare. Contractele de proiecte și ofertele Project Service Automation au o nouă filă **Listele de prețuri ale proiectului**. Această filă afișează o vizualizare asociată a tuturor listelor de prețuri de proiect care sunt atașate la oferta Project Service Automation sau la contractul de proiect. Pentru a crea o listă de prețuri particularizată dintr-o listă de prețuri existentă care este deja asociată cu oferta sau contractul de proiect, faceți clic pe **Creați prețuri particularizate**. Acest lucru va face o copie a tuturor listelor de prețuri asociate și le va atașa la ofertă sau contract. Acum aveți posibilitatea să deschideți lista de prețuri și să editați prețul categoriei de roluri sau de cheltuieli, astfel încât aceste modificări de prețuri să se aplice numai la această ofertă sau contract. 
  
Următorul grafic este înainte de crearea de liste de prețuri particularizate.

![Înainte de liste de prețuri particularizate](media/before-custom-price-lists-13.png)

Următorul grafic apare după crearea de liste de prețuri particularizate.

![După liste de prețuri particularizate](media/after-custom-price-lists-14.png)

> [!NOTE]
> Este posibil să apară un decalaj scurt între momentul în care faceți clic pe **Creați prețuri particularizate** și cel la care se creează lista de prețuri particularizate. Recomandăm reîmprospătarea grilei în loc să faceți clic de mai multe ori. S-a creat o listă de prețuri particularizată dacă numele listei de prețuri asociate are numele ofertei sau numele contractului de proiect anexat la acesta.
