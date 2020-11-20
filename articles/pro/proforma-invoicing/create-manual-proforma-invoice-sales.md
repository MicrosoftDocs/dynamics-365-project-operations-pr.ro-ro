---
title: Crearea unei facturi proforma manuale - simplificat
description: Acest subiect furnizează informații despre crearea unei facturi proforma manuale în Project Operations.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 87ef090454b2a7ab997e7c21d8d10badc31c8235
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176401"
---
# <a name="create-a-manual-proforma-invoice---lite"></a>Crearea unei facturi proforma manuale - simplificat

_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_

În Dynamics 365 Project Operations, facturile proforma pot fi create manual, după cum este necesar. Puteți crea manual o factură proforma din pagina listei **Contracte de proiect** sau din pagina de detalii **Contract de proiect**.

##  <a name="project-contracts-list-page"></a>Pagina listă contracte de proiect

Din pagina de listă **Contracte de proiect**, selectați unul sau mai multe contracte de proiect și creați facturi pentru toate înregistrările selectate.

Sistemul verifică pentru a vedea care dintre contractele de proiect selectate are restanțe **Gata de facturare** înainte de data de astăzi. Din aceste contracte, sistemul creează proiecte de facturi proforma. Dacă un contract de proiect are mai mulți clienți, poate exista o factură creată pentru fiecare client și mai multe facturi pentru fiecare contract de proiect.

Toate facturile de proiect create sunt disponibile pe pagina **Factură fiscală** din secțiunea **Facturare** din zona **Vânzări**.

## <a name="project-contract-details-page"></a>Pagina de detalii contract de proiect

O factură proforma poate fi creată și din pagina de detalii **Contract de proiect**, care creează factura pentru acel contract specific de proiect. Sistemul verifică dacă contractul de proiect are o restanță **Gata de facturare** înainte de data de astăzi. Din aceste contracte, sistemul creează proiecte de facturi proforma pe baza numărului de clienți de pe fiecare linie de contract.

Când este creată o singură factură proforma, se deschide pagina **Factura fiscala**. Dacă există mai multe facturi create pentru acel contract de proiect, atunci pagina listă **Facturi** se deschide pentru a afișa toate facturile create.
