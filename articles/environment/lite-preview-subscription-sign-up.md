---
title: Înscrieți-vă pentru un abonament de previzualizare - simplificat
description: Acest subiect oferă informații despre cum să vă abonați și să implementați Project Operations simplificat - gestionați facturarea proforma.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5ba43ba9f917da068415fb62067ab73433b701139ee07014b6bd8c02612008ce
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/06/2021
ms.locfileid: "6991546"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a>Înscrierea pentru un abonament de previzualizare - simplificat 

Acest subiect explică modul de abonare la oferta de încercare și de implementare a Dynamics 365 Project Operations cu implementare simplă - gestionarea facturării proforma.

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


1. Accesați [Centrul de administrare Microsoft 365](https://portal.office.com/) pentru a atribui licențele utilizatorilor dvs.
2. Pe pagina **Utilizatori activi**, selectați utilizatorii cărora doriți să le atribuiți o licență.
3. Verificați dacă este selectată licența **Dynamics 365 Project Operations**. 
4. Selectați **Salvați modificările**.

## <a name="create-a-new-dataverse-environment"></a>Creați un nou mediu Dataverse

1. Asigurați acces la un nou mediu de implementare Project Operations Dataverse urmând instrucțiunile din subiectul, [Model de implementare Dataverse](lite-deployment.md). Când selectați tipul de mediu, asigurați-vă că utilizați **Versiune de încercare (pe bază de abonament)**.

  ![Mediu nou.](./media/19CreateEnvironment.png)

2. Selectați setarea **Activați aplicațiile Dynamics 365** și lăsați **Implementați automat aceste aplicații** gol.  
3. Selectați **Salvare** pentru a crea mediul.

  ![Adăugați baza de date.](./media/20CreateEnvironment1.png)

4. După crearea mediului, instalați soluția **Microsoft Dynamics 365 Project Operations**. 

![Instalați soluția.](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a>Instalați o configurare CDS și instalați date demonstrative

Instalați configurația CDS și configurați datele demo urmând instrucțiunile din subiect, [Aplicați datele de instalare și configurare demonstrative](lite-apply-demo-setup-config-data.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
