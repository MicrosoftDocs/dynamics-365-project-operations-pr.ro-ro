---
title: Scenarii multivalută (versiunea 3. x)
description: Acest subiect furnizează informații despre scenariile multivalută.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 12/26/2018
ms.topic: article
ms.author: rumant
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
ms.openlocfilehash: 2925d431258a150d5830238fb5ff365499b1b440
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8590177"
---
# <a name="multiple-currency-scenarios"></a>Scenarii multivalută

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Microsoft Dynamics 365 are două concepte de valute:

- **Moneda tranzacției** – valuta în care are loc o tranzacție. 
- **Moneda de bază** – valuta instanței Dynamics 365. Această monedă este configurată atunci când o instanță Dynamics 365 este furnizată. Aceasta nu poate fi modificată.

De exemplu, Contoso US a vândut 100 de tricouri unui client din Regatul Unit pentru 15 lire sterline (GBP) fiecare. Următorul tabel arată modul în care această tranzacție este înregistrată în entitatea Produs comandă.

| Produs | Cantitate | Preț unitar | Monedă | Valoare | Curs de schimb | Preț unitar (de bază)| Volum (de bază)|
|---------|----------|----------------|----------|--------|---------------|----------------------|--------------|
| Tricou | 100      | 15             | GBP      | 1500   | 0.94          | 17,25 USD               | 1.725 USD       |

Coloana **Monedă** afișează moneda de tranzacționare, care este valuta în care a avut loc vânzarea. Coloana **Curs de schimb** reprezintă cursul de schimb între moneda de tranzacționare și moneda de bază. Moneda de bază este dolarul american (USD). Această monedă de bază a fost configurată atunci când s-a asigurat accesul la o instanță Dynamics 365.
După arată tabelul, fiecare tranzacție este înregistrată atât în moneda de tranzacționare, cât și în moneda de bază. Dynamics 365 utilizează cursul de schimb valutar pentru a calcula sumele în moneda de bază.

## <a name="project-service-automation-extensions"></a>Extensiile Project Service Automation

Dynamics 365 Project Service Automation influențează moneda de tranzacționare, deoarece tranzacțiile de afaceri au de obicei două aspecte: costuri și vânzări.

Următoarele entități sunt considerate tranzacții de afaceri:

- Detaliu linie de ofertă
- Detaliu linie contract pentru proiect
- Linie estimată
- Linie de jurnal
- Detaliu linie factură
- Real

În fiecare dintre aceste entități, există o înregistrare care reprezintă suma costului sau suma vânzărilor. În ceea ce privește orice entitate Dynamics 365 care are un câmp **Sumă**, fiecare înregistrare include sume atât în moneda de tranzacționare, cât și în moneda de bază. 

PSA extinde conceptul de monedă de tranzacționare pentru cost și vânzări în următoarele moduri:

- Moneda de tranzacționare a costului pentru tranzacții de timp întotdeauna provine din moneda unității organizaționale care deține sau gestionează proiectul. Această unitate organizațională este cunoscută ca unitatea contractantă.
- Moneda de tranzacționare a vânzărilor pentru tranzacțiile de timp și cheltuieli provine întotdeauna din moneda contractului de proiect.
- Moneda de tranzacționare a costului pentru cheltuieli provine din moneda în care a fost creată intrarea de cheltuieli.

## <a name="multiple-currency-scenario"></a>Scenariu multivalută

Această secțiune descrie un exemplu de proiect pe care Contoso UK îl livrează pentru un client denumit Fabrikam, Japonia. Iată cum a fost configurat scenariul:

1. GBP și yenul japonez (JPY) sunt configurate în **Setări** \> **Gestionare firmă** \> **Monede**. 
2. Un cont de client denumit **Fabrikam – Japonia** este configurat, iar JPY este selectat ca monedă pe cont.
3. O unitate organizațională denumită **Contoso UK** este configurată și GBP este selectată ca monedă.
4. Este creat un contract de proiect, în care **Contoso UK** este specificată ca unitatea contractantă și **Fabrikam – Japonia** este specificată drept client.
5. Se creează linii de contract de proiect, pe baza acordurilor de facturare pentru diversele clase de tranzacții din proiect, cum ar fi facturarea pentru timp versus facturarea pentru cheltuieli.
6. Este creat un proiect, în care **Contoso UK** este specificată ca unitatea contractantă. Acest proiect este creat și mapat la liniile de contract de proiect.


În timpul estimării care utilizează detaliile liniei de ofertă, detaliile liniei de contract de proiect sau pe linia de estimare a planificării, sunt întotdeauna create două înregistrări în entitate. O înregistrare este pentru cost, iar cealaltă înregistrare este pentru vânzări.

- În mod implicit, moneda de tranzacționare din înregistrarea costului este setată la moneda unității contractante a proiectului. În acest exemplu, moneda este GBP.
- În mod implicit, moneda de tranzacționare din înregistrarea vânzărilor este setată la moneda contractului de proiect. În acest exemplu, moneda este JPY.

Când sunt create valori reale pentru timp utilizând intrarea de timp sau linia de jurnal, se produce următorul comportament:

- În mod implicit, moneda de tranzacționare din înregistrarea costului este setată la moneda unității contractante a proiectului.
- În mod implicit, moneda de tranzacționare din înregistrarea vânzărilor este setată la moneda contractului de proiect.

Când sunt create valori reale pentru cheltuieli utilizând intrarea de cheltuieli sau linia de jurnal, se produce următorul comportament:

- Aveți posibilitatea să înregistrați suma cheltuielilor în orice monedă. Selectați moneda utilizând selectorul de valută de pe pagina **Intrare cheltuieli** sau de pe pagina **Linie de jurnal**. În mod implicit, moneda de tranzacționare pentru înregistrarea costului este setată la moneda din intrarea de cheltuieli. 
- În mod implicit, moneda de tranzacționare pentru înregistrarea vânzărilor este moneda contractului de proiect. Pentru a seta această monedă, sistemul convertește mai întâi suma tranzacției în moneda pe care utilizatorul a introdus-o în moneda de bază. Apoi, acesta transformă suma în moneda contractului de proiect. 

### <a name="computing-roll-ups-when-project-actuals-are-recorded-in-multiple-transaction-currencies"></a>Calcularea cumulărilor atunci când valorile reale ale proiectului sunt înregistrate în mai multe monede de tranzacționare

Dynamics 365 gestionează automat cumulări de sume în monede diferite. Iată un exemplu.

| Clasă de tranzacții | Tipul tranzacției| Dată   | Resursă | Categorie tranzacție | Cantitate | Preț unitar | Valoare      | Curs de schimb | Volum în moneda de bază |
|-------------------|------------------|--------|----------|----------------------|----------|--------------|-------------|---------------|----------------|
| Time              | Vânzări nefacturate   | 14 iun. | Daniel  |                      | 8 ore    | 20.000 JPY    | 160.000 JPY | 123           | 1.300,81 USD    |
| Time              | Vânzări nefacturate   | 15 iun. | Daniel  |                      | 8 ore    | 20.000 JPY    | 160.000 JPY | 123           | 1.300,81 USD    |
| Cheltuială           | Vânzări nefacturate   | 16 iun. | Daniel  | Hotel                | 1 ea     | 250 EUR      | 250 EUR     | 0.94          | 265,95 USD     |
| Cheltuială           | Vânzări nefacturate   | 17 iun. | Daniel  | Închirieri auto           | 1 ea     | 150 EUR      | 150 EUR     | 0.94          | 159,57 USD     |

Pentru a calcula valoarea totală a vânzărilor nefacturate din proiect, aveți posibilitatea să creați un câmp de cumul pentru câmpul **Sumă** pe toate valorile reale de vânzări nefacturate corelate. Câmpul de cumul este o construcție a Dynamics 365 care permite formule rapide pe înregistrări corelate.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
