---
title: Gestionați mai mulți clienți în linii de oferte bazate pe contract - simplificat
description: Acest subiect oferă informații despre gestionarea mai multor clienți pe linii de contract bazate pe proiecte.
author: rumant
ms.date: 10/27/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a7e29b1a92a5fefcf4812931383d03e5f81a27001f0e6525bb4eeb8dc93b18b9
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/06/2021
ms.locfileid: "7001806"
---
# <a name="manage-multiple-customers-on-project-based-contract-lines---lite"></a>Gestionați mai mulți clienți în linii de oferte bazate pe contract - simplificat

_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_

Liniile contractuale bazate pe proiecte pot include o listă a clienților care sunt responsabili pentru plată. Această listă de clienți de pe linia de contract bazată pe proiecte poate fi aceeași cu lista de clienți din contract, dar nu este necesară. Când se câștigă o ofertă de proiect și se creează un contract de proiect, lista de clienți de pe linia de ofertă este copiată pe linia de contract corespunzătoare. Clienții din ofertă sunt copiați în contract.

Atunci când contractul de proiect este facturat, lista de clienți de pe linia de contract bazată pe proiect are prioritate față de lista de clienți din contract. Lista de clienți din contractul de proiect este utilizată numai pentru implicirea noilor linii de contract.

Toți clienții contractuali de pe fila **Clienți** din contractul de proiect implicit ca clienți ai liniei de contract pe orice linii de contract noi create pentru contractul de proiect. Orice linie contractuală existentă nu va moșteni noile înregistrări ale clienților contractului create după acestea.

## <a name="create-update-or-delete-a-contract-line-customer-record"></a>Creați, actualizați sau ștergeți o înregistrare client de linie contractuală

Puteți crea, actualiza sau șterge un client de linie contractuală din Clienți de linii contractuale fila de pe Linie de contract bazată pe proiect pagină. Atunci când se adaugă un client nou pe linia contractuală bazată pe proiect, aceștia sunt adăugați și pe contractul general ca client contract cu un procentaj de facturare implicit de zero la sută. Procentul de împărțire a facturării pe contractul global este copiat pe noile linii de contract și pe eventualul contract de proiect. Cu toate acestea, la facturarea din contract, se utilizează procentajul împărțirii facturării la nivelul liniei contractului și nu procentul împărțirii facturării la nivelul contractului global.

Mai jos sunt câmpurile de pe înregistrarea de client a liniei **Contract** a unei linii de contract bazate pe proiecte pe care să o țineți cont de faptul că lucrați cu aceasta:

| Câmp | Locație | Descriere | Impactul din aval |
| --- | --- | --- | --- |
| **Cont** | Grilă editabilă pe fila **Clienți contractuali** și fișierul **Principal** și formularul **Creare rapidă** pentru un client contractual. | Toate conturile active. Acest câmp este blocat după crearea înregistrării. Pentru a actualiza câmpul, ștergeți înregistrarea și creați o nouă înregistrare. Dacă ați înregistrat date reale, nu puteți șterge înregistrarea. Cu toate acestea, puteți marca procentajul împărțirii facturării ca zero pentru contul respectiv. Atunci când înregistrarea este marcată ca zero, toate costurile viitoare și veniturile reale care sunt atribuite sau împărțite acestui client sunt afectate. | Când alegeți un cont din lista principală de conturi pentru a le adăuga și a le salva, clientul din linia contractuală este adăugat și ca client contractual. Clienții cu linie de contract sunt utilizați atunci când sunt generate facturi. |
| **Procent de divizare factură** | Grilă editabilă pe fila **Clienți contractuali** și fișierul **Principal** și formularul **Creare rapidă** pentru un client contractual. | Acest câmp reprezintă procentul din fiecare tranzacție de vânzare nefacturată care va fi atribuită acestui client de linie contractuală. | Clienții din linia contractuală și procentajele de facturare sunt utilizate atunci când realitățile sunt create după aprobare și când se generează factura. |
| **Limită de nedepășire** | Grilă editabilă pe fila **Clienți contractuali** și fișierul **Principal** și formularul **Creare rapidă** pentru un client contractual. | Indică dacă există o limită sau o limită negociată pentru suma totală care va fi facturată acestui client pentru linia contractuală. | Limita de depășire pentru clientul de linie contractuală este utilizată atunci când sunt create facturi și sunt generate facturile. |
| **Este rotunjire** | Grilă editabilă pe fila **Clienți contractuali** și formularele **Principal** și **Creare rapidă** pentru un client de contractuală. | Acest câmp indică dacă acest client este un client implicit de rotunjire pentru această linie de contract bazată pe proiect. | Atunci când generați un procent real în funcție de procentajul împărțit de facturare, pot exista unele diferențe de rotunjire. Acestui client i se atribuie diferențele de rotunjire în acest caz. |

## <a name="edit-billing-split-percentages"></a>Editați procente de facturare

Procentele de facturare împărțite pot fi editate în grilă. Atunci când procentajele de împărțire a facturării nu totalizează 100%, va apărea o eroare. După ce editați procentele de facturare împărțite, reîmprospătați pagina pentru a elimina eroarea.

Puteți selecta și **Distribuire uniformă** pe subgrila liniei de contract a clientului. Această acțiune alocă în mod uniform împărțiri de facturare tuturor clienților din linia contractuală. Dacă există vreun factor de rotunjire, acesta va fi adăugat clientului de rotunjire. Un client de linie contractuală este întotdeauna etichetat drept client de **Rotunjire** cu semnalizator **Rotunjire** setat la **Da**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]