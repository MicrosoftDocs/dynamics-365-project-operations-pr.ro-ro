---
title: Aplicarea datelor de instalare și configurare demonstrative - simplificat
description: Acest articol oferă informații despre cum se aplică datele de instalare și configurare demo pentru Project Operations.
author: sigitac
ms.date: 11/29/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 8ac8c910ce2d91fa47df08e8fb6efb723c0dc5fa
ms.sourcegitcommit: 38cb012502cbd640abbc21a0912b195112b27ccb
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 11/30/2022
ms.locfileid: "9811041"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a>Aplicați date de configurare și instalare pentru Project Operations - simplificat 

_**Implementare simplificată - facturare de la tranzacție la proforma_



## <a name="prerequisites"></a>Cerințe preliminare

Înainte să începeți configurarea, trebuie să aveți un mediu Dataverse furnizat pentru Dynamics 365 Project Operations.


## <a name="instructions"></a>Instrucțiuni

1. Descărcați [Pachetul de date de configurare](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData-%20CE%20only.zip). 
1. Navigați la dosar *ProjOpsSampleSetupData - CE numai CMT* și rulați fișierul executabil, *DataMigrationUtility*.
1. Pe pagina 1 din Common Data Service Expertul Migrare configurare (CMT), selectați **Importați date** și apoi selectați **Continuare**.

    ![Migrare configurare.](./media/1ConfigurationMigration.png)

1. Pe pagina 2 a Expertului CMT, selectați **Microsoft 365** după **Tipul de implementare**.
1. Selectați **Afișați o listă a organizațiilor disponibile** și casetele de selectare **Afișați avansat**.
1. Selectați regiunea chiriașului, introduceți acreditările, apoi selectați **Autentificare**.

   ![Conectare de configurare.](./media/2ConfigurationSignin.png)

1. Pe pagina 3, din lista Organizațiilor de pe entitatea găzduită, selectați în ce organizație doriți să importați datele demo și apoi selectați **Autentificare**.
1. La pagina 4, selectați fișierul zip, *SampleSetupAndConfigData* din folderul despachetat, *ProjOpsSampleSetupData - CMT numai CE*.

   ![Fișier zip.](./media/3ZipFile.png)

   ![Selectați un fișier.](./media/4SelectAFile.png)

1. După selectarea fișierului zip, selectați **Importați date**.

   ![Importul datelor.](./media/5ImportData.png)

1. Importul va rula aproximativ două-zece minute, în funcție de viteza rețelei. După finalizare, ieșiți din CMT Wizard. 
1. Verificați organizația pentru date în următoarele 18 de entități:

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

    ![Finalizați importul.](./media/6CompleteImport.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
