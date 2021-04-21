---
title: 'Prezentare generală linii de oferte bazate pe proiect '
description: Acest subiect oferă informații despre utilizarea liniilor de ofertă bazate pe proiecte pentru lucrările de proiect.
author: rumant
manager: Annbe
ms.date: 03/30/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cfe98fc89130c93dd0a36af8583881fdcb4550c0
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858713"
---
# <a name="project-based-quote-lines-overview"></a>Prezentare generală a liniilor de oferte bazate pe proiect 

_**Se aplică la:** Implementare Lite - tratarea facturării proforma, Project Operations pentru resurse/scenarii bazate pe altceva decât stocuri_

Liniile de ofertă bazate pe proiect sunt concepute pentru a ajuta la estimarea muncii proiectului pe baza unui angajament. Structura unei linii de ofertă bazată pe proiect este extinsă pentru estimările proiectului cu următoarele concepte:

- Metodă de facturare
- Mapare de proiect și activități
- Clase de tranzacții incluse
- Limită de nedepășire
- Configurare posibilitate de tarifare
- Estimare folosind Detaliile liniei de ofertă
- Clienți de linie de ofertă

Următorul tabel oferă informații despre câmpurile de pe fila **General** a liniei de ofertă bazată pe proiect. Aceste câmpuri ajută la stabilirea bazei unei estimări detaliate, fundamentate pentru lucrările de proiect.

| **Câmp** | **Descriere** | **Impactul din aval** |
| --- | --- | --- |
| Nume | Numele liniei de ofertă care vă ajută să identificați componenta discretă a ofertei care este estimată. | Copiat pe linia contractului de proiect care este creată din această linie de cotație atunci când oferta este câștigată. |
| Metodă de facturare | Pe o ofertă creată dintr-o oportunitate, această valoare este copiată din câmpul corespunzător de pe linia de oportunitate. Acest câmp include cele două modele principale de contractare acceptate de Dynamics 365 Project Operations:</br>- Preț fix</br>- Timp și material.| Această valoare este copiată pe linia contractului de proiect care este creată din această linie de ofertă atunci când este câștigată oferta. |
| Project | Utilizați acest câmp opțional pentru a identifica proiectul care va fi utilizat pentru a furniza lucrările la acest angajament. Atunci când un proiect este mapat la o linie de ofertă, ajută la configurarea sarcinilor cu taxă și, de asemenea, la introducerea unei estimări bazate pe proiect la linia de estimare ca detalii despre linia de estimare. Atunci când un proiect nu este mapat la o linie de ofertă bazată pe proiect, devizul trebuie creat manual prin crearea fiecărui detaliu al liniei de estimare. | Această valoare este copiată pe linia contractului de proiect care este creată din această linie de ofertă atunci când este câștigată oferta.|
| Activități incluse | Indică dacă această linie de cotație este utilizată pentru toate sau unele dintre sarcinile proiectului pentru proiectul selectat. Acest câmp are următoarele valori posibile:</br>- Toate activitățile de proiect</br>- Numai activități de proiect selectate</br>O valoare necompletată în acest câmp este echivalentă cu opțiunea **Toate sarcinile proiectului**. | Când este selectat **Numai sarcini de proiect selectate** pe pagina proiectului, fila **Configurarea activității de facturare** vă permite să selectați sarcini specifice pentru a le asocia la această linie de ofertă. Această valoare este copiată pe linia contractului de proiect care este creată din această linie de ofertă atunci când este câștigată oferta. |
| Includeți timpul | O valoare **Da**/**Nu** indică dacă tranzacțiile de timp sau costurile forței de muncă pentru proiectul selectat vor fi incluse în estimarea de pe această linie de ofertă. O valoare de semnalizator **Nu** indică faptul că tranzacțiile de timp sau costul cu forța de muncă nu vor fi incluse în estimarea acestei linii de ofertă. O valoare de semnalizator **Da** indică faptul că tranzacțiile de timp sau costul cu forța de muncă vor fi incluse în estimarea acestei linii de ofertă. | Această valoare este copiată pe linia contractului de proiect care este creată din această linie de ofertă atunci când este câștigată oferta. |
| Includeți cheltuielile | O valoare **Da**/**Nu** indică dacă costurile de cheltuieli pentru proiectul selectat vor fi incluse în estimarea de pe această linie de ofertă. O valoare de semnalizator **Nu** indică faptul că costurile de cheltuieli nu vor fi incluse în estimarea acestei linii de ofertă. O valoare de semnalizator **Da** indică faptul că costurile de cheltuieli vor fi incluse în estimarea acestei linii de ofertă. | Această valoare este copiată pe linia contractului de proiect care este creată din această linie de ofertă atunci când este câștigată oferta. |
| Includeți materialele | O valoare **Da**/**Nu** indică dacă costurile cu materiale pentru proiectul selectat vor fi incluse în estimarea de pe această linie de ofertă. O valoare **Nu** indică că costurile cu materiale pentru proiectul selectat nu vor fi incluse în estimarea de pe această linie de ofertă. O valoare **Da** indică că costurile cu materiale pentru proiectul selectat vor fi incluse în estimarea de pe această linie de ofertă. | Această valoare este copiată pe linia contractului de proiect care este creată din această linie de ofertă atunci când este câștigată oferta. |
| Includeți tariful | O valoare **Da**/**Nu** indică dacă taxele pentru proiectul selectat vor fi incluse în estimarea de pe această linie de ofertă. O valoare **Nu** indică faptul că taxele nu vor fi incluse în estimarea acestei linii de ofertă. O valoare **Da** indică faptul că taxele vor fi incluse în estimarea acestei linii de ofertă. | Această valoare este copiată pe linia contractului de proiect care este creată din această linie de ofertă atunci când este câștigată oferta. |
| Valoare cotă | Aceasta este suma care va fi oferită clientului pentru toate lucrările prognozate pe această linie de ofertă bazată pe proiect. Pe o ofertă creată dintr-o oportunitate, această valoare este copiată din câmpul **Buget de client** de pe linia de oportunitate. Când linia de estimare bazată pe proiect are detalii despre linie, acest câmp este blocat pentru editare și este rezumat din suma din detaliile liniei de estimare. | Această valoare este copiată pe linia contractului de proiect care este creată din această linie de ofertă atunci când este câștigată oferta. |
| Impozit estimat | Acesta este un câmp editabil pentru ca utilizatorul să adauge suma fiscală estimată pe linia de ofertă. Când o linie de estimare bazată pe proiect are detalii despre linie, acest câmp este blocat pentru editare și este rezumat din suma taxelor din detaliile liniei de estimare. | Această valoare este copiată pe linia contractului de proiect care este creată din această linie de ofertă atunci când este câștigată oferta. |
| Valoare ofertată după taxe | Acest câmp reprezintă suma liniei de cotare după impozitare și este doar în citire. Suma din acest câmp este calculată ca *Suma oferită + Taxe*. | Această valoare este copiată pe linia contractului de proiect care este creată din această linie de ofertă atunci când este câștigată oferta. |
| Limită de nedepășire | Acest câmp este editabil și este disponibil numai pe liniile de cotație bazate pe proiecte care au o metodă de facturare **Timp și material**. | Această valoare este copiată pe linia contractului de proiect care este creată din această linie de ofertă atunci când este câștigată oferta. |
| Buget client | Acest câmp se poate edita și este copiat din câmpul corespunzător de pe linia de oportunitate dacă oferta a fost creată dintr-o oportunitate. | Această valoare este copiată pe linia contractului de proiect care este creată din această linie de ofertă atunci când este câștigată oferta. |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a>Reguli de validare pentru câmpurile din fila General a liniilor de ofertă bazate pe proiect

**Regula 1**: Dacă câmpul **Sarcini incluse** este necompletat sau dacă este setat la **Toate sarcinile proiectului**, un proiect este inclus în linia de ofertă.

**Regula 2**: Dacă câmpul **Sarcini incluse** este necompletat sau dacă este setat la **Toate sarcinile proiectului**, un proiect și o anumită clasă de tranzacții pot fi incluse numai pe o singură linie de ofertă bazată pe proiect.

**Regula 3**: Dacă câmpul **Sarcini incluse** este setat la **Doar activitățile de proiect selectate**, un proiect și o anumită clasă de tranzacții pot fi incluse numai pe o linie de ofertă multiplă bazată pe proiect.

**Regula 4**: Dacă o oportunitate are mai multe ghilimele, pot exista linii de ofertă din oferte diferite care fac referire la același proiect și includ aceeași clasă de tranzacții.

**Regula 5**: Dacă ofertele nu aparțin aceleiași oportunități, nu pot include același proiect și aceeași clasă de tranzacții.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="59" valign="top">
                <p>
                    <strong>Oportunitate</strong>
                </p>
            </td>
            <td width="39" valign="top">
                <p>
                    <strong>Ofertă</strong>
                </p>
            </td>
            <td width="40" valign="top">
                <p>
                    <strong>Linie de ofertă</strong>
                </p>
            </td>
            <td width="41" valign="top">
                <p>
                    <strong>Project</strong>
                </p>
            </td>
            <td width="77" valign="top">
                <p>
                    <strong>Activități incluse</strong>
                </p>
            </td>
            <td width="45" valign="top">
                <p>
                    <strong>Includeți timpul</strong>
                </p>
            </td>
            <td width="46" valign="top">
                <p>
                    <strong>Includeți cheltuielile</strong>
                </p>
            </td>
            <td width="43" valign="top">
                <p>
                    <strong>Includeți materialele</strong>
                </p>
            </td>
            <td width="41" valign="top">
                <p>
                    <strong>Includere</strong>
                </p>
                <p>
                    <strong>Taxă</strong>
                </p>
            </td>
            <td width="49" valign="top">
                <p>
                    <strong>Valid/nu este valid</strong>
                </p>
            </td>
            <td width="200" valign="top">
                <p>
                    <strong>Motiv</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
T1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Necompletat </p>
            </td>
            <td width="45" valign="top">
                <p>
Da </p>
            </td>
            <td width="46" valign="top">
                <p>
Da </p>
            </td>
            <td width="43" valign="top">
                <p>
Da </p>
            </td>
            <td width="41" valign="top">
                <p>
Da </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Nu este valid </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Încălcarea regulii #2. Timpul, cheltuielile și taxele pentru proiectul P1 sunt incluse pe liniile de ofertă, QL1 și QL2 </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
T1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Necompletat </p>
            </td>
            <td width="45" valign="top">
                <p>
Da </p>
            </td>
            <td width="46" valign="top">
                <p>
Da </p>
            </td>
            <td width="43" valign="top">
                <p>
Da </p>
            </td>
            <td width="41" valign="top">
                <p>
Da </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
T1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Necompletat </p>
            </td>
            <td width="45" valign="top">
                <p>
Da </p>
            </td>
            <td width="46" valign="top">
                <p>
No </p>
            </td>
            <td width="43" valign="top">
                <p>
Da </p>
            </td>
            <td width="41" valign="top">
                <p>
Da </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Nu este valid </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Încălcarea regulii #2. Timpul, materialele și taxele pentru proiectul P1 sunt incluse pe liniile de ofertă, QL1 și QL2 </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
T1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Necompletat </p>
            </td>
            <td width="45" valign="top">
                <p>
Da </p>
            </td>
            <td width="46" valign="top">
                <p>
Da </p>
            </td>
            <td width="43" valign="top">
                <p>
Da </p>
            </td>
            <td width="41" valign="top">
                <p>
Da </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
T1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Necompletat </p>
            </td>
            <td width="45" valign="top">
                <p>
Da </p>
            </td>
            <td width="46" valign="top">
                <p>
No </p>
            </td>
            <td width="43" valign="top">
                <p>
Da </p>
            </td>
            <td width="41" valign="top">
                <p>
Da </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Valid </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Timpul, materialele și taxele pentru proiectul P1 sunt incluse pe QL1 <br>
Cheltuielile pentru proiectul P1 sunt incluse în QL2 <br>
Nicio suprapunere în ceea ce este inclus pe fiecare linie de ofertă și, prin urmare, este valabilă.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
T1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Necompletat </p>
            </td>
            <td width="45" valign="top">
                <p>
No </p>
            </td>
            <td width="46" valign="top">
                <p>
Da </p>
            </td>
            <td width="43" valign="top">
                <p>
No </p>
            </td>
            <td width="41" valign="top">
                <p>
No </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
T1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Numai activități selectate </p>
            </td>
            <td width="45" valign="top">
                <p>
Da </p>
            </td>
            <td width="46" valign="top">
                <p>
Da </p>
            </td>
            <td width="43" valign="top">
                <p>
Da </p>
            </td>
            <td width="41" valign="top">
                <p>
Da </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Nu este valid </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Încălcarea regulii #2 </p>
                <p>
Q1 include Timp, Material, Cheltuieli și Taxe pentru un subset de sarcini din proiectul P1 </p>
                <p>
QL2 include timp, cheltuieli și taxe pentru întregul proiect P1 și, prin urmare, se suprapune cu ceea ce este inclus pe Q1.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
T1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Necompletat </p>
            </td>
            <td width="45" valign="top">
                <p>
Da </p>
            </td>
            <td width="46" valign="top">
                <p>
Da </p>
            </td>
            <td width="43" valign="top">
                <p>
Da </p>
            </td>
            <td width="41" valign="top">
                <p>
Da </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
T1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Numai activități selectate </p>
            </td>
            <td width="45" valign="top">
                <p>
Da </p>
            </td>
            <td width="46" valign="top">
                <p>
Da </p>
            </td>
            <td width="43" valign="top">
                <p>
Da </p>
            </td>
            <td width="41" valign="top">
                <p>
Da </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Valid </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Conform regulii nr. 3, </p>
                <p>
Q1 include Timp, Material, Cheltuieli și Taxe pentru un subset de sarcini din proiectul P1.
                </p>
                <p>
QL2 include Timp, Material, Cheltuieli și Taxe pentru un subset de sarcini din proiectul P1.
                </p>
                <p>
Singura validare suplimentară este în jurul subsetului de activități de pe QL1, care este diferit de subsetul de activități de pe QL2 pentru a se asigura că nu există suprapuneri. Acest lucru este realizat de sistem atunci când sarcinile sunt asociate.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
T1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Numai activități selectate </p>
            </td>
            <td width="45" valign="top">
                <p>
Da </p>
            </td>
            <td width="46" valign="top">
                <p>
Da </p>
            </td>
            <td width="43" valign="top">
                <p>
Da </p>
            </td>
            <td width="41" valign="top">
                <p>
Da </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
T1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Toate activitățile de proiect sau necompletat </p>
            </td>
            <td width="45" valign="top">
                <p>
Da </p>
            </td>
            <td width="46" valign="top">
                <p>
Da </p>
            </td>
            <td width="43" valign="top">
                <p>
Da </p>
            </td>
            <td width="41" valign="top">
                <p>
Da </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Valid </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Conform regulii # 5, Q1 și Q2 sunt două oferte cu aceeași oportunitate, deci ambele pot estima pentru aceleași componente ale unui proiect.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
T2 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Toate activitățile de proiect sau necompletat </p>
            </td>
            <td width="45" valign="top">
                <p>
Da </p>
            </td>
            <td width="46" valign="top">
                <p>
Da </p>
            </td>
            <td width="43" valign="top">
                <p>
Da </p>
            </td>
            <td width="41" valign="top">
                <p>
Da </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
T1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Toate activitățile de proiect sau necompletat </p>
            </td>
            <td width="45" valign="top">
                <p>
Da </p>
            </td>
            <td width="46" valign="top">
                <p>
Da </p>
            </td>
            <td width="43" valign="top">
                <p>
Da </p>
            </td>
            <td width="41" valign="top">
                <p>
Da </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Nu este valid </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Conform regulii # 4, Q1 și Q2 sunt două oferte pe oportunități diferite, deci nu pot estima pentru aceleași componente ale aceluiași proiect.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O2 </p>
            </td>
            <td width="39" valign="top">
                <p>
T1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Toate activitățile de proiect sau necompletat </p>
            </td>
            <td width="45" valign="top">
                <p>
Da </p>
            </td>
            <td width="46" valign="top">
                <p>
Da </p>
            </td>
            <td width="43" valign="top">
                <p>
Da </p>
            </td>
            <td width="41" valign="top">
                <p>
Da </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
