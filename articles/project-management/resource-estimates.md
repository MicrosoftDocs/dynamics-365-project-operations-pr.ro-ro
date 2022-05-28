---
title: Estimări financiare pentru timpul alocat resurselor în proiecte
description: Acest subiect oferă informații despre modul în care sunt calculate estimările financiare pentru timp.
author: rumant
ms.date: 03/19/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: aab5c11a7dc23331c935403a4f96ec7197ec1572
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8592569"
---
# <a name="financial-estimates-for-resource-time-on-projects"></a>Estimări financiare pentru timpul alocat resurselor în proiecte

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Estimările financiare pentru timp sunt calculate pe baza a trei factori: 

- Tipul de membru generic sau numit al echipei atribuit fiecărei sarcini de nod frunză din planul de proiect. 
- Tipul de complexitate a lucrului.
- Răspândirea efortului pentru atribuirea resursei pe activitate. 

Primii doi factori influențează costul unitar sau rata de facturare a alocării unei resurse. Costul unitar sau rata facturării unei alocări de resurse este determinată de atributele resursei alocate. Aceste atribute includ unitatea organizațională căreia îi aparține resursa și rolul standard al resursei. De asemenea, puteți adăuga atribute personalizate relevante pentru afacerea dvs. pentru resursă, cum ar fi titlul standard sau nivelul de experiență, și să le influențeze costul unitar sau rata de facturare a atribuirii.
În plus față de atributele resursei, atributele de lucru, cum ar fi sarcina, pot influența, de asemenea, rata facturării unitare sau rata costului atribuirii. De exemplu, atunci când anumite sarcini sunt mai complexe, atribuirea resursei la acele sarcini specifice are ca rezultat un cost unitar sau o rată de facturare mai mare decât sarcinile care sunt mai puțin complexe.   

Al treilea factor furnizează cantitatea de ore la acel ritm. În cazurile în care o sarcină acoperă două perioade de preț, este probabil ca prima parte a alocării resurselor pentru acea sarcină să fie stabilită la un preț diferit față de cea de-a doua parte a activității. Estimarea efortului pentru fiecare alocare a resurselor este o valoare complexă stocată cu distribuția zilnică a efortului pe zi.

Pentru instrucțiuni detaliate despre cum să configurați atribute personalizate de lucru și resurse ca dimensiuni de stabilire a prețurilor și costuri, consultați [Prezentare generală a dimensiunilor prețurilor](../pricing-costing/pricing-dimensions-overview.md).

Estimarea financiară pentru fiecare alocare a resurselor este calculată ca **rata/oră pentru sarcină înmulțită cu numărul de ore.**  Similar cu estimarea efortului, estimarea financiară pentru cost și venituri pentru fiecare alocare a resurselor este o valoare complexă stocată cu distribuția zilnică a sumei monetare pe zi. 

## <a name="summarizing-financial-estimates-for-time"></a>Rezumând estimările financiare pentru timp
O estimare financiară a timpului pe o sarcină de nod frunză este suma estimărilor financiare pentru toate atribuțiile de resurse pentru acea activitate.

O estimare financiară a timpului pe o sarcină de nod frunză este suma estimărilor financiare pentru toate activitățile sale secundare. Acesta este costul estimat al forței de muncă pentru proiect. 

![Estimări de resurse.](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a>Prețul de cost implicit și valuta de cost

Prețul de cost implicit provine din listele de prețuri atașate unității contractante a proiectului. Moneda de cost a unui proiect este mereu moneda unității contractante a proiectului. La o alocare de resurse, estimarea financiară pentru cost este stocată în moneda de cost a proiectului. Uneori, moneda în care rata de cost este stabilită în lista de prețuri este diferită de moneda de cost a proiectului. În aceste cazuri, aplicația convertește moneda în care este stabilit prețul de cost pentru moneda proiectului. Pe grila **Estimări**, toate estimările costurilor sunt afișate și sintetizate în moneda costurilor proiectului. 

## <a name="default-bill-rate-and-sales-currency"></a>Rata de facturare implicită și moneda de vânzare

Prețul de vânzare implicit provine din listele de prețuri ale proiectului atașate contractului de proiect aferent dacă afacerea este câștigată sau din oferta de proiect aferentă dacă afacerea este încă în etapa de pre-vânzare. Moneda de vânmzare a proiectului este mereu moneda ofertei de proiect sau a contractului de proiect. La o alocare de resurse, estimarea financiară pentru vânzări este stocată în moneda de vânzare a proiectului. Spre deosebire de cost, prețul de vânzare care este stabilit în lista de prețuri nu poate fi niciodată diferit de moneda de vânzare a proiectului. Nu există un scenariu în care este necesară conversia valutară. Pe grila **Estimări**, toate estimările vânzărilor sunt afișate și sintetizate în moneda de vânzări a proiectului. 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
