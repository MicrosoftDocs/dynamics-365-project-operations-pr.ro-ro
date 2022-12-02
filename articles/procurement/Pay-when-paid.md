---
title: Plățile de la furnizor cu plată la plată
description: Acest subiect explică cum să utilizați scenariul cu plata la plată (PWP).
author: mukumarm
ms.date: 08/18/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: mukumarm
ms.openlocfilehash: d1fe8d92663b31b22dc405fc1f3e06d976e6c5dc
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 09/16/2022
ms.locfileid: "9525390"
---
# <a name="pay-when-paid-vendor-payments"></a>Plățile de la furnizor cu plată la plată

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

Acest subiect explică cum să utilizați scenariul cu plata la plată (PWP).

## <a name="create-a-purchase-order-that-has-pwp-terms"></a>Creați o comandă de achiziție care are termeni PWP

Când publicați o factură de la un furnizor, dacă furnizorul este supus condițiilor PWP, acești termeni sunt afișați pe liniile de comandă de cumpărare (PO). Pentru a crea un PO care are termeni PWP, urmați acești pași.

1. În Microsoft Dynamics 365 Finance, urmați cel puțin unul dintre următorii pași:

    - Accesați **Achiziții și aprovizionare** \> **Ordine de achiziție** \> **Toate comenzile de cumpărare**. În panoul de acțiuni, selectați **Nou**. În caseta de dialog **Creare comandă de cumpărare**, selectați furnizorul pentru care sunt configurați termenii PWP în proiect, introduceți alte informații necesare, apoi selectați **O.K**.
    - Accesați **Gestionarea proiectului și contabilitate** \> **Proiecte** \> **Toate proiectele**. În Panoul de acțiuni, pe fila **Gestionați**, selectați **Sarcină articol**. Selectați comanda de cumpărare. Selectați furnizorul pentru care sunt configurați termenii PWP în proiect, apoi selectați **O.K**.

2. Pe pagina **Comandă de cumpărare**, pe fila rapidă **Linii de comandă de cumpărare**, selectați **Adăugare linie** pentru a crea o linie de comandă de cumpărare.
3. Selectați numărul articolului sau categoria de achiziție și introduceți celelalte detalii necesare. Revizuiți detaliile liniei PO pentru furnizor.

    Opțiunea **Plătește când este plătit** este selectată automat, iar valoarea din câmpul **Procentul de prag PWP** este copiată automat din câmpul **Procentul de prag PWP** pe pagina **Proiecte**.

4. Dacă nu doriți să aplicați termeni PWP la furnizor pentru o linie PO, ștergeți opțiunea **Plătește când este plătit**. În acest caz, câmpul **Pragul procentual PWP** pentru linia PO va fi resetat la **0** (zero).
5. Pe pagina **Comandă de cumpărare**, în Panoul de acțiuni, pe fila **Achiziție**, selectați **Confirmare** pentru a confirma comanda de cumpărare.
6. În Panoul de acțiuni, pe fila **Factură**, selectați **Factură** pentru a genera factura pentru comanda de cumpărare.

## <a name="create-a-project-invoice-proposal"></a>Creați o propunere de facturare pentru proiect

Propunerile de facturi de proiect sunt folosite pentru a crea facturi de proiect pentru client. În scenariul PWP, plățile furnizorilor depind de plățile clienților, conform setărilor PWP. Cu toate acestea, există opțiuni care vă permit să eliberați plățile fără plățile clienților, după cum doriți. Pentru a crea o factură de proiect pentru client, urmați acești pași.

1. În aplicațiile de implicare a clienților, accesați **Proiect** \> **Proiecte** și selectați proiectul.
2. Pe fila **Valori reale**, selectați linia reală care este generată de PO care are tipul de tranzacție **Vânzări nefacturate**. Apoi, selectați **Gata de facturare**.
3. Accesați **Vânzări** \> **Vânzări** \> **Contract de proiect** și selectați contractul de proiect.
4. Pe Panoul de acțiuni, selectați **Factură** pentru a genera factura personalizată.
5. În Finanțe, accesați **Management de proiect și contabilitate** \> **Periodic** \> **Importați din tabelul de etapizare** și selectați **O.K.** pentru a genera Jurnalul de integrare Project Operations.
6. Accesați **Management de proiect și contabilitate** \> **Facturi de proiect** \> **Propunere de factură de proiect** și selectați **Publicare** pentru a publica propunerea de factură care a fost generată pentru proiect.

## <a name="update-a-customer-payment-and-pay-the-vendor"></a>Actualizați o plată a clientului și plătiți furnizorul

Atunci când un furnizor își finalizează lucrările la un proiect și vă trimite o factură, trebuie să revizuiți starea proiectului și facturile clienților pentru a determina dacă au fost îndeplinite condițiile PWP pentru proiect. Dacă au fost îndeplinite condițiile PWP pentru furnizor, puteți stabili ce linii din factura furnizorului să plătiți, pe baza plăților clienților pentru proiect. Dacă decideți să plătiți vânzătorul, chiar dacă nu au fost îndepliniți condițiile PWP, puteți înlocui termenii PWP pe pagina **Factură furnizor cu plată la plată**.

1. În Finanțe, accesați **Management de proiect și contabilitate** \> **Proiecte** \> **Toate proiectele** și selectați proiectul.
2. În Panoul de acțiuni, selectați **Control**, apoi selectați **Facturi de furnizor** pentru a afișa toate facturile furnizorilor care au fost generate pentru proiect.
3. Pe pagina **Facturile furnizorului cu plată la plată**, în câmpul de căutare, introduceți valori pentru a găsi factura furnizorului pe care doriți să o examinați, apoi selectați **Căutare**.
4. Selectați opțiunea **Plată la plată** pentru a vizualiza numai facturile PWP.
5. Pe fila rapidă **Linii de factură de furnizor**, selectați liniile pe care doriți să le eliberați pentru plată.
6. Selectați **Eliberare plată furnizor**. Opțiunea **Plătește când este plătit** este ștearsă, iar valoarea câmpului **Gata pentru plată** este schimbată în **Da**.
