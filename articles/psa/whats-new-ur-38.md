---
title: Ce este nou sau schimbat în Project Service Automation versiunea actualizată 38, V3
description: Acest subiect listează caracteristicile și remedierile disponibile în Actualizarea Microsoft Dynamics 365 Project Service Automation, versiunea 38, V3.
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
ms.openlocfilehash: 16994535d57dc1d7fefbe6e892c154f52638c7c0
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8598733"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-38-v3"></a>Ce este nou sau schimbat în Project Service Automation versiunea actualizată 38, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Suntem încântați să anunțăm cea mai recentă actualizare pentru aplicația Microsoft Dynamics 365 Project Service Automation. Această versiune include câteva îmbunătățiri importante ale calității, performanței și utilizabilității. Este compatibil cu Dynamics 365 9.x. Pentru a actualiza această versiune, accesați pagina de soluții online din Centrul de administrare pentru Dynamics 365 și instalați actualizarea. Pentru informații suplimentare, consultați: [Instalarea, actualizarea sau eliminarea unei soluții preferate](/power-platform/admin/install-remove-preferred-solution).

Acest subiect listează caracteristicile și corecțiile care sunt noi sau modificate pentru Project Service Automation, versiunea actualizată 38, V3. Această versiune are un număr de versiune V3.10.59.117 și este în general disponibilă printr-o actualizare automată în decembrie 2021.

## <a name="update-release-38"></a>Lansarea de actualizări 38

### <a name="bug-fixes"></a>Remedieri de erori

S-au remediat următoarele probleme.

**Timp și cheltuială**

- O excepție apare atunci când lungimea jurnalelor setului de aprobare depășește 100.000 de înregistrări.
- Utilizatorii nu pot accesa **Intrarea timpului** grila din The **Intrarea timpului** Pagina principală.
- The **Import de intrare de timp** caseta de dialog nu afișează niciun text atunci când niciun element nu este eligibil pentru import.
- Utilizatorii pot crea seturi de aprobare în care **Stare țintă** câmpul este setat la **Necunoscut**.

**Gestionare de proiect**

- Contururile nu sunt afișate corect în alocări de resurse pentru UTC(+09:30) și UTC(+10:00) când începe ora de vară.
- The **Coloană suplimentară** câmpul pentru structurile de defalcare a muncii este ascuns în unele locații.
- Selectorul de date pentru controlul calendarului din **Sarcina proiectului** grila nu este localizată corect pentru chineză.

**Vânzări**

- **Executarea contractului** și **Costul real al proiectului** valorile nu se potrivesc atunci când resursele rezervabile care au unități contractante și valute diferite trimit înregistrări de timp.
- Un flux de lucru personalizat pentru confirmarea automată a facturilor eșuează atunci când facturile sunt importate ca soluție gestionată. Este afișat următorul mesaj: „Microsoft.Xrm.Sdk.InvalidPluginExecutionException Mesaj: starea facturii nevalidă”.
- Când **Rădăcină** este selectat ca opțiune de rezumare, iar proiectul are estimări dintr-un amestec de clase de tranzacții (de exemplu, o combinație de timp, cheltuieli și estimări materiale), sistemul rezumă pe toate clasele de tranzacții ca o singură linie de taxă.
- În scenariile în care o linie de cheltuieli este adăugată înainte ca o linie de contract să fie asociată unui proiect, prețul corect nu este introdus ca valoare implicită în **Actualizați prețul** camp.
- Sumele de vânzări negative nu sunt permise **Proiect** și **Sarcină** entitati.
