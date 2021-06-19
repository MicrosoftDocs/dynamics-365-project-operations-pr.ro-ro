---
title: Ce este nou sau schimbat în Project Service Automation versiunea actualizată 22, V3
description: Acest subiect listează caracteristicile și corecțiile care sunt disponibile în Project Service Automation V3, versiunea actualizată 22, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 07/28/2020
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
ms.openlocfilehash: 5694aa27afe7618cfca6b27444393634a9686600
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006571"
---
# <a name="project-service-automation-update-release-22-v3"></a>Project Service Automation, versiunea actualizată 22, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Suntem încântați să anunțăm cea mai recentă actualizare pentru aplicația Project Service Automation pentru Dynamics 365. Această versiune include câteva îmbunătățiri importante ale calității, performanței și utilizabilității. Această versiune este compatibilă cu Dynamics 365 9.x. Pentru a actualiza această versiune, accesați Centrul de administrare pentru Dynamics 365, pagina de soluții online pentru a instala actualizarea. Pentru informații suplimentare, consultați: [Instalarea, actualizarea sau eliminarea unei soluții preferate](/power-platform/admin/install-remove-preferred-solution).

Acest subiect listează caracteristicile și corecțiile care sunt noi sau modificate pentru Project Service Automation V3, versiunea actualizată 22. Această versiune are un număr de versiune V 3.10.33.48 și este disponibil în general printr-o autoactualizare în iunie 2020.

## <a name="update-release-22"></a>Lansarea de actualizări 22

### <a name="bug-fixes"></a>Remedieri de erori



**Timp și cheltuială**

S-au remediat următoarele probleme:

- **Intrările de timp** nu sunt adăugate automat în planificarea de intrări de timp după import.
- Selectorul de date grilă **Intrare de timp** nu recunoaște setările regionale ale unui utilizator.

**Gestionarea resurselor**

S-au remediat următoarele probleme:

- În modul manual, modificările la contururile **Alocarea resurselor** nu sunt recunoscute când se generează **Cerințe de resurse**.
- **Solicitări de resurse** nu acceptă stări de solicitare personalizate.

**Gestionare de proiect**

S-au remediat următoarele probleme:

- Utilizând dublu clic pe EstimateGridControl nu va analiza corect numerele formatului olandez.
- Orele alocate nu se actualizează corect atunci când alocările sunt schimbate folosind suplimentul client de desktop Microsoft Project.
- Rețelele de urmărire și estimare a proiectului afișează cod de monedă de vânzare incorect atunci când moneda contractului este diferită de moneda clientului și organizația este configurată pentru a afișa coduri valutare în loc de simboluri valutare.
- Data de încheiere a unui membru al echipei va adăuga o zi dacă programul orelor de lucru este de 24 de ore pe zi.
- Pe Planificarea de proiect, adăugarea unei categorii de tranzacții la o sarcină nu declanșează salvarea automată.
- Următoarea eroare este afișată la adăugarea unui membru al echipei la șablonul de proiect: „Cerințele de resurse nu pot fi asociate cu șabloanele de proiect”. 
- Scriptul de regulă al panglicii „msdyn.Approval.CanApproveOrReject” afișează o eroare de expirare.

**Sales**

S-au remediat următoarele probleme:

- Mesaj de eroare de validare care nu este afișat atunci când este selectată o listă de prețuri de costuri în căutarea Listă de prețuri în formularul/entitatea „Ofertă nouă de preț de proiect”.
- Închiderea ofertei ca câștigată nu navighează la contractul creat dacă un BPF atașat la ofertă se află în etapa finală.
- Reversul **Vânzări fără factură** este legat de costul inițial atunci când este înregistrată o intrare în timp.
- După selectarea butonului **Confirmare**, starea facturii nu se modifică la **Confirmat** cu excepția cazului în care factura este actualizată.


[!INCLUDE[footer-include](../includes/footer-banner.md)]