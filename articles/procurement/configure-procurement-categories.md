---
title: Utilizați categorii de achiziții cu comenzile de achiziție de proiect și facturile furnizorilor în așteptare
description: Acest subiect descrie modul de configurare a categoriilor de achiziții care pot fi utilizate cu comenzile de achiziție de proiect și facturile furnizorilor în așteptare.
author: sigitac
ms.date: 04/07/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: ee68d7906cb0c887c19a32363ec7fda547cb74bd
ms.sourcegitcommit: 9916f536a71b6a0078297402564ac79308ec6890
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 04/18/2022
ms.locfileid: "8613363"
---
# <a name="use-procurement-categories-with-project-purchase-orders-and-pending-vendor-invoices"></a>Utilizați categorii de achiziții cu comenzile de achiziție de proiect și facturile furnizorilor în așteptare

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

Profesioniștii în achiziții pot crea și menține cataloage ale articolelor și serviciilor care pot fi utilizate în comenzile de achiziție ale proiectelor și în facturile furnizorilor în așteptare. [Cataloage de achiziții](/dynamics365/supply-chain/procurement/procurement-catalogs) vă oferă o modalitate ușoară de a clasifica achizițiile fără a fi nevoie să configurați și să utilizați un catalog de produse lansat. Fiecare categorie de achiziții poate fi mapată la o categorie de proiect pentru timp, cheltuieli sau tranzacții cu articole. După ce o factură de furnizor în așteptare care folosește o categorie de achiziții este înregistrată, sistemul va crea timp, cheltuieli sau date reale ale proiectului, tranzacții de proiect și intrări în registrul secundar.

## <a name="minimum-version-requirements"></a>Cerințe minime pentru versiune

Următoarele versiuni sunt necesare pentru a utiliza categoriile de achiziții cu comenzile de achiziție pentru proiecte pentru Microsoft Dynamics 365 Project Operations scenarii neaprovizionate/bazate pe resurse:

- Operațiuni de proiect Dataverse versiunea soluției 4.41.0.45 sau ulterioară
- Mediul Finance and Operations versiunea 10.0.26 sau o versiune ulterioară

## <a name="run-dual-write-maps-for-procurement-category-support"></a>Rulați hărți cu scriere duală pentru suport pentru categoriile de achiziții

Asigurați-vă că maparea pentru **Proiect Operations integrare proiect furnizor linie factură export entitate msdyn\_ proiectevendorinvoicelines** folosește versiunea 1.0.0.4 sau o versiune ulterioară.

## <a name="enable-the-feature-key-for-procurement-categories"></a>Activați cheia de funcții pentru categoriile de achiziții

Urmați acești pași pentru a activa funcționalitatea de utilizare a categoriilor de achiziții cu comenzile de achiziție de proiect.

1. În Dynamics 365 Finance, deschideți **Managementul caracteristicilor** spațiu de lucru.
1. În lista de caracteristici, găsiți **Utilizați categoriile de achiziții în Operațiuni de proiect pentru scenarii bazate pe resurse/ne-aprovizionate** caracteristică, apoi selectați **Permite**.

> [!IMPORTANT]
> Ca o condiție prealabilă, trebuie să activați și **Activați facturile furnizorilor în așteptare pentru operațiunile de proiect pentru scenariile bazate pe resurse/nestoc** caracteristică.

## <a name="map-project-categories-in-the-procurement-category-hierarchy"></a>Hartați categoriile de proiecte în ierarhia categoriilor de achiziții

Urmați acești pași pentru a mapa categoriile de proiecte cu categoriile de achiziții în **Categoria de achiziții** ierarhie:

1. Mergi la **Achiziții și aprovizionare \> Categorii de achiziții**.
1. Selectați **Editați ierarhia categoriilor**.
1. Selectați nodul dorit de ierarhie a categoriilor și apoi, pe **Atribuiți categorii de proiecte** fila, asociați nodul cu categoria de proiect din **Timp**, Cheltuieli** sau **,Proiect articol** categorie (adică **Timp implicit** sau **Implicit-Cheltuieli** categorie).
1. Selectați **Salvare**.
1. Închideți pagina.

> [!NOTE]
> Maparea unei categorii de achiziții la o categorie de proiect este opțională. Dacă o categorie de achiziție nu este mapată, sistemul va folosi valoarea care este setată în **Articol** câmp în **Valorile implicite ale categoriei de proiect** secțiunea despre **Operațiuni de proiect pe Dynamics 365 Implicarea clienților** fila din **Management de proiect și parametri contabili** pagină.
