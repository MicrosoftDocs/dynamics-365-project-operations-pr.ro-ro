---
title: Jaloane linie de subcontract
description: Acest subiect explică cum să creați și să mențineți un program de facturare bazat pe un jalon pentru un subcontract cu un furnizor.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3301e5a627e4842009fcd5e352f1b76fd3053ee3
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323791"
---
# <a name="subcontract-line-milestones"></a>Jaloane linie de subcontract

[!include [banner](../../includes/dataverse-preview.md)]

_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_

În Dynamics 365 Project Operations, o linie de subcontract cu o metodă de facturare la preț fix poate specifica un program de facturare bazat jalon cu furnizorul.

jaloanele pentru facturarea furnizorului pot fi generate automat utilizând o frecvență stabilită sau le puteți crea manual.

## <a name="automatically-create-a-milestone-based-invoice-schedule-for-a-subcontract-line"></a>Creați automat un program de facturare bazat pe un jalon pentru o linie de subcontract

Parcurgeți pașii următori pentru a genera automat un program de facturare bazat pe un jalon pentru un set fix de jaloane distribuite în mod egal.

1. Accesați **Setări** > **Frecvențe factură** și setați frecvența facturii pentru liniile de subcontract.
2. Deschideți pagina **Subcontracte**, deschideți subcontractul cu care doriți să lucrați, apoi deschideți linia de subcontract cu preț fix pentru care doriți să creați un program de jaloane.
3. Pe fila **Jaloane linie subcontract**, selectați **Generare jaloane periodice**.
4. În caseta de dialog, introduceți sau selectați un interval de timp, numărul de jaloane și frecvența de facturare. Puteți selecta o dată de începere sau puteți selecta numărul de jaloane și frecvența de facturare sau data de începere sau puteți selecta data de încheiere și frecvența de facturare. Nu puteți selecta data de încheiere și numărul de jaloane.
Folosind aceste informații, sistemul generează jaloane și înregistrări care sunt afișate în grila **Jaloane**.

   - **Nume jalon** - Numele jalonului este setat la data jalonului, în funcție de frecvența de facturare.
   - **Data jalonului** - Data bazată pe frecvența de facturare.
   - **Valoarea jalonului** - Calculată prin împărțirea sumei subtotalului de pe linia de subcontract la numărul de jaloane.

Dacă linia de subcontract are o valoare în câmpul **Valoare estimată taxă**, această valoare este adăugată la fiecare jalon în mod egal atunci când se generează jaloane periodice.

Suma valorilor pentru jaloanele liniei de subcontract trebuie să fie egală cu valoarea de pe linia de subcontract. Dacă nu sunt egale, apare o eroare. Puteți remedia eroarea și puteți verifica dacă totalul jalonului este egal cu valoarea liniei de subcontract prin crearea, editarea sau ștergerea valorilor de jalon și taxe. După efectuarea modificărilor, salvați și reîmprospătați pagina pentru a vă asigura că nu mai există erori.

## <a name="manually-create-subcontract-line-milestones"></a>Creați manual jaloane de linii de subcontract

Jaloanele cu preț fix de pe o linie de subcontract pot fi generate manual atunci când nu sunt împărțite periodic. Pentru a crea manual un jalon de linie de subcontract, parcurgeți pașii următori.

1. Pe panoul de navigare, selectați **Subcontracte**, apoi deschideți subcontractul cu care doriți să lucrați.
2. Deschideți linia de subcontract cu preț fix pentru care doriți să creați un jalon.
3. Pe fila **Jaloane linie de subcontract**, pe sub-grila secundară, selectați **+ Nou jalon linie subcontract**.
4. Pe pagina **Nou jalon linie subcontract**, introduceți informațiile necesare pe baza tabelului următor.

    | Câmp | Descriere |
    | --- | --- |
    | Nume jalon | Numele datei scadente. |
    | Descriere | O descriere a jalonului.  |
    | Dată jalon | Data la care procesul automat de creare a facturilor ar trebui să caute starea acestui jalon pentru a o lua în considerare la facturare. Această valoare este inclusă pe linia de facturare a furnizorului la facturarea acestui subcontract. |
    | Sumă | Valoarea sau valoarea etapei care va fi facturată clientului. Această valoare este inclusă pe linia de facturare a furnizorului la facturarea acestui subcontract. |
    | Taxe | Suma impozitului aplicată la reper. Această valoare este inclusă pe linia de facturare a furnizorului la facturarea acestui subcontract. |
    | Valoare după taxe | Acest câmp de numai citire, care este calculat ca Valoare + Taxă. Această valoare este inclusă pe linia de facturare a furnizorului la facturarea acestui subcontract. |
    | Stare factură | Când se creează jalonul, această stare este întotdeauna setată la **Nu este pregătit pentru facturare**.  Când starea este **Gata de facturare**, crearea facturii furnizorului include acest jalon pe factura furnizorului. |

5. Selectați **Salvare și închidere**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
