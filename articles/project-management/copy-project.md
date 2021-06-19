---
title: Copierea unui proiect
description: Acest subiect furnizează informații despre copierea proiectelor în Dynamics 365 Project Operations.
author: ruhercul
ms.date: 05/21/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: c3055ab5b8c07faa2bc9167956d283e2a66029dd
ms.sourcegitcommit: 173f2b1f4e063c440a5f78d76d456c62aadbd89e
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 05/24/2021
ms.locfileid: "6091269"
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
- Data estimată de început: Aceasta este data la care proiectul este creat din copie.
- Data estimată de finalizare: această dată este ajustată pe baza datei de începere a noului proiect care a fost realizat din copie.
- Efort (ore)
- Cost estimat cu munca
- Cheltuieli estimate
- Cost estimat materiale

> [!NOTE]
> Proiectul de copiere este o operațiune de lungă durată. Înregistrările proiectului, atributele relevante ale acestora și multe entități conexe sunt, de asemenea, copiate. Datorită naturii de funcționare îndelungată a operațiunii, după începerea copierii, pagina proiectului țintă este blocată pentru editare până la finalizarea operațiunii de copiere.

## <a name="work-breakdown-structure"></a>Structură detaliată a proiectului

Când proiectul este copiat, este copiată întreaga structură detaliată a proiectului încărcată cu resurse. Resursele numite sunt înlocuite cu resurse generice. Dacă resursele numite nu au aceleași ore de lucru ca resursa generică, programul va fi recalculat și durata sarcinilor se poate modifica.

## <a name="project-team-members"></a>Membrii echipei de proiect

Când o echipă de proiect este copiată din proiectul sursă, resursele generice sunt copiate. Atribuirile de resurse generice sunt păstrate cum erau în proiectul sursă. Resursele denumite vor fi convertite în membri generici ai echipei.

## <a name="estimates"></a>Estimări

Când proiectul este copiat, resursele, cheltuielile și liniile de estimare a materialului sunt copiate din proiectul sursă. 

Pentru informații despre cum să accesați programul Copiere proiect, consultați [Elaborați șabloane de proiect cu Copiere proiect](dev-copy-project.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
