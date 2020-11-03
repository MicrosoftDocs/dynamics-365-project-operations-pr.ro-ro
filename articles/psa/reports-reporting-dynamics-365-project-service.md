---
title: Pagina de pornire raportare
description: Acest subiect oferă informații despre raportare în Dynamics 365 Project Service Automation.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 30411818bdc1b370a71148cf79f743413167dab2
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083023"
---
# <a name="reporting-home-page"></a><span data-ttu-id="cf7c7-103">Pagina de pornire raportare</span><span class="sxs-lookup"><span data-stu-id="cf7c7-103">Reporting home page</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="cf7c7-104">Microsoft Dynamics 365 Project Service Automation le permite organizațiilor bazate pe proiecte să-și gestioneze eficient operațiunile activității.</span><span class="sxs-lookup"><span data-stu-id="cf7c7-104">Microsoft Dynamics 365 Project Service Automation lets project-based organizations efficiently manage the operations of their business.</span></span> <span data-ttu-id="cf7c7-105">În orice proiect, membrii echipei trebuie să gestioneze oportunitatea, să oferteze și să planifice activitatea, să stabilească resurse proiectele, să gestioneze lucrările conform planului, să factureze lucrările și apoi să realizeze lucrările pentru finalizarea proiectului.</span><span class="sxs-lookup"><span data-stu-id="cf7c7-105">On any project, team members must manage the opportunity, quote and plan the work, resource the projects, manage the work according to the plan, bill for the work, and then do the work to complete the project.</span></span> <span data-ttu-id="cf7c7-106">Capacitatea de a raporta operațiunile este esențială pentru determinarea stării de sănătate a organizației și pentru luarea oricărei acțiuni corective necesare.</span><span class="sxs-lookup"><span data-stu-id="cf7c7-106">The ability to report on operations is key to determining the health of the organization and taking any corrective action that's required.</span></span> <span data-ttu-id="cf7c7-107">PSA utilizează metode și tehnologii de raportare Microsoft Dynamics 365 pentru toate rapoartele.</span><span class="sxs-lookup"><span data-stu-id="cf7c7-107">PSA uses Microsoft Dynamics 365 reporting methods and technologies for all its reporting.</span></span> <span data-ttu-id="cf7c7-108">Pentru mai multe informații despre opțiunile de raportare, consultați [Ghid de scriere a raportului pentru Dynamics 365 Customer Engagement (on-premises), versiunea 9](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/reporting-analytics-with-dynamics-365).</span><span class="sxs-lookup"><span data-stu-id="cf7c7-108">For more information about the options for reporting, see the [Report writing guide for Dynamics 365 Customer Engagement (on-premises), version 9](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/reporting-analytics-with-dynamics-365).</span></span>

## <a name="report-wizard"></a><span data-ttu-id="cf7c7-109">Asistent raport</span><span class="sxs-lookup"><span data-stu-id="cf7c7-109">Report Wizard</span></span>

<span data-ttu-id="cf7c7-110">Asistentul raport le permite non-dezvoltatorilor să creeze rapoarte simple.</span><span class="sxs-lookup"><span data-stu-id="cf7c7-110">The Report Wizard lets non-developers create simple reports.</span></span> <span data-ttu-id="cf7c7-111">Deoarece aplicația este construită pe o platformă existentă, experiența este aceeași cu experiența documentată în [Crearea sau editarea unui raport utilizând Asistentul raport](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/basics/create-edit-copy-report-wizard).</span><span class="sxs-lookup"><span data-stu-id="cf7c7-111">Because the app is built on an existing platform, the experience is the same as the experience that is documented in [Create or edit a report using the Report Wizard](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/basics/create-edit-copy-report-wizard).</span></span> <span data-ttu-id="cf7c7-112">Cu toate acestea, veți utiliza entitățile specifice Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="cf7c7-112">However, you will use the Project Service Automation-specific entities.</span></span>

## <a name="custom-sql-server-reporting-services-reports"></a><span data-ttu-id="cf7c7-113">Rapoarte SQL Server Reporting Services particularizate</span><span class="sxs-lookup"><span data-stu-id="cf7c7-113">Custom SQL Server Reporting Services reports</span></span>

<span data-ttu-id="cf7c7-114">Dacă afacerea dumneavoastră necesită un raport specific care nu poate fi creat utilizând Asistentul raport, aveți posibilitatea să creați un raport particularizat.</span><span class="sxs-lookup"><span data-stu-id="cf7c7-114">If your business requires a specific report that can't be created by using the Report Wizard, you can create a custom report.</span></span> <span data-ttu-id="cf7c7-115">Trebuie să aveți instalat Microsoft Visual Studio, împreună cu extensiile adecvate Microsoft SQL Server Data Tools și de creare a rapoartelor.</span><span class="sxs-lookup"><span data-stu-id="cf7c7-115">You must have Microsoft Visual Studio installed, together with the appropriate Microsoft SQL Server Data Tools and Report Authoring Extensions.</span></span> <span data-ttu-id="cf7c7-116">Pentru mai multe informații despre instrumente și versiuni, consultați [Mediu de scriere rapoarte folosind SQL Server Data Tools](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/report-writing-environment-using-sql-server-data-tools).</span><span class="sxs-lookup"><span data-stu-id="cf7c7-116">For more information about tools and versions, see [Report writing environment using SQL Server Data Tools](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/report-writing-environment-using-sql-server-data-tools).</span></span> <span data-ttu-id="cf7c7-117">Pentru informații despre cum se creează un raport particularizat, consultați [Crearea unui raport nou utilizând SQL Server Data Tools](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/create-a-new-report-using-sql-server-data-tools).</span><span class="sxs-lookup"><span data-stu-id="cf7c7-117">For information about how to create a custom report, see [Create a new report using SQL Server Data Tools](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/create-a-new-report-using-sql-server-data-tools).</span></span>

## <a name="power-bi-insights-apps"></a><span data-ttu-id="cf7c7-118">aplicații Insights Power BI</span><span class="sxs-lookup"><span data-stu-id="cf7c7-118">Power BI insights apps</span></span>

<span data-ttu-id="cf7c7-119">Împreună, Microsoft Power BI și Dynamics 365 vă oferă o modalitate puternică de lucru cu datele dvs., sub formă de aplicații Insights.</span><span class="sxs-lookup"><span data-stu-id="cf7c7-119">Together, Microsoft Power BI and Dynamics 365 give you a powerful way to work with your data, in the form of insights apps.</span></span> <span data-ttu-id="cf7c7-120">Pentru informații despre disponibilitatea aplicațiilor Insights, consultați [Pagina de aplicații Insights Power BI](https://powerbi.microsoft.com/power-bi-insights-apps/).</span><span class="sxs-lookup"><span data-stu-id="cf7c7-120">For information about the availability of insights apps, see the [Power BI insights apps page](https://powerbi.microsoft.com/power-bi-insights-apps/).</span></span>


## <a name="additional-resources"></a><span data-ttu-id="cf7c7-121">Resurse suplimentare</span><span class="sxs-lookup"><span data-stu-id="cf7c7-121">Additional resources</span></span>
<span data-ttu-id="cf7c7-122">Pentru mai multe informații despre raportarea în PSA, consultați următoarele subiecte:</span><span class="sxs-lookup"><span data-stu-id="cf7c7-122">For more information about reporting in PSA, see the following topics:</span></span>

- [<span data-ttu-id="cf7c7-123">Lucrul cu modelul de date Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="cf7c7-123">Working with the Project Service data model</span></span>](reports-working-project-service-data-model.md)
- [<span data-ttu-id="cf7c7-124">Tablouri de bord</span><span class="sxs-lookup"><span data-stu-id="cf7c7-124">Dashboards</span></span>](reports-dashboards.md)

