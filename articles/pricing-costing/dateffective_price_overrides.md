---
title: Prețurile efective de date
description: Acest articol explică cum să configurați înlocuiri de preț pentru anumite prețuri din lista de prețuri.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 41af5176c0809c9621fc0fa946a04492da7d152b
ms.sourcegitcommit: 37293b0b28f072deafc00112ddbbea91c48a7802
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 09/08/2022
ms.locfileid: "9446008"
---
# <a name="date-effective-price-overrides"></a>Prețurile efective de date 

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

*Prețurile efective de date* oferă o modalitate de a modifica sau de a modifica anumite prețuri din lista de prețuri. De exemplu, aveți o listă de prețuri standard care este în vigoare de la 1 ianuarie 2022 până la 31 decembrie 2022. Această listă de prețuri are prețuri pentru multe roluri. Prețul care este stabilit pentru **Tehnician de rețea** rolul este de 100 de dolari SUA (USD) pe oră. Când un tehnician de rețea înregistrează ora între 1 ianuarie 2022 și 31 decembrie 2022, ora are prețul la 100 USD. La 1 octombrie 2022, trebuie să ajustați prețul *numai* pentru **Tehnician de rețea** rol, de la 100 USD pe oră la 110 USD pe oră. The **Datele efective ale prețului sunt anulate** caracteristica vă permite să configurați această modificare ca o înlocuire a rândului pentru acel preț specific pentru rol. Prin urmare, nu trebuie să copiați întreaga listă de prețuri și să modificați prețul doar acelui rând.

## <a name="date-effective-price-overrides-for-labor-pricing"></a>Prețurile efective în funcție de dată pentru prețul forței de muncă

Procesul de stabilire a depășirilor de preț efective la data pentru timpul de muncă într-un proiect constă în doi pași de bază.

1. Permite **Datele efective ale prețului sunt anulate** caracteristică.
1. Configurați o modificare a prețului efectivă la data.

### <a name="enable-the-date-effective-price-overrides-feature"></a>Activați funcția Data pentru anularea prețului în vigoare

> [!NOTE]
> După **Datele efective ale prețului sunt anulate** caracteristica este activată, nu poate fi dezactivată.

Pentru a activa **Prețurile efective de date** caracteristică, urmați acești pași.

1. Mergi la **Setări** \> **Parametrii**.
1. Deschide **Parametrii** record.
1. În panoul de acțiuni, pe **Controlul caracteristicilor** filă, selectați **Activați anulări ale prețurilor la data efectivă**.
1. În caseta de dialog de confirmare, selectați **OK**.
1. După câteva momente, reîmprospătați browserul. Capacitățile de anulare a prețului efective în funcție de dată ar trebui să fie acum disponibile. Veți ști că aceste capabilități au fost activate dacă **Activați anulări ale prețurilor la data efectivă** nu mai apare în panoul de acțiuni.

### <a name="set-up-a-date-effective-price-override"></a>Configurați o modificare a prețului efectivă la data

Depășirile de preț efective în funcție de dată pot fi configurate pe **Cost**, **·**, sau **Cumpărare** liste de preturi.

> [!NOTE]
>Comportamentul lui **Datele efective ale prețului sunt anulate** are în prezent următoarele limitări:
>
> - Numai prețurile rolului și markupurile prețului rolului acceptă **Datele efective ale prețului sunt anulate** caracteristică în Operațiuni de proiect.
> - Când copiați o listă de prețuri utilizând **Copie** acțiune asupra **Detalii lista de preturi** și atunci când creați o listă de prețuri de proiect dintr-o listă de prețuri standard sau personalizată în timpul creării contractului, înlocuirile de preț efective la data sunt **nu** copiat din lista de prețuri sursă.

Pentru a configura o modificare a prețului valabilă la data pentru un preț de rol sau un markup pentru prețul rolului, urmați acești pași.

1. Deschideți pagina pentru lista de prețuri pentru care doriți să configurați anularea prețului în vigoare la data.
1. Selectează **Prețurile de rol** fila. Această filă listează toate **Prețul rolului** înregistrări în lista de prețuri.
1. Selectează **Prețul rolului** înregistrați pentru care doriți să configurați un nou preț de anulare efectiv în funcție de dată, apoi atingeți de două ori (sau faceți dublu clic) **Prețul rolului** pentru a deschide **Detalii preț rol** pagină.
1. Selectează **Înlocuirea datei în vigoare** fila. Grila din această filă listează toate înlocuirile de preț valabile pentru data selectate **Prețul rolului** record.
1. Pe bara de instrumente de deasupra grilei, selectați **Înlocuirea prețului de nou rol**. The **Înlocuirea prețului de nou rol** glisorul se deschide.
1. Specificați data de intrare în vigoare, unitatea și noul preț pentru anularea prețului. Apoi selectați **Salvați**, și închideți formularul.

> [!NOTE]
> - O modificare a prețului efectivă la data pentru un preț de rol sau o markup pentru prețul rolului este aplicabilă aceleiași combinații de valori ale dimensiunii de preț care există în părintele.**Prețul rolului** sau **Markup prețul rolului** rând.
> - Data care este selectată în **Efectiv de la** câmpul ar trebui să se încadreze în datele de intrare în vigoare ale listei de prețuri părinte. Modificarea prețului va intra în vigoare la data selectată în **Efectiv de la** câmp și se va aplica până la sfârșitul datei de încheiere a listei de prețuri părinte. Dacă configurați o altă modificare a prețului valabilă la data pentru același preț de rol, prima modificare a prețului va intra în vigoare la data care este selectată în **Efectiv de la** câmp și se va aplica până la începutul celei de-a doua opțiuni.

## <a name="examples"></a>Exemple

### <a name="example-1-determining-date-effectivity-for-a-role-price-that-has-role-price-overrides"></a>Exemplul 1: determinarea datei de intrare în vigoare pentru un preț de rol care are suprascrieri ale prețului rolului

Următorul exemplu arată cum este determinată data efectuării pentru un anumit preț de rol pentru care sunt configurate înlocuirile de preț de rol.

**Lista de prețuri A: 1 ianuarie - 30 iunie**

*Prețul rolului*

| Prețul rolului | Unitate | Preț | Efectul asupra prețurilor pentru tranzacțiile primite |
|---|---|---|---|
| Tehnician de rețea | Oră | 100 | Acest preț va fi utilizat pentru orice tranzacție la care data tranzacției este între 1 ianuarie și 14 martie. |

*Suprascrierea prețului rolului*

| Efectiv de la | Unitate | Preț | Efectul asupra prețurilor pentru tranzacțiile primite |
|---|---|---|---|
| Martie 15 | Oră | 110 | Acest preț va fi utilizat pentru orice tranzacție la care data tranzacției este între 15 și 30 martie. |
| Aprilie 1 | Oră | 120 | Acest preț va fi utilizat pentru orice tranzacție la care data tranzacției este între 1 aprilie și 30 iunie. |

### <a name="example-2-determining-date-effectivity-for-a-role-price-markup-that-has-role-price-markup-overrides"></a>Exemplul 2: determinarea datei de intrare în vigoare pentru un markup pentru prețul rolului care are suprascrieri ale prețului rolului

Următorul exemplu arată modul în care este determinată data efectuării pentru un anumit markup al prețului pentru rol pentru care sunt configurate înlocuiri ale markupului.

**Lista de prețuri A: 1 ianuarie - 30 iunie**

*Prețul rolului*

| Prețul rolului | Ore de lucru | Unitate | Preț | Efectul asupra prețurilor pentru tranzacțiile primite |
|---|---|---|---|---|
| Tehnician de rețea | Regulat | Oră | 100 | Acest preț va fi utilizat pentru orice tranzacție la care data tranzacției este între 1 ianuarie și 14 martie. |

*Markup prețul rolului*

| Unitate de organizare | Ore de lucru | Marcare % |
|---|---|---|
| Contoso US | Ore suplimentare | 10% |

*Înlocuirea markupului prețului rolului*

| Efectiv de la | Preț | Efectul asupra prețurilor pentru tranzacțiile primite |
|---|---|---|
| Martie 15 | 20% | Acest procent de markup va fi utilizat pentru orice tranzacții la care data tranzacției este între 15 și 30 martie. |
| Aprilie 1 | 25% | Acest markup va fi utilizat pentru orice tranzacție la care data tranzacției este între 1 aprilie și 30 iunie. |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
