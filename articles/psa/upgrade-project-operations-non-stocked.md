---
title: Upgrade de la Project Service Automation la Project Operations
description: Acest subiect oferă o prezentare generală a procesului de la care să faceți upgrade Microsoft Dynamics 365 Project Service Automation la Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/13/2022
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
ms.openlocfilehash: 3f31173197a3055cdc51567261dd91925fc9f430
ms.sourcegitcommit: bec7382d1319d59645e8e79fdb20df58617c97c6
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 04/21/2022
ms.locfileid: "8626743"
---
# <a name="upgrade-from-project-service-automation-to-project-operations"></a>Upgrade de la Project Service Automation la Project Operations

Suntem încântați să anunțăm prima dintre cele trei faze de la care trebuie să faceți upgrade Microsoft Dynamics 365 Project Service Automation la Dynamics 365 Project Operations. Acest subiect oferă o imagine de ansamblu pentru clienții care pornesc în această călătorie interesantă. Subiectele viitoare vor include considerații pentru dezvoltatori și detalii despre îmbunătățirile caracteristicilor. Ei nu numai că vă vor oferi îndrumări pentru a vă ajuta să vă pregătiți pentru upgrade-ul la Operațiuni de proiect, dar vă vor explica și la ce vă puteți aștepta după ce ați făcut upgrade.

Programul de livrare a upgrade-ului va fi împărțit în trei faze.

| Livrare upgrade | Faza 1 (ianuarie 2022) | Faza 2 (valul aprilie 2022) | Faza 3  |
|------------------|------------------------|---------------------------|---------------------------|
| Nicio dependență de structura de defalcare a lucrărilor (WBS) pentru proiecte | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| WBS în limitele suportate în prezent ale operațiunilor de proiect | | :heavy_check_mark: | :heavy_check_mark: |
| WBS în afara limitelor suportate în prezent ale operațiunilor de proiect, inclusiv suport pentru clientul desktop Project | | | :heavy_check_mark: |

## <a name="upgrade-process-features"></a>Funcțiile procesului de upgrade 

Ca parte a procesului de actualizare, am adăugat jurnalele de actualizare pe harta site-ului, astfel încât administratorii să poată diagnostica mai ușor defecțiunile. Pe lângă noua interfață, vor fi adăugate noi reguli de validare pentru a asigura integritatea datelor după o actualizare. Următoarele validări vor fi adăugate procesului de actualizare.

| Validari | Faza 1 (ianuarie 2022) | Faza 2 (valul aprilie 2022) | Faza 3  |
|-------------|------------------------|---------------------------|---------------------------|
| WBS va fi validat împotriva încălcărilor comune ale integrității datelor (de exemplu, alocări de resurse care sunt asociate cu aceeași sarcină părinte, dar au proiecte părinte diferite). | | :heavy_check_mark: | :heavy_check_mark: |
| WBS va fi validat în raport cu [limitele cunoscute ale Proiectului pentru Web](/project-for-the-web/project-for-the-web-limits-and-boundaries). | | :heavy_check_mark: | :heavy_check_mark: |
| WBS va fi validat în raport cu limitele cunoscute ale clientului desktop Project. | |  | :heavy_check_mark: |
| Resursele rezervabile și calendarele proiectelor vor fi evaluate în raport cu excepțiile comune ale regulilor calendaristice incompatibile. | | :heavy_check_mark: | :heavy_check_mark: |

În faza 2, clienții care fac upgrade la Project Operations vor avea proiectele existente actualizate la o experiență doar în citire pentru planificarea proiectelor. În această experiență numai în citire, WBS complet va fi vizibil în grila de urmărire. Pentru a edita WBS, managerii de proiect pot selecta **Convertit** pe principal **Proiecte** pagină. Un proces de fundal va actualiza apoi proiectul, astfel încât să accepte noua experiență de planificare a proiectelor din Project for the Web. Această fază este potrivită pentru clienții care au proiecte care se încadrează în [limitele cunoscute ale Proiectului pentru Web](/project-for-the-web/project-for-the-web-limits-and-boundaries).

În faza 3, se va adăuga suport pentru clientul desktop Project, în beneficiul clienților care doresc să continue să își editeze proiectele din acea aplicație. Cu toate acestea, dacă proiectele existente sunt convertite în noua experiență Proiect pentru Web, accesul la programul de completare va fi dezactivat pentru fiecare proiect convertit.

## <a name="prerequisites"></a>Cerințe preliminare

Pentru a fi eligibil pentru faza 1 de actualizare, un client trebuie să îndeplinească următoarele criterii:

- Mediul țintă nu trebuie să conțină nicio înregistrare în **msdyn_projecttask** entitate.
- Licențele de operațiuni de proiect valide trebuie alocate tuturor utilizatorilor activi ai clientului. 
- Clientul trebuie să valideze procesul de actualizare în cel puțin un mediu non-producție care are un set de date reprezentativ care este aliniat cu datele de producție.
- Mediul țintă trebuie actualizat la Project Service Automation Update Release 41 (3.10.62.162) sau mai târziu.

Cerințele preliminare pentru faza 2 și faza 3 vor fi actualizate pe măsură ce se apropie datele generale de disponibilitate.

## <a name="licensing"></a>Licențiere

Dacă aveți licențe active pentru Project Service Automation, puteți instala și utiliza Project Operations, care include toate capabilitățile Project Service Automation și multe altele. În acest fel, puteți testa capabilitățile Project Operations în timp ce continuați să utilizați Project Service Automation în producție. După expirarea licențelor Project Service Automation, va trebui să treceți la Project Operations. Când planificați această tranziție, trebuie să luați în considerare faptul că licența Project Operations nu include o licență Project Service Automation.

## <a name="testing-and-refactoring-customizations"></a>Testarea și refactorizarea personalizărilor

Ca punct de plecare, importați toate personalizările într-un mediu curat de operațiuni de proiect (lite) pentru a confirma că importul are succes și că operațiunile de afaceri se comportă conform așteptărilor.

Iată câteva lucruri la care trebuie să fii atent:

- Importul poate eșua din cauza dependențelor lipsă. Cu alte cuvinte, personalizările fac referire la câmpuri sau alte componente care au fost eliminate în Operațiuni de proiect. În acest caz, eliminați aceste dependențe din mediul de dezvoltare.
- Dacă soluțiile dvs. negestionate și gestionate includ componente care nu sunt personalizate, eliminați acele componente din soluție. De exemplu, când personalizați **Proiect** entitate, adăugați numai antetul entității la soluția dvs. Nu adăugați toate câmpurile. Dacă ați adăugat anterior toate subcomponentele, poate fi necesar să creați manual o nouă soluție și să adăugați componente relevante.
- Este posibil ca formularele și vizualizările să nu apară așa cum era de așteptat. În anumite circumstanțe, dacă ați personalizat oricare dintre formularele sau vizualizările disponibile, personalizările ar putea împiedica noile actualizări din Operațiunile de proiect să intre în vigoare. Pentru a identifica aceste probleme, vă recomandăm să faceți o revizuire paralelă a unei instalări curate a Project Operations și a unei instalări a Project Operations care include personalizările dvs. Comparați cele mai frecvent utilizate formulare în afacerea dvs. pentru a confirma că versiunea dvs. a formularului încă are sens și că nu lipsește ceva din versiunea curată a formularului. Faceți același tip de revizuire una lângă alta pentru toate vizualizările pe care le-ați personalizat.
- Logica de afaceri poate eșua în timpul execuției. Deoarece referințele la câmpurile din pluginurile dvs. nu sunt validate în momentul importului, logica de afaceri poate eșua din cauza referințelor la câmpuri care nu mai există și este posibil să primiți un mesaj de eroare care seamănă cu următorul exemplu: „„Proiect” entitatea nu conține un atribut cu Name = 'msdyn_plannedhours' și NameMapping = 'Logical'." În acest caz, modificați personalizările astfel încât acestea să utilizeze noile câmpuri. Dacă utilizați clase de proxy generate automat și referințe de tip puternic în logica plug-in-ului, luați în considerare regenerarea acelor proxy dintr-o instalare curată. În acest fel, puteți identifica cu ușurință toate locurile în care pluginurile dvs. depind de câmpurile învechite.

După ce vă actualizați personalizările pentru a importa în mod curat operațiunile de proiect, treceți la pașii următori.

## <a name="end-to-end-testing-in-development-environments"></a>Testare end-to-end în medii de dezvoltare

### <a name="initiate-upgrade"></a>Inițiază upgrade 

1. În Power Platform centru de administrare, găsiți și selectați mediul dvs. Apoi, în aplicații, găsiți și selectați **Dynamics 365 Project Operations**.
2. Selectați **Instalare** pentru a începe upgrade-ul. The Power Platform Centrul de administrare va prezenta această instalare ca o nouă instalare. Cu toate acestea, va fi detectată prezența unei versiuni anterioare a Project Service Automation, iar instalația existentă va fi actualizată.

    După finalizarea upgrade-ului, mediul ar trebui să arate că Project Operations este instalat și că Project Service Automation nu este instalat.

    > [!NOTE]
    > În funcție de cantitatea de date din mediu, upgrade-ul poate dura câteva ore. Echipa de bază care gestionează upgrade-ul ar trebui să planifice în consecință și să execute upgrade-ul în timpul orelor de lucru. În unele cazuri, dacă volumul de date este mare, upgrade-ul ar trebui să fie rulat în weekend. Decizia privind programarea ar trebui să se bazeze pe rezultatele testării în medii inferioare.

3. Actualizați soluțiile personalizate după caz. În acest moment, implementați orice modificări pe care le-ați făcut personalizărilor dvs. în [Testarea și refactorizarea personalizărilor](#testing-and-refactoring-customizations) secțiunea acestui subiect.
4. Mergi la **Setări** \> **Soluții**, și selectați pentru a dezinstala **Operațiuni de proiect Componente depreciate** soluţie.

    Această soluție este o soluție temporară care deține modelul de date existent și componentele care sunt prezente în timpul upgrade-ului. Prin eliminarea acestei soluții, eliminați toate câmpurile și componentele care nu mai sunt utilizate. În acest fel, ajutați la simplificarea interfeței și facilitați integrarea și extinderea.
    
### <a name="validate-common-scenarios"></a>Validați scenariile comune

Când validați personalizările dvs. specifice, vă recomandăm să examinați și procesele de afaceri care sunt acceptate în cadrul aplicațiilor. Aceste procese de afaceri includ, dar nu se limitează la, crearea de entități de vânzări, cum ar fi cotații și contracte, și crearea de proiecte care includ WBS și aprobarea datelor reale.

## <a name="major-changes-between-project-service-automation-and-project-operations"></a>Schimbări majore între Project Service Automation și Project Operations

Această secțiune oferă un rezumat al schimbărilor majore la care vă puteți aștepta între Project Service Automation și Project Operations.

### <a name="project-planning"></a>Planificarea unui proiect

Capacitățile de planificare a proiectelor din Operațiunile de proiect nu se mai bazează pe o combinație de logică pe partea clientului și pe logica pe partea serverului. În schimb, Project Operations folosește Project pentru Web ca motor de planificare. Această modificare a capabilităților de programare permite mai multe funcții noi, cum ar fi vizualizările Board și Gantt, planificarea bazată pe resurse, [elemente din lista de verificare a sarcinilor](https://support.microsoft.com/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c), și modurile de programare a proiectelor. Noile capabilități de programare sunt susținute și de un set bogat de noi [interfețe de programare a aplicațiilor (API)](../project-management/schedule-api-preview.md). Aceste API-uri sunt menite să ajute să se asigure că nicio operațiune programatică pentru crearea, actualizarea sau ștergerea unei entități din WBS nu corupe câmpurile calculate din program.

## <a name="billing-and-pricing"></a>Facturarea și stabilirea prețurilor

Ca parte a investițiilor continue în Operațiunile de Proiect, sunt disponibile câteva capabilități noi în Facturare și stabilire a prețurilor. Iată câteva exemple:

- [Înregistrarea utilizării materialelor pe proiecte și sarcini ale proiectului](../material/material-usage-log.md)
- [Managementul subcontractelor](../pro/subcontracting/managing-subcontracts-overview.md)
- [Avansuri și contracte bazate pe garanții](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Statutul contractului de a nu depăși și validările](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- Facturare bazată pe sarcini

## <a name="frequently-asked-questions"></a>Întrebări frecvente

### <a name="which-deployment-types-are-currently-supported-for-upgrade"></a>Ce tipuri de implementare sunt acceptate în prezent pentru upgrade?

| Sursă                                                 | Țintă                                                    | Status                  |
|--------------------------------------------------------|-----------------------------------------------------------|-------------------------|
| Project Service Automation                             | Proiect Operations Lite Deployment                        | Acceptat               |
| Dynamics 365 Finance Management de proiect și contabilitate | Proiect Operations Lite Deployment                        | Nu este acceptat momentan |
| Finanțe Management de proiect și contabilitate              | Project Operations pentru resurse/scenarii fără stoc     | Nu este acceptat momentan |
| Finanțe Management de proiect și contabilitate              | Project Operations pentru scenarii cu stocuri/comenzi de producție | Nu este acceptat momentan |
| Project Service Automation 3.x                         | Project Operations pentru resurse/scenarii fără stoc     | Nu este acceptat momentan |
| Proiect pentru Web (mediu dedicat)            | Proiect Operations Lite Deployment                        | Nu este acceptat momentan |

### <a name="how-can-i-install-project-operations-before-the-upgrade-tooling-is-available"></a>Cum pot instala Project Operations înainte ca instrumentele de actualizare să fie disponibile?

Există două opțiuni pentru instalarea Project Operations înainte ca instrumentul de actualizare să fie disponibil:

- Furnizați un mediu nou.
- Implementați operațiunile de proiect separat în orice organizație de vânzări în care Project Service Automation nu este prezent.

> [!NOTE]
> Dacă Project Service Automation este instalat într-o organizație, dar nu a fost folosit, poate fi dezinstalat. După ce eliminați complet Project Service Automation, Project Operations poate fi instalat în aceeași organizație.
