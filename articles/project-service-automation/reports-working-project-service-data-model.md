---
title: Lucrul cu modelul de date Project Service Automation
description: Acest subiect oferă informații despre modul de lucru cu modelul de date.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: e1a177a8-cd16-4ac4-acb8-a8f1a8f9e4bf
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: b909099af2493c4010103189c2add6175eea8add
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754800"
---
# <a name="working-with-the-project-service-automation-data-model"></a>Lucrul cu modelul de date Project Service Automation

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation extinde alte entități ale aplicației și introduce propriile entități în modelul de date Common Data Service. Acest subiect descrie unele dintre entitățile pe care le veți întâlni în scenarii tipice de raportare PSA.

## <a name="reporting-on-opportunities"></a>Raportarea oportunităților

Project Service Automation extinde entitatea **Oportunitate** a Dynamics 365 Sales prin adăugarea de câmpuri care permit scenarii bazate pe proiect. Aceste câmpuri sunt identificate printr-un nume de schemă care este prefixat cu **msdyn\_**. Un câmp nou, care este important pentru raportarea pe oportunități PSA este **Tipul de comandă**. O valoare a acestui câmp de **Pe bază de lucru** indică faptul că oportunitatea este o oportunitate PSA. Alte câmpuri care au fost adăugate la entitate includ **Organizația contractantă**, care surprinde organizația care deține oportunitatea și **Managerul de cont**, care surprinde numele managerului de cont care este responsabil pentru oportunitate.

Entitatea **Linie de oportunitate** include, de asemenea, câmpuri care sunt legate de Project service. **Metoda de facturare** indică dacă linia de oportunitate trebuie facturată pe bază de timp și materiale sau pe bază de preț fix, iar **Proiect** surprinde numele proiectului care sprijină oportunitatea. Alte câmpuri pe care le puteți raporta captează costurile și sumele din bugetul clientului pentru articolul de linie.

## <a name="reporting-on-quotes"></a>Raportarea ofertelor

PSA extinde entitatea **Ofertă** vânzări, adăugând câmpuri legate de proiect. **Tipul comenzii** distinge ofertele PSA de ofertele non-PSA. O valoare a acestui câmp de **Pe bază de lucru** indică faptul că oferta este o ofertă PSA. Alte câmpuri care pot fi relevante pentru raportarea ofertelor PSA includ câmpurile de valoare, precum **Costuri tarifabile**, **Costuri netarifabile**, **Marjă brută**, **Estimări** și **Buget**. Alte domenii utile indică dacă oferta este profitabilă, dacă aceasta va fi finalizată conform programării și dacă îndeplinește așteptările bugetului clientului.

PSA extinde, de asemenea entitatea **Linie ofertă** vânzări. Un câmp pe care PSA îl adaugă este **Metoda de facturare**, care indică modul în care va fi facturată linia de ofertă (timp și materiale sau preț fix). Alte câmpuri care au fost adăugate entității capturează proiectul corelat care sprijină linia de ofertă, facturarea, costul și bugetul.

PSA adaugă, de asemenea, noi entități legate de ofertă la modelul de date Dynamics 365. Iată câteva exemple:

- **Detaliu linie ofertă** – Această entitate conține detaliile estimării proiectului pentru linia de ofertă. Are două înregistrări pentru fiecare linie de ofertă. O înregistrare stochează detaliile costului și costului liniei de ofertă, iar cealaltă înregistrare stochează suma vânzărilor și detaliile de vânzare ale liniei de ofertă.
- **Program factură linie ofertă** – Această entitate conține programul de facturare pentru linia de ofertă. Acest program este generat pe baza frecvenței de facturare care este atribuită liniei de ofertă.
- **Jalon linie de ofertă** – Această entitate conține jaloanele de facturare pentru liniile de ofertă cu preț fix.
- **Defalcare analitică linie ofertă** – Această entitate conține detaliile financiare pentru linia de ofertă. Aceste detalii pot fi utile pentru raportarea vânzărilor din ofertă și a costurilor estimate după diverse dimensiuni.

Alte entități pe care PSA adaugă la oferte sunt **Listă de prețuri proiect linie de ofertă**, **Categorie resurse linie de ofertă** și **Categorie tranzacție linie de ofertă**.

![Diagrama care arată oferta, linia de ofertă și relațiile de proiect](media/PS-Reporting-image2.png "Diagrama care arată oferta, linia de ofertă și relațiile de proiect")

## <a name="reporting-on-project-contracts"></a>Raportarea contractelor de proiect

PSA extinde entitatea **Comandă** de vânzări care se utilizează la înregistrarea contractelor de proiect. Se adaugă un câmp nou important, **Tip de comandă**, care identifică contractul ca un contract de proiect PSA în loc de o comandă de vânzare. O valoare a acestui câmp de **Pe bază de lucru** indică faptul că respectiva comandă este un contract de proiect PSA. Alte câmpuri noi care sunt adăugate la entitatea **Comandă** capturează detalii despre costuri, starea contractului PSA și organizația care deține contractul.

PSA extinde, de asemenea entitatea **Linie ofertă vânzări**. Printre câmpurile pe care le adaugă sunt câmpuri care capturează metoda de facturare (timp și materiale sau preț fix), sumele din bugetul clientului și proiectul subiacent.

PSA adaugă, de asemenea, noi entități care sunt proiectate pentru contractele de proiect. Iată câteva exemple:

- **Detaliu linie contract proiect** – Această entitate conține detaliile la nivel de linie care sunt rulate până la suma liniei de contract. Acestea pot fi la fel de detaliate ca elemente de linie care sunt generate dintr-un program de proiect la nivel de activitate.
- **Program factură linie contract** – Această entitate conține programul de facturare generat pe baza frecvenței facturii care este asociată liniei de contract.
- **Jalon contract** – Această entitate conține etapele de facturare pentru liniile de contract care au un termen de facturare cu preț fix.

Alte entități pe care PSA le adaugă la contracte sunt **Listă de prețuri proiect linie pe proiect**, **Categorie resurse linie contract pe proiect** și **Categorie tranzacție linie contract pe proiect**.

![Diagrama care arată comanda, linia de comandă și relațiile de proiect](media/PS-Reporting-image3.png "Diagrama care arată comanda, linia de comandă și relațiile de proiect")

## <a name="reporting-on-projects"></a>Raportarea pe proiecte

Entitatea **Proiecte** și entitățile asociate sunt exclusive pentru PSA. **Proiect** este entitatea de nivel superior care este utilizată pentru a captura partea de lucru și de cost a operațiunilor. Iată o listă a entităților corelate:

- **Membru echipă de proiect** - Această entitate conține detalii despre resursele care se pot rezerva care sunt atribuite proiectului. Aceste resurse pot fi resurse rezervate generic, sau pot fi numite resurse care se pot rezerva care sunt fie introduse de managerul de proiect, fie generate din programul de proiect.
- **Activitate proiect** – Această entitate conține activitățile care alcătuiesc planul sau programul de proiect.
- **Atribuire resurse** – Această entitate conține atribuirea sarcinilor pentru resursa care se poate rezerva.
- **Cerință resursă** – Această entitate conține cerințele pentru orice membri generici ai echipei de resurse.
- **Estimare** și **Linie estimare** -Aceste entități au o relație antet/linie și conțin estimări de cheltuieli pentru proiect. Estimările de activitate sunt stocate pe entitatea **Estimare resursă**.

![Diagrama care arată cerința de resurse și relațiile de proiect](media/PS-Reporting-image4.png "Diagrama care arată cerința de resurse și relațiile de proiect")

## <a name="reporting-on-resources"></a>Raportarea resurselor

Resursele proiectului utilizează entitățile **Resursă care poate fi rezervată** din Universal Resource Scheduling (URS) care sunt partajate cu alte aplicații, precum Microsoft Dynamics 365 Field Service. Iată o listă a entităților pe care este posibil să le utilizați atunci când raportați resursele proiectului:

- **Resursă care poate fi rezervată** – Această entitate reprezintă utilizatorul, persoana de contact, resursa generică, contul, grupul sau echipamentul utilizat în echipa de proiect.
- **Caracteristici resursă care poate fi utilizată** – Această entitate include abilitățile, certificările sau educația resursei. Caracteristicile pot avea valori de rating care sunt definite de modelul de rating.
- **Categoria resursei care poate fi rezervate** – Această entitate reprezintă rolul resursei care poate fi rezervată.
- **Rezervările de resurse care pot fi rezervate** – Această entitate reprezintă timpul rezervat pe proiecte pentru resursă. Fiecare rezervare are atât o entitate antet, cât și entități de linie, iar fiecare linie are o stare care reprezintă starea rezervării.

![Diagrama care prezintă relațiile cu caracteristicile resurselor rezervabile](media/PS-Reporting-image5.png "Diagrama care prezintă relațiile cu caracteristicile resurselor rezervabile")

## <a name="reporting-on-actual-transactions"></a>Raportarea tranzacțiilor efective

Când aprobați o foaie de pontaj sau o cheltuială sau când facturați un contract în PSA, tranzacția de business este capturată în entitatea **Valoare reală**. Această entitate poate servi drept bază pentru aproape toate rapoartele legate de finanțare în PSA. Entitatea **Valoare reală** surprinde tranzacțiile cost și vânzări pentru evenimentul de business. De asemenea, surprinde multe atribute relevante.

Când lucrați cu entitatea **Valoare reală**, este important să înțelegeți ce tranzacție sau tranzacții sunt înregistrate în entitate și când sunt înregistrate tranzacțiile. Iată fluxul tipic atunci când lucrați cu înregistrări de timp (fluxul pentru înregistrările de cheltuieli este similar):

1. Când se salvează înregistrarea de timp, nu sunt create înregistrări în entitatea **Valoare reală**.
2. Când se remite înregistrarea de timp, nu sunt create înregistrări în entitatea **Valoare reală**.
3. Când este aprobată intrarea de timp, se creează o înregistrare în entitatea **Valoare reală** și se poate crea și o a doua înregistrare. Prima înregistrare stochează costul înregistrării de timp. A doua înregistrare stochează suma de vânzări nefacturată a intrării de timp. A doua înregistrare depinde dacă proiectul are un client, o ofertă sau o linie de contract atribuită.

    | Data documentului | Tipul tranzacției | Clasă de tranzacții | Client         | Contract   | Resursă     | Rol resursă | Tip de facturare | Cantitate | Preț unitar | Valoare |
    |---------------|------------------|-------------------|------------------|------------|--------------|---------------|--------------|----------|------------|--------|
    | 2/3/18        | Cost             | Time              | Casă de schi alpin | Alpine CRM | Maria Bușcan | Manager Project   | Taxabil   | 8.0      | 50.00      | 400.00 |
    | 2/3/18        | Vânzări nefacturate   | Time              | Casă de schi alpin | Alpine CRM | Maria Bușcan | Manager Project   | Taxabil   | 8.0      | 100.00     | 800.00 |

    Aceste două înregistrări sunt separate, dar legate. Nu sunt nici debite, nici credite.

4. Dacă un contract este asociat cu proiectul, atunci când este facturată intrarea de timp, două mai multe înregistrări sunt create în entitatea **Valoare reală**. În primul rând, este creată o sumă negativă pentru înregistrarea de vânzări nefacturată. Această înregistrare inversează, în esență, vânzarea nefacturată. În al doilea rând, este creată o tranzacție pentru vânzarea facturată. Încă o dată, aceste înregistrări sunt separate, dar legate între ele, nu debite și credite.

    | Data documentului | Tipul tranzacției | Clasă de tranzacții | Client         | Contract   | Resursă     | Rol resursă | Tip de facturare | Cantitate | Preț unitar | Valoare   |
    |---------------|------------------|-------------------|------------------|------------|--------------|---------------|--------------|----------|------------|----------|
    | 2/4/18        | Vânzări nefacturate   | Time              | Casă de schi alpin | Alpine CRM | Maria Bușcan | Manager Project   | Taxabil   | - 8,0    | 100.00     | - 800,00 |
    | 2/4/18        | Vânzări facturate     | Time              | Casă de schi alpin | Alpine CRM | Maria Bușcan | Manager Project   | Taxabil   | 8.0      | 100.00     | 800.00   |

Entitatea **Origine tranzacție** înregistrează originea înregistrării **Valoare reală** și entitatea **Conexiune tranzacție** înregistrează înregistrările corelate pentru înregistrarea **Valoare reală**. În plus, înregistrarea **Valoare reală** conține referințe la proiect, contractul de proiect (comanda), resursa care se poate rezerva și client.

![Diagrama care arată conexiunea tranzacției, originea și relațiile reale](media/PS-Reporting-image6.png "Diagrama care arată conexiunea tranzacției, originea și relațiile reale")
