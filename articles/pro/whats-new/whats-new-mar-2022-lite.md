---
title: Ce este nou în martie 2022 - Implementare simplificată Project Operations
description: Acest subiect oferă informații despre actualizările de calitate care sunt disponibile în versiunea din martie 2022 a implementării Project Operations lite.
author: sigitac
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 8a83491da1d312406dfb36f5ad214c307c15cfbf
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8583765"
---
# <a name="whats-new-march-2022---project-operations-lite-deployment"></a>Ce este nou în martie 2022 - Implementare simplificată Project Operations

_Se aplică pentru: implementare simplificată - înțelegere la emiterea facturii proforme_

Acest subiect se aplică următoarelor componente și versiuni ale Microsoft Dynamics 365 Project Operations:

- Operațiuni de proiect în a Dataverse versiunea de mediu 4.30.0.99

## <a name="features-included-in-this-release"></a>Caracteristicile incluse în această versiune

- Subcontractare: crearea de facturi de furnizor și experiențe de potrivire

## <a name="quality-updates"></a>Actualizări de calitate

| Zonă de caracteristici | Număr de referință | Actualizare de calitate |
| --- | --- | --- |
| Timp și cheltuieli | 2388011 | Afișați comentariile de respingere celor care trimit datele de timp în timpul aprobării în bloc. |
| Planificarea și urmărirea proiectului | 2495294 | Detaliile proiectului nu trebuie să fie editabile pe **Detalii despre sarcină** pagină. |
| Facturarea și stabilirea prețurilor | 2499605 | Etapele contractului care sunt create din reperele de cotație sunt marcate incorect ca doar pentru citire. |
| Planificarea și urmărirea proiectului | 2506050 | Setul de operații rămâne în așteptare timp de o oră dacă nu există nicio modificare de salvat. Setul este apoi marcat fals ca **A eșuat**, în timp ce ar trebui finalizat imediat. |
| Facturarea și stabilirea prețurilor | 2507401 | Unitățile de contractare implicite sunt introduse incorect în proiecte din cauza memorării în cache incorecte. |
| Facturarea și stabilirea prețurilor | 2541660 | **Validarea creării comenzii de vânzare** în dublă scriere ar trebui să fie doar pentru comenzi bazate pe proiecte. |
| Facturarea și stabilirea prețurilor | 2552745 | Taxele nu sunt împărțite între clienții care au stabilit reguli de facturare divizate. |
| Facturarea și stabilirea prețurilor | 2558859 | Mesaje de eroare îmbunătățite la configurarea dimensiunilor de preț. |
| Facturarea și stabilirea prețurilor | 2558933 | **Import din estimări de proiect** eșuează când **msdyn\_ proiect** este adăugată ca dimensiune a prețului. |
| Facturarea și stabilirea prețurilor | 2559101 | Ștergerea parametrilor de proiect nu este blocată și provoacă probleme. |
| Managementul oportunităților | 2570390 | Pluginul cu dublă scriere forțează tipul de cont pe cotații, comenzi și oportunități să fie **Client**, chiar și atunci când acel tip de cont nu este corect. |
| Facturarea și stabilirea prețurilor | 2586097 | Costurile efective facturate divizate nu sunt inversate atunci când un proiect este eliminat dintr-o linie de contract de proiect. |
| Facturarea și stabilirea prețurilor | 2589619 | Taxa pe materialul înscris este propagată în efectivele de vânzări nefacturate și pe factură. |
| Managementul oportunităților | 2594015 | O cotație nu poate fi închisă ca câștigată pentru clienții care au **Net60** termeni de plată. |
| Planificarea și urmărirea proiectului | 2595841 | În Project for the Web, utilizatorii primesc un mesaj de eroare despre o lipsă **msdyn\_ actualstart** când creează o nouă cerere de resursă. |
| Timp și cheltuială | 2602511 | The **Respins de** se afișează câmpul pentru intrările de timp **Sistem** în loc de un utilizator numit ca respingător. |
| Timp și cheltuială | 2602528 | Un aprobator de proiect poate aproba timpul pentru proiectele în care nu sunt listate ca aprobare. |
| Facturarea și stabilirea prețurilor | 2608550 | O factură de corectare poate fi confirmată chiar dacă nu există modificări la original. |

## <a name="removed-and-deprecated-features"></a>Funcții eliminate și depreciate

The [Caracteristici eliminate sau depreciate în Operațiuni de proiect](../../whats-new/removed-depreciated-features-project.md) subiectul descrie caracteristici pentru care au fost eliminate sau depreciate Dynamics 365 Project Operations.

- O caracteristică eliminat nu mai este disponibilă în produs.
- O funcție învechită nu este în dezvoltare activă și ar putea fi eliminată într-o actualizare viitoare.

Un anunț de depreciere va apărea în [Caracteristici eliminate sau depreciate în Operațiuni de proiect](../../whats-new/removed-depreciated-features-project.md) subiect cu 12 luni înainte ca orice caracteristică să fie eliminată din produs.
