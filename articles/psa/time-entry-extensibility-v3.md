---
title: Particularizarea înregistrării săptămânale de timp
description: Acest subiect furnizează informații despre cum să implementați reguli de business particularizate care susțin practicile unei organizații.
author: stsporen
ms.custom:
- dyn365-projectservice
ms.date: 07/09/2019
ms.topic: article
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
ms.openlocfilehash: fa2ef927e0234919ee4777f24c60569fb33a8570f6d48be6aef356df4f08a6e7
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/06/2021
ms.locfileid: "7002301"
---
# <a name="customize-weekly-time-entry"></a>Particularizarea intrărilor de timp săptămânale 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

În Microsoft Dynamics 365 Project Service Automation versiunea 3.3, Microsoft a introdus o grilă modernă care le permite resurselor unui proiect să introducă rapid timpul pentru până la o săptămână o dată. Noua grilă de introducere a timpului săptămânal poate afișa totaluri pentru intrări după dată, rând sau săptămână. Resursele pot face copii ale înregistrărilor de timp în săptămâna și, de asemenea, în copii vrac din săptămânile anterioare. Particularizatoarele de sistem pot personaliza vizualizarea adăugând câmpuri, adăugând căutări la alte entități și implementând reguli de afaceri particularizate pentru a accepta practicile organizației lor.

Introducerea de timp și noua grilă săptămânală de timp sunt accesate prin intermediul hărții site-ului. Experiența de introducere a timpului particularizată non-extensibilă care făcea parte din versiunile PSA anterioare a fost înlocuită de grila de introducere săptămânală a timpului extensibilă și, de asemenea, de o experiență alternativă în grila și calendarul doar în citire. Din cauza acestei modificări, utilizatorii pot introduce timp în calupuri săptămânale.

## <a name="page-layout"></a>Aspect pagină
Noua grilă de introducere de timp săptămânal este un control particularizat care are o bară de instrumente și două secțiuni principale **Dimensiuni** și **Durată**. Bara de instrumente include un buton care se aplică numai la acest control particularizat pentru grila de introducere de timp. În contrast, butoanele din panoul de acțiuni din partea de sus a paginii se aplică celor trei tipuri de controale care sunt acceptate pentru introducerea de timp: controlul de introducere săptămânală a timpului, controlul doar în citire și controlul calendarului.

### <a name="dimensions"></a>Dimensiuni
Secțiunea **Dimensiuni** afișează, ca titluri de coloană, toate dimensiunile la care se poate introduce timpul. Următoarele dimensiuni sunt suportate predefinit:

- Proiect
- Sarcina proiectului
- Rol
- Tip
- Stare intrare

Secțiunea **Dimensiuni** nu permite editarea inline. Această secțiune este susținută de o vizualizare care permite adăugarea de câmpuri particularizate la grila de introducere săptămânală a timpului. Pentru informații despre cum se adaugă câmpuri particularizate, consultați secțiunea „Extensibilitate” mai jos în acest subiect.

### <a name="duration"></a>Durată
Secțiunea Durată afișează zilele săptămânii ca anteturi de coloană. Această secțiune permite editarea inline. După ce se creează un rând de introducere de timp care are dimensiuni corespunzătoare, utilizatorii pot introduce rapid, inline, cantitatea de timp pe care au cheltuit-o pe aceste dimensiuni.

## <a name="create-a-new-time-entry"></a>Creați o înregistrare nouă de timp
Pentru a crea o nouă înregistrare de timp în grila de introducere a timpului, selectați **Nou**. Apare caseta de dialog **Creare rapidă înregistrare de timp**. În această casetă de dialog, utilizatorii pot selecta data înregistrării de timp, apoi introduc date pentru dimensiunile **Proiect**, **Activitate proiect**, **Rol** și **Durată** în minute, ore sau zile, tastând **h**, **m**, sau **d**, împreună cu numărul. Utilizatorii pot introduce, de asemenea, o descriere și comentarii care pot fi partajate extern pentru înregistrarea de timp. Când utilizatorii salvează modificările, valorile pe care le-au introdus pe dimensiuni apar în secțiunea **Dimensiuni**. Informațiile privind durata pe care le-au introdus în câmpul **Durată** apar la data pentru care a fost creată înregistrarea de timp.

Câmpurile de căutare sunt susținute de vizualizări de sistem. De exemplu, după ce un utilizator intră într-o **Activitate proiect,** câmpul este setat la vizualizarea **Copiere** în mod implicit. Pentru a crea înregistrări de timp pentru activități care nu sunt atribuite unui utilizator, selectați **Schimbare vizualizare** în caseta de dialog căutare, apoi selectați vizualizarea **Toate sarcinile de proiect active**.

## <a name="edit-a-time-entry"></a>Editați o înregistrare de timp
Detaliile din unele câmpuri din pagina de introducere de timp, precum **Descriere** și **Comentarii externe**, nu sunt afișate în grila de introducere săptămânală a timpului. În schimb, un mic indicator triunghiular apare în celulele de durată care au aceste detalii suplimentare. Selectați celula, apoi selectați **Editare detalii** pentru a vizualiza datele în panoul de **Editare rapidă**. Pentru a edita sau actualiza detaliile pentru o anumită înregistrare de timp care nu face parte din grila săptămânală de introducere de timp, utilizatorii trebuie să deschidă **Panoul de editare rapidă**.

## <a name="copy-a-time-entry-row"></a>Copierea unei înregistrări de timp
După ce a fost creat primul rând de înregistrare de timp, utilizatorii pot selecta **Copiere rând** pentru a copia întregul rând pe un rând nou. Atunci când un rând este copiat în acest fel, dimensiunile și duratele sunt, de asemenea, copiate. Utilizatorii pot selecta, de asemenea, **Editare rând** pentru a actualiza inline valorile de dimensiune și duratele în secțiunea **Durată**.

## <a name="open-a-time-entry"></a>Deschideți o înregistrare de timp
Pentru a sprijini introducerea optimă și rapidă în cele mai proeminente câmpuri, grila săptămânală de introducere a timpului afișează un subset de dimensiuni și durate de timp selectate. Pentru a vizualiza toate detaliile unei singure introduceri de timp, sub **Editare intrare**, selectați **Deschidere**.

## <a name="submit-a-time-entry"></a>Remiteți o înregistrare de timp
Utilizatorii pot remite o singură înregistrare de timp sau un grup de înregistrări de timp selectând un bloc de celule sau un rând întreg de introducere de timp, apoi selectând **Remitere**. Înregistrările de timp remise apar ca înregistrări în curs de aprobare pe pagina **Aprobare** a aprobatorilor. După ce înregistrările de timp sunt remise cu succes, ele nu pot fi editate.

## <a name="recall-a-time-entry"></a>Retrageți o înregistrare de timp
Puteți retrage înregistrările de timp pe care le-ați remis. Puteți retrage o singură înregistrare, un bloc de înregistrări de timp sau un întreg rând de înregistrări de timp. Intrările de timp retrase sunt disponibile pentru resurse pentru editare.

## <a name="time-entry-status"></a>Stare înregistrare timp
Noilor înregistrări de timp li se atribuie automat un statut **Proiect**. Când este depusă o înregistrare de timp, starea este actualizată la **Trimis**. Când o înregistrare de timp depusă este aprobată, starea este actualizată la **Aprobat**. Dacă o înregistrare de timp este respinsă, starea este actualizată la **Returnat**, iar înregistrarea devine disponibilă pentru corectare și retransmitere. Numai înregistrările de timp cu starea **Proiect** pot fi șterse.

## <a name="view-rejection-comments"></a>Vizualizați comentarii de respingere
Atunci când o înregistrare de timp este respinsă de un aprobator, aprobatorul poate adăuga comentarii de respingere pentru a ajuta resursa să înțeleagă motivul respingerii. Pentru a vizualiza comentariile de respingere pentru o înregistrare de timp, selectați **Deschidere înregistrare**. Comentariile de respingere vor fi afișate în cronologie. În cronologie, resursa poate răspunde la comentariile de respingere înainte de a remite înregistrarea.

## <a name="copy-week"></a>Copiați săptămâna
După ce au fost create câteva înregistrări de timp, utilizatorii pot selecta **Copiere săptămână** pentru a crea în bloc înregistrări de timp suplimentare. Apare caseta de dialog **Copiere**. În secțiunea **De la perioada**, utilizați câmpurile **Data de început** și **Data de sfârșit** pentru a defini intervalul de date din care să copiați înregistrările de timp. În secțiunea **La perioadă**, în câmpul **Data de început**, specificați data pentru care să creați înregistrări de timp. Apoi selectați **Copiere**. Pentru data specificată în perioada „la", se creează o copie a înregistrărilor de timp pentru ziua corespunzătoare a săptămânii în perioada „de la". De exemplu, înregistrarea de timp pentru luni de săptămâna trecută este copiată pentru lunea săptămânii indicate drept perioada „la".

## <a name="import"></a>Import
Același proces de bază este utilizat pentru importul din rezervări, misiuni și schimburi. Utilizatorii pot specifica intervalul de date din care se importă rezervările. Apoi, aceștia trebuie să aleagă în mod explicit rezervările care ar trebui să fie copiate în înregistrările de timp în schiță. În versiunea anterioară, înregistrările de timp sugerate apăreau în grilă și în calendar și se pierdeau atunci când sesiunea era reîmprospătată.

## <a name="extensibility"></a>Extensibilitate
### <a name="add-custom-fields-that-have-lookups-to-other-entities"></a>Adăugați câmpuri particularizate care au căutări la alte entități
Există trei pași principali pentru adăugarea unui câmp particularizat la grila de intrare de timp săptămânală.

1.  Adăugați câmpul particularizat la caseta de dialog Creare rapidă.
2.  Configurați grila pentru a afișa câmpul particularizat.
3.  Adăugați câmpul particularizat fie la rândul de flux de activități de editare, fie la fluxul de activități de editare a celulei, după caz.

De asemenea, trebuie să vă asigurați că noul câmp are validările necesare în fluxul de activitate de editare a rândului sau celulei. Ca parte a acestui pas, trebuie să blocați câmpul, pe baza stării înregistrării de timp.

#### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Adăugați câmpul particularizat la caseta de dialog Creare rapidă
Trebuie să adăugați câmpul particularizat în caseta de dialog Creare introducere rapidă a înregistrării de timp. astfel încât utilizatorii să poată introduce o valoare pentru aceasta atunci când adaugă înregistrări de timp utilizând butonul **Nou**.

#### <a name="configure-the-grid-to-show-the-custom-field"></a>Configurați grila pentru a afișa câmpul particularizat
Există două modalități pentru adăugarea unui câmp particularizat la grila de introducere de timp săptămânală. Prima opțiune este să particularizați **Vizualizarea înregistrărilor mele săptămânale** și să adăugați câmpul particularizat la acesta. Aveți posibilitatea să alegeți poziția și dimensiunea câmpului particularizat din grilă editând acele proprietăți în vizualizare.

A doua opțiune este să creați o nouă vizualizare de înregistrare de timp personalizată și să o setați ca vizualizare implicită. Această vizualizare ar trebui să conțină câmpurile **Descriere** și **Comentarii externe**, în plus față de coloanele pe care doriți să le aveți în grilă. Aveți posibilitatea să alegeți poziția, dimensiunea și ordinea implicită de sortare a grilei editând acele proprietăți în vizualizare. Apoi, configurați controlul particularizat pentru această vizualizare, astfel încât să fie un control **Grilă introducere timp**. Adăugați acest control la vizualizare și selectați-l pentru web, telefon și tabletă. Apoi, configurați parametrii pentru grila de introducere de timp săptămânal. Setați câmpul **Data de începere** la **msdyn_date**, setați câmpul **Durată** la **msdyn_duration** și setați câmpul **Stare** la **msdyn_entrystatus**. Pentru vizualizarea implicită, câmpul **Listă de stare doar în citire** este setat la **192350002,192350003,192350004**, câmpul **Flux activitate editare rând** este setat la **msdyn_timeentryrowedit** și **Flux sarcină editare celulă** este setat la **msdyn_timeentryedit**. Aveți posibilitatea să particularizați aceste câmpuri pentru a adăuga sau elimina starea doar în citire sau pentru a utiliza o altă experiență bazată pe sarcini (TBX) pentru editarea rândului sau a celulelor. Aceste câmpuri trebuie să fie legate la o valoare statică.

#### <a name="add-the-custom-field-to-the-appropriate-edit-task-flow"></a>Adăugați câmpul particularizat la fluxul de activități de editare corespunzătoare
Paginile TBX care sunt utilizate pentru editare pot fi găsite în **Procese**. Paginile implicite sunt **Project service - Editare rând înregistrare timp** și **Project service - Editare înregistrare timp**. Aveți posibilitatea fie să editați aceste pagini implicite, fie să creați noi pagini TBX particularizate.

> [!NOTE] 
> Ambele opțiuni vor elimina unele filtrări predefinite pe entitățile **Proiect** și **Sarcină proiect**, astfel încât toate vizualizările de căutare pentru entități vor fi vizibile. În mod implicit, numai vizualizările de căutare relevante sunt vizibile.

Trebuie să determinați fluxul de activitate corespunzător pentru câmpul particularizat. Cel mai probabil, dacă ați adăugat câmpul la grilă, acesta ar trebui să meargă fluxul de activități de editare câmp care este utilizat pentru câmpurile care se aplică la întregul rând de înregistrări de timp. În cazul în care câmpul particularizat are o valoare unică în fiecare zi, ar fi un câmp particularizat pentru **Ora de sfârșit**, acesta ar trebui să meargă în fluxul de activități de editare a celulei.

Pentru a adăuga câmpul particularizat la un flux de activitate, glisați un element **Câmp** în poziția corespunzătoare din pagină, apoi setați-i proprietățile. Setați proprietatea **Sursă** la **Înregistrare timp** și setați proprietatea **Câmp de date** la câmpul particularizat. Proprietatea **Câmp** specifică numele afișat pe pagina TBX. Selectați **Aplicare** pentru a vă salva modificările la câmp. Selectați apoi **Actualizare** pentru a vă salva modificările pe pagină.

Pentru a utiliza o nouă pagină particularizată TBX în schimb, creați un proces nou. Setați categoria la **Flux de business**, setați entitatea la **Înregistrare timp** și setați tipul de proces de afaceri la **Executare proces ca flux de activități**. Sub **Proprietăți**, proprietatea **Nume de pagină** trebuie setată la numele afișat pentru pagină. Adăugați toate câmpurile relevante la pagina TBX. Salvați și activați procesul și apoi actualizați proprietatea de control particularizat pentru fluxul de activități relevant la valoarea **Nume** în proces.

### <a name="add-new-option-set-values"></a>Adăugați noi valori set de opțiuni
Pentru a adăuga valori set de opțiuni la un câmp predefinit, deschideți pagina de editare pentru câmp, apoi, sub **Tip**, selectați **Editare** lângă setul de opțiuni. Apoi, adăugați o nouă opțiune care are o etichetă și o culoare particularizate. Dacă doriți să adăugați o nouă stare de înregistrare de timp, câmpul predefinit este **Stare înregistrare**, nu **Stare.**

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Desemnați o nouă stare de înregistrare de timp ca doar în citire
Pentru a desemna o nouă stare de înregistrare de timp ca doar în citire, adăugați noua valoare a înregistrare de timp (numărul, nu eticheta) la proprietatea **listă de stare doar în citire**. Partea editabilă a grilei de înregistrare de timp va fi blocată pentru rândurile care au starea nouă.
Apoi, adăugați reguli de afaceri pentru a bloca toate câmpurile de pe paginile TBX **Editare rând introducere timp** și **Editare înregistrare timp**. Puteți accesa regulile de business pentru aceste pagini deschizând editorul flux de business pentru pagină, apoi selectând **Reguli de afaceri**. Aveți posibilitatea să adăugați starea nouă la condiția din regulile de business existente sau să adăugați o nouă regulă de business pentru noua stare.

### <a name="add-custom-validation-rules"></a>Adăugarea de reguli de validare particularizate
Există două tipuri de reguli de validare pe care le puteți adăuga pentru experiența de grilă de introducere a timpului săptămânal: • Reguli de business pe partea de client care funcționează în casete de dialog de creare rapidă și pe pagini TBX • Validări de inserturi pe partea de server care se aplică la toate actualizările de înregistrări de timp

#### <a name="business-rules"></a>Regulile de business
Utilizați reguli de business pentru a bloca și debloca câmpuri, pentru a introduce valori implicite în câmpuri și pentru a defini validări care necesită informații numai din înregistrarea de intrare de timp curentă. Puteți accesa regulile de business pentru o pagină TBX deschizând editorul flux de business pentru pagină, apoi selectând **Reguli de business**. Aveți posibilitatea să editați regulile de business existente sau să adăugați o nouă regulă de business. Pentru validări și mai personalizate, puteți utiliza o regulă de business pentru a executa JavaScript.

#### <a name="plug-in-validations"></a>Validări insert
Ar trebui să utilizați validările de insert pentru orice validări care necesită mai mult context decât este disponibil într-o singură înregistrare de intrare de timp sau pentru orice validări pe care doriți să executați pe actualizările inline în grilă. Pentru a finaliza validarea, creați un insert particularizat pe entitatea de **Înregistrare timp**.

> [!IMPORTANT] 
> În prezent, o problemă cunoscută pe paginile TBX împiedică utilizatorii să corecteze informațiile și să re-selecteze Efectuat atunci când o actualizare nu reușește o validare de insert. Ca o soluție, configurați validări de regulă de business pentru a preveni această situație cât mai mult posibil.


[!INCLUDE[footer-include](../includes/footer-banner.md)]