---
title: Facturarea unui avans sau unui onorariu
description: Acest subiect furnizează informații despre cum să facturați un onorariu sau un avans în Project Operations.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 12bf3822227badcf8c83d84d6aef6c0fdc7a972a
ms.sourcegitcommit: 250270409412ba4cad95fbd4c345a80d3d2b3e53
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 11/21/2020
ms.locfileid: "4596207"
---
# <a name="invoice-a-retainer-or-an-advance"></a>Facturarea unui avans sau unei garanții

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Dynamics 365 Project Operations acceptă contracte bazate pe onorarii și avansuri unice. Într-un contract de proiect, puteți înregistra un o planificare de onorarii sau un avans unic. Cu toate acestea, înregistrarea la nivelul contractului de proiect nu pune imediat la dispoziție un onorariu sau un avans pentru utilizare. Pentru a utiliza o rețină sau un avans pe o factură care facturează efectiv clientul, onorariul sau avansul trebuie să fie facturate mai întâi.

Parcurgeți pașii următori pentru a factura un onorariu sau un avans.

1. Selectați **Vânzări** > **Facturare** > **Onorarii și avansuri**. 
2. Pe pagina **Avansuri și onorarii**, utilizați filtrul pentru a selecta rețeaua specifică sau avansul pentru a factura și marcați-l ca **Gata de facturare**.
3. Creați o factură fie manual din lista **Contract de proiect** sau pagină de detalii. Deținătorul sau avansul este afișat pe proiectul de factură în secțiunea **Avansuri și onorarii** de pe pagina **Factură**.
4. Confirmați factura. Acest lucru va face dispozitivul de reținere sau avansul disponibil pentru utilizare. Puteți verifica factura pe pagina listei **Onorarii și avansuri**. Pentru un avans sau onorariu facturat, în grilă este afișată suma disponibilă.

## <a name="create-a-retainer-or-advance-from-the-invoice-grid"></a>Creați un onorariu sau avans din grila de facturi

Puteți crea un deținător sau un avans direct pe o factură.

1. Pe un proiect de factură, pe subgrila **Rețele și onorarii** subgrid, selectați **Nou** pentru a crea un nou onorariu sau avans. 
2. Pe pagina **Creare rapidă** pagină, adăugați informațiile necesare, apoi selectați **Salvare**. Onorariul sau avansul este creat pe contractul de proiect aferent facturii. Onorariul sau avansul este marcat automat ca **Gata de facturat** și apoi adăugat la subgrila **Avansuri și onorarii** pe pagina **Factură**.

## <a name="reconcile-an-invoiced-retainer-or-advance"></a>Reconcițiați un avans sau un onorariu facturat

După facturarea unui onorariu sau avans, acestea pot fi utilizate sau reconciliate pe factură cu timp, cheltuieli, repere sau alte taxe bazate pe proiect. Clientul va vedea suma facturii redusă de suma de onorariu sau avans utilizată pe această factură.

Pe fiecare factură generată pentru un contract de proiect care are facturi de onorarii sau avansuri, Project Operation aplică automat onorariul sau avansul pe factură.

Acest lucru poate fi văzut în grila **Onorarii și avansuri aplicate** pe pagina **Factură**. Următorul tabel oferă informații despre câmpurile pe grila **Onorarii și avansuri aplicate** pe pagina **Factură de proiect**.

| Câmp | Locație | Descriere | Impactul din aval |
| --- | --- | --- | --- |
| Descriere | Grila **Onorarii și avansuri aplicate** pe pagina **Factură de proiect** |Acest câmp numai în citire oferă o descriere a onorariului sau avansului utilizat pe această factură. Această valoare nu poate fi modificată pe factură. Această valoare poate fi actualizată pe subgrila de pe pagina **Contract de proiect**. | Acest câmp poate fi afișat clientului pe factura tipărită pentru a indica care onorariu sau avans se aplică pe factură. |
| Livrat la | Grila **Onorarii și avansuri aplicate** pe pagina **Factură de proiect**  | Acest câmp numai în citire oferă o dată de facturare a onorariului sau avansului utilizat pe această factură. Această valoare nu poate fi modificată pe factură. Această valoare poate fi actualizată pe subgrila de pe pagina **Contract de proiect**. | Acest câmp poate fi afișat clientului pe factura tipărită pentru a indica data la care onorariul sau avansul a fost facturat pentru prima oară clientului. |
| Sumă | Grila **Onorarii și avansuri aplicate** pe pagina **Factură de proiect**  | Acest câmp numai în citire oferă suma onorariului sau avansului utilizat pe această factură. Această valoare nu poate fi modificată pe factură. Această valoare poate fi actualizată pe subgrila de pe pagina **Contract de proiect**. | Acest câmp poate fi afișat clientului pe factura tipărită pentru a indica suma originală a onorariului sau avansului care a fost plătit de client. |
| Sumă utilizată | Grila **Onorarii și avansuri aplicate** pe pagina **Factură de proiect**  | Acest câmp de numai citire oferă valoarea calculată care rezumă cât din onorariu sau avans a fost utilizat. | Acest câmp poate fi afișat clientului pe factura tipărită pentru a indica suma din acest onorariu sau avansului care a fost deja utilizat. |
| Valoare extinsă | Grila **Onorarii și avansuri aplicate** pe pagina **Factură de proiect**  | Acest câmp editabil furnizează suma onorariului sau avansului care este utilizat pe această factură de proiect. Această sumă nu poate fi mai mare decât cea disponibilă în avans. Sistemul calculează automat acest lucru ca diferență între câmpurile **Sumă** și **Suma utilizată** de pe grilă. Puteți reduce această sumă pentru a utiliza mai puțin decât ceea ce este disponibil, dar nu puteți crește suma pentru a utiliza mai mult decât ceea ce este disponibil. | Acest câmp poate fi afișat clientului pe factura tipărită pentru a indica suma din acest onorariu sau avansului care era utilizat pe factură. |
| Sumă onorariu sold. | Grila **Onorarii și avansuri aplicate** pe pagina **Factură de proiect**  | Acest câmp numai în citire oferă valoarea cât de mult din onorariu sau avans va rămâne după confirmarea facturii. | Acest câmp poate fi afișat clientului pe factura imprimată pentru a indica suma care va rămâne din acest onorariu sau avans după ce factura este confirmată și plătită. |
