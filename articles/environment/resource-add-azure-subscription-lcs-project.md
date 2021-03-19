---
title: Adăugarea unui abonament Azure unui proiectul LCS
description: Acest subiect oferă informații despre cum să vă conectați abonamentul Azure la un proiect LCS.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: ad1ddd69cbb8db7780b8277a7ed7533d3ea3d053
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289924"
---
# <a name="add-an-azure-subscription-to-an-lcs-project"></a>Adăugarea unui abonament Azure unui proiectul LCS

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

Mediile găzduite în cloud trebuie să fie implementate utilizând un abonament Azure existent. Acest subiect explică cum să vă conectați abonamentul Azure existent la un proiect LCS. 

## <a name="grant-admin-consent"></a>Acordă consimțământul administratorului

1. În proiectul dvs. LCS, în secțiunea **Medii**, selectați **Microsoft Azure setări**.

![Setările Microsoft Azure](./media/1MicrosoftAzureSettings.png)

2. Pe pagina **Setările proiectului**, pe fila **Conectori Azure**, selectați **Autorizare**. Acest lucru permite implementarea mediilor în acest proiect.

![Conectori Azure](./media/2AzureConnectors.png)

3. Selectați **Autorizare** din nou pentru a furniza consimțământul administratorului.

![Acordați consimțământul administratorului](./media/3GrantAdminConsent.png)

4. Acceptați solicitarea de permisiuni.

![Acceptați solicitarea de permisiune](./media/4AcceptPermissionRequest.png)

Autorizația este acum completă. 

![Autorizarea a reușit](./media/5AuthorizationComplete.png)

## <a name="provide-dynamics-deployment-services-access-to-your-azure-subscription"></a><a name="provide"></a>Oferiți acces la serviciile de implementare dinamică la abonamentul dvs. Azure

1. Accesați [Microsoft Azure facturare](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) și selectați-vă abonamentul. Dynamics Deployment Services trebuie să acceseze acest abonament pentru a putea implementa medii.

![Detalii abonament Azure](./media/6AzureSubscription.png)

2. Selectați **Control acces (IAM)** în panoul de navigare, apoi selectați **Adăugați atribuirea de roluri**.
3. În glisorul din partea dreaptă, selectați **Rol de colaborator**, și în lista furnizată, găsiți și selectați **Dynamics Deployment Services**. 
4. Selectați **Salvare**.

![Acces abonamente](./media/7SubscriptionAccess.png)

### <a name="add-a-subscription-connector-to-an-lcs-project"></a>Adăugați un conector de abonament la un proiect LCS

1. În proiectul dvs. LCS, pe pagina **Microsoft Azure setări**, selectați **Adăugare** pentru a adăuga un nou conector.
2. Introduceți codul de abonament Azure. Puteți găsi ID-ul dvs. de abonament Azure în [Portal Azure](https://ms.portal.azure.com/), sub  **Setări**  în colțul din stânga jos al ecranului.
3. În câmpul **Configurați pentru a utiliza Azure Resource Manager**, selectați **Da**.
4. Asigurați-vă că Abonamentul Azure AAD Domeniu entitate găzduită se potrivește cu abonamentul Azure deținut de domeniu pe care îl utilizați și selectați **Următorul**.
5. Pe ecranul **Microsoft Azure Instalare** ecran, selectați **Următorul** pentru a confirma. Dacă primiți o eroare pe acest ecran, reveniți la secțiunea [Oferiți acces la serviciile de implementare dinamică la abonamentul Azure](#provide) în acest subiect și asigurați-vă că ați parcurs toți pașii.
6. Descărcați certificatul de gestionare Azure într-un folder local de pe computer, apoi încărcați-l în Azure Management Portal accesând **Setări** > **Certificate de management**. Acest certificat va permite LCS să comunice cu Azure în numele dvs. Puteți sări peste acest pas dacă utilizatorul dvs. are acces la abonament.
7. Selectați  **Următorul**.
8. Selectați regiunea Azure în care să implementați și selectați un centru de date care este aproape de locul în care intenționați să utilizați acest sistem.
9.  Selectați  **Conectare**.

Ați conectat cu succes abonamentul Azure. Acum puteți implementa medii găzduite în cloud Dynamics 365 Finance.




[!INCLUDE[footer-include](../includes/footer-banner.md)]