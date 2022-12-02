---
title: Planificarea externă
description: Acest articol oferă informații despre planificarea externă.
author: ruhercul
ms.date: 10/31/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 746fb3a7c812b2b387ec707e58796d02d2473847
ms.sourcegitcommit: b1a5b9bb8b826678fc52f1d5a3d199a71caccb0a
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 11/03/2022
ms.locfileid: "9736992"
---
# <a name="external-scheduling"></a>Planificarea externă

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Modul de planificare externă vă permite să creați, să actualizați și să ștergeți în mod nativ entități care sunt legate de structurile de defalcare a lucrărilor (WBS), dar fără limitele actuale impuse de Microsoft Project for the Web. De asemenea, oferă validare limitată. Acest mod ar trebui utilizat numai de următorii clienți:

- Clienții care au instrumentele necesare pentru a defini un WBS în afara logicii de planificare furnizate de Project Operations
- Clienții care trebuie să gestioneze ierarhia programelor, dependențele sau durata sarcinii

> [!IMPORTANT]
> Este posibil ca datele care nu sunt introduse corect în entitățile legate de WBS să nu fie redate în grila de reconciliere a resurselor, grila de estimări, grila de urmărire sau grila de alocare a resurselor.

## <a name="configuration"></a>Configurație

Această caracteristică este activată în mod implicit. Cu toate acestea, pe pagina principală predefinită pentru proiecte, câmpul aferent nu este vizibil în mod implicit. Pentru a activa câmpul, în Maker portal, deschideți pagina principală pentru entitatea de proiect, selectați câmpul **Motor de programare**, apoi schimbați câmpul în **Vizibil implicit**. Dacă nu utilizați pagina principală predefinită a proiectului, editați pagina existentă și adăugați câmpul **Motor de programare** la aceasta.

## <a name="settings"></a>Setări

Pentru a utiliza modul de programare externă, trebuie mai întâi să creați un nou proiect și să selectați motorul de programare **Programat extern** în lista derulantă de pe pagina principală a proiectului. După ce acest mod a fost configurat pentru un proiect, nu poate fi schimbat.

## <a name="viewing-the-wbs"></a>Vizualizarea WBS

Dacă un proiect este programat extern, accesul la Project for the Web este restricționat pentru acel proiect. Pentru a vizualiza WBS, trebuie să mergeți la grila de urmărire, unde este afișat WBS complet.

## <a name="creating-and-editing-the-wbs"></a>Crearea și editarea WBS

Dacă programarea externă este activată pentru un proiect, trebuie să definiți datele pentru toate entitățile legate de WBS, inclusiv sarcinile, membrii echipei, alocarea resurselor și dependențele.

Următoarea ilustrație prezintă modelul de date pentru planificarea proiectului.

![Model de date de planificare a proiectului.](media/projectplanningdatamodel.png)

## <a name="functional-limitations"></a>Limitări funcționale

Următoarele operațiuni nu sunt permise pentru proiectele programate extern.

### <a name="project-planning"></a>Planificarea unui proiect

- **Copiere proiect** – Această operațiune nu este acceptată în proiectele planificate extern.
- **Mutare proiect** – Modificările datei de începere a unui proiect nu vor muta începutul sarcinilor sau alocărilor de resurse în WBS.
- **Actualizarea managerului de proiect** – Modificările aduse managerului de proiect de pe pagina principală a proiectului nu vor crea automat un nou membru al echipei de proiect până când proiectul nu este convertit.
- **Actualizarea șablonului de oră de lucru al proiectului** – Modificările aduse șablonului de oră de lucru al proiectului nu vor recalcula programul proiectului.
- **Contururi de alocare a resurselor** – Crearea atribuirilor de resurse nu va actualiza automat câmpul **mdyn\_PlannedWork**. Acest câmp este folosit pentru a stoca contururi pentru efortul de alocare a resurselor. Dacă afișați efortul în etape în timp în grila de alocare a resurselor sau în grila de reconciliere a resurselor, trebuie să definiți contururi de alocare a resurselor valide. Aceste contururi trebuie să fie formatate corect, astfel încât să declanșeze calculul atât al contururilor de cost, cât și al contururilor prețului de vânzare. Vă recomandăm să creați un proiect de testare care este programat de Project for the Web și apoi să examinați datele asociate pentru a confirma cerințele și formatarea.

### <a name="resource-management"></a>Gestionarea resurselor

- **Îndeplinirea resurselor generice** – Îndeplinirea resurselor generice nu este acceptată pentru proiectele programate extern. Încercările de a îndeplini cerințele deschise active vor crea noi membri ai echipei de proiect, dar nu va șterge membrul generic al echipei și nu îl va înlocui pe membrul generic al echipei în nicio atribuire de resurse existente.
- **Ștergere membru echipă** – Ștergerea unui membru al echipei nu va șterge automat atribuirile de resurse.

### <a name="quoting-and-contracting"></a>Ofertarea și contractarea

- **Importarea detaliilor liniei de cotație și liniei de contract** – Atunci când detaliile liniei de ofertă sau de contract sunt importate dintr-un proiect, aplicația a fost testată pentru a suporta maximum 500 de sarcini în WBA, pe baza unei limite de 20 de atribuiri per sarcină.

### <a name="actuals-and-invoicing"></a>Valori reale și facturare

- Deși nu există modificări ale validărilor existente între WBS și tranzacțiile financiare, este important să vă conformați modelului de date predefinite, pentru a vă asigura că toate tranzacțiile din aval rulează conform așteptărilor.
