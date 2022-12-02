---
title: Rezervarea provizorie a unei resurse
description: Acest articol oferă informații despre cum se realizează o rezervare provizorie pentru membrii echipei de proiect.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 9/25/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.app:
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 6c666e5c0a83a3d1b440144a62cbd58a58c5db81
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929137"
---
# <a name="soft-book-a-resource"></a>Rezervarea provizorie a unei resurse

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Aveți posibilitatea să programați provizoriu sau să faceți o rezervare provizorie a unei resurse pe o echipă de proiect pentru a vă arăta planul de alocare a resursei pentru un proiect. Rezervările provizorii nu consumă capacitatea disponibilă a unei resurse și aveți posibilitatea să asociați membrii echipei rezervați provizoriu pentru activitățile proiectului. Cu toate acestea, deoarece rezervarea provizorie nu consumă capacitatea unei resurse, puteți „rezerva ferm” resursa pentru alte sarcini în același interval. Resursele generice nu pot fi rezervate provizoriu, respectiv o rezervare provizorie nu poate îndeplini o solicitare pentru o resursă generică.

Membrii echipei de proiect rezervați provizoriu sunt enumerați pe fila **Echipă** de pe pagina **Proiect**, cu orele rezervate provizoriu afișate în coloana **Ore rezervate provizoriu** în vizualizarea **Resurse menționate**. Membrii echipei rezervați provizoriu sunt listați, de asemenea, pe tabloul de planificare. Deoarece aceștia sunt rezervați provizoriu, tabloul de planificare nu arată niciun consum de capacitate pentru aceste resurse. Timpul rezervat provizoriu nu apare în fila **Reconciliere**, nici nu este indicat în câmpul **Extindere rezervări** din fila **Reconciliere** a panoului de planificare. 

Există două modalități de a rezerva un membru al echipei pe un proiect: direct din tabloul de planificare sau prin adăugarea membrului echipei în fila **Echipă**. 

## <a name="soft-book-from-the-schedule-board"></a>Rezervare provizorie din panoul de planificare
Parcurgeți pașii următori pentru a rezerva provizoriu o resursă din tabloul de planificare. 

1. Deschideți Panoul de planificare, apoi panoul **Cerințe de rezervare**, selectați fila **Proiect**.
2. Găsiți un proiect pentru care doriți să rezervați provizoriu o resursă. Dacă există un număr mare de proiecte în listă, selectați antetul coloanei **Proiect**, apoi utilizați filtrul pentru a căuta unul sau mai multe proiecte.
3. Selectați proiectul, apoi glisați-l și fixați-l în grila de timp a resursei.
5. În panoul **Creați o rezervare de resurse**, ajustați data de început și de sfârșit, setați **Stare rezervare** la **Provizoriu**, apoi setați orele. 
6. Faceți clic pe **Rezervare**. Resursa arată acum în fila **Echipă** ca o resursă pentru proiect. Pe vizualizarea **Membru echipă menționat** veți vedea orele rezervate provizoriu în coloana **Ore rezervate provizoriu**.

> [!NOTE]
> Aveți posibilitatea să atribuiți acum elementele rezervate provizoriu la sarcinile de pe fila **Planificare**. Pe fila **Reconciliere**, resursa prezintă un deficit de rezervare față de atribuirea sarcinii deoarece fila **Reconciliere** ia în calcul doar rezervările ferme. Puteți utiliza caracteristica **Extindere rezervări** pentru rezervarea fermă a resursei pentru eliminarea deficitului de rezervări ferme în raport cu atribuirile de resurse. Va trebui să anulați manual rezervarea provizorie pentru resursă utilizând **Menține rezervările**.

## <a name="soft-book-on-the-team-tab"></a>Rezervare provizorie pe fila Echipă

Puteți să adăugați membrii echipei direct pe fila **Echipă** și apoi modificați statutul lor de rezervare de la **Ferm** la **Provizoriu** cu **Menține rezervările**. Când adăugați un membru al echipei în acest mod, va avea întotdeauna drept consecință o rezervare fermă, cu excepția cazului în care selectați metoda de alocare **Niciuna**.

Pentru a utiliza această metodă, parcurgeți următorii pași.

1. Pe pagina **Proiect**, în fila **Echipă**, faceți clic pe **Nou**.
2. Afișează resursa rezervabilă, rolul și datele de la și până la.
3. Selectați o metodă de alocare, alta decât **Niciuna**.
4. Selectați **Salvare**. Veți vedea resursa pe grilă și orele în coloana **Ore rezervate ferm**.
5. Mențineți rezervările resursei selectând **Menținere rezervări**.
6. Pe tabloul de planificare, extindeți resursa pentru a arăta rezervările. Veți vedea rezervarea afișată ca **Ferm**.
7. Faceți clic dreapta pe rezervare și la **Modificare stare**, selectați **Rezervare provizorie** \> **Provizoriu**. Starea rezervării este acum **Provizoriu**.
8. După închiderea taboului de planificare, veți vedea că orele pentru resursă s-au mutat din coloana **Ore rezervate ferm** în **Ore rezervate provizoriu** pe grila filei **Echipă** când vă uitați la vizualizarea **Membri echipă numiți**.

> [!NOTE]
> Când utilizați **Menținere rezervări** pentru a modifica starea din **Ferm** în **Provizoriu**, dacă rezervați ferm o resursă pe echipă și apoi le atribuiți activități în resursă, atribuirile de activități pentru resursă sunt menținute. Cu toate acestea, pe fila **Reconciliere**, resursa va avea un deficit de rezervare deoarece doar rezervările ferme sunt luate în calcul atunci când sunt reconciliate rezervările față de atribuiri. Puteți utiliza caracteristica **Extindere rezervări** pe fila **Reconciliere** pentru a rezerva ferm resursa pentru eliminarea deficitului de rezervări ferme în raport cu atribuirile de resurse. Va trebui să anulați rezervarea provizorie pentru resursă utilizând **Menține rezervările**.

Când sunteți gata să modificați o resursă de membru echipă rezervat provizoriu la un membru echipă rezervat ferm, efectuați următoarele:

1. Pe tabloul de planificare, extindeți resursa pentru a arăta rezervările. Veți vedea rezervarea afișată ca **Provizoriu**.
2. Faceți clic dreapta pe rezervare și la **Modificare stare**, selectați **Rezervare fermă** \> **Ferm**. Starea rezervării este acum **Ferm**.
3. După închiderea taboului de planificare, reveniți la proiect și deschideți fila **Echipă**, și veți vedea că orele pentru resursă s-au mutat din coloana **Ore rezervate provizoriu** în **Ore rezervate ferm** pe grila filei **Echipă** când vă uitați la vizualizarea **Membri echipă numiți**. Dacă resursa a fost atribuită la sarcini, acestea nu vor mai prezenta un deficit de rezervare pe fila **Reconciliere** deoarece rezervările lor sunt acum ferme.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
