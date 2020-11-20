---
title: Rezervări resurse și care este legătura sa cu atribuirile sarcinilor
description: Acest subiect oferă informații despre modul în care se gestionează resursele denumite, rezervările de resurse și atribuirile de activități și modul în care acestea se asociază între ele.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/27/2019
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
ms.openlocfilehash: c4b976b49bd643bc7a774a86b1ba89bd76d7c916
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4125020"
---
# <a name="resource-bookings-and-how-they-relate-to-task-assignments"></a>Rezervări resurse și care este legătura sa cu atribuirile sarcinilor


Există două moduri resursele denumite care pot fi rezervate la o echipă de proiect și li se pot atribui sarcini de proiect:

- Resursa poate fi rezervată direct pe un proiect și ulterior atribuită pe sarcini de proiect.
- Sarcinile pot fi atribuite la o resursă generică, care este apoi utilizată pentru a găsi și înlocui resursa generică cu o resursă denumită. 

În ambele cazuri, actul de rezervare a resursei rezervă capacitatea resursei.

Managerul de proiect care planifică proiectul deține planul de proiect și planificarea. Prin utilizarea resursei generice pentru atribuire și apoi prin generarea unei solicitări de resurse din ea, managerul de proiect poate rezerva resurse pe proiect cu contururi prevăzute în planul de proiect. Pot rezerva resurse pe un proiect și le pot atribui apoi la activități, dar nu există nici o modalitate de a alinia contururile de rezervare cu contururile sarcinilor. Rezervările nu afectează planificarea proiectului.

Gândiți-vă la un proiect complex cu mai multe sarcini ce se suprapun, unde mai multe resurse de același tip trebuie să lucreze simultan. În cazul în care unei resurse i se dă un contur care diferă de cel al tuturor sarcinilor sale, este dificil să se modifice sarcinile pentru a se potrivi conturul rezervărilor cu sarcinile lor detaliate și cu contururile lor originale.

În exemplul de mai jos, efortul total cerut de aceeași resursă dintr-un set de patru sarcini este de 62 de ore pe o perioadă de două săptămâni și nu există un anumit contur. În cazul în care resursa Bob este rezervat pentru 62 de ore în timpul acelorași două săptămâni, dar cu un contur diferit, cerința și rezervarea sunt aliniate.

| **Contururi de sarcini**    | **Ore totale** | L 4/6 | M 5/6 | M 6/6 | J 7/6 | V 8/6 | S 9/6 | D 10/6 | L 11/6 | M 12/6 | M 13/6 | J 14/6 | V 15/6 |
|----------------------|-----------------|--------|--------|--------|--------|--------|--------|---------|---------|---------|---------|---------|---------|
| Sarcina 1               | 24              | 8      | 8      | 4      |        |        |        |         |         |         | 4       |         |         |
| Sarcina 2               | 16              |        |        | 4      | 4      |        |        |         | 8       |         |         |         |         |
| Sarcina 3               | 10              |        |        |        |        | 4      |        |         |         | 4       |         | 2       |         |
| Sarcina 4               | 12              |        |        |        |        |        |        |         |         |         | 4       |         | 8       |
|                      |                 |        |        |        |        |        |        |         |         |         |         |         |         |
| **Totaluri**           | 62              | 8      | 8      | 8      | 4      | 4      |        |         | 8       | 4       | 8       | 2       | 8       |
|                      |                 |        |        |        |        |        |        |         |         |         |         |

### <a name="bobs-availability"></a>Disponibilitatea lui Bob
| **Rezervare resurse** | **Ore totale** | L 4/6 | M 5/6 | M 6/6 | J 7/6 | V 8/6 | S 9/6 | D 10/6 | L 11/6 | M 12/6 | M 13/6 | J 14/6 | V 15/6 |
|------------------------|-----------------|--------|--------|--------|--------|--------|--------|---------|---------|---------|---------|---------|---------|
| Bob                    | 62              | 4      | 4      | 8      | 8      | 8      |        |         | 4       | 4       | 8       | 8       | 6       |

Cu toate acestea, nu există nici o modalitate sistematică a atribui conturul de ore rezervate pe activități la nivel de zi. În cazul în care managerul de proiect este dispus să modifice planificarea proiectului pentru a satisface disponibilitatea resursei,va trebui să elimine atribuirea și să revizuiască toate sarcinile pentru a se potrivi cu contururile de rezervare.

În cazul în care unei organizații a dat sarcina de planificare a proiectului atât unui manager de proiect, cât și unui manager de resurse, managerul de proiect stabilește planificarea, iar acest lucru include conturarea lucrărilor necesare. Managerul de resurse nu ar trebui să poată afecta planificarea fără ca managerul de proiect să știe, prin schimbarea contururilor de efort în timp ce rezervă resurse reale. În cazul în care managerul de resurse realizează ceva diferit față de ceea ce a solicitat managerul de proiect, trebuie să ajungă la acord cu privire la modificările necesare în planificarea proiectului.

Deoarece rezervările atribuirile nu sunt strâns cuplate, este posibil să se rezerve contururi care sunt diferite de contururile de activitate sau să se modifice atribuiri care să rezulte în cazuri în care rezervările și atribuirile nu sunt aliniate.

**Vizualizarea Reconciliere** permite managerului de proiect să vadă rezervările și atribuirile pentru fiecare membru al echipei proiectului. Vizualizarea folosește culori si umbre pentru a arăta unde există o neconcordanță între rezervările și atribuirile pentru un membru al echipei. Pe baza acestor informații, managerul de proiect poate lua măsuri corective, fie să extindă rezervările de resurse pentru cazurile în care există atribuiri și nu există rezervări, fie să anuleze rezervările în cazul în care resursele sunt rezervate, dar nu au atribuiri.

> [!NOTE]
> Dacă mutați o activitate pe care ați conturat-o chiar dvs., aceste contururi nu sunt menținute. Contururile sunt generate din nou conform calendarului proiectului pentru a ține cont de modificările orelor de program și de sărbători. Acest lucru este proiectat întrucât sistemul nu cunoaște intenția conturului original și nu poate determina dacă are sens să păstreze acel contur într-un nou interval de timp. Întrucât rezervările și atribuirile sunt deconectate, rezervările păstrează contururile de rezervare originale. În acest caz, va trebui să anulați și să rezervați din nou la noul contur de atribuire.

