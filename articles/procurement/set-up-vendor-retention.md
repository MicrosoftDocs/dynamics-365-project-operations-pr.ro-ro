---
title: Configurarea reținerii furnizorilor
description: Acest subiect explică modul de configurare a păstrării furnizorului.
author: sigitac
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 9511da6212aafbf5b173efc6eb1ceaacbc8264a2
ms.sourcegitcommit: 098ea345ecfaf4445520094c32f5511b67e7953c
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/02/2021
ms.locfileid: "7594620"
---
# <a name="set-up-vendor-retention"></a>Configurarea reținerii furnizorilor

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

Acest subiect furnizează informații despre cum să configurați retenția furnizorului.

## <a name="set-up-a-vendor-retention-account-in-general-ledger"></a>Configurați un cont de păstrare a furnizorului în registrul general

1. În Dynamics 365 Finance, accesați **Registrul general** > **Configurarea publicării** > **Conturi pentru tranzacții automate**.
2. Adăugați o linie nouă.
3. În câmpul **Tip de publicare**, selectați **Păstrarea furnizorului**.
4. Selectați contul principal pentru înregistrarea de păstrare a furnizorului.

## <a name="create-vendor-retention-terms"></a>Creați termeni de păstrare a furnizorilor

Utilizați pagina **Condiții de păstrare a furnizorilor** pentru a configura și menține termenii de păstrare pentru plățile furnizorilor. Introduceți procentul plății furnizorului de reținut și procentul sumelor reținute anterior de eliberat. Sumele sunt reținute automat pe facturile furnizorului până când contractul atinge starea de finalizare specificată. După ce sunt stabiliți termenii de păstrare pentru un furnizor, îi puteți aplica la orice proiect pe care lucrează furnizorul.

1. În Finanțe, accesați **Management de proiect și contabilitate** > **Configurați** > **Retenţie** > **Condiții de păstrare a plăților furnizorilor**.
2. Selectați **Nou** pentru a adăuga un nou termen de reținere a furnizorului. Valoarea din câmpul **ID-ul regulii** se introduce automat câmpul pentru noul termen. 
3. În câmpul **Descriere**, introduceți un nume descriptiv pentru noul termen.
4. Pe fila  **Termeni**, selectați  **Adăugați linie**  pentru a introduce un termen de păstrare a furnizorului.
5. În câmpul  **Procentul de unități livrate**, introduceți un procent de finalizare pentru regulă. Sumele sunt reținute automat pe facturile furnizorului până când faza de finalizare a proiectului este egală cu procentul pe care îl introduceți. De exemplu, dacă introduceți 50,00, sumele sunt reținute până când proiectul este finalizat cu 50%.
6. În câmpul  **Procent de reținut**, introduceți procentajul unei sume de factură de vânzător de reținut. De exemplu, dacă introduceți 10.00 în acest câmp, 10 la sută din suma pe facturile furnizorului este păstrată până când proiectul atinge procentul de finalizare pe care îl selectați în câmpul  **Procentul de unități livrate**.
7. În câmpul  **Procent de eliberat**, introduceți procentajul oricăror sume reținute anterior de eliberat la nivelul selectat de finalizare a proiectului.

> [!NOTE]
> Dacă aveți mai mult de o etapă importantă pentru diferite niveluri de finalizare a proiectului, introduceți o linie separată de termen de păstrare a furnizorului pentru fiecare regulă de păstrare. Fiecare linie poate specifica un procent diferit de reținut și un procent diferit de eliberat pentru fiecare nivel desemnat de finalizare a proiectului.

## <a name="set-up-a-vendor-agreement-for-the-project"></a>Configurați un acord de furnizor pentru proiect

Configurați termenii de păstrare a furnizorilor care se aplică proiectului. Condițiile de retenție a furnizorului sunt, de asemenea, afișate pe comenzile de cumpărare pe care le creați pentru furnizor.

1. În Finanțe, accesați **Management de proiect și contabilitate** > **Proiecte** > **Toate proiectele**. 
2. Selectați un proiect și, în panoul de acțiuni, selectați **Grupul de proiect** > **Acorduri de vânzător**.
3. Pe pagina **Acorduri de vânzător**, adăugați o nouă linie.
4. În câmpul **Câmpul codului contului**, selectați una dintre următoarele opțiuni:
   - **Tabel**: Termenii de retenție a furnizorilor se aplică unui singur furnizor.
   - **Grup**: Termenii de retenție a furnizorilor se aplică tuturor furnizorilor dintr-un grup de furnizori.
   - **Toți**: Condiții de retenție a furnizorilor se aplică tuturor furnizorilor.
5. În câmpul **Câmpul Furnizor/Grupul de furnizori**, selectați furnizorul sau grupul de furnizori cărora li se aplică condițiile de retenție a furnizorilor. Dacă ați selectat  **Toți**  în pasul anterior, acest câmp nu este disponibil.
6. În câmpul **Condiții de păstrare a furnizorilor**, selectați ID-ul regulii pentru termenii de păstrare care trebuie aplicați acestui furnizor.
