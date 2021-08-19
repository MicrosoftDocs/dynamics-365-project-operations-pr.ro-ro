---
title: Gestionarea stării și validărilor care nu trebuie depășite
description: Acest subiect oferă informații despre verificările limită de nedepășit efectuate în Project Operations.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b08a6834fa0bc5254f4baab15b40c7f733d0dc6ec7e6c4fceea2836e5e4c656a
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/06/2021
ms.locfileid: "7003516"
---
# <a name="manage-not-to-exceed-status-and-validations"></a>Gestionarea stării și validărilor care nu trebuie depășite 

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

## <a name="not-to-exceed-on-approvals"></a>Nu trebuie depășit la aprobări

Când se trimite o intrare de timp, cheltuială sau utilizare a materialului, se creează o înregistrare de aprobare. Dacă aprobarea se plătește și se asociază unei linii contractuale de timp și materiale, sistemul finalizează o verificare de validare care nu trebuie depășită la următoarele niveluri:

  - Verificați limita stabilită pentru client pe linia contractului de proiect
  - Verificați limita stabilită pe linia de contract
  - Verificați limita configurată pentru client
  - Verificați limita stabilită pe contract

Verificările la fiecare nivel implică asigurarea faptului că valoarea valorii vânzărilor din această aprobare nu va încălca limita de depășire la acel nivel după contabilizarea cantității de restante de facturare deja înregistrate și a sumei facturate până în prezent la acel nivel.

Dacă verificarea trece, aprobării i se acordă un statut de validare de **Succes**.

Dacă verificarea eșuează, aprobării i se acordă un statut de validare de **Eșuat**. Detaliile de validare care nu trebuie depășite vor informa utilizatorul la ce nivel de validare nu a reușit.

Când intrarea de timp, cheltuială sau utilizare a materialului trimisă este considerată netaxabilă, starea de validare care nu trebuie depășită este setată la **Nu se aplică** cu detaliul de validare egal cu **Nu se aplică**.

## <a name="not-to-exceed-on-unbilled-sales-actuals"></a>Nu trebuie depășit pentru vânzările reale facturate

Atunci când este aprobată o înregistrare de timp, cheltuială sau utilizare a materialului, se creează înregistrări reale ale costurilor și ale vânzărilor nefacturate. Dacă vânzările reale nefacturate create sunt facturabile și mapate la o linie de contract de timp și materiale, aplicația realizează o validare care nu trebuie depășită la următoarele niveluri:

  - Verificați limita stabilită pentru client pe linia contractului de proiect
  - Verificați limita stabilită pe linia de contract
  - Verificați limita configurată pentru client
  - Verificați limita stabilită pe contract

Verificările la fiecare nivel asigură faptul că valoarea valorii vânzărilor reale nu va încălca limita de depășire la acel nivel după contabilizarea cantității de restante de facturare deja înregistrate și a sumei facturate până în prezent la acel nivel.

Dacă cecul trece, vânzările nefacturate efective primesc statutul de a nu depăși **Comis**.

Dacă verificarea eșuează, vânzările nefacturate efective primesc statutul de a nu depăși **Eșuat**. Detaliile de validare informează utilizatorul la ce nivel de validare nu a reușit.

Când vânzările reale facturate sunt considerate neimpozabile sau gratuite, dacă nu există o setare a limitei care să nu depășească la vreunul dintre cele patru niveluri sau dacă realitatea creată este cost, onorariu, unitate de resurse sau vânzări între organizații, câmpurile **Starea de a nu depăși** și **Detalii de validare care nu trebuie depășite** trebuie setate la **Nu se aplică**.

## <a name="reset-the-not-to-exceed-status"></a>Resetați starea de nedepășire

Puteți efectua o resetare masivă a stării nu trebuie depășit. Managerii de proiect pot ajusta validarea „nu depășește” pentru a prioritiza facturarea unui anumit corp de muncă, timp, cheltuială sau utilizare de materiale față de altele care sunt deja angajate din suma disponibilă care nu trebuie depășită.

După ce starea de depășit este resetată pentru vânzările nefacturate, suma angajată este redusă. Managerul de proiect poate selecta un alt corp de muncă, timp, cheltuială sau intrare de utilizare a materialului care nu a reușit anterior validarea de nedepășire și să o reevalueze. Odată cu reducerea sumei angajate, aceste date reale trec acum de validare, ceea ce îl ajută pe managerul de proiect să exercite o mai mare influență și control asupra tranzacțiilor facturabile pentru perioada respectivă.

Pentru a reseta starea care nu trebuie depășită, selectați una sau mai multe date reale din vizualizarea **Restanțe de facturare de timp și materiale** sau **Reale**, apoi selectați **Resetați starea de nedepășire**.

Starea de depășit este resetată la **Neevaluat** pe toate datele relevante selectate. Informațiile care au resetarea stării care nu trebuie depășite sunt facturi de vânzare nefacturate care nu sunt deja facturate, nu sunt incluse într-o schiță de factură și sunt marcate drept taxabile. Orice alte date selectate sunt ignorate.

## <a name="reevaluate-not-to-exceed-status"></a>Reevaluați starea de nedepășire

Puteți efectua o reevaluare masivă a stării care nu trebuie depășită. Reevaluarea stării de a nu depăși este utilă atunci când:

  - A existat o renegociere a limitelor care nu trebuie depășite cu clientul, iar realitatea va trebui reevaluată.
  - Managerul de proiect dorește să regleze fin facturarea restanțelor de vânzări nefacturate, prioritizând un corp de lucru în locul altui.

Pentru a reevalua starea care nu trebuie depășită, selectați una sau mai multe date reale din vizualizarea **Restanțe de facturare de timp și materiale** sau **Reale**, apoi selectați **Resetați starea de nedepășire**.

Toate datele relevante selectate cu o limită de depășit vor fi evaluate în raport cu setarea limită de depășire. Informațiile care sunt relevante pentru reevaluarea stării care nu trebuie depășite sunt facturi de vânzare nefacturate care nu sunt deja facturate, nu sunt incluse într-o schiță de factură și sunt marcate drept facturabile. Orice alte elemente selectate selectate.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
