---
title: Ce este nou 2021 acces timpuriu valul 2 - implementare Project Operations lite
description: Acest subiect oferă informații despre caracteristicile disponibile în versiunea Project Operations de implementare lite cu acces timpuriu disponibilă în valul 2 din 2021.
author: sigitac
ms.date: 08/10/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a201e3e4333b8892eea72387222d64e18b74d71b
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323926"
---
# <a name="whats-new-2021-wave-2-early-access---project-operations-lite-deployment"></a>Ce este nou 2021 acces timpuriu valul 2 - implementare Project Operations lite

_Se aplică pentru: implementare simplificată - înțelegere la emiterea facturii proforme_

Acest subiect se aplică următoarelor componente și versiuni Dynamics 365 Project Operations:

  - Project Operations pe mediul Dataverse versiunea 4.23.0.4

Versiunea se aplică numai atunci când este un mediu [a optat pentru Acces timpuriu](/power-platform/admin/opt-in-early-access-updates#how-to-enable-early-access-updates).

## <a name="features-included-in-this-release"></a>Caracteristicile incluse în această versiune

[Managementul subcontractelor](../subcontracting/subcontracting_EA_scope.md) - Această caracteristică oferă o mai bună vizibilitate și un mai bun control asupra tuturor aspectelor lucrului la un proiect. Previzualizarea gestionării subcontractelor include următoarele capacități:

  - Un manager de proiect poate crea un subcontract cu un furnizor. În mod implicit, listele de prețuri atașate la înregistrarea furnizorului sunt utilizate pentru subcontract. Contul de furnizor are un tip de relație **Vânzător** sau **Furnizor**.
  - Un manager de proiect poate detalia toate achizițiile ca elemente de linie pe subcontract. Liniile de subcontract pot fi pentru timp, cheltuieli sau produse. Clasa de tranzacție care a liniei de subcontract stabilește pentru ce este linia.
  - Managerul de cont al furnizorului și managerul de proiect pot itera subcontractul. Prețurile pot fi ajustate în listele de prețuri de achiziție atașate subcontractului.
  - În timpul procesului, dacă linia de subcontract este pentru timp, managerul contului de furnizor poate asocia persoanele de contact ale furnizorului cu fiecare linie de subcontract. Această asociere oferă informații managerului de proiect care lucrează la subcontract. Când o persoană de contact a furnizorului este asociată cu o linie de subcontract, sistemul creează automat o resursă ce se poate rezerva din contact, dacă o resursă ce se poate rezerva nu există deja.
  - Metoda de facturare pe fiecare linie de subcontract poate fi Preț fix sau Timp și material. Pentru liniile de subcontract cu preț fix, se configurează o planificare de facturare bazată pe jaloane.
