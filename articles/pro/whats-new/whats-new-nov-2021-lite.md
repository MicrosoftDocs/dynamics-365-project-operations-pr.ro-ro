---
title: Noutăți noiembrie 2021 – implementare Project Operations lite
description: Acest articol oferă informații despre actualizările de calitate care sunt disponibile în versiunea din noiembrie 2021 de implementare a Project Operations lite.
author: sigitac
ms.date: 11/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 947e7f6183ddeef3ab9a88d140331956bbcf23bd
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913819"
---
# <a name="whats-new-november-2021---project-operations-lite-deployment"></a>Noutăți noiembrie 2021 – implementare Project Operations lite

_Se aplică pentru: implementare simplificată - înțelegere la emiterea facturii proforme_

Acest articol se aplică următoarelor componente și versiuni de Microsoft Dynamics 365 Project Operations:

- Project Operations într-un mediu Dataverse versiunilre 4.26.0.145, 4.26.0.148, 4.26.0.150, 4.26.0.155
  
## <a name="features-included-in-this-release"></a>Caracteristicile incluse în această versiune

Următoarele caracteristici sunt incluse în această versiune:

- Interfețele de Tablou de planificare a aplicațiilor (API) pentru planificarea proiectelor acceptă acum capacitatea de a crea și de a șterge Pachetele de proiect

## <a name="quality-updates"></a>Actualizări de calitate

### <a name="project-operations-in-dataverse"></a>Project Operations în Dataverse

| Zonă de caracteristici | Număr de referință | Actualizare de calitate |
| --- | --- | --- |
| Facturarea și stabilirea prețurilor | 2358236 | Corectarea facturii trebuie să permită corecții care au linii de preț zero. |
| Gestionarea de resurse | 2410072 | Permite configurarea unei resurse care este atribuită sarcinii ca manager de proiect. |
| Facturarea și stabilirea prețurilor | 2430234 | Remediați o problemă de calcul al performanței costurilor. |
| Timp și cheltuială | 2436978 | Permiteți introducerea timpului în format hh:mm. |
| Facturarea și stabilirea prețurilor | 2448623 | Permiteți actualizarea listelor de prețuri după ce sunt asociate cu o unitate organizațională. |
| Timp și cheltuială | 2460396 | Permiteți ștergerea unei intrări de timp prin ștergerea celulei. |
| Facturarea și stabilirea prețurilor | 2467386 | Permiteți ștergerea unui proiect care are o sarcină, chiar și atunci când sarcina este asociată cu o ofertă câștigată. |
| Timp și cheltuială | 2461744 | Vizualizarea **Aprobarea mea eșuată** conține numai aprobări de proiecte în starea de **Trimis**. |
| Timp și cheltuială | 2464082 | Eliminați legătura de la aprobările de proiect la setul de aprobare atunci când se potrivește o stare țintă. |
| Timp și cheltuială | 2468108 | Lucrarea de programare nu trebuie să seteze o stare **Prelucrare** pentru setul de aprobare. |
| Timp și cheltuială | 2471503 | Ștergeți seturile de aprobare vechi de șapte zile. |
| Facturarea și stabilirea prețurilor | 2480687 | Referința liniei de ofertă nu trebuie eliminată atunci când este creat un jalon al liniei de ofetă. |
