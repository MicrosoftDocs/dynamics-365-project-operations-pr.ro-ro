---
title: Parametri de gestionare a cheltuielilor
description: Următorii parametri controlează comportamentul în gestionarea cheltuielilor.
author: KimANelson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 454d3f6feb46b28762a6a1249df2336f1aa5e91a
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960397"
---
# <a name="expense-management-parameters"></a>Parametri de gestionare a cheltuielilor


Parametrii de control ai comportamentului general în gestionarea cheltuielilor.

### <a name="general"></a>General

| **Câmp**                                                | **Descriere**                                                 |
|----------------------------------------------------------|---------------------------------------------------------------------|
| **Rata standard a kilometrajului**                             | Introduceți rata de rambursare pentru cheltuielile de kilometraj. Rata va fi înmulțită cu kilometrajul introdus pentru cheltuială pentru a calcula suma care este rambursată pentru cheltuielile de călătorie.                       |
|**Cheltuieli personale plătite de**                             | Selectați cine este responsabil pentru plata oricăror tranzacții cu cardul de credit clasificate drept personale.                                                                                                     |
|**Afișați întregul raport de cheltuieli pe drillback**               | Selectați această opțiune pentru a afișa toate cheltuielile pentru un raport de cheltuieli atunci când vizualizați detaliile documentului original pentru un voucher specific care a fost generat la raportarea cheltuielilor.              |
|**Pre-autorizarea călătoriei este obligatorie**                 | Selectați această opțiune pentru a solicita trimiterea și aprobarea unei cereri de călătorie înainte ca un angajat să poată prezenta un raport de cheltuieli.                                                                    |
|**Permiteți editarea distribuțiilor înainte de publicare**            | Selectați dacă distribuțiile unui raport de cheltuieli pot fi editate înainte de publicare.                                                                                                                 |
|**Evaluează politicile de gestionare a cheltuielilor**                     | Selectați când sunt evaluate cheltuielile pentru a determina dacă a fost încălcată o politică de cheltuieli. Cheltuielile pot fi verificate pentru încălcări atunci când se introduce și se salvează înregistrarea cheltuielilor sau când cheltuielile sunt supuse aprobării. Regulile de politică pentru încasările necesare vor fi verificate la salvarea liniei de cheltuieli.                   |
|**Permiteți liniile de cheltuieli între companii**                         | Selectați pentru a permite intrarea cheltuielilor pentru alte persoane juridice într-un raport de cheltuieli.                                                                                                          |
|**Permiteți modificarea cursului de schimb pentru cheltuielile cu cardul de credit** | Selectați această opțiune pentru a permite utilizatorului să editeze rata de schimb valutar pentru cheltuielile importate cu cardul de credit.                                                                        |
|**Câmpuri de ierarhie pe mai multe niveluri de afișat**                  | Selectați câmpurile de aprobare pe care să le afișați atunci când tipul de atribuire a fluxului de lucru al raportului de cheltuieli este setat să fie o ierarhie și selecția ierarhiei este setată pentru a utiliza ierarhia aprobării pe mai multe niveluri a cheltuielilor. Când ierarhia de aprobare pe mai multe niveluri este utilizată pentru un flux de lucru, câmpurile selectate vor fi afișate și editabile în raportul Cheltuieli. |
|**Introduceți numărul cardului de credit al angajatului (actualizarea din iulie 2017)**     | Selectați dacă un număr de 15 sau 16 caractere poate fi introdus și salvat în câmpul **Card de identitate** pe pagina **Carduri de credit** pentru un angajat.                                                                          |

### <a name="financial"></a>Servicii financiare

| **Câmp**                                                            | **Descriere**     |
|----------------------------------------------------------------------|------------------------------------|
|**Numele jurnalului de zi cu zi**                                         | Selectați numele jurnalului în care sunt înregistrate rapoartele de cheltuieli aprobate.            |
|**Permiteți recuperarea impozitelor din cheltuieli**                                  | Selectați această opțiune pentru a activa recuperarea impozitului pe cheltuieli pentru cheltuielile eligibile. Această opțiune nu poate fi activată dacă sunt activate regulile privind impozitul pe vânzări în SUA și taxele de utilizare.      |
|**Înregistrați imediat avansuri în numerar**                                     | Selectați această opțiune pentru a înregistra un avans de numerar aprobat la finalizarea procesului de plată și transfer. Dacă această opțiune nu este selectată, procesul de plată și transfer va genera un jurnal general nepublicat. |
|**Corectați data de contabilitate în timpul publicării**                             | Selectați această opțiune pentru a actualiza data contabilă la înregistrarea cheltuielilor, dacă perioada curentă este suspendată sau închisă. Data contabilă va fi setată la următoarea perioadă deschisă.   |
|**Permiteți gruparea tranzacțiilor pe baza contului compensat specificat în metoda de plată**      | Selectați această opțiune pentru a rezuma tranzacțiile de cheltuieli pentru un raport de cheltuieli, pe baza contului compensat specificat în metoda de plată pentru cheltuieli.   
|**Taxe incluse**                                                   | Selectați această opțiune pentru a include în mod implicit impozitul pe vânzări în suma cheltuielilor.             |
|**Eliberați sarcini la închiderea cererilor de călătorie**            | Selectați această opțiune pentru a elibera fonduri grevate atunci când o cerere de călătorie aprobată este închisă.                                                                                   |
|**Permiteți cererea de călătorie să depună depășirea bugetului pentru registrul bugetului și bugetul proiectului** | Selectați această opțiune pentru a permite angajaților să trimită cereri de călătorie spre aprobare, care depășesc fie bugetul permis care este stabilit în registrul bugetului, fie bugetul permis pentru un proiect.            |
|**Permiteți depunerea raportului de cheltuieli pentru depășirea bugetului pentru registrul bugetului și bugetul proiectului**    | Selectați această opțiune pentru a permite angajaților să trimită rapoarte de cheltuieli spre aprobare, dacă depășesc fie bugetul permis care este stabilit în registrul bugetului, fie bugetul permis pentru un proiect.                |
|**Permiteți aprobarea raportului de cheltuieli pentru depășirea bugetului doar pentru registrul bugetului**                | Selectați această opțiune pentru a permite aprobatorilor să aprobe rapoarte de cheltuieli care depășesc bugetul permis care este stabilit în registrul bugetului.                                                                       |

### <a name="per-diem"></a>Per diem

| **Câmp**                             | **Descriere**             |
|---------------------------------------|--------------------------------------------------------------------------------------|
|**Ore minime pentru diurnă**           | Introduceți numărul minim de ore implicit pe care un angajat trebuie să-l lucreze într-o zi pentru a fi eligibil să primească o diurnă pentru cheltuieli legate de călătorie.  Această valoare este utilizată numai ca valoare implicită pentru câmpul Ore minime pentru nivelurile ratei de diurnă.                                                                                      |
|**Procent de masă**                          | Introduceți procentajul implicit al diurnei pentru mese care este utilizat în prima și ultima zi a cheltuielilor legate de călătorie atunci când câmpul **Calculați reducerea mesei cu** este setat la oricare **Tip de masă pe zi** sau **Numărul de mese pe zi**. Ziua de lucru din prima și ultima zi ar putea fi mai scurtă decât o zi de lucru standard. Prin urmare, valoarea diurnei în aceste zile ar putea diferi de suma standard. Dacă procentul este setat la 0 atunci deducerile pentru prima și ultima zi vor fi de 0,00. |
|**Procentul hotelului**                        | Introduceți procentajul implicit al diurnei pentru hoteluri care este utilizat în prima și ultima zi a cheltuielilor legate de călătorie. Ziua de lucru din prima și ultima zi ar putea fi mai scurtă decât o zi de lucru standard. Prin urmare, valoarea diurnei în aceste zile ar putea diferi de suma standard. Dacă procentul este setat la 0 atunci deducerile pentru prima și ultima zi vor fi de 0,00.                                              |
|**Alte procente**                        | Introduceți procentajul implicit al diurnei pentru diverse cheltuieli care este utilizat în prima și ultima zi a cheltuielilor legate de călătorie. Ziua de lucru din prima și ultima zi ar putea fi mai scurtă decât o zi de lucru standard. Prin urmare, valoarea diurnei în aceste zile ar putea diferi de suma standard. Dacă procentul este setat la 0 atunci deducerile pentru prima și ultima zi vor fi de 0,00.                                                                                                     |
|**Reducerea procentului pentru micul dejun** | Introduceți suma la care se reduce diurna pentru micul dejun. De exemplu, dacă un angajat primește un mic dejun gratuit, este posibil să doriți să reduceți cuantumul diurnei cu 10%.                               |
|**Reducerea procentului pentru prânz**    | Introduceți suma la care se reduce diurna pentru prânz. De exemplu, dacă un angajat primește un prânz gratuit, este posibil să doriți să reduceți cuantumul diurnei cu 15%.                                       |
|**Reducerea procentului pentru cină**   | Introduceți suma la care se reduce diurna pentru cină. De exemplu, dacă un angajat primește o cină gratuită, este posibil să doriți să reduceți cuantumul diurnei cu 25%.                                     |
|**Calculați reducerea mesei cu**         | Selectați modul în care sistemul ar trebui să calculeze reducerea zilnică a mesei, selectând dacă reducerea se bazează pe tipul de masă pe călătorie sau pe zi sau dacă reducerea se bazează pe numărul de mese permis pe zi.|
|**Rotunjirea diurnei**                  | Selectați tipul de rotunjire care este utilizat pentru cheltuielile de diurnă. Dacă selectați rotunjirea normală, orice cheltuială de diurnă care are o sumă de 0,50 este rotunjită la 1,00 și orice cheltuială pe zi care are o sumă mai mică de 0,50 este rotunjită în jos la 0,00.                                                                                              |
|**Baza de calcul pentru diurnă pe**         | Selectați dacă o sumă de diurnă se bazează pe o zi calendaristică sau pe o perioadă de 24 de ore.       |

### <a name="fax-cover-pages"></a>Paginile de copertă ale faxului

| **Câmp**                      | **Descriere**            |
|--------------------------------|-----------------------------------------------------------------------------|
| **Instrucțiuni**                   | Introduceți instrucțiunile pe care angajații trebuie să le urmeze atunci când creează o copertă pentru un fax care este utilizat pentru a trimite chitanțe legate de un raport de cheltuieli. Pentru a introduce text specific limbii care va fi afișat, pe baza limbii utilizatorului, faceți clic pe butonul **Traduceri**. |
|**ID utilizator (informații cod bare)** | Selectați această opțiune pentru a stoca identificatorul unic al unui angajat în codul de bare care este utilizat pe pagina de copertă a faxului.                 |
|**Cod de bare**                      | Selectați codul de bare utilizat pe pagina de copertă a faxului. Codurile de bare 39 și 128 sunt acceptate în gestionarea cheltuielilor.               |

### <a name="anti-corruption"></a>Anticorupție

|                 <strong>Câmp</strong>                 |                                                                                                                                                                                            <strong>Descriere</strong>                                                                                                                                                                                             |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|  <strong>Afișați atestarea anticorupție</strong>  | Selectați această opțiune pentru a afișa textul anticorupție atunci când creați un nou raport de cheltuieli. Pot fi apoi activate categorii de cheltuieli specifice care vor necesita selectarea atestatului anticorupție în raportul de cheltuieli. De exemplu, o categorie de cadouri care are legătură cu o cheltuială oficială a guvernului ar putea cere angajatului să confirme că cheltuiala respectă politica companiei care este legată de oficialii guvernamentali. |
| <strong>Mesaj anticorupție pentru expeditor</strong> |                                                                                             Introduceți textul care va fi afișat angajatului la crearea unui nou raport de cheltuieli. Pentru a introduce text specific limbii care va fi afișat, pe baza limbii utilizatorului, faceți clic pe butonul <strong>Traduceri</strong>.                                                                                             |
| <strong>Mesaj anticorupție pentru aprobator</strong>  |                                                                                             Introduceți textul care va fi afișat aprobatorului la crearea unui nou raport de cheltuieli. Pentru a introduce text specific limbii care va fi afișat, pe baza limbii utilizatorului, faceți clic pe butonul <strong>Traduceri</strong>.                                                                                             |

