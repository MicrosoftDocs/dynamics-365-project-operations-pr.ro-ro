---
title: Ce este nou sau schimbat în Project Service Automation versiunea actualizată 27, V3
description: Acest subiect listează caracteristicile și corecțiile care sunt disponibile în Project Service Automation V3, versiunea actualizată 27, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/12/2021
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
ms.openlocfilehash: e6dd514e573d2ee977010311cd7f7fcb201abc27
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999236"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-27-v3"></a>Ce este nou sau schimbat în Project Service Automation versiunea actualizată 27, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Suntem încântați să anunțăm cea mai recentă actualizare pentru aplicația Project Service Automation pentru Dynamics 365. Această versiune include câteva îmbunătățiri importante ale calității, performanței și utilizabilității. Această versiune este compatibilă cu Dynamics 365 9.x. Pentru a actualiza această versiune, accesați Centrul de administrare pentru Dynamics 365, pagina de soluții online pentru a instala actualizarea. Pentru informații suplimentare, consultați: [Instalarea, actualizarea sau eliminarea unei soluții preferate](/power-platform/admin/install-remove-preferred-solution).

Acest subiect listează caracteristicile și corecțiile care sunt noi sau modificate pentru Project Service Automation V3, versiunea actualizată 27. Această versiune are un număr de V3.10.45.98 și este, în general, disponibilă printr-o auto-actualizare în ianuarie 2021.

## <a name="update-release-27"></a>Lansarea de actualizări 27

### <a name="bug-fixes"></a>Remedieri de erori

**General**

S-au remediat următoarele probleme:

- Jurnalele generate de inserturi în Project Service Automation nu au fost setate pe ștergere automată.
- Actualizarea automată eșuează deoarece soluția Project Service Automation conține un NavBarArea vechi și un element de titlu.

**Timp și cheltuială**

S-au remediat următoarele probleme:

- Grila **Intrare de timp** afișează date incorecte pentru comportamentul de dată **Independent de zona orară**.
- Grila **Intrare de timp** crează timpul incorect pentru comportamentul de dată **Independent de zona orară**.
- Căutarea sarcinilor nu se limitează la proiectul selectat de pe pagina **Editați introducerea timpului**.
- Aprobarea timpului pentru intrările de timp care nu fac parte din proiect este blocată pentru că sistemul caută un rol de aprobator de proiect.
- Intrările corecte din Valori reale afișează un mesaj de eroare incorect.
- Când o sarcină conține o valoare nulă pentru costul real și totalurile proiectului sunt actualizate, apare următoarea eroare, „Cheia dată nu este prezentă în dicționar”.
- În cazuri specifice, filtrele **A se grupa după** de pe fila **Estimare proiect** nu afișează estimările cheltuielilor.
- Intervalul **Ora oficială de vară** nu este corect pentru intrările de timp.

**Gestionare de proiect**

S-au remediat următoarele probleme:

- Îmbunătățiri în cache, care îmbunătățesc performanțele legate de încărcarea paginii **Proiect**.
- Regulă de afaceri învechită care împiedică finalizarea sarcinilor proiectului.
- Configurația programului de completare Microsoft Project nu respectă calendarul programului de completare, rezultând cerințe incorecte de resurse.
- Crearea proiectelor din șabloane setează incorect datele de atribuire și împiedică posibilitatea de a genera cerințe de resurse.
- Utilizatorul nu poate accesa opțiunile **Categorie**, **Descriere**, **Stare** folosind tastatura.
- Valorile reale de vânzare ale proiectului nu includ taxele și valorile vânzărilor de materiale.
- Agregarea de vânzări reale și costuri reale are loc în mod incorect cu cursuri de schimb diferite.
- Descrierea din **Șablon implicit pentru ora de lucru** este derutantă.
- Indentarea unei sarcini nu elimină **Categorie** în interfața cu utilizatorul până când este reîmprospătată.
- Nu este permisă validarea pentru a asigura mutarea unui proiect după data de încheiere.

**Sales**

S-au remediat următoarele probleme:

- O excepție de referință nulă este generată pe o linie de ofertă a proiectului deoarece opțiunea **Import din estimarea proiectului** este vizibilă când un proiect nu a fost selectat.
- Următoarea eroare, „Referința obiectului nu este setată la o instanță a unui obiect” apare la închiderea unei oferte drept **Câștigat**.
- Starea de ajustare nu este setată în timpul unei inversări reale în timp ce deconectați un proiect de o linie de contract.
- Când atât Dynamics 365 Field Service cât și Project Service Automation sunt instalate, opțiunile **Blocare prețuri** și **Folosiți prețurile actuale** nu sunt afișate în același timp pe pagina **Factură**.
- Pentru limba japoneză, există o traducere inconsistentă cu alte pagini bazate pe calendar.
- Opțiunile **Activați** și **Dezactivați** au fost eliminate din entitățile **Asociere listă de prețuri** în Project Service Automation.


[!INCLUDE[footer-include](../includes/footer-banner.md)]