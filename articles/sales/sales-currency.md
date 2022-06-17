---
title: Moneda
description: Acest articol oferă informații despre cum să adăugați și să eliminați tipuri de monede în Operațiuni de proiect.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 0fbfd1039fe0a7401376bb8c27b118297fdc87f5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921547"
---
# <a name="currency"></a>Monedă

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_



Monedele stabilesc prețurile pentru produse în catalogul de produse și costul tranzacțiilor, de exemplu comenzi de vânzare. Dacă clienții dvs. se află în regiuni geografice diferite, adăugați monedele lor în pentru a vă gestiona tranzacțiile. Adăugați monedele cele mai potrivite pentru cerințele dvs. de business actuale și viitoare.  

> [!NOTE]
> Dacă mediul dvs. este unul Common Data Service, sunteți în centrul de administrare Power Platform și selectați pagina **Monede** (**Medii** > [selectați mediul] > **Setări** > **Afacere** > **Monede**), pagina va fi goală. Aceasta deoarece setarea unei monede nu este acceptată în mediile Common Data Service.

## <a name="add-a-currency"></a>Adăugarea unei monede  
Înainte de a începe această procedură, verificați dacă rol de securitate include permisiuni de administrator de sistem. 

1. Selectați un mediu în Centrul de administrare Power Platform. 
2. Selectați **Setări** > **Firmă**.
3. Selectați **Monede**.  
4. Selectați **Nou**.  
5. Completați informațiile solicitate.  


   |          Câmp          |                                                                                                                                                                                                                                                                                                                                                                            Descriere                                                                                                                                                                                                                                                                                                                                                                            |
   |-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |    **Tip monedă**    | - **Sistem** - Selectați această opțiune dacă doriți să utilizați monedele disponibile în aplicațiile pe bază de model în Dynamics 365. Selectați **Căutare** pentru a căuta o monedă. Atunci când selectați un cod monetar, opțiunile **Nume monedă** și **Simbol monedă** sunt adăugate automat pentru moneda selectată.<br />- **Particularizat** - Selectați această opțiune dacă doriți să adăugați o monedă care nu este disponibilă în aplicațiile pe bază de model în Dynamics 365. În acest caz, trebuie să introduceți manual valorile pentru **Cod monetar**, **Precizie monedă**, **Nume monedă**, **Simbol monedă** și **Conversie monedă**. |
   |    **Cod monedă**    |                                                                                                                                                                                                                                                                                                                                            Prescurtarea pentru monedă. De exemplu, **USD** pentru dolarul american.                                                                                                                                                                                                                                                                                                                                            |
   | **Precizie monedă**  |                                                                                                                                                                                  Tastați numărul de zecimale pe care doriți să îl utilizați pentru monedă.  Aveți posibilitatea să adăugați o valoare între 0 și 4. **Notă:**  Dacă ați setat o valoare de precizie în caseta de dialog **Setări sistem**, valoarea respectivă va apărea aici.                                                                                                                                                                                  |
   |    **Nume monedă**    |                                                                                                                                                                                                                                         Dacă ați selectat un cod monetar din lista monedelor disponibile în aplicații pe bază de model în Dynamics 365, numele monedei pentru codul selectat este afișat aici. Dacă ați selectat **Particularizat** ca tip de monedă, tastați numele monedei.                                                                                                                                                                                                                                          |
   |   **Simbol monetar**   |                                                                                                                                                                                                                                                                      Dacă ați selectat un cod monetar din lista monedelor disponibile, simbolul monedei selectate este afișat aici. Dacă ați selectat **Particularizat** ca tip de monedă, introduceți simbolul noii monede.                                                                                                                                                                                                                                                                       |
   | **Conversie monedă** |                                                                                                                                                                                                                                     Tastați valoarea monedei selectate raportată la un dolar american. Aceasta este suma la care moneda selectată este convertită în moneda de bază. **Important:**  Asigurați-vă că actualizați această valoare cât de des este necesar pentru a evita orice calcule inexacte în tranzacții.                                                                                                                                                                                                                                      |


6. După ce ați terminat pe bara de comandă, selectați **Salvare** sau **Salvare și închidere**.  

   > [!TIP]
   >  Pentru a edita o monedă, selectați monedă și tastați sau selectați noile valori.  

## <a name="delete-a-currency"></a>Ștergerea unei monede  

1. Selectați un mediu în Centrul de administrare Power Platform. 
2. Selectați **Setări** > **Firmă**.
3. Selectați **Monede**.  
4. În lista de monede afișată, selectați moneda pe care doriți să o ștergeți.  
5. Selectați **Ștergere**.  
6. Confirmați ștergerea.  

> [!IMPORTANT]
>  Nu puteți șterge monedele utilizate de alte înregistrări, puteți doar să le dezactivați. Dezactivarea înregistrărilor de monedă nu elimină informațiile de monedă stocate în înregistrările existente, cum ar fi oportunități sau comenzi. Cu toate acestea, nu veți putea selecta moneda dezactivată pentru tranzacții noi.  


[!INCLUDE[footer-include](../includes/footer-banner.md)]