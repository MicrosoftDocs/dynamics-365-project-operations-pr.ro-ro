---
title: Configurarea și utilizarea plăților de la furnizor cu plată la plată
description: Acest subiect explică cum să creați termeni de plată atunci când plătiți (PWP), astfel încât să puteți elibera plăți parțiale de la furnizor, pe baza plăților clienților.
author: RadhikaRS
manager: AnnBe
ms.date: 03/30/2020
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
ms.openlocfilehash: e872c4a2d35cef4cddc6851615c6c4d73b4e9d9a
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082775"
---
# <a name="set-up-and-use-pay-when-paid-vendor-payments"></a>Configurarea și utilizarea plăților de la furnizor cu plată la plată

[!include [banner](../includes/banner.md)]

Când aprobați un furnizor să lucreze ca subcontractant, este posibil să doriți să rețineți plata către furnizor până când clientul dvs. vă plătește pentru proiect. Pentru a susține acest scenariu, puteți configura termeni de plată la plată (PWP) atunci când configurați comanda de cumpărare (PO) cu furnizorul.

De exemplu, atunci când un client plătește o sumă pe o factură de proiect, puteți elibera o parte sau o parte din suma facturii furnizorului. Trebuie doar să configurați termeni PWP care specifică faptul că furnizorul va fi plătit după ce veți primi un procent din plata aferentă de la client. Dacă primiți o plată parțială de la un client, puteți elibera manual unele dintre facturile aferente furnizorului pentru plată.

Următorul exemplu prezintă procesul când sunt folosiți termenii PWP.

## <a name="example"></a>Exemplu

Organizația dvs. este de acord să ofere unui client 100 de computere care au software instalat, la un preț de 150,00 dolari SUA (USD) per computer. Apoi angajați un furnizor pentru a vă furniza computerele care au software instalat. Conform acordului, clientul trebuie să aprobe calitatea computerelor înainte ca acesta să plătească organizației dvs. Politica organizației dvs. este de a reține plata către furnizori până când clientul vă plătește. Prin urmare, configurați proiectul astfel încât acesta să aibă un procent PWP de 100%.

Furnizorul vă trimite cele 100 de computere care au software instalat, împreună cu o factură pentru 10.000,00 USD. Deoarece termenii PWP sunt stabiliți pentru proiectul dvs., nu plătiți furnizorul la primirea computerelor. În schimb, trimiteți computerele către client, împreună cu o factură pentru 15.000,00. Clientul inspectează computerele și aprobă suma totală a facturii proiectului.

După ce primiți plata integrală de la client, plătiți vânzătorului 10.000,00, suma integrală a facturii furnizorului.

## <a name="set-up-pwp-terms-for-a-project"></a>Configurați termenii PWP pentru un proiect

Când configurați condițiile PWP pentru un proiect, trebuie să specificați, în procente, suma minimă pe care un client trebuie să o plătească pentru proiect înainte de a plăti vânzătorului. Suma pragului este calculată automat pe facturile clienților pentru proiect. Urmați acești pași pentru a seta procentul de prag pentru termenii PWP.

1. Accesați **Gestionarea proiectului și contabilitate** \> **Proiecte** \> **Toate proiectele**.
2. Găsiți și deschideți proiectul pentru care doriți să configurați termenii PWP.
3. Pe **Acorduri de vânzător** FastTab, selectați **Adăugați linie**.
3. În câmpul **Câmpul codului contului** , selectați una dintre următoarele opțiuni:

    - **Tabel** - Termenii PWP se aplică unui singur furnizor.
    - **Grup** - Termenii PWP se aplică tuturor furnizorilor dintr-un grup de furnizori.
    - **Toți** - Condiții PWP se aplică tuturor furnizorilor.

4. Dacă ați selectat **Tabel** sau **Grup** în pasul anterior, în câmpul **Furnizor/Grup de furnizori** , selectați furnizorul sau grupul de furnizori căruia i se aplică termenii PWP. Dacă ați selectat **Toate** în pasul anterior, câmpul **Furnizor/Grup de furnizori** nu poate fi editat.
5. Dacă termenii de păstrare a furnizorului sunt stabiliți pentru furnizor în proiect, în câmpul **Condiții de păstrare a furnizorilor** , selectați ID-ul regulii pentru termenii de păstrare.
6. În câmpul **Procentul de prag PWP** , introduceți procentul de prag pentru proiect. Procentul pe care îl introduceți pentru proiect definește suma minimă pe care trebuie să o plătească clientul înainte de a plăti vânzătorului.

## <a name="create-a-po-that-has-pwp-terms"></a>Creați un PO care are termeni PWP

Când postați o factură de la un furnizor, dacă furnizorul este supus condițiilor PWP, acești termeni sunt afișați pe liniile PO. Pentru a crea un PO care are termeni PWP, urmați acești pași.

1. Accesați **Achiziții și aprovizionare** \> **Ordine de achiziție** \> **Toate comenzile de cumpărare**.
2. În panoul de acțiuni, selectați **Nou**. Apoi, în caseta de dialog **Creați comanda de cumpărare** , introduceți informațiile necesare și selectați **OK**.

    Alternativ, deschideți un PO existent pe pagina listei **Toate comenzile de cumpărare**.

4. Pe pagina **Comandă de achiziție** , pe **Linii de comandă de cumpărare** FastTab, consultați detaliile liniei PO pentru furnizor. Opțiunea **Plătește când este plătit** este selectată automat, iar valoarea din câmpul **Procentul de prag PWP** este copiată automat din câmpul **Procentul de prag PWP** pe pagina **Proiecte**.
6. Dacă nu doriți să aplicați termeni PWP la furnizor pentru o linie PO, ștergeți opțiunea **Plătește când este plătit**. În acest caz, câmpul **Procentul de prag PWP** pentru linia PO va fi resetat la 0 (zero).

## <a name="update-a-customer-payment-and-pay-the-vendor"></a>Actualizați o plată a clientului și plătiți furnizorul

Atunci când un furnizor își finalizează lucrările la un proiect și vă trimite o factură, trebuie să examinați starea proiectului și facturile clienților pentru a determina dacă au fost îndeplinite condițiile PWP pentru proiect. Dacă au fost îndeplinite condițiile PWP pentru furnizor, puteți stabili ce linii din factura furnizorului să plătiți, pe baza plăților clienților pentru proiect. Dacă decideți să plătiți vânzătorul, chiar dacă nu au fost îndepliniți condițiile PWP, puteți înlocui termenii PWP pe pagina **Factură furnizor cu plată la plată**.

1. Accesați **Management de proiect și contabilitate** \> **Cereri și rapoarte** \> **Anchete de păstrare** \> **Factură furnizor cu plată la plată**.
2. Pe pagina **Facturile furnizorului cu plată la plată** , în câmpul de căutare, introduceți valori pentru a găsi factura furnizorului pe care doriți să o examinați, apoi selectați **Căutare**.
3. Pe FastTab **Linii de facturare a furnizorului** , selectați liniile pe care doriți să le modificați.
4. Dacă condițiile **Plătește când este plătit** sunt îndeplinite pentru linia de facturare, selectați **Eliberați plata furnizorului**. Opțiunea **Plătește când este plătit** este ștearsă, iar valoarea câmpului **Gata pentru plată** este schimbată în **Da**.
