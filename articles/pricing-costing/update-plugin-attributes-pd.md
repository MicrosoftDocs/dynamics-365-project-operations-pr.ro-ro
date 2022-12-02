---
title: Actualizarea atributelor inserturilor cu noile dimensiuni de preț
description: Acest articol furnizează informații despre cum să actualizați atributele inserturilor pentru dimensiunile de preț.
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 2ae502fea533d9f199ef5ee1cc85b623f08cbd84
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920029"
---
# <a name="update-plug-in-attributes-with-new-pricing-dimensions"></a>Actualizați atributele inserturilor cu noile dimensiuni de preț

Acest articol furnizează informații despre cum să actualizați atributele inserturilor pentru dimensiunile de preț.

> [!NOTE]
> Acest articol se aplică numai caracteristicilor de ofertă și contract în Dynamics 365 Project Operations.

## <a name="prerequisites"></a>Cerințe preliminare
Înainte de a finaliza pașii din acest articol, trebuie să fi finalizat procedurile din următoarele articole:

  - [Crearea câmpurilor și entităților particularizate](create-custom-fields-entities-pricing-dimensions.md) 
  - [Adăugarea câmpurilor particularizate la configurarea prețurilor și la entitățile tranzacționale ](add-custom-fields-price-setup-transactional-entities.md)
  - [Configurarea câmpurilor particularizate ca dimensiuni de preț](set-up-custom-fields-pricing-dimensions.md). 
  
Dacă nu ați finalizat acele proceduri, finalizați-le și apoi reveniți la acest articol.

## <a name="register-a-plug-in"></a>Înregistrați un insert
Când se creează un detaliu de linie de ofertă pe pagina **Linie de ofertă** pentru o linie de ofertă de proiect, sistemul creează două linii de estimare. O linie este pentru partea de cost a estimării, iar cealaltă linie este pentru partea de vânzări. Acest lucru este la fel pentru liniile de contract de proiect.

Când efectuați o modificare a cantității sau a unui câmp pe partea de cost, acea modificare este propagată și pe partea de vânzare. Acest lucru este posibil deoarece pluginurile PreOperation de pe entitățile de detalii Quotelinedetail și contractline conectează atribute specifice din partea costurilor cu partea de vânzări a tranzacției. Dacă aveți nevoie de modificări ale valorilor dimensiunii prețurilor din partea vânzărilor, care trebuie făcute și din partea costurilor, următoarele inserturi trebuie să fie reînregistrate după efectuarea modificărilor la dimensiunea prețurilor.

Acestea sunt inserturile pentru actualizare și reînregistrare:

- PreOperationContractLineDetailUpdate - **Update msdyn_orderlinetransaction**
- PreOperationQuoteLineDetailUpdate - **Updates msdyn_quotelinetransaction**

Parcurgeți pașii următori pentru a actualiza și a înregistra din nou inserturile.

1. Deschideți **PluginRegistrationTool** și conectați-vă la mediul dvs. Project Operations Dataverse.
2. Selectați **Căutare** și tastați primele litere ale insertului care urmează să fie actualizat.
3. După ce se găsește insertul, selectați-l și apoi selectați **Selectați pe formularul principal**.
4. Selectați pasul **Actualizați msdyn_orderlinetransaction**, faceți clic dreapta și apoi selectați **Actualizați**.
5. În caseta de dialog **Actualizare** selectați elipsa (**...**) în atributele de filtrare.
6. Fereastra de atribute de filtrare se deschide și oferă o listă cu toate atributele din entitate și dimensiunile de stabilire a prețurilor. Bifați casetele de selectare pentru atributele dimensiunii de preț.
7. Selectați **OK** pentru a închide pagina, apoi selectați **Actualizare pas**.
8. Repetați pașii 2-7 pentru al doilea insert, **PreOperationQuoteLineDetail**. Pentru acest insert, trebuie să actualizați pasul **Update of msdyn_quotelinetransaction**.
9. Închideți **PluginRegistrationTool**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]