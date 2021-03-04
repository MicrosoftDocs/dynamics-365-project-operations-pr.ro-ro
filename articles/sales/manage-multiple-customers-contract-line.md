---
title: Gestionarea mai multor clienți în linii de contract bazate pe proiect
description: Acest subiect oferă informații despre lucrul cu liniile contractuale și contractele care conțin mai mulți clienți.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 71081775ab45167bc1bff1979f7856a2a2a91385
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181917"
---
# <a name="manage-multiple-customers-on-project-based-contract-lines"></a>Gestionarea mai multor clienți în linii de contract bazate pe proiect

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Liniile contractuale bazate pe proiecte pot include o listă a clienților care sunt responsabili pentru plată. Această listă de clienți de pe linia de contract bazată pe proiecte poate fi aceeași cu lista de clienți din contract, dar nu este necesară. Când se câștigă o ofertă de proiect și se creează un contract de proiect, lista de clienți de pe linia de ofertă este copiată pe linia de contract corespunzătoare. Clienții din ofertă sunt copiați în contract.

Atunci când contractul de proiect este facturat, lista de clienți de pe linia de contract bazată pe proiect are prioritate față de lista de clienți din contract. Lista de clienți din contractul de proiect este utilizată numai pentru implicirea noilor linii de contract.

Toți clienții contractuali de pe fila **Clienți** din contractul de proiect implicit ca clienți ai liniei de contract pe orice linii de contract noi create pentru contractul de proiect. Orice linie contractuală existentă nu va moșteni noile înregistrări ale clienților contractului create după acestea.

## <a name="create-update-or-delete-a-contract-line-customer-record"></a>Creați, actualizați sau ștergeți o înregistrare client de linie contractuală

Puteți crea, actualiza sau șterge un client de linie contractuală din fila **Clienți de linii contractuale** de pe pagina **Linie de contract bazată pe proiect**. Atunci când se adaugă un client nou pe linia contractuală bazată pe proiect, aceștia sunt adăugați și pe contractul general ca client contract cu un procentaj de facturare implicit de zero la sută. Procentul de împărțire a facturării pe contractul global este copiat pe noile linii de contract și pe eventualul contract de proiect. Cu toate acestea, la facturarea din contract, se utilizează procentajul împărțirii facturării la nivelul liniei contractului și nu procentul împărțirii facturării la nivelul contractului global. 

Mai jos sunt câmpurile de pe înregistrarea de client a liniei Contract a unei linii de contract bazate pe proiecte pe care să o țineți cont de faptul că lucrați cu aceasta:

| Câmp | Locație | Descriere | Impactul din aval |
| --- | --- | --- | --- |
| Cont | Grilă editabilă pe fila **Clienți de linie contractuală** și formulare principale și de creare rapidă pentru un client de linie contractuală | Toate conturile active. Acest câmp este blocat după crearea înregistrării. Pentru a actualiza câmpul, ștergeți înregistrarea și creați o nouă înregistrare. Dacă ați înregistrat date reale, nu puteți șterge înregistrarea. Cu toate acestea, puteți marca procentajul împărțirii facturării ca zero pentru contul respectiv. Atunci când înregistrarea este marcată ca zero, toate costurile viitoare și veniturile reale care sunt atribuite sau împărțite acestui client sunt afectate. | Când alegeți un cont din lista principală de conturi pentru a le adăuga și a le salva, clientul din linia contractuală este adăugat și ca client contractual. Clienții cu linie de contract sunt utilizați atunci când sunt generate facturi. |
| Procent de divizare de factură | Grilă editabilă pe fila **Clienți de linie contractuală** și formularele principale și de creare rapidă pentru un client de linie contractuală | Acest câmp reprezintă procentul din fiecare tranzacție de vânzare nefacturată care va fi atribuită acestui client de linie contractuală. | Clienții din linia contractuală și procentajele de facturare sunt utilizate atunci când realitățile sunt create după aprobare și când se generează factura. |
| Limită de nedepășire | Grilă editabilă pe fila **Clienți de linie contractuală** și formulare principale și de creare rapidă pentru un client de linie contractuală | Indică dacă există o limită sau o limită negociată pentru suma totală care va fi facturată acestui client pentru linia contractuală. | Limita de depășire pentru clientul de linie contractuală este utilizată atunci când sunt create facturi și sunt generate facturile. |
| Firmă proprietară | Grilă editabilă pe fila **Ofertă de linie contractuală** și formularele principale și de creare rapidă pentru un client de linie de ofertă | Persoana juridică în care este înființat acest client. Acest câmp este doar în citire și este setat la compania deținătoare a ofertei. Lista clienților de adăugat în câmpul **Cont** este deja filtrat în lista de la această companie deținătoare. | Conceptul de companie proprietară echivalează cu conceptul de persoană juridică. Toate costurile și veniturile provenite din acest proiect sunt contabilizate în registrul general al companiei deținătoare. |
| Este rotunjire | Grilă editabilă pe fila **Clienți de linie contractuală** și formulare principale și de creare rapidă pentru un client de linie contractuală | Acest câmp indică dacă acest client este un client implicit de rotunjire pentru această linie de contract bazată pe proiect. | Atunci când generați un procent real în funcție de procentajul împărțit de facturare, pot exista unele diferențe de rotunjire. Acestui client i se atribuie diferențele de rotunjire în acest caz. |

## <a name="edit-billing-split-percentages"></a>Editați procente de facturare

Procentele de facturare împărțite pot fi editate în grilă. Atunci când procentajele de împărțire a facturării nu totalizează 100%, va apărea o eroare. După ce editați procentele de facturare împărțite, reîmprospătați pagina pentru a elimina eroarea.

Puteți încerca și să selectați **Distribuire uniformă** pe subgrila liniei de contract a clientului. Această acțiune alocă în mod uniform împărțiri de facturare tuturor clienților din linia contractuală. Dacă există vreun factor de rotunjire, acesta va fi adăugat clientului de rotunjire. Un client de linie contractuală este întotdeauna etichetat drept client de **Rotunjire** cu semnalizator **Rotunjire** setat la **Da**.