---
title: Ce este nou sau schimbat în Project Service Automation versiunea actualizată 14, V3
description: Acest subiect oferă informații despre ceea ce este nou și schimbat în Project Service Automation versiunea 14 V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/29/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: f9347741d8dae2c9a810bb5b3a32d4d6c0a628ed
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147173"
---
# <a name="project-service-automation-update-release-14-v3"></a>Project Service Automation, versiunea actualizată 14, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Suntem încântați să anunțăm cea mai recentă actualizare pentru aplicația Dynamics 365 Project Service Automation (PSA). Această versiune include câteva îmbunătățiri importante ale calității, performanței și utilizabilității. Această versiune este compatibilă cu Dynamics 365 9.x. Pentru a actualiza această versiune, accesați Centrul de administrare pentru Dynamics 365 online și accesați pagina cu soluții pentru a instala actualizarea. Pentru informații suplimentare, consultați: [Instalarea, actualizarea sau eliminarea unei soluții preferate](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Acest subiect listează caracteristicile și corecțiile care sunt noi sau modificate pentru PSA V3, Update Release 14. Această versiune are un număr de V3.10.4.21 și este disponibilă în următoarea planificare:

- **Disponibilitate generală (autoactualizare):** ianuarie 2020
- **Actualizare automată:** februarie 2020

## <a name="update-release-14"></a>Lansarea de actualizări 14

### <a name="enhancements"></a>Îmbunătățiri

- Sales

     - Valorile câmpului personalizate din **Detalii despre linie de ofertă** sunt copiate în **Detalii linie contract contract** când o ofertă este actualizată la **Închisă drept câștigată**.
     - Proiectele confirmate pot fi **Închise ca pierdute**.

- Gestionarea de resurse

     - Când extindeți rezervările, utilizatorii vor primi o casetă de dialog de confirmare pentru a rezuma rezultatele rezervării și pentru a oferi un link către Menținerea rezervărilor.


### <a name="bug-fixes"></a>Remedieri de erori

- Timp și cheltuială

     - Remediat: experiența îmbunătățită a utilizatorului atunci când acesta nu a selectat nicio înregistrare care trebuie corectată.

- Gestionarea de resurse

     - Remediat: Rezervarea unei resurse de mai multe ori revărsă numele resursei rezervabile.

- Sales

     - Remediat: prețul total de vânzare nu este calculat până când utilizatorul introduce și un preț de cost pentru estimările cheltuielilor la un proiect.
     - Remediat: Închiderea unei oferte ca **Câștigată** eșuează dacă contractul de proiect asociat nu se află într-o stare de **Schiță**.

