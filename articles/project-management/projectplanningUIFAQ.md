---
title: Depanare de funcționare în grila de activități
description: Acest subiect oferă informații legate de depanare necesare atunci când lucrați în grila de activități.
author: ruhercul
manager: tfehr
ms.date: 01/19/2021
ms.topic: article
ms.product: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: dedd989cc7c959d9ea97a0abfb13f8f1b2150a56
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286578"
---
# <a name="troubleshoot-working-in-the-task-grid"></a>Depanare de funcționare în grila de activități 

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Acest subiect descrie cum să remediați problemele care ar putea apărea în timp ce lucrați cu gestionarea costurilor.

## <a name="enable-cookies"></a>Activați module cookie

Project Operations are nevoie ca modulele cookie de la terți să fie activate pentru a reda structura detaliată a proiectului. Când modulele cookie de terță parte nu sunt activate, în loc să vedeți sarcini, veți vedea o pagină goală când selectați fila **Sarcini** de pe pagina **Proiect**.

![Fila goală când modulele cookie de terță parte nu sunt activate](media/blankschedule.png)


### <a name="workaround"></a>Soluție
Pentru browser-ele Microsoft Edge sau Google Chrome, următoarele proceduri descriu cum să actualizați setările browser-ului pentru a activa modulele cookie de terță parte.

#### <a name="microsoft-edge"></a>Microsoft Edge

1. Deschideți browserul Microsoft Edge.
2. În colțul din dreapta sus, selectați **puncte de suspensie** (...), apoi selectați **Setări**.
3. La **Module cookie și permisiuni de site**, Selectați **Module cookie-uri și date despre site-uri**.
4. Dezactivați opțiunea **Blocați modulele cookie de terță parte**.

#### <a name="google-chrome"></a>Google Chrome

1. Deschideți browserul Chrome.
2. În colțul din dreapta sus, selectați cele trei puncte verticale, apoi selectați **Setări**.
3. La **Confidențialitate și securitate**, Selectați **Module cookie-uri și alte date despre site-uri**.
4. Selectați **Permiteți toate modulele cookie**.

> [!IMPORTANT]
> Dacă blocați modulele cookie de terță parte, toate modulele cookie și datele site-urilor de pe alte site-uri vor fi blocate, chiar dacă site-ul este autorizat pe lista dvs. de excepții.

## <a name="pex-endpoint"></a>Punct final PEX

Project Operations necesită ca un parametru de proiect să facă referire la punctul final PEX. Acest punct final este necesar pentru a comunica cu serviciul utilizat pentru a reda structura detaliată a proiectului. Dacă parametrul nu este activat, veți primi eroarea „Parametrul proiectului nu este valid”. 

### <a name="workaround"></a>Soluție
 ![Câmpul punct final PEX în parametrul proiectului](media/projectparameter.png)

1. Adăugați câmpul **Punct final PEX** pe pagina **Parametrii proiectului**.
2. Actualizați câmpul cu următoarea valoare: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=\<id>&type=2`
3. Eliminați câmpul de pe pagina **Parametrii proiectului**.

## <a name="privileges-for-project-for-the-web"></a>Privilegii de proiect pentru Web

Project Operations se bazează pe un serviciu de planificare externă. Serviciul necesită ca un utilizator să aibă mai multe roluri atribuite pentru a citi și scrie entităților asociate la structura detaliată a proiectului. Aceste entități includ sarcini de proiect, alocări de resurse și dependențe de sarcini. Dacă un utilizator nu poate reda structura detaliată a proiectului de pe fila **Sarcini** fila, probabil este pentru că Proiect pentru Project Operations nu a fost activat. Un utilizator poate primi fie o eroare rol de securitate, fie o eroare legată de refuzul de acces.


## <a name="workaround"></a>Soluție

1. Accesați vizualizarea **Setări > Securitate > Utilizatori > Utilizatorii aplicației**.  

   ![Cititor aplicație](media/applicationuser.jpg)
   
2. Faceți dublu clic pe înregistrarea utilizatorului aplicației pentru a verifica următoarele:

 - Utilizatorul are acces la proiect. De obicei, această verificare se face prin asigurarea faptului că utilizatorul are rol de securitate **Manager de proiect**.
 - Utilizatorul aplicației Microsoft Project există și este configurat corect.
 
3. Dacă acest utilizator nu există deja, puteți crea o nouă înregistrare de utilizator. Selectați **Utilizatori noi**. Schimbați formularul de înregistrare în **Utilizator de aplicație**, apoi adăugați **ID-ul aplicației**.

   ![Detalii utilizator aplicație](media/applicationuserdetails.jpg)

4. Verificați dacă utilizatorului i s-a atribuit licența corectă și că serviciul este activat în detaliile abonamentelor de servicii ale licenței.
5. Verificați dacă utilizatorul poate deschide project.microsoft.com.
6. Verificați prin parametrii proiectului dacă sistemul indică punctul final corect al proiectului.
7. Verificați dacă este creat utilizatorul aplicației de proiect.
8. Aplicați următoarele roluri de securitate pentru utilizator:

  - Utilizator Dataverse
  - Sistem Project Operations
  - Sistemul proiectului

## <a name="error-when-updating-the-work-breakdown-structure"></a>Eroare la actualizarea structurii detaliate a proiectului

Când se efectuează una sau mai multe actualizări la structura detaliată a proiectului, în cele din urmă modificările eșuează și nu sunt salvate. Apare o eroare în grila de programare observând că „Modificarea recentă pe care ați făcut-o nu a putut fi salvată”.

### <a name="workaround"></a>Soluție

1. Verificați dacă utilizatorului i s-a atribuit licența corectă și că serviciul este activat în detaliile abonamentelor de servicii ale licenței.
2. Verificați dacă utilizatorul poate deschide project.microsoft.com.
3. Verificați dacă sistemul indică punctul final corect al proiectului.
4. Verificați dacă utilizatorul aplicației de proiect a fost creat.
5. Aplicați următoarele roluri de securitate pentru utilizator:
  
  - Utilizator Dataverse sau utilizator de bază
  - Sistem Project Operations
  - Sistemul proiectului
  - Sistemul de scriere dublă al Project Operations (Acest rol este necesar dacă implementați scenariul bazat pe resurse/ne-stocat al Project Operations.)


[!INCLUDE[footer-include](../includes/footer-banner.md)]