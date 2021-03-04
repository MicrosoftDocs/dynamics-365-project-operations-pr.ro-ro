---
title: Asigurarea accesului pentru un nou mediu
description: Acest subiect furnizează informații despre ucm să provizionați un nou mediu Project Operations.
author: sigitac
manager: Annbe
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 09af2a7693c45d1d0b9c75420d018cc50d2cc0fa
ms.sourcegitcommit: 04c446746aad97fc3f4c3d441983c586b918a3a6
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 12/11/2020
ms.locfileid: "4727805"
---
# <a name="provision-a-new-environment"></a>Asigurarea accesului pentru un nou mediu

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Acest subiect furnizează informații despre cum să furnizați un mediu nou Dynamics 365 Project Operations pentru scenarii bazate pe resurse/fără stoc.

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a>Activați pregătirea automată a Project Operations într-un proiect LCS

Utilizați pașii următori pentru a activa fluxul automatizat de pregătire pentru Project Operations pentru proiectul dvs. LCS.

1. Accesați [LCS](https://lcs.dynamics.com/v2) și selectați titlul **Previzualizarea gestionării caracteristicilor**.
2. În lista **Caracteristică de previzualizare**, selectați **Caracteristică Project Operations** și apoi selectați **Caracteristica de previzualizare activată** pentru a activa Project Operations.

> [!NOTE]
> Acest pas se efectuează o singură dată pentru fiecare proiect LCS.

## <a name="provision-a-project-operations-environment"></a>Furnizarea unui mediu de Project Operations

1. Deschideți un nou Dynamics 365 Finance [mediul demonstrativ](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) sau o implementare [sandbox/ mediu de producție](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure). 
2. Vom arăta expertul **Pregătirea mediului**. 

> [!IMPORTANT]
> Asigurați-vă că versiunea aplicației selectate este 10.0.13 sau mai mare.

3. Pentru a pregări Project Operations, în secțiunea **Setări avansate**, selectați **Common Data Service**. 
4. Activați **Common Data Service Setarea** prin selectarea **Da** și apoi introduceți informații în câmpurile obligatorii:

  - Nume
  - Regiune
  - Limbă
  - Monedă
 
5. În câmpul **Common Data Service Șablon**, selectați **Project Operations** 

6. Selectați tipul de mediu pentru implementarea dvs. O versiune de probă bazată pe abonament vă va permite să implementați un mediu CDS timp de 30 de zile. 

![Setări de implementare](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> Selectați **De acord** pentru a confirma condițiile de utilizare și apoi selectați **Terminat** pentru a reveni la setările de implementare.

![Acord de implementare](./media/2DeploymentConsent.png)

7. Opțional - Aplicați date demonstrative pentru mediu. Mergi la **Setări avansate**, Selectați **Personalizați configurația bazei de date SQL**, și setați **Specificați un set de date pentru baza de date a aplicației** la **Demonstrativ**.

8. Completați câmpurile obligatorii rămase în expert și confirmați implementarea. Timpul de aprovizionare a mediului variază în funcție de tipul de mediu. Pregătirea poate dura până la șase ore.

  După ce implementarea se finalizează cu succes, mediul se va afișa ca **Implementat**.

9. Pentru a confirma că mediul a fost implementat cu succes, selectați **Autentificare** și conectați-vă la mediu pentru a confirma.

![Detalii despre mediu](./media/3EnvironmentDetails.png)

## <a name="apply-updates-to-the-finance-environment"></a>Aplicați actualizările la mediul de finanțe

Project Operations necesită un mediu financiar cu versiunea aplicației **10.0.13 (10.0.569.20009)** sau mai recentă.

Este posibil să trebuiască să aplicați actualizări de calitate mediului dvs. financiar pentru a primi această versiune.

1. În LCS, pe pagina **Detalii despre mediu**, în secțiunea **Actualizări disponibile**, selectați **Vizualizare actualizare**.

![Vizualizare actualizări](./media/5ViewUpdates.png)

2. Pe pagina **Actualizări binare**, selectați **Salvați pachetul.**

![Salvați pachetul](./media/6SavePackage.png)

3. Faceți clic pe **Selectați tot** și apoi selectați **Salvați pachetul**.

![Revizuiți și salvați actualizările](./media/7ReviewAndSaveUpdates.png)

4. Introduceți un nume și o descriere a pachetului, apoi selectați **Salvați**. În funcție de conexiunea la internet, acest proces poate dura ceva timp.

![Încărcați pachetul în Biblioteca de active](./media/8UploadPackageToAssetsLibrary.png)

5. După salvarea pachetului, selectați **Terminat** și salvați acest pachet în biblioteca Active din proiectul dvs. LCS.

Salvarea și validarea pachetului ar putea dura aproximativ 15 minute.

6. Pentru a aplica actualizarea, navigați la pagina **Detalii despre mediu** în LCS și selectați **Menţine** > **Aplicați actualizări**.

![Mențineți mediile](./media/9MaintainEnvironment.png)

7. În lista de actualizări, selectați pachetul pe care l-ați creat și selectați **Aplicare**.

![Aplicați actualizări](./media/10ApplyUpdates.png)

Întreținerea mediului va dura ceva timp. După ce este complet, mediul va reveni la o stare implementată.

![Mediu implementat](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a>Stabiliți o conexiune Dual Write 

1. În proiectul dvs. LCS, accesați pagina **Detalii despre mediu**.
2. Sub **Common Data Service Informații despre mediu**, selectați **Link către CDS pentru aplicații**.
3. După ce linkul este complet, selectați din nou **Link către CDS pentru aplicații**. Veți fi redirecționat către Dual Write în Finanțe.

![Link la CDS](./media/12LinktoCDS.png)

4. Selectați **Aplicați soluția** pentru a accesa entitățile care vor fi mapate în integrare.

![Aplicați soluții](./media/13ApplySolutions.png)

5. Selectați ambele soluții, **Dynamics 365 Finance and Operations Harta entității cu scriere dublă** și **Dynamics 365 Project Operations Hărți cu entități de scriere duală**, apoi selectați **Aplicare**.

![Confirmați soluțiile](./media/14ConfirmSolutions.png)

După aplicarea soluțiilor, entitățile Dual Write sunt aplicate mediului.

![Aplicarea soluțiilor](./media/15ApplyingSolutions.png)

După aplicarea entităților, toate mapările disponibile sunt listate în mediu.

![Hărți Dual Write](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a>Reîmprospătați entitățile de date după actualizare

1. În Finanțe, accesați spațiul de lucru **Gestionarea datelor**..

![Spațiul de lucru pentru gestionarea datelor](./media/16DataManagement.png)

2. Selectați dala **Parametrii cadru**.

![Parametrii de cadru](./media/17FrameworkParameters.png)

3. Pe pagina **Setări entitate**, selectați **Reîmprospătați lista entităților**.

![Reîmprospătare listă entitate](./media/18RefreshEntityList.png)

Reîmprospătarea va dura aproximativ 20 de minute. Veți primi o alertă când aceasta este completă.

![Reîmprospătare confirmare](./media/19RefreshConfirmation.png)

## <a name="update-security-settings-on-project-operations-on-dataverse"></a>Actualizați setările de securitate pentru Project Operations pe Dataverse

1. Mergeți la Project Operations pe mediul dvs. Dataverse. 
2. Accesați **Setări** > **Securitate** > **Roluri de securitate**. 
3. Pe pagina **Roluri de securitate**, în lista de roluri, selectați **utilizator de aplicație cu scriere duală** și selectați fila **Entități personalizate**.  
4. Verificați dacă rolul are permisiunile **Citit** și **Adăuga la** pentru:
      
      - **Tipul cursului de schimb valutar**
      - **Plan de conturi**
      - **Calendar fiscal**
      - **Registru**

5. După actualizarea rolului de securitate, accesați **Setări** > **Securitate** > **Echipe** și selectați echipa implicită în vizualizarea de echipă **Proprietar de afaceri locale**.
6. Selectați **Gestionați rolurile** și verificați dacă privilegiul de securitate **utilizator de aplicație cu scriere duală** este aplicabil pentru această echipă.

## <a name="run-project-operations-dual-write-maps"></a>Rulare hărți Project Operations Dual Write

1. În proiectul dvs. LCS, accesați pagina **Detalii despre mediu**.
2. Sub **Common Data Service Informații despre mediu**, selectați **Link către CDS pentru aplicații.** După ce selectați linkul, veți fi redirecționat către lista entităților din mapări.
3. Porniți hărțile așa cum este descris în tabelul următor. Asigurați-vă că urmați secvența așa cum este listată.

| **Mapare entități** | **Reîmprospătați entitatea** | **Sincronizare inițială** | **Coordonator pentru sincronizarea inițială** | **Rulați cerințe preliminare** | **Cerințe preliminare sincronizare inițială** |
| --- | --- | --- | --- | --- | --- |
| **Roluri de resurse ale proiectului pentru toate companiile (bookableresourcecategories)** | No | Da | Common Data Service | No | N\A |
| **Entități legale (cdm\_companii)** | No | Da | Aplicații Finance and Operations | No | N\A |
| **Registru (msdyn_ledgers)** | No | Da | Aplicații Finance and Operations | Da | Da, aplicații Finance and Operations |
| **Actualități de integrare a Project Operations (msdyn\_actuale)** | No | Nicio | N\A | Da | Nicio |
| **Linii de contract de proiect (salesorderdetails)** | Nicio | Nicio | N\A | Nicio | Nicio |
| **Entitate de integrare pentru relațiile de tranzacție ale proiectului (msdyn\_transactionconnections)** | Nicio | Nicio | N\A | Nicio | N\A |
| **Integrare Project Operations etape linie de contract (msdyn\_contractlinesscheduleofvalues)** | Nicio | Nicio | N\A | Nicio | N\A |
| **Entitate de integrare a Project Operations pentru estimări de cheltuieli (msdyn\_estimateslines)** | Nicio | Nicio | N\A | Nicio | N\A |
| **Entitate de integrare de export Project Operations pentru categorii de cheltuieli (msdyn\_expensecategories)** | Nicio | Nicio | N\A | Nicio | N\A |
| **Entitate de integrare a Project Operations pentru cheltuieli de export (msdyn\_expenses)** | Da | Nicio | N\A | Nicio | N\A |
| **Entitate de integrare a Project Operations pentru estimări orare (msdyn\_resourceassignments)** | Da | Nicio | N\A | Nicio | N\A |


4. Pentru a reîmprospăta entitatea, selectați numele hărții, apoi selectați **Reîmprospătați entități**. 


![Reîmprospătați harta](./media/20RefreshMapping.png)

5. După finalizarea reîmprospătării, rulați harta. Înainte de a activa următoarea hartă, verificați dacă harta din tabel se află în starea **Rulării**. Rularea hărților cu un număr mai mare de condiții prealabile ar putea dura ceva timp.

Pentru a rula o hartă cu condiții prealabile, activați comutarea **Afișați hărți de entități corelate**. Dacă tabelul indică **Sincronizare inițială preliminară** este **Nu**, verificați dacă semnalizarea **Sincronizare inițială** este **Dezactivat** în toate hărțile premise înainte de a-l rula.

![Rulați Harta](./media/21RunMap.png)

6. Validați toate hărțile legate de proiect sunt în starea de rulare.

![Toate hărțile rulează](./media/22AllMapsRunning.png)


## <a name="apply-configuration-data-in-cds-for-project-operations-optional"></a>Aplicarea datelor de configurare în CDS pentru Project Operations (opțional)

Dacă ați aplicat date demonstrative mediului financiar, consultați [Configurați și aplicați datele de configurare în Common Data Service pentru Project Operations](resource-apply-pro-setup-config-data.md) pentru a aplica date demonstrative mediului CDS.


Mediul dvs. Project Operations are acum asigurat accesul și este configurat. 
