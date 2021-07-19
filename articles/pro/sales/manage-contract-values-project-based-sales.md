---
title: Prezentare generală a liniilor de contract bazate pe proiect
description: Acest subiect oferă informații despre lucrul cu linii de contract bazate pe proiect.
author: rumant
ms.date: 10/28/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: 22e8ff927c5ff6c3748a35031e7703e3fcfe0dab
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369931"
---
# <a name="project-based-contract-lines-overview"></a>Prezentare generală a liniilor de contract bazate pe proiect

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Liniile de contract bazate pe proiecte din Dynamics 365 Project Operations sunt concepute pentru a păstra acordurile de estimare și facturare pentru anumite componente ale lucrărilor de proiect într-un angajament. Structura unei linii de contract bazate pe proiect este extinsă pentru estimări de proiect și scenarii de facturare cu următoarele concepte:

- Metoda de facturare
- Mapare de proiect și activități
- Clase de tranzacții incluse
- Limită de nedepășire
- Configurare posibilitate de tarifare
- Estimări utilizând detaliile liniei contractului
- Clienți de linie de contract

Următorul tabel include câmpurile de pe fila **General** a liniilor contractuale bazate pe proiecte care ajută la stabilirea bazei pentru o estimare detaliată și bazată pe aranjamente de facturare pentru lucrările bazate pe proiect.

| Câmp | Descriere | Impactul din aval |
| --- | --- | --- |
| **Nume** | Numele liniei de contract. Aceasta identifică componenta discretă a contractului care este estimată. Pentru un contract de proiect creat dintr-o ofertă, această valoare este copiată dintr-o valoare corespunzătoare a liniei de ofertă bazată pe proiect. | Numele copiat peste linia de facturare a proiectului care este creată din această linie de contract la crearea facturii. |
| **Metodă de facturare** | Pe un contract de proiect creat dintr-o ofertă, această valoare este copiată din câmpul corespunzător pe linia de ofertă. Acesta este un set de opțiuni care reprezintă cele două modele principale de contractare susținute de Project Operations:</br>- **Preț fix**</br>- **Ora și materialul** | Pe baza metodei de facturare a liniei contractuale de referință, tranzacția efectivă va fi procesată. Dacă linia contractuală la care se face referire prin real are o metodă de facturare a timpului și a materialelor, se creează un cost și înregistrări reale ale vânzărilor nefacturate. Dacă linia contractuală la care se face referire prin actual are o metodă de facturare cu preț fix, se creează doar un cost real. |
| **Project** | Utilizați acest câmp pentru a identifica proiectul care va fi utilizat pentru a realiza lucrările legate de acest angajament. | Această valoare va fi utilizată împreună cu **Sarcini incluse** și **Clase de tranzacții incluse** pentru a rezolva referința liniei de contract pe o înregistrare de linie reală sau estimată. |
| **Activități incluse** | Indică dacă această linie de contract include toate sarcinile proiectului pentru proiectul selectat sau numai un subset de sarcini. Acesta este un set de opțiuni care are următoarele valori posibile:</br>- **Toate activitățile de proiect**</br>- **Numai activități de proiect selectate**. O valoare necompletată în acest câmp este egală cu selectarea **Toate activitățile proiectului**. | Dacă este selectat **Numai activități selectate**, puteți selecta anumite sarcini și le puteți asocia la această linie contractuală pe fila **Configurarea facturării sarcinilor** de pe pagina **Proiect**. Valoarea va fi utilizată împreună cu **Proiect** și clase de **Tranzacții incluse** pentru a rezolva referința liniei contractului pe o înregistrare de linie reală sau estimată. |
| **Includeți timpul** | O valoare **Da**/**Nu** indică dacă tranzacțiile de timp sau costurile forței de muncă pentru proiectul selectat vor fi incluse pe această linie de contract. O valoare **Nu** indică faptul că timpul tranzacțiilor sau costurile forței de muncă nu vor fi incluse pe această linie contractuală. O valoare **Da** indică faptul că vor fi. | Această valoare este utilizată împreună cu proiectul pentru a rezolva referința liniei de contract într-o înregistrare de linie reală sau estimată. |
| **Includeți cheltuielile** | O valoare **Da**/**Nu** indică dacă costurile de cheltuieli pentru proiectul selectat vor fi incluse în această linie de contract. O valoare **Nu** indică faptul că costul de cheltuieli nu vor fi incluse pe această linie contractuală. O valoare **Da** indică faptul că va fi. | Această valoare este utilizată împreună cu proiectul pentru a rezolva referința liniei de contract într-o înregistrare de linie reală sau estimată. |
| **Includere materiale** | O valoare **Da**/**Nu** indică dacă costurile de materiale pentru proiectul selectat vor fi incluse în această linie de contract. O valoare **Nu** indică că costurile cu materiale nu vor fi incluse în această linie de contract. O valoare **Da** indică faptul că va fi. | Această valoare este utilizată împreună cu proiectul pentru a rezolva referința liniei de contract într-o înregistrare de linie reală sau estimată. |
| **Includeți tariful** | O valoare **Da**/**Nu** indică dacă taxele pentru proiectul selectat vor fi incluse în această linie de contract. O valoare **Nu** indică faptul că taxeel nu vor fi incluse pe această linie contractuală. O valoare **Da** indică faptul că vor fi. | Această valoare este utilizată împreună cu proiectul pentru a rezolva referința liniei de contract într-o înregistrare de linie reală sau estimată. |
| **Cantitate contractată** | Pe o linie contractuală cu preț fix, această sumă este valoarea convenită care va fi facturată clientului pentru toate componentele de lucru asociate acestei linii contractuale. Pe o linie de contract de timp și material, această sumă este o valoare estimată a ceea ce va fi facturat clientului pentru toate componentele de lucru asociate acestei linii de contract. Pe un contract de proiect care este creat dintr-o ofertă, această valoare este copiată din câmpul corespunzător pe linia de ofertă. Când o linie de contract bazată pe proiect are detalii despre linie, acest câmp este blocat pentru editare și este rezumat din suma din detaliile liniei de contract. | Când linia contractuală are detalii de linie, această valoare poate fi modificată prin modificarea sumelor din detaliile liniei. Pe o linie contractuală cu preț fix, această valoare este utilizată pentru a genera suma înainte de impozitare pentru etapele de facturare periodice. |
| **Impozit estimat** | Utilizatorul poate edita acest câmp pentru a introduce valoarea taxei estimate pe linia contractului. Când o linie de contract bazată pe proiect are detalii despre linie, acest câmp este blocat pentru editare și este rezumat din suma taxelor din detaliile liniei de contract. | Când linia contractuală are detalii de linie, această valoare poate fi modificată prin modificarea sumelor taxelor din detaliile liniei. Pe o linie contractuală cu preț fix, această valoare este utilizată pentru a genera impozitul pentru etapele de facturare periodice. |
| **Valoare contractată după impozitare** | Suma de pe linia de contract după impozit. Acest câmp este numai în citire și este calculat ca **Suma contractată + impozit**. | Pe o linie contractuală cu preț fix, această valoare este utilizată pentru a genera etapele de facturare periodice. |
| **Limită de nedepășire** | Utilizatorul poate edita acest câmp și este disponibil numai pe linii de contract bazate pe proiecte care au metoda de facturare setată ca timp și materiale. | Utilizatorul poate edita acest câmp. Atunci când o cheltuială de timp sau de material face referire la această linie contractuală în ceea ce privește timpul și materialul, suma reală este evaluată în raport cu limita care nu trebuie depășită pe această linie contractuală. Această evaluare este finalizată după contabilizarea sumelor deja cheltuite și angajate. |
| **Buget client** | Acest câmp este editabil și este copiat din câmpul corespondent pe linia de ofertă, dacă contractul a fost creat dintr-o ofertă. | Acest câmp este utilizat doar pentru informații și nu are nicio semnificație din aval. |

## <a name="validation-rules-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a>Regulile de validare pentru opțiunile din fila General a liniilor contractuale bazate pe proiect

Regula 1: Dacă câmpul **Activități incluse** este necompletat sau setat la **Toate activitățile proiectului**, toate activitățile proiectului sunt incluse pe linia contractului.

Regula 2: Când câmpul **Activități incluse** este necompletat sau setat în mod explicit la **Toate activitățile proiectului**, un proiect și o anumită clasă de tranzacții pot fi incluse numai pe o linie de contract bazată pe proiect a unui contract.

Regula 3: Când câmpul **Activități incluse** este setat la **Doar activități de proiect selectate**, un proiect și o anumită clasă de tranzacție poate fi inclusă pe mai multe linii de contract pe bază de proiect a unui contract.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="43" valign="top">
                <p>
                    <strong>Contract</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Linie contract</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Project</strong>
                </p>
            </td>
            <td width="67" valign="top">
                <p>
                    <strong>Activități incluse</strong>
                </p>
            </td>
            <td width="48" valign="top">
                <p>
                    <strong>Includeți timpul</strong>
                </p>
            </td>
            <td width="48" valign="top">
                <p>
                    <strong>Includeți cheltuielile</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Includere materiale</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Includere</strong>
                </p>
                <p>
                    <strong>Taxă</strong>
                </p>
            </td>
            <td width="53" valign="top">
                <p>
                    <strong>Valid/nu este valid</strong>
                </p>
            </td>
            <td width="250" valign="top">
                <p>
                    <strong>Motiv</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Necompletat </p>
            </td>
            <td width="48" valign="top">
                <p>
Da </p>
            </td>
            <td width="48" valign="top">
                <p>
Da </p>
            </td>
            <td width="42" valign="top">
                <p>
Da </p>
            </td>
            <td width="42" valign="top">
                <p>
Da </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Nu este valid </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Încălcarea regulii #2. Timpul, cheltuielile, materialele și taxele pentru proiectul P1 sunt incluse în ambele linii de ofertă, CL1 și CL2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Necompletat </p>
            </td>
            <td width="48" valign="top">
                <p>
Da </p>
            </td>
            <td width="48" valign="top">
                <p>
Da </p>
            </td>
            <td width="42" valign="top">
                <p>
Da </p>
            </td>
            <td width="42" valign="top">
                <p>
Da </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Necompletat </p>
            </td>
            <td width="48" valign="top">
                <p>
Da </p>
            </td>
            <td width="48" valign="top">
                <p>
No </p>
            </td>
            <td width="42" valign="top">
                <p>
Da </p>
            </td>
            <td width="42" valign="top">
                <p>
Da </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Nu este valid </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Încălcarea regulii #2. Timpul, materialele și taxele pentru proiectul P1 sunt incluse în ambele linii de ofertă, CL1 și CL2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Necompletat </p>
            </td>
            <td width="48" valign="top">
                <p>
Da </p>
            </td>
            <td width="48" valign="top">
                <p>
Da </p>
            </td>
            <td width="42" valign="top">
                <p>
Da </p>
            </td>
            <td width="42" valign="top">
                <p>
Da </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Necompletat </p>
            </td>
            <td width="48" valign="top">
                <p>
Da </p>
            </td>
            <td width="48" valign="top">
                <p>
No </p>
            </td>
            <td width="42" valign="top">
                <p>
Da </p>
            </td>
            <td width="42" valign="top">
                <p>
Da </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Valid </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Timpul, materialele și taxele pentru proiectul P1 sunt incluse pe CL1.
                </p>
                <ul>
                    <li>
Cheltuielile pentru proiectul P1 sunt incluse în CL2.
                    </li>
                </ul>
                <p>
Nicio suprapunere în ceea ce este inclus pe fiecare linie de contract și, prin urmare, este valabilă.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Necompletat </p>
            </td>
            <td width="48" valign="top">
                <p>
No </p>
            </td>
            <td width="48" valign="top">
                <p>
Da </p>
            </td>
            <td width="42" valign="top">
                <p>
No </p>
            </td>
            <td width="42" valign="top">
                <p>
No </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Numai activități selectate </p>
            </td>
            <td width="48" valign="top">
                <p>
Da </p>
            </td>
            <td width="48" valign="top">
                <p>
Da </p>
            </td>
            <td width="42" valign="top">
                <p>
Da </p>
            </td>
            <td width="42" valign="top">
                <p>
Da </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Nu este valid </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Încălcarea regulii #2 </p>
                <p>
C1 include Timp, Materiale, Cheltuieli și Taxe pentru un subset de sarcini din proiectul P1.
                </p>
                <p>
CL2 include timp, materiale, cheltuieli și taxe pentru întregul proiect P1 și, prin urmare, se suprapune cu ceea ce este inclus pe C1.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Necompletat </p>
            </td>
            <td width="48" valign="top">
                <p>
Da </p>
            </td>
            <td width="48" valign="top">
                <p>
Da </p>
            </td>
            <td width="42" valign="top">
                <p>
Da </p>
            </td>
            <td width="42" valign="top">
                <p>
Da </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Numai activități selectate </p>
            </td>
            <td width="48" valign="top">
                <p>
Da </p>
            </td>
            <td width="48" valign="top">
                <p>
Da </p>
            </td>
            <td width="42" valign="top">
                <p>
Da </p>
            </td>
            <td width="42" valign="top">
                <p>
Da </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Valid </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Conform regulii nr. 3 </p>
                <p>
C1 include Timp, Cheltuieli, Materiale, Cheltuieli și Taxe pentru un subset de sarcini din proiectul P1.
                </p>
                <p>
CL2 include Timp, Cheltuieli, Materiale și Taxe pentru un subset de sarcini din proiectul P1.
                </p>
                <p>
Singura validare suplimentară este în jurul subsetului de sarcini de pe CL1, care este diferit de subsetul de sarcini de pe CL2 pentru a se asigura că nu există suprapuneri acolo. Acest lucru este realizat de sistem atunci când sarcinile sunt asociate.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Numai activități selectate </p>
            </td>
            <td width="48" valign="top">
                <p>
Da </p>
            </td>
            <td width="48" valign="top">
                <p>
Da </p>
            </td>
            <td width="42" valign="top">
                <p>
Da </p>
            </td>
            <td width="42" valign="top">
                <p>
Da </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
