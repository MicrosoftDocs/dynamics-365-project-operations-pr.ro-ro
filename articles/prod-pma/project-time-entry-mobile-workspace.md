---
title: Spațiul de lucru mobil pentru intrarea de timp a proiectului
description: Acest articol oferă informații despre spațiul de lucru mobil pentru intrarea de timp a proiectului. Acest spațiu de lucru permite utilizatorilor să intre și să economisească timp pentru un proiect utilizând dispozitivul mobil.
author: Yowelle
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 272101
ms.assetid: 4505f021-b9bb-4b87-be24-6bf0bd88ee60
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 50388bd024fdf2de0d28e49ef07a01b03c6b88f0
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029683"
---
# <a name="project-time-entry-mobile-workspace"></a>Spațiul de lucru mobil pentru intrarea de timp a proiectului

[!include [banner](../includes/banner.md)]

Acest articol oferă informații despre spațiul de lucru mobil pentru **Intrarea de timp a proiectului**. Acest spațiu de lucru permite utilizatorilor să intre și să economisească timp pentru un proiect utilizând dispozitivul mobil.

Acest spațiu de lucru mobil este destinat să fie utilizat cu aplicația mobilă Dynamics 365 Unified Ops. 

## <a name="overview"></a>Prezentare generală
Ca parte a muncii lor zilnice, resursele proiectului sunt adesea la fața locului sau călătoresc. Spațiul de lucru mobil **Intrarea în timp a proiectului** permite utilizatorilor să introducă timpul facturabil sau ne-facturabil în raport cu un proiect pe dispozitivul mobil la alegere. Prin urmare, resursele proiectului pot înregistra intrările de timp oricând și oriunde. De asemenea, pot vizualiza intrările de timp care au fost deja înregistrate. 

Mai exact, în spațiul de lucru mobil **Intrarea în timp a proiectului**, utilizatorii pot îndeplini aceste sarcini:

-   Pentru orice dată selectată, introduceți numărul de ore pe care le-ați petrecut pentru o anumită sarcină.
-   Căutați după numele proiectului sau client pentru a găsi proiectul pentru care introduceți timpul.
-   Specificați categoria și activitatea pentru timpul petrecut.
-   Înregistrați ora ca facturabilă sau ne-facturabilă pentru proiect.
-   Introduceți opțional orice comentarii externe sau interne.

## <a name="prerequisites"></a>Cerințe preliminare
Cerințele preliminare diferă, în funcție de versiunea de Microsoft Dynamics 365 care a fost implementat pentru organizația dvs.

### <a name="prerequisites-if-you-use-dynamics-365-finance"></a>Cerințe preliminare dacă utilizați Dynamics 365 Finance
Dacă Finanța a fost implementată pentru organizația dvs., administratorul de sistem trebuie să publice fișierul spațiu de lucru mobil **Intrarea în timp a proiectului**. Pentru instrucțiuni, consultați [Publicați un spațiu de lucru mobil](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace).

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a>Condiții preliminare dacă utilizați versiunea 1611 cu platforma 3 actualizare sau o versiune ulterioară
Dacă versiunea 1611 cu actualizarea platformei 3 sau o versiune ulterioară a fost implementată pentru organizația dvs., administratorul de sistem trebuie să îndeplinească următoarele condiții prealabile. 

<table>
<thead>
<tr class="header">
<th>Cerințe preliminare</th>
<th>Rol</th>
<th>Descriere</th>
</tr>
</thead>
<tbody>
<tr class="odd">

<td>Implementați KB 4018050.</td>
<td>Administrator de sistem</td>
<td>KB 4018050 este o actualizare X++ sau metadate remediere rapidă care conține spațiu de lucru mobil <strong>Intrarea în timp a proiectului</strong>. Pentru a implementa KB 4018050, administratorul de sistem trebuie să urmeze acești pași.
<ol>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">Descărcați remedierea rapidă a metadatelor de la Microsoft Dynamics Lifecycle Services (LCS)</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Instalați remedierea rapidă a metadatelor</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Creați un pachet implementabil</a> care conține modele <strong>ApplicationSuite</strong> și <strong>ProjectMobile</strong> și apoi încărcați pachetul implementabil la LCS.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Aplicați pachetul implementabil</a>.</li>

</ol></td>
</tr>
<tr class="even">
<td>Publicați spațiul de lucru mobil <strong>Proiect de intrare de timp</strong>.</td>
<td>Administrator de sistem</td>
<td>Consultați <a href="/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Publicați un spațiu de lucru mobil</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>Descărcați și instalați aplicația mobilă

Descărcați și instalați aplicația mobilă pentru finanțe și operațiuni:

-   [Pentru telefoane Android](https://go.microsoft.com/fwlink/?linkid=850662)
-   [Pentru telefoane iPhone](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Conectați-vă la aplicația mobilă
1.  Deschideți aplicația pe dispozitivul mobil.
2.  Introduceți adresa URL Dynamics 365.
3.  Prima dată când vă conectați, vi se solicită numele de utilizator și parola. Introduceți acreditările.
4.  După ce vă conectați, sunt afișate spațiile de lucru disponibile pentru compania dvs. Rețineți că, dacă administratorul de sistem publică mai târziu un spațiu de lucru nou, va trebui să reîmprospătați lista spațiilor de lucru mobile.

[![Trageți pentru a reîmprospăta.](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="enter-time-by-using-the-project-time-entry-mobile-workspace"></a>Introduceți ora utilizând spațiul de lucru mobil pentru introducerea timpului proiectului
1.  Pe dispozitivul dvs. mobil, selectați spațiul de lucru **Intrarea în timp a proiectului**.
2.  Selectați **Intrare de timp**. Sunt afișate datele calendaristice pentru săptămâna curentă.
3.  Pentru o dată selectată, selectați **Acțiuni** &gt; **Intrare nouă**.
4.  Introduceți numărul de ore de înregistrat.
5.  Selectați proiectul pentru intrarea în timp. O listă arată proiectele care sunt încărcate în aplicația dvs. pentru utilizare offline. În mod implicit, sunt încărcate 50 de articole, dar un dezvoltator poate schimba acest număr. Pentru informații suplimentare, consultați [Platformă mobilă](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).
6.  Dacă proiectul dvs. nu se află în listă, selectați **Căutare**. Căutați după nume sau comutați la căutare după numele proiectului sau client.
7.  Selectați o categorie. O listă arată categoriile care sunt încărcate în aplicația dvs. pentru utilizare offline. În mod implicit, sunt încărcate 50 de articole, dar un dezvoltator poate schimba acest număr. Pentru informații suplimentare, consultați [Platformă mobilă](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).
8.  Dacă categoria dvs. nu se află în listă, selectați **Căutare**. Căutați după categorie sau comutați la căutare după numele categoriei.
9.  Selectați o activitate. O listă arată activitățile care sunt încărcate în aplicația dvs. pentru utilizare offline. În mod implicit, sunt încărcate 50 de articole, dar un dezvoltator poate schimba acest număr. Pentru informații suplimentare, consultați [Platformă mobilă](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).
10. Dacă activitatea dvs. nu se află în listă, selectați **Căutare**. Căutați după numărul de activitate sau comutați la căutare după scop.

11. Selectați proprietatea de linie.
12. Opțional: introduceți orice comentarii interne și externe.
13. Selectați **Terminat**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]