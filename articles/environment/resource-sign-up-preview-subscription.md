---
title: Înscrieți-vă pentru abonamente de previzualizare a Project Operations pentru resurse/scenarii ne-stocate
description: Acest subiect oferă informații despre cum să aboneze și implementeze Project Operations pentru resurse/scenarii care nu sunt bazate pe stoc.
author: sigitac
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: dc3b353f19b915f645aed91dc2a8127117027034
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121143"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>Înscrieți-vă pentru abonamente de previzualizare a Project Operations pentru resurse/scenarii ne-stocate

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

Acest subiect explică cum să vă abonați la oferta de previzualizare/parteneriat și să implementați mediul Project Operations pentru resurse/scenarii bazate pe stoc.

## <a name="prerequisites"></a>Cerințe preliminare

- Veți primi un e-mail care vă invită să participați la previzualizare. Puteți solicita o previzualizare pe [Site-ul web al Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- Utilizatorul care implementează previzualizarea trebuie să aibă drepturi de administrator global entitate găzduită Azure.
- Implementarea unui mediu financiar necesită un abonament Azure valid care va fi facturat pe mediu. Puteți utiliza abonamentul existent al organizațiilor dvs. sau puteți utiliza o [versiune de încercare Azureal](https://azure.microsoft.com/en-us/free/) pentru a începe. Mediul CDS va fi furnizat gratuit pentru o perioadă limitată de 30 de zile.

## <a name="subscribe"></a>Abonare

Când [cerere de previzualizare](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) este aprobată, veți primi trei oferte de la Microsoft prin e-mail. Aceste oferte vă permit să implementați previzualizarea Project Operations:

- Dynamics 365 Project Operations (CRM) – previzualizare versiune de încercare
- Office 365 Project Operations - Previzualizare versiune de încercare
- Dynamics 365 Finance - previzualizare versiune de încercare

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

### <a name="dynamics-365-finance-preview-trial"></a>Dynamics 365 Finance previzualizare versiune de încercare

Repetați aceiași pași cu ultima ofertă din e-mailul de bun venit.

## <a name="assign-licenses"></a>Atribuiți licențe

> [!IMPORTANT]
> Veți avea nevoie de acces administrativ la organizația dvs. Microsoft 365 Portal pentru a finaliza pașii următori.

1. Accesați [Centrul de administrare Microsoft 365](https://portal.office.com/) pentru a atribui licențele utilizatorilor dvs.

![Pagina principală a centrului de administrare](./media/14AdminPortal.png)

2. Pe pagina **Utilizatori activi**, selectați utilizatorii cărora doriți să le atribuiți o licență.

![Atribuiți licențe](./media/15AssignLicenses.png)

3. Verificați dacă **Previzualizare Operațiuni de proiect Dynamics 365 (CRM)** și licența **Office 365 Operațiuni de proiect - Previzualizare** au fost selectate și selectați **Salvează modificările**.

> [!NOTE]
> Oferta de încercare finanțe nu trebuie să fie atribuită unui utilizator.

## <a name="start-a-new-project-in-lcs"></a>Începerea unui nou proiect în LCS

Creați un nou proiect LCS așa cum este descris în subiect, [Începeți un nou proiect în LCS](create-lcs-project.md)

## <a name="add-an-azure-subscription-to-an-lcs-project"></a>Adăugarea unui abonament Azure unui proiectul LCS

Pentru a finaliza această sarcină, urmați pașii din subiect, [Adăugați un abonament Azure la proiectul LCS](resource-add-azure-subscription-lcs-project.md).

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a>Implementați mediul demo de finanțare cu Project Operations pentru resurse/scenarii fără stoc

Urmați îndrumările din subiect, [Furnizarea accesului la un mediu nou](resource-provision-new-environment.md) pentru a finaliza implementarea. Utilizați tipul de implementare [mediu demonstrativ](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) pentru previzualizare. 

## <a name="install-cds-setup-and-configuration-data"></a>Instalați datele de instalare și configurare CDS

Instalați datele de configurare și configurare CDS așa cum este descris în subiect, [Configurați și aplicați datele de configurare în Common Data Service](resource-apply-pro-setup-config-data.md).
Finalizați acest pas numai după ce mediul de demonstrație Finance este implementat și datele demo din FO sunt gata.
