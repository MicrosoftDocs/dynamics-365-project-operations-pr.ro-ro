---
title: Asigurarea accesului pentru un nou mediu
description: Acest articol furnizează informații despre cum să asigurați accesul la un nou mediu în Project Operations.
author: sigitac
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 78f40ebe79c038799fbc59902442ad6c23fb94d4
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028533"
---
# <a name="provision-a-new-environment"></a>Asigurarea accesului pentru un nou mediu

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_



Acest articol furnizează informații despre cum să asigurați accesul la un mediu nou Dynamics 365 Project Operations pentru scenarii bazate pe resurse/fără stoc.

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a>Activați pregătirea automată a Project Operations într-un proiect LCS

Utilizați pașii următori pentru a activa fluxul automatizat de pregătire pentru Project Operations pentru proiectul dvs. LCS.

1. Accesați [LCS](https://lcs.dynamics.com/v2) și selectați titlul **Previzualizarea gestionării caracteristicilor**.
2. În lista **Caracteristică de previzualizare**, selectați **Caracteristică Project Operations** și apoi selectați **Caracteristica de previzualizare activată** pentru a activa Project Operations.

   > [!NOTE]
   > Acest pas se efectuează o singură dată pentru fiecare proiect LCS.

## <a name="provision-a-project-operations-environment"></a>Furnizarea unui mediu de Project Operations

1. Deschideți un nou [mediu demonstrativ](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) Dynamics 365 Finance sau o/un [implementare sandbox/mediu de producție](/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure). 
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

     ![Setări de implementare.](./media/1DeploymentSettings.png)

    > [!IMPORTANT]
    > Selectați **De acord** pentru a confirma condițiile de utilizare și apoi selectați **Terminat** pentru a reveni la setările de implementare.
    >
    >![Acord de implementare.](./media/2DeploymentConsent.png)

7. Opțional - Aplicați date demonstrative pentru mediu. Mergi la **Setări avansate**, Selectați **Personalizați configurația bazei de date SQL**, și setați **Specificați un set de date pentru baza de date a aplicației** la **Demonstrativ**.
8. Completați câmpurile obligatorii rămase în expert și confirmați implementarea. Timpul de aprovizionare a mediului variază în funcție de tipul de mediu. Pregătirea poate dura până la șase ore.

   După ce implementarea se finalizează cu succes, mediul se va afișa ca **Implementat**.

9. Pentru a confirma că mediul a fost implementat cu succes, selectați **Autentificare** și conectați-vă la mediu pentru a confirma.

    ![Detalii despre mediu.](./media/3EnvironmentDetails.png)

## <a name="apply-updates-to-the-finance-environment"></a>Aplicați actualizările la mediul de finanțe

Project Operations necesită un mediu financiar cu versiunea aplicației **10.0.13 (10.0.569.20009)** sau mai recentă.

Este posibil să trebuiască să aplicați actualizări de calitate mediului dvs. financiar pentru a primi această versiune.

1. În LCS, pe pagina **Detalii despre mediu**, în secțiunea **Actualizări disponibile**, selectați **Vizualizare actualizare**.

    ![Vizualizare actualizări.](./media/5ViewUpdates.png)

2. Pe pagina **Actualizări binare**, selectați **Salvați pachetul.**

    ![Salvați pachetul.](./media/6SavePackage.png)

3. Faceți clic pe **Selectați tot** și apoi selectați **Salvați pachetul**.

    ![Revizuiți și salvați actualizările.](./media/7ReviewAndSaveUpdates.png)

4. Introduceți un nume și o descriere a pachetului, apoi selectați **Salvați**. În funcție de conexiunea la internet, acest proces poate dura ceva timp.

    ![Încărcați pachetul în Biblioteca de active.](./media/8UploadPackageToAssetsLibrary.png)

5. După salvarea pachetului, selectați **Terminat** și salvați acest pachet în biblioteca Active din proiectul dvs. LCS.

   Salvarea și validarea pachetului ar putea dura aproximativ 15 minute.

6. Pentru a aplica actualizarea, navigați la pagina **Detalii despre mediu** în LCS și selectați **Menţine** > **Aplicați actualizări**.

    ![Mențineți mediile.](./media/9MaintainEnvironment.png)

7. În lista de actualizări, selectați pachetul pe care l-ați creat și selectați **Aplicare**.

    ![Aplicați actualizări.](./media/10ApplyUpdates.png)

   Întreținerea mediului va dura ceva timp. După ce este complet, mediul va reveni la o stare implementată.

    ![Mediu implementat.](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a>Stabiliți o conexiune Dual Write 

1. În proiectul dvs. LCS, accesați pagina **Detalii despre mediu**.
2. Sub **Common Data Service Informații despre mediu**, selectați **Link către CDS pentru aplicații**.
3. După ce linkul este complet, selectați din nou **Link către CDS pentru aplicații**. Veți fi redirecționat către Dual Write în Finanțe.

    ![Link la CDS.](./media/12LinktoCDS.png)

4. Selectați **Aplicați soluția** pentru a accesa entitățile care vor fi mapate în integrare.

    ![Aplicați soluții.](./media/13ApplySolutions.png)

5. Selectați ambele soluții, **Hartă entități cu scriere duală Dynamics 365 Finance Dual Write Entity Map** și **Hartă entități cu scriere duală** Dynamics 365 Project Operations, apoi selectați **Aplicare**.

    ![Confirmați soluțiile.](./media/14ConfirmSolutions.png)

    După aplicarea soluțiilor, entitățile Dual Write sunt aplicate mediului.

    ![Aplicarea soluțiilor.](./media/15ApplyingSolutions.png)

    După aplicarea entităților, toate mapările disponibile sunt listate în mediu.

    ![Hărți Dual Write.](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a>Reîmprospătați entitățile de date după actualizare

1. În Finanțe, accesați spațiul de lucru **Gestionarea datelor**..

    ![Spațiul de lucru pentru gestionarea datelor.](./media/16DataManagement.png)

2. Selectați dala **Parametrii cadru**.

    ![Parametrii de cadru.](./media/17FrameworkParameters.png)

3. Pe pagina **Setări entitate**, selectați **Reîmprospătați lista entităților**.

    ![Reîmprospătare listă entitate.](./media/18RefreshEntityList.png)

Reîmprospătarea va dura aproximativ 20 de minute. Veți primi o alertă când aceasta este completă.

  ![Reîmprospătare confirmare.](./media/19RefreshConfirmation.png)

## <a name="update-security-settings-on-project-operations-on-dataverse"></a>Actualizați setările de securitate pentru Project Operations pe Dataverse

1. Mergeți la Project Operations pe mediul dvs. Dataverse. 
2. Accesați **Setări** > **Securitate** > **Roluri de securitate**. 
3. Pe pagina **Roluri de securitate**, în lista de roluri, selectați **utilizator de aplicație cu scriere duală** și selectați fila **Entități personalizate**.  
4. Verificați dacă rolul are permisiuni **Citit** și **Adăugare la** pentru următoarele entități:
      
      - **Tipul cursului de schimb valutar**
      - **Plan de conturi**
      - **Calendar fiscal**
      - **Registru**
      - **Companie**
      - **Cheltuială**

5. După actualizarea rolului de securitate, accesați **Setări** > **Securitate** > **Echipe** și selectați echipa implicită în vizualizarea de echipă **Proprietar de afaceri locale**.
6. Selectați **Gestionați rolurile** și verificați dacă privilegiul de securitate **utilizator de aplicație cu scriere duală** este aplicabil pentru această echipă.

## <a name="run-project-operations-dual-write-maps"></a>Rulare hărți Project Operations Dual Write

1. În proiectul dvs. LCS, accesați pagina **Detalii despre mediu**.
2. Sub **Common Data Service Informații despre mediu**, selectați **Link către CDS pentru aplicații.** După ce selectați linkul, veți fi redirecționat către lista entităților din mapări.
3. Porniți hărțile. Pentru mai multe informații, consultați [versiuni mapări cu scriere duală Project Operations](resource-dual-write-maps.md#project-operations-dual-write-maps)
4. Validați toate hărțile legate de proiect sunt în starea de rulare.

    ![Toate hărțile rulează.](./media/22AllMapsRunning.png)


## <a name="apply-configuration-data-in-cds-for-project-operations-optional"></a>Aplicarea datelor de configurare în CDS pentru Project Operations (opțional)

Dacă ați aplicat date demonstrative mediului financiar, consultați [Configurați și aplicați datele de configurare în Common Data Service pentru Project Operations](resource-apply-pro-setup-config-data.md) pentru a aplica date demonstrative mediului CDS.


Mediul dvs. Project Operations are acum asigurat accesul și este configurat. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
