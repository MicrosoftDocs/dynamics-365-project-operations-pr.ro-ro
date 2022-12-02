---
title: Jurnalul de integrare în Project Operations
description: Acest articol oferă informații despre lucrul cu jurnalul de integrare în Project Operations.
author: sigitac
ms.date: 09/22/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: e947fe895a1caa9c9ea092597957a859cd8d61c9
ms.sourcegitcommit: b1c26ea57be721c5b0b1a33f2de0380ad102648f
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 09/20/2022
ms.locfileid: "9541093"
---
# <a name="integration-journal-in-project-operations"></a>Jurnalul de integrare în Project Operations

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

Intrările de timp, cheltuieli, taxe și materiale creează tranzacții **Reale** care reprezintă vizualizarea operațională a lucrului realizat într-un proiect. Dynamics 365 Project Operations oferă contabililor un instrument pentru a revizui tranzacțiile și a ajusta atributele contabile după cum este necesar. După finalizarea revizuirii și ajustărilor, tranzacțiile sunt înregistrate în contabilitatea proiectului și registrul general. Un contabil poate efectua aceste activități folosind jurnalul **Integrare Project Operations** (jurnalul **Dynamics 365 Finance** > **Management de proiect și contabilitate** > **Jurnale** > **Integrare Project Operations**.

![Fluxul jurnalului de integrare.](./media/IntegrationJournal.png)

### <a name="create-records-in-the-project-operations-integration-journal"></a>Creați înregistrări în jurnalul Project Operations de integrare

Înregistrările din jurnalul de integrare a Project Operations sunt create utilizând un proces periodic, **Importați din tabelul de etapizare**. Puteți rula acest proces accesând **Dynamics 365 Finance** > **Management de proiect și contabilitate** > **Periodic** > **Integrare Project Operations** > **Importare din tabelul de etapizare**. Puteți rula procesul interactiv sau configura procesul pentru a rula în fundal, după cum este necesar.

Când rulează procesul periodic, sunt găsite toate datele care nu sunt încă adăugate în jurnalul de integrare a Project Operations. Se creează o linie jurnal pentru fiecare tranzacție reală.
Sistemul grupează liniile jurnalului în jurnale separate pe baza valorii selectate în câmpul **Unitate periodică în jurnalul de integrare a Project Operations** (fila **Finanțe** > **Management de proiect și contabilitate** > **Configurare** > **Management de proiect și parametri contabili**, **Project Operations în Dynamics 365 Customer Engagement**). Valorile posibile pentru acest câmp includ:

  - **Zile**: datele reale sunt grupate după data tranzacției. Se creează un jurnal separat pentru fiecare zi.
  - **Luni**: datele reale sunt grupate după luna calendaristică. Se creează un jurnal separat pentru fiecare lună.
  - **Ani**: datele reale sunt grupate după anul calendaristic. Se creează un jurnal separat pentru fiecare an.
  - **Toate**: Toate tranzacțiile efective sunt incluse în același jurnal de integrare. Dacă jurnalul nu este disponibil când rulează procesul periodic, de exemplu dacă jurnalul este în proces de înregistrare a tranzacțiilor, se creează un jurnal nou.

Liniile de jurnalul sunt create pe baza realității proiectului. Următoarea listă include unele dintre cele mai notabile reguli implicite și de transformare:

  - Fiecare tranzacție reală a proiectului are o linie în jurnalul de integrare a Project Operations. Costul și tranzacțiile de vânzare nefacturate pentru timpul și tipul de facturare materială sunt afișate pe linii separate.
  - Câmpul **Date** reprezintă data tranzacției. Câmpul **Data de contabilitate** reprezintă data la care tranzacția este înregistrată în registru. Dacă data contabilă se află într-o [perioadă financiară închisă](/dynamics365/finance/general-ledger/close-general-ledger-at-period-end) și parametrul **Setați automat data contabilă pentru a deschide perioada contabilă** este setat pe fila **Financiar** din pagina **Managementul proiectului și parametrii contabili**, sistemul va ajusta data contabilă a tranzacției la prima dată în următoarea perioadă de registru deschis.
  - Câmpul **Voucher** afișează numărul voucherului pentru fiecare tranzacție reală. Secvența numerelor de voucher este definită pe fila **Secvențe numerice**, pe pagina **Managementul proiectului și parametrii contabili**. Fiecărei linii i se atribuie un număr nou. După afișarea voucherului, puteți vedea modul în care sunt legate costurile și tranzacțiile de vânzare nefacturate selectând **Vouchere corelate** pe pagina **Tranzacție voucher**.
  - Câmpul **Categorie** reprezintă o tranzacție a proiectului și valorile implicite se bazează pe categoria de tranzacții pentru proiectul real.
    - Dacă **Categoria tranzacției** este setat în Proiectul real și un **Categoria proiectului** corelat există într-o anumită entitate juridică, categoria este implicită la această categorie de proiect.
    - Dacă **Categoria de tranzacție** nu este setată în proiectul real, sistemul folosește valoarea în câmpul **Categorii de proiecte implicite** pe fila **Project Operations în Dynamics 365 Customer Engagement** de pe pagina **Management de proiect și parametri contabili**.
  - Câmpul **Resursă** reprezintă resursa proiectului legată de această tranzacție. Resursa este utilizată ca referință în propunerile de facturare ale proiectului către clienți.
  - Câmpul **Curs de schimb valutar** este preluat implicit din **Rată de schimb valutar** configurat în Dynamics 365 Finance Dacă setarea ratei de schimb lipsește, procesul periodic **Import din etapă** nu va adăuga înregistrarea într-un jurnal și un mesaj de eroare va fi adăugat în jurnalul de execuție a lucrării.
  - Câmpul **Proprietate de linie** reprezintă tipul de facturare în realitatea proiectului. Proprietatea de linie și maparea tipului de facturare sunt definite pe fila **Project Operations în Dynamics 365 Customer Engagement** de pe pagina **Management de proiect și parametri contabili**.

Numai următoarele atribute contabile pot fi actualizate în liniile jurnalului de integrare a Project Operations:

- **Grup de impozitare pe vânzare** și **Grup de impozitare pe vânzare articol de facturare**
- **Dimensiuni financiare** (folosind acțiunea **Distribuiți sume**)

Liniile jurnalului de integrare pot fi șterse. Cu toate acestea, toate liniile nepublicate vor fi inserate din nou în jurnal după ce ați relansat procesul periodic **Import din etapă**.

### <a name="post-the-project-operations-integration-journal"></a>Publicarea Jurnalului de integrare Project Operations

Când postați jurnalul de integrare, se creează o tranzacție de contabilitate de proiect și contabilitate generală. Acestea sunt utilizate în facturarea clienților din aval, recunoașterea veniturilor și raportarea financiară.

Jurnalul de integrare Project Operations selectat poate fi publicat utilizând **Publicare** pe pagina jurnalului de integrare Project Operations. Toate jurnalele pot fi publicate automat prin rularea unui proces la **Periodice** > **Integrare Project Operations** > **Publicare jurnal de integrare Project Operations**.

Publicarea poate fi efectuată interactiv sau în lot. Rețineți că toate jurnalele care au mai mult de 100 de rânduri vor fi publicate automat într-un lot. Pentru o performanță mai bună atunci când jurnalele care au multe linii sunt postate într-un lot, activați funcția **Publicare jurnal de integrare Project Operations folosind mai multe sarcini de lot** în spațiul de lucru **Gestionare caracteristici**. 

#### <a name="transfer-all-lines-that-have-posting-errors-to-a-new-journal"></a>Transferarea tuturor liniilor care au erori de înregistrare într-un nou jurnal

> [!NOTE]
> Pentru a utiliza această capacitate, activați funcția **Transferarea tuturor liniilor cu erori de postare într-un nou jurnal de integrare Project Operations** înspațiul de lucru **Gestionare caracteristici**.

Această funcție ajută la îmbunătățirea experienței cu jurnalul de integrare Project Operations. Când este activat, problemele de sincronizare cu scriere duală și problemele de configurare nu mai împiedică publicarea jurnalelor valide. În timpul publicării în jurnalul de integrare Project Operations, sistemul validează fiecare linie din jurnal. Publică toate liniile care nu au erori și creează un nou jurnal pentru toate liniile care au erori de publicate.

Pentru a examina jurnalele care au linii de eroare de publicare, accesați **Management de proiect si contabilitate** \> **Jurnale** \> **Jurnal de integrare Project Operations** și filtrați lista de jurnale utilizând câmpul **Jurnal inițial**. Următoarea ilustrație arată un exemplu în care jurnalele de pe pagina **Jurnal de integrare Project Operations** au fost filtrate în acest fel.

![Jurnalul inițial afișat pe pagina jurnalului de integrare Project Operations.](./media/transferLines-originalJournal.png)

Dacă o operațiune în bloc este configurată pentru a publica jurnalul de integrare, se va reîncerca publicarea, iar jurnalele vor fi publicate dacă problema de sincronizare a fost remediată. Toate jurnalele rămase trebuie investigate manual, examinând jurnalele și luând orice acțiune necesară.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
