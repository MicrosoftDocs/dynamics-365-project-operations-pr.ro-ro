---
title: Concepte unice pentru ofertele bazate pe proiecte
description: Acest articol oferă informații despre ofertele de proiecte în Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/02/2022
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 89867cfbe92f47d58b16da40b62d3d9dd6a15b64
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824343"
---
# <a name="concepts-unique-to-project-based-quotes"></a>Concepte unice pentru ofertele bazate pe proiecte

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

Înainte de a începe să utilizați citatele de proiect în Microsoft Dynamics 365 Project Operations, ar trebui să fiți conștienți de următoarele concepte cheie.

## <a name="owning-company"></a>Firmă deținătoare

Societatea proprietară reprezintă persoana juridică care deține livrarea proiectului. Clientul din cotație ar trebui să fie un client valid în acea entitate juridică în aplicațiile financiare și operaționale. Moneda companiei proprietare și moneda unității contractante care este selectată pe o ofertă bazată pe proiect trebuie să se potrivească.

## <a name="contracting-unit"></a>Unitate contractantă

O unitate contractantă reprezintă divizia sau practica care deține livrarea proiectului. Puteți seta costurile resurselor pentru fiecare unitate contractantă. Când specificați costuri de resurse pentru o resursă dintr-o unitate contractantă, puteți configura rate de cost diferite pentru resursele de la care unitatea contractantă le împrumută sau pentru alte divizii sau practici din întreprindere. Aceste rate de cost sunt denumite prețuri de transfer, împrumuturi de resurse sau prețuri de schimb. Când configurați costul împrumutării resurselor de la alte divizii, puteți configura ratele de cost în moneda diviziei de creditare.

## <a name="cost-currency"></a>Monedă de cost

Moneda de cost din Operațiunile de proiect este moneda în care sunt raportate costurile. Această monedă este derivată din moneda care este atașată câmpului **Unitate contractantă** de pe cotație, contract și proiect. Costurile pentru un proiect pot fi înregistrate în orice monedă. Cu toate acestea, există o conversie valutară din moneda în care au fost înregistrate costurile în moneda de cost a proiectului.

Deoarece cursurile de schimb de pe platforma Dataverse nu pot fi aplicate în funcție de dată, totalurile de pe ecran pentru cost s-ar putea schimba în timp dacă actualizați cursurile de schimb valutar. Cu toate acestea, costurile care sunt înregistrate în baza de date rămân neschimbate, deoarece sumele sunt stocate în moneda în care au fost suportate.

## <a name="sales-currency"></a>Monedă de vânzare

Moneda de vânzări în Operațiunile de proiect este moneda în care sunt înregistrate și afișate sumele estimate și efective ale vânzărilor. Este, de asemenea, moneda în care clientul este facturat pentru tranzacție. Pentru o ofertă de proiect, o monedă de vânzări implicită este setată din înregistrarea clientului sau a contului și poate fi schimbată atunci când este creată oferta. Cu toate acestea, moneda de vânzare nu poate fi schimbată după ce cotația este salvată. Listele de prețuri implicite pentru produse și proiecte sunt stabilite pe baza valuta de vânzare a cotației.

Spre deosebire de costuri, valorile vânzărilor pot fi înregistrate **numai** în moneda vânzărilor.

## <a name="billing-method"></a>Metoda de facturare

Proiectele au, de obicei, modele de contractare cu taxă fixă și bazate pe consum. În Operațiuni de proiect, modelul de contractare al unui proiect este reprezentat de metoda de facturare. Metoda de facturare are două valori: timp și material și preț fix.

- **Timp și material** – Un model de contractare bazat pe consum, în care fiecare cost suportat este susținut de veniturile corespunzătoare. Pe măsură ce estimați sau suportați mai multe costuri, vânzările corespunzătoare estimate și reale cresc, de asemenea. Puteți specifica limite care nu trebuie depășite pentru liniile de ofertă care au această metodă de facturare. În acest fel, puteți limita veniturile reale. Venitul estimat nu este afectat de limitele de a nu depăși.
- **Preț fix** – Un model de contractare cu taxă fixă în care valorile vânzărilor sunt independente de costurile suportate. Valoarea vânzărilor este fixă și nu se modifică pe măsură ce estimați sau suportați mai multe costuri.

## <a name="project-price-lists"></a>Liste de prețuri pentru proiecte

Listele de prețuri ale proiectelor sunt liste de prețuri care sunt folosite pentru a introduce prețuri implicite, nu rate de cost, pentru timp, cheltuieli și alte componente legate de proiect. Pot exista mai multe liste de prețuri și fiecare listă poate avea propria eficacitate a datei pentru fiecare ofertă de proiect. Operațiunile de proiect nu acceptă suprapunerea datei de intrare în vigoare pentru listele de prețuri ale proiectelor.

## <a name="product-price-lists"></a>Liste de prețuri pentru produse

Listele de prețuri pentru produse sunt liste de prețuri care sunt utilizate pentru a introduce prețuri implicite, nu rate de cost, pentru liniile bazate pe produse dintr-o ofertă. Există o singură listă de prețuri pentru produse pe ofertă.

## <a name="transaction-classes"></a>Clase de tranzacții

Project Operations acceptă patru tipuri de clase de tranzacții:

- Timp
- Cheltuială
- Material
- Taxă

Costurile și valorile vânzărilor pot fi estimate și suportate pe **Timp**, **Cheltuieli** și **Material** clase de tranzacții. **Taxa** este o clasă de tranzacții numai cu venituri.

## <a name="work-entities-and-billing-entities"></a>Entități de muncă și entități de facturare

Proiectele și Sarcinile sunt entități care reprezintă munca. Liniile de cotație și liniile Contract sunt entități care reprezintă facturarea. Puteți lega diferite entități de lucru la opțiunile de facturare asociindu-le cu linii de cotație sau linii de contract.

## <a name="multi-customer-deals"></a>Oferte multi-clienți

Ofertele cu mai mulți clienți apar atunci când există mai mult de un client pe factură. Iată câteva exemple tipice:

- **Întreprinderile producătorilor de echipamente originale (OEM) și partenerii acestora** – Partenerii și revânzătorii vând un produs care include servicii cu valoare adăugată. În timpul unei tranzacții cu un client, OEM-ul oferă de obicei să finanțeze o parte a proiectului.
- **Proiecte din sectorul public** – Mai multe departamente ale unei administrații locale sunt de acord să finanțeze un proiect și sunt facturate conform unei împărțiri convenite anterior. De exemplu, un district școlar și orașul sau departamentul guvernamental local sunt de acord să finanțeze construirea unei piscine.

## <a name="invoice-schedules"></a>Planificări factură

Programele de facturare sunt specifice fiecărei linii de cotație și sunt opționale. Programele de facturare sunt create pe baza unor date de început și de încheiere specifice și a unei frecvențe de facturare. Acestea sunt utilizate în timpul etapei contractului, când este configurat procesul de creare automată a facturilor. În timpul etapei de ofertă, graficele de facturare sunt opționale. Dacă sunt create în timpul etapei de ofertă, sunt copiate în contractul de proiect care este creat atunci când o ofertă de proiect este câștigată.

## <a name="differences-from-dynamics-365-sales-quotes"></a>Diferențele față de ofertele Dynamics 365 Sales

Cotațiile pentru operațiuni de proiect sunt construite pe cotațiile Dynamics 365 Sales. Cu toate acestea, există câteva diferențe importante în funcționalitate pe care ar trebui să le cunoașteți:

- Cotațiile Project Operations au două tipuri diferite de linii: una pentru proiecte și una pentru produse.
- Cotațiile pentru operațiuni de proiect au propriile elemente de pagină și interfață cu utilizatorul (UI), reguli de afaceri, logica de afaceri în plug-in-uri și scripturi la nivelul clientului care le fac distincte de ofertele de vânzări.
- În Vânzări, puteți atașa mai multe comenzi la o singură ofertă de vânzare. În Operațiuni de proiect, puteți atașa un singur contract de proiect la o ofertă de proiect.
- Când câștigați o ofertă de vânzare, oportunitatea aferentă poate rămâne deschisă. După ce se câștigă o ofertă de proiect, oportunitatea corelată este închisă.
- O ofertă de vânzare nu include anumite câmpuri și concepte pe care le include o ofertă de proiect. Câmpurile includ **Unitatea contractantă**, **Managerul de cont** și **Facturare către Nume persoană de contact**.
- Ofertele de vânzare și ofertele de proiect sunt identificate prin câmpul set de opțiuni-based **Tip** . Pentru o ofertă de vânzare, valoarea acestui câmp este **Pe articol**. Pentru o ofertă de proiect, valoarea este **Bazată pe muncă**.

Din cauza acestor diferențe, nu vă recomandăm să utilizați cotațiile de vânzări și ofertele de operațiuni de proiect în mod interschimbabil.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
