---
title: Adăugarea de noi formulare de entități particularizate (Project Service Automation 2. x)
description: Acest subiect furnizează informații despre cum se adaugă formulare de entități particularizate pentru oportunități, oferte, comenzi sau facturi în Dynamics 365 Project Service Automation 2.x.
author: makk
ms.custom:
- dyn365-projectservice
ms.date: 3/14/2019
ms.topic: article
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 400d817ee7cbae6f6da95db4286ad6c4d6ff349a
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6008011"
---
# <a name="add-new-custom-entity-forms-project-service-automation-2x"></a>Adăugarea de noi formulare de entități particularizate (Project Service Automation 2. x)

[!include [banner](../../includes/psa-now-project-operations.md)]

## <a name="type-field"></a>Tip de câmp 

Dynamics 365 Project Service Automation se bazează pe câmpul **Tip** (**msdyn\_tipcomandă**) al entităților Oportunitate, Ofertă, Comandă și Factură pentru a distinge versiunile **bazate pe activități** ale acestor entități de versiunile **bazate pe articole** și **bazate pe servicii**. Versiunile bazate pe activități ale acestor entități sunt gestionate de PSA. O mare parte din logica de afaceri pe partea de client și pe partea de server a soluției depinde de câmpul **Tip**. De aceea, este important ca câmpul să fie inițializat cu o valoare corectă atunci când entitățile sunt create. O valoare incorectă poate provoca comportamente incorecte și o parte din logica de afaceri ar putea să nu ruleze corect.

## <a name="automatic-form-switching"></a>Comutare automată a formularului

Pentru a evita deteriorarea potențială a datelor și comportamente neașteptate care sunt provocate de inițializarea incorectă și editarea înregistrărilor entității de vânzări, PSA include acum logica pentru comutarea automată a formularelor în formulare predefinite. Această logică duce utilizatorii la formularul corect pentru lucrul cu versiunea bazată pe activități sau cu orice alt tip de entitate Oportunitate, Ofertă, Comandă sau Factură. Când un utilizator deschide versiunea bazată pe activități a unei entități Oportunitate, Ofertă, Comandă sau Factură, formularul este comutat la **Informații proiect**.

Logica de comutare automată a formularului se bazează pe maparea dintre valoarea **formId** și câmpul **msdyn\_tipcomandă**. Toate formularele predefinite au fost adăugate la acea mapare. Cu toate acestea, formularele particularizate trebuie adăugate manual pentru a indica ce versiune a entității se intenționează să gestioneze. Acest lucru se bazează pe câmpul **msdyn\_tipcomandă**. Dacă comutarea formularului lipsește din mapare, logica va comuta la formularul predefinit, pe baza valorii salvate în câmpul **msdyn\_tipcomandă** al entității.

## <a name="add-custom-forms-and-turn-on-the-form-switching-logic"></a>Adăugarea formularelor particularizate și activarea logicii de comutare a formularului

Următorul exemplu arată cum să adăugați un formular particularizat, **Informațiile mele de proiect**, astfel încât să funcționeze cu oportunități bazate pe activități. Același proces este utilizat pentru a adăuga formulare particularizate, astfel încât acestea să funcționeze cu oferte, comenzi și facturi.

Urmați acești pași pentru a crea o versiune particularizată a formularului **Informații proiect**.

1. În entitatea Oportunitate, deschideți formularul **Informații proiect** și salvați o copie sub numele **Informațiile mele de proiect**.
2. Deschideți formularul nou, și apoi, din proprietăți, asigurați-vă că scripturile de inițializare a formularului din formularul **Informații proiect** sunt prezente. 

    > [!IMPORTANT]
    > Nu eliminați scripturile. În caz contrar, unele date pot fi inițializate incorect.

3. Verificați că câmpul **Tip** (**msdyn\_tipcomandă**) este prezent în formular. 

    > [!IMPORTANT]
    > Nu eliminați acest câmp. În caz contrar, scripturile de inițializare vor eșua.

4. Găsiți valoarea **formId** a noului formular. Puteți finaliza acest pas în două moduri diferite:

    - Exportați formularul **Informațiile mele de proiect** ca parte a unei soluții negestionate și apoi căutați valoarea **formId** în fișierul customization.xml al soluției exportate.
    - Deschideți formularul **Informațiile mele de proiect** în editorul de formular, și apoi căutați identificatorul unic global (GUID) lângă parametrul **fromId** în URL, așa se arată în următoarea ilustrație.

    ![Valoarea formId a noului formular din URL.](media/how-to-add-custom-forms-in-v2.0.png)

5. Creați o mapare **msdyn\_tipcomandă** pentru valoarea **formId** editând resursa web msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js. Eliminați codul din resursă și înlocuiți-l cu următorul cod.

    ```javascript
    define(["require", "exports"], function (require, exports) {
        "use strict";
        var SalesDocumentCustomFormIds = (function () {
            function SalesDocumentCustomFormIds() {
            }
            SalesDocumentCustomFormIds.overwriteFormIds = function (mappedFormIds) {
                /*
                ---- Notes ----
                mappedFormIds[SalesEntity][OrderType] => The array of forms IDs that support particular entity and order type
                Add or overwrite customized formId for the particular entity and order type by calling:
                    mappedFormIds[<EntityType>][<msdyn_ordertype>].push("<formId>");
                Allowed msdyn_ordertype values for reference:
                    ServiceBased: 690970002 (Field Service version of the entity)
                    WorkBased: 192350001 (PSA version of the entity)
                    ItemBased: 192350000 (Regular out of the box entity)
                Uncomment and update one of the following lines to register custom PSA form for required entity:
                */      
                //mappedFormIds[1][192350001].push("<formId>"); //Quote
                //mappedFormIds[5][192350001].push("<formId>"); //Quote Line
                //mappedFormIds[2][192350001].push("<formId>"); //Sales Order
                //mappedFormIds[6][192350001].push("<formId>"); //Sales Order Line
                // In this example we have added new form for Opportunity
                mappedFormIds[0][192350001].push("192EE537-DCC4-45D3-B7AF-EA694B9113D2"); //Opportunity
                //mappedFormIds[4][192350001].push("<formId>"); //Opportunity Line
            };
            return SalesDocumentCustomFormIds;
        }());
        exports.default = SalesDocumentCustomFormIds;
    });
    ```

6. Salvați și apoi publicați particularizările.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]