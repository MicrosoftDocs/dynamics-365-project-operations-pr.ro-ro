---
title: Înscrieți-vă pentru abonamente de previzualizare a Project Operations pentru resurse/scenarii ne-stocate
description: Acest subiect oferă informații despre cum să aboneze și implementeze Project Operations pentru resurse/scenarii care nu sunt bazate pe stoc.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4d35a8bf9e8a841b45808b26ae2587c5b7d99d72
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949032"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>Înscrieți-vă pentru abonamente de previzualizare a Project Operations pentru resurse/scenarii ne-stocate

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

Acest subiect explică cum să vă abonați la oferta de previzualizare/parteneriat și să implementați mediul Project Operations pentru resurse/scenarii bazate pe stoc.

## <a name="prerequisites"></a>Cerințe preliminare

- Veți primi un e-mail care vă invită să participați la previzualizare. Puteți solicita o previzualizare pe [Site-ul web al Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- Utilizatorul care implementează previzualizarea trebuie să aibă drepturi de administrator global entitate găzduită Azure.
- Implementarea unui mediu financiar necesită un abonament Azure valid care va fi facturat pe mediu. Puteți utiliza abonamentul existent al organizațiilor dvs. sau puteți utiliza o [versiune de încercare Azureal](https://azure.microsoft.com/en-us/free/) pentru a începe. Mediul CDS va fi furnizat gratuit pentru o perioadă limitată de 30 de zile.

## <a name="subscribe"></a>Abonare

Când [cerere de previzualizare](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) este aprobat, veți primi două oferte de la Microsoft prin e-mail. Aceste oferte vă permit să implementați previzualizarea Project Operations:

- Dynamics 365 Project Operations – versiune de încercare de previzualizare
- Dynamics 365 for Finance and Operations Previzualizare versiune de încercare.

> [!IMPORTANT]
> O singură persoană, administratorul entității găzduite, dintr-o organizație trebuie să îndeplinească această sarcină. Dacă nu sunteți abonatul la această versiune, așteptați până când organizația dvs. a fost înregistrată și ați primit acreditările dvs. de utilizator.

### <a name="dynamics-365-project-operations--preview-trial"></a>Dynamics 365 Project Operations – Versiune de încercare de previzualizare

1. Valorificați prima ofertă, **Versiune de încercare Dynamics 365 Project Operations**, cu adresa URL furnizată în e-mailul binevenit.

![Prima ofertă](./media/1FirstOffer.png)

2. Verificați dacă sunteți conectat ca utilizator care aparține organizației care se va abona la serviciu.
3. Continuați cu valorificarea ofertei. 
4. Selectați **Da, adăugați-l la contul meu**.

![Valorificați oferta](./media/2RedeemFirstOffer.png)

![Confirmați oferta](./media/3ConfirmFirstOffer.png)

![Ofertă valorificată](./media/4OfferSuccessfulyRedeemed.png)

### <a name="dynamics-365-finance-preview-trial"></a>Dynamics 365 Finance previzualizare versiune de încercare

Repetați aceiași pași cu a doua ofertă din e-mailul de bun venit.

## <a name="assign-licenses"></a>Atribuiți licențe

> [!IMPORTANT]
> Veți avea nevoie de acces administrativ la organizația dvs. Office 365 Portal pentru a finaliza pașii următori.

1. Accesați [Centrul de administrare Microsoft 365](https://portal.office.com/) pentru a atribui licențe utilizatorilor dvs.

![Portal de administrare Office](./media/5OfficeAdminPortal.png)

2. Pe pagina **Utilizatori activi**, selectați utilizatorii cărora doriți să le atribuiți o licență.

![Atribuiți licențe](./media/6AssignLicenses.png)

3. Verificați dacă a fost selectată licența Project Operations și selectați **Salvează modificările**. 

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

