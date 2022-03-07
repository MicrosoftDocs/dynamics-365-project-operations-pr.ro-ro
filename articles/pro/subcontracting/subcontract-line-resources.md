---
title: Resurse de pe linia de subcontract
description: Acest subiect explică modul de precizare a resurselor dedicate oferite de furnizor pentru o anumită linie de subcontract pentru timp.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 48440f82170bde7f0a0a45f8f9849d688b232949
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323386"
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
4. Pe pagina **Nou jalon linie subcontract**, introduceți informațiile necesare și apoi selectați **Salvare și închidere**.

Tabelul următor explică câmpurile din resursa liniei de subcontract.

| Câmp |  Descriere |
| ----- | ------------ |
| Resursă ce se poate rezerva | Selectați o resursă rezervabilă de tip „Lucrător contractual” pe care doriți să o utilizați ca resursă pe linia de subcontract. Dacă nu ați creat încă o resursă rezervabilă pentru lucrătorul contractual, lăsați acest câmp gol. O resursă rezervabilă este creată atunci când salvați înregistrarea.  |
| Contact | În cazul în care câmpul **Resurse rezervabile** este gol, vă puteți crea resursa de linie de subcontract de la un contact existent. Utilizați căutarea pentru a vizualiza lista contactelor active din sistem. Selectați un contact pentru furnizorul acestui subcontract. Contactul pe care îl selectați este validat atunci când salvați înregistrarea. Dacă contactul pe care l-ați selectat nu este un contact valid, înregistrarea dvs. nu se va salva. Dacă nu există o resursă rezervabilă pentru contactul selectat, sistemul creează o resursă rezervabilă pentru contactul selectat înainte de a crea resursa liniei de subcontract. |
| Utilizator | În cazul în care câmpul **Resursă rezervabile** este gol, vă puteți crea o resursă de linie de subcontract prin selectarea unui utilizator activ. Utilizați căutarea pentru a vizualiza lista utilizatorilor activi din sistem. Dacă nu există o resursă rezervabilă pentru utilizatorul selectat, sistemul creează o resursă rezervabilă pentru utilizatorul selectat înainte de a crea resursa liniei de subcontract. |
| Data inițială | Data la care va începe misiunea lucrătorului subcontractat. Dacă această resursă este rezervată pentru o perioadă care se încadrează înainte de acest interval de date, va apărea un avertisment. |
| Data de sfârșit | Data la care se termină misiunea lucrătorului subcontractat. Dacă această resursă este rezervată pentru o perioadă care se încadrează după acest interval de timp, va apărea un avertisment. |
| Efort | Numărul total de ore de efort pe care lucrătorul subcontractat le va petrece pe această linie de subcontract. Dacă această resursă este rezervată peste efortul la care este alocată în acest subcontract, va apărea un avertisment. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
