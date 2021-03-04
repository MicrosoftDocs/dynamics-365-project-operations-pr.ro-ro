---
title: Înscrieți-vă pentru un abonament de previzualizare - simplificat
description: Acest subiect oferă informații despre cum să vă abonați și să implementați Project Operations simplificat - gestionați facturarea proforma.
author: sigitac
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6f4360b7febab57b97df0776ef9148d2a38f16a7
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/30/2020
ms.locfileid: "4175906"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a>Înscrieți-vă pentru un abonament de previzualizare - simplificat 

Acest subiect explică cum să vă abonați la oferta de previzualizare de partener și să implementați Dynamics 365 Project Operations implementare simplificată - facturare de la tranzacție la proforma.

> [!NOTE]
> Acest proces se va schimba în versiunile viitoare ale Project Operations.

## <a name="prerequisites"></a>Cerințe preliminare

- Veți primi un e-mail care vă invită să participați la previzualizare. Puteți solicita o previzualizare pe [Site-ul web al Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- Utilizatorul care implementează previzualizarea trebuie să aibă drepturi de administrator global entitate găzduită Azure.
- Examinați toți termenii și condițiile.

## <a name="subscribe"></a>Abonare

Când primiți o aprobare de [cerere de previzualizare](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u), veți primi două oferte de la Microsoft prin e-mail. Aceste oferte vă permit să implementați previzualizarea Project Operations:

- Dynamics 365 Project Operations (CRM) – previzualizare versiune de încercare
- Office 365 Project Operations - Previzualizare versiune de încercare

> [!IMPORTANT]
> O singură persoană, administratorul entității găzduite, dintr-o organizație trebuie să îndeplinească această sarcină. Dacă nu sunteți abonatul la această versiune, așteptați până când organizația dvs. a fost înregistrată și ați primit acreditările dvs. de utilizator.

### <a name="dynamics-365-project-operations-crm---preview-trial"></a>Dynamics 365 Project Operations (CRM) – previzualizare versiune de încercare 

Înainte de a începe, asigurați-vă că sunteți conectat la un browser cu contul de lucru al utilizatorului în chiriașul în care doriți previzualizarea Project Operations.

1. Valorificați primul cod de ofertă, **Dynamics 365 Project Operations (CRM) - Previzualizare versiune de încercare** lipindu-l în URL-ul browserului.

![Valorificați oferta](./media/16RedeemFirstOfferNew.png)

2. Confirmați comanda.
![Confirmați comanda](./media/17ConfirmOrderNew.png)

Veți vedea că oferta de confirmare a fost valorificată cu succes.

![Confirmare](./media/18OrderConfirmationNew.png)

### <a name="office-365-project-operations---preview-trial"></a>Office 365 Project Operations - Previzualizare versiune de încercare

Repetați aceiași pași ca la primul cod de ofertă. Asigurați-vă că adăugați al doilea cod de ofertă utilizând același cont de utilizator care a fost utilizat cu primul cod de ofertă.

## <a name="assign-licenses"></a>Atribuiți licențe

> [!IMPORTANT]
> Veți avea nevoie de acces administrativ la organizația dvs. Microsoft 365 Portal pentru a finaliza pașii următori.


1. Accesați [Centrul de administrare Microsoft 365](https://portal.office.com/) pentru a atribui licențele utilizatorilor dvs.

![Pagina principală a centrului de administrare](./media/14AdminPortal.png)

2. Pe pagina **Utilizatori activi**, selectați utilizatorii cărora doriți să le atribuiți o licență.

![Atribuiți licențe](./media/15AssignLicenses.png)

3. Verificați ca licențele **Dynamics 365 Project Operations (CRM) Previzualizare** și **Office 365 Project Operations - Previzualizare** să fie selectate. 
4. Selectați **Salvați modificările**.

## <a name="create-a-new-cds-environment"></a>Creați un nou mediu CDS

1. Furnizați un nou mediu de implementare CDS pentru Project Operations urmând instrucțiunile din subiect, [Model de implementare CDS](lite-deployment.md). Când selectați tipul de mediu, asigurați-vă că utilizați **Versiune de încercare (pe bază de abonament)**.
![Mediu nou](./media/19CreateEnvironment.png)

2. Selectați setarea **Activați aplicațiile Dynamics 365** și lăsați **Implementați automat aceste aplicații** gol.  
3. Selectați **Salvare** pentru a crea mediul.

![Adăugați baza de date](./media/20CreateEnvironment1.png)

4. După crearea mediului, instalați soluția **Microsoft Dynamics 365 Project Operations**. 

![Instalați soluția](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a>Instalați o configurare CDS și instalați date demonstrative

Instalați configurația CDS și configurați datele demo urmând instrucțiunile din subiect, [Aplicați datele de instalare și configurare demonstrative](lite-apply-demo-setup-config-data.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]