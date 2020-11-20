---
title: Lucrul cu linii de contract bazate pe proiect
description: Acest subiect oferă informații despre linii de contract bazate pe proiect.
author: rumant
manager: Annbe
ms.date: 10/28/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 14d880eccd5547c122ebe37b63022e64fa2fb6fe
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181736"
---
# <a name="work-with-projectbased-contract-lines"></a>Lucrul cu linii de contract bazate pe proiect

Liniile de contract bazate pe proiecte din Dynamics 365 Project Operations sunt concepute pentru a păstra acordurile de estimare și facturare pentru anumite componente ale lucrărilor de proiect într-un angajament. Structura unei linii de contract bazate pe proiect este extinsă pentru estimări de proiect și scenarii de facturare cu următoarele concepte:

- Metoda de facturare
- Mapare de proiect și activități
- Clase de tranzacții incluse
- Limită de nedepășire
- Configurare posibilitate de tarifare
- Estimări utilizând detaliile liniei contractului
- Clienți de linie de contract

Următoarele câmpuri sunt incluse în fila **General** de linii contractuale bazate pe proiecte. Aceste câmpuri ajută la stabilirea bazei pentru o estimare detaliată, de bază și a modalităților de facturare pentru lucrările bazate pe proiecte.

| Câmp | Descriere | Impactul din aval |
| --- | --- | --- |
| **Nume** | Numele liniei contractuale care identifică componenta discretă a contractului care este estimată. Pentru un contract de proiect creat dintr-o ofertă, această valoare este copiată dintr-o valoare corespunzătoare a liniei de ofertă bazată pe proiect. | Această valoare a câmpului este copiată pe linia de facturare a proiectului care este creată din această linie de contract la crearea facturii. |
| **Metodă de facturare** | Pe un contract de proiect creat dintr-o ofertă, această valoare este copiată din câmpul corespunzător pe linia de ofertă. Acesta este un set de opțiuni care reprezintă cele două modele principale de contractare susținute de Project Operations:</br>- **Preț fix**</br>- **Ora și materialul** | Pe baza metodei de facturare a liniei contractuale de referință, tranzacția efectivă va fi procesată. Dacă linia contractuală la care se face referire prin real are o metodă de facturare a timpului și a materialelor, se creează un cost și o înregistrare reală a vânzărilor nefacturate. Dacă linia contractuală la care se face referire prin actual are o metodă de facturare cu preț fix, se creează doar un cost real. |
| **Project** | Utilizați acest câmp pentru a identifica proiectul care va fi utilizat pentru a realiza lucrările legate de acest angajament. | Valoarea din acest câmp este utilizată împreună cu **Activități incluse** și câmpuri **Clase de tranzacții incluse** pentru a rezolva referința liniei contractului pe o înregistrare de linie reală sau estimată. |
| **Includeți timpul** | Un semnalizator indică dacă tranzacțiile de timp sau costurile forței de muncă pentru proiectul selectat sunt incluse pe această linie de contract. O valoare **Nu** indică faptul că timpul tranzacțiilor sau costurile forței de muncă nu vor fi incluse pe această linie contractuală. O valoare **Da** indică faptul că vor fi. | Această valoare de câmp este utilizată împreună cu proiectul pentru a rezolva referința liniei contractului într-o înregistrare de linie reală sau estimată. |
| **Includeți cheltuielile** | Un semnalizator indică dacă costurile cheltuielilor pentru proiectul selectat vor fi incluse pe această linie de contract. O valoare **Nu** indică faptul că costul de cheltuieli nu vor fi incluse pe această linie contractuală. O valoare **Da** indică faptul că va fi. | Această valoare de câmp este utilizată împreună cu proiectul pentru a rezolva referința liniei contractului într-o înregistrare de linie reală sau estimată. |
| **Includeți tariful** | Un semnalizator indică dacă taxele pentru proiectul selectat vor fi incluse pe această linie de contract. O valoare **Nu** indică faptul că taxeel nu vor fi incluse pe această linie contractuală. O valoare **Da** indică faptul că vor fi. | Această valoare de câmp este utilizată împreună cu proiectul pentru a rezolva referința liniei contractului într-o înregistrare de linie reală sau estimată. |
| **Cantitate contractată** | Pe o linie contractuală cu preț fix, aceasta este valoarea convenită care va fi facturată clientului pentru toate componentele de lucru asociate acestei linii contractuale. Pe o linie de contract de timp și material, această sumă este o valoare estimată a ceea ce va fi facturat clientului pentru toate componentele de lucru asociate acestei linii de contract. Pe un contract de proiect care este creat dintr-o ofertă, această valoare este copiată din câmpul corespunzător pe linia de ofertă. Când o linie de contract bazată pe proiect are detalii despre linie, acest câmp este blocat pentru editare și este rezumat din suma din detaliile liniei de contract. | Când linia contractuală are detalii de linie, această valoare poate fi modificată prin modificarea sumelor din detaliile liniei. Pe o linie contractuală cu preț fix, această valoare este utilizată pentru a genera suma înainte de impozitare pentru etapele de facturare periodice. |
| **Impozit estimat** | Utilizatorul poate edita acest câmp pentru a introduce valoarea taxei estimate pe linia contractului. Când o linie de contract bazată pe proiect are detalii despre linie, acest câmp este blocat pentru editare și este rezumat din suma taxelor din detaliile liniei de contract. | Când linia contractuală are detalii de linie, această valoare poate fi modificată prin modificarea sumelor taxelor din detaliile liniei. Pe o linie contractuală cu preț fix, această valoare este utilizată pentru a genera taxele pentru etapele de facturare periodice. |
| **Valoare contractată după impozitare** | Suma de pe linia de contract după impozit. Acest câmp este numai în citire și este calculat ca **Suma contractată + impozitul**. | Pe o linie contractuală cu preț fix, această valoare este utilizată pentru a genera etapele de facturare periodice. |
| **Limită de nedepășire** | Utilizatorul poate edita acest câmp și este disponibil numai pe linii de contract bazate pe proiecte care au o metodă de facturare a timpului și a materialelor. | Utilizatorul poate edita acest câmp. Atunci când o cheltuială de timp sau cheltuială face referire la această linie contractuală în ceea ce privește timpul și materialul, suma reală este evaluată în raport cu limita care nu trebuie depășită pe această linie contractuală, după contabilizarea sumelor deja cheltuite și angajate. |
| **Buget client** | Acest câmp este editabil și este copiat din câmpul corespondent pe linia de ofertă, dacă contractul a fost creat dintr-o ofertă. | Acest câmp este utilizat doar pentru informații și nu are nicio semnificație din aval. |

## <a name="validation-rule-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a>Regula de validare pentru opțiunile din fila General a liniilor contractuale bazate pe proiect

Regulă: un proiect și o anumită clasă de tranzacții pot fi incluse numai pe o linie de contract bazată pe proiect într-un contract.

| Contract | Linie contract | Project | Includeți timpul | Includeți cheltuielile | Includeți taxa | Valid/nu este valid | Motiv                                                                                                                                                                                                  |
|----------|---------------|---------|--------------|-----------------|-------------|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| C1       | CL1           | P1      | Da          | Da             | Da         | Nu este valid       | Încalcă regula. Timpul, cheltuielile și taxele pentru proiectul P1 sunt incluse pe ambele linii contractuale, CL1 și CL2.                                                                                       |
| C1       | CL2           | P1      | Da          | Da             | Da         | Nu este valid       | Încalcă regula. Timpul, cheltuielile și taxele pentru proiectul P1 sunt incluse pe ambele linii contractuale, CL1 și CL2.                                                                                       |
| C1       | CL1           | P1      | Da          | Nicio              | Da         | Nu este valid       | Încalcă regula. Timpul și taxele pentru proiectul P1 sunt incluse pe ambele linii contractuale, CL1 și CL2.                                                                                                   |
| C1       | CL2           | P1      | Da          | Da             | Da         | Nu este valid       | Încalcă regula. Timpul și taxele pentru proiectul P1 sunt incluse pe ambele linii contractuale, CL1 și CL2.                                                                                                   |
| C1       | CL1           | P1      | Da          | Nicio              | Da         | Valid           | Timpul și taxele pentru proiectul P1 sunt incluse pe CL1. Cheltuielile pentru proiectul P1 sunt incluse în CL2. </br>   Nu există suprapuneri în ceea ce este inclus pe fiecare linie contractuală și, prin urmare, este valabil.  |
| C1       | CL2           | P1      | Nicio           | Da             | Nicio          | Valid           | Timpul și taxele pentru proiectul P1 sunt incluse pe CL1. Cheltuielile pentru proiectul P1 sunt incluse în CL2. </br>   Nu există suprapuneri în ceea ce este inclus pe fiecare linie contractuală și, prin urmare, este valabil.  |
| C1       | CL1           | P1      | Da          | Da             | Da         | Nu este valid       | Încalcă regula. Timpul, cheltuielile și taxele pentru proiectul P1 sunt incluse pe liniile celor două contracte.                                                                                               |
| CL2      | CL2           | P1      | Da          | Da             | Da         | Nu este valid       | Încalcă regula. Timpul, cheltuielile și taxele pentru proiectul P1 sunt incluse pe liniile celor două contracte.                                                                                               |
