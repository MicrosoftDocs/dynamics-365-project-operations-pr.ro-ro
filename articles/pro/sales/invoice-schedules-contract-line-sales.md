---
title: Crearea planificărilor de facturare pentru o linie de contract bazată pe proiect - simplificat
description: Acest subiect oferă informații despre crearea planificărilor și etapelor de facturare.
author: rumant
ms.date: 10/26/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: edacae144f5c4879d3cfdf9585281858d7312589
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8581989"
---
# <a name="create-invoice-schedules-on-a-project-based-contract-line---lite"></a>Crearea planificărilor de facturare pentru o linie de contract bazată pe proiect - simplificat

_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_

Puteți atașa o planificare de factură la o linie de contract bazată pe proiect. Facturarea este permisă numai după câștigarea contractului pentru a crea un contract de proiect. Planificările facturilor permit crearea automată a proiectelor de facturi pentru o linie de contract bazată pe proiect. Dacă intenționați să creați întotdeauna facturi manual, puteți sări peste crearea programelor de facturare pe o linie de contract bazată pe proiect sau pe o linie de contract.

## <a name="create-a-time-and-material-invoice-schedule-for-a-project-based-contract-line"></a>Creați o planificare de facturare de timp și materiale pentru o linie de contract bazată pe proiect

Atunci când o linie de contract bazată pe proiect are o metodă de facturare de timp și material, puteți crea o planificare de facturare bazată pe date. Pentru a genera automat o planificare de facturare bazat pe date, parcurgeți pașii următori.

1. Accesați **Setări** > **Frecvențe factură** pentru a seta frecvența facturii.
2. Deschideți contractul de proiect și pe fila **Rezumat**, setați data de livrare solicitată.
3. Deschideți linia contractuală de timp și materiale pentru care doriți să creați o planificare de facturare bazată pe date. 
4. Pe fila **Planificarea facturilor**, selectați o dată de începere a facturării și frecvența facturii. 
5. Pe sub-grilă, selectați **Generați planificarea facturilor**.

    Sistemul generează planificarea de facturare cu următoarele informații de câmp:

    - **Data executării facturii** este setată la dată pe baza frecvenței facturii.
    - **Data limită de tranzacție** este setată cu o zi înainte de **Data executării facturii**.
    - **Rulați starea** este setat automat la **Neexecutat**. Când operațiunea de creare automată a facturii rulează pentru o anumită **Dată de rulare a facturii**, acest câmp este actualizat la **Rulare reușită** sau **Rulare eșuată**.

## <a name="create-a-fixed-price-invoice-schedule-for-a-project-based-contract-line"></a>Crearea unei planificări de facturare cu preț fix pentru o linie de contract bazată pe proiect

Atunci când o linie de contract bazată pe proiecte are o metodă de facturare cu preț fix, puteți crea o planificare de facturare bazat pe o etapă importantă. Parcurgeți pașii următori pentru a genera automat o planificare de facturare bazat pe un reper pentru un set fix de repere care se distribuie în mod egal pentru perioada calendaristică.

1. Accesați **Setări** > **Frecvențe factură** pentru a seta frecvența facturii.
2. Deschideți contractul de proiect și pe fila **Rezumat**, setați data de livrare solicitată.
3. Deschideți linia contractuală cu preț fix pe care trebuie să creați o planificare de etapă. 
4. Pe fila **Planificarea facturilor (Jaloane de facturare)**, selectați o dată de începere a facturării și frecvența facturii. 
5. Pe sub-grilă, selectați **Generați date scadente periodice**.

    Sistemul generează planificarea de facturare cu următoarele informații de jaloane.

    - **Nume de jalon** este setat la data dictată pe baza frecvenței facturii.
    - **Dată de jalon** este setată la data dictată pe baza frecvenței facturii.
    - **Suma de jalon** se calculează prin împărțirea sumei contractului pe linia de contract bazată pe proiect la numărul de repere determinate de frecvență, începutul facturării și datele de livrare solicitate.
    - Dacă linia contractuală are o valoare în câmpul **Suma estimată a impozitului**, acest câmp este, de asemenea, repartizat la fiecare etapă în mod egal atunci când se generează jaloane periodice.

Jaloanele de facturare ar trebui să fie egale cu valoarea contractată a liniei de contract bazate pe proiect. Dacă nu sunt egale, apare o eroare. Puteți remedia acea eroare verificând dacă etapele de facturare totalizează valoarea contractată a liniei, fie prin crearea, editarea sau ștergerea etapelor de referință. După efectuarea modificărilor, reîmprospătați pagina.

### <a name="manually-create-milestones"></a>Creați manual date scadente

Etapele prețurilor fixe pot fi generate manual atunci când nu sunt împărțite periodic. Pentru a crea o etapă manuală, parcurgeți pașii următori.

1. Deschideți linia contractuală cu preț fix pe care doriți să creați o etapă. 
2. Pe fila **Planificarea facturii**, pe subgrilă, selectați **+ Creați o etapă nouă a liniei Contract**.
3. Pe formularul **Creare de reper**, introduceți informațiile solicitate pe baza tabelului următor. 

| Câmp | Locație | Descriere | Impactul din aval |
| --- | --- | --- | --- |
| Nume jalon | Creare rapidă | Câmp text pentru numele etapei de referință. | Acest câmp este inclus în etapa de referință a liniei contractului de proiect și pe factură. |
| Activitate de proiect | Creare rapidă | Dacă jalonul este legat de o activitate de proiect, utilizați această referință pentru a adăuga logică personalizată și setați starea jalonului pe baza stării activității. | Nu există un impact în aval al acestei referințe la o activitate. |
| Dată jalon | Creare rapidă | Data la care procesul de creare automată a facturilor ar trebui să caute starea acestei etape pentru a o lua în considerare la facturare. | Acesta este inclus în etapa de referință a liniei contractului de proiect și pe factură. |
| Stare factură | Creare rapidă | Când se creează jalonul, această stare este întotdeauna setată la **Nu este pregătit pentru facturare** sau **Nu a început**. | Acesta este inclus în etapa de referință a liniei contractului de proiect și pe factură. |
| Valoare linie | Creare rapidă | Valoarea sau valoarea etapei care va fi facturată clientului. | Acest câmp este inclus în etapa de referință a liniei contractului de proiect și pe factură, |
| Taxe | Creare rapidă | Suma impozitului aplicată la reper. | Acesta este inclus în etapa de referință a liniei contractului de proiect și pe factură. |

4. Selectați **Salvare și închidere**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]