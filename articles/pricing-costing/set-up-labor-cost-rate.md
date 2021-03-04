---
title: Configurarea tarifelor de cost pentru muncă
description: Acest subiect oferă informații despre modul de configurare al ratelor de cost pentru forța de muncă în Project Operations
author: rumant
manager: Annbe
ms.date: 10/12/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 697129b65f53359615ea537fe135d657748dd909
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/31/2020
ms.locfileid: "4180612"
---
# <a name="set-up-labor-cost-rates"></a>Configurarea tarifelor de cost pentru muncă

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_


Fiecare listă de prețuri are un set de rate ale forței de muncă (prețuri de rol) care se aliniază la conținutul și efectivitatea datei listei de prețuri.

1. Creați o listă de prețuri și pe fila **Prețul rolului**, în subgrilă, selectați **Rol nou**.
2. Pe pagina **Creare rapidă**, selectați rolul și unitatea de organizare.
3. Introduceți orice altă informație de câmp necesar.

Tabelul următor include câteva dintre câmpurile care sunt importante atunci când se creează rate ale forței de muncă pe o listă de prețuri de cost.

| Câmp | Locație | Descriere | Impactul din aval |
| --- | --- | --- | --- |
| Rol | Fila **General** și pagini **Creare rapidă** | Selectați rolul căruia i se aplică rata de cost. | Rolul din estimarea de intrare sau real va fi asortat cu această linie pentru a stabili implicit costul rolului. |
| Firmă de resurse | Fila **General** și pagini **Creare rapidă** | Selectați entitatea juridică căreia i se atribuie rolul. De exemplu, un dezvoltator din Fabrikam India sau un dezvoltator din Fabrikam SUA. | Firma de resurse din estimarea de intrare sau real va fi asortat cu această linie pentru a stabili implicit rata de cost a rolului. |
| Unitate de finanțare | Fila **General** și pagini **Creare rapidă** | Selectați unitatea organizațională sau divizia companiei din care va fi utilizat acest rol. De exemplu, un dezvoltator din divizia Robotics din Fabrikam India sau un dezvoltator din divizia Software din Fabrikam USA. | Unitatea de resurse din estimarea de intrare sau real va fi asortat cu această linie pentru a stabili implicit costul rolului. |
| Preț | Fila **General** și pagini **Creare rapidă** | Configurați rata de cost pentru rolul, compania de resurse și combinația de unități de resurse. De exemplu, un dezvoltator din Fabrikam India costă 1000 INR sau un dezvoltator din Fabrikam SUA costă 150 USD. | Prețul este rata de cost implicită pentru costul pe unitate al estimării primite sau al liniei reale pentru clasa tranzacției **Timp**. |
| Monedă | Fila **General** și pagini **Creare rapidă** | În mod implicit, valoarea monedei provine din moneda din antetul listei de prețuri de cost, dar poate fi anulată. De exemplu, un dezvoltator din Fabrikam India costă 1000 INR. Un dezvoltator din Fabrikam SUA costă 150 USD. | Moneda este implicită pentru costul pe unitate al estimării primite sau al liniei reale de cost pentru clasa tranzacției **Timp**. Pe o estimare a proiectului, valoarea monedei este convertită în moneda proiectului și afișată în vizualizarea în timp a estimării. |
| Planificare unitate | Fila **General** și pagini **Creare rapidă** | Programul de unitate este implicit Timp și nu poate fi modificat pe entitatea cu preț de rol, deoarece este utilizat tarifele expres pe unități de timp. | Nu există niciun impact în aval. |
| Unitate | Fila **General** și pagini **Creare rapidă** | În mod implicit, valoarea vine de la câmpul **Unitate de timp** pe antetul listei de prețuri de cost. Valoarea poate fi anulată. De exemplu, un dezvoltator din Fabrikam India costă 1000 INR de **Zi de India**. Un dezvoltator din Fabrikam SUA costă 150 USD per **Ziua SUA**. | Sistemul utilizează sistemul de unități și conversia în unități de bază pentru a calcula un cost pe unitate pentru a calcula prețul implicit pe unitate pe o estimare primită sau pe o linie reală. De exemplu, o estimare este pentru 10 **Zile de India** în valoare de muncă pentru un dezvoltator din India și unitatea, **Zi de India** este definit ca 10 ore. Atunci când calculează acea linie estimativă, aplicația calculează costul unitar pe estimare ca: 1000 INR/10 ore = 100 INR pe oră, care este convertit în USD și afișat ca cost unitar pe pagina **Estimări ale proiectului**. |

## <a name="transfer-pricing-and-costs-for-resources-outside-of-your-division-or-legal-entity"></a>Prețurile de transfer și costurile pentru resurse în afara diviziei sau persoanei juridice

În companiile bazate pe proiect, este un lucru comun utilizarea angajaților din diferite entități juridice sau divizii pe proiecte. Un proiect poate fi executat de o singură persoană juridică, dar angajații sau consultanții care lucrează la proiect ar putea proveni de la aceeași persoană juridică sau de la una diferită, sau poate exista o combinație a ambelor. În Dynamics 365 Project Operations, entitatea juridică care deține livrarea proiectului este **Compania deținătoare** iar diviziunea care deține livrarea este **Unitatea Contractantă**. Alte persoane juridice care furnizează resurse sunt **Companii de resurse** iar diviziile care furnizează resurse sunt **Unități de resurse**. În majoritatea țărilor, companiilor li se cere să se asigure că entitatea juridică sau divizia de resurse, taxează compania deținătoare și unitatea contractantă pentru utilizarea resurselor.

De exemplu, corporația Fabrikam trebuie să se asigure că Fabrikam India-Robotics a negociat un card de tarif cu Fabrikam US-Robotics sau Fabrikam UK-Robotics.

Un dezvoltator de la Fabrikam India-Robotic taxează $100 când este împrumutat lui Fabrikam US-Robotics și $150 când este împrumutat Fabrikam U-Robotics.

### <a name="set-up-costs-for-outside-resources"></a>Stabiliți costurile pentru resursele externe

1. Creați o listă de prețuri de cost numită, *Tarifele de cost Fabrikam SUA-Robotics* și setați un interval efectiv de dată.
2. În lista de prețuri de cost, setați tarifele folosind informațiile din tabelul următor. 

| Rol | Firmă de resurse | Unitate de finanțare | Rată cost |
| --- | --- | --- | --- |
| Dezvoltator | Fabrikam India | Fabrikam India-Robotics | $100 |
| Dezvoltator | Fabrikam Filipine | Fabrikam Philippines-Robotics | $90 |
| Dezvoltator | Fabrikam US | Fabrikam US-Robotics | $150 |

3. Atașați această listă de prețuri la unitatea organizațională Fabrikam US-Robotics.

### <a name="set-up-transfer-pricing-for-a-resource-in-the-appropriate-currency"></a>Configurați prețurile de transfer pentru o resursă în moneda corespunzătoare 

În Project Operations, prețul resurselor poate fi configurat în orice monedă. Valuta este implicită la antetul listei de prețuri, dar poate fi modificată.

Folosind exemplul pentru configurarea prețului de transfer, informațiile ar putea fi modificate în:

Corporația Fabrikam trebuie să se asigure că Fabrikam India-Robotics a negociat un card de tarif cu Fabrikam US-Robotics sau Fabrikam UK-Robotics.

Un dezvoltator de la Fabrikam India-Robotics taxează 5000 INR când este împrumutat lui Fabrikam US-Robotics și 5500 INR când este împrumutat Fabrikam UK-Robotics.

În lista de prețuri pentru Fabrikam US-Robotics, tarifele de cost pot fi exprimate ca:

| Rol | Firmă de resurse | Cost |
| --- | --- | --- |
| Dezvoltator | Fabrikam India | 5000 INR |
| Dezvoltator | Fabrikam US | 115 USD |

În lista de prețuri pentru Fabrikam UK-Robotics, tarifele de cost pot fi exprimate mai jos:

| Rol | Firmă de resurse | Cost |
| --- | --- | --- |
| Dezvoltator | Fabrikam India | 5500 INR |
| Dezvoltator | Fabrikam UK | 115 GBP |

Lista prețurilor de cost poate oferi rate ale forței de muncă în mai multe valute. Atunci când se generează o estimare a costului proiectului, Project Operations vor converti aceste rate de cost în moneda proiectului și le vor afișa utilizatorului. Când se aprobă o înregistrare temporală și se creează un cost real, costul real este evaluat în moneda liniei de preț de rol corespunzătoare din lista de prețuri de cost. Costurile reale pentru timpul unui singur proiect pot fi înregistrate în mai multe valute. Cu toate acestea, atunci când rulați sau rezumați costurile reale ale forței de muncă la nivelul proiectului, Operațiunile proiectului vor converti toate sumele costurilor forței de muncă în moneda proiectului, pe care utilizatorul o poate vizualiza.


[!INCLUDE[footer-include](../includes/footer-banner.md)]