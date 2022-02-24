---
title: Gestionarea mai multor clienți în contractele de proiect
description: Acest subiect oferă informații despre cum să gestionați mai mulți clienți pe un contract de proiect.
author: rumant
manager: Annbe
ms.date: 11/18/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5554cb062710c3587d81b1a29771a7af84d2d05f
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 11/25/2020
ms.locfileid: "4643188"
---
# <a name="manage-multiple-customers-on-project-contracts"></a>Gestionarea mai multor clienți în contractele de proiect

Acest subiect oferă informații despre cum să gestionați mai mulți clienți pe un contract de proiect. Puteți utiliza un contract de proiect atunci când este necesar un acord contractual pentru mai mulți clienți pentru finanțarea unei tranzacții. Pe pagina **Contract de proiect**, fila **Rezumat** include informații despre clientul principal pentru o ofertă. Alți clienți care participă la tranzacție pot fi adăugați la fila **Clienți**.

Toți clienții contractuali de pe fila **Clienți** din contractul de proiect implicit ca clienți ai liniei de contract pe orice linii de contract noi pe bază de proiect create pentru contractul de proiect. Orice linii de contract existente bazate pe proiecte nu moștenesc înregistrări de clienți contractuali noi care sunt create ulterior.

Puteți adăuga, actualiza sau șterge clienți de contract și de linii de contract oricând înainte de câștigarea contractului. Un client din contractul de proiect trebuie să fie înființat ca client în compania sau entitatea juridică deținută de pe pagina **Clienți**. Persoanele juridice sunt configurate în modulul **Management de proiect și contabilitate** al Dynamics 365 Project Operations și sunt disponibile drept companii în modulele **Vânzări de proiect** și **Livrare** ale Project Operations.

## <a name="primary-customers"></a>Clienți principali

Clientul potențial de pe fila **Rezumat** a contractului de proiect este clientul principal al contractului. Nu puteți actualiza clientul principal din lista de clienți de contract. Dacă încercați să ștergeți clientul principal dintr-o listă de clienți din contract, va apărea o eroare care spune că o înregistrare de client principal pe un contract nu poate fi ștearsă. În schimb, modificați clientul din câmpul **Client potențial** de pe fila **Rezumat** a contractului de proiect. Când actualizați acest câmp, clientul nou selectat este adăugat ca nou client de contract cu marcajul **Principal** setat la **Da**. Clientul primar anterior este încă client în contract, totuși nu mai este clientul principal.

## <a name="create-update-or-delete-a-contract-customer-record"></a>Creați, actualizați sau ștergeți o înregistrare client de contract

Puteți crea, actualiza sau șterge un client de contract din fila **Clienți de contract** pe pagina **Contract**. Următoarele câmpuri sunt incluse în înregistrarea de client de contract a unui contract de proiect.

| **Câmp** | **Locaţie** | **Descriere** | 
| --- | --- | --- | 
| Cont | Grila editabilă pe fila **Clienți de contract** și paginile principale și de creare rapidă pentru un client de contract. | Listează toate conturile active. Acest câmp este blocat după crearea înregistrării. Pentru a actualiza înregistrarea, trebuie să o ștergeți și apoi să o creați din nou. Dacă ați înregistrat date reale sau dacă înregistrarea clientului contractual este un client principal, nu puteți șterge înregistrarea. Când o linie de contract este creată, clienții de contract sunt copiați drept clienți de linie de contract. |
| Procent de divizare factură | Grila editabilă pe fila **Clienți de contract** și paginile principale și de creare rapidă pentru un client de contract. | Reprezintă procentul din fiecare tranzacție de vânzare nefacturată atribuită clientului de contract. Atunci când se creează noi linii de contract de proiect, procentul de facturare împărțit este copiat la toate liniile de contract create și la clienții de linie de contract de proiect. |
| Facturare către nume persoană de contact | Grila editabilă pe fila **Clienți de contract** și paginile principale și de creare rapidă pentru un client de contract. | Acest câmp text trebuie utilizat pentru a identifica persoana de contact pentru factură pentru client. Valoarea implicită vine din înregistrarea contului corelat. Numele persoanei de contact este copiat la **Numele adresei de facturare de pe contract** de pe factura generată pentru client. |
| Nume Facturare către | Grila editabilă pe fila **Clienți de contract** și paginile principale și de creare rapidă pentru un client de contract. | Utilizați acest câmp pentru a identifica persoana de contact pentru factură pentru client. Valoarea implicită vine din înregistrarea contului corelat. Numele este copiat pe câmpul **Numele adresei de facturare de pe contract** de pe factura generată pentru client. |
| Condiții de plată | Grila editabilă pe fila **Clienți de contract** și paginile principale și de creare rapidă pentru un client de contract. | Valoarea implicită vine din înregistrarea contului corelat. Termenii sunt copiați pe **Numele adresei de facturare de pe contract** de pe factura generată pentru client. |
| Firmă proprietară | Grila editabilă pe fila **Clienți de proiect de contract** și paginile principale și de creare rapidă pentru un client de proiect de contract. | Entitatea juridică în care este setat clientul în modulul **Management de proiect și contabilitate**. Acest câmp este doar în citire și este setat la compania deținătoare a contractului de proiect.</br>Lista clienților de adăugat în câmpul **Cont** este deja filtrat în lista de la această companie deținătoare în modulul **Management de proiect și contabilitate** din Project Operations. Compania deținătoare este egală cu entitatea juridică din modulul **Management de proiect și contabilitate** Project Operations. Toate costurile și veniturile provenite din proiect sunt contabilizate în registrul general al companiei deținătoare. |
| Este rotunjire | Grila editabilă pe fila **Clienți de contract** și paginile principale și de creare rapidă pentru un client de contract. | Indică dacă clientul este un client implicit de rotunjire pentru tranzacție. Pe un contract de proiect nu poate exista decât un singur client de rotunjire. Atunci când costurile și vânzările nefacturate se împart pe cantitate și duc la o diferență de rotunjire, această diferență se aplică datelor reale care sunt asociate acestui client. |
| Limită de nedepășire | Grila editabilă pe fila **Clienți de contract** și paginile principale și de creare rapidă pentru un client de contract. | Indică dacă există o limită sau o limită negociată pentru suma totală care va fi facturată clientului pentru angajament. Limita de nedepășire configurată la nivel de client de contract este evaluată pe baza datelor reale de vânzări nefacturate care fac referire la acest client de contract. |

## <a name="edit-billing-split-percentages"></a>Editați procente de facturare

Puteți edita procentele de facturare împărțite editând în grilă. Atunci când procentajele de împărțire a facturării nu totalizează 100%, apare o eroare. După ce editați un procent de facturare împărțit, reîmprospătați pagina **Contract de proiect** pentru a elimina eroarea.

Puteți selecta și **Distribuire uniformă** pe subgrila clienților de contract de proiect. Împărțirile de facturare sunt alocate uniform tuturor clienților de pe contractul de proiect. Dacă există vreun factor de rotunjire, factorul va fi adăugat clientului de rotunjire. Unul dintre clienții contractului are întotdeauna marcajul **Rotunjire** setat la **Da**. Clientul respectiv este clientul de rotunjire. De obicei, clientul de rotunjire este, de asemenea, clientul principal al contractului, dar acest lucru nu este necesar.
