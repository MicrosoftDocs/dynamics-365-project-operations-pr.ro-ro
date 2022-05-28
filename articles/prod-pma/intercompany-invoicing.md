---
title: Facturare între companii
description: Acest articol oferă informații și exemple despre facturarea între companii pentru proiecte.
author: Yowelle
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerInterCompany
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 94153
ms.assetid: 33e98da7-01c1-4369-923d-aa1c8326cb80
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a1f66af9b7e2cb0e18a5464b23216ff03b63a0a3
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 05/04/2022
ms.locfileid: "8685439"
---
# <a name="intercompany-invoicing"></a>Facturare între companii

[!include [banner](../includes/banner.md)]

Acest articol oferă informații și exemple despre facturarea între companii pentru proiecte.

Organizația dvs. ar putea avea mai multe divizii, filiale și alte entități juridice care își transferă produse și servicii reciproc pentru proiecte. Persoana juridică care furnizează serviciul sau produsul se numește *persoană juridică de creditare*, iar entitatea juridică care primește serviciul sau produsul se numește *persoana juridică care împrumută*. 

Următoarea ilustrație prezintă un scenariu tipic în care două entități juridice, SI FR (entitatea juridică care împrumută) și SI SUA (entitatea juridică care împrumută) împart resurse pentru a livra un proiect pentru clientul A. Pentru acest scenariu, SI FR este contractată pentru livrarea lucrului la clientul A. 

[![Exemplu de facturare între companii.](./media/interco.invoicing-01.jpg)](./media/interco.invoicing-01.jpg) 

Scopul este de a face controlul costurilor, recunoașterea veniturilor, impozitelor și prețul de transfer pentru tranzacțiile de proiecte inter-companii mai flexibil și mai puternic. În plus, sunt furnizate următoarele funcții:

-   Creați facturi de clienți pentru un proiect într-o entitate juridică împrumutată utilizând foile de pontaj inter-companii, cheltuielile și facturile furnizorului într-o entitate juridică de creditare.
-   Acceptă calculele impozitelor și costurile indirecte.
-   Amânați recunoașterea veniturilor într-o entitate juridică de creditare și atunci când o entitate juridică care împrumută ar trebui să recunoască costul.
-   Acumulați venituri din munca în curs (WIP) în cadrul entității juridice de creditare.
-   Setați prețuri de transfer care pot fi bazate pe diferite modele de prețuri. Iată câteva exemple:
    -   **Cantitate** - Suma pe care o introduceți în câmpul **Prețuri** este costul real pe cantitate sau unitate.
    -   **Suma taxelor** - Prețul/costul pe tranzacție plus suma taxelor pe care le introduceți în câmpul **Prețuri**.
    -   **Procentul de taxe** - Prețul de transfer este prețul/costul pe tranzacție înmulțit cu procentul de taxe pe care îl introduceți în câmpul **Prețuri**.
    -   **Procentul din prețul de vânzare** - Procentul din prețul de vânzare care este transferat persoanei juridice de creditare.
    -   **Suma sub prețul de vânzare** - Suma pe care entitatea juridică împrumutată o reține din prețurile de vânzare înainte de transferul către entitatea juridică de creditare.
    -   **Raportul de contribuție** - Numărul pe care îl introduceți în câmpul **Prețuri** este raportul de contribuție, care este exprimat ca procent din prețul de vânzare.

## <a name="example-1-set-up-parameters-for-intercompany-invoicing"></a>Exemplul 1: configurați parametrii pentru facturarea între companii
În acest exemplu, USSI este o entitate juridică care împrumută, iar resursele sale raportează timp pentru entitatea juridică care împrumută, FRSI, care deține contractul cu clientul final. Orele și cheltuielile raportate de angajații USSI pot fi incluse în factura proiectului generată de FRSI. În plus, există o a treia sursă de tranzacții care poate proveni de la entitatea juridică de creditare (USSI în acest exemplu) atunci când furnizează servicii partajate de vânzători către filiale (cum ar fi FRSI) și apoi transferă aceste costuri proiectelor din cadrul acestor filiale. Toate documentele de facturare și calculele fiscale corespunzătoare sunt completate de către Finanțe. 

Pentru acest exemplu, FRSI trebuie să fie un client al entității juridice USSI și USSI trebuie să fie un furnizor al entității juridice FRSI. Apoi puteți configura o relație între companii între cele două persoane juridice. Următoarea procedură arată cum să configurați parametrii, astfel încât ambele persoane juridice să poată participa la facturarea între companii.

1. Configurați FRSI ca un client în entitatea juridică USSI și configurați USSI ca furnizor în entitatea juridică FRSI. Există trei puncte de intrare pentru pașii necesari pentru această sarcină.

   | Pas |                                                       Punct de intrare                                                        |                                                                                                                                                                                               Descriere                                                                                                                                                                                               |
   |------|--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |  A   | În USSI, faceți clic pe <strong>Conturi clienți</strong> &gt; <strong>Clienți</strong> &gt; <strong>Toți clienții</strong>. |                                                                                                                                                                  Creați o nouă înregistrare de client pentru FRSI și selectați grupul de clienți.                                                                                                                                                                  |
   |  A   |    În FRSI, faceți clic pe <strong>Conturi furnizori</strong> &gt; <strong>Furnizori</strong> &gt; <strong>Toți furnizorii</strong>.     |                                                                                                                                                                    Creați o nouă înregistrare de furnizor pentru USSI și selectați grupul de furnizori.                                                                                                                                                                    |
   |  C   |                                  În FRSI, deschideți înregistrarea furnizorului pe care tocmai l-ați creat.                                  | În panoul de acțiuni, în fila <strong>General</strong>, în grupul <strong>Configurați</strong>, faceți clic pe <strong>Între companii</strong>. Pe pagina <strong>Între companii</strong>, pe fila <strong>Relația comercială</strong>, setați glisorul <strong>Activ</strong> la <strong>Da</strong>. În câmpul <strong>Compania clientului</strong>, selectați înregistrarea clientului pe care ați creat-o la pasul A. |


2. Clic **Management de proiect și contabilitate** &gt; **Configurare** &gt; **Parametrii contabili ai managementului de proiect**, apoi faceți clic pe fila **Între companii**. Modul în care configurați parametrii depinde dacă sunteți persoana juridică împrumutată sau persoana juridică care împrumută.
   -   Dacă sunteți persoana juridică împrumutată, selectați categoria de achiziții care ar trebui utilizată pentru a se potrivi cu facturile furnizorului, care sunt generate automat.
   -   Dacă sunteți entitatea juridică care împrumută, pentru fiecare entitate împrumutată, selectați o categorie implicită de proiect pentru fiecare tip de tranzacție. Categoriile de proiecte sunt utilizate pentru configurarea impozitului atunci când categoria facturată în tranzacțiile între companii există doar la entitatea juridică împrumutată. Puteți alege să acumulați venituri pentru tranzacții între companii. Această acumulare se face atunci când sunt înregistrate tranzacțiile și este apoi inversată atunci când este înregistrată factura intercompaniilor.

3. Faceți clic pe **Management de proiect și contabilitate** &gt; **Configurare** &gt; **Prețuri** &gt; **Prețul de transfer**.
4. Selectați o monedă, un tip de tranzacție și un model de preț de transfer. Moneda utilizată pe factură este moneda care este configurată în evidența clientului pentru entitatea juridică împrumutată în entitatea juridică care împrumută. Moneda este utilizată pentru a se potrivi cu intrările din tabelul prețurilor de transfer.
5. Clic **Registrul general** &gt; **Configurare publicare** &gt; **Contabilitate între companii** și stabiliți o relație pentru USSI și FRSI.

## <a name="example-2-create-and-post-an-intercompany-timesheet"></a>Exemplul 2: creați și postați o foaie de pontaj între companii
USSI, entitatea juridică care împrumută, trebuie să creeze și să posteze foaia de pontaj pentru un proiect de la FRSI, entitatea juridică împrumutată. Există două puncte de intrare pentru pașii necesari pentru această sarcină.

| Pas | Punct de intrare                                                                       | Descriere                                                                                                                                                                                       |
|------|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Management de proiect și contabilitate** &gt; **Foi de pontaj** &gt; **Toate foile de pontaj** | Crearea unei noi foi de pontaj. Pe linia foii de pontaj, în câmpul **Entitate legală**, selectați **FRSI**. În **ID-ul proiectului**, selectați proiectul în FRSI. Introduceți orele pentru fiecare zi a săptămânii. |
| A    | Pagina **Foaia de pontaj**                                                                | După executarea fluxului de lucru, postați foaia de pontaj și notați numărul voucherului.                                                                                                               |

## <a name="example-3-create-and-post-an-intercompany-vendor-invoice"></a>Exemplul 3: creați și postați factura furnizorului între companii
USSI, entitatea juridică care împrumută, trebuie să creeze și să posteze factura furnizorului între companii pentru un proiect de la FRSI, entitatea juridică împrumutată. Această factură a furnizorului reprezintă forța de muncă și cheltuielile externalizate care au fost efectuate de furnizorii care sunt plătiți de USSI. Există două puncte de intrare pentru pașii necesari pentru această sarcină.

| Pas | Punct de intrare                                                                                      | Descriere                                                                                                                                                                                                                                                                          |
|------|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Conturi furnizori** &gt; **Facturi** &gt; **Deschideți facturile furnizorului** &gt; **Nouă factură de la furnizor** | Creați o nouă factură de furnizor și introduceți serviciile achiziționate în numele proiectului FRSI.                                                                                                                                                                                  |
| A    | Pagina **Factura furnizorului**                                                                      | Introduceți linii care reprezintă serviciile externalizate în numele FRSI. Pe fila rapidă **Detalii despre linie**, pe fila **Proiect** pentru linia de facturare, în câmpul **Companie de proiect**, introduceți **FRSI**. Introduceți proiectul și informațiile corespunzătoare. Apoi publicați factura furnizorului. |

## <a name="example-4-create-and-post-the-intercompany-invoice"></a>Exemplul 4: creați și postați factura între companii
USSI, entitatea juridică de creditare, trebuie să creeze și să înregistreze factura intercompaniilor. Există două puncte de intrare pentru pașii necesari pentru această sarcină.

| Pas | Punct de intrare                                                                                             | Descriere                                                                                                                                      |
|------|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Management de proiect și contabilitate** &gt; **Facturi de proiect** &gt; **Factura clientului între companii**  | faceți clic pe **Nou** pentru a deschide pagina **Creați factură între companii**.                                                                                  |
| A    | **Management de proiect și contabilitate** &gt; **Facturi de proiect** &gt; **Facturile clientului între companii** | Pe pagina **Creați factură între companii**, introduceți entitatea juridică, specificați tranzacția care ar trebui inclusă, apoi faceți clic pe **Căutare**. |
| C    | **Management de proiect și contabilitate** &gt; **Facturi de proiect** &gt; **Facturile clientului între companii** | Selectați tranzacțiile de facturat sau faceți clic pe **Selectați tot** pentru a factura toate tranzacțiile din listă, apoi faceți clic pe **OK**.                  |
| D    | Pagina **Factura între companii**                                                                       | Se afișează propunerea de facturare pentru clienți între companii.                                                                                             |
| E    | Pagina **Factura între companii**                                                                       | Faceți clic pe **Postați**.                                                                                                                                  |

## <a name="example-5-post-the-vendor-invoice-and-invoice-the-customer"></a>Exemplul 5: Înregistrați factura furnizorului și facturați clientul
Atunci când entitatea juridică de creditare, USSI, înregistrează factura clientului între companii, se creează o factură de vânzător în așteptare potrivită în entitatea juridică împrumutată, FRSI. După ce această factură de furnizor este postată, FRSI facturează, de asemenea, clientului proiectului pentru orele pe care le-a introdus USSI. Există trei puncte de intrare pentru pașii necesari pentru această sarcină.

| Pas | Punct de intrare                                                                                        | Descriere                                                                                                             |
|------|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| A    | **Conturi furnizori** &gt; **Facturi** &gt; **Facturile furnizorului în așteptare**                            | Examinați factura pentru a verifica dacă sunt incluse valorile foii de pontaj, apoi înregistrați factura furnizorului.                  |
| A    | **Management de proiect și contabilitate** &gt; **Facturi de proiect** &gt; **Propuneri de facturi de proiect** | Creați o nouă factură de proiect pentru proiect și verificați dacă apar tranzacțiile orare care au fost înregistrate.            |
| C    | Pagina **Factura proiectului**                                                                       | Selectați factura proiectului, apoi faceți clic pe **Vizualizați detaliile** pentru a revizui costul și suma vânzărilor. Apoi publicați factura. |


Pentru mai multe informații, consultați [Configurați facturarea proiectelor între companii](tasks/configure-intercompany-project-invoicing.md).




[!INCLUDE[footer-include](../includes/footer-banner.md)]