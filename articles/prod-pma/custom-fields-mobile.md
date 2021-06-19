---
title: Implementați câmpuri personalizate pentru aplicație mobilă Microsoft Dynamics 365 Project Timesheet pe iOS și Android
description: Acest subiect oferă modele comune pentru utilizarea extensiilor pentru a implementa câmpuri personalizate.
author: Yowelle
ms.date: 05/29/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.3
ms.search.validFrom: 2019-05-29
ms.openlocfilehash: 23b002559dcbb9118ccb2b36d70707ccb37b19ad
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003060"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a><span data-ttu-id="a6dc2-103">Implementați câmpuri personalizate pentru aplicație mobilă Microsoft Dynamics 365 Project Timesheet pe iOS și Android</span><span class="sxs-lookup"><span data-stu-id="a6dc2-103">Implement custom fields for the Microsoft Dynamics 365 Project Timesheet mobile app on iOS and Android</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a6dc2-104">Acest subiect oferă modele comune pentru utilizarea extensiilor pentru a implementa câmpuri personalizate.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-104">This topic provides common patterns for using extensions to implement custom fields.</span></span> <span data-ttu-id="a6dc2-105">Sunt abordate următoarele subiecte:</span><span class="sxs-lookup"><span data-stu-id="a6dc2-105">The following topics are covered:</span></span>

- <span data-ttu-id="a6dc2-106">Diferitele tipuri de date acceptate de cadrul de câmp personalizat</span><span class="sxs-lookup"><span data-stu-id="a6dc2-106">The various data types that the custom field framework supports</span></span>
- <span data-ttu-id="a6dc2-107">Cum se afișează câmpuri numai în citire sau editabile în intrările din foaia de pontaj și cum se salvează valorile furnizate de utilizator în baza de date</span><span class="sxs-lookup"><span data-stu-id="a6dc2-107">How to show read-only or editable fields on timesheet entries, and save user-provided values back to the database</span></span>
- <span data-ttu-id="a6dc2-108">Cum se afișează câmpuri numai în citire în antetul foii de pontaj</span><span class="sxs-lookup"><span data-stu-id="a6dc2-108">How to show read-only fields on the timesheet header</span></span>
- <span data-ttu-id="a6dc2-109">Cum se integrează alte logici de afaceri personalizate pentru a introduce valorile implicite în câmpuri și pentru a efectua validări suplimentare</span><span class="sxs-lookup"><span data-stu-id="a6dc2-109">How to integrate other custom business logic to enter default values in fields and do additional validation</span></span>

## <a name="audience"></a><span data-ttu-id="a6dc2-110">Public</span><span class="sxs-lookup"><span data-stu-id="a6dc2-110">Audience</span></span>

<span data-ttu-id="a6dc2-111">Acest subiect este destinat dezvoltatorilor care își integrează câmpurile personalizate în aplicație mobilă Microsoft Dynamics 365 Project Timesheet disponibilă pentru Apple iOS și Google Android.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-111">This topic is intended for developers who are integrating their custom fields into the Microsoft Dynamics 365 Project Timesheet mobile application that is available for Apple iOS and Google Android.</span></span> <span data-ttu-id="a6dc2-112">Ipoteza este că cititorii sunt familiarizați cu dezvoltarea X++ și funcționalitatea foii de timp a proiectului.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-112">The assumption is that readers are familiar with X++ development and project timesheet functionality.</span></span>

## <a name="data-contract--tstimesheetcustomfield-x-class"></a><span data-ttu-id="a6dc2-113">Contract de date - clasa TSTimesheetCustomField X++</span><span class="sxs-lookup"><span data-stu-id="a6dc2-113">Data contract – TSTimesheetCustomField X++ class</span></span>

<span data-ttu-id="a6dc2-114">Clasa **TSTimesheetCustomField** este clasa contractului de date X++ care reprezintă informații despre un câmp personalizat pentru funcționalitatea foii de pontaj.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-114">The **TSTimesheetCustomField** class is the X++ data contract class that represents information about a custom field for timesheet functionality.</span></span> <span data-ttu-id="a6dc2-115">Listele obiectelor de câmp personalizate sunt transmise atât în contractul de date TSTimesheetDetails, cât și în contractul de date TSTimesheetEntry pentru a afișa câmpuri personalizate în aplicația mobilă.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-115">Lists of the custom field objects are passed on both the TSTimesheetDetails data contract and the TSTimesheetEntry data contract to show custom fields in the mobile app.</span></span>

- <span data-ttu-id="a6dc2-116">**TSTimesheetDetails** - Contractul antetului de foaie de pontaj.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-116">**TSTimesheetDetails** - The timesheet header contract.</span></span>
- <span data-ttu-id="a6dc2-117">**TSTimesheetEntry** - Contractul de tranzacție cu foaie de pontaj.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-117">**TSTimesheetEntry** - The timesheet transaction contract.</span></span> <span data-ttu-id="a6dc2-118">Grupuri de aceste obiecte care au aceleași informații despre proiect și valoarea **timesheetLineRecId** constituie o linie.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-118">Groups of these objects that have the same project information and **timesheetLineRecId** value constitute a line.</span></span>

### <a name="fieldbasetype-types"></a><span data-ttu-id="a6dc2-119">fieldBaseType (Tipuri)</span><span class="sxs-lookup"><span data-stu-id="a6dc2-119">fieldBaseType (Types)</span></span>

<span data-ttu-id="a6dc2-120">Proprietatea **FieldBaseType** pe obiectul **TsTimesheetCustom** determină tipul câmpului care apare în aplicație.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-120">The **FieldBaseType** property on the **TsTimesheetCustom** object determines the type of the field that appears in the app.</span></span> <span data-ttu-id="a6dc2-121">Următoarele valori de **Tipuri** care sunt acceptate.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-121">The following **Types** values that are supported.</span></span>

| <span data-ttu-id="a6dc2-122">Tipuri de valoare</span><span class="sxs-lookup"><span data-stu-id="a6dc2-122">Types value</span></span> | <span data-ttu-id="a6dc2-123">Tip</span><span class="sxs-lookup"><span data-stu-id="a6dc2-123">Type</span></span>              | <span data-ttu-id="a6dc2-124">Note</span><span class="sxs-lookup"><span data-stu-id="a6dc2-124">Notes</span></span> |
|-------------|-------------------|-------|
| <span data-ttu-id="a6dc2-125">0</span><span class="sxs-lookup"><span data-stu-id="a6dc2-125">0</span></span>           | <span data-ttu-id="a6dc2-126">Șir (și Enum)</span><span class="sxs-lookup"><span data-stu-id="a6dc2-126">String (and Enum)</span></span> | <span data-ttu-id="a6dc2-127">Câmpul apare ca un câmp de text.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-127">The field appears as a text field.</span></span> |
| <span data-ttu-id="a6dc2-128">1</span><span class="sxs-lookup"><span data-stu-id="a6dc2-128">1</span></span>           | <span data-ttu-id="a6dc2-129">Integer</span><span class="sxs-lookup"><span data-stu-id="a6dc2-129">Integer</span></span>           | <span data-ttu-id="a6dc2-130">Valoarea este afișată ca un număr fără zecimale.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-130">The value is shown as a number without decimal places.</span></span> |
| <span data-ttu-id="a6dc2-131">2</span><span class="sxs-lookup"><span data-stu-id="a6dc2-131">2</span></span>           | <span data-ttu-id="a6dc2-132">Real</span><span class="sxs-lookup"><span data-stu-id="a6dc2-132">Real</span></span>              | <span data-ttu-id="a6dc2-133">Valoarea este afișată ca un număr care are zecimale.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-133">The value is shown as a number that has decimal places.</span></span><p><span data-ttu-id="a6dc2-134">Pentru a afișa valoarea reală ca monedă în aplicație, utilizați proprietatea **fieldExtenededType**.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-134">To show the real value as a currency in the app, use the **fieldExtenededType** property.</span></span> <span data-ttu-id="a6dc2-135">Puteți utiliza proprietatea **numberOfDecimals** pentru a seta numărul de zecimale care sunt afișate.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-135">You can use the **numberOfDecimals** property to set the number of decimal places that are shown.</span></span></p> |
| <span data-ttu-id="a6dc2-136">3</span><span class="sxs-lookup"><span data-stu-id="a6dc2-136">3</span></span>           | <span data-ttu-id="a6dc2-137">Data</span><span class="sxs-lookup"><span data-stu-id="a6dc2-137">Date</span></span>              | <span data-ttu-id="a6dc2-138">Formatele de dată sunt determinate de setarea utilizatorului **Data, orele și formatul numerelor** care este specificată la **Limba și preferința țării/regiunii** în **Opțiuni utilizator**.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-138">Date formats are determined by the user's **Date, times, and number format** setting that is specified under **Language and country/region preference** in **User options**.</span></span> |
| <span data-ttu-id="a6dc2-139">4</span><span class="sxs-lookup"><span data-stu-id="a6dc2-139">4</span></span>           | <span data-ttu-id="a6dc2-140">Boolean</span><span class="sxs-lookup"><span data-stu-id="a6dc2-140">Boolean</span></span>           | |
| <span data-ttu-id="a6dc2-141">15</span><span class="sxs-lookup"><span data-stu-id="a6dc2-141">15</span></span>          | <span data-ttu-id="a6dc2-142">GUID</span><span class="sxs-lookup"><span data-stu-id="a6dc2-142">GUID</span></span>              | |
| <span data-ttu-id="a6dc2-143">16</span><span class="sxs-lookup"><span data-stu-id="a6dc2-143">16</span></span>          | <span data-ttu-id="a6dc2-144">Int64</span><span class="sxs-lookup"><span data-stu-id="a6dc2-144">Int64</span></span>             | |

- <span data-ttu-id="a6dc2-145">Dacă proprietatea **stringOptions** nu este furnizată pe obiectul **TSTimesheetCustomField**, un câmp de text liber este furnizat utilizatorului.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-145">If the **stringOptions** property isn't provided on the **TSTimesheetCustomField** object, a free-text field is provided to the user.</span></span>

    <span data-ttu-id="a6dc2-146">Proprietatea **stringLength** poate fi utilizată pentru a seta lungimea maximă a șirului pe care utilizatorii o pot introduce.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-146">The **stringLength** property can be used to set the maximum string length that users can enter.</span></span>

- <span data-ttu-id="a6dc2-147">Dacă proprietatea **stringOptions** este furnizată pe obiectul **TSTimesheetCustomField**, acele elemente de listă sunt singurele valori pe care utilizatorii le pot selecta folosind butoanele de opțiune (butoanele radio).</span><span class="sxs-lookup"><span data-stu-id="a6dc2-147">If the **stringOptions** property is provided on the **TSTimesheetCustomField** object, those list elements are the only values that users can select by using option buttons (radio buttons).</span></span>

    <span data-ttu-id="a6dc2-148">În acest caz, câmpul șir poate acționa ca o valoare enum în scopul intrării utilizatorului.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-148">In this case, the string field can act as an enum value for the purpose of user entry.</span></span> <span data-ttu-id="a6dc2-149">Pentru a salva valoarea în baza de date ca o enumerare, mapați manual valoarea șirului înapoi la valoarea enumerată înainte de a salva în baza de date utilizând lanțul de comandă (consultați secțiunea „Utilizați lanțul de comandă din clasa TSTimesheetEntryService pentru a salva o intrare din foaia de pontaj din aplicație înapoi în baza de date" de mai târziu din acest subiect pentru o exemplificare).</span><span class="sxs-lookup"><span data-stu-id="a6dc2-149">To save the value to the database as an enum, manually map the string value back to the enum value before you save to the database by using chain of command (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a><span data-ttu-id="a6dc2-150">fieldExtendedType (TSCustomFieldExtendedType)</span><span class="sxs-lookup"><span data-stu-id="a6dc2-150">fieldExtendedType (TSCustomFieldExtendedType)</span></span>

<span data-ttu-id="a6dc2-151">Puteți utiliza această proprietate pentru a formata valorile reale ca monedă.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-151">You can use this property to format real values as currency.</span></span> <span data-ttu-id="a6dc2-152">Această abordare este aplicabilă numai atunci când valoarea **fieldBaseType** este **Reală**.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-152">This approach is applicable only when the **fieldBaseType** value is **Real**.</span></span>

- <span data-ttu-id="a6dc2-153">**TSCustomFieldExtendedType:None** – Nu se aplică nicio formatare.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-153">**TSCustomFieldExtendedType:None** – No formatting is applied.</span></span>
- <span data-ttu-id="a6dc2-154">**TSCustomFieldExtendedType::Currency** – Formatați valoarea ca monedă.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-154">**TSCustomFieldExtendedType::Currency** – Format the value as currency.</span></span>

    <span data-ttu-id="a6dc2-155">Când formatarea monedei este activă, câmpul **stringValue** poate fi folosit dincolo de codul monedei care ar trebui să fie afișat în aplicație.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-155">When currency formatting is active, the **stringValue** field can be used pass the currency code that should be shown in the app.</span></span> <span data-ttu-id="a6dc2-156">Valoarea este o valoare numai în citire.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-156">The value is a read-only value.</span></span>

    <span data-ttu-id="a6dc2-157">Câmpul **realValue** conține suma de bani care trebuie salvată în baza de date.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-157">The **realValue** field contains the money amount that should be saved to the database.</span></span>

### <a name="fieldsection-tscustomfieldsection"></a><span data-ttu-id="a6dc2-158">fieldSection (TSCustomFieldSection)</span><span class="sxs-lookup"><span data-stu-id="a6dc2-158">fieldSection (TSCustomFieldSection)</span></span>

<span data-ttu-id="a6dc2-159">Puteți utiliza această proprietate, specificați unde ar trebui să apară câmpul personalizat în aplicație.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-159">You can use this property specify where the custom field should appear in the app.</span></span>

- <span data-ttu-id="a6dc2-160">**Antetul TSCustomFieldSection::** – Câmpul va apărea în secțiunea **Vizualizați mai multe detalii** din aplicație.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-160">**TSCustomFieldSection::Header** – The field will appear in the **View more details** section in the app.</span></span> <span data-ttu-id="a6dc2-161">Aceste câmpuri sunt întotdeauna numai în citire.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-161">These fields are always read-only.</span></span>
- <span data-ttu-id="a6dc2-162">**Linia TSCustomFieldSection::** - Câmpul va apărea după toate câmpurile de linie predefinite de pe intrările de foaie de pontaj.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-162">**TSCustomFieldSection::Line** – The field will appear after all the out-of-box line fields on timesheet entries.</span></span> <span data-ttu-id="a6dc2-163">Aceste câmpuri pot fi modificabile sau doar în citire.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-163">These fields can be either editable or read-only.</span></span>

### <a name="fieldname-fieldnameshort"></a><span data-ttu-id="a6dc2-164">fieldName (FieldNameShort)</span><span class="sxs-lookup"><span data-stu-id="a6dc2-164">fieldName (FieldNameShort)</span></span>

<span data-ttu-id="a6dc2-165">Această proprietate identifică câmpul atunci când valorile pe care le oferă aplicația sunt salvate înapoi în baza de date.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-165">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="tablename-tablenameshort"></a><span data-ttu-id="a6dc2-166">tableName (TableNameShort)</span><span class="sxs-lookup"><span data-stu-id="a6dc2-166">tableName (TableNameShort)</span></span>

<span data-ttu-id="a6dc2-167">Această proprietate identifică câmpul atunci când valorile pe care le oferă aplicația sunt salvate înapoi în baza de date.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-167">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="iseditable-noyes"></a><span data-ttu-id="a6dc2-168">isEditable (NoYes)</span><span class="sxs-lookup"><span data-stu-id="a6dc2-168">isEditable (NoYes)</span></span>

<span data-ttu-id="a6dc2-169">Setați această proprietate la **Da** pentru a specifica că câmpul din secțiunea de introducere a foii de pontaj ar trebui să fie modificabil de către utilizatori.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-169">Set this property to **Yes** to specify that the field in the timesheet entry section should be editable by users.</span></span> <span data-ttu-id="a6dc2-170">Setați proprietatea la **Nu** pentru a trece câmpul numai în citire.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-170">Set the property to **No** to make the field read-only.</span></span>

### <a name="ismandatory-noyes"></a><span data-ttu-id="a6dc2-171">isMandatory (NoYes)</span><span class="sxs-lookup"><span data-stu-id="a6dc2-171">isMandatory (NoYes)</span></span>

<span data-ttu-id="a6dc2-172">Setați această proprietate la **Da** pentru a specifica că câmpul din secțiunea de introducere a foii de pontaj ar trebui să fie obligatoriu.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-172">Set this property to **Yes** to specify that the field in the timesheet entry section should be mandatory.</span></span>

### <a name="label-str"></a><span data-ttu-id="a6dc2-173">label (str)</span><span class="sxs-lookup"><span data-stu-id="a6dc2-173">label (str)</span></span>

<span data-ttu-id="a6dc2-174">Această proprietate specifică eticheta care este afișată lângă câmpul din aplicație.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-174">This property specifies the label that is shown next the field in the app.</span></span>

### <a name="stringoptions-list-of-strings"></a><span data-ttu-id="a6dc2-175">stringOptions (Lista de șiruri)</span><span class="sxs-lookup"><span data-stu-id="a6dc2-175">stringOptions (List of Strings)</span></span>

<span data-ttu-id="a6dc2-176">Această proprietate este aplicabilă numai atunci când **fieldBaseType** este setat la **Șir**.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-176">This property is applicable only when **fieldBaseType** is set to **String**.</span></span> <span data-ttu-id="a6dc2-177">Dacă **stringOptions** este setat, valorile șirurilor disponibile pentru selectare prin butoanele de opțiune (butoanele radio) sunt specificate de șirurile din listă.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-177">If **stringOptions** is set, the string values that are available for selection via option buttons (radio buttons) are specified by the strings in the list.</span></span> <span data-ttu-id="a6dc2-178">Dacă nu sunt furnizate șiruri, este permisă introducerea textului liber în câmpul șirului (consultați secțiunea „Utilizați lanțul de comandă din clasa TSTimesheetEntryService pentru a salva o intrare din foaia de pontaj din aplicație înapoi în baza de date" de mai târziu din acest subiect pentru o exemplificare) .</span><span class="sxs-lookup"><span data-stu-id="a6dc2-178">If no strings are provided, free-text entry in the string field is allowed (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="stringlength-int"></a><span data-ttu-id="a6dc2-179">stringLength (int)</span><span class="sxs-lookup"><span data-stu-id="a6dc2-179">stringLength (int)</span></span>

<span data-ttu-id="a6dc2-180">Această proprietate specifică lungimea maximă pentru un câmp șir.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-180">This property specifies the maximum length for a string field.</span></span> <span data-ttu-id="a6dc2-181">Aceasta se aplică numai atunci când **fieldBaseType** este setat la **Șir**.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-181">It's applicable only when **fieldBaseType** is set to **String**.</span></span>

### <a name="numberofdecimals-int"></a><span data-ttu-id="a6dc2-182">numberOfDecimals (int)</span><span class="sxs-lookup"><span data-stu-id="a6dc2-182">numberOfDecimals (int)</span></span>

<span data-ttu-id="a6dc2-183">Această proprietate specifică numărul de zecimale care sunt afișate pentru un câmp real.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-183">This property specifies the number of decimal places that are shown for a real field.</span></span> <span data-ttu-id="a6dc2-184">Aceasta se aplică numai atunci când **fieldBaseType** este setat la **Real**.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-184">It's applicable only when **fieldBaseType** is set to **Real**.</span></span>

### <a name="ordersequence-int"></a><span data-ttu-id="a6dc2-185">orderSequence (int)</span><span class="sxs-lookup"><span data-stu-id="a6dc2-185">orderSequence (int)</span></span>

<span data-ttu-id="a6dc2-186">Această proprietate controlează ordinea în care câmpurile personalizate sunt afișate în aplicație atunci când sunt specificate mai multe câmpuri personalizate.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-186">This property controls the order in which the custom fields are shown in the app when more than one custom field is specified.</span></span> <span data-ttu-id="a6dc2-187">Câmpurile care au numere mai mici sunt afișate mai întâi.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-187">Fields that have lower numbers are shown first.</span></span>

### <a name="booleanvalue-boolean"></a><span data-ttu-id="a6dc2-188">booleanValue (boolean)</span><span class="sxs-lookup"><span data-stu-id="a6dc2-188">booleanValue (boolean)</span></span>

<span data-ttu-id="a6dc2-189">Pentru câmpurile de tipul **Boolean**, această proprietate trece valoarea booleană a câmpului dintre server și aplicație.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-189">For fields of the **Boolean** type, this property passes the Boolean value of the field between the server and the app.</span></span>

### <a name="guidvalue-guid"></a><span data-ttu-id="a6dc2-190">guidValue (guid)</span><span class="sxs-lookup"><span data-stu-id="a6dc2-190">guidValue (guid)</span></span>

<span data-ttu-id="a6dc2-191">Pentru câmpurile de tipul **GUID**, această proprietate trece valoarea identificator unic global (GUID) a câmpului dintre server și aplicație.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-191">For fields of the **GUID** type, this property passes the globally unique identifier (GUID) value of the field between the server and the app.</span></span>

### <a name="int64value-int64"></a><span data-ttu-id="a6dc2-192">int64Value (int64)</span><span class="sxs-lookup"><span data-stu-id="a6dc2-192">int64Value (int64)</span></span>

<span data-ttu-id="a6dc2-193">Pentru câmpurile de tipul **Int64**, această proprietate trece valoarea Int64 a câmpului dintre server și aplicație.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-193">For fields of the **Int64** type, this property passes the int64 value of the field between the server and the app.</span></span>

### <a name="intvalue-int"></a><span data-ttu-id="a6dc2-194">intValue (int)</span><span class="sxs-lookup"><span data-stu-id="a6dc2-194">intValue (int)</span></span>

<span data-ttu-id="a6dc2-195">Pentru câmpurile de tipul **Int**, această proprietate trece valoarea Int a câmpului dintre server și aplicație.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-195">For fields of the **Int** type, this property passes the int value of the field between the server and the app.</span></span>

### <a name="realvalue-real"></a><span data-ttu-id="a6dc2-196">realValue (reală)</span><span class="sxs-lookup"><span data-stu-id="a6dc2-196">realValue (real)</span></span>

<span data-ttu-id="a6dc2-197">Pentru câmpurile de tipul **Reală**, această proprietate trece valoarea reală a câmpului dintre server și aplicație.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-197">For fields of the **Real** type, this property passes the real value of the field between the server and the app .</span></span>

### <a name="stringvalue-str"></a><span data-ttu-id="a6dc2-198">stringValue (str)</span><span class="sxs-lookup"><span data-stu-id="a6dc2-198">stringValue (str)</span></span>

<span data-ttu-id="a6dc2-199">Pentru câmpurile de tipul **Șir**, această proprietate trece valoarea șirului câmpului dintre server și aplicație.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-199">For fields of the **String** type, this property passes the string value of the field between the server and the app.</span></span> <span data-ttu-id="a6dc2-200">Este, de asemenea, utilizat pentru câmpurile de tipul **Real** care sunt formatate ca monedă.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-200">It's also used for fields of the **Real** type that are formatted as currency.</span></span> <span data-ttu-id="a6dc2-201">Pentru acele câmpuri, proprietatea este utilizată pentru a transmite codul monedei aplicației.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-201">For those fields, the property is used to pass the currency code to the app.</span></span>

### <a name="datevalue-date"></a><span data-ttu-id="a6dc2-202">dateValue (data)</span><span class="sxs-lookup"><span data-stu-id="a6dc2-202">dateValue (date)</span></span>

<span data-ttu-id="a6dc2-203">Pentru câmpurile de tipul **Data**, această proprietate trece valoarea datei câmpului dintre server și aplicație.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-203">For fields of the **Date** type, this property passes the date value of the field between the server and the app.</span></span>

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a><span data-ttu-id="a6dc2-204">Afișați și salvați un câmp personalizat în secțiunea de introducere a foii de pontaj</span><span class="sxs-lookup"><span data-stu-id="a6dc2-204">Show and save a custom field in the timesheet entry section</span></span>

<span data-ttu-id="a6dc2-205">Mai jos este o captură de ecran din aplicația mobilă a unei creații de intrare a foii de pontaj.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-205">Below is a screenshot from the mobile app of a timesheet entry creation.</span></span> <span data-ttu-id="a6dc2-206">Afișează câmpurile predefinite și un câmp personalizat în secțiunea „Intrare pontaj” numită „Șir de testare”, cu o valoare enum de „A doua opțiune” deja setată.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-206">It shows the out-of-box fields and a custom field in the "Time entry" section called "Test string" with an enum value of "Second option" already set.</span></span>

![Testați câmpul personalizat al șirului în aplicație](media/timesheet-entry.jpg)



<span data-ttu-id="a6dc2-208">Mai jos este o captură de ecran din aplicația mobilă a utilizatorului care selectează una dintre opțiunile de enum disponibile pentru câmpul personalizat „Șir de testare”.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-208">Below is a screenshot from the mobile app of the user selecting one of the enum options available for the "Test string" custom field.</span></span>  <span data-ttu-id="a6dc2-209">Cele două opțiuni sunt „Prima opțiune” și „A doua opțiune” afișate ca butoane radio.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-209">The two options are "First option" and "Second option" shown as radio buttons.</span></span> <span data-ttu-id="a6dc2-210">În prezent, este selectată a doua opțiune.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-210">The second option is currently selected.</span></span>

![Butoane de opțiune (butoane radio) pentru câmpul personalizat Șir de testare](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="a6dc2-212">Extindeți tabelul TSTimesheetLine astfel încât să aibă un câmp personalizat</span><span class="sxs-lookup"><span data-stu-id="a6dc2-212">Extend the TSTimesheetLine table so that it has a custom field</span></span>

<span data-ttu-id="a6dc2-213">În scenarii tipice, este probabil ca datele pentru un câmp personalizat din secțiunea de intrare a foii de pontaj să fie salvate în tabelul TSTimesheetLine.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-213">In typical scenarios, it's likely that the data for a custom field in the timesheet entry section will be saved to the TSTimesheetLine table.</span></span> <span data-ttu-id="a6dc2-214">Cu toate acestea, se pot utiliza și alte tabele dacă datele pot fi recuperate pe baza unei înregistrări TSTimesheetTrans furnizate sau dacă nu au un context de înregistrare specific (de exemplu, dacă câmpul este setat ca numai în citire în parametrii proiectului) .</span><span class="sxs-lookup"><span data-stu-id="a6dc2-214">However, other tables can be used if the data can be retrieved based on a TSTimesheetTrans record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="a6dc2-215">Rețineți că câmpurile personalizate nu trebuie să aibă nicio înregistrare de bază de date.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-215">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="a6dc2-216">Ele pot fi generate dinamic pe baza logicii X++.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-216">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="a6dc2-217">Această abordare poate fi utilă în scenarii doar de citire (consultați secțiunea „Utilizați lanțul de comandă din clasa TSTimesheetDetails, metoda buildCustomFieldListForHeader pentru a completa detaliile foii de pontaj” pentru un exemplu de valori ale câmpurilor personalizate generate dinamic.)</span><span class="sxs-lookup"><span data-stu-id="a6dc2-217">This approach can be useful in read-only scenarios (see the “Use chain of command on the TSTimesheetDetails class, buildCustomFieldListForHeader method to fill in timesheet details” section for an example of dynamically generated custom field values.)</span></span>

<span data-ttu-id="a6dc2-218">Mai jos este o captură de ecran din Visual Studio din arborele obiectelor aplicației.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-218">Below is a screenshot from Visual Studio of the Application Object Tree.</span></span> <span data-ttu-id="a6dc2-219">Afișează o extensie a tabelului TSTimesheetLine cu câmpul TestLineString adăugat ca un câmp personalizat.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-219">It shows an extension of the TSTimesheetLine table with the TestLineString field added as a custom field.</span></span>

![Șir de linie](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a><span data-ttu-id="a6dc2-221">Utilizați lanțul de comandă pe metoda buildCustomFieldList a clasei TSTimesheetSettings pentru a afișa un câmp în secțiunea de intrare a foii de pontaj</span><span class="sxs-lookup"><span data-stu-id="a6dc2-221">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the timesheet entry section</span></span>

<span data-ttu-id="a6dc2-222">Acest cod controlează setările de afișare pentru câmpul din aplicație.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-222">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="a6dc2-223">De exemplu, controlează tipul de câmp, eticheta, dacă câmpul este obligatoriu și în ce secțiune apare câmpul.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-223">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="a6dc2-224">Următorul exemplu arată un câmp șir la intrările de timp.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-224">The following example shows a string field on time entries.</span></span> <span data-ttu-id="a6dc2-225">Acest câmp are două opțiuni, **Prima opțiune** și **A doua opțiune**, care sunt disponibile prin intermediul butoanelor de opțiune (butoane radio).</span><span class="sxs-lookup"><span data-stu-id="a6dc2-225">This field has two options, **First option** and **Second option**, that are available via option buttons (radio buttons).</span></span> <span data-ttu-id="a6dc2-226">Câmpul din aplicație este asociat cu câmpul **TestLineString** care este adăugat la tabelul TSTimesheetLine.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-226">The field in the app is associated with the **TestLineString** field that is added to the TSTimesheetLine table.</span></span>

<span data-ttu-id="a6dc2-227">Rețineți utilizarea metodei **TSTimesheetCustomField::newFromMetatdata()** pentru simplificarea inițializării proprietăților câmpului personalizat: **fieldBaseType**, **tableName**, **fieldname**, **eticheta**, **isEditable**, **isMandatory**, **stringLength** și **numberOfDecimals**.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-227">Note the use of the **TSTimesheetCustomField::newFromMetatdata()** method to simplify the initialization of the custom field properties: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength**, and **numberOfDecimals**.</span></span> <span data-ttu-id="a6dc2-228">De asemenea, puteți seta acești parametri manual, după cum doriți.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-228">You can also set these parameters manually, as you prefer.</span></span>

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('Second option');
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a><span data-ttu-id="a6dc2-229">Utilizați lanțul de comandă pe metoda buildCustomFieldListForEntry a clasei TSTimesheetEntry pentru a introduce valori într-o intrare de foaie de pontaj</span><span class="sxs-lookup"><span data-stu-id="a6dc2-229">Use chain of command on the buildCustomFieldListForEntry method of the TSTimesheetEntry class to enter values in a timesheet entry</span></span>

<span data-ttu-id="a6dc2-230">Metoda **buildCustomFieldListForEntry** este utilizată pentru a introduce valori pe liniile de foaie de pontaj salvate în aplicația mobilă.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-230">The **buildCustomFieldListForEntry** method is used to enter values on the saved timesheet lines in the mobile app.</span></span> <span data-ttu-id="a6dc2-231">Este nevoie de o înregistrare TSTimesheetTrans ca parametru.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-231">It takes a TSTimesheetTrans record as a parameter.</span></span> <span data-ttu-id="a6dc2-232">Câmpurile din acea înregistrare pot fi folosite pentru a completa valoarea câmpului personalizat din aplicație.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-232">Fields from that record can be used to fill in the custom field value in the app.</span></span>

```xpp
...
[ExtensionOf(classStr(TsTimesheetEntry))]
final class TsTimesheetEntry_Extension
{
    protected List buildCustomFieldListForEntry(TSTimesheetTrans _tsTimesheetTrans)
    {
        List customFieldList = next buildCustomFieldListForEntry(_tsTimesheetTrans);
        TSTimesheetLine tsTimesheetLine = _tsTimesheetTrans.timesheetLine();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        tsTimesheetCustomField.parmStringValue(tsTimesheetLine.TestLineString);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('second option;);
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a><span data-ttu-id="a6dc2-233">Utilizați lanțul de comandă din clasa TSTimesheetEntryService pentru a salva o intrare din foaia de pontaj din aplicație înapoi în baza de date</span><span class="sxs-lookup"><span data-stu-id="a6dc2-233">Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database</span></span>

<span data-ttu-id="a6dc2-234">Pentru a salva un câmp personalizat înapoi în baza de date în utilizarea obișnuită, trebuie să extindeți mai multe metode:</span><span class="sxs-lookup"><span data-stu-id="a6dc2-234">To save a custom field back to the database in typical usage, you must extend multiple methods:</span></span>

- <span data-ttu-id="a6dc2-235">Metoda **timesheetLineNeedsUpdating** este utilizată pentru a determina dacă înregistrarea de linie a fost modificată de utilizator în aplicație și trebuie salvată în baza de date.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-235">The **timesheetLineNeedsUpdating** method is used to determine whether the line record has been changed by the user in the app and must be saved to the database.</span></span> <span data-ttu-id="a6dc2-236">Dacă performanța nu este o problemă, această metodă poate fi simplificată astfel încât să returneze întotdeauna **true**.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-236">If performance isn't a concern, this method can be simplified so that it always returns **true**.</span></span>
- <span data-ttu-id="a6dc2-237">Metodele **populateTimesheetLineFromEntryDuringCreate** și **populateTimesheetLineFromEntryDuringUpdate** pot fi extinse astfel încât să introducă valori în înregistrarea bazei de date TSTimesheetLine din înregistrarea contractului de date TSTimesheetEntry care este furnizat.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-237">The **populateTimesheetLineFromEntryDuringCreate** and **populateTimesheetLineFromEntryDuringUpdate** methods can be extended so that they enter values in the TSTimesheetLine database record from the TSTimesheetEntry data contract record that is provided.</span></span> <span data-ttu-id="a6dc2-238">În exemplul care urmează, observați cum maparea între câmpul bazei de date și câmpul de intrare se face manual prin codul X++.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-238">In the example that follows, notice how the mapping between the database field and the entry field is manually done via X++ code.</span></span>
- <span data-ttu-id="a6dc2-239">Metoda **populateTimesheetWeekFromEntry** poate fi extinsă și în cazul în care câmpul personalizat care este mapat la obiectul **TSTimesheetEntry** trebuie să proceseze datele în tabelul bazei de date TSTimesheetLineweek.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-239">The **populateTimesheetWeekFromEntry** method can also be extended if the custom field that is mapped to the **TSTimesheetEntry** object must write back to the TSTimesheetLineweek database table.</span></span>

> [!NOTE]
> <span data-ttu-id="a6dc2-240">Următorul exemplu salvează valoarea **firstOption** sau **secondOption** pe care utilizatorul o selectează în baza de date ca valoare brută a șirului.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-240">The following example saves the **firstOption** or **secondOption** value that the user selects to the database as a raw string value.</span></span> <span data-ttu-id="a6dc2-241">Dacă câmpul bazei de date este un câmp de tipul **Enum**, acele valori pot fi mapate manual la o valoare enum și apoi salvate într-un câmp enum de pe tabelul bazei de date.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-241">If the database field is a field of the **Enum** type, those values can be manually mapped to an enum value and then saved to an enum field on the database table.</span></span>

```xpp
...
[ExtensionOf(classStr(TSTimesheetEntryService))]
final class TSTimesheetEntryService_Extension
{
    protected boolean timesheetLineNeedsUpdating(TSTimesheetLine _tsTimesheetLine,
    TsTimesheetEntry _tsTimesheetEntry)
    {
        boolean ret = next timesheetLineNeedsUpdating(_tsTimesheetLine,
        _tsTimesheetEntry);
        if (!ret)
        {
            */ Loop through custom fields to see if value needs updating*/
            ListEnumerator enumerator =  _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    */ If Custom field value for TestLineString field has changed, We need to update the timesheet line.*/
                    if (_tsTimesheetLine.TestLineString != customField.parmStringValue())
                    {
                        ret = true;
                    }
                }
            }
        }
        return ret;
    }
    protected void populateTimesheetLineFromEntryDuringCreate(TSTimesheetLine
    _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
    {
        next populateTimesheetLineFromEntryDuringCreate(_tsTimesheetLine,
        _tsTimesheetEntry);
        this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
        _tsTimesheetEntry);
        }
        protected void populateTimesheetLineFromEntryDuringUpdate(TSTimesheetLine
        \_tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            next populateTimesheetLineFromEntryDuringUpdate(_tsTimesheetLine,
            _tsTimesheetEntry);
            this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
            _tsTimesheetEntry);
        }
        private void populateTimesheetLineFromCustomFields(TSTimesheetLine
        _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            ListEnumerator enumerator =
            _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    _tsTimesheetLine.TestLineString = customField.parmStringValue();
                }
            }
        }
    }
...
```

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a><span data-ttu-id="a6dc2-242">Afișați un câmp personalizat în secțiunea de antet a foii de pontaj</span><span class="sxs-lookup"><span data-stu-id="a6dc2-242">Show a custom field in the timesheet header section</span></span>

<span data-ttu-id="a6dc2-243">Mai jos este o captură de ecran din aplicația mobilă a unui utilizator care vizualizează o foaie de pontaj.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-243">Below is a screenshot from the mobile app of a user viewing a timesheet.</span></span> <span data-ttu-id="a6dc2-244">Butonul „Mai multe informații” a fost selectat în colțul din dreapta sus pentru a afișa opțiunea „Vizualizați mai multe detalii”.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-244">The "More information" button has been selected in the upper-right corner to show the "View more details" option.</span></span>  

![Afișați mai multe detalii de comandă](media/show-more.png)

<span data-ttu-id="a6dc2-246">Mai jos este o captură de ecran din aplicația mobilă care arată secțiunea „Mai multe” a unei foi de pontaj.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-246">Below is a screenshot from the mobile app showing the “More” section of a timesheet.</span></span> <span data-ttu-id="a6dc2-247">Un câmp personalizat numit „Rata de utilizare a acestei foi de pontaj (câmp personalizat calculat)” a fost adăugat la secțiunea de antet a foii de pontaj.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-247">A custom field called “Utilization rate of this timesheet (computed custom field)” has been added to the timesheet header section.</span></span> <span data-ttu-id="a6dc2-248">O valoare de numai în citire „0.667” este setată în câmpul personalizat.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-248">A read-only value of "0.667" is set on the custom field.</span></span>

![Mai multe secțiuni](media/more-section.jpg)

### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="a6dc2-250">Extindeți tabelul TSTimesheetTable astfel încât să aibă un câmp personalizat</span><span class="sxs-lookup"><span data-stu-id="a6dc2-250">Extend the TSTimesheetTable table so that it has a custom field</span></span>

<span data-ttu-id="a6dc2-251">În scenarii tipice, este probabil ca datele pentru un câmp personalizat din secțiunea de antet să fie extrase din tabelul TSTimesheetTable.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-251">In typical scenarios, it's likely that the data for a custom field in the header section will be pulled from the TSTimesheetHeader table.</span></span> <span data-ttu-id="a6dc2-252">Cu toate acestea, se pot utiliza și alte tabele dacă datele pot fi recuperate pe baza unei înregistrări TSTimesheetTable furnizate sau dacă nu au un context de înregistrare specific (de exemplu, dacă câmpul este setat ca numai în citire în parametrii proiectului) .</span><span class="sxs-lookup"><span data-stu-id="a6dc2-252">However, other tables can be used if the data can be retrieved based on a TSTimesheetTable record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="a6dc2-253">Rețineți că câmpurile personalizate nu trebuie să aibă nicio înregistrare de bază de date.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-253">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="a6dc2-254">Ele pot fi generate dinamic pe baza logicii X++.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-254">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="a6dc2-255">Exemplul care urmează arată această abordare.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-255">The example that follows shows this approach.</span></span>

<span data-ttu-id="a6dc2-256">Câmpurile din secțiunea antet sunt întotdeauna numai în citire în aplicație.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-256">Fields in the header section are always read-only in the app.</span></span>

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a><span data-ttu-id="a6dc2-257">Utilizați lanțul de comandă pe metoda buildCustomFieldList a clasei TSTimesheetSettings pentru a afișa un câmp în secțiunea de antet</span><span class="sxs-lookup"><span data-stu-id="a6dc2-257">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the header section</span></span>

<span data-ttu-id="a6dc2-258">Acest cod controlează setările de afișare pentru câmpul din aplicație.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-258">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="a6dc2-259">De exemplu, controlează tipul de câmp, eticheta, dacă câmpul este obligatoriu și în ce secțiune apare câmpul.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-259">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="a6dc2-260">Următorul exemplu arată o valoare calculată în secțiunea antet din aplicație.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-260">The following example shows a computed value in the header section in the app.</span></span>

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a><span data-ttu-id="a6dc2-261">Utilizați lanțul de comandă pe metoda buildCustomFieldListForHeader a clasei TSTimesheetDetails pentru a completa detaliile foii de pontaj</span><span class="sxs-lookup"><span data-stu-id="a6dc2-261">Use chain of command on the buildCustomFieldListForHeader method of the TSTimesheetDetails class to fill in timesheet details</span></span>

<span data-ttu-id="a6dc2-262">Metoda **buildCustomFieldListForHeader** este utilizată pentru a completa detaliile antetului foii de pontaj în aplicația mobilă.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-262">The **buildCustomFieldListForHeader** method is used to fill in the timesheet header details in the mobile app.</span></span> <span data-ttu-id="a6dc2-263">Este nevoie de o înregistrare TSTimesheetTable ca parametru.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-263">It takes a TSTimesheetTable record as a parameter.</span></span> <span data-ttu-id="a6dc2-264">Câmpurile din acea înregistrare pot fi folosite pentru a completa valoarea câmpului personalizat din aplicație.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-264">Fields from that record can be used to fill in the custom field value in the app.</span></span> <span data-ttu-id="a6dc2-265">Următorul exemplu nu citește nicio valoare din baza de date.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-265">The following example doesn't read any values from the database.</span></span> <span data-ttu-id="a6dc2-266">În schimb, folosește logica X++ pentru a genera o valoare calculată care este apoi afișată în aplicație.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-266">Instead, it uses X++ logic to generate a computed value that is then shown in the app.</span></span>


```xpp
...
[ExtensionOf(classStr(TSTimesheetDetails))]
final class TSTimesheetDetails_Extension
{
    protected List buildCustomFieldListForHeader(TSTimesheetTable
    _tsTimesheetTable)
    {
        List customFieldList = next buildCustomFieldListForHeader(_tsTimesheetTable);
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        real utilizationRate = 0;
        if (_tsTimesheetTable.totalHours() != 0)
        {
            utilizationRate = _tsTimesheetTable.totalHoursBillable() /
            _tsTimesheetTable.totalHours();
        }
        tsTimesheetCustomField.parmRealValue(utilizationRate);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

## <a name="other-configurabilityextensibility-opportunities"></a><span data-ttu-id="a6dc2-267">Alte posibilități de configurabilitate/extensibilitate</span><span class="sxs-lookup"><span data-stu-id="a6dc2-267">Other configurability/extensibility opportunities</span></span>

### <a name="adding-additional-validation-for-the-app"></a><span data-ttu-id="a6dc2-268">Adăugarea unei validări suplimentare pentru aplicație</span><span class="sxs-lookup"><span data-stu-id="a6dc2-268">Adding additional validation for the app</span></span>

<span data-ttu-id="a6dc2-269">Logica existentă pentru funcționalitatea foii de pontaj la nivelul bazei de date va funcționa în continuare așa cum era de așteptat.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-269">Existing logic for timesheet functionality at the database level will still work as expected.</span></span> <span data-ttu-id="a6dc2-270">Pentru a întrerupe finalizarea operațiilor de salvare sau trimitere și pentru a afișa un anumit mesaj de eroare, puteți adăuga **eroare de returnare („mesaj către utilizator”)** către cod printr-un lanț de extensie de comandă.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-270">To interrupt the completion of save or submit operations and show a specific error message, you can add **throw error("message to user")** to the code via a chain of command extension.</span></span> <span data-ttu-id="a6dc2-271">Iată trei exemple de metode extensibile utile:</span><span class="sxs-lookup"><span data-stu-id="a6dc2-271">Here are three examples of useful extensible methods:</span></span>

- <span data-ttu-id="a6dc2-272">Dacă **validateWrite** în tabelul TSTimesheetLine returnează **fals** în timpul unei operații de salvare pentru o linie de foaie de pontaj, un mesaj de eroare este afișat în aplicația mobilă.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-272">If **validateWrite** on the TSTimesheetLine table returns **false** during a save operation for a timesheet line, an error message is shown in the mobile app.</span></span>
- <span data-ttu-id="a6dc2-273">Dacă **validateSubmit** în tabelul TSTimesheetTable returnează **fals** în timpul trimiterii foii de pontaj în aplicație, un mesaj de eroare este afișat în aplicația mobilă.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-273">If **validateSubmit** on the TSTimesheetTable table returns **false** during timesheet submission in the app, an error message is shown to the user.</span></span>
- <span data-ttu-id="a6dc2-274">Logica care completează câmpuri (de exemplu, **Linia de proprietate**) în timpul metodei **inserare** de pe tabelul TSTimesheetLine va rula în continuare.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-274">Logic that fills in fields (for example, **Line Property**) during the **insert** method on the TSTimesheetLine table will still run.</span></span>

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a><span data-ttu-id="a6dc2-275">Ascunderea și marcarea câmpurilor predefinite ca doar citire prin configurare</span><span class="sxs-lookup"><span data-stu-id="a6dc2-275">Hiding and marking out-of-box fields as read-only via configuration</span></span>

<span data-ttu-id="a6dc2-276">Din parametrii proiectului, puteți crea câmpuri predefinite doar în citire sau ascunse în aplicația mobilă.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-276">From the project parameters, you can make out-of-box fields read-only or hidden in the mobile app.</span></span> <span data-ttu-id="a6dc2-277">Setați opțiunile din secțiunea **Fișe de pontaj mobile** de pe fila **Fișă de pontaj** din pagina **Managementul proiectului și parametrii contabili**.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-277">Set the options in the **Mobile timesheets** section on the **Timesheet** tab of the **Project management and accounting parameters** page.</span></span>

![Parametrii proiect](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a><span data-ttu-id="a6dc2-279">Schimbarea activităților disponibile pentru selectare prin extensii</span><span class="sxs-lookup"><span data-stu-id="a6dc2-279">Changing the activities that are available for selection via extensions</span></span>

<span data-ttu-id="a6dc2-280">Activitățile disponibile pentru selectarea unui proiect sunt completate prin intermediul metodelor **getActivitiesForProject()** și **getActivityQuery()** în clasa **TsTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-280">The activities that are available for selection for a project are filled in via the **getActivitiesForProject()** and **getActivityQuery()** methods in the **TsTimesheetProjectService** class.</span></span> <span data-ttu-id="a6dc2-281">Puteți utiliza lanțul de comandă pentru a modifica acest comportament pentru a se potrivi scenariului dvs. de afaceri pentru activitățile disponibile pentru selectare pentru un anumit proiect.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-281">You can use chain of command to change this behavior to match your business scenario for the activities that are available for selection for a specific project.</span></span>

### <a name="entering-a-default-project-category-on-timesheet-entries"></a><span data-ttu-id="a6dc2-282">Introducerea unei categorii de proiect implicite la intrările din foaia de pontaj</span><span class="sxs-lookup"><span data-stu-id="a6dc2-282">Entering a default project category on timesheet entries</span></span>

<span data-ttu-id="a6dc2-283">Introducerea unei categorii de proiect implicite la intrările din foaia de pontaj are loc la trei niveluri.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-283">Entry of a default project category on timesheet entries occurs at three levels.</span></span> <span data-ttu-id="a6dc2-284">Puteți utiliza lanțul de comandă pentru a extinde comportamentul la oricare sau la toate aceste niveluri pentru a atinge comportamentul dorit.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-284">You can use chain of command to extend the behavior at any or all of these levels to achieve the desired behavior.</span></span> <span data-ttu-id="a6dc2-285">Se utilizează următoarea ierarhie:</span><span class="sxs-lookup"><span data-stu-id="a6dc2-285">The following hierarchy is used:</span></span>

1. <span data-ttu-id="a6dc2-286">Aplicația încearcă să plaseze categoria implicită din resursa proiectului.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-286">The app tries to put the default category from the project resource.</span></span> <span data-ttu-id="a6dc2-287">Această categorie implicită este setată în metodele **getCurrentUserResource** și **getDelegatedResourcesForCurrentUser** în clasa **TSTimesheetSettingsService**.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-287">This default category is set in the **getCurrentUserResource** and **getDelegatedResourcesForCurrentUser** methods in the **TSTimesheetSettingsService** class.</span></span>
2. <span data-ttu-id="a6dc2-288">Dacă categoria implicită nu este furnizată la nivelul resurselor proiectului, aplicația încearcă să o retragă din activitatea proiectului.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-288">If the default category isn't provided at the project resource level, the app tries to pull it from the project activity.</span></span> <span data-ttu-id="a6dc2-289">Această categorie implicită este setată în metoda **getActivitiesForProject** în clasa **TSTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-289">This default category is set in the **getActivitiesForProject** method in the **TSTimesheetProjectService** class.</span></span>
3. <span data-ttu-id="a6dc2-290">Dacă categoria implicită nu este furnizată la nivelul activității proiectului, categoria implicită a fost luată din parametrii proiectului.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-290">If the default category isn't provided at the project activity level, the default category it taken from the project parameters.</span></span> <span data-ttu-id="a6dc2-291">Această categorie implicită este setată în metoda **getProjectDetailsbyRule** în clasa **TSTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="a6dc2-291">This default category is set in the **getProjectDetailsbyRule** method in the **TSTimesheetProjectService** class.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]