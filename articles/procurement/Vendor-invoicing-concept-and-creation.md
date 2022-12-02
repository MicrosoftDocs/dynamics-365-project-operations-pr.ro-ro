---
title: Crearea facturilor de furnizor
description: Acest articol descrie conceptul de facturi de furnizor și explică modul de creare a acestora în Microsoft Dynamics 365 Project Operations.
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
# <a name="create-vendor-invoices"></a>Crearea facturilor de furnizor

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

Pentru a utiliza funcționalitatea descrisă în acest articol, trebuie să activați caracteristica **Activare procesare a valorilor reale pentru subcontract cu Project Operations pentru scenarii bazate pe resurse** în spațiul de lucru **Managementul caracteristicilor**.

Facturarea furnizorilor în Microsoft Dynamics 365 Project Operations poate fi utilizată pentru a înregistra costurile din livrările de servicii și/sau materiale pe un proiect care este finalizat de către furnizori.

Atunci când serviciile și/sau materialele sunt subcontractate unui furnizor, un subcontract reprezintă acordul contractual cu acel furnizor. Pe măsură ce furnizorul furnizează serviciile sau pe măsură ce materialele sunt primite și utilizate pentru sarcinile proiectului, costurile sunt înregistrate în proiect. Apoi, furnizorul trimite periodic facturi. Aceste facturi sunt verificate și potrivite cu costurile care sunt înregistrate în proiect. După finalizarea procesului de verificare, factura furnizorului este confirmată și eliberată pentru plată.

## <a name="scenarios-for-use"></a>Scenarii de utilizare

Facturile de furnizor din Project Operations pot fi utilizate pentru a susține două scenarii distincte:

- Clienții folosesc toate experiențele de subcontractare.
- Clienții nu folosesc toate experiențele de subcontractare, dar doresc să aibă o viziune unificată a costurilor proiectelor în Project Operations.

### <a name="customers-use-the-full-subcontracting-experiences"></a>Clienții folosesc toate experiențele de subcontractare

Experiențele de facturare a furnizorilor oferă o modalitate de a verifica intrările de timp, utilizarea materialelor și intrările de cheltuieli care fac referire la componentele subcontractate și le potrivesc cu liniile de factură de furnizor. Acest proces poate fi utilizat pentru a verifica acuratețea liniilor de factură a furnizorului. După finalizarea procesului de verificare și confirmarea facturii furnizorului, sistemul inversează valorile reale care au fost înregistrate de jurnalele aprobate de timp, cheltuieli și utilizare a materialelor și va crea, mai apoi, noi costuri reale utilizând liniile de factură de furnizor.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>Clienții nu folosesc toate experiențele de subcontractare, dar doresc să aibă o viziune unificată a costurilor proiectelor în Project Operations

Dacă urmăriți procesul de subcontractare într-un sistem terță parte, puteți înregistra costurile din acel sistem terță parte către Project Operations, creând facturi de furnizor care nu fac referire la subcontracte. În acest fel, managerii dvs. de proiect pot avea o vedere unică și unificată a tuturor costurilor pentru un anumit proiect.

## <a name="create-vendor-invoices-in-project-operations"></a>Creați facturile de furnizor în Project Operations

Facturile de furnizor sunt create în Dynamics 365 Finance, utilizând modulul **Conturi de plată**. Nu puteți crea facturi de furnizor direct în Dataverse.

### <a name="set-up-vendor-invoice-verification"></a>Configurați verificarea facturii de furnizor

Dacă factura de furnizor este destinată unui subcontract în Dataverse, trebuie să activați parametrul **Este necesară verificarea manuală de către PM**. Setarea opțiunii determină dacă factura furnizorului trebuie confirmată automat în Dataverse sau dacă necesită confirmare manuală. Antetul fiecărei facturi de furnizor de proiect include o opțiune cu același nume. În mod implicit, opțiunea din antetul tuturor facturilor de furnizor de proiect este setată la valoarea pe care ați setat-o aici. Cu toate acestea, puteți actualiza valoarea după cum este necesar în antetul facturilor individuale ale furnizorilor.

Dacă opțiunea este setată la **Da**, factura de furnizor care este creată în Finanțe și sincronizată cu Dataverse are starea **Schiță**. Factura trebuie apoi să fie validată și verificată de managerul de proiect și confirmată, înainte de a fi procesată și înregistrată în conturile specifice de proiect și în cele contabile din Finanțe.

Dacă opțiunea este setată la **Nu**, factura de furnizor este confirmată automat. Nu este necesară nicio acțiune suplimentară.

Pentru a configura verificarea facturii de furnizor, urmați acești pași.

1. În Finanțe, accesați **Gestionarea proiectelor și contabilitate** \> **Configurare** \> **Gestionarea proiectelor și parametrii contabili**.
1. Pe fila **Financiar**, setați opțiunea **Este necesară verificarea manuală de către PM** la **Da** dacă politica companiei solicită verificarea facturilor de furnizor ale subcontractanților. Dacă nu este necesară verificarea de către managerul de proiect în Dataverse, lăsați setarea de opțiune la **Nu**. În mod implicit, setarea va fi utilizată pe pagina **Factură de furnizor în așteptare**.

> [!NOTE]
> Facturile de furnizor care sunt create pentru subcontracte în Dataverse pot fi procesate corect numai dacă opțiunea **Este necesară verificarea manuală de către PM** este setată la **Da**. Timpul, materialele și costurile reale pe care le creează subcontractanții pot fi asociate manual cu liniile de factură ale furnizorului de către managerul de proiect numai dacă această opțiune este setată la **Da**.

### <a name="set-up-a-procurement-integration-account-for-vendor-invoices"></a>Configurați un cont de integrare a achizițiilor pentru facturile de furnizor

Când o factură de furnizor este înregistrată în Finanțe pentru Project Operations – Mediu integrat (inexistent în stoc), datele financiare sunt înregistrate în contul de integrare Achiziții. Sistemul generează valorile reale în Dataverse pentru factura publicată. Aceste valori reale sunt publicate în Finanțe utilizându-se Jurnalul de integrare a proiectului. Publicarea jurnalului de integrare a proiectului publică costul real și inversează contul de Integrare a achizițiilor.

Pentru a configura un Cont de integrare a achizițiilor pentru facturile furnizorilor, urmați acești pași.

1. În Finanțe, accesați **Gestionarea proiectelor și contabilitate** \> **Configurare** \> **Gestionarea proiectelor și parametrii contabili**.
1. Pe fila **Project operations on Dynamics 365 customer engagement**, selectați **Materiale** \> **Cont de integrare a achizițiilor**.

### <a name="create-and-post-subcontract-vendor-invoices"></a>Crearea și publicarea facturilor furnizorilor subcontracți

Atunci când un funcționar pentru Conturi de plată primește o factură de la subcontractant, se creează o nouă factură în Finanțe.

1. În Finanțe, accesați **Conturi de plată** \> **Facturi** \> **Facturi de furnizor în așteptare**.
1. Pe **Panoul de acțiuni**, selectați **Nou** pentru a crea o factură de furnizor.
1. Pe antetul facturii, în câmpul **Cont de factură**, selectați **Subcontractant**.
1. Selectați data facturii.
1. Pe fila **Antet**, setați opțiunea **Este necesară verificarea manuală de către PM** la **Da**. Setarea implicită a acestei opțiuni se află pe pagina **Management de proiect și parametrii contabili**. Cu toate acestea, aceasta poate fi modificată la nivel de factură de furnizor.
1. Pe FastTab **Linie de factură**, selectați **Adăugare linie** pentru a crea o linie de factură pentru furnizor.
1. Selectați categoria de achiziții care a fost creată pentru liniile de subcontractare și introduceți prețul unitar, unitatea de măsură și cantitatea.
1. În secțiunea linii de factură de furnizor, pe fila **Proiect**, selectați proiectul pentru care subcontractantul partajează factura de subcontract.
1. Selectați categoria de proiect. Poate fi de orice tip de **Articol**, **Cheltuieli**, **Materiale** sau **Ore**.
1. Selectați rolul numai dacă categoria de proiect selectată este de tip **Oră**.
1. Selectați **Publicare** pentru a publica factura furnizorului.

Alternativ, puteți crea o factură de furnizor accesând **Conturi de plată** \> **Facturi** \> **Deschidere facturi de furnizori** și selectând **Nou**.

Când factura furnizorului este publicată, aceasta devine disponibilă în Dataverse pentru verificarea si prelucrarea de către managerul de proiect.

## <a name="vendor-invoice-processing-in-dataverse"></a>Procesarea facturii furnizorului în Dataverse

În factura de furnizor care este creată în Dataverse, unele valori de câmp provin din factura de furnizor care este înregistrată în Finanțe. Alte valori sunt valori implicite care provin din subcontract.

Următoarele câmpuri și înregistrările aferente vor fi copiate din subcontract în antetul facturii furnizorului:

- Moneda
- Unitate contractantă
- Termeni de plată

Pe liniile de factură de furnizor, Project Operations utilizează următoarele valori de câmp pentru a introduce referința implicită a subcontractului și a liniei de subcontract:

- Clasă de tranzacții
- Rol
- Categorie tranzacție
- Câmpuri de produs
- Project
- Activitate

> [!NOTE]
> Liniile de subcontractare cu preț fix nu sunt acceptate în Project Operations.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
