---
title: Configurați câmpuri particularizate ca dimensiuni de preț
description: Acest subiect oferă informații despre parametrizarea dimensiunilor de preț particularizate.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/20/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: d5f59779-a6ed-4854-ab82-2810dace288f
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 8f19254acfc7f03ed7ccca95ed7e2b94cc199d3b
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754716"
---
# <a name="set-up-custom-fields-as-pricing-dimensions"></a>Configurați câmpuri particularizate ca dimensiuni de preț 

Înainte de a începe, acest subiect presupune că ați finalizat procedurile din subiectele [Crearea de câmpuri și entități particularizate](create-custom-fields-entities.md) și [Adăugarea de câmpuri particularizate la parametrizare preț și entități tranzacționale](field-references.md). Dacă nu ați finalizat aceste proceduri, reveniți și completați-le și apoi reveniți la acest subiect. 

Acest subiect oferă informații despre parametrizarea dimensiunilor de preț particularizate. În interfața Web Project Service, pe pagina **Parametri**, fila **Dimensiuni prețuri bazate pe sumă** afișează înregistrările din entitățile dimensiune de preț. În mod implicit, instalarea Project Service creează 2 rânduri în grilă în această filă:

- **msdyn_resourcecategory** (Rol)
- **msdyn_OrganizationalUnit** (Unitate organizatorică)

> [!IMPORTANT]
> Nu ștergeți aceste rânduri. Cu toate acestea, dacă nu aveți nevoie de ele, le puteți face să nu se aplice într-un anumit context prin stabilirea tuturor setărilor **Aplicabil la cost**, **Aplicabil la vânzări** și **Aplicabil la achiziție** la valoarea **Nu**. Setarea acestor valori de atribut la **Nu** are același efect ca nu a avea câmpul ca dimensiune de preț.

Pentru ca un câmp să devină o dimensiune de preț, trebuie să fie:

- Creat ca un câmp în entitățile **Preț rol** și **Adaos preț rol**. Pentru mai multe informații despre cum se face acest lucru, consultați [Adăugarea câmpurilor particularizate la parametrizarea prețurilor și entitățile tranzacționale](field-references.md).
- Creat ca rând în tabelul **Dimensiune preț**. De exemplu, adăugați rânduri de dimensiuni de preț așa cum se arată în graficul următor. 

![Rânduri de dimensiuni de preț bazate pe sume](media/Amt-based-PD.png)

Observați că programul de lucru resurse (**msdyn_resourceworkhours**) a fost adăugat ca o dimensiune bazată pe adaos și a fost adăugat la grilă pe fila **Dimensiune de preț bazată pe adaos** .

![Rânduri de dimensiuni de preț bazate pe adaos](media/Markup-based-PD.png)

> [!IMPORTANT]
> Orice modificare a datelor de dimensiune de preț în acest tabel, existente sau noi, este propagată în logica de business de tarifare Project Service numai după reîmprospătarea cache. Timpul de reîmprospătare a memoriei cache poate dura până la 10 minute. Permiteți acea perioadă de timp pentru a vedea modificările din logica de nerambursare a prețului care trebuie să rezulte din modificările datelor dimensiunii prețurilor.


## <a name="attributes-of-the-pricing-dimensions-table"></a>Atributele tabelului dimensiuni preț
Următoarele secțiuni furnizează informații despre atributele diferite din tabelul **Dimensiuni preț**.

### <a name="pricing-dimension-name"></a>Nume dimensiune de preț
Această valoare ar trebui să fie exact la fel ca numele schemei câmpului care este adăugat la tabelul de **Preț rol** pentru dimensiunile de prețuri particularizate. Pentru mai multe informații despre adăugarea câmpurilor la tabelul **Prețuri de rol**, consultați [Adăugarea câmpurilor particularizate la parametrizarea prețurilor și la entitățile tranzacționale](field-references.md).

### <a name="type-of-dimension"></a>Tipul de dimensiune
Există două tipuri de dimensiuni de preț:
  
  - **Dimensiuni bazate pe sume**: Valorile de dimensiune din contextul de intrare sunt potrivite cu valorile de dimensiune din linia **Preț rol**, iar prețul/costul este implicit direct din tabelul **Preț rol**.
  - **Dimensiuni bazate pe adaos**: Acestea sunt dimensiuni în care Project Service va adopta următorul proces în 3 pași pentru a obține prețul/costul
 
    1. Project service potrivește valorile de dimensiune non-adaos din contextul de intrare la linia de preț de rol pentru a obține rata de bază.
    2. Project service potrivește toate valorile de dimensiune non-adaos din contextul de intrare la linia **Adaos preț rol** pentru a obține un procent de adaos.
    3. Project Service aplică procentul de marcare de la al doilea pas la rata de bază obținută din tabelul de **Preț de rol** în primul pas pentru a ajunge la prețul/costul final.
   
   Următorul tabel ilustrează calcularea adaosurilor de preț.
  
| Rol        | Unitate organizațională    |Locație de lucru      |Titlu standard      |Ore de lucru resursă      |  Adaos|
| ------------|-------------|-------------------|--------------------|-------------------------|--------:|
|             | Contoso India|Local            |                    |Ore suplimentare                 |15     |
|             | Contoso India|Local             |                    |Ore suplimentare                 |10     |
|             | Contoso US   |Local             |                    |Ore suplimentare                 |20     |


Dacă o resursă de la Contoso India a cărei rată de bază este 100 USD lucrează la fața locului, și înregistrează 8 ore de timp regulat și 2 ore suplimentare pe înregistrarea de timp, motorul de tarifare Project Service va folosi rata de bază de 100 pentru 8 ore pentru a înregistra 800 USD. Pentru cele 2 ore suplimentare, se va aplica un adaos de 15% la rata de bază de 100 pentru a obține un preț unitar de 115 USD și va înregistra un cost total de 230 USD.

### <a name="applicable-to-cost"></a>Aplicabil la cost 
Dacă este setat la **Da**, asta indică faptul că valoarea de dimensiune din contextul de intrare ar trebui să se potrivească cu **Preț rol** și **Adaos preț rol** la obținerea costului și a ratelor de adaos.

### <a name="applicable-to-sales"></a>Aplicabil la vânzări
Dacă este setat la **Da**, asta indică faptul că valoarea de dimensiune din contextul de intrare ar trebui să se potrivească cu **Preț rol** și **Adaos preț rol** la obținerea facturii și a ratelor de adaos.

### <a name="applicable-to-purchase"></a>Aplicabil la achiziție
Dacă este setat la **Da**, asta indică faptul că valoarea de dimensiune din contextul de intrare ar trebui să se potrivească cu **Preț rol** și **Adaos preț rol** la obținerea prețului de achiziție. În prezent Project Service nu acceptă scenarii de subcontractare, astfel încât acest câmp nu este utilizat. 

### <a name="priority"></a>Prioritate
Setarea priorității de dimensiune ajută tarifarea Project Service să producă un preț chiar și atunci când nu poate găsi o potrivire exactă între valorile dimensiunilor de intrare și valorile din tabelele de **Preț rol** sau **Adaos preț rol**. În acest scenariu, Project Service va utiliza valori Null pentru valori de dimensiune fără potrivire prin cântărirea dimensiunilor în ordinea priorității lor.

- **Prioritate cost**: Valoarea priorității costului unei dimensiuni va indica ponderea acelei dimensiuni atunci când se potrivește cu parametrizarea prețurilor de cost. Valoarea de **Prioritate cost** trebuie să fie unică între dimensiunile care sunt **Aplicabile costului**.
- **Prioritate vânzări**: Valoarea priorității vânzărilor unei dimensiuni va indica ponderea acelei dimensiuni atunci când se potrivește cu parametrizarea prețurilor de vânzare sau a ratelor de facturare. Valoarea de **Prioritate vânzări** trebuie să fie unică între dimensiunile care sunt **Aplicabile vânzărilor**.
