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
ms.openlocfilehash: 9e4e910d0ff0a5f2603148fcc5daa0d423a4d174
ms.sourcegitcommit: a9dbcd3aff4c6ae495412e4980e105ae160fd1ec
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 11/10/2020
ms.locfileid: "4483963"
---
# <a name="developer-notes-for-approvals"></a><span data-ttu-id="742ba-103">Note pentru dezvoltatori pentru aprobări</span><span class="sxs-lookup"><span data-stu-id="742ba-103">Developer notes for Approvals</span></span>

<span data-ttu-id="742ba-104">_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_</span><span class="sxs-lookup"><span data-stu-id="742ba-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="742ba-105">Dynamics 365 Project Operations includ o logică de validare care asigură tranziția corectă a înregistrării prin etapele de aprobare.</span><span class="sxs-lookup"><span data-stu-id="742ba-105">Dynamics 365 Project Operations includes validation logic that ensures correct record transition through the approval stages.</span></span> <span data-ttu-id="742ba-106">Tranzițiile corecte ale înregistrării asigură:</span><span class="sxs-lookup"><span data-stu-id="742ba-106">Correct record transitions ensure:</span></span> 

  - <span data-ttu-id="742ba-107">Toate rândurile de susținere sunt create în tabele corelate, cum ar fi jurnalele și actualitățile.</span><span class="sxs-lookup"><span data-stu-id="742ba-107">All supporting rows are created in related tables, such as journals and actuals.</span></span>
  - <span data-ttu-id="742ba-108">Aprobatorul este marcat ca **Aprobator de proiect** în proiect înainte de a continua.</span><span class="sxs-lookup"><span data-stu-id="742ba-108">The approver is marked as a **Project Approver** in the project before proceeding.</span></span>
