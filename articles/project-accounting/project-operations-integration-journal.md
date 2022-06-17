---
title: Jurnalul de integrare în Project Operations
description: Acest articol oferă informații despre lucrul cu jurnalul de integrare în Operațiuni de proiect.
author: sigitac
ms.date: 10/27/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: befb1756ad77708805f3cbb06168b93e44296df0
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923893"
---
# <a name="integration-journal-in-project-operations"></a>Jurnalul de integrare în Project Operations

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

Intrări de timp și cheltuieli creează tranzacții **Reale** care reprezintă vizualizarea operațională a lucrului realizat într-un proiect. Dynamics 365 Project Operations oferă contabililor un instrument pentru a revizui tranzacțiile și a ajusta atributele contabile după cum este necesar. După finalizarea revizuirii și ajustărilor, tranzacțiile sunt înregistrate în contabilitatea proiectului și registrul general. Un contabil poate efectua aceste activități folosind **Integrarea operațiunilor de proiect** jurnal(**Dynamics 365 Finance** > **Management de proiect si contabilitate** > **Jurnalele** > **Integrarea operațiunilor de proiect** jurnal.

![Fluxul jurnalului de integrare.](./media/IntegrationJournal.png)

### <a name="create-records-in-the-project-operations-integration-journal"></a>Creați înregistrări în jurnalul Project Operations de integrare

Înregistrările din jurnalul de integrare a Project Operations sunt create utilizând un proces periodic, **Importați din tabelul de etapizare**. Puteți rula acest proces accesând **Dynamics 365 Finance** > **Management de proiect si contabilitate** > **Periodic** > **Integrarea operațiunilor de proiect** > **Importați din tabelul de pregătire**. Puteți rula procesul interactiv sau configura procesul pentru a rula în fundal, după cum este necesar.

Când rulează procesul periodic, sunt găsite toate datele care nu sunt încă adăugate în jurnalul de integrare a Project Operations. Se creează o linie jurnal pentru fiecare tranzacție reală.
Sistemul grupează liniile jurnalului în jurnale separate pe baza valorii selectate în **Unitate de perioadă pe jurnalul de integrare a operațiunilor de proiect** camp (**Finanţa** > **Management de proiect si contabilitate** > **Înființat** > **Management de proiect și parametri contabili**, **de proiect pe Dynamics 365 Customer Engagement** fila). Valorile posibile pentru acest câmp includ:

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
    - Dacă **Categoria tranzacției** nu este setat în proiectul actual, sistemul folosește valoarea din **Valorile implicite ale categoriei de proiect** câmp de pe **Operațiuni de proiect pe Dynamics 365 Customer Engagement** fila pe **Management de proiect și parametri contabili** pagină.
  - Câmpul **Resursă** reprezintă resursa proiectului legată de această tranzacție. Resursa este utilizată ca referință în propunerile de facturare ale proiectului către clienți.
  - The **Rata de schimb** câmpul este implicit de la **Cursul de schimb valutar** stabilit în Dynamics 365 Finance. Dacă setarea ratei de schimb lipsește, procesul periodic **Import din etapă** nu va adăuga înregistrarea într-un jurnal și un mesaj de eroare va fi adăugat în jurnalul de execuție a lucrării.
  - Câmpul **Proprietate de linie** reprezintă tipul de facturare în realitatea proiectului. Proprietățile liniei și maparea tipului de facturare sunt definite pe **Operațiuni de proiect pe Dynamics 365 Customer Engagement** fila pe **Management de proiect și parametri contabili** pagină.

Numai următoarele atribute contabile pot fi actualizate în liniile jurnalului de integrare a Project Operations:

- **Grup de impozitare pe vânzare** și **Grup de impozitare pe vânzare articol de facturare**
- **Dimensiuni financiare** (folosind acțiunea **Distribuiți sume**)

Liniile jurnalului de integrare pot fi șterse, cu toate acestea, toate liniile neîncărcate vor fi inserate din nou în jurnal după ce ați relansat procesul periodic **Import din etapă**.

Când postați jurnalul de integrare, se creează o tranzacție de contabilitate de proiect și contabilitate generală. Acestea sunt utilizate în facturarea clienților din aval, recunoașterea veniturilor și raportarea financiară.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
