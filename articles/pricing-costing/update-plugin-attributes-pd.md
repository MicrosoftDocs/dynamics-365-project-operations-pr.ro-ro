---
title: Actualizarea atributelor inserturilor cu noile dimensiuni de preț
description: Acest subiect furnizează informații despre cum să actualizați atributele inserturilor pentru dimensiunile de tarifare.
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d57ec617d2c7b10a01a75e7eaa9ca2d646af3f6ee1d06d4e6fb228fc0533da27
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/06/2021
ms.locfileid: "6988351"
---
# <a name="update-plug-in-attributes-with-new-pricing-dimensions"></a>Actualizați atributele inserturilor cu noile dimensiuni de preț

Acest subiect furnizează informații despre cum să actualizați atributele inserturilor pentru dimensiunile de tarifare.

> [!NOTE]
> Acest subiect se aplică numai caracteristicilor de ofertă și contract în Dynamics 365 Project Operations.

## <a name="prerequisites"></a>Cerințe preliminare
Înainte de a finaliza pașii din acest subiect, trebuie să fi finalizat procedurile din următoarele subiecte:

  - [Crearea câmpurilor și entităților particularizate](create-custom-fields-entities-pricing-dimensions.md) 
  - [Adăugarea câmpurilor particularizate la configurarea prețurilor și la entitățile tranzacționale ](add-custom-fields-price-setup-transactional-entities.md)
  - [Configurarea câmpurilor particularizate ca dimensiuni de preț](set-up-custom-fields-pricing-dimensions.md). 
  
Dacă nu ați finalizat aceste proceduri, completați-le și apoi reveniți la acest subiect.

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