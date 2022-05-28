---
title: Configurarea facturării între companii
description: Acest subiect oferă informații și exemple despre configurarea facturării între companii pentru proiecte.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: ad6022670048e5aa3635998852b78c49af461d4e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8591603"
---
# <a name="configure-intercompany-invoicing"></a>Configurarea facturării între companii

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

Parcurgeți pașii următori pentru a configura facturarea între companii pentru proiecte în Dynamics 365 Project Operations. Tranzacțiile între companii sunt tranzacții de timp și cheltuieli dintr-un contract de proiect care aparțin unei companii sau unei unități organizaționale, în timp ce resursele din contractul de proiect fac parte dintr-o altă companie sau unitate organizațională.

## <a name="example-configure-intercompany-invoicing"></a>Exemplu: Configurarea facturării între companii

În exemplul următor, Contoso Robotics SUA (USPM) este entitatea juridică care ia împrumutul, iar Contoso Robotics UK (GBPM) este entitatea juridică care împrumută. 

1. **Configurați contabilitatea între companii între entități juridice**. Fiecare pereche de persoane juridice care iau cu împrumut și împrumută trebuie să fie configurată pe pagina registrului general [Contabilitate între companii](/dynamics365/finance/general-ledger/intercompany-accounting-setup).
    
    1. În Dynamics 365 Finance, accesați **Registrul general** > **Configurarea postării** > **Contabilitatea intercompanii**. Creați o înregistrare cu următoarele informații:

        - **Companie originară** = **GBPM**
        - **Compania destinatară** = **USPM**

2. **Configurați relația comercială între entitățile juridice**. Înregistrarea clientului care reprezintă entitatea juridică care ia cu împrumut trebuie creată în entitatea juridică care împrumută. Înregistrarea vânzătorului care reprezintă entitatea juridică care împrumută trebuie creată în entitatea juridică care ia cu împrumut.

     1. În Finanțe, selectați entitatea juridică **GBPM**.
     2. Accesați **Conturi clienți** > **Client** > **Toți clienții**. Creați o nouă înregistrare pentru entitatea juridică, **USPM**.
     3. Extindeți **Nume**, filtrați înregistrările după **Tip** și selectați **Entități legale**. 
     4. Găsiți și selectați înregistrarea clientului pentru **Contoso Robotics SUA (USPM)**.
     5. Selectați **Folosiți potrivirea**. 
     6. Selectați grupul de clienți **50 - Clienți între companii** și apoi salvați înregistrarea.
     7. Selectați entitatea juridică **USPM**.
     8. Accesați **Conturi furnizori** > **Furnizori** > **Toți furnizorii**. Creați o nouă înregistrare pentru entitatea juridică, **GBPM**.
     9. Extindeți **Nume**, filtrați înregistrările după **Tip** și selectați **Entități juridice**. 
     10. Găsiți și selectați înregistrarea clientului pentru **Contoso Robotics UK (USPM)**.
     11. Selectați **Folosiți potrivirea**, selectați grupul de furnizori, apoi salvați înregistrarea.
     12. În înregistrarea furnizorului, selectați **General** > **Configurare** > **Între firme**.
     13. Pe fila **Relația comercială**, set **Activ** la **Da**.
     14. Setați câmpul **Compania client** la **GBPM** iar la **Registrul contului meu**, selectați registrul clienți pe care l-ați creat anterior în timpul procedurii.

3. **Configurați setările între companii în gestionarea proiectelor și parametrii contabili**. 

    1. Selectați entitatea juridică **USPM** și accesați **Management de proiect și contabilitate** > **Configurare** > **Managementul proiectului și parametrii contabili**.
    2. Pe fila **Între companii**, selectați categoria de achiziții pentru a se potrivi cu facturile furnizorului care sunt generate automat.
    3. În **Categorie implicită**, selectați **Resurse între companii**.
    4. Selectați entitatea juridică **GBPM** și accesați **Management de proiect și contabilitate** > **Configurare** > **Managementul proiectului și parametrii contabili**.
    5. Pe fila **Între companii**, selectați o categorie de proiect implicită pentru fiecare tip de tranzacție. Categoriile de proiecte sunt utilizate pentru configurarea impozitului atunci când categoria facturată în tranzacțiile între companii există doar la entitatea juridică împrumutată. Puteți alege să acumulați venituri pentru tranzacții între companii. Acumularea se întâmplă atunci când tranzacțiile sunt înregistrate prin jurnalul de integrare a Project Operations în entitatea juridică de creditare. Jurnalul este inversat când se înregistrează factura între companii.
    6. În grupul **La împrumutarea resurselor**, selectați **...** > **Nou**. 
    7. În grilă, selectați informațiile următoare:

          - **Împrumutul entității juridice** = **USPM**
          - **Acumulați venituri** = **Da**
          - **Categorie implicită a foii de timp** = **Implicit - Oră**
          - **Categorie de cheltuieli implicite** = **Implicit - cheltuială**

4. **Setați conturi de costuri și venituri între companii în configurarea înregistrării Registru**. Contul de venituri între companii este creditat atunci când factura clientului între companii este înregistrată în entitatea juridică de creditare. Contul de costuri între companii este debitat atunci când factura vânzătorului potrivit este înregistrată în entitatea juridică de împrumut. Aceste conturi sunt înființate în entități juridice corespunzătoare. 
      
     1. În Finanțe, selectați entitatea juridică de împrumut **USPM**. 
     2. Accesați **Management de proiect și contabilitate** > **Configurat** > **Postare** > **Configurare înregistrare registru**. 
     3. Pe fila **Conturi de cost**, în **Tip de cont de registru**, selectați **Costul între companii**. Creați o înregistrare nouă cu următoarele informații:
      
        - **Entitate juridică de împrumut** = **GBPM**
        - **Cont principal** = Selectați contul principal pentru costul între companii. Această configurare este obligatorie. Configurarea este utilizată pentru fluxurile intercompaniilor din Finanțe, dar nu și pentru fluxurile intercompaniilor legate de proiect. Această selecție nu are impact în aval. 
        
     4. Selectați entitatea juridică de împrumut, **GBPM**. 
     5. Accesați **Management de proiect și contabilitate** > **Configurat** > **Postare** > **Configurare înregistrare registru**. 
     6. Pe fila **Conturi de venit**, în **Tip de cont de registru**, selectați **Venitul între companii**. Creați o înregistrare nouă cu următoarele informații:

        - **Împrumutul entității juridice** = **USPM**
        - **Contul principal** = Selectați contul principal pentru venitul între companii. Această configurare este obligatorie. Configurarea este utilizată pentru fluxurile intercompaniilor din Finanțe, dar nu și pentru fluxurile intercompaniilor legate de proiect. Această selecție nu are impact în aval. 

5. **Configurați prețurile de transfer pentru forța de muncă**. Prețurile de transfer între companii sunt configurate în Project Operations pe Dataverse. Configurați [ratele costului forței de muncă](../pricing-costing/set-up-labor-cost-rate.md#transfer-pricing-and-costs-for-resources-outside-of-your-division-or-legal-entity) și [ratele facturii muncii](../pricing-costing/set-up-labor-bill-rate.md#transfer-pricing-or-set-up-bill-rates-for-resources-from-other-organizational-units-or-divisions) pentru facturare între companii. Prețurile de transfer nu sunt acceptate pentru tranzacțiile de cheltuieli între companii. Prețul de vânzare unitar între organizații va fi întotdeauna stabilit la aceeași valoare ca și prețul de cost al unității de resurse.

      Costul resurselor dezvoltatorului în Contoso Robotics UK este de 88 GBP pe oră. Contoso Robotics UK va factura Contoso Robotics SUA 120 USD pentru fiecare oră în care această resursă a lucrat la proiecte din SUA. Contoso Robotics SUA va factura clientului Adventure Works 200 USD pentru munca depusă de resursa dezvoltatorului Contoso Robotics UK.

      1. În Project Operations pe Dataverse, accesați la **Vânzare** > **Liste de prețuri**. Creați o nouă listă de prețuri de cost numită **Tarifele de cost ale Contoso Robotics UK.** 
      2. În lista de prețuri de cost, creați o înregistrare cu următoarele informații:
         - **Rol** = **Dezvoltator**
         - **Cost** = **88 GBP**
      3. Accesați **Setări** > **Unități organizatorice** și atașați această listă de prețuri la unitatea organizațională **Contoso Robotics UK**.
      4. Accesați **Vânzări** > **Liste de prețuri**. Creați o nouă listă de prețuri de cost numită **Rate de cost ale Contoso Robotics SUA**. 
      5. În lista de prețuri de cost, creați o înregistrare cu următoarele informații:
          - **Rol** = **Dezvoltator**
          - **Firmă de resurse** = **Contoso Robotics UK**
          - **Cost** = **120 USD**
      6. Accesați **Setări** > **Unități organizaționale** și atașați lista cu prețuri de cost **Ratele de cost Contoso Robotics USA** la unitatea organizațională **Contoso Robotics USA**.
      7. Accesați **Vânzări** > **Liste de prețuri**. Creați o listă de prețuri de vânzare numită **Ratele facturilor Adventure Works**. 
      8. În lista de prețuri de vânzare, creați o înregistrare cu următoarele informații:
          - **Rol** = **Dezvoltator**
          - **Firmă de resurse** = **Contoso Robotics UK**
          - **Rata de facturare** = **200 USD**
      9. Accesați **Vânzări** > **Contracte de proiect** și atașați lista de prețuri **Ratele facturilor Adventure Works** la lista de prețuri a proiectului Adventure Works din contractul de proiect.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
