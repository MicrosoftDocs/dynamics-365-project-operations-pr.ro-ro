---
title: Copierea contractelor de proiect - simplificat
description: Acest subiect furnizează informații despre copierea contractelor de proiect în Project Operations.
author: rumant
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a0ffb807c8254f4d392c4750fa0b4a60f7fd26b0
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273753"
---
# <a name="copy-project-contracts---lite"></a>Copierea contractelor de proiect - simplificat

_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_

Puteți crea cu ușurință noi contracte de proiect făcând copii ale contractelor existente într-unul din cele două moduri: 

  - Pe pagina de listă **Contracte de proiect**, selectați un contract de proiect și apoi selectați **Copie**.
  - Pe pagina de detalii **Contract de proiect**, selectați **Copie**.

Se va deschide o pagină de dialog în care puteți selecta parametrii contractului copiat. Următoarele câmpuri sunt incluse în dialog. În funcție de valorile pe care le selectați în acest dialog, procesul de copiere se poate modifica.

| **Câmp** | **Descriere** | **Impactul din aval** |
| --- | --- | --- |
| Subiect | Introduceți subiectul contractului țintă. Când se deschide pagina de dialog, sistemul va seta acest câmp la numele contractului sursă cu **-copie** anexat la acesta. | Nu există niciun impact din aval pentru acest domeniu. |
| Client | Trimitere la compania clientului sau la înregistrarea contului. Când se deschide caseta de dialog, sistemul va seta acest câmp la contul din contractul sursă. | Acest câmp este clientul principal din contract. |
| Unitate contractantă | Unitatea organizației care este responsabilă pentru livrarea proiectului/proiectelor asociate acestei tranzacții. Când se deschide pagina de dialog, sistemul o va seta la unitatea contractantă a contractului sursă. | Unitatea contractantă este divizia companiei care va exeecuta proiectele după încheierea tranzacției. Fiecare unitate contractantă are o monedă. Moneda este utilizată pentru a raporta costurile estimate și reale suportate în timpul proiectului. |
| Monedă | Moneda în care este calculată tranzacția. Când se deschide pagina de dialog, sistemul va seta câmpul la moneda contractului sursă. Moneda poate fi schimbată. Dacă este, câmpul **Copiere preț** este întotdeauna setat la **Nu** deoarece listele de prețuri din contractul sursă nu mai sunt relevante. | Moneda este utilizată pentru listele de prețuri implicite, pentru stabilirea estimărilor financiare pe contract și pentru facturarea clientului atunci când se câștigă tranzacția. |
| Dată de livrare solicitată | Data de livrare solicitată de client. | Această dată este utilizată ca dată de încheiere când creați date de facturare pe o anumită frecvență. |
| Copiați prețul | Indică dacă prețul contractului trebuie copiat din contractul sursă. | Dacă câmpul este setat la **Da**, referințele pentru lista de prețuri a proiectului și lista de prețuri pentru produse sunt copiate din contractul sursă în contractul țintă. Dacă **Nu** este selectat, listele de prețuri au valoarea implicită pe baza celor mai recente liste de prețuri de pe parametrii contului sau proiectului. |

Când selectați **OK** pe pagina de dialog, sistemul creează o copie a contractului pe baza parametrilor selectați. Se va deschide noul contract.

Următoarele informații nu sunt copiate de la **Sursa** la **Contractul țintă**:

  - Planificări factură
  - Contract și clienți de linie de contract
  - Referința proiectului pe liniile de contract pe bază de proiect
  - Informații despre bugetul clienților

Deoarece aceste informații sunt specifice fiecărui contract, aceste câmpuri și înregistrări nu sunt copiate. Se copiază liniile de contract pentru proiecte și produse, estimările privind detaliile liniei de contract și valorile care nu trebuie depășite la nivelul contractului. Prețul și costul implicit depind de selecția din câmpul **Preț copiere** de pe pagina de dialog **Copiați parametrii**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]