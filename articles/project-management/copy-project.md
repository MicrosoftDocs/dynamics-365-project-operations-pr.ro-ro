---
title: Copierea unui proiect
description: Acest articol oferă informații despre copierea proiectelor în Dynamics 365 Project Operations.
author: ruhercul
ms.date: 03/07/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: b358f9e45278d886f3e6e8e8cd747fc0ea30212b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925779"
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
- Liste de verificare proiect
- Pachete de proiect

## <a name="project-properties"></a>Proprietăți de proiect

Când proiectul este copiat, valorile din următoarele câmpuri sunt copiate.

| Câmp | Project Operations pentru materiale care nu se află pe stoc | Project Operations Lite | Project for the Web |
|-------|------------------------------------------|-------------------------|---------------------|
| Nume | :bifă solidă: | :bifă solidă: | :bifă solidă: |
| Descriere | :bifă solidă: | :bifă solidă: | |
| client | :bifă solidă: | :bifă solidă: | |
| Șablon de calendar | :bifă solidă: | :bifă solidă: | :bifă solidă: |
| Moneda | :bifă solidă: | :bifă solidă: | |
| Unitate contractantă | :bifă solidă: | :bifă solidă: | |
| Firmă proprietară | :bifă solidă: | | |
| Manager de proiect | :bifă solidă: | :bifă solidă: | :bifă solidă: |
| Status | :bifă solidă: | :bifă solidă: | |
| Stare generală proiect | :bifă solidă: | :bifă solidă: | |
| Comentarii | :bifă solidă: | :bifă solidă: | |
| Estimări | :bifă solidă: | :bifă solidă: | |
| <p>Dată pornire estimată</p><p><strong>Notă:</strong> Acest câmp precizează data la care proiectul este creat din copie. | :bifă solidă: | :bifă solidă: | |
| <p>Dată de încheiere estimată</p><p><strong>Notă:</strong> Data din acest câmp este ajustată pe baza datei de începere a noului proiect care a fost realizat din copie.</p> | :bifă solidă: | :bifă solidă: | |
| Efort (ore) | :bifă solidă: | :bifă solidă: | |
| Cost estimat cu munca | :bifă solidă: | :bifă solidă: | |
| Cheltuieli estimate | :bifă solidă: | :bifă solidă: | |
| Cost estimat materiale | | :bifă solidă: | |

> [!NOTE]
> Proiectul de copiere este o operațiune de lungă durată. Înregistrările proiectului, atributele relevante ale acestora și multe entități conexe sunt, de asemenea, copiate. Datorită naturii de funcționare îndelungată a operațiunii, după începerea copierii, pagina proiectului țintă este blocată pentru editare până la finalizarea operațiunii de copiere.

## <a name="work-breakdown-structure"></a>Structură detaliată a proiectului

Când proiectul este copiat, este copiată întreaga structură detaliată a proiectului încărcată cu resurse. Resursele numite sunt înlocuite cu resurse generice. Dacă resursele numite nu au aceleași ore de lucru ca resursa generică, programul va fi recalculat și durata sarcinilor ar putea fi modificată.

## <a name="project-team-members"></a>Membrii echipei de proiect

Când o echipă de proiect este copiată din proiectul sursă, resursele generice sunt copiate. Atribuirile de resurse generice sunt păstrate cum erau în proiectul sursă. Resursele denumite vor fi convertite în membri generici ai echipei.

> [!NOTE]
> Membrii echipei și sarcinile nu sunt copiate în Project for the Web.

## <a name="estimates"></a>Estimări

Când proiectul este copiat, resursele, cheltuielile și liniile de estimare a materialului sunt copiate din proiectul sursă. 

Pentru informații despre cum să accesați programul Copiere proiect, consultați [Elaborați șabloane de proiect cu Copiere proiect](dev-copy-project.md).

## <a name="quotes-and-contracts"></a>Oferte și contracte

Ofertele și contractele nu sunt legate de proiectul de destinație.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
