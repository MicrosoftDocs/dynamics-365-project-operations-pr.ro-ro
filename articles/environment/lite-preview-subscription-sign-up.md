---
title: Înscrierea pentru un abonament de previzualizare - simplificat
description: Acest articol oferă informații despre cum să vă abonați și să implementați implementarea Project Operations lite - acord cu facturarea proforma.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 6953956c0b3401a6c64ee597f966ba4a4c0d07b5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921271"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a>Înscrierea pentru un abonament de previzualizare - simplificat 

Acest articol explică cum să vă abonați la oferta de încercare și să implementați Dynamics 365 Project Operations implementare simplă - acord cu facturarea proforma.

> [!NOTE]
> Acest proces se va schimba în versiunile viitoare ale Project Operations.

## <a name="prerequisites"></a>Cerințe preliminare
- Utilizatorul care implementează previzualizarea trebuie să aibă drepturi de administrator global entitate găzduită Azure. Puteți crea o entitate găzduită în timpul primei răscumpărări a ofertei.

> [!IMPORTANT]
> O singură persoană, administratorul entității găzduite, dintr-o organizație trebuie să îndeplinească această sarcină. Dacă nu sunteți abonatul la această versiune, așteptați până când organizația dvs. a fost înregistrată și ați primit acreditările dvs. de utilizator.
> 
> Încercările sunt de unică folosință în entitate găzduită. Puteți rula o versiune de încercare o singură dată. Vă recomandăm să creați o nouă entitate găzduită în scopul versiunii de încercare.

### <a name="dynamics-365-project-operations-trial"></a>Versiune de încercare Dynamics 365 Project Operations 

Înainte de a începe, asigurați-vă că sunteți conectat la un browser cu contul de lucru al utilizatorului în chiriașul în care doriți previzualizarea Project Operations.

1. Accesați [Project Operations versiune de încercare](https://aka.ms/try-po) pentru a valorifica primul cod de ofertă, **Dynamics 365 Project Operations**.
2. Confirmați comanda.

  Veți vedea că oferta de confirmare a fost valorificată cu succes.

## <a name="assign-licenses"></a>Atribuiți licențe

> [!IMPORTANT]
> Veți avea nevoie de acces administrativ la organizația dvs. Microsoft 365 Portal pentru a finaliza pașii următori.


1. Mergi la [Microsoft 365 centru de administrare](https://portal.office.com/) pentru a atribui licențele utilizatorilor dvs.
2. Pe pagina **Utilizatori activi**, selectați utilizatorii cărora doriți să le atribuiți o licență.
3. Verificați dacă este selectată licența **Dynamics 365 Project Operations**. 
4. Selectați **Salvați modificările**.

## <a name="create-a-new-dataverse-environment"></a>Creați un nou mediu Dataverse

1. Furnizarea unui nou proiect Operațiuni Dataverse mediu de implementare urmând instrucțiunile din articol, [Dataverse model de implementare](lite-deployment.md). Când selectați tipul de mediu, asigurați-vă că utilizați **Versiune de încercare (pe bază de abonament)**.

  ![Mediu nou.](./media/19CreateEnvironment.png)

2. Selectați setarea **Activați aplicațiile Dynamics 365** și lăsați **Implementați automat aceste aplicații** gol.  
3. Selectați **Salvare** pentru a crea mediul.

  ![Adăugați baza de date.](./media/20CreateEnvironment1.png)

4. După crearea mediului, instalați soluția **Microsoft Dynamics 365 Project Operations**. 

![Instalați soluția.](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a>Instalați o configurare CDS și instalați date demonstrative

Instalați configurația CDS și configurați datele demo urmând instrucțiunile din articol, [Aplicați datele de configurare și configurare demo](lite-apply-demo-setup-config-data.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
