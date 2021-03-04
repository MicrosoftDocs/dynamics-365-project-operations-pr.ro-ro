---
title: Model de securitate
description: Acest subiect oferă informații despre modelul de securitate din Dynamics 365 Project Operations.
author: stsporen
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: b01f3d88dd021895933bc863b762f019ae50eed6
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642918"
---
# <a name="security-model"></a>Model de securitate

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Microsoft Dynamics 365 Project Operations conține un model unic de securitate care permite un model de securitate de afaceri bazat pe roluri, care colaborează cu Grupuri Microsoft Office. 


## <a name="security-roles"></a>Roluri de securitate
Capabilitățile front-end ale Project Operations includ următoarele roluri:

| Rol                          | Descriere                                                                                                                                                                 | Domeniu de acoperire |
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------|
| Manager de practică              | Sprijină raportarea între proiecte.                                                                                                            | Unitate de business              |
| Aprobator de proiect              | Aprobă timpul și cheltuielile la un proiect.                                                                                                                              | Unitate de business |
| Administrator de facturare de proiect | Creează propunerea de facturare.                                                                                                                                                 | Unitate de business |
| Manager de proiect               | Creează planul de proiect și solicită resurse.                                                                                                                              | Unitate de business |
| Resursă de proiect              | Membrii echipei care pot fi rezervați și raportează timpul.                                                                                                          | Unitate de business|
| Manager resurse              | Toate funcțiile de gestionare a resurselor, cum ar fi îndeplinirea cererilor și rezervărilor de resurse, separate pentru a susține o configurație hibridă de manager de proiect + Manager resurse și un rol unic și centralizat de Manager resurse. | Unitate de business |


Microsoft Project pentru web include următoarele roluri:

| Rol           | Descriere                                                                                                        | Domeniu de acoperire  |
|----------------|--------------------------------------------------------------------------------------------------------------------|--------|
| Utilizator de proiect   | Utilizator colaborativ al Project   care este capabil să își creeze propriile proiecte și să vizualizeze orice proiecte partajate cu   acesta. | Utilizator   |
| Sistemul proiectului | Rolul utilizat pentru contextul   aplicației. Clienții nu ar trebui să utilizeze acest rol de sistem.                                    | Global |

## <a name="security-enforcement"></a>Aplicarea securității
Acțiunile care sunt efectuate la nivelul proiectului sunt efectuate în contextul utilizatorului conectat. Aceasta înseamnă că, pentru a crea, deschide sau șterge un proiect, utilizatorul trebuie să aibă acces disponibil în CDS. Accesul în CDS poate fi acordat prin oricare dintre mecanismele posibile incluse în platformă. De exemplu, un utilizator cu un domeniu mai mare de acces poate accesa proiectul sau dacă a fost efectuată o acțiune explicită de partajare a proiectului care îi acordă utilizatorului acces.

Este important să luați în considerare acest lucru atunci când creați proiecte în Project Operations.

## <a name="modern-group-collaboration-with-project-operations"></a>Colaborare modernă de grup cu Project Operations
Proiect pentru web și Project Operations susțin grupuri moderne pentru colaborare. Utilizatorii adăugați la proiect printr-un grup pot edita planul de proiect.

Project for the Web adaugă utilizatorii în grup automat la alocare.

Grupurile permit ca permisiunile proiectului și sprijinirea artefactelor de colaborare să fie lucrate în colaborare. Următoarea diagramă ilustrează evenimentele și modificările de stare care au loc în timpul procesului de atribuire a grupului.

Project Operations nu creează un grup prin acțiune implicită și face acest lucru doar prin acțiunea explicită a apăsării grupurilor.

Căutarea membrilor grupului în dialogul **Managementul grupului**, este limitat la cei care sunt setați ca parte a grupului de securitate al mediului. Pentru mai multe informații, consultați [Controlul accesului utilizatorilor la medii: grupuri de securitate și licențe](https://docs.microsoft.com/power-platform/admin/control-user-access).

![Mod grup](./media/groupsmode.png)

1. Proiectul este creat și deținut de utilizatorul care a creat.
2. Proprietarul proiectului este actualizat echipei.
3. Echipa Proprietar este mapată la grupul Office specificat sau creat.
4. Proprietarul inițial al proiectului este adăugat la Office Group.

## <a name="deployment-recommendation"></a>Implementarea recomandării
Pe măsură ce modelul de colaborare în grup Office evoluează, funcționalitatea va fi adăugată pentru a oferi un control mai detaliat în timp. Clienții care desfășoară Project Operations astăzi sunt încurajați să se concentreze pe un model de securitate tradițional Microsoft Dynamics 365.

Pentru mai multe informații consultați [Securitate în Common Data Service](https://docs.microsoft.com/power-platform/admin/wp-security).

## <a name="project-operations-and-microsoft-dynamics-365-finance-security"></a>Project Operations și securitate Microsoft Dynamics 365 Finance
Project Operations include următoarele roluri:

- Manager de proiect
- Contabil de proiect

Pentru mai multe informații despre rolurile de securitate în finanțe, consultați [Securitate pe bază de rol](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/role-based-security).




[!INCLUDE[footer-include](../includes/footer-banner.md)]