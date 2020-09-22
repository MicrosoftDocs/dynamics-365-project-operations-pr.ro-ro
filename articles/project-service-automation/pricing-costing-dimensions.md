---
title: Pagină principală prețuri și dimensiuni de cost
description: Acest subiect oferă o prezentare generală a dimensiunilor prețurilor.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 425d7bb8-9015-4f67-b9c9-cf3602e9afe8
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 2379d0d2e038f28a1a8df87a851e9bf7db7fe33f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754727"
---
# <a name="pricing-and-costing-dimensions-home-page"></a>Pagină principală prețuri și dimensiuni de cost

Dimensiunile care sunt utilizate în resursele umane pentru stabilirea prețurilor și a costurilor se încadrează în două categorii:

- Persoane
- Lucru programat

Din acest motiv, există două tipuri de valori de dimensiune de preț disponibile în Project Service Automation (PSA): 

- **Seturi de opțiuni**- dimensiuni care sunt enumerări fixe pentru un set de valori.
- **Valori bazate pe entități** - dimensiuni care pot fi un set variat de valori.

## <a name="pricing-dimensions"></a>Dimensiuni de preț

PSA livrează cu un set implicit de dimensiuni de stabilire a prețurilor. Le puteți vizualiza accesând **Project Service** > **Parametri**. În înregistrarea parametru, pe fila **Dimensiuni de preț bazate pe volum**, verificați că rolul **, msdyn_resourcecategory** și unitatea organizațională de obținere a resurselor **msdyn_organizationalunit** au câmpurile **Aplicabile vânzărilor** și **Aplicabile costurilor** setate la **Da**. Acest lucru vă va permite să configurați prețul și costul pentru fiecare rol și combinație de unitate organizatorică.

![Captură de ecran a parametrilor Project Service cu „Aplicabil vânzărilor” evidențiat](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> Dacă ați utilizat câmpurile predefinite de unitate de rol și organizaționale ca dimensiuni ale prețurilor la versiunea 3 a PSA, nu va exista nicio modificare observabilă. Puteți continua să utilizați Project Service ca de obicei. 

Dacă aveți nevoie de preț sau cost pentru resurse utilizând atribute suplimentare, aveți posibilitatea să creați câmpuri, entități și dimensiuni particularizate. Pentru mai multe informații, consultați următoarele subiecte, însă rețineți că trebuie să finalizați procedurile în ordinea de mai jos:

- [Crearea câmpurilor și entităților particularizate](create-custom-fields-entities.md)
- [Adăugarea câmpurilor particularizate la parametrizarea prețurilor și la entitățile tranzacționale](field-references.md)
- [Configurare câmpuri particularizate ca dimensiuni de tarifare](set-up-pricing-dimensions.md)
- [Actualizați atributele inserturilor pentru a include noi dimensiuni de tarifare](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a>Preț timp resurse umane
Cum o organizație stabilește prețul timpul resurselor umane este adesea o considerație strategică importantă care afectează direct profitabilitatea organizației. Lucrați cu echipele de finanțe și cu șefii practicilor atunci când organizația este pregătită să identifice modul în care dorește să configureze ratele de factură și cost pentru timpul resurselor umane.

Alte considerente de stabilire a prețurilor includ dacă să reutilizați câmpuri sau entități care nu sunt în prezent dimensiuni de preț, dar se aplică ca o dimensiune de preț pentru organizația dvs. Câmpuri precum **Categoria de tranzacție** (**msdyn_transactioncategory**) și **Resursă care se poate rezerva** (**bookableresource**) sunt exemple de dimensiuni candidat. 

De asemenea, ar trebui să luați în considerare dacă dimensiunea de preț ar trebui să fie un tabel sau un set de opțiuni. Dacă preconizați modificări ale valorilor unei dimensiuni care va depăși 10 sau 12 și aveți nevoie de atribute suplimentare pentru aceste valori, puteți crea o entitate mai degrabă decât un set de opțiuni. Menținerea unui set de opțiuni, cum ar fi adăugarea sau eliminarea valorilor, necesită un administrator sau un dezvoltator, în timp ce adăugarea de noi rânduri la un tabel se poate face de către majoritatea utilizatorilor.

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
