---
title: Note pentru dezvoltatori pentru aprobări
description: Acest subiect oferă informații suplimentare pentru dezvoltatori despre lucrul cu aprobări.
author: stsporen
manager: Annbe
ms.date: 11/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: d58c776b0341c08b0292e1b459a7d7ebac550bcc
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290284"
---
# <a name="developer-notes-for-approvals"></a><span data-ttu-id="a19df-103">Note pentru dezvoltatori pentru aprobări</span><span class="sxs-lookup"><span data-stu-id="a19df-103">Developer notes for Approvals</span></span>

<span data-ttu-id="a19df-104">_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_</span><span class="sxs-lookup"><span data-stu-id="a19df-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a19df-105">Dynamics 365 Project Operations include o logică de validare care asigură tranziția corectă a înregistrării prin etapele de aprobare.</span><span class="sxs-lookup"><span data-stu-id="a19df-105">Dynamics 365 Project Operations includes validation logic that ensures correct record transition through the approval stages.</span></span> <span data-ttu-id="a19df-106">Tranzițiile corecte ale înregistrării asigură:</span><span class="sxs-lookup"><span data-stu-id="a19df-106">Correct record transitions ensure:</span></span> 

  - <span data-ttu-id="a19df-107">Toate rândurile de susținere sunt create în tabele corelate, cum ar fi jurnalele și actualitățile.</span><span class="sxs-lookup"><span data-stu-id="a19df-107">All supporting rows are created in related tables, such as journals and actuals.</span></span>
  - <span data-ttu-id="a19df-108">Aprobatorul este marcat ca **Aprobator de proiect** în proiect înainte de a continua.</span><span class="sxs-lookup"><span data-stu-id="a19df-108">The approver is marked as a **Project Approver** in the project before proceeding.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]