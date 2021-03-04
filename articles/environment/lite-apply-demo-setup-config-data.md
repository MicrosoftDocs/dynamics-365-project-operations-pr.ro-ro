---
title: Aplicarea datelor de instalare și configurare demonstrative - simplificat
description: Acest subiect oferă informații despre cum se aplică datele de configurare și configurare demo pentru Project Operations.
author: sigitac
manager: Annbe
ms.date: 01/27/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 762b0cf317d442565a033f56033a53a5b5cc435c
ms.sourcegitcommit: b4298ca4729643c1040ef35dde8c67f829461ce7
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 01/29/2021
ms.locfileid: "5089134"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a>Aplicați date de configurare și instalare pentru Project Operations - simplificat 

_**Implementare simplificată - facturare de la tranzacție la proforma_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a>Cerințe preliminare

Înainte să începeți configurarea, trebuie să aveți un mediu Common Data Service (CDS) furnizat pentru Dynamics 365 Project Operations.


## <a name="instructions"></a>Instrucțiuni

1. Descărcați [Pachetul de date master](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip). 
2. Navigați la dosarul *ProjOpsDemoDataSetupAndMaster - CMT integrat* și rulați fișierul executabil, *DataMigrationUtility*.
3. Pe pagina 1 din Common Data Service Expertul Migrare configurare (CMT), selectați **Importați date** și apoi selectați **Continuare**.

    ![Migrarea configurării](./media/1ConfigurationMigration.png)

4. Pe pagina 2 a expertului CMT, selectați **Microsoft 365** ca **Tip de implementare**.
5. Selectați **Afișați o listă a organizațiilor disponibile** și casetele de selectare **Afișați avansat**.
6. Selectați regiunea chiriașului, introduceți acreditările, apoi selectați **Autentificare**.

   ![Conectare de configurare](./media/2ConfigurationSignin.png)

7. Pe pagina 3, din lista Organizațiilor de pe entitatea găzduită, selectați în ce organizație doriți să importați datele demo și apoi selectați **Autentificare**.
8. La pagina 4, selectați fișierul zip, *MasterAndSetupData* din folderul despachetat, *ProjOpsDemoDataSetupAndMaster - CMT integrat*.

   ![Fișier zip](./media/3ZipFile.png)

   ![Selectați un fișier](./media/4SelectAFile.png)

9. După selectarea fișierului zip, selectați **Importați date**.

   ![Importați date](./media/5ImportData.png)

10. Importul va rula aproximativ două-zece minute, în funcție de viteza rețelei. După finalizare, ieșiți din CMT Wizard. 
11. Verificați organizația pentru date în următoarele 20 de entități:

    -   Monedă
    -   Cont
    -   Unitate organizațională
    -   Contact
    -   Unitate
    -   Grup de unități
    -   Listă de prețuri
    -   Listă de prețuri parametru proiect 
    -   Frecvență factură
    -   Categoria resursei ce se poate rezerva
    -   Categorie tranzacție
    -   Categorie de cheltuieli
    -   Preț pentru rol
    -   Preț pentru categoria de tranzacție
    -   Caracteristică
    -   Resursă ce se poate rezerva
    -   Asociere categorie resursă care se poate rezerva
    -   Caracteristică a resursei ce se poate rezerva

    ![Finalizați importul](./media/6CompleteImport.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]