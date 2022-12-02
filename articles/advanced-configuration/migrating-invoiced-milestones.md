---
title: Migrarea jaloanelor de facturare complet facturate la transfer
description: Acest articol explică cum să migrați jaloanele de facturare cu preț fix care au fost facturate clientului pentru contractele de proiect deschise înainte de data lansării.
author: sigitac
ms.date: 01/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 05cd71f9860b5698e3a26bc72660b0b2044206c8
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028717"
---
# <a name="migrate-fully-invoiced-billing-milestones-at-cutover"></a>Migrarea jaloanelor de facturare complet facturate la transfer

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

## <a name="scenario"></a>Scenariu

Contoso este disponibil cu Microsoft Dynamics 365 Project Operations pentru scenarii de resurse/neaprovizionate. Ca parte a activităților de transfer, echipa de implementare trebuie să migreze contractele de proiect deschise din vechiul sistem. Unele dintre contractele de proiect includ linii de contract care folosesc metoda de facturare la preț fix și au fost deja parțial facturate către clientul final. Echipa de implementare trebuie să migreze aceste etape de facturare ca **Factură client afișată**, deoarece acestea trebuie incluse în valoarea totală a contractului în scopul recunoașterii veniturilor. Cu toate acestea, soldurile clienților din Conturi creanțe și Contabilitate nu trebuie să fie afectate.

## <a name="solution"></a>Soluție

### <a name="prerequisites"></a>Cerințe preliminare

- Trebuie instalat Dynamics 365 Finance 10.0.24 sau o versiune ulterioară.
- Mediul în care vor fi finalizați pașii de migrare trebuie să fie în modul de întreținere. Nu trebuie efectuate alte activități în timp ce jaloanele sunt migrate.
- Pașii de migrare trebuie urmați exact așa cum este descris aici și pot fi utilizați numai pentru activitatea de transfer. Microsoft nu acceptă altă utilizare a acestei capabilități.

### <a name="create-a-cutover-version-of-the-project-operations-integration-contract-line-milestones-dual-write-map"></a>Creați o versiune de transfer a hărții cu scriere duală a jaloanelor pentru linia de contract de integrare a Project Operations 

1. Asigurați-vă că maparea țintă pentru entitatea **Jaloane pentru linia de contract de integrare a Project Operations** este la zi. 

    1. În Finanțe, accesați **Management de date** \> **Entități de date** și selectați entitatea **Jaloane pentru linia de contract de integrare a Project Operations**. 
    2. Selectați **Modificați mapările țintă**. 
    3. Pe pagina **Montare hartă la țintă**, selectați **Generați mapare**, apoi confirmați că doriți să generați maparea.

2. Opriți și reîmprospătați harta cu scriere duală **Jaloane pentru linia de contract de integrare a Project Operations** (**msdyn\_contractlinescheduleofvalues**). 

    1. Accesați **Management de date** \> **Scriere duală**, selectați harta și deschideți detaliile acesteia. 
    2. Selectați **Stop** și așteptați până când sistemul oprește harta. 
    3. Selectați **Reîmprospătare tabele**.

3. Adăugați o mapare pentru starea tranzacției.

    1. Selectați **Adăugare mapare**.
    2. Pe noua linie, în coloana **Aplicații finanțe și operațiuni**, selectați câmpul **TRANSSTATUS \[TRANSSTATUS\]**.
    3. În coloana **Microsoft Dataverse**, selectați **msdyn\_starea facturii \[Starea facturii\]**.
    4. În coloana **Tip hartă**, selectați săgeata dreapta (**\>**).
    5. În caseta de dialog care apare, în câmpul **Direcția de sincronizare**, selectați **Dataverse la Aplicații Finanțe și Operațiuni**.
    6. Selectați **Adăugare transformare**.
    7. În câmpul **Tip transformare**, selectați **ValueMap**.
    8. Selectați **Adăugare mapare valoare**.
    9. În câmpul din stânga, introduceți **4**. În câmpul din dreapta, introduceți **192350001**. 
    10. Selectați **Salvare** și apoi închideți caseta de dialog.

4. Selectați **Salvare ca** pentru a salva versiunea hărții cu scriere duală. 
5. În panoul **Adăugare tabel**, în câmpul **Editor**, selectați **Editor implicit**.
6. În câmpul **Versiune**, introduceți versiunea.
7. În câmpul **Descriere**, introduceți o notă despre această versiune de transfer a hărții. 
8. Selectați **Salvare**.
9. Porniți harta.

### <a name="migrate-invoiced-milestones-to-the-dataverse-environment"></a>Migrați jaloanele facturate la mediul Dataverse

1. În mediul Project Operations Dataverse, creați jaloane care au un statut de facturare de **Gata pentru facturare**. În acest moment, nu migrați niciun jalon care nu a fost facturat.

    > [!NOTE]
    > Înainte de a migra jaloanele de facturare, asigurați-vă că dimensiunile financiare care sunt legate de linia de contract de proiect sunt setate conform așteptărilor. Dimensiunile financiare nu pot fi editate după finalizarea migrării.

2. După ce toate jaloanele sunt migrate, opriți următoarele hărți cu scriere duală:

    - Jaloane pentru linia de contract de integrarea Project Operations (msdyn\_contractlinescheduleofvalues)
    - Actualități de integrare a Project Operations (msdyn\_actuale)
    - Propunere de facturi de proiect V2 (facturi)

    Pentru a opri hărțile, urmați acești pași:

    1. În Finanțe, accesați **Management de date** \> **Scriere duală**, selectați o hartă și deschideți detaliile acesteia.
    2. Selectați **Stop** și așteptați până când sistemul oprește harta.

3. În mediul Project Operations Dataverse, creați și confirmați facturile pro-formă pentru jaloanele de facturare. 

    1. În harta site-ului, accesați contractele de proiect, selectați contractele și apoi selectați **Creați facturi**.
    2. După ce facturile sunt create, deschideți-le din meniul **Facturi** din harta site-ului și apoi selectați **Confirmare**.

    Acest pas creează înregistrările necesare în mediul Dataverse. Cu toate acestea, nu afectează finanțele și conturile creanțe, deoarece hărțile cu scriere duală listate anterior au fost oprite.

4. După ce toate facturile pro-formă sunt confirmate, readuceți toate hărțile cu scriere duală la starea lor inițială.

    1. Actualizați versiunea hărții cu scriere duală **Jaloane pentru linia de contract de integrare a Project Operations** (**msdyn\_contractlinescheduleofvalues**) înapoi la cea originală. 
    2. Selectați harta cu scriere duală din lista de hărți, selectați **Versiunea hărții de tabel**, apoi selectați versiunea originală a hărții tabelului.
    3. Selectați **Salvare**.
    4. Reporniți următoarele hărți cu scriere duală:

        - Jaloane pentru linia de contract de integrarea Project Operations (msdyn\_contractlinescheduleofvalues)
        - Actualități de integrare a Project Operations (msdyn\_actuale)
        - Propunere de facturi de proiect V2 (facturi)

Jaloanele sunt acum migrate, iar sistemul este pregătit pentru următorii pași în activitatea de transfer.
