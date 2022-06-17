---
title: Ce este nou 2021 acces timpuriu valul 2 - implementare Project Operations lite
description: Acest articol oferă informații despre caracteristicile disponibile în lansarea de acces anticipat al valului 2 din 2021 a implementării Project Operations lite.
author: sigitac
ms.date: 08/10/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d245868c8bd9ff332707a81c074d6c7ae3649378
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924123"
---
# <a name="whats-new-2021-wave-2-early-access---project-operations-lite-deployment"></a>Ce este nou 2021 acces timpuriu valul 2 - implementare Project Operations lite

_Se aplică pentru: implementare simplificată - înțelegere la emiterea facturii proforme_

Acest articol se aplică la următoarele Dynamics 365 Project Operations componente si versiuni:

  - Project Operations pe mediul Dataverse versiunea 4.23.0.4

Versiunea se aplică numai atunci când este un mediu [a optat pentru Acces timpuriu](/power-platform/admin/opt-in-early-access-updates#how-to-enable-early-access-updates).

## <a name="features-included-in-this-release"></a>Caracteristicile incluse în această versiune

[Managementul subcontractelor](/dynamics365/project-operations/pro/subcontracting/managing-subcontracts-overview) - Această caracteristică oferă o mai bună vizibilitate și un mai bun control asupra tuturor aspectelor lucrului la un proiect. Previzualizarea gestionării subcontractelor include următoarele capacități:

  - Un manager de proiect poate crea un subcontract cu un furnizor. În mod implicit, listele de prețuri atașate la înregistrarea furnizorului sunt utilizate pentru subcontract. Contul de furnizor are un tip de relație **Vânzător** sau **Furnizor**.
  - Un manager de proiect poate detalia toate achizițiile ca elemente de linie pe subcontract. Liniile de subcontract pot fi pentru timp, cheltuieli sau produse. Clasa de tranzacție care a liniei de subcontract stabilește pentru ce este linia.
  - Managerul de cont al furnizorului și managerul de proiect pot itera subcontractul. Prețurile pot fi ajustate în listele de prețuri de achiziție atașate subcontractului.
  - În timpul procesului, dacă linia de subcontract este pentru timp, managerul contului de furnizor poate asocia persoanele de contact ale furnizorului cu fiecare linie de subcontract. Această asociere oferă informații managerului de proiect care lucrează la subcontract. Când o persoană de contact a furnizorului este asociată cu o linie de subcontract, sistemul creează automat o resursă ce se poate rezerva din contact, dacă o resursă ce se poate rezerva nu există deja.
  - Metoda de facturare pe fiecare linie de subcontract poate fi Preț fix sau Timp și material. Pentru liniile de subcontract cu preț fix, se configurează o planificare de facturare bazată pe jaloane.
