---
title: Crearea unei structuri detaliate a proiectului
description: Acest subiect explică cum să creați o structură detaliată a proiectului (WBS) incluzând comenzile de bază în noua interfață de planificare.
author: ruhercul
manager: tfehr
ms.date: 01/07/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 695bbc2ae1ba1e762472b5f5fa853c89017d2f52
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287028"
---
# <a name="create-a-work-breakdown-structure-wbs"></a>Creați o structuri detaliate a proiectului (WBS)

O planificare de proiect comunică ce proiect trebuie să fie terminat, resursele care vor efectua munca și intervalul de timp în care trebuie să fie terminat proiectul. Planificarea proiectului reflectă toate activitățile asociate cu livrarea proiectului la timp. În Dynamics 365 Project Operations, creați un program de proiect prin:

  - Defalcarea proiectului pe sarcini gestionabile.
  - Estimarea timpului necesar pentru a efectua fiecare sarcină.
  - Setarea dependențelor de sarcini în cadrul proiectului.
  - Setarea duratelor sarcinilor.
  - Estimarea resurselor generice care vor îndeplini sarcinile. 

Planificarea de proiect este creată pe fila **Planificare** de pe pagina **Proiect**.

## <a name="tasks"></a>Activități

Primul pas în crearea unei planificări de proiect este de a defalca elementele de lucru în porțiuni gestionabile. Planificarea în Project Operations acceptă următoarele caracteristici:

- Activități rezumat sau container
- Activitățile nodului frunză

### <a name="summary-tasks"></a>Sarcini rezumative

Sarcinile rezumative pot stoca alte sarcini rezumative sau sarcini nod de frunză. Ei nu au nici un efort de lucru sau de cost al lor. În schimb, efortul lor de lucru și costul sunt un set de efort de lucru și costul activităților lor container. Data de începere a activității de rezumat este data de începere a activităților container, iar data de sfârșit este data de încheiere a activităților container. Numele unei sarcini rezumative poate fi editat, dar proprietățile de planificare, inclusiv efortul, datele și durata, nu pot fi editate. Dacă ștergeți o activitate rezumat, ștergeți și toate activitățile sale container.

### <a name="leaf-node-tasks"></a>Activitățile nodului frunză

Activitățile nod frunză reprezintă cel mai granular lucru din proiect. Au un efort estimat, resurse, date planificate de început și sfârșit și o durată.

## <a name="create-a-task-hierarchy"></a>Creați o ierarhie de sarcini

### <a name="add-a-task"></a>Adăugarea unei activități

Parcurgeți următorii pași pentru a adăuga una sau mai multe sarcini.

1. Mergeți la **Proiecte** și selectați și deschideți înregistrarea de proiect pentru care doriți să creați un program. 
2. Selectaţi fila **Sarcini**. 
3. Selectați **Adăugați o sarcină nouă**, introduceți un nume pentru sarcină, apoi apăsați tasta Enter.
2. Introduceți un alt nume de sarcină și apăsați din nou pe Enter până când aveți o listă completă de sarcini.

### <a name="manage-hierarchy-of-a-task"></a>Gestionați ierarhia unei sarcini

Când o activitate este indentată, devine un fiu al activității care este direct deasupra ei. ID-ul de planificare al activității este apoi recalculat, astfel încât se bazează pe ID-ul de planificare al noului său părinte și urmează schema de numerotare schiță. Sarcina primară este acum o sarcină rezumativă. Prin urmare, acesta devine un cumul al sarcinilor sale copil. Când o sarcină este promovată, nu mai este o sarcină secundară a sarcinii care a fost sarcina sa principală. ID-ul de planificare este apoi recalculat astfel încât să reflecte adâncimea și poziția actualizată a activității în ierarhie. Efortul, costul și datele activității părinte anterioare sunt recalculate astfel încât să nu includă această activitate.

Parcurgeți următorii pași pentru a indenta sau promova o sarcină.

1. Pe pagina **Proiect**, fila **Sarcini**, opțiunea **Sarcini rezumative**, selectați cele trei puncte verticale după numele sarcinii, apoi selectați **Realizați sarcină secundară**. 
2. Selectați sarcina de indentat sau promovat. Pentru a selecta mai mult de o sarcină, selectați o sarcină, țineți tasta Ctrl apăsată, apoi selectați sarcinile suplimentare.
2. Selectați **Indentare** sau **Promovare sub-sarcină**  pentru a muta sarcinile sub sau în afara sarcinilor rezumative.

### <a name="move-tasks-up-and-down"></a>Mutați sarcini în sus și în jos

Sarcinile pot fi mutate la orice nivel în structura detaliată a proiectului în unul din cele două moduri:

- Selectați una sau mai multe sarcini și trageți-le în locația dorită.
- Selectați una sau mai multe sarcini, faceți clic dreapta și selectați **Decupare**, selectați celula de destinație în program, apoi faceți clic dreapta și selectați **Lipire**.

## <a name="task-attributes"></a>Atributele activității

Numele unei activități descrie lucrul care trebuie să fie finalizat. În Project Operations, atributele asociate unei sarcini descriu planificarea sarcinii și cerințele sale de personal.

## <a name="schedule-attributes"></a>Planificare atribute

Atributele **Efort**, **Dată de început**, **Dată de sfârșit** și **Durată** definesc planificarea pentru activitate.

Următorul tabel prezintă atribute de programare suplimentare.

| **Nume afișat final** | **Descriere finală** |
| --- | --- |
| Efort finalizat (ore) | Volumul total de muncă finalizat pentru sarcină în ore. |
| Durată | Afișează durata pentru sarcină în zile. |
| Efort total | Volumul total de muncă pentru sarcină în ore. |
| Terminați | Data și ora de finalizare |
| % finalizat | Procentul din sarcină care este finalizat. |
| Pachet de proiect | Panoul de activități poate fi grupat după pachet, astfel încât fiecare pachet să aibă propria coloană. |
| Efort rămas (ore) | Volumul total de lucru rămas pentru sarcină în ore. |
| Start | Data și ora de începere. |
| Nume | Numele sarcinii. |
| ID | ID-ul sarcinii din structura detaliată a proiectului. |

În calitate de administrator, puteți defini câmpuri personalizate pe entitatea sarcină. Cu toate acestea, câmpurile nu pot fi afișate în grila de programare. Pentru a vedea câmpurile personalizate, adăugați-le la pagina de detalii pentru **Sarcina proiectului**.

## <a name="staffing-attributes"></a>Atribute de personal

Atributele de personal sunt accesate prin câmpul **Resurse** din planificare. Aveți posibilitatea fie să căutați o resursă existentă, fie să selectați **Creare** și în panoul **Creare rapidă** să adăugați un membru al echipei de proiect ca o resursă nouă.

Câmpurile **Rol**, **Unitate de resursă** și **Nume poziție** sunt utilizate pentru a descrie cerințele de personal pentru activitate. Aceste atribute de personal, împreună cu planificarea sarcinii, sunt utilizate pentru a găsi resursele disponibile pentru a realiza această sarcină.

   - **Rol**: Specificați tipul de resursă care este necesar pentru a realiza sarcina.
   - **Unitate resursă**: Specificați unitatea de la care ar trebui să se atribuie resursele pentru sarcină. Acest atribut afectează estimarea costurilor și vânzărilor pentru activitate dacă rata de cost și de facturare pentru resursă se setează pe baza unităților de resurse.
   - **Numele poziției**: Introduceți un nume pentru resursa generică ce servește ca un substituent pentru resursa care în cele din urmă va efectua activitatea.

Câmpul **Resurse** deține numele de poziție al resursei generice sau al resursei numite atunci când se găsește unul.

Câmpul **Categorie** reține valorile care indică un tip mai amplu de activitate în care se poate grupa activitatea. Acest câmp nu afectează planificarea sau personalul. În schimb, câmpul este utilizat numai pentru raportare.

## <a name="task-dependencies"></a>Dependențe de activitate

Aveți posibilitatea să utilizați planificarea în Project Operations pentru a crea relații predecesoare între sarcini. Câmpul **Predecesor** utilizează una sau mai multe valori pentru a indica sarcinile de care depinde o altă sarcină. Când valorile pedecesoare sunt atribuite unei sarcini, sarcina poate începe numai după ce toate sarcinile predecesoare au fost finalizate. Din cauza dependenței, data planificată de începere a activității este resetată la data la care sunt finalizate activitățile predecesoare.

Modul de activitate nu are niciun efect asupra actualizărilor efectuate la datele de început și de sfârșit ale activităților predecesoare/dependente.

## <a name="accessibility-and-keyboard-shortcuts"></a>Comenzi rapide de la tastatură și accesibilitate

Grila de **Planificare** este complet accesibilă și poate fi utilizată cu cititoare de ecran, ar fi Narator, JAWS sau NVDA. Aveți posibilitatea să vă deplasați prin zona grilă utilizând tastele săgeată (ca în Microsoft Excel), puteți utiliza tasta Tab pentru a avansa printre elementele interfeței cu utilizatorul interactive și puteți utiliza tasta săgeată în jos, tasta Enter sau bara de spațiu pentru a selecta și a deschide meniurile verticale.


[!INCLUDE[footer-include](../includes/footer-banner.md)]