---
title: Întrebări frecvente de gestionarea resurselor
description: Acest subiect oferă răspunsuri la întrebările frecvente despre gestionarea resurselor.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: 20562b98ccc8451ab57dd42fb8c2f9f303811dbe
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5283158"
---
# <a name="resource-management-faq"></a>Întrebări frecvente de gestionarea resurselor

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

## <a name="what-is-the-difference-between-a-team-member-and-a-resource-requirement"></a>Care este diferența dintre un membru al echipei și o cerință de resurse?

Un membru al echipei de proiect poate fi atribuit la activități, rezervat sau supra-rezervat și poate fi setat ca aprobator. O cerință de resurse poate exista fără un membru al echipei de proiect, ca o notă de proiect de cerere. 

## <a name="what-is-the-difference-between-proposed-and-soft-booked-hours"></a>Care este diferența dintre orele propuse și cele cu rezervare provizorie?

Orele propuse și orele de rezervate provizoriu diferă ca vizibilitate. Orele propuse sunt vizibile numai pentru managerii de resurse și managerul de proiect care a inițiat cererea utilizând o solicitare de resurse. Orele rezervate provizoriu sunt vizibile pentru oricine are acces la panoul de planificare.

## <a name="how-can-i-see-the-soft-booked-hours-for-resources-on-a-team"></a>Pot vedea orele de rezervate provizoriu pentru resurse într-o echipă?

Rezervările provizorii pot fi făcute când vă rezervați o cerere de resurse. Resursele care sunt rezervate provizoriu într-o echipă de proiect apar ca membri ai echipei care au ore cu rezervare provizorie. Acestea apar, de asemenea, pe tabloul de planificare.

## <a name="how-do-i-change-the-required-hours-and-the-start-and-end-dates-for-a-resource-generic-or-named-that-i-booked"></a>Cum modific orele necesare și datele de început și de sfârșit pentru o resursă (generică sau denumită) pe care am rezervat-o?

După ce resursele sunt rezervate, selectați **Menținere rezervări** pentru a face orice modificări necesare.

## <a name="what-resources-types-does-project-service-automation-support"></a>Ce tipuri de resurse suportă Project Service Automation?

**Utilizator** și **Persoană de contact** sunt singurele tipuri de resurse care sunt acceptate în Dynamics 365 Project Service Automation. Deși puteți crea alte tipuri de resurse (de exemplu, **Echipamente** și **Grupuri**), nu este acceptat niciun caz de utilizare completă pentru ele.

## <a name="what-is-the-difference-between-an-assignment-and-a-booking"></a>Care este diferența dintre o atribuire și o rezervare?

Atribuirile sunt alocarea de resurse pentru activitățile de proiect în planificarea proiectului. Resursele pot fi reale sau generice. Rezervările sunt alocarea fermă sau provizorie de resurse pentru un proiect. Rezervările ferme consumă capacitatea unei resurse. În mod ideal, pentru resurse reale, rezervările și atribuirile ar trebui să fie în acord, deoarece acestea nu diferă. Cu toate acestea, PSA nu pune în aplicare acest acord. Vizualizarea Reconciliere arată unui manager de proiect locurile în care rezervările și atribuirile unei resurse nu sunt de acord.


[!INCLUDE[footer-include](../includes/footer-banner.md)]