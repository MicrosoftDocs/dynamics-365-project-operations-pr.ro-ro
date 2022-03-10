---
title: Configurarea categoriilor de proiecte
description: Acest subiect furnizează informații despre configurarea categoriilor de proiect.
author: sigitac
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: cea43422469adf12f336f7686814a8199717090c18804d3d0a7509452349566e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/06/2021
ms.locfileid: "6997126"
---
# <a name="configure-project-categories"></a>Configurarea categoriilor de proiecte

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

Operațiunile de proiect oferă capabilități solide pentru clasificarea veniturilor și cheltuielilor pe proiecte. Categoriile oferă posibilitatea de a raporta și analiza tranzacțiile proiectului și de a conduce postarea în registrul general.

Următoarea diagramă ilustrează corelația dintre categoriile de tranzacții, categoriile partajate și categoriile de proiecte. 

Categoriile de tranzacții sunt gruparea de bază pentru tranzacțiile proiectului. În cadrul grupării respective, există un set de categorii partajate care pot fi partajate între aplicații și module. Intrând și mai în detaliu, categoriile de proiecte sunt cel mai granular nivel de categorii. Categoriile de proiecte sunt specifice entității juridice, modulului și aplicației.

![Corelația dintre categoriile de tranzacții, categoriile partajate și categoriile de proiecte.](media/project-categories.png)

## <a name="transaction-categories"></a>Categorii de tranzacții

Categoriile de tranzacții reprezintă gruparea de bază pentru tranzacțiile proiectului și nu sunt specifice companiei sau tipului de tranzacție. De exemplu, Contoso Robotics utilizează categoriile de proiectare, călătorie, instalare și tranzacții de servicii pentru a grupa tranzacțiile proiectului.

Categoriile de tranzacții sunt definite în modulul Project Operations. 
1. Accesați **Setări** \> **Categorii de tranzacții** pentru a deschide formularul. 
2. Creați o nouă categorie de tranzacții fie selectând **Nou** sau selectând **Importați din Excel**.

## <a name="shared-categories"></a>Categorii partajate

Dynamics 365 folosește conceptul de categorii partajate pentru a clasifica cheltuielile în diferite aplicații, cum ar fi Dynamics 365 Finance, Dynamics 365 Supply Chain și Dynamics 365 Project Operations. Pentru fiecare categorie de tranzacții creată, Project Operationst creează automat patru categorii comune partajate: Ore, Cheltuieli, Taxe și Articol. Puteți examina și ajusta categoriile partajate accesând **Management de proiect și contabilitate** \> **Configurare** \> **Categorii** \> **Categorii partajate**.

## <a name="project-categories"></a>Categorii de proiecte

Categoriile de proiecte reprezintă cel mai granular nivel de configurare a categoriilor și trebuie configurate separat și pentru fiecare companie, de către un contabil de proiect.

1. Accesați **Management de proiect și contabilitate** \> **Configurare** \> **Categorii** \> **Categorii de proiecte**.
2. Selectați **Nou**.
3. Selectați **ID categorie** din categoria partajat pe care ați creat-o în secțiunea anterioară. Project Operations permit utilizarea numai a acelor categorii partajate care sunt asociate cu categoriile de tranzacții.
4. Selectați un grup de categorii.

## <a name="category-groups"></a>Grupuri de categorie

Grupurile de categorii sunt folosite pentru a partaja proprietăți, în principal postarea profilurilor, între categoriile de proiecte conexe. Trebuie să existe cel puțin un grup de categorii pentru fiecare tip de tranzacție și fiecărei categorii de proiect i se atribuie un grup.

Specificațiile de înregistrare din Project Operations sunt definite de regulile profilului de cost și de venit al proiectului, categoriile de proiecte și grupurile de categorii. Puteți configura grupuri de categorii accesând **Management de proiect și contabilitate** \> **Configurare** \> **Categorii** \> **Grupuri de categorii**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]