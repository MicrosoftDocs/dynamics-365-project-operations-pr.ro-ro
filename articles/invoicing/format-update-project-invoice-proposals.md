---
title: Gestionarea propunerilor de facturare pentru proiect
description: Acest subiect oferă o detalii despre procesarea facturilor trimise la client cu Project Operations pentru scenarii bazate pe resurse/ne-stocate.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 61b43e05eb179e2b00189076290433dd72f89a6bc7ef72140fc1efd752149d43
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/06/2021
ms.locfileid: "6989926"
---
# <a name="manage-project-invoice-proposals"></a>Gestionarea propunerilor de facturare pentru proiect

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

Propunerile de facturare pentru proiect pot fi procesate de departamentul dvs. de facturare când sunt îndeplinite următoarele două condiții:

  - Managerul de proiect confirmă factura proformă în Microsoft Dataverse.
  - Toate tranzacțiile de timp și materiale nefacturate, care sunt incluse în factura proformă, sunt înregistrate utilizând jurnalul **Integrare Project Operations** în Dynamics 365.

Utilizați pașii următori pentru a finaliza o propunere de facturare a proiectului în Dynamics 365 Finance.

1. Examinați informațiile de facturare pentru tranzacțiile de timp și materiale și postați jurnalul **Integrarea Project Operations**.
2. Examinați informațiile de facturare pentru reperele de facturare cu preț fix.
3. Analizați și formatați o propunere de facturare a proiectului.
4. Postați și imprimați facturile pentru proiect.

## <a name="manage-billing-information-in-the-project-operations-integration-journal"></a>Gestionați informațiile de facturare în jurnalul de integrare Project Operations

Valorile reale ale proiectului creat în Dataverse sunt revizuite și postate în Finanțe de către contabilul proiectului. Pentru mai multe informații despre lucrul cu jurnalul de integrare, consultați [Jurnal de integrare în Project Operations](../project-accounting/project-operations-integration-journal.md).

Valorile reale ale costurilor și valorile reale ale vânzărilor sunt adăugate în jurnalul de integrare ca linii separate:

  - Prețul costului unitar și valoarea costului pentru valoare reală implicită a costului din tranzacția costului real al proiectului în Dataverse.
  - Prețul unitar de vânzare și valoarea vânzărilor pentru tranzacțiile de vânzare nefacturate rezultă din tranzacțiile de vânzare ale proiectului nefacturate în Dataverse.

### <a name="billing-sales-tax"></a>Impozit pe vânzări la facturare

Calculul impozitului pe vânzări pentru facturare este determinat de combinația de câmpuri **Grup de impozitare pe vânzare** și **Grup de impozitare pe vânzare articol de facturare** dintr-o înregistrare de vânzări nefacturată pe linia de jurnal **Integrarea Project Operations**. Sistemul redă în mod implicit aceste valori de câmp pe baza setărilor din fila **Date financiare** de pe pagina **Managementul proiectului și parametrii contabili**.

- **Metoda grupului de impozitare pe vânzări** determină logica implicită a grupului de impozitare pe vânzări:
  
  - **Proiect**: Va rezulta întotdeauna în mod implicit grupul de impozitare pe vânzări din proiect. Puteți revizui sau modifica grupul implicit de facturare a grupului de impozite pe vânzare pentru un proiect selectând **Afișați contabilitatea implicită** pe pagina **Toate proiectele**.
  - **Contract de proiect**: Va rezulta întotdeauna în mod implicit grupul de impozitare pe vânzări facturate din contractul de proiect. Puteți revizui sau modifica grupul implicit de impozitare pe vânzare pentru un contract de proiect selectând **Afișați contabilitatea implicită** pe pagina **Contracte de proiect**.
  - **Client**: Va rezulta întotdeauna în mod implicit grupul de impozitare pe vânzări facturate din proiect de la client.
  - **Căutare** : Va căuta prin toate entitățile de mai sus și va selecta prima valoare disponibilă. Căutarea începe cu entitatea **Proiect**, apoi cu entitatea **Contract de proiect** entitate, și în cele din urmă entitatea **Client**.

- **Metoda grupului de impozitare pe vânzări de articole** determină logica implicită a grupului de impozitare pe vânzări de articole facturate:
  
  - Pentru tipurile de tranzacții de timp, cheltuială și taxă, grupul de impozitare pe vânzare facturată va rezulta întotdeauna în mod implicit din entitatea **Categoria proiectului**.
  - Pentru tipurile de tranzacții cu materiale, grupul de impozitare pe vânzări facturare pentru articol rezultă în mod implicit pe baza setării **Metoda grupului de impozitare pe vânzări de articole** din **Managementul proiectului și parametrii contabili**. Numărul articolului generează în mod implicit grupul de impozitare pe vânzări articol din entitatea **Produs lansat**. Categoria generează în mod implicit grupul de impozitare pe vânzări articol din entitatea **Categorie de proiect**.

### <a name="financial-dimensions"></a>Dimensiuni financiare

Dimensiunile financiare pentru înregistrările de vânzări nefacturate în jurnalul **Integrarea Project Operations** reiese implict din entitatea **Proiect**. Dimensiunile financiare pot fi revizuite și ajustate selectând **Distribuiți sume**. Dacă trebuie să modificați dimensiunile financiare ale înregistrării de vânzări nefacturate după publicarea jurnalului de integrare, dar înainte de confirmarea facturii Proforma, accesați **Toate proiectele** > **Administrați** > **Tranzacții înregistrate**, selectați tranzacția, apoi selectați **Procesați** > **Ajustați contabilitate**.

### <a name="exchange-rates"></a>Cursuri de schimb

Moneda de tranzacție nefacturată în Dataverse este utilizată ca monedă a tranzacției în Finanțe și convertită în moneda contabilă a companiei utilizând cursurile de schimb definite în Finanțe.


## <a name="manage-the-financial-attributes-of-billing-milestones"></a>Gestionați atributele financiare ale reperelor de facturare 

Liniile contractuale de proiect care utilizează metoda de facturare cu preț fix sunt facturate prin intermediul [Repere cu preț fix](../sales/invoice-schedules-contract-line.md#create-a-fixed-price-invoice-schedule-for-a-contract-line). Contabilul Proiectului poate revizui reperele de facturare în Finanțe accesând **Management de proiect și contabilitate** > **Toate proiectele** > **Administrați** > **Tranzacții în cont**.

### <a name="billing-sales-tax"></a>Impozit pe vânzări la facturare

Valorile **Grup de impozitare pe vânzări** și **Grup de impozitare pe vânzările articolelor**  valorile reies în mod implicit din setări când se creează un nou reper de facturare în Dataverse. Sistemul redă în mod implicit valorie acestor câmp pe baza setărilor din fila **Financiar** de pe pagina **Managementul proiectului și parametrii contabili**.

- **Metoda grupului de impozitare pe vânzări** determină logica implicită a **Grupului de impozitare pe vânzări**:

    - **Proiect**: va rezulta întotdeauna în mod implicit grupul de impozitare pe vânzări din proiect. Puteți revizui sau modifica grupul de impozitare pe vânzări nefacturate implict pentru un proiect selectând **Afișați contabilitatea implicită** pe pagina **Toate proiectele**.
    - **Contract de proiect**: va rezulta întotdeauna în mod implicit grupul de impozitare pe vânzări facturate din contractul de proiect. Puteți revizui sau modifica grupul implicit de impozitare pe vânzare pentru un contract de proiect selectând **Afișați contabilitatea implicită** pe pagina **Contracte de proiect**.
    - **Client**: Va rezulta întotdeauna în mod implicit la grupul de impozitare pe vânzări facturate din proiect de la client.
    - **Căutare** va căuta prin toate entitățile din această listă și va selecta prima valoare disponibilă. Căutarea începe cu entitatea **Proiect**, apoi cu entitatea **Contract de proiect** entitate, și apoi entitatea **Client**.

- **Grup de taxe pe vânzări de articole de referință cu preț fix** este utilizat ca valoare implicită în câmpului **Grup de taxe pe vânzări de articole** pentru etapa de facturare. Contabilul poate revizui și modifica această valoare pe pagina **Tranzacții în cont**. Sistemul folosește valoarea din tranzacția în cont atunci când creează o linie de propunere de factură de proiect.
 

### <a name="financial-dimensions"></a>Dimensiuni financiare

Dimensiunile financiare implicite pentru etapa de facturare cu preț fix sunt stabilite pe liniile contractuale ale proiectului. Mergeți la **Contracte de proiect** > **Afișați contabilitate implicită** și pe fila **Linii contractuale**, selectați **linia contractului de pret**, apoi setați valorile dimensiunii financiare pe care doriți să le utilizați ca implicite.

Contabilul proiectului poate edita informațiile privind impozitul pe vânzări și dimensiunile financiare pe etapele facturii până la crearea propunerii de factură pentru proiect.


## <a name="create-project-invoice-proposals"></a>Creați propuneri de facturare pentru proiect

Propunerile de facturare pentru proiectului pot fi revizuite în modulul **Management de proiect și contabilitate** accesând **Facturi de proiect** > **Propuneri de facturare pentru proiect**.

Antetul propunerii de facturare pentru proiect este creat în Finanțe când factura Proforma este confirmată în Dataverse. Pentru o reconciliere mai ușoară, sistemul setează numărul propunerii de facturare pentru proiect în Finanțe la același număr cu ID-ul facturii Proforma din Dataverse. Deoarece facturile proforme nu sunt neapărat confirmate în aceeași ordine în care au fost create, secvența de număr de propunere de facturare pentru proiect în Finanțe trebuie să permită modificări la numere mai mici și mai mari. Configurați secvențele de numere urmând pașii următori:

1. În Finanțe, accesați **Administrația organizației** > **Secvențe de numere** > **Secvențe de numere**.
2. La filtrul **Zonă**, selectați **Proiecte**.
3. La filtrul **Referinţă**, selectați **Propunere de facturare**.
4. Utilizați câmpul **Companie** pentru a filtra fiecare persoană juridică cu integrarea Project Operations Dataverse activată.
5. Deschideți **Detalii secvență de numere**, iar pe fila **General** setați:

    - **Permiteți modificările utilizatorului: la un număr mai mic** = **Da**
    - **Permiteți modificările utilizatorului: la un număr mai mare** = **Da**

Liniile de propunere de facturare pentru proiect sunt adăugate de sistem folosind procesul periodic **Importați din tabelul de etapizare** (**Management de proiect și contabilitate** > **Periodic** > **Integrarea Project Operations** > **Importați din tabelul de etapizare**). Acest proces poate fi rulat manual sau utilizând un program periodic. Sistemul nu va adăuga linii în documentul propunerii de facturare înainte ca toate liniile să fie gata de facturare. Tranzacțiile de timp și materiale sunt gata să fie facturate numai când sunt înregistrate folosind jurnalul **Integrarea Project Operations** jurnal.

## <a name="format-and-print-invoice-proposals"></a>Formatați și tipăriți propunerile de facturare

Contabilul proiectului poate personaliza imprimarea facturii proiectului utilizând pagina **Formatați propunerea de facturare** și capabilitățile de gestionare a tipăririi.

### <a name="format-invoice-proposals"></a>Formatați propunerile de facturare

Pagina **Formatați propunerile de facturare** permite ca tranzacțiile de grupare personalizate să fie afișate în factura proiectului către client.

1. Pe pagina **Propunere de facturare proiect**, selectați **Imprimare** > **Formatați propunerea de facturare**.
2. Selectați **Nou** pentru a crea o nouă grupare pentru imprimarea facturii proiectului.
3. În câmpul **Detaliu/Rezumat**, selectați opțiuni pentru această grupare:

    - Selectați **Detaliu** pentru a imprima detaliile tranzacției din factura către client.
    - Selectați **Rezumat** pentru a imprima un rezumat al tranzacției din factura către client.

> [!NOTE]
> Selecția din câmpul **Detaliu/Rezumat** de pe pagina **Formatați propunerea de facturare** suprascrie opțiunea selectată în câmpul **Format factură** pe pagina **Propuneri de facturare** pentru a imprima o factură detaliată sau o factură rezumativă.

- Selectați liniile de tranzacție pe care să le includeți în această secțiune de pe fila **Tranzacții disponibile** și selectați **Includeți tranzacții** pentru a le muta la fila **Tranzacții selectate**.
- Selectați **Mutați în sus** și **Mutați în jos** pentru a schimba ordinea secțiunilor.
- Selectați **Previzualizare imprimare** pentru a previzualiza factura formatată.

### <a name="print-management"></a>Gestionarea imprimării

Gestionarea imprimării utilizează diferite fișiere de rapoarte pentru a imprima, specifica destinații și a personaliza textul de subsol pentru factură. Gestionarea imprimării poate fi configurată la nivelul modulului, însă aceste setări pot fi anulate pentru un anumit client, contract sau propunere de facturare. Pentru a accesa această funcție de pe paguna **Propunere de facturare pentru proiect**, selectați **Imprimare** > **Managementul imprimării**.

Configurarea gestionării tipăririi este afișată ca o vizualizare de tip arbore, unde fiecare nivel de nod afișează documentele disponibile pentru ajustare. Puteți atribui imprimări personalizate la nivel de modul, client, contract sau propunere de facturare. Pentru a modifica imprimarea documentului original, extindeți nodul dorit și selectați **Element original**. În câmpul **Format raport**, selectați formatul raportului care va fi utilizat pentru imprimare. Puteți utiliza formate de raport personalizate utilizând [Cadrul de gestionare a documentelor de afaceri](/dynamics365/fin-ops-core/dev-itpro/analytics/er-business-document-management).

## <a name="post-invoice-proposals"></a>Înregistrați propuneri de facturare

După ce factura a fost revizuită și editată și liniile de propunere de facturare sunt satisfăcătoare, verificați totalul facturii și impozitul pe vânzări. În grupul **Detalii**, selectați **Totaluri** și apoi selectați **Înregistrare** pentru a înregistra factura.

Pentru a vizualiza factura înainte de înregistrare, debifați caseta de bifare **Înregistrare**. Textul **Proformă** va apărea imprimat pe factură pentru a se ști că este o mostră de factură. Pentru a imprima factura, marcați caseta de bifare **Imprimați factura**.

Pe lângă pagina **Propunere de factură**, propunerile de facturare pot fi înregistrate și prin executarea operațiunii periodice, **Înregistrați propuneri de facturare**. Pentru a găsi această operațiune, accesați **Management de proiect și contabilitate** > **Periodic** > **Facturi de proiect** > **Înregistrați propuneri de facturare**.

Această pagină afișează toate propunerile de facturare care sunt gata de înregistrare. Puteți programa înregistrarea propunerilor de facturare selectând **În serie**. Setați **Parametru de procesare în serie** pe **Da** și setați recurența procesării în serie selectând **Recurență**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
