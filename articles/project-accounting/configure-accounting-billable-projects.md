---
title: Configurați contabilitatea pentru proiectele facturabile
description: Acest subiect furnizează informații despre opțiunile contabile pentru proiectele facturabile.
author: sigitac
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1159a31ba4f30f09734bf9c5a9e594b5c77a831e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8596479"
---
# <a name="configure-accounting-for-billable-projects"></a>Configurați contabilitatea pentru proiectele facturabile

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Dynamics 365 Project Operations acceptă diverse opțiuni contabile pentru proiectele facturabile care includ tranzacții de timp și materiale și cu preț fix.

- **Timp și tranzacții materiale**: Aceste tranzacții sunt facturate pe măsură ce lucrările progresează pe baza consumului de ore, cheltuieli, articole sau taxe din proiect. Aceste costuri de tranzacție pot fi corelate cu veniturile din fiecare tranzacție, iar proiectul este facturat pe măsură ce lucrările progresează. Veniturile proiectului se pot acumula și în momentul în care are loc tranzacția. În timpul facturării, veniturile sunt recunoscute și, dacă este cazul, veniturile acumulate sunt inversate.
- **Tranzacții cu preț fix**: aceste tranzacții sunt facturate conform unui program de facturare care se bazează pe contractul de proiect. Veniturile pentru tranzacțiile cu preț fix pot fi recunoscute la facturare sau calculate și înregistrate periodic, conform metodelor **Contract finalizat** sau **Procent finalizat**.

Un proiect este considerat facturabil atunci când este asociat cu una sau mai multe linii de contract. O linie de contract de proiect definește singură ce metodă de facturare și tipuri de tranzacții sunt permise.

De exemplu, Fabrikam Robotics a câștigat un contract de proiect cu corporația Adatum pentru optimizarea echipamentelor. Adatum va plăti o sumă fixă de 10.000 USD pentru a acoperi cheltuielile suportate pentru proiect. Acesta este o metodă de facturare cu preț fix. Timpul și taxele proiectului vor fi facturate pe utilizare. Aceasta este o metodă de facturare pentru timp și materiale. Toate lucrările vor fi urmărite în cadrul unui singur proiect numit, optimizarea echipamentelor Adatum.

Un membru al echipei de proiect transmite opt ore de lucru la proiectul de optimizare a echipamentelor Adatum. Când managerul de proiect aprobă această dată, sistemul utilizează metoda de facturare a timpului și materialului pentru a crea tranzacții reale, o factură și un cont. Această tranzacție nu va fi inclusă în calculul estimării veniturilor cu preț fix.

Un alt membru al echipei de proiect înaintează o cheltuială de călătorie pentru $2000,00 USD în raport cu proiectul de optimizare a echipamentelor Adatum. Când managerul de proiect aprobă această interogare, sistemul utilizează metoda de facturare cu preț fix pentru a crea tranzacții reale, o factură și un cont pentru această cheltuială de proiect. Clientul nu va fi facturat pe baza acestei tranzacții. În schimb, acestea vor fi facturate utilizând repere de facturare configurate separat. Această tranzacție de cheltuială, împreună cu estimările de cheltuială, va fi inclusă în calculul estimării veniturilor cu preț fix.

Principiile contabile pentru tranzacțiile proiectului sunt definite în profilurile de cost și venituri ale proiectului. Pentru fiecare tranzacție a proiectului, sistemul determină costul proiectului și profilul de venituri adecvat utilizând regulile de profil și costul proiectului care au fost configurate.

## <a name="define-project-cost-and-revenue-profiles"></a>Definiți costul de proiect și profilele de venituri 

Costul de proiect și profilele de venituri determină regulile de contabilitate pentru tranzacțiile proiectului. Aceste profiluri sunt configurate în managementul de proiect și contabilitate. 

Parcurgeți pașii următori pentru a crea un nou profil de cost și venit al proiectului. 

1. Accesați **Management de proiect și contabilitate** > **Configurare** > **Publicare** > **Profilurile de cost și venituri ale proiectului**. 
2. Selectați **Nou** pentru a crea un nou profil al costurilor și veniturilor proiectului.
3. În câmpul **Nume**, introduceți numele și o scurtă descriere a profilului.
4. În câmpul **Metoda de facturare**, selectați **Timp și material** sau **Preț fix**.
5. Extindeți **Registrul** FastTab. Câmpurile din această filă definesc principiile contabile care sunt utilizate atunci când tranzacțiile de proiect sunt jurnalizate utilizând jurnalul de integrare a Project Operations și apoi facturate prin propunerea de facturare a proiectului.
6. Selectați informația potrivită în următoarele câmpuri ale **Registrului** FastTab:

    - **Costuri post - oră**:

       - *Fără registru*: Costul tranzacțiilor de timp nu va fi înregistrat în registrul contabil atunci când este înregistrat jurnalul de integrare a Project Operations. Cu toate acestea, contabilul poate publica costuri utilizând funcția Publicare costuri ulterior.
       - **Sold**: Costul tranzacțiilor de timp va fi debitat în tipul de cont Registru, *WIP - Valoarea costului* și creditat la *Cont de alocare a salarizării* în configurarea de publicare Registru. Contabilul va utiliza funcția Înregistrare costuri pentru a muta periodic acest cost dintr-un cont de sold într-un cont de profit și pierderi.
       - **Profit și pierdere**: La publicare jurnalului de integrare a operațiunilor de proiect, costul tranzacției în timp va fi debitat în tipul de cont Registru *Cost*, și creditat la *Cont de alocare a salarizării* definit pe fila **Cost** de pe pagina **Configurare înregistrare contabilitate** (**Management de proiect și contabilitate** \> **Configurare** \> **Publicare** \> **Configurare înregistrare contabilitate**). Aceasta este cea mai frecventă configurare pentru tranzacții de timp și materiale.
        - *Niciodată Registru*: Costul tranzacțiilor temporale nu va fi niciodată înregistrat în registrul contabil.

    - **Publicare costuri - cheltuieli**:

         - **Sold**: La postarea jurnalului de integrare a operațiunilor de proiect, costul tranzacției de cheltuieli va fi debitat în tipul de cont Registru *WIP - Valoarea costului* așa cum este definit pe fila **Cost** de pe pagina **Configurare înregistrare contabilitate** și creditat în contul offset de pe linia jurnalului. Conturile compensate implicite pentru cheltuieli sunt definite în **Management de proiect și contabilitate** > **Configurat** \> **Publicare** \> **Cont de compensare implicit pentru cheltuieli**. Contabilul va utiliza funcția **Publicare costuri** pentru a muta periodic acest cost dintr-un cont de sold într-un cont de profit și pierderi.
        - **Profit și pierdere**: La publicarea jurnalului de integrare a operațiunilor de proiect, costul tranzacției de cheltuieli va fi debitat în tipul de cont Registru *WIP - Valoarea costului* așa cum este definit pe fila **Cost** de pe pagina **Configurare înregistrare contabilitate** și creditat în contul offset de pe linia jurnalului. Conturile compensate implicite pentru cheltuieli sunt definite în **Management de proiect și contabilitate** \> **Configurare** \> **Publicare** \> **Cont de decalaj implicit pentru cheltuieli**.
      
    - **Costuri poștale - articol**:

         - **Sold**: La postarea jurnalului de integrare Project Operations, costul tranzacției articolului va fi debitat în tipul de cont Registru *WIP - Valoarea costului - articol* așa cum este definit pe fila **Cost** de pe pagina **Configurare înregistrare contabilitate** și va fi creditat la următoarele:
    
              - Pentru utilizarea tipului de document: cont **Cost - articol** pe **Configurare înregistrare contabilitate**.  
              - Pentru tipul de document achiziție: **Cont de integrare a achizițiilor** pe **Managementul proiectelor și parametrii contabili**.
           Contabilul va utiliza funcția **Publicare costuri** pentru a muta periodic acest cost dintr-un cont de sold într-un cont de profit și pierderi.
        - **Profit și pierdere**: La postarea jurnalului de integrare Project Operations, costul tranzacției articolului va fi debitat în tipul de cont Registru *Cost* așa cum este definit pe fila **Cost** de pe pagina **Configurare înregistrare contabilitate** și va fi creditat la următoarele:
         
             - Pentru utilizarea tipului de document: cont **Cost - articol** pe **Configurare înregistrare contabilitate**.  
             - Pentru tipul de document achiziție: **Cont de integrare a achizițiilor** pe **Managementul proiectelor și parametrii contabili**.
       
    - **Despre facturarea contului**:

        - **Sold**: La publicarea propunerii de facturare a proiectului, o tranzacție pe cont (etapă de facturare) va fi creditată în tipul de cont Registru *WIP facturat - pe cont* așa cum este definit pe fila **Venituri** de pe pagina **Configurare înregistrare contabilitate** și debitat în contul de sold al clienților.
         - **Profit și pierdere**: La publicarea propunerii de facturare a proiectului, o tranzacție pe cont (etapă de facturare) va fi creditată în tipul de cont Registru *Venit facturat - pe cont* așa cum este definit pe fila **Venituri** de pe pagina **Configurare înregistrare contabilitate** și debitat în contul de sold al clienților. Conturile de sold ale clienților sunt definite în **Conturi clienți** \> **Configurare** \> **Profiluri de publicare ale clienților**.

   Când definiți profilurile de postare pentru metodele de facturare pentru timp și materiale, aveți opțiunea de a acumula venituri pe tip de tranzacție (oră, cheltuială, articol și taxă). Dacă opțiunea **Venituri acumulate** este setată la **Da**, tranzacțiile de vânzare necotificate în jurnalul de integrare a operațiunilor de proiect vor fi înregistrate în registrul general. Valoarea vânzărilor este debitată către **WIP - cont de valoare pentru vânzări** și creditat în contul **Venituri acumulate - valoarea vânzărilor** care a fost creat pe pagina **Configurare înregistrare contabilitate**, pe fila **Venituri**. 
  
  > [!NOTE]
  > Optiunea, **Acumulați venituri** este disponibilă numai atunci când tipul respectiv de tranzacție **Cost** este înregistrat în contul de profit și pierdere.
    
7. Extindeți **Estimarea** FastTab. Câmpurile din această filă definesc setările de calcul pentru estimările veniturilor la prețuri fixe. Câmpurile din această filă se aplică numai profilurilor de costuri și venituri ale proiectului cu o metodă de facturare de **Preț fix**.
8. Selectați informația potrivită în următoarele câmpuri ale **Estimare** FastTab:

    - **Principiul utilizat pentru calculele de finalizare a proiectului**:

        - **Contract finalizat**: Corelarea costurilor și recunoașterea veniturilor nu au loc până la sfârșitul proiectului. Costurile se reflectă ca WIP în sold până la finalizarea proiectului.
        - **Procent finalizat**: Veniturile acumulate sunt calculate și înregistrate în registru în fiecare perioadă pe baza procentului de finalizare a proiectului. Există mai multe metode disponibile pentru a calcula procentul de finalizare. Aceste metode pot fi automate bazate pe configurare sau manual.
        - **Fără WIP**: Această configurație este utilizată pentru proiecte cu preț fix cu un interval de timp scurt și în care factura și costurile au loc în aceeași perioadă. În acest caz, valoarea câmpului **Facturare pe cont** pe **Registru** FastTab este setat automat la **Profit și pierdere** pentru a se asigura că veniturile sunt recunoscute la facturare. Procesul de estimare a veniturilor nu va fi utilizat pentru acest profil de cost și profil de venituri.

    - **Principiul de potrivire**: Acest câmp determină modul în care valoarea vânzărilor calculate (venituri acumulate) va fi înregistrată în registru.

        - Utilizând principiul **Valoarea vânzărilor**, sistemul va calcula valoarea vânzărilor prin potrivirea costurilor și veniturilor și apoi înregistrarea acesteia ca o singură sumă.
        - Utilizând principiul **Producție și profit**, sistemul va împărți valoarea vânzărilor în costuri realizate și profit calculat. Acestea sunt postate separat.

    - **Șabloane de costuri**: Permiteți gruparea tranzacțiilor de proiect pe baza tipului de tranzacție și a categoriei de proiect și definiți regulile de calcul al procentului de finalizare pentru aceste grupuri.
    - **Coduri de perioadă**: Definiți frecvența cu care sunt calculate estimările veniturilor pentru un anumit profil al proiectului de cost și venit.
    - **Categorii pentru estimare**: utilizat pentru înregistrarea valorii vânzărilor (venituri acumulate) în tranzacțiile proiectului. Mai întâi, configurați categoria de proiect dedicată pentru un tip de tranzacție **Taxă** și apoi setați steagul, **Estimare** pentru această categorie de proiect. Apoi, în funcție de principiul de potrivire selectat, alegeți această categorie de proiect în valoarea **Vânzări** sau **Profit** din profilul de cost și venituri al proiectului.

### <a name="sample-configurations-for-project-cost-and-revenue-profiles"></a>Exemple de configurații pentru profilurile de cost și venituri ale proiectului

Timp și materiale - fără WIP

![Profil de costuri și venituri: Timp și materiale - fără WIP.](media/time-material-no-wip.png)

Timp și materiale - WIP (venit)

![Profil de costuri și venituri: Timp și materiale - WIP.](media/time-material-with-wip.png)

Preț fix - fără WIP

![Profil de cost și venituri: preț fix - fără WIP.](media/fixed-price-no-wip.png)

Preț fix - contract finalizat

![Profil de cost și venituri: preț fix - contract finalizat.](media/fixed-price-completed-contract.png)

Preț fix - finalizare procentuală

![Profil de cost și venituri: preț fix - finalizare procentuală.](media/fixed-price-completed-percentage.png)


## <a name="accounting-event-examples-for-sample-project-cost-and-revenue-profiles"></a>Exemple de eveniment de contabilitate pentru pentru profilurile de eșantion de cost și venituri ale proiectului.

| Eveniment contabil                  | Timp și material - fără WIP                       | Timp și material - WIP                                                                                           | Preț fix - fără WIP                                            | Preț fix - contract finalizat                                                                            | Preț fix - procent finalizat                             |
|-----------------------------------|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| Jurnalizarea tranzacțiilor în timp    | Debit - Cost <br>Credit - Alocare salarizare          | Debit - Cost <br>Credit - Alocare stat de plată <br>Debit –WIP Valoarea vânzărilor <br>Credit - Valoarea vânzărilor veniturilor acumulate                | Debit - Cost <br>Credit - Alocare salarizare                         | Debit - Cost <br>Credit – Alocare stat de plată                                                                    | Debit - Cost <br>Credit – Alocare stat de plată                       |
| Jurnalizarea tranzacțiilor de cheltuieli | Debit - Cost <br>Credit - Cont compensat pentru cheltuieli | Debit - Cost <br>Credit - Cont compensat pentru cheltuieli <br>Debit – WIP Valoarea vânzărilor <br>Credit - Valoarea vânzărilor veniturilor acumulate      | Debit – Cost <br>Credit - Cont compensat pentru cheltuieli                 | Debit - Cost<br> Credit - Cont compensat pentru cheltuieli                                                            | Debit - Cost <br>Credit - Cont compensat pentru cheltuieli               |
| Facturarea clientului                | Debit –Sold clienți <br>Credit –Venituri facturate | Debit – Sold clienți <br>Credit – Venituri facturate <br>Credit - WIP Valoarea vânzărilor Debit - Venitul acumulat Valoarea vânzărilor | Debit – Sold clienți <br>Credit – Venituri facturate - pe cont | Debit –Sold clienți <br>Credit – WIP - Facturat pe cont                                                  | Debit – Sold clienți <br>Credit – WIP - Facturat pe cont    |
| Venit așteptat estimat             | Nu se aplică                                   | Nu se aplică                                                                                                    | Nu se aplică                                                  | Debit - Valoarea costului WIP <br>Credit – Cost                                                                         | Debit - WIP - Valoarea vânzărilor <br>Credit – Valoarea vânzărilor veniturilor acumulate |
| Eliminare                         | Nu se aplică                                   | Nu se aplică                                                                                                    | Nu se aplică                                                  | Credit - Valoarea costului WIP <br>Debit - Cost <br>Credit – Venit acumulat - Valoarea vânzărilor <br>Debit – WIP facturat pe cont | Debit – WIP – facturat pe cont <br>Credit - WIP Valoarea vânzărilor     |

## <a name="configure-project-cost-and-revenue-profile-rules"></a>Configurați costul de proiect și regulile profilului de venit

Regulile privind profilul și veniturile proiectului determină profilul și costul proiectului care trebuie utilizate la procesarea oricăror tranzacții facturabile. Definiți regulile mergând la **Management de proiect și contabilitate** \> **Configurare** \> **Publicare** \> **Costul proiectului și regulile profilului veniturilor**.

Regulile pot fi definite de contractul de proiect, grupul de proiect sau de un anumit proiect. Sistemul va alege întotdeauna cea mai mare regulă de granularitate mai întâi.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
