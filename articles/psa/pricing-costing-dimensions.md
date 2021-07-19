---
title: Pagină principală prețuri și dimensiuni de cost
description: Acest subiect oferă o prezentare generală a dimensiunilor prețurilor.
author: rumant
ms.custom:
- dyn365-projectservice
- intro-internal
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 5c8c28839f5e7b3259afbea4ab400d0c4fca95fd
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368896"
---
# <a name="pricing-and-costing-dimensions-home-page"></a>Pagină principală prețuri și dimensiuni de cost

[!include [banner](../includes/psa-now-project-operations.md)]

Dimensiunile utilizate pentru stabilirea prețurilor și costurilor forței de muncă în organizațiile bazate pe proiecte sunt influențate de următoarele atribute:

- Oamenii care fac o muncă similară cu experiența, rolul sau geografia lor
- Lucrarea care trebuie efectuată similară cu complexitatea sau ora din zi

Având în vedere natura tipică a acestor atribute de lucru și persoanele necesare pentru a efectua lucrarea, există două tipuri de valori ale dimensiunii prețurilor disponibile în Project Service Automation: 

- **Seturi de opțiuni** - atribute care sunt enumerări fixe pentru un set de valori.
- **Valori bazate pe entități** - Atribute care pot avea un set variat de valori care sunt finite, dar se pot schimba în timp.

## <a name="pricing-dimensions"></a>Dimensiuni de preț

PSA livrează cu un set implicit de dimensiuni de stabilire a prețurilor. Le puteți vizualiza accesând **Project Service** > **Parametri**. În înregistrarea parametru, pe fila **Dimensiuni de preț bazate pe volum**, verificați că rolul **, msdyn_resourcecategory** și unitatea organizațională de obținere a resurselor **msdyn_organizationalunit** au câmpurile **Aplicabile vânzărilor** și **Aplicabile costurilor** setate la **Da**. Acest lucru vă va permite să configurați prețul și costul pentru fiecare rol și combinație de unitate organizatorică.

![Captură de ecran a parametrilor Project Service cu „Aplicabil vânzărilor” evidențiat](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> Dacă ați utilizat câmpurile predefinite de unitate de rol și organizaționale ca dimensiuni ale prețurilor la versiunea 3 a PSA, nu va exista nicio modificare observabilă. Puteți continua să utilizați Project Service ca de obicei. 

Dacă aveți nevoie de preț sau cost pentru resurse utilizând atribute suplimentare, aveți posibilitatea să creați câmpuri, entități și dimensiuni particularizate. Pentru mai multe informații, consultați următoarele subiecte, însă rețineți că trebuie să finalizați procedurile în ordinea de mai jos:

- [Crearea câmpurilor și entităților particularizate](create-custom-fields-entities.md)
- [Adăugarea câmpurilor particularizate la parametrizarea prețurilor și la entitățile tranzacționale](field-references.md)
- [Configurarea câmpurilor particularizate ca dimensiuni de preț ](set-up-pricing-dimensions.md)
- [Actualizați atributele inserturilor pentru a include noi dimensiuni de tarifare](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a>Preț timp resurse umane
Cum o organizație stabilește prețul timpul resurselor umane este adesea o considerație strategică importantă care afectează direct profitabilitatea organizației. Lucrați cu echipele de finanțe și cu șefii practicilor atunci când organizația este pregătită să identifice modul în care dorește să configureze ratele de factură și cost pentru timpul resurselor umane.

Alte considerente de stabilire a prețurilor includ dacă să reutilizați câmpuri sau entități care nu sunt în prezent dimensiuni de preț, dar se aplică ca o dimensiune de preț pentru organizația dvs. Câmpuri precum **Categoria de tranzacție** (**msdyn_transactioncategory**) și **Resursă care se poate rezerva** (**bookableresource**) sunt exemple de dimensiuni candidat. 

Luați în considerare dacă dimensiunea de preț ar trebui să fie un tabel sau un set de opțiuni. Dacă preconizați modificări ale valorilor unei dimensiuni care va depăși 10 sau 12 și aveți nevoie de atribute suplimentare pentru aceste valori, ați putea crea o entitate mai degrabă decât un set de opțiuni. Menținerea unui set de opțiuni, cum ar fi adăugarea sau eliminarea valorilor, necesită un administrator sau un dezvoltator, în timp ce adăugarea de noi rânduri la un tabel se poate face de către majoritatea utilizatorilor de business.

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