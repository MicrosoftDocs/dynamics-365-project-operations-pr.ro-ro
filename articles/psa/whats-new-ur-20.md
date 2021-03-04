---
title: Ce este nou sau schimbat în Project Service Automation versiunea actualizată 20, V3
description: Acest subiect listează caracteristicile și corecțiile care sunt disponibile în Project Service Automation V3, versiunea actualizată 20, V3
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 06/12/2020
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
ms.openlocfilehash: ee3be43da401af405ab329b9b5a724a2e95c0219
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147128"
---
# <a name="project-service-automation-update-release-20-v3"></a><span data-ttu-id="000ca-103">Project Service Automation, versiunea actualizată 20, V3</span><span class="sxs-lookup"><span data-stu-id="000ca-103">Project Service Automation Update Release 20, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="000ca-104">Suntem încântați să anunțăm cea mai recentă actualizare pentru aplicația Project Service Automation pentru Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="000ca-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="000ca-105">Această versiune include câteva îmbunătățiri importante ale calității, performanței și utilizabilității.</span><span class="sxs-lookup"><span data-stu-id="000ca-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="000ca-106">Această versiune este compatibilă cu Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="000ca-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="000ca-107">Pentru a actualiza această versiune, accesați Centrul de administrare pentru Dynamics 365, pagina de soluții online pentru a instala actualizarea.</span><span class="sxs-lookup"><span data-stu-id="000ca-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="000ca-108">Pentru informații suplimentare, consultați: [Instalarea, actualizarea sau eliminarea unei soluții preferate](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="000ca-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="000ca-109">Acest subiect listează caracteristicile și corecțiile care sunt noi sau modificate pentru Project Service Automation V3, versiunea actualizată 20.</span><span class="sxs-lookup"><span data-stu-id="000ca-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 20.</span></span> <span data-ttu-id="000ca-110">Această versiune are un număr de versiune V 3.10.31.37 și este disponibil în general printr-o autoactualizare în iunie 2020.</span><span class="sxs-lookup"><span data-stu-id="000ca-110">This version has a build number of V 3.10.31.37 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-20"></a><span data-ttu-id="000ca-111">Lansarea de actualizări 20</span><span class="sxs-lookup"><span data-stu-id="000ca-111">Update Release 20</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="000ca-112">Remedieri de erori</span><span class="sxs-lookup"><span data-stu-id="000ca-112">Bug fixes</span></span>

<span data-ttu-id="000ca-113">**Gestionare de proiect**</span><span class="sxs-lookup"><span data-stu-id="000ca-113">**Project Management**</span></span>

<span data-ttu-id="000ca-114">S-au remediat următoarele probleme:</span><span class="sxs-lookup"><span data-stu-id="000ca-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="000ca-115">Importarea membrilor echipei de proiect cu o metodă de alocare care necesită ore are ca rezultat un mesaj de eroare neclar atunci când orele specificate sunt zero.</span><span class="sxs-lookup"><span data-stu-id="000ca-115">Importing project team members with an allocation method that requires hours results in an unclear error message when the specified hours are zero.</span></span>
- <span data-ttu-id="000ca-116">Utilizatorii primesc o eroare incorectă atunci când numărul maxim de caractere a fost introdus în câmpul **Descriere** pentru o sarcină de proiect.</span><span class="sxs-lookup"><span data-stu-id="000ca-116">Users receive an incorrect error when the maximum number of characters have been entered into the **Description** field for a project task.</span></span>
- <span data-ttu-id="000ca-117">Pagina **Microsoft Dynamics 365 Project Service Automation descărcare program de completare** redirecționează către pagina de descărcare în engleză atunci când setările de limbă ale utilizatorului sunt setate pe japoneză.</span><span class="sxs-lookup"><span data-stu-id="000ca-117">The **Microsoft Dynamics 365 Project Service Automation add-in download** page redirects to the English download page when the user’s language settings are set to Japanese.</span></span>
- <span data-ttu-id="000ca-118">Când apare o eroare de server, eticheta de sincronizare de pe fila **Planificare** din formularul **Proiecte** rămâne uneori.</span><span class="sxs-lookup"><span data-stu-id="000ca-118">When a server error occurs, the synchronization label on the **Schedule** tab of the **Projects** form sometimes remains.</span></span>
- <span data-ttu-id="000ca-119">Actualizările de sarcini redundante sunt trimise serverului atunci când o sarcină este modificată.</span><span class="sxs-lookup"><span data-stu-id="000ca-119">Redundant task updates are being sent to the server when a task is modified.</span></span>

<span data-ttu-id="000ca-120">**Sales**</span><span class="sxs-lookup"><span data-stu-id="000ca-120">**Sales**</span></span>

<span data-ttu-id="000ca-121">S-au remediat următoarele probleme:</span><span class="sxs-lookup"><span data-stu-id="000ca-121">The following issues have been fixed:</span></span>

- <span data-ttu-id="000ca-122">Pe formularul **Contract**, dublul clic pe **Creați factură** creează două facturi pentru o singură înregistrare de date reale.</span><span class="sxs-lookup"><span data-stu-id="000ca-122">On the **Contract** form, double-clicking **Create Invoice** creates two invoices for a single actuals record.</span></span>
- <span data-ttu-id="000ca-123">În Internet Explorer 11, utilizatorii nu pot crea intrări de cheltuieli.</span><span class="sxs-lookup"><span data-stu-id="000ca-123">In Internet Explorer 11, users are unable to create expense entries.</span></span>
- <span data-ttu-id="000ca-124">Inversarea costurilor și inversarea Cifrelor reale din vânzările nefacturate nu sunt legate.</span><span class="sxs-lookup"><span data-stu-id="000ca-124">Reversal of Cost and reversal of Unbilled Sales Actuals are not linked.</span></span>
- <span data-ttu-id="000ca-125">Butonul **Reîmprospătați valorile reale** de pe formularul **Proiect** nu reîmprospătează **Activitate ore efective**.</span><span class="sxs-lookup"><span data-stu-id="000ca-125">The **Refresh Actuals** button on the **Project** form does not refresh **Task Actual Hours**.</span></span>
- <span data-ttu-id="000ca-126">Insertul **PreValidateProjectTeamMemberCreate** poate crea resurse generice duplicate care se pot rezerva când atributul **msdyn_isgenericresourceprojectscoped** este setat la **Fals**.</span><span class="sxs-lookup"><span data-stu-id="000ca-126">The **PreValidateProjectTeamMemberCreate** plug-in can create duplicate generic bookable resources when the attribute **msdyn_isgenericresourceprojectscoped** is set to **False**.</span></span>
- <span data-ttu-id="000ca-127">**Recalcularea** șterge costurile exigibile pentru detaliile liniei de ofertă bazate pe produse și detaliile liniei contractului.</span><span class="sxs-lookup"><span data-stu-id="000ca-127">**Recalculate** clears chargeable costs of product-based quote line details and contract line details.</span></span>
- <span data-ttu-id="000ca-128">În scenarii specifice, insertul **PostEstimateLineUpdate** afișează o eroare de excepție nulă.</span><span class="sxs-lookup"><span data-stu-id="000ca-128">In specific scenarios, the **PostEstimateLineUpdate** plug-in displays a null teference exception error.</span></span>
- <span data-ttu-id="000ca-129">Durata fazei de timp pe **Graficul analizei rentabilității** nu se potrivește cu durata costurilor din detaliul liniei de ofertă la preț fix.</span><span class="sxs-lookup"><span data-stu-id="000ca-129">Time phase duration on the **Profitability Analysis Chart** does not match duration of the costs in the fixed-price quote line detail of the quote.</span></span>
- <span data-ttu-id="000ca-130">Valorile grupului unitar și ale unităților nu implicit corect pentru categoriile de cheltuieli din **Detalii linie contract** și formulare **Detalii despre linie de ofertă**.</span><span class="sxs-lookup"><span data-stu-id="000ca-130">Unit and unit group values do not default correctly for expense categories on the **Contract Line Details** and **Quote Line Details** forms.</span></span>
- <span data-ttu-id="000ca-131">Listele **Preț cost unitate organizațională** permit suprapunerea efectivității datei.</span><span class="sxs-lookup"><span data-stu-id="000ca-131">**Org Unit Cost Price** lists permit overlaps in the date effectivity.</span></span>
- <span data-ttu-id="000ca-132">Utilizatorii nu au voie să schimbe **OrgUnit** când tipul de comandă nu este bazat pe lucru, deoarece va duce la o eroare nulă de excepție de referință.</span><span class="sxs-lookup"><span data-stu-id="000ca-132">Users are not permitted to change the **OrgUnit** when the order type is not work-based because it will lead to a null reference exception error.</span></span>
- <span data-ttu-id="000ca-133">Când încercați să navigați din formularul **Detalii despre linie de ofertă**, înapoi la fila **Oferta**, formularul reîmprospătează și afișează fila **Rezumat**.</span><span class="sxs-lookup"><span data-stu-id="000ca-133">When attempting to navigate from the **Quote Line Details** form, back to the **Quote** tab, the form refreshes and displays the **Summary** tab.</span></span>
