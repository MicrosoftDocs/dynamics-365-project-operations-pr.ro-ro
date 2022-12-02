---
title: Configurarea resurselor proiectului
description: Acest articol furnizează informații despre configurarea sau solicitarea resurselor de proiect.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5a4e6fe829d6b39aed9eb6aaea42f245fc997593
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8933783"
---
# <a name="set-up-project-resources"></a>Configurarea resurselor proiectului

[!include [banner](../includes/banner.md)]

Trebuie să configurați un calendar și să îl asociați cu un angajat sau cu un lucrător. Calendarul este folosit pentru a planifica proiectul și timpul de lucru al resurselor rezervate pentru proiect. În timpul configurării calendarului, managerii de proiect pot realiza nivelarea resurselor ca parte a optimizării resurselor. Pe baza planificării calendaristice, pot fi impuse restricții asupra resurselor. Puteți configura un calendar din pagina **Calendare**.

Când configurați un angajat ca resursă a proiectului, puteți selecta dintre angajații care lucrează în compania pentru care configurați resursele. Alternativ, puteți selecta angajați din alte companii din organizația dvs. Acești angajați sunt cunoscuți ca resurse între companii.

Următoarele proceduri explică cum să configurați un angajat ca o resursă de proiect în compania dvs. și cum să configurați o resursă de proiect între companii.

## <a name="set-up-a-worker-as-a-project-resource"></a>Configurați un angajat ca resursă a proiectului

1. Din pagina **Angajați**, în lista **Angajați**, selectați angajatul pe care îl adăugați ca resursă a proiectului și deschideți înregistrarea angajatului.
2. În panoul de acțiuni, selectați **Proiect** &gt; **Configurare** &gt; **Configurarea proiectului**.
3. Selectați un calendar, apoi închideți pagina.

De asemenea, puteți specifica proiecte implicite pentru o resursă ca un tip de pre-atribuire. Pre-atribuirile pot fi utilizate atunci când managerul de resurse sau managerul de proiect știe în avans la ce proiecte va lucra resursa. Pre-atribuirile se pot baza și pe cererea unui sponsor de proiect sau a unui client. Pentru a pre-atribui un proiect, din pagina **Atribuire proiecte**, în fila **Proiecte**, în lista **Proiecte rămase**, selectați proiectul corespunzător.

## <a name="set-up-an-intercompany-resource"></a>Configurați o resursă între companii

Când configurați un angajat ca resursă între companii, trebuie să finalizați configurarea atât în compania sursă, cât și în cea țintă.

### <a name="in-the-lending-company"></a>În compania sursă

1. În Finanțe, verificați dacă este selectată compania sursă, apoi finalizați procedura din secțiunea anterioară „Configurați un angajat ca resursă a proiectului”.
2. În pagina **Contabilitate între companii**, selectați **Nou**.
3. În câmpul **ID-ul entității juridice**, selectați compania sursă. Completați corespunzător câmpurile rămase, și apoi selectați **Salvare**.
4. În pagina **Preț de transfer**, selectați **Nou**.
5. În câmpul **Entitate juridică țintă**, selectați compania adecvată.
6. Pentru a împrumuta companiei țintă numai resursa pe care ați creat-o la începutul acestei secțiuni, în câmpul **Resursă**, selectați numele resursei pe care ați creat-o. Pentru a pune la dispoziția companiei țintă toate resursele din compania sursă, lăsați câmpul **Resursă** necompletat.
7. Din pagina **Managementul proiectului și parametri contabili**, în fila **Între companii**, setați opțiunea **Activați planificarea resurselor și foilor de pontaj între companii** la **Da**.

### <a name="in-the-borrowing-company"></a>În compania țintă

- Din pagina **Lista resurselor**, în filtrul de căutare, introduceți numele resursei pe care ați creat-o pentru compania sursă, pentru a verifica dacă numele este inclus în lista de resurse pentru compania țintă.

## <a name="request-project-resources"></a>Solicitați resurse de proiect
Funcționalitatea pentru planificarea resurselor proiectului permite doar managerilor de resurse să distribuie resursele de personal pe implicări sau proiecte. Pentru a activa această funcționalitate, finalizați următoarele activități sau verificați dacă acestea au fost finalizate:

- Configurare secvențe numerice.
- Configurare fluxuri de lucru de management de proiect și contabilitate.
- Activare fluxuri de lucru de solicitare a resurselor.

După finalizarea sarcinilor precedente, puteți finaliza următoarele sarcini după necesități:

- Crearea unei solicitări de resursă dintr-o resursă de personal cu rezervare provizorie.
- Monitorizarea solicitărilor de resurse.
- Completarea solicitărilor de resurse.
- Solicitarea unei resurse de personal de la o WBS.
- Rezervarea de resurse la un proiect fără a avea o solicitare pentru o resursă de personal.


[!INCLUDE[footer-include](../includes/footer-banner.md)]