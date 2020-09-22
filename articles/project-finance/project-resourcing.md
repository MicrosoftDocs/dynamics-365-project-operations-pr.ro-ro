---
title: Alocarea de resurse proiectului
description: Acest subiect oferă informații despre alocarea de resurse proiectului.
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f9352465f83abe19097945dd34eada365cd03b8f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754682"
---
# <a name="project-resourcing"></a>Alocarea de resurse proiectului

[!include [banner](../includes/banner.md)]

Acest subiect oferă informații despre alocarea de resurse proiectului.

O provocare pentru managerii de proiect și managerii de resurse în etapa de planificare a proiectului este alocarea resurselor, în care aceștia trebuie să determine și să rezerve resursa corectă pentru a lucra la un proiect. În Dynamics 365 Finance, capabilitățile de resurse pentru proiecte vă permit să definiți roluri care sunt tratate ca resurse temporare care pot fi rezervate pentru o anumită implicare sau o parte dintr-o implicare. Acest tip de alocare de resurse permite managerilor de proiect și managerilor de resurse să îndeplinească următoarele sarcini:

- Definirea unui rol care are competențele necesare, astfel încât să fie ușor să potrivească resursele.
- Folosirea de roluri pentru a defini un program inițial de implicare bazat pe resurse rezervate.
- Estimarea costurilor și determinarea unui buget inițial, pe baza rolurilor și resurselor atribuite pentru un proiect.
- Folosirea de roluri pentru a estima numărul de rezervări de resurse necesare pentru fiecare implicare.
- Estimarea numărului de resurse necesare pentru întregul ciclu de viață al unui proiect.
- Elaborarea structurii detaliate a proiectului (WBS) utilizând atribuirile inițiale de resurse.

[![Ciclul de viață al proiectului](./media/projectresourcing02-1024x812.jpg)](./media/projectresourcing02.jpg)

Pe măsură ce planificarea proiectului continuă, resursele planificate pot fi înlocuite cu resurse de personal. Managerul de proiect poate, de asemenea, să revină și să actualizeze rezervările de resurse în orice etapă a proiectului.

## <a name="set-up-project-resources"></a>Configurarea resurselor proiectului
Trebuie să configurați un calendar și să îl asociați cu un angajat sau cu un lucrător. Calendarul este folosit pentru a planifica proiectul și timpul de lucru al resurselor rezervate pentru proiect. În timpul configurării calendarului, managerii de proiect pot realiza nivelarea resurselor ca parte a optimizării resurselor. Pe baza planificării calendaristice, pot fi impuse restricții asupra resurselor. Puteți configura un calendar din pagina **Calendare**.

Când configurați un angajat ca resursă a proiectului, puteți selecta dintre angajații care lucrează în compania pentru care configurați resursele. Alternativ, puteți selecta angajați din alte companii din organizația dvs. Acești angajați sunt cunoscuți ca resurse între companii.

Următoarele proceduri explică cum să configurați un angajat ca o resursă de proiect în compania dvs. și cum să configurați o resursă de proiect între companii.

### <a name="set-up-a-worker-as-a-project-resource"></a>Configurați un angajat ca resursă a proiectului

1. Din pagina **Angajați**, în lista **Angajați**, selectați angajatul pe care îl adăugați ca resursă a proiectului și deschideți înregistrarea angajatului.
2. În panoul de acțiuni, selectați **Proiect** &gt; **Configurare** &gt; **Configurarea proiectului**.
3. Selectați un calendar, apoi închideți pagina.

De asemenea, puteți specifica proiecte implicite pentru o resursă ca un tip de pre-atribuire. Pre-atribuirile pot fi utilizate atunci când managerul de resurse sau managerul de proiect știe în avans la ce proiecte va lucra resursa. Pre-atribuirile se pot baza și pe cererea unui sponsor de proiect sau a unui client. Pentru a pre-atribui un proiect, din pagina **Atribuire proiecte**, în fila **Proiecte**, în lista **Proiecte rămase**, selectați proiectul corespunzător.

### <a name="set-up-an-intercompany-resource"></a>Configurați o resursă între companii

Când configurați un angajat ca resursă între companii, trebuie să finalizați configurarea atât în compania sursă, cât și în cea țintă.

**În compania sursă**

1. În Finanțe, verificați dacă este selectată compania sursă, apoi finalizați procedura din secțiunea anterioară „Configurați un angajat ca resursă a proiectului”.
2. În pagina **Contabilitate între companii**, selectați **Nou**.
3. În câmpul **ID-ul entității juridice**, selectați compania sursă. Completați corespunzător câmpurile rămase, și apoi selectați **Salvare**.
4. În pagina **Preț de transfer**, selectați **Nou**.
5. În câmpul **Entitate juridică țintă**, selectați compania adecvată.
6. Pentru a împrumuta companiei țintă numai resursa pe care ați creat-o la începutul acestei secțiuni, în câmpul **Resursă**, selectați numele resursei pe care ați creat-o. Pentru a pune la dispoziția companiei țintă toate resursele din compania sursă, lăsați câmpul **Resursă** necompletat.
7. Din pagina **Managementul proiectului și parametri contabili**, în fila **Între companii**, setați opțiunea **Activați planificarea resurselor și foilor de pontaj între companii** la **Da**.

**În compania țintă**

- Din pagina **Lista resurselor**, în filtrul de căutare, introduceți numele resursei pe care ați creat-o pentru compania sursă, pentru a verifica dacă numele este inclus în lista de resurse pentru compania țintă.

## <a name="manage-resource-competencies"></a>Gestionarea competențelor de resurse
Competențele de resurse sunt o parte esențială a gestionării resurselor. Competențele pot fi utilizate ca bază pentru a determina resursele care au echilibrul corect de abilități, educație, certificare și experiență în proiect. Ar trebui să configurați aceste informații pentru fiecare resursă și să le actualizați în mod regulat. În acest fel, puteți maximiza capacitățile atunci când competențele specifice resurselor sunt potrivite în timpul alocării resurselor proiectului.

[![Exemple de abilități, certificări, educație și experiență în proiect](./media/projectresourcing06-1024x383.jpg)](./media/projectresourcing06.jpg)

Următoarele proceduri explică modul de configurare a unor competențe pentru o resursă.

Pentru a configura competențe pentru un angajat, puteți utiliza fie pagina listei **Angajați** în Resurse umane sau pagina listei **Resurse** în Gestionarea proiectelor și contabilitate. Pentru următoarele proceduri, este utilizată pagina listei **Angajați** din Resurse umane.

### <a name="set-up-competencies-certificates"></a>Configurare competențe: certificate

1. Din pagina listei **Angajați**, selectați linia pentru care angajatul va adăuga informații despre certificat.
2. În panoul de acțiuni, în fila **Angajat**, în grupul **Competențe**, selectați **Certificate**.
3. Selectați **Nou**, și apoi din câmpul **Tip certificat**, selectați **PMP**.
4. În câmpul **Dată de început**, selectați **10/1/2015**, și selectați **Salvare**.

### <a name="set-up-competencies-skills"></a>Configurare competențe: abilități

1. În pagina listei **Angajați**, asigurați-vă că angajatul pe care l-ați folosit în procedura anterioară este încă selectat. Apoi, în panoul de acțiuni, în fila **Angajat**, în grupul **Competențe**, selectați **Abilități**.
2. Selectați **Nou**.
3. În câmpul **Abilitate**, selectați **Management de proiect**.
4. În câmpul **Nivel**, selectați **5 Expert**.
5. În câmpul **Dată nivel**, selectați **1-/14/2014**.
6. În câmpul **Ani de experiență**, introduceți **10**.
7. Selectați **Salvare**, apoi închideți pagina.

## <a name="create-a-new-project"></a>Creați un nou proiect
1. În pagina **Management de proiect**, selectați **Proiect nou**, și introduceți următoarele valori:

    - **Tipul proiectului:** Timp și material
    - **Denumirea proiectului:** Faza 2 de upgrade XYZ
    - **Grup de proiect:** TM\_WIP
    - **ID contract proiect:** 00000002

2. Selectați **Creați un proiect**.

### <a name="assign-a-resource-to-a-project"></a>Atribuirea unei resurse unui proiect

1. Din pagina **Angajați**, în lista **Angajați**, selectați înregistrarea pentru angajatul pentru care ați configurat anterior competențele, și deschideți înregistrarea angajatului.
2. În panoul de acțiuni, în fila **Proiect**, în grupul **Configurare**, selectați **Atribuire proiecte**.
3. Din pagina **Validarea resurselor pentru atribuiri în proiect**, din fila **Proiecte**, în câmpul **Adăugați proiectul la proiectele selectate**, filtrați pentru proiectul **Faza 2 de upgrade XYZ**.
4. În panoul **Proiecte rămase**, selectați un proiect, apoi selectați butonul săgeată pentru a-l adăuga la panoul **Proiecte selectate**.

De asemenea, puteți atribui categorii pentru o resursă după cum doriți. Tipul categoriei este fie **Cost** fie **Venit**. Tipul categoriei este determinat de organizația dvs. Dacă nu sunt alocate categorii pentru o resursă, Finanțele caută categoria implicită a prețurilor orare pentru costuri și venituri.

### <a name="set-up-project-resource-and-role-characteristics"></a>Configurați resursele proiectului și caracteristicile rolului

Un manager de proiect poate utiliza funcționalitatea de alocare de resurse proiectului pentru a crea rolurile necesare pentru proiect. Rolurile pot fi utilizate dacă resursele confirmate sunt încă necunoscute atunci când resursele sunt rezervate. Rolurile pot fi rezervate temporar ca resurse planificate, astfel încât să puteți continua etapele de planificare a proiectului.

[![Exemplu de rol](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Scenariu:** Contoso a fost angajat pentru a finaliza un proiect de timp și materiale care are o cartă de proiect aprobată. Managerul de proiect junior continuă să finalizeze domeniul de aplicare al proiectului. Managerul de resurse identifică în prezent resursele specifice care vor fi rezervate pentru a lucra la noul proiect. Datorită naturii critice a proiectului, sponsorul proiectului a solicitat managerul de proiect senior ca unul dintre roluri. Managerul de resurse trebuie să dobândească noua resursă și să definească rolul în sistem în cazul în care managerul de proiect junior are nevoie de informații despre resurse în timpul planificării proiectului.

Următorii pași arată modul în care managerul de resurse poate configura rolul de manager de proiect senior și poate asocia caracteristicile resursei acestuia. Ulterior, rolul poate fi folosit pentru a căuta resursele disponibile care corespund competențelor necesare pentru resursă.

1. În pagina **Configurare roluri**, selectați **Nou**, și introduceți următoarele valori:

    - **ID rol:** Manager de proiect senior
    - **Descriere:** Manager de proiect senior

2. Selectați **Creare**.
3. Selectați rolul **Manager de proiect senior**, apoi selectați **Configurare caracteristici**.
4. În câmpul **Tip caracteristici**, selectați **Abilitate**.
5. În câmpul **Caracteristici disponibile**, introduceți abilitatea de căutat.
6. În câmpul **Tip caracteristică**, selectați **Certificat**.
7. În câmpul **Caracteristici disponibile**, introduceți tipul de certificat de căutat.

### <a name="assign-a-project-resource-to-a-project"></a>Atribuirea unei resurse de proiect unui proiect

1. Din pagina **Toate proiectele**, selectați proiectul **Faza 2 de upgrade XYZ**.
2. Din fila **Echipa proiectului și planificarea**, selectați **Adăugare**.
3. În câmpul **Rol**, selectați **Membru al echipei**.
4. Selectați **Rezervare din calendar**.
5. Din pagina **Disponibilitate resurse**, selectați **Vizualizare setări**.
6. În pagina **Reglați setările de vizualizare**, introduceți următoarele valori:

    - **Format pentru vizualizarea intervalului de dată:** Zi
    - **Afișați descrierile disponibilității:** Da
    - **Afișați capacitatea rămasă:** Da

7. În lista de resurse, selectați o resursă.
8. Selectați **Rezervare fermă** și **Capacitate completă**.


### <a name="assign-a-resource-to-a-default-role"></a>Atribuirea unei resurse unui rol implicit

Pentru a ajuta managerii de proiect sau de resurse pentru drill down mai mult pentru resursele care pot fi rezervate pentru un proiect. Puteți asocia un rol implicit cu o resursă existentă sau cu o resursă nou achiziționată. De exemplu, când Daniel a fost angajat, avea experiența și abilitățile pentru a ocupa rolul de analist de afaceri. Managerul de resurse a atribuit acest rol ca rolul implicit al lui Daniel. Prin urmare, managerul de resurse l-a adăugat pe Daniel la un grup de analiști de afaceri care sunt disponibili să lucreze la proiecte.

În timpul rezervării resurselor, managerii de proiect pot filtra resursele de rol disponibile pentru a lucra la proiecte. Aceștia pot utiliza aceste informații ca un criteriu atunci când efectuează o analiză a deciziilor pe mai multe criterii în timpul îndeplinirii resurselor. De asemenea, pot adăuga alte caracteristici ale resurselor la filtru pentru a căuta resurse care au abilități, educație și experiență specifice pentru un anumit proiect.

**Scenariu:** A început un proiect aprobat, iar rolul Manager de proiect senior a fost rezervat ca resursă planificată în etapa de planificare a proiectului. Managerul de resurse a achiziționat acum o resursă pentru a îndeplini rolul de manager de proiect senior.

1. Din pagina **Lista resurselor**, selectați **Daniel Goldschmidt**.
2. În pagina **Rol resursă**, selectați **Nou**, și introduceți următoarele valori:

    - **În vigoare:** Introduceți data curentă.
    - **Expirare:** introduceți **Niciodată**.
    - **Rol:** introduceți **Manager de proiect senior**.

3. Selectați **Salvare**, apoi închideți pagina.
4. Din fila **Competențe**, adăugați abilitatea **ProjectMgmt** și certificatul **PMP**.

## <a name="set-up-role-based-pricing"></a>Configurați prețurile bazate pe roluri
Toate costurile, vânzările și prețurile de transfer pot fi configurate pentru roluri.

1. Din pagina **Preț de vânzare (oră)**, selectați **Nou**, și introduceți o dată efectivă.
2. În coloana **Rol**, selectați un rol.
3. În coloana **Prețuri**, introduceți un preț pentru rolul de resursă selectat.

## <a name="form-a-project-team"></a>Formați o echipă de proiect
Pentru a utiliza rolurile care au fost configurate anterior într-un proiect, un manager de proiect trebuie să asocieze rolurile cu proiectul. Pentru un proiect pot fi atribuite mai multe roluri. Pentru a preveni confuzia, aceste roluri sunt etichetate automat în timpul rezervării. De exemplu, dacă managerul de proiect necesită trei ingineri software, trei roluri de inginer software care au etichetele **inginer software 1**, **inginer software 2**, și **inginer software 3** sunt generate automat. Când caracteristicile rolului au fost setate anterior pentru rol, acestea sunt aplicate ca filtru în timpul căutărilor unei resurse. Pot fi adăugate caracteristici suplimentare, după cum este necesar, pentru a rafina în continuare căutarea.

Setările de vizualizare pot fi, de asemenea, personalizate pentru a oferi o imagine mai bună a disponibilității resurselor. Există opțiuni pentru a afișa disponibilitatea orară, zilnică, săptămânală, lunară, trimestrială și anuală. Există, de asemenea, o opțiune pentru a arăta capacitatea disponibilă și rămasă pentru resurse. Această opțiune este utilă pentru gestionarea timpului, atunci când estimați timpul disponibil pentru activități sau disponibilitatea resurselor.

Managerul de proiect poate selecta un rol pe pagină și apoi, dacă există o resursă disponibilă care se potrivește cerinței, selectează să rezerve o resursă pentru a ocupa rolul. Rețineți că resursele nu trebuie rezervate în acest moment în etapa de planificare. Când creați un WBS, puteți înlocui rolurile cu resurse de personal pentru proiect. Dacă rolurile sunt înlocuite cu resurse de personal în WBS, configurarea resurselor actualizează automat lista și programarea echipei de proiect.

[![Listarea echipei de proiect care include atât roluri, cât și resurse reale](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

Managerul de proiect are diverse opțiuni pentru rezervarea unei resurse pentru un proiect, cum ar fi **Capacitate rămasă**, **Capacitate completă**, **Procent de capacitate**, și **Specificare ore**. Aceste opțiuni de rezervare pot fi anulate în orice moment în cazul în care se schimbă atribuirea resurselor. Sunt acceptate două tipuri de rezervări:

- **Rezervare fermă** - Rezervarea resurselor a fost aprobată și confirmată pentru a lucra la implicare pe durata specificată.
- **Rezervare provizorie** - Rezervarea resurselor a fost stabilită provizoriu pentru a lucra la implicare pe durata specificată.

Următoarea procedură explică cum se creează o echipă de proiect.

### <a name="create-a-project-team"></a>Crearea unei echipe de proiect

1. Din pagina listă **Toate proiectele**, selectați un proiect, apoi selectați **Editare**.
2. Din fila **Echipa proiectului și planificarea**, în câmpul **Data de încheiere a planificării**, introduceți data de începere a planificării plus o lună. De exemplu, dacă data de începere a planificării este 24 iunie 2017 (24/06/2017), introduceți **24/07/2017**.
3. Selectați **Adăugare**.
4. În panoul **Adăugare roluri la proiect**, în câmpul **Rol**, selectați **Manager de proiect senior**.
5. Selectați **Competențe necesare**.
6. Din pagina **Alegere caracteristici**, caracteristicile pe care le-ați setat anterior pentru rolul de manager de proiect senior sunt selectate în mod implicit. Selectați **OK**.
7. Din pagina **Adăugare roluri la proiect**, în câmpul **Număr de resurse**, introduceți **1**.
8. În câmpul **Resursă**, căutarea arată toate resursele care au competențele necesare. Selectați **Daniel Goldschmidt**, apoi selectați **Creare**.
9. În pagina **Proiect**, selectați **Adăugare**.
10. În panoul **Adăugare roluri la proiect**, în câmpul **Rol**, selectați **Membru al echipei**. În câmpul **Număr de resurse**, introduceți **5**.
11. Selectați **Creare**.
12. Din pagina **Proiecte**, selectați **Completați resursa**.

## <a name="resource-capacity-synchronization"></a>Sincronizarea capacității resursei
Procesele de sincronizare a resurselor contribuie la garantarea faptului că informațiile pentru calendar și calendarul de bază se transferă în planificarea resurselor proiectului. Când calendarul este modificat, procesele fac actualizările necesare pentru planificarea resurselor proiectului. Procesele contribuie, de asemenea, la îmbunătățirea performanței, deoarece informațiile despre resurse ale calendarului sunt sincronizate în avans. Prin urmare, actualizările informațiilor de planificare a resurselor apar mai rapid. Vă recomandăm să planificați procesele ca un lot în loc de unul câte unul. În caz contrar, există riscul ca cineva să uite datele inclusive în care informațiile au fost sincronizate ultima dată. Dacă datele inclusive nu sunt utilizate, pot apărea lacune în timpul sincronizării datei.

![Sincronizare calendar](./media/projectresourcing04-1024x471.jpg)

### <a name="synchronize-resource-capacity-roll-ups"></a>Cumulări de sincronizare a capacității resursei

Procesul de sincronizare este conceput pentru a sincroniza toate informațiile din calendarul resurselor. Aceste informații includ informații de bază despre calendar despre orice modificare a tabelului de capacitate a calendarului de resurse al proiectului. Dacă în proiect sunt adăugate resurse noi, sincronizarea ajută la garantarea disponibilității informațiilor de calendar actualizate. Această sincronizare se poate face oricând.

Vă recomandăm să utilizați un lot. Opțiunile sunt disponibile în timpul sincronizării rezervărilor de capacitate.

1. Selectați **Management de proiect și contabilitate** &gt; **Periodic** &gt; **Sincronizarea capacității** &gt; **Cumulare sincronizare resurse de capacitate**.
2. Setați opțiunile în tabelul următor.

    | Opțiune      | Descriere |
    |-------------|-------------|
    | Codul perioadei | Opțional, selectați codul intervalului de dată pentru registrul general pentru a seta datele de început și de sfârșit pentru procesul de sincronizare pentru cumulările de capacitate a resurselor. |
    | Data de început  | Introduceți data de începere pentru procesul de sincronizare pentru cumulările de capacitate a resurselor. |
    | Dată de sfârșit    | Introduceți data de încheiere pentru procesul de sincronizare pentru cumulările de capacitate a resurselor. |

[![Proces de sincronizare](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)

## <a name="set-up-roles-on-wbs-templates"></a>Configurați roluri pe șabloanele WBS
Managerii de proiect pot configura șabloanele WBS pe care le pot aplica atunci când creează un WBS pentru noi proiecte. Managerii de proiect pot adăuga roluri atunci când creează un șablon. Utilizați următoarea procedură pentru a atribui un rol unui șablon WBS.

1. Selectați **Management de proiect și contabilitate** &gt; **Configurare** &gt; **Proiecte** &gt; **Șabloane structură detaliată a proiectului**.
2. Selectați **Detalii** pentru un șablon WBS selectat.
3. Selectați o sarcină din listă și apoi în câmpul **Rol**, selectați un rol pe care să îl atribuiți sarcinii.

### <a name="work-with-a-wbs"></a>Lucrul cu un WBS

Aveți posibilitatea să creați un nou WBS, sau puteți copia un WBS existent ca șablon WBS. Un manager de proiect poate gestiona cu ușurință resursele atribuind roluri noilor sarcini de pe WBS. Rolurile pot fi înlocuite fie după obținerea unei resurse, fie după identificarea unei resurse confirmate pentru a lucra la sarcină. Această flexibilitate permite managerilor de proiect să îndeplinească următoarele sarcini:

- Identificarea numărului de resurse necesare pachetelor de lucru WBS.
- Estimarea costurilor proiectelor.
- Determinarea unui buget preliminar.
- Estimarea duratei activității, pe baza rolurilor și resurselor.
- Elaborarea câtorva planuri de management de proiect, pe baza informațiilor disponibile despre proiect.

Opțiuni suplimentare au fost adăugate în WBS pentru a utiliza mai bine funcționalitatea de resurse.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Opțiune</th>
<th>Descriere</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Atribuiri de resurse</td>
<td>Vizualizați resursele alocate, datele, numărul de ore și tipul de rezervare pentru sarcini pe WBS.</td>
</tr>
<tr class="even">
<td>Generare automată echipă</td>
<td>Adăugați automat resurse planificate utilizând roluri asociate cu o sarcină. Finanțele sugerează automat resursele planificate utilizând analiza deciziilor cu mai multe criterii, care se bazează pe roluri. După ce rolurile și efortul (orele) au fost stabilite pentru sarcinile dintr-un WBS și după ce structura a fost lansată, selectați <strong>Generarea automată a echipei</strong>. Numărul necesar de resurse planificate este adăugat la WBS și la fila <strong>Planificarea proiectului și echipei</strong>.</td>
</tr>
<tr class="odd">
<td>Resursă (listă verticală)</td>
<td>Din pagina <strong>Lansare atribuire resurse</strong>, puteți selecta resurse pentru rezervare fermă sau rezervare provizorie, în funcție de durata specificată. Puteți ajusta setările de vizualizare pentru a vedea și seta durata activităților de resurse. Puteți selecta și atribui resurse la nivelul pachetului de lucru utilizând următoarele opțiuni:
<ul>
<li><strong>Accept</strong> - Confirmați modificările resursei care este atribuită unei sarcini.</li>
<li><strong>Anulare</strong> - Anulați modificările resursei care este atribuită unei sarcini.</li>
<li><strong>Alocare automată</strong> - O resursă de personal disponibilă care are un rol potrivit este selectată automat și atribuită sarcinii selectate.</li>
</ul></td>
</tr>
</tbody>
</table>

1. Din pagina **Toate proiectele**, selectați proiectul **Faza 2 de upgrade XYZ**.
2. Selectați **Plan** &gt; **Activități** &gt; **Structură detaliată a proiectului**.
3. Selectați **Nou** pentru a adăuga la WBS următoarele activități de nivel unu:

    - Inițiere
    - Se planifică
    - Se execută
    - Monitorizare și control
    - Închideți

4. Setați datele și efortul (orele), așa cum se arată în ilustrația următoare.

    [![Stabilirea datelor și efortului](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)

5. Selectați linia de sarcină **Inițiere** și apoi în câmpul **Rol**, selectați **Manager de proiect senior**.
6. Selectați **Publicare**.
7. Pe aceeași linie, în câmpul **Resursă**, selectați **Daniel Goldschmidt**, apoi selectați **Accept**.
8. Selectați linia de sarcină **Planificare** și apoi în câmpul **Rol**, selectați **Analist de afaceri**.
9. Selectați **Publicare**, apoi selectați **Generarea automată a echipei**.
10. În caseta de mesaj care apare, selectați **Da**.
11. În câmpul **Resursă**, verificați dacă valoarea este **Analist de afaceri 1**.
12. Pentru resursa **Analist de afaceri 1**, deschideți căutarea și selectați **Lansare atribuiri de resurse**. Apoi selectați un angajat pentru sarcină.
13. Selectați **Atribuire provizorie** &gt; **Capacitate completă**.

    > [!NOTE] 
    > Nu primiți un avertisment că resursa specificată este acum 2, deoarece numărul de resurse rămâne 1.

14. Din pagina **Structură detaliată a proiectului**, validați atribuirea resurselor pe WBS, apoi selectați **Salvare**.

## <a name="resource-fulfillment-for-planned-resources"></a>Completarea resurselor pentru resursele planificate
Un manager de proiect poate planifica rolurile de resurse necesare pentru un proiect. Managerul de resurse va vedea aceste resurse planificate ca solicitări în pagina **Completarea resurselor** și poate atribui resurse reale.

1. Din pagina **Toate proiectele**, selectați proiectul **Faza 2 de upgrade XYZ**.
2. Selectați **Proiect**, apoi selectați **Editare**.
3. Din fila **Echipa proiectului și planificarea**, selectați **Adăugare**.
4. În caseta de dialog **Adăugare roluri**, selectați rolul **Dezvoltator de software**.
5. Selectați **Creare**, apoi închideți pagina proiectului.
6. Din pagina **Completarea resurselor**, selectați **Dezvoltator de software 1** pentru proiectul **Proiect Faza 2 de upgrade XYZ**.
7. Selectați un angajat, apoi selectați **Atribuire**.
8. Verificați dacă linia pentru **Dezvoltator de software 1** a fost eliminată pentru proiectul **Proiect Faza 2 de upgrade XYZ**.
9. Din fila **Echipa proiectului și planificare**, pentru proiectul **Faza 2 de upgrade XYZ**, verificați dacă angajatul pe care l-ați selectat în pasul anterior a fost adăugat ca **Dezvoltator de software**.

## <a name="requests-for-project-resources"></a>Cereri pentru resurse ale proiectului
Funcționalitatea pentru planificarea resurselor proiectului permite doar managerilor de resurse să distribuie resursele de personal pe implicări sau proiecte. Pentru a activa această funcționalitate, finalizați următoarele activități sau verificați dacă acestea au fost finalizate:

- Configurare secvențe numerice.
- Configurare fluxuri de lucru de management de proiect și contabilitate.
- Activare fluxuri de lucru de solicitare a resurselor.

După finalizarea sarcinilor precedente, puteți finaliza următoarele sarcini după necesități:

- Crearea unei solicitări de resursă dintr-o resursă de personal cu rezervare provizorie.
- Monitorizarea solicitărilor de resurse.
- Completarea solicitărilor de resurse.
- Solicitarea unei resurse de personal de la o WBS.
- Rezervarea de resurse la un proiect fără a avea o solicitare pentru o resursă de personal.

## <a name="monitor-project-teams"></a>Monitorizarea echipelor de proiect
1. Din pagina **Toate proiectele**, selectați linkul **ID proiect** pentru proiectul **Faza 2 de upgrade XYZ**.
2. Din fila rapidă **Echipa proiectului și planificarea**, verificați dacă resursele proiectului ce sunt listate sunt corecte.
