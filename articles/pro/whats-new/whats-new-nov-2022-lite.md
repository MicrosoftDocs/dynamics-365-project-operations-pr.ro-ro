---
title: Noutăți noiembrie 2022 – implementare Project Operations lite
description: Acest articol oferă informații despre actualizările de calitate care sunt disponibile în versiunea din noiembrie 2022 a implementării Microsoft Dynamics 365 Project Operations lite.
author: ryansandness
ms.date: 12/16/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ryansandness
ms.openlocfilehash: ed61f8c03c4ab1960aaf97712b3d46dc298ce96a
ms.sourcegitcommit: 952fcefe33de192ad48f4108c3adbe658fd7b94f
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 12/08/2022
ms.locfileid: "9831139"
---
# <a name="whats-new-november-2022---project-operations-lite-deployment"></a>Noutăți noiembrie 2022 – implementare Project Operations lite

_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_

Acest articol se aplică următoarelor componente și versiuni de Microsoft Dynamics 365 Project Operations:

- Project Operations într-un mediu Dataverse versiunea 4.58.0.119


## <a name="quality-updates"></a>Actualizări de calitate

| Zonă de caracteristici | Număr de referință | Actualizare de calitate |
| --- | --- | --- |
| Facturarea și stabilirea prețurilor | 2781818 | Eroare cheie nu a fost găsită la stabilirea prețului implicit pentru jurnalul de utilizare a materialelor. |
| Facturarea și stabilirea prețurilor | 2922373 | Nu se poate conecta linia de ofertă la proiectul care s-a închis ca ofertă pierdută. |
| Facturarea și stabilirea prețurilor | 2943206 | **Câmpul Contract Line** din Entitatea de proiect ar trebui să fie opțional. |
| Facturarea și stabilirea prețurilor | 2953182 | Îmbunătățiți mesajul de eroare pentru facturile de corectare.|
| Facturarea și stabilirea prețurilor | 2959500 | Nu se poate conecta linia de ofertă la o sarcină de proiect care este deja asociată cu o ofertă pierdută.|
| Facturarea și stabilirea prețurilor | 2959560 | Mesajul „Acest client este deja în contractul de proiect” a primit în timp ce închidea oferta ca câștigată în anumite locații. |
| Facturarea și stabilirea prețurilor | 3031727 | Atribuțiile de resurse eșuează cu eroare lipsă în câmpul obligatoriu „msdyn_Company”. |
| Facturarea și stabilirea prețurilor | 3036905 | Compania proprietară nu este niciodată inițializată pe ProjectTeamMember. |
| Managementul oportunităților | 2763519 | Eroare de referință nulă în EnsureProjectContractAllowsUpdates. |
| Managementul oportunităților | 2783798 | La importarea estimărilor de proiect pe linia de cotație, lipsesc descrierile sarcinilor pentru estimările de cheltuieli și materiale.|
| Managementul oportunităților | 2988635 | Îmbunătățiți descrierea mesajului de eroare la ștergerea clientului din cotație. |
| Managementul oportunităților | 3001191 | Nu se poate crea o ofertă din Opportunity unde metoda de facturare este specificată ca nulă. |
| Upgrade | 3012324 | Conversia proiectului a eșuat pentru un proiect cu caractere de control precum Tab în numele său. || Planificare și urmărire de proiect | 2790384 | Timeout-ul Pending OperationSet este prea scurt. |
| Planificare și urmărire de proiect | 3044275 | Lipsește localizarea pentru: missingProjectSchedulerErrorMessage. |
| Planificare și urmărire de proiect | 3044277 | Grila Project Recon nu se încarcă când planificatorul este dezactivat.|
| Gestionarea de resurse | 2943153 | Actualizați fila Urmărire pentru a afișa două zecimale pentru Durată.|
| Subcontractare | 2932774 | Linia de factură a furnizorului, eroare de aruncare numai în citire incorect. |
| Subcontractare | 2939556 | Starea antetului facturii furnizorului nu ar trebui să fie setată la Ștergerea online a schiței dacă nu este activă. |
| Timp și cheltuială | 2939998 | Utilizați noua versiune TESA în ProjOps. |
