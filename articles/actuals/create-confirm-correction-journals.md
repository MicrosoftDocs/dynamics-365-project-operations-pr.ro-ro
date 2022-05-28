---
title: Creați și confirmați jurnalele de corecție
description: Acest subiect oferă informații despre cum să creați și să confirmați un jurnal de corecție.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: c15db854e3d130150ad7afc707a126b37c57f62d
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582818"
---
# <a name="create-and-confirm-correction-journals"></a>Creați și confirmați jurnalele de corecție

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Ocazional, o intrare de timp sau de cheltuieli poate fi introdusă incorect. De exemplu, un consultant poate selecta data greșită atunci când creează o intrare de timp sau ar putea selecta proiectul greșit atunci când introduce o cheltuială. Dacă un consultant nu poate actualiza intrările trimise, un administrator back-end poate corecta direct datele reale pentru un proiect.

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

 
## <a name="correct-approved-expense-entries"></a>Intrări de cheltuieli aprobate corect

Urmați pașii următori pentru a corecta una sau mai multe intrări de cheltuieli. 

1. În zona **Vânzări**, în panoul de navigare din stânga, sub **Tranzacții**, selectați **Cheltuieli aprobate**.

2. În lista **Cheltuieli aprobate**, selectați proiectul pe care doriți să îl corectați, apoi selectați **Corectați intrările**. Un nou jurnal de corecție va fi creat automat, cu tipul alocat **Corecție de cheltuială**. 

3. Din pagina **Jurnal nou**, introduceți o **Descriere** pentru corecție și din fila **Corecție cheltuieli**, în secțiunea **Valori noi pentru cheltuieli**, selectați câmpurile de date pe care doriți să le corectați pentru liniile de cheltuieli selectate. De exemplu, puteți atribui cheltuielile altui **Proiect**, sau corecta **Categoria de cheltuieli**, **Data cheltuielilor**, sau **Resursă rezervabilă**.

4. Selectați **Previzualizare**. În caseta de dialog, selectați **OK**. 

5. Verificați corecțiile de pe fila **Linii de jurnal**. Puteți vedea o listă cu datele reale originale care sunt legate de intrările de cheltuieli selectate care au fost inversate și liniile corespunzătoare corectate care au fost create.

6. Când valorile corectate apar așa cum este așteptat, selectați **Confirmare**. În caseta de dialog, selectați **OK.** Dacă valorile nu se afișează așa cum este așteptat, selectați **Anulare** pentru a reveni la lista **Cheltuieli aprobate**. Repetați pașii 2 până la 5. 

7. După ce confirmați jurnalul de corecție, reveniți la proiectul sau proiectele pe care le-ați actualizat pentru a vedea modificările.

8. Pe pagina proiectului, pe **Actuale** fila, revizuiți **Vedere asociată reală** listă. Sunt enumerate intrările originale și intrările corectate.


## <a name="correct-approved-material-usage-logs"></a>Corectați jurnalele de utilizare a materialelor aprobate

Parcurgeți următorii pași pentru a corecta una sau mai multe intrări din jurnalul de utilizare a materialelor.

1. În **Vânzări** zonă, în panoul de navigare din stânga, sub **Tranzacții**, Selectați **Actuale**.

2. În **Actuale** listă, utilizați filtre de coloană pentru a selecta **Material** clasa de tranzacție, astfel încât să fie afișate doar valorile reale pentru materiale. Utilizați alte filtre de coloană pentru a limita și mai mult valorile reale afișate. După ce puteți găsi setul dorit de valori reale, selectați datele reale, apoi selectați **Intrări corecte**. Un nou jurnal de corecție este creat automat și **Corecție materială** este atribuit tipul.

3. Pe **Jurnal nou** pagina, în **Descriere** câmp, introduceți o descriere pentru corecție. Apoi, pe **Corectarea materialului** fila, în **Noi valori pentru materiale** secțiunea, selectați câmpurile de date de corectat pentru liniile de material selectate. De exemplu, puteți atribui materialul unui alt proiect sau puteți corecta produsul, data materialului sau subcontractul.

4. Selectați **Previzualizare**. Apoi, în caseta de dialog, selectați **Bine**.

5. Pe **Rânduri de jurnal** fila, verificați corecțiile. Puteți vizualiza o listă cu valorile reale originale care sunt legate de intrările de material selectate care au fost inversate și liniile corespunzătoare corectate care au fost create.

6. Când valorile corectate apar așa cum este așteptat, selectați **Confirmare**. Apoi, în caseta de dialog, selectați **Bine**. Dacă valorile nu sunt cele așteptate, selectați **Anulare** a reveni la **Actuale** listă. Apoi repetați pașii de la 2 la 5.

7. După ce confirmați jurnalul de corecție, reveniți la proiectul sau proiectele pe care le-ați actualizat pentru a vedea modificările.

8. Pe pagina proiectului, pe **Actuale** fila, revizuiți **Vedere asociată reală** listă. Sunt enumerate intrările originale și intrările corectate.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
