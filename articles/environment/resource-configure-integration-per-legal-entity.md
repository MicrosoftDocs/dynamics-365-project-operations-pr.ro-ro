---
title: Configurarea integrării Project Operations per entitate juridică
description: Acest articol oferă informații despre configurarea integrării de către persoana juridică în Operațiuni de proiect.
author: sigitac
ms.date: 10/21/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 3f33e641ee0932655282618c99a26e2603660059
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914693"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a>Configurarea integrării Project Operations per entitate juridică 

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

Acest articol vă prezintă pașii necesari pentru a configura Dynamics 365 Project Operations pe persoană juridică.

## <a name="enable-feature-keys-in-dynamics-365-finance"></a>Activați cheile de funcție în Dynamics 365 Finance

Parcurgeți pașii următori pentru a activa funcțiile necesare.

1. În Dynamics 365 Finance, accesați **Managementul caracteristicilor** spațiu de lucru.
2. În **Listă de caracteristici**, găsiți și activați următoarele caracteristici:
  
    - **Activați mai multe linii contractuale pentru un proiect**
    - **Activați operațiunile de proiect pe Dynamics 365 Customer Engagement**

> [!NOTE]
> Dacă nu vedeți **Taste funcționale** afișat, verificați dacă versiunea dvs. de finanțare îndeplinește cerința de versiune minimă (versiunea aplicației 10.0.13 cu toate actualizările de calitate aplicate sau mai mare). Selectați **Verifică pentru actualizări** pentru a reîmprospăta lista de funcții.

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a>Definiți scenariul de implementare a Project Operations pentru o entitate juridică

Puteți activa Operațiunile de proiect pe Dynamics 365 Customer Engagement la nivel de entitate juridică. Puteți avea o singură entitate juridică care folosește Operațiuni de proiect pe Dynamics 365 Customer Engagement pentru scenarii bazate pe resurse/nestoc. În același mediu, puteți avea o altă entitate juridică care utilizează Project Operations pentru scenarii stocate/comandă de producție.

1. În Dynamics 365 Finance, accesați **Management de proiect si contabilitate** > **Înființat** > **Management global de proiect și parametri contabili**.
2. În lista de entități juridice disponibile, selectați entitățile în care vor fi activate mai multe linii de contract și operațiuni de proiect pe Dynamics 365 Customer Engagement. Lăsați persoanele juridice care vor folosi Project Operations pentru scenarii stocate/comandă de producție neselectate.

> [!NOTE]
> O entitate juridică poate fi selectată numai dacă nu are proiecte existente.

## <a name="configure-project-management-and-accounting-parameters"></a>Configurați Gestionarea proiectului și parametrii de contabilitate

Fiecare entitate juridică care utilizează Operațiuni de proiect pe Dynamics 365 Customer Engagement are nevoie de un set de parametri impliciti. Acești parametri sunt configurați pe fila **Project Operations** de pe pagina **Managementul proiectului și parametrii contabili**. Parametrii sunt:

  - **Tip implicit de facturare**: Project Operations utilizează un set fix de valori implicite de tip facturare care trebuie mapate la proprietățile liniei Finanțare. Creați o înregistrare pentru fiecare tip de facturare: **Nespecificat**, **Taxabil**, **Netaxabil**, **Gratuit**, și **Nu e disponibil**.
  - **Categorii de proiecte implicite**: Selectați categoriile implicite de proiect care vor fi utilizate pentru fiecare tip de tranzacție. Aceste valori implicite vor fi utilizate în **Jurnal de integrare a Project Operations** și în estimări în care nu este specificată nicio categorie de tranzacții pentru proiectul real.
  - **Prognoze**: Selectați modelul de prognoză care va fi utilizat pentru estimări de timp și cheltuieli.


[!INCLUDE[footer-include](../includes/footer-banner.md)]