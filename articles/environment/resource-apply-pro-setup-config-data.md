---
title: Instalați și aplicați datele de configurare în Common Data Service
description: Acest subiect furnizează informații despre configurare și aplicarea datelor de configurare în Project Operations.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7742e81316b217066f9f3b8d5c23aa64f1a7efc4
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642243"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service"></a>Instalați și aplicați datele de configurare în Common Data Service 

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a>Cerințe preliminare

Înainte de a începe să configurați datele în Common Data Service (CDS), trebuie îndeplinite următoarele condiții prealabile:

1.  Furnizați un mediu CDS și un mediu Dynamics 365 Finance pentru Project Operations.
2.  Informații privind entitatea juridică de la Dynamics 365 Finance este partajat mediului CDS. Aceasta înseamnă că entitatea **Companie** din CDS are următoarele înregistrări ale companiei:
  - THPM
  - USPM
  - GBPM

## <a name="install-setup-and-configuration-data"></a>Instalați datele de instalare și configurare

1. Descărcați, deblocați și dezarhivați fișierul [Setare și configurare pachet de date](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).
2. Navigați la dosarul dezarhivat și rulați fișierul executabil, *DataMigrationUtility*.
3. Pe pagina 1 din Common Data Service Expertul Migrare configurare (CMT), selectați **Importați date** și apoi selectați **Continuare**.

![Migrarea configurării](./media/1ConfigurationMigration.png)

4. Pe pagina 2 a expertului CMT, selectați **Microsoft 365** ca **Tip de implementare**.
5. Selectați **Afișați o listă a organizațiilor disponibile** și casetele de selectare **Afișați avansat**.
6. Selectați regiunea entității dvs. găzduite, introduceți acreditările, apoi selectați **Conectare**.

![Conectare de configurare](./media/2ConfigurationSignin.png)

7. Pe pagina 3, din lista de organizații de pe entitatea găzduită, selectați organizația în care doriți să importați datele demo și apoi selectați **Conectare**.
8. La pagina 4, selectați fișierul arhivat, *SampleSetupAndConfigData* din dosarul arhivat.

![Selecție fișier arhivat](./media/3ZipFile.png)

![Selectați un fișier](./media/4SelectAFile.png)

9. După selectarea fișierului zip, selectați **Importați date**.

![Import date](./media/5ImportData.png)

10. Importul va rula aproximativ două-zece minute, în funcție de viteza rețelei. După ce se termină importarea, ieșiți din expertul CMT. 
11. Verificați organizația pentru date în următoarele 19 de entități:

  - Monedă
  - Unitate organizațională
  - Contact
  - Grup fiscal
  - Grup de clienți
  - Unitate
  - Grup de unități
  - Listă de prețuri
  - Listă de prețuri parametru proiect
  - Frecvență factură
  - Categoria resursei ce se poate rezerva
  - Categorie tranzacție
  - Categorie de cheltuieli
  - Preț pentru rol
  - Preț pentru categoria de tranzacție
  - Caracteristică
  - Resursă ce se poate rezerva
  - Asociere categorie resursă care se poate rezerva
  - Caracteristică a resursei ce se poate rezerva

![Finalizați importul](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a>Actualizați configurațiile Project Operations

1. Navigați la mediul CE. O puteți găsi deschizând fișierul [Centrul de administrare Power Platform](https://admin.powerplatform.microsoft.com/environments), selectând mediul, apoi selectând **Mediu deschis**. 

![Mediu deschis](./media/7OpenEnvironment.png)

2. Accesați **Proiecte** > **Resurse** și apoi selectați **Nou** pentru a crea o resursă care se poate rezerva pentru utilizatorul dvs.

![Resurse ce se pot rezerva](./media/8BookableResources.png)

3. Pe fila **General**, selectați-vă utilizatorul de administrator. Verificați dacă fusul orar se potrivește cu cel în care vă aflați. 

![Resursă nouă care se poate rezerva](./media/9NewBookableResource.png)

4. Pe fila **Planificare**, în câmpul **Companie**, alegeți compania **USPM**, apoi selectați **Salvare**. 

![Filă de planificare](./media/10SchedulingTab.png)

5. Selectați fila **Ore de lucru**.  

![Ore de lucru](./media/11WorkHours.png)

6. Faceți dublu clic pe orice valoare din calendar și selectați **Editați** > **Toate evenimentele din serie**. 

![Calendar de lucru](./media/12WorkCalendar.png)

7. Schimbați orele de lucru într-o zi de lucru de opt (8) ore, marcați weekendurile ca zile nelucrătoare și asigurați-vă că fusul orar se potrivește cu al dvs. 
8. Selectați **Salvați și închideți**.

![Actualizare calendar](./media/13UpdateCalendar.png)

9. Accesați **Setări** > **Șabloane de calendar** și selectați **Nou**.
 
 ![Șabloane de calendar](./media/14CalendarTemplates.png)
 
 10. Introduceți un nume, selectați resursa șablon pe care ați creat-o, apoi selectați **Salvare**. 
 
 ![Salvați șablonul de calendar](./media/15SaveCalendarTemplate.png)
 
 11. Accesați **Parametri** și faceți dublu clic pe înregistrare. 
 
 ![Parametri proiect](./media/16ProjectParameters.png)
 
12. Actualizați următoarele câmpuri:

 - **Companie implicită**: USPM
 - **Unitate organizațională implicită**: Contoso Robotics Global
 - **Frecvența facturii**: a șaptea și ultima zi
 - **Șablon de oră de lucru**: modificați șablonul pe care l-ați creat.

13. Selectați **Salvare**. 

![Parametri de proiect actualizați](./media/17UpdatedProjectParameters.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]