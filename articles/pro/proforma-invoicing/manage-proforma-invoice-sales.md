---
title: Gestionarea unei facturi proforma - simplificată
description: Acest subiect oferă informații despre lucrul cu facturi proforme.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cd56b99c3ed455848edbd9ff4419afa58d782a3e
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181557"
---
# <a name="manage-a-proforma-invoice---lite"></a>Gestionarea unei facturi proforma - simplificată

_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_

În Operațiunile de proiect Dynamics 365, facturile proforma sunt construite ca o extensie a facturilor în Dynamics 365 Sales. Cu toate acestea, există multe diferențe în procesul de facturare între vânzări și Sales Operations atunci când vine vorba de facturare. De exemplu, nu este posibil să creați o nouă factură din **Lista facturilor** în Project Operations, dar este posibil să faceți acest lucru în Vânzări. Aceste diferențe și extensii sunt în vigoare pentru a sprijini procesele de facturare pentru proiecte care sunt diferite de o factură tipică pentru o comandă de vânzare.

> [!IMPORTANT]
> Din cauza diferențelor, nu utilizați facturi în Vânzări și Project Operations în mod interschimbabil.

## <a name="invoice-header"></a>Antetul facturii

Următoarele informații sunt disponibile pe un antet de factură proforma în Project Operations.

| Câmp | Locație | Descriere | Impactul din aval |
| --- | --- | --- | --- |
| **ID factură** | Fila **Rezumat** | ID-ul care este generat automat când se creează o factură proformă. Un câmp numai pentru citire care este blocat de la editare. | Acest câmp este utilizat ca referință pentru fiecare factură proforma. |
| **Nume** | Fila **Rezumat** | Setați implicit numele contractului de proiect. Acest câmp poate fi editat de utilizator. | &nbsp;  |
| **Monedă** | Fila **Rezumat** | Setați implicit la moneda contractului de proiect. Un câmp numai pentru citire care este blocat de la editare. |&nbsp; |
| **Listă de prețuri** | Fila **Rezumat** | Setați implicit la lista de prețuri a contractului de proiect. Un câmp numai pentru citire care este blocat de la editare. | &nbsp; |
| **Oportunitate** | Fila **Rezumat** | Referința la oportunitatea legată. Un câmp numai pentru citire care este blocat de la editare. | &nbsp;  |
| **Contract** | Fila **Rezumat** | Referința la contractul de proiect legat. Un câmp numai pentru citire care este blocat de la editare. | &nbsp; |
| **Client** | Fila **Rezumat** | Referința la contractul de proiect legat. Un câmp numai pentru citire care este blocat de la editare. |&nbsp;  |
| **Descriere** | Fila **Rezumat** | Câmpul de text care descrie factura. Acest câmp poate fi editat de utilizator. | &nbsp; |
| **Adresa de facturare** și câmpuri conexe | **Fila rezumat** | Valorile implicite sunt stabilite de la clientul contractului de proiect. Acest câmp poate fi editat de utilizator.  | &nbsp; |
| **Stare** | Fila **Rezumat** | Setează următoarele opțiuni: **Activ**, **Închis**, **Plătit** și **Anulat** și poate fi editat de utilizator. | Stările neacceptate pentru Project Operations includ **Închis** și **Anulat**. </br> Starea este setată la **Activ** când se creează factura. </br>Starea ar trebui să fie setată la **Plătit** numai după confirmarea facturii. |
| **Stare factură proiect** | Fila **Rezumat** | Setează următoarele opțiuni **Schiță**, **În curs de revizuire** și **Confirmat** și poate fi editat de utilizator. | În ambele stări, **Schiță** și **În curs de revizuire**, factura poate fi editată. Factura nu poate fi editată după confirmare. |
| **Valoare detaliată** | Fila **Rezumat** | Suma sumelor pe toate liniile de facturare după avansuri și deduceri. Un câmp numai pentru citire care este blocat de la editare. | Acest câmp este utilizat pentru a calcula suma finală. |
| **Discount (%)** | Fila **Rezumat** | Acest câmp poate fi editat pentru a introduce un procent de discount. Acest câmp nu este acceptat de funcționalitatea Project Operations. | Acesta este un câmp neacceptat. |
| **Valoare discount** | Fila **Rezumat** | Acest câmp poate fi editat pentru a introduce procentul de discount. Acest câmp nu este acceptat de funcționalitatea Project Operations. | Acesta este un câmp neacceptat. |
| **Total fără transport** | **Fila rezumat** | Suma totală a facturii după aplicarea reducerilor. Un câmp numai pentru citire care este blocat de la editare. | Acest câmp este utilizat pentru a calcula suma finală. |
| **Valoare taxe de transport** | Fila **Rezumat** | Acest câmp poate fi editat pentru a introduce procentul de taxe de transport. Acest câmp nu este acceptat de funcționalitatea Project Operations. | Acesta este un câmp neacceptat. |
| **Impozit total** | Fila **Rezumat** | Impozitul total din toate liniile de facturare de pe factură. Un câmp numai pentru citire care este blocat de la editare. | Niciunul. |
| **Valoare totală** | Fila **Rezumat** | Suma sumei după reduceri și impozite. | Suma este suma pe care trebuie să o plătească clientul. |
## <a name="project-based-invoice-lines"></a>Linii de factură bazate pe proiect

În Project Operations, există întotdeauna o linie de facturare pentru fiecare linie de contract de proiect. Linia de facturare este creată chiar dacă nu există date reale. Următoarele informații sunt disponibile pe o linie de factură proforma.

| Câmp | Locație | Descriere | Impactul din aval |
| --- | --- | --- | --- |
| **ID factură** | Fila **General** | Referința la ID-ul facturii. Un câmp numai pentru citire care este blocat de la editare. | Linkul la ID factură poate fi utilizată pentru a naviga înapoi la antetul facturii. |
| **Nume** | Fila **General** | Numele liniei de facturare setat implicit din numele liniei de contract. Acest câmp poate fi editat de utilizator. | &nbsp; |
| **Project** | Fila **General** | Proiectul de pe linia contractuală a proiectului aferent. Un câmp numai pentru citire care este blocat de la editare. | Link-ul proiectului poate fi utilizat pentru a naviga la proiect. |
| **Metodă de facturare** | Fila **General** | Metoda de facturare de pe linia contractuală a proiectului aferent. Un câmp numai pentru citire care este blocat de la editare. | &nbsp; |
| **Valoarea liniei de contract** | Fila **General** | Suma de pe contract pe linia de contract a proiectului corelat. Un câmp numai pentru citire care este blocat de la editare. | &nbsp; |
| **Facturat până la data** | Fila **General** | Suma sumelor pe toate detaliile liniei de facturare a acestei facturi. Un câmp numai pentru citire care este blocat de la editare. | &nbsp; |
| **Valoare** | Fila **General** | Suma sumelor pe toate detaliile tarifabile ale liniei de facturare a acestei facturi. Un câmp numai pentru citire care este blocat de la editare. | Acest câmp este utilizat pentru a calcula suma finală pe antetul facturii. |
| **Impozit** | Fila **General** | Suma sumelor de impozite pe toate detaliile liniei de facturare a acestei linie de factură. Un câmp numai pentru citire care este blocat de la editare. | Acest câmp este utilizat pentru a calcula suma finală de impozite pe antetul facturii. |
| **Valoare extinsă** | Fila **General** | Suma sumelor totale (**Impozit + Sume**) pe toate detaliile liniei tarifabile a facturii ale acestei linii de factură. Un câmp numai pentru citire care este blocat de la editare. | Acest câmp este utilizat pentru a calcula suma finală pe antetul facturii. |


## <a name="invoice-line-details"></a>Detalii linie de factură

Fiecare linie de factură dintr-o factură de proiect include detalii despre linia de facturare. Aceste detalii despre linie sunt legate de cifrele reale de vânzare și de etapele de referință care se referă la linia de contract la care face referire linia de facturare. Toate aceste tranzacții sunt marcate **Gata de facturare**.

Pentru linia **Timp și factură de material**, detaliile liniei facturii sunt grupate în **Facturabil**, **Nefacturabil** și **Gratuit** pe pagina **Linie de factură**. Detaliile de **Linie facturabilă de factură** se adaugă la totalul liniei de facturare. **Gratuitate** și **Costuri netarifabile reale** nu se adaugă la totalul liniei de facturare.

Pentru linia **Factură cu preț fix**, detaliile liniei facturii sunt create din repere marcate ca **Gata de facturare** pe linia contractuală corelată. După ce detaliile liniei de facturare sunt create dintr-o etapă de referință, starea de facturare a etapei de actualizare se actualizează la **Factura clientului a fost creată**.

### <a name="edit-invoice-line-details"></a>Editați detaliile liniei de factură

Următoarele câmpuri sunt disponibile pe un deetaliu al liniei de facturare, care sunt susținute de un efectiv de vânzări nefacturate:

| Câmp | Descriere | Impactul din aval |
| --- | --- | --- |
| **Linie de factură** | O referință la **ID linie de factură**. Câmp doar în citire, blocat pentru editare. | Acest link poate fi utilizat pentru a naviga înapoi la antetul facturii. |
| **Descriere** | O descriere a detaliului liniei de factură. Setați implicit din câmpul **Comentarii interne** pe **Intrare de timp** și din câmpul **Descriere** pe **Intrare cheltuieli**. Câmpul poate fi editat de utilizator.| &nbsp; |
| **Descriere externă** | O descriere a detaliului liniei de factură. Setați implicit din câmpul **Comentarii externe** pe **Intrare de timp** și din câmpul **Descriere** pe **Intrare cheltuieli**. Câmpul poate fi editat de utilizator. | Această descriere poate fi utilizată pentru a determina ce ar trebui să fie pe factura tipărită care va fi trimisă clientului. În Project Operations, o factură proforma nu are toate funcționalitățile necesare pentru a configura setările de imprimare pentru o factură. |
| **Dată de început** | Setați implicit din sursa reală. Un câmp numai pentru citire care este blocat de la editare. | Acest câmp poate fi editat pe un nou detaliu al liniei de facturare care nu este susținut de o sursă reală. |
| **Project** | Setați implicit din sursa reală. Un câmp numai pentru citire care este blocat de la editare. | Setați implicit la proiect pe linia de contract corelată. |
| **Sarcină** | Setați implicit din sursa reală. Un câmp numai pentru citire care este blocat de la editare. | Câmulp poate fi editat pe un nou detaliu al liniei de facturare care nu este susținut de o sursă reală. O listă derulantă arată toate sarcinile care sunt asociate liniei contractului de proiect aferent.  |
| **Categorie tranzacție** | Setați implicit din sursa reală. Un câmp numai pentru citire care este blocat de la editare. | Câmpul poate fi editat pe un nou detaliu al liniei de facturare care nu este susținut de o sursă reală. |
| **Rol** | Setați implicit din sursa reală. Un câmp numai pentru citire care este blocat de la editare. | Câmpul poate fi editat pe un nou detaliu al liniei de facturare care nu este susținut de o sursă reală. |
| **Resursă ce se poate rezerva** | Setați implicit din sursa reală. Un câmp numai pentru citire care este blocat de la editare. | Câmpul poate fi editat pe un nou detaliu al liniei de facturare care nu este susținut de o sursă reală. |
| **Unitate de finanțare** | Setați implicit din sursa reală. Un câmp numai pentru citire care este blocat de la editare. | Câmpul poate fi editat pe un nou detaliu al liniei de facturare care nu este susținut de o sursă reală. |
| **Cantitate** | Setați implicit din sursa reală. Un câmp numai pentru citire care este blocat de la editare. | Câmpul poate fi editat pe un nou detaliu al liniei de facturare care nu este susținut de o sursă reală. |
| **Planificare unitate** | Pentru detaliile liniei de facturare pentru timp, aceasta este întotdeauna setată la timp și nu poate fi editată. Pentru cheltuieli, acest lucru este setat implicit din sursa de cheltuieli reale. Un câmp numai pentru citire care este blocat de la editare. | Setați implicit la **Timp** pe un nou detaliu al liniei de facturare care nu este susținut de date reale. |
| **Unitate** | Setați implicit din sursa reală. Un câmp numai pentru citire care este blocat de la editare. | Câmpul poate fi editat pe un nou detaliu al liniei de facturare care nu este susținut de o sursă reală |
| **Preț** | Setați implicit din sursa reală. Un câmp numai pentru citire care este blocat de la editare. | Câmpul poate fi editat pe un nou detaliu al liniei de facturare care nu este susținut de o sursă reală. Dacă nu este introdusă nicio valoare, aceasta este setată implicit după **Salvare**. |
| **Monedă** | Setați implicit din sursa reală. Un câmp numai pentru citire care este blocat de la editare. | Setați în mod implicit din antetul facturii atunci când creați un nou detaliu al facturii, fără sprijin efectiv.  Un câmp numai pentru citire care este blocat de la editare. |
| **Valoare** | Setați implicit din sursa reală. Un câmp numai pentru citire care este blocat de la editare. | Calculat drept **Cantitate \* Preț** atunci când creați un nou detaliu al facturii fără o copie de siguranță reală. Se calculează după **Salvare**. Un câmp numai pentru citire care este blocat de la editare. |
| **Impozit** | Setați implicit din sursa reală. Câmpul poate fi editat de utilizator | Câmpul poate fi editat de utilizator atunci când creează un nou detaliu de linie de factură fără o copie de siguranță reală. |
| **Valoare extinsă** | Un câmp calculat, calculat ca **Sumă + Impozit**. Un câmp numai pentru citire care este blocat de la editare. | &nbsp; |
| **Tip de facturare** | Setați implicit din sursa reală. Câmpul poate fi editat de utilizator. | Selectarea **Taxabil** adaugă linia la totalul liniei de facturare. **Gratuit** și **Neimpozabil** îl va exclude din totalul liniei de facturare. |
| **Tip de tranzacție** | Setați implicit din sursa reală. Un câmp numai pentru citire care este blocat de la editare. | Setați implicit la **Vânzări facturate** și blocat la crearea unui nou **Detaliu linie factură** fără un suport real.  |
| **Clasă de tranzacții** | Setați implicit din sursa reală. Un câmp numai pentru citire care este blocat de la editare. | Setați implicit în funcție de faptul dacă utilizatorul alege să creeze un detaliu de linie de facturare **Timp**, **Cheltuieli**, sau **Taxă** creând în același timp un nou **Detaliu linie factură** fără un suport propriu-zis. Blocat pentru editare. |

Următoarele câmpuri sunt disponibile pe un detaliu al liniei de facturare, care sunt susținute de o etapă:

| Câmp | Descriere | Impactul din aval |
| --- | --- | --- |
| **Linie de factură** | Referință la **ID linie de factură**. Un câmp numai pentru citire care este blocat de la editare. | Linkul poate fi utilizat pentru a naviga înapoi la antetul facturii. |
| **Descriere** | Descrierea detaliului liniei de factură. Setați implicit din descrierea etapei de sursă. | &nbsp; |
|**Descriere externă** | Descrierea detaliilor liniei facturii care este setată implicit din descrierea etapei sursă. | Acest câmp poate fi utilizat pentru a determina ce ar trebui să fie pe factura tipărită care va fi trimisă clientului. O factură proforma din Project Operations nu are toate funcționalitățile necesare pentru a configura setările de imprimare pentru o factură. |
| **Dată de început** | Setați implicit din data **Etapă** la sursa etapei. Un câmp numai pentru citire care este blocat de la editare. | &nbsp; |
| **Project** | Setați implicit din sursa etapei. Un câmp numai pentru citire care este blocat de la editare. | &nbsp; |
| **Sarcină** | Setați implicit din sursa etapei. Un câmp numai pentru citire care este blocat de la editare. | &nbsp; |
| **Categorie tranzacție** | Un câmp numai pentru citire care este blocat de la editare. | &nbsp; |
| **Rol** | Un câmp numai pentru citire care este blocat de la editare. | &nbsp; |
| **Resursă ce se poate rezerva** | Un câmp numai pentru citire care este blocat de la editare. | &nbsp; |
| **Unitate de finanțare** | Un câmp numai pentru citire care este blocat de la editare. | &nbsp; |
| **Planificare unitate** | Un câmp numai pentru citire care este blocat de la editare. | &nbsp; |
| **Unitate** | Un câmp numai pentru citire care este blocat de la editare. | &nbsp; |
| **Preț** | Setați implicit din descrierea sumei de pe etapa de sursă. Un câmp numai pentru citire care este blocat de la editare. | &nbsp; |
| **Monedă** | Setați implicit din sursa etapei. Un câmp numai pentru citire care este blocat de la editare. |&nbsp; |
| **Valoare** | Setați implicit din descrierea sumei de pe etapa de sursă. Un câmp numai pentru citire care este blocat de la editare. | &nbsp; |
| **Impozit** | Setați implicit din descrierea impozitului de pe etapei de sursă. Un câmp numai pentru citire care este blocat de la editare. | &nbsp; |
| **Valoare extinsă** | Setați implicit din descrierea sumei extinse de pe etapa de sursă. Câmpul poate fi editat de utilizator | &nbsp; |
| **Tip de facturare** | Setați întotdeauna în mod implicit la **Facturabil**. Un câmp numai pentru citire care este blocat de la editare. | &nbsp; |
| **Tip de tranzacție** | Setați implicit din sursa etapei. Un câmp numai pentru citire care este blocat de la editare. | &nbsp; |
| **Clasă de tranzacții** | Setați implicit din sursa etapei. Un câmp numai pentru citire care este blocat de la editare. | &nbsp; |

### <a name="create-new-invoice-line-details"></a>Creați noi detaliu de linie de factură

La timp și linii de facturare materiale, puteți crea noi detalii de linie de facturare. Aceste detalii despre linia de facturare nu sunt susținute de un real. Pe linia de facturare a unei linii de facturare de timp și materiale, puteți selecta **Nou** pentru a crea un nou detaliu de linie de facturare pentru clasele de tranzacții care sunt incluse pe linia de contract.

## <a name="refresh-invoice-transactions"></a>Reîmprospătați tranzacțiile de factură

Dacă aveți informații care au venit după crearea facturii, puteți include aceste facturi pe factură.

1. În **Vizualizare restanțe de facturare**, marcați datele ca **Gata de facturare**.   
2. Deschideți proiectul de factură proforma și, pe panglica **Acțiuni**, faceți clic pe **Reîmprospătați tranzacțiile pe linie de factură**.

  Acest lucru creează detalii despre linia de facturare pentru orice date efective care sunt date și marcate ca **Gata de facturare**; dar nu este inclus în factură.

## <a name="product-based-invoice-lines"></a>Linii de factură bazate pe produs

În Project Operations, puteți crea linii de facturare pentru produsele care nu se aplică niciunui proiect sau pentru toate proiectele, împreună cu linii de facturare bazate pe proiect. Aceste linii de facturare sunt create ca linii de contract pe bază de produs și după ce sunt marcate ca fiind gata de facturare, sunt adăugate ca linii de facturare pe bază de produs.

După ce ați adăugat linii de facturare bazate pe produse, acestea nu pot fi modificate. Cu toate acestea, acestea pot fi șterse din schița de factură proforma.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]