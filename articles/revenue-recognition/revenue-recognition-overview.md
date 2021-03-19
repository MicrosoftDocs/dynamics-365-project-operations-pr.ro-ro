---
title: Prezentare generală a recunoașterii veniturilor
description: Acest subiect furnizează informații despre recunoașterea veniturilor în Project Operations.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5e77a0442f634a50f8099fadec42ff400fee0e81
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278883"
---
# <a name="revenue-recognition-overview"></a>Prezentare generală a recunoașterii veniturilor

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

În Dynamics 365 Project Operations, principiile de recunoaștere a veniturilor variază în funcție de metoda de facturare selectată pentru un proiect sau porțiune din proiect. Acest subiect furnizează informații despre recunoașterea veniturilor în Project Operations.

## <a name="transactions-accounted-using-time-and-material-billing-method"></a>Tranzacțiile contabilizate utilizând metoda de facturare de materiale și timp

- Recunoașterea costurilor și a veniturilor sunt conectate. Costul tranzacției și vânzările nefacturate sunt înregistrate utilizând [Jurnal de integrare a Project Operations](../project-accounting/project-operations-integration-journal.md).
- Costul proiectului și profilul de venituri determină dacă tranzacțiile de vânzare nefacturate sunt înregistrate în registrul general. Dacă este selectat **Acumulați venituri**, sistemul utilizează **Valoarea vânzărilor WIP** și conturi **Valoarea vânzărilor din venituri acumulate** în timpul postării. În continuare este prezentat un exemplu al acestei metode.  

  | Tip de tranzacție | Debit/Credit | Sumă |
  | --- | --- | --- |
  | WIP valoarea Vânzărilor | Debit | 100 |
  | Venit acumulat valoarea vânzărilor | Credit | 100 |

- Veniturile sunt recunoscute în timpul facturării. Sistemul utilizează contul **Venituri facturate** în timpul publicării. În continuare este prezentat un exemplu al acestei metode.  

  | Tip de tranzacție | Debit/Credit | Sumă |
  | --- | --- | --- |
  | Soldul clienților | Debit | 120 |
  | Conturi impozit pe vânzări | Credit | 20 |
  | Venit facturat | Credit | 100 |

- În cazul în care veniturile au fost acumulate atunci când sunt înregistrate vânzările nefacturate, sistemul va inversa veniturile acumulate la facturare.

  | Tip de tranzacție | Debit/Credit | Sumă |
  | --- | --- | --- |
  | WIP valoarea Vânzărilor | Credit | 100 |
  | Venit acumulat valoarea vânzărilor | Debit | 100 |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a>Tranzacțiile contabilizate utilizând metoda de facturare de preț fix

- Recunoașterea costurilor și a veniturilor sunt separate. Costul tranzacției nefacturate este înregistrat utilizând [Jurnal de integrare a Project Operations](../project-accounting/project-operations-integration-journal.md). Tranzacțiile de vânzare necotificate nu sunt create.
- Veniturile pot fi recunoscute în timpul facturării dacă costul proiectului și profilul de venituri au **Principiul utilizat pentru calculele de finalizare a proiectului** setat la **Fără WIP**. Folosiți această metodă doar pentru proiecte simple pe termen scurt.
- Veniturile pot fi recunoscute utilizând estimări ale veniturilor la preț fix, fie cu **Contract finalizat** sau metoda **Recunoașterea veniturilor realizate în procente**.

## <a name="additional-resources"></a>Resurse suplimentare
[Configurarea contabilității pentru articolul de proiecte facturabile](../project-accounting/configure-accounting-billable-projects.md)

[Proiecte cu estimarea veniturilor cu preț fix](rev-rec-percentage-completion-method.md)

[Gestionarea estimărilor de venituri](rev-rec-completed-contract-method.md)

[Metode pentru costul de finalizare](cost-complete-methods.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]