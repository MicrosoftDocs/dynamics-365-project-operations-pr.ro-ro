---
title: Gestionarea mai multor clienți într-o ofertă de proiect
description: Acest subiect furnizează informații despre lucrul la oferte care implică mai mulți clienți care vor finanța proiectul.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: eef3e8754cdfdb810ffd5283976445edbb126b51e20d5b51d603d2ba9e2c02c9
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/06/2021
ms.locfileid: "6991996"
---
# <a name="manage-multiple-customers-on-a-project-quote"></a>Gestionarea mai multor clienți într-o ofertă de proiect

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Cotațiile proiectului susțin scenariul în care propunerea implică mai mulți clienți care vor finanța afacerea. Fila **Rezumat** a Ofertei are câmpul **Client potențial** care identifică clientul principal al tranzacției. Alți clienți pentru afacere pot fi setați pe fila **Clienți** a ofertei de proiect.

Toți clienții de ofertă de pe fila **Clienți** din oferta de proiect implicită ca clienți de linie de ofertă pe orice linii **noi** de ofertă bazate pe proiect create pentru ofertă. Orice linie de ofertă existentă bazată pe proiect nu va moșteni înregistrările noi ale clienților de ofertă create după acestea.

Clienții de ofertă și clienții de linie de ofertă pot fi adăugați, actualizați sau șterse în orice moment înainte de a câștiga oferta. Un client valid din ofertă trebuie să fie înființat ca client în compania deținătoare sau entitate juridică de pe pagina **Clienți**. Persoanele juridice sunt configurate în modulul **Management de proiect și contabilitate** al Dynamics 365 Project Operations și sunt puse la dispoziție drept Companii în modulele **Vânzări de proiect și Livrare** din Project Operations.

## <a name="concept-of-a-primary-customer"></a>Conceptul de client principal

Clientul listat pe fila **Rezumat** a ofertei de proiect drept client potențial este clientul principal al ofertei. Când încercați să ștergeți clientul principal din lista de clienți din ofertă, veți primi o eroare conform căreia înregistrarea unui client principal dintr-o ofertă nu poate fi ștearsă.

Clientul principal nu ar trebui să fie actualizat din lista de clienți din ofertă. Cu toate acestea, puteți influența clientul principal schimbând clientul potențial pe fila **Rezumat** a ofertei. Când acest câmp este actualizat pe **Rezumat ofertă**, clientul potențial nou selectat este adăugat ca un nou client de ofertă cu setul de semnalizare **Primar**. Vechiul client potențial va rămâne în continuare client la ofertă.

## <a name="create-update-or-delete-a-quote-customer-record"></a>Creați, actualizați sau ștergeți o înregistrare de ofertă client

Un client de ofertă poate fi creat, actualizat sau șters din fila **Clienți de ofertă** de pe pagina **Ofertă**. Câmpurile enumerate în tabelul următor sunt în evidența clienților de ofertă a unei oferte de proiect.

| **Câmp** | **Locaţie** | **Descriere** | **Impactul din aval** |
| --- | --- | --- | --- |
| Cont | Grilă editabilă pe fila **Clienți de ofertă** și formularele **Principal** și **Creare rapidă** pentru un client de ofertă. | Listează toate conturile active. Acest câmp este blocat după crearea înregistrării. Dacă doriți să o actualizați, ștergeți înregistrarea și recreați-o. Dacă ați înregistrat date reale sau dacă înregistrarea clientului de ofertă este un client principal, vi se va permite să ștergeți înregistrarea. | Clienții de ofertă sunt copiați peste drept clienți de linie de ofertă când este creată o linie de ofertă. Clienții de ofertă sunt copiați și peste clienții de contract de proiect când este câștigată o ofertă. |
| Procent de divizare de factură | Grilă editabilă pe fila **Clienți de ofertă** și formularele **Principal** și **Creare rapidă** pentru un client de ofertă. | Reprezentați procentul din fiecare tranzacție de vânzare nefacturată care va fi atribuită acestui client de ofertă. | Copiat pe noi linii de ofertă create și pe clienții contractuali de proiect. |
| Facturare către nume persoană de contact | Grilă editabilă pe fila **Clienți de ofertă** și formularele **Principal** și **Creare rapidă** pentru un client de ofertă. | Acesta este un câmp text și trebuie utilizat pentru a identifica persoana de contact cu factura pentru acest client. Acestea sunt implicite din înregistrarea contului aferent | Copiat peste clienții contractului de proiect atunci când se câștigă o ofertă și, la rândul său, la câmpul Numele facturii către contract de pe factura generată pentru acest client. |
| Facturare către nume | Grilă editabilă pe fila **Clienți de ofertă** și formularele **Principal** și **Creare rapidă** pentru un client de ofertă. | Acest câmp text ar trebui utilizat pentru a identifica persoana de contact cu factura pentru acest client. | Copiat clienților contractului de proiect atunci când se câștigă o ofertă și, la rândul său, la câmpul **Numele facturii către contract** de pe factura generată pentru acest client. |
| Condiții de plată | Grilă editabilă pe fila **Clienți de ofertă** și formularele **Principal** și **Creare rapidă** pentru un client de ofertă. | Acesta este un set de opțiuni cu valori care sunt implicite din înregistrarea contului aferent. | Copiat clienților contractului de proiect atunci când se câștigă o ofertă și, la rândul său, la câmpul **Numele facturii către contract** de pe factura generată pentru acest client. |
| Este rotunjire | Grilă editabilă pe fila **Clienți de ofertă** și formularele **Principal** și **Creare rapidă** pentru un client de ofertă. | Indică dacă acest client este un client implicit de rotunjire pentru această ofertă. | Copiat clienților contractului de proiect atunci când se câștigă o ofertă. |
| Firmă proprietară | Grilă editabilă pe fila **Clienți de ofertă** și formularele **Principal** și **Creare rapidă** pentru un client de ofertă. | Persoana juridică înființată de acest client în cadrul modulului **Management de proiect și contabilitate**. Acest câmp este numai în citire și este setat la compania proprietară a ofertei în sine. Lista clienților de adăugat în câmpul **Cont** este deja filtrat în lista de la această companie deținută în **Management de proiect și contabilitate** modulul Project Operations. | Compania deținătoare echivalează cu conceptul de entitate juridică din modulul **Management de proiect și contabilitate** Project Operations. Toate costurile și veniturile generate de acest proiect sunt contabilizate în registrul general al companiei proprietar, |
| Limită de nedepășire | Grilă editabilă pe fila **Clienți de ofertă** și formularele **Principal** și **Creare rapidă** pentru un client de ofertă. | Indică dacă există o limită superioară sau o limită negociată pentru suma totală care va fi facturată acestui client pentru acest angajament. | Copiat clienților contractului de proiect atunci când se câștigă o ofertă. |

## <a name="editing-billing-split-percentages"></a>Editarea procentajelor de facturare

Puteți modifica procentajele de împărțire a facturării utilizând experiența de editare a grilei în linie. Atunci când procentajele de împărțire a facturării nu totalizează 100%, va apărea o eroare. După actualizarea procentajelor de facturare, actualizați pagina pentru a elimina eroarea.

De asemenea, puteți încerca să selectați **Distribuiți uniform** pe subgrila clienților de cotare. Această acțiune alocă împărțiri de facturare tuturor clienților de ofertă. Dacă există vreun factor de rotunjire, acesta va fi adăugat clientului de rotunjire. Unul dintre clienții de cotare este întotdeauna etichetat drept client de rotunjire. Acest lucru înseamnă că înregistrarea clientului de ofertă are semnalizarea **Rotunjire** setată la **Da**. De obicei, acesta este clientul principal al ofertelor, dar acesta poate fi modificat.


[!INCLUDE[footer-include](../includes/footer-banner.md)]