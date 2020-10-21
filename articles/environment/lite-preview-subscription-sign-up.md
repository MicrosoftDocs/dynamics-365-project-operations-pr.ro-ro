---
title: Înscrieți-vă pentru un abonament de previzualizare
description: Acest subiect oferă informații despre cum să vă abonați și să implementați Project Operations simplificat - gestionați facturarea proforma.
author: sigitac
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a9c1432e8971eeb7918e23e00be9989294335f49
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949029"
---
# <a name="sign-up-for-a-preview-subscription-for-lite-deployment--deal-to-proforma-invoicing"></a>Înscrieți-vă pentru un abonament de previzualizare pentru implementare simplificată - faceți facturi proforma

Acest subiect explică cum să vă abonați la oferta de previzualizare de partener și să implementați Dynamics 365 Project Operations implementare simplificată - facturare de la tranzacție la proforma.

> [!NOTE]
> Acest proces se va schimba în versiunile viitoare ale Project Operations.

## <a name="prerequisites"></a>Cerințe preliminare

- Veți primi un e-mail care vă invită să participați la previzualizare. Puteți solicita o previzualizare pe [Site-ul web al Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- Utilizatorul care implementează previzualizarea trebuie să aibă drepturi de administrator global entitate găzduită Azure.
- Utilizatorul care implementează previzualizarea va avea nevoie de un număr de telefon și un card de credit valid. În timpul înscrierii, nu vor exista taxe pe card timp de șase luni. După șase luni, trebuie să anulați abonamentul. 
- Examinați toți termenii și condițiile.

## <a name="subscribe"></a>Abonare

Când primiți o aprobare [cerere de previzualizare](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u), veți primi două oferte de la Microsoft prin e-mail. Aceste oferte vă permit să implementați previzualizarea Project Operations:

- Previzualizare încercare Dynamics 365 Customer Service - cod de o singură utilizare
- Dynamics 365 Project Operations – versiune de încercare de previzualizare

### <a name="dynamics-365-customer-service-paid-offer"></a>Ofertă plătită Dynamics 365 Customer Service

1. Folosind o fereastră de browser InPrivate/Incognito, valorificați primul cod de ofertă pentru Dynamics 365 Customer Service. Pentru a vă înscrie la serviciu pentru relații cu clienții, veți avea nevoie de:

- Un număr de telefon
- Un card de credit. Când vă înscrieți, timp de șase luni cardul nu va fi taxat. După șase luni, trebuie să anulați abonamentul.
- Examinați toți termenii și condițiile.

2. Furnizați informațiile dvs. de contact.

![Informații contact](./media/1ContactInformation.png)

3. Furnizați detaliile noilor entități găzduite.

![Creați ID de utilizator](./media/2CreateUserID.png)

4. Verificați-vă identitatea, salvați noul ID de utilizator, apoi selectați **Instalare**.

![Salvați informații](./media/3SaveInfo.png)

5. Finalizați înscrierea cardului de credit și examinați toți termenii și condițiile. 

![Finalizați cardul de credit](./media/4CompleteCreditCard.png)

![Extrageți cardul de credit](./media/5CreditCardCheckout.png)

![Salvați comanda](./media/6SaveOrder.png)

![Confirmare card de credit](./media/7Confirmation.png)

## <a name="cancel-the-dynamics-365-customer-service-enterprise-offer"></a>Anulați oferta de întreprindere Dynamics 365 Customer Service

Oferta Dynamics 365 Customer Service pentru întreprinderi este oferită gratuit timp de șase luni. Oferta va fi reînnoită la tariful complet la sfârșitul perioadei de șase luni. Pentru a anula înainte de data reînnoirii, completați următoarele instrucțiuni. 

> [!NOTE]
> După ce parcurgeți acești pași, nu veți mai putea utiliza mediul de previzualizare publică Project Operations.

1. Accesați [Portal de administrare](https://admin.microsoft.com/) și sub **Facturare**, selectați **Produsele dvs.**.

![Portal de administrare, pagina Produsele dvs.](./media/8AdminPortal.png)

2. Selectați **Oferta de întreprindere Dynamics 365 Customer Service**.

![Anulați abonamentul](./media/9CancelSubscription.png)

3. Selectați **Setări** > **Acțiuni** > **Anulați abonamentul**.
4. Pe formularul **Anularea abonamentului**, introduceți informații în câmpurile obligatorii.
5. Selectați **Anulare** > **Abonament.**

### <a name="dynamics-365-project-operations--preview-trial"></a>Dynamics 365 Project Operations – Versiune de încercare de previzualizare

1. Valorificați a doua ofertă, Versiune de încercare Dynamics 365 Project Operations, cu adresa URL furnizată în e-mailul binevenit.

![Valorificați oferta 2](./media/10RedeemOffer2.png)

2. Verificați dacă sunteți conectat ca utilizator care aparține aceleiași organizații care a fost abonată utilizând primul cod de ofertă și apoi continuați cu valorificarea ofertei. 
3. Selectați **Da, adăugați-l la contul meu**.

![Adăugare la cont](./media/11AddToAccount.png)

![Încercați Ecran acum](./media/12TryNow.png)

![Detalii comandă](./media/13Confirmation.png)

## <a name="assign-licenses"></a>Atribuiți licențe

> [!IMPORTANT]
> Veți avea nevoie de acces administrativ la organizația dvs. Office 365 Portal pentru a finaliza pașii următori.

1. Accesați [Centrul de administrare Microsoft 365](https://portal.office.com/) pentru a atribui licențele utilizatorilor dvs.

![Pagina principală a centrului de administrare](./media/14AdminPortal.png)

2. Pe pagina **Utilizatori activi**, selectați utilizatorii cărora doriți să le atribuiți o licență.

![Atribuiți licențe](./media/15AssignLicenses.png)

3. Verificați ca **Customer Service Enterprise** și licența**Project Operations** au fost selectate și selectați **Salvați modificările**.

## <a name="create-a-new-cds-environment"></a>Creați un nou mediu CDS

Furnizați un nou mediu de implementare CDS pentru Project Operations urmând instrucțiunile din subiect, [Model de implementare CDS](lite-deployment.md).

## <a name="install-a-cds-configuration-and-setup-demo-data"></a>Instalați o configurare CDS și instalați date demonstrative

Instalați configurația CDS și configurați datele demo urmând instrucțiunile din subiect, [Aplicați datele de instalare și configurare demonstrative](lite-apply-demo-setup-config-data.md).
