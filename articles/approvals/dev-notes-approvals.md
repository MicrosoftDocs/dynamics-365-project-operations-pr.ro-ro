---
title: Note pentru dezvoltatori pentru aprobări
description: Acest subiect oferă informații suplimentare pentru dezvoltatori despre lucrul cu aprobări.
author: stsporen
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: a89ea669a262c145b9f391fddc19e79a425fabb5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996806"
---
# <a name="developer-notes-for-approvals"></a><span data-ttu-id="8d17f-103">Note pentru dezvoltatori pentru aprobări</span><span class="sxs-lookup"><span data-stu-id="8d17f-103">Developer notes for Approvals</span></span>

<span data-ttu-id="8d17f-104">_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_</span><span class="sxs-lookup"><span data-stu-id="8d17f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="8d17f-105">Dynamics 365 Project Operations include o logică de validare care asigură tranziția corectă a înregistrării prin etapele de aprobare.</span><span class="sxs-lookup"><span data-stu-id="8d17f-105">Dynamics 365 Project Operations includes validation logic that ensures correct record transition through the approval stages.</span></span> <span data-ttu-id="8d17f-106">Tranzițiile corecte ale înregistrării asigură:</span><span class="sxs-lookup"><span data-stu-id="8d17f-106">Correct record transitions ensure:</span></span> 

  - <span data-ttu-id="8d17f-107">Toate rândurile de susținere sunt create în tabele corelate, cum ar fi jurnalele și actualitățile.</span><span class="sxs-lookup"><span data-stu-id="8d17f-107">All supporting rows are created in related tables, such as journals and actuals.</span></span>
  - <span data-ttu-id="8d17f-108">Aprobatorul este marcat ca **Aprobator de proiect** în proiect înainte de a continua.</span><span class="sxs-lookup"><span data-stu-id="8d17f-108">The approver is marked as a **Project Approver** in the project before proceeding.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]