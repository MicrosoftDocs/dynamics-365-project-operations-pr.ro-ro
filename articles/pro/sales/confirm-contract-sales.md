---
title: Confirmarea unui contract de proiect
description: Acest subiect oferă informații despre cum să confirmați un contract în Project Operations.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 24da0887c0266d51bddcbbf8efd6f2644b6d0f4f
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128298"
---
# <a name="confirm-a-project-contract"></a>Confirmarea unui contract de proiect

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Un contract de proiect în Dynamics 365 Project Operations poate fi activ cu un motiv de **Confirmat**, sau închis cu un motiv de **Pierdut**. Când confirmați un contract de proiect, starea se actualizează de la **Schiță** la **Activ** iar motivul de stare este **Confirmat**. Un contract activ sau închis nu poate fi editat sau redeschis. 

### <a name="financial-impact-of-confirming-a-project-contract"></a>Impactul financiar al confirmării unui contract de proiect

După confirmarea unui contract de proiect, aplicația recalculează costurile prin inversarea costurilor mai vechi și creând costuri noi. Noile costuri efective sunt apoi procesate pe baza metodei de facturare a liniei contractului de proiect asociat. În cazul în care costurile reale fac referire la o linie contractuală de timp și materiale, aplicația recreează automat efectele corespunzătoare de vânzări nefacturate. În cazul în care costurile reale fac referire la o linie de contract cu preț fix, aplicația încetează să reproceseze costurile reale.

Limitele care nu trebuie depășite, configurarea taxării, precum și stabilirea prețurilor și a costurilor pentru datele reale sunt evaluate și apoi actualizate ca parte a procesului de confirmare.

## <a name="close-a-project-contract-as-lost"></a>Închideți un contract de proiect ca pierdut

Când închideți un contract de proiect ca pierdut, starea contractului este actualizată la **Închis** iar motivul de stare este **Pierdut**. Contractul de proiect devine doar în citire. Apare un dialog de confirmare înainte de finalizarea modificărilor, deoarece nu puteți redeschide un contract de proiect închis.

Dacă contractul de proiect închis ca pierdut face referire la un proiect pe liniile sale, acel proiect este de asemenea marcat ca închis. Orice rezervare de resurse începând cu ziua respectivă este anulată. Orice vânzări reale nefacturate din contractul de proiect care nu sunt deja pe factură vor fi anulate.

> [!NOTE]
> În Dynamics 365 Project Operations, închiderea unui contract de proiect ca pierdut nu va avea impact asupra stării oportunității asociate. Oportunitatea va rămâne deschisă și trebuie închisă manual.
