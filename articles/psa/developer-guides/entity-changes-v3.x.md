---
title: Modificări de entitate, control și interfață cu utilizatorul (Project Service Automation 3.x)
description: Acest subiect descrie modificările soluției pentru Microsoft Dynamics Project Service Automation 3.x.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 03/15/2019
ms.topic: article
ms.service: business-applications
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: fa80f459260f30360e78a1e7bcc00706dbc0b5a4
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5284913"
---
# <a name="entity-control-and-user-interface-changes-project-service-automation-3x"></a>Modificări de entitate, control și interfață cu utilizatorul (Project Service Automation 3.x)

[!include [banner](../../includes/psa-now-project-operations.md)]


Odată cu lansarea Microsoft Dynamics Project Service Automation (PSA) 3.x, s-au efectuat multe modificări la nivelul entităților, controalelor, vizualizărilor și interfeței cu utilizatorul. Acest subiect oferă informații despre aceste modificări importante.

## <a name="parent-child-relationships-for-sales-document-sales-document-line-sales-document-line-detail-entities"></a>Relațiile părinte-fiu pentru documentul de vânzări, linia documentului de vânzări, entitățile detalii de linie document de vânzări
În versiunile de Dynamics 365 Project Service Automation (PSA) lansate înainte de versiunea 3.0, anumite relații dintre documentele de vânzări, liniile de document de vânzări și entitățile detalii de linie document de vânzări au fost implementate prin câmpuri de șir care ar deține o reprezentare a șirului de GUID a entității afiliate. Acest lucru s-a datorat limitărilor de platformă care necesită cod particularizat semnificativ pe partea server și client a soluției pentru a face aceste relații să funcționeze similar cu relațiile tipice de entitate Dynamics CRM și pentru a face ca aceste câmpuri șir să acționeze sub formă de câmpuri de căutare.

PSA 3.0 a fost actualizat pentru a profita de noile relații între entități între entitățile document de vânzări și de linie de document de vânzări.

Întrucât câmpurile de căutare pot fi utilizate acum pentru a indica referințe la entități, câmpurile care au deținut valoarea șir a GUID-ului entității corelate în versiunile anterioare nu mai sunt necesare și, prin urmare, au fost perimate. Codul pe partea server și client particularizat care gestionează relațiile definite de câmpuri șir moștenite este și el perimat.

### <a name="entity-schema-changes"></a>Modificările schemei de entitate
Următorul tabel furnizează o listă unu-la-unu a câmpurilor de șir perimate și a noilor câmpuri de căutare pentru entități. 

 Entitate |   Câmp perimat (șir) | Câmp nou (căutare)
--- | --- | ---
invoicedetail (linie factură) |  msdyn_contractline |    msdyn_contractlineid
msdyn_actual (Actual) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_contractlineinvoiceschedule (Planificare facturi linie contract de proiect) |    msdyn_contractline |    msdyn_contractlineid
msdyn_contractlinescheduleofvalue (Jalon linie contract de proiect) |   msdyn_contractline |    msdyn_contractlineid
msdyn_fact (fact) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_invoicelinetransaction (Detaliu linie factură) | msdyn_invoiceline <br> msdyn_salescontractline | msdyn_invoicelineid <br> msdyn_salescontractlineid
msdyn_journalline (linie de jurnal) |  msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_orderlineresourcecategory (Categorie de resurse linie contract de proiect) | msdyn_salescontractline |   msdyn_contractlineid
msdyn_orderlinetransaction (Detaliu linie contract pentru proiect) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_orderlinetransactioncategory (Categorie de tranzacții linie contract de proiect) |   msdyn_contractline |    msdyn_contractlineid
msdyn_orderlinetransactionclassification (Clasificare de tranzacții linie contract de proiect) |   msdyn_contractline |    msdyn_contractlineid
msdyn_quotelineinvoiceschedule (Planificare factură linie de ofertă) |  msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelineresourcecategory (Categorie de resurse linie de ofertă) |    msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinescheduleofvalue (Jalon linie de ofertă) | msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransaction (Detaliu linie de ofertă) |    msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransactioncategory (Categorie de tranzacții linie de ofertă) |  msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransactionclassification (Clasificare de tranzacții linie de ofertă) |  msdyn_quoteline |   msdyn_quotelineid
SalesOrderDetail (Linie de comandă) | msdyn_quotelineid | msdyn_quoteline 

### <a name="deprecated-custom-views-and-controls"></a>Vizualizări și controale particularizate perimate
Următoarele vizualizări și controale particularizate și artefactele lor corelate au fost perimate.

- Vizualizare posibilitate de tarifare.
- Controalele grilă particularizate pentru afișarea detaliilor liniei de ofertă în pagina **Informații proiect** pentru linia de ofertă.
- Controale grilă particularizate pentru afișarea detaliilor liniei de contract de proiect pe pagina **Informații proiect** pentru linia comenzii de vânzare.

> [!NOTE]
> Pentru lista completă a resurselor perimate, consultați [Resurse web perimate în Project Service Automation v3.x](../developer-guides/web-resources-deprecated-v3.x.md)

## <a name="unified-client-interface-app-module"></a>Modul de aplicație Unified Client Interface
Odată cu introducerea de modulelor de aplicație Unified Client Interface (UCI), intrările de hartă de site PSA au fost eliminate din sistem.  
Funcționalitatea legată de comutarea formularului pentru Oportunitate, Ofertă, Comandă, Factură a fost perimată întrucât nu mai este necesară deoarece modulul de aplicație UCI include numai versiunile PSA ale formularelor.  

Următoarele resurse web au fost perimate:

- msdyn_\SalesDocument\SalesDocumentFormLoader.js
- msdyn_\SalesDocument\PSSalesDocumentCustomFormIds.js

> [!NOTE]
> Pentru lista completă a resurselor perimate, consultați [Resurse web învechite în Project Service Automation v3.x.](../developer-guides/web-resources-deprecated-v3.x.md)




[!INCLUDE[footer-include](../../includes/footer-banner.md)]