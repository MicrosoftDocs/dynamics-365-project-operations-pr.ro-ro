---
title: Creați facturi pentru furnizori
description: Acest articol descrie conceptul de facturi ale furnizorului și explică cum să le creați în Microsoft Dynamics 365 Project Operations.
author: suvaidya
ms.date: 9/12/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 7f6c1ec46f23b6823734b28755b80ced4e3f9325
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475473"
---
# <a name="create-vendor-invoices"></a>Creați facturi pentru furnizori

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

Pentru a utiliza funcționalitatea descrisă în acest articol, trebuie să activați **Activați procesarea subcontractelor reale cu Operațiuni de proiect pentru scenarii bazate pe resurse** caracteristică în **Managementul caracteristicilor** spațiu de lucru.

Facturarea furnizorilor în Microsoft Dynamics 365 Project Operations poate fi folosit pentru a înregistra costurile din livrările de servicii și/sau materiale pe un proiect care este finalizat de furnizori.

Atunci când serviciile și/sau materialele sunt subcontractate unui furnizor, un subcontract reprezintă acordul contractual cu acel furnizor. Pe măsură ce furnizorul furnizează serviciile sau pe măsură ce materialele sunt primite și utilizate în sarcinile proiectului, costurile sunt înregistrate în proiect. Apoi, vânzătorul trimite periodic facturi. Aceste facturi sunt verificate și corelate cu costurile care sunt înregistrate în proiect. După finalizarea procesului de verificare, factura furnizorului este confirmată și eliberată pentru plată.

## <a name="scenarios-for-use"></a>Scenarii de utilizare

Facturile furnizorilor din Operațiunile de proiect pot fi utilizate pentru a susține două scenarii distincte:

- Clienții folosesc toate experiențele de subcontractare.
- Clienții nu folosesc experiențele complete de subcontractare, dar doresc să aibă o vedere unificată a costurilor pe proiecte în Operațiuni de proiect.

### <a name="customers-use-the-full-subcontracting-experiences"></a>Clienții folosesc toate experiențele de subcontractare

Experiențele de facturare a furnizorilor oferă o modalitate de a verifica intrările de timp, utilizarea materialelor și intrările de cheltuieli care fac referire la componentele subcontractate și de a le potrivi cu liniile de factură ale furnizorului. Acest proces poate fi utilizat pentru a verifica acuratețea liniilor de factură a furnizorului. După finalizarea procesului de verificare și confirmarea facturii furnizorului, sistemul inversează valorile reale care au fost înregistrate prin jurnalele aprobate de timp, cheltuieli și utilizare a materialelor, apoi creează noi valori efective ale costurilor utilizând liniile de factură a furnizorului.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>Clienții nu folosesc toate experiențele de subcontractare, dar doresc să aibă o viziune unificată a costurilor proiectelor în Operațiuni de proiect

Dacă urmăriți procesul de subcontractare într-un sistem terță parte, puteți înregistra costurile din acel sistem terță parte către Operațiuni de proiect, creând facturi de furnizor care nu fac referire la subcontracte. În acest fel, managerii dvs. de proiect pot avea o vedere unică și unificată a tuturor costurilor pentru un anumit proiect.

## <a name="create-vendor-invoices-in-project-operations"></a>Creați facturi de furnizor în Operațiuni de proiect

Facturile furnizorilor sunt create în Dynamics 365 Finance, folosind **Creanţe** modul. Nu puteți crea facturi de furnizor direct în Dataverse.

### <a name="set-up-vendor-invoice-verification"></a>Configurați verificarea facturii furnizorului

Dacă factura furnizorului este destinată unui subcontract în Dataverse, trebuie să activați **Este necesară verificarea manuală de către PM** parametru. Setarea opțiunii determină dacă factura furnizorului trebuie confirmată automat în Dataverse, sau dacă necesită confirmare manuală. Antetul fiecărei facturi de furnizor de proiect include o opțiune cu același nume. În mod implicit, opțiunea din antetul tuturor facturilor furnizorilor de proiect este setată la valoarea pe care ați setat-o aici. Cu toate acestea, puteți actualiza valoarea după cum este necesar în antetul facturilor individuale ale furnizorilor.

Dacă opțiunea este setată la **da**, factura de furnizor care este creată în Finanțe și sincronizată cu Dataverse are **Proiect** stare. Factura trebuie apoi validată și verificată de managerul de proiect și confirmată, înainte de a fi procesată și înregistrată în conturile specifice de proiect și contabile în Finanțe.

Dacă opțiunea este setată la **Nu**, factura furnizorului este confirmată automat. Nu este necesară nicio acțiune suplimentară.

Pentru a configura verificarea facturii furnizorului, urmați acești pași.

1. În Finanțe, accesați **Management de proiect si contabilitate** \> **Înființat** \> **Management de proiect și parametri contabili**.
1. Pe **Financiar** fila, setați **Este necesară verificarea manuală de către PM** opțiunea pentru **da** dacă politica companiei necesită verificarea facturilor furnizorilor subcontractanților. Dacă nu este necesară verificarea de către managerul de proiect în Dataverse, lăsați set de opțiuni **Nu**. În mod implicit, setarea va fi utilizată pe **Factura furnizorului în așteptare** pagină.

> [!NOTE]
> Facturi de furnizor care sunt create pentru subcontracte în Dataverse pot fi procesate corect numai dacă **Este necesară verificarea manuală de către PM** opțiunea este setată la **da**. Timpul, materialul și costurile reale pe care le creează subcontractanții pot fi asociate manual cu liniile de factură ale furnizorului de către managerul de proiect numai dacă această opțiune este setată la **da**.

### <a name="set-up-a-procurement-integration-account-for-vendor-invoices"></a>Configurați un cont de integrare a achizițiilor pentru facturile furnizorilor

Când o factură de furnizor este înregistrată în Finanțe pentru operațiuni de proiect – Mediu integrat (fără stoc), datele financiare sunt înregistrate în contul de integrare Achiziții. Sistemul generează efectivele în Dataverse pentru factura afisata. Aceste date reale sunt publicate în Finanțe utilizând jurnalul de integrare a proiectului. Înregistrarea jurnalului de integrare a proiectului înregistrează costul real și inversează contul de integrare a achizițiilor.

Pentru a configura un cont de integrare Achiziții pentru facturile furnizorilor, urmați acești pași.

1. În Finanțe, accesați **Management de proiect si contabilitate** \> **Înființat** \> **Management de proiect și parametri contabili**.
1. Pe **Operațiuni de proiect privind implicarea clienților Dynamics 365** filă, selectați **Materiale** \> **Cont de integrare a achizițiilor**.

### <a name="create-and-post-subcontract-vendor-invoices"></a>Creați și postați facturi furnizorilor de subcontractare

Atunci când un funcționar pentru conturi plătibile primește o factură de la subcontractant, se creează o nouă factură în Finanțe.

1. În Finanțe, accesați **Conturi creditoare** \> **Facturi** \> **Facturi de furnizor în așteptare**.
1. Pe **Panoul de acțiuni**, Selectați **Nou** pentru a crea o factură de furnizor.
1. Pe antetul facturii, în **Cont de factură** câmp, selectați **Subcontractant**.
1. Selectați data facturii.
1. Pe **Antet** fila, setați **Este necesară verificarea manuală de către PM** opțiunea pentru **da**. Setarea implicită a acestei opțiuni vine de la **Management de proiect și parametri contabili** pagină. Cu toate acestea, acesta poate fi modificat la nivelul facturii furnizorului.
1. Pe **Linia de factură** FastTab, selectați **Adăugați linie** pentru a crea o linie de factură pentru furnizor.
1. Selectați categoria de achiziții care a fost creată pentru liniile de subcontractare și introduceți prețul unitar, unitatea de măsură și cantitatea.
1. În secțiunea linii de factură furnizor, pe **Proiect** fila, selectați proiectul pentru care subcontractantul împărtășește factura de subcontract.
1. Selectați categoria proiectului. Poate fi de orice tip de **Articol**, **·**, **·**, sau **Ore**.
1. Selectați rolul numai dacă categoria de proiect selectată este din **Ora** tip.
1. Selectați **Post** pentru a posta factura furnizorului.

Alternativ, puteți crea o factură de furnizor accesând **Creanţe** \> **Facturi** \> **Deschideți facturile furnizorilor** și selectând **Nou**.

Când factura furnizorului este înregistrată, aceasta devine disponibilă în Dataverse pentru verificarea si prelucrarea managerului de proiect.

## <a name="vendor-invoice-processing-in-dataverse"></a>Procesarea facturii furnizorului în Dataverse

În factura de furnizor care este creată în Dataverse, unele valori de câmp provin din factura furnizorului care este înregistrată în Finanțe. Alte valori sunt valori implicite care provin din subcontract.

Următoarele câmpuri și înregistrările aferente vor fi copiate din subcontract în antetul facturii furnizorului:

- Moneda
- Unitate contractantă
- Termeni de plată

Pe liniile de factură pentru furnizor, Project Operations utilizează următoarele valori de câmp pentru a introduce referința implicită a subcontractului și a liniei de subcontract:

- Clasă de tranzacții
- Rol
- Categorie tranzacție
- Câmpurile de produse
- Project
- Activitate

> [!NOTE]
> Liniile de subcontractare cu preț fix nu sunt acceptate în Operațiunile de proiect.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
