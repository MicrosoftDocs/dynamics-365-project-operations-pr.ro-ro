---
title: Aplicarea datelor demonstrative unui mediu găzduit în Finance Cloud
description: Acest subiect explică modul de aplicare a datelor demo din Project Operations la un mediu Dynamics 365 Finance găzduit în cloud.
author: sigitac
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7d8a198b3bfd71ae08bc338d17896519b5ffd6b8
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000181"
---
# <a name="apply-demo-data-to-a-finance-cloud-hosted-environment"></a>Aplicarea datelor demonstrative unui mediu găzduit în Finance Cloud

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

> [!IMPORTANT]
> Acest subiect se aplică numai Microsoft Dynamics 365 Finance versiunea 10.0.13 și poate fi efectuată numai pe un mediu găzduit în cloud. Finalizați pașii din acest subiect **ÎNAINTE DE** aplicați actualizări de calitate mediului.

1. În proiectul dvs. LCS, deschideți pagina **Detalii despre mediu**. Observați că include detaliile necesare pentru a vă conecta la mediu utilizând Remote Desktop Protocol (RDP).

![Detalii despre mediul ](./media/1EnvironmentDetails.png)

Primul set de acreditări evidențiate sunt acreditările contului local și conțin un hyperlink către conexiunea desktop la distanță. Acreditările includ numele de utilizator și parola administratorului mediului. Al doilea set de acreditări este utilizat pentru a vă conecta la SQL Server în acest mediu.

2. conectați-vă la mediu prin hyperlink în **Conturi locale**, și utilizați **Acreditări de cont local** pentru a autentifica.
3. Accesați **Servicii de informare pe internet** > **Grupuri de aplicații** > **Serviciul AOSS** și opriți serviciul. Opriți serviciul în acest moment, astfel încât să puteți continua să înlocuiți baza de date SQL.

![Stop AOS](./media/2StopAOS.png)

4. Accesați **Servicii** și opriți următoarele două elemente:

- Microsoft Dynamics 365 Unified Operations: Serviciul de gestionare a loturilor
- Microsoft Dynamics 365 Unified Operations: Cadrul de export al importului de date

![Opriți serviciile](./media/3StopServices.png)

5. Deschideți Microsoft SQL Server Management Studio. Conectați-vă cu acreditările serverului SQL și utilizați utilizatorul și parola axdbadmin din pagina LCS **Detalii despre medii**.

![SQL Server Management Studio](./media/4SSMS.png)

6. În Object Explorer, **Baze de date** și localizați **AXDB**. Veți înlocui baza de date cu o nouă bază de date care se află în [Centrul de descărcare](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip). 
7. Copiați fișierul zip în VM-ul în care sunteți îndepărtat și extrageți conținutul zip.
8. În SQL Server Management Studio, faceți clic dreapta **AxDB**, apoi selectați **Sarcini** > **Restabili** > **Bază de date**.

![Restaurați baza de date](./media/5RestoreDatabase.png)

9. Selectați **Dispozitiv sursă** și navigați la fișierul extras din zip pe care l-ați copiat.

![Dispozitive sursă](./media/6SourceDevice.png)

10. Selectați **Opțiuni**, apoi selectați **Suprascrieți baza de date existentă** și **Închideți conexiunile existente la baza de date destinație**. 
11. Selectați **OK**.

![Restaurați setări](./media/7RestoreSetting.png)

Veți primi confirmarea că restaurarea AXDB a avut succes. După ce primiți această confirmare, puteți închide SQL Services Management Studio.

12. Reveniți la **Servicii de informare pe internet** > **Grupuri de aplicații** > **Serviciul AOSS** și porniți serviciul AOSS.
13. Accesați **Servicii** și porniți cele două servicii pe care le-ați oprit mai devreme.

14. Găsiți instrumentul AdminUserProvisioning pe această mașină virtuală. Căutați sub, K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe.
15. Rulați fișierul .ext folosind adresa de utilizator din câmpul **Adresa de email**. 
16. Selectați **Remitere**.

![Furnizare acces utilizator administrator](./media/8AdminUserProvisioning.png)

Finalizarea acestui proces durează câteva minute. Ar trebui să primiți un mesaj de confirmare a faptului că utilizatorul administratorului a fost actualizat cu succes.

17. În cele din urmă, executați Command Prompt ca administrator și efectuați iisreset

![Reiniţializare IIS](./media/9IISReset.png)

18. Închideți sesiunea desktop la distanță și utilizați pagina LCS **Detalii despre mediu** pentru a vă conecta la mediu pentru a confirma că funcționează conform așteptărilor.

![Finance and Operations](./media/10FinanceAndOperations.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]