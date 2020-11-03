---
title: Prezentare generală a dimensiunilor de preț
description: Acest subiect furnizează informații despre dimensiunile de preț în Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 6b1ebdc97ec4704ba256acb521c0f2e7c474940b
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082903"
---
# <a name="pricing-dimensions-overview"></a>Prezentare generală a dimensiunilor de preț

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Dimensiunile care sunt utilizate în resursele umane pentru stabilirea prețurilor și a costurilor se încadrează în două categorii:

- Persoane
- Lucru programat

Din acest motiv, există două tipuri de valori de dimensiune de preț disponibile:

- **Seturi de opțiuni** : dimensiuni care sunt enumerări fixe pentru un set de valori.
- **Valori bazate pe entități** : dimensiuni care pot fi un set variat de valori.

## <a name="pricing-dimensions"></a>Dimensiuni de preț

Project Operations Dynamics 365 sunt livrate cu un set implicit de dimensiuni de preț. Puteți vizualiza aceste dimensiuni de preț accesând **Operațiuni de preț** > **Parametri**. În înregistrarea parametru, pe fila **Dimensiuni de preț bazate pe volum** , verificați că rolul **, msdyn_resourcecategory** și unitatea organizațională de obținere a resurselor **msdyn_organizationalunit** au câmpurile **Aplicabile vânzărilor** și **Aplicabile costurilor** setate la **Da**. Când sunt activate aceste câmpuri, puteți configura prețul și costul pentru fiecare rol și combinație de unitate organizatorică.

Dacă aveți nevoie de preț sau cost pentru resurse utilizând atribute suplimentare, aveți posibilitatea să creați câmpuri, entități și dimensiuni particularizate.

## <a name="pricing-human-resource-time"></a>Preț timp resurse umane
Cum o organizație stabilește prețul timpul resurselor umane este adesea o considerație strategică importantă care afectează direct profitabilitatea organizației. Lucrați cu echipele de finanțe și cu șefii practicilor atunci când organizația este pregătită să identifice modul în care dorește să configureze ratele de factură și cost pentru timpul resurselor umane.

Alte considerente de stabilire a prețurilor includ dacă să reutilizați câmpuri sau entități care nu sunt în prezent dimensiuni de preț, dar se aplică ca o dimensiune de preț pentru organizația dvs. Câmpuri precum **Categoria de tranzacție** ( **msdyn_transactioncategory** ) și **Resursă care se poate rezerva** ( **bookableresource** ) sunt exemple de dimensiuni candidat. 

Luați în considerare dacă dimensiunea de preț ar trebui să fie un tabel sau un set de opțiuni. Dacă preconizați modificări ale valorilor unei dimensiuni care va depăși 10 sau 12 și aveți nevoie de atribute suplimentare pentru aceste valori, puteți crea o entitate mai degrabă decât un set de opțiuni. Menținerea unui set de opțiuni, cum ar fi adăugarea sau eliminarea valorilor, necesită un administrator sau un dezvoltator, în timp ce adăugarea de noi rânduri la un tabel se poate face de către majoritatea utilizatorilor.

Următorul exemplu arată ratele de facturare care sunt configurate pe baza rolului și unității de resurse organizaționale la care aparține resursa. Ratele de cost sunt de obicei bazate pe banda de salariu a angajatului și unitatea de organizație la care aparțin. În acest exemplu, rata de facturare și tabelele ratei de cost va arata în felul următor.

**Exemple de rate de facturare**

| Rol        | Unitate organizațională    |Unitate      |Preț      |Monedă  |
| ------------|-------------|----------|----------:|----------|
| Dezvoltator   | Contoso US  |Hour | 200|USD     |
| Dezvoltator   | Contoso India |Hour|   112|USD     |


**Eșantion de rate de cost**

| Bandă de salariu     | Unitate organizațională    |Unitate      |Preț      |Monedă  |
| ----------------|-------------|----------|----------:|----------|
| company_Band1 a mea | Contoso US  |Hour | 145|USD     |
| company_Band2 a mea | Contoso India |Hour|   67|USD     |
