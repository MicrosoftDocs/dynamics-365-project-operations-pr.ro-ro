---
title: Migrați etapele de facturare complet facturate la trecere
description: Acest articol explică cum să migrați etapele de facturare cu preț fix care au fost facturate clientului pentru contractele de proiect deschise înainte de data lansării.
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
# <a name="migrate-fully-invoiced-billing-milestones-at-cutover"></a>Migrați etapele de facturare complet facturate la trecere

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

## <a name="scenario"></a>Scenariu

Contoso este disponibil cu Microsoft Dynamics 365 Project Operations pentru scenarii de resurse/neaprovizionate. Ca parte a activităților de transfer, echipa de implementare trebuie să migreze contractele de proiect deschise din vechiul sistem. Unele dintre contractele de proiect includ linii de contract care folosesc metoda de facturare la preț fix și au fost deja parțial facturate către clientul final. Echipa de implementare trebuie să migreze aceste etape de facturare ca **Factura client afisata**, deoarece acestea trebuie incluse în valoarea totală a contractului în scopul recunoașterii veniturilor. Cu toate acestea, soldurile clienților din Conturi de creanță și Cartea mare nu trebuie să fie afectate.

## <a name="solution"></a>Soluție

### <a name="prerequisites"></a>Cerințe preliminare

- Dynamics 365 Finance 10.0.24 sau o versiune ulterioară trebuie instalată.
- Mediul în care vor fi finalizați pașii de migrare trebuie să fie în modul de întreținere. Nu trebuie efectuate alte activități în timp ce etapele de referință sunt migrate.
- Pașii de migrare trebuie urmați exact așa cum este descris aici și pot fi utilizați numai pentru activitatea de trecere. Microsoft nu acceptă altă utilizare a acestei capabilități.

### <a name="create-a-cutover-version-of-the-project-operations-integration-contract-line-milestones-dual-write-map"></a>Creați o versiune de trecere a hărții cu dublă scriere a liniilor de referință a contractului de integrare a operațiunilor de proiect 

1. Asigurați-vă că maparea țintă pentru **Etape ale liniilor contractului de integrare a operațiunilor de proiect** entitatea este la zi. 

    1. În Finanțe, accesați **Management de date** \> **Entități de date**, și selectați **Etape ale liniilor contractului de integrare a operațiunilor de proiect** entitate. 
    2. Selectați **Modificați mapările țintei**. 
    3. Pe **Harta montaj la tinta** pagina, selectați **Generați cartografiere**, apoi confirmați că doriți să generați maparea.

2. Opriți și reîmprospătați **Etape ale liniilor contractului de integrare a operațiunilor de proiect** (**msdyn\_ contractlinesscheduleofvalues**) hartă cu dublă scriere. 

    1. Mergi la **Management de date** \> **Scriere dublă**, selectați harta și deschideți detaliile acesteia. 
    2. Selectați **Stop** și așteptați până când sistemul oprește harta. 
    3. Selectați **Reîmprospătați tabelele**.

3. Adăugați o mapare pentru starea tranzacției.

    1. Selectați **Adăugați mapare**.
    2. Pe noua linie, în **Aplicații de finanțare și operațiuni** coloana, selectați **TRANSSTATUS\[ TRANSSTATUS\]** camp.
    3. În **Microsoft Dataverse** coloană, selectați **msdyn\_ starea facturii\[ Starea facturii\]**.
    4. În **Tip hartă** coloana, selectați săgeata dreapta (**\>**).
    5. În caseta de dialog care apare, în **Direcția de sincronizare** câmp, selectați **Dataverse la aplicațiile Finanțe și Operațiuni**.
    6. Selectați **Adăugați transformare**.
    7. În **Tip de transformare** câmp, selectați **ValueMap**.
    8. Selectați **Maparea valorii adăugate**.
    9. În câmpul din stânga, introduceți **4**. În câmpul din dreapta, introduceți **192350001**. 
    10. Selectați **Salvați**, apoi închideți caseta de dialog.

4. Selectați **Salvează ca** pentru a salva versiunea hărții cu dublă scriere. 
5. În **Adăugați un tabel** panou, în **Editor** câmp, selectați **Editor prestabilit**.
6. În **Versiune** câmp, introduceți versiunea.
7. În **Descriere** câmp, introduceți o notă despre această versiune de tăiere a hărții. 
8. Selectați **Salvare**.
9. Începeți harta.

### <a name="migrate-invoiced-milestones-to-the-dataverse-environment"></a>Migrați reperele facturate la Dataverse mediu inconjurator

1. În Operațiunile de Proiect Dataverse mediu, creați etape care au un statut de factură de **Gata pentru facturare**. În acest moment, nu migrați nicio etapă care nu a fost facturată.

    > [!NOTE]
    > Înainte de a migra etapele de facturare, asigurați-vă că dimensiunile financiare care sunt legate de linia contractului de proiect sunt setate conform așteptărilor. Dimensiunile financiare nu pot fi modificate după finalizarea migrării.

2. După ce toate etapele de referință sunt migrate, opriți următoarele hărți cu scriere duală:

    - Etape ale liniilor de contract de integrare a operațiunilor de proiect (msdyn\_ contractlinesscheduleofvalues)
    - Actualități de integrare a Project Operations (msdyn\_actuale)
    - Propunere de facturi de proiect V2 (facturi)

    Pentru a opri hărțile, urmați acești pași:

    1. În Finanțe, accesați **Management de date** \> **Scriere dublă**, selectați o hartă și deschideți detaliile acesteia.
    2. Selectați **Stop** și așteptați până când sistemul oprește harta.

3. În Operațiunile de Proiect Dataverse mediu, creați și confirmați facturile pro-forma pentru etapele de facturare. 

    1. În harta site-ului, accesați contractele de proiect, selectați contractele, apoi selectați **Creați facturi**.
    2. După ce facturile sunt create, deschideți-le din **Facturi** meniul din harta site-ului, apoi selectați **A confirma**.

    Acest pas creează înregistrările necesare în Dataverse mediu inconjurator. Cu toate acestea, nu afectează situația financiară și conturile de încasat, deoarece hărțile cu dublă scriere listate anterior au fost oprite.

4. După ce toate facturile pro-forma sunt confirmate, readuceți toate hărțile cu dublă scriere la starea lor inițială.

    1. Actualizați versiunea **Etape ale liniilor contractului de integrare a operațiunilor de proiect** (**msdyn\_ contractlinesscheduleofvalues**) hartă cu dublă scriere înapoi la original. 
    2. Selectați harta cu scriere duală din lista de hărți, selectați **Versiunea hărții de tabel**, apoi selectați versiunea originală a hărții tabelului.
    3. Selectați **Salvare**.
    4. Reporniți următoarele hărți cu scriere duală:

        - Etape ale liniilor de contract de integrare a operațiunilor de proiect (msdyn\_ contractlinesscheduleofvalues)
        - Actualități de integrare a Project Operations (msdyn\_actuale)
        - Propunere de facturi de proiect V2 (facturi)

Etapele de referință sunt acum migrate, iar sistemul este pregătit pentru următorii pași în activitatea de trecere.
