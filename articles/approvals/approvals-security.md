---
title: Securitate și aprobări
description: Acest articol oferă informații despre configurarea de securitate pentru lucrul cu aprobări în Microsoft Dynamics 365 Project Operations.
author: stsporen
ms.date: 08/29/2022
ms.topic: security
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 0dcadaa142bf46e4c54f160759602ac749022108
ms.sourcegitcommit: 73aff2b3c5e5b8a2254735b0b25931cbb6754c87
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/20/2022
ms.locfileid: "9709413"
---
# <a name="security-and-approvals"></a>Securitate și aprobări

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Microsoft Dynamics 365 Project Operations utilizează două roluri de securitate pentru a permite aprobarea înregistrărilor de timp, cheltuieli și materiale:

- Aprobator proiect
- Administrator aprobator de proiect

## <a name="project-approver"></a>Aprobator proiect

Trebuie să aveți rolul de securitate **Aprobator de proiect** pentru a aproba timpul de proiect, cheltuielile și intrările de materiale. De asemenea, trebuie să aveți acces la entitățile relevante corespunzătoare, cum ar fi **Proiect**. Acest acces poate fi atribuit de cineva care are rolul de **Manager de proiect**. În plus, trebuie să fii membru al echipei de proiect și să fii marcat ca aprobator.

Pentru a aproba intrări non-proiect, trebuie să fii managerul solicitantului.

## <a name="project-approver-admin"></a>Administrator aprobator de proiect

> [!NOTE]
> Funcția [Seturi de aprobare](approval-sets.md) trebuie să fie activată înainte de a putea utiliza funcționalitatea de administrare a avizului de proiect.

Rolul de securitate **Administrator aprobator de proiect** permite utilizatorilor să ocolească politicile și permite aprobarea intrărilor în toate proiectele. Atribuirea acestui rol va ocoli logica de validare care necesită apartenența la echipă și marcarea ca aprobator. Trebuie să aveți acces la tabelele relevante corespunzătoare, cum ar fi **Proiect**, prin rolurile de securitate atribuite dvs.

Contextul utilizatorului SISTEM ocolește validările în același mod ca rolul de securitate Administrator aprobator de proiect.
