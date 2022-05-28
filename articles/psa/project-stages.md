---
title: Tipuri de etape de proiect
description: Acest subiect oferă informații despre etapele de proiect.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 06/19/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 7f893b5429dd61ae45ad9d536420c96b2f58605b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8586865"
---
# <a name="project-stage-types"></a>Tipuri de etape de proiect 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Fazele de proiect sunt proiectate să reflecte starea proiectului pe măsură ce progresează. Particularizările pot fi utilizate pentru a actualiza automat etapele cu fluxuri de proces de afaceri, Power Automate sau extensii de inserturi.

Următoarele etape sunt definite în BPF implicit:

- Noi
- Ofertă
- Plan
- Livrare
- Finalizare
- Închidere 

## <a name="new"></a>Nou

Când creați un proiect, etapa de proiect este setată la **Nou**. Dacă proiectul a fost creat dintr-un șablon, este posibil să aibă date de planificare, estimare și echipă. În caz contrar, este doar o schiță a proiectului, iar componentele rămase trebuie să fie introduse.

## <a name="quote"></a>Ofertă

Când asociați un proiect cu o ofertă sau când creați un proiect de la o ofertă, faza proiectului este setată la **Ofertă** și datele de început și de sfârșit estimate sunt actualizate. În timp ce proiectul este în etapa de **Ofertă**, fila **Vânzări** de pe pagina **Entitate de proiect** afișează detaliile ofertei.

## <a name="plan"></a>Plan

Atunci când câștigați o ofertă care este asociată cu un proiect și acesta este mutat la faza de **Contract**, etapa proiectului este actualizată la **Plan**. În timp ce proiectul este în etapa de **Plan**, pagina **Entitate de proiect** afișează detaliile contractului.

## <a name="deliver"></a>Livrare

Când planul de proiect este finalizat și sunteți gata să porniți proiectul, managerul de proiect ar trebui să actualizeze faza proiectului la **Livrare** pentru a arăta că proiectul a început.

## <a name="complete"></a>Finalizare 

Când lucrarea pentru proiect este finalizată, managerul de proiect poate actualiza etapa la **Finalizare**. Prin actualizarea etapei de proiect la **Finalizare**, managerul de proiect indică faptul că lucrarea este 100% finalizată, dar că proiectul este ținut deschis, astfel încât orice timp în așteptare sau intrările de cheltuieli să poată fi înregistrate.

## <a name="close"></a>Închidere

Când toate tranzacțiile sunt înregistrate pentru proiect, managerul de proiect poate actualiza etapa la **Închidere**. În acel moment, nu pot fi înregistrate tranzacții, iar proiectul este setat la doar în citire.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
