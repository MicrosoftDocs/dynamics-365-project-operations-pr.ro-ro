---
title: Gestionarea mai multor clienți în contractele de proiect - simplificat
description: Acest subiect oferă informații despre gestionarea mai multor clienți pe contracte de proiect.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3c9804c77cc0931352b026f15fd764f43361757f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273168"
---
# <a name="manage-multiple-customers-on-project-contracts---lite"></a>Gestionarea mai multor clienți în contractele de proiect - simplificat

_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_

Contractele de proiect din Dynamics 365 Project Operations acceptă scenariul în care un acord contractual implică mai mulți clienți care finanțează o afacere. Fila **Rezumat** de pe pagina **Contract de proiect** include câmpul **Client**. Acest câmp identifică clientul principal al tranzacției. Alți clienți pentru afacere pot fi setați pe fila **Clienți** din pagina **Contract de proiect**.

Toți clienții contractuali listați pe contractul de proiect implicit ca clienți ai liniei de contract pe orice linii de contract noi bazate pe proiect care sunt create pentru contractul de proiect. Liniile contractuale existente bazate pe proiecte nu moștenesc clienții contractuali noi pe măsură ce sunt create înregistrări noi.

Liniile contractuale bazate pe produse sunt asociate automat clientului principal.

Clienții cu contract și clienții cu linie de contract pot fi adăugați, actualizați sau șterse în orice moment înainte de câștigarea contractului.

## <a name="primary-customer"></a>Client principal

Clientul listat pe fila **Rezumat** a contractului de proiect, deoarece clientul potențial este clientul principal al contractului. Când încercați să ștergeți clientul principal din lista de clienți din contract, veți primi un mesaj de eroare conform căruia înregistrarea unui client principal dintr-un contract nu poate fi ștearsă.

Clientul principal nu poate fi actualizat din lista de clienți contractuali. În schimb, schimbați potențialul client pe fila **Rezumat** a contractului. Când acest câmp este actualizat pe pagina **Rezumatul contractului**, noul client este adăugat ca un nou client contract cu semnalizatorul **Primar** setat. Clientul primar anterior va fi în continuare client în contract.

## <a name="create-update-or-delete-a-contract-customer-record"></a>Creați, actualizați sau ștergeți o înregistrare client de contract

Un client contract poate fi creat, actualizat sau șters din fila **Clienți** de pe pagina **Contract de proiect**. Câmpurile din tabelul următor sunt în evidența contractului de client a unui contract de proiect și ar trebui să fie luate în considerare pe măsură ce lucrați cu contractul.

| Câmp | Locație | Descriere | Impactul din aval |
| --- | --- | --- | --- |
| **Cont** | Grila poate fi editată pe fila **Clienți contractuali** și formularele **Principal** și de **Creare rapidă** pentru un client contractual. | Listează toate conturile active. Acest câmp este blocat după crearea înregistrării. Pentru a actualiza contul, ștergeți înregistrarea și creați-o din nou. Dacă ați înregistrat date reale sau dacă înregistrarea clientului contractual este un client principal, nu puteți șterge înregistrarea. | Clienții contractuali sunt copiați ca clienți ai liniei contractuale atunci când se creează o linie contractuală. |
| **Procent de divizare factură** | Grila poate fi editată pe fila **Clienți contractuali** și formularele **Principal** și de **Creare rapidă** pentru un client contractual. | Reprezintă procentul din fiecare tranzacție de vânzare nefacturată care este atribuită acestui client de contract. | Copiat pe noile linii contractuale și pe clienții liniei contractuale proiectate pe noile linii contractuale de proiect. |
| **Facturare către nume persoană de contact** | Grila poate fi editată pe fila **Clienți contractuali** și formularele **Principal** și de **Creare rapidă** pentru un client contractual. | Acest câmp text ar trebui utilizat pentru a identifica persoana de contact cu factura pentru acest client. Acest câmp implicit din înregistrarea contului aferent. | Copiat în câmpul **Numele facturii către contract** de pe factura generată pentru acest client. |
| **Nume Facturare către** | Grila poate fi editată pe fila **Clienți contractuali** și formularele **Principal** și de **Creare rapidă** pentru un client contractual | Acest câmp text ar trebui utilizat pentru a identifica persoana de contact cu factura pentru acest client. Acest câmp implicit din înregistrarea contului aferent. | Copiat în câmpul **Numele facturii către contract** de pe factura generată pentru acest client. |
| **Termeni de plată** | Grila poate fi editată pe fila **Clienți contractuali** și formularele **Principal** și de **Creare rapidă** pentru un client contractual. | Valorile implicite din înregistrarea contului corelat. | Copiat în câmpul **Numele facturii către contract** de pe factura generată pentru acest client. |
| **Este rotunjire** | Grila poate fi editată pe fila **Clienți contractuali** și formularele **Principal** și de **Creare rapidă** pentru un client contractual. | Indică dacă acest client este un client implicit de rotunjire pentru această ofertă. Pe un contract de proiect nu poate exista decât un singur client de rotunjire. | Atunci când costurile și vânzările nefacturate se împart pe cantitate, duc la o diferență de rotunjire, această diferență se aplică efectivului care este asociat acestui client. |
| **Limită de nedepășire** | Grila poate fi editată pe fila **Clienți contractuali** și formularele **Principal** și de **Creare rapidă** pentru un client contractual | Indică dacă există o limită sau o limită negociată pentru suma totală care va fi facturată clientului pentru acest angajament. | **Limita de depășire** configurată la nivel de client de contract va fi evaluat pe **Vânzări reale facturate** care face referire la acest client de contract. |

## <a name="edit-billing-split-percentages"></a>Editați procente de facturare

Procentele de facturare împărțite pot fi editate utilizând experiența de editare la rând din grilă. Atunci când procentajele de împărțire a facturării nu totalizează 100%, veți primi o eroare. După ce editați procentele de facturare împărțite, reîmprospătați pagina pentru a îndepărta eroarea.

De asemenea, puteți selecta **Distribuiți uniform** pe subgrila **Clienți contractuali** pentru a aloca fracțiuni de facturare în mod egal tuturor clienților contractuali. Dacă există un factor de rotunjire, acesta va fi adăugat clientului de rotunjire. Unul dintre clienții contractului este întotdeauna etichetat ca client de **rotunjire**, ceea ce înseamnă că înregistrarea clientului contractului are marcajul de rotunjire setat la **Da**. De obicei, acesta este clientul principal al contractului, dar poate fi schimbat și el.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]