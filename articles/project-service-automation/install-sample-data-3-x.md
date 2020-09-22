---
title: Instalare date eșantion
ms.custom: dyn365-projectservice
ms.date: 11/08/2018
ms.reviewer: kfend
ms.suite: ''
ms.technology: ''
applies_to: Dynamics 365 Project Service Automation
author: ruhercul
ms.assetid: 8580fc8b-868a-42a3-aa04-2afab28d6de4
ms.author: ruhercul
search.audienceType: IT Pro, Developer
search.app: ''
ms.openlocfilehash: 1c1300116fe42091620267fb128ca6c63184970e
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754671"
---
# <a name="sample-data-installation-for-the-project-service-application"></a><span data-ttu-id="0bed2-102">Instalarea datelor eșantion pentru aplicația Project Service</span><span class="sxs-lookup"><span data-stu-id="0bed2-102">Sample data installation for the Project Service application</span></span>

<span data-ttu-id="0bed2-103">Pentru a vă ajuta să creați propriile medii demonstartive, Microsoft furnizează pachete de date eșantion descărcabile ce evidențiază capacitățile aplicațiilor dvs.</span><span class="sxs-lookup"><span data-stu-id="0bed2-103">To help you build your own demo environments, Microsoft provides downloadable sample data packages that showcase the capabilities of your apps.</span></span> <span data-ttu-id="0bed2-104">Există două tipuri de pachete de date eșantion:</span><span class="sxs-lookup"><span data-stu-id="0bed2-104">There are two types of sample data packages:</span></span>
- <span data-ttu-id="0bed2-105">referință/configurare date</span><span class="sxs-lookup"><span data-stu-id="0bed2-105">reference/setup data</span></span>
- <span data-ttu-id="0bed2-106">Date demonstrative (referință/configurare și date tranzacționale, cum ar fi comenzi de lucru și proiecte)</span><span class="sxs-lookup"><span data-stu-id="0bed2-106">demo data (reference/setup and transactional data such as work orders and projects)</span></span>

<span data-ttu-id="0bed2-107">Pachetele de date eșantion pentru **referință** pot fi descărcate în trei pachete diferite, astfel încât să puteți instala date doar pentru Project Service sau doar pentru Field Service sau puteți instala date eșantion pentru ambele aplicații simultan.</span><span class="sxs-lookup"><span data-stu-id="0bed2-107">The sample **reference** data packages are downloadable in three different packages, so you can install data only for Project Service, or only for Field Service, or you can install sample data for both applications at once.</span></span>

<span data-ttu-id="0bed2-108">Pachetele de date eșantion pentru configurare/referință sunt:</span><span class="sxs-lookup"><span data-stu-id="0bed2-108">The sample setup/reference data packages are:</span></span>

- [<span data-ttu-id="0bed2-109">**V902PSMasterData** - doar Project Service versiunea 3.x</span><span class="sxs-lookup"><span data-stu-id="0bed2-109">**V902PSMasterData** - Project Service version 3.x only</span></span>](https://go.microsoft.com/fwlink/?linkid=2026540&clcid=0x409)

- [<span data-ttu-id="0bed2-110">**V902FSMasterData** - doar Field Service versiunea 8.x</span><span class="sxs-lookup"><span data-stu-id="0bed2-110">**V902FSMasterData** - Field Service version 8.x only</span></span>](https://go.microsoft.com/fwlink/?linkid=2026536&clcid=0x409)

- [<span data-ttu-id="0bed2-111">**V902FPSMasterData** - Field Service 8.x și Project Service 3.x</span><span class="sxs-lookup"><span data-stu-id="0bed2-111">**V902FPSMasterData** - Field Service 8.x and Project Service 3.x</span></span>](https://go.microsoft.com/fwlink/?linkid=2026041&clcid=0x409)

<span data-ttu-id="0bed2-112">Cel mai recent pachet de date **demonstrative** este:</span><span class="sxs-lookup"><span data-stu-id="0bed2-112">The latest **demo** data package is:</span></span>

 - [<span data-ttu-id="0bed2-113">**FPSDemoData** - Field Service 8.x și Project Service 3.x</span><span class="sxs-lookup"><span data-stu-id="0bed2-113">**FPSDemoData** - Field Service 8.x and Project Service 3.x</span></span>](https://aka.ms/fpsdemodatapackage)

   <span data-ttu-id="0bed2-114">Instrucțiunile de instalare diferă puțin în funcție de utilizatori pentru a crea și a configura secțiunea, dar restul rămâne ca în [**publicarea pe blog**](https://aka.ms/fpsdemodatablog) anterioară.</span><span class="sxs-lookup"><span data-stu-id="0bed2-114">Installation instructions differ slightly in the users to create and configure section but the rest is the same as in the previous [**blog post**](https://aka.ms/fpsdemodatablog).</span></span> <span data-ttu-id="0bed2-115">Acest pachet prezintă un set de date demonstrative redus și durează circa 3 ore pentru a se instala.</span><span class="sxs-lookup"><span data-stu-id="0bed2-115">This package features a reduced demo data set and takes approximately 3 hours to install.</span></span>

<span data-ttu-id="0bed2-116">Aceste pachete de date eșantion sunt disponibile numai în limba engleză.</span><span class="sxs-lookup"><span data-stu-id="0bed2-116">These sample data packages are available in English only.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0bed2-117">**Nu există nicio modalitate de a dezinstala datele eșantion.**</span><span class="sxs-lookup"><span data-stu-id="0bed2-117">**There is no way to uninstall the sample data.**</span></span> <span data-ttu-id="0bed2-118">Trebuie să instalați aceste pachete numai pe sisteme demonstrative, de evaluare, instruire și testare.</span><span class="sxs-lookup"><span data-stu-id="0bed2-118">You should only install these packages on demonstration, evaluation, training, or test systems.</span></span> <span data-ttu-id="0bed2-119">De asemenea, rețineți că instalarea unui pachet individual și instalarea celuilalt pachet individual nu este acceptată.</span><span class="sxs-lookup"><span data-stu-id="0bed2-119">Also note that installing an individual package, and then installing the other individual package, is not supported.</span></span> <span data-ttu-id="0bed2-120">(Cu alte cuvinte, nu se poate instala **FSMasterData** urmat de **PSMasterData** sau viceversa.) Dacă se întâmplă să aveți nevoie de date eșantion pentru ambele aplicații în orice moment în viitor, ar trebui să instalați pachetul **v902FPSMasterData**.</span><span class="sxs-lookup"><span data-stu-id="0bed2-120">(In other words, you can't install **FSMasterData** followed by **PSMasterData**, or vice versa.) If you see yourself needing sample data for both applications at any point in the future, you should install the **v902FPSMasterData** package.</span></span>

<span data-ttu-id="0bed2-121">Atunci când instalați oricare dintre pachetele de date eșantion, procesul de instalare efectuează următoarele acțiuni:</span><span class="sxs-lookup"><span data-stu-id="0bed2-121">When you install any of the sample data packages, the installation process performs the following actions:</span></span>

- <span data-ttu-id="0bed2-122">Creează sau setează parametri impliciți pentru a folosi Project Service, Field Service sau ambele aplicații (după caz).</span><span class="sxs-lookup"><span data-stu-id="0bed2-122">Creates or sets default parameters for using Project Service, Field Service, or both applications (if applicable).</span></span>

- <span data-ttu-id="0bed2-123">Importă date esantion pentru aplicații, cum ar fi resurse ce se pot rezerva, roluri specifice aplicațiilor, liste de vânzări și de prețuri, unități organizaționale, înregistrări ale procesului de vânzări și alte entități pentru a demonstra capacitățile cheie.</span><span class="sxs-lookup"><span data-stu-id="0bed2-123">Imports sample data for the applications, such as bookable resources, application-specific roles, sales and cost price lists, organizational units, sales process records, and other entities to demonstrate key capabilities.</span></span>  

<span data-ttu-id="0bed2-124">Cu pachetul de **date demonstrative**, veți obține datele tranzacționale de mai sus, precum și date tranzacționale suplimentare, cum ar fi comenzi de lucru și proiecte.</span><span class="sxs-lookup"><span data-stu-id="0bed2-124">With the **demo data** package, you get the above and additional transactional data such as work orders and projects.</span></span>

<span data-ttu-id="0bed2-125">Vă întrebați ce capabilități puteți demonstra cu date eșantion?</span><span class="sxs-lookup"><span data-stu-id="0bed2-125">Wondering what capabilities you can demo with the sample data?</span></span> <span data-ttu-id="0bed2-126">Consultați scenariul fictiv Fabrikam Robotics din [Note tehnice](#technical-notes).</span><span class="sxs-lookup"><span data-stu-id="0bed2-126">See the Fabrikam Robotics fictitious scenario in [Technical notes](#technical-notes).</span></span>

<span data-ttu-id="0bed2-127">Dacă aveți întrebări despre instalarea acestor pachete de date eșantion, [trimiteți-ne un e-mail la fpsdemodata@microsoft.com](mailto:fpsdemodata@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="0bed2-127">If you have questions about installing these sample data packages, [send us an email at fpsdemodata@microsoft.com](mailto:fpsdemodata@microsoft.com).</span></span>

## <a name="requirements"></a><span data-ttu-id="0bed2-128">Cerințe</span><span class="sxs-lookup"><span data-stu-id="0bed2-128">Requirements</span></span>

<span data-ttu-id="0bed2-129">Protocolul de instalare presupune următoarele despre instanța (organizația) dvs. țintă:</span><span class="sxs-lookup"><span data-stu-id="0bed2-129">The installation protocol assumes the following about your target instance (org):</span></span>

- <span data-ttu-id="0bed2-130">Limba de bază este limba engleză, iar moneda de bază este dolarul american (USD, $).</span><span class="sxs-lookup"><span data-stu-id="0bed2-130">Base language is English and base currency is US dollar (USD,$).</span></span>

- <span data-ttu-id="0bed2-131">Organizația nu are pregătite date Project Service sau Field Service sau are doar date de bază implicite care vin cu orice organizație nouă.</span><span class="sxs-lookup"><span data-stu-id="0bed2-131">The org has no Project Service or Field Service data already, or only has barebones default data that comes with any new org.</span></span>

- <span data-ttu-id="0bed2-132">Versiunea corectă a aplicației de afaceri este instalată deja:</span><span class="sxs-lookup"><span data-stu-id="0bed2-132">The correct version of the business application is already installed:</span></span>
       
    - <span data-ttu-id="0bed2-133">**Pentru FPSDemoData sau v902FPSMasterData:** organizația are instalată Field Service versiunea 8.x și Project Service versiunea 3.x.</span><span class="sxs-lookup"><span data-stu-id="0bed2-133">**For FPSDemoData or v902FPSMasterData:** The org has Field Service version 8.x and Project Service version 3.x installed.</span></span>

    - <span data-ttu-id="0bed2-134">**Pentru v902PSMasterData:** organizația are instalată Project Service versiunea 3.x.</span><span class="sxs-lookup"><span data-stu-id="0bed2-134">**For v902PSMasterData:** The org has Project Service version 3.x installed.</span></span>

    - <span data-ttu-id="0bed2-135">**Pentru v902FSMasterData:** organizația are instalată Field Service versiunea 8.x.</span><span class="sxs-lookup"><span data-stu-id="0bed2-135">**For v902FSMasterData:** The org has Field Service version 8.x installed.</span></span>

> [!NOTE]
> <span data-ttu-id="0bed2-136">Dacă trebuie să instalați datele eșantion peste versiunea de încercare sau mediul demonstrativ Project Service și Field Service care are deja date (nu este recomandat), va trebui să suspendați verificările preliminare de siguranță efectuate de programul de instalare.</span><span class="sxs-lookup"><span data-stu-id="0bed2-136">If you need to install the sample data on top of an existing Project Service and Field Service trial or demo environment that already has data (not recommended), you'll need to suspend the safety prechecks performed by the installer.</span></span> <span data-ttu-id="0bed2-137">Pentru mai multe informații, consultați notele tehnice de mai jos.</span><span class="sxs-lookup"><span data-stu-id="0bed2-137">For more information, see the technical notes below.</span></span>

## <a name="prepare-for-installation"></a><span data-ttu-id="0bed2-138">Pregătirea instalării</span><span class="sxs-lookup"><span data-stu-id="0bed2-138">Prepare for installation</span></span>

<span data-ttu-id="0bed2-139">Trebuie să rulați programul de instalare pe un computer cu o versiune recentă de Windows (preferabil Windows 10).</span><span class="sxs-lookup"><span data-stu-id="0bed2-139">You need to run the installer on a computer with a recent version of Windows (Windows 10 preferred).</span></span>

<span data-ttu-id="0bed2-140">Ar trebui să planificați ca acel computer să rămână conectat la o rețea, și ca instalarea să ruleze până la **1 oră** pentru **date pentru configurare/referință**.</span><span class="sxs-lookup"><span data-stu-id="0bed2-140">You should plan for the computer to remain connected to a network, and for the installation to run for up to **1 hour** for **setup/reference data**.</span></span> <span data-ttu-id="0bed2-141">(În mod normal, instalarea durează aproximativ 30 de minute pentru **FPSMasterData**, care include date eșantion pentru ambele aplicații.) Pentru **FPSDemoData**, instalarea va lua circa **3 ore**.</span><span class="sxs-lookup"><span data-stu-id="0bed2-141">(Normally the installation takes around 30 minutes for **FPSMasterData**, which includes sample data for both applications.) For the **FPSDemoData**, the installation will take around **3 hours**.</span></span>

<span data-ttu-id="0bed2-142">Computerul trebuie să aibă dezactivată funcția Economizor de ecran.</span><span class="sxs-lookup"><span data-stu-id="0bed2-142">The computer should have the screen saver function turned off.</span></span> <span data-ttu-id="0bed2-143">În caz contrar, acreditările de sesiune pentru instalare se pot pierde atunci când economizorul de ecran se angajează (cu excepția cazului în care păstrați sesiunea activă).</span><span class="sxs-lookup"><span data-stu-id="0bed2-143">Otherwise, session credentials for the installation may be lost when the screen saver engages (unless you keep your session active throughout).</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="0bed2-144">![Captură de ecran a setărilor de economizor de ecran, cu economizorul de ecran oprit](media/sample-data-1.png)</span><span class="sxs-lookup"><span data-stu-id="0bed2-144">![Screenshot of screen saver settings, with screen saver turned off](media/sample-data-1.png)</span></span>

## <a name="download-and-unpack"></a><span data-ttu-id="0bed2-145">Descărcați și dezarhivați</span><span class="sxs-lookup"><span data-stu-id="0bed2-145">Download and unpack</span></span>

<span data-ttu-id="0bed2-146">Programul de instalare a datelor eșantion Project Service și Field Service este distribuit ca executabil cu extragere automată.</span><span class="sxs-lookup"><span data-stu-id="0bed2-146">The Project Service and Field Service sample data installer is distributed as a self-extracting executable.</span></span> <span data-ttu-id="0bed2-147">Numele fișierului poate varia, în funcție de pachetul de date eșantion, dar, altfel, pașii sunt aceieași indiferent ce pachet instalați.</span><span class="sxs-lookup"><span data-stu-id="0bed2-147">The file names may vary depending on the sample data package, but otherwise the steps are the same no matter which package you install.</span></span>

<span data-ttu-id="0bed2-148">După descărcarea unui pachet, rulați fișierul .exe, apoi acceptați termenii și condițiile pentru a dezarhiva fișierul zip comprimat.</span><span class="sxs-lookup"><span data-stu-id="0bed2-148">After downloading a package, run the .exe file, and then accept terms and conditions to unpack the compressed zip file.</span></span> <span data-ttu-id="0bed2-149">Apoi trebuie să extrageți conținutul acelui fișier într-un folder de pe computer.</span><span class="sxs-lookup"><span data-stu-id="0bed2-149">You then need to extract contents of that file to a folder on the computer.</span></span>

<span data-ttu-id="0bed2-150">În funcție de sistemul de operare și de setările de securitate, poate fi necesar să efectuați următorii pași după dezarhivarea fișierului zip:</span><span class="sxs-lookup"><span data-stu-id="0bed2-150">Depending on the operating system and security settings, you may need to perform the following steps after unpacking the zip file:</span></span>

1. <span data-ttu-id="0bed2-151">Găsiți și faceți clic dreapta pe fișierul **FPSDemoData.dll** din folderul **v902FPSMasterData** / **PackageDeployer_FPSDemoData**.</span><span class="sxs-lookup"><span data-stu-id="0bed2-151">Find and right-click the **FPSDemoData.dll** file in the **v902FPSMasterData** / **PackageDeployer_FPSDemoData** folder.</span></span>

2. <span data-ttu-id="0bed2-152">Alegeți **Deblocare**.</span><span class="sxs-lookup"><span data-stu-id="0bed2-152">Choose **Unblock**.</span></span>

3. <span data-ttu-id="0bed2-153">Selectați **Se aplică**.</span><span class="sxs-lookup"><span data-stu-id="0bed2-153">Select **Apply**.</span></span>

4. <span data-ttu-id="0bed2-154">Selectați **OK**.</span><span class="sxs-lookup"><span data-stu-id="0bed2-154">Select **OK**.</span></span>


## <a name="create-or-configure-users"></a><span data-ttu-id="0bed2-155">Creați sau configurați utilizatorii</span><span class="sxs-lookup"><span data-stu-id="0bed2-155">Create or configure users</span></span>

<span data-ttu-id="0bed2-156">Pachetul **FPSDemoData** necesită șase utilizatori, în timp ce pachetele **FPSMasterData** au nevoie de un singur utilizator.</span><span class="sxs-lookup"><span data-stu-id="0bed2-156">The **FPSDemoData** package requires six users while **FPSMasterData** packages require one user.</span></span> <span data-ttu-id="0bed2-157">Consultați-l pe cel corect pentru pachetul dvs. de date eșantion.</span><span class="sxs-lookup"><span data-stu-id="0bed2-157">Refer to the correct one for your sample data package.</span></span>

## <a name="create-or-configure-users---setupreference-data-packages"></a><span data-ttu-id="0bed2-158">Crearea sau configurarea utilizatorilor - pachete de date pentru configurare/referință</span><span class="sxs-lookup"><span data-stu-id="0bed2-158">Create or configure users - setup/reference data packages</span></span>

<span data-ttu-id="0bed2-159">Pachetul **FPSMasterData** este conceput pentru a fi instalat cu un utilizator numit Spencer Low, cu setarile descrise aici.</span><span class="sxs-lookup"><span data-stu-id="0bed2-159">The **FPSMasterData** package is designed to install with one user named Spencer Low with the settings described here.</span></span> <span data-ttu-id="0bed2-160">Pentru a instala pachetul corect, aveți nevoie să creați (sau să redenumiți temporar) utilizatori în mediul dvs., pentru a se potrivi configurației de date eșantion primite.</span><span class="sxs-lookup"><span data-stu-id="0bed2-160">To install the package correctly, you need to create (or temporarily rename) users in your environment to match the incoming sample data configuration.</span></span>

<span data-ttu-id="0bed2-161">Pentru a crea sau a configura utilizatori, accesați **Setări** > **Securitate** > **Utilizatori** și efectuați următoarele:</span><span class="sxs-lookup"><span data-stu-id="0bed2-161">To create or configure users, go to **Settings** > **Security** > **Users**, and do the following:</span></span>

1. <span data-ttu-id="0bed2-162">Setați UserFullname="Spencer Low" cu numele "spencerl" (**litere mici**) la rolurile Manager de proiect și Manager de practică.</span><span class="sxs-lookup"><span data-stu-id="0bed2-162">Set UserFullname="Spencer Low" with username "spencerl" (**lowercase**) to the Project Manager and Practice Manager roles.</span></span>

2. <span data-ttu-id="0bed2-163">Selectați utilizatorul **Spencer Low** și apoi selectați **Gestionare roluri**.</span><span class="sxs-lookup"><span data-stu-id="0bed2-163">Select the **Spencer Low** user, and then select **Manage Roles**.</span></span> <span data-ttu-id="0bed2-164">Găsiți și selectați rolul **Administrator de sistem**, apoi selectați **OK** pentru a acorda drepturi de administrator complete utilizatorului Spencer Low.</span><span class="sxs-lookup"><span data-stu-id="0bed2-164">Find and select the **System Administrator** role, and then select **OK** to grant full admin rights to Spencer Low.</span></span> <span data-ttu-id="0bed2-165">Acest pas este necesar pentru a asigura că înregistrările eșantion sunt create cu dreptul de proprietate de utilizator corect și, prin urmare, populează corect vizualizările.</span><span class="sxs-lookup"><span data-stu-id="0bed2-165">This step is necessary to ensure that sample records are created with the correct user ownership and therefore populate views correctly.</span></span>

3. <span data-ttu-id="0bed2-166">Din pachetul descărcat, trebuie să actualizați un fișier de mapare de date cu adresele de e-mail ale contextului de utilizator implicit.</span><span class="sxs-lookup"><span data-stu-id="0bed2-166">From the downloaded package, you need to update a data mapping file with email addresses of the default user context.</span></span> <span data-ttu-id="0bed2-167">Pentru a face asta, deschideți **PkgFolder** și apoi găsiți și deschideți fișierul **ImportUserMapFile.xml** în Notepad (sau Visual Studio sau alt editor XML).</span><span class="sxs-lookup"><span data-stu-id="0bed2-167">To do this, open **PkgFolder**, and then find and open the **ImportUserMapFile.xml** file in Notepad (or Visual Studio or another XML editor).</span></span> <span data-ttu-id="0bed2-168">Setați câmpul **DefaultUserToMapTo=** la adresa de e-mail a utilizatorului Spencer Low.</span><span class="sxs-lookup"><span data-stu-id="0bed2-168">Set the **DefaultUserToMapTo=** field to the email address of the Spencer Low user.</span></span>

4. <span data-ttu-id="0bed2-169">Dacă nu utilizați Spencer Low cu numele de utilizator **spencerl**, trebuie să actualizați un fișier suplimentar.</span><span class="sxs-lookup"><span data-stu-id="0bed2-169">If you aren't using Spencer Low with username **spencerl**, you need to update an additional file.</span></span> <span data-ttu-id="0bed2-170">Deschideți fișierul **DemoDataPreImportConfig.xml**, apoi găsiți eticheta **userstocreateandconfigure**.</span><span class="sxs-lookup"><span data-stu-id="0bed2-170">Open the **DemoDataPreImportConfig.xml** file, and then find the **userstocreateandconfigure** tag.</span></span> <span data-ttu-id="0bed2-171">Actualizați eticheta **\<conectare\>** cu numele de utilizator al utilizatorului Spencer Low.</span><span class="sxs-lookup"><span data-stu-id="0bed2-171">Update the **\<login\>** tag with the username of your Spencer Low user.</span></span> <span data-ttu-id="0bed2-172">Pentru detalii suplimentare, consultați [Note tehnice](#technical-notes).</span><span class="sxs-lookup"><span data-stu-id="0bed2-172">For additional details, see [Technical notes](#technical-notes).</span></span>

## <a name="create-or-configure-users---demo-data-package"></a><span data-ttu-id="0bed2-173">Crearea sau configurarea utilizatorilor - pachet de date demonstrative</span><span class="sxs-lookup"><span data-stu-id="0bed2-173">Create or configure users - demo data package</span></span>

<span data-ttu-id="0bed2-174">Pachetul de date demonstrative necesită șase utilizatori.</span><span class="sxs-lookup"><span data-stu-id="0bed2-174">The demo data package requires six users.</span></span> <span data-ttu-id="0bed2-175">Pentru instalarea corectă a pachetului, efectuați următoarele:</span><span class="sxs-lookup"><span data-stu-id="0bed2-175">For the package to install correctly, do the following:</span></span>

 1. <span data-ttu-id="0bed2-176">Creați sau redenumiți temporar utilizatorii existenți pentru a se potrivi configurației de date eșantion primite accesând **Setări** > **Securitate** > **Utilizatori**.</span><span class="sxs-lookup"><span data-stu-id="0bed2-176">Create or temporarily rename existing users to match incoming sample data configuration by going to **Settings** > **Security** > **Users**.</span></span>
 
    <span data-ttu-id="0bed2-177">Aceste roluri sunt necesare numai pentru demonstrațiile în care sunt implicate persoane.</span><span class="sxs-lookup"><span data-stu-id="0bed2-177">These roles are only needed for persona-based demos.</span></span>  
    - <span data-ttu-id="0bed2-178">Utilizator Fullname="David So" tehnician Field Service</span><span class="sxs-lookup"><span data-stu-id="0bed2-178">User Fullname="David So" as Field Service Technician</span></span>   
    - <span data-ttu-id="0bed2-179">Utilizator Fullname="Jamie Reding" ca Dispecer Customer Service & Field Service</span><span class="sxs-lookup"><span data-stu-id="0bed2-179">User Fullname="Jamie Reding" as Customer Service & Field Service Dispatcher</span></span>   
    - <span data-ttu-id="0bed2-180">Utilizator Fullname="Molly Clark" ca Manager de cont</span><span class="sxs-lookup"><span data-stu-id="0bed2-180">User Fullname="Molly Clark" as Account Manager</span></span>   
    - <span data-ttu-id="0bed2-181">Utilizator Fullname="Spencer Low" ca Manager de practică și Manager de proiect</span><span class="sxs-lookup"><span data-stu-id="0bed2-181">User Fullname="Spencer Low" as Practice and Project Manager</span></span>  
    - <span data-ttu-id="0bed2-182">Utilizator Fullname="Veronica Quek" ca Membru echipă</span><span class="sxs-lookup"><span data-stu-id="0bed2-182">User Fullname="Veronica Quek" as Team Member</span></span>   
    - <span data-ttu-id="0bed2-183">Utilizator Fullname="William Contoso"</span><span class="sxs-lookup"><span data-stu-id="0bed2-183">User Fullname="William Contoso"</span></span>
  
2. <span data-ttu-id="0bed2-184">Pentru a importa datele demonstrative, atribuiți cei șase utilizatori deasupra rolului de Administrator, astfel încât înregistrările eșantion să fie importate corect.</span><span class="sxs-lookup"><span data-stu-id="0bed2-184">For the purposes of demo data import, assign the six users above the Administrator role so sample records import correctly.</span></span> 

3. <span data-ttu-id="0bed2-185">Deschideți **PkgFolder**, iar apoi găsiți și deschideți **ImportUserMapFile.xml**.</span><span class="sxs-lookup"><span data-stu-id="0bed2-185">Open **PkgFolder** and then find and open **ImportUserMapFile.xml**.</span></span> <span data-ttu-id="0bed2-186">Actualizați câmpurile **Nou=** la adresele de e-mail ale utilizatorilor corespunzători din sistemul dvs.</span><span class="sxs-lookup"><span data-stu-id="0bed2-186">Update the **New=** fields to the email addresses of corresponding Users in your system.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="0bed2-187">![Captură de ecran a UserMapFile](media/sample-data-7.png)</span><span class="sxs-lookup"><span data-stu-id="0bed2-187">![Screen shot of UserMapFile](media/sample-data-7.png)</span></span>

4. <span data-ttu-id="0bed2-188">În cazul în care numele complet "Spencer Low" al utilizatorului are un ID de utilizator diferit de **"spencerl"**, trebuie să actualizați un fișier suplimentar.</span><span class="sxs-lookup"><span data-stu-id="0bed2-188">If your "Spencer Low" full name user has a different user ID than **"spencerl"**, then you need to update an additional file.</span></span> <span data-ttu-id="0bed2-189">Deschideți **DemoDataPreImportConfig.xml** și găsiți eticheta **userstocreateandconfigure**.</span><span class="sxs-lookup"><span data-stu-id="0bed2-189">Open **DemoDataPreImportConfig.xml** and find the **userstocreateandconfigure** tag.</span></span> <span data-ttu-id="0bed2-190">Actualizați eticheta **\<conectare\>** cu Id conectare(sensibil la litere mari și mici).</span><span class="sxs-lookup"><span data-stu-id="0bed2-190">Update the **\<login\>** tag with the loginId (case-sensitive).</span></span> 

5. <span data-ttu-id="0bed2-191">Primul calendar al utilizatorului (în eticheta **userstocreateandconfigure**) este folosit pentru a popula orele de lucru pentru toate resursele care se pot rezerva la importul de date demonstrative.</span><span class="sxs-lookup"><span data-stu-id="0bed2-191">The first user's calendar (in the **userstocreateandconfigure** tag) is used to populate the work hours for all bookable resources on import of demo data.</span></span> <span data-ttu-id="0bed2-192">Navigați la **Setări** > **Securitate** > **Utilizatori**, găsiți utilizatorul "Spencer Low" și deschideți opțiunea „Ore de lucru”.</span><span class="sxs-lookup"><span data-stu-id="0bed2-192">Navigate to **Settings** > **Security** > **Users**, find your "Spencer Low" user, and open the "Work Hours" option.</span></span> <span data-ttu-id="0bed2-193">Editați orele de lucru existente, selectând opțiunea **Planificare săptămânală recurentă în totalitate de la început la sfârșit**.</span><span class="sxs-lookup"><span data-stu-id="0bed2-193">Edit the existing work hours, selecting the **Entire recurring weekly schedule from start to end** option.</span></span> <span data-ttu-id="0bed2-194">Asigurați-vă că **Orele de lucru sunt setate pentru 08:00-17:00 (9 ore), de luni până vineri și cu fusul orar stabilit la ora Pacificului (SUA și Canada)**.</span><span class="sxs-lookup"><span data-stu-id="0bed2-194">Ensure the **Work hours are set to 8 AM - 5 PM (9 Hours), Monday to Friday and with the Timezone set to Pacific Time (US & Canada)**.</span></span> <span data-ttu-id="0bed2-195">Acest lucru este necesar pentru a garanta că panoul de Proiect și Planificare este conform așteptărilor.</span><span class="sxs-lookup"><span data-stu-id="0bed2-195">This is needed to ensure that the Project and Schedule board show as expected.</span></span>

<span data-ttu-id="0bed2-196">**Recomandare:** luați în considerare crearea unei copii backup a organizației dvs. acum, în cazul în care trebuie să reveniți la punctul de plecare dacă ceva nu merge bine în timpul instalării datelor eșantion.</span><span class="sxs-lookup"><span data-stu-id="0bed2-196">**Recommendation:** Consider creating a backup of your org now, in case you need to revert to your starting point if something goes wrong during the sample data installation.</span></span> <span data-ttu-id="0bed2-197">Pentru informații suplimentare, consultați [Backupul și restaurarea instanțelor](https://docs.microsoft.com/dynamics365/customer-engagement/admin/backup-restore-instances).</span><span class="sxs-lookup"><span data-stu-id="0bed2-197">For more information, see [Backup and restore instances](https://docs.microsoft.com/dynamics365/customer-engagement/admin/backup-restore-instances).</span></span>

## <a name="run-the-package-deployer"></a><span data-ttu-id="0bed2-198">Rulați Package Deployer</span><span class="sxs-lookup"><span data-stu-id="0bed2-198">Run the Package Deployer</span></span>

1. <span data-ttu-id="0bed2-199">Găsiți și rulați **PackageDeployer.exe** în folderul **v902FPSMasterData** SAU **PackageDeployer_FPSDemoData**.</span><span class="sxs-lookup"><span data-stu-id="0bed2-199">Find and run **PackageDeployer.exe** in the **v902FPSMasterData** OR **PackageDeployer_FPSDemoData** folder.</span></span>

2. <span data-ttu-id="0bed2-200">Acceptați termenii și condițiile</span><span class="sxs-lookup"><span data-stu-id="0bed2-200">Accept the terms and conditions.</span></span>

3. <span data-ttu-id="0bed2-201">În fereastra următoare:</span><span class="sxs-lookup"><span data-stu-id="0bed2-201">On the next window:</span></span>

   <span data-ttu-id="0bed2-202">a.</span><span class="sxs-lookup"><span data-stu-id="0bed2-202">a.</span></span> <span data-ttu-id="0bed2-203">Selectați tipul de implementare **Office 365**.</span><span class="sxs-lookup"><span data-stu-id="0bed2-203">Select deployment type **Office 365**.</span></span>

   <span data-ttu-id="0bed2-204">b.</span><span class="sxs-lookup"><span data-stu-id="0bed2-204">b.</span></span> <span data-ttu-id="0bed2-205">Utilizați utilizatorul și parola utilizatorului administrator de sistem configurat în „Creați sau configurați utilizatori” („Spencer Low” cu numele de utilizator „spencerl”).</span><span class="sxs-lookup"><span data-stu-id="0bed2-205">Use the user and password of the system administrator user configured in "Create or configure users" ("Spencer Low" with "spencerl" username).</span></span>

   <span data-ttu-id="0bed2-206">c.</span><span class="sxs-lookup"><span data-stu-id="0bed2-206">c.</span></span> <span data-ttu-id="0bed2-207">Asigurați-vă că ați bifat **Afișați lista de organizații disponibile**.</span><span class="sxs-lookup"><span data-stu-id="0bed2-207">Make sure **Display list of available organizations** is selected.</span></span>

      > [!div class="mx-imgBorder"]
      > <span data-ttu-id="0bed2-208">![Captură de ecran a ferestrei Package Deployer cu opțiunea „Afișați lista de organizații disponibile” selectată](media/sample-data-2.png)</span><span class="sxs-lookup"><span data-stu-id="0bed2-208">![Screenshot of Package Deployer window with "Display list of available organizations" selected](media/sample-data-2.png)</span></span>

4. <span data-ttu-id="0bed2-209">Selectați organizația unde doriți să instalați date eșantion.</span><span class="sxs-lookup"><span data-stu-id="0bed2-209">Select the organization where you want to install the sample data.</span></span>

5. <span data-ttu-id="0bed2-210">Selectați **Următorul** până când vedeți caseta de dialog **Configurare date demonstrative**.</span><span class="sxs-lookup"><span data-stu-id="0bed2-210">Select **Next** until you see the **Demo Data Setup** dialog.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="0bed2-211">![Captură de ecran a ferestrei de stare a instalatorului de date demonstrative](media/sample-data-3.png)</span><span class="sxs-lookup"><span data-stu-id="0bed2-211">![Screenshot of the demo data installer status window](media/sample-data-3.png)</span></span>

6. <span data-ttu-id="0bed2-212">Înainte de a continua, rețineți că instalarea datelor eșantion ar putea dura până la o oră (în mod normal, durează cam 10 minute).</span><span class="sxs-lookup"><span data-stu-id="0bed2-212">Before proceeding, note that installing sample data could take up to one hour (normally ~10 minutes).</span></span> <span data-ttu-id="0bed2-213">Va trebui să vă asigurați că rămâne pornit și conectat la o rețea computerul în timpul procesului de instalare și că sesiunea rămâne activă.</span><span class="sxs-lookup"><span data-stu-id="0bed2-213">You'll need to make sure the computer remains on and connected to a network throughout the installation process, and that your session remains active.</span></span>   

7. <span data-ttu-id="0bed2-214">Când sunteți gata, faceți clic pe **Următorul** pentru a începe procesul de instalare a datelor eșantion.</span><span class="sxs-lookup"><span data-stu-id="0bed2-214">When you're ready, click **Next** to start the sample data installation process.</span></span> <span data-ttu-id="0bed2-215">După ce sunt încărcate datele eșantion, faceți clic pe **Terminare**.</span><span class="sxs-lookup"><span data-stu-id="0bed2-215">After the sample data is loaded, click **Finish**.</span></span>

## <a name="verify-the-sample-data-installation"></a><span data-ttu-id="0bed2-216">Verificați instalarea datelor eșantion</span><span class="sxs-lookup"><span data-stu-id="0bed2-216">Verify the sample data installation</span></span>

<span data-ttu-id="0bed2-217">Pentru o verificare a funcționării, verificați dacă numărul de înregistrări și tipuri de entități listate in scenariul fictiv Fabrikam Robotics apar așa cum vă așteptați.</span><span class="sxs-lookup"><span data-stu-id="0bed2-217">For a sanity check, verify that the number of records and types of entities listed in Fabrikam Robotics fictitious scenario appear as expected.</span></span>

<span data-ttu-id="0bed2-218">După încărcarea completă a datelor eșantion, conectați-vă ca utilizatorul Spencer Low și confirmați următoarele:</span><span class="sxs-lookup"><span data-stu-id="0bed2-218">After the sample data completely loads, sign in as the Spencer Low user and confirm the following:</span></span>

- <span data-ttu-id="0bed2-219">Dacă este instalată aplicația Project Service, accesați **Project Service** > **Setări** > **Liste de prețuri**.</span><span class="sxs-lookup"><span data-stu-id="0bed2-219">If the Project Service application is installed, go to **Project Service** > **Settings** > **Price Lists**.</span></span> <span data-ttu-id="0bed2-220">Confirmați dacă sumele de facturare și costurile există cu moneda corespunzătoare pentru fiecare țară/regiune din setul de date.</span><span class="sxs-lookup"><span data-stu-id="0bed2-220">Confirm that bill rates and costs rates exist with the appropriate currency for each country/region in the data set.</span></span>

- <span data-ttu-id="0bed2-221">Dacă este instalată aplicația Project Service, accesați **Universal Resource Scheduling** > **Setări** > **Unități organizaționale**.</span><span class="sxs-lookup"><span data-stu-id="0bed2-221">If the Project Service application is installed, go to **Universal Resource Scheduling** > **Settings** > **Organizational Units**.</span></span> <span data-ttu-id="0bed2-222">Confirmați dacă a fost asociată o listă de prețuri cu moneda corespunzătoare cu fiecare unitate de organizație (cu excepția intrărilor de oraș).</span><span class="sxs-lookup"><span data-stu-id="0bed2-222">Confirm that a cost price list with the appropriate currency has been associated with each org unit (excluding city entries).</span></span> <span data-ttu-id="0bed2-223">În cazul în care oricare lipsește, găsiți și asociați lista de prețuri corectă.</span><span class="sxs-lookup"><span data-stu-id="0bed2-223">If any are missing, find and associate the correct cost price list.</span></span>

- <span data-ttu-id="0bed2-224">Dacă este instalată aplicația Field Service, accesați **Project Service** > **Setări** > **Liste de prețuri**.</span><span class="sxs-lookup"><span data-stu-id="0bed2-224">If the Field Service application is installed, go to **Project Service** > **Settings** > **Price Lists**.</span></span> <span data-ttu-id="0bed2-225">Confirmați că tarifele și costurile există.</span><span class="sxs-lookup"><span data-stu-id="0bed2-225">Confirm that bill rates and costs rates exist.</span></span> <span data-ttu-id="0bed2-226">Accesați **Field Service** > **Setări** > **Liste de prețuri** și verificați dacă sumele de facturare și costurile există, cu moneda corespunzătoare, pentru fiecare țară/regiune din setul de date.</span><span class="sxs-lookup"><span data-stu-id="0bed2-226">Go to **Field Service** > **Settings** > **Price Lists** and check that bill rates and costs rates exist, with the appropriate currency, for each country/region in the data set.</span></span>

  > [!div class="mx-imgBorder"]
  > <span data-ttu-id="0bed2-227">![Captură de ecran cu listele de prețuri active](media/sample-data-4.png)</span><span class="sxs-lookup"><span data-stu-id="0bed2-227">![Screenshot of active price lists](media/sample-data-4.png)</span></span>

  > [!div class="mx-imgBorder"]
  > <span data-ttu-id="0bed2-228">![Captură de ecran cu unitățile organizaționale active](media/sample-data-5.png)</span><span class="sxs-lookup"><span data-stu-id="0bed2-228">![Screenshot of active organizational units](media/sample-data-5.png)</span></span>

## <a name="technical-notes"></a><span data-ttu-id="0bed2-229">Note tehnice</span><span class="sxs-lookup"><span data-stu-id="0bed2-229">Technical notes</span></span>

<span data-ttu-id="0bed2-230">Consultați secțiunea de mai jos pentru mai multe detalii tehnice despre instalarea acestor date.</span><span class="sxs-lookup"><span data-stu-id="0bed2-230">See below for more technical details on the installation of this data.</span></span>

### <a name="installing-sample-data-on-top-of-existing-data-not-recommended"></a><span data-ttu-id="0bed2-231">Instalarea datelor eșantion peste datele existente (nerecomandat)</span><span class="sxs-lookup"><span data-stu-id="0bed2-231">Installing sample data on top of existing data (not recommended)</span></span>

<span data-ttu-id="0bed2-232">Dacă trebuie să instalați datele eșantion peste versiunea de încercare sau mediul demonstrativ Field Service sau Project Service care are deja date, va trebui să suspendați verificările preliminare de siguranță efectuate de programul de instalare.</span><span class="sxs-lookup"><span data-stu-id="0bed2-232">If you need to install sample data on top of an existing Field Service or Project Service trial or demo environment that already has data, you'll need to suspend the safety prechecks performed by the installer.</span></span>

<span data-ttu-id="0bed2-233">Pentru a face acest lucru, accesați folderul **PkgFolder** pentru a găsi și a deschide fișierul **DemoDataPreImportConfig.xml** cu Notepad (sau cu un alt editor XML).</span><span class="sxs-lookup"><span data-stu-id="0bed2-233">To do this, go to the **PkgFolder** folder to find and open the **DemoDataPreImportConfig.xml** file with Notepad (or another XML editor).</span></span>

<span data-ttu-id="0bed2-234">Găsiți următoarea valoare, apoi modificați setarea de la adevărat la fals:</span><span class="sxs-lookup"><span data-stu-id="0bed2-234">Find the following value, and then change the setting from true to false:</span></span>

```alias
<TerminateOnPreCheckFailure>true</TerminateOnPreCheckFailure>
```

<span data-ttu-id="0bed2-235">Această modificare face ca programul de instalare să ocolească anumite verificări importante de siguranță, inclusiv:</span><span class="sxs-lookup"><span data-stu-id="0bed2-235">This change causes the installer to bypass some important safety checks, including:</span></span>

- <span data-ttu-id="0bed2-236">Confirmarea că există doar o înregistrare **Unitate organizațională** activă, apoi redenumirea ei în **Fabrikam US**.</span><span class="sxs-lookup"><span data-stu-id="0bed2-236">Confirming that there is no more than one active **Organizational Unit** record, and then renaming it to **Fabrikam US**.</span></span>

- <span data-ttu-id="0bed2-237">Confirmarea că există doar o înregistrare **Șablon de lucru** activă.</span><span class="sxs-lookup"><span data-stu-id="0bed2-237">Confirming that there is no more than one active **Work Template** record.</span></span>

- <span data-ttu-id="0bed2-238">Confirmarea că există doar o înregistrare **Parametru proiect** activă, apoi redenumirea acelei intrări în **Parametri**.</span><span class="sxs-lookup"><span data-stu-id="0bed2-238">Confirming that there is no more than one active **Project Parameter** record, and then renaming that entry to **Parameters**.</span></span>

### <a name="configuration-components"></a><span data-ttu-id="0bed2-239">Componente de configurație</span><span class="sxs-lookup"><span data-stu-id="0bed2-239">Configuration components</span></span>

<span data-ttu-id="0bed2-240">Există o serie de alte componente de configurație în acest fișier de configurare de pre-import.</span><span class="sxs-lookup"><span data-stu-id="0bed2-240">There are a number of other configuration components in this pre-import configuration file.</span></span> <span data-ttu-id="0bed2-241">Pentru utilizatorii tehnici, printre acestea se numără:</span><span class="sxs-lookup"><span data-stu-id="0bed2-241">For technical users, some of these include:</span></span>

- <span data-ttu-id="0bed2-242">**\<RequiredSolutions\>** specifică instalările de soluții preliminare și numerele lor de versiune.</span><span class="sxs-lookup"><span data-stu-id="0bed2-242">**\<RequiredSolutions\>** specifies prerequisite solution installations and their version numbers.</span></span>

- <span data-ttu-id="0bed2-243">**\<InstallSampleData\>** controlează dacă sunt instalate date eșantion predefinite pentru aplicațiile.</span><span class="sxs-lookup"><span data-stu-id="0bed2-243">**\<InstallSampleData\>** controls whether out-of-the-box sample data for the apps is installed.</span></span>

    - <span data-ttu-id="0bed2-244">fals - omite instalarea acestor date predefinite (care se pot elimina)</span><span class="sxs-lookup"><span data-stu-id="0bed2-244">false - skips installation of this built-in data (which is removable)</span></span>

    - <span data-ttu-id="0bed2-245">adevărat - instalează datele încorporate în paralel cu instalarea datelor eșantion FS și PSA</span><span class="sxs-lookup"><span data-stu-id="0bed2-245">true - installs the built-in data concurrent with installation of the FS and PSA sample data</span></span>

- <span data-ttu-id="0bed2-246">**\<PreImportDataCollection\>** specifică mapările de date flat-file și înregistrările asociate care vor fi importate înainte de instalarea datelor eșantion principale.</span><span class="sxs-lookup"><span data-stu-id="0bed2-246">**\<PreImportDataCollection\>** specifies flat-file Data Maps and associated Records to be imported ahead of the main sample data installation.</span></span>

- <span data-ttu-id="0bed2-247">**\<EntitiesToEnableScheduling\>** specifică entitățile care ar trebui să fie activate pentru Rezervare în Microsoft Dynamics Scheduling (sau Universal Resource Scheduling).</span><span class="sxs-lookup"><span data-stu-id="0bed2-247">**\<EntitiesToEnableScheduling\>** specifies which entities should be enabled for Booking in Microsoft Dynamics Scheduling (aka Universal Resource Scheduling).</span></span>

- <span data-ttu-id="0bed2-248">**\<UsersToCreateAndConfigure\>** specifică resursele ce se pot rezerva care vor fi create (dacă acestea nu exista deja) înainte să se execute importul datelor eșantion.</span><span class="sxs-lookup"><span data-stu-id="0bed2-248">**\<UsersToCreateAndConfigure\>** specifies Bookable Resources that will be created (if they don't exist already) before the sample data import executes.</span></span> <span data-ttu-id="0bed2-249">Rețineți că resursa ce se poate rezerva pentru datele eșantion de sistem sursă se potrivesc cu înregistrările de resurse ce se pot rezerva din sistemul țintă pentru numele complet și conectarea fiecărei resurse.</span><span class="sxs-lookup"><span data-stu-id="0bed2-249">Note that the source system sample data Bookable Resource match with the target system Bookable Resource records on the FullName and login of each resource.</span></span> <span data-ttu-id="0bed2-250">Prin urmare, NU este posibil să modificați numele din acest fișier de preconfigurare decât dacă importați mai întâi datele eșantion într-un sistem țintă utilizând aceste nume, apoi redenumiți Resursele care se pot rezerva la setul de nume dorit, împreună cu înregistrările de Utilizator activat și apoi exportați datele din nou pentru a le importa în sistemul dvs. de destinație final (actualizând intrările **ImportUserMapFile.xml** vechi și noi în consecință).</span><span class="sxs-lookup"><span data-stu-id="0bed2-250">Therefore, it is NOT possible to change the names in this preconfiguration file unless you first import sample data into a target system using these names, then rename the Bookable Resources to your desired name set along with the Enabled User records, and then export the data again for import into your final destination system (updating the **ImportUserMapFile.xml** Old and New entries accordingly).</span></span>

- <span data-ttu-id="0bed2-251">**\<PluginsToDisable\>** specifică inserturi în linia de element foarte discrete, care trebuie să fie dezactivate în timpul importului datelor eșantion și reactivate după aceea.</span><span class="sxs-lookup"><span data-stu-id="0bed2-251">**\<PluginsToDisable\>** specifies very discrete line-item plug-ins that must be disabled during the sample data import and then reenabled afterwards.</span></span>

### <a name="fabrikam-robotics-fictitious-scenario"></a><span data-ttu-id="0bed2-252">Scenariu fictiv Fabrikam Robotics</span><span class="sxs-lookup"><span data-stu-id="0bed2-252">Fabrikam Robotics fictitious scenario</span></span>

<span data-ttu-id="0bed2-253">Pachetele de date eșantion pentru referință Field Service și Project Service instalează **Soluția Fabrikam Manufacturing Master Data (v3.0.0.0)**, împreună cu aproximativ 4.000 de înregistrări și aproximativ 40 de entități diferite.</span><span class="sxs-lookup"><span data-stu-id="0bed2-253">The Field Service and Project Service sample reference data packages install the **Fabrikam Manufacturing Master Data (v3.0.0.0) solution**, along with approximately 4,000 records and approximately 40 different entities.</span></span> <span data-ttu-id="0bed2-254">Pachetele de date eșantion separate pentru Field Service sau Project Service conțin un subset de date eșantion **v902FPSMasterData** pentru acea aplicație.</span><span class="sxs-lookup"><span data-stu-id="0bed2-254">The separate sample data packages for Field Service or Project Service contain a subset of the **v902FPSMasterData** sample data for that application.</span></span> <span data-ttu-id="0bed2-255">Pachetul **Date demonstrative** instalează **Soluția Fabrikam Manufacturing Demo Data (v3.0.0.7)** cu aproximativ 22.000 de înregistrări în 148 de entități.</span><span class="sxs-lookup"><span data-stu-id="0bed2-255">The **Demo Data** package installs the **Fabrikam Manufacturing Demo Data (v3.0.0.7) solution** with approximately 22,000 records across 148 entities.</span></span>

<span data-ttu-id="0bed2-256">Compania fictivă Fabrikam Robotics este un producător de roboți pentru linia de asamblare a dispozitivelor electronice și este cunoscută pentru calitatea produselor, inovație și un serviciu serios pentru clienți, inclusiv pentru planificarea instalării, implementare și servicii de întreținere permanente.</span><span class="sxs-lookup"><span data-stu-id="0bed2-256">The fictional company, Fabrikam Robotics, is a manufacturer of electronic device assembly line robots and is known for their product quality, innovation, and solid customer service, including installation planning, implementation, and ongoing maintenance services.</span></span> <span data-ttu-id="0bed2-257">Fabrikam are sediul în Statele Unite ale Americii (Fabrikam US) și are operațiuni de service bazate pe proiecte în Franța, India, Regatul Unit și Elveția.</span><span class="sxs-lookup"><span data-stu-id="0bed2-257">Fabrikam is headquartered in the United States (Fabrikam US), and has project-based service operations in France, India, the United Kingdom, and Switzerland.</span></span>

<span data-ttu-id="0bed2-258">Operațiunile Field Service sunt centrate în Statele Unite, în principal în zona Seattle.</span><span class="sxs-lookup"><span data-stu-id="0bed2-258">Field service operations are centered in the United States, mostly in the greater Seattle area.</span></span> <span data-ttu-id="0bed2-259">Compania este axată pe valorificarea conectivității Internet of Things (IoT) pentru a monitoriza performanța activelor de client și a livra servicii tot mai proactive la fața locului.</span><span class="sxs-lookup"><span data-stu-id="0bed2-259">The company is focused on leveraging Internet of Things (IoT) connectivity to monitor customer asset performance and deliver increasingly proactive onsite services.</span></span>

<span data-ttu-id="0bed2-260">O prezentare generală la nivel înalt a datelor eșantion este următoarea:</span><span class="sxs-lookup"><span data-stu-id="0bed2-260">A high-level overview of the sample data is as follows:</span></span>

- <span data-ttu-id="0bed2-261">Elemente de date eșantion comune (incluse pentru ambele aplicații)</span><span class="sxs-lookup"><span data-stu-id="0bed2-261">Common sample data elements (included for both applications)</span></span>

    - <span data-ttu-id="0bed2-262">1 utilizator</span><span class="sxs-lookup"><span data-stu-id="0bed2-262">1 user</span></span>

    - <span data-ttu-id="0bed2-263">71 de conturi</span><span class="sxs-lookup"><span data-stu-id="0bed2-263">71 accounts</span></span>

    - <span data-ttu-id="0bed2-264">137 de persoane de contact</span><span class="sxs-lookup"><span data-stu-id="0bed2-264">137 contacts</span></span>

    - <span data-ttu-id="0bed2-265">Diferite tipuri de tranzacții și categorii</span><span class="sxs-lookup"><span data-stu-id="0bed2-265">Various transaction types and categories</span></span>

    - <span data-ttu-id="0bed2-266">50 de produse cu 1 listă de prețuri pentru produse</span><span class="sxs-lookup"><span data-stu-id="0bed2-266">50 products with 1 product price list</span></span>

    - <span data-ttu-id="0bed2-267">14 liste de prețuri/costuri</span><span class="sxs-lookup"><span data-stu-id="0bed2-267">14 price/cost lists</span></span>

    - <span data-ttu-id="0bed2-268">31 de caracteristici (competențe ale resurselor) în 2 modele de evaluare cu 3 nivele (valori de evaluare)</span><span class="sxs-lookup"><span data-stu-id="0bed2-268">31 characteristics (resource skills) in 2 rating models with 3 levels (rating values)</span></span>

- <span data-ttu-id="0bed2-269">Project Service</span><span class="sxs-lookup"><span data-stu-id="0bed2-269">Project Service</span></span>

    - <span data-ttu-id="0bed2-270">8 unități organizaționale</span><span class="sxs-lookup"><span data-stu-id="0bed2-270">8 organizational units</span></span>

    - <span data-ttu-id="0bed2-271">6 niveluri de utilizare specifice rolurilor</span><span class="sxs-lookup"><span data-stu-id="0bed2-271">6 role-specific utilization levels</span></span>

    - <span data-ttu-id="0bed2-272">+2,8k de specificații rol-preț</span><span class="sxs-lookup"><span data-stu-id="0bed2-272">2.8k+ role-price specifications</span></span>

- <span data-ttu-id="0bed2-273">Field Service</span><span class="sxs-lookup"><span data-stu-id="0bed2-273">Field Service</span></span>

    - <span data-ttu-id="0bed2-274">4 teritorii</span><span class="sxs-lookup"><span data-stu-id="0bed2-274">4 territories</span></span>

    - <span data-ttu-id="0bed2-275">5 tipuri de comenzi de lucru</span><span class="sxs-lookup"><span data-stu-id="0bed2-275">5 work order types</span></span>

    - <span data-ttu-id="0bed2-276">22 de active de client</span><span class="sxs-lookup"><span data-stu-id="0bed2-276">22 customer assets</span></span>

    - <span data-ttu-id="0bed2-277">9 tipuri de incidente cu o zonă de caracteristici de resurse asociate (9), servicii (13) și activități de service (13)</span><span class="sxs-lookup"><span data-stu-id="0bed2-277">9 incident types with a range of associated resource characteristics (9), services (13) and service tasks (13)</span></span>
   
<span data-ttu-id="0bed2-278">Pachetul **Date demonstrative** instalează aproximativ 179 de comenzi de lucru, 12 proiecte și date asociate tranzacționale.</span><span class="sxs-lookup"><span data-stu-id="0bed2-278">The **Demo Data** package installs approximately 179 work orders, 12 projects, and associated transactional data.</span></span> 

### <a name="change-the-work-hours-for-sample-resources"></a><span data-ttu-id="0bed2-279">Modificați orele de lucru pentru resursele eșantion</span><span class="sxs-lookup"><span data-stu-id="0bed2-279">Change the work hours for sample resources</span></span>

<span data-ttu-id="0bed2-280">În mod implicit, toate resursele care se pot rezerva au un calendar de 24 de ore de lucru.</span><span class="sxs-lookup"><span data-stu-id="0bed2-280">By default, all bookable resources have a 24 work hours calendar.</span></span>

<span data-ttu-id="0bed2-281">În cazul în care trebuie să modificați orele de lucru pentru resursele eșantion care se pot rezerva, accesați **Universal Resource Scheduling** > **Planificare** > **Resurse**.</span><span class="sxs-lookup"><span data-stu-id="0bed2-281">If you need to change the work hours for sample bookable resources, go to **Universal Resource Scheduling** > **Scheduling** > **Resources**.</span></span>

<span data-ttu-id="0bed2-282">Selectați un utilizator (de exemplu, Spencer Low) și schimbați orele de lucru ale lui Spencer în orele pe care doriți să le aplicați pentru mai mulți utilizatori.</span><span class="sxs-lookup"><span data-stu-id="0bed2-282">Select a user (for example, Spencer Low) and change Spencer's work hours to the hours you want to apply to multiple users.</span></span> <span data-ttu-id="0bed2-283">Accesați **Universal Resource Scheduling** > **Setări** > **Șabloane de ore de lucru** și editați înregistrarea **Șablon implicit de lucru**.</span><span class="sxs-lookup"><span data-stu-id="0bed2-283">Go to **Universal Resource Scheduling** > **Settings** > **Work Hour Templates** and edit the **Default Work Template** record.</span></span> <span data-ttu-id="0bed2-284">În câmpul **Resursă șablon**, selectați un utilizator cu orele de lucru pe care doriți să le aplicați la alte resurse.</span><span class="sxs-lookup"><span data-stu-id="0bed2-284">In the **Template Resource** field, select a user with work hours that you want to apply to other resources.</span></span> <span data-ttu-id="0bed2-285">Accesați **Universal Resource Scheduling** > **Programare** > **Resurse** > **Resurse active ce se pot rezerva**.</span><span class="sxs-lookup"><span data-stu-id="0bed2-285">Go to **Universal Resource Scheduling** > **Scheduling** > **Resources** > **Active Bookable Resources**.</span></span> <span data-ttu-id="0bed2-286">Selectați resursele pe care doriți să le modificați, apoi selectați **Setare calendar**.</span><span class="sxs-lookup"><span data-stu-id="0bed2-286">Select the resources you want to change, and then select **Set Calendar**.</span></span> <span data-ttu-id="0bed2-287">În lista verticală **Șablon de lucru**, selectați șablonul **Ore de lucru implicite** sau un alt șablo cu resursa de șablon corectă.</span><span class="sxs-lookup"><span data-stu-id="0bed2-287">On the **Work Template** drop-down list, select the **Default Work Hour** template or another template with the correct templating resource.</span></span> <span data-ttu-id="0bed2-288">Când accesați panoul de planificare, ar trebui să vedeți că resursele au acum ore de lucru actualizate.</span><span class="sxs-lookup"><span data-stu-id="0bed2-288">When you go to the schedule board, you should see that the resources now have updated work hours.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="0bed2-289">![Captură de ecran cu resurse active ce se pot rezerva](media/sample-data-6.png)</span><span class="sxs-lookup"><span data-stu-id="0bed2-289">![Screenshot of active bookable resources](media/sample-data-6.png)</span></span>
