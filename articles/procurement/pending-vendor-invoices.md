---
title: Achiziții de materiale care nu există pe stoc sau categorii de achiziții care utilizează o factură de furnizor neachitată
description: Acest articol explică modul de înregistrare a facturilor de furnizor neachitate.
author: sigitac
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: b1c05755f6759e90e031a11261f15a2c4b6b716e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922007"
---
# <a name="purchase-non-stocked-materials-or-procurement-categories-using-a-pending-vendor-invoice"></a>Achiziții de materiale care nu există pe stoc sau categorii de achiziții care utilizează o factură de furnizor neachitată

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

Întrucât o companie cumpără materiale care nu sunt stocate sau categorii de achiziții pentru un proiect, costurile pot fi înregistrate imediat în raport cu proiectul. 

De exemplu, Contoso Robotics SUA realizează un proiect de reînnoire a echipamentelor și are nevoie de licențe software. Aceste licențe sunt achiziționate de la un furnizor terță parte.  Folosind Dynamics 365 Finance, funcționarul pentru Conturi de plată înregistrează un document de factură de furnizor în așteptare și atribuie costurile licenței direct proiectului de reînnoire a echipamentului. 

> [!IMPORTANT]
> Înainte de a utiliza funcționalitatea descrisă în acest articol, revizuiți și aplicați configurațiile necesare. Pentru mai multe informații, consultați [Activarea materialelor care nu sunt stocate și facturile de furnizor aflate în așteptare](configure-materials-nonstocked.md) și [Utilizarea categoriilor de achiziții cu comenzile de cumpărare de proiect și facturile de furnizor aflate în așteptare](configure-procurement-categories.md)

## <a name="post-a-project-related-pending-vendor-invoice"></a>Postați o factură de vânzător neachitată legată de proiect 

Facturile neachitate de la vânzător pot fi înregistrate pe pagina **Facturi de vânzător neachitate** (**Conturi furnizori** > **Facturi** > **Facturi de vânzător neachitate**). Parcurgeți pașii următori pentru a posta o factură de furnizor neachitată legată de proiect:

1. Accesați **Conturi de plată** > **Facturi** și selectați **Nou**. 
1. În câmpul **Cont de factură**, selectați un furnizor și apoi, în câmpul **Număr**, introduceți identificarea facturii de furnizor.
1. Adăugați o linie la factura de furnizor și apoi, în câmpul **Număr articol**, selectați articolul care nu se află în stoc cumpărat de la furnizor. Alternativ, în câmpul **Categorie de achiziții**, selectați categoria de achiziții care a fost achiziționată de la furnizor.   
1. Adăugați cantitatea care a fost achiziționată. Sistemul completează prețul unitar pe baza configurației prețului articolului care nu se află în stoc. 
1. Verificați suma totală și alte detalii necesare pe linie.
1. În detaliile de linie, pe fila **Proiect**, selectați ID-ul proiectului în care va fi înregistrat acest element.
1. Opțional: Selectați numărul activității și actualizați categoria de proiect și proprietatea liniei.
1. Publicați factura de furnizor aflată în așteptare. Când factura este publicată, sistemul înregistrează următoarele informații:
    
    - Valoarea soldului furnizorului.
    - Valoare impozit pe vânzări.
    - Costul aferent proiectului este înregistrat în contul de integrare a achizițiilor.
    - Tranzacția costului real al proiectului în Dataverse.  Această tranzacție este procesată în continuare folosind [Jurnalul de integrare Project Operations](../project-accounting/project-operations-integration-journal.md). Postarea acestui jurnal mută suma din contul de integrare a achizițiilor în contul de cost de proiect. 
    - Achizițiile care sunt facturate către clientul proiectului utilizând metoda de facturare a timpului și a materialelor. În plus, sunt create tranzacții de vânzare necotificate pentru achizițiile din Dataverse. Lista de prețuri a produsului în Dataverse este utilizat pentru prețurile și sumele de vânzare pentru tranzacțiile de vânzare nefacturate.
