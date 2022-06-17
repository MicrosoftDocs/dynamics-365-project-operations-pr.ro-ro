---
title: Prezentare generală a recunoașterii veniturilor
description: Acest articol oferă informații despre recunoașterea veniturilor în Operațiunile de proiect.
author: sigitac
ms.date: 11/16/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 22486693226256f765589b272e6df36aceaf9c1c
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926285"
---
# <a name="revenue-recognition-overview"></a>Prezentare generală a recunoașterii veniturilor

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

În Dynamics 365 Project Operations, principiile de recunoaștere a veniturilor variază în funcție de metoda de facturare selectată pentru un proiect sau porțiune din proiect. Acest articol oferă informații despre recunoașterea veniturilor în Operațiunile de proiect.

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