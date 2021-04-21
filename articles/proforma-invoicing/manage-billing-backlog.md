---
title: Gestionarea restanțelor de facturare
description: Acest subiect oferă informații despre cum să vizualizați și să lucrați cu restanțele de facturare în Project Operations.
author: rumant
manager: Annbe
ms.date: 04/05/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: e428b551a755220cee67d54b2e63dd7a3c2ca393
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 04/07/2021
ms.locfileid: "5866792"
---
# <a name="manage-billing-backlog"></a>Gestionarea restanțelor de facturare

_ **Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc

Dynamics 365 Project Operations are vizualizări dedicate pentru a ajuta la gestionarea vânzărilor nefacturate. Pentru a gestiona restanțele de facturare, selectați linkurile din zona **Vânzări**, sub **Facturare**. 

Sunt disponibile următoarele vizualizări:

- Onorarii și avansuri
- Onorarii și avansuri disponibile
- Repere cu preț fix
- Jurnal de așteptare pentru facturarea timpului și a materialelor

## <a name="retainers-and-advances"></a>Onorarii și avansuri

Vizualizarea **Rețineri și avansuri** listează reținerile și avansurile în toate contractele de proiect. După facturarea unui onorariu sau avans, suma avansului devine disponibilă pentru utilizare.

## <a name="available-retainers-and-advances"></a>Onorarii și avansuri disponibile

Vizualizarea **Rețineri și avansuri disponibile** listează toate reținerile și avansurile disponibile din toate contractele de proiect. După facturarea unui onorariu sau avans, suma avansului devine disponibilă pentru utilizare și este adăugată la listă. După ce suma reținerii sau avansului este utilizată complet, este eliminată din listă.

## <a name="fixed-price-milestones"></a>Repere cu preț fix

Vizualizarea **Repere cu preț fix** listează toate reperele prețurilor fixe de pe toate liniile contractuale ale proiectului. Din această vizualizare, marcajele unice sau multiple pot fi marcate ca **Gata de facturare** sau **Nu este pregătit pentru facturare**. Marcarea unui reper ca **Gata de facturare** îl pune la dispoziție pentru a fi pus pe o schiță de factură.

Atunci când liniile contractuale pentru mai mulți clienți au o metodă de facturare la preț fix, se creează o etapă importantă pentru fiecare client de pe linia contractuală. O etapă de referință poate fi creată și apoi împărțită în înregistrări individuale specifice de client. Această împărțire este internă și în conformitate cu procentul de facturare împărțit definit pentru fiecare client pe linia contractului. În vizualizarea **Repere cu preț fix**, veți vedea înregistrările individuale de referință specifice clientului. Fiecare dintre aceste înregistrări de referință poate fi marcată ca **Gata de facturare** separat de această vizualizare. Atunci când una sau mai multe dintre împărțirile marcajelor legate sunt marcate ca **Gata de facturare**, starea antetului se actualizează la **În curs** din **Nu a început**. Când toate facturile de reper sunt facturate, starea antetului reperului se actualizează la **Finalizat**.

O etapă importantă pentru o schiță de factură este afișată în această vizualizare cu o stare de facturare de **Factura clientului a fost creată**. Când se confirmă schița de factură, starea de facturare din înregistrare este actualizată la **Factură de client publicată**. 

> [!NOTE] 
> Nu actualizați această valoare de stare utilizând cod personalizat. Project Operations nu funcționează corect atunci când aceste valori de stare sunt actualizate cu cod particularizat.

## <a name="time-and-material-billing-backlog"></a>Jurnal de așteptare pentru facturarea timpului și a materialelor

Vizualizarea **Restanțe de facturare de timp și materiale** listează toate efectele de vânzare necotificate din toate contractele de proiect din sistem care nu au fost facturate. Datele reale de vânzări nefacturate unice sau multiple pot fi marcate ca **Gata de facturare** sau **Nu sunt gata de facturare** din această vizualizare. Marcarea unei vânzări nefacturate ca fiind **Gata de facturare** o face disponibilă pentru a fi pus pe schiță de factură.

Vânzări reale facturate cu o stare **A nu depăși** la **Eșuat** nu poate fi marcat ca **Gata de facturare**. Dacă valorile reale trebuie să fie marcate ca **Gata de facturare**, resetați starea pe celelalte valori reale de pe linia de contract care sunt angajate și apoi reevaluați starea **A nu se depăși**.

În cazul în care liniile contractuale cu mai mulți clienți au o metodă de facturare a timpului și a materialelor, atunci când timpul și cheltuielile sunt aprobate, se creează o vânzare reală nefacturată pentru fiecare client de pe linia contractului în funcție de procentul de facturare împărțit definit pentru fiecare dintre clienți. În vizualizarea **Restanțe de facturare de timp și materiale**, veți vedea aceste rezultate individuale ale vânzărilor nefacturate specifice fiecărui client. Fiecare dintre aceste înregistrări de vânzări nefacturate poate fi marcată ca **Gata de facturare** separat de această vizualizare.

O valoare reală de vânzări nefacturate care se află pe o factură nefinalizată este afișat în această vizualizare cu starea de facturare **Factura clientului a fost creată**. Când se confirmă schița de factură, starea de facturare din această înregistrare este actualizată la **Factura clientului a fost postată**. 

> [!NOTE] 
> Nu actualizați această valoare de stare utilizând cod personalizat. Project Operations nu funcționează corect atunci când aceste valori de stare sunt actualizate cu cod particularizat.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
