---
title: Gestionarea listelor de prețuri ale proiectelor din contractele de proiecte
description: Acest subiect oferă informații despre gestionarea listelor de prețuri de proiecte pe contractele de proiecte.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 2ad0e260fde65cf3eb32539fbcdb7101796cb53b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8600527"
---
# <a name="manage-project-price-lists-on-project-contracts"></a>Gestionarea listelor de prețuri ale proiectelor din contractele de proiecte

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Contractele de proiect din Dynamics 365 Project Operations sunt concepute pentru a accepta listele de prețuri de vânzare efective cu mai multe date dintr-un contract. În Project Operations există o nouă entitate asociată numită **Listele de prețuri ale proiectului**. Această entitate are o relație unu-la-mulți cu un contract de proiect.

Listele de prețuri ale proiectului sunt folosite pentru a stabili prețurile pentru tranzacții de timp, materiale și cheltuieli pentru un proiect. Atunci când un contract are una sau mai multe liste de prețuri ale proiectelor, aceste liste de prețuri sunt utilizate pentru a stabili prețul pentru timp, materiale, estimări ale cheltuielilor și valori reale pentru proiectele care sunt asociate cu contractul prin linia de contract.

Când nu există liste de prețuri ale proiectului pe un contract de proiect, veți vedea un mesaj de avertizare că nu există liste de prețuri ale proiectului, iar estimările dvs., lucrările efective ale proiectului, materialele și cheltuielile înregistrate nu vor fi evaluate. Nu va exista preț pentru valorile vânzărilor.

## <a name="associate-or-unassociate-a-project-price-list-on-a-project-contract"></a>Asociați sau anulați o listă de prețuri a proiectului într-un contract de proiect

### <a name="create-or-associate-a-specific-price-list-for-estimating-project-based-work-material-and-expenses"></a>Creați sau asociați o listă de prețuri specifică pentru estimarea lucrărilor, materialelor și cheltuielilor bazate pe proiecte

1. În contractul de proiect, selectați fila **Listele de prețuri ale proiectului**.
2. În subgrilă, selectați **+ Adăugați o listă de prețuri de proiect nou**.
3. Pe glisorul **Creare rapidă**, selectați o listă de prețuri. 

  Lista verticală afișează toate listele de prețuri care au contextul setat la **Vânzări**, unde moneda din lista de prețuri se potrivește cu moneda din contract.
  
4. Introduceți o descriere pentru asocierea listei de prețuri a proiectului, selectați **Salvați** și apoi închideți glisorul **Creare rapidă**.

   Este creată o asociere de listă de prețuri de proiect.
   
5. Repetați pașii 1-4 pentru a asocia mai multe liste de prețuri de proiect la contractul de proiect. Creați mai multe liste de prețuri ale proiectului numai dacă aveți o eficiență diferită a datei pentru fiecare dintre listele de prețuri asociate proiectului.

> [!NOTE]
> Project Operations nu acceptă suprapunerea efectivității datei a listelor de prețuri ale proiectului. Dacă există mai multe liste de prețuri pentru proiecte pentru o tranzacție cu o dată dată, prețul pentru acea tranzacție va fi implicit la zero.

### <a name="remove-a-project-price-list-association"></a>Eliminați asocierea unei liste de prețuri de proiect

- Selectați lista de prețuri a proiectului, apoi selectați **Ștergeți lista de prețuri a proiectului contractului** pe subgrilă. 

  Lista de prețuri este eliminată din listele de prețuri ale proiectului din contract. Lista de prețuri în sine nu va fi ștearsă. Doar asocierea la contract va fi ștearsă.

## <a name="set-up-automatic-defaulting-of-project-price-lists-on-a-contract"></a>Configurați implicit automat listele de prețuri ale proiectului într-un contract

O listă de prețuri a proiectului poate fi configurată ca listă de prețuri implicită a proiectului. Această configurare asigură faptul că toate contractele din organizația dvs. încep întotdeauna cu o listă de prețuri standard a proiectului pentru perioada respectivă de preț.

### <a name="set-up-the-organizational-default-for-project-price-lists"></a>Configurați implicit organizațional pentru listele de prețuri ale proiectului

1. Accesați **Setări** > **General**, apoi selectați **Parametrii**.
2. În pagina listei **Parametri activi**, selectați și faceți dublu clic pe înregistrare pentru a o deschide. În timp ce faceți dublu clic, asigurați-vă că nu faceți clic pe o valoare de câmp care este hyperlink. 
3. Pe pagina **Parametri activi**, selectați fila **Listă de prețuri**. O subgrilă afișează o listă de liste de prețuri implicite. Aceasta este o listă de costuri standard și liste de prețuri de vânzare. Având o listă de prețuri de **Vânzări** asociată aici pentru fiecare monedă în care vindeți vă asigură că lista de prețuri de vânzare este implicită pentru orice contract pe care îl creați pentru clienții care tranzacționează în această monedă.

### <a name="set-up-a-customer-specific-project-price-list"></a>Configurați o listă de prețuri specifice proiectului

Puteți configura, de asemenea, liste de prețuri specifice proiectului pentru clienți atunci când ați negociat un contract principal de stabilire a prețurilor cu clienții dvs.

1. Accesați **Vânzări** > **Clienți**.
2. Din lista de conturi active, selectați clientul pentru care au listă de prețuri speciale.
3. Selectați înregistrarea clientului pentru ao deschide, apoi selectați fila **Listele de prețuri ale proiectului**. O subgrilă afișează o listă cu listele de prețuri ale proiectului specifice acestui client. 
4. Creați aici o nouă asociație de listă de prețuri pentru a avea lista de prețuri a proiectului specifică acestui client.

## <a name="custom-pricing-on-a-project-contract"></a>Prețuri personalizate pentru un contract de proiect

După ce aveți liste de prețuri de proiect implicite organizaționale și specifice clientului, contractele dvs. de proiect vor fi create automat cu aceste asociații de liste de prețuri de proiect. Cu toate acestea, listele de prețuri ale proiectului dintr-un contract de proiect sunt întotdeauna copiate cu data și numele contractului anexate acestora. Managerii de cont și de proiect pot începe apoi să facă modificări la prețurile acestor copii. Aceste prețuri modificate vor fi aplicabile numai acestui contract de proiect.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
