---
title: Aplicarea datelor de instalare și configurare demonstrative
description: Acest subiect oferă informații despre cum se aplică datele de configurare și configurare demo pentru Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 42e02f393e89d20b2a462645f519a3792bee8f2f
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949027"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations-lite-deployment---deal-to-proforma-invoicing"></a>Aplicați datele de configurare și configurare a demonstrației pentru implementarea Project Operations simplificat - de la tranzacție la factura proforma

_**Implementare simplificată - facturare de la tranzacție la proforma_

1. Descărcați [Pachetul de date master](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip). 
2. Navigați la dosarul *ProjOpsDemoDataSetupAndMaster - CMT integrat* și rulați fișierul executabil, *DataMigrationUtility*.
3. Pe pagina 1 din Common Data Service Expertul Migrare configurare (CMT), selectați **Importați date** și apoi selectați **Continuare**.

![Migrarea configurării](./media/1ConfigurationMigration.png)

4. Pe pagina 2 a Expertului CMT, selectați **Office 365** după **Tipul de implementare**.
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
- Detaliu frecvență factură
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
