---
title: Configurarea câmpurilor particularizate ca dimensiuni de preț
description: Acest subiect oferă informații despre cum să configurați dimensiunile de preț utilizând câmpuri particularizate.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: e40f0336d98cd8452642eb582c4d9daf2304ceb2532ef75ce9d03a0fa4bd8e8b
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/06/2021
ms.locfileid: "7003606"
---
# <a name="set-up-custom-fields-as-pricing-dimensions"></a>Configurarea câmpurilor particularizate ca dimensiuni de preț

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Înainte de a începe, acest subiect presupune că ați finalizat procedurile din subiectele [Crearea de câmpuri și entități particularizate](create-custom-fields-entities-pricing-dimensions.md) și [Adăugarea de câmpuri necesare particularizate la configurarea prețului și entități tranzacționale](add-custom-fields-price-setup-transactional-entities.md). Dacă nu ați finalizat aceste proceduri, reveniți și completați-le și apoi reveniți la acest subiect. 

Acest subiect oferă informații despre parametrizarea dimensiunilor de preț particularizate. Pe pagina **Parametri**, fila **Dimensiuni de preț pe baza sumei**, afișează înregistrările în entitățile de dimensiune a prețului. În mod implicit, există două rânduri în grilă pe această filă:

- **msdyn_resourcecategory** (Rol)
- **msdyn_OrganizationalUnit** (Unitate organizatorică)

> [!IMPORTANT]
> Nu ștergeți aceste rânduri. Cu toate acestea, dacă nu aveți nevoie de ele, le puteți face să nu se aplice într-un anumit context prin stabilirea tuturor setărilor **Aplicabil la cost**, **Aplicabil la vânzări** și **Aplicabil la achiziție** la valoarea **Nu**. Setarea acestor valori de atribut la **Nu** are același efect ca nu a avea câmpul ca dimensiune de preț.

Pentru ca un câmp să devină o dimensiune de preț, trebuie să fie:

- Creat ca un câmp în entitățile **Preț rol** și **Adaos preț rol**. Pentru mai multe informații despre cum se face acest lucru, consultați [Adăugarea câmpurilor particularizate la parametrizarea prețurilor și entitățile tranzacționale](add-custom-fields-price-setup-transactional-entities.md).

- Creat ca rând în tabelul **Dimensiune preț**. De exemplu, adăugați rânduri de dimensiuni de preț așa cum se arată în graficul următor. 

![Rânduri de dimensiuni de preț bazate pe sume.](media/Amt-based-PD.png)

Observați că programul de lucru resurse (**msdyn_resourceworkhours**) este adăugat ca o dimensiune bazată pe adaos și a fost adăugat la grilă pe fila **Dimensiune de preț bazată pe adaos** .

![Rânduri de dimensiuni de preț bazate pe adaos.](media/Markup-based-PD.png)


> [!IMPORTANT]
> Orice modificare a datelor de dimensiune de preț în acest tabel, existente sau noi, este propagată în logica de business de tarifare numai după reîmprospătarea cache. Timpul de reîmprospătare a memoriei cache poate dura până la 10 minute. Permiteți acea perioadă de timp pentru a vedea modificările din logica de nerambursare a prețului care trebuie să rezulte din modificările datelor dimensiunii prețurilor.


## <a name="attributes-of-the-pricing-dimensions-table"></a>Atributele tabelului dimensiuni preț
Următoarele secțiuni furnizează informații despre atributele diferite din tabelul **Dimensiuni preț**.

### <a name="pricing-dimension-name"></a>Nume dimensiune de preț
Această valoare ar trebui să fie exact la fel ca numele schemei câmpului care este adăugat la tabelul de **Preț rol** pentru dimensiunile de prețuri particularizate. Pentru mai multe informații despre adăugarea câmpurilor la tabelul **Prețuri de rol**, consultați [Adăugarea câmpurilor particularizate la parametrizarea prețurilor și la entitățile tranzacționale](add-custom-fields-price-setup-transactional-entities.md).

### <a name="type-of-dimension"></a>Tipul de dimensiune
Există două tipuri de dimensiuni de preț:
  
  - **Dimensiuni bazate pe sume**: Valorile de dimensiune din contextul de intrare sunt potrivite cu valorile de dimensiune din linia **Preț rol**, iar prețul/costul este implicit direct din tabelul **Preț rol**.
  - **Dimensiuni bazate pe adaos**: Acestea sunt dimensiuni în care este utilizat următorul proces în trei pași pentru a obține prețul/costul:
 
    1. Valorile de dimensiune non-adaos din contextul de intrare sunt potrivite la linia de preț de rol pentru a obține rata de bază.
    2. Valorile de dimensiune non-adaos din contextul de intrare sunt potrivite la linia **Adaos preț rol** pentru a obține un procent de adaos.
    3. Se aplică procentul de marcare de la al doilea pas la rata de bază obținută din tabelul de **Preț de rol** în primul pas pentru a ajunge la prețul/costul final.
   
   Următorul tabel ilustrează calcularea adaosurilor de preț.
  
| Rol        | Unitate organizațională    |Locație de lucru      |Titlu standard      |Ore de lucru resursă      |  Adaos|
| ------------|-------------|-------------------|--------------------|-------------------------|--------:|
|             | Contoso India|Local            |                    |Ore suplimentare                 |15     |
|             | Contoso India|Local             |                    |Ore suplimentare                 |10     |
|             | Contoso SUA   |Local             |                    |Ore suplimentare                 |20     |


Dacă o resursă din Contoso India a cărei rată de bază este 100 USD lucrează la fața locului, și înregistrează 8 ore de timp regulat și 2 ore suplimentare pe înregistrarea de timp, motorul de tarifare va folosi rata de bază de 100 pentru 8 ore pentru a înregistra 800 USD. Pentru cele 2 ore suplimentare, se va aplica un adaos de 15% la rata de bază de 100 pentru a obține un preț unitar de 115 USD și va înregistra un cost total de 230 USD.

### <a name="applicable-to-cost"></a>Aplicabil la cost 
Dacă este setat la **Da**, asta indică faptul că valoarea de dimensiune din contextul de intrare ar trebui să se potrivească cu **Preț rol** și **Adaos preț rol** la obținerea costului și a ratelor de adaos.

### <a name="applicable-to-sales"></a>Aplicabil la vânzări
Dacă este setat la **Da**, asta indică faptul că valoarea de dimensiune din contextul de intrare ar trebui să se potrivească cu **Preț rol** și **Adaos preț rol** la obținerea facturii și a ratelor de adaos.

### <a name="applicable-to-purchase"></a>Aplicabil la achiziție
Dacă este setat la **Da**, asta indică faptul că valoarea de dimensiune din contextul de intrare ar trebui să se potrivească cu **Preț rol** și **Adaos preț rol** la obținerea prețului de achiziție. Scenariile de subcontractare nu sunt acceptate, deci acest câmp nu este utilizat. 

### <a name="priority"></a>Prioritate
Setarea priorității de dimensiune ajută tarifarea să producă un preț chiar și atunci când nu poate găsi o potrivire exactă între valorile dimensiunilor de intrare și valorile din tabelele de **Preț rol** sau **Adaos preț rol**. În acest scenariu, valori nule sunt utilizate pentru valori de dimensiune fără potrivire prin cântărirea dimensiunilor în ordinea priorității lor.

- **Prioritate cost**: Valoarea priorității costului unei dimensiuni va indica ponderea acelei dimensiuni atunci când se potrivește cu parametrizarea prețurilor de cost. Valoarea de **Prioritate cost** trebuie să fie unică între dimensiunile care sunt **Aplicabile costului**.
- **Prioritate vânzări**: Valoarea priorității vânzărilor unei dimensiuni va indica ponderea acelei dimensiuni atunci când se potrivește cu parametrizarea prețurilor de vânzare sau a ratelor de facturare. Valoarea de **Prioritate vânzări** trebuie să fie unică între dimensiunile care sunt **Aplicabile vânzărilor**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]