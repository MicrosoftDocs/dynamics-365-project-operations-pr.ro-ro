---
title: Concepte de estimare financiară
description: Acest articol oferă informații despre estimările financiare ale proiectelor în Operațiuni de proiect.
author: rumant
ms.date: 03/22/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f8a4c3dd31cf5612c352331891178ac0ab852921
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931023"
---
# <a name="financial-estimation-concepts"></a>Concepte de estimare financiară

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

În Dynamics 365 Project Operations, vă puteți estima financiar proiectele în două etape: 
1. În etapa de pre-vânzare înainte ca afacerea să fie câștigată. 
2. În etapa de execuție după crearea contractului de proiect. 

Puteți crea o estimare financiară pentru lucrările bazate pe proiecte utilizând oricare dintre următoarele 3 pagini:
- Pagina **Linie de ofertă**, folosind detaliile liniei de ofertă.  
- Pagina **Linie de ofertă**, folosind detaliile liniei de contract. 
- Pagina **Proiect**, folosind paginile de file **Sarcini** sau **Estimări de cheltuieli**.

## <a name="use-a-project-quote-to-create-an-estimate"></a>Utilizați o ofertă de proiect pentru a crea o estimare
Pe o ofertă bazată pe proiect, aveți posibilitatea să utilizați entitatea **Detaliu linie de ofertă** pentru a estima activitatea necesară pentru livrarea unui proiect. Apoi puteți partaja această estimare cu clientul.

Liniile de ofertă bazate pe proiect pot avea zero sau mai multe detalii de linie de ofertă. Detaliile liniei de ofertă sunt utilizate pentru estimarea timpului, a cheltuielilor sau a taxelor. Microsoft Dynamics 365 Project Operations nu permite estimarea materialelor la detaliile liniei de ofertă. Acestea sunt numite clase de tranzacții. Sumele estimate de impozit pot fi, de asemenea, introduse într-o clasă de tranzacții.

Pe lângă clasele de tranzacții, detaliile liniei de ofertă au un tip de tranzacție. Două tipuri de tranzacții sunt acceptate pentru detaliile liniei de ofertă: **Cost** și **Contract de proiect**.

## <a name="use-a-project-contract-to-create-an-estimate"></a>Utilizați un contract de proiect pentru a crea o estimare

Dacă ați utilizat o ofertă când ați creat un contract bazat pe proiect, estimarea pe care ați făcut-o pentru fiecare linie de ofertă din ofertă este copiată în contractul proiectului. Structura unui contract de proiect este ca structura ofertei de proiect care are linii, detalii linie și programări de facturi.

Estimările se pot face direct într-un contract de proiect, ca într-o ofertă de proiect. Pentru o ofertă de proiect, estimarea se face utilizând liniile de contract și detaliile liniei de contract. Detaliile liniei de contract pot fi generate și dintr-un plan de proiect care a fost creat utilizând abordarea estimativă de jos în sus.

Detaliile liniei de contract pot fi utilizate pentru a estima timpul, cheltuielile sau comisioanele. Sumele estimate de impozitare pot fi, de asemenea, introduse într-un detaliu de linie de contract.

Estimările de materiale nu sunt permite pe detaliile liniei de contract.

## <a name="use-a-project-to-create-an-estimate"></a>Utilizați un proiect pentru a crea o estimare 

Puteți estima timpul și cheltuielile pentru proiecte. Project Operations nu acceptă estimări de materiale sau taxe pentru proiecte.

Estimările de timp sunt generate atunci când creați o activitate și identificați atributele unei resurse generice necesare pentru a efectua activitatea. Estimările de timp sunt generate de activitățile planificate. Estimările de timp nu sunt create dacă creați membrii de echipă generici în afara contextului planificării.

Estimările de cheltuieli sunt introduse în grila de pe pagina **Estimări cheltuieli**.

Crearea unei estimări pentru un proiect este considerată o bună practică, deoarece puteți crea estimări detaliate de jos în sus pentru forță de muncă sau timp și cheltuieli pentru fiecare sarcină din planul de proiect. Puteți utiliza apoi această estimare detaliată pentru a crea estimări pentru fiecare linie de ofertă și pentru a crea o ofertă mai credibilă pentru client. Când importați sau creați o estimare detaliată pe linia de ofertă utilizând planul de proiect, Project Operations importă valorile vânzărilor și valorile costurilor acestor estimări. După import, puteți vizualiza valorile rentabilității, marjelor și fezabilității în oferta de proiect.

## <a name="understanding-estimates"></a>Înțelegerea estimărilor

Utilizați următorul tabel ca un ghid pentru înțelegerea logicii de afaceri în faza de estimare.

| Scenariu                                                                                                                                                                                                                                                                                                                                          | Înregistrare de entitate                                                                                                                                                                                                       | Tip de tranzacție | Clasă de tranzacții | Informații suplimentare                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------|-------------|-----------------------------------------------------------------------------------|
| Când trebuie să estimați valoarea vânzărilor de timp privind o ofertă                                                                                                                                                                                                                                                                                    | Se creează înregistrarea detaliilor liniei de ofertă (QLD)                                                                                                                                                                               | Contract pentru proiect | Time        | Câmpul origine tranzacție de pe rândul QLD partea de vânzări face trimitere la QLD pe partea costului |
|                                                                                                                                                                                                                                                                                     | O a doua înregistrare QLD este creată de sistem pentru stocarea valorilor de cost corespunzătoare. Toate câmpurile non-monetare sunt copiate din QLD de vânzări în QLD cost de către sistem.                                                                                                                                                                               | Cost | Time        | Câmpul origine tranzacție pe rândul (QLD) cu detalii de linie ofertă pe partea de vânzări face trimitere la QLD pe partea costului |
| Când trebuie să estimați valoarea vânzărilor de timp în cazul unui contract                                                                                                                                                                                                                                                                                 | Înregistrarea detaliului linie contract pentru proiect (CLD) este creată                                                                                                                                                                    | Contract de proiect | Time        | Câmpul origine tranzacție pe rândul CLD pe partea de vânzări face trimitere la CLD cost      |
|                                                                                                                                                                                                                                                                                  | O a doua înregistrare CLD este creată de sistem pentru stocarea valorilor de cost corespunzătoare. Toate câmpurile non-monetare sunt copiate din CLD vânzări la CLD cost de către sistem.                                                                                                                                                                    | Cost | Time        | Câmpul origine tranzacție pe rândul CLD pe partea de vânzări face trimitere la CLD cost      |
| Când utilizatorul descrie o resursă pe o activitate de proiect                                                                                                                                                                                                                                                                                            | Înregistrarea liniei estimate pentru a afișa valoarea vânzărilor activității este creată atunci când o activitate este creată cu toate dimensiunile de preț necesare. Rolul și unitățile organizatorice sunt dimensiunile de prețuri | Contract pentru proiect | Timp        |                                                                                   |
|     | Înregistrarea liniei estimate pentru a afișa valoarea costului activității este creată atunci când este creată o activitate cu toate dimensiunile de preț necesare. Toate câmpurile non-monetare sunt copiate din linia estimată de vânzări la linia estimată de costuri de către sistem. Rolul și unitatea organizațională sunt dimensiuni de prețuri, atât pentru de cost, cât și de facturare.                                                                                                                                                                                                                | Cost             | Timp           |                                                                                   |



## <a name="customize-the-quote-line-detail-and-contract-line-detail-entities"></a>Particularizați entitățile detaliu linie de ofertă și detaliu linie de contract

Dacă ați adăugat un câmp particularizat în detaliul liniei de ofertă și doriți ca sistemul să introducă valoarea câmpului ca valoare implicită pe linia de cost corelată pe care o creează, utilizați instrumentele insert de preînregistrare **PreOperationContractLineDetailUpdate** și **PreOperationQuoteLineDetailUpdate**. Aceste inserturi trebuie reînregistrate după ce detaliul liniei de ofertă sau detaliul liniei de contract se modifică. Urmați acești pași pentru a finaliza procesul.

1. Deschideți PluginRegistrationTool și conectați-vă la instanța dvs. online.
2. Selectați **Căutare** și căutați insertul pentru actualizare.
3. Selectați insertul, apoi, în pagina principală, faceți clic pe **Selectare**.
4. Selectați pasul insertului pentru a actualiza, faceți clic dreapta, iar apoi selectați **Actualizare**.
5. În caseta de dialog **Actualizarea pasului existent**, în câmpul **Filtrarea atributelor**, selectați butonul puncte de suspensie (**...**):
6. În caseta de dialog **Selectare atribute**, bifați casetele de selectare pentru atributele particularizate.
7. Selectați **OK** pentru a închide caseta de dialog, apoi selectați **Actualizați pasul**.
8. Repetați pașii de la 1 la 7 pentru al doilea insert.
9. Închideți **PluginRegistrationTool**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
