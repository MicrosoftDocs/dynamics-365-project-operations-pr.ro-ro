---
title: Ce este nou în martie 2022 - Implementare simplificată Project Operations
description: Acest articol oferă informații despre actualizările de calitate care sunt disponibile în versiunea din martie 2022 de implementare a Project Operations lite.
author: sigitac
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 321d59568bfd33bb00a1500afe514fbecf9a0250
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8934243"
---
# <a name="whats-new-march-2022---project-operations-lite-deployment"></a>Ce este nou în martie 2022 - Implementare simplificată Project Operations

_Se aplică pentru: implementare simplificată - înțelegere la emiterea facturii proforme_

Acest articol se aplică următoarelor componente și versiuni de Microsoft Dynamics 365 Project Operations:

- Project Operations într-un mediu Dataverse versiunea 4.30.0.99

## <a name="features-included-in-this-release"></a>Caracteristicile incluse în această versiune

- Subcontractare: crearea de facturi de furnizor și experiențe de potrivire

## <a name="quality-updates"></a>Actualizări de calitate

| Zonă de caracteristici | Număr de referință | Actualizare de calitate |
| --- | --- | --- |
| Timp și cheltuieli | 2388011 | Afișați comentariile de respingere celor care trimit înregistrările de timp în timpul aprobării în bloc. |
| Planificarea și urmărirea proiectului | 2495294 | Detaliile proiectului nu trebuie să fie editabile pe pagina **Detalii sarcină**. |
| Facturarea și stabilirea prețurilor | 2499605 | Etapele contractuale care sunt create din reperele de cotație sunt marcate incorect ca doar pentru citire. |
| Planificarea și urmărirea proiectului | 2506050 | Setul de operațiuni rămâne în așteptare timp de o oră dacă nu există nicio modificare de salvat. Setul este apoi marcat fals ca **Eșuat**, în timp ce ar trebui finalizat imediat. |
| Facturarea și stabilirea prețurilor | 2507401 | Unitățile de contractare implicite sunt introduse incorect în proiecte din cauza memorării incorecte în cache. |
| Facturarea și stabilirea prețurilor | 2541660 | **Validarea creării comenzii de vânzare** în scriere duală ar trebui să fie doar pentru comenzi bazate pe proiecte. |
| Facturarea și stabilirea prețurilor | 2552745 | Impozitul nu este împărțit între clienții care au stabilit reguli de facturare divizate. |
| Facturarea și stabilirea prețurilor | 2558859 | Mesaje de eroare îmbunătățite atunci când sunt configurați parametrii de preț. |
| Facturarea și stabilirea prețurilor | 2558933 | **Import din estimări de proiect** eșuează când **msdyn\_proiect** este adăugată ca dimensiune a prețului. |
| Facturarea și stabilirea prețurilor | 2559101 | Ștergerea parametrilor de proiect nu este blocată și provoacă probleme. |
| Managementul oportunităților | 2570390 | Pluginul cu scriere duală obligă ca tipul de cont pe oferte, comenzi și oportunități să fie **Client**, chiar și atunci când acel tip de cont nu este corect. |
| Facturarea și stabilirea prețurilor | 2586097 | Costurile reale facturate împărțite nu sunt inversate atunci când un proiect este eliminat dintr-o linie de contract de proiect. |
| Facturarea și stabilirea prețurilor | 2589619 | Impozitul pe materialul din afara catalogului este propagat la valorile reale de vânzări nefacturate și la factură. |
| Managementul oportunităților | 2594015 | O ofertă nu poate fi închisă ca fiind câștigată pentru clienții care au termeni de plată **Net60**. |
| Planificarea și urmărirea proiectului | 2595841 | În Project for the Web, utilizatorii primesc un mesaj de eroare despre o lipsă **msdyn\_actualstart** când creează o nouă cerere de resursă. |
| Timp și cheltuială | 2602511 | Câmpul **Respins de** pentru intrările de timp afișează **Sistem** în loc de un utilizator numit ca respingător. |
| Timp și cheltuială | 2602528 | Un aprobator de proiect poate aproba timpul pentru proiectele în care nu sunt listate ca aprobator. |
| Facturarea și stabilirea prețurilor | 2608550 | O factură de corectare poate fi confirmată chiar dacă nu există modificări ale originalului |

## <a name="removed-and-deprecated-features"></a>Caracteristici eliminate și perimate

Articolul [Caracteristici eliminate sau perimate în Project Operations](../../whats-new/removed-depreciated-features-project.md) descrie funcțiile care au fost eliminate sau perimate pentru Dynamics 365 Project Operations.

- O caracteristică eliminat nu mai este disponibilă în produs.
- O caracteristică perimată nu este în dezvoltare activă și ar putea fi eliminată într-o actualizare viitoare.

Un anunț de perimare va apărea în articolul [Caracteristici eliminate sau perimate în Project Operations](../../whats-new/removed-depreciated-features-project.md) cu 12 luni înainte ca orice caracteristică să fie eliminată din produs.
