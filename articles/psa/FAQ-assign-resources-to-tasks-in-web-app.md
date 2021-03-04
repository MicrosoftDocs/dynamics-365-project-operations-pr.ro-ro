---
title: Cum atribui o resursă care se poate rezerva unei activități în aplicația web
description: Prezentare generală a modurilor în care puteți atribui resurse care pot fi rezervate.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 27a93c41243f300cadb632c697672180e5a3817b
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146588"
---
# <a name="how-do-i-assign-a-bookable-resource-to-a-task-in-the-web-app-project-service-app-v2x"></a>Cum atribui o resursă care se poate rezerva unei sarcină în aplicația web (aplicația Project Service v2.x)?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Există două modalități de a atribui o resursă unei sarcini în Project Service. Puteți rezerva o resursă ca un membru al echipei și apoi să o atribuiți la o sarcină. Sau puteți că creați un membru al echipei generic prin intermediul atribuirii rolurilor pe sarcini, să generați o echipă și apoi să îndepliniți cerințele subiacente cu o resursă desemnată.

Rețineți că dacă doriți să atribuiți o resursă care se poate rezerva la o sarcină, membrul echipei de resurse care se poate rezerva trebuie să aibă rezervări suficiente disponibile. Starea rezervării trebuie să fie Tip comitere Rezervare fermă și Stare Comisă. În cazul în care nu există suficiente rezervări pentru resursă, Project Service elimină alocarea și afișează următorul mesaj de eroare:

*Imposibil de alocat resursa la sarcină - Următoarea/ următoarele resurse nu are/au suficiente ore rezervate pe proiect*

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a>Rezervați o resursă ca un membru al echipei și apoi atribuiți resursa la o sarcină.

Cu această metodă adăugați o resursă la echipa proiectului și apoi atribuiți sarcini resursei în planificarea proiectului. Iată cum se face:
1.  Pe grila de membru echipă, adăugați un nou membru al echipei selectând **Nou**.
2.  Pe ecranul Creare rapidă membru echipă, selectați numele resursei care se poate rezerva și setați un rol.
3.  Selectați datele **De la** și **Până la**.

    > [!div class="mx-imgBorder"] 
    > ![Captura de ecran a adăugării membrilor echipei](media/FAQ-Resources-to-Tasks2-1.png "Captura de ecran a adăugării membrilor echipei")
 
4.  Selectați una dintre următoarele metode de alocare pentru a rezerva resursa:
    - **Capacitate completă** rezervă întreaga capacitate a resursei pentru datele de pornire și finalizare indicate.
    - **Capacitate procentaj** rezervă resursa pentru un procent din capacitatea resursei pentru datele de pornire și finalizare indicate.
    - **După ore - Distribuiți uniform** rezervă resursa pentru un anumit număr de ore, distribuind-o uniform pe zi intre datele de început și sfârșit indicate.
    - **După ore - Încărcare frontală** rezervă resursa pentru un anumit număr de ore, încărcând frontal timpul pe zi între datele de început și sfârșit indicate.

    Nu selectați **Niciuna**, deoarece acest lucru adaugă resursa la echipă, dar nu creează rezervări care să absoarbă capacitatea resursei.
5.  Selectați **Salvare**.

    Rețineți că orele rezervării trebuie să fie suficiente pentru a acoperi orele de efort si intervalele de dată de ale sarcinilor pentru care atribuiți această resursă. În cazul în care acestea nu sunt aliniate, nu puteți asocia resursa la sarcină.

6.  Pentru structura detaliată a proiectului (WBS) pentru sarcină, faceți clic pe lista verticală din celula resursei. Apoi: 

    1. Selectați **Adăugare**.
    2. Selectați lista derulantă de sub **Resurse** și selectați membrul de echipă adăugat anterior.
    3. Selectați **OK**. Membrul echipei este acum atribuit la sarcină.

    > [!div class="mx-imgBorder"] 
    > ![Screenshot de adăugare a resurselor cu WBS](media/FAQ-Resources-to-Tasks2-2.png "Screenshot de adăugare a resurselor cu WBS")
 
Pe grila de membru echipă, veți vedea totalul orelor atribuite ale resursei, sub Ore alocate. Acesta va fi mai mic sau egal cu orele rezervate pentru resursă. 

> [!div class="mx-imgBorder"] 
> ![Captură de ecran cu ore alocate pentru o resursă](media/FAQ-Resources-to-Tasks2-3.png "Captură de ecran cu ore alocate pentru o resursă")
 
În cazul în care sarcina pe care încercați să o atribuiți resursei începe după data de sfârșit a rezervărilor pentru de resursă, resursa nu va apărea în lista derulantă.

Rețineți că aveți posibilitatea să îi atribuiți unei resurse mai multe ore decât orele lor rezervate dacă resursa are capacitate rămasă neatribuită. În acest caz resursa va doar fi parțial atribuită, în funcție de rezervări. Puteți vedea aceste ore de sarcini rămase neatribuite prin adăugarea coloanei Ore neacoperite de personal la structura detaliată a proiectului.

În cazul în care resursele sunt atribuite la orele lor rezervate (orele lor rezervate sunt egale cu orele lor atribuite), veți vedea următorul mesaj de eroare atunci când încercați să le atribuiți alte sarcini:

*Imposibil de alocat resursa la sarcină - Următoarea/ următoarele resurse nu are/au suficiente ore rezervate pe proiect.*

În plus, membrul echipei care este managerul implicit de proiect care este adăugat la echipă atunci când creați proiectul este adăugat fără rezervări și nu îi pot fi atribuite sarcini. Aceștia nu apar în lista verticală de resurse pentru sarcini.

În cazul în care doriți să atribuiți această resursă, trebuie să le scoateți din echipă și apoi să le adăugați din nou cu o metodă de alocare diferită de Niciuna. Motivul pentru care acestea sunt adăugate la echipă atunci când este creat proiectul este ca fiecare proiect să aibă cel puțin o persoană implicită care face aprobarea.

## <a name="create-a-generic-team-member-through-role-assignment-on-tasks"></a>Creați un membru generic al echipei prin atribuirea de roluri pe sarcini

Această metodă asigură că resursele au suficiente rezervări pentru sarcini. Mai întâi, creați un substituent sau o resursă generică care descrie caracteristicile resursei care doriți să lucreze la final pe sarcini, prin generarea unei echipe după atribuirea rolurilor la sarcini. Iată cum se face:

1. Selectați o sarcină pe structura detaliată a proiectului.
2. Selectați pictograma derulantă **Rol atribuit** din celula resursei.
3. Selectați lista derulantă **Rol** și selectați rolul pentru resursa generică.
4. Selectați **OK**.

    > [!div class="mx-imgBorder"] 
    > ![Captură de ecran a utilizării WBS pentru a adăuga o resursă](media/FAQ-Resources-to-Tasks2-4.png "Captură de ecran a utilizării WBS pentru a adăuga o resursă")
 
Odată ce ați completat atribuirea de roluri la sarcini în WBS, selectați **Generare echipă de proiect**. Project Service creează numărul minim de membri ai echipei generice pe baza rolurilor, a unităților organizaționale din care provin resursele și a calendarului de proiect prin agregarea atribuirilor de sarcini.

> [!div class="mx-imgBorder"] 
> ![Captură de ecran a echipei de generare a proiectului](media/FAQ-Resources-to-Tasks2-5.png "Captură de ecran a echipei de generare a proiectului")
 
Pr grila de Membru al echipei, veți vedea resursele de tip Resursă generică cu rolul și numele poziției. În cazul în care sunt necesare două resurse pentru un rol pentru a finaliza lucrările, caracteristica Generare echipă creează doi membri ai echipei și utilizează numele poziției pentru a-i diferenția.

> [!div class="mx-imgBorder"] 
> ![Captură de ecran cu adăugarea a două resurse generice](media/FAQ-Resources-to-Tasks2-6.png "Captură de ecran cu adăugarea a două resurse generice")
 
Puteți deschide cerința de resurse subiacente pentru membrul generic de echipă prin selectarea link-ul de la Cerință de resurse.

> [!div class="mx-imgBorder"] 
> ![Captură de ecran cu cerința de deschidere de resurse subiacente](media/FAQ-Resources-to-Tasks2-7.png "Captură de ecran cu cerința de deschidere de resurse subiacente")

Selectați **Rezervare** pentru resursa generică și apoi puteți folosi tabloul de planificare pentru a găsi și rezerva o resursă reală. Puteți trimite solicitarea de realizare de către un manager de resurse, selectând **Remite solicitare**.

Când resursa generică este îndeplinită cu o anumită resursă, resursa generică este scoasă din echipă și atribuirile de sarcini pentru resursa generică sunt atribuite resursei indicate care a îndeplinit cerința de resurse a resursei generice.
 



[!INCLUDE[footer-include](../includes/footer-banner.md)]