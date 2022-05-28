---
title: Creați și confirmați jurnalele de intrare
description: Acest subiect oferă informații despre cum să creați și să confirmați jurnalele de intrare în Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 8cb768337bc197895a837670f93b99b132c97437
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584243"
---
# <a name="create-and-confirm-entry-journals"></a>Creați și confirmați jurnalele de intrare

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Folosiți jurnalele de intrare pentru a înregistra datele reale direct în Microsoft Dynamics 365 Project Operations. Când utilizați jurnalele de intrare, nu trebuie să introduceți jurnalele de utilizare a timpului, cheltuielilor și materialelor în Operațiuni de proiect.

Un singur jurnal de intrare vă permite să creați mai multe linii de jurnal. Când jurnalul este confirmat, o linie de jurnal de intrare înregistrează valoarea reală pentru următoarele detalii:

- Costul sau venitul, în funcție de tipul tranzacției care a fost selectat.
- Clasa de tranzacție selectată. Clasele disponibile sunt **Timp**, **·**, **·**, **·**, **de hotar**, și **Impozit**.
- Proiectul și/sau o sarcină care este selectată pe linia jurnalului.

Urmați acești pași pentru a crea un jurnal de intrare în Operațiuni de proiect.

1. Mergi la **Vânzări** \> **Tranzacții** \> **Jurnalele**.
2. Pe **Jurnalele de intrare** pagina cu listă, în panoul de acțiuni, selectați **Nou** pentru a crea un jurnal.
3. Pe **Jurnal nou** pagina, în **Descriere** câmp, introduceți o descriere a jurnalului.
4. Asigurați-vă că **Tipul jurnalului** câmpul este setat la **Intrare**, apoi selectați **salva**. După ce noul jurnal de intrare este salvat, a **Rânduri de jurnal** fila ar trebui să apară pe pagina jurnalului.
5. Pe **Rânduri de jurnal** fila, pe bara de instrumente de deasupra grilei, selectați **Nou** pentru a crea o linie de jurnal de intrare.
6. În **Creare rapidă** caseta de dialog pentru crearea unei linii de jurnal de intrare, setați câmpurile așa cum este descris în tabelul următor.

    | Câmp | Descriere | Impact funcțional |
    | --- | --- | --- |
    | Clasă de tranzacții | Linia jurnalului poate fi clasificată în una dintre cele șase clase de tranzacții: **Timp**, **·**, **·**, **·**, **de hotar**, sau **Impozit**. | The **Impozit** clasa de tranzacție a fost depreciată în Operațiuni de proiect. <br> Dacă creați un **Impozit** clasa de tranzacție, nu va fi procesată prin facturare sau în calcule de costuri sau venituri. **Piatra de hotar** este o clasă de tranzacții numai cu venituri. <br>The **Reținere** clasa de tranzacție reprezintă un avans primit de la un client. Ar trebui să fie întotdeauna creat ca o pereche de linii de jurnal de vânzări facturate și vânzări nefacturate. |
    | Tip de tranzacție | The **Cost**, **Interorg**, și **Costul unitar al resurselor** tipurile de tranzacții ar trebui utilizate pentru a înregistra costul.<br> The **Vânzări nefacturate** și **Vânzări facturate** tipurile de tranzacții ar trebui utilizate pentru a înregistra veniturile. | The **Reținere** clasa de tranzacții funcționează numai cu **Vânzări nefacturate** și **Vânzări facturate** tipuri de tranzacții.<br> The **Piatra de hotar** clasa de tranzacții funcționează numai cu **Vânzări facturate** tipul tranzacției. <br>The **Vânzări Interorg** și **Costul unitar al resurselor** tipurile de tranzacții sunt aplicabile numai pentru **Timp** clasa de tranzacție și acestea sunt disponibile numai în jurnalele de intrare în scenariul de implementare Lite și nu atunci când implementați Operațiuni de proiect în scenariile Resurse/Nestocitate. |
    | Selectare produs | Cand **Material** clasa de tranzacție este selectată, acest câmp vă permite să specificați dacă tranzacția materială pentru care creați linia de jurnal este un produs existent sau un produs înscris. | Dacă selectați **Produs de scriere**, puteți introduce un nume pentru produs. |
    | Produs | O referire la produsul din catalog. | |
    | Descriere | O descriere a liniei jurnalului pentru a facilita identificarea acesteia. | Pentru liniile de jurnal de vânzări nefacturate, valoarea va fi utilizată ca descriere atunci când sunt create detaliile liniei de factură. |
    | Descriere externă | O descriere a liniei jurnalului care poate fi folosită pentru partajarea cu părțile interesate externe. | Pentru liniile de jurnal de vânzări nefacturate, valoarea va fi utilizată ca descriere externă atunci când sunt create detaliile liniei de factură. Poate apărea și pe factura care este trimisă clientului. |
    | Tip de facturare | O valoare care indică dacă linia jurnalului va fi socotită ca componentă taxabilă, gratuită sau netaxabilă a proiectului. | Într-un flux tipic, tipul de facturare este derivat din condițiile convenite care sunt stabilite în contract. Cu toate acestea, atunci când înregistrați o linie de jurnal, puteți introduce o valoare în acest câmp. |
    | Data documentului | Folosiți o dată când a avut loc tranzacția. | |
    | Data inițială | Folosiți data la care a avut loc tranzacția. | Acest câmp este utilizat pentru compararea cu data creării facturii pentru tranzacțiile de la **Vânzări nefacturate** tip. Această comparație vă va ajuta să decideți dacă tranzacția este datată în viitor sau în trecut. Doar tranzacțiile cu date trecute vor fi adăugate pe factură. |
    | Data de sfârșit | Folosiți data la care a avut loc tranzacția. | |
    | Dată contabilitate | Utilizați data la care va fi înregistrat impactul contabil. | |
    | Client linie de contract | În mod implicit, dacă linia de contract are un singur client, acest câmp este setat la clientul de pe linia de contract atunci când linia de jurnal este salvată. Dacă linia de contract are mai mulți clienți, selectați clientul corect pe linia de contract. | Dacă sistemul nu poate determina clientul liniei de contract pe linia jurnalului și dacă este necompletat pe numărul real al **Vânzări nefacturate** tip care este creat din linia jurnalului, efectivul nu va fi facturat. |
    | Project | Selectați proiectul pentru a înregistra actualul. | Pe baza proiectului selectat, a clasei de tranzacție și a sarcinii, sistemul va încerca să determine contractul, linia de contract și clientul liniei de contract. |
    | Activitate | Selectați sarcina pentru a înregistra realitatea. | Dacă ați asociat sarcini cu linii de contract în timpul configurării contractului, sistemul va folosi sarcina selectată, împreună cu un proiect și o clasă de tranzacție, pentru a determina contractul, linia de contract și clientul liniei de contract. |
    | Categorie tranzacție | Selectați categoria tranzacției pentru a înregistra valoarea reală. | Pentru cheltuieli, categoria de tranzacție selectată determină prețul implicit care va fi introdus pe linia jurnalului atunci când este salvat. |
    | Rol | Acest câmp este relevant pentru liniile Jurnalului de timp. Selectați rolul resursei care a petrecut timp pe proiect și/sau sarcină. | Pentru liniile de jurnal de timp, dacă utilizați configurația out-of-box pentru introducerea costurilor implicite de resurse și a ratelor de facturare, rolul selectat este utilizat împreună cu unitatea de resurse pentru a determina prețul implicit care va fi introdus pe linia de jurnal atunci când este salvat. Dacă utilizați o configurație personalizată pentru introducerea prețurilor implicite, ar trebui să revizuiți acea configurație pentru a determina dacă **Rol** câmpul este utilizat pentru a introduce valori implicite ale prețului. |
    | Subcontract | Dacă linia jurnalului reprezintă capacitatea subcontractată sau cheltuielile sau materialele subcontractate, selectați subcontractul relevant. | Când sunt înregistrate linii jurnal de cost, subcontractul selectat va determina lista de prețuri care este utilizată pentru a introduce costul unitar implicit. |
    | Linia de subcontractare | Dacă linia jurnalului reprezintă capacitatea subcontractată sau cheltuielile sau materialele subcontractate, selectați linia de subcontractare relevantă. | Când sunt înregistrate linii jurnal de cost, linia de subcontract selectată se va asigura că calculele de capacitate disponibile pe linia de subcontract sunt corect calculate. |
    | Metodă valoare | În mod implicit, acest câmp este setat la **Înmulțiți cantitatea cu prețul**. Când se utilizează această metodă, suma va fi calculată ca *Cantitate* ×*Preț*. Cealaltă metodă acceptată este **Preț fix**. Când se folosește această metodă, prețul va fi setat la suma, iar cantitatea nu va fi utilizată în calcul. | |
    | Orarul unității și unitatea | Împreună, programul unității și unitatea identifică unitatea cantității. | Combinația dintre unitatea și categoria tranzacției este utilizată pentru a introduce prețuri implicite pentru cheltuieli. În configurația implicită a Operațiunilor de proiect, combinația dintre unitate, rol și unitate de resurse este utilizată pentru a introduce prețuri implicite pentru timp. Dacă aveți o configurație personalizată pentru introducerea prețurilor implicite, aceasta va fi folosită împreună cu unitatea. Combinația dintre produs și unitate este utilizată pentru a introduce prețuri implicite pentru materiale. |
    | Cantitate | Introduceți cantitatea. | |
    | Preț | Dacă prețul este lăsat necompletat atunci când este creată linia jurnalului, valorile relevante vor fi folosite pentru a introduce prețurile implicite, în funcție de clasa tranzacției. Dacă se introduce un preț la crearea liniei de jurnal, acel preț va fi utilizat. | |
    | Taxe | Introduceți orice sumă de impozit. | În funcție de valoarea taxei care este introdusă, suma extinsă va fi calculată ca *Cantitate* + *Impozit*. |

## <a name="confirm-an-entry-journal"></a>Confirmați un jurnal de intrare

După ce ați introdus toate rândurile jurnalului într-un jurnal de intrare, puteți confirma jurnalul. Acest proces va înregistra fiecare linie de jurnal ca date reale pentru proiectele corespunzătoare.

După ce un jurnal este confirmat, nu îl mai puteți edita sau vreuna dintre rândurile acestuia.

## <a name="actuals-created-by-entry-journal-confirmation"></a>Date reale create prin confirmarea jurnalului de intrare

Există câteva diferențe cheie între efectivele care sunt create prin confirmarea jurnalului de intrare și efectivele care sunt create în timpul aprobării jurnalelor de utilizare a timpului, cheltuielilor și materialelor și confirmării facturii în Operațiuni de proiect:

- Jurnalele de intrare nu folosesc conexiuni de tranzacție pentru a lega costul real cu vânzările reale nefacturate. Datele reale care sunt create atunci când jurnalele de utilizare a timpului, cheltuielilor și materialelor sunt aprobate folosesc întotdeauna conexiuni de tranzacție pentru a lega costurile și efectivele de vânzări nefacturate.
- Jurnalele de intrare nu folosesc originile tranzacțiilor pentru a lega costul real și vânzările reale nefacturate la orice înregistrare de origine. Datele reale care sunt create atunci când sunt aprobate jurnalele de utilizare a timpului, cheltuielilor și materialelor folosesc întotdeauna originile tranzacției pentru a lega costurile și vânzările efective nefacturate la intrarea de timp inițială.
- Când sunt facturate efectivele de vânzări nefacturate care sunt create prin confirmarea jurnalului de intrare, efectivele de vânzări facturate care sunt create în timpul confirmării facturii sunt legate de vânzările reale nefacturate, într-un mod similar cu datele reale de vânzări nefacturate care sunt create când Timp, Cheltuieli și Jurnalele de utilizare a materialelor sunt aprobate.
- Liniile de jurnal de intrare care sunt create pentru timpul care este introdus de resursele interorganizaționale nu provoacă valori reale ale **Costul unitar al resurselor** și **Vânzări Interorg** tipuri care urmează să fie create automat. Aceste date reale trebuie create manual. Acest comportament diferă de comportamentul pentru intrările de timp care sunt înregistrate de resursele inter-organizaționale. În acest caz, când ora este aprobată, aplicația creează automat date reale ale **Cost** tastați pe proiectul și datele reale ale **Costul unitar al resurselor** și **Vânzări Interorg** tipuri pe divizia deținătoare a angajatului. Apoi utilizează conexiuni de tranzacție pentru a lega acele date efective împreună și originile tranzacției pentru a le lega la intrarea de timp de origine.
- Când jurnalele de intrare sunt confirmate, ele creează date reale. Cu toate acestea, jurnalele de corecție nu pot fi folosite pentru a corecta acele date reale. Acest comportament diferă de comportamentul pentru datele reale care sunt create atunci când sunt aprobate jurnalele de utilizare a timpului, cheltuielilor și materialelor. În acest caz, aplicația vă permite să utilizați jurnalele de corecție pentru a corecta datele reale pentru a remedia eventualele erori, cu condiția ca acele date reale să nu fi fost încă facturate. Dacă acestea au fost deja facturate, puteți în continuare să corectați un real dacă procesați un credit complet din acel real către client.

> [!NOTE]
> Jurnalele de intrare nu impun reguli stricte implicite. Prin urmare, utilizați aceste Jurnal de intrare cât mai puțin posibil și aveți grijă și aveți grijă pentru a vă asigura că nu creați date financiare corupte în sistemul dvs. Ori de câte ori puteți, utilizați jurnalele de utilizare a timpului, cheltuielilor și materialelor, configurarea jalonului și a reținerii pe contractele de proiect și procesul de confirmare a facturilor de proiect în loc de jurnalele de intrare pentru a crea date reale.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
