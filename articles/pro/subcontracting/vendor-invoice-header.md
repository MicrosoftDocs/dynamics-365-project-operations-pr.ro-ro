---
title: Detaliile din antet pentru facturile de furnizori
description: Acest articol explică funcționalitatea furnizată în antetul facturii furnizorului în Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 95f84f2d2a357abbd8d507705412a0434b44f658
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929873"
---
# <a name="header-details-for-vendor-invoices"></a>Detaliile din antet pentru facturile de furnizori

[!include [banner](../../includes/dataverse-preview.md)]

_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_

Acest articol explică funcționalitatea furnizată în antetul facturii furnizorului în Microsoft Dynamics 365 Project Operations.

Pe măsură ce managerii de proiect planifică și execută proiecte, aceștia ar putea angaja subcontractanți și pot cumpăra produse și servicii de la furnizori. În timpul execuției unui proiect, costurile sunt suportate din serviciile, materialele și categoriile de cheltuieli care sunt achiziționate prin subcontracte cu furnizorii. Furnizorii facturează aceste costuri proiectelor prin crearea de facturi pentru furnizori.

Următorul tabel oferă informații despre câmpurile din anteturile facturii furnizorului din Operațiuni de proiect.

| Câmp | Descriere | Impact funcțional |
| --- | --- | --- |
| Nume | Numele facturii furnizorului. | În toate listele derulante cu facturile furnizorului, numele facturii furnizorului este listat în prima coloană pentru a vă ajuta să identificați factura furnizorului. În mod implicit, atunci când o factură de furnizor este creată dintr-un subcontract, **Nume** câmpul facturii furnizorului este setat la o valoare care constă din numele subcontractului plus data curentă. |
| Descriere | O scurtă descriere a serviciilor și produselor care sunt facturate pe factura furnizorului. | Fără |
| Furnizor | Numele companiei care facturează produsele și serviciile. Această companie ar trebui să fie o înregistrare de cont care are un tip de relație de **Furnizor** sau **Furnizor**. | <p>În funcție de furnizorul selectat, valorile implicite sunt introduse automat în următoarele câmpuri:</p><ul><li>Moneda</li><li>Liste de prețuri</li><li>Termeni de plată</li><li>Adresa de plata</li></ul> |
| Subcontract | O referire la subcontractul pentru factura furnizorului. | <p>Pe baza subcontractului selectat, valorile implicite sunt introduse automat în următoarele câmpuri:</p><ul><li>Moneda</li><li>Liste de prețuri</li><li>Termeni de plată</li><li>Adresa de plata</li></ul><p>Subcontractul care este selectat în antetul facturii furnizorului este introdus implicit în liniile facturii furnizorului și nu poate fi modificat acolo.</p> |
| Data facturii | Data pentru costurile reale care vor fi create atunci când factura furnizorului este confirmată. | Data facturii este, de asemenea, utilizată pentru a selecta lista corectă de prețuri de achiziție fie din listele de prețuri atașate furnizorului aferent, fie din parametrii proiectului. |
| Motiv stare | Starea facturii furnizorului. | <p>Starea determină locul în care se află factura furnizorului în procesul de afaceri și dacă poate fi editată. Iată câteva dintre valorile disponibile:</p><ul><li>**Proiect** – Factura furnizorului poate fi editată.</li><li>**Confirmat** – Factura furnizorului a fost verificată și confirmată. Facturile furnizorilor în această stare nu pot fi editate sau șterse.</li><li>**In proces** – Factura furnizorului este în curs de revizuire. Facturile furnizorilor în această stare pot fi editate, dar nu pot fi șterse.</li><li>**Anulat** – Factura furnizorului a fost anulată. Facturile furnizorilor în această stare nu pot fi editate sau șterse.</li></ul> |
| Moneda | Moneda în care vânzătorul facturează pentru produsele și serviciile de pe factura furnizorului. | Pe o factură de furnizor care face referire la un subcontract, moneda subcontractului este introdusă implicit ca monedă a facturii de furnizor. Pe o factură de furnizor care nu face referire la un subcontract, valoarea implicită este introdusă din înregistrarea contului de furnizor și poate fi modificată. După ce o factură de furnizor este salvată, moneda nu mai poate fi editată. |
| Unitate contractantă | Divizia companiei care este responsabilă pentru primirea serviciilor și/sau produselor de la furnizor. | Fără |
| Termeni de plată | Condițiile de plată pe facturile de furnizor care sunt emise. Valoarea implicită este introdusă automat din contul furnizorului. | Condițiile de plată dintr-un subcontract sunt copiate pe toate facturile furnizorilor care sunt legate de subcontract. Condițiile de plată pot fi actualizate dacă factura furnizorului are statutul de **Proiect**. |
| Adresa de plata | Adresa furnizorului către care trebuie trimise plățile. Valoarea implicită este introdusă automat din contul furnizorului. | Adresa de plată dintr-un subcontract este copiată ca adresă de plată pe toate facturile furnizorilor care sunt create pentru acel subcontract. Adresa de plată poate fi actualizată dacă factura furnizorului are statutul de **Proiect**. |
| Subtotal | Dacă factura furnizorului nu are rânduri, introduceți subtotalul facturii înainte de taxe. Dacă factura furnizorului are rânduri, acest câmp este numai pentru citire. În acest caz, suma care este afișată este suma subtotală din toate rândurile de pe factura furnizorului. | Fără |
| Impozitul total | Dacă factura furnizorului nu are rânduri, introduceți taxele totale pe subcontract. Dacă factura furnizorului are rânduri, acest câmp este numai pentru citire. În acest caz, suma care este afișată este suma sumelor de taxe din toate rândurile de pe factura furnizorului. | Fără |
| Valoare totală | Acest câmp calculat arată suma totală a facturii furnizorului după includerea taxelor. | Fără |

> [!NOTE]
> Următoarele câmpuri de pe o factură de furnizor nu pot fi modificate după ce este salvată factura de furnizor: **Furnizor**, **·**, **·**, **contractantă**, și **Termeni de plată**. Dacă sunt necesare modificări ale acestor câmpuri pe o factură de furnizor, trebuie să ștergeți factura de furnizor și să creați o nouă factură de furnizor.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
