---
title: Crearea și aplicarea condițiilor de reținere a plăților către furnizor
description: Acest subiect oferă informații despre cum să configurați și să mențineți termenii de retenție pentru plățile furnizorilor.
author: Yowelle
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 1970a24a5073de6af43db1f1c068332c9ba9c8fe
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082933"
---
# <a name="create-and-apply-vendor-payment-retention-terms"></a>Crearea și aplicarea condițiilor de reținere a plăților către furnizor

[!include [banner](../includes/banner.md)] 

Configurarea condițiilor de păstrare a plăților pentru furnizori pentru un proiect este utilă atunci când organizația dvs. dorește să rețină o parte din plățile efectuate către un furnizor. De exemplu, atunci când doriți să rețineți plata către un furnizor până când produsele livrate îndeplinesc așteptările dvs. Condițiile de păstrare a plăților furnizorului pot fi specificate atunci când negociați un contract de furnizor.

## <a name="create-vendor-payment-retention-terms"></a>Crearea condițiilor de reținere a plăților către furnizor

Puteți introduce procentul plății furnizorului pentru păstrare și procentul sumelor reținute anterior care urmează să fie eliberate. Sumele sunt reținute automat pe facturile furnizorului până când contractul atinge starea de finalizare specificată. După ce configurați termenii de reținere, îi puteți aplica oricărui proiect pentru acel furnizor.

Urmați pașii următori pentru a configura și a menține termenii de reținere pentru plățile furnizorilor. 

1. Accesați **Management de proiect și contabilitate** > **Retenție** > **Condiții de reținere a plăților către furnizor**.
2. Selectați **Nou** pentru a adăuga un nou termen de reținere a furnizorului. Valoarea **ID-ul regulii** pentru noul termen este introdusă automat. 
3. Introduceți o scurtă descriere în câmpul **Descriere** și pe **Termeni** al FastTab, selectați **Adăugați linie** pentru a introduce valori de termen pentru următoarele:

   - **Procentul de unități livrate** : Introduceți un procent de finalizare pentru termen. Sumele sunt reținute automat pe facturile furnizorului până când etapa de finalizare a proiectului este egală cu procentul specificat. De exemplu, dacă introduceți 50,00, sumele sunt reținute până când proiectul este finalizat cu 50%.
   - **Procent de păstrat** : Introduceți un procent din suma facturii furnizorului care urmează să fie reținută. De exemplu, dacă introduceți 10,00, atunci 10 la sută din suma pe o factură de furnizor este reținută până când proiectul atinge procentul de finalizare stabilit în **Câmpul procentului de unități livrate**.
   - **Procent de eliberat** : Selectați **Adăugați linie** pentru a introduce un procent din sumele reținute anterior care urmează să fie eliberate pentru nivelul selectat de finalizare a proiectului.

> [!NOTE]
> Dacă aveți mai mult de o etapă pentru niveluri diferite de finalizare a proiectului, introduceți o linie separată de termen de retenție pentru furnizor pentru fiecare regulă de retenție. Fiecare linie poate specifica un procent de retenție diferit și un procent de eliberare diferit pentru fiecare nivel desemnat de finalizare a proiectului.

După ce creați termeni de retenție a furnizorului pentru un furnizor, puteți aplica termenii unui proiect.

## <a name="apply-vendor-retention-terms-to-a-project"></a>Aplicați condițiile de retenție ale furnizorilor unui proiect

1. Accesați **Management de proiect și contabilitate** > **Proiecte** > **Toate proiectele** și deschideți un proiect din pagina listei de proiecte.
2. Pe **Acorduri de vânzător** FastTab, selectați **Adăugați linie**.
3. În **Câmpul codului contului** , selectați una dintre următoarele opțiuni: 

   - **Tabel** : Termenii de retenție a furnizorilor se aplică unui singur furnizor.
   - **Grup** : Termenii de retenție a furnizorilor se aplică tuturor furnizorilor dintr-un grup de furnizori.
   - **Toți** : Condiții de retenție a furnizorilor se aplică tuturor furnizorilor.

4. În **Câmpul Furnizor/Grupul de furnizori** , selectați furnizorul sau grupul de furnizori cărora li se aplică condițiile de retenție a furnizorilor. Dacă ați selectat **Toți** în pasul anterior, acest câmp nu este disponibil.
5. În câmpul **Condiții de retenție a furnizorilor** , selectați termenii de retenție pe care i-ați creat în procedura anterioară.
6. Dacă proiectul are, de asemenea, condiții cu plată la plată (PWP) stabilite pentru furnizor, introduceți procentul de prag pentru proiect în câmpul **Procentul de prag PWP**.

Condițiile de retenție a furnizorului sunt, de asemenea, afișate pe comenzile de cumpărare pe care le creați pentru furnizor.
