---
title: Achiziții de materiale care nu există pe stoc utilizând o factură de vânzător neachitată
description: Acest subiect explică modul de înregistrare a facturilor neachitate de la furnizor.
author: sigitac
manager: tfehr
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7a706f419443dcdf92ce3b247d719943272907d0
ms.sourcegitcommit: 7468d668c48c1d87934aab9a034decd51e56dec6
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 04/13/2021
ms.locfileid: "5880676"
---
# <a name="purchase-non-stocked-materials-using-a-pending-vendor-invoice"></a>Achiziții de materiale care nu există pe stoc utilizând o factură de vânzător neachitată

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

Deoarece o companie cumpără materiale care nu sunt stocate pentru un proiect, costurile pot fi înregistrate imediat în raport cu proiectul. 

De exemplu, Contoso Robotics SUA realizează un proiect de reînnoire a echipamentelor și are nevoie de licențe de software. Aceste licențe sunt achiziționate de la un furnizor terță parte.  Folosind Dynamics 365 Finance, funcționarul de conturi furnizori înregistrează un document de factură neachitată a furnizorului și atribuie costurile licenței direct proiectului de reînnoire a echipamentului. 

> [!IMPORTANT]
> Înainte de a utiliza funcționalitatea descrisă în acest subiect, revizuiți și aplicați configurațiile necesare. Pentru mai multe informații, consultați [Activarea materialelor care nu există pe stoc și a facturilor de la furnizori neachitate](configure-materials-nonstocked.md). 

## <a name="post-a-project-related-pending-vendor-invoice"></a>Postați o factură de vânzător neachitată legată de proiect 

Facturile neachitate de la vânzător pot fi înregistrate pe pagina **Facturi de vânzător neachitate** (**Conturi furnizori** > **Facturi** > **Facturi de vânzător neachitate**). Parcurgeți pașii următori pentru a posta o factură de furnizor neachitată legată de proiect:

1. Accesați **Conturi furnizori** > **Facturi** și selectați **Nou**. 
2. În câmpul **Cont de factură**, selectați un furnizor și în câmpul **Număr**, introduceți identificarea facturii furnizorului.
3. Adăugați o linie la factura furnizorului și în câmpul **Numărul de element**, selectați elementul care nu este stocat cumpărat de la furnizor. 

    > [!NOTE]
    > Liniile de facturare ale furnizorului care se bazează pe o categorie de achiziții nu pot fi înregistrate în cadrul proiectului. 
    
5. Adăugați cantitatea achiziționată. Sistemul va completa prețul unitar pe baza configurației prețului articolului care nu este stocat. 
6. Verificați suma totală și alte detalii necesare pe linie.
7. Pe detaliile liniei, pe fila **Proiect**, selectați ID-ul proiectului în care va fi înregistrat acest element.
8. Opțional, selectați numărul activității și actualizați categoria de proiect și proprietatea liniei.
9. Postați factura furnizorului în așteptare. Când factura este publicată, sistemul înregistrează:
    
    - Valoarea soldului furnizorului.
    - Valoare impozit pe vânzări.
    - Costul aferent proiectului este înregistrat în contul de integrare a achizițiilor.
    - Tranzacția efectivă a proiectului în Dataverse. Această tranzacție este procesată în continuare folosind [Jurnalul de integrare Project Operations](../project-accounting/project-operations-integration-journal.md). Postarea acestui jurnal mută suma din contul de integrare a achizițiilor în contul de cost de proiect.