---
title: Gestionarea clienților potențiali
description: Acest articol furnizează informații despre gestionarea clienților potențiali pe bază de proiect.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 080f53ee2f800b8433d055525852f5c2e21aab77
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920213"
---
# <a name="manage-leads"></a>Gestionarea clienților potențiali

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

Oportunitățile bazate pe proiect pot fi gestionate și calificate în Project Operations. Procesul de gestionare a clienților potențiali include crearea de clienți potențiali pe bază de muncă și calificarea acestora. 

## <a name="project-sales-leads"></a>Clienți potențiali de proiect de vânzări

În secțiunea **Vânzări**, în panoul de navigare din stânga, deschideți pagina listă **Clienți potențiali** pentru a vizualiza o listă cu toate înregistrările potențiale din sistem. Lista de clienți potențiali afișați este bazată pe muncă și alte tipuri de clienți potențiali care pot fi creați dacă aveți și Dynamics 365 Sales sau aplicații Dynamics 365 Field Service.

Puteți crea o vizualizare filtrată pentru a vedea numai clienți potențiali bazate pe proiecte, creând un filtru pe valoarea **Tip**. De exemplu, puteți selecta să afișați numai clienți potențiali pe bază de muncă.

## <a name="create-a-new-lead-for-a-project-based-deal"></a>Creați un nou client potențial pentru o tranzacție pe bază de proiect

Când un client bazat pe proiect este calificat, se creează o oportunitate și un cont. O oportunitate bazată pe proiect este punctul de plecare pentru activitățile de urmărire a vânzărilor în faza oportunitate. Oportunitățile bazate pe proiecte au capacități unice care sunt necesare pentru vânzarea lucrărilor de proiect. Aceste funcții includ:

- Metode de facturare pentru timp și material și preț fix
- Liste de prețuri cu date multiple pentru resurse umane, cheltuieli și materiale suportate în cadrul proiectelor

Pentru ca un potențial calificat să creeze automat o oportunitate, setați atributul **Tip** la **Pe bază de muncă** atunci când creați clientul potențial. Dacă alegeți un alt tip, clientul potențial nu va crea o oportunitate bazată pe proiect atunci când este calificat. Dacă oportunitatea bazată pe proiect nu este creată, capacitățile specifice proiectului nu vor fi disponibile în procesele de vânzare din aval.

Tabelul următor include informații importante de câmp pentru un potențial și implicațiile din aval ale acestor câmpuri.
 
| **Câmp** | **Locaţie** | **Descriere** | **Impactul din aval** |
| --- | --- | --- | --- |
| Subiect | Fila General | Acest câmp text ar trebui să conțină o scurtă descriere a tranzacției. | Subiectul clientului potențial va fi implicit ca subiect al oportunității și Numele contractului de ofertă și proiect. |
| Tip | Fila General | Acest câmp set de opțiuni are următoarele opțiuni:</br>- Pe bază de muncă (disponibil numai când este instalat Project Operations)</br>- Pe bază de element (disponibil numai atunci când sunt instalate Project Operations și Vânzări)</br>- Serviciu bazat pe întreținere (disponibil când este instalat Field Service) | Când valoarea acestui câmp este setată la **Pe bază de muncă** pe clientul potențial, acesta este calificat pentru a crea o oportunitate bazată pe proiect. O oportunitate pe bază de proiect este necesară pentru a permite toate extensiile și funcționalitățile specifice proiectului în procesul de vânzare din aval pentru această tranzacție. |
| Prenume | Fila General | Prenumele persoanei de contact ale clientului prospectat | Când clientul potențial este calificat, sunt create un cont, persoană de contact și oportunitatea. Prenumele persoanei de contact este valoarea stabilită aici. |
| Nume | Fila General | Numele de familie al persoanei de contact ale clientului prospectat | Când clientul potențial este calificat, sunt create un cont, persoană de contact și oportunitatea. Numele de familie al persoanei de contact este valoarea stabilită aici. |
| Companie | Fila General | Numele companiei clientului prospectați | Când clientul potențial este calificat, sunt create un cont, persoană de contact și oportunitatea. Numele contului creat valoarea stabilită aici. |
| Monedă | Fila Detalii | Moneda clientului potențial | Când clientul potențial este calificat, sunt create un cont, persoană de contact și oportunitatea. Moneda contului creat este valoarea stabilită aici. |

## <a name="qualify-a-new-project-based-lead"></a>Calificați un nou client potențial bazat pe proiecte

Clienții potențiali care au valoarea **Tip** setată la **Bazat pe muncă** sunt numiți clienți potențiali pe bază de proiect. Când un potențial bazat pe proiect este calificat, se creează următoarele:

- Un cont care utilizează câmpul **Companie** din clientul potențial.
- O înregistrare de contact asociată contului pe baza valorilor din **Prenume** și câmpurile **Nume de familie** pe clientul potențial.
- O oportunitate pe bază de proiect care are câmpul **Tip** setat la **Bazat pe muncă**.

Pentru informații mai detaliate despre calificarea clienților potențiali, consultați [Calificați sau convertiți clienții potențiali](/dynamics365/sales-enterprise/qualify-lead-convert-opportunity-sales).

## <a name="lead-qualification-and-legal-entity-information"></a>Calificare client potențial și informații despre entitatea juridică 

Când rulați Project Operations utilizând modul de implementare, Project Operations pentru resurse/scenarii bazate pe stoc, fiecare client și oportunitate va necesita să aibă câmpul **Compania deținătoare** instalat. Compania deținătoare este o entitate juridică din organizația dvs. care deține livrarea proiectului. Fiecare client sau cont cu tip de relație de client trebuie să aibă valoarea de câmp **Compania deținătoare** setată la entitatea juridică care contractează și negociază cu acest client. Un client nu poate fi decât într-o singură persoană juridică.

Atunci când un client potențial este calificat, clientul și înregistrările de oportunitate create vor avea câmpul **Compania deținătoare** la compania înregistrării resurselor rezervabile ale utilizatorului curent.

Dacă înregistrarea resursei rezervabile a utilizatorului curent este goală, atunci valoarea câmpului **Compania deținătoare** din înregistrarea utilizatorului este utilizată ca setare implicită pentru client și înregistrările de oportunitate.

## <a name="business-process-flow-for-project-based-deals"></a>Flux de business pentru oferte bazate pe proiecte

Următoarele fluxuri de proces de afaceri sunt acceptate pentru tranzacții bazate pe proiecte în Project Operations:

- Client potențial la procesul de business oportunitate
- Proces de vânzări de oportunitate

Procesul de afaceri client la oportunitate susține următoarele etape:

| Nume de fază | Entitate mapată | Funcționalitate |
| --- | --- | --- |
| Calificare | Client potențial | Calificați clientul potențial pentru a crea un cont, o persoană de contact și o oportunitate. |
| Dezvoltare | Oportunitate | Dezvoltați oportunitatea de a adăuga mai multe informații despre activitatea implicată, părțile interesate cheie și concurența. |
| Propunere | Oportunitate | Elaborați propunerea și obțineți aprobarea de la echipa de revizuire internă. |
| Închideți | Oportunitate | Câștigați oportunitatea pentru a închide tranzacția. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]