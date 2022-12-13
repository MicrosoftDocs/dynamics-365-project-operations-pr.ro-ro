---
title: Noutăți octombrie 2022 - implementare simplificată Project Operations
description: Acest articol oferă informații despre actualizările de calitate care sunt disponibile în versiunea din octombrie 2022 a implementării Microsoft Dynamics 365 Project Operations lite.
author: ramagadu
ms.date: 11/17/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: b6975e1f8645721fc03239b355b117eb664785f0
ms.sourcegitcommit: 1f162707ac342343fb5390fb9ae335e4cea4f3f2
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 11/29/2022
ms.locfileid: "9806764"
---
# <a name="whats-new-october-2022---project-operations-lite-deployment"></a>Noutăți octombrie 2022 - implementare simplificată Project Operations

_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_

Acest articol se aplică următoarelor componente și versiuni de Microsoft Dynamics 365 Project Operations:

- Project Operations într-un mediu Dataverse versiunea 4.57.0.176

## <a name="features-included-in-this-release"></a>Caracteristicile incluse în această versiune

| Zonă de caracteristici | Denumire funcție | Mai multe informații |
| --- | --- | --- |
| Planificare și urmărire de proiect | **Operațiuni de proiect Programare externă**<br>Modul de planificare externă permite clienților să creeze, să actualizeze și să ștergă în mod nativ entități care sunt legate de structurile de defalcare a lucrărilor (WBS) utilizând API-urile native Dataverse , fără limitele actuale impuse de Project for the Web. | [Programare externă](/dynamics365/project-operations/project-management/external-scheduling) |
| Implementare și configurare | <p>**Permiteți clienților să aleagă tipul de implementare**<br>Actualizările bazate pe produs (PDU) ale Project Operations sunt folosite pentru a instala automat soluția Project Operations Dual-write atunci când soluțiile de bază și orchestrare Dual-write sunt instalate în mediu.</p><p>Această caracteristică introduce un nou parametru **Comportament de actualizare a soluției** în Parametrii proiectului. Când acest parametru este setat la **Numai Lite**, PUD-urile nu vor mai instala automat soluția de scriere dublă Project Operations, chiar dacă în mediu sunt instalate soluții de bază și de orchestrare dual-write. . Acest comportament va aduce beneficii clienților care intenționează să folosească soluții Dual-write pentru a integra comenzile de vânzări în aplicațiile de finanțare și operațiuni, dar doresc să folosească Operațiunile de proiect într-un mod simplificat (adică fără integrare în aplicațiile de finanțare și operațiuni).</p> | |

## <a name="quality-updates"></a>Actualizări de calitate

| Zonă de caracteristici | Număr de referință | Actualizare de calitate |
| --- | --- | --- |
| Facturarea și stabilirea prețurilor | 2316317 | Sistemul permite crearea unei facturi care nu au tranzacții taxabile. |
| Facturarea și stabilirea prețurilor | 2737300 | Validați pentru disponibilitatea câmpului Client înainte de accesarea formularului. |
| Facturarea și stabilirea prețurilor | 2744948 | Adăugați o verificare nulă pentru Metoda de facturare. |
| Facturarea și stabilirea prețurilor | 2763515 | Gândirea erorii de referință nulă atunci când lipsește contractul de vânzare al facturii. |
| Facturarea și stabilirea prețurilor | 2844301 | Crearea facturii lot eșuează din cauza unei erori. |
| Facturarea și stabilirea prețurilor | 2845869 | Stocarea incorectă a serviciului de organizare. |
| Facturarea și stabilirea prețurilor | 2853729 | Detaliile despre rol și preț sunt actualizate atunci când se modifică Tipul de facturare. |
| Facturarea și stabilirea prețurilor | 2940350 | Când prețurile reale sunt stabilite, numai listele de prețuri active ar trebui introduse automat. |
| Implementare și configurare | 3001206 | Entitatea msdyn\_ replaylogheader împiedică actualizările organizațiilor clienților. |
| Managementul oportunităților | 2755582 | Gestionarea excepțiilor de referință nulă în Ajutorul regulilor de facturare împărțită. |
| Managementul oportunităților | 2761477 | Când se utilizează facturarea divizată, ștergerea unei etape (antet) lasă repere orfane. |
| Managementul oportunităților | 2767595 | Când o înregistrare de utilizare a materialului este deschisă în formularul principal, resursa rezervabilă pentru înregistrare este schimbată în utilizatorul conectat în prezent. |
| Planificare și urmărire de proiect | 2790384 | Timeout-ul Pending OperationSet este prea scurt. |
| Gestionarea de resurse | 2751560 | Unități de organizare preferate inconsecvente în necesarul de resurse. |
| Subcontractare | 2907231 | Etapa de procesare a facturilor furnizorilor nu poate avansa. |
| Timp și cheltuială | 2867363 | Înregistrările nu ies din vizualizarea Absențe/Vacanțe pentru aprobare atunci când sunt puse în coadă pentru aprobare. |
| Timp și cheltuială | 2894405 | TESA: Directorul POC neutilizat cauzează probleme de conformitate. |
