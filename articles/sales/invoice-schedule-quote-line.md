---
title: Planificările de facturi pe linii de ofertă bazate pe proiect
description: Acest articol oferă informații despre crearea de programe de facturare și repere pentru liniile de ofertă.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b1e431bc3586f9fef7a01348555e4ee4e06cc66c
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918327"
---
# <a name="invoice-schedules-on-project-based-quote-lines"></a>Planificările de facturi pe linii de ofertă bazate pe proiect

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

O linie de ofertă bazată pe proiect oferă posibilitatea de a exprima o planificare de facturare. Acest lucru este opțional în faza de ofertă, deoarece aplicația nu acceptă facturarea unui proiect atunci când este legat de o linie de ofertă. Facturarea este permisă numai după ce se câștigă oferta. Singurul impact din aval al creării unei planificări de facturare în timpul fazei de ofertare este că acest program de facturare este copiat pe linia contractuală bazată pe proiect. Dacă nu creați o planificare de facturare în timpul fazei de ofertă, veți putea face acest lucru pe linia de contract bazată pe proiect.

În general, scopul planificărilor de facturare este de a permite crearea automată a proiectelor de facturi pentru o linie de contract bazată pe proiecte. 

## <a name="create-a-time-and-material-invoice-schedule-for-a-project-based-quote-line"></a>Creați un program de facturare în timp și materiale pentru o linie de ofertă bazată pe proiect

Atunci când metoda de facturare pentru o linie de ofertă bazată pe proiect este Timp și material, sistemul generează o planificare de facturare bazată pe date. Pentru a genera automat o planificare de facturare bazat pe date, parcurgeți pașii următori.

1. Accesați **Setări** > **frecvențe de facturare** și setați o frecvență de facturare.
2. Pe pagina **Oferte**, deschideți oferta proiectului și pe fila **Rezumat**, setați o dată de livrare solicitată.
3. Deschideți linia ofertă de timp și material pentru care aveți nevoie pentru a crea o planificare de facturare bazată pe date. 
4. Pe fila **Planificarea facturilor**, selectați valori în câmpurile **Începutul facturării** și **Frecvența facturii**. 
5. Pe sub-grilă, selectați **Generați planificarea facturilor**.
6. Aplicația generează programul de facturare cu câmpurile **Data executării facturii**, **Data limită tranzacție** și **Rulați starea** setate în felul următor:

    - **Data executării facturii** este setată la data dictată pe baza frecvenței facturii.
    - **Data limită a tranzacției** este setată cu o zi înainte de **Data executării facturii**.
    - **Rulați starea** este setat automat la **Neexecutat**. Când operațiunea de creare automată a facturii rulează pentru o anumită dată de rulare a facturii, va actualiza acest câmp la oricare dintre ele **Rulare reușită** sau **Rularea nu a reușit**.

## <a name="create-a-fixed-price-invoice-schedule-for-a-project-based-quote-line"></a>Creați o planificare de factură cu preț fix pentru o linie de ofertă bazată pe proiect

Când linia de ofertă bazată pe proiect are o metodă de facturare **Fixă**, sistemul creează o planificare de facturare bazată pe o dată scadentă. Parcurgeți pașii următori pentru a genera automat această planificare pentru un set fix de repere care sunt distribuite în mod egal pentru perioada calendaristică.

1. Accesați **Setări** > **frecvențe de facturare** și setați o frecvență de facturare.
2. Pe pagina **Oferte**, deschideți oferta proiectului și pe fila **Rezumat**, setați o dată de livrare solicitată.
3. Deschideți linia de preț fix pentru care trebuie să creați o planificare de dată scadentă. 
4. Pe fila **Planificarea facturilor**, selectați valori în câmpurile **Începutul facturării** și **Frecvența facturii**. 
5. Pe sub-grilă, selectați **Generați date scadente periodice**.
6. Aplicația generează planificarea facturilor cu un nume, o dată și o sumă.

    - Numele datei scadente este setat la data dictată pe baza frecvenței facturii.
    - Data scadentă este setată la data dictată pe baza frecvenței facturii.
    - Suma de referință este calculată prin împărțirea sumei de ofertă pe linia de ofertă bazată pe proiect la numărul de repere determinate de frecvența și începutul facturării și de datele de livrare solicitate.
    - Dacă linia de ofertă are, de asemenea, valoarea estimată a impozitului, această valoare este împărțită în mod egal între fiecare etapă la generarea date scadente periodice.

### <a name="manually-create-milestones"></a>Creați manual date scadente

Datele scadente ale prețurilor fixe pot fi, de asemenea, generate manual atunci când nu sunt împărțite periodic. Pentru a crea manual o dată scadentă:

Deschideți linia de ofertă de preț fix unde trebuie să creați o dată scadentă. Pe fila **Planificarea facturilor**, pe subgrilă, selectați **+ Creați o etapă nouă pentru linia de ofertă** și introduceți informațiile solicitate pe baza tabelului următor.

| **Câmp** | **Locaţie** | **Descriere** | **Impactul din aval** |
| --- | --- | --- | --- |
| Nume dată scadentă | Creare rapidă | Numele datei scadente. | Acest lucru este propagat la datei scadente a liniei contractului de proiect și la factură |
| Activitate de proiect | Creare rapidă | Dacă data scadentă este legată de sarcina proiectului, puteți utiliza această referință pentru a adăuga o logică personalizată, setați starea datei scadente pe baza stării activității. | Aplicația nu are niciun impact în aval al acestei referințe la o activitate. |
| Data datei scadente | Creare rapidă | Setați data la care procesul automat de creare a facturilor ar trebui să caute starea acestei etape pentru a o lua în considerare la facturare. | Acest lucru este propagat la datei scadente a liniei contractului de proiect și la factură. |
| Stare factură | Creare rapidă | Când se creează o etapă de referință, această stare este întotdeauna setată la **Nu este pregătit pentru facturare**. | Acest lucru este propagat la datei scadente a liniei contractului de proiect și la factură. |
| Valoare linie | Creare rapidă | Suma sau valoarea jalonului care va fi facturat clientului. | Acest lucru este propagat la datei scadente a liniei contractului de proiect și la factură. |
| Taxe | Creare rapidă | Suma impozitului care va fi aplicată jalonului. | Acest lucru este propagat la datei scadente a liniei contractului de proiect și la factură. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]