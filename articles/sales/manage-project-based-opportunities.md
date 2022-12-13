---
title: Gestionarea oportunităților de proiecte
description: Acest articol oferă informații despre cum să lucrați cu oportunități legate de proiecte.
author: rumant
ms.date: 10/21/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 56eba38476dd5b49f0043eee5d411d51f9bf56b8
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 12/05/2022
ms.locfileid: "9825347"
---
# <a name="manage-project-opportunities"></a>Gestionarea oportunităților de proiecte

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Companiile bazate pe proiecte își desfășoară de obicei operațiunile de livrare răspândite în mai multe țări și geografii. Costul execuției și livrării proiectului poate varia în funcție de geografie sau divizie care gestionează livrarea. La rândul său, acest lucru poate afecta marjele tranzacției. Furnizarea de servicii bazate pe proiecte implică de obicei cantități mari de timp pentru resurse umane, cheltuieli considerabile pentru călătorie, costuri materiale și alte cheltuieli.

Oportunități bazate pe proiecte în Dynamics 365 Project Operations sunt proiectate cu extensii la Dynamics 365 Sales. Articolul oferă detalii despre diferitele câmpuri și logica de afaceri incluse în funcționalitatea suplimentară necesară companiilor bazate pe proiecte pentru a gestiona oportunitățile bazate pe proiecte.

## <a name="view-all-project-based-opportunities"></a>Vizualizați toate oportunitățile bazate pe proiecte

O listă cu toate oportunitățile bazate pe proiect poate fi văzută din pagina listei **Oportunitate**. 

1. Accesați **Vânzări** > **Oportunități**.
2. Utilizați **Comutator de vizualizare** pentru a selecta alte vizualizări filtrate ale oportunităților. Puteți crea propriile vizualizări cu criterii de filtrare personalizate pentru a configura aceste vizualizări și opțiuni de navigare.

Oportunitățile de proiect pot fi create sau șterse din această pagină a listei sau din pagina de detalii.

## <a name="business-process-flow-for-project-based-deals"></a>Flux de business pentru oferte bazate pe proiecte

Următoarele fluxuri de proces de afaceri sunt acceptate pentru tranzacții bazate pe proiecte în Project Operations:

- Client potențial la procesul de business oportunitate
- Proces de vânzări de oportunitate

### <a name="lead-to-opportunity-business-process"></a>Proces de afaceri de la client potențial la oportunitate 
Procesul de afaceri de la client potențial la oportunitate susține următoarele etape:

| Etapă | Entitate mapată | Funcționalitate |
| --- | --- | --- |
| Calificare | Client potențial | Calificați clientul potențial pentru a crea un cont, o persoană de contact și o oportunitate. |
| Dezvoltare | Oportunitate | Dezvoltați oportunitatea de a adăuga mai multe informații despre activitatea implicată, părțile interesate cheie și concurența. |
| Propunere | Oportunitate | Elaborați propunerea și obțineți aprobarea de la echipa de revizuire internă. |
| Închideți | Oportunitate | Câștigați oportunitatea pentru a închide tranzacția. |

### <a name="opportunity-sales-process"></a>Proces de vânzări de oportunitate
Proceul de Oportunitate de vânzări în Project Operations este o extensie a procesului de afaceri a Oportunității de vânzări în aplicația Vânzări. Acest proces de afaceri este conceput pentru a susține următoarele etape într-o oportunitate bazată pe proiect.

| Etapă | Entitate mapată | Funcționalitate |
| --- | --- | --- |
| Calificare | Oportunitate | Calificați clientul potențial pentru a crea un cont, o persoană de contact și o oportunitate. |
| Propunere | Ofertă | Dezvoltați propunerea utilizând oferte de proiect și obțineți aprobare de la echipa de recenzie internă. |
| Contract | Contract pentru proiect | Câștigați oferta pentru a crea contractul și începeți executarea și livrarea proiectului. |
| Închideți | Contract pentru proiect | Finalizați lucrarea cu succes și închideți contractul de proiect. |

> [!NOTE]
> Dacă afacerea dvs. bazată pe proiect a început cu un client potențial, procesul de business de la client potențial la oportunitate are prioritate.
>
> Dacă afacerea dvs. bazată pe proiect a început cu o oportunitate, procesul de vânzări de oportunitate de vânzări are prioritate.

Puteți edita produsul flux de business sau puteți crea propriile fluxuri de procese de afaceri pentru a vă urmări procesul de vânzare, după cum este necesar. Pentru mai multe informații despre fluxul de business, consultați [Prezentare generală a fluxurilor de business](/dynamics365/customerengagement/on-premises/customize/business-process-flows-overview).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
