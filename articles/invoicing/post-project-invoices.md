---
title: Prezentare generală a procesului de facturare
description: Acest articol oferă o prezentare generală a procesului de facturare în Project Operations pentru scenarii bazate pe resurse/fără stoc.
author: sigitac
ms.date: 01/29/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 6b285a88be14a5972e9a4604713d7d35a3a442b6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923111"
---
# <a name="invoicing-process-overview"></a>Prezentare generală a procesului de facturare

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

Project Operations pentru scenariile bazate pe resurse/ne-stocate oferă capabilități cuprinzătoare adaptate pentru a se potrivi atât nevoilor managerului de proiect, cât și ale funcționarului responsabil cu conturile de creanțe/contabilului proiectului. Pentru procesul de facturare, managerul de proiect gestionează restanțele de facturare ale proiectului, iar funcționarul responsabil cu conturile de creanțe/contabilul proiectului creează un document de factură conform și precis pentru transmiterea către client.

![Diagrama fluxului de facturare.](./media/invoicing-flow.png)

Linia contractului de proiect definește metoda de facturare pentru tranzacțiile asociate proiectului. Când Managerul de proiect aprobă tranzacțiile de timp și cheltuieli, sistemul înregistrează tranzacțiile în entitatea **Valori reale ale proiectului** și trimite informațiile către modulul **Management de proiect și contabilitate** în Dynamics 365 Finance. Contabilul proiectului revizuiește apoi și postează înregistrările folosind [Jurnal de integrare din Project Operations](../project-accounting/project-operations-integration-journal.md). Acest jurnal include detalii contabile importante pentru datele reale proiectului, cum ar fi facturarea, grupul de impozitare pe vânzări, grupul de impozitare pe vânzare și dimensiuni financiare.

Managerul de proiect poate revizui tranzacțiile de vânzare nefacturate folosind metoda de facturare a timpului și a materialului din [Restanțe de facturare de timp și materiale](../proforma-invoicing/manage-billing-backlog.md#time-and-material-billing-backlog) și facturare cu preț fix în [Repere cu preț fix](../proforma-invoicing/manage-billing-backlog.md#fixed-price-milestones). Aceste vizualizări vă permit să filtrați și să selectați tranzacțiile care trebuie incluse în următorul ciclu de facturare și apoi să le marcați ca **Gata de facturare**.

Puteți [crea manual o factură proformă](../proforma-invoicing/create-manual-proforma-invoice.md) sau să folosiți un [proces periodic](../proforma-invoicing/configure-automated-invoice-creation.md). Managerul de proiect poate [realiza o schiță a unei facturi proforme](../proforma-invoicing/manage-proforma-invoice.md) după cum este necesar și apoi să o confirme.

Factura proformă confirmată este trimisă către modulul **Management de proiect și contabilitate** în Finanțe. Contabilul de proiect formatează și actualizează propunerea de facturare a proiectului, apoi postează și tipărește documentul. Facturile de proiect postate sunt înregistrate în registrul general, precum și în registrele secundare ale clientului și ale proiectului.


[!INCLUDE[footer-include](../includes/footer-banner.md)]