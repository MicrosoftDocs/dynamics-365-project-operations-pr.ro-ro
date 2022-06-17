---
title: Instalarea datelor eșantion
description: Acest articol oferă informații despre instalarea datelor eșantion în Project Service Automation.
ms.custom: dyn365-projectservice
ms.date: 11/08/2018
ms.reviewer: johnmichalak
ms.suite: ''
applies_to: Dynamics 365 Project Service Automation
author: ruhercul
ms.author: ruhercul
search.audienceType: IT Pro, Developer
search.app: ''
ms.openlocfilehash: 8fb3854c139125abbf499622d048e2ff0791516a
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926791"
---
# <a name="sample-data-installation-for-the-project-service-application"></a>Instalarea datelor eșantion pentru aplicația Project Service

[!include [banner](../includes/psa-now-project-operations.md)]

Pentru a vă ajuta să creați propriile medii demonstartive, Microsoft furnizează pachete de date eșantion descărcabile ce evidențiază capacitățile aplicațiilor dvs. Există două tipuri de pachete de date eșantion:
- referință/configurare date
- Date demonstrative (referință/configurare și date tranzacționale, cum ar fi comenzi de lucru și proiecte)

Pachetele de date eșantion pentru **referință** pot fi descărcate în trei pachete diferite, astfel încât să puteți instala date doar pentru Project Service sau doar pentru Field Service sau puteți instala date eșantion pentru ambele aplicații simultan.

Pachetele de date eșantion pentru configurare/referință sunt:

- [**V902PSMasterData** - doar Project Service versiunea 3.x](https://go.microsoft.com/fwlink/?linkid=2026540&clcid=0x409)

- [**V902FSMasterData** - doar Field Service versiunea 8.x](https://go.microsoft.com/fwlink/?linkid=2026536&clcid=0x409)

- [**V902FPSMasterData** - Field Service 8.x și Project Service 3.x](https://go.microsoft.com/fwlink/?linkid=2026041&clcid=0x409)

Cel mai recent pachet de date **demonstrative** este:

 - [**FPSDemoData** - Field Service 8.x și Project Service 3.x](https://aka.ms/fpsdemodatapackage)

   Instrucțiunile de instalare diferă puțin în funcție de utilizatori pentru a crea și a configura secțiunea, dar restul rămâne ca în [**publicarea pe blog**](https://aka.ms/fpsdemodatablog) anterioară. Acest pachet prezintă un set de date demonstrative redus și durează circa 3 ore pentru a se instala.

Aceste pachete de date eșantion sunt disponibile numai în limba engleză.

> [!IMPORTANT]
> **Nu există nicio modalitate de a dezinstala datele eșantion.** Trebuie să instalați aceste pachete numai pe sisteme demonstrative, de evaluare, instruire și testare. De asemenea, rețineți că instalarea unui pachet individual și instalarea celuilalt pachet individual nu este acceptată. (Cu alte cuvinte, nu se poate instala **FSMasterData** urmat de **PSMasterData** sau viceversa.) Dacă se întâmplă să aveți nevoie de date eșantion pentru ambele aplicații în orice moment în viitor, ar trebui să instalați pachetul **v902FPSMasterData**.

Atunci când instalați oricare dintre pachetele de date eșantion, procesul de instalare efectuează următoarele acțiuni:

- Creează sau setează parametri impliciți pentru a folosi Project Service, Field Service sau ambele aplicații (după caz).

- Importă date esantion pentru aplicații, cum ar fi resurse ce se pot rezerva, roluri specifice aplicațiilor, liste de vânzări și de prețuri, unități organizaționale, înregistrări ale procesului de vânzări și alte entități pentru a demonstra capacitățile cheie.  

Cu pachetul de **date demonstrative**, veți obține datele tranzacționale de mai sus, precum și date tranzacționale suplimentare, cum ar fi comenzi de lucru și proiecte.

Vă întrebați ce capabilități puteți demonstra cu date eșantion? Consultați scenariul fictiv Fabrikam Robotics din [Note tehnice](#technical-notes).

Dacă aveți întrebări despre instalarea acestor pachete de date eșantion, [trimiteți-ne un e-mail la fpsdemodata@microsoft.com](mailto:fpsdemodata@microsoft.com).

## <a name="requirements"></a>Cerințe

Protocolul de instalare presupune următoarele despre instanța (organizația) dvs. țintă:

- Limba de bază este limba engleză, iar moneda de bază este dolarul american (USD, $).

- Organizația nu are pregătite date Project Service sau Field Service sau are doar date de bază implicite care vin cu orice organizație nouă.

- Versiunea corectă a aplicației de afaceri este instalată deja:
       
    - **Pentru FPSDemoData sau v902FPSMasterData:** organizația are instalată Field Service versiunea 8.x și Project Service versiunea 3.x.

    - **Pentru v902PSMasterData:** organizația are instalată Project Service versiunea 3.x.

    - **Pentru v902FSMasterData:** organizația are instalată Field Service versiunea 8.x.

> [!NOTE]
> Dacă trebuie să instalați datele eșantion peste versiunea de încercare sau mediul demonstrativ Project Service și Field Service care are deja date (nu este recomandat), va trebui să suspendați verificările preliminare de siguranță efectuate de programul de instalare. Pentru mai multe informații, consultați notele tehnice de mai jos.

## <a name="prepare-for-installation"></a>Pregătirea instalării

Trebuie să rulați programul de instalare pe un computer cu o versiune recentă de Windows (preferabil Windows 10).

Ar trebui să planificați ca acel computer să rămână conectat la o rețea, și ca instalarea să ruleze până la **1 oră** pentru **date pentru configurare/referință**. (În mod normal, instalarea durează aproximativ 30 de minute pentru **FPSMasterData**, care include date eșantion pentru ambele aplicații.) Pentru **FPSDemoData**, instalarea va lua circa **3 ore**.

Computerul trebuie să aibă dezactivată funcția Economizor de ecran. În caz contrar, acreditările de sesiune pentru instalare se pot pierde atunci când economizorul de ecran se angajează (cu excepția cazului în care păstrați sesiunea activă).

> [!div class="mx-imgBorder"]
> ![Captură de ecran a setărilor de economizor de ecran, cu economizorul de ecran oprit.](media/sample-data-1.png)

## <a name="download-and-unpack"></a>Descărcați și dezarhivați

Programul de instalare a datelor eșantion Project Service și Field Service este distribuit ca executabil cu extragere automată. Numele fișierului poate varia, în funcție de pachetul de date eșantion, dar, altfel, pașii sunt aceieași indiferent ce pachet instalați.

După descărcarea unui pachet, rulați fișierul .exe, apoi acceptați termenii și condițiile pentru a dezarhiva fișierul zip comprimat. Apoi trebuie să extrageți conținutul acelui fișier într-un folder de pe computer.

În funcție de sistemul de operare și de setările de securitate, poate fi necesar să efectuați următorii pași după dezarhivarea fișierului zip:

1. Găsiți și faceți clic dreapta pe fișierul **FPSDemoData.dll** din folderul **v902FPSMasterData** / **PackageDeployer_FPSDemoData**.

2. Alegeți **Deblocare**.

3. Selectați **Se aplică**.

4. Selectați **OK**.


## <a name="create-or-configure-users"></a>Creați sau configurați utilizatorii

Pachetul **FPSDemoData** necesită șase utilizatori, în timp ce pachetele **FPSMasterData** au nevoie de un singur utilizator. Consultați-l pe cel corect pentru pachetul dvs. de date eșantion.

## <a name="create-or-configure-users---setupreference-data-packages"></a>Crearea sau configurarea utilizatorilor - pachete de date pentru configurare/referință

Pachetul **FPSMasterData** este conceput pentru a fi instalat cu un utilizator numit Spencer Low, cu setarile descrise aici. Pentru a instala pachetul corect, aveți nevoie să creați (sau să redenumiți temporar) utilizatori în mediul dvs., pentru a se potrivi configurației de date eșantion primite.

Pentru a crea sau a configura utilizatori, accesați **Setări** > **Securitate** > **Utilizatori** și efectuați următoarele:

1. Setați UserFullname="Spencer Low" cu numele "spencerl" (**litere mici**) la rolurile Manager de proiect și Manager de practică.

2. Selectați utilizatorul **Spencer Low** și apoi selectați **Gestionare roluri**. Găsiți și selectați rolul **Administrator de sistem**, apoi selectați **OK** pentru a acorda drepturi de administrator complete utilizatorului Spencer Low. Acest pas este necesar pentru a asigura că înregistrările eșantion sunt create cu dreptul de proprietate de utilizator corect și, prin urmare, populează corect vizualizările.

3. Din pachetul descărcat, trebuie să actualizați un fișier de mapare de date cu adresele de e-mail ale contextului de utilizator implicit. Pentru a face asta, deschideți **PkgFolder** și apoi găsiți și deschideți fișierul **ImportUserMapFile.xml** în Notepad (sau Visual Studio sau alt editor XML). Setați câmpul **DefaultUserToMapTo=** la adresa de e-mail a utilizatorului Spencer Low.

4. Dacă nu utilizați Spencer Low cu numele de utilizator **spencerl**, trebuie să actualizați un fișier suplimentar. Deschideți fișierul **DemoDataPreImportConfig.xml**, apoi găsiți eticheta **userstocreateandconfigure**. Actualizați eticheta **\<login\>** cu numele de utilizator al utilizatorului Spencer Low. Pentru detalii suplimentare, consultați [Note tehnice](#technical-notes).

## <a name="create-or-configure-users---demo-data-package"></a>Crearea sau configurarea utilizatorilor - pachet de date demonstrative

Pachetul de date demonstrative necesită șase utilizatori. Pentru instalarea corectă a pachetului, efectuați următoarele:

 1. Creați sau redenumiți temporar utilizatorii existenți pentru a se potrivi configurației de date eșantion primite accesând **Setări** > **Securitate** > **Utilizatori**.
 
    Aceste roluri sunt necesare numai pentru demonstrațiile în care sunt implicate persoane.  
    - Utilizator Fullname="David So" tehnician Field Service   
    - Utilizator Fullname="Jamie Reding" ca Dispecer Customer Service & Field Service   
    - Utilizator Fullname="Molly Clark" ca Manager de cont   
    - Utilizator Fullname="Spencer Low" ca Manager de practică și Manager de proiect  
    - Utilizator Fullname="Veronica Quek" ca Membru echipă   
    - Utilizator Fullname="William Contoso"
  
2. Pentru a importa datele demonstrative, atribuiți cei șase utilizatori deasupra rolului de Administrator, astfel încât înregistrările eșantion să fie importate corect. 

3. Deschideți **PkgFolder**, iar apoi găsiți și deschideți **ImportUserMapFile.xml**. Actualizați câmpurile **Nou=** la adresele de e-mail ale utilizatorilor corespunzători din sistemul dvs.

   > [!div class="mx-imgBorder"]
   > ![Captură de ecran a UserMapFile.](media/sample-data-7.png)

4. În cazul în care numele complet "Spencer Low" al utilizatorului are un ID de utilizator diferit de **"spencerl"**, trebuie să actualizați un fișier suplimentar. Deschideți **DemoDataPreImportConfig.xml** și găsiți eticheta **userstocreateandconfigure**. Actualizați eticheta **\<login\>** cu Id conectare (sensibil la litere mari și mici). 

5. Primul calendar al utilizatorului (în eticheta **userstocreateandconfigure**) este folosit pentru a popula orele de lucru pentru toate resursele care se pot rezerva la importul de date demonstrative. Navigați la **Setări** > **Securitate** > **Utilizatori**, găsiți utilizatorul "Spencer Low" și deschideți opțiunea „Ore de lucru”. Editați orele de lucru existente, selectând opțiunea **Planificare săptămânală recurentă în totalitate de la început la sfârșit**. Asigurați-vă că **Orele de lucru sunt setate pentru 08:00-17:00 (9 ore), de luni până vineri și cu fusul orar stabilit la ora Pacificului (SUA și Canada)**. Acest lucru este necesar pentru a garanta că panoul de Proiect și Planificare este conform așteptărilor.

**Recomandare:** luați în considerare crearea unei copii backup a organizației dvs. acum, în cazul în care trebuie să reveniți la punctul de plecare dacă ceva nu merge bine în timpul instalării datelor eșantion. Pentru informații suplimentare, consultați [Backupul și restaurarea instanțelor](/dynamics365/customer-engagement/admin/backup-restore-instances).

## <a name="run-the-package-deployer"></a>Rulați Package Deployer

1. Găsiți și rulați **PackageDeployer.exe** în folderul **v902FPSMasterData** SAU **PackageDeployer_FPSDemoData**.

2. Acceptați termenii și condițiile.

3. În fereastra următoare:

   a. Selectați tipul de implementare **Office 365**.

   b. Utilizați utilizatorul și parola utilizatorului administrator de sistem configurat în „Creați sau configurați utilizatori” („Spencer Low” cu numele de utilizator „spencerl”).

   c. Asigurați-vă că ați bifat **Afișați lista de organizații disponibile**.

      > [!div class="mx-imgBorder"]
      > ![Captură de ecran a ferestrei Package Deployer cu opțiunea „Afișați lista de organizații disponibile” selectată](media/sample-data-2.png)

4. Selectați organizația unde doriți să instalați date eșantion.

5. Selectați **Următorul** până când vedeți caseta de dialog **Configurare date demonstrative**.

   > [!div class="mx-imgBorder"]
   > ![Captură de ecran a ferestrei de stare a instalatorului de date demonstrative.](media/sample-data-3.png)

6. Înainte de a continua, rețineți că instalarea datelor eșantion ar putea dura până la o oră (în mod normal, durează cam 10 minute). Va trebui să vă asigurați că rămâne pornit și conectat la o rețea computerul în timpul procesului de instalare și că sesiunea rămâne activă.   

7. Când sunteți gata, faceți clic pe **Următorul** pentru a începe procesul de instalare a datelor eșantion. După ce sunt încărcate datele eșantion, faceți clic pe **Terminare**.

## <a name="verify-the-sample-data-installation"></a>Verificați instalarea datelor eșantion

Pentru o verificare a funcționării, verificați dacă numărul de înregistrări și tipuri de entități listate in scenariul fictiv Fabrikam Robotics apar așa cum vă așteptați.

După încărcarea completă a datelor eșantion, conectați-vă ca utilizatorul Spencer Low și confirmați următoarele:

- Dacă este instalată aplicația Project Service, accesați **Project Service** > **Setări** > **Liste de prețuri**. Confirmați dacă sumele de facturare și costurile există cu moneda corespunzătoare pentru fiecare țară/regiune din setul de date.

- Dacă este instalată aplicația Project Service, accesați **Universal Resource Scheduling** > **Setări** > **Unități organizaționale**. Confirmați dacă a fost asociată o listă de prețuri cu moneda corespunzătoare cu fiecare unitate de organizație (cu excepția intrărilor de oraș). În cazul în care oricare lipsește, găsiți și asociați lista de prețuri corectă.

- Dacă este instalată aplicația Field Service, accesați **Project Service** > **Setări** > **Liste de prețuri**. Confirmați că tarifele și costurile există. Accesați **Field Service** > **Setări** > **Liste de prețuri** și verificați dacă sumele de facturare și costurile există, cu moneda corespunzătoare, pentru fiecare țară/regiune din setul de date.

  > [!div class="mx-imgBorder"]
  > ![Captură de ecran cu listele de prețuri active.](media/sample-data-4.png)

  > [!div class="mx-imgBorder"]
  > ![Captură de ecran cu unitățile organizaționale active.](media/sample-data-5.png)

## <a name="technical-notes"></a>Note tehnice

Consultați secțiunea de mai jos pentru mai multe detalii tehnice despre instalarea acestor date.

### <a name="installing-sample-data-on-top-of-existing-data-not-recommended"></a>Instalarea datelor eșantion peste datele existente (nerecomandat)

Dacă trebuie să instalați datele eșantion peste versiunea de încercare sau mediul demonstrativ Field Service sau Project Service care are deja date, va trebui să suspendați verificările preliminare de siguranță efectuate de programul de instalare.

Pentru a face acest lucru, accesați folderul **PkgFolder** pentru a găsi și a deschide fișierul **DemoDataPreImportConfig.xml** cu Notepad (sau cu un alt editor XML).

Găsiți următoarea valoare, apoi modificați setarea de la adevărat la fals:

```alias
<TerminateOnPreCheckFailure>true</TerminateOnPreCheckFailure>
```

Această modificare face ca programul de instalare să ocolească anumite verificări importante de siguranță, inclusiv:

- Confirmarea că există doar o înregistrare **Unitate organizațională** activă, apoi redenumirea ei în **Fabrikam US**.

- Confirmarea că există doar o înregistrare **Șablon de lucru** activă.

- Confirmarea că există doar o înregistrare **Parametru proiect** activă, apoi redenumirea acelei intrări în **Parametri**.

### <a name="configuration-components"></a>Componente de configurație

Există o serie de alte componente de configurație în acest fișier de configurare de pre-import. Pentru utilizatorii tehnici, printre acestea se numără:

- **\<RequiredSolutions\>** specifică instalările de soluții preliminare și numerele lor de versiune.

- **\<InstallSampleData\>** controlează dacă sunt instalate date eșantion predefinite pentru aplicațiile.

    - fals - omite instalarea acestor date predefinite (care se pot elimina)

    - adevărat - instalează datele încorporate în paralel cu instalarea datelor eșantion FS și PSA

- **\<PreImportDataCollection\>** specifică mapările de date flat-file și înregistrările asociate care vor fi importate înainte de instalarea datelor eșantion principale.

- **\<EntitiesToEnableScheduling\>** specifică entitățile care ar trebui să fie activate pentru Rezervare în Microsoft Dynamics Scheduling (sau Universal Resource Scheduling).

- **\<UsersToCreateAndConfigure\>** specifică resursele ce se pot rezerva care vor fi create (dacă acestea nu exista deja) înainte să se execute importul datelor eșantion. Rețineți că resursa ce se poate rezerva pentru datele eșantion de sistem sursă se potrivesc cu înregistrările de resurse ce se pot rezerva din sistemul țintă pentru numele complet și conectarea fiecărei resurse. Prin urmare, NU este posibil să modificați numele din acest fișier de preconfigurare decât dacă importați mai întâi datele eșantion într-un sistem țintă utilizând aceste nume, apoi redenumiți Resursele care se pot rezerva la setul de nume dorit, împreună cu înregistrările de Utilizator activat și apoi exportați datele din nou pentru a le importa în sistemul dvs. de destinație final (actualizând intrările **ImportUserMapFile.xml** vechi și noi în consecință).

- **\<PluginsToDisable\>** specifică inserturi în linia de element foarte discrete, care trebuie să fie dezactivate în timpul importului datelor eșantion și reactivate după aceea.

### <a name="fabrikam-robotics-fictitious-scenario"></a>Scenariu fictiv Fabrikam Robotics

Pachetele de date eșantion pentru referință Field Service și Project Service instalează **Soluția Fabrikam Manufacturing Master Data (v3.0.0.0)**, împreună cu aproximativ 4.000 de înregistrări și aproximativ 40 de entități diferite. Pachetele de date eșantion separate pentru Field Service sau Project Service conțin un subset de date eșantion **v902FPSMasterData** pentru acea aplicație. Pachetul **Date demonstrative** instalează **Soluția Fabrikam Manufacturing Demo Data (v3.0.0.7)** cu aproximativ 22.000 de înregistrări în 148 de entități.

Compania fictivă Fabrikam Robotics este un producător de roboți pentru linia de asamblare a dispozitivelor electronice și este cunoscută pentru calitatea produselor, inovație și un serviciu serios pentru clienți, inclusiv pentru planificarea instalării, implementare și servicii de întreținere permanente. Fabrikam are sediul în Statele Unite ale Americii (Fabrikam US) și are operațiuni de service bazate pe proiecte în Franța, India, Regatul Unit și Elveția.

Operațiunile Field Service sunt centrate în Statele Unite, în principal în zona Seattle. Compania este axată pe valorificarea conectivității Internet of Things (IoT) pentru a monitoriza performanța activelor de client și a livra servicii tot mai proactive la fața locului.

O prezentare generală la nivel înalt a datelor eșantion este următoarea:

- Elemente de date eșantion comune (incluse pentru ambele aplicații)

    - 1 utilizator

    - 71 de conturi

    - 137 de persoane de contact

    - Diferite tipuri de tranzacții și categorii

    - 50 de produse cu 1 listă de prețuri pentru produse

    - 14 liste de prețuri/costuri

    - 31 de caracteristici (competențe ale resurselor) în 2 modele de evaluare cu 3 nivele (valori de evaluare)

- Project Service

    - 8 unități organizaționale

    - 6 niveluri de utilizare specifice rolurilor

    - +2,8k de specificații rol-preț

- Field Service

    - 4 teritorii

    - 5 tipuri de comenzi de lucru

    - 22 de active de client

    - 9 tipuri de incidente cu o zonă de caracteristici de resurse asociate (9), servicii (13) și activități de service (13)
   
Pachetul **Date demonstrative** instalează aproximativ 179 de comenzi de lucru, 12 proiecte și date asociate tranzacționale. 

### <a name="change-the-work-hours-for-sample-resources"></a>Modificați orele de lucru pentru resursele eșantion

În mod implicit, toate resursele care se pot rezerva au un calendar de 24 de ore de lucru.

În cazul în care trebuie să modificați orele de lucru pentru resursele eșantion care se pot rezerva, accesați **Universal Resource Scheduling** > **Planificare** > **Resurse**.

Selectați un utilizator (de exemplu, Spencer Low) și schimbați orele de lucru ale lui Spencer în orele pe care doriți să le aplicați pentru mai mulți utilizatori. Accesați **Universal Resource Scheduling** > **Setări** > **Șabloane de ore de lucru** și editați înregistrarea **Șablon implicit de lucru**. În câmpul **Resursă șablon**, selectați un utilizator cu orele de lucru pe care doriți să le aplicați la alte resurse. Accesați **Universal Resource Scheduling** > **Programare** > **Resurse** > **Resurse active ce se pot rezerva**. Selectați resursele pe care doriți să le modificați, apoi selectați **Setare calendar**. În lista verticală **Șablon de lucru**, selectați șablonul **Ore de lucru implicite** sau un alt șablo cu resursa de șablon corectă. Când accesați panoul de planificare, ar trebui să vedeți că resursele au acum ore de lucru actualizate.

> [!div class="mx-imgBorder"]
> ![Captură de ecran cu resurse active ce se pot rezerva.](media/sample-data-6.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]