---
title: Revizuiți jurnalul de așteptare de facturare pe proiecte și contracte de proiect
description: Acest articol oferă informații despre cum se revizuiesc jurnalele de așteptare de timp, cheltuieli și produs și cum se marchează ca fiind pregătite pentru facturare.
author: rumant
ms.custom: ''
ms.author: rumant
ms.date: 03/11/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 833ace7fd6285191f4b023a029286cd36b5de8f4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928907"
---
# <a name="review-the-invoicing-backlog-on-projects-and-project-contracts"></a>Revizuiți jurnalul de așteptare de facturare pe proiecte și contracte de proiect

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Când o tranzacție este gata pentru a avea o factură creată și procesată, tranzacția ar trebui să fie marcată ca **Gata de facturare**. Acest articol descrie tipurile de tranzacții care pot fi create.

## <a name="review-the-time-and-material-billing-backlog"></a>Revizuiți jurnalele de așteptare de facturare timp și materiale

Atunci când o intrare de timp sau cheltuieli este remisă și aprobată pentru un proiect, PSA creează un proiect real. În cazul în care combinația de proiect și clasa de tranzacții sunt mapate la o linie de contract pentru un proiect de timp și materiale, două date reale sunt create atunci când intrarea este aprobată:

- Cost real 
- Vânzări reale nefacturate

Vânzările reale nefacturate reprezintă jurnalul de așteptare de facturare, iar starea lor de facturare trebuie setată la **Gata de facturare**. Când se creează o factură proiect, vânzările reale nefacturate care sunt marcate **Gata de facturare** sunt copiate ca detalii de linie de facturare.

Pentru a revizui jurnalele de așteptare de facturare pentru timp și materiale, accesați **Vânzări** \> **Facturare** \> **Jurnale de așteptare de facturare timp și materiale**. Selectați toate vânzările reale nefacturate care sunt pregătite pentru a fi facturate, apoi selectați **Gata de facturare**. Starea de facturare a acestor date reale este modificată la **Gata de facturare**.

![Jurnal de așteptare pentru facturarea timpului și a materialelor.](media/TMBacklog.png)

## <a name="review-the-product-billing-backlog"></a>Vizualizați jurnalul de așteptare pentru facturarea produselor

În PSA, atunci când un contract de proiect are linii de contract bazate pe produse, aceste linii sunt luate în calcul pentru facturare ori de câte ori se creează o factură pentru contractul de proiect. Orice produs care are linii de contract marcate **gata de facturare** este copiat la factura de proiect ca linii de factură proiect.

Pentru a revizui jurnalele de așteptare facturare pentru produse, accesați **Vânzări** \> **Facturare** \> **Jurnal de așteptare facturare produs**. Selectați toate liniile de contract pe bază de produs care sunt pregătite pentru a fi facturate, apoi selectați **Gata de facturare**. Starea de facturare a acestor linii este modificată la **Gata de facturare**.

![Jurnal de așteptare pentru facturarea produselor.](media/ProductBacklog.png)

## <a name="review-billing-milestones-on-fixed-price-contracts"></a>Revizuiți etapele de facturare pentru contractele cu preț fix

Fiecare linie de contract de proiect care are o metodă de facturare cu preț fix trebuie să definească etapele contractului. Aceste repere ale contractului pot fi facturate numai dacă sunt marcate **Gata de facturare**. 

Pentru a revizui etapele de facturare, accesați **Vânzări** \> **Facturare** \> **Repere preț fix**. Selectați toate reperele care sunt pregătite pentru a fi facturate, apoi selectați **Gata de facturare**. Starea de facturare a acestor repere este modificată la **Gata de facturare**.

![Repere cu preț fix.](media/FPBacklog.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
