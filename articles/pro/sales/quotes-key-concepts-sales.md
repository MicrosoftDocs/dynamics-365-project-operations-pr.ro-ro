---
title: Oferte - concepte cheie - simplificat
description: Acest subiect furnizează informații despre utilizarea ofertelor de proiect în Project Operations.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 279e7dd47d3d61b02227b307a5833ca0bac66f4a774b5ff23cb69aac417e2f0e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/06/2021
ms.locfileid: "7009456"
---
# <a name="concepts-unique-to-project-quotes"></a>Concepte unice pentru ofertele de Proiecte

_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_


Următoarele elemente sunt concepte cheie de care trebuie să fiți conștient înainte de a începe să utilizați ofertele de proiect în Dynamics 365 Project Operations:

## <a name="contracting-unit"></a>Unitate contractantă

Unitatea contractantă reprezintă divizia sau practica care deține livrarea proiectului. Puteți seta costurile resurselor pentru fiecare unitate contractantă. Când specificați costul resursei pentru o resursă în unitatea contractantă, veți putea, de asemenea, să setați rate de cost diferite pentru resursele de la care această unitate contractantă împrumută, sau alte divizii sau practici din cadrul întreprinderii. Acestea sunt denumite prețuri de transfer, împrumuturi de resurse sau prețuri de schimb. Când setați costul împrumutului resurselor de la alte divizii, puteți alege, de asemenea, să configurați aceste rate de cost în moneda diviziei de împrumut.

## <a name="cost-currency"></a>Monedă de cost

Moneda costurilor în Project Operations este moneda în care sunt raportate costurile. Această monedă este derivată din moneda atașată de câmpul **Unitatea contractantă** pe ofertă, contract și proiect. Costurile pot fi înregistrate în orice valută pentru un proiect. Cu toate acestea, există o conversie valutară de la costurile valutare în care au fost înregistrate, la moneda de cost a proiectului.

Datorită faptului că ratele de schimb din platforma CDS nu pot fi eficiente la dată, totalele de pe ecran pentru costuri se pot modifica în timp, dacă actualizați ratele de schimb valutar. Cu toate acestea, costurile înregistrate în baza de date rămân neschimbate deoarece sumele sunt stocate în moneda în care au fost suportate.

## <a name="sales-currency"></a>Monedă de vânzare

Moneda vânzărilor în Project Operations este moneda în care sunt înregistrate și afișate sumele estimate și reale ale vânzărilor. Este, de asemenea, moneda în care clientul este facturat pentru tranzacție. Într-o ofertă de proiect, moneda de vânzări este implicită din înregistrarea clientului sau a contului și poate fi modificată atunci când este creată oferta. După salvarea ofertei, moneda de vânzare nu poate fi schimbată. Listele de prețuri ale produselor și proiectelor sunt implicite în funcție de moneda de vânzare a ofertei.

Spre deosebire de costuri, valorile vânzărilor pot fi înregistrate numai în moneda de vânzări.

## <a name="billing-method"></a>Metoda de facturare

Proiectele au de obicei modele de contractare fixe pe bază de taxe și consum. Aceasta este reprezentată în Operațiuni de proiect ca **Metoda de facturare** și are două valori, timpul și materialul și prețul fix.

- **Timp și material:** Acesta este un model de contract bazat pe consum în care fiecare cost suportat este susținut de venituri corespunzătoare. Pe măsură ce estimați sau suportați mai multe costuri, vânzările corespunzătoare estimate și reale vor crește, de asemenea. Puteți specifica limite care nu trebuie depășite pentru liniile de ofertă care au această metodă de facturare. Acest lucru va limita veniturile reale. Veniturile estimate nu sunt afectate de limitele care nu trebuie depășite.
- **Preț fix:** Acesta este un model de contract cu taxă fixă care indică faptul că valorile vânzărilor vor fi independente de costurile suportate. Valoarea vânzărilor este fixă și nu se modifică pe măsură ce estimați sau suportați mai multe costuri.

## <a name="project-price-lists"></a>Liste de prețuri pentru proiecte

Listele de prețuri ale proiectelor sunt listele de prețuri care sunt folosite la prețuri implicite, nu la costuri, pentru timp, cheltuială și alte componente legate de proiect. Pot exista mai multe liste de prețuri și fiecare listă poate avea propria eficacitate a datei pentru fiecare ofertă de proiect. Eficacitatea datei suprapuse pe listele de prețuri a proiectului nu este acceptată în Project Operations.

## <a name="product-price-lists"></a>Liste de prețuri pentru produse

Listele de prețuri ale produselor sunt liste de prețuri care sunt folosite la prețurile implicite, nu la tarifele de cost, pentru liniile bazate pe produse pe o ofertă. Există o singură listă de prețuri pentru fiecare produs pe ofertă.

## <a name="transaction-classes"></a>Clase de tranzacții

Project Operations acceptă patru tipuri de clase de tranzacții:

- Timp
- Cheltuială
- Material
- Taxă

Costurile și valorile vânzărilor pot fi estimate și suportate în clasele de tranzacții Timp, Cheltuieli și Materiale. Taxa este o clasă de tranzacții numai pentru venituri.

## <a name="work-entities-and-billing-entities"></a>Entități de muncă și entități de facturare

Entitățile care reprezintă munca sunt proiecte și sarcini. Entitățile care reprezintă facturarea sunt liniile de ofertă și liniile de contract. Puteți conecta diferite entități de lucru la opțiunile de facturare, asociindu-le cu liniile ofertă sau contract.

## <a name="multi-customer-deals"></a>Oferte multi-clienți

Se fac tranzacții cu mai mulți clienți atunci când există mai mulți clienți care trebuie să factureze. Exemplele obișnuite includ:

- **Întreprinderi OEM și partenerii lor:** Partenerii și distribuitorii vând un produs cu servicii cu valoare adăugată. Acesta este de obicei un scenariu în care, în timpul unei anumite tranzacții cu un client, OEM-ul se oferă să finanțeze o parte din proiect. 

- **Proiecte din sectorul public:** mai multe departamente ale unei autorități locale sunt de acord să finanțeze un proiect și sunt facturate conform unei împărțiri convenite anterior. De exemplu, un district școlar și orașul sau departamentul guvernamental local sunt de acord să finanțeze construirea unei piscine.

## <a name="invoice-schedules"></a>Planificări factură

Planificările facturilor sunt specifice fiecărei linii de ofertă și sunt, de asemenea, opționale. Planificările facturilor sunt create în funcție de anumite date de început și de terminare și de frecvența facturilor. Planificările facturilor sunt utilizate în etapa contractului atunci când procesul de creare automată a facturilor este configurat. În etapa ofertei, planificările sunt opționale. Când sunt create planuri de facturare în etapa **Ofertă**, acestea sunt copiate în contractul de proiect care este creat atunci când se câștigă o ofertă de proiect.

## <a name="changes-from-dynamics-365-sales-quote"></a>Modificările din oferta Dynamics 365 Sales:

Ofertele Project Operations sunt construite pe ofertele Dynamics 365 Sales. Cu toate acestea, există câteva diferențe importante în funcționalitate pe care ar trebui să le cunoașteți:

- Acțiunile **Revizui** și **Activare** nu sunt acceptate.
- Ofertele Project Operations au două tipuri diferite de linii. Una este pentru proiecte și celalatlă este pentru produse.
- Ofertele Project Operations au propriile lor elemente de formă și de interfață, reguli de afaceri, logică de afaceri în inserturi și scripturi de partea clientului care le fac unice din ofertele de vânzări.

Din aceste motive, nu este recomandat să utilizați în mod interschimbabil o ofertă de vânzări și o ofertă de Project Operations.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
