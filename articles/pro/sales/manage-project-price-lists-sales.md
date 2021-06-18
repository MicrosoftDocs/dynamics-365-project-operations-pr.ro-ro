---
title: Gestionarea listelor de prețuri ale proiectelor din ofertele de proiecte
description: Acest subiect oferă informații despre lucrul cu liste de prețuri de proiect pe oferte.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 926581f877f91e3a351d51cac9c2b1daba035126
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994916"
---
# <a name="manage-project-price-lists-on-project-quotes"></a>Gestionarea listelor de prețuri ale proiectelor din ofertele de proiecte 

_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_

Cotațiile proiectului sunt concepute pentru a susține listele de prețuri de vânzare eficiente cu mai multe date. Cu Dynamics 365 Project Operations, s-a adăugat o nouă entitate asociată denumită **Listele de prețuri ale proiectului**. Această entitate are o relație de la 1 la mulți cu o ofertă de proiect.

Listele de prețuri ale proiectului sunt folosite pentru a stabili prețurile pentru tranzacții de timp, materiale și cheltuieli pentru un proiect. Atunci când o ofertă are una sau mai multe liste de prețuri ale proiectelor, aceste liste de prețuri sunt utilizate pentru a stabili prețul pentru timp, materiale, estimări ale cheltuielilor și valori reale pentru proiectele care sunt asociate cu oferta prin linia de ofertă.

Când nu există liste de prețuri ale proiectului pe o ofertă de proiect, veți primi un mesaj de avertizare. Mesajul afirmă că, deoarece nu există liste de prețuri ale proiectului, lucrările și cheltuielile estimate și reale ale proiectului nu vor fi evaluate. În schimb, vor avea un preț zero (0) pentru valorile vânzărilor.

## <a name="associate-or-disassociate-a-project-price-list-on-a-project-quote"></a>Asociați sau dezasociați o listă de prețuri a proiectului într-o ofertă de proiect

Pentru a crea sau a selecta o listă de prețuri specifică pentru estimarea lucrărilor și a cheltuielilor bazate pe proiect, parcurgeți pașii următori.

1. Pe ofertă, selectați fila **Prețul proiectului** și în subgrilă, selectați **+ Adăugați o listă de prețuri pentru proiectul nou**.
2. Pe pagina Creare rapidă, selectați o listă de prețuri. Lista verticală afișează toate listele de prețuri care au contextul setat la **Vânzări** iar moneda se potrivește cu moneda din ofertă.
4. Introduceți o descriere pentru asocierea listei de prețuri a proiectului și selectați **Salvați și închideți**.

Este creată o asociere de listă de prețuri de proiect.

Puteți repeta acest proces dacă trebuie să asociați mai mult de o listă de prețuri de proiect la oferta de proiect. Creați mai multe liste de prețuri ale proiectului numai dacă aveți date efective diferite pentru fiecare dintre listele de prețuri asociate proiectului.

> [!NOTE]
> Project Operations nu acceptă suprapunerea datei efective a listei de prețuri a proiectului. Dacă există mai multe liste de prețuri ale proiectului pentru o tranzacție cu data dată, prețul pentru acea tranzacție va fi implicit la zero (0).
Pentru a elimina o asociere a listei de prețuri a proiectului, selectați lista de prețuri a proiectului și apoi selectați **Ștergeți lista de prețuri a proiectului de ofertă**. Lista de prețuri este eliminată din listele de prețuri ale proiectului, dar lista de prețuri în sine nu este ștearsă. Este ștearsă doar asocierea la ofertă.

## <a name="set-up-default-project-price-lists-on-a-quote"></a>Configurați listele de prețuri implicite ale proiectului pe o ofertă

Listele de prețuri ale proiectului pot fi setate ca implicite la o ofertă de proiect. Această configurație asigură faptul că toate ofertele din organizația dvs. încep întotdeauna cu o listă de preț standard pentru perioada respectivă de preț.

### <a name="set-up-organizational-default-for-project-price-lists"></a>Configurați setările implicite organizaționale pentru listele de prețuri ale proiectului

1. Accesați **Setări** > **General** > **Parametri**.
2. Pe pagina listei **Parametri activi**, localizați înregistrarea și faceți dublu clic pentru a o deschide. 
3. Pe pagina **Parametri**, selectați fila **Listă de prețuri**. Puteți vedea lista listelor de prețuri implicite. Aceasta este o listă de costuri standard și liste de prețuri de vânzare. Având o listă de prețuri de vânzare asociată aici pentru fiecare monedă în care vindeți, vă veți asigura că această listă de prețuri de vânzare este implicită pentru orice ofertă pe care o creați pentru clienții care tranzacționează în această monedă.

### <a name="set-up-customer-specific-project-price-lists"></a>Configurați liste de prețuri specifice proiectului pentru clienți

Listele de prețuri specifice proiectului pentru clienți pot fi, de asemenea, configurate atunci când ați negociat un contract de stabilire a prețurilor cu clienții dvs.

Pentru a configura o listă de prețuri a proiectului specifică clientului, parcurgeți pașii următori.

1. În zona **Vânzări**, selectați **Clienți**.
2. În lista conturilor dvs. active, selectați și deschideți înregistrarea clientului pentru care aveți o listă de prețuri specială.
3. Pe fila **Listele de prețuri ale proiectului**, puteți crea o nouă asociație de listă de prețuri pentru a avea lista de prețuri a proiectului care este specifică acestui client.

## <a name="create-custom-pricing-on-a-project-quote"></a>Creați prețuri particularizate pentru o ofertă de proiect

După ce aveți liste de prețuri implicite organizaționale și specifice clientului, ofertele dvs. de proiect vor fi create automat cu aceste asociații de liste de prețuri ale proiectului. Cu toate acestea, în anumite cazuri, poate fi necesar să creați prețuri personalizate pentru o anumită ofertă de proiect. 

1. Pe **Oferta de proiect**, pe fila **Lista de prețuri a proiectului**, verificați în subgrilă dacă nu este selectată nicio înregistrare specifică a listei de prețuri.
2. Selectați **Creați prețuri particularizate**. Aceasta va face copii ale tuturor listelor de preț standard asociate în prezent cu oferta și va asocia aceste copii cu oferta. Asocierile existente la listele standard de prețuri vor fi eliminate. Agentul de vânzări poate începe apoi să editeze prețurile pe aceste copii. Aceste prețuri modificate vor fi aplicabile numai pentru această ofertă de proiect.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
