---
title: Gestionarea jurnalului de așteptare pentru facturarea proiectului
description: Acest subiect oferă informații despre diferitele vizualizări disponibile de utilizat atunci când gestionați restanțele de facturare pentru proiecte.
author: rumant
ms.date: 10/26/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 27ef2ae90778394d15b979a13215c8f5af483cda0312682e9fc7256b8282b999
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/06/2021
ms.locfileid: "6988306"
---
# <a name="manage-project-billing-backlog"></a>Gestionarea jurnalului de așteptare pentru facturarea proiectului 

_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_

Dynamics 365 Project Operations are vizualizări dedicate pentru a ajuta la gestionarea vânzărilor nefacturate. Pentru a gestiona restanțele de facturare, selectați linkurile din zona **Vânzări**, sub **Facturare**. 

Sunt disponibile următoarele vizualizări:

- Onorarii și avansuri
- Onorarii și avansuri disponibile
- Repere cu preț fix
- Jurnal de așteptare pentru facturarea produselor
- Jurnal de așteptare pentru facturarea timpului și a materialelor

## <a name="retainers-and-advances"></a>Onorarii și avansuri

Vizualizarea **Onorarii și avansuri** listează toate reținerile și avansurile în toate contractele de proiect din sistem. După facturarea unui onorariu sau avans, suma avansului devine disponibilă pentru utilizare.

## <a name="available-retainers-and-advances"></a>Onorarii și avansuri disponibile

Vizualizarea **Onorarii și avansuri disponibile** listează toate reținerile și avansurile disponibile în toate contractele de proiect din sistem. După facturarea unui onorariu sau avans, suma avansului devine disponibilă pentru utilizare și este adăugată la listă. După ce suma de onorariu sau avans este utilizată complet, aceasta este eliminată din listă.

## <a name="fixed-price-milestones"></a>Repere cu preț fix

Vizualizarea **Repere cu preț fix** listează toate etapele prețurilor fixate pe toate liniile contractuale ale proiectului din sistem. Repere unice sau multiple pot fi marcate ca **Gata de facturare** sau **Nu este gata de facturare** din această vizualizare. Marcarea unui reper ca **Gata de facturare** îl pune la dispoziție pentru a fi pus pe o schiță de factură.

Atunci când liniile contractuale pentru mai mulți clienți au o metodă de facturare la preț fix, se creează o etapă importantă pentru fiecare client de pe linia contractuală. O etapă de referință poate fi creată și apoi împărțită în înregistrări individuale specifice de client. Această împărțire este internă și în conformitate cu procentul de facturare împărțit definit pentru fiecare client pe linia contractului. În vizualizarea **Repere cu preț fix**, veți vedea înregistrările individuale de referință specifice clientului. Fiecare dintre aceste înregistrări de referință poate fi marcată ca **Gata de facturare** separat de această vizualizare. Când una sau mai multe dintre împărțirile de referință aferente sunt marcate ca **Gata de facturare**, starea antetului este actualizată la **În derulare** din **Nu a început**. Când toate facturile de repartizare sunt facturate, starea de repere a antetului este actualizată la **Efectuat**.

O etapă importantă pentru o schiță de factură este afișată în această vizualizare cu o stare de facturare de **Factura clientului a fost creată**. Când se confirmă schița de factură, starea de facturare din înregistrare este actualizată la **Factură de client publicată**. Nu actualizați această valoare de stare utilizând cod particularizat. Project Operations nu funcționează corect atunci când aceste valori de stare sunt actualizate cu cod particularizat.

## <a name="product-billing-backlog"></a>Jurnal de așteptare pentru facturarea produselor

Vizualizarea **Restante de facturare a produselor** listează toate liniile de contracte bazate pe produse din toate contractele de proiect din sistem. Linii de contract de proiect bazat pe produs unice sau multiple pot fi marcate ca **Gata de facturare** sau **Nu este gata de facturare** din această vizualizare. Marcarea unei linii de contract bazat pe produs ca **Gata de facturare** îl pune la dispoziție pentru a fi pus pe o schiță de factură.

O linie de contract bazată pe produse care se află pe o schiță de factură este afișată în această vizualizare cu o stare de facturare de **Factura clientului a fost creată**. Când se confirmă schița de factură, starea de facturare din această înregistrare este actualizată la **Factura clientului a fost postată**. Nu actualizați această valoare de stare utilizând cod particularizat. Project Operations nu funcționează corect atunci când aceste valori de stare sunt actualizate cu cod particularizat.

## <a name="time-and-material-billing-backlog"></a>Jurnal de așteptare pentru facturarea timpului și a materialelor

Vizualizarea **Restanțe de facturare de timp și materiale** listează toate efectele de vânzare necotificate din toate contractele de proiect din sistem care nu au fost facturate. Datele reale de vânzări nefacturate unice sau multiple pot fi marcate ca **Gata de facturare** sau **Nu sunt gata de facturare** din această vizualizare. Marcarea unei vânzări nefacturate ca fiind **Gata de facturare** o face disponibilă pentru a fi pus pe schiță de factură.

Vânzări reale facturate cu o stare **A nu depăși** la **Eșuat** nu poate fi marcat ca **Gata de facturare**. Dacă actualele trebuie să fie marcate ca **Gata de facturare**, resetați starea pentru alte date reale de pe linia de contract angajate. și apoi reevaluați starea **A nu se depăși**.

În cazul în care liniile contractuale cu mai mulți clienți au o metodă de facturare a timpului și a materialelor, atunci când timpul și cheltuielile sunt aprobate, se creează o vânzare reală nefacturată pentru fiecare client de pe linia contractului în funcție de procentul de facturare împărțit definit pentru fiecare dintre clienți. În vizualizarea **Restanțe de facturare de timp și materiale**, veți vedea aceste rezultate individuale ale vânzărilor nefacturate specifice fiecărui client. Fiecare dintre aceste înregistrări de vânzări nefacturate poate fi marcată ca **Gata de facturare** separat de această vizualizare.

O vânzare nefacturată care este pe o schiță de factură este afișată în această vizualizare cu o stare de facturare de **Factura clientului a fost creată**. Când se confirmă schița de factură, starea de facturare din această înregistrare este actualizată la **Factura clientului a fost postată**. Nu actualizați această valoare de stare utilizând cod particularizat. Project Operations nu funcționează corect atunci când aceste valori de stare sunt actualizate cu cod particularizat.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
