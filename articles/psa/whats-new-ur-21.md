---
title: Ce este nou sau schimbat în Project Service Automation versiunea actualizată 21, V3
description: Acest subiect listează caracteristicile și corecțiile care sunt disponibile în Project Service Automation V3, versiunea actualizată 21, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
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
ms.openlocfilehash: 799be481c365e82e8ffb59ba242e30378644008b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4126723"
---
# <a name="project-service-automation-update-release-21-v3"></a>Project Service Automation, versiunea actualizată 21, V3

Suntem încântați să anunțăm cea mai recentă actualizare pentru aplicația Project Service Automation pentru Dynamics 365. Această versiune include câteva îmbunătățiri importante ale calității, performanței și utilizabilității. Această versiune este compatibilă cu Dynamics 365 9.x. Pentru a actualiza această versiune, accesați Centrul de administrare pentru Dynamics 365, pagina de soluții online pentru a instala actualizarea. Pentru informații suplimentare, consultați: [Instalarea, actualizarea sau eliminarea unei soluții preferate](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Acest subiect listează caracteristicile și corecțiile care sunt noi sau modificate pentru Project Service Automation V3, versiunea actualizată 21. Această versiune are un număr de versiune V 3.10.32.50 și este disponibil în general printr-o autoactualizare în iunie 2020.

## <a name="update-release-21"></a>Lansarea de actualizări 21

### <a name="bug-fixes"></a>Remedieri de erori

**Timp și cheltuială**

S-au remediat următoarele probleme:

- La găzduirea **Control grilă introducere timp** în tablouri de bord, grila nu utilizează lățimea completă a containerului grilei tabloului de bord.
- Pentru anumite zone orare, controlul grilei **Intrare de timp** nu afișează înregistrări.
- Înregistrările orare care sunt după ora 21:00 apar în ziua greșită.
- Utilizatorii nu pot depune cheltuieli dacă categoria de cheltuieli, **Chitanța de cheltuială necesară** nu are nicio valoare.

**Gestionarea resurselor**

S-au remediat următoarele probleme:

- Rezervările inactive sunt afișate în vizualizarea **Reconciliere**.
- Lipsa de validare a resurselor generice a lipsit pentru a se asigura că există o stare de rezervare valabilă.

**Gestionare de proiect**

S-au remediat următoarele probleme:

- Grilele formularului **Proiect** (**Atribuirea resurselor**, **Activitate**, vizualizarea **Reconciliere**, **Estimarea cheltuielilor**) rămân editabile chiar și atunci când un proiect nu este activ.
- Clienții duplicat nu pot fi îmbinați cu clienții care sunt legați de contractele de proiect confirmate.
- Când se adaugă o resursă care nu are un calendar valid, sistemul nu returnează un mesaj de eroare de utilizator.
- Butonul **Adăugați activitate** de pe grila de activități este activat atunci când proiectul este conectat **Program de completare Microsoft Project**.
- Efortul crește incontrolabil atunci când o sarcină cu o categorie este atribuită unei resurse cu un rol pentru care este definit un preț de cost.

**Sales**

Au fost realizate următoarele îmbunătățiri:

- **Frecvența facturilor** și **Startul facturării** au fost mutați în fila **Planificarea facturilor**.

S-au remediat următoarele probleme:

- **Preț total de vânzare** este zero (0) pentru **Categorie** chiar dacă **Rol** are un preț total de vânzare care nu este zero.
- Clienții nu pot modifica valoarea câmpului **Starea facturii** la **Gata pentru facturare** când un alt proces personalizat actualizează un câmp suplimentar.
- Butonul **Actualizați liniile de factură** poate crea mai multe linii duplicate dacă este selectat în mod repetat.
- Butonul **Actualizați prețurile** nu funcționează pe subgrila **Prețurile rolului** în formularul **Vizualizare rapidă**.
- Logica **Rezolvare listă prețuri de vânzare** gestionează în mod necorespunzător zonele orare, rezultând în selecția incorectă a listelor de prețuri.
- **Costul real total** al unui proiect poate fi decalat cu o sumă fracționată după aprobarea unei singure intrări.
- Logica **Rezoluția prețurilor** nu oferă un mesaj de eroare ușor de utilizat dacă **Preluare RolePrice** nu are valori în câmpurile **„Unitate primară”** și **„Preț în unitatea primară”**.
