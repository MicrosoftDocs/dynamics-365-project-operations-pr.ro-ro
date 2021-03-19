---
title: Copierea unui proiect
description: Acest subiect furnizează informații despre copierea proiectelor în Dynamics 365 Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 02/22/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: af1942e81691d9e13fdcbbf68599c1a8a4004582
ms.sourcegitcommit: 24528bb9c0ef8898077cb3bc672daa211c0e73aa
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 03/04/2021
ms.locfileid: "5479534"
---
# <a name="copy-a-project"></a>Copierea unui proiect

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Cu Dynamics 365 Project Operations, puteți construi rapid proiecte noi selectând opțiunea **Copiați proiect** de pe formularul **Proiecte**. Pentru a copia un proiect, deschideți proiectul pe care doriți să îl copiați, apoi selectați **Copiați proiectul**. Acțiunea va copia:

- Proprietățile proiectului (Data estimată de începere este copiată din proiectul sursă)
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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
