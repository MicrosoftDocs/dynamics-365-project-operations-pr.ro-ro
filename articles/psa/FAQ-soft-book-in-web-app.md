---
title: Cum fac o „rezervare provizorie” de resurse în versiunea de aplicație 2.x?
description: Acest articol descrie cum se realizează o rezervare provizorie pentru membrii echipei de proiect cu Project Service.
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
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
ms.openlocfilehash: 472529c146fbb5e7a4540676c880cabd4ab1a32b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8585209"
---
# <a name="how-do-i-soft-book-resources-in-the-web-app-project-service-app-v2x"></a>Cum se realizează o rezervare provizorie de resurse în aplicația web (Project Service app v2.x)?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Aveți posibilitatea să programați provizoriu sau să faceți o rezervare provizorie a unei resurse pe o echipă de proiect pentru a vă arăta planul de alocare a resursei pentru un proiect. Rezervările provizorii nu consumă capacitatea disponibilă a resursei. Membrii echipei rezervați provizoriu nu pot fi atribuiți sarcinilor de proiect. Numai resursele cu statutul Rezervat ferm și tipul de comitere Comis pot fi atribuite sarcinilor (presupunând că au suficiente ore de rezervare fermă pentru a acoperi efortul de atribuire).

Membrii echipei de proiect rezervați provizoriu apar în grila Membru echipă cu orele de rezervare provizorie indicate în coloana Rezervare provizorie. Acestea apar, de asemenea, pe tabloul de planificare. De asemenea, acestea nu indică niciun consum de capacitate deoarece rezervarea provizorie nu consumă capacitatea unei resurse.

Există trei modalități de rezervare provizorie a unui membru al echipei pe un proiect cu Project Service versiunea 2.x. Puteți rezerva provizoriu prin tabloul de planificare, puteți utiliza caracteristica Menține rezervările, sau prin crearea unei resurse generice. Aceste metode sunt descrise mai jos.

## <a name="soft-book-with-the-schedule-board"></a>Rezervare provizorie cu tabloul de planificare

Pentru a rezerva provizoriu cu tabloul de planificare, urmați această procedură: 
1. Deschideți tabloul de planificare.
2. Selectați fila Proiect în partea de jos a panoului Rezervare cerințe a tabloului de planificare.
3. Găsiți proiectul pentru care doriți să rezervați provizoriu o resursă. Dacă aveți mai multe proiecte, faceți clic pe antetul coloanei proiectului și apoi utilizați filtrul pentru a găsi proiectului dumneavoastră.
4. Faceți clic pe proiect, apoi glisați și fixați-l pe grila de timp a resursei.
5. Acesta deschide panoul Creare rezervare resursă din partea dreaptă. Ajustați data de început și de sfârșit, selectați starea de rezervare ca provizorie și setați ora. 
6. Faceți clic pe Rezervare.
7. Înapoi la proiectul, resursa va arăta acum ca un membru al echipei cu orele rezervate provizoriu în coloana Rezervare provizorie.

Rețineți că nu le puteți atribui sarcini pe structura detaliată a proiectului (WBS) deoarece resursele trebuie să fie rezervare ferm pe echipă pentru a fi atribuite.

## <a name="soft-book-using-the-maintain-bookings-feature"></a>Rezervare provizorie utilizând caracteristica Menține rezervările

Pentru a rezerva provizoriu cu Menține rezervările, urmați această procedură:
1. Din grila membru echipă, faceți clic pe Nou.
2. Selectați resursa care poate fi rezervată, rolul, din/către.
3. Selectați o metodă de alocare, alta decât Niciuna:
- Capacitate completă
- Capacitate procentaj
- După ore - Distribuiți uniform
- După ore - Încărcare frontală
4. Faceți clic pe Salvare. Veți vedea resursa pe grila de echipă și orele lor indicate ca Ferm.
5. Mențineți rezervările resursei făcând clic pe Menține rezervările.
6. Atunci când tabloul de planificare se deschide, extindeți resursa pentru a arăta rezervările. Veți vedea rezervarea indicată ca Ferm.
7. Faceți clic dreapta pe rezervare, sub Modificare stare, selectați Rezervare provizorie și apoi Provizoriu. Starea rezervării este acum Provizorie.
8. După închiderea tabloului de planificare, veți vedea că orele pentru resurse s-au modificat de la Ferm la Provizoriu pe grila de membru de echipă.
Rețineți că dacă rezervați ferm o resursă pe echipă și apoi le atribuiți sarcini în WBS, atunci când utilizați Menține rezervările pentru a schimba starea de la Ferm la Provizoriu, se vor elimina atribuirile de la sarcini pentru această resursă, deoarece doar resursele rezervate ferm poate fi atribuite sarcinilor.

## <a name="soft-book-by-creating-a-generic-resource"></a>Rezervare provizorie prin crearea unei resurse generice

Puteți crea o rezervare provizorie prin generarea unei resurse generice membru echipă, procesând tabloul de planificare sau cerința de resurse și modificând tipul în timpul rezervării.
Pentru a face acest lucru, utilizați următoarea procedură:

1. În WBS proiect, atribuiți roluri sarcinilor pentru care doriți să generați membri echipă generici.
2. Faceți clic pe Generare echipă proiect.
3. Pe grila de membru al echipei de proiect, selectați resursa generică și faceți clic pe Rezervare.
4. Pe tabloul de planificare, selectați resursă pe care doriți să rezervați.
5. Pe panoul Creați rezervare resursă al tabloului de planificare, modificați starea la rezervare la Provizoriu.
6. Faceți clic pe Rezervare sau Rezervare și Ieșire.

După închiderea tabloului de planificare, veți vedea resursa selectată adăugată la echipă cu ore rezervate provizoriu precum și ore atribuite. De asemenea, veți vedea că resursa generică rămâne în echipă ca un indicator că sarcinile sunt atribuite unui membru al echipei rezervat provizoriu.

Când sunteți gata să modificați o resursă de membru echipă rezervat provizoriu la un membru echipă rezervat ferm, astfel încât să le puteți atribui sarcini, efectuați următoarele:

1. Selectați această resursă și faceți clic pe Menține rezervările.
2. Atunci când tabloul de planificare se deschide, extindeți resursa pentru a arăta rezervările. Veți vedea rezervarea marcată ca Provizorie.
3. Faceți clic dreapta pe rezervare, sub Modificare stare, selectați Rezervare fermă și apoi Ferm. Starea rezervării este acum Fermă.
4. După închiderea tabloului de planificare, veți vedea că orele pentru resurse s-au modificat de la Provizoriu la Ferm pe grila de membru de echipă. Acum puteți atribui resursa sarcinilor (cu condiția să existe aliniere între orele rezervate ferm și orele de efort ale sarcinii pentru atribuire). Rețineți că, dacă urmați pașii generici de procesare a resurselor de la punctul #3 de mai sus, atunci când schimbați starea resurselor care se pot rezerva de la provizoriu la ferm, membrul echipei generice este eliminat din echipă.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
