---
title: Procese vânzări
description: Acest subiect oferă informații despre procesele de vânzări de bază.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: a169dee5-f4a7-42c8-9bf1-7f0018cc25cb
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: eaaa4b8fe6577ff572489ac0c6abac3c4e970c63
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754759"
---
# <a name="sales-processes"></a><span data-ttu-id="30df4-103">Procese vânzări</span><span class="sxs-lookup"><span data-stu-id="30df4-103">Sales processes</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="30df4-104">Procesele de vânzări care sunt utilizate într-o organizație bazată pe proiecte diferă de procesele de vânzări care sunt utilizate într-o organizație bazată pe produse.</span><span class="sxs-lookup"><span data-stu-id="30df4-104">The sales processes that are used in a project-based organization differ from the sales processes that are used in a product-based organization.</span></span> <span data-ttu-id="30df4-105">Această diferență apare deoarece ciclurile de vânzări pentru organizațiile bazate pe proiecte sunt mai lungi și necesită tehnici de estimare particularizate pentru a analiza și a crea oferte pentru fiecare tranzacție.</span><span class="sxs-lookup"><span data-stu-id="30df4-105">This difference occurs because the sales cycles for project-based organizations are longer and require customized estimation techniques to analyze and create quotes for each deal.</span></span> <span data-ttu-id="30df4-106">Dynamics 365 Project Service Automation utilizează o parte din aceeași funcționalitate care este utilizată în procesul de vânzări pentru Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="30df4-106">Dynamics 365 Project Service Automation uses some of the same functionality that is used in the sales process for Dynamics 365 Sales.</span></span> <span data-ttu-id="30df4-107">Iată câteva exemple:</span><span class="sxs-lookup"><span data-stu-id="30df4-107">Here are some examples:</span></span>

- <span data-ttu-id="30df4-108">O entitate Client potențial este utilizată pentru a urmări procesul de vânzări.</span><span class="sxs-lookup"><span data-stu-id="30df4-108">A Lead entity is used to track the sales process.</span></span>
- <span data-ttu-id="30df4-109">Clienții potențiali care se califică sunt urmăriți ca oportunități.</span><span class="sxs-lookup"><span data-stu-id="30df4-109">Qualifying leads are tracked as opportunities.</span></span> <span data-ttu-id="30df4-110">Procesul de vânzări poate începe, de asemenea, cu oportunitatea.</span><span class="sxs-lookup"><span data-stu-id="30df4-110">The sales process can also start with opportunity.</span></span>
- <span data-ttu-id="30df4-111">Toate artefactele corelate pentru o oportunitate sunt accesate.</span><span class="sxs-lookup"><span data-stu-id="30df4-111">All related artifacts for an opportunity are accessed.</span></span> <span data-ttu-id="30df4-112">Aceste artefacte includ echipa de vânzări, participanții direct interesați, probabilitatea, evaluarea, etapele vânzărilor și procesele de afaceri.</span><span class="sxs-lookup"><span data-stu-id="30df4-112">These artifacts include the sales team, stakeholders, probability, rating, sales stages, and business processes.</span></span>
- <span data-ttu-id="30df4-113">Mai multe oferte sunt create pentru o oportunitate.</span><span class="sxs-lookup"><span data-stu-id="30df4-113">Multiple quotes are created for an opportunity.</span></span>
- <span data-ttu-id="30df4-114">O ofertă este marcată ca **Închisă drept câștigată** pentru a crea o comandă de vânzări.</span><span class="sxs-lookup"><span data-stu-id="30df4-114">A quote is marked **Closed as Won** to create a sales order.</span></span> <span data-ttu-id="30df4-115">În PSA, comanda de vânzări este particularizată și se numește contract de proiect.</span><span class="sxs-lookup"><span data-stu-id="30df4-115">In PSA, the sales order is customized and is called a project contract.</span></span>

<span data-ttu-id="30df4-116">Următoarea ilustrație arată un proces tipic de vânzări într-o organizație bazată pe proiecte.</span><span class="sxs-lookup"><span data-stu-id="30df4-116">The following illustration shows a typical sales process in a project-based organization.</span></span>

> ![Procesul de vânzări într-o organizație bazată pe proiecte](media/basic-guide-1.png)

## <a name="estimating-a-sale"></a><span data-ttu-id="30df4-118">Estimarea unei vânzări</span><span class="sxs-lookup"><span data-stu-id="30df4-118">Estimating a sale</span></span>
<span data-ttu-id="30df4-119">Valoarea unei vânzări poate fi estimată pe baza proiectelor care au fost livrate anterior și a complexității proiectelor.</span><span class="sxs-lookup"><span data-stu-id="30df4-119">The value of a sale can be estimated based on projects that have previously been delivered and the complexity of projects.</span></span> <span data-ttu-id="30df4-120">Pentru proiectele care implică extensii la proiecte anterioare sau proiectele în care expertiza furnizorului este mare și sunt utilizate șabloane de lucru bine cunoscute, puteți utiliza un proces de estimare mai simplu.</span><span class="sxs-lookup"><span data-stu-id="30df4-120">For projects that involve extensions to previous projects, or projects where the vendor's expertise is high and well-known work templates are used, you can use a simpler estimation process.</span></span> <span data-ttu-id="30df4-121">Proiectele mai complexe au de obicei un proces de achiziție mai lung.</span><span class="sxs-lookup"><span data-stu-id="30df4-121">More complex projects usually have a longer purchase process.</span></span> <span data-ttu-id="30df4-122">Prin urmare, există mai multe etape în procesul de estimare a vânzărilor.</span><span class="sxs-lookup"><span data-stu-id="30df4-122">Therefore, there are more stages in the sales estimation process.</span></span> <span data-ttu-id="30df4-123">La începutul procesului, echipa de vânzări utilizează contribuția administratorilor de cont și a experților în materie (EM) pentru a începe să creeze o estimare la nivel înalt pentru fiecare componentă distinctă a lucrărilor care este ofertată.</span><span class="sxs-lookup"><span data-stu-id="30df4-123">Early in the process, the sales team uses the input of account managers and subject matter experts (SMEs) to start to create a high-level estimate for each distinct component of work that is quoted.</span></span> <span data-ttu-id="30df4-124">Aceste componente ale lucrărilor sunt reprezentate prin linii de ofertă.</span><span class="sxs-lookup"><span data-stu-id="30df4-124">These components of work are represented by quote lines.</span></span> 

<span data-ttu-id="30df4-125">Aveți posibilitatea să creați o estimare la nivel înalt a ofertei.</span><span class="sxs-lookup"><span data-stu-id="30df4-125">You can create a high-level estimate of the quote.</span></span> <span data-ttu-id="30df4-126">În cele din urmă, această estimare la nivel înalt va fi înlocuită cu o estimare mai detaliată care se bazează pe un plan de proiect pe care îl creați utilizând șabloanele de proiect standardizate.</span><span class="sxs-lookup"><span data-stu-id="30df4-126">Eventually, this high-level estimate will be replaced by a more detailed estimate that is based on a project plan that you create by using the standardized project templates.</span></span> <span data-ttu-id="30df4-127">Aceste șabloane vă ajută să construiți o planificare și să determinați valorile monetare pe ofertă și pe componentele sale (linii de ofertă).</span><span class="sxs-lookup"><span data-stu-id="30df4-127">These templates help you build a schedule and determine monetary values on the quote and its components (quote lines).</span></span> 

<span data-ttu-id="30df4-128">Aveți posibilitatea să creați mai multe oferte pentru un proiect și să le grupați sub un singur tip de entitate oportunitate.</span><span class="sxs-lookup"><span data-stu-id="30df4-128">You can create multiple quotes for a project and group them under a single opportunity entity type.</span></span> <span data-ttu-id="30df4-129">În cele din urmă, una dintre aceste oferte este marcată ca **Închisă drept câștigată** și se creează un contract de proiect sau o specificație de lucru (SL).</span><span class="sxs-lookup"><span data-stu-id="30df4-129">Eventually, one of those quotes is marked **Closed as Won**, and a project contract or statement of work (SOW) is created.</span></span> <span data-ttu-id="30df4-130">Un contract de proiect deține valoarea contractată pentru fiecare componentă (linie de contract) care este acceptată de client pentru livrare.</span><span class="sxs-lookup"><span data-stu-id="30df4-130">A project contract holds the contracted value for each component (contract line) that is accepted by the customer for delivery.</span></span> <span data-ttu-id="30df4-131">O SL este de obicei creată ca document Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="30df4-131">An SOW is usually created as a Microsoft Word document.</span></span> <span data-ttu-id="30df4-132">Toate facturile trimise clientului pe parcursul livrării proiectului fac referire la contractul de proiect sau la SL.</span><span class="sxs-lookup"><span data-stu-id="30df4-132">All invoices that are sent to the customer over the course of the project's delivery reference the project contract or SOW.</span></span>

<span data-ttu-id="30df4-133">De asemenea, aveți posibilitatea să creați oferte alternative sub un tip de entitate oportunitate sau să configurați sistemul astfel încât să se creeze un contract de proiect atunci când se câștigă o ofertă.</span><span class="sxs-lookup"><span data-stu-id="30df4-133">You can also create alternate quotes under one opportunity entity type or set up the system so that a project contract is created when a quote is won.</span></span> <span data-ttu-id="30df4-134">În acest caz, aveți posibilitatea să atașați un document Word care reprezintă SL la înregistrarea de contract de proiect.</span><span class="sxs-lookup"><span data-stu-id="30df4-134">In this case, you can attach a Word document that represents the SOW to the project contract record.</span></span>

![Închiderea unei oferte pentru a crea un contract de proiect](media/basic-guide-2.png)

## <a name="configuring-the-sales-process"></a><span data-ttu-id="30df4-136">Configurarea procesului de vânzări</span><span class="sxs-lookup"><span data-stu-id="30df4-136">Configuring the sales process</span></span>
<span data-ttu-id="30df4-137">Aveți posibilitatea să utilizați fluxurile de business (FB) în Microsoft Dynamics 365 pentru a configura procesul de vânzări.</span><span class="sxs-lookup"><span data-stu-id="30df4-137">You can use business process flows (BPFs) in Microsoft Dynamics 365 to configure your sales process.</span></span> <span data-ttu-id="30df4-138">FB-urile oferă personalului dvs. de vânzări o interfață vizuală ghidată pe care acesta o poate folosi pentru a face tranzacțiile să avanseze prin etapele care sunt tipice pentru compania dvs.</span><span class="sxs-lookup"><span data-stu-id="30df4-138">BPFs give your sales staff a guided visual interface that they can use to move deals forward through the stages that are typical for your company.</span></span>

<span data-ttu-id="30df4-139">De exemplu, compania dvs. poate avea următoarele șase etape în procesul de vânzări:</span><span class="sxs-lookup"><span data-stu-id="30df4-139">For example, your company might have the following six stages in the sales process:</span></span>

1. <span data-ttu-id="30df4-140">Calificare</span><span class="sxs-lookup"><span data-stu-id="30df4-140">Qualify</span></span>
2. <span data-ttu-id="30df4-141">Estimat</span><span class="sxs-lookup"><span data-stu-id="30df4-141">Estimate</span></span>
3. <span data-ttu-id="30df4-142">Recenzie internă</span><span class="sxs-lookup"><span data-stu-id="30df4-142">Internal review</span></span>
4. <span data-ttu-id="30df4-143">Contract</span><span class="sxs-lookup"><span data-stu-id="30df4-143">Contract</span></span>
5. <span data-ttu-id="30df4-144">Livrare</span><span class="sxs-lookup"><span data-stu-id="30df4-144">Deliver</span></span>
6. <span data-ttu-id="30df4-145">Închidere</span><span class="sxs-lookup"><span data-stu-id="30df4-145">Close</span></span>

<span data-ttu-id="30df4-146">Aceste șase etape sunt reprezentate de ghilimelele unghiulare (\>) pe care le selectați pentru a extinde în fiecare oportunitate tipul de entitate pe care îl creați.</span><span class="sxs-lookup"><span data-stu-id="30df4-146">These six stages are represented by chevrons (\>) that you select to expand in each opportunity entity type that you create.</span></span>

![Configurarea proceselor comerciale în Dynamics 365](media/basic-guide-3.png)
 
<span data-ttu-id="30df4-148">Organizația dvs. poate utiliza entități diferite pentru a reprezenta aceeași tranzacție, pe măsură ce aceasta evoluează.</span><span class="sxs-lookup"><span data-stu-id="30df4-148">Your organization might use different entities to represent the same deal as it evolves.</span></span> <span data-ttu-id="30df4-149">La începutul procesului de vânzări, o tranzacție este reprezentată de entitatea Oportunitate.</span><span class="sxs-lookup"><span data-stu-id="30df4-149">Early in the sales process, a deal is represented by the Opportunity entity.</span></span> <span data-ttu-id="30df4-150">Pe măsură ce trece timpul și apar mai multe detalii, este posibil să utilizați estimări de nivel înalt pentru a crea una sau mai multe oferte.</span><span class="sxs-lookup"><span data-stu-id="30df4-150">As time passes and more details emerge, you might use high-level estimates to create one or more quotes.</span></span> <span data-ttu-id="30df4-151">Dacă una dintre aceste oferte este revizuită de către participanții direct interesați interni și ai clienților, entitatea Ofertă reprezintă tranzacția.</span><span class="sxs-lookup"><span data-stu-id="30df4-151">If one of these quotes is reviewed by internal and customer stakeholders, the Quote entity represents the deal.</span></span> <span data-ttu-id="30df4-152">După ce clientul acceptă oferta, un contract de proiect sau o SL reprezintă tranzacția.</span><span class="sxs-lookup"><span data-stu-id="30df4-152">After the customer accepts the quote, a project contract or SOW represents the deal.</span></span> <span data-ttu-id="30df4-153">Pentru a sprijini acest comportament, FB-urile sunt structurate astfel încât fiecare etapă din proces este legată la un tabel de baze de date diferit.</span><span class="sxs-lookup"><span data-stu-id="30df4-153">To support this behavior, BPFs are structured so that each stage in the process is linked to a different database table.</span></span>

<span data-ttu-id="30df4-154">Etapa **Calificare** din procesul de vânzări poate fi susținută de o entitate Oportunitate.</span><span class="sxs-lookup"><span data-stu-id="30df4-154">The **Qualify** stage in the sales process can be backed by an Opportunity entity.</span></span> <span data-ttu-id="30df4-155">Etapele **Estimare** și **Recenzie internă** pot fi susținute de o entitate Ofertă.</span><span class="sxs-lookup"><span data-stu-id="30df4-155">The **Estimate** and **Internal Review** stages can be backed by a Quote entity.</span></span> <span data-ttu-id="30df4-156">Etapele **Contract**, **Livrare** și **Închidere** pot fi susținute de o entitate Contract de proiect.</span><span class="sxs-lookup"><span data-stu-id="30df4-156">The **Contract**, **Delivery**, and **Close** stages can be backed by a Project Contract entity.</span></span>

<span data-ttu-id="30df4-157">Pe măsură ce faceți tranzacțiile să avanseze prin etape, vi se solicită să creați înregistrarea de entitate corespunzătoare pentru a vă ajuta și ghida prin proces.</span><span class="sxs-lookup"><span data-stu-id="30df4-157">As you move deals through the stages, you're prompted to create the appropriate entity record to help and guide you through the process.</span></span> <span data-ttu-id="30df4-158">Etapele pot fi condiționate.</span><span class="sxs-lookup"><span data-stu-id="30df4-158">The stages can be conditional.</span></span> <span data-ttu-id="30df4-159">De exemplu, dacă aveți nevoie de o revizuire internă a unei oferte numai dacă oferta utilizează o listă de prețuri particularizată, aveți posibilitatea să configurați această condiție în stadiul corespunzător al procesului de afaceri.</span><span class="sxs-lookup"><span data-stu-id="30df4-159">For example, if you require an internal review of a quote only if the quote uses a custom price list, you can configure that condition in the appropriate stage of the business process.</span></span> <span data-ttu-id="30df4-160">Etapa **Recenzie internă** este apoi afișată numai pentru ofertele care utilizează o listă de prețuri personalizată.</span><span class="sxs-lookup"><span data-stu-id="30df4-160">The **Internal Review** stage is then shown only for quotes that use a custom price list.</span></span> <span data-ttu-id="30df4-161">Pentru toate celelalte tranzacții și oferte, etapa **Estimare** este urmată de etapa **Contract**.</span><span class="sxs-lookup"><span data-stu-id="30df4-161">For all other deals and quotes, the **Estimate** stage is followed by the **Contract** stage.</span></span>

> [!NOTE]
> <span data-ttu-id="30df4-162">PSA are anumite pagini pentru entitățile Oportunitate, Ofertă, Comandă și Factură.</span><span class="sxs-lookup"><span data-stu-id="30df4-162">PSA has specific pages for the Opportunity, Quote, Order, and Invoice entities.</span></span> <span data-ttu-id="30df4-163">Trebuie să creați oportunități de servicii de proiecte, oferte, comenzi și facturi utilizând paginile de informații ale proiectului pentru aceste entități.</span><span class="sxs-lookup"><span data-stu-id="30df4-163">You must create project service opportunities, quotes, orders, and invoices using the project information pages for these entities.</span></span> <span data-ttu-id="30df4-164">Dacă utilizați o altă pagină pentru a crea o înregistrare, nu veți putea deschide înregistrarea din pagina **Informații proiect**.</span><span class="sxs-lookup"><span data-stu-id="30df4-164">If you use another page to create a record, you won't be able to open the record from the **Project Information** page.</span></span> <span data-ttu-id="30df4-165">Dacă doriți să deschideți o înregistrare din pagina **Informații proiect**, trebuie să ștergeți înregistrarea și să o recreați utilizând pagina **Informații proiect**.</span><span class="sxs-lookup"><span data-stu-id="30df4-165">If you want to open a record from the **Project Information** page, you must delete the record and recreate it using the **Project Information** page.</span></span> <span data-ttu-id="30df4-166">În pagina **Informații proiect**, logica de business pentru fiecare dintre aceste tipuri de entități asigură faptul că câmpul **Tip** al înregistrării este setat corect și toate conceptele obligatorii sunt inițializate corect.</span><span class="sxs-lookup"><span data-stu-id="30df4-166">On the **Project Information** page, business logic for each of these entity types ensures that the **Type** field of the record is set correctly, and all of the mandatory concepts are properly initialized.</span></span>

> ![Informații despre proiect pentru o nouă comandă](media/basic-guide-4.png)
 
## <a name="differences-between-project-service-automation-and-sales"></a><span data-ttu-id="30df4-168">Diferențele dintre Project Service Automation și Sales</span><span class="sxs-lookup"><span data-stu-id="30df4-168">Differences between Project Service Automation and Sales</span></span>
<span data-ttu-id="30df4-169">Deși procesul de vânzări în PSA utilizează capacitățile de bază ale procesului de vânzări din Sales, acesta prezintă unele diferențe cheie din cauza variațiilor în practicile de afaceri ale organizațiilor bazate pe proiecte.</span><span class="sxs-lookup"><span data-stu-id="30df4-169">Although the sales process in PSA uses the basic capabilities of the sales process in Sales, it does have some key differences because of variations in the business practices of project-based organizations.</span></span> <span data-ttu-id="30df4-170">Iată câteva exemple:</span><span class="sxs-lookup"><span data-stu-id="30df4-170">Here are some examples:</span></span>

- <span data-ttu-id="30df4-171">**Oferte proiect** – în Project Service Automation, o ofertă este închisă după ce un contract de proiect este creat dintr-o ofertă.</span><span class="sxs-lookup"><span data-stu-id="30df4-171">**Project quotes** – In Project Service Automation, a quote is closed after a project contract is created from a quote.</span></span> <span data-ttu-id="30df4-172">În Sales, puteți să păstrați o ofertă deschisă după ce ați câștigat-o.</span><span class="sxs-lookup"><span data-stu-id="30df4-172">In Sales, you can keep a quote open after you've won it.</span></span> <span data-ttu-id="30df4-173">Motivul pentru această diferență este că o potrivire între o ofertă și un contract de proiect este mai bună pentru organizațiile bazate pe proiecte.</span><span class="sxs-lookup"><span data-stu-id="30df4-173">The reason for this difference is that a match between a quote and a project contract is better for project-based organizations.</span></span> 
- <span data-ttu-id="30df4-174">**Activarea și revizuirile** – în PSA, activarea și revizuirile nu sunt acceptate pentru ofertele de proiect.</span><span class="sxs-lookup"><span data-stu-id="30df4-174">**Activation and revisions** – In PSA, activation and revisions aren't supported for project quotes.</span></span> <span data-ttu-id="30df4-175">În Sales, o ofertă poate fi blocată pentru a preveni editările suplimentare.</span><span class="sxs-lookup"><span data-stu-id="30df4-175">In Sales, a quote can be locked to prevent additional edits.</span></span>
- <span data-ttu-id="30df4-176">**Închiderea unei oferte ca pierdută sau câștigată** – în PSA, când o ofertă de proiect este închisă ca câștigată sau pierdută, oportunitatea rămâne deschisă.</span><span class="sxs-lookup"><span data-stu-id="30df4-176">**Closing a quote as lost or won** – In PSA, when a project quote is closed as won or lost, the opportunity remains open.</span></span> <span data-ttu-id="30df4-177">Toate celelalte oferte din oportunitate sunt închise ca pierdute.</span><span class="sxs-lookup"><span data-stu-id="30df4-177">All other quotes on the opportunity are closed as lost.</span></span> <span data-ttu-id="30df4-178">În Sales, când o ofertă este închisă ca câștigată sau pierdută, utilizatorului i se solicită să ia o măsură cu privire la oportunitate.</span><span class="sxs-lookup"><span data-stu-id="30df4-178">In Sales, when a quote is closed as won or lost, the user is prompted to take an action on the opportunity.</span></span> <span data-ttu-id="30df4-179">În funcție de contribuția utilizatorului, oportunitatea de bază poate fi închisă sau lăsată deschisă.</span><span class="sxs-lookup"><span data-stu-id="30df4-179">Depending on the user input, the underlying opportunity might be closed or left open.</span></span>

## <a name="tracking-revisions-to-quotes-and-project-plans-in-the-sales-cycle"></a><span data-ttu-id="30df4-180">Urmărirea revizuirilor la oferte și planuri de proiect în ciclul de vânzări</span><span class="sxs-lookup"><span data-stu-id="30df4-180">Tracking revisions to quotes and project plans in the sales cycle</span></span>
<span data-ttu-id="30df4-181">În PSA, nu puteți urmări revizuirile care sunt făcute la o ofertă.</span><span class="sxs-lookup"><span data-stu-id="30df4-181">In PSA, you can't track revisions that are made to a quote.</span></span> <span data-ttu-id="30df4-182">În schimb, trebuie să marcați oferta existentă ca **Închisă drept pierdută** și apoi să creați o ofertă nouă.</span><span class="sxs-lookup"><span data-stu-id="30df4-182">Instead, you must mark the existing quote **Closed as Lost** and then create a new quote.</span></span> <span data-ttu-id="30df4-183">Aveți posibilitatea să copiați o ofertă sau să clonați o ofertă bazată pe proiect utilizând PSA.</span><span class="sxs-lookup"><span data-stu-id="30df4-183">You can copy a quote or clone a project-based quote by using PSA.</span></span>

## <a name="tracking-comments-and-approvals-of-quotes-and-project-contracts"></a><span data-ttu-id="30df4-184">Urmărirea comentariilor și aprobărilor de oferte și contracte de proiect</span><span class="sxs-lookup"><span data-stu-id="30df4-184">Tracking comments and approvals of quotes and project contracts</span></span>
<span data-ttu-id="30df4-185">Puteți gestiona revizuirea și aprobarea ofertelor și a contractelor de proiect utilizând peretele de înregistrări și postările.</span><span class="sxs-lookup"><span data-stu-id="30df4-185">You can manage the review and approval of quotes and project contracts by using the record wall and posts.</span></span> <span data-ttu-id="30df4-186">Organizația dvs. poate crea fluxuri de lucru și inserturi particularizate pentru a atribui, redirecționa, escalada și gestiona notificările de elemente de lucru de revizuire și aprobare.</span><span class="sxs-lookup"><span data-stu-id="30df4-186">Your organization can create custom workflows and plug-ins to assign, redirect, escalate, and manage notifications of review and approval work items.</span></span>