---
title: Upgrade de la Project Service Automation la Project Operations
description: Acest articol oferă o prezentare generală a procesului de upgrade de la Microsoft Dynamics 365 Project Service Automation la Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/11/2022
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: ac2435c99f3aa9b2a6cdb08d7ce5f6628e7f6ac4
ms.sourcegitcommit: bea5f9b4066277344add1da3a1567ed56a0cfd31
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 11/02/2022
ms.locfileid: "9736682"
---
# <a name="upgrade-from-project-service-automation-to-project-operations"></a>Upgrade de la Project Service Automation la Project Operations

Suntem încântați să anunțăm cea de-a doua dintre cele trei faze de upgrade de la Microsoft Dynamics 365 Project Service Automation la Microsoft Dynamics 365 Project Operations. Acest articol oferă o prezentare generală pentru clienții care pornesc în această călătorie interesantă. 

Programul de livrare a upgrade-ului va fi împărțit în trei faze.

| Livrare upgrade | Faza 1 (ianuarie 2022) | Faza 2 (noiembrie 2022) | Faza 3 (valul aprilie 2023)  |
|------------------|------------------------|---------------------------|---------------------------|
| Nicio dependență de structura de defalcare a lucrărilor (WBS) pentru proiecte | :bifă solidă: | :bifă solidă: | :bifă solidă: |
| Un WBS în limitele suportate în prezent de Project Operations | | :bifă solidă: | :bifă solidă: |
| Un WBS în afara limitelor suportate în prezent de Project Operations, inclusiv suport pentru Project desktop client | | | :bifă solidă: |

## <a name="upgrade-process-features"></a>Caracteristicile procesului de upgrade 

Ca parte a procesului de actualizare, am adăugat jurnalele de actualizare pe harta site-ului pentru a permite administratorilor să diagnosticheze mai ușor defecțiunile. Pe lângă noua interfață, vor fi adăugate noi reguli de validare pentru a asigura integritatea datelor după o actualizare. Următoarele validări vor fi adăugate procesului de actualizare.

| Validări | Faza 1 (ianuarie 2022) | Faza 2 (noiembrie 2022) | Faza 3  |
|-------------|------------------------|---------------------------|---------------------------|
| WBS va fi validat împotriva încălcărilor comune ale integrității datelor (de exemplu, alocări de resurse care sunt asociate cu aceeași sarcină părinte, dar au proiecte părinte diferite). | | :bifă solidă: | :bifă solidă: |
| WBS va fi validat în raport cu [limitele cunoscute din Project for the Web](/project-for-the-web/project-for-the-web-limits-and-boundaries). | | :bifă solidă: | :bifă solidă: |
| WBS va fi validat în raport cu limitele cunoscute din Project desktop client. | |  | :bifă solidă: |
| Resursele rezervabile și calendarele proiectelor vor fi evaluate în raport cu excepțiile comune ale regulilor calendaristice incompatibile. | | :bifă solidă: | :bifă solidă: |

În faza 2, clienții care fac upgrade la Project Operations vor avea proiectele existente actualizate la o experiență numai în citire pentru planificarea proiectelor. În această experiență numai în citire, WBS complet va fi vizibil în grila de urmărire. Pentru a edita WBS, managerii de proiect pot selecta [**Convertire**](/PSA-Upgrade-Project-Conversion.md) pe pagina principală a proiectului. Un proces de fundal actualizează apoi proiectul, astfel încât să accepte noua experiență de planificare a proiectelor din Project for the Web. Această fază este potrivită pentru clienții care au proiecte care se încadrează în [limitele cunoscute din Project for the Web](/project-for-the-web/project-for-the-web-limits-and-boundaries).

În faza 3, se va adăuga suport pentru Project desktop client, în beneficiul clienților care doresc să continue să își editeze proiectele din acea aplicație. Cu toate acestea, dacă proiectele existente sunt convertite în noua experiență Project for the Web, accesul la programul de completare va fi dezactivat pentru fiecare proiect convertit.

## <a name="prerequisites"></a>Cerințe preliminare

Pentru a fi eligibil pentru Faza 1 de upgrade, trebuie să îndepliniți următoarele criterii:

- Mediul țintă nu trebuie să conțină nicio înregistrare în entitatea **msdyn_projecttask**.
- Licențele de Project Operations valide trebuie alocate tuturor utilizatorilor activi. 
- Trebuie să validați procesul de actualizare în cel puțin un mediu care nu este de producție care conține un set de date reprezentativ care este aliniat cu mediul dumneavoastră de producție.
- Mediul țintă trebuie actualizat la Project Service Automation Update Release 37 (V3.10.58.120) sau o versiune ulterioară.

Pentru a fi eligibil pentru Faza 2 de upgrade, trebuie să îndepliniți următoarele criterii:

- Licențele de Project Operations valide trebuie alocate tuturor utilizatorilor activi. 
- Trebuie să validați procesul de actualizare în cel puțin un mediu care nu este de producție care conține un set de date reprezentativ care este aliniat cu mediul dumneavoastră de producție.
- Mediul țintă trebuie actualizat la Project Service Automation Update Release 37 (V3.10.58.120) sau o versiune ulterioară.
- Mediile care conțin sarcini (msdyn_projecttask) sunt acceptate numai dacă numărul total de sarcini per proiect este de 500 sau mai puțin.

Cerințele preliminare pentru Faza 3 vor fi actualizate pe măsură ce se apropie data disponibilității generale.

## <a name="licensing"></a>Licențiere

Dacă aveți licențe active pentru Project Service Automation, puteți instala și utiliza Project Operations, care include toate capabilitățile Project Service Automation și multe altele. În acest fel, puteți testa capabilitățile Project Operations în timp ce continuați să utilizați Project Service Automation în producție. După expirarea licențelor Project Service Automation, va trebui să treceți la Project Operations. Când planificați această tranziție, trebuie să luați în considerare faptul că licența Project Operations nu include o licență Project Service Automation. Clienții care au scenarii în care au implementat Project Service Automation și trebuie să continue să folosească sau să-și mărească licențele pentru PSA în timp ce intenționează să treacă la Project Operations, pot solicita licențe PSA temporare pe baza licențelor achiziționate de Project Operations. Va fi eliberată o licență Project Service Automation pentru o licență Project Operations. Licențele PSA temporare pot fi solicitate utilizând acest link: aka.ms/ineedpsa

## <a name="testing-and-refactoring-customizations"></a>Testarea și refactorizarea personalizărilor

Ca punct de plecare, importați toate personalizările într-un mediu curat din Project Operations (Lite) pentru a confirma că importul a avut succes și că operațiunile de afaceri se comportă conform așteptărilor.

Iată câteva lucruri cărora trebuie să le acordați atenție:

- Importul poate eșua din cauza dependențelor lipsă. Cu alte cuvinte, personalizările fac referire la câmpuri sau alte componente care au fost eliminate în Project Operations. În acest caz, eliminați aceste dependențe din mediul de dezvoltare.
- Dacă soluțiile dvs. negestionate și gestionate includ componente care nu sunt personalizate, eliminați acele componente din soluție. De exemplu, atunci când personalizați entitatea **Proiect**, adăugați numai antetul entității la soluția dvs. Nu adăugați toate câmpurile. Dacă ați adăugat anterior toate subcomponentele, ar putea fi necesar să creați manual o soluție nouă și să adăugați componente relevante.
- Este posibil ca formularele și vizualizările să nu apară așa cum era de așteptat. În anumite circumstanțe, dacă ați personalizat oricare dintre formularele sau vizualizările predefinite, personalizările pot împiedica noile actualizări din Project Operations să producă efect. Pentru a identifica aceste probleme, vă recomandăm să faceți o revizuire paralelă a unei instalări curate a Project Operations și a unei instalări a Project Operations care include personalizările dvs. Comparați cele mai frecvent utilizate formulare în afacerea dvs. pentru a confirma că versiunea formularului dvs. încă are sens și că nu lipsește ceva din versiunea curată a formularului. Faceți același tip de revizuire alăturată pentru toate vizualizările pe care le-ați personalizat.
- Logica de afaceri ar putea eșua în timpul execuției. Întrucât referințele la câmpurile din plug-in-urile dvs. nu sunt validate în momentul importului, logica de afaceri poate eșua din cauza referințelor la câmpuri care nu mai există și este posibil să primiți un mesaj de eroare care seamănă cu următorul exemplu: „„Entitatea proiect” nu conține un atribut cu Name = 'msdyn_plannedhours' și NameMapping = 'Logical'." În acest caz, modificați personalizările astfel încât acestea să utilizeze noile câmpuri. Dacă utilizați clase de proxy generate automat și referințe de tip puternic în logica plug-in-ului, luați în considerare regenerarea acelor proxy dintr-o instalare curată. În acest fel, puteți identifica cu ușurință toate locurile în care pluginurile dvs. depind de câmpurile învechite.

După ce vă actualizați personalizările pentru a importa în mod curat Project Operations, treceți la pașii următori.

## <a name="end-to-end-testing-in-development-environments"></a>Testare integrală în medii de dezvoltare

### <a name="initiate-upgrade"></a>Inițiază upgrade 

1. În centrul de administrare Power Platform, găsiți și selectați mediul dvs. Apoi, în aplicații, găsiți și completați **Dynamics 365 Project Operations**.
2. Selectați **Instalare** pentru a începe actualizarea. Centrul de administrare Power Platform va prezenta această instalare ca pe o nouă instalare. Cu toate acestea, va fi detectată prezența unei versiuni anterioare a Project Service Automation, iar instalarea existentă va fi actualizată.

    După finalizarea upgrade-ului, mediul ar trebui să arate că Project Operations este instalat și că Project Service Automation nu este instalat.

    În funcție de cantitatea de date din mediu, upgrade-ul poate dura câteva ore Echipa de bază care gestionează upgrade-ul ar trebui să planifice în consecință și să execute upgrade-ul în timpul orelor de lucru. În unele cazuri, dacă volumul de date este mare, upgrade-ul ar trebui să fie rulat în weekend. Decizia privind programarea ar trebui să se bazeze pe rezultatele testării în medii inferioare.

3. Actualizați soluțiile personalizate după caz. În acest moment, implementați orice modificări pe care le-ați adus personalizărilor dvs. în secțiunea [Testare și refactorizare personalizări](#testing-and-refactoring-customizations) din acest articol.
4. Accesați **make.powerapps.com**, selectați mediul dvs. din meniul vertical din dreapta sus a portalului, selectați **Soluții** din meniul din stânga, selectați soluția **Componente depreciate Project Operations** și **Dezinstalare**.

    Această soluție este o soluție temporară care deține modelul de date existent și componentele care sunt prezente în timpul upgrade-ului. Prin eliminarea acestei soluții, eliminați toate câmpurile și componentele care nu mai sunt utilizate. În acest fel, contribuiți la simplificarea interfeței și facilitați integrarea și extinderea.
    
### <a name="upgrade-to-project-operations-lite"></a>Faceți upgrade la Project Operations Lite

Următorii pași descriu procesul de actualizare și înregistrarea erorilor asociate:

1. **Verificarea versiunii PSA:** Pentru a instala Project Operations, trebuie să aveți V3.10.58.120 sau ulterioară.
1. **Prevalidare:** Când un administrator inițiază o actualizare, sistemul rulează o operațiune de pre-validare pentru fiecare entitate care este esențială pentru soluția Project Operations. Acest pas verifică dacă toate referințele de entități sunt valide și asigură că datele care sunt legate de WBS se încadrează în limitele publicate de Project for the Web.
1. **Actualizare metadate:** După prevalidarea cu succes, sistemul inițiază modificări ale schemei și creează o soluție de componente depreciate. Puteți elimina această soluție învechită după ce ați finalizat toate refactorizările necesare ale personalizărilor. Acest pas reprezintă cea mai lungă parte a procesului de actualizare și poate dura până la patru ore pentru a fi finalizat.
1. **Upgrade de date:** După ce toate modificările necesare ale schemei au fost finalizate în pasul de actualizare a metadatelor, datele dvs. sunt migrate la noua schemă și sunt efectuate toate recalculările și revenirile implicite necesare.
1. **Actualizarea motorului de planificare a proiectului:** După actualizarea cu succes a datelor, fila **Planificare** de pe pagina principală este reetichetată ca **Sarcini**. Când un utilizator selectează această filă după actualizare, acesta este direcționat să navigheze la grila de urmărire pentru a vedea o versiune numai pentru citire a WBS. Pentru a edita WBS, trebuie să inițieze planificarea [proces de conversie](/PSA-Upgrade-Project-Conversion.md). Toate proiectele fără un WBS preexistent pot folosi noua experiență de programare direct, fără conversie.
 
### <a name="validate-common-scenarios"></a>Validarea scenariilor comune

Când validați personalizările dvs. specifice, vă recomandăm să examinați și procesele de afaceri care sunt acceptate în toate aplicațiile. Aceste procese de afaceri includ, dar nu se limitează la, crearea de entități de vânzări, cum ar fi oferte și contracte, și crearea de proiecte care includ WBS și aprobarea valorilor reale.

## <a name="major-changes-between-project-service-automation-and-project-operations"></a>Schimbări majore între Project Service Automation și Project Operations

Această secțiune oferă un rezumat al schimbărilor majore la care vă puteți aștepta între Project Service Automation și Project Operations.

### <a name="project-planning"></a>Planificarea unui proiect

Capacitățile de planificare a proiectelor din Project Operations nu se mai bazează pe o combinație de logică pe parte de clientul și pe logica pe parte de server. În schimb, Project Operations folosește Project for the Web ca motor de planificare. Această modificare a capabilităților de planificare permite mai multe funcții noi, cum ar fi vizualizări Board și Gantt, planificare bazată pe resurse, [elemente din lista de verificare a sarcinilor](https://support.microsoft.com/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c) și modurile de planificare a proiectelor. Noile capabilități de programare sunt susținute și de un set bogat de noi [interfețe de programare a aplicațiilor (API)](../project-management/schedule-api-preview.md). Aceste API-uri sunt menite să ajute să se asigure că nicio operațiune programatică pentru crearea, actualizarea sau ștergerea unei entități din WBS nu corupe câmpurile calculate din planificare.

### <a name="billing-and-pricing"></a>Facturarea și stabilirea prețurilor

Ca parte a investițiilor continue în Project Operations, sunt disponibile câteva capabilități noi în Facturare și stabilire a prețurilor. Iată câteva exemple:

- [Înregistrarea utilizării de materiale pentru proiecte și activitățile proiectului](../material/material-usage-log.md)
- [Gestionarea subcontractării](../pro/subcontracting/managing-subcontracts-overview.md)
- [Avansuri și contracte bazate pe garanții](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Statutul contractului de a nu depăși și validările](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- Facturare pe bază de activități

### <a name="resource-management"></a>Gestionarea resurselor

Project Operations oferă suport opțional pentru asistentul de bord și de programare Universal Resource Scheduling (URS). Această nouă experiență va deveni obligatorie în valul din aprilie 2023.

## <a name="frequently-asked-questions"></a>Întrebări frecvente

### <a name="which-deployment-types-are-currently-supported-for-upgrade"></a>Ce tipuri de implementare sunt acceptate în prezent pentru upgrade?

| Sursă                                                 | Țintă                                                    | Status                  |
|--------------------------------------------------------|-----------------------------------------------------------|-------------------------|
| Project Service Automation                             | Implementare Project Operations Lite                        | Acceptat               |
| Management de proiect și contabilitate Dynamics 365 Finance | Implementare Project Operations Lite                        | Nu este acceptat momentan |
| Management de proiect și contabilitate Finance              | Project Operations pentru resurse/scenarii fără stoc     | Nu este acceptat momentan |
| Project Service Automation 3.x                         | Project Operations pentru resurse/scenarii fără stoc     | Nu este acceptat momentan |
| Project for the web (mediu dedicat)            | Implementare Project Operations Lite                        | Nu este acceptat momentan |

### <a name="how-can-i-install-project-operations-before-the-upgrade-tooling-is-available"></a>Cum pot instala Project Operations înainte ca instrumentele de actualizare să fie disponibile?

Există două opțiuni pentru instalarea Project Operations înainte ca instrumentul de actualizare să fie disponibil:

- Asigurarea accesului pentru un nou mediu.
- Implementați Project Operations separat în orice organizație de vânzări în care Project Service Automation nu este prezent.

Dacă Project Service Automation este instalat într-o organizație, dar nu a fost folosit, poate fi dezinstalat. După ce eliminați complet Project Service Automation, Project Operations poate fi instalat în aceeași organizație.
