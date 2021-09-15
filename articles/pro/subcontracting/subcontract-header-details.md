---
title: Detalii antet pentru subcontracte
description: Acest subiect explică funcționalitatea oferită pe antetul subcontractului în Project Operations.
author: rumant
ms.date: 08/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 49158af1a430033db3a5db57a840512c45bc17e2
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323656"
---
# <a name="header-details-for-subcontracts"></a>Detalii antet pentru subcontracte

[!include [banner](../../includes/dataverse-preview.md)]

_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_

Acest subiect explică funcționalitatea oferită pe antetul subcontractului în Dynamics 365 Project Operations.

Pe măsură ce un manager de proiect planifică și execută proiecte, acesta poate angaja subcontractanți și poate achiziționa produse și servicii de la furnizori. Atunci când un manager de proiect trebuie să achiziționeze produse sau servicii, acesta poate crea un subcontract în Project Operations.

Pentru a crea un subcontract, parcurgeți pașii următori.

1. În panoul de navigare, selectați **Subcontracte** iar pe pagina **Subcontract** selectați **Nou**.
2. Introduceți informațiile solicitate și apoi selectați **Salvare**.

    Următorul tabel oferă informații despre câmpurile din pagina antetului Subcontract.

    | **Câmp** | **Descriere** |
    | --- | --- | 
    | Nume | Numele subcontractului. |
    | Descriere | O scurtă descriere a serviciilor și produselor care sunt achiziționate în subcontract. |
    | Furnizor | Numele companiei de la care sunt achiziționate produsele și serviciile. Această înregistrare de cont are un tip de relație **Vânzător** sau **Furnizor**. |
    | Dată subcontract | Data creării subcontractului. |
    | Motiv stare | Starea subcontractului. |
    | Monedă | Moneda în care sunt achiziționate produsele și serviciile. Valoarea din acest câmp este implicită din contul furnizorului, dar poate fi modificată. Listele de prețuri ale proiectelor sunt utilizate pentru stabilirea prețurilor produselor și serviciilor din subcontract trebuie să fie în această monedă. Listele de prețuri în orice altă monedă nu pot fi asociate subcontractului. Costul produselor și serviciilor suportate pentru acest subcontract va fi înregistrat pe proiect în această monedă. |
    | Unitate contractantă | Diviziunea companiei care încheie un contract de cumpărare sau un subcontract cu furnizorul. |
    | Termeni de plată | Condițiile de plată pentru facturile furnizorului care sunt emise pe acest subcontract. Valoarea din acest câmp este implicită din înregistrarea din contul furnizorului. |
    | Adresă de plată | Adresa la care se trimite plata facturilor furnizorului. Valoarea din acest câmp este implicită din înregistrarea din contul furnizorului. |
    | Nume Facturare către | Numele persoanei sau diviziei din compania furnizorului care va trimite factura. Valoarea din acest câmp este implicită din înregistrarea contului furnizorului și va fi utilizată ca numele contactului principal pe facturile furnizorului create pentru acest subcontract. |
    | Adresă de facturare | Adresa utilizată pe facturile de la acest furnizor. Valoarea din acest câmp este implicită din înregistrarea din contul furnizorului. Această adresă este, de asemenea, utilizată ca adresa de facturare de pe facturile furnizorului create pentru acest subcontract. |
    | Subtotal | Dacă un subcontract nu are linii, introduceți o valoare în acest câmp care denotă subtotalul comenzii înainte de impozite. Dacă subcontractul are linii, acest câmp este numai în citire. Suma afișată este valoarea subtotalului din toate liniile din subcontract. |
    | Impozit total | Dacă un subcontract nu are linii, introduceți o valoare în acest câmp care să indice taxele din acest subcontract. Dacă subcontractul are linii, acest câmp este numai în citire. Valoarea afișată este valoarea suma taxelor din toate liniile din subcontract. |
    | Sumă totală |  Acest câmp calculat arată valoarea totală a subcontractului după includerea taxelor.  |
    | Data confirmării | Data la care s-a confirmat subcontractul.  |
    | Solicitat de | Valoarea din acest câmp este în mod implicit numele utilizatorului care creează subcontractul. Această valoare poate fi modificată de către creatorul subcontractului pentru a indica persoana în numele căreia creează subcontractul.  |
    | Manager cont distribuitor | Numele persoanei de contact principale pentru contul furnizorului. Valoarea din acest câmp este implicită din înregistrarea din contul furnizorului. Această valoare a câmpului poate fi modificată de utilizator pentru a selecta un contact diferit ca manager de cont furnizor pentru subcontract. Alertele prin e-mail și negocierile de preț pot fi configurate și trimise de acest contact. |


