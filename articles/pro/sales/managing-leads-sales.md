---
title: Gestionarea clienților potențiali - simplificat
description: Acest subiect furnizează informații despre gestionarea clienților potențiali pe bază de proiect (pro).
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5e789295d4b1f5a53fcf179a2998f60d35f48f99
ms.sourcegitcommit: 869bde007805ef255f61b03937e4a44aeef61df9
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 11/12/2020
ms.locfileid: "4513804"
---
# <a name="manage-leads---lite"></a>Gestionarea clienților potențiali - simplificat

_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_

Oportunitățile bazate pe proiect pot fi gestionate și calificate în Project Operations. Procesul de gestionare a clienților potențiali include crearea de clienți potențiali pe bază de muncă și calificarea acestora. 

## <a name="list-of-project-sales-leads"></a>Lista clienților potențiali în de Proiect

În secțiunea **Vânzări**, în panoul de navigare din stânga, deschideți pagina listă **Clienți potențiali** pentru a vizualiza o listă cu toate înregistrările potențiale din sistem. Oportunitățile din listă sunt bazate pe lucru și alte tipuri de oportunități care pot fi create dacă aveți și aplicațiile Dynamics 365 Sales sau Dynamics 365 Field Service.

Puteți crea o vizualizare filtrată pentru a vedea numai clienți potențiali bazate pe proiecte, creând un filtru pe valoarea **Tip**. De exemplu, puteți selecta să afișați numai clienți potențiali pe bază de muncă.

## <a name="creating-a-new-lead-for-a-project-based-deal"></a>Crearea unui nou client potențial pentru o afacere bazată pe proiecte

Când un client bazat pe proiect este calificat, se creează o oportunitate și un cont. O oportunitate bazată pe proiect este punctul de plecare pentru activitățile de urmărire a vânzărilor în faza oportunitate. Oportunitățile bazate pe proiecte au capacități unice care sunt necesare pentru vânzarea lucrărilor de proiect. Aceste funcții includ:

- Metode de facturare pentru timp și material și preț fix
- Liste de prețuri cu date multiple pentru resurse umane, cheltuieli și materiale suportate în cadrul proiectelor.

Pentru ca un potențial calificat să creeze automat o oportunitate, setați atributul **Tip** la **Bazat pe muncă** atunci când creați clientul potențial. Dacă alegeți un alt tip, clientul potențial nu va crea o oportunitate bazată pe proiect atunci când este calificat. Dacă oportunitatea bazată pe proiect nu este creată, capacitățile specifice proiectului nu vor fi disponibile în procesele de vânzare din aval.

Tabelul următor include informații importante de câmp pentru un potențial și implicațiile din aval ale acestor câmpuri.

| **Câmp** | **Locaţie** | **Descriere** | **Impactul din aval** |
| --- | --- | --- | --- |
| Subiect | Fila General | Acest câmp text și ar trebui să conțină o scurtă descriere a tranzacției. | Subiectul clientului potențial va fi implicit ca subiect al oportunității și numele contractului de ofertă și proiect. |
| Tip | Fila General | Acest câmp set de opțiuni are următoarele opțiuni:</br>- Pe bază de muncă (disponibil numai când este instalat Project Operations)</br>- Pe bază de element (disponibil numai atunci când sunt instalate Project Operations și Vânzări)</br>- Serviciu bazat pe întreținere (disponibil când este instalat Field Service) | Când valoarea acestui câmp este setată la **Pe bază de muncă** pe clientul potențial, acesta este calificat pentru a crea o oportunitate bazată pe proiect. O oportunitate pe bază de proiect este necesară pentru a permite toate extensiile și funcționalitățile specifice proiectului în procesul de vânzare din aval pentru această tranzacție. |
| Prenume | Fila General | Prenumele persoanei de contact ale clientului prospectat | Când clientul potențial este calificat, sunt create un cont, persoană de contact și oportunitatea. Prenumele persoanei de contact este valoarea stabilită aici. |
| Nume | Fila General | Numele de familie al persoanei de contact ale clientului prospectat | Când clientul potențial este calificat, sunt create un cont, persoană de contact și oportunitatea. Numele de familie al persoanei de contact este valoarea stabilită aici. |
| Companie | Fila General | Numele companiei clientului prospectați | Când clientul potențial este calificat, sunt create un cont, persoană de contact și oportunitatea. Numele contului creat este valoarea stabilită aici. |
| Monedă | Fila Detalii | Moneda clientului potențial | Când clientul potențial este calificat, sunt create un cont, persoană de contact și oportunitatea. Moneda contului creat este valoarea stabilită aici. |

## <a name="qualify-a-new-project-based-lead"></a>Calificați un nou client potențial bazat pe proiecte

Clienții potențiali care au valoarea **Tip** setată la **Bazat pe muncă** sunt numiți clienți potențiali pe bază de proiect. Când un potențial bazat pe proiect este calificat, se creează următoarele:

- Un cont care utilizează câmpul **Companie** din clientul potențial.
- O înregistrare de contact asociată contului pe baza valorilor din **Prenume** și câmpurile **Nume de familie** pe clientul potențial.
- O oportunitate pe bază de proiect care are câmpul **Tip** setat la **Bazat pe muncă**.

Pentru informații mai detaliate despre calificarea clienților potențiali, consultați [Calificați sau convertiți clienții potențiali](https://docs.microsoft.com/dynamics365/sales-enterprise/qualify-lead-convert-opportunity-sales).

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
