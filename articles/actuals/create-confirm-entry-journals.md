---
title: Crearea și confirmarea jurnalelor de intrări
description: Acest articol oferă informații despre cum să creați și să confirmați Jurnalele de intrare în Microsoft Dynamics 365 Project Operations.
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
ms.openlocfilehash: 138dccd72607d6515eeeffb066fa485f83eabbec
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912347"
---
# <a name="create-and-confirm-entry-journals"></a>Crearea și confirmarea jurnalelor de intrări

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Utilizați Jurnalele de intrare pentru a înregistra valori reale direct în Microsoft Dynamics 365 Project Operations. Când utilizați Jurnalele de intrare, nu trebuie să introduceți jurnalele de utilizare a timpului, cheltuielilor și materialelor în Project Operations.

Un singur jurnal de intrare vă permite să creați mai multe linii de jurnal. Când jurnalul este confirmat, o Linie de jurnal de intrare înregistrează valoarea reală pentru următoarele detalii:

- Costul sau venitul, în funcție de tipul tranzacției care a fost selectat.
- Clasa de tranzacție selectată. Clasele disponibile sunt **Timp**, **Cheltuială**, **Materiale**, **Avans**, **Jalon** și **Impozit**.
- Proiectul și/sau o sarcină care este selectată pe linia de jurnal.

Urmați acești pași pentru a crea un jurnal de intrare în Project Operations.

1. Accesați **Vânzări** \> **Tranzacții** \> **Jurnale**.
2. Pe pagina listă **Jurnale de intrare**, din Panoul acțiuni, selectați **Nou** pentru a crea un jurnal.
3. Pe pagia **Jurnal nou**, în câmpul **Descriere**, introduceți o descriere a jurnalului.
4. Asigurați-vă că este setat câmpul **Tip de jurnal** la **Intrare** și apoi selectați **Salvați**. După ce noul jurnal de intrare este salvat, fila **Linii de jurnal** ar trebui să apară pe pagina jurnalului.
5. Pe fila **Linii de jurnal**, în bara de instrumente de deasupra grilei, selectați **Nou** pentru a crea o linie de jurnal de intrare.
6. În caseta de dialog **Creare rapidă** pentru crearea unei linii de jurnal de intrare, setați câmpurile așa cum este descris în tabelul următor.

    | Câmp | Descriere | Impact funcțional |
    | --- | --- | --- |
    | Clasă de tranzacții | Linia de jurnal poate fi clasificată într-una dintre cele șase clase de tranzacții: **Timp**, **Cheltuială**, **Materiale**, **Avans**, **Jalon** sau **Impozit**. | Clasa de tranzacție **Impozit** a fost anulată în Project Operations. <br> Dacă creați o clasă de tranzacție **Impozit**, nu va fi procesată prin facturare sau în calcule de costuri sau venituri. **Jalon** este o clasă de tranzacții numai pentru venituri. <br>Clasa de tranzacție **Avans** reprezintă un avans primit de la un client. Trebuie să se creeze întotdeauna ca o pereche de linii de jurnal de vânzări facturate și vânzări nefacturate. |
    | Tip de tranzacție | Tipurile de tranzacții **Cost**, **Vânzări Interorg** și **Costul unitar al resurselor** trebuie utilizate pentru a înregistra costul.<br> Tipurile de tranzacții **Vânzări nefacturate** și **Vânzări facturate** trebuie utilizate pentru a înregistra veniturile. | Clasa de tranzacție **Avans** funcționează numai cu tipurile de tranzacții **Vânzări nefacturate** și **Vânzări facturate**.<br> Clasa de tranzacție **Jalon** funcționează numai cu tipul de tranzacție **Vânzări facturate**. <br>Tipurile de tranzacții **Vânzări Interorg** și **Costul unitar al resurselor** sunt aplicabile numai pentru clasa de tranzacție **Timp** și acestea sunt disponibile numai în jurnalele de intrare în scenariul de implementare Lite și nu atunci când implementați Project Operations în scenariile Resurse/Nestocat. |
    | Selectare produs | Atunci când clasa de tranzacție **Materiale** este selectată, acest câmp vă permite să specificați dacă tranzacția de materiale pentru care creați linia de jurnal este un produs existent sau un produs din afara catalogului. | Dacă selectați un produs **Din afara catalogului**, puteți introduce un nume pentru produs. |
    | Produs | O referință la produsul din catalog. | |
    | Descriere | O descriere a liniei de jurnal pentru a facilita identificarea acesteia. | Pentru liniile de jurnal de vânzări nefacturate, valoarea va fi utilizată ca descriere atunci când sunt create detaliile liniei de facturare. |
    | Descriere externă | O descriere a liniei de jurnal care poate fi folosită pentru partajarea cu părțile interesate externe. | Pentru liniile de jurnal de vânzări nefacturate, valoarea va fi utilizată ca descriere externă atunci când sunt create detaliile liniei de facturare. Aceasta poate apărea și pe factura care este trimisă clientului. |
    | Tip de facturare | O valoare care indică dacă linia de jurnal va fi considerată drept componentă taxabilă, gratuită sau netaxabilă a proiectului. | Într-un flux tipic, tipul de facturare este derivat din condițiile convenite care sunt stabilite în contract. Cu toate acestea, atunci când înregistrați o linie de jurnal, puteți introduce o valoare în acest câmp. |
    | Data documentului | Utilizați o dată la care a avut loc tranzacția. | |
    | Data inițială | Utilizați data la care a avut loc tranzacția. | Acest câmp este utilizat pentru compararea cu data creării facturii pentru tranzacțiile de tipul **Vânzări nefacturate**. Această comparație vă va ajuta să decideți dacă tranzacția este datată în viitor sau în trecut. Doar tranzacțiile cu date trecute vor fi adăugate pe factură. |
    | Data de sfârșit | Utilizați data la care a avut loc tranzacția. | |
    | Dată contabilitate | Utilizați data la care va fi înregistrat impactul contabil. | |
    | Client pentru linia de contract | În mod implicit, dacă linia de contract are un singur client, acest câmp este setat la clientul de pe linia de contract atunci când linia de jurnal este salvată. Dacă linia de contract are mai mulți clienți, selectați clientul corect pe linia de contract. | Dacă sistemul nu poate determina clientul liniei de contract pe linia de jurnal și dacă este necompletat pe valoarea reală de tip **Vânzări nefacturate** care este creată din linia de jurnal, valoarea reală nu va fi facturată. |
    | Project | Selectați proiectul pentru a înregistra valoarea reală. | Pe baza proiectului selectat, a clasei de tranzacție și a sarcinii, sistemul va încerca să determine contractul, linia de contract și clientul liniei de contract. |
    | Activitate | Selectați sarcina pentru a înregistra valoarea reală. | Dacă ați asociat sarcini cu linii de contract în timpul configurării contractului, sistemul va folosi sarcina selectată, împreună cu un proiect și o clasă de tranzacție, pentru a determina contractul, linia de contract și clientul liniei de contract. |
    | Categorie tranzacție | Selectați categoria de tranzacție pentru a înregistra valoarea reală. | Pentru cheltuieli, categoria de tranzacție selectată determină prețul implicit care va fi introdus pe linia de jurnal când este salvat. |
    | Rol | Acest câmp este relevant pentru liniile de jurnal de timp. Selectați rolul resursei care a petrecut timp pe proiect și/sau sarcină. | Pentru liniile de jurnal de timp, dacă utilizați configurația out-of-box pentru introducerea costurilor implicite de resurse și a ratelor de facturare, rolul selectat este utilizat împreună cu unitatea de resurse pentru a determina prețul implicit care va fi introdus pe linia de jurnal atunci când este salvat. Dacă utilizați o configurație personalizată pentru introducerea prețurilor implicite, trebuie să examinați acea configurație pentru a determina dacă câmpul **Rol** este folosit pentru a introduce valorile implicite ale prețului. |
    | Subcontract | Dacă linia de jurnal reprezintă capacitatea subcontractată sau cheltuielile sau materialele subcontractate, selectați subcontractul corespunzător. | Când sunt înregistrate linii de jurnal de cost, subcontractul selectat va determina lista de prețuri care este utilizată pentru a introduce costul unitar implicit. |
    | Linie de subcontractare | Dacă linia de jurnal reprezintă capacitatea subcontractată sau cheltuielile sau materialele subcontractate, selectați linia de subcontractare corespunzătoare. | Când sunt înregistrate linii de jurnal de cost, linia de subcontractare selectată se va asigura că calculele de capacitate disponibile pe linia de subcontractare sunt calculate corect. |
    | Metodă valoare | Implicit, acest câmp este setat la **Înmulțire cantitate cu prețul**. Când se utilizează această metodă, suma va fi calculată ca *Cantitate* × *Preț*. Cealaltă metodă acceptată este **Preț fix**. Când se folosește această metodă, prețul va fi setat la sumă, iar cantitatea nu va fi utilizată în calcul. | |
    | Programul unității și unitatea | Împreună, programul unității și unitatea identifică unitatea cantității. | Combinația de unitate și categorie de tranzacție este utilizată pentru a introduce prețurile implicite pentru cheltuieli. În configurația implicită a Project Operations, combinația dintre unitate, rol și unitate de resurse este utilizată pentru a introduce prețuri implicite pentru timp. Dacă aveți o configurație personalizată pentru introducerea prețurilor implicite, aceasta va fi folosită împreună cu unitatea. Combinația de produs și unitate este utilizată pentru introducerea prețurilor implicite pentru materiale. |
    | Cantitate | Introduceți cantitatea. | |
    | Preț | Dacă prețul este lăsat necompletat atunci când este creată linia de jurnal, valorile corespunzătoare vor fi folosite pentru a introduce prețurile implicite, în funcție de clasa de tranzacție. Dacă se introduce un preț la crearea liniei de jurnal, acel preț va fi utilizat. | |
    | Taxe | Introduceți orice sumă de impozit. | În funcție de valoarea impozitului care este introdusă, suma extinsă va fi calculată ca *Cantitate* + *Impozit*. |

## <a name="confirm-an-entry-journal"></a>Confirmați un jurnal de intrare

După ce ați introdus toate liniile de jurnal într-un jurnal de intrare, puteți confirma jurnalul. Acest proces va înregistra fiecare linie de jurnal ca valori reale pentru proiectele corespunzătoare.

După ce un jurnal este confirmat, nu îl mai puteți edita, precum nici unul dintre rândurile acestuia.

## <a name="actuals-created-by-entry-journal-confirmation"></a>Valori reale create prin confirmarea jurnalului de intrare

Există câteva diferențe cheie între valorile reale care sunt create prin confirmarea jurnalului de intrare și valorile reale care sunt create în timpul aprobării jurnalelor de utilizare pentru Timp, Cheltuială și Materiale și confirmarea facturii în Project Operations:

- Jurnalele de intrare nu folosesc conexiuni de tranzacție pentru a lega costul real la vânzările reale nefacturate. Valorile reale care sunt create atunci când jurnalele de utilizare pentru Timp, Cheltuială și Materiale sunt aprobate folosesc întotdeauna conexiuni de tranzacție pentru a lega costurile și valorile reale pentru vânzări nefacturate.
- Jurnalele de intrare nu folosesc origini de tranzacție pentru a lega costul real și valorile reale pentru vânzările nefacturate la nicio înregistrare inițială. Valorile reale care sunt create atunci când jurnalele de utilizare pentru Timp, Cheltuială și Materiale sunt aprobate folosesc întotdeauna origini de tranzacție pentru a lega costurile și valorile reale pentru vânzări nefacturate la intrarea de timp inițială.
- Când sunt facturate valorile reale pentru vânzări nefacturate care sunt create prin confirmarea jurnalului de intrare, valorile reale pentru vânzări facturate care sunt create în timpul confirmării facturii sunt legate la valorile reale pentru vânzări nefacturate într-un mod similar cu valorile reale pentru vânzări nefacturate care sunt create când jurnalele de utilizare pentru Timp, Cheltuială și Materiale sunt aprobate.
- Liniile de jurnal de intrare care sunt create pentru timpul care este introdus de resursele inter-organizaționale nu generează valori reale de tip **Costul unitar al resurselor** și **Vânzări Interorg** care urmează să fie create automat. Aceste valori reale trebuie create manual. Acest comportament diferă de comportamentul pentru intrările de timp care sunt înregistrate de resursele inter-organizaționale. În acest caz, când timpul este aprobat, aplicația creează automat valori reale de tip **Cost** pe proiectul și valorile reale de tip **Costul unitar al resurselor** și **Vânzări Interorg**, pe divizia deținătoare a angajatului. Apoi, utilizează conexiuni de tranzacție pentru a lega acele valori reale și originile tranzacției pentru a le lega la intrarea de timp inițială.
- Când jurnalele de intrare sunt confirmate, acestea creează valori reale. Cu toate acestea, jurnalele de corecție nu pot fi folosite pentru a corecta acele valori reale. Acest comportament diferă de comportamentul pentru valorile reale care sunt create atunci când sunt aprobate jurnalele de utilizare pentru Timp, Cheltuială și Materiale. În acest caz, aplicația vă permite să utilizați jurnalele de corecție pentru a corecta valorile reale cu scopul de a remedia eventualele erori, cu condiția ca acele valori reale să nu fi fost încă facturate. Dacă acestea au fost deja facturate, încă mai puteți corecta o valoare reală dacă procesați o creditare completă din acea valoare reală către client.

> [!NOTE]
> Jurnalele de intrare nu impun reguli stricte implicite. Prin urmare, utilizați aceste jurnale de intrare cât mai puțin posibil și fiți precauți și atenți pentru a vă asigura că nu creați date financiare corupte în sistemul dvs. Ori de câte ori puteți, utilizați jurnalele de utilizare pentru Timp, Cheltuieli și Materiale, configurarea jalonului și a avansului pe contractele de proiect și procesul de confirmare a facturilor de proiect în loc de jurnalele de intrare pentru a crea valori reale.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
