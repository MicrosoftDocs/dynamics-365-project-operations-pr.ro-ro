---
title: Facturare furnizori - Concepere și creare
description: Acest articol descrie conceptul de facturi de furnizor, scenarii de utilizare și modul de creare a facturilor de furnizor în Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 38f0760697522b7a5e561cec7d38dfd5c3eaf9fc
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911473"
---
# <a name="vendor-invoicing---concept-and-creation"></a>Facturare furnizori - Concepere și creare

[!include [banner](../../includes/dataverse-preview.md)]

_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_

Facturarea furnizorilor în Microsoft Dynamics 365 Project Operations poate fi folosit pentru a înregistra costurile din livrările de servicii și/sau materiale pe un proiect de către furnizori.

Atunci când serviciile și/sau materialele sunt subcontractate unui furnizor, un subcontract reprezintă acordul contractual cu acel furnizor. Pe măsură ce furnizorul furnizează serviciile sau materialele sunt primite și utilizate pentru sarcinile proiectului, costurile sunt înregistrate în proiect. Periodic, furnizorul trimite facturi care sunt verificate și corelate cu costurile care sunt înregistrate în proiect. După finalizarea procesului de verificare, factura furnizorului este confirmată și eliberată pentru plată.

## <a name="scenarios-for-use"></a>Scenarii de utilizare

Facturile furnizorilor din Operațiunile de proiect pot fi utilizate pentru a susține două scenarii distincte.

### <a name="customers-use-the-full-subcontracting-experiences"></a>Clienții folosesc toate experiențele de subcontractare

Experiențele de facturare a furnizorilor oferă o modalitate de a verifica și de a potrivi intrările de timp, utilizarea materialelor și intrările de cheltuieli care fac referire la componentele subcontractate cu liniile de factură ale furnizorului. Acest proces poate fi utilizat pentru a verifica acuratețea liniilor de factură a furnizorului. După finalizarea procesului de verificare și confirmarea facturii furnizorului, aplicația va inversa valorile reale care au fost înregistrate prin jurnalele aprobate de timp, cheltuieli și utilizare a materialelor și va crea noi valori efective ale costurilor utilizând liniile de factură pentru furnizor.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>Clienții nu folosesc experiențele complete de subcontractare, dar doresc să aibă o vedere unificată a costurilor pe proiecte în Operațiuni de proiect

Dacă urmăriți procesul de subcontractare într-un sistem terță parte, puteți înregistra costurile din acel sistem terță parte către Operațiuni de proiect, creând facturi de furnizor care nu fac referire la subcontracte. În acest fel, managerii dvs. de proiect pot avea o vedere unică și unificată a tuturor costurilor pentru un anumit proiect.

## <a name="creation-of-vendor-invoices-in-project-operations"></a>Crearea facturilor furnizorilor în Operațiuni de proiect

Facturile furnizorilor pot fi create în două moduri:

- Din pagina cu listă de facturi de furnizor sau din pagina de detalii pentru o singură factură de furnizor
- Din pagina cu lista de subcontracte sau din pagina de detalii pentru un singur subcontract

### <a name="creation-from-the-vendor-invoice-list-page-or-details-page"></a>Creare din pagina cu lista facturii furnizorului sau din pagina de detalii

1. Mergi la **Achizitie** \> **Facturi de furnizor**.
2. Pe pagina cu listă de facturi de furnizor sau pe pagina de detalii pentru o singură factură de furnizor, selectați **Nou** pentru a crea o nouă factură de furnizor.

Facturile de furnizor care sunt create în acest fel pot face referire și la un subcontract.

### <a name="creation-from-the-subcontract-list-page-or-details-page"></a>Creare din pagina cu lista de subcontracte sau din pagina de detalii

1. Mergi la **Achizitie** \> **Subcontracte**.
2. Selectați unul sau mai multe subcontracte.
3. Pe pagina cu lista de subcontracte sau pe pagina cu detalii pentru un singur subcontract, selectați **Creați factura de furnizor** pentru a crea o nouă factură de furnizor.

O nouă factură de furnizor în **Proiect** starea este creată pentru fiecare subcontract pe care l-ați selectat.

Facturile de furnizor pe care le creați în acest fel fac întotdeauna referire la subcontractul din antetul facturii de furnizor. Fiecare linie din subcontract care are o metodă de facturare de timp și material va determina crearea unei linii pe factura furnizorului. Fiecare linie din subcontract care are o metodă de facturare cu preț fix va determina crearea unei linii pe factura furnizorului pentru fiecare etapă de linie de subcontractare care are statutul de **Gata de facturare**.

Următoarele câmpuri și înregistrările aferente vor fi copiate din subcontract în antetul facturii furnizorului:

- Furnizor.
- Listele de prețuri aferente vor fi copiate pe factura furnizorului ca liste de prețuri.
- Monedă.
- Unitatea contractantă.
- Termeni de plată.

Pentru liniile de subcontractare Timp și material, următoarele câmpuri și înregistrările aferente vor fi copiate din linia de subcontractare în linia de factură a furnizorului:

- Referințe de linii de subcontractare și subcontractare
- Clasă de tranzacții
- Rol
- Categorie tranzacție
- Câmpurile de produse
- Project
- Activitate
- Resursă ce se poate rezerva

Pentru liniile de subcontractare cu preț fix, următoarele câmpuri vor fi copiate din linia de subcontractare și din linia de referință de subcontractare în linia de factură a furnizorului:

- Referințe de linii de subcontractare și subcontractare.
- Clasa de tranzacții. În mod implicit, valoarea va fi **Piatra de hotar**.
- Numele jalonului și suma vor fi copiate de la etapa aferentă liniei de subcontractare.
- Utilizatorul va putea selecta un proiect și o sarcină pe linia de factură a furnizorului.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
