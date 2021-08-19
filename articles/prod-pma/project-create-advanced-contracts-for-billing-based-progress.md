---
title: Crearea de contracte avansate pentru facturare pe baza progresului
description: Acest subiect explică modul de creare a contractelor de proiect, astfel încât să puteți genera facturi pentru clienți, pe baza unui procent din lucrările finalizate.
author: RadhikaRS
ms.date: 03/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 661e8aa0be70e9c8aadcb3a3d9dd6d39d1bcb2fd55d198b3c9af19fc2d0ae9d3
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/06/2021
ms.locfileid: "7000996"
---
# <a name="create-advanced-contracts-for-billing-based-on-progress"></a>Crearea de contracte avansate pentru facturare pe baza progresului
[!include [banner](../includes/banner.md)]

Acest subiect explică modul de creare a contractelor de proiect, astfel încât să puteți crea facturi pentru clienți, pe baza unui procent din lucrările finalizate. Sumele facturii sunt calculate automat pentru categoriile bugetare de lucru pe care le-ați configurat pentru un proiect. Momentul facturii este stabilit atunci când negociați contractul de proiect cu clientul.

Utilizați procedurile din acest subiect pentru a configura un contract, un proiect asociat și regulile de facturare care calculează sumele facturii pentru categoriile de lucrări bugetare pe care le-ați configurat pentru proiect.

După ce ați creat contractul și proiectul, puteți configura detaliile proiectului. De exemplu, puteți defini activități și atribui lucrători la proiect.

## <a name="example"></a>Exemplu

Organizația dvs. este o firmă de dezvoltare software. Sunteți de acord să dezvoltați un pachet de contabilitate a salariilor pentru un client pentru o taxă totală de 20.000 de dolari SUA (USD). Organizația dvs. este de acord să factureze clientul pe măsură ce completați procente specifice din proiect. Configurați următoarele categorii de proiecte pentru lucrare, astfel încât să le puteți utiliza în procesul de facturare:

- Consultanță
- Proiect
- Instalare

Puteți, de asemena, să configurați reguli de facturare care calculează automat sumele facturii pentru procentul de muncă de proiect finalizat în fiecare categorie.

Managerul bugetului creează un buget pentru categoriile de proiecte. Cantitatea lucrărilor finalizate este calculată automat ca procent din munca efectivă în comparație cu sumele bugetate.

## <a name="prerequisites"></a>Cerințe preliminare

Înainte de a crea un proiect care utilizează reguli de facturare, trebuie să configurați secvențele numerice pentru regulile de facturare și un jurnal de taxe care este utilizat pentru a înregistra facturări de progres.

1. Accesați **Gestionarea proiectelor și contabilitate** \> **Configurare** \> **Gestionarea proiectelor și parametrii contabili**.
2. Pe pagina **Managementul proiectului și parametrii contabili**, pe fila **Secvențe numerice**, configurați secvența numerică pe care doriți să o utilizați atunci când sunt create regulile de facturare.
3. Accesați **Gestionarea proiectului și contabilitate** \> **Jurnale** \> **Taxă**.
4. Pe pagina **Jurnal cu taxe**, selectați **Nou** și introduceți numele jurnalului.

## <a name="create-a-contract-for-progress-billings"></a>Creați un contract pentru facturarea progresivă

Folosiți această procedură pentru a crea un contract de proiect pentru un proiect cu preț fix. Creați o factură de proiect atunci când lucrările finalizate la proiect ating un procent specificat.

1. Accesați **Gestionarea proiectului și contabilitate** \> **Proiecte** \> **Contracte de proiect**.
2. Pe pagina **Contracte de proiect**, selectați **Nou**.
3. În caseta de dialog **Noul contract de proiect**, setați următoarele câmpuri:

    - **Nume**
    - **Tip de finanțare**
    - **Sursă de finanțare**
    - **Moneda de vânzare** - În mod implicit, această monedă este utilizată pentru facturile clienților care sunt asociate cu contractul de proiect. Cu toate acestea, puteți modifica moneda de vânzare pe o anumită factură de client.

4. Selectați **OK**. Informațiile sunt copiate în antetul paginii **Contracte de proiect**.
5. Pe pagina **Contracte de proiect**, completați restul informațiilor necesare pentru proiect.

## <a name="create-a-project-for-progress-billings"></a>Creați un proiect pentru facturarea progresivă

Urmați acești pași pentru a crea un proiect și orice subproiecte care sunt asociate cu un contract de proiect.

1. Accesați **Gestionarea proiectului și contabilitate** \> **Proiecte** \> **Toate proiectele**.
2. Pe pagina **Toate proiectele**, selectați **Nou**.
3. În caseta de dialog **Proiect nou**, în câmpul **Tipul proiectului**, selectați **Timp și material**.
4. Selectați un grup de proiect. Un grup de proiect definește informațiile de înregistrare pentru proiectele care sunt atribuite grupului.
5. Selectați **Creați un proiect**.
6. După crearea proiectului, setați etapa proiectului la **În proces**.

## <a name="create-a-budget-for-a-project"></a>Creați un buget pentru un proiect

Categoriile de buget sunt utilizate pentru a calcula automat sumele de facturi pentru procentul de muncă finalizat pentru fiecare categorie. Urmați acești pași pentru a crea categorii de buget pentru costurile estimate.

1. Accesați **Gestionarea proiectului și contabilitate** \> **Proiecte** \> **Toate proiectele**.
2. Pe pagina **Toate proiectele**, selectați și deschideți proiectul dorit.
3. Pe pagina **Proiecte**, pe panoul de acțiune, pe fila **Plan**, în grupul **Buget**, selectați **Bugetul proiectului**.
4. Pe pagina **Bugetul proiectului**, introduceți un cost estimat pentru fiecare categorie din proiect.

## <a name="create-billing-rules-for-progress-billings"></a>Creați reguli de facturare pentru facturarea progresivă

1. Accesați **Gestionarea proiectului și contabilitate** \> **Proiecte** \> **Contracte de proiect**.
2. Pe pagina **Contracte de proiect**, selectați și deschideți un contract de proiect.
3. Pe pagina contractului de proiect, pe FastTab **Regulile de facturare**, selectați **Adăugare**.
4. Pe pagina **Regula de facturare**, în câmpul **Tip de linie**, selectați **Progres**.
5. Pe FastTab **Detalii despre linia regulii de facturare**, în **Valoarea contractului**, introduceți valoarea totală a contractului.
6. În câmpul **Categorie**, selectați categoria în care să înregistrați tranzacția cu taxă.
7. În câmpul **Proiect**, selectați proiectul care utilizează această regulă de facturare.
8. Opțional: atribuiți regula de facturare proiectelor suplimentare. Pe FastTab **Proiect**, în secțiunea **Proiecte disponibile**, selectați un proiect, apoi selectați butonul săgeată dreapta pentru a adăuga proiectul la secțiunea **Proiecte selectate**.
9. Opțional: calculați suma procentuală pe care clientul o reține din plăți pe o factură. Pe FastTab **Condiții de plată a retenției**, selectați sursa de finanțare și apoi, în câmpul **Procentul de retenție**, introduceți procentul de retenție.
10. Repetați acești pași pentru a crea reguli de facturare suplimentare pentru contractul de proiect.


[!INCLUDE[footer-include](../includes/footer-banner.md)]