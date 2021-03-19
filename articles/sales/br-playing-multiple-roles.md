---
title: Estimează vânzările și costurile proiectului atunci când o resursă care poate fi rezervată îndeplinește mai multe roluri într-un proiect
description: Acest subiect explică modul de utilizare a dimensiunilor de stabilire a prețurilor pentru a sprijini estimarea prețurilor și a costurilor pentru o resursă care îndeplinește mai multe roluri într-un proiect.
author: rumant
manager: tfehr
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f01c9c6adfeedc11fcb04a7e8b8f5a55e5f8dc79
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278838"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-multiple-roles-on-a-project"></a>Estimează vânzările și costurile proiectului atunci când o resursă care poate fi rezervată îndeplinește mai multe roluri într-un proiect 

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/non-stoc, implementare simplificată - facturare de la ofertă la proforma, Project Operations pentru scenarii stocate/bazate pe producție_ 

Companiile bazate pe proiecte au deseori nevoia unei resurse pentru a îndeplini mai multe roluri într-un proiect. Fiecare rol poate fi măsurat și calculat diferit. Aceasta înseamnă că timpul aceleiași resurse pentru un proiect ar putea obține o estimare financiară diferită în funcție de factură și de ratele de cost pentru fiecare rol. Puteți configura valorile din înregistrarea membrilor echipei pentru resursa numită cu diferite suprascrieri pentru fiecare dintre sarcinile la care este atribuit membrul echipei.

Următorul exemplu vă prezintă modul în care simpla suprascriere a unei valori permite unei resurse să aibă mai multe roluri într-un proiect cu costuri și rate de facturare diferite.

## <a name="create-tasks"></a>Crearea de activități
Pentru a crea sarcini, trebuie să adăugați sarcini, precum și sarcini sumare, după care trebuie să atribuiți sarcina înainte de a adăuga durata sarcinii. 

### <a name="add-tasks-and-summary-tasks"></a>Adăugați sarcini și activități rezumative
Pentru a adăuga o activitate, efectuați următorii pași.

1. Accesați **Proiecte** și deschideți proiectul la care doriți să adăugați activități.
2. Selectați **Adăugare activitate nouă**. Denumiți activitatea, apoi apăsați **Introduceți**.
3. Denumiți alt nume de activitate, apoi apăsați **Introduceți**. Repetați acest lucru până când aveți o listă completă de activități.
3. Pentru a indenta activitățile sub activitățile **Rezumat**, selectați cele trei puncte verticale după numele sarcinii, apoi selectați **Realizați activitate secundară**. 

  > [!TIP]
  > Pentru a selecta mai multe activități, selectați o activități, țineți apăsat **Ctrl**, apoi selectați o altă activitate.
  >
  > De asemenea, puteți alege **Promovați subactivitate** pentru a muta activitățile de sub activitățile **Rezumat**.

### <a name="assign-tasks"></a>Atribuiți activități

Finalizați următorii pași pentru a atribui activități.

1. În coloana  **Atribuit**  pentru o activtate, selectați pictograma persoană.
2. Alegeți un membru al echipei din listă sau introduceți text pentru a căuta un nume.

### <a name="add-task-duration-and-columns"></a>Adăugați durata activității și coloane

Este adesea cel mai ușor să începeți construirea proiectului cu durata. Parcurgeți următorii pași pentru a adăuga o durată de activitate.

1. În coloana **Durată** pentru o activitate, tastați numărul de zile în care credeți că va dura pentru a realiza activitatea. Dacă doriți să utilizați o unitate de timp diferită, introduceți un număr plus cuvântul **ore**, **săptămâni**, sau **luni**.
2. Dacă doriți ca activitatea dvs. să apară ca un jalon în formă de diamant în vizualizarea **Cronologie**, în coloana **Durată**, introduceți **0 zile**.
3. Apăsați **Introduceți**  pentru a accesa câmpul **Durată** a următoarei activități și continuați să introduceți durate.

  > [!NOTE]
  > Nu puteți introduce o durată pentru activități rezumative.

Puteți adăuga coloane la proiect pentru a oferi mai multe detalii. Pentru a face acest lucru, selectați **Adăugați coloană**. 

Pentru mai multe informații, consultați [Creați un proiect](https://support.microsoft.com/en-us/office/create-a-project-a5b5e823-fb2e-45fd-be00-7d84422d9749).

## <a name="set-up-the-role-and-organization-unit-for-a-generic-project-team-member"></a>Configurați rolul și unitatea de organizare pentru un membru generic al echipei de proiect
Parcurgeți pașii următori pentru a configura un rol și o unitate organizațională pentru un membru generic al echipei.

1. Pe pagina **Activități**, selectați rândul **Activități** pentru **Activitatea A**. 
2. În **Atribuit**, selectați **Adăugați o resursă generică**. Aceasta deschide pagina **Creare rapidă a membrilor echipei**.
3. Pe pagina **Creare rapidă a membrilor echipei**, specificați atributele membrilor echipei generice care pot îndeplini această activitate.
4. Selectați rolul și unitatea organizațională corespunzătoare, apoi selectați **Salvați și închideți**. Un membru generic al echipei este creat și atribuit acestei activități. 
5. Repetați pașii 1-4 pentru **Activitatea B**. În orice caz, **Activitatea B** trebuie să aibă un rol și o unitate organizațională diferită atribuite membrilor echipei generice decât **Activitatea A**. 

## <a name="set-up-the-role-and-organization-unit-for-a-project-task"></a>Configurați rolul și unitatea de organizare pentru o activitate de proiect
Parcurgeți pașii următori pentru a configura un rol și o unitate organizațională pentru o activitate.

1. După ce creați **Activitatea A**, selectați activitatea, apoi selectați pictograma **i** pentru a deschide panoul **Detalii despre activitate**. 
2. Pe panoul **Detalii despre activitate**, derulați până jos și selectați **Vizualizați detalii** pentru a deschide pagina **Detalii despre activitate**.
3. Pe pagina **Detalii despre activitate**, în **Rol** și **Unitate organizațională**, adăugați valorile necesare pentru realizarea acestei activități pentru resursă. 

  > [!NOTE]
  > Dacă finalizați acest scenariu folosind datele demo Project Operations, selectați **Conducător consultant** pentru rol și **Fabrikam SUA** ca unitate organizatorică.

4. Selectați **Activitatea B** și apoi selectați activitatea.
5. Selectați pictograma **i** pentru a deschide panoul **Detalii despre activitate**. 
6. Pe panoul **Detalii despre activitate**, derulați până jos și selectați **Vizualizare detalii** pentru a deschide pagina **Detalii despre activitate**.
7. Pe pagina **Detalii despre activitate**, în **Rol** și **Unitate organizațională**, adăugați valorile necesare pentru o resursă care ar realiza această activitate. Valorile din **Rol** și **Unitate organizațională** pentru **Activitatea B** trebuie să fie diferite de cele pentru **Activitatea A**. 

  > [!NOTE]
  > Dacă finalizați acest scenariu folosind datele demo Project Operations, selectați **Tehnician de rețea** pentru rol și **Fabrikam SUA** ca unitate organizatorică.

8. Salvați și închideți pagina **Detalii activitate**. 

## <a name="team-member-and-estimates-behavior"></a>Membru al echipei și estimează comportamentul 
Pentru a înțelege comportamentul pe grila **Membru al echipei** și estimările, parcurgeți pașii următori.

1. Pe grila **Membru al echipei**, selectați cei doi membri generici ai echipei, apoi selectați **Generați cerințe**. Aceasta va genera cerințele de resurse. 
2. Selectați rândul membrului echipei pentru **Lider consultant** și apoi selectați **Rezervare**. Tabloul de planificare se deschide cu o listă de resurse. Selectați o resursă și apoi selectați **Rezervare** pentru a rezerva resursa la acea cerință.
3. Selectați rândul membrului echipei pentru **Tehnician de rețea** și apoi selectați **Rezervare**. Tabloul de planificare se deschide cu o listă de resurse. Selectați aceeași resursă ca mai sus și apoi selectați **Rezervare** pentru a rezerva resursa la acea cerință.

### <a name="team-member-grid"></a>Grila membrilor echipei 

Pe grila **Membru al echipei**, cele două înregistrări generice ale membrilor echipei sunt șterse și înlocuite cu o singură resursă. Există un set de valori pentru resursa respectivă, care reprezintă un set implicit de valori pentru **Rol** și **Unitate organizațională**.

Când extindeți rândul pentru înregistrarea respectivă a membrilor echipei, puteți vedea atribuții distincte în înregistrarea membrilor echipei pentru ambele sarcini. Fiecare rând de atribuire are valori specifice activității pentru **Rol** și **Unitate organizațională**. 

### <a name="estimates-grid"></a>Grilă estimări 

Pe grila **Estimări**, ambele atribuții pentru aceeași resursă au un preț diferit. Atribuirea pentru resursa din **Activitatea A** este evaluată cu ajutorul valorii atributului **Rol** al **Lider consultant**. Atribuirea pentru aceeași resursă din **Activitatea B** este evaluată cu ajutorul valorii atributului **Rol** pentru **Tehnician rețea**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]