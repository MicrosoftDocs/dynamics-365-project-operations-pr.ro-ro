---
title: Configurarea integrării Project Operations per entitate juridică
description: Acest subiect furnizează informații despre configurarea integrării după entitatea juridică în Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/21/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: c0e02ef2d17bf49209369f7adad681d9a5981e2a
ms.sourcegitcommit: 91ad491e94a421f256a378b0f4b26ed48c67bc93
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/22/2020
ms.locfileid: "4096767"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a>Configurarea integrării Project Operations per entitate juridică 

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

Acest subiect vă prezintă pașii necesari pentru configurarea Dynamics 365 Project Operations pe entitate juridică.

## <a name="enable-feature-keys-in-dynamics-365-finance"></a>Activați tastele de caracteristică în Dynamics 365 Finance

Parcurgeți pașii următori pentru a activa funcțiile necesare.

1. În Dynamics 365 Finance, accesați spațiul de lucru **Gestionarea caracteristicilor**.
2. În **Listă de caracteristici** , găsiți și activați următoarele caracteristici:
  
    - **Activați mai multe linii contractuale pentru un proiect**
    - **Activați Project Operations pe Dynamics 365 Customer Engagement**

> [!NOTE]
> Dacă nu vedeți **Taste funcționale** afișat, verificați dacă versiunea dvs. de finanțare îndeplinește cerința de versiune minimă (versiunea aplicației 10.0.13 cu toate actualizările de calitate aplicate sau mai mare). Selectați **Verifică pentru actualizări** pentru a reîmprospăta lista de funcții.

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a>Definiți scenariul de implementare a Project Operations pentru o entitate juridică

Puteți activa Project Operations pe Dynamics 365 Customer Engagement la un nivel de entitate juridică. Puteți avea o singură persoană juridică folosind Project Operations pe Dynamics 365 Customer Engagement pentru resurse/scenarii bazate pe stoc. În același mediu, puteți avea o altă entitate juridică care utilizează Project Operations pentru scenarii stocate/comandă de producție.

1. În Dynamics 365 Finance, accesați **Gestionarea proiectelor și contabilitate** > **Configurare** > **Gestionare globală de proiect și parametri de contabilitate**.
2. În lista persoanelor juridice disponibile, selectați entitățile în care sunt activate mai multe linii contractuale și Project Operations pe caracteristicile Dynamics 365 Customer Engagement vor fi activate. Lăsați persoanele juridice care vor folosi Project Operations pentru scenarii stocate/comandă de producție neselectate.

> [!NOTE]
> O entitate juridică poate fi selectată numai dacă nu are proiecte existente.

## <a name="configure-project-management-and-accounting-parameters"></a>Configurați Gestionarea proiectului și parametrii de contabilitate

Fiecare persoană juridică care folosește Project Operations pe Dynamics 365 Customer Engagement are nevoie de un set de parametri impliciti. Acești parametri sunt configurați pe fila **Project Operations** de pe pagina **Managementul proiectului și parametrii contabili**. Parametrii sunt:

  - **Tip implicit de facturare** : Project Operations utilizează un set fix de valori implicite de tip facturare care trebuie mapate la proprietățile liniei Finanțare. Creați o înregistrare pentru fiecare tip de facturare: **Nespecificat** , **Taxabil** , **Netaxabil** , **Gratuit** , și **Nu e disponibil**.
  - **Categorii de proiecte implicite** : Selectați categoriile implicite de proiect care vor fi utilizate pentru fiecare tip de tranzacție. Aceste valori implicite vor fi utilizate în **Jurnal de integrare a Project Operations** și în estimări în care nu este specificată nicio categorie de tranzacții pentru proiectul real.
  - **Prognoze** : Selectați modelul de prognoză care va fi utilizat pentru estimări de timp și cheltuieli.
