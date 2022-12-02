---
title: Copierea contractelor bazate pe proiect
description: Acest articol furnizează informații despre copierea contractelor de proiect în Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 21994ef6d8f6e6cdf321599d107cc80368c96ecc
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410376"
---
# <a name="copy-project-based-contracts"></a>Copierea contractelor bazate pe proiect

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

Puteți crea cu ușurință noi contracte de proiect prin copierea contractelor existente într-unul din cele două moduri:

- Pe pagina de listă **Contracte de proiect**, selectați un contract de proiect și apoi selectați **Copiere**.
- Pe pagina de detalii **Contract de proiect**, selectați **Copie**.

În ambele cazuri, apare o casetă de dialog, în care puteți seta parametrii contractului copiat. Caseta de dialog include următoarele câmpuri. În funcție de valorile pe care le selectați, procesul de copiere se poate modifica.

| Câmp | Descriere | Impactul din aval |
| --- | --- | --- |
| Subiect | Introduceți subiectul contractului țintă. Când se deschide caseta de dialog, sistemul setează câmpul la numele contractului sursă, dar cuvântul „copiere” este atașat acestuia. | Nu există niciun impact în aval pentru acest câmp. |
| client | O trimitere la compania clientului sau la înregistrarea contului. Când se deschide caseta de dialog, sistemul setează câmpul la contul din contractul sursă. | Acest câmp este clientul principal din contract. |
| Firmă proprietară | Compania care este responsabilă pentru livrarea proiectelor care sunt asociate cu această afacere. Când se deschide caseta de dialog, sistemul setează câmpul companiei care deține contractul sursă. | Compania proprietară este entitatea juridică care va executa proiectul după încheierea tranzacției. Moneda companiei proprietare trebuie să se potrivească cu moneda unității contractante. |
| Unitate contractantă | Unitatea organizatorică care este responsabilă de livrarea proiectelor care sunt asociate cu această afacere. Când se deschide caseta de dialog, sistemul setează câmpul la unitatea contractantă a contractului sursă. | Unitatea contractantă este divizia companiei care va exeecuta proiectele după încheierea tranzacției. Fiecare unitate contractantă are o monedă. Această monedă este utilizată pentru a raporta costurile estimate și reale care sunt suportate în timpul proiectului. |
| Moneda | Moneda în care este calculată tranzacția. Când se deschide caseta de dialog, sistemul setează câmpul la moneda contractului sursă. Moneda poate fi schimbată. Dacă este cazul, câmpul **Copiere preț** este întotdeauna setat la **Nu** întrucât listele de prețuri din contractul sursă nu mai sunt relevante. | Această monedă este utilizată pentru listele implicite de prețuri, pentru a genera estimări financiare privind contractul și pentru a factura clientului atunci când tranzacția este câștigată. |
| Dată de livrare solicitată | Data de livrare care este solicitată de client. | Această dată este utilizată ca dată de încheiere când creați date de facturare la o anumită frecvență. |
| Copiați prețul | O valoare care indică dacă prețul contractului trebuie copiat din contractul sursă. | Dacă câmpul este setat la **Da**, referințele la proiect și la lista de prețuri ale produselor sunt copiate din contractul sursă în contractul țintă. Dacă este setat la **Nu**, sunt utilizate listele de prețuri implicite pe baza celor mai recente liste de prețuri din parametrii contului sau proiectului. |

Când selectați **OK** în caseta de dialog, sistemul creează o copie a contractului pe baza parametrilor valorilor pe care le setați. Apoi, este deschis noul contract.

Următoarele informații **nu** sunt copiate din contractul sursă în contractul țintă, deoarece sunt specifice fiecărui contract:

- Planificări factură
- Contract și clienți de linie de contract
- Referința proiectului pe liniile de contract pe bază de proiect
- Informații despre bugetul clienților

Se copiază liniile de contract pentru proiecte și produse, estimările în detaliile liniei de contract și valorile care nu trebuie depășite la nivelul contractului. Introducerea prețurilor implicite și a ratelor de cost depinde de selecția din câmpul **Copiere preț** de pe pagina de dialog **Copiere parametri**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
