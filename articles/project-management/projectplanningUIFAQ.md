---
title: Depanare de funcționare în grila de activități
description: Acest articol oferă informații de depanare necesare atunci când lucrați în grila de activități.
author: ruhercul
ms.date: 04/05/2022
ms.topic: article
ms.product: ''
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: e6ab4f34fe3f6732f7bef252f298671e07a3c3ca
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911059"
---
# <a name="troubleshoot-working-in-the-task-grid"></a>Depanare de funcționare în grila de activități 


_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stoc, implementare Lite - facturare de la ofertă și până la proforma, Project for the web_

Grila de activități utilizată de Dynamics 365 Project Operations este un iframe găzduit în cadrul Microsoft Dataverse. Ca urmare a acestei utilizări, trebuie îndeplinite cerințe specifice pentru a se asigura că autentificarea și autorizarea funcționează corect. Acest articol subliniază problemele comune care pot afecta capacitatea de a reda grila sau de a gestiona sarcini în structura de defalcare a lucrărilor (WBS).

Printre problemele comune se numără:

- Fila **Activitate** din grila de activități este goală.
- La deschiderea proiectului, proiectul nu se încarcă și interfața cu utilizatorul (UI) este blocată pe spinner.
- Administrarea privilegiilor pentru **Project for the Web**.
- Modificările nu sunt salvate când creați, actualizați sau ștergeți o activitate.

## <a name="issue-the-task-tab-is-empty"></a>Problemă: fila Activitate este goală

### <a name="mitigation-1-enable-cookies"></a>Diminuare 1: activați cookie-urile

Project Operations necesită activarea cookie-urilor terță parte pentru a reda structura detaliată a proiectului. Când modulele cookie de terță parte nu sunt activate, în loc să vedeți sarcini, veți vedea o pagină goală când selectați fila **Sarcini** de pe pagina **Proiect**.

Pentru browser-ele Microsoft Edge sau Google Chrome, următoarele proceduri descriu cum să actualizați setările browser-ului pentru a activa modulele cookie de terță parte.

#### <a name="microsoft-edge"></a>Microsoft Edge

1. Deschideți browserul Microsoft Edge.
2. În colțul din dreapta sus, selectați **puncte de suspensie** (...), apoi selectați **Setări**.
3. La **Module cookie și permisiuni de site**, Selectați **Module cookie-uri și date despre site-uri**.
4. Dezactivați opțiunea **Blocați modulele cookie de terță parte**.
5. Reîmprospătați browserul. 

#### <a name="google-chrome"></a>Google Chrome

1. Deschideți browserul Chrome.
2. În colțul din dreapta sus, selectați cele trei puncte verticale, apoi selectați **Setări**.
3. La **Confidențialitate și securitate**, Selectați **Module cookie-uri și alte date despre site-uri**.
4. Selectați **Permiteți toate modulele cookie**.
5. Reîmprospătați browserul. 

> [!NOTE]
> Dacă blocați modulele cookie de terță parte, toate modulele cookie și datele site-urilor de pe alte site-uri vor fi blocate, chiar dacă site-ul este autorizat pe lista dvs. de excepții.

### <a name="mitigation-2-validate-the-pex-endpoint-has-been-correctly-configured"></a>Diminuare 2: Validați punctul final PEX a fost configurat corect

Project Operations necesită ca un parametru de proiect să facă referire la punctul final PEX. Acest punct final este necesar pentru a comunica cu serviciul utilizat pentru a reda structura detaliată a proiectului. Dacă parametrul nu este activat, veți primi eroarea „Parametrul proiectului nu este valid”. Pentru a actualiza punctul final PEX, parcurgeți pașii următori.

1. Adăugați câmpul **Punct final PEX** pe pagina **Parametrii proiectului**.
2. Identificați tipul de produs pe care îl utilizați. Această valoare este utilizată atunci când este setat punctul final PEX. După regăsire, tipul de produs este deja definit în punctul final PEX. Păstrați această valoare.
3. Actualizați câmpul cu următoarea valoare: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=<id>&type=2`. Următorul tabel oferă parametrul de tip care trebuie utilizat pe baza tipului de produs.

      | **Tip produs**                     | **Parametru tip** |
      |--------------------------------------|--------------------|
      | Project for the Web pe organizație implicită   | tip=0             |
      | Project for the Web pe organizație numită CDS | tip=1             |
      | Project Operations                   | tip=2             |

4. Eliminați câmpul de pe pagina **Parametrii proiectului**.

### <a name="mitigation-3-sign-in-to-projectmicrosoftcom"></a>Atenuare 3: conectați-vă la project.microsoft.com
În dumneavoastră Microsoft Edge browser, deschideți o filă nouă, accesați project.microsoft.com și conectați-vă utilizând rolul de utilizator pe care îl utilizați pentru a accesa Operațiunile de proiect.

## <a name="issue-the-project-doesnt-load-and-the-ui-is-stuck-on-the-spinner"></a>Problemă: Proiectul nu se încarcă, iar interfața de utilizare este blocată pe spinner

În scopul autentificării, ferestrele pop-up trebuie să fie activate pentru a se încărca grila de activități. Dacă ferestrele pop-up nu sunt activate, ecranul va fi blocat pe spinner-ul de încărcare. Următorul grafic arată adresa URL cu o etichetă pop-up blocată în bara de adrese, ceea ce duce la blocarea spinner-ului în încercarea de a încărca pagina. 

   ![Spinner blocat și blocare de pop-up.](media/popupsblocked.png)

### <a name="mitigation-1-enable-pop-ups"></a>Diminuare 1: activați pop-up-urile

Când proiectul dvs. este blocat pe spinner, este posibil ca ferestrele pop-up să nu fie activate.

#### <a name="microsoft-edge"></a>Microsoft Edge

Există două moduri de a activa ferestrele pop-up în browserul dvs. Edge.

1. În browserul Edge, selectați notificarea din partea dreaptă sus a browserului.
2. Selectați **Permiteți întotdeauna ferestre pop-up și redirecționări de la** mediul specific Dataverse.
 
     ![Fereastra pop-up blocată.](media/enablepopups.png)

Alternativ, puteți parcurge următorii pași.

1. Deschideți browserul Microsoft Edge.
2. În colțul din dreapta sus, selectați **elipsă** (...) și apoi selectați **Setări** > **Permisiuni de site** > **Ferestre pop-up și redirecționări**.
3. Comutați la oprit **Ferestre pop-up și redirecționări** pentru blocarea ferestrelor pop-up sau comutați la pornit pentru a permite ferestrele pop-up de pe dispozitiv.
4. După ce activați ferestrele pop-up, reîmprospătați browserul. 

#### <a name="google-chrome"></a>Google Chrome
1. Deschideți browserul Chrome.
2. Navigați la o pagină în care ferestrele pop-up sunt blocate.
3. În bara de adrese, selectați **Pop-up blocat**.
4. Selectați linkul pentru fereastra pop-up pe care doriți să o vedeți.
5. După ce activați ferestrele pop-up, reîmprospătați browserul. 

> [!NOTE]
> Pentru a vedea întotdeauna ferestre pop-up pentru site, selectați **Permiteți întotdeauna ferestre pop-up și redirecționări de pe [site]** și apoi selectați **Terminat**.

## <a name="issue-3-administration-of-privileges-for-project-for-the-web"></a>Problema 3: Administrarea privilegiilor pentru Project for the Web

Project Operations se bazează pe un serviciu de planificare externă. Serviciul necesită ca un utilizator să aibă mai multe roluri atribuite, care să le permită să citească și să scrie către entități legate de WBS. Aceste entități includ sarcini de proiect, alocări de resurse și dependențe de sarcini. Dacă un utilizator nu poate reda WBS atunci când navighează pe fila **Activități**, este probabil pentru că **Proiect** pentru **Project Operations** nu a fost activat. Un utilizator poate primi fie o eroare rol de securitate, fie o eroare legată de refuzul de acces.

### <a name="mitigation-1-validate-the-application-user-and-end-user-security-roles"></a>Atenuare 1: Validați rolurile de securitate ale utilizatorului aplicației și ale utilizatorului final

1. Accesați **Setare** > **Securitate** > **Utilizatori** > **Utilizatori de aplicație**.  

   ![Cititor aplicație.](media/applicationuser.jpg)
   
2. Faceți dublu clic pe înregistrarea utilizatorului aplicației pentru a verifica:

     - Utilizatorul are acces la proiect. Puteți face acest lucru verificând dacă utilizatorul are rolul de securitate **Manager de proiect**.
     - Utilizatorul aplicației Microsoft Project există și este configurat corect.
 
3. Dacă acest utilizator nu există, creați o nouă înregistrare de utilizator. 
4. Selectați **Utilizatori noi**, modificați formularul de înregistrare în **Utilizator de aplicație**, apoi adăugați **ID-ul aplicației**.

   ![Detalii utilizator aplicație.](media/applicationuserdetails.jpg)


## <a name="issue-4-changes-arent-saved-when-you-create-update-or-delete-a-task"></a>Problema 4: Modificările nu sunt salvate când creați, actualizați sau ștergeți o activitate

Când efectuați una sau mai multe actualizări la WBS, modificările nu reușesc și nu sunt salvate. Apare o eroare în grila de programare cu un mesaj care spune: „Modificarea recentă pe care ați făcut-o nu a putut fi salvată”.

### <a name="mitigation-1-validate-the-license-assignment"></a>Atenuare 1: Validați atribuirea licenței

1. Verificați dacă utilizatorului i s-a atribuit licența corectă și că serviciul este activat în detaliile abonamentelor de servicii ale licenței.  
2. Verificați dacă utilizatorul poate deschide **project.microsoft.com**.
    
### <a name="mitigation-2-validation-configuration-of-the-project-application-user"></a>Atenuare 2: Configurarea validării utilizatorului aplicației Project
1. Verificați dacă utilizatorul aplicației de Proiect a fost creat.
2. Aplicați următoarele roluri de securitate pentru utilizator:
  
  - Utilizator Dataverse sau utilizator de bază
  - Sistem Project Operations
  - Sistemul proiectului
  - Scriere duală pentru Project Operations. Acest rol este necesar pentru scenariul de implementare de resurse/care nu sunt bazate pe stoc al Project Operations.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
