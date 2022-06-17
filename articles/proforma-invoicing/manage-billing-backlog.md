---
title: Gestionarea restanțelor de facturare
description: Acest articol oferă informații despre cum să vizualizați și să lucrați cu restanța de facturare în Operațiuni de proiect.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 5be05639650bb5b9d646067e8d83bada60824081
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929393"
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
