---
title: Resurse de pe linia de subcontract
description: Acest subiect explică modul de precizare a resurselor dedicate oferite de furnizor pentru o anumită linie de subcontract pentru timp.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4a929b985a51ab49d3e34ce4a5c277af4c05c216
ms.sourcegitcommit: d507a75a19c992a9421e4f3605162a2faa84a445
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 09/27/2021
ms.locfileid: "7558472"
---
# <a name="subcontract-line-resources"></a>Resurse de pe linia de subcontract

[!include [banner](../../includes/dataverse-preview.md)]

_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_

În Dynamics 365 Project Operations, un furnizor poate indica resurse care vor fi utilizate pentru a furniza capacitatea resurselor achiziționate pe linia de subcontract pentru timp.

## <a name="create-subcontract-line-resources"></a>Crearea de resurse pentru linia de subcontract

Pentru a crea resurse pentru linia de subcontract, parcurgeți pașii următori.

1. Pe panoul de navigare, selectați **Subcontracte**, apoi deschideți subcontractul cu care doriți să lucrați.
2. Deschideți linia de subcontract pentru timpul pe care doriți să specificați resursele furnizorului.
3. Pe fila **Resurse linie de subcontract**, în sub-grilă, selectați **+ Nouă resursă linie subcontract**.
4. Pe pagina **Resursă nouă de linie de subcontractare**, introduceți informațiile necesare și apoi selectați **Salvați și închideți**.

Tabelul următor explică câmpurile din resursa liniei de subcontract.

| Câmp | Descriere | Impact funcțional |
| ----- | ----------- | ----------------- |
| Resursă ce se poate rezerva | Selectați o resursă care poate fi rezervată de tip **Lucrător contractual** pe care doriți să o utilizați ca resursa de pe linia de subcontract.| Dacă nu ați creat o resursă care poate fi rezervată pentru lucrătorul contractual, lăsați acest câmp gol. O resursă care poate fi rezervată va fi creată atunci când salvați înregistrarea.  |
| Contactați | Puteți crea resursa dvs. de subcontractare dintr-un contact existent. Utilizați căutarea pentru a vizualiza lista contactelor active din sistem. Selectați un contact pentru furnizorul acestui subcontract. Dacă contactul pe care l-ați selectat nu este un contact valid pentru furnizorul din subcontract, înregistrarea resurselor liniei de subcontract nu va fi salvată.| Dacă nu există o resursă rezervabilă pentru contactul selectat, sistemul creează o resursă rezervabilă pentru contactul selectat înainte de a crea resursa liniei de subcontract. |
| Utilizator | Puteți crea o resursă de linie de subcontractare selectând un utilizator activ. Utilizați căutarea pentru a vizualiza lista utilizatorilor activi din sistem.| Dacă nu există o resursă rezervabilă pentru utilizatorul selectat, sistemul creează o resursă rezervabilă pentru utilizatorul selectat înainte de a crea resursa liniei de subcontract. |
| Data inițială | Data la care va începe misiunea lucrătorului subcontractat.| Dacă această resursă este rezervată pentru o perioadă care se încadrează înainte de acest interval de date, va apărea un avertisment. |
| Data de sfârșit | Data la care se termină misiunea lucrătorului subcontractat.| Dacă această resursă este rezervată pentru o perioadă care se încadrează după acest interval de timp, va apărea un avertisment. |
| Efort | Numărul total de ore de efort pe care lucrătorul contractual le va petrece pe această linie de subcontractare.| Dacă această resursă este rezervată dincolo de efortul alocat acestui subcontract, va apărea un avertisment. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
