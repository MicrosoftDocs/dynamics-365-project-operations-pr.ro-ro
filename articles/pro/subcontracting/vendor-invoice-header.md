---
title: Detaliile din antet pentru facturile de furnizori
description: Acest articol explică funcționalitatea furnizată în antetul facturii furnizorului în Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: d575ebe44e45411e1009c64e9b575777b741322f
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261698"
---
# <a name="header-details-for-vendor-invoices"></a>Detaliile din antet pentru facturile de furnizori

_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_

Acest articol explică funcționalitatea furnizată în antetul facturii furnizorului în Microsoft Dynamics 365 Project Operations.

Pe măsură ce managerii de proiect planifică și execută proiecte, aceștia ar putea angaja subcontractanți și achiziționa produse și servicii de la furnizori. În timpul execuției unui proiect, costurile sunt suportate din serviciile, materialele și categoriile de cheltuieli care sunt achiziționate prin subcontracte cu furnizorii. Furnizorii facturează aceste costuri pentru proiecte prin crearea de facturi pentru furnizor.

Următorul tabel oferă informații despre câmpurile de pe anteturile facturii furnizorului în Project Operations.

| Câmp | Descriere | Impact funcțional |
| --- | --- | --- |
| Nume | Numele facturii furnizorului. | În toate listele derulante de facturi de furnizor, numele facturii de furnizor este listat în prima coloană pentru a vă ajuta să identificați factura furnizorului. În mod implicit, atunci când o factură de furnizor este creată dintr-un subcontract, câmpul **Nume** de pe factura furnizorului este setat la o valoare care constă din numele subcontractului plus data curentă. |
| Descriere | O scurtă descriere a serviciilor și produselor care sunt facturate în factura de furnizor. | Fără |
| Furnizor | Numele companiei care facturează produsele și serviciile. Această companie ar trebui să fie o înregistrare de cont care are un tip de relație de **Vânzător** sau **Furnizor**. | <p>Pe baza furnizorului selectat, valorile implicite sunt introduse automat în următoarele câmpuri:</p><ul><li>Moneda</li><li>Liste de prețuri</li><li>Termeni de plată</li><li>Adresă de plată</li></ul> |
| Subcontract | O referire la subcontractul pentru factura furnizorului. | <p>Pe baza subcontractului selectat, valorile implicite sunt introduse automat în următoarele câmpuri:</p><ul><li>Moneda</li><li>Liste de prețuri</li><li>Termeni de plată</li><li>Adresa de plată</li></ul><p>Subcontractul care este selectat în antetul facturii furnizorului este introdus implicit în liniile facturii furnizorului și nu poate fi modificat acolo.</p> |
| Data facturii | Data pentru costurile reale care vor fi create atunci când factura furnizorului este confirmată. | Data facturii este, de asemenea, utilizată pentru a selecta lista corectă de prețuri de achiziție, fie din listele de prețuri atașate furnizorului aferent, fie din parametrii proiectului. |
| Motiv stare | Starea facturii furnizorului. | <p>Starea determină unde se află factura de furnizor în procesul de afaceri și dacă poate fi editată. Iată unele dintre valorile disponibile:</p><ul><li>**Schiță**: – Factura furnizorului poate fi editată.</li><li>**Confirmat** – Factura furnizorului a fost verificată și confirmată. Facturile furnizorului în această stare nu pot fi editate sau șterse.</li><li>**În procesare** – Factura furnizorului este în curs de revizuire. Facturile furnizorului în această stare pot fi editate, dar nu pot fi șterse.</li><li>**Anulat** – Factura furnizorului a fost anulată. Facturile furnizorului în această stare nu pot fi editate sau șterse.</li></ul> |
| Moneda | Moneda în care vânzătorul facturează pentru produsele și serviciile de pe factura furnizorului. | Pe o factură de furnizor care face referire la un subcontract, moneda subcontractului este introdusă implicit ca monedă a facturii de furnizor. Pe o factură de furnizor care nu face referire la un subcontract, valoarea implicită este introdusă din înregistrarea contului furnizorului și poate fi modificată. După ce o factură de furnizor este salvată, moneda nu mai poate fi editată. |
| Unitate contractantă | Divizia companiei care este responsabilă pentru primirea serviciilor și/sau produselor de la furnizor. | Fără |
| Termeni de plată | Condițiile de plată pentru facturile furnizorului care sunt emise. Valoarea implicită este introdusă automat din contul furnizorului. | Condițiile de plată dintr-un subcontract sunt copiate la toate facturile furnizorului care sunt legate de subcontract. Termenii de plată pot fi actualizați dacă factura furnizorului are statrea de **Schiță**. |
| Adresa de plată | Adresa furnizorului către care trebuie trimise plățile. Valoarea implicită este introdusă automat din contul furnizorului. | Adresa de plată dintr-un subcontract este copiată ca adresă de plată în toate facturile furnizorului care sunt create pentru acel subcontract. Adresa de plată poate fi actualizată dacă factura furnizorului are starea de **Schiță**. |
| Subtotal | Dacă factura furnizorului nu are linii, introduceți subtotalul facturii înainte de impozite. Dacă factura furnizorului are linii, acest câmp este numai în citire. În acest caz, suma afișată este suma subtotală din toate liniile din factura furnizorului. | Fără |
| Impozit total | Dacă factura furnizorului nu are linii, introduceți totalul impozitelor pe subcontract. Dacă factura furnizorului are linii, acest câmp este numai în citire. În acest caz, suma afișată este suma valorilor impozitelor din toate liniile din factura furnizorului. | Fără |
| Valoare totală | Acest câmp calculat arată valoarea totală a facturii furnizorului după includerea taxelor. | Fără |

> [!NOTE]
> Următoarele câmpuri de pe o factură de furnizor nu pot fi modificate după ce este salvată factura de furnizor: **Furnizor**, **Subcontract**, **Valută**, **Unitatea contractantă** și **Termeni de plată**. Dacă sunt necesare modificări ale acestor câmpuri pe o factură de furnizor, trebuie să ștergeți factura de furnizor și să creați o nouă factură de furnizor.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
