---
title: Copierea unui proiect
description: Acest subiect furnizează informații despre copierea proiectelor în Dynamics 365 Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: cf80f2a1cd27aae33d123e45dee70d94ea4d01a9
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082737"
---
# <a name="copy-a-project"></a>Copierea unui proiect

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Cu Dynamics 365 Project Operations, puteți construi rapid proiecte noi selectând **Copie proiect** pe formularul **Proiecte**. Pentru a copia un proiect, deschideți proiectul pe care doriți să îl copiați, apoi selectați **Copiați proiectul**. Acțiunea va copia:

- Proprietăți de proiect
- Structura detaliată a proiectului
- Membrii echipei de proiect
- Estimări de proiect
- Estimări de cheltuieli proiect

## <a name="project-properties"></a>Proprietăți de proiect

Când proiectul este copiat, valorile din următoarele câmpuri sunt copiate:

- Nume
- Descriere
- Client
- Șablon de calendar
- Monedă
- Unitate contractantă
- Manager de proiect
- Stare
- Stare generală proiect
- Comentarii
- Estimări
- Dată pornire estimată
- Data de terminare
- Efort (ore)
- Cost estimat cu munca
- Cheltuieli estimate

## <a name="work-breakdown-structure"></a>Structură detaliată a proiectului

Când proiectul este copiat, este copiată întreaga structură detaliată a proiectului încărcată cu resurse. Resursele numite sunt înlocuite cu resurse generice. Dacă resursele numite nu au aceleași ore de lucru ca resursa generică, programul va fi recalculat și durata sarcinilor se poate modifica.

## <a name="project-team-members"></a>Membrii echipei de proiect

Când o echipă de proiect este copiată din proiectul sursă, resursele generice sunt copiate. Atribuirile de resurse generice sunt păstrate cum erau în proiectul sursă. Resursele denumite vor fi convertite în membri generici ai echipei.

## <a name="estimates"></a>Estimări

Când proiectul este copiat, ambele linii de estimare a resurselor și a cheltuielilor sunt copiate din proiectul sursă. 

Pentru informații despre cum să accesați programul Copiere proiect, consultați [Elaborați șabloane de proiect cu Copiere proiect](dev-copy-project.md).
