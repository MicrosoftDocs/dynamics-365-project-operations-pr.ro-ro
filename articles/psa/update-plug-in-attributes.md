---
title: Actualizați atributele inserturilor pentru a include noi dimensiuni de tarifare
description: Acest subiect furnizează informații despre actualizarea atributelor inserturilor pentru dimensiunile de tarifare.
author: Rumant
manager: kfend
ms.custom: ''
ms.date: 11/19/2018
ms.topic: article
ms.service: dynamics-365-customerservice
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: f215555dd7b29444e00499c0e731624e51057250
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082879"
---
# <a name="update-plug-in-attributes-to-include-new-pricing-dimensions"></a>Actualizați atributele inserturilor pentru a include noi dimensiuni de tarifare

> [!NOTE]
> Dacă nu utilizați funcțiile de ofertare și contractare Project Service Automation (PSA), puteți sări peste acest subiect.

Acest subiect presupune că ați finalizat procedurile din subiectele [Crearea de câmpuri și entități particularizate](create-custom-fields-entities.md), [Adăugarea de câmpuri particularizate la parametrizare preț și entități tranzacționale](field-references.md) și [Configurare câmpuri particularizate ca dimensiuni de tarifare](set-up-pricing-dimensions.md). Dacă nu ați finalizat aceste proceduri, reveniți și completați-le și apoi reveniți la acest subiect.

Când se creează un detaliu al liniei de ofertă în pagina **linie ofertă** pentru o linie de ofertă de proiect, sistemul creează două linii de estimare în fundal -- o linie pentru partea de cost a estimării și una pentru partea de vânzări. Acest lucru este la fel pentru liniile de contract de proiect.

Când efectuați o modificare a cantității sau a unui câmp pa partea de cost, acea modificare este propagată pe partea de vânzare. Asta este posibil din cauza următoarele inserturi care trebuie să fie re-înregistrate după o modificare a dimensiunilor de tarifare.

- PreOperationContractLineDetailUpdate - Actualizări **msdyn_orderlinetransaction**.
- PreOperationQuoteLineDetailUpdate - Actualizări **msdyn_quotelinetransaction**.

Următorii pași vă explică procesul de înregistrare a inserturilor.

1. Deschideți **PluginRegistrationTool** și conectați-vă la instanța dvs. online.
2. Faceți clic pe **Căutare** și căutați insertul de actualizat.

 ![Captură de ecran a arborelui de căutare](media/PRT-1.png)

3. După ce se găsește insertul, selectați-l și apoi faceți clic pe **Selectați în formularul principal**.

4. Selectați pasul insertului de actualizat, faceți clic dreapta, iar apoi selectați **Actualizare**.

 ![Captură de ecran cu insertul de actualizat](media/PRT-2.png)
 
5. În fereastra de actualizare, faceți clic pe puncte de suspensie ( **...** ) în atributele de filtrare.

 ![Captură de ecran a informațiilor de configurare Actualizare pas existent](media/PRT-3.png)
 
6. Selectați casetele de validare a atributului de tarifare.

 ![Captură de ecran care arată selectarea casetei de validare pentru atributele de tarifare](media/PRT-4.png)

7. Faceți clic pe **OK** pentru a închide pagina, apoi selectați **Actualizare pas**.

 ![Captură de ecran cu butonul „Actualizare pas"](media/PRT-5.png)
 
8. Repetați acest proces pentru al doilea insert, **PreOperationQuoteLineDetail - Actualizare msdyn_quotelinetransaction**.

9. Închideți instrumentul de înregistrare inserturi.
