---
title: Determinați costurile de proiect și estimările de venituri
description: Cum să determinați costurile de proiect și estimările de venituri în Project Service
author: ruhercul
manager: kfend
ms.prod: ''
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 851e98cf5481ec7df3f430801a9d3b327794f68c
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5284958"
---
# <a name="determine-project-cost-and-revenue-estimates"></a>Determinați costurile de proiect și estimările de venituri 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Estimările proiectului oferă perspectiva financiară a lucrului estimat și planificat în structura detaliată a proiectului. Vizualizarea cu estimări vă informează în legătură cu costurile și veniturile lucrului planificat. Vizualizarea cu estimări oferă un instrument pentru a vedea informații despre o serie de dimensiuni predefinite, ca să beneficiați de cele mai bune date despre impactul financiar al proiectului.  
  
## <a name="cost-and-sales-value-of-the-project"></a>Costul și valoarea vânzărilor proiectului  
Listele de prețuri [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] definesc costul și tarifele pentru rolurile utilizate de proiecte. În funcție de rolurile asociate cu activitățile din structura detaliată a proiectului, puteți determina impactul costurilor și veniturilor pentru lucrul implicat.  
  
## <a name="cost-price-defaulting"></a>Prețul de cost implicit  
Fiecare proiect face parte dintr-o organizație (indicat în **Unitate deținătoare** din proiect). Lista de prețuri asociată cu unitatea organizațională deținătoare determină prețul de cost unitar. [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] determină prețurile de cost pentru roluri, căutând combinația de rol, unitate și unitate organizațională în lista de prețuri de cost, pentru a obține prețul de cost corect pentru data efectivă în liniile de estimare.  
  
În cazul în care combinația rol, unitate și unitatea organizațională nu are ca rezultat un preț de cost din lista de prețuri a unității deținătoare, unitatea este ignorată în favoarea combinației de rol și unitate organizațională. În cazul în care există un preț de cost, acest preț este transformat în unitatea pe care ați ales-o în linia de estimare.  
  
Dacă combinația de rol și unitate organizațională nu are ca rezultat un preț de cost, unitatea organizațională este ignorată în favoarea combinației de rol și unitate, iar prețul are o valoare implicită după aplicarea oricărei conversii, dacă este necesar.  
  
 Dacă nu există un preț pentru rol, atunci prețul de cost devine implicit 0,00 în linia de estimare.  
  
 Toate valorile de costuri din liniile de estimare a costurilor de proiect sunt în moneda unității organizaționale deținătoare.  
  
## <a name="sales-price-defaulting"></a>Prețul de vânzări implicit  
Lista de prețuri de vânzare se bazează pe entitatea de vânzări de care aparține proiectul. Lista de prețuri de vânzări asociată cu oferta sau contractul determină prețul de vânzări unitar. Dacă oferta sau contractul are o listă de prețuri particularizată, aceasta este lista de prețuri implicitã pentru estimările de proiect. În cazul în care nu există nicio asociere cu entitățile de vânzări, atunci lista de prețuri de vânzări implicită configurată în setări de parametri va fi lista de prețuri de vânzări implicită pentru proiect. Fiecare linie de estimare are asociată o unitate organizațională de resurse pentru a indica unitatea organizațională de la care vor fi rezervate resursele pentru efectuarea activității. Prețul de vânzări pentru rolurile asociate se determină prin căutarea combinației de rol, unitate și unitate organizațională de resurse în lista de prețuri de vânzări, pentru a obține prețul de vânzări corect pentru data efectivă în liniile de estimare.  
  
În cazul în care combinația de rol, unitate și unitate organizațională de resurse nu are drept rezultat un preț de vânzări din lista de prețuri de vânzări, sistemul va ignora unitatea și va căuta combinația de rol și unitate organizațională de resurse. În cazul în care se găsește un preț de vânzări, acesta este transformat în unitatea pe care ați ales-o în linia de estimare a vânzărilor.  
  
Dacă sistemul nu găsește un preț pentru rol, atunci prețul de vânzări devine implicit 0,00 în linia de estimare.  
  
Vizualizarea de estimări are o grilă care afișează o grilă brută cu linii de estimare cu unitatea, costul unitar și prețul de vânzare.  
  
## <a name="time-phased-view-of-project-estimates"></a>Vizualizarea pe etape a estimărilor proiectului  
În vizualizarea pe etape a estimărilor de proiect, datele estimate din vizualizarea grilă sunt pivotate în mod implicit după rol și se afișează o desfășurare a datelor estimate în cronologia din scara de timp aleasă.  
  
## <a name="effort-estimate-allocation-based-on-task-mode"></a>Alocarea efortului estimat bazată pe modul de activitate  
În vizualizarea pe etape, efortul total estimat pentru activitate este distribuit prin alocarea unui anumit număr de ore de efort pentru fiecare perioadă de timp de unitate din scara de timp aleasă. În Project Service, modul de activitate determină cât efort este alocat pe durata activității. Cele două tipuri de alocare sunt alocarea uniformă și alocarea pe baza orelor de lucru. 
  
## <a name="work-hours-based-allocation"></a>Alocare pe baza orelor de lucru  
Modul de activitate planificat automat pentru o activitate reglementează numărul de resurse estimate pentru activitate; acestea sunt estimate a fi utilizate pentru toate orele de lucru zilnice. Acest lucru este valabil atunci când se alocă efortul prin scindarea lui pe durata activităților, și în vizualizarea pe etape. De exemplu, într-o scară de timp „Zi”, pentru o activitate estimată a fi efectuată de o resursă, efortul alocat pe zi nu va depăși orele de lucru zilnice definite în calendarul proiectului. Prin urmare, alocarea efortului asigură întotdeauna că resursele sunt estimate a fi utilizate pentru întreaga zi.  
  
## <a name="even-distribution"></a>Distribuire uniformă  
Modul de activitate planificat manual nu onorează orele de lucru, calendarul de proiect sau numărul de resurse definite pentru activitate. Planificarea activităților se bazează pe date introduse de utilizator. Pentru astfel de activități, alocarea efortului pentru fiecare perioadă de timp de unitate din scara de timp aleasă nu are factori de limitare. Efortul total pentru activitate este scindat în mod egal și alocat pentru fiecare perioadă de timp de unitate din scara de timp aleasă.  
  
În acest fel, modul de activitate definit pentru activitate determină distribuirea efortului sau alocarea efortului pentru fiecare perioadă de timp de unitate în timp - estimări în etape.  
  
## <a name="grouping-and-time-phasing-options"></a>Opțiuni de grupare și etape  
Această vizualizare vă ajută să înțelegeți distribuirea efortului, costurile și estimările de vânzare după zi, săptămână, lună sau an. Opțiunea Grupare după permite pivotarea datelor estimate în două alte dimensiuni: categorie și resurse. În vizualizarea grilă și vizualizarea pe etape, puteți să alegeți câmpurile care să fie afișate. Totalurile pentru fiecare bloc de timp sunt afișate în partea de jos, indicând efortul total estimat, costul și vânzările pentru ziua, săptămâna, luna sau anul în cauză.  
  
Prețul implicit de cost și prețul de vânzare este pentru data efectivă. Când tarifele pentru roluri se modifică, va deveni mai transparent în vizualizarea pe etape atunci când se vizualizează datele estimate pivotate în „Resursă” și în timpul segmentat după săptămână.  
  
## <a name="expense-estimates"></a>Estimări de cheltuieli  
Orice cheltuială care va fi suportată în cadrul proiectului care nu este direct legată de activitatea care urmează să fie extinsă poate fi înregistrată în estimările de proiect din vizualizarea grilă. Puteți face acest lucru utilizând **Adăugați estimarea de cheltuieli** din vizualizarea grilă. Estimările de cheltuieli pot fi înregistrate pentru o anumită activitate sau pentru întregul proiect. Puteți alege categoriile de cheltuieli pe aceste linii și puteți alege o dată provizorie când se așteaptă ca respectiva cheltuiala să fie suportată. Dacă listele de prețuri de costuri și vânzări au prețuri implicite sau s-au definit procente de adaos pentru categoriile de cheltuieli, valoarea implicită va fi linia de estimare din asociere.  
  
### <a name="see-also"></a>Consultați și  
 [Ghidul Managerului de proiect](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]