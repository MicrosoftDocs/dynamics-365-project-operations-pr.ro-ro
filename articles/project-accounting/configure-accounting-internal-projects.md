---
title: Configurați contabilitatea pentru proiectele interne
description: Acest subiect oferă informații despre modul de configurare a practicilor contabile pentru proiecte interne în Project Operations.
author: sigitac
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: ad8b974ef75cb0a4e43af0aa254cec1bbcab154a
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012871"
---
# <a name="configure-accounting-for-internal-projects"></a><span data-ttu-id="8547b-103">Configurați contabilitatea pentru proiectele interne</span><span class="sxs-lookup"><span data-stu-id="8547b-103">Configure accounting for internal projects</span></span>

<span data-ttu-id="8547b-104">_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_</span><span class="sxs-lookup"><span data-stu-id="8547b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="8547b-105">Proiectele interne permit companiilor să urmărească costurile legate de activitățile care nu sunt facturate unui client.</span><span class="sxs-lookup"><span data-stu-id="8547b-105">Internal projects allow companies track cost related to activities that aren't being billed to a customer.</span></span> <span data-ttu-id="8547b-106">Exemple de proiecte interne includ:</span><span class="sxs-lookup"><span data-stu-id="8547b-106">Examples of internal projects include:</span></span>

- <span data-ttu-id="8547b-107">Dezvoltarea unui produs, cum ar fi o aplicație mobilă și urmărirea costurilor asociate dezvoltării.</span><span class="sxs-lookup"><span data-stu-id="8547b-107">Developing a product, such as a mobile app, and tracking the cost associated with the development.</span></span>
- <span data-ttu-id="8547b-108">Gestionarea timpului și a cheltuielilor de pre-vânzare.</span><span class="sxs-lookup"><span data-stu-id="8547b-108">Managing pre-sale time and expense.</span></span> <span data-ttu-id="8547b-109">Acest proiect intern de pre-vânzare poate fi transformat ulterior într-un proiect facturabil dacă se câștigă o ofertă.</span><span class="sxs-lookup"><span data-stu-id="8547b-109">This pre-sale internal project can be converted later to a billable project if quote is won.</span></span>

<span data-ttu-id="8547b-110">Orice proiect care nu este asociat cu un contract în Dynamics 365 Project Operations este tratat ca intern.</span><span class="sxs-lookup"><span data-stu-id="8547b-110">Any project not associated with a contract in Dynamics 365 Project Operations is treated as internal.</span></span> <span data-ttu-id="8547b-111">Costul de proiect și profilele de venituri nu sunt folosite pentru a determina regulile de contabilitate pentru proiect.</span><span class="sxs-lookup"><span data-stu-id="8547b-111">Project cost and revenue profiles aren't used to determine accounting rules for the project.</span></span> <span data-ttu-id="8547b-112">Costul intern al proiectului este întotdeauna înregistrat utilizând principiile de profit și pierdere.</span><span class="sxs-lookup"><span data-stu-id="8547b-112">Internal project cost is always posted using profit and loss principles.</span></span> <span data-ttu-id="8547b-113">Conturile contabile pentru înregistrări sunt definite pe pagina **Configurare înregistrare contabilitate**.</span><span class="sxs-lookup"><span data-stu-id="8547b-113">Ledger accounts for postings are defined on the **Ledger posting setup** page.</span></span>

- <span data-ttu-id="8547b-114">Tranzacțiile în timp sunt înregistrate prin debitarea contului **Cost** și prin creditarea contului **Alocarea salarizării**.</span><span class="sxs-lookup"><span data-stu-id="8547b-114">Time transactions are posted by debiting the **Cost** account and crediting the **Payroll allocation** account.</span></span>
- <span data-ttu-id="8547b-115">Tranzacțiile de cheltuieli sunt înregistrate prin debitarea contului **Cost** și prin creditarea **Cont compensat pentru cheltuieli**.</span><span class="sxs-lookup"><span data-stu-id="8547b-115">Expense transactions are posted by debiting the **Cost** account and crediting the **Offset account for expense**.</span></span>
- <span data-ttu-id="8547b-116">Tranzacțiile articolelor sunt postate prin debitarea contului **Cost** și creditarea contului **Cost - Articol**.</span><span class="sxs-lookup"><span data-stu-id="8547b-116">Item transactions are posted by debiting the **Cost** account and crediting the **Cost - Item** account.</span></span>

<span data-ttu-id="8547b-117">După ce tranzacțiile sunt înregistrate în proiect, dacă proiectul este asociat cu un contract de proiect, sistemul anulează toate tranzacțiile acumulate și creează noi tranzacții facturabile.</span><span class="sxs-lookup"><span data-stu-id="8547b-117">After transactions are posted to the project, if the project is associated with a project contract, the system reverses all accumulated transactions and creates new billable transactions.</span></span> <span data-ttu-id="8547b-118">Tranzacțiile facturabile respectă regulile contabile definite în costul proiectului respectiv și în profilul de venituri.</span><span class="sxs-lookup"><span data-stu-id="8547b-118">The billable transactions follow the accounting rules defined in respective Project cost and revenue profile.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]
