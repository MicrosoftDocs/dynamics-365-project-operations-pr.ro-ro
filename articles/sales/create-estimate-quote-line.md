---
title: Crearea de estimări într-o linie de ofertă
description: Acest subiect oferă informații despre cum să creați o estimare pe o linie de ofertă pentru un proiect.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: e841ab7c37e0b348a4d1570123a5aea00ede0047
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898502"
---
# <a name="create-estimates-on-a-quote-line"></a>Crearea de estimări într-o linie de ofertă

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Pe o ofertă bazată pe proiect, aveți posibilitatea să utilizați entitatea Detaliu linie de ofertă pentru a estima activitatea necesară pentru livrarea unui proiect. Apoi puteți partaja această estimare cu clientul.

Liniile de ofertă bazate pe proiect nu trebuie să aibă detalii despre linia de ofertă. Alternativ, ele pot avea multe detalii despre linia de ofertă. Detaliile liniei de ofertă sunt utilizate pentru estimarea timpului, a cheltuielilor sau a taxelor. Project Operations Dynamics 365 nu permite estimarea materialelor privind detaliile liniei de ofertă. Acestea sunt numite clase de tranzacții. Sumele estimate de impozit pot fi, de asemenea, introduse într-o clasă de tranzacții.

Pe lângă clasele de tranzacții, detaliile liniei de ofertă au un tip de tranzacție. Sunt două tipuri de tranzacții pentru detaliile liniei de ofertă, **Cost** și **Contract de proiect**.

## <a name="estimate-by-using-a-contract"></a>Estimați prin utilizarea unui contract

Dacă ați utilizat o ofertă de Project Operations când ați creat un contract bazat pe proiect, estimarea pe care ați făcut-o pentru fiecare linie de ofertă din ofertă este copiată în contractul proiectului. Structura unui contract de proiect este ca structura ofertei de proiect care are linii, detalii linie și programări de facturi.

Estimările se pot face direct într-un contract de proiect, ca într-o ofertă de proiect. Pentru o ofertă de proiect, estimarea se face utilizând liniile de contract și detaliile liniei de contract. Detaliile liniei de contract pot fi generate și dintr-un plan de proiect care a fost creat utilizând abordarea estimativă de jos în sus.

Detaliile liniei de contract pot fi utilizate pentru a estima timpul, cheltuielile sau comisioanele. Sumele estimate de impozitare pot fi, de asemenea, introduse într-un detaliu de linie de contract.

Estimările de materiale nu sunt permite pe detaliile liniei de contract.

Procesele care sunt acceptate într-un contract de proiect sunt crearea și confirmarea facturii. Crearea facturii creează o schiță a unei facturi bazate pe proiect care include toate valorile reale de vânzări nefacturate până la data curentă.

Confirmarea trece contractul în starea „doar în citire” și îi modifică starea din **Schiță** în **Confirmat**. După ce întreprindeți această acțiune, nu o mai puteți anula. Întrucât această acțiune este permanentă, este cea mai bună practică de a menține contractul într-o stare **Schiță**.

Singurele diferențe dintre contractele schiță și contractele confirmate le reprezintă statutul lor și faptul că contractele schiță pot fi editate, în timp ce contractele confirmate nu pot. Crearea facturii și valorile reale de urmărire se pot face atât în cazul proiectelor de contracte, cât și al contractelor confirmate.

Modificările de comenzi nu sunt acceptate pe contracte sau proiecte.

## <a name="estimating-projects"></a>Estimarea proiectelor

Puteți estima timpul și cheltuielile pentru proiecte, dar nu materiale sau taxe.

Estimările de timp sunt generate atunci când creați o activitate și identificați atributele unei resurse generice necesare pentru a efectua activitatea. Estimările de timp sunt generate de activitățile planificate. Estimările de timp nu sunt create dacă creați membrii de echipă generici în afara contextului planificării.

Estimările de cheltuieli sunt introduse în grila de pe pagina **Estimări**.

## <a name="understand-estimation"></a>Înțelegeți estimarea

Utilizați următorul tabel ca un ghid pentru înțelegerea logicii de afaceri în faza de estimare.

| Scenariu                                                                                                                                                                                                                                                                                                                                          | Înregistrarea entității                                                                                                                                                                                                       | Tip de tranzacție | Clasă de tranzacții | Informații suplimentare                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------|-------------|-----------------------------------------------------------------------------------|
| Când trebuie să estimați valoarea vânzărilor de timp privind o ofertă                                                                                                                                                                                                                                                                                    | Se creează înregistrarea detaliilor liniei de ofertă (QLD)                                                                                                                                                                               | Contract pentru proiect | Time        | Câmpul origine tranzacție de pe rândul QLD partea de vânzări face trimitere la QLD pe partea costului |
|                                                                                                                                                                                                                                                                                     | O a doua înregistrare QLD este creată de sistem pentru stocarea valorilor de cost corespunzătoare. Toate câmpurile non-monetare sunt copiate din QLD de vânzări în QLD cost de către sistem.                                                                                                                                                                               | Cost | Time        | Câmpul origine tranzacție pe rândul (QLD) cu detalii de linie ofertă pe partea de vânzări face trimitere la QLD pe partea costului |
| Când trebuie să estimați valoarea vânzărilor de timp în cazul unui contract                                                                                                                                                                                                                                                                                 | Înregistrarea detaliului linie contract pentru proiect (CLD) este creată                                                                                                                                                                    | Contract de proiect | Time        | Câmpul origine tranzacție pe rândul CLD pe partea de vânzări face trimitere la CLD cost      |
|                                                                                                                                                                                                                                                                                  | O a doua înregistrare CLD este creată de sistem pentru stocarea valorilor de cost corespunzătoare. Toate câmpurile non-monetare sunt copiate din CLD vânzări la CLD cost de către sistem.                                                                                                                                                                    | Cost | Time        | Câmpul origine tranzacție pe rândul CLD pe partea de vânzări face trimitere la CLD cost      |
| Când utilizatorul descrie o resursă pe o activitate de proiect                                                                                                                                                                                                                                                                                            | Înregistrarea liniei estimate pentru a afișa valoarea vânzărilor activității este creată atunci când o activitate este creată cu toate dimensiunile de preț necesare. Rolul și unitățile organizatorice sunt dimensiunile de prețuri | Contract pentru proiect | Timp        |                                                                                   |
|     | Înregistrarea liniei estimate pentru a afișa valoarea costului activității este creată atunci când este creată o activitate cu toate dimensiunile de preț necesare. Toate câmpurile non-monetare sunt copiate din linia estimată de vânzări la linia estimată de costuri de către sistem. Rolul și unitatea organizațională sunt dimensiuni de prețuri, atât pentru de cost, cât și de facturare.                                                                                                                                                                                                                | Cost             | Timp           |                                                                                   |



## <a name="customize-the-quote-line-detail-and-contract-line-detail-entities"></a>Particularizați entitățile detaliu linie de ofertă și detaliu linie de contract

Dacă ați adăugat un câmp particularizat în detaliul liniei de ofertă și doriți ca sistemul să introducă valoarea câmpului ca valoare implicită pe linia de cost corelată pe care o creează, utilizați instrumentele de înregistrare a insertului PreOperationContractLineDetailUpdate și PreOperationQuoteLineDetailUpdate. Aceste inserturi trebuie reînregistrate după ce detaliul liniei de ofertă sau detaliul liniei de contract se modifică. Urmați acești pași pentru a finaliza procesul.

1. Deschideți PluginRegistrationTool și conectați-vă la instanța dvs. online.
2. Selectați **Căutare**și căutați insertul pentru actualizare.
3. Selectați insertul, apoi, în pagina principală, selectați **Selectare**.
4. Selectați pasul insertului pentru a actualiza, faceți clic dreapta, iar apoi selectați **Actualizare**.
5. În caseta de dialog **Actualizarea pasului existent**, în câmpul **Filtrarea atributelor**, selectați butonul puncte de suspensie (**...**):
6. În caseta de dialog **Selectare atribute**, bifați casetele de selectare pentru atributele particularizate.
7. Selectați **OK** pentru a închide caseta de dialog, apoi selectați **Actualizați pasul**.
8. Repetați pașii de la 1 la 7 pentru al doilea insert.
9. Închideți PluginRegistrationTool.
