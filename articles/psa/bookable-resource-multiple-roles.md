---
title: Estimează vânzările și costurile proiectului atunci când o resursă care poate fi rezervată îndeplinește mai multe roluri pentru un proiect
description: Acest subiect oferă informații referitoare la modul în care pot fi utilizate dimensiunile de stabilire a prețurilor pentru a sprijini estimarea prețurilor și a costurilor pentru o resursă care îndeplinește mai multe roluri în cadrul unui proiect.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: be24bb3bdf2f3c8351fc396ae67457b5213e1cd800e9d2ad23d59d0d038f22b9
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/06/2021
ms.locfileid: "6987496"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-multiple-roles-for-a-project"></a>Estimează vânzările și costurile proiectului atunci când o resursă care poate fi rezervată îndeplinește mai multe roluri pentru un proiect 

[!include [banner](../includes/psa-now-project-operations.md)]

Companiile bazate pe proiecte au deseori nevoia unei resurse pentru a realiza mai multe roluri în cadrul unui proiect. Pentru fiecare dintre aceste roluri ar putea fi prețurile și costurile ar putea fi calculate diferit, ceea ce înseamnă că timpul aceleiași resurse pentru proiect ar putea obține o estimare financiară diferită în funcție de factură și de ratele de cost pentru fiecare dintre roluri. Project Service Automation permite setarea valorilor din înregistrarea membrilor echipei pentru resursa numită și permite diferențieri diferite pentru fiecare dintre activitățile la care este atribuit membrul echipei.

Următorul exemplu explică modul în care simpla înlocuire a acestei valori permite unei resurse să aibă mai multe roluri într-un proiect cu costuri și rate de facturare diferite.

## <a name="create-tasks"></a>Crearea de activități
Creați două activități de proiect pentru 40 de ore fiecare, activitatea A și activitatea B. Selectați activitatea A ca predecesor pentru activitatea B.

## <a name="set-up-role-and-organization-unit-for-a-generic-project-team-member"></a>Configurați rolul și unitatea organizațională pentru un membru generic al echipei de proiect

1. Pe pagina **Planificare**, selectați rândul **Activitate** pentru Activitatea A. 
2. În câmpul **Resurse**, selectați **Creare** în lista verticală.
3. Pe pagina **Creare rapidă a membrilor echipei**, specificați atributele membrilor echipei generice care pot îndeplini această activitate.
4. Selectați rolul și unitatea organizațională corespunzătoare, apoi selectați **Salvați și închideți**. Un membru generic al echipei este creat și atribuit acestei activități. 

Repetați acești pași pentru Activitatea B și asigurați-vă că rolul și unitatea organizațională a membrilor echipei generice create pentru Activitatea B sunt diferite de Activitatea A. 

## <a name="set-up-role-and-organization-unit-for-a-project-task"></a>Configurați rolul și unitatea organizațională pentru o activitate de proiect

1. După ce creați Activitatea A, selectați activitatea, apoi selectați **Editați activitatea**.
2. Pe pagina **Detalii despre activitate** pagina, găsiți câmpurile **Rol** și **Unitate organizațională**, adăugați valorile necesare unei resurse care ar efectua această activitate. 

  > [!NOTE]
  > Dacă completați aceste scenarii utilizând datele demo ale Project Service Automation, selectați **Lider consultant** pentru rol și **Fabrikam SUA** ca unitate organizațională.

3. Selectați Activitatea B, apoi selectați **Editare activitate**.
4. Pe pagina **Detalii despre activitate** pagina, găsiți câmpurile **Rol** și **Unitate organizațională**, adăugați valorile necesare unei resurse care ar efectua această activitate. Asigurați-vă că valorile din câmpurile **Rol** și **Unitate organizațională** sunt diferite pentru sarcina B de valorile pentru sarcina A. 

  > [!NOTE]
  > Dacă completați aceste scenarii utilizând datele demo ale Project Service Automation, selectați **Tehnician rețea** pentru rol și **Fabrikam SUA** ca unitate organizațională.

5. Salvați și închideți pagina **Detalii activitate**. 

## <a name="team-member-and-estimates-behavior"></a>Membru al echipei și estimează comportamentul 

1. Pe pagina **Detalii despre activitate**, pe **Membru al echipei**, selectați cei doi membri generici ai echipei și apoi selectați **Generați cerințe**. 
2. Selectați rândul membrului echipei pentru **Lider consultant** și apoi selectați **Rezervare**. Tabloul de programare se deschide și rezervă o resursă pentru acea cerință.
3. Selectați rândul membrului echipei pentru **Tehnician rețea** și apoi selectați **Rezervare**. Tabloul de programare se deschide și rezervă aceeași resursă pentru acea cerință.

### <a name="team-member-grid"></a>Grila membrilor echipei 
Pe grila **Membru al echipei**, observați că cele două înregistrări generice ale membrilor echipei sunt șterse și au fost înlocuite cu o singură resursă. Există un set de valori pentru resursa respectivă care arată un set implicit de valori pentru **Rol** și **Unitate organizațională**.
Când extindeți rândul înregistrării acelui membru al echipei, puteți vedea atribuiri distincte în înregistrarea membrilor echipei pentru ambele activități. Fiecare rând de atribuire are valori specifice activității pentru **Rol** și **Unitate organizațională**. 

### <a name="estimates-grid"></a>Grilă estimări 
Când navigați la grila **Estimări**, veți observa că ambele activități pentru aceeași resursă au un preț diferit.
Atribuirea pentru resursa din Activitatea A este evaluată cu ajutorul valorii atributului **Rol** al **Lider consultant**. Atribuirea pentru aceeași resursă din Activitatea A este evaluată cu ajutorul valorii atributului **Rol** pentru **Tehnician rețea**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]