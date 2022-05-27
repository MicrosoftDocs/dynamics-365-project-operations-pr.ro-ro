---
title: Înscrieți-vă pentru abonamente de previzualizare a Project Operations pentru resurse/scenarii ne-stocate
description: Acest subiect oferă informații despre cum să aboneze și implementeze Project Operations pentru resurse/scenarii care nu sunt bazate pe stoc.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 9094b6928c5c276a40166ef5d8cb0facb539685b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8575825"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>Înscrieți-vă pentru abonamente de previzualizare a Project Operations pentru resurse/scenarii ne-stocate

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_



Acest subiect explică cum să vă abonați la oferta de încercare și să implementați mediul Project Operations pentru scenarii bazate pe resurse/nebazate pe stoc.

## <a name="prerequisites"></a>Cerințe preliminare
- Utilizatorul care implementează previzualizarea trebuie să aibă drepturi de administrator global entitate găzduită Azure. Puteți crea o entitate găzduită în timpul primei răscumpărări a ofertei. 
- Implementarea unui mediu financiar necesită un abonament Azure valid care va fi facturat pe mediu. Puteți utiliza abonamentul existent al organizațiilor dvs. sau puteți utiliza o [versiune de încercare Azureal](https://azure.microsoft.com/free/) pentru a începe. Mediul CDS va fi furnizat gratuit pentru o perioadă limitată de 30 de zile.

> [!IMPORTANT]
> O singură persoană, administratorul entității găzduite, dintr-o organizație trebuie să îndeplinească această sarcină. Dacă nu sunteți abonatul la această versiune, așteptați până când organizația dvs. a fost înregistrată și ați primit acreditările dvs. de utilizator.
> 
> Încercările sunt de unică folosință în entitate găzduită. Puteți rula o versiune de încercare o singură dată. Vă recomandăm să creați o nouă entitate găzduită în scopul versiunii de încercare.


### <a name="dynamics-365-project-operations-ce---preview-trial"></a>Dynamics 365 Project Operations (CE) - versiune preliminară de încercare 

Înainte de a începe, asigurați-vă că sunteți conectat la un browser cu contul de lucru al utilizatorului în chiriașul în care doriți previzualizarea Project Operations.

1. Valorificați primul cod de ofertă, **Dynamics 365 Project Operations** aici [Project Operations versiune de încercare](https://aka.ms/try-po).
2. Confirmați comanda.

  Veți vedea că oferta de confirmare a fost valorificată cu succes.

### <a name="dynamics-365-finance-preview-trial"></a>Probă de previzualizare Dynamics 365 Finance

Accesați [Dynamics 365 for Finance versiune prekiminară de încercare](https://aka.ms/trypoche) și repetați pașii din secțiunea anterioară cu oferta, Înscrieți-vă în mediul găzduit în cloud.  

## <a name="assign-licenses"></a>Atribuiți licențe

> [!IMPORTANT]
> Veți avea nevoie de acces administrativ la organizația dvs. Microsoft 365 Portal pentru a finaliza pașii următori.

1. Mergi la [Microsoft 365 centru de administrare](https://portal.office.com/) pentru a atribui licențele utilizatorilor dvs.

2. Pe pagina **Utilizatori activi**, selectați utilizatorii cărora doriți să le atribuiți o licență.

3. Verificați dacă licența **Dynamics 365 Project Operations** a fost selectată și selectați **Salvați modificările**.

> [!NOTE]
> Oferta de încercare finanțe nu trebuie să fie atribuită unui utilizator.

## <a name="start-a-new-project-in-lcs"></a>Începerea unui nou proiect în LCS

Creați un nou proiect LCS așa cum este descris în subiect, [Începeți un nou proiect în LCS](create-lcs-project.md)

## <a name="add-an-azure-subscription-to-an-lcs-project"></a>Adăugarea unui abonament Azure unui proiectul LCS

Pentru a finaliza această sarcină, urmați pașii din subiect, [Adăugați un abonament Azure la proiectul LCS](resource-add-azure-subscription-lcs-project.md).

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a>Implementați mediul demo de finanțare cu Project Operations pentru resurse/scenarii fără stoc

Urmați îndrumările din subiect, [Furnizarea accesului la un mediu nou](resource-provision-new-environment.md) pentru a finaliza implementarea. Utilizați tipul de implementare [mediu demonstrativ](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) pentru previzualizare. 

## <a name="install-cds-setup-and-configuration-data"></a>Instalați datele de instalare și configurare CDS

Instalați datele de configurare și configurare CDS așa cum este descris în subiect, [Configurați și aplicați datele de configurare în Common Data Service](resource-apply-pro-setup-config-data.md).
Finalizați acest pas numai după ce mediul de demonstrație Finance este implementat și datele demonstrative sunt gata.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
