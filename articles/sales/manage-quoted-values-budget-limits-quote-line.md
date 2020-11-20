---
title: 'Prezentare generală linii de oferte bazate pe proiect '
description: Acest subiect oferă informații despre utilizarea liniilor de ofertă bazate pe proiecte pentru lucrările de proiect.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ea54d83b1e26d1ee3520dbfab9ba56ffd1191dc9
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181872"
---
# <a name="project-based-quote-lines-overview"></a>Prezentare generală linii de oferte bazate pe proiect 

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

Liniile de ofertă bazate pe proiect sunt concepute pentru a ajuta la estimarea muncii proiectului pe baza unui angajament. Structura unei linii de ofertă bazată pe proiect este extinsă pentru estimările proiectului cu următoarele concepte:

- Metodă de facturare
- Maparea proiectului
- Clase de tranzacții incluse
- Limită de nedepășire
- Configurare posibilitate de tarifare
- Estimare folosind Detaliile liniei de ofertă
- Clienți de linie de ofertă

Următorul tabel oferă informații despre câmpurile de pe fila **General** a liniei de ofertă bazată pe proiect. Aceste câmpuri ajută la stabilirea bazei unei estimări detaliate, fundamentate pentru lucrările de proiect.

| **Câmp** | **Descriere** | **Impactul din aval** |
| --- | --- | --- |
| Nume | Numele liniei de cotație care ar trebui să vă ajute să identificați componenta discretă a cotației care este estimată. | Copiat pe linia contractului de proiect care este creată din această linie de cotație atunci când oferta este câștigată. |
| Metodă de facturare | Pe o ofertă creată dintr-o oportunitate, această valoare este copiată din câmpul corespunzător de pe linia de oportunitate. Acest câmp include cele două modele principale de contractare acceptate de Dynamics 365 Project Operations:</br>- Preț fix</br>- Timp și material.| Această valoare de câmp este copiată pe linia de contract de proiect care este creată din această linie de ofertă atunci când oferta este câștigată. |
| Project | Utilizați acest câmp opțional pentru a identifica proiectul care va fi utilizat pentru a furniza lucrările la acest angajament. Atunci când un proiect este mapat la o linie de ofertă, ajută la configurarea sarcinilor cu taxă și, de asemenea, la introducerea unei estimări bazate pe proiect la linia de estimare ca detalii despre linia de estimare. Atunci când un proiect nu este mapat la o linie de ofertă bazată pe proiect, devizul trebuie creat manual prin crearea fiecărui detaliu al liniei de estimare. | Această valoare de câmp este copiată pe linia de contract de proiect care este creată din această linie de ofertă atunci când oferta este câștigată. |
| Includeți timpul | Un semnalizator **Da**/**Nu** indică dacă tranzacțiile de timp sau costurile forței de muncă pentru proiectul selectat vor fi incluse în estimarea de pe această linie de ofertă. O valoare de semnalizator **Nu** indică faptul că tranzacțiile de timp sau costul cu forța de muncă nu vor fi incluse în estimarea acestei linii de ofertă. O valoare de semnalizator **Da** indică faptul că tranzacțiile de timp sau costul cu forța de muncă vor fi incluse în estimarea acestei linii de ofertă. | Această valoare de câmp este copiată pe linia de contract de proiect care este creată din această linie de ofertă atunci când oferta este câștigată. |
| Includeți cheltuielile | Un semnalizator **Da**/**Nu** indică dacă costurile de cheltuieli pentru proiectul selectat vor fi incluse în estimarea de pe această linie de ofertă. O valoare de semnalizator **Nu** indică faptul că costurile de cheltuieli nu vor fi incluse în estimarea acestei linii de ofertă. O valoare de semnalizator **Da** indică faptul că costurile de cheltuieli vor fi incluse în estimarea acestei linii de ofertă. | Această valoare de câmp este copiată peste linia de contract de proiect care este creată din această linie de ofertă atunci când oferta este câștigată. |
| Includeți tariful | Un semnalizator **Da**/**Nu** indică dacă taxele pentru proiectul selectat vor fi incluse în estimarea de pe această linie de ofertă. O valoare de semnalizator **Nu** indică faptul că taxele nu vor fi incluse în estimarea acestei linii de ofertă. O valoare de semnalizator **Da** indică faptul că taxele vor fi incluse în estimarea acestei linii de ofertă. | Această valoare de câmp este copiată pe linia de contract de proiect care este creată din această linie de ofertă atunci când oferta este câștigată. |
| Valoare cotă | Aceasta este suma care va fi cotată clientului pentru toate lucrările prognozate pe această linie de ofertă bazată pe proiect. Pe o ofertă creată dintr-o oportunitate, această valoare este copiată din câmpul **Buget de client** de pe linia de oportunitate. Când linia de estimare bazată pe proiect are detalii despre linie, acest câmp este blocat pentru editare și este rezumat din suma din detaliile liniei de estimare. | Această valoare de câmp este copiată pe linia de contract de proiect care este creată din această linie de ofertă atunci când oferta este câștigată. |
| Impozit estimat | Acesta este un câmp editabil pentru ca utilizatorul să adauge suma fiscală estimată pe linia de ofertă. Când o linie de estimare bazată pe proiect are detalii despre linie, acest câmp este blocat pentru editare și este rezumat din suma taxelor din detaliile liniei de estimare. | Această valoare de câmp este copiată pe linia de contract de proiect care este creată din această linie de ofertă atunci când oferta este câștigată. |
| Valoare ofertată după taxe | Acest câmp reprezintă suma liniei de cotare după impozitare și este doar în citire. Suma din acest câmp este calculată ca *Suma oferită + Taxe*. | Această valoare de câmp este copiată pe linia de contract de proiect care este creată din această linie de ofertă atunci când oferta este câștigată. |
| Limită de nedepășire | Acest câmp este editabil și este disponibil numai pe liniile de cotație bazate pe proiecte care au o metodă de facturare **Timp și material**. | Această valoare de câmp este copiată pe linia de contract de proiect care este creată din această linie de ofertă atunci când oferta este câștigată. |
| Buget client | Acest câmp se poate edita și este copiat din câmpul corespunzător de pe linia de oportunitate dacă oferta a fost creată dintr-o oportunitate. | Această valoare de câmp este copiată pe linia de contract de proiect care este creată din această linie de ofertă atunci când oferta este câștigată. |

## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a>Reguli de validare pentru câmpurile din fila General a liniilor de ofertă bazate pe proiect

**Regula 1**: O anumită clasă de tranzacție pentru proiectul selectat poate fi inclusă numai pe o singură linie de ofertă bazată pe proiect.

**Regula 2**: Dacă o oportunitate are mai multe ghilimele, pot exista linii de ofertă din oferte diferite care fac referire la același proiect și includ aceeași clasă de tranzacții.

**Regula 3**: Dacă ofertele nu aparțin aceleiași oportunități, nu pot include același proiect și aceeași clasă de tranzacții.

<table border="1" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p>
                    <strong>Oportunitate</strong>
                </p>
            </td>
            <td width="41" valign="top">
                <p>
                    <strong>Ofertă</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Linie de ofertă</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Project</strong>
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
                    <strong>Includere</strong>
                </p>
                <p>
                    <strong>taxă</strong>
                </p>
            </td>
            <td width="54" valign="top">
                <p>
                    <strong>Valid/nu este valid</strong>
                </p>
            </td>
            <td width="308" valign="top">
                <p>
                    <strong>Motiv</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
T1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
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
            <td width="54" rowspan="2" valign="top">
                <p>
Nu este valid </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Încălcarea regulii #1. Timpul, cheltuielile și taxele pentru proiectul P1 sunt incluse pe ambele linii de ofertă, QL1 și QL2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
T1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
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
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
T1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="48" valign="top">
                <p>
Da </p>
            </td>
            <td width="48" valign="top">
                <p>
Nicio </p>
            </td>
            <td width="42" valign="top">
                <p>
Da </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
Nu este valid </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Încălcarea regulii #1. Timpul și taxele pentru proiectul P1 sunt incluse pe ambele linii de ofertă, QL1 și QL2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
T1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
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
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
T1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="48" valign="top">
                <p>
Da </p>
            </td>
            <td width="48" valign="top">
                <p>
Nicio </p>
            </td>
            <td width="42" valign="top">
                <p>
Da </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
Valid </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                 <p>
Timpul și taxele pentru proiectul P1 sunt incluse pe QL1.
Cheltuielile pentru proiectul P1 sunt incluse în QL2.
Nu există o suprapunere în ceea ce este inclus pe fiecare linie de cotare, deci este valabilă.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
T1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="48" valign="top">
                <p>
Nicio </p>
            </td>
            <td width="48" valign="top">
                <p>
Da </p>
            </td>
            <td width="42" valign="top">
                <p>
Nicio </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
T1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
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
            <td width="54" rowspan="2" valign="top">
                <p>
Nu este valid </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Încălcarea regulii #1 de mai sus </p>
                <p>
Q1 include timp, cheltuieli și taxe pentru întregul proiect P1.
                </p>
                <p>
QL2 include timp, cheltuieli și taxe pentru întregul proiect P1 și se suprapune cu ceea ce este inclus în Q1.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
T1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
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
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
T1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
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
            <td width="54" valign="top">
                <p>
Valid </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Pe baza regulii #2, Q1 și Q2 sunt două citate cu aceeași oportunitate, astfel încât ambele pot estima pentru aceleași componente ale unui proiect.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
T2 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 pe Q2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
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
            <td width="54" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
T1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
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
            <td width="54" valign="top">
                <p>
Valid </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Pe baza regulii #3, Q1 și Q2 sunt două citate cu oportunități diferite, astfel încât ambele nu pot estima pentru aceleași componente ale aceluiași proiect.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O2 </p>
            </td>
            <td width="41" valign="top">
                <p>
T1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
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
            <td width="54" valign="top">
                <p>
Nu este valid </p>
            </td>
        </tr>
    </tbody>
</table>

