---
title: Crearea unei facturi proforma manuale - simplificat
description: Acest subiect furnizează informații despre crearea unei facturi proforma manuale în Project Operations.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 104c2f3f7f0ca0682158d0f7fa0f50a4967e6dd0
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274203"
---
# <a name="create-a-manual-proforma-invoice---lite"></a>Crearea unei facturi proforma manuale - simplificat

_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_

În Dynamics 365 Project Operations, facturile proforme pot fi create manual, după necesități. Puteți crea manual o factură proforma din pagina listei **Contracte de proiect** sau din pagina de detalii **Contract de proiect**.

##  <a name="project-contracts-list-page"></a>Pagina listă contracte de proiect

Din pagina de listă **Contracte de proiect**, selectați unul sau mai multe contracte de proiect și creați facturi pentru toate înregistrările selectate.

Sistemul verifică să vadă care dintre contractele de proiecte are un registru **Gata de facturat** cu o dată anterioară celei de azi. Din aceste contracte, sistemul creează proiecte de facturi proforma. Dacă un contract de proiect are mai mulți clienți, poate exista o factură creată pentru fiecare client și mai multe facturi pentru fiecare contract de proiect.

Toate facturile de proiect create sunt disponibile pe pagina **Factură fiscală** din secțiunea **Facturare** din zona **Vânzări**.

## <a name="project-contract-details-page"></a>Pagina de detalii contract de proiect

O factură proformă poate fi creată și din pagina de detalii a **Contract de proiect**. Sistemul verifică dacă contractul de proiect are un registru **Gata de facturat** cu dată anterioară celei de azi. Din aceste contracte, sistemul creează proiecte de facturi proforma pe baza numărului de clienți de pe fiecare linie de contract.

Când este creată o singură factură proforma, se deschide pagina **Factura fiscala**. În cazul în care sunt create mai multe facturi pentru respectivul contract de proiect, se deschide pagina care conține lista de **Facturi** pentru a afișa toate facturile create.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]