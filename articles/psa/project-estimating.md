---
title: Costuri și venit de proiect
description: Acest subiect furnizează informații despre estimarea costurilor și veniturilor proiectului.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: 48f313b15f788645b88a4d878e3bece419d63126
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6009181"
---
# <a name="project-costs-and-revenue"></a>Costuri și venit de proiect

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Estimările proiectului furnizează perspectiva financiară a lucrului estimat și planificat în planificarea proiectului. Fila **Estimări** de pe pagina **Proiecte** proiecte afișează impactul costurilor și veniturilor lucrului pe care îl planificați. De asemenea, oferă informații despre multe dimensiuni predefinite. 

> ![Fila Estimări](media/project-5.png)

## <a name="cost-and-sales-values-of-the-project"></a>Costul și valoarea de vânzărilor a proiectului

Listele de prețuri definesc costul și ratele de facturare pentru roluri într-un proiect. Aveți posibilitatea să determinați impactul activității asupra costului și veniturilor, pe baza rolurilor asociate cu numele poziției și cu resursa denumită care este atribuită unei activități. Dacă există activități care nu au nicio atribuire (generică sau denumită), nu puteți obține estimări de cost sau de vânzări. Valorile costurilor și vânzărilor consideră data care este definită în listele de prețuri.

### <a name="default-cost-price"></a>Preț de cost implicit  

Fiecare proiect aparține unei organizații. Această organizație este afișată în câmpul **Unitate contractantă** din proiect. Lista de prețuri asociată cu unitatea contractantă este utilizată pentru a determina prețul de cost unitar. Pentru a determina prețurile de cost corecte la roluri pentru data care este definită pe liniile de estimare, căutați combinația de rol, unitate și unitate organizațională din lista cu prețuri de cost. 

Astfel încât prețurile lor de cost pot fi calculate, toate activitățile trebuie să fie atribuite la o resursă. Orice activități neatribuite vor avea un preț de cost de 0,00.

Dacă combinația de rol, unitate și unitate organizatorică nu returnează un preț de cost din lista de prețuri a unității contractante, sistemul ignoră unitatea. În schimb, se caută combinația de doar rolul și unitatea organizațională. Dacă se găsește un preț de cost, factorii de conversie sunt utilizați pentru a-l converti în unitatea selectată pe linia de estimare.

Dacă combinația de rol și unitate organizatorică nu returnează un preț de cost, sistemul ignoră unitatea organizațională. În schimb, acesta caută combinația de rol și unitate pentru a seta prețul implicit (după ce se aplică orice conversie).

Dacă sistemul nu găsește un preț pentru rol, prețul de cost a liniei estimate este stabilit la o valoare implicită de **0,00**. Toate volumurile de cost de pe liniile de estimare a costului de proiect sunt înregistrate în moneda unității de contractare.

> [!NOTE]
> În mod implicit Microsoft Dynamics 365 stochează sumele de cost în moneda de bază. Cu toate acestea, volumurile costului care sunt afișate în fila **Estimări** sunt în moneda unității contractante.  

### <a name="default-sales-price"></a>Preț de vânzări implicit 

Lista de prețuri de vânzare este determinată fie de entitatea de vânzări la care este atașat proiectul, fie de clientul proiectului. Când o entitate de vânzări, ar fi oportunitate, ofertă sau contract, este asociată cu proiectul, prețul de vânzare al entității de vânzare este determinat de lista de prețuri asociată cu oferta sau contractul. Dacă ofeta sau contractul are o listă de prețuri particularizată, acea listă de prețuri este utilizată ca lista de prețuri implicitã pentru estimările de proiect. Dacă nu există nicio asociere cu entități de vânzări, lista de prețuri de vânzare implicită din parametri este utilizată ca listă de prețuri de vânzare implicită a proiectului, potrivită cu valuta clientului care este definită în proiect.

Fiecare linie estimativă are o unitate de resurse care este asociată cu aceasta. Unitatea de resurse indică unitatea organizatorică din care sunt rezervate resursele pentru a finaliza activitatea. Pentru a determina prețul de vânzare pentru rolurile asociate, căutați combinația dintre rol, unitate și unitate de resurse din lista de prețuri de vânzare. Dacă nu există atribuiri în activitate, prețul de vânzare pentru activitate este 0,00.

Dacă combinația de rol, unitate și unitate de resurse nu întoarce un preț de vânzare din lista de prețuri de vânzare, sistemul ignoră unitatea. În schimb, acesta caută combinația de doar rolul și unitatea de resurse. Dacă se găsește un preț de vânzări, se utilizează factorii de conversie pentru a-l converti la unitatea pe care ați selectat-o pe linia estimărilor de vânzări. 

Dacă combinația de rol și unitate de resurse nu întoarce un preț de vânzare din lista de prețuri de vânzare, sistemul ignoră unitatea de resurse. În schimb, acesta caută combinația de rol și unitate pentru a seta prețul implicit (după ce se aplică orice conversie).

Dacă sistemul nu găsește un preț pentru rol, prețul de vânzări al liniei estimate este stabilit la o valoare implicită de **0,00**.

Fila **Estimări** are o vizualizare grilă care afișează linii de estimare. Grila include coloanele pentru unitate, prețul total de cost și prețul total de vânzare, așa se arată în ilustrația următoare. 

> ![Vizualizare grilă pe fila Estimări](media/project-6.png)

## <a name="time-phased-view-of-project-estimates"></a>Vizualizarea pe etape a estimărilor proiectului

Vizualizarea pe etape a estimărilor de proiect arată datele estimate din vizualizarea grilă din cronologie, într-o scală de timp selectată. În mod implicit, datele estimate sunt pivotate pe dimensiunea **Rolului**.

> ![Vizualizarea pe etape pentru estimările proiectului](media/project-7.png)

## <a name="allocating-estimated-effort-based-on-the-task-mode"></a>Alocarea efortului estimat pe baza modului de activitate

În vizualizarea pe etape, distribuiți efortul total estimat pentru activitate este distribuit prin alocarea unui anumit număr de ore de efort în perioada de timp din scala de timp selectată. Modul de activitate determină cât efort este alocat pe durata activității. Cele două tipuri de alocare sunt **Uniform** și **Pe baza orelor de lucru**.

### <a name="work-hours-based-allocation"></a>Alocare pe baza orelor de lucru
 
În modul de activitate de planificare automată, orele implicite zilnice pentru resursele de activitate sunt setate la rata completă a orei de lucru. Acest comportament se aplică atunci când efortul este alocat împărțindu-l pe durata activității în vizualizarea pe etape. De exemplu, dacă estimați că o activitate va fi terminată de o resursă în scala de timp **Zi**, efortul care este alocat pe zi nu va depăși orele de lucru pe zi care sunt definite în calendarul de proiect. Prin urmare, alocarea efortului asigură întotdeauna că resursele sunt estimate pentru a fi utilizate întreaga zi.

### <a name="even-allocation"></a>Alocare uniformă

În modul de activitate planificat manual, orele de lucru din calendarul proiectului nu sunt utilizate. În schimb, planificarea activității se bazează pe intrările de la utilizator. Pentru aceste activități, alocarea efortului pentru fiecare perioadă de timp de unitate în scara de timp selectată nu are niciun factor de limitare. Efortul total pentru activitate este împărțit în mod egal și alocat pentru fiecare perioadă de timp de unitate din sclra de timp aleasă. Prin urmare, modul de activitate definit pentru activitate determină distribuirea efortului sau alocarea efortului pentru fiecare perioadă de timp în estimări pe etape.

## <a name="grouping-and-time-phasing-options"></a>Opțiuni de grupare și etape

Această vizualizare pe etape arată distribuția estimărilor de efort, cost și vânzări zilnice, săptămânale, lunare sau anuale. În mod implicit, datele estimate sunt pivotate pe dimensiunea **Rolului**. Cu toate acestea, puteți utiliza opțiunea **Grupare după** pentru a pivota pe două alte dimensiuni: **Categorie** și **Resursă**.

Atât în vizualizarea grilă cât și în vizualizarea pe etape, aveți posibilitatea să selectați ce câmpuri sunt afișate. Totalurile pentru fiecare bloc de timp sunt afișate în partea de jos a proiectului. Acestea arată efortul total estimat, costul și vânzările pentru zi, săptămână, lună sau an. Prețul implicit de cost și prețul de vânzare sunt pentru data efectivă. Cu alte cuvinte, acestea se modifică pentru fiecare resursă, pe baza vizualizării pe etape pe care o selectați.

## <a name="expense-estimates"></a>Estimări de cheltuieli

Butonul **Adăugați o nouă estimare de cheltuieli** în vizualizarea grilă vă permite să înregistrați orice cheltuieli care sunt achitate în proiect, dar care nu sunt direct legate de muncă. Aveți posibilitatea să înregistrați estimările de cheltuieli pentru o anumită activitate sau pentru întregul proiect. Selectați categoriile de cheltuieli și data orientativă atunci când vă așteptați să achite cheltuielile. Dacă lista de prețuri de cost și lista de prețuri de vânzări au prețuri implicite (sau dacă procentele de adaos sunt definite pentru categorii de cheltuială), sunt introduse automat pe linia de estimare când are loc asocierea.


[!INCLUDE[footer-include](../includes/footer-banner.md)]