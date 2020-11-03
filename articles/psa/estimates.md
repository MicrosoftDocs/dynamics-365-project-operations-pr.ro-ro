---
title: Estimări
description: Acest subiect oferă informații despre estimări în Dynamics 365 Project Service Automation.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 1/31/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: e21511f78d92ff672e462f63f0dd0d098578516a
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082998"
---
# <a name="estimates"></a>Estimări

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Pe o ofertă bazată pe proiect, aveți posibilitatea să utilizați entitatea Detaliu linie de ofertă pentru a estima activitatea necesară pentru livrarea unui proiect. Apoi puteți partaja această estimare cu clientul.

Liniile de ofertă bazate pe proiect nu trebuie să aibă detalii despre linia de ofertă. Alternativ, ele pot avea multe detalii despre linia de ofertă. Detaliile liniei de ofertă sunt utilizate pentru estimarea timpului, a cheltuielilor sau a taxelor. PSA nu permite estimarea materialelor privind detaliile liniei de ofertă. Acestea sunt numite clase de tranzacții. Sumele estimate de impozit pot fi, de asemenea, introduse într-o clasă de tranzacții.

Pe lângă clasele de tranzacții, detaliile liniei de ofertă au un tip de tranzacție. PSA acceptă două tipuri de tranzacții pentru detaliile liniei de ofertă: **Cost** și **Contract de proiect**.

## <a name="estimate-by-using-a-contract"></a>Estimați prin utilizarea unui contract

Dacă ați utilizat o ofertă PSA când ați creat un contract bazat pe proiect, estimarea pe care ați făcut-o pentru fiecare linie de ofertă din ofertă este copiată în contractul proiectului. Structura unui contract de proiect este ca structura ofertei de proiect care are linii, detalii linie și programări de facturi.

Estimările se pot face direct într-un contract de proiect, ca într-o ofertă de proiect. Pentru o ofertă de proiect, estimarea se face utilizând liniile de contract și detaliile liniei de contract. Detaliile liniei de contract pot fi generate și dintr-un plan de proiect care a fost creat utilizând abordarea estimativă de jos în sus.

Detaliile liniei de contract pot fi utilizate pentru a estima timpul, cheltuielile sau comisioanele. Sumele estimate de impozitare pot fi, de asemenea, introduse într-un detaliu de linie de contract.

PSA nu permite estimări materiale în detaliile liniei de contract.

Procesele care sunt acceptate într-un contract de proiect sunt crearea și confirmarea facturii. Crearea facturii creează o schiță a unei facturi bazate pe proiect care include toate valorile reale de vânzări nefacturate până la data curentă.

Confirmarea trece contractul în starea „doar în citire” și îi modifică starea din **Schiță** în **Confirmat**. După ce întreprindeți această acțiune, nu o mai puteți anula. Întrucât această acțiune este permanentă, este cea mai bună practică de a menține contractul într-o stare **Schiță**.

Singurele diferențe dintre contractele schiță și contractele confirmate le reprezintă statutul lor și faptul că contractele schiță pot fi editate, în timp ce contractele confirmate nu pot. Crearea facturii și valorile reale de urmărire se pot face atât în cazul proiectelor de contracte, cât și al contractelor confirmate.

PSA nu acceptă modificarea comenzilor în cazul contractelor sau proiectelor.

## <a name="estimating-projects"></a>Estimarea proiectelor

Puteți estima timpul și cheltuielile pentru proiecte. PSA nu permite estimări pentru materiale sau taxe pe proiecte.

Estimările de timp sunt generate atunci când creați o activitate și identificați atributele unei resurse generice necesare pentru a efectua activitatea. Estimările de timp sunt generate de activitățile planificate. Estimările de timp nu sunt create dacă creați membrii de echipă generici în afara contextului planificării.

Estimările de cheltuieli sunt introduse în grila de pe pagina **Estimări**.

## <a name="understanding-estimation"></a>Înțelegerea estimării

Utilizați următorul tabel ca un ghid pentru înțelegerea logicii de afaceri în faza de estimare.

| Scenariu                                                                                                                                                                                                                                                                                                                                          | Înregistrarea entității                                                                                                                                                                                                       | Tip de tranzacție | Clasă de tranzacții | Informații suplimentare                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------|-------------|-----------------------------------------------------------------------------------|
| Când trebuie să estimați valoarea vânzărilor de timp privind o ofertă                                                                                                                                                                                                                                                                                    | Se creează înregistrarea detaliilor liniei de ofertă (QLD)                                                                                                                                                                               | Contract pentru proiect | Time        | Câmpul origine tranzacție de pe rândul QLD partea de vânzări face trimitere la QLD pe partea costului |
|                                                                                                                                                                                                                                                                                     | O a doua înregistrare QLD este creată de sistem pentru stocarea valorilor de cost corespunzătoare. Toate câmpurile non-monetare sunt copiate din QLD de vânzări în QLD cost de către sistem.                                                                                                                                                                               | Cost | Time        | Câmpul origine tranzacție pe rândul (QLD) cu detalii de linie ofertă pe partea de vânzări face trimitere la QLD pe partea costului |
| Când trebuie să estimați valoarea vânzărilor de timp în cazul unui contract                                                                                                                                                                                                                                                                                 | Înregistrarea detaliului linie contract pentru proiect (CLD) este creată                                                                                                                                                                    | Contract de proiect | Time        | Câmpul origine tranzacție pe rândul CLD pe partea de vânzări face trimitere la CLD cost      |
|                                                                                                                                                                                                                                                                                  | O a doua înregistrare CLD este creată de sistem pentru stocarea valorilor de cost corespunzătoare. Toate câmpurile non-monetare sunt copiate din CLD vânzări la CLD cost de către sistem.                                                                                                                                                                    | Cost | Time        | Câmpul origine tranzacție pe rândul CLD pe partea de vânzări face trimitere la CLD cost      |
| Când utilizatorul descrie o resursă pe o activitate de proiect                                                                                                                                                                                                                                                                                            | Înregistrarea liniei estimate pentru a afișa valoarea vânzărilor activității este creată atunci când o activitate este creată cu toate dimensiunile de preț necesare. Rolul și unitățile organizatorice sunt dimensiunile de prețuri OOB Project Service | Contract de proiect | Time        |                                                                                   |
|     | Înregistrarea liniei estimate pentru a afișa valoarea costului activității este creată atunci când este creată o activitate cu toate dimensiunile de preț necesare. Toate câmpurile non-monetare sunt copiate din linia estimată de vânzări la linia estimată de costuri de către sistem. Rolul și unitatea organizațională sunt dimensiuni de prețuri OOB PSA pentru ambele rate de cost și de facturare.                                                                                                                                                                                                                | Cost             | Time           |                                                                                   |



## <a name="customizing-the-quote-line-detail-and-contract-line-detail-entities"></a>Particularizarea entităților detaliu linie de ofertă și detaliu linie de contract

Dacă ați adăugat un câmp particularizat în detaliul liniei de ofertă și doriți ca sistemul să introducă valoarea câmpului ca valoare implicită pe linia de cost corelată pe care o creează, utilizați instrumentele de înregistrare a insertului PreOperationContractLineDetailUpdate și PreOperationQuoteLineDetailUpdate. Aceste inserturi trebuie reînregistrate după ce detaliul liniei de ofertă sau detaliul liniei de contract se modifică. Urmați acești pași pentru a finaliza procesul.

1. Deschideți PluginRegistrationTool și conectați-vă la instanța dvs. online.
2. Selectați **Căutare** și căutați insertul pentru actualizare.

    ![Caseta de dialog Căutare structură](media/basic-guide-19.png)

3. Selectați insertul, apoi, în pagina principală, selectați **Selectare**.
4. Selectați pasul insertului pentru a actualiza, faceți clic dreapta, iar apoi selectați **Actualizare**.

    ![Selectarea unui pas în insert](media/basic-guide-20.png)

5. În caseta de dialog **Actualizarea pasului existent** , în câmpul **Filtrarea atributelor** , selectați butonul puncte de suspensie ( **...** ):
 
    ![Actualizați caseta de dialog Pas existent](media/basic-guide-21.png)

6. În caseta de dialog **Selectare atribute** , bifați casetele de selectare pentru atributele particularizate.

    ![Selectați caseta de dialog Atribute](media/basic-guide-22.png)

7. Selectați **OK** pentru a închide caseta de dialog, apoi selectați **Actualizați pasul**.
 
    ![Buton Actualizați pasul](media/basic-guide-23.png)

8. Repetați pașii de la 1 la 7 pentru al doilea insert.
9. Închideți PluginRegistrationTool.
