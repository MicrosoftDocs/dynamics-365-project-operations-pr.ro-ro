---
title: Crearea de facturi de client și furnizor între companii
description: Acest subiect oferă informații despre cum să creați facturi de client și vânzător între companii.
author: sigitac
manager: tfehr
ms.date: 11/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: dd9aa1a4d167d556206a487e79983090b3f4592a
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287478"
---
# <a name="create-intercompany-customer-and-vendor-invoices"></a>Crearea de facturi de client și furnizor între companii

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

Un contabil de proiect dintr-o entitate juridică care împrumută creează o factură de client între companii pentru costurile proiectului care sunt transferate către entitatea împrumutată. După ce se aprobă și se înregistrează factura clientului între companii, entitatea juridică care acordă împrumuturi trimite factura între companii către persoana juridică care împrumută.

Contabilul de proiect pentru entitatea juridică care acordă împrumuturi poate stabili un proces de lot pentru a genera facturi între companii pe o bază recurentă. Contabilul de proiect specifică criteriile, cum ar fi proiecte specifice, pentru a crea facturi între companii într-un lot.

## <a name="manually-create-an-intercompany-customer-invoice-for-project-transactions"></a>Creați manual o factură client între companii pentru tranzacțiile proiectului 

Utilizați această procedură pentru a crea manual o factură de client între companii pentru tranzacții de proiect. Căutați orele care au fost postate de lucrători în proiecte ale entităților juridice care împrumutau și cheltuielile suportate de persoana dvs. juridică în numele entităților juridice care împrumutau. Puteți căuta după numele entității juridice, numărul contractului de proiect, numărul proiectului, intervalul de date sau orice combinație a acestor opțiuni. În rezultatele căutării, selectați tranzacțiile pe care să le adăugați la o factură între companii.

1. În Dynamics 365 Finance, accesați **Management de proiect și contabilitate** > **Facturi de proiect** > **Facturi de clienți între companii**. Pe pagina listă **Facturi clienți între companii**, în panoul de acțiuni, selectați **Nou.**
2. Pe pagina **Creați factură între companii**, în câmpul **Entitate legală**, selectați o entitate juridică care împrumută.
3. Opțional: introduceți un anumit contract de proiect și un număr de proiect.
4. Limitați căutarea selectând un interval de date. Introduceți date specifice în câmpurile **Data de început** și **Data de încheiere**. Numai tranzacțiile între companii care sunt înregistrate în acest interval de date sunt afișate în rezultatele căutării.
5. Stabiliți **Parametru avansat de linie jurnal proiect** la **Da** și selectați **Căutare**.
6. În rezultatele căutării, selectați tranzacțiile pe care să le includeți în propunerea de facturare între companii, apoi selectați **OK**.
7. Pe pagina **Factură de client între companii**, sunt afișate tranzacțiile proiectului între companii pe care le-ați selectat din rezultatele căutării. Pentru a modifica tranzacțiile înainte de a trimite factura persoanei juridice împrumutate, procedați în felul următor:
  
    1. Deschideți pagina **Creați o propunere de factură**. Selectați tranzacții suplimentare între companii pentru factura curentă, apoi selectați **Adăugați linie**.
    2. Pentru a elimina o linie, selectați-o, apoi selectați **Eliminare**.
    3. Vizualizați comentarii, motive, dimensiuni financiare și alte informații despre o linie selectată pe FastTab  **Linii de facturare**.
    
8. Pentru a publica factura de client între companii, pe panoul de acțiuni, selectați **Publicare**.

> [!NOTE]
> Dacă organizația dvs. solicită revizuirea facturilor între companii înainte de a fi postate, un administrator de sistem ar putea seta un flux de lucru pentru facturile între companii. Dacă nu este configurat un flux de lucru pentru facturile între companii, puteți posta factura între companii.

## <a name="create-a-batch-job-for-intercompany-invoices"></a>Creați o operațiune în lot pentru facturile între companii

Puteți crea mai multe facturi între companii în același timp pentru toate persoanele juridice care împrumută. Folosind funcționalitatea de căutare, puteți, de exemplu, să căutați toate tranzacțiile care sunt înregistrate de lucrătorii împrumutați și care sunt legate de proiecte gestionate de alte entități juridice. Apoi, pentru fiecare entități juridice care împrumută, puteți crea o factură între companii pentru tranzacțiile furnizate în rezultatele căutării.

1. Accesați **Management de proiect și contabilitate** > **Periodic** > **Facturi de proiect** > **Creați facturi de clienți între companii**.
2. Pe pagina **Creați facturi de clienți între companii**, în câmpul **Companie**, selectați o entitate juridică de facturat. Dacă nu selectați o companie, toate tranzacțiile care îndeplinesc criteriile de căutare sunt afișate pentru toate entitățile juridice care împrumută.
3. În **Creați o factură per**, selectați dacă doriți să creați o factură pentru tranzacțiile între companii pe baza unui proiect sau pe baza unei entități juridice care împrumută.
4. Opțional: pentru a selecta un anumit proiect și un contract de proiect pentru care să creați facturi între companii, faceți clic pe **Selectați**. Pe pagina **Interogare**, în câmpul **Criterii**, selectați contractul de proiect, numărul proiectului sau ambele, apoi selectați **OK**.
5. Pe fila **Lot**, configurați un proces discontinuu pentru a crea facturi între companii în mod recurent. Pentru mai multe informații, consultați [Trimiteți o operațiune de procesare în serie dintr-un formular](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/submit-a-batch-processing-job-from-a-form).
6. Pentru a publica facturi între companii, pe panoul de acțiuni, selectați **Publicare**.

> [!NOTE]
> Dacă organizația dvs. solicită revizuirea facturilor între companii înainte de a fi postate, un administrator de sistem ar putea seta un flux de lucru pentru facturile între companii. Dacă nu este configurat un flux de lucru pentru facturile între companii, puteți posta facturi între companii.

## <a name="post-the-intercompany-vendor-invoice"></a>Înregistrați factura furnizorului între companii

Un contabil de proiect din entitatea juridică care împrumută poate revizui facturile de la furnizori între companii neplătite când este publicată factura corespunzătoare de client între companii. În Finanțe, în entitatea juridică cu împrumut, accesați **Conturi furnizori** > **Facturi** > **Factură de furnizor în așteptare**. Numărul de factură în așteptare se va potrivi cu numărul de factură al clientului între companii. Verificați dacă factura este corectă și apoi postați factura. Înregistrarea facturii furnizorului între companii creează un cont de proiect și o tranzacție de contabilitate generală care reflectă costurile tranzacției în entitatea juridică care împrumută.


[!INCLUDE[footer-include](../includes/footer-banner.md)]