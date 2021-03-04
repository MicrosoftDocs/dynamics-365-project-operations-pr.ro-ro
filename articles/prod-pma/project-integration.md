---
title: Integrare Microsoft Project Client
description: Planificarea și menținerea unui plan de proiect pot fi complexe, astfel încât managerii de proiect trebuie să utilizeze instrumente care îi ajută să gestioneze această sarcină. Integrarea cu Microsoft Project Client oferă suport pentru deschiderea și gestionarea unei structuri detaliate a proiectului.
author: Yowelle
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 732b72d9819fc149c4b2c783b3dc7f7eec3f0393
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082857"
---
# <a name="microsoft-project-client-integration"></a>Integrare Microsoft Project Client

[!include [banner](../includes/banner.md)]

Planificarea și menținerea unui plan de proiect pot fi complexe, astfel încât managerii de proiect trebuie să utilizeze instrumente care îi ajută să gestioneze această sarcină. Integrarea cu Microsoft Project Client oferă suport pentru deschiderea și gestionarea unei structuri detaliate a proiectului. Managerul de proiect poate publica orice modificări înapoi la structura detaliată a proiectului Dynamics 365 Finance.

> [!NOTE]
> Dacă utilizați actualizarea din iulie (versiunea 10.0.4), trebuie să instalați KB 4054797 și 4055884.

## <a name="configure-the-microsoft-project-client-add-in"></a>Configurați programul de completare Microsoft Project Client
Pentru a permite integrarea cu Microsoft Project Client, a Microsoft Dynamics 365 programul de completare trebuie să fie instalat în aplicația client Microsoft Project a utilizatorului. Acest lucru se face prin deschiderea **Spațiul de lucru pentru gestionarea proiectelor**.

•   Faceți clic pe **Configurați programul de completare pentru clientul de proiect** din la secțiunea **Linkuri** > **Configurare** a spațiului de lucru.

•   Faceți clic pe **Deschidere** , apoi apăsați **Rulare** când vi se solicită.

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a>Deschideți și editați o structură detaliată a proiectului existentă în Microsoft Project Client
Dacă un proiect în Dynamics 365 Finance are deja creată o structură detaliată a proiectului, structura detaliată a proiectului poate fi deschisă în aplicația Microsoft Project Client dacă structura detaliată a proiectului este în starea de schiță. Pentru a deschide din pagina **Proiect** , faceți clic pe linkul **Deschideți în Microsoft Project** din fila **Plan**. Această pagină poate fi deschisă și din aplicația Microsoft Project Client făcând clic pe **Deschidere** în fila **Microsoft Dynamics 365**. Selectați **Entitate legală** și **Proiect** din listă.

> [!NOTE]
> Dacă folosiți Internet Explorer ca browser, va trebui să faceți clic pe **Salvare** pentru a deschide manual din locația în care este descărcat fișierul. Sau faceți clic pe **Salvare și deschidere** pentru a deschide fișierul în Microsoft Project Client. Nu redenumiți numele fișierului atunci când salvați.

Înainte de a efectua modificări ale fișierului utilizând Microsoft Project Client, trebuie să îl verificați. Faceți clic pe **Verificare** în fila **Microsoft Dynamics 365**. Acest lucru va împiedica ceilalți utilizatori să editeze structura detaliată a proiectului din Finance în același timp. Pentru a publica structura detaliată a proiectului după finalizarea oricăror modificări, faceți clic pe **Confirmare** pe fila **Microsoft Dynamics 365**.

Dacă o echipă de proiect a fost deja adăugată la proiect în Finance, lista resurselor va fi completată cu membrii echipei. Dacă o echipă de proiect nu a fost încă adăugată la proiect, puteți selecta resurse și puteți construi echipa în cadrul Microsoft Project Client făcând clic pe butonul **Resurse** de pe fila **Microsoft Dynamics 365**. 

Următoarele date vor fi sincronizate înapoi la Finance ca parte a procesului de confirmare:

•   Numele activității

•   Data de început

•   Data de terminare

•   Predecesori

•   Numele resurselor

•   Categorie

•   Categorie resursă

•   Ore de lucru

•   Note

•   Prioritate

> [!NOTE]
> Dacă adăugați alte coloane în fișierul dvs. Microsoft Project Client, acestea nu vor fi salvate în fișier și nu vor fi afișate când fișierul este deschis din nou.

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>Creați structura detaliată a proiectului pentru un proiect existent utilizând Microsoft Project Client
Pentru a crea o nouă structură detaliată a proiectului utilizând Microsoft Project Client, urmați acești pași:


1.  Deschideți Microsoft Project Client.

2.  În fila **Microsoft Dynamics 365** , faceți clic pe **Deschidere**.

3.  Selectați **Entitatea legală** pentru proiect.

4.  Selectați **Proiect**.

5.  Faceți clic pe **Verificare** pe fila **Microsoft Dynamics 365**.

6.  Când sunteți gata să publicați în Finance, faceți clic pe **Verificare** pe fila **Microsoft Dynamics 365**.

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>Înlocuiți structura detaliată a proiectului existentă pentru un proiect existent utilizând Microsoft Project Client
Pentru a crea o nouă structură detaliată a proiectului utilizând Microsoft Project Client și a înlocui o structură detaliată a proiectului existentă pentru un proiect existent, urmați acești pași:

1.  Deschideți Microsoft Project Client.

2.  Creați planificarea în Microsoft Project Client.

3.  Din fila **Microsoft Dynamics 365** , faceți clic pe **Salvare modificări** > **Înlocuire proiect existent**.

4.  Selectați **Entitatea legală** pentru proiect.

5.  Selectați **Proiect**.

6.  Faceți clic pe **OK**.

## <a name="create-a-new-project-from-within-microsoft-project-client"></a>Creați un proiect nou din Microsoft Project Client


1.  Deschideți Microsoft Project Client.

2.  Creați planificarea în Microsoft Project Client.

3.  Din fila **Microsoft Dynamics 365** , faceți clic pe **Salvare modificări** > **Salvare ca proiect nou**.

4.  Selectați **Entitatea legală** pentru proiect.

5.  Introduceți **ID-ul proiectului** , dacă este necesar.

6.  Introduceți **Numele proiectului**.

7.  Selectați **Tipul proiectului** , **Grup de proiect** și **ID-ul contractului de proiect**. Alternativ, puteți crea un nou contract de proiect făcând clic pe **Nou**.

8.  Selectați **Calendar** pentru a fi folosit pentru resurse.

11. Faceți clic pe **OK**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]