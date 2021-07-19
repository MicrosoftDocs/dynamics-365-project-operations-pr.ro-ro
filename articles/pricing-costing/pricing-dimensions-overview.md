---
title: Prezentare generală a dimensiunilor de preț
description: Acest subiect oferă informații despre dimensiunile stabilirii prețurilor în Dynamics 365 Project Operations.
author: rumant
ms.date: 11/30/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: e8d62dcf9975e5427926210a881dec2c256f1b8b
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368491"
---
# <a name="pricing-dimensions-overview"></a>Prezentare generală a dimensiunilor de preț

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Dimensiunile care sunt utilizate în resursele umane pentru stabilirea prețurilor și a costurilor se încadrează în două categorii:

- Persoane
- Lucru programat

Din acest motiv, există două tipuri de valori de dimensiune de preț disponibile:

- **Seturi de opțiuni**: dimensiuni care sunt enumerări fixe pentru un set de valori.
- **Valori bazate pe entități**: dimensiuni care pot fi un set variat de valori.

## <a name="pricing-dimensions"></a>Dimensiuni de preț

Dynamics 365 Project Operations livrează cu un set implicit de dimensiuni de stabilire a prețurilor. Puteți vizualiza aceste dimensiuni de preț accesând **Operațiuni de preț** > **Parametri**. În înregistrarea parametru, pe fila **Dimensiuni de preț bazate pe volum**, verificați că rolul **, msdyn_resourcecategory** și unitatea organizațională de obținere a resurselor **msdyn_organizationalunit** au câmpurile **Aplicabile vânzărilor** și **Aplicabile costurilor** setate la **Da**. Când sunt activate aceste câmpuri, puteți configura prețul și costul pentru fiecare rol și combinație de unitate organizatorică.

![Captură de ecran a parametrilor Project Service cu „Aplicabil vânzărilor” evidențiat](media/PS-OOB-parameters.png)

Dacă aveți nevoie de preț sau cost pentru resurse utilizând atribute suplimentare, aveți posibilitatea să creați câmpuri, entități și dimensiuni particularizate. Pentru informații suplimentare, consultați următoarele subiecte. 
  
  > [!NOTE]
  > Procedurile trebuie finalizate în ordinea în care sunt listate.

1. [Crearea unei soluții pentru dimensiunile de tarifare particularizate](../sales/create-solution-custompd.md)
2. [Crearea câmpurilor și entităților particularizate](create-custom-fields-entities-pricing-dimensions.md)
3. [Adăugarea câmpurilor particularizate la configurarea prețurilor și la entitățile tranzacționale ](add-custom-fields-price-setup-transactional-entities.md)
4. [Configurarea câmpurilor particularizate ca dimensiuni de preț ](set-up-custom-fields-pricing-dimensions.md)
5. [Actualizați atributele inserturilor pentru a include noi dimensiuni de tarifare](update-plugin-attributes-pd.md)


## <a name="pricing-human-resource-time"></a>Preț timp resurse umane
Cum o organizație stabilește prețul timpul resurselor umane este adesea o considerație strategică importantă care afectează direct profitabilitatea organizației. Lucrați cu echipele de finanțe și cu șefii practicilor atunci când organizația este pregătită să identifice modul în care dorește să configureze ratele de factură și cost pentru timpul resurselor umane.

Alte considerente de stabilire a prețurilor includ dacă să reutilizați câmpuri sau entități care nu sunt în prezent dimensiuni de preț, dar se aplică ca o dimensiune de preț pentru organizația dvs. Câmpuri precum **Categoria de tranzacție** (**msdyn_transactioncategory**) și **Resursă care se poate rezerva** (**bookableresource**) sunt exemple de dimensiuni candidat. 

Luați în considerare dacă dimensiunea de preț ar trebui să fie un tabel sau un set de opțiuni. Dacă preconizați modificări ale valorilor unei dimensiuni care va depăși 10 sau 12 și aveți nevoie de atribute suplimentare pentru aceste valori, puteți crea o entitate mai degrabă decât un set de opțiuni. Menținerea unui set de opțiuni, cum ar fi adăugarea sau eliminarea valorilor, necesită un administrator sau un dezvoltator, în timp ce adăugarea de noi rânduri la un tabel se poate face de către majoritatea utilizatorilor.

Următorul exemplu arată ratele de facturare care sunt configurate pe baza rolului și unității de resurse organizaționale la care aparține resursa. Ratele de cost sunt de obicei bazate pe banda de salariu a angajatului și unitatea de organizație la care aparțin. În acest exemplu, rata de facturare și tabelele ratei de cost va arata în felul următor.

**Exemple de rate de facturare**

| Rol        | Unitate organizațională    |Unitate      |Preț      |Monedă  |
| ------------|-------------|----------|----------:|----------|
| Dezvoltator   | Contoso SUA  |Oră | 200|USD     |
| Dezvoltator   | Contoso India |Oră|   112|USD     |


**Eșantion de rate de cost**

| Bandă de salariu     | Unitate organizațională    |Unitate      |Preț      |Monedă  |
| ----------------|-------------|----------|----------:|----------|
| company_Band1 a mea | Contoso SUA  |Oră | 145|USD     |
| company_Band2 a mea | Contoso India |Oră|   67|USD     |


[!INCLUDE[footer-include](../includes/footer-banner.md)]