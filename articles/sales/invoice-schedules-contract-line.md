---
title: Crearea unei planificări de facturare pentru o linie de contract bazată pe proiect
description: Acest subiect oferă informații despre cum să creați planificări de facturare și repere pe liniile de contract.
author: rumant
manager: Annbe
ms.date: 10/17/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b2fbec567c07d7567f1d133fa3512496039f16a1
ms.sourcegitcommit: 869bde007805ef255f61b03937e4a44aeef61df9
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 11/12/2020
ms.locfileid: "4513939"
---
# <a name="create-an-invoice-schedule-on-a-project-based-contract-line"></a>Crearea unei planificări de facturare pentru o linie de contract bazată pe proiect 

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

Puteți atribui o planificare de facturare unei linii de contract bazată pe proiect. Facturarea este permisă numai după ce contractul este câștigat și creați un contract de proiect. Un program de facturare permite crearea automată a proiectelor de facturi pentru o linie de contract bazată pe proiect. Cu toate acestea, dacă creați numai facturi manual, puteți sări peste crearea planificărilor de facturare pe liniile contractuale.

## <a name="create-a-time-and-material-invoice-schedule-for-a-contract-line"></a>Creați o planificare de facturare de timp și material pentru o linie de contract

Atunci când o linie de contract bazată pe proiect are o metodă de facturare de timp și material, puteți crea o planificare de facturare bazată pe date. Pentru a genera automat o planificare de facturare bazat pe date, parcurgeți pașii următori.

1. Accesați **Setări** > **Frecvențe de facturare** și setați o frecvență de facturare.
2. Accesați înregistrarea contractului de proiect și accesați fila **Rezumat**, în **Data de livrare solicitată**, selectați o dată.
3. Deschideți linia de contract **Timp și material** pentru care faceți planificarea de factură bazată pe date. 
4. Pe fila **Planificare de facturare**, selectați data de început pentru facturare și frecvența facturii.
5. Pe sub-grilă, selectați **Generați planificarea facturilor**. Planificarea facturării este generat cu câmpurile **Data executării facturii**, **Data limită de tranzacție** și **Rulați starea** setate în felul următor:

    - **Data executării facturii**: această dată este dictată pe baza frecvenței facturii.
    - **Data limită a tranzacției**: ziua înaintea datei limite a facturii.
    - **Rulați starea**: este setat automat la **Neexecutat**. Când operațiunea de creare automată a facturii rulează pentru o anumită dată de rulare a facturii, acest câmp este actualizat la **Rulare reușită** sau **Rularea nu a reușit**.

## <a name="create-a-fixed-price-invoice-schedule-for-a-contract-line"></a>Creați o planificare de factură cu preț fix pentru o linie de contract

Când o linie de contract are o metodă de facturare fixă, puteți crea o planificare de factură pe bază de reper. 

> [!NOTE]
> Reperele nu pot fi create pe o linie de contract dacă nu există niciun proiect mapat la linia de contract.

Parcurgeți pașii următori pentru a genera această planificare de facturare bazată pe repere pentru un set fix de repere distribuite în mod egal pentru perioada calendaristică.

1. Accesați **Setări** > **Frecvențe de facturare** și setați o frecvență de facturare.
2. Accesați înregistrarea contractului de proiect și accesați fila **Rezumat**, în **Data de livrare solicitată**, selectați o dată.
3. Deschideți linia de contract **Preț fix** pentru care creați planificarea de reper. Pe fila **Repere de facturare**, selectați data de început pentru facturare și frecvența facturii. 
4. Pe sub-grilă, selectați **Generați date scadente periodice**. Programul facturilor este generat cu **Nume de reper**, **Data reperului**, și câmpurile **Suma de reper** setate după cum urmează:

    - **Nume de reper**: acest nume este dictat de frecvența facturii.
    - **Data reperului**: această dată este dictată pe baza frecvenței facturii.
    - **Suma de reper**: această sumă este calculată prin împărțirea sumei de contract la linia de contract după numărul de repere așa cum este dictat de frecvență, începutul facturării și datele de livrare solicitate.

    Dacă linia contractuală are o valoare în câmpul **Suma estimată a impozitului**, atunci acest câmp este, de asemenea, repartizat la fiecare etapă în mod egal atunci când se generează repere periodice.

Etapele de facturare trebuie să fie egale cu valoarea contractată a liniei contractuale. Dacă nu, veți primi o eroare pe pagina **Linie de contract**. Puteți remedia eroarea verificând dacă etapele de facturare totalizează valoarea contractată a liniei prin crearea, editarea sau ștergerea unor repere. După efectuarea modificărilor, reîmprospătați pagina pentru a elimina eroarea.

### <a name="manually-create-milestones"></a>Creați manual date scadente

Puteți genera prețuri fixe de repere manual atunci când nu sunt împărțite periodic. Parcurgeți pașii următori pentru a crea manual un nou reper.

1. Deschideți linia contractuală cu preț fix pentru care creați o etapă de referință și pe fila **Planificarea facturilor**, pe subgrilă, selectați **+ Creați un reper nou al liniei Contract**. 
2. Pe pagina **Creare de reper**, introduceți informațiile necesare pe baza tabelului următor.

| Câmp | Locație | Descriere | Impactul din aval |
| --- | --- | --- | --- |
| Nume jalon | Creare rapidă | Câmp text pentru numele etapei de referință. | Acest lucru este copiat la reperul datei scadente a liniei contractului de proiect și la factură. |
| Activitate de proiect | Creare rapidă | Dacă data scadentă este legată de sarcina proiectului, puteți utiliza această referință pentru a adăuga o logică personalizată, pentru a seta starea datei scadente pe baza stării activității. | Aplicația nu are niciun impact în aval al acestei referințe la o activitate. |
| Dată jalon | Creare rapidă | Setați data la care procesul automat de creare a facturilor ar trebui să caute starea acestei etape pentru a o lua în considerare la facturare. | Acest lucru este copiat la reperul datei scadente a liniei contractului de proiect și la factură. |
| Stare factură | Creare rapidă | Când este creat un reper, această stare este mereu setată la **Nu este pregătit pentru facturare** sau **Nu a început**. | Acest lucru este copiat la reperul datei scadente a liniei contractului de proiect și la factură. |
| Valoare linie | Creare rapidă | Suma sau valoarea jalonului care va fi facturat clientului. | Acest lucru este copiat la reperul datei scadente a liniei contractului de proiect și la factură. |
| Taxe | Creare rapidă | Suma impozitului aplicată la reper. | Acest lucru este copiat la reperul datei scadente a liniei contractului de proiect și la factură. |

3. Selectați **Salvare și închidere**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]