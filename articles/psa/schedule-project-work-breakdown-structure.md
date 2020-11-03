---
title: Planificarea unui proiect cu o structură detaliată a proiectului
description: Cum să planificați un proiect cu o structură detaliată a proiectului în Project Service
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: d77d9f8427f06015d4f4cb9438d7f59ac840b061
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082978"
---
# <a name="schedule-a-project-with-a-work-breakdown-structure-project-service"></a>Planificarea unui proiect cu o structură detaliată a proiectului (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

O planificare de proiect comunică ce lucru trebuie să fie efectuat, ce resurse vor efectua lucrul și intervalul de timp în care trebuie să fie efectuat lucrul. Planificarea proiectului reflectă tot lucrul asociat cu livrarea proiectului la timp. Unul dintre primii pași din faza de inițiere a proiectului este livrarea unei planificări de proiect. Pentru a stabili o planificare de proiect, trebuie să creați o structură detaliată a proiectului.  
  
 Creați o structură de proiect cu o structură detaliată a proiectului, care vă ajută să:  
  
- Scindați lucrul în activități gestionabile  
  
- Estimați timpul necesar pentru a finaliza o activitate  
  
- Setați dependențele pentru activități și durata activităților  
  
- Determinați rolurile necesare pentru finalizarea fiecărei activități  
  
  Planificarea proiectului în structura detaliată a proiectului are un aspect și un stil familiar, completat cu o diagramă Gantt interactivă.  
  
## <a name="create-a-work-breakdown-structure-for-a-project"></a>Creați o structură detaliată a proiectului pentru un proiect  
 Creați o structură detaliată a proiectului pentru a reprezenta secvența de activități dintr-un proiect. Structură detaliată a proiectului include activitățile, cerințele pentru fiecare activitate și informațiile despre venituri și costuri. În structură detaliată a proiectului, aveți posibilitatea să adăugați:  
  
-   Succesiunea de activități dintr-o ierarhie  
  
-   Alte activități, dacă există, care trebuie să fie finalizate înainte de începerea activității  
  
-   Data de început, data de sfârșit și durata unei activități  
  
-   Numărul de ore necesare pentru o activitate  
  
-   Orice abilități și educația necesare pentru un angajat  
  
-   Angajații cărora li s-a atribuit o activitate  
  
-   Venitul și costurile estimate  
  
## <a name="task-types"></a>Tipuri de activitate  
Veți utiliza următoarele tipuri de activități atunci când creați structura detaliată a proiectului:  

| | | 
|---------------------------------------|-----------------------------------------------------------------| 
| **Nodul rădăcină al proiectului** | Activitatea rezumat de nivel superior pentru proiect. Toate celelalte activități de proiect create în cadrul acestuia. Numele activității rădăcină este numele proiectului. Efortul, datele și durata nodului rădăcină se bazează pe valorile din ierarhia de sub acesta. Nu puteți edita proprietățile nodului rădăcină sau șterge nodul rădăcină. | 
| **Activități rezumat sau container** | O activitate rezumat este o activitate care are subactivități. O activitate rezumat nu are niciun efort de lucru sau cost propriu. Efortul său de lucru și costurile sunt un cumul al subactivităților. Puteți schimba numele unei activități de rezumat, dar nu puteți modifica efortul, datele sau durata, deoarece acestea sunt calculate automat. Ștergerea unei activități de rezumat șterge activitatea și toate subactivitățile ei.|  
| **Activitățile nodului frunză** | O activitate nod frunză reprezintă lucrul cel mai detaliat la proiect. Include o estimare a efortului, un număr de resurse planificate, datele de început și de sfârșit planificate și o durată.|

  
## <a name="task-hierarchy"></a>Ierarhia de activități  
 Aveți următoarele opțiuni atunci când creați o ierarhie de activități:  
  
- **Adăugați activitatea**.   Puteți adăuga o activitate la o poziție pe care o alegeți în ierarhia de activități. Dacă nu selectați o poziție, activitatea nouă apare la sfârșit.  
  
- **Indentați activitatea**.   Indentați o activitate pentru a o face subordonată activității aflate direct deasupra ei.  
  
- **Indentați negativ activitatea**.   Indentați negativ o activitate, ca să nu mai fie subactivitate a activității sale părinte inițiale.  
  
- **Mutați în sus și în jos**.   Mutați activitățile în sus și în jos în ierarhia lor părinte. Mutarea unei activități în sus sau în jos nu are niciun efect asupra efortului, costurilor, datelor sau duratei.  
  
## <a name="task-attributes"></a>Atributele activității  
 Numele unei activități descrie lucrul care trebuie să fie finalizat. Utilizați diverse atribute de sarcină activități pentru a descrie cerințele de planificare și personal pentru activitate.  
  
### <a name="schedule-attributes"></a>Planificare atribute

 - Atribuiți valori pentru **Ore de efort** , **Număr de resurse** , **Data de început** , **Data de sfârșit** și **Durată** pentru a stabili planificarea pentru activitate. 
 - **Efortul** este o estimare a orelor necesare pentru a finaliza activitata.
 - **Număr de resurse** este o estimare efectuată de managerul proiectului în activitate, pentru a ajuta la realizarea celui mai bun program posibil. 
 - **Duraăa** (în zile) indică numărul de zile de lucru necesare pentru a finaliza activitatea.  
  
### <a name="staffing-attributes"></a>Atribute de personal

 - **Rol** , **Unitate organizațională de resurse** , **Număr de resurse** și **Resurse** descriu cerințele de personal pentru activitate. 
 - **Rol** descrie tipul de resurse necesare pentru a îndeplini activitatea. 
 - **Unitate organizațională de resurse** indică unitatea organizațională din care ar trebui să fie recrutate resurse pentru această activitate; de asemenea, acest lucru afectează estimarea de costuri și vânzări pentru activitate, deoarece este contabilizat atunci când se stabilește prețul de vânzare unitar pentru resursă. 
 - **Resurse** înseamnă o resursă generică sau o resursă denumită, atunci când este găsită una.  
  
## <a name="task-dependencies"></a>Dependențe de activitate  
 Aveți posibilitatea să creați relații de precedare între una sau mai multe activități în structură detaliată a proiectului. Puteți seta una sau mai multe valori pentru câmpul predecesor în activități, care să indice activitățile de care va depinde. Când asociați o valoare de predecesor la o activitate, activitatea poate începe numai atunci când s-au terminat toate activitățile predecesoare. Stabilirea acestei dependențe pentru o activitate va avea drept consecință recalcularea datei de început planificate a activității ca cea mai recentă dată de sfârșit a tuturor predecesorilor săi. Impactul legat de predecesor pentru o planificare nu este limitat de modul de activitate definit pentru activitate.  
  
## <a name="task-mode"></a>Mod de activitate  
 Modul de activitate este unul dintre factorii importanți care determină planificarea activităților de nod frunză. Există două moduri de activitate pentru fiecare activitate: modul de planificare automată și modul de planificare manuală.  
  
-   **Planificare automată**.   Când setați modul de activitate la Planificat automat, motorul de planificare a activităților utilizează regulile de planificare pentru următoarele atribute de activitate, pentru a determina planificarea pentru activitate:  
  
    -   Predecesori  
  
    -   Efort  
  
    -   Număr de resurse  
  
    -   Datele de sfârșit și de început  
  
-   **Regulile mele de planificare**.   Data de început a unei activități nod frunză care nu are predecesori impliciți pentru data de început a planificării proiectului. Durata unei activități nod frunză se calculează întotdeauna ca numărul de zile lucrătoare dintre datele sale de început și de sfârșit. Când o activitate este planificată automat, motorul de planificare urmează regulile de mai jos:  
  
    -   Datele de început și de sfârșit ale unei activități trebuie să fie întotdeauna zile lucratoare, conform calendarului de planificare a proiectului  
  
    -   Data de început a unei activități care are predecesori devine implicit cea mai recentă dată de sfârșit a predecesorilor săi  
  
    -   Efort = numărul de persoane * durata * orele dintr-o zi de lucru standard din calendarul proiectului  
  
-   **Planificare manuală**.   În unele cazuri, ați putea dori să vă abateți de la aceste reguli. În aceste cazuri, puteți seta modul de activitate pentru activitatea care va fi planificată manual. Aceasta oprește ca motorul de planificare să calculeze valorile pentru alte atribute de planificare. Setarea de predecesori pentru activități afectează întotdeauna data de început a activității dependente.  
  
## <a name="create-a-work-breakdown-structure"></a>Creați o structură detaliată a proiectului  
  
1.  Accesați **Project Service > Proiecte**.  
  
2.  Faceți clic pe proiectul la care doriți să lucrați.  
  
3.  În bara din partea de sus a ecranului, selectați săgeata în jos de lângă numele proiectului, apoi faceți clic pe Structură detaliată a proiectului.  
  
4.  Pentru a adăuga o activitate, faceți clic pe **Adăugare activitate**. Completați câmpurile pentru activitate, apoi faceți clic pe **Salvare**.  
  
5.  Continuați să adăugați activități până când se finalizează structură detaliată a proiectului. În timp ce creați structură detaliată a proiectului, puteți face următoarele pentru a vă organiza activitățile:  
  
    -   Selectați o activitate și faceți clic pe **Indentare** pentru a o muta sub o altă activitate sau faceți clic pe Indentare negativă pentru a o muta în afară cu un nivel.  
  
    -   Selectați o activitate și faceți clic pe **Mutare în sus** sau pe **Mutare în jos** pentru a o muta în sus sau în jos în listă.  
  
    -   Faceți clic pe **Ascundere Gantt** pentru a ascunde diagrama Gantt și faceți clic pe **Afișare Gantt** pentru a o afișa din nou.  
  
    -   Selectați o perioadă diferită pentru diagrama Gantt în **Scară de timp**.  
  
6.  Pentru a adăuga rolurile specificate în structura detaliată a proiectului pentru membrii echipei proiectului dvs., faceți clic pe **Generare echipă de proiect**.  
  
7.  Faceți clic pe **Salvare** în colțul din dreapta jos al ecranului după ce ați terminat de efectuat modificările.  
  
### <a name="see-also"></a>Consultați și  
 [Ghidul managerului de proiect](../psa/project-manager-guide.md)
