---
title: Moduri de planificare
description: Acest subiect oferă informații despre moduri de planificare.
author: ruhercul
ms.date: 05/28/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: cb507528c4815f5149c813bba0a354f7d840a4a5
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8588429"
---
# <a name="scheduling-modes"></a>Moduri de planificare

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_


Dynamics 365 Project Operations oferă capacitatea organizațiilor de a defini modul în care gestionează modificările variabilelor cheie în sarcinile din cadrul structurii detaliate a proiectului. Pe baza nevoilor specifice de organizație, managerii de proiect pot aduce modificări modului de planificare atunci când este creat un proiect.

Există trei moduri de planificare disponibile în Project Operations:

  - Durată fixă (acesta este modul implicit)
  - Efort fix (*Lucru*)
  - Unități fixe

Valorile afectate de definiția unui mod de planificare specific sunt determinate de următoarea formulă:

  Efort = Durată x Unități

Când definiți modul de planificare al unui proiect, setați una dintre aceste valori, care apoi nu poate fi modificată. Păstrarea acestei valori ca constantă acordă o prioritate acelei valori, care notifică sistemul astfel încât să nu o modifice atunci când se schimbă celelalte două valori. Tabelul următor oferă informații despre impactul selectării unui mod specific.

| **În această sarcină**             | **Dacă revizuiți unitățile**   | **Dacă revizuiți durata** | **Dacă revizuiți efortul**  |
|----------------------|---------------------------|----------------------------|---------------------------|
| Unități fixe de sarcină     | Durata este recalculată. | Efortul este recalculat.    | Durata este recalculată. |
| Efort fix de sarcină    | Durata este recalculată. | Unitățile sunt recalculate.    | Durata este recalculată. |
| Durată fixă de sarcină  | Efortul este recalculat.   | Efortul este recalculat.    | Unitățile sunt recalculate.   |

Pentru mai multe informații privind implicațiile unui mod dat, consultați [Schimbați tipul de activitate pentru o planificare mai precisă](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72). În subiect, termenul **Muncă** este folosit în loc de **Efort**.

## <a name="change-the-organizations-scheduling-mode"></a>Schimbați modul de planificare al organizației

Parcurgeți următorii pași pentru a defini modul de planificare al unei organizații.

1. Accesați **Setări** \> **General** \> **Parametrii**, apoi selectați parametrul proiectului. 
2. Pe pagina **Parametrii proiectului**, selectați modul de planificare implicit pentru organizație, apoi definiți capacitatea managerului de proiect de a suprascrie setarea atunci când creați un proiect nou.

## <a name="change-the-scheduling-mode-setting-on-a-project"></a>Modificați setarea modului de planificare pentru un proiect

Dacă o organizație permite managerului de proiect să suprascrie modul de planificare implicit, managerul de proiect poate face această modificare atunci când creează un proiect nou. Cu toate acestea, după ce proiectul a fost salvat, modul de planificare nu poate fi schimbat.

## <a name="copied-projects"></a>Proiecte copiate

Deoarece un proiect este creat atunci când se ia acțiunea de copiere a acelui proiect, managerul de proiect nu poate seta modul de planificare. Proiectul de destinație va fi implicit întotdeauna la modul definit la nivel organizațional.

## <a name="copied-tasks"></a>Sarcini copiate

Când este copiată o sarcină de la un proiect la altul, sarcina moștenește modul de planificare al proiectului de destinație.
