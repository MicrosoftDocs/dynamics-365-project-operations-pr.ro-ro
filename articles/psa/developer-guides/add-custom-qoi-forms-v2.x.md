---
title: Adăugarea de noi formulare de entități particularizate (Project Service Automation 2. x)
description: Acest subiect furnizează informații despre cum se adaugă formulare de entități particularizate pentru oportunități, oferte, comenzi sau facturi în Dynamics 365 Project Service Automation 2.x.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 3/14/2019
ms.topic: article
ms.service: business-applications
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 57d4b9aad433af6d3e73369c76f2793f349c6965
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082990"
---
# <a name="add-new-custom-entity-forms-project-service-automation-2x"></a><span data-ttu-id="20ea0-103">Adăugarea de noi formulare de entități particularizate (Project Service Automation 2. x)</span><span class="sxs-lookup"><span data-stu-id="20ea0-103">Add new custom entity forms (Project Service Automation 2.x)</span></span>

## <a name="type-field"></a><span data-ttu-id="20ea0-104">Tip de câmp</span><span class="sxs-lookup"><span data-stu-id="20ea0-104">Type field</span></span> 

<span data-ttu-id="20ea0-105">Dynamics 365 Project Service Automation se bazează pe câmpul **Tip** ( **msdyn\_tipcomandă** ) al entităților Oportunitate, Ofertă, Comandă și Factură pentru a distinge versiunile **bazate pe activități** ale acestor entități de versiunile **bazate pe articole** și **bazate pe servicii**.</span><span class="sxs-lookup"><span data-stu-id="20ea0-105">Dynamics 365 Project Service Automation relies on the **Type** ( **msdyn\_ordertype** ) field of the Opportunity, Quote, Order, and Invoice entities to distinguish **work-based** versions of these entities from **item-based** and **service-based** versions.</span></span> <span data-ttu-id="20ea0-106">Versiunile bazate pe activități ale acestor entități sunt gestionate de PSA.</span><span class="sxs-lookup"><span data-stu-id="20ea0-106">Work-based versions of these entities are handled by PSA.</span></span> <span data-ttu-id="20ea0-107">O mare parte din logica de afaceri pe partea de client și pe partea de server a soluției depinde de câmpul **Tip**.</span><span class="sxs-lookup"><span data-stu-id="20ea0-107">Lots of business logic on the client side and server side of the solution depends on the **Type** field.</span></span> <span data-ttu-id="20ea0-108">De aceea, este important ca câmpul să fie inițializat cu o valoare corectă atunci când entitățile sunt create.</span><span class="sxs-lookup"><span data-stu-id="20ea0-108">Therefore, it's important that the field be initialized with a correct value when the entities are created.</span></span> <span data-ttu-id="20ea0-109">O valoare incorectă poate provoca comportamente incorecte și o parte din logica de afaceri ar putea să nu ruleze corect.</span><span class="sxs-lookup"><span data-stu-id="20ea0-109">An incorrect value can cause incorrect behaviors, and some business logic might not run correctly.</span></span>

## <a name="automatic-form-switching"></a><span data-ttu-id="20ea0-110">Comutare automată a formularului</span><span class="sxs-lookup"><span data-stu-id="20ea0-110">Automatic form switching</span></span>

<span data-ttu-id="20ea0-111">Pentru a evita deteriorarea potențială a datelor și comportamente neașteptate care sunt provocate de inițializarea incorectă și editarea înregistrărilor entității de vânzări, PSA include acum logica pentru comutarea automată a formularelor în formulare predefinite.</span><span class="sxs-lookup"><span data-stu-id="20ea0-111">To avoid potential data corruption and unexpected behaviors that are caused by incorrect initialization and editing of the sales entity records, PSA now includes logic for automatic form switching in out-of-box forms.</span></span> <span data-ttu-id="20ea0-112">Această logică duce utilizatorii la formularul corect pentru lucrul cu versiunea bazată pe activități sau cu orice alt tip de entitate Oportunitate, Ofertă, Comandă sau Factură.</span><span class="sxs-lookup"><span data-stu-id="20ea0-112">This logic takes users to the correct form for working with the work-based version or any other type of Opportunity, Quote, Order, or Invoice entity.</span></span> <span data-ttu-id="20ea0-113">Când un utilizator deschide versiunea bazată pe activități a unei entități Oportunitate, Ofertă, Comandă sau Factură, formularul este comutat la **Informații proiect**.</span><span class="sxs-lookup"><span data-stu-id="20ea0-113">When a user opens the work-based version of an Opportunity, Quote, Order, or Invoice entity, the form is switched to **Project Information**.</span></span>

<span data-ttu-id="20ea0-114">Logica de comutare automată a formularului se bazează pe maparea dintre valoarea **formId** și câmpul **msdyn\_tipcomandă**.</span><span class="sxs-lookup"><span data-stu-id="20ea0-114">The automatic form switching logic relies on the mapping between the **formId** value and the **msdyn\_ordertype** field.</span></span> <span data-ttu-id="20ea0-115">Toate formularele predefinite au fost adăugate la acea mapare.</span><span class="sxs-lookup"><span data-stu-id="20ea0-115">All out-of-box forms have been added to that mapping.</span></span> <span data-ttu-id="20ea0-116">Cu toate acestea, formularele particularizate trebuie adăugate manual pentru a indica ce versiune a entității se intenționează să gestioneze.</span><span class="sxs-lookup"><span data-stu-id="20ea0-116">However, custom forms must be manually added to indicate which version of the entity they are intended to handle.</span></span> <span data-ttu-id="20ea0-117">Acest lucru se bazează pe câmpul **msdyn\_tipcomandă**.</span><span class="sxs-lookup"><span data-stu-id="20ea0-117">This is based on the **msdyn\_ordertype** field.</span></span> <span data-ttu-id="20ea0-118">Dacă comutarea formularului lipsește din mapare, logica va comuta la formularul predefinit, pe baza valorii salvate în câmpul **msdyn\_tipcomandă** al entității.</span><span class="sxs-lookup"><span data-stu-id="20ea0-118">If the form switching is missing from the mapping, logic will switch to the out-of-box form, based on the value that is saved in the **msdyn\_ordertype** field of the entity.</span></span>

## <a name="add-custom-forms-and-turn-on-the-form-switching-logic"></a><span data-ttu-id="20ea0-119">Adăugarea formularelor particularizate și activarea logicii de comutare a formularului</span><span class="sxs-lookup"><span data-stu-id="20ea0-119">Add custom forms and turn on the form switching logic</span></span>

<span data-ttu-id="20ea0-120">Următorul exemplu arată cum să adăugați un formular particularizat, **Informațiile mele de proiect** , astfel încât să funcționeze cu oportunități bazate pe activități.</span><span class="sxs-lookup"><span data-stu-id="20ea0-120">The following example shows how to add a custom form, **My Project Information** , so that it works with work-based opportunities.</span></span> <span data-ttu-id="20ea0-121">Același proces este utilizat pentru a adăuga formulare particularizate, astfel încât acestea să funcționeze cu oferte, comenzi și facturi.</span><span class="sxs-lookup"><span data-stu-id="20ea0-121">The same process is used to add custom forms so that they work with quotes, orders, and invoices.</span></span>

<span data-ttu-id="20ea0-122">Urmați acești pași pentru a crea o versiune particularizată a formularului **Informații proiect**.</span><span class="sxs-lookup"><span data-stu-id="20ea0-122">Follow these steps to create a custom version of the **Project Information** form.</span></span>

1. <span data-ttu-id="20ea0-123">În entitatea Oportunitate, deschideți formularul **Informații proiect** și salvați o copie sub numele **Informațiile mele de proiect**.</span><span class="sxs-lookup"><span data-stu-id="20ea0-123">In the Opportunity entity, open the **Project Information** form, and save a copy under the name **My Project Information**.</span></span>
2. <span data-ttu-id="20ea0-124">Deschideți formularul nou, și apoi, din proprietăți, asigurați-vă că scripturile de inițializare a formularului din formularul **Informații proiect** sunt prezente.</span><span class="sxs-lookup"><span data-stu-id="20ea0-124">Open the new form, and then, in the properties, make sure that the form initialization scripts from the **Project Information** form are present.</span></span> 

    > [!IMPORTANT]
    > <span data-ttu-id="20ea0-125">Nu eliminați scripturile.</span><span class="sxs-lookup"><span data-stu-id="20ea0-125">Don't remove the scripts.</span></span> <span data-ttu-id="20ea0-126">În caz contrar, unele date pot fi inițializate incorect.</span><span class="sxs-lookup"><span data-stu-id="20ea0-126">Otherwise, some data might be initialized incorrectly.</span></span>

3. <span data-ttu-id="20ea0-127">Verificați că câmpul **Tip** ( **msdyn\_tipcomandă** ) este prezent în formular.</span><span class="sxs-lookup"><span data-stu-id="20ea0-127">Verify that the **Type** ( **msdyn\_ordertype** ) field is present in the form.</span></span> 

    > [!IMPORTANT]
    > <span data-ttu-id="20ea0-128">Nu eliminați acest câmp.</span><span class="sxs-lookup"><span data-stu-id="20ea0-128">Don't remove this field.</span></span> <span data-ttu-id="20ea0-129">În caz contrar, scripturile de inițializare vor eșua.</span><span class="sxs-lookup"><span data-stu-id="20ea0-129">Otherwise, the initialization scripts will fail.</span></span>

4. <span data-ttu-id="20ea0-130">Găsiți valoarea **formId** a noului formular.</span><span class="sxs-lookup"><span data-stu-id="20ea0-130">Find the **formId** value of the new form.</span></span> <span data-ttu-id="20ea0-131">Puteți finaliza acest pas în două moduri diferite:</span><span class="sxs-lookup"><span data-stu-id="20ea0-131">You can complete this step in two ways:</span></span>

    - <span data-ttu-id="20ea0-132">Exportați formularul **Informațiile mele de proiect** ca parte a unei soluții negestionate și apoi căutați valoarea **formId** în fișierul customization.xml al soluției exportate.</span><span class="sxs-lookup"><span data-stu-id="20ea0-132">Export the **My Project Information** form as part of an unmanaged solution, and then look up the **formId** value in the customization.xml file of the exported solution.</span></span>
    - <span data-ttu-id="20ea0-133">Deschideți formularul **Informațiile mele de proiect** în editorul de formular, și apoi căutați identificatorul unic global (GUID) lângă parametrul **fromId** în URL, așa se arată în următoarea ilustrație.</span><span class="sxs-lookup"><span data-stu-id="20ea0-133">Open the **My Project Information** form in the form editor, and then look for the globally unique identifier (GUID) next to the **fromId** parameter in the URL, as shown in the following illustration.</span></span>

    ![Valoarea formId a noului formular din URL.](media/how-to-add-custom-forms-in-v2.0.png)

5. <span data-ttu-id="20ea0-135">Creați o mapare **msdyn\_tipcomandă** pentru valoarea **formId** editând resursa web msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js.</span><span class="sxs-lookup"><span data-stu-id="20ea0-135">Create an **msdyn\_ordertype** mapping for the **formId** value by editing the msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js web resource.</span></span> <span data-ttu-id="20ea0-136">Eliminați codul din resursă și înlocuiți-l cu următorul cod.</span><span class="sxs-lookup"><span data-stu-id="20ea0-136">Remove the code from the resource, and replace it with the following code.</span></span>

    ```javascript
    define(["require", "exports"], function (require, exports) {
        "use strict";
        var SalesDocumentCustomFormIds = (function () {
            function SalesDocumentCustomFormIds() {
            }
            SalesDocumentCustomFormIds.overwriteFormIds = function (mappedFormIds) {
                /*
                ---- Notes ----
                mappedFormIds[SalesEntity][OrderType] => The array of forms IDs that support particular entity and order type
                Add or overwrite customized formId for the particular entity and order type by calling:
                    mappedFormIds[<EntityType>][<msdyn_ordertype>].push("<formId>");
                Allowed msdyn_ordertype values for reference:
                    ServiceBased: 690970002 (Field Service version of the entity)
                    WorkBased: 192350001 (PSA version of the entity)
                    ItemBased: 192350000 (Regular out of the box entity)
                Uncomment and update one of the following lines to register custom PSA form for required entity:
                */      
                //mappedFormIds[1][192350001].push("<formId>"); //Quote
                //mappedFormIds[5][192350001].push("<formId>"); //Quote Line
                //mappedFormIds[2][192350001].push("<formId>"); //Sales Order
                //mappedFormIds[6][192350001].push("<formId>"); //Sales Order Line
                // In this example we have added new form for Opportunity
                mappedFormIds[0][192350001].push("192EE537-DCC4-45D3-B7AF-EA694B9113D2"); //Opportunity
                //mappedFormIds[4][192350001].push("<formId>"); //Opportunity Line
            };
            return SalesDocumentCustomFormIds;
        }());
        exports.default = SalesDocumentCustomFormIds;
    });
    ```

6. <span data-ttu-id="20ea0-137">Salvați și apoi publicați particularizările.</span><span class="sxs-lookup"><span data-stu-id="20ea0-137">Save and then publish the customizations.</span></span>
