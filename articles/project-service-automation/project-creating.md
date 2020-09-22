---
title: Planificări de proiect
description: Acest subiect oferă informații despre cum să creați o planificare.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 3/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 10e8f8aa-ddfb-4626-b936-86f054808dc2
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: e6c259677fbc43e2e6087e013955f156ae2dac4e
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754725"
---
# <a name="project-schedules"></a>Planificări de proiect 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

O planificare de proiect comunică ce lucru trebuie să fie terminat, ce resurse vor efectua lucrul și intervalul de timp în care trebuie să fie terminat lucrul. Reflectă tot lucrul care este asociat cu livrarea proiectului la timp. În Dynamics 365 Project Service Automation, creați o planificare de proiect prin defalcarea lucrului în activități gestionabile, estimând timpul necesar pentru a realiza fiecare activitate, stabilind dependințele de activități, stabilind duratele activităților și estimând resursele generice care vor realiza activitățile. Planificarea de proiect este creată pe fila **Planificare** a paginii proiectului.
 
## <a name="tasks"></a>Sarcini

Primul pas în crearea unei planificări de proiect este de a defalca elementele de lucru în porțiuni gestionabile. Planificarea în PSA acceptă următoarele caracteristici:

- Nodul rădăcină al proiectului
- Activități rezumat sau container
- Activitățile nodului frunză

### <a name="project-root-node"></a>Nodul rădăcină al proiectului

Nodul rădăcină de proiect este activitatea rezumat de nivel superior pentru proiect. Toate celelalte activități de proiect create în cadrul acestuia. Numele activității nodului rădăcină este mereu setat la numele proiectului. Efortul, datele și durata nodului rădăcină sunt rezumate pe baza valorilor din ierarhia de sub acesta. Nu puteți edita proprietățile nodului rădăcină. De asemenea, nu puteți șterge nodul rădăcină.

### <a name="summary-or-container-tasks"></a>Activități rezumat sau container 

Activitățile de sinteză au sub-activități sau activități container sub ele. Ei nu au nici un efort de lucru sau de cost al lor. În schimb, efortul lor de lucru și costul sunt un set de efort de lucru și costul activităților lor container. Data de începere a activității de rezumat este data de începere a activităților container, iar data de sfârșit este data de încheiere a activităților container. Numele unei activități rezumat poate fi editat, dar proprietățile de planificare (efort, date și durată) nu pot fi editate. Dacă ștergeți o activitate rezumat, ștergeți și toate activitățile sale container.

### <a name="leaf-node-tasks"></a>Activitățile nodului frunză

Activitățile nod frunză reprezintă cel mai granular lucru din proiect. Au un efort estimat, resurse, date planificate de început și sfârșit și o durată.
 
## <a name="creating-a-task-hierarchy"></a>Crearea unei ierarhii de activități

Puteți crea o ierarhie de activități utilizând următoarele opțiuni:

- Buton **Adăugare activitate**
- Butonul **Indentare activitate**
- Buton **Indentare exterior activitate**
- Butoane **Mutare în sus** și **Mutare în jos**
- Comenzi rapide de la tastatură și accesibilitate

### <a name="add-task"></a>Adăugați activitatea

Butonul **Adăugare activitate** vă permite să creați o activitate nouă în ierarhie. Dacă nu selectați o poziție, activitatea nouă este inserată la final. 

Un ID de planificare este atribuit la fiecare activitate. ID-ul de planificare reprezintă adâncimea și poziția activității în ierarhie. Se utilizează numărul conturului. Pentru activități în primul nivel sub nodul rădăcină de proiect, se utilizează o schemă de numerotare de 1, 2, 3 și așa mai departe. Pentru activități sub primul nivel sub nodul rădăcină de proiect, se utilizează o schemă de numerotare de 1.1, 1.2, 1.3 și așa mai departe.

### <a name="indent-task"></a>Indentați activitatea

Când o activitate este indentată, devine un fiu al activității care este direct deasupra ei. ID-ul de planificare al activității este apoi recalculat, astfel încât se bazează pe ID-ul de planificare al noului său părinte și urmează schema de numerotare schiță. Activitatea părinte este acum o activitate rezumat sau o activitate container. Prin urmare, acesta devine un cumul al sarcinilor sale copil.

### <a name="outdent-task"></a>Indentați exterior activitatea 

Când o activitate este indentată exterior, nu mai este un fiu al activității care a fost părintele său. ID-ul de planificare este apoi recalculat astfel încât să reflecte adâncimea și poziția actualizată a activității în ierarhie. Efortul, costul și datele activității părinte anterioare sunt recalculate astfel încât să nu includă această activitate.

### <a name="move-up-and-move-down"></a>Mutare în sus și Mutare în jos 

Butoanele **Mutare în sus** și **Mutare în jos** modifică poziția unei activități în ierarhia părinte. Modificările de acest tip nu afectează efortul, costul, datele sau durata activității. Este afectat numai ID-ul de planificare al activității. ID-ul de planificare este apoi recalculat astfel încât să reflecte adâncimea și noua poziție în lista părintelui de activități-fiu.

### <a name="accessibility-and-keyboard-shortcuts"></a>Comenzi rapide de la tastatură și accesibilitate

Grila de **Planificare** este complet accesibilă și poate fi utilizată cu cititoare de ecran, ar fi Narator, JAWS sau NVDA. Aveți posibilitatea să mutați prin zona grilă utilizând tastele săgeată (ca în Microsoft Excel), puteți utiliza tasta Tab pentru a avansa prin elementele interactive UI și puteți utiliza tasta săgeată în jos, tasta Enter sau bara de spațiu pentru a selecta și invoca meniurile verticale. Anteturile coloanelor sunt, de asemenea, interactive. Aveți posibilitatea să ascundeți și să afișați coloane, să utilizați tasta Tab și tastele săgeți pentru a vă deplasa prin anteturile coloanelor și pentru a utiliza butoanele de acțiune de pe bara de instrumente. În plus, puteți utiliza următoarele comenzi rapide de la tastatură:

- **Reîmprospătare**: ALT+SHIFT+F5
- **Adăugare**: ALT+SHIFT+Insert
- **Ștergere**: ALT+SHIFT+Delete
- **Mutare în sus/jos**: ALT+SHIFT+Săgeți sus/jos
- **Indentare/Indentare exterioară**: ALT_SHIFT + săgeți stânga/dreapta
- **Extindere/restrângere ierarhii**: tastele ALT+SHIFT + Plus/Minus

## <a name="task-attributes"></a>Atributele activității

Numele unei activități descrie lucrul care trebuie să fie finalizat. În PSA, atributele care sunt asociate cu o activitate descriu planificarea activității și cerințele sale de personal.

> ![Atributele activității](media/project-2.png)
 
### <a name="schedule-attributes"></a>Planificare atribute

Atributele **Efort**, **Dată de început**, **Dată de sfârșit** și **Durată** definesc planificarea pentru activitate.

Atributele de program suplimentare includ:

- **Ore de efort**: introduceți o estimare a orelor necesare pentru finalizarea activității. 
- **Durata**: specificați numărul de zile lucrătoare care sunt necesare pentru a finaliza activitatea.
- **ID Planificare**: acest ID generat automat este utilizat pentru a comanda activități în ierarhie. Dependențele dintre activități gestionează ordinea efectivă în care sunt lucrate activitățile.
 
### <a name="staffing-attributes"></a>Atribute de personal

Atributele de personal sunt accesate prin câmpul **Resurse** din planificare. Aveți posibilitatea fie să căutați o resursă existentă, fie să faceți clic pe **Creare** și în panoul **Creare rapidă**, adăugați un membru al echipei de proiect ca o resursă nouă.

Câmpurile **Rol**, **Unitate de resursă** și **Nume poziție** sunt utilizate pentru a descrie cerințele de personal pentru activitate. Aceste atribute de personal împreună cu planificarea de activitate sunt utilizate pentru a găsi resursele disponibile pentru a face această activitate.

**Rol** - specificați tipul de resursă care este necesar pentru a realiza activitatea.

**Unitate resursă**- specificați unitatea de la care ar trebui să se atribuie resursele pentru activitate. Acest atribut afectează estimarea costurilor și vânzărilor pentru activitate dacă rata de cost și de facturare pentru resursă se setează pe baza unităților de resurse.

**Numele poziției**- introduceți un nume prietenos pentru resursa generică ce servește ca un substituent pentru resursa care va efectua lucrul în cele din urmă.

Câmpul **Resurse** deține numele de poziție al resursei generice sau al resursei numite atunci când se găsește unul.

Câmpul **Categorie** reține valorile care indică un tip mai amplu de activitate în care se poate grupa activitatea. Acest câmp nu afectează planificarea sau personalul. Este utilizat doar pentru raportare.

### <a name="task-dependencies"></a>Dependențe de activitate 

Aveți posibilitatea să utilizați planificarea în PSA pentru a crea relații predecesoare între activități. Câmpul **Predecesor** de sub **Activități** are una sau mai multe valori pentru a indica activitățile care depinde o activitate. Când valorile pedecesoare sunt atribuite unei activități, aceasta poate începe numai după ce toate activitățile predecesoare au fost terminate. Din cauza dependenței, data planificată de începere a activității este resetată la data la care sunt finalizate activitățile predecesoare.

Modul de activitate nu are niciun efect asupra actualizărilor efectuate la datele de început și de sfârșit ale activităților predecesoare/dependente.

## <a name="task-mode"></a>Mod de activitate 

Modul de activitate determină planificarea activităților nod frunză. PSA acceptă două moduri de activitate pentru fiecare activitate: planificare automată și planificare manuală.

### <a name="auto-scheduling"></a>Auto-planificare 
 
Când modul de activitate este configurat la **Planificat automat** pentru o activitate, motorul de planificare a activității utilizează regulile de planificare pe atributele de activitate pentru a determina planificarea pentru activitate.

#### <a name="scheduling-rules"></a>Reguli de planificare

În mod implicit, dacă o activitate nod frunză nu are predecesori, data sa de început este configurată la data de început planificată a proiectului. Durata unei activități nod frunză se calculează întotdeauna ca numărul de zile lucrătoare dintre datele sale de început și de sfârșit. Când o activitate este planificată automat, motorul de planificare urmează aceste reguli:

- Datele de început și de sfârșit ale activității trebuie să fie întotdeauna zile lucrătoare, conform calendarului de planificare a proiectului. 
- Pentru orice activitate care are activități predecesoare, data de început este configurată automat la ultima dată de final a predecesorilor săi.
- Efortul se calculează utilizând această formulă: numărul de persoane × durata × ore într-o zi de lucru standard în calendarul proiectului.

### <a name="manual-scheduling"></a>Planificare manuală

Dacă regulile planificării automate nu îndeplinesc cerințele dvs., aveți posibilitatea să setați modul de activitate pentru activitate la **Planificată manual**. Această setare oprește ca motorul de planificare să calculeze valorile celorlaltor atribute de planificare. Indiferent de modul de activitate, dacă setați predecesorii pe activități, afectați întotdeauna data de începere a activității dependente.
