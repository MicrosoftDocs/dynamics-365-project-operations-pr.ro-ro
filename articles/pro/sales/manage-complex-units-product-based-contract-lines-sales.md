---
title: Gestionarea unităților complexe pentru liniile de contract bazate pe produse - simplificat
description: Acest subiect oferă informații despre sprijinirea vânzării produselor bazate pe abonament.
author: rumant
ms.date: 10/28/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6bd4e11bf96d9f7d77c77fe081fde02b421c3139915150480a8d1a4d812887f6
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/06/2021
ms.locfileid: "7003381"
---
# <a name="manage-complex-units-for-product-based-contract-lines---lite"></a>Gestionarea unităților complexe pentru liniile de contract bazate pe produse - simplificat

_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_

Dynamics 365 Project Operations utilizează factori de cantitate pentru a asista vânzarea de produse pe bază de abonament. Pentru produsele bazate pe abonament, cantitatea din linia de contract sau proiect este exprimată ca număr de luni de utilizare.

Prețul software-ului de abonament este stocat în catalogul ca prețul pe utilizator pe lună. În timpul procesului de vânzări, prețul de pe linia de contract este, de obicei, prețul per utilizator, pe lună, care a fost negociat și actualizat de către agentul de vânzări IT. Fiecare afacere are un număr diferit de utilizatori și un număr diferit de luni de abonament. Cantitatea utilizată pentru a calcula suma liniei de contract este un produs al numărului de utilizatori și numărul de luni de abonament.

Pentru a sprijini acest tip de vânzare, Project Operations acceptă conceptul de *factori de cantitate*. Factorii de cantitate se bazează pe atributele produsului. Când configurați proprietăți specifice pentru un produs, puteți semnaliza un subset al acelor proprietăți sau toate proprietățile, ca factori de cantitate.

Project Operations validează că numai proprietățile numerice sau proprietățile produsului care au un tip de date numerice sunt marcate ca factori de cantitate. Când un produs cu factori de cantitate configurați este adăugat la o linie de contract, câmpul **Cantitate** devine numai în citire. După ce introduceți valori pentru proprietățile produsului care sunt factori de cantitate, Project Operations calculează cantitatea liniei de contract.

De exemplu, Dynamics 365 Sales poate avea următoarele proprietăți:

- **Nr. de utilizatori**: numărul de utilizatori.
- **Nr. de luni**: numărul de luni de abonament.
- **SKU produs**: Unitatea de stocare a stocului (SKU) pentru produs.

Proprietățile **Nr. de utilizatori** și **Nr. de luni** pot fi marcate ca factori de cantitate prin editarea proprietăților de linie de produs.

Pentru a crea factori de cantitate din proprietățile produsului, parcurgeți pașii următori.

1. Pe **Project Operations**, selectați **Vânzări-Produse**.
2. Deschideți produsul pentru care trebuie să setați factori de cantitate. Asigurați-vă că produsul are proprietăți deja configurate.
3. Pe pagina **Informații de proiect**, selectați fila **Factori de cantitate**.
4. În subgrilă selectați **+ Calcul de câmp nou**.
5. Introduceți numele **Factorului Cantitate** și selectați valoarea proprietății care se mapează la calculul câmpului.
6. Salvați și închideți formulatul.
7. Repetați pașii 2-6 pentru toate proprietățile care împreună vor constitui cantitatea pentru linia contractuală bazată pe produs.

Cu setarea factorilor de cantitate, atunci când utilizatorul creează o linie contractuală pentru acest produs, cantitatea liniei contractuale este blocată. Cantitatea este apoi calculată ca produs al valorilor proprietății pentru acea linie contractuală.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]