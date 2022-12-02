---
title: Înlocuiri de preț cu dată efectivă
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
# <a name="date-effective-price-overrides"></a>Înlocuiri de preț cu dată efectivă 

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

*Înlocuiri de preț cu dată efectivă* oferă o modalitate de a înlocui sau modifica anumite prețuri din lista de prețuri. De exemplu, aveți o listă de prețuri standard care este în vigoare de la 1 ianuarie 2022 până la 31 decembrie 2022. Această listă de prețuri are prețuri pentru multe roluri. Prețul care este stabilit pentru rolul **Tehnician de rețea** este de 100 de dolari SUA (USD) pe oră. Când un tehnician de rețea înregistrează ora între 1 ianuarie 2022 și 31 decembrie 2022, ora are prețul de 100 USD. La 1 octombrie 2022, trebuie să ajustați prețul *numai* pentru rolul **Tehnician de rețea**, de la 100 USD pe oră la 110 USD pe oră. Funcția **Înlocuiri de preț cu dată efectivă** vă permite să configurați această modificare ca o înlocuire a rândului pentru acel preț specific pentru rol. Prin urmare, nu trebuie să copiați întreaga listă de prețuri și să modificați prețul doar acelui rând.

## <a name="date-effective-price-overrides-for-labor-pricing"></a>Înlocuirile de preț cu dată efectivă pentru tarifarea forței de muncă

Procesul de stabilire a înlocuirilor de preț cu dată efectivă pentru timpul de muncă într-un proiect constă în doi pași de bază.

1. Activați funcția **Înlocuiri de preț cu dată efectivă**.
1. Configurați o înlocuire de preț cu dată efectivă.

### <a name="enable-the-date-effective-price-overrides-feature"></a>Activarea funcției Înlocuiri de preț cu dată efectivă

> [!NOTE]
> După activarea funcției **Înlocuiri de preț cu dată efectivă**, aceasta nu poate fi dezactivată.

Pentru a activa funcția **Înlocuiri de preț cu dată efectivă**, urmați acești pași.

1. Accesați **Setări** \> **Parametri**.
1. Deschideți înregistrarea **Parametri**.
1. În Panoul acțiuni, pe fila **Controlul caracteristicilor**, selectați **Activați înlocuiri de preț cu dată efectivă**.
1. În caseta de dialog de confirmare, selectați **OK**.
1. După câteva momente, reîmprospătați browserul. Capabilitățile de înlocuire de preț cu dată efectivă ar trebui să fie acum disponibile. Veți ști că aceste capabilități au fost activate dacă **Activați înlocuirile de preț cu dată efectivă** nu mai apare în Panoul acțiuni.

### <a name="set-up-a-date-effective-price-override"></a>Configurarea unei înlocuiri de preț cu dată efectivă

Înlocuirile de preț cu dată efectivă pot fi configurate în listele de prețuri **Cost**, **Vânzări** sau **Achiziții**.

> [!NOTE]
>Comportamentul funcției **Înlocuiri de preț cu dată efectivă** are în prezent următoarele limitări:
>
> - Numai prețurile de rol și adaosurile de preț de rol acceptă funcția **Înlocuiri de preț cu dată efectivă** în Project Operations.
> - Când copiați o listă de prețuri utilizând acțiunea **Copiere** asupra paginii **Detalii listă de prețuri** și atunci când creați o listă de prețuri de proiect dintr-o listă de prețuri standard sau personalizată în timpul creării contractului, înlocuirile de preț cu dată efectivă **nu** sunt copiate din lista de prețuri sursă.

Pentru a configura o înlocuire de preț cu dată efectivă pentru un preț de rol sau un adaos de preț de rol, urmați acești pași.

1. Deschideți pagina pentru lista de prețuri pentru care doriți să configurați înlocuirea de preț cu dată efectivă.
1. Selectați fila **Prețurile de rol**. Această filă listează toate înregistările **Preț de rol** din lista de prețuri.
1. Selectați înregistrarea **Preț de rol** pentru care doriți să configurați o nouă înlocuire de preț cu dată efectivă, apoi atingeți de două ori (sau faceți dublu clic) pe **Preț de rol** pentru a deschide pagina **Detalii preț de rol**.
1. Selectați fila **Înlocuiri dată efectivă**. Grila din această filă listează toate înlocuirile de preț cu dată efectivă pentru înregistrarea **Preț de rol** selectată.
1. Pe bara de instrumente de deasupra grilei, selectați **Înlocuire de preț de rol nouă**. Glisorul **Înlocuire de preț de rol nouă** se deschide.
1. Specificați data de intrare în vigoare, unitatea și noul preț pentru înlocuirea prețului. Apoi, selectați **Salvare** și închideți formularul.

> [!NOTE]
> - O înlocuire de preț cu dată efectivă pentru preț de rol sau un adaos de preț de rol este aplicabilă aceleiași combinații de valori ale dimensiunii de preț care există în rândul părinte **Preț de rol** sau **Preț de adaos de rol**.
> - Data care este selectată în câmpul **În vigoare de la** ar trebui să se încadreze în datele de intrare în vigoare din lista de prețuri părinte. Înlocuirea de preț se va produce la data selectată în câmpul **În vigoare de la** și se va aplica până la sfârșitul datei de încheiere din lista de prețuri părinte. Dacă configurați o altă înlocuire de preț cu dată efectivă pentru același preț de rol, prima înlocuire de preț va intra în vigoare la data care este selectată în câmpul **În vigoare de la** și se va aplica până la începutul celei de-a doua înlocuiri.

## <a name="examples"></a>Exemple

### <a name="example-1-determining-date-effectivity-for-a-role-price-that-has-role-price-overrides"></a>Exemplul 1: stabilirea datei de intrare în vigoare pentru un preț de rol care are înlocuiri de preț de rol

Următorul exemplu arată cum este stabilită data de intrare în vigoare pentru un anumit preț de rol pentru care sunt configurate înlocuirile de preț de rol.

**Lista de prețuri A: 1 ianuarie – 30 iunie**

*Preț de rol*

| Preț de rol | Unitate | Preț | Efectul asupra prețurilor pentru tranzacțiile primite |
|---|---|---|---|
| Tehnician de rețea | Oră | 100 | Acest preț va fi utilizat pentru orice tranzacții ale căror dată de tranzacție este cuprinsă între 1 ianuarie și 14 martie. |

*Înlocuire de preț de rol*

| În vigoare de la | Unitate | Preț | Efectul asupra prețurilor pentru tranzacțiile primite |
|---|---|---|---|
| Martie 15 | Oră | 110 | Acest preț va fi utilizat pentru orice tranzacții ale căror dată de tranzacție este cuprinsă între 15 martie și 30 martie. |
| Aprilie 1 | Oră | 120 | Acest preț va fi utilizat pentru orice tranzacții ale căror dată de tranzacție este cuprinsă între 1 aprilie și 30 iunie. |

### <a name="example-2-determining-date-effectivity-for-a-role-price-markup-that-has-role-price-markup-overrides"></a>Exemplul 2: stabilirea datei de intrare în vigoare pentru un adaos de preț de rol care are înlocuiri de adaos de preț de rol

Următorul exemplu arată cum este stabilită data de intrare în vigoare pentru un anumit adaos de preț de rol pentru care sunt configurate înlocuirile de adaos de preț de rol.

**Lista de prețuri A: 1 ianuarie – 30 iunie**

*Preț de rol*

| Preț de rol | Ore de lucru | Unitate | Preț | Efectul asupra prețurilor pentru tranzacțiile primite |
|---|---|---|---|---|
| Tehnician de rețea | Obișnuit | Oră | 100 | Acest preț va fi utilizat pentru orice tranzacții ale căror dată de tranzacție este cuprinsă între 1 ianuarie și 14 martie. |

*Adaos de preț de rol*

| Unitate organizațională | Ore de lucru | Adaos % |
|---|---|---|
| Contoso US | Ore suplimentare | 10% |

*Înlocuire adaos de preț de rol*

| În vigoare de la | Preț | Efectul asupra prețurilor pentru tranzacțiile primite |
|---|---|---|
| Martie 15 | 20% | Acest procent de adaos va fi utilizat pentru orice tranzacții ale căror dată de tranzacție este cuprinsă între 15 martie și 30 martie. |
| Aprilie 1 | 25% | Acest adaos va fi utilizat pentru orice tranzacții ale căror dată de tranzacție este cuprinsă între 1 aprilie și 30 iunie. |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
