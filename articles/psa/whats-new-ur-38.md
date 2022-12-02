---
title: Ce este nou sau schimbat în Project Service Automation versiunea actualizată 38, V3
description: Acest articol listează caracteristicile și remedierile disponibile în Microsoft Dynamics 365 Project Service Automation, versiunea de actualizare 38, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 12/06/2021
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: ccc08cd0bc365bd4761424a4c0ceac91985e7c89
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915200"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-38-v3"></a>Ce este nou sau schimbat în Project Service Automation versiunea actualizată 38, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Suntem încântați să anunțăm cea mai recentă actualizare pentru aplicația Microsoft Dynamics 365 Project Service Automation. Această versiune include câteva îmbunătățiri importante ale calității, performanței și utilizabilității. Este compatibil cu Dynamics 365 9.x. Pentru a actualiza această versiune, accesați pagina de soluții online din Centrul de administrare pentru Dynamics 365 și instalați actualizarea. Pentru informații suplimentare, consultați: [Instalarea, actualizarea sau eliminarea unei soluții preferate](/power-platform/admin/install-remove-preferred-solution).

Acest articol listează caracteristicile și corecțiile care sunt noi sau modificate pentru Project Service Automation, versiunea de actualizare 38, V3. Această versiune are un număr de versiune V3.10.59.117 și este în general disponibilă printr-o actualizare automată în decembrie 2021.

## <a name="update-release-38"></a>Lansarea de actualizări 38

### <a name="bug-fixes"></a>Remedieri de erori

S-au remediat următoarele probleme.

**Timp și cheltuială**

- O excepție apare atunci când lungimea jurnalelor setului de aprobare depășește 100.000 de înregistrări.
- Utilizatorii nu pot accesa grila **Intrare de timp** de pe pagina principală **Intrare de timp**.
- Caseta de dialog **Import intrare de timp** nu afișează niciun text atunci când niciun element nu este eligibil pentru import.
- Utilizatorii pot crea seturi de aprobare în care câmpul **Stare țintă** este setat la **Necunoscut**.

**Gestionare de proiect**

- Contururile nu sunt afișate corect în alocări de resurse pentru UTC(+09:30) și UTC(+10:00) când începe ora de vară.
- Câmpul **Coloană suplimentară** pentru structurile de defalcare a muncii este ascuns în unele locații.
- Selectorul de date pentru controlul calendarului în grila **Sarcină proiect** nu este localizată corect pentru limba chineză.

**Vânzări**

- Valorile **Executare contract** și **Cost real al proiectului** nu se potrivesc atunci când resursele rezervabile care au unități contractante și valute diferite trimit intrări de timp.
- Un flux de lucru personalizat pentru confirmarea automată a facturilor eșuează atunci când facturile sunt importate ca soluție gestionată. Este afișat următorul mesaj: „Microsoft.Xrm.Sdk.InvalidPluginExecutionException Message: Invalid invoice status.”
- Când **Rădăcină** este selectat ca opțiune de rezumare, iar proiectul are estimări dintr-o combinație de clase de tranzacții (de exemplu, o combinație de timp, cheltuieli și estimări materiale), sistemul rezumă pentru toate clasele de tranzacții ca o singură linie de taxă.
- În scenariile în care o linie de cheltuieli este adăugată înainte ca o linie de contract să fie asociată unui proiect, prețul corect nu este introdus ca valoare implicită în câmpul **Actualizare preț**.
- Sumele de vânzări negative nu sunt permise în entitățile **Proiect** și **Sarcină**.
