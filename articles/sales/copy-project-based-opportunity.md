---
title: Copierea oportunităților bazate pe proiect
description: Acest subiect furnizează informații despre copierea de oportunități bazate pe proiect în Project Operations.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 83fe41cb16be6bdd91219fc59e517ae0e5848afec5f771edde575bb5c24f9865
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/06/2021
ms.locfileid: "6999736"
---
# <a name="copy-project-based-opportunities"></a>Copierea oportunităților bazate pe proiect

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_


Oportunitățile de proiect pot fi copiate cu ușurință pentru a crea noi oportunități de proiect. 

1. Accesați lista de pagină **Oportunități de proiect** și selectați o oportunitate din listă. Sau deschideți pagina de detalii a unei anumite oportunități. 
2. Din oricare dintre pagini, selectați **Copie**. Se va deschide o pagină de dialog care conține următoarele informații despre câmp. În funcție de valorile selectate în acest dialog, procesul de copiere se poate modifica.

    | **Câmp** | **Descriere** | **Impactul din aval** |
    | --- | --- | --- |
    | Subiect | Introduceți subiectul relevant sau numele oportunității țintă. Când se deschide dialogul, sistemul îl va seta la subiectul ofertei de oportunitate cu **-copie** anexat la acesta. | Nu există niciun impact din aval pentru acest domeniu. |
    | Cont | Trimiteri la compania clientului sau la înregistrarea contului. Când se deschide caseta de dialog, sistemul îl va seta la contul din oportunitatea sursă. | Acest câmp este clientul principal din oportunitate. |
    | Unitate contractantă | Unitatea organizației responsabilă pentru livrarea proiectelor asociate acestei tranzacții. Când se deschide caseta de dialog, sistemul îl va seta la unitatea contractantă de oportunitate sursă. | Unitatea contractantă este divizia companiei care execută proiectele după încheierea tranzacției. Fiecare unitate contractantă are o monedă, iar această monedă este utilizată pentru a raporta costurile estimate și reale suportate în timpul proiectului. |
    | Monedă | Moneda în care este calculată tranzacția. Când se deschide pagina de dialog, sistemul o va seta la moneda de oportunitate sursă. | Moneda este utilizată pentru a stabili implicit o listă de prețuri și pentru a construi estimări financiare pe ofertă. În cele din urmă, moneda este utilizată pentru a factura clientul atunci când afacerea este câștigată. |
    | Copiați prețul | O valoare Da/Nu care indică dacă prețul oportunității ar trebui copiat din oportunitatea sursă. | Dacă **Da** este selectat, listele de prețuri sunt copiate de la sursă la oportunitatea țintă. Dacă **Nu** este selectat, listele de prețuri sunt setate implicit pe baza celor mai recente liste de prețuri care au fost configurate. |

3. Selectați **OK**. Sistemul creează o copie a oportunității de proiect pe baza parametrilor selectați și noua oportunitate de proiect este deschisă.


[!INCLUDE[footer-include](../includes/footer-banner.md)]