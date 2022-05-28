---
title: Achiziționați materiale care nu sunt stocate sau categorii de achiziții folosind o factură de furnizor în așteptare
description: Acest subiect explică modul de înregistrare a facturilor neachitate de la furnizor.
author: sigitac
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: e81f7a54e304ae6fc9a9f2637124579b6e7b54e9
ms.sourcegitcommit: 9916f536a71b6a0078297402564ac79308ec6890
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 04/18/2022
ms.locfileid: "8612672"
---
# <a name="purchase-non-stocked-materials-or-procurement-categories-using-a-pending-vendor-invoice"></a>Achiziționați materiale care nu sunt stocate sau categorii de achiziții folosind o factură de furnizor în așteptare

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

Deoarece o companie achiziționează materiale neaprovizionate sau categorii de achiziții pentru un proiect, costurile pot fi înregistrate imediat în raport cu proiectul. 

De exemplu, Contoso Robotics SUA realizează un proiect de reînnoire a echipamentelor și are nevoie de licențe software. Aceste licențe sunt achiziționate de la un furnizor terță parte.  Folosind Dynamics 365 Finance, funcționarul conturi plătibile înregistrează un document de facturare a furnizorului în așteptare și atribuie costurile de licență direct proiectului de reînnoire a echipamentului. 

> [!IMPORTANT]
> Înainte de a utiliza funcționalitatea descrisă în acest subiect, revizuiți și aplicați configurațiile necesare. Pentru mai multe informații, vezi [Activați materialele care nu sunt stocate și facturile furnizorilor în așteptare](configure-materials-nonstocked.md) și [Utilizați categorii de achiziții cu comenzile de achiziție de proiect și facturile furnizorilor în așteptare](configure-procurement-categories.md)

## <a name="post-a-project-related-pending-vendor-invoice"></a>Postați o factură de vânzător neachitată legată de proiect 

Facturile neachitate de la vânzător pot fi înregistrate pe pagina **Facturi de vânzător neachitate** (**Conturi furnizori** > **Facturi** > **Facturi de vânzător neachitate**). Parcurgeți pașii următori pentru a posta o factură de furnizor neachitată legată de proiect:

1. Mergi la **Creanţe** > **Facturi**, și selectați **Nou**. 
1. În **Cont de factură** câmp, selectați un furnizor și apoi, în **Număr** câmp, introduceți identificarea facturii furnizorului.
1. Adăugați o linie la factura furnizorului, apoi, în **Numărul de articol** câmp, selectați articolul care nu este stocat care a fost achiziționat de la furnizor. Alternativ, în **Categoria de achiziții** câmp, selectați categoria de achiziție care a fost achiziționată de la furnizor.   
1. Adăugați cantitatea care a fost achiziționată. Sistemul completează prețul unitar, pe baza configurației prețului articolului care nu este stocat. 
1. Verificați suma totală și alte detalii necesare pe linie.
1. În detaliile rândului, pe **Proiect** fila, selectați ID-ul proiectului în care va fi înregistrat acest articol.
1. Opțional: Selectați numărul activității și actualizați categoria proiectului și proprietatea liniei.
1. Postați factura de furnizor în așteptare. Când factura este înregistrată, sistemul înregistrează următoarele informații:
    
    - Valoarea soldului furnizorului.
    - Valoare impozit pe vânzări.
    - Costul aferent proiectului este înregistrat în contul de integrare a achizițiilor.
    - Tranzacția costului real al proiectului în Dataverse.  Această tranzacție este procesată în continuare folosind [Jurnalul de integrare Project Operations](../project-accounting/project-operations-integration-journal.md). Postarea acestui jurnal mută suma din contul de integrare a achizițiilor în contul de cost de proiect. 
    - Achizițiile care sunt facturate către clientul proiectului utilizând metoda de facturare a timpului și a materialelor. În plus, sunt create tranzacții de vânzare necotificate pentru achizițiile din Dataverse. Lista de prețuri a produsului în Dataverse este utilizat pentru prețurile și sumele de vânzare pentru tranzacțiile de vânzare nefacturate.
