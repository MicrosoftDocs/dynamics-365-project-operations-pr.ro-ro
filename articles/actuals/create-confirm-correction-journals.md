---
title: Creați și confirmați jurnalele de corecție
description: Acest subiect oferă informații despre cum să creați și să confirmați un jurnal de corecție.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: f12cdba286a9e29e2c4eb4041effbe779cba65f3562684d625b21bc3bae809d6
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986731"
---
# <a name="create-and-confirm-correction-journals"></a>Creați și confirmați jurnalele de corecție

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Ocazional, o intrare de timp sau de cheltuială poate fi introdusă incorect. De exemplu, un consultant ar putea selecta data greșită atunci când creează o intrare de timp sau ar putea transpune numerele la intrarea unei cheltuieli. Dacă un consultant nu poate efectua actualizările intrărilor trimise, un administrator poate corecta direct intrarea pentru un proiect.

Pentru a finaliza procedurile din acest subiect, veți avea nevoie de permisiuni de administrator.

## <a name="correct-approved-time-entries"></a>Intrări de timp aprobate corect     

Urmați pașii următori pentru a corecta intrările de timp unice sau multiple pentru un proiect.

1. În zona **Vânzări**, selectați **Tranzacții**, apoi selectați **Timp aprobat**. 

2. În lista **Timp aprobat**, localizați și selectați una sau mai multe intrări de timp aprobate pentru a fi corectate. Puteți utiliza filtrul pentru a localiza intrările conexe. De exemplu, puteți filtra pentru un ID de proiect și puteți selecta toate intrările de timp aprobate cu acel ID de proiect.

3. Selectați **Corectați intrările**. Un nou jurnal de corecție este creat automat, cu tipul alocat **Corecție de timp**. Intrările selectate sunt adăugate în jurnal. 

4. Din pagina **Jurnal nou**, introduceți o **Descriere** pentru jurnalul de corectare, apoi selectați fila **Corecții intrări de timp**.  

5. În secțiunea **Valori noi pentru intrările de timp**, actualizați câmpurile cu informațiile corecte, după caz. De exemplu, puteți modifica proiectul alocat sau resursa rezervabilă.

6. Selectați **Previzualizare**. În caseta de dialog, selectați **OK**. Pe fila **Linii de jurnal**, puteți vedea o listă cu datele reale originale care sunt legate de intrările de timp selectate care au fost inversate și liniile corespunzătoare corectate care au fost create. Dacă trebuie efectuate corecții suplimentare, repetați pașii 5 și 6. 

> [!NOTE]
> Toate datele reale corectate vor avea aceleași valori pe care le-ați selectat în secțiunea **Valori noi pentru intrările de timp**.

7. Când corecțiile apar așa cum este așteptat, selectați **Confirmare**. În caseta de dialog, selectați **OK**.

8. Reveniți la zona **Vânzări**, selectați **Proiecte**, apoi deschideți proiectul pentru care tocmai ați actualizat intrările de timp. 

9. Din pagina **Proiecte**, pe fila **Date reale**, vizualizați modificările pe care le-ați făcut. 

> [!NOTE]
> Dacă fila **Date reale** nu este vizibilă, selectați **Date reale** > **asociate**.  

10. În lista **Vizualizare asociată valori reale**, puteți vedea că intrările de timp originale care au fost inversate sunt încă listate, la fel și intrările de timp corectate corespunzătoare. 

De exemplu, în graficul următor, există două elemente linie cu o cantitate de 8,00 care au debite listate în coloana Sumă. În plus, există două elemente linie cu o cantitate de -8,00 care arată sumele creditate în coloana Sumă. Aceste corecții aduc cantitatea la zero.

 
## <a name="correct-approved-expense-entries"></a>Intrări de cheltuieli aprobate corect

Urmați pașii următori pentru a corecta una sau mai multe intrări de cheltuieli. 

1. În zona **Vânzări**, în panoul de navigare din stânga, sub **Tranzacții**, selectați **Cheltuieli aprobate**.

2. În lista **Cheltuieli aprobate**, selectați proiectul pe care doriți să îl corectați, apoi selectați **Corectați intrările**. Un nou jurnal de corecție va fi creat automat, cu tipul alocat **Corecție de cheltuială**. 

3. Din pagina **Jurnal nou**, introduceți o **Descriere** pentru corecție și din fila **Corecție cheltuieli**, în secțiunea **Valori noi pentru cheltuieli**, selectați câmpurile de date pe care doriți să le corectați pentru liniile de cheltuieli selectate. De exemplu, puteți atribui cheltuielile altui **Proiect**, sau corecta **Categoria de cheltuieli**, **Data cheltuielilor**, sau **Resursă rezervabilă**.

4. Selectați **Previzualizare**. În caseta de dialog, selectați **OK**. 

5. Verificați corecțiile de pe fila **Linii de jurnal**. Puteți vedea o listă cu datele reale originale care sunt legate de intrările de cheltuieli selectate care au fost inversate și liniile corespunzătoare corectate care au fost create.

6. Când valorile corectate apar așa cum este așteptat, selectați **Confirmare**. În caseta de dialog, selectați **OK.** Dacă valorile nu se afișează așa cum este așteptat, selectați **Anulare** pentru a reveni la lista **Cheltuieli aprobate**. Repetați pașii 2 până la 5. 

> [!NOTE]
> Datele reale corectate vor avea aceleași valori pe care le-ați selectat în secțiunea **Valori noi pentru cheltuieli**.

7. După ce confirmați jurnalul de corecție, navigați înapoi la proiectul sau proiectele pe care le-ați actualizat, pentru a vizualiza modificările.  

8. În pagina proiectului, pe fila **Date reale**, treceți în revistă **Vizualizare asociată valori reale**. Sunt enumerate intrările originale și intrările corectate. Următorul grafic arată sumele de intrare pentru cheltuieli originale și sumele corespunzătoare de intrare ale cheltuielilor corectate. 




[!INCLUDE[footer-include](../includes/footer-banner.md)]