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
# <a name="developer-notes-for-approvals"></a>Note pentru dezvoltatori pentru aprobări

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Dynamics 365 Project Operations includ o logică de validare care asigură tranziția corectă a înregistrării prin etapele de aprobare. Tranzițiile corecte ale înregistrării asigură: 

  - Toate rândurile de susținere sunt create în tabele corelate, cum ar fi jurnalele și actualitățile.
  - Aprobatorul este marcat ca **Aprobator de proiect** în proiect înainte de a continua.
