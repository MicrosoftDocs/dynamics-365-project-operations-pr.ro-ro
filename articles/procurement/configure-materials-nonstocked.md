---
title: Configurarea materialelor care nu există pe stoc și a facturilor de la furnizori neachitate
description: Acest subiect explică modul de activare a materialelor care nu există pe stoc și a facturilor de la furnizori neachitate.
author: sigitac
ms.date: 06/22/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1b14ab17a317e7082bc9c24709590745a5c48ea8
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8592983"
---
# <a name="configure-non-stocked-materials-and-pending-vendor-invoices"></a>Configurarea materialelor care nu există pe stoc și a facturilor de la furnizori neachitate

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

## <a name="minimum-version-requirement"></a>Versiune minimă necesară

Folosirea materialelor care nu există pe stoc și a facturilor neachitate de la furnizori pentru scenariile Dynamics 365 Project Operations privind materialele care nu există pe stoc/pe baza resurselor necesită următoarele versiuni:

Soluții pentru Dynamics 365 Dataverse:

- Project Operations – 4.9.0.221 sau superior
- Soluție de orchestrare a aplicației cu scriere duală - 2.2.2.23 sau superioară

Dynamics 365 Finance:
- 10.0.18 (10.0.793.52) sau superioară. Asigurați-vă că mediul dvs. financiar este de actualitate și că toate actualizările privind calitatea sunt aplicate pentru a îndeplini cerințele minime ale versiunii.

## <a name="run-dual-write-maps-for-non-stocked-materials-and-vendor-invoice-integration"></a>Rulați hărțile cu scriere duală pentru materialele care nu există pe stoc și pentru integrarea facturilor de la furnizori

Această secțiune oferă informații despre hărțile specifice necesare pentru materialele care nu există pe stoc și pentru facturile de la furnizori. Verificați dacă hărțile preliminare menționate în subiectul [Furnizarea unui mediu nou](../environment/resource-provision-new-environment.md#run-project-operations-dual-write-maps) rulează în mediul dvs.

1. Accesați Lifecycle Services (LCS), navigați la proiectul dvs. LCS și accesați pagina **Detalii despre mediu**.
2. În secțiunea **Common Data Service Informații despre mediu**, selectați **Link către CDS for Apps**. După ce selectați linkul, veți fi redirecționat către lista entităților din mapări.
3. Asigurați-vă că următoarele hărți rulează. Dacă nu rulează, porniți-le și asigurați-vă că includeți toate hărțile aferente pe bază de tabele.

    - CDS a lansat produse distincte (produse)
    - Furnizori v2 (msdyn_vendors)
    - Tabel cu Project Operations pentru estimările privind materialele (msdyn_estimatelines)
    - Entitatea privind exportul facturilor de la furnizori în proiectul de integrare Project Operations (msdyn_projectvendorinvoices)
    - Entitatea privind exportul liniilor de factură de la furnizori în proiectul de integrare Project operations (msdyn_projectvendorinvoicelines)
    - Valori reale privind integrarea în Project Operations (msdyn_actuals). Asigurați-vă că rulați versiunea hărții 1.0.0.14 sau superioară. Puteți vedea versiunea activă a hărții în coloana **Versiune** de pe pagina **Scriere duală**. Puteți activa o nouă versiune a hărții selectând **Versiunea hărții cu tabele** și apoi salvând versiunea selectată.

Dacă utilizați date demo standard, poate fi necesar de asemenea să opriți și să reporniți următoarele hărți de entități cu sincronizare inițială:
  - Zile de plată CDS V2 (msdyn_paymentdays)
  - Calendar de plăți (msdyn_paymentschedules)
  - Termeni de plată (msdyn_paymentterms)
  - Grupuri de furnizori (msdyn_vendorgroups)
  - Unități (uom)

> [!NOTE]
> Sincronizarea inițială pentru grupurile și unitățile de furnizori ar putea eșua în cazul câtorva înregistrări din setul de date demonstrative existente. Puteți ignora erorile, deoarece acestea nu vă vor împiedica să utilizați datele demonstrative cu Project Operations.

## <a name="configure-prerequisites-in-dataverse"></a>Configurarea cerințelor preliminare în Dataverse

### <a name="activate-workflow-to-create-accounts-based-on-vendor-entity"></a>Activați fluxul de lucru pentru a crea conturi bazate pe entitatea furnizorului

Soluția de orchestrare cu scriere duală oferă [Integrarea principală a furnizorilor](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/vendor-mapping). Ca o condiție prealabilă pentru această caracteristică, datele furnizorului trebuie create în entitatea **Conturi**. Activați un proces privind fluxul de lucru tip șablon pentru a crea furnizori în tabelul **Conturi** așa cum este descris în [Comutați între proiectele furnizorilor](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/vendor-switch).

### <a name="set-products-to-be-created-as-active"></a>Setați ca produsele să fie create ca active

Materialele care nu există pe stoc trebuie să fie configurate ca **Produse lansate** în Finanțe. Soluția de orchestrare cu scriere duală oferă o [Integrare a produselor lansate în Catalogul de produse Dataverse](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/product-mapping) neconvențională. În mod implicit, produsele de la Finanțe sunt sincronizate cu Dataverse sub formă de schiță. Pentru a sincroniza produsul la o stare activă, astfel încât să poată fi utilizat direct în documentele de utilizare a materialelor sau în facturile de la furnizori neachitate, accesați **Sistem** > **Administrare** > **Administrarea sistemului** > **Setările sistemului** și pe fila **Vânzări**, setați **Creați produse în starea activă** la **Da**.

## <a name="configure-prerequisites-in-finance"></a>Configurarea cerințelor preliminare în Finanțe

### <a name="enable-the-feature-key-for-pending-vendor-invoices"></a>Activarea caracteristicii cheie pentru facturile neachitate de la furnizori

Parcurgeți pașii următori pentru a activa funcționalitatea de a adăuga detalii ale proiectului la liniile din cadrul facturilor neachitate de la furnizori.

1. În Finanțe, accesați spațiul de lucru **Administrarea caracteristicilor**.
2. În lista de caracteristici, găsiți caracteristica **Activați facturile neachitate de la furnizori de la Project Operations pentru scenarii bazate pe resurse/cu materiale care nu există pe stoc** și selectați **Activare**.

### <a name="define-category-groups-and-project-categories-for-items"></a>Definirea grupurilor de categorii și categoriilor de proiecte pentru elemente

Configurați cel puțin un grup de categorii pentru tipul de tranzacție **Articol** și cel puțin o categorie de proiect care utilizează acest grup. Pentru mai multe informații, consultați [Configurați categoriile de proiect](../project-accounting/configure-project-categories.md#category-groups).

Revizuiți costurile proiectului și profilurile veniturilor și configurați setarea privind postarea în registrul contabil în cazul tranzacțiilor cu articole. Pentru mai multe informații, consultați [Configurarea contabilității pentru proiectele facturabile](../project-accounting/configure-accounting-billable-projects.md).

### <a name="set-up-a-write-in-product"></a>Configurarea unui produs din afara catalogului

În Project Operations, puteți înregistra estimările și utilizările materialelor pentru produsele din catalog care sunt configurate în catalogul de produse lansat și pentru produsele din afara catalogului. Utilizarea produselor din afara catalogului necesită un singur produs lansat, care este configurat în Finanțe în acest scop. Parcurgeți pașii următori pentru a configura un produs din afara catalogului. Repetați acești pași în cazul fiecărei entități juridice care utilizează Project Operations pentru scenarii privind resursele/materialele care nu există pe stoc.

1. În Finanțe, accesați **Managementul informațiilor despre produse** > **Produse** > **Produse lansate** și selectați **Noi**.
2. În câmpul **Tip produs**, selectați **Articol** și în câmpul **Subtipul produsului**, selectați **Produs**.
3. Introduceți numărul produsului (WRITEIN) și numele produsului (Produs din afara catalogului).
4. Selectați grupul cu modele de articole. Asigurați-vă că grupul cu modele de articole pe care îl selectați are câmpul **Politica de inventar privind Produsul stocat** setat la **Fals**.
5. Selectați valorile din câmpurile **Grupul cu articole**, **Grupul privind dimensiunea de stocare** și **Grupul privind dimensiunea de urmărire**. Utilizați **Dimensiunea de stocare** numai pentru **Site** și în câmpul **Dimensiuni de urmărire**, selectați **Nici unul**.
6. Selectați valorile din câmpul **Unitate de inventar**, **Unitate de achiziții** și **Unitate de vânzări**, apoi salvați-vă modificările.
7. În fila **Plan**, setați setările implicite ale comenzii și pe fila **Inventar**, setați site-ul și depozitul implicit.
8. Accesați **Management de proiect și contabilitate** > **Configurare** > **Management de proiect și parametrii contabili** și deschideți **Project Operations pe Dynamics 365 Dataverse**. 
9. Pe fila **Materiale**, în câmpul **Produs din afara catalogului**, selectați produsul pe care l-ați creat.
10. În mediul dumneavoastră Dataverse, pe harta site-ului, deschideți entitatea **Produse** și găsiți înregistrarea cu produsul din afara catalogului. 
11. Deschideți detaliile înregistrării și setați starea produsului la **Retras**. Această stare a produsului împiedică pe oricine să folosească accidental această înregistrare direct în estimările de materiale și în documentele de utilizare.

### <a name="set-up-a-procurement-integration-account"></a>Configurați un cont de integrare a achizițiilor

Contul de integrare a achizițiilor este utilizat drept cont de compensare atunci când se postează o factură de la furnizor neachitată, cu linii, atribuite unui proiect.

Când sistemul postează o factură de la furnizori neachitată, acest cont este utilizat pentru suma reprezentând costul proiectului. Detaliile facturilor de la furnizor sunt procesate în Dataverse și se creează o valoare reală a proiectului corespunzător. Informațiile din valorile reale ale proiectului sunt adăugate în Jurnalul de integrare Project Operations. Când postați jurnalul de integrare, suma este ștearsă din contul de integrare al achizițiilor și este înregistrată în costul proiectului.

1. Pentru a configura contul de integrare a achizițiilor, accesați **Management de proiect și contabilitate** > **Configurare** > **Management de proiect și parametrii contabili** și deschideți **Project Operations pe Dynamics 365 Dataverse**. 
2. Selectați fila **Materiale** și selectați o valoare în câmpul **Cont de integrare a achizițiilor**.

#### <a name="set-up-project-category-defaults-for-an-item"></a>Configurați valorile implicite ale categoriei de proiect pentru un articol

1. În Finanțe, accesați **Management de proiect și contabilitate** > **Configurare** > **Management de proiect și parametrii contabili** și deschideți **Project Operations pe Dynamics 365 Dataverse**. 
2. Pe fila **Categorii implicite de proiect**, în câmpul **Element**, selectați o valoare. Această categorie de proiect este utilizată pentru tranzacții semnificative dacă categoria de proiect nu a fost setată în înregistrarea privind valorile reale ale proiectului.
