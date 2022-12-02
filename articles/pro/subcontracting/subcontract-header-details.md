---
title: Detalii antet pentru subcontracte
description: Acest articol explică funcționalitatea oferită pe antetul subcontractului în Project Operations.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 00b7c08235654d4bed0bcb4053d2044a3d092b54
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522576"
---
# <a name="header-details-for-subcontracts"></a>Detalii antet pentru subcontracte

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Acest articol explică funcționalitatea oferită pe antetul subcontractului în Dynamics 365 Project Operations.

Pe măsură ce un manager de proiect planifică și execută proiecte, acesta poate angaja subcontractanți și poate achiziționa produse și servicii de la furnizori. Atunci când un manager de proiect trebuie să achiziționeze produse sau servicii, acesta poate crea un subcontract în Project Operations.

Pentru a crea un subcontract, parcurgeți pașii următori.

1. În panoul de navigare, selectați **Subcontracte** iar pe pagina **Subcontract** selectați **Nou**.
2. Introduceți informațiile solicitate și apoi selectați **Salvare**.

    Următorul tabel oferă informații despre câmpurile din pagina **Antet subcontract**.

    | Câmp | Descriere |Impact funcțional |
    |---|------|---| 
    | Nume | Numele subcontractului. | În toate listele derulante de subcontractare, numele subcontractului este listat în prima coloană pentru a vă ajuta să identificați subcontractul. | 
    | Descriere | O scurtă descriere a serviciilor și produselor care sunt achiziționate în subcontract. | Fără |
    | Furnizor | Numele companiei de la care sunt achiziționate produsele și serviciile. Această înregistrare de cont are un tip de relație **Vânzător** sau **Furnizor**. | Pe baza furnizorului selectat, valorile implicite sunt introduse automat pentru următoarele câmpuri:<br/> **• Monedă** </br> **• Liste de prețuri** </br> **• Termeni de plată**</br> **• Adresă de plată**</br> **• Adresă de facturare**</br> **• Nume Facturare către** </br>**• Manager cont distribuitor**|
    | Dată subcontract | Data la care este creat subcontractul. | Data subcontractării este utilizată pentru a selecta lista corectă de prețuri de achiziție, fie din listele de prețuri atașate furnizorului aferent, fie din parametrii proiectului. |
    | Motiv stare | Starea subcontractului. | Starea determină unde se află subcontractul în procesul de afaceri și dacă poate fi editat. <br/>Valorile includ:<br>• **Schiță**: Subcontractul poate fi editat. Puteți edita doar subcontractele cu starea **Schiță**.<br/>• **Confirmat**: Negocierea cu furnizorul este completă și subcontractul este aprobat pentru livrare. <br/>• **Închis**: Livrarea subcontractului este finalizată.<br/>• **Anulat**: Subcontractul a fost anulat și nu este planificată nicio livrare.  | 
    | Monedă | Moneda în care sunt achiziționate produsele și serviciile. Valoarea implicită este introdusă automat din contul furnizorului, dar poate fi modificată. | Moneda subcontractului este utilizată pentru a corecta lista corectă de prețuri de achiziție, fie din listele de prețuri atașate furnizorului aferent, fie din parametrii proiectului. Listele de prețuri într-o altă monedă nu pot fi asociate cu subcontractul. Costul timpului, cheltuielilor și materialelor pe care resursele furnizorilor le livrează din acest subcontract sunt înregistrate în această monedă pe proiect. După salvarea înregistrării subcontractului, moneda subcontractului nu poate fi modificată.|
    | Unitate contractantă | Diviziunea companiei care încheie un contract de cumpărare sau un subcontract cu furnizorul. | Fără |
    | Termeni de plată | Condițiile de plată pentru facturile furnizorului care sunt emise pe acest subcontract. Valoarea implicită este introdusă automat din contul furnizorului. | Condițiile de plată din subcontract sunt copiate la toate facturile furnizorului care sunt legate de acest subcontract. Termenii de plată pot fi actualizați dacă subcontractul are statutul de **Schiță**. | 
    | Adresă de plată | Adresa furnizorului către care trebuie trimise plățile. Valoarea implicită este introdusă automat din contul furnizorului. | Adresa de plată din subcontract este copiată ca adresă de plată în toate facturile furnizorului care sunt create pentru acest subcontract. Adresa de plată poate fi actualizată dacă subcontractul are statutul de **Schiță**.|
    | Nume Facturare către | Numele persoanei sau diviziei din compania furnizorului care va trimite factura. Valoarea implicită este introdusă automat din contul furnizorului. | Valoarea **Nume Facturare la** din subcontract este copiată la toate facturile furnizorului care sunt legate de acest subcontract. Acest câmp poate fi actualizat dacă subcontractul are statutul de **Schiță**.|
    | Adresă de facturare | Adresa utilizată pe facturile de la furnizor. Valoarea implicită este introdusă automat din contul furnizorului. | Această adresă este adresa „factură de la” de pe facturile furnizorului care sunt create pentru acest subcontract. |
    | Subtotal | Dacă un subcontract nu are linii, introduceți subtotalul comenzii înainte de impozite. Dacă subcontractul are linii, acest câmp este numai în citire. Suma afișată este suma subtotală din toate liniile din subcontract. | Fără |
    | Impozit total | Dacă un subcontract nu are linii, introduceți totalul impozitelor pe acest subcontract. Dacă subcontractul are linii, acest câmp este numai în citire. Suma care este afișată este suma impozitelor din toate liniile de pe subcontract. | Fără |
    | Sumă totală | Acest câmp calculat arată valoarea totală a subcontractului după includerea taxelor. | Fără |
    | Data confirmării | Data la care a fost confirmat subcontractul. | Fără |
    | Solicitat de | În mod implicit, acest câmp este setat la numele utilizatorului care creează subcontractul. Cu toate acestea, creatorul subcontractului poate modifica valoarea pentru a indica persoana căreia creează subcontractul în numele. | Fără |
    | Manager cont distribuitor | Numele persoanei de contact principale pentru contul furnizorului. Valoarea implicită este introdusă automat din contul furnizorului. Puteți selecta un contact diferit ca manager de cont furnizor al subcontractului. | Puteți configura alerte prin e-mail pentru a notifica contactul atunci când sunt aduse modificări subcontractului ca urmare a negocierilor de preț. |
