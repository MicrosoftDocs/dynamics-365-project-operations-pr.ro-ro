---
title: Gestionarea restanțelor de facturare
description: Acest subiect oferă informații despre cum să vizualizați și să lucrați cu restanțele de facturare în Project Operations.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c3752abd26e760d27320d2b86079d84a967d53cf
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287748"
---
# <a name="manage-the-billing-backlog"></a>Gestionarea restanțelor de facturare

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Dynamics 365 Project Operations are două vizualizări dedicate pentru vă ajuta să gestionați și să lucrați cu vânzările nefacturate. Sunt **Repere cu preț fix** și **Restanțe de facturare de timp și materiale** Pentru a selecta o vizualizare, în zona **Vânzări** a Project Operations, în pagina de navigare din stânga, selectați **Facturare**. Acolo sunt stocate linkurile către restanțele de facturare.

## <a name="fixed-price-milestones"></a>Repere cu preț fix

Această vizualizare listează toate etapele prețurilor fixe pe toate liniile contractuale de proiect din sistem. Repere unice sau multiple pot fi marcate ca **Gata de facturare** sau **Nu sunt gata de facturare** din această perspectivă. Când marcați un reper ca **Gata de facturare**, reperul devine disponibil pentru o schiță de factură.

Atunci când liniile contractuale pentru mai mulți clienți au o metodă de facturare la preț fix, se creează un reper pentru fiecare client de pe linia contractuală. Utilizatorul creează o etapă de referință și acea etapă de împărțire este împărțită în client = înregistrări de repere specifice intern, în funcție de procentul de facturare împărțit definit pentru fiecare client pe linia de contract. În vizualizarea **Repere cu preț fix**, veți vedea înregistrări individuale specifice pentru clienți. Fiecare dintre aceste înregistrări de referință poate fi marcată ca **Gata de facturare** separat de această vizualizare. Atunci când una sau mai multe dintre împărțirile de referință aferente sunt marcate ca **Gata de facturare**, antetul trece la o stare de **În progres** din **Nu a început**. Când au fost facturate toate împărțirile etapei, starea etapei antet devine **Efectuat**.

O etapă importantă pentru o schiță de factură este afișată în această vizualizare cu o stare de facturare de **Factura clientului a fost creată**. Când se confirmă proiectul de factură, starea de facturare din această înregistrare este actualizată la **Factură postată**. Actualizarea acestei valori de stare prin utilizarea codului personalizat nu este recomandată. Project Operations nu vor funcționa corect dacă aceste valori de stare sunt actualizate cu cod personalizat.

## <a name="time-and-material-billing-backlog"></a>Jurnal de așteptare pentru facturarea timpului și a materialelor

Această vizualizare listează toate cifrele reale de vânzare care nu au fost facturate în toate contractele de proiect din sistem. Datele reale de vânzări nefacturate unice sau multiple pot fi marcate ca **Gata de facturare** sau **Nu sunt gata de facturare** din această vizualizare. Marcarea unei vânzări nefacturate ca fiind **Gata de facturare** o face disponibilă pentru a fi pus pe schiță de factură.

Vânzări reale facturate care au o stare de **A nu depăși** de **Eșuat** nu poate fi marcat ca **Gata de facturare**. Dacă aceste date reale trebuie să fie marcate ca atare, resetați starea pe alte date reale pe linia contractului care sunt angajate, apoi evaluați starea **A nu depăși**.

În cazul liniilor contractuale cu mai mulți clienți care au o metodă de facturare a timpului și a materialelor, atunci când timpul și cheltuielile sunt aprobate, se creează o vânzare reală nefacturată pentru fiecare client pe linia contractului în funcție de procentul de facturare împărțit definit pentru fiecare client pe linie contractuală. În vizualizarea **Restanțe de facturare de timp și materiale**, veți vedea aceste rezultate individuale de vânzări nefacturate specifice clienților. Fiecare dintre aceste înregistrări de vânzări nefacturate poate fi marcată ca **Gata de facturare** separat de această vizualizare.

Date reale de vânzări negacturate pe o schiță de factură este afișată în această vizualizare cu o **Stare de facturare** de **Factura clientului a fost creată**. Când se confirmă schița de factură, starea de facturare din această înregistrare este actualizată la **Factura clientului a fost postată**. Actualizarea acestei valori de stare când se află în această stare prin utilizarea codului personalizat nu este recomandată. Project Operations nu vor funcționa corect când aceste valori de stare sunt actualizate cu cod personalizat.


[!INCLUDE[footer-include](../includes/footer-banner.md)]