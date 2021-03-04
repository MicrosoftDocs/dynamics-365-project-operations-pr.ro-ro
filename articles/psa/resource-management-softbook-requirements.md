---
title: Cerințe de rezervare provizorie
description: Acest subiect oferă informații despre modul de creare a rezervărilor provizorii.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: 09f7acb95be014034cc03d7eed9d37363d430601
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147398"
---
# <a name="soft-book-requirements"></a><span data-ttu-id="0ed07-103">Cerințe de rezervare provizorie</span><span class="sxs-lookup"><span data-stu-id="0ed07-103">Soft-book requirements</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="0ed07-104">O cerință de resurse poate fi rezervată ferm.</span><span class="sxs-lookup"><span data-stu-id="0ed07-104">A resource requirement can be hard-booked.</span></span> <span data-ttu-id="0ed07-105">O rezervare fermă creează o propunere care consumă capacitatea unei resurse.</span><span class="sxs-lookup"><span data-stu-id="0ed07-105">A hard booking creates a proposal that consumes a resource's capacity.</span></span> <span data-ttu-id="0ed07-106">Propunerea este apoi trimisă înapoi solicitantului spre aprobare.</span><span class="sxs-lookup"><span data-stu-id="0ed07-106">The proposal is then sent back to the requester for approval.</span></span> <span data-ttu-id="0ed07-107">O rezervare provizorie adaugă temporar o resursă la o echipă de proiect și are o stare diferită în panoul de planificare, dar nu consumă capacitatea resursei.</span><span class="sxs-lookup"><span data-stu-id="0ed07-107">A soft booking tentatively adds a resource to a project team and has a different status on the Schedule Board, but it doesn't consume the resource's capacity.</span></span> <span data-ttu-id="0ed07-108">Pentru a rezerva provizoriu o resursă din tabloul de planificare, setați câmpul **stare rezervare** la **Provizoriu**.</span><span class="sxs-lookup"><span data-stu-id="0ed07-108">To soft-book a resource from the Schedule Board, set the **Booking Status** field to **Soft**.</span></span>

![Starea de rezervare este setată la Provizoriu](media/Resource-Management-image77.png)

<span data-ttu-id="0ed07-110">Când fila **Echipă** este în vizualizarea **Membri denumiți ai echipei**, resursa apare acolo.</span><span class="sxs-lookup"><span data-stu-id="0ed07-110">When the **Team** tab is in the **Named Team Members** view, the resource appears there.</span></span> <span data-ttu-id="0ed07-111">Orele de rezervare provizorie sunt raportate în coloana **Ore rezervate provizoriu**.</span><span class="sxs-lookup"><span data-stu-id="0ed07-111">The soft-booked hours are reported in the **Soft Booked Hours** column.</span></span>

![Orele rezervate provizoriu în vizualizarea membrilor numiți ai echipei](media/Resource-Management-image78.png)

<span data-ttu-id="0ed07-113">Membrii echipei rezervați provizoriu pot fi atribuiți sarcinilor.</span><span class="sxs-lookup"><span data-stu-id="0ed07-113">Soft-booked team members can be assigned to tasks.</span></span>

![Membru al echipei rezervat provizoriu atribuit unei sarcini.](media/Resource-Management-image79.png)

<span data-ttu-id="0ed07-115">În fila **Reconciliere**, nu sunt afișate rezervări pentru o resursă cu rezervare provizorie, deoarece fila **Reconciliere** ia în considerare numai rezervările ferme.</span><span class="sxs-lookup"><span data-stu-id="0ed07-115">On the **Reconciliation** tab, no bookings are shown for a soft-book resource, because the **Reconciliation** tab considers only hard-bookings.</span></span>

![Resursă cu rezervare provizorie fără rezervări în fila reconciliere](media/Resource-Management-image80.png)

> [!NOTE]
> <span data-ttu-id="0ed07-117">Nu se poate rezerva provizoriu o resursă dintr-o cerință care a fost generată de un membru de echipă generic.</span><span class="sxs-lookup"><span data-stu-id="0ed07-117">You can't soft-book a resource from a requirement that was generated from a generic team member.</span></span>

<span data-ttu-id="0ed07-118">În panoul de planificare, este utilizată o colorare diferită pentru rezervările provizorii pentru o resursă.</span><span class="sxs-lookup"><span data-stu-id="0ed07-118">On the Schedule Board, a different coloring is used for soft bookings for a resource.</span></span>

![Rezervare provizorie în panoul de planificare](media/Resource-Management-image81.png)

<span data-ttu-id="0ed07-120">Pentru a converti o rezervare provizorie într-o rezervare fermă, pe panoul de planificare, faceți clic dreapta pe rezervarea provizorie, apoi selectați **Modificare stare** \> **Rezervare fermă** \> **Ferm**.</span><span class="sxs-lookup"><span data-stu-id="0ed07-120">To convert a soft booking to a hard booking, on the Schedule Board, right-click the soft booking, and then select **Change Status** \> **Hard Book** \> **Hard**.</span></span>

![Schimbarea stării rezervării la Ferm](media/Resource-Management-image82.png)

<span data-ttu-id="0ed07-122">Rezervarea este schimbată, iar starea se modifică în panoul de planificare.</span><span class="sxs-lookup"><span data-stu-id="0ed07-122">The booking is changed, and the status is changed on the Schedule Board.</span></span> <span data-ttu-id="0ed07-123">Deoarece starea rezervării este acum **Ferm**, resursa este afișată ca fiind rezervată, iar capacitatea și disponibilitatea acesteia sunt ajustate.</span><span class="sxs-lookup"><span data-stu-id="0ed07-123">Because the booking status is now **Hard**, the resource is shown as booked, and its capacity and availability are adjusted.</span></span>

<span data-ttu-id="0ed07-124">Puteți utiliza aceeași metodă pentru a anula o rezervare fermă sau o rezervare provizorie din panoul de planificare.</span><span class="sxs-lookup"><span data-stu-id="0ed07-124">You can use the same method to cancel a hard booking or a soft booking from the Schedule Board.</span></span>

<span data-ttu-id="0ed07-125">Pentru a converti o resursă care este rezervată provizoriu în rezervată ferm pe fila **Echipă** a proiectului, selectați resursa și apoi selectați **Confirmare**.</span><span class="sxs-lookup"><span data-stu-id="0ed07-125">To convert a resource that is soft-booked to hard-booked on the project's **Team** tab, select the resource, and then select **Confirm**.</span></span>

![Confirmare comandă](media/Resource-Management-image83.png)
