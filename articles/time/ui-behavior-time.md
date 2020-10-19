---
title: Comportamentul interfeței de utilizare a intrării în timp
description: Acest subiect oferă informații despre comportamentul intrării de timp a interfeței de utilizator.
author: stsporen
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 86f805cd33f81e70bf9ae3c1fb20a1c310473604
ms.sourcegitcommit: 2cf93d8bf0be5b61a739195a41334c34d910e9ba
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961739"
---
# <a name="time-entry-ui-behavior"></a>Comportamentul interfeței de utilizare a intrării în timp

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_


Grila **Intrare de timp săptămânală** este un control particularizat care are două secțiuni principale, **Dimensiuni** și **Durată**.

## <a name="dimensions"></a>Dimensiuni
Secțiunea **Dimensiuni** afișează dimensiunile la care se poate introduce timpul. Următoarele dimensiuni sunt acceptate predefinit:

  - Project
  - Activitate de proiect
  - Rol
  - Tip
  - Stare intrare

Secțiunea **Dimensiuni** nu permite editarea în linie. Această secțiune este susținută de o vizualizare care permite adăugarea de câmpuri particularizate la grila de introducere săptămânală a timpului.

## <a name="duration"></a>Durată
Secțiunea Durată afișează zilele săptămânii ca anteturi de coloană. Această secțiune permite editarea în linie. După ce se creează un rând de introducere de timp cu dimensiuni corespunzătoare, utilizatorii pot introduce rapid intervalul de timp pe care l-au petrecut pe aceste dimensiuni.

## <a name="create-a-new-time-entry"></a>Creați o înregistrare nouă de timp

1. În grila de intrare de timp, selectați **Nou**. 
2. În caseta de dialog **Crearea rapidă a intrării de timp**, selectați data introducerii orei.
3. Introduceți date pentru dimensiunile **Proiect**, **Activitatea de proiect**, **Rol** și dimensiunile **Durată**. Aceste informații trebuie adăugate în câteva minute, ore sau zile, tastând **h**, **m**, sau **d**, împreună cu numărul. 
4. Introduceți o descriere pentru intrare și orice comentarii care pot fi partajate extern referitor la intrarea de timp. 

Când salvați intrarea, valorile introduse apar în secțiunea **Dimensiuni**. Informațiile introduse în câmpul **Durată** apare pe data pentru care a fost creată intrarea de timp.

Câmpurile de căutare sunt susținute de vizualizări de sistem. De exemplu, după ce un utilizator intră într-o **Activitate proiect,** câmpul este setat la vizualizarea **Copiere** în mod implicit. Pentru a crea înregistrări de timp pentru activități care nu sunt atribuite unui utilizator, selectați **Schimbare vizualizare** în caseta de dialog căutare, apoi selectați vizualizarea **Toate sarcinile de proiect active**.

## <a name="edit-a-time-entry"></a>Editați o înregistrare de timp 
Detaliile din unele câmpuri din pagina de introducere de timp, precum **Descriere** și **Comentarii externe**, nu sunt afișate în grila de introducere săptămânală a timpului. În schimb, apare un mic indicator triunghiular în celulele **Durată** care au aceste detalii suplimentare. 

1. Pentru a edita o intrare de timp, selectați celula pe care doriți să o actualizați în intrarea de timp.
2. Selectați **Editați detaliile** pentru a actualiza datele din panoul **Formular principal de intrare în timp**. 

## <a name="copy-a-time-entry-row"></a>Copierea unei înregistrări de timp
După ce a fost creat rândul, puteți selecta **Copiere rând** pentru a copia întregul rând pe un rând nou. Atunci când un rând este copiat în acest fel, dimensiunile și duratele sunt, de asemenea, copiate. Puteți selecta, de asemenea, **Editare rând** pentru a actualiza valorile de dimensiune și duratele în secțiunea **Durată**.

## <a name="open-a-time-entry-behavior"></a>Deschideți un comportament de intrare de timp
Pentru a sprijini introducerea rapidă și rapidă în cele mai proeminente câmpuri, grila săptămânală de introducere a timpului afișează un subset de dimensiuni și durate de timp selectate. Pentru a vizualiza toate detaliile unei singure introduceri de timp, sub **Editare intrare**, selectați **Deschidere**.

## <a name="submit-a-time-entry"></a>Remiteți o înregistrare de timp
Puteți remite o singură înregistrare de timp sau un grup de înregistrări de timp selectând un bloc de celule sau un rând întreg de introducere de timp, apoi selectând **Remitere**. Înregistrările de timp remise apar ca înregistrări în curs de aprobare pe pagina **Aprobare** a aprobatorilor. După ce înregistrările de timp sunt remise cu succes, ele nu pot fi editate.

## <a name="recall-a-time-entry"></a>Retrageți o înregistrare de timp
Puteți retrage înregistrările de timp pe care le-ați remis. Puteți retrage o singură înregistrare, un bloc de înregistrări de timp sau un întreg rând de înregistrări de timp. Intrările de timp amintite pot fi editate.

## <a name="time-entry-status"></a>Stare înregistrare timp

- **Schiță**: intrărilor de timp noi le sunt atribuite automat o stare de **Schiță**. Numai înregistrările de timp cu starea **Proiect** pot fi șterse.
- **Trimis**: Când este trimisă o intrare de timp, starea este actualizată la **Trimisă**. 
- **Aprobat**: Când o înregistrare de timp depusă este aprobată, starea este actualizată la **Aprobat**. 
- **Returnat**: Dacă o înregistrare de timp este respinsă, starea este actualizată la **Returnat**, iar înregistrarea devine disponibilă pentru corectare și retransmitere. 

## <a name="view-rejection-comments"></a>Vizualizați comentarii de respingere
Atunci când o înregistrare de timp este respinsă de un aprobator, aprobatorul poate adăuga comentarii pentru a ajuta resursa să înțeleagă motivul respingerii. Pentru a vizualiza comentariile de respingere pentru o înregistrare de timp, selectați **Deschidere înregistrare**. Comentariile de respingere vor fi afișate în cronologie. Utilizatorul poate răspunde la comentariile de respingere înainte de a retrimite intrarea.

## <a name="copy-week"></a>Copiați săptămâna
După ce au fost create câteva intrări de timp, utilizatorii pot crea mai multe intrări de timp în același timp.

1. În formularul **Intrări de timp**, selectați **Copiați săptămâna** pentru a crea în bloc intrări de timp suplimentare. 
2. În caseta de dialog **Copiere**, în secțiunea **Perioada de la**, utilizați câmpurile **Dată de început** și **Dată de sfârșit** pentru a defini intervalul de date din care să copiați intrările de timp. 
3. În secțiunea **La perioadă**, în câmpul **Data de început**, specificați data pentru care să creați înregistrări de timp. 
4. Selectați **Copiați**. Pentru data specificată în **Perioada la** se creează o copie a înregistrărilor de timp pentru ziua corespunzătoare a săptămânii în **Perioada de la**. De exemplu, înregistrarea de timp pentru luni de săptămâna trecută este copiată pentru lunea săptămânii indicate drept **Perioada la**.

## <a name="import"></a>Import
Același proces de bază este utilizat pentru importul din rezervări, misiuni și schimburi. Aveți posibilitatea să specificați intervalul de date din care sunt importate rezervările și apoi selectați în mod explicit rezervări care ar trebui copiate în intrări de timp schiță. 
