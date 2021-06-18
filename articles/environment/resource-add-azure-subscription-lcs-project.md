---
title: Adăugarea unui abonament Azure unui proiectul LCS
description: Acest subiect oferă informații despre cum să vă conectați abonamentul Azure la un proiect LCS.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6daa86d453ec5022cdd75dff0394c8818292406c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000631"
---
# <a name="add-an-azure-subscription-to-an-lcs-project"></a><span data-ttu-id="0da1e-103">Adăugarea unui abonament Azure unui proiectul LCS</span><span class="sxs-lookup"><span data-stu-id="0da1e-103">Add an Azure subscription to an LCS project</span></span>

<span data-ttu-id="0da1e-104">_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_</span><span class="sxs-lookup"><span data-stu-id="0da1e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="0da1e-105">Mediile găzduite în cloud trebuie să fie implementate utilizând un abonament Azure existent.</span><span class="sxs-lookup"><span data-stu-id="0da1e-105">Cloud-hosted environments must be deployed using an existing Azure subscription.</span></span> <span data-ttu-id="0da1e-106">Acest subiect explică cum să vă conectați abonamentul Azure existent la un proiect LCS.</span><span class="sxs-lookup"><span data-stu-id="0da1e-106">This topic explains how to connect your existing Azure subscription to an LCS project.</span></span> 

## <a name="grant-admin-consent"></a><span data-ttu-id="0da1e-107">Acordă consimțământul administratorului</span><span class="sxs-lookup"><span data-stu-id="0da1e-107">Grant admin consent</span></span>

1. <span data-ttu-id="0da1e-108">În proiectul dvs. LCS, în secțiunea **Medii**, selectați **Microsoft Azure setări**.</span><span class="sxs-lookup"><span data-stu-id="0da1e-108">In your LCS project, in the **Environments** section, select **Microsoft Azure settings**.</span></span>

![Setările Microsoft Azure](./media/1MicrosoftAzureSettings.png)

2. <span data-ttu-id="0da1e-110">Pe pagina **Setările proiectului**, pe fila **Conectori Azure**, selectați **Autorizare**.</span><span class="sxs-lookup"><span data-stu-id="0da1e-110">On the **Project settings** page, on the **Azure connectors** tab, select **Authorize**.</span></span> <span data-ttu-id="0da1e-111">Acest lucru permite implementarea mediilor în acest proiect.</span><span class="sxs-lookup"><span data-stu-id="0da1e-111">This allows environments to be deployed to this project.</span></span>

![Conectori Azure](./media/2AzureConnectors.png)

3. <span data-ttu-id="0da1e-113">Selectați **Autorizare** din nou pentru a furniza consimțământul administratorului.</span><span class="sxs-lookup"><span data-stu-id="0da1e-113">Select **Authorize** again to provide admin consent.</span></span>

![Acordați consimțământul administratorului](./media/3GrantAdminConsent.png)

4. <span data-ttu-id="0da1e-115">Acceptați solicitarea de permisiuni.</span><span class="sxs-lookup"><span data-stu-id="0da1e-115">Accept the permissions request.</span></span>

![Acceptați solicitarea de permisiune](./media/4AcceptPermissionRequest.png)

<span data-ttu-id="0da1e-117">Autorizația este acum completă.</span><span class="sxs-lookup"><span data-stu-id="0da1e-117">The authorization is now complete.</span></span> 

![Autorizarea a reușit](./media/5AuthorizationComplete.png)

## <a name="provide-dynamics-deployment-services-access-to-your-azure-subscription"></a><a name="provide"></a><span data-ttu-id="0da1e-119">Oferiți acces la serviciile de implementare dinamică la abonamentul dvs. Azure</span><span class="sxs-lookup"><span data-stu-id="0da1e-119">Provide Dynamics Deployment Services access to your Azure subscription</span></span>

1. <span data-ttu-id="0da1e-120">Accesați [Microsoft Azure facturare](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) și selectați-vă abonamentul.</span><span class="sxs-lookup"><span data-stu-id="0da1e-120">Go to [Microsoft Azure billing](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) and select your subscription.</span></span> <span data-ttu-id="0da1e-121">Dynamics Deployment Services trebuie să acceseze acest abonament pentru a putea implementa medii.</span><span class="sxs-lookup"><span data-stu-id="0da1e-121">Dynamics Deployment Services needs to access this subscription to be able to deploy environments.</span></span>

![Detalii abonament Azure](./media/6AzureSubscription.png)

2. <span data-ttu-id="0da1e-123">Selectați **Control acces (IAM)** în panoul de navigare, apoi selectați **Adăugați atribuirea de roluri**.</span><span class="sxs-lookup"><span data-stu-id="0da1e-123">Select **Access control (IAM)** in the navigation pane, and then select **Add role assignment**.</span></span>
3. <span data-ttu-id="0da1e-124">În glisorul din partea dreaptă, selectați **Rol de colaborator**, și în lista furnizată, găsiți și selectați **Dynamics Deployment Services**.</span><span class="sxs-lookup"><span data-stu-id="0da1e-124">In the slider on the right side, select **Contributor role**, and in the list provided, find and select **Dynamics Deployment Services**.</span></span> 
4. <span data-ttu-id="0da1e-125">Selectați **Salvare**.</span><span class="sxs-lookup"><span data-stu-id="0da1e-125">Select **Save**.</span></span>

![Acces abonamente](./media/7SubscriptionAccess.png)

### <a name="add-a-subscription-connector-to-an-lcs-project"></a><span data-ttu-id="0da1e-127">Adăugați un conector de abonament la un proiect LCS</span><span class="sxs-lookup"><span data-stu-id="0da1e-127">Add a subscription connector to an LCS project</span></span>

1. <span data-ttu-id="0da1e-128">În proiectul dvs. LCS, pe pagina **Microsoft Azure setări**, selectați **Adăugare** pentru a adăuga un nou conector.</span><span class="sxs-lookup"><span data-stu-id="0da1e-128">In your LCS project, on the **Microsoft Azure settings** page, select **Add** to add a new connector.</span></span>
2. <span data-ttu-id="0da1e-129">Introduceți codul de abonament Azure.</span><span class="sxs-lookup"><span data-stu-id="0da1e-129">Enter your Azure subscription ID.</span></span> <span data-ttu-id="0da1e-130">Puteți găsi ID-ul dvs. de abonament Azure în [Portal Azure](https://ms.portal.azure.com/), sub  **Setări**  în colțul din stânga jos al ecranului.</span><span class="sxs-lookup"><span data-stu-id="0da1e-130">You can find your Azure subscription ID in the [Azure portal](https://ms.portal.azure.com/), under  **Settings**  in the lower left of the screen.</span></span>
3. <span data-ttu-id="0da1e-131">În câmpul **Configurați pentru a utiliza Azure Resource Manager**, selectați **Da**.</span><span class="sxs-lookup"><span data-stu-id="0da1e-131">In the **Configure to use Azure Resource Manager** field, select **Yes**.</span></span>
4. <span data-ttu-id="0da1e-132">Asigurați-vă că Abonamentul Azure AAD Domeniu entitate găzduită se potrivește cu abonamentul Azure deținut de domeniu pe care îl utilizați și selectați **Următorul**.</span><span class="sxs-lookup"><span data-stu-id="0da1e-132">Make sure Azure's Subscription AAD Tenant Domain matches the domain-owning Azure subscription that you are using, and select **Next**.</span></span>
5. <span data-ttu-id="0da1e-133">Pe ecranul **Microsoft Azure Instalare** ecran, selectați **Următorul** pentru a confirma.</span><span class="sxs-lookup"><span data-stu-id="0da1e-133">On the **Microsoft Azure Setup** screen, select **Next** to confirm.</span></span> <span data-ttu-id="0da1e-134">Dacă primiți o eroare pe acest ecran, reveniți la secțiunea [Oferiți acces la serviciile de implementare dinamică la abonamentul Azure](#provide) în acest subiect și asigurați-vă că ați parcurs toți pașii.</span><span class="sxs-lookup"><span data-stu-id="0da1e-134">If you receive an error on this screen, return to the section [Provide Dynamics Deployment Services access to Azure subscription](#provide) in this topic and make sure you have completed all of the steps.</span></span>
6. <span data-ttu-id="0da1e-135">Descărcați certificatul Azure Management într-un folder local de pe computer.</span><span class="sxs-lookup"><span data-stu-id="0da1e-135">Download the Azure Management Certificate to a local folder on your computer.</span></span> <span data-ttu-id="0da1e-136">Solicitați administratorului dvs. de abonament Azure să încarce certificatul în portalul Azure Management selectând abonamentul și accesând **Setări** > **Certificate de management**.</span><span class="sxs-lookup"><span data-stu-id="0da1e-136">Ask your Azure subscription administrator to upload the certificate to Azure Management Portal by selecting the subscription and going to **Settings** > **Management Certificates**.</span></span> <span data-ttu-id="0da1e-137">Acest certificat permite LCS să comunice cu Azure în numele dvs.</span><span class="sxs-lookup"><span data-stu-id="0da1e-137">This certificate enables LCS to communicate with Azure on your behalf.</span></span> <span data-ttu-id="0da1e-138">Puteți sări peste acest pas dacă utilizatorul dvs. are acces la abonament.</span><span class="sxs-lookup"><span data-stu-id="0da1e-138">You can skip this step if your user has access to the subscription.</span></span>
7. <span data-ttu-id="0da1e-139">Selectați  **Următorul**.</span><span class="sxs-lookup"><span data-stu-id="0da1e-139">Select  **Next**.</span></span>
8. <span data-ttu-id="0da1e-140">Selectați regiunea Azure în care să implementați și selectați un centru de date care este aproape de locul în care intenționați să utilizați acest sistem.</span><span class="sxs-lookup"><span data-stu-id="0da1e-140">Select the Azure region to deploy in and select a data center that is close to where you plan to use this system.</span></span>
9.  <span data-ttu-id="0da1e-141">Selectați  **Conectare**.</span><span class="sxs-lookup"><span data-stu-id="0da1e-141">Select  **Connect**.</span></span>

<span data-ttu-id="0da1e-142">Ați conectat cu succes abonamentul Azure.</span><span class="sxs-lookup"><span data-stu-id="0da1e-142">You have successfully connected your Azure subscription.</span></span> <span data-ttu-id="0da1e-143">Acum puteți implementa medii găzduite în cloud Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="0da1e-143">You can now deploy Dynamics 365 Finance cloud-hosted environments.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]
