---
title: Rapoartele de cheltuieli reinventate
description: Acest subiect oferă informații despre experiența reproiectată și reinventată pentru introducerea raportului de cheltuieli.
author: suvaidya
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: cd0d415b9cc85bac91de8fb9427da290ae0c6108
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897151"
---
# <a name="expense-reports-reimagined"></a>Rapoartele de cheltuieli reinventate

Intrarea raportului de cheltuieli a fost reproiectată pentru a simplifica procesul și a reduce timpul necesar pentru finalizarea unui raport. Iată componentele majore ale noii experiențe de cheltuieli:

- Un nou spațiu de lucru pentru gestionarea cheltuielilor, care vă permite să accesați cheltuielile delegatului.
- O nouă experiență de potrivire a chitanțelor pentru a afișa mai bine chitanțele la nivel de antet și pentru a simplifica procesul de atașare a chitanțelor la liniile de cheltuieli.
- O nouă grilă numai în citire care vă permite să vizualizați mai multe linii de cheltuieli și coloane suplimentare de date. Acum puteți vedea toate liniile detaliate și împărțite, împreună cu cheltuielile lor părinte.
- Un panou simplificat pentru cheltuieli de editare.
- Mesaje de eroare, avertisment și politică reproiectate pentru a oferi contextul corect și înțelegerea problemei și modul de soluționare a acesteia. Am eliminat mai multe dintre mesajele care au apărut înainte ca utilizatorii să își poată finaliza sarcinile și să rezolve problemele.
- O nouă pagină pentru a specifica câmpurile obligatorii, câmpurile opționale și câmpurile care nu ar trebui incluse. Această pagină ajută la reducerea numărului de câmpuri care trebuie setate.
- Un aspect nou pentru rapoartele de cheltuieli, astfel încât rapoartele să nu mai pară că ar fi concepute pentru contabilitate.

Pentru a activa noua experiență, utilizați spațiul de lucru **Managementul caracteristicilor** pentru a activa caracteristica **Rapoartele de cheltuieli reinventate**. Când activați această caracteristică, au loc următoarele acțiuni:

- Spațiul de lucru existent de cheltuieli este înlocuit cu noul spațiu de lucru.
- Se adaugă un nou element de meniu pentru vizibilitatea câmpului de cheltuieli.
- Nu sunt eliminate elemente de meniu existente pentru rapoartele de cheltuieli (pagina existentă) sau câmpurile pentru rapoarte de cheltuieli.
- Fluxurile de lucru și orice aprobări vă duc în continuare la pagina de rapoarte de cheltuieli existente.

## <a name="getting-started-video-for-new-users"></a>Video de început pentru noii utilizatori

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE2Y7gO]

[Experiența de cheltuieli în videoclipul Dynamics 365 for Finance and Operations](https://youtu.be/Ocy-MsTvEE0) (prezentat mai sus) este inclus în [Finance and Operations playlistul](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) disponibil pe YouTube.

## <a name="new-features"></a>Caracteristici noi

| Caracteristică nouă | Descriere |
|---|----|
| Extindeți vizibilitatea câmpului | O nouă pagină de configurare vă permite să specificați câmpurile care trebuie dezactivate pentru o organizație, care câmpuri ar trebui să fie obligatorii și ce câmpuri sunt recomandate. |
| Câmpuri obligatorii | O nouă configurație simplă vă permite să creați câteva câmpuri necesare, fără a fi nevoie să utilizați cadrul de politici. |
| Câmpuri opționale | Se adaugă o a doua pagină pentru câmpurile opționale. În acest fel, angajații nu vor simți că ar trebui să seteze câmpurile, dar câmpurile sunt încă ușor accesibile. |
| Adăugați chitanțe neatașate | Capacitatea de a adăuga chitanțe neatașate la raportul de cheltuieli este mai vizibilă din spațiul de lucru și din raportul de cheltuieli. |
| Mesagerie îmbunătățită | Există o vizibilitate mai bună a liniilor de cheltuieli care au avertismente sau erori. |
| Reducerea mesajelor din bara de mesaje| Numărul de mesaje Infolog a scăzut și s-a făcut un efort pentru a preveni apariția mesajelor duplicate în multe cazuri. |
| Grupate împreună acțiuni comune | Interfața a fost curățată cu adăugarea unui nou buton de acțiuni pentru majoritatea acțiunilor comune la nivel de linie și adăugarea unui buton de punctă de suspensie (...) pentru antet și alte acțiuni mai puțin frecvente. |
| Nou spațiu de lucru pentru a crește vizibilitatea | Un nou spațiu de lucru unifică caracteristicile și linkurile care permit utilizatorilor să se mute în diferite zone. |
| Adăugați cheltuielile și încasările existente în timpul creării cheltuielilor | Când creați rapoarte de cheltuieli, puteți adăuga toate cheltuielile și chitanțele selectate sau selectate. |
| Calculator de curs valutar | Se adaugă un calculator al cursului valutar, care vă permite să calculați rata de schimb pentru tranzacțiile din mai multe buzunare. |
| Salvați și adăugați noi linii de cheltuieli | Butoanele **Salvați** și **Nou** sunt disponibile atunci când sunt introduse noi cheltuieli, pentru a vă ajuta să introduceți rapid liniile de cheltuieli. |
| O vizibilitate mai bună în linii separate și detaliate | Liniile detaliate și împărțite sunt adăugate direct la lista cheltuielilor pentru a crește vizibilitatea și a vă ajuta să determinați cu ușurință dacă există erori. |
| Afișați chitanțele în timpul detalierii | Chitanțele pot fi afișate în timpul detalierii. |

Versiunea inițială este axată pe scenarii de intrare a cheltuielilor. Orice scenariu de revizuire sau aprobare a raportului de cheltuieli va continua să folosească pagina de introducere a cheltuielilor existente.

Următoarele funcții sunt prezente pe pagina existentă, dar nu sunt încă prezente pe pagina nouă. Aceste caracteristici vor fi reintroduse în următoarele câteva versiuni:

- Aprobări
- Aprobarea conturilor de plătit și posibilitatea de a edita contabilitatea
- Puncte multiple de intrare
- Integrarea cererii de călătorie
- Entitate de date pentru vizibilitatea câmpului de cheltuieli
- Intrare pentru cheltuieli diurne
- Flux de lucru la nivel de linie
- Suport interimar pentru aprobare
- Detaliere avansată
