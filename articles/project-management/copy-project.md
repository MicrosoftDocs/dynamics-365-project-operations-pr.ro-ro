---
title: Copierea unui proiect
description: Acest subiect furnizează informații despre copierea proiectelor în Dynamics 365 Project Operations.
author: ruhercul
ms.date: 03/07/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: e9b637d2d282d123dfacb8a295292ea06549aa1e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8574445"
---
# <a name="copy-a-project"></a>Copierea unui proiect

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Cu Dynamics 365 Project Operations, puteți construi rapid proiecte noi selectând opțiunea **Copiați proiect** de pe formularul **Proiecte**. Pentru a copia un proiect, deschideți proiectul pe care doriți să îl copiați, apoi selectați **Copiați proiectul**. Acțiunea va copia următoarele:

- Proprietăți de proiect 
- Structură detaliată a proiectului
- Membrii echipei de proiect
- Estimări de proiect
- Estimări de cheltuieli proiect
- Estimări material de proiect
- Liste de verificare a proiectelor
- Găleți de proiect

## <a name="project-properties"></a>Proprietăți de proiect

Când proiectul este copiat, valorile din următoarele câmpuri sunt copiate.

| Câmp | Operațiuni de proiect Materiale nestocizate | Project Operations Lite | Proiect pentru web |
|-------|------------------------------------------|-------------------------|---------------------|
| Nume | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Descriere | :heavy_check_mark: | :heavy_check_mark: | |
| client | :heavy_check_mark: | :heavy_check_mark: | |
| Șablon de calendar | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Moneda | :heavy_check_mark: | :heavy_check_mark: | |
| Unitate contractantă | :heavy_check_mark: | :heavy_check_mark: | |
| Firmă proprietară | :heavy_check_mark: | | |
| Manager de proiect | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Status | :heavy_check_mark: | :heavy_check_mark: | |
| Stare generală proiect | :heavy_check_mark: | :heavy_check_mark: | |
| Comentarii | :heavy_check_mark: | :heavy_check_mark: | |
| Estimări | :heavy_check_mark: | :heavy_check_mark: | |
| <p>Dată pornire estimată</p><p><strong>Notă:</strong> Acest câmp specifică data la care proiectul este creat din copie. | :heavy_check_mark: | :heavy_check_mark: | |
| <p>Dată de încheiere estimată</p><p><strong>Notă:</strong> Data din acest câmp este ajustată în funcție de data de începere a noului proiect care a fost realizat din copie.</p> | :heavy_check_mark: | :heavy_check_mark: | |
| Efort (ore) | :heavy_check_mark: | :heavy_check_mark: | |
| Cost estimat cu munca | :heavy_check_mark: | :heavy_check_mark: | |
| Cheltuieli estimate | :heavy_check_mark: | :heavy_check_mark: | |
| Cost estimat materiale | | :heavy_check_mark: | |

> [!NOTE]
> Proiectul de copiere este o operațiune de lungă durată. Înregistrările proiectului, atributele relevante ale acestora și multe entități conexe sunt, de asemenea, copiate. Datorită naturii de funcționare îndelungată a operațiunii, după începerea copierii, pagina proiectului țintă este blocată pentru editare până la finalizarea operațiunii de copiere.

## <a name="work-breakdown-structure"></a>Structură detaliată a proiectului

Când proiectul este copiat, este copiată întreaga structură detaliată a proiectului încărcată cu resurse. Resursele numite sunt înlocuite cu resurse generice. Dacă resursele numite nu au aceleași ore de lucru ca și resursa generică, programul va fi recalculat și durata sarcinilor se poate modifica.

## <a name="project-team-members"></a>Membrii echipei de proiect

Când o echipă de proiect este copiată din proiectul sursă, resursele generice sunt copiate. Atribuirile de resurse generice sunt păstrate cum erau în proiectul sursă. Resursele denumite vor fi convertite în membri generici ai echipei.

> [!NOTE]
> Membrii echipei și sarcinile nu sunt copiate în Project for the Web.

## <a name="estimates"></a>Estimări

Când proiectul este copiat, resursele, cheltuielile și liniile de estimare a materialului sunt copiate din proiectul sursă. 

Pentru informații despre cum să accesați programul Copiere proiect, consultați [Elaborați șabloane de proiect cu Copiere proiect](dev-copy-project.md).

## <a name="quotes-and-contracts"></a>Oferte și contracte

Cotațiile și contractele nu sunt legate de proiectul de destinație.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
