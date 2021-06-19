---
title: Configurarea șabloanelor de cost
description: Acest subiect oferă informații despre cum să creați și să utilizați șabloanele de cost în Project Operations.
author: sigitac
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: f4a515db31a31028af4a60927ab360be6c261a3f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013906"
---
# <a name="set-up-cost-templates"></a>Configurarea șabloanelor de cost

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_


Acest subiect oferă informații despre cum să creați și să utilizați șabloanele de cost în Project Operations. Un șablon de cost determină:

- Categoriile de proiecte pentru tranzacțiile prognozate și efective să fie incluse într-un procent din calculul finalizării proiectului. Valoarea procentuală completă este apoi utilizată pentru a calcula cât de mult venit este recunoscut.
- Dacă procentul de finalizare poate fi modificat dacă este calculat automat.
- Dacă procentul complet este calculat pe baza sumelor sau a unităților.

## <a name="cost-template-example"></a>Exemplu de șablon de cost

Lucrați la un proiect de proiectare a site-ului web pentru un client în care percepeți o taxă forfetară de 10.000 USD. Ați prognozat că va dura 100 de ore (5.000 USD) pentru finalizarea proiectului. De asemenea, prognozați două bilete de avion și patru nopți într-un hotel pentru călătorii la site-ul clientului (1.800 USD). Acest lucru are ca rezultat un cost total estimat de USD 6.800.

Când executați procesul de recunoaștere a veniturilor cu preț fix pentru a crea o estimare la sfârșitul lunii, constatați că ați lucrat 35 de ore la proiect. Aceasta nu include încă zborurile sau costurile hotelului. De asemenea, ați avut un asistent care a efectuat cinci ore de cercetare pentru proiect la un cost de 100 USD, pe care nu l-ați planificat.

Când calculați valoarea procentuală completă pentru acest proiect, aveți de făcut următoarele alegeri:

- Doriți să includeți toate costurile (ore și cheltuieli) sau doar ore?
- Doriți să includeți toate orele sau doar orele planificate?
- Doriți să calculați procentul complet pe baza costului în dolari al orelor planificate (5.000 USD) sau doar pe numărul de ore (100)?

Răspunsurile dvs. la aceste întrebări determină opțiunile pe care le setați pe șablonul de cost și categoriile pe care le selectați pe liniile șablonului de cost.

Tabelul următor ilustrează rezultatele diferitelor metode de calcul al valorii procentuale complete pentru acest scenariu.

| Finalizare bazată pe | Costul în dolari sau unitățile | Procentaj finalizat | Calcul |
| --- | --- | --- | --- |
| Toate orele, fără cheltuieli | Costul în dolari | 37% 35 x 50 USD + 100 USD = 1.850 USD 1.850/5.000 USD |
| Toate orele, fără cheltuieli | Unități | 40% | 40 ore/100 ore (inclusiv cinci ore neplanificate) |
| Ore planificate, fără cheltuieli | Costul în dolari sau unitate | 35% | 35/100 ore sau 35 x 50/5.000 USD |
| Toate orele și cheltuielile | Costul în dolari | 27,2% | 1.850 USD/6.800 USD |

Decizia ce abordare trebuie adoptată pentru a crea un șablon de cost poate depinde de mai multe considerații:

- Dacă includeți ore neplanificate în șablonul de costuri, riscați să ajungeți la 100% la finalizarea proiectului. Acest lucru se datorează faptului că orele reale vor fi mai mari decât orele planificate. Dacă utilizați oricare dintre primele două metode enumerate în tabel, ar trebui să modificați planul (unități prognozate) atunci când veți cunoaște abaterile. În acest caz, ați adăuga sau scădea ore pe baza cunoștințelor dvs. despre ceea ce este necesar pentru finalizarea proiectului. Dacă proiectul va necesita încă 65 de ore pentru finalizare, ați adăuga cinci ore la plan pentru un total de 105. Dacă știți că asistentul dvs. va efectua alte cinci ore de cercetare, totalul va deveni 110 ore.
- Dacă utilizați a treia metodă enumerată în tabel, veți actualiza doar orele planificate pentru timpul dvs. pentru a menține calculul procentual complet corect. Profitabilitatea dvs. se va schimba atunci când sunt înregistrate orele neplanificate, dar veți rămâne pe o traiectorie procentuală cunoscută.
- Dacă utilizați a patra metodă enumerată în tabel, riscul este ca cheltuielile să aibă loc în momente neregulate și să nu se reflecte în progresul finalizat. Prin urmare, dacă sunt incluse cheltuielile, acestea pot face ca procentul dvs. complet să fluctueze mai mult decât este de dorit. De exemplu, pentru că nu ați luat încă un zbor, procentul complet a fost de 27 la sută în loc de 35 la sută sau 37 la sută dacă ar fi să calculați calculul numai în timp. Dacă ați fi făcut o călătorie timp de două nopți și ați fi prevăzut cu precizie costurile de zbor și hotel, procentul complet ar fi fost de 40,4% (1850 USD pentru forța de muncă și 900 USD pentru cheltuieli = 2750 USD/6800 USD = 40,4%). Prin urmare, suportarea cheltuielilor pentru o singură călătorie cu avionul ar schimba procentul complet de la 27 la sută la 40 la sută.

## <a name="create-cost-templates"></a>Creați șabloane de cost
Pentru a crea șabloane de cost, urmați acești pași:

1. Pentru a accesa șabloane de cost, în mediul Dynamics 365 Finance, accesați **Management de proiect și contabilitate** > **Configurare** > **Estimări** > **Șablon de cost**.
2. Selectați **Nou** pentru a crea un șablon nou de cost. Introduceți un nume și descriere.
3. Furnizați codul liniei de cost pentru fiecare tip de tranzacție.
4. Selectați o metodă implicită de finalizare:

  - **Automat**: procentul de finalizare este calculat automat pentru un proiect. Valoarea rezultată nu poate fi modificată.
  - **Manual**: procentul de finalizare este calculat automat pentru un proiect. Valoarea rezultată poate fi modificată.

  > [!NOTE]
  > Pentru calculele manuale, procentul de finalizare este menținut în **Calcul manual** pe fila **General** de pe pagina **Estimare**.

5. În **Finalizare bazată pe**, selectați una dintre următoarele valori:

  - **Cantitate**: suma în moneda contabilă calculează procentul de finalizare.
  - **Unitate**: cantitatea calculează procentul de finalizare.
  - **Linie dreaptă**: sistemul calculează procentul de finalizare în mod proporțional utilizând datele de început și de sfârșit ale proiectului pentru a determina durata proiectului.

6. Selectați **Linii de cost** pentru a revizui liniile de cost ale șablonului de costuri. Este necesar cel puțin o linie de cost pentru fiecare tip de tranzacție. Cu toate acestea, puteți crea mai multe linii de cost pentru aceleași tipuri de tranzacții și puteți seta atributele dorite pentru aceste linii.
7. Pe fila **Categorii**, selectați categoriile de proiecte care vor fi incluse pe linia șablonului de cost.
8. Pe fila **General**, selectați dacă această linie va fi inclusă în procentul de calcul de finalizare.
9. Selectați metoda costului de finalizat care va fi utilizată la calcularea procentului de finalizare.


[!INCLUDE[footer-include](../includes/footer-banner.md)]