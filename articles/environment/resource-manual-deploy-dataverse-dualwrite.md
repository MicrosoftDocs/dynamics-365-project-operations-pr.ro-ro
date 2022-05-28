---
title: Implementarea manuală a aplicației Project Operations Dataverse cu suport pentru scriere duală
description: Acest subiect explică cum să implementați manual aplicația Project Operations Dataverse pentru a suporta scrierea duală.
author: stsporen
ms.date: 06/18/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: b82eef7b5f64705f37f224172c14f6734612329e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8591235"
---
# <a name="manually-deploy-the-project-operations-dataverse-app-with-dual-write-support"></a>Implementarea manuală a aplicației Project Operations Dataverse cu suport pentru scriere duală

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

Acest subiect explică cum să implementați manual Microsoft Dynamics 365 Project Operations în Microsoft Dataverse pentru a suporta scrierea duală. Project Operations detectează configurația mediului și adaugă suport suplimentar pentru scrierea duală dacă sunt îndeplinite condițiile prealabile.

În timpul implementarii prin Microsoft Dynamics Lifecycle Services (LCS), dacă ați urmat instrucțiunile din acest subiect, puteți sări peste implementarea integrării Microsoft Power Platform (cunoscută anterior sub numele de mediu Common Data Service).

Procesul de implementare a Project Operations în Dataverse, astfel încât să accepte scrierea duală, are patru pași principali:

1. [Creați un mediu nou în Dataverse care acceptă scrierea duală](#create).
2. [Adăugați condiții preliminare pentru scriere duală la mediu](#prerequisites).
3. [Adăugați aplicația Project Operations Dataverse](#dataverse).
4. [Legați mediile](#link).

## <a name="create-a-new-environment-in-dataverse-that-supports-dual-write"></a><a name="create"></a>Creați un mediu nou în Dataverse care acceptă scrierea duală

Pentru a finaliza această procedură, trebuie să vă conectați ca administrator.

1. Deschideți [Centrul de administrare Power Platform](https://admin.powerplatform.com) și conectați-vă ca administrator.
2. Creați un mediu nou și numiți-l.
3. Selectați tipul de mediu. Dacă v-ați înscris pentru oferta de versiune de încercare, selectați **Versiune de încercare (bazată pe abonament)**.
4. Confirmați regiunea de implementare.
5. Activați opțiunea **Creați o bază de date pentru acest mediu**. 
6. Confirmați limba, apoi confirmați că moneda se potrivește cu moneda aplicațiilor dvs. Finanțe și Operațiuni.
7. Activați opțiunea **Aplicații Dynamics 365** și confirmați că câmpul **Implementați automat aceste aplicații** este setat la **Niciuna**.
8. Adăugați un grup de securitate, dacă este necesar un grup de securitate.
9. Selectați **Salvare** pentru a crea mediul.
10. Așteptați până când implementarea este finalizată și mediul ajunge la starea **Gata**.

## <a name="add-dual-write-prerequisites-to-the-environment"></a><a name="prerequisites"></a>Adăugați condiții preliminare pentru scriere duală la mediu

Suportul pentru scriere duală include câmpuri suplimentare care sunt adăugate la entități cheie, cum ar fi entitatea **Companie**. Dacă adăugați suport de scriere duală la un mediu existent, este posibil să trebuiască să actualizați datele pentru a activa asistența. Pentru informații despre cum să faceți bootstrap pentru date, consultați [Bootstrap Date companie](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/bootstrap-company-data). Pentru mai multe informații despre scrierea duală, consultați [Cerințe de sistem pentru scrierea duală](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req).

Finalizați această procedură pentru a adăuga condițiile preliminare pentru scrierea duală în mediul dvs.

1. Deschideți mediul pe care tocmai l-ați creat și apoi accesați **Resursă** \> **Aplicații Dynamics 365**.
2. Selectați **Soluție de bază scriere duală** în lista de aplicații și instalați-o.
3. Așteptați până la finalizarea instalării. Apoi selectați **Soluție orchestrare aplicație scriere duală** în lista de aplicații și instalați-o.

## <a name="add-the-project-operations-dataverse-app"></a><a name="dataverse"></a>Adăugați aplicația Project Operations Dataverse

Puteți finaliza această procedură numai dacă ați finalizat procedurile anterioare înainte de a instala Project Operations. În timpul instalării, sistemul analizează configurația mediului și adaugă suport pentru scrierea duală, dacă este necesar.

1. Deschideți mediul pe care tocmai l-ați creat mai devreme și apoi accesați **Resursă** \> **Aplicații Dynamics 365**.
2. Selectați **Microsoft Dynamics 365 Project Operations** în lista de aplicații și instalați-l.

## <a name="link-your-environments"></a><a name="link"></a>Legați mediile

După Dataverse mediu este implementat, puteți configura linkul în aplicațiile dvs. Finanțe și Operațiuni. Urmați pașii din [Utilizați expertul cu scriere duală pentru a vă conecta mediile](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/link-your-environment).
