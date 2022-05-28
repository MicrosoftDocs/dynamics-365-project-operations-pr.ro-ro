---
title: Ce este nou sau schimbat în Project Service Automation versiunea actualizată 28, V3
description: Acest subiect listează caracteristicile și corecțiile care sunt disponibile în Project Service Automation V3, versiunea actualizată 28, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/26/2021
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
ms.reviewer: johnmichalak
ms.openlocfilehash: b3afeaf131c8bab25e1ed3a9eb3b41cb3059f711
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8586819"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-28-v3"></a>Ce este nou sau schimbat în Project Service Automation versiunea actualizată 28, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Suntem încântați să anunțăm cea mai recentă actualizare pentru aplicația Project Service Automation pentru Dynamics 365. Această versiune include câteva îmbunătățiri importante ale calității, performanței și utilizabilității. Această versiune este compatibilă cu Dynamics 365 9.x. Pentru a actualiza această versiune, accesați Centrul de administrare pentru Dynamics 365, pagina de soluții online pentru a instala actualizarea. Pentru informații suplimentare, consultați: [Instalarea, actualizarea sau eliminarea unei soluții preferate](/power-platform/admin/install-remove-preferred-solution).

Acest subiect listează caracteristicile și corecțiile noi sau modificate pentru Project Service Automation V3, Actualizare versiunea 28 Această versiune are un număr de compilare de V3.10.46.32 și este, în general, disponibilă prin auto-actualizare în ianuarie 2021.

## <a name="update-release-28"></a>Lansarea de actualizări 28

### <a name="bug-fixes"></a>Remedieri de erori

**Timp și cheltuială**

S-au remediat următoarele probleme:

- Utilizatorii pot folosi funcția **Editare în bloc** pentru a actualiza intrările de timp care au fost aprobate și trimise.

**Gestionare de proiect**

S-au remediat următoarele probleme:

- În cazurile în care sarcina GUID este interpretat ca un număr, sarcinile nu pot fi deschise pentru editare folosind comanda **Editați sarcina** de pe panglica de la pagina **Structura defalcării lucrului**.

**Sales**

S-au remediat următoarele probleme:

- O excepție de referință nulă este generată atunci când insertul **ObținețiEstimăriPentruProiect** este invocat.
- Comanda **Marcați gata de facturare** pe grila de repere actualizează doar parțial atributele, cu excepția atributului **Stare factură**, care este actualizat.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
