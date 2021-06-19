---
title: Lucrul cu cheltuieli personale pe un raport de cheltuieli
description: Acest subiect oferă informații despre cum să lucrați cu cheltuielile personale suportate de angajați în timp efectuează deplasări în interes de serviciu.
author: suvaidya
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: ae25eca08089d224f1e17e95eeb571054de8a5c0
ms.sourcegitcommit: fd6e9ff78392c7bac35591d9130c00d2750438ae
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 05/12/2021
ms.locfileid: "6025699"
---
# <a name="work-with-personal-expenses-on-an-expense-report"></a><span data-ttu-id="848c7-103">Lucrul cu cheltuieli personale pe un raport de cheltuieli</span><span class="sxs-lookup"><span data-stu-id="848c7-103">Work with personal expenses on an expense report</span></span>

<span data-ttu-id="848c7-104">_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_</span><span class="sxs-lookup"><span data-stu-id="848c7-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="848c7-105">În timpul deplasărilor în interes de serviciu, un angajat poate realiza cheltuieli personale pe cardul lor de credit corporativ.</span><span class="sxs-lookup"><span data-stu-id="848c7-105">During business travel, an employee might charge personal expenses to their corporate credit card.</span></span> <span data-ttu-id="848c7-106">Dacă nu a fost definit un proces pentru gestionarea cheltuielilor personale, procesul de aprobare a raportului de cheltuieli ar putea fi întrerupt atunci când un angajat prezintă raportul de cheltuieli detaliat.</span><span class="sxs-lookup"><span data-stu-id="848c7-106">If a process hasn't been defined for handling personal expenses, the expense report approval process might be disrupted when an employee submits their itemized expense report.</span></span>

<span data-ttu-id="848c7-107">Există două metode pe care le puteți utiliza pentru a lucra cu cheltuielile personale ale unui angajat:</span><span class="sxs-lookup"><span data-stu-id="848c7-107">There are two methods you can use to work with an employee's personal expenses:</span></span>

  - <span data-ttu-id="848c7-108">**Plătit de angajat**: Organizația dvs. nu plătește cheltuielile personale care apar pe factura pentru cardul de credit al companiei.</span><span class="sxs-lookup"><span data-stu-id="848c7-108">**Paid by employee**: Your organization doesn't pay personal expenses that appear on the bill for the corporate credit card.</span></span> <span data-ttu-id="848c7-109">În schimb, angajatul plătește direct furnizorului cardului de credit pentru cheltuieli.</span><span class="sxs-lookup"><span data-stu-id="848c7-109">Instead, the employee pays the credit card vendor directly for the expenses.</span></span> 
  - <span data-ttu-id="848c7-110">**Plătit de companie**: Organizația dvs. plătește factura completă pentru cardul de credit corporativ și apoi debitează contul angajatului pentru cheltuielile personale.</span><span class="sxs-lookup"><span data-stu-id="848c7-110">**Paid by company**: Your organization pays the full bill for the corporate credit card, and then debits the worker's account for the personal expenses.</span></span>

<span data-ttu-id="848c7-111">Puteți selecta metoda pe care organizația dvs. o folosește pe pagina **Parametrii de gestionare a cheltuielilor**.</span><span class="sxs-lookup"><span data-stu-id="848c7-111">You can select the method that your organization uses on the **Expense management parameters** page.</span></span>


## <a name="enable-split-expense-function-when-personal-amount-field-has-value-defined"></a><span data-ttu-id="848c7-112">Activați funcția de cheltuială divizată atunci când câmpul cu sumă personală are valoarea definită</span><span class="sxs-lookup"><span data-stu-id="848c7-112">Enable split expense function when personal amount field has value defined</span></span>

<span data-ttu-id="848c7-113">Caracteristica, **Activați funcția de cheltuială divizată atunci când câmpul cu sumă personală are valoarea definită** se aplică numai rapoartelor de cheltuieli care sunt aprobate utilizând un flux de lucru la nivel de linie.</span><span class="sxs-lookup"><span data-stu-id="848c7-113">The feature, **Enable split expense function when personal amount field has value defined** only applies to expense reports that are approved using a line-level workflow.</span></span> <span data-ttu-id="848c7-114">Rapoartele sunt aprobate accesând **Procesați rapoarte de cheltuieli** > **Rapoarte de cheltuieli care mi-au fost atribuite** > **Raport de cheltuieli deschis**.</span><span class="sxs-lookup"><span data-stu-id="848c7-114">Reports are approved by going to **Process expense reports** > **Expense reports assigned to me** > **Open expense report**.</span></span> 

<span data-ttu-id="848c7-115">Pentru a activa această caracteristică, accesați **Spații de lucru** > **Managementul caracteristicilor**, selectați **Activați funcția de cheltuială divizată atunci când câmpul cu sumă personală are valoarea definită**, apoi selectați **Activați acum**.</span><span class="sxs-lookup"><span data-stu-id="848c7-115">To enable this feature, go to **Workspaces** > **Feature Management**, select **Enable split expense function when personal amount field has value defined**, and then select **Enable now**.</span></span> 

<span data-ttu-id="848c7-116">Când funcția este activată, liniile de cheltuieli care utilizează această funcționalitate generează două linii atunci când raportul este trimis.</span><span class="sxs-lookup"><span data-stu-id="848c7-116">When the feature is enabled, expense lines that use this functionality generate two lines when the report is submitted.</span></span> <span data-ttu-id="848c7-117">Sunt generate două linii, astfel încât aprobatorul să poată aproba fiecare linie separat.</span><span class="sxs-lookup"><span data-stu-id="848c7-117">Two lines are generated so that the approver can approve each line separately.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
