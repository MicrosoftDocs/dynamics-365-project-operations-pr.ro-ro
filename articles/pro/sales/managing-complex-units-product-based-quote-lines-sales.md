---
title: Gestionarea unităților complexe, cum ar fi liniile de ofertă bazate pe produse per utilizator, pe lună
description: Acest subiect oferă informații despre gestionarea unităților complexe pentru linii de ofertă bazate pe produs.
author: rumant
manager: Annbe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 741230e69302138cce8f7379f520f7178e1c80af
ms.sourcegitcommit: fd8ea1779db2bb39a428f459ae3293c4fd785572
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/06/2020
ms.locfileid: "3965866"
---
# <a name="managing-complex-units-such-as-per-user-per-month-for-product-based-quote-lines"></a>Gestionarea unităților complexe, cum ar fi liniile de ofertă bazate pe produse per utilizator, pe lună

_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_

Dynamics 365 Project Operations utilizează factori de cantitate pentru a asista vânzarea de produse pe bază de abonament. Pentru produsele bazate pe abonament, cantitatea din linia de contract de ofertă sau de proiect este exprimată ca număr de luni de utilizare.

De obicei, prețul software-ului de abonament este stocat în catalogul ca prețul pe utilizator pe lună. În timpul procesului de vânzări, prețul de pe linia de ofertă este, de obicei, prețul per utilizator, pe lună, care a fost negociat și actualizat de către agentul de vânzări IT. Fiecare afacere are un număr diferit de utilizatori și un număr diferit de luni de abonament. Cantitatea utilizată pentru a calcula linia de ofertă este un produs al numărului de utilizatori și numărul de luni de abonament.

Pentru a sprijini acest tip de vânzare, Project Operations a introdus conceptul de factori de cantitate. Factorii de cantitate se bazează pe atributele produsului în Dynamics 365. Când configurați proprietăți specifice pentru un produs, Project Operations vă permite să semnalizați un subset al acelor proprietăți sau toate proprietățile, ca factori de cantitate.

Project Operations validează că numai proprietățile numerice sau proprietățile produsului care au un tip de date numerice sunt marcate ca factori de cantitate. Când adăugați un produs cu factori de cantitate la o linie de ofertă, câmpul **Cantitate** devine numai în citire. După ce introduceți valori pentru proprietățile produsului care sunt factori de cantitate, Project Operations cantitatea liniei de ofertă.

De exemplu, Dynamics 365 Sales poate avea următoarele proprietăți:

- **Nr. de utilizatori**: numărul de utilizatori
- **Nr. de luni**: numărul de luni de abonament
- **Produs SKU**

Puteți semnaliza proprietățile **Nr. de utilizatori** și **Nr. de luni** ca factori de cantitate prin editarea proprietăților de linie de produs.

Pentru a crea factori de cantitate din proprietățile produsului, urmați acești pași:

1. În panoul de navigare din stânga Project Operations, accesați **Vânzări** > **Produse**.
2. Deschideți produsul pentru care trebuie să configurați factorii de cantitate. Asigurați-vă că produsul are proprietăți deja configurate.
3. Pe pagina **Informații despre proiect** pentru produs, selectați fila **Factori de cantitate**.
4. În subgrilă selectați **+ Calcul de câmp nou**.
5. Introduceți numele factorului Cantitate și selectați valoarea proprietății care se mapează la calculul câmpului.
6. Salvați și închideți formulatul. Repetați acești pași pentru toate proprietățile de utilizat pentru calcularea cantității pentru linia de cotare bazată pe produs.

Când creați o linie de ofertă bazată pe produs pentru un produs, cantitatea liniei de ofertă va fi blocată. Cantitatea va fi calculată ca produs al valorilor proprietății pe care le introduceți pentru acea linie de ofertă.
