---
title: Liniile de factură ale furnizorului pentru etapele de referință
description: Acest subiect explică cum să creați linii de factură de furnizor pentru etapele unui subcontract.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 4fa11e2a4f459016b3ce141b03fe97e55c9a2759
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8590637"
---
# <a name="vendor-invoice-lines-for-milestones"></a>Liniile de factură ale furnizorului pentru etapele de referință

[!include [banner](../../includes/dataverse-preview.md)]

_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_

O factură de furnizor în Microsoft Dynamics 365 Project Operations poate avea linii de factură de furnizor pentru etapele de referință care sunt definite pe o linie de subcontractare. Managerii de proiect pot folosi liniile de factură ale furnizorului pentru etapele de referință pentru a înregistra costurile serviciilor care sunt achiziționate ca costuri bazate pe etape care sunt suportate pentru serviciile sau produsele care sunt achiziționate pentru proiect.

Liniile de factură pentru furnizori pentru etape trebuie să facă întotdeauna referire la o linie de subcontractare care are o metodă de facturare cu preț fix. Atunci când o linie de factură a furnizorului pentru etapele de referință face referire la o linie de subcontractare, managerii de proiect vor putea să potrivească și să verifice costurile subiacente ale timpului, cheltuielilor sau materialelor care fac referire la acea linie de subcontractare cu etapa care este facturată de furnizor.

Următorul tabel oferă informații despre câmpurile de pe liniile de factură pentru furnizori pentru etape.

| Câmp | Descriere | Impact funcțional |
| --- | --- | --- |
| Nume | Numele liniei de factură a furnizorului, pentru a ajuta la identificare. | Acest nume va fi afișat ca prima coloană în toate căutările care se bazează pe liniile de factură pentru furnizor. |
| Descriere | O scurtă descriere a serviciilor care sunt facturate de către furnizor pe linia de factură pentru furnizor. | Fără |
| Subcontract | Subcontractul pe care au fost comandate inițial serviciile. | Când este selectat un subcontract pentru factura de furnizor, toate liniile de pe factura de furnizor vor moșteni acea selecție. O factură de furnizor nu poate avea linii de factură de furnizor care să facă referire la diferite subcontracte. |
| Linia de subcontractare | Linia de subcontractare pe care au fost comandate serviciile. Lista liniilor de subcontract care pot fi selectate este limitată la liniile din subcontractul selectat. | Când o linie de subcontractare este selectată pe o linie de factură a furnizorului pentru etape, **Rol** și **Categoria tranzacției** câmpurile și câmpurile legate de produs sunt irelevante și nu sunt disponibile. The **Cantitate**, **·**, și **Grup de unitati** câmpurile nu sunt, de asemenea, relevante pentru liniile de factură pentru furnizori bazate pe etape. |
| Data tranzacției | Data la care costul real al liniei de factură a furnizorului va fi înregistrat în proiect. | Fără |
| Clasă de tranzacții | Selectați **Piatra de hotar** pentru a înregistra o factură de furnizor pentru o etapă finalizată care a fost definită pe o linie de subcontractare. | Fără |
| Jalon | Selectați jalonul care este definit pe linia de subcontractare aferentă care este marcată ca **Gata de facturare**. | Etape ale liniei de subcontractare care au statutul de **Gata de facturare** poate fi selectat pe o linie de factură a furnizorului. |
| Project | Numele proiectului pentru care au fost utilizate serviciile care sunt facturate. | Acest câmp este obligatoriu și nu poate fi lăsat necompletat. |
| Activitate | Numele sarcinii de proiect pentru care au fost utilizate serviciile care sunt facturate. Acest câmp este disponibil numai dacă este selectat un proiect. Selectarea unei sarcini de proiect este opțională. | Dacă acest câmp este lăsat necompletat, managerul de proiect poate potrivi linia de factură a furnizorului cu clasa de tranzacții de pe linia de subcontractare aferentă care este înregistrată pentru orice activitate a proiectului. Dacă linia de factură a furnizorului nu face referire la o linie de subcontractare și acest câmp este lăsat necompletat, costul real creat de linia de factură a furnizorului nu va fi legat de nicio valoare reală a vânzărilor nefacturate. În acest caz, dacă este configurată facturarea bazată pe sarcini, este posibil ca costurile să nu poată fi facturate clientului final. |
| Valoare jalon | Introduceți valoarea etapei care este definită pe linia de subcontractare care este gata de facturare. | Fără |
| Impozit pe vânzări | Introduceți valoarea impozitului pe vânzări. | Fără |
| Valoare totală | Suma totală a liniei de factură a furnizorului, inclusiv taxele. Acest câmp este calculat ca *Suma de reper* + *Taxa de vanzari*. | Fără |

> [!NOTE]
> Când este creată o linie de factură de furnizor care face referire la o etapă a liniei de subcontractare, starea etapei de subcontractare este actualizată la **S-a creat factura de furnizor**. Apoi, când acea factură de furnizor este confirmată, starea jalonului liniei de subcontractare este actualizată la **Factura furnizorului confirmată**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
