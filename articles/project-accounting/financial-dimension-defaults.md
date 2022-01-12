---
title: Valori implicite pentru dimensiunile financiare
description: Acest subiect oferă informații despre cum să configurați valorile implicite ale dimensiunii financiare.
author: sigitac
ms.date: 12/14/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 8c1eb71d13ca7fc59118d15fef7ac914577b3b0e
ms.sourcegitcommit: fe5610464fdb5be756aa6a6a5b3c9a991dea0ed8
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 12/15/2021
ms.locfileid: "7922953"
---
# <a name="financial-dimension-defaults"></a>Valori implicite pentru dimensiunile financiare

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dynamics 365 Project Operations utilizează cadrul [Dimensiuni financiare](/dynamics365/finance/general-ledger/financial-dimensions) în Dynamics 365 Finance pentru a furniza detalii suplimentare cu privire la tranzacțiile cu contabilitate de proiect și contabilitate generală.

Dimensiunile financiare implicite pot fi stabilite pentru un client, o sursă de finanțare a proiectului, o etapă importantă, o linie de contract de proiect sau un proiect.

## <a name="define-default-financial-dimensions-for-a-customer"></a>Definiți dimensiunile financiare implicite pentru un client

Valorile implicite ale dimensiunii clienților sunt specificate în Finanțe. Completați următorii pași pentru a seta valorile implicite ale dimensiunii.

1. Accesați **Conturi clienți** > **Clienți** > **Toți clienții**.
2. Pe pagina **Clienți**, pe fila **Dimensiuni financiare**, setați valorile dimensiunii financiare pentru un anumit client.

## <a name="define-default-financial-dimensions-for-project-contracts"></a>Definiți dimensiunile financiare implicite pentru contracte de proiect

Contractele de proiect sunt create și menținute în Common Data Service (CDS). Atributele contabile pentru contractele de proiect sunt stabilite în module **Management de proiect și contabilitate** în Finanțe.

### <a name="set-financial-dimensions-for-a-project-funding-source"></a>Stabiliți dimensiunile financiare pentru o sursă de finanțare a proiectului

1. Accesați **Gestionarea proiectului și contabilitate** > **Proiecte** > **Contracte de proiect**.
2. Selectați înregistrarea pe care doriți să o actualizați și pe fila **Contract de proiect**, selectați **Afișați contabilitatea implicită**.
3. Extindeți **Informații conexe** și selectați fila **Surse de finanțare**.
4. Setați valorile implicite ale dimensiunii financiare. Observați că dimensiunile financiare sunt implicite din contul clientului.

### <a name="set-financial-dimensions-for-a-project-contract-line"></a>Stabiliți dimensiunile financiare pentru o linie de contract de proiect

1. Accesați **Gestionarea proiectului și contabilitate** > **Proiecte** > **Contracte de proiect**.
2. Selectați înregistrarea pe care doriți să o actualizați și pe fila **Contract de proiect**, selectați **Afișați contabilitatea implicită**.
3. Extindeți **Informații conexe** și selectați fila **Linii de contract**.
4. Setați valorile implicite ale dimensiunii financiare. Valorile implicite ale dimensiunii financiare sunt aplicabile și pot fi utilizate numai cu liniile contractuale cu preț fix (etapă de referință).

Aceste valori implicite sunt utilizate pentru tranzacțiile aferente proiectului și liniile de facturare aferente.

## <a name="define-default-financial-dimensions-for-projects"></a>Definiți dimensiunile financiare implicite pentru proiecte

Proiectele sunt create și menținute în CDS. Atributele contabile pentru proiectele sunt stabilite în module **Management de proiect și contabilitate** în Finanțe.

1. Accesați **Managementul proiectelor și contabilitate** > **Proiecte** > **Toate proiectele**.
2. Selectați înregistrarea pe care doriți să o actualizați și pe fila **Proiect**, selectați **Afișați contabilitatea implicită**.
3. Extindeți **Informații conexe** și selectați fila **Configurare**.
4. Setați valorile implicite ale dimensiunii financiare. Observați că dimensiunile financiare sunt implicite din contul clientului. În cazul în care proiectul este asociat cu o linie contractuală cu mai mulți clienți contractuali ai proiectului, clientul principal este utilizat la dimensiunile financiare implicite.

Dimensiunile financiare implicite ale proiectului sunt utilizate pentru a seta valorile implicite ale liniei jurnalului pentru tranzacțiile de timp, cheltuială și taxă din **Jurnal de integrare a operațiunilor de proiect** și pe liniile de facturare aferente proiectului.

## <a name="apply-financial-dimensions-for-project-time-entries"></a>Aplicați dimensiuni financiare pentru înregistrările de timp ale proiectului
Pentru a aplica dimensiuni financiare pentru intrările de timp ale proiectului, rețineți că valoarea implicită a dimensiunii se bazează pe următoarea ordine:

1. Resursă
2. Project
3. Sursă de finanțare

De exemplu, dacă dimensiunea implicită este specificată pe o resursă, aceasta va fi aplicată peste o dimensiune implicită care este specificată în proiect. În mod similar, o dimensiune implicită de proiect va fi aplicată peste valoarea implicită care este specificată în sursa de finanțare.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
