---
title: Rezolvarea prețurilor de vânzări pentru estimări de proiect și date reale
description: Acest subiect oferă informații despre rezolvarea prețurilor de vânzare pe estimările și realitățile proiectului.
author: rumant
manager: Annbe
ms.date: 04/07/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3bf4686b414300370e6b364834b33edad98b7f39
ms.sourcegitcommit: ac90be6106592f883a0de39a75836fb40255d65a
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 04/09/2021
ms.locfileid: "5877371"
---
# <a name="resolve-sales-prices-for-project-estimates-and-actuals"></a>Rezolvarea prețurilor de vânzări pentru estimări de proiect și date reale

_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_

Când prețurile de vânzare pentru estimări și valori reale sunt rezolvate în Dynamics 365 Project Operations, sistemul folosește mai întâi data și moneda ofertei sau contractului aferent proiectului pentru a rezolva lista de prețuri de vânzare. După rezolvarea listei de prețuri de vânzare, sistemul rezolvă rata vânzărilor sau a facturilor.

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-time"></a>Rezolvați ratele de vânzare pe datele reale și estimate pentru timp

În Project Operations, liniile de estimare pentru timp sunt utilizate pentru a indica linia de ofertă și detaliile liniei contractului pentru timp și alocările de resurse din proiect.

După ce se rezolvă o listă de prețuri pentru vânzări, sistemul parcurge următorii pași pentru a stabili implicit rata facturării.

1. Sistemul utilizează câmpul **Rol** și **Unitatea de resurse** pe linia estimată pentru timp, pentru a se potrivi cu rolul liniilor de prețuri în lista de prețuri rezolvate. Această potrivire presupune că utilizați dimensiuni de stabilire a prețurilor predefinite pentru rate de facturare. Dacă ați configurat prețurile pe baza oricăror altor câmpuri în loc de sau în plus față de **Rol** și **Unitate de resurse**, atunci aceasta este combinația care va fi utilizată pentru a regăsi o linie de preț de rol potrivită.
2. Dacă sistemul găsește o linie de preț de rol care are o rată de facturare pentru combinația de câmpuri **Rol** și **Unitate de resurse**, atunci aceasta este rata de facturare implicită.
3. Dacă sistemul nu poate potrivi valorile de câmp **Rol** și valorile de câmp **Unitate de resurse** , atunci aceasta întoarce liniile de preț ale rolului cu un rol de potrivire, dar valori nule de **Unitate de resurse**. După ce sistemul găsește o înregistrare de preț de rol potrivită, va seta implicit rata facturării din acea înregistrare. Această potrivire presupune o configurație out-of-the-box pentru prioritatea relativă a **Rol** vs. **Unitate de resurse** ca dimensiune a prețurilor de vânzare.

> [!NOTE]
> Dacă ați configurat o prioritate diferită de **Rol** și **Unitate de resurse**, sau dacă aveți alte dimensiuni care au prioritate mai mare, acest comportament se va schimba în consecință. Sistemul preia înregistrările prețului de rol cu valori care se potrivesc fiecăreia dintre valorile parametrilor de stabilire a prețurilor în ordinea priorității, cu rânduri care au valori nule pentru dimensiunile din urmă.

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-expense"></a>Rezolvați ratele de vânzare pe datele reale și estimate pentru cheltuială

În Project Operations, liniile de estimare pentru cheltuială sunt utilizate pentru a indica linia de ofertă și detaliile liniei contractului pentru cheltuială și liniile estimate de cheltuieli pe proiect.

După ce se rezolvă o listă de prețuri pentru vânzări, sistemul parcurge următorii pași pentru a stabili implicit prețul de vânzare pe unitate.

1. Sistemul utilizează combinația de câmpuri **Categorie** și **Unitate** pe linia de estimare pentru ca o cheltuială să se potrivească cu liniile de categorii de preț în lista de prețuri care a fost rezolvată.
2. Dacă sistemul găsește o linie de preț de categorie care are o rată de vânzări pentru combinația de câmp **Categorie** și **Unitate**, atunci rata de vânzare este implicită.
3. Dacă sistemul găsește o linie de preț de categorie potrivită, metoda de stabilire a prețurilor poate fi utilizată pentru a seta implicit prețul de vânzare. Următorul tabel de mai jos prezintă comportamentul de neplată a prețului cheltuielilor în Project Operations.

    | Context | Metodă de stabilire a prețului | Preț implicit |
    | --- | --- | --- |
    | Estimată | Preț unitar | Pe baza liniei de preț a categoriei |
    | &nbsp; | La cost | 0.00 |
    | &nbsp; | Adaos peste cost | 0.00 |
    | Real | Preț unitar | Pe baza liniei de preț a categoriei |
    | &nbsp; | La cost | Pe baza costului real aferent |
    | &nbsp; | Adaos peste cost | Aplicați un adaos așa cum este definit de linia de preț a categoriei pe rata de cost unitară a costului aferent real |

4. Dacă sistemul nu este în măsură să se potrivească cu valorile de câmp **Categorie** și **Unitate**, rata de vânzare este implicită la zero (0).

## <a name="resolving-sales-rates-on-actual-and-estimate-lines-for-material"></a>Rezolvarea ratelor de vânzări pe liniile reale și estimări pentru material

În Project Operations, liniile de estimare pentru material sunt utilizate pentru a indica detaliile liniei de ofertă și a liniei de contract pentru materiale și liniile de estimare a materialului din proiect.

După ce se rezolvă o listă de prețuri pentru vânzări, sistemul parcurge următorii pași pentru a stabili implicit prețul de vânzare pe unitate.

1. Sistemul utilizează combinația de câmpuri **Produs** și **Unitate** pe linia estimativă pentru material pentru a se potrivi cu liniile de articole din lista de prețuri din lista de prețuri care a fost rezolvată.
2. Dacă sistemul găsește o listă de articole din lista de prețuri care are o rată de vânzare pentru combinația de câmp **Produs** și **Unitate** și metoda de stabilire a prețurilor este **Suma monedei**, se folosește prețul de vânzare specificat pe linia listei de prețuri.
3. Dacă valorile de câmp **Produs** și **Unitate** nu se potrivesc, rata de vânzare este implicită la zero.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
