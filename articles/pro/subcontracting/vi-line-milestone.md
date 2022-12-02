---
title: Liniile de factură furnizor pentru jaloane
description: Acest articol explică cum să creați linii de factură de furnizor pentru jaloanele unui subcontract.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f066c2ac7377a989a92a9ae2e9a732d3c979a0db
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261044"
---
# <a name="vendor-invoice-lines-for-milestones"></a>Liniile de factură furnizor pentru jaloane

_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_

O factură de furnizor în Microsoft Dynamics 365 Project Operations poate avea linii de factură de furnizor pentru jaloanele care sunt definite pe o linie de subcontractare. Managerii de proiect pot folosi liniile de factură de furnizor pentru jaloane cu scopul de a înregistra costurile serviciilor care sunt achiziționate drept costuri bazate pe jaloane, care sunt suportate pentru serviciile sau produsele care sunt achiziționate pentru proiect.

Liniile de factură de furnizor pentru jaloane trebuie să facă întotdeauna referire la o linie de subcontractare care are o Metodă de facturare cu preț fix. Când o linie de factură a furnizorului pentru jaloane face referire la o linie de subcontractare, managerii de proiect vor putea să potrivească și să verifice costurile de bază pentru timp, cheltuieli sau materiale care fac referire la acea linie de subcontractare în raport cu jalonul care este facturat de furnizor.

Următorul tabel oferă informații despre câmpurile de pe liniile de factură de furnizor pentru jaloane.

| Câmp | Descriere | Impact funcțional |
| --- | --- | --- |
| Nume | Numele liniie de factură de furnizor, pentru a ajuta la identificare. | Acest nume va fi afișat ca prima coloană din toate căutările care sunt bazate pe liniile de factură de furnizor. |
| Descriere | O scurtă descriere a serviciilor care sunt facturate de furnizor pe linia de factură de furnizor. | Fără |
| Subcontract | Subcontractul pe care au fost comandate inițial serviciile. | Când este selectat un subcontract pentru factura de furnizor, toate liniile de pe factura de furnizor vor prelua acea selecție. O factură de furnizor nu poate avea linii de factură de furnizor care să facă referire la diferite subcontracte. |
| Linie de subcontractare | Linia de subcontractare pe care au fost comandate serviciile. Lista liniilor de subcontractare care pot fi selectate este limitată la liniile din subcontractul selectat. | Când o linie de subcontractare este selectată pe o linie de factură de furnizor pentru jaloane, câmpurile **Rol** și **Categorie de tranzacție** și câmpurile legate de produs sunt irelevante și nu sunt disponibile. Câmpurile **Cantitate**, **Unitate**, și **Grup de unități** nu sunt, de asemenea, relevante pentru liniile de factură de furnizor bazate pe jaloane. |
| Data tranzacției | Data la care costul real al liniei de factură a furnizorului va fi înregistrat în proiect. | Fără |
| Clasă de tranzacții | Selectați **Jalon** pentru a înregistra o factură de furnizor pentru un jalon finalizat care a fost definit pe o linie de subcontractare. | Fără |
| Jalon | Selectați jalonul care este definit pe linia de subcontractare aferentă care este marcată ca **Gata de facturare**. | Jaloanele liniei de subcontractare care au starea **Gata de facturare** pot fi selectate pe o linie de factură de furnizor. |
| Project | Numele proiectului pentru care au fost utilizate serviciile care sunt facturate. | Acest câmp este obligatoriu și nu poate fi lăsat necompletat. |
| Activitate | Numele sarcinii de proiect pentru care au fost utilizate serviciile care sunt facturate. Acest câmp este disponibil numai dacă este selectat un proiect. Selectarea unei sarcini de proiect este opțională. | Dacă acest câmp este lăsat necompletat, managerul de proiect poate potrivi linia de factură de furnizor cu clasa de tranzacții de pe linia de subcontractare aferentă care este înregistrată pe orice sarcină a proiectului. Dacă linia de factură a furnizorului nu face referire la o linie de subcontractare și acest câmp este lăsat necompletat, costul real creat de linia de factură a furnizorului nu va fi legat de nicio valoare reală a vânzărilor nefacturate. În acest caz, dacă este configurată facturarea bazată pe sarcini, este posibil ca costurile să nu poată fi facturate clientului final. |
| Valoare jalon | Introduceți valoarea jalonului care este definit pe linia de subcontractare pregătită pentru facturare. | Fără |
| Impozit pe vânzări | Introduceți valoarea impozitului pe vânzări. | Fără |
| Valoare totală | Valoarea totală a liniei de factură de furnizor, inclusiv impozitele. Acest câmp este calculat ca *Valoare jalon* + *Impozit pe vânzări*. | Fără |

> [!NOTE]
> Când este creată o linie de factură de furnizor care face referire la un jalon al liniei de subcontractare, starea jalonului subcontractului este actualizată la **Factură de furnizor creată**. Apoi, când acea factură de furnizor este confirmată, starea jalonului liniei de subcontractare este actualizată la **Factură de furnizor confirmată**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
