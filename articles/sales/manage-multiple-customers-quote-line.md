---
title: Gestionați mai mulți clienți în linii de oferte bazate pe proiect
description: Acest subiect oferă informații despre cum să gestionați mai mulți clienți pe linii de ofertă pe bază de proiect.
author: rumant
manager: Annbe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ffb89a954b8af9d726c64cceeafca638c3393130
ms.sourcegitcommit: fd8ea1779db2bb39a428f459ae3293c4fd785572
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/06/2020
ms.locfileid: "3965865"
---
# <a name="manage-multiple-customers-on-project-based-quote-lines"></a>Gestionați mai mulți clienți în linii de oferte bazate pe proiect

Liniile de ofertă bazate pe proiecte acceptă scenarii în care fiecare linie de ofertă are o listă de clienți care plătesc pentru aceasta. Această listă de clienți de pe linia de ofertă bazată pe proiecte poate fi aceeași cu lista de clienți din ofertă. De asemenea, puteți modifica lista clienților pentru a fi diferiți. Pentru a crea contractul eventualului proiect când se câștigă o ofertă de proiect, lista de clienți de pe linia de ofertă bazată pe proiect este copiată pe linia de contract corespunzătoare bazată pe proiect. Clienții din oferta pe bază de de proiect sunt copiați în contractul de proiect.

Când facturați eventualul contract de proiect, lista clienților de pe linia de contract bazată pe proiect are prioritate față de lista din contractul de proiect. Lista clienților din contractul de proiect este utilizată pentru valorile implicite ale noilor linii de contract de proiect.

Toți clienții de ofertă de pe fila **Clienți** a ofertei de proiect sunt implicit clienți de linie de ofertă pe orice linii noi de ofertă bazată pe proiect create pentru oferta de proiect. Orice linie de ofertă existentă bazată pe proiect nu moștenesc înregistrările noi ale clienților de ofertă create după acestea.

## <a name="create-update-or-delete-a-quote-line-customer-record"></a>Creați, actualizați sau ștergeți o înregistrare de client de linie de ofertă

Puteți crea, actualiza sau șterge un client de linie de ofertă pe fila **Clienți de linie de ofertă** de pe pagina **Linie de ofertă bazată pe proiect**. Când adăugați un client nou pe linia de ofertă bazată pe proiecte, clientul este adăugat și la oferta globală ca client de ofertă, cu un procent implicit împărțit de facturare la oferta generală de 0%. Procentul de împărțire a facturării din oferta globală este copiat pe liniile noi de ofertă și în eventualul contract de proiect. Cu toate acestea, facturați din contract, se folosește procentul de împărțire a facturării la nivelul liniei de ofertă, nu procentul de împărțire a facturării la nivelul global al contractului. 

Tabelul următor arată câmpurile pe înregistrarea de client de linie de ofertă a unei linii de ofertă bazată pe proiect.

| Câmp | Locație | Descriere și îndrumare | Impactul din aval |
| --- | --- | --- | --- |
| **Cont** | O grilă editabilă pe fila **Clienți de linie de ofertă**, formularul principal și formularul de creare rapidă pentru un client de linie de ofertă. | Listează toate conturile active. Acest câmp este blocat după crearea înregistrării. Dacă trebuie să actualizați câmpul, ștergeți și recreați înregistrarea. Dacă ați înregistrat date reale, nu puteți șterge înregistrarea. | Atunci când alegeți un cont din lista principală de conturi de adăugat, clientul de linie de ofertă este adăugat și ca client de ofertă. Când se câștigă o ofertă, clienții liniei de ofertă sunt copiați la clienții din linia contractului de proiect. |
| **Procent de divizare de factură** | O grilă editabilă pe fila **Clienți de linie de ofertă**, formularul principal și formularul de creare rapidă pentru un client de linie de ofertă. | Reprezintă procentul din fiecare tranzacție de vânzare nefacturată care va fi atribuită acestui client de linie de ofertă. | Copiat pentru clienți de linii de contract de proiect. |
| **Limită de nedepășire** | O grilă editabilă pe fila **Clienți de linie de ofertă**, formularul principal și formularul de creare rapidă pentru un client de linie de ofertă. | Indică dacă există o limită superioară sau o limită negociată pentru suma totală care va fi facturată acestui client pentru această linie de ofertă. | Copiat clienților de linii de contract de proiect atunci când se câștigă o ofertă. |
| **Firmă deținătoare** | O grilă editabilă pe fila **Clienți de linie de ofertă**, formularul principal și formularul de creare rapidă pentru un client de linie de ofertă, | Entitatea juridică în care este instalat acest client în cadrul modulului **Management de proiect și contabilitate**. Acest câmp este numai în citire și este setat la compania proprietară a ofertei în sine. Lista clienților de adăugat în câmpul **Cont** este deja filtrat în lista de la această companie deținătoare în modulul **Management de proiect și contabilitate** din Project Operations. | Compania deținătoare echivalează cu conceptul de persoană juridică. Toate costurile și veniturile care se acumulează de acest proiect sunt contabilizate în registrul general al companiei deținătoare. |
| **Este rotunjire** | O grilă editabilă pe fila **Clienți de linie de ofertă**, formularul principal și formularul de creare rapidă pentru un client de linie de ofertă. | Indică dacă acest client este un client implicit de rotunjire pentru această linie de ofertă bazată pe proiect. | Copiat clienților de contract de proiect atunci când se câștigă o ofertă. |

## <a name="edit-billing-split-percentages"></a>Editați procente de facturare

Puteți modifica procentele de facturare împărțite în linie. Atunci când procentajele de împărțire a facturării nu totalizează 100%, apare o eroare. După editare procentajelor de facturare, actualizați pagina de linie de ofertă pentru a elimina eroarea.

Utilizați acțiunea de distribuire uniformă pe subgrila clienților liniei de ofertă pentru a aloca împărțiri de facturare tuturor clienților din linia de ofertă. Dacă există un factor de rotunjire, acesta va fi adăugat clientului de rotunjire. Unul dintre clienții liniei de ofertă este întotdeauna etichetat ca client de rotunjire, ceea ce înseamnă că înregistrarea clientului de linie de ofertă are marcajul de rotunjire setat la **Da**. 
