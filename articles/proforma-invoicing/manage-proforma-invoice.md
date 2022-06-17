---
title: Gestionarea unei facturi proforma bazate pe proiect
description: Acest articol oferă informații despre cum să gestionați și să lucrați cu facturile proforma bazate pe proiecte.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 31822947a4fbb60218ce1c3c9415a60491f6d8fa
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932127"
---
# <a name="manage-a-proforma-project-based-invoice"></a>Gestionarea unei facturi proforma bazate pe proiect

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

În Dynamics 365 Project Operations, facturile proforma sunt construite ca o extensie a facturilor din Dynamics 365 Sales. Cu toate acestea, există multe diferențe în procesul de facturare între vânzări și Sales Operations atunci când vine vorba de facturare. De exemplu, nu este posibil să creați o nouă factură din **Lista facturilor** în Project Operations, dar este posibil să faceți acest lucru în Vânzări. Aceste diferențe și extensii sunt în vigoare pentru a sprijini procesele de facturare pentru proiecte care sunt diferite de o factură tipică pentru o comandă de vânzare.

> [!IMPORTANT]
> Din cauza diferențelor, nu utilizați facturi în Vânzări și Project Operations în mod interschimbabil.

## <a name="invoice-header"></a>Antetul facturii

Următoarele informații sunt disponibile pe un antet de factură proforma în Project Operations.

| Câmp | Locație | Descriere |
| --- | --- | --- | 
| **ID factură** | Fila **Rezumat** | ID-ul care este generat automat când se creează o factură proformă. Un câmp numai pentru citire care este blocat de la editare. Acest câmp este utilizat ca referință pentru fiecare factură proforma. |
| **Nume** | Fila **Rezumat** | Setați implicit numele contractului de proiect. Acest câmp poate fi editat. | 
| **Monedă** | Fila **Rezumat** | Setați implicit la moneda contractului de proiect. Un câmp numai pentru citire care este blocat de la editare. |
| **Listă de prețuri** | Fila **Rezumat** | Setați implicit la lista de prețuri a contractului de proiect. Un câmp numai pentru citire care este blocat de la editare. | 
| **Oportunitate** | Fila **Rezumat** | Referința la oportunitatea legată. Un câmp numai pentru citire care este blocat de la editare. | 
| **Contract** | Fila **Rezumat** | Referința la contractul de proiect legat. Un câmp numai pentru citire care este blocat de la editare. | 
| **Client** | Fila **Rezumat** | Referința la contractul de proiect legat. Un câmp numai pentru citire care este blocat de la editare. |
| **Descriere** | Fila **Rezumat** | Câmpul de text care descrie factura. Acest câmp poate fi editat. | 
| **Adresa de facturare** și câmpuri conexe | **Fila rezumat** | Valorile implicite sunt stabilite de la clientul contractului de proiect. Acest câmp poate fi editat.  | 
| **Stare** | Fila **Rezumat** | Setează următoarele opțiuni: **Activ**, **Închis**, **Plătit** și **Anulat** și poate fi editat. Stările neacceptate pentru Project Operations includ **Închis** și **Anulat**. </br> Starea este setată la **Activ** când se creează factura. </br>Starea ar trebui să fie setată la **Plătit** numai după confirmarea facturii.  | 
| **Stare factură proiect** | Fila **Rezumat** | Setează următoarele opțiuni: **Proiect**, **În revizuire** și **Confirmat** și poate fi editat. În ambele stări, **Schiță** și **În curs de revizuire**, factura poate fi editată. Factura nu poate fi editată după confirmare. | 
| **Valoare detaliată** | Fila **Rezumat** | Suma sumelor pe toate liniile de facturare după avansuri și deduceri. Un câmp numai pentru citire care este blocat de la editare.  Acest câmp este utilizat pentru a calcula suma finală. | 
| **Discount (%)** | Fila **Rezumat** | Acest câmp poate fi editat pentru a introduce un procent de discount. Acest câmp nu este acceptat de funcționalitatea Project Operations. Acesta este un câmp neacceptat.|  
| **Valoare discount** | Fila **Rezumat** | Acest câmp poate fi editat pentru a introduce procentul de discount. Acest câmp nu este acceptat de funcționalitatea Project Operations. Acesta este un câmp neacceptat. |  
| **Total fără transport** | **Fila rezumat** | Suma totală a facturii după aplicarea reducerilor. Un câmp numai pentru citire care este blocat de la editare. Acest câmp este utilizat pentru a calcula suma finală.  | 
| **Valoare taxe de transport** | Fila **Rezumat** | Acest câmp poate fi editat pentru a introduce procentul de taxe de transport. Acest câmp nu este acceptat de funcționalitatea Project Operations. Acesta este un câmp neacceptat. |
| **Impozit total** | Fila **Rezumat** | Impozitul total din toate liniile de facturare de pe factură. Un câmp numai pentru citire care este blocat de la editare. | 
| **Sumă totală** | Fila **Rezumat** | Suma sumei după reduceri și impozite. Suma este suma pe care trebuie să o plătească clientul. | 

## <a name="project-based-invoice-lines"></a>Linii de factură bazate pe proiect

În Project Operations, există întotdeauna o linie de facturare pentru fiecare linie de contract de proiect. Linia de facturare este creată chiar dacă nu există date reale. Următoarele informații sunt disponibile pe o linie de factură proforma.

| Câmp | Locație | Descriere | 
| --- | --- | --- |
| **ID factură** | Fila **General** | Referința la ID-ul facturii. Un câmp numai pentru citire care este blocat de la editare. Linkul la ID factură poate fi utilizată pentru a naviga înapoi la antetul facturii. | 
| **Nume** | Fila **General** | Numele liniei de facturare setat implicit din numele liniei de contract. Acest câmp poate fi editat. |
| **Project** | Fila **General** | Proiectul de pe linia contractuală a proiectului aferent. Un câmp numai pentru citire care este blocat de la editare. Link-ul proiectului poate fi utilizat pentru a naviga la proiect. | 
| **Metodă de facturare** | Fila **General** | Metoda de facturare de pe linia contractuală a proiectului aferent. Un câmp numai pentru citire care este blocat de la editare. |
| **Valoarea liniei de contract** | Fila **General** | Suma de pe contract pe linia de contract a proiectului corelat. Un câmp numai pentru citire care este blocat de la editare. | 
| **Facturat până la data** | Fila **General** | Suma sumelor pe toate detaliile liniei de facturare a acestei facturi. Un câmp numai pentru citire care este blocat de la editare. | 
| **Valoare** | Fila **General** | Suma sumelor pe toate detaliile tarifabile ale liniei de facturare a acestei facturi. Un câmp numai pentru citire care este blocat de la editare. Acest câmp este utilizat pentru a calcula suma finală pe antetul facturii. | 
| **Impozit** | Fila **General** | Suma sumelor de impozite pe toate detaliile liniei de facturare a acestei linie de factură. Un câmp numai pentru citire care este blocat de la editare. Acest câmp este utilizat pentru a calcula suma finală de impozite pe antetul facturii. | 
| **Valoare extinsă** | Fila **General** | Suma sumelor totale (**Impozit + Sume**) pe toate detaliile liniei tarifabile a facturii ale acestei linii de factură. Un câmp numai pentru citire care este blocat de la editare. Acest câmp este utilizat pentru a calcula suma finală pe antetul facturii. |

## <a name="invoice-line-details"></a>Detalii linie de factură

Fiecare linie de factură dintr-o factură de proiect include detalii despre linia de facturare. Aceste detalii despre linie sunt legate de cifrele reale de vânzare și de etapele de referință care se referă la linia de contract la care face referire linia de facturare. Toate aceste tranzacții sunt marcate **Gata de facturare**.

Pentru o linie **Factură timp și material**, detaliile liniei de factură sunt grupate în **Taxabil**, **Netaxabil** și **Gratuit** pe pagina **Linie de factură**. Detaliile de **Linie facturabilă de factură** se adaugă la totalul liniei de facturare. **Gratuitate** și **Costuri netarifabile reale** nu se adaugă la totalul liniei de facturare.

Pentru o linie **Factură cu preț fix**, detaliile liniei de factură sunt create din repere marcate ca **Gata de facturare** pe linia contractuală aferentă. După ce detaliile liniei de facturare sunt create dintr-o etapă de referință, starea de facturare a etapei de actualizare se actualizează la **Factura clientului a fost creată**.

### <a name="edit-invoice-line-details"></a>Editați detaliile liniei de factură

Următoarele câmpuri sunt disponibile pe detaliile liniei de facturare, care sunt susținute de un efectiv de vânzări nefacturate.

| Câmp | Descriere |
| --- | --- | 
| **Linie de factură** | O referință la **ID linie de factură**. Acest câmp este doar în citire și este blocat pentru editare. Acest link poate fi utilizat pentru a naviga înapoi la antetul facturii. | 
| **Descriere** | O descriere a detaliului liniei de factură. Setați implicit din câmpul **Comentarii interne** pe **Intrare de timp** și din câmpul **Descriere** pe **Intrare cheltuieli**. Câmpul poate fi editat.| 
| **Descriere externă** | O descriere a detaliului liniei de factură. Setați implicit din câmpul **Comentarii externe** pe **Intrare de timp** și din câmpul **Descriere** pe **Intrare cheltuieli**. Câmpul poate fi editat. Această descriere poate fi utilizată pentru a determina ce ar trebui să fie pe factura tipărită care va fi trimisă clientului. În Project Operations, o factură proforma nu are toate funcționalitățile necesare pentru a configura setările de imprimare pentru o factură. | 
| **Data de început** | Acesta este un câmp doar în citire care este setat implicit din sursa reală. |
| **Project** | Acesta este un câmp de numai citire care este setat implicit de la sursa reală la proiect pe linia contractuală aferentă. |  
| **Activitate** | Setați implicit din sursa reală. Un câmp numai pentru citire care este blocat de la editare. |
| **Categorie tranzacție** | Setați implicit din sursa reală. Un câmp numai pentru citire care este blocat de la editare. | 
| **Rol** | Setați implicit din sursa reală. Un câmp numai pentru citire care este blocat de la editare. |  
| **Resursă ce se poate rezerva** | Setați implicit din sursa reală. Un câmp numai pentru citire care este blocat de la editare. | 
| **Firmă de resurse** | Setați implicit din sursa reală. Un câmp numai pentru citire care este blocat de la editare. | 
| **Unitate de resurse** | Setați implicit din sursa reală. Un câmp numai pentru citire care este blocat de la editare. | 
| **Cantitate** | Setați implicit din sursa reală. Un câmp numai pentru citire care este blocat de la editare. |  
| **Planificare unitate** | Pentru detaliile liniei de facturare pentru timp, aceasta este întotdeauna setată la timp și nu poate fi editată. Pentru cheltuieli, acest lucru este setat implicit din sursa de cheltuieli reale. Un câmp numai pentru citire care este blocat de la editare. | 
| **Unitate** | Setați implicit din sursa reală. Un câmp numai pentru citire care este blocat de la editare. |  
| **Preț** | Setați implicit din sursa reală. Un câmp numai pentru citire care este blocat de la editare. |
| **Monedă** | Setați implicit din sursa reală. Un câmp numai pentru citire care este blocat de la editare. | 
| **Sumă** | Setați implicit din sursa reală. Un câmp numai pentru citire care este blocat de la editare. | 
| **Taxe** | Setați implicit din sursa reală. Câmpul poate fi editat.| 
| **Valoare extinsă** | Un câmp calculat, calculat ca **Sumă + Impozit**. Un câmp numai pentru citire care este blocat de la editare. | 
| **Tip de facturare** | Setați implicit din sursa reală. Câmpul poate fi editat. Selectarea **Taxabil** adaugă linia la totalul liniei de facturare. **Gratuit** și **Neimpozabil** îl va exclude din totalul liniei de facturare.| 
| **Selectare produs** | Setați implicit din sursa reală. Un câmp numai pentru citire care este blocat de la editare. |
| **Produs** | Setați implicit din sursa reală. Un câmp numai pentru citire care este blocat de la editare. | 
| **Nume produs** | Setați implicit din sursa reală. Un câmp numai pentru citire care este blocat de la editare. |  
| **Descriere din afara catalogului** | Setați implicit din sursa reală. Un câmp numai pentru citire care este blocat de la editare. |
| **Tip de tranzacție** | Acesta este un câmp doar în citire care este setat implicit din sursa reală la **Vânzări facturate**. |  
| **Clasă de tranzacții** | Setați implicit din sursa reală. Un câmp numai pentru citire care este blocat de la editare. | 

Următoarele câmpuri sunt disponibile pe un detaliu al liniei de facturare, care sunt susținute de o etapă.

| Câmp | Descriere |
| --- | --- | 
| **Linie de factură** | Referință la **ID linie de factură**. Un câmp numai pentru citire care este blocat de la editare. Linkul poate fi utilizat pentru a naviga înapoi la antetul facturii.  | 
| **Descriere** | Descrierea detaliului liniei de factură. Setați implicit din descrierea etapei de sursă. | 
|**Descriere externă** | Descrierea detaliilor liniei facturii care este setată implicit din descrierea etapei sursă. Acest câmp poate fi utilizat pentru a determina ce ar trebui să fie pe factura tipărită care va fi trimisă clientului. O factură proforma din Project Operations nu are toate funcționalitățile necesare pentru a configura setările de imprimare pentru o factură. | 
| **Dată de început** | Setați implicit din data **Etapă** la sursa etapei. Un câmp numai pentru citire care este blocat de la editare. | 
| **Project** | Setați implicit din sursa etapei. Un câmp numai pentru citire care este blocat de la editare. |
| **Sarcină** | Setați implicit din sursa etapei. Un câmp numai pentru citire care este blocat de la editare. | 
| **Categorie tranzacție** | Un câmp numai pentru citire care este blocat de la editare. |
| **Rol** | Un câmp numai pentru citire care este blocat de la editare. | 
| **Resursă ce se poate rezerva** | Un câmp numai pentru citire care este blocat de la editare. | 
| **Unitate de finanțare** | Un câmp numai pentru citire care este blocat de la editare. | 
| **Planificare unitate** | Un câmp numai pentru citire care este blocat de la editare. | 
| **Unitate** | Un câmp numai pentru citire care este blocat de la editare. | 
| **Preț** | Setați implicit din descrierea sumei de pe etapa de sursă. Un câmp numai pentru citire care este blocat de la editare. |
| **Monedă** | Setați implicit din sursa etapei. Un câmp numai pentru citire care este blocat de la editare. |
| **Valoare** | Setați implicit din descrierea sumei de pe etapa de sursă. Un câmp numai pentru citire care este blocat de la editare. | 
| **Impozit** | Setați implicit din descrierea impozitului de pe etapei de sursă. Un câmp numai pentru citire care este blocat de la editare. |
| **Valoare extinsă** | Setați implicit din descrierea sumei extinse de pe etapa de sursă. Câmpul poate fi editat. | 
| **Tip de facturare** | Setați întotdeauna în mod implicit la **Facturabil**. Un câmp numai pentru citire care este blocat de la editare. |
| **Tip de tranzacție** | Setați implicit din sursa etapei. Un câmp numai pentru citire care este blocat de la editare. | 
| **Clasă de tranzacții** | Setați implicit din sursa etapei. Un câmp numai pentru citire care este blocat de la editare. | 

## <a name="refresh-invoice-transactions"></a>Reîmprospătați tranzacțiile de factură

Dacă aveți informații care au venit după crearea facturii, puteți include aceste facturi pe factură.

1. În **Vizualizare restanțe de facturare**, marcați datele ca **Gata de facturare**.   
2. Deschideți proiectul de factură proforma și, pe panglica **Acțiuni**, selectați **Reîmprospătați tranzacțiile pe linie de factură**.

  Detaliile liniei de factură sunt create pentru orice date reale care sunt datate în trecut și marcate ca **Gata de facturare**, dar nu sunt incluse pe factură.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
