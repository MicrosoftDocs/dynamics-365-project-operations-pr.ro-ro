---
title: Recuperarea TVA în gestionarea cheltuielilor
description: Acest articol explică modul de primire a rambursărilor pentru tranzacțiile eligibile cu taxa pe valoarea adăugată (TVA).
author: suvaidya
ms.date: 10/10/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 1df921bbef4c11c7e07ed38775644117215a50fb
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927941"
---
# <a name="vat-recovery-in-expense-management"></a>Recuperarea TVA în gestionarea cheltuielilor

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

Pentru a primi rambursări pentru tranzacțiile eligibile cu taxa pe valoarea adăugată (TVA), o companie sau organizație trebuie să identifice, să colecteze, să verifice și să transmită informații exacte. Acest proces include sarcini multiple și, în funcție de mărimea companiei dvs., poate include mai mulți angajați sau roluri.

Pentru a recupera TVA în modulul **Gestionarea cheltuielilor**, trebuie îndeplinite următoarele condiții prealabile:

- Trebuie create coduri fiscale pentru țările/regiunile care sunt alocate categoriilor de cheltuieli.
- Trebuie creat un grup de taxe pe vânzări pentru fiecare cod fiscal.
- Trebuie creat un cod de element de taxe pe vânzări pentru fiecare grup de taxe pe vânzări.

După finalizarea condițiilor prealabile, trebuie parcurși următorii pași pentru a solicita rambursări pentru tranzacțiile cu TVA.

1. Într-un raport de cheltuieli, introduceți informații fiscale despre tranzacțiile cu cardul de credit pentru a identifica rambursările eligibile de TVA.
2. Verificați dacă toate informațiile fiscale sunt complete, apoi încărcați raportul de cheltuieli.
3. Procesați cheltuielile care sunt eligibile pentru recuperarea internațională a TVA.
4. Trimiteți date de recuperare TVA furnizorului terț pentru a depune declarații internaționale de recuperare.
5. Cheltuieli de proces pentru recuperarea TVA internă.

Următoarele secțiuni oferă exemple care arată modul în care angajații Contoso finalizează fiecare pas.

## <a name="enter-tax-information-about-credit-card-transactions-to-identify-eligible-vat-refunds"></a>Introduceți informații fiscale despre tranzacțiile cu cardul de credit pentru a identifica rambursările eligibile de TVA

Constanța, un reprezentant de vânzări Contoso, cu sediul în Statele Unite, s-a întors recent dintr-o călătorie de vânzări în Regatul Unit. În timpul călătoriei, Constanța a suportat niște cheltuieli personale cu cardul de credit pentru mese. Constanța trebuie acum să creeze un raport de cheltuieli pentru a concilia cheltuielile.

Când Constanța introduce informații despre raportul de cheltuieli, ea selectează **Regatul Unit** în câmpul **Țară/regiune** pe pagina **Editați raportul de cheltuieli**. Lista grupurilor de taxe pe vânzări este apoi filtrată astfel încât să afișeze numai grupurile care se aplică Regatului Unit. Cosntanța selectează grupul de taxe **Regatul Unit 001** pe vânzări și apoi selectează elementul **Mese** de grup de impozit pe vânzări. Apoi, Constanța adaugă o nouă tranzacție pentru cazare. Deoarece există un singur grup de taxe pe vânzări și un grup de taxe pe vânzări pentru un articol în Regatul Unit, aceste informații sunt completate automat în raportul de cheltuieli al Constanței.

Conform politicii Contoso, toate cheltuielile trebuie să aibă o chitanță corespunzătoare. Prin urmare, atunci când Constanța salvează raportul de cheltuieli, primește un mesaj care spune că trebuie să atașeze o chitanță pentru fiecare tranzacție pe care a enumerat-o în raportul de cheltuieli. Constanța verifică că a atașat o imagine digitală a fiecărei chitanțe de tranzacție la raportul de cheltuieli și apoi își trimite raportul pentru aprobare. Apoi trimite chitanțele de hârtie către echipa de procesare back-office. Această echipă va trimite datele de recuperare a TVA furnizorului terț care depune declarații internaționale de recuperare a TVA pentru Contoso.

## <a name="verify-tax-information-and-post-an-expense-report"></a>Verificați informațiile fiscale și publicați un raport de cheltuieli

Înainte ca April, coordonatorul de conturi de furnizori pentru Contoso poate publica un raport de cheltuieli, trebuie să introducă orice informație fiscală care îi lipsește. Ea deschide pagina **Detalii raport cheltuieli** și vede raportul de cheltuieli aprobat de Constanța. April deschide apoi raportul de cheltuieli pentru a vizualiza detaliile tranzacțiilor. Ea vede că Constanța nu a intrat într-un grup de impozite pe vânzări pentru una dintre tranzacții. Deoarece aceste informații nu sunt furnizate, April nu poate posta raportul de cheltuieli. Prin urmare, ea se uită la pagina **Configurații fiscale** din Gestionarea cheltuielilor și găsește grupul adecvat de impozitare pe vânzări pentru țară/regiune și tipul tranzacției. April poate posta acum raportul de cheltuieli la registrul general.

Când April publică raportul de cheltuieli, se creează un articol de lucru recuperabil din TVA. Acest articol de lucru este atribuit unui membru al echipei de procesare back-office. April primește un mesaj care confirmă că postarea a avut succes. Acest mesaj listează, de asemenea, numărul de tranzacții cu TVA care au fost identificate pentru recuperare.

## <a name="process-expenses-that-are-eligible-for-international-vat-recovery"></a>Procesați cheltuielile care sunt eligibile pentru recuperarea internațională a TVA

Arnie, membru al echipei de procesare back-office a Contoso, este responsabil pentru verificarea faptului că toate informațiile necesare pentru recuperarea TVA sunt incluse în rapoartele de cheltuieli. El deschide pagina **Recuperarea cheltuielilor fiscale** și selectează raportul de cheltuieli trimis de Constanța. Arnie verifică apoi că toate chitanțele necesare sunt atașate și că au fost introduse codurile corecte ale taxei de vânzare și articolului.

Când Arnie primește chitanțele pe hârtie de la Constanța, le verifică împotriva chitanțelor digitale și apoi schimbă starea raportului de cheltuieli în **Gata pentru recuperare**.

## <a name="send-vat-recovery-data-to-the-third-party-vendor"></a>Trimiteți date de recuperare TVA furnizorului terț

Când Arnie este gata să trimită datele raportului de cheltuieli furnizorului terț care va depune declarațiile de recuperare a TVA, acesta deschide pagina **Recuperarea cheltuielilor fiscale**. El filtrează pagina astfel încât să afișeze numai rapoartele de cheltuieli marcate ca **Gata pentru recuperare**. Arnie selectează apoi **Fişier** &gt; **Exportați în Excel**. Informațiile TVA din rapoartele de cheltuieli sunt exportate către o foaie de lucru Microsoft Excel. Arnie trimite această foaie de lucru furnizorului terță parte și include un mesaj care spune că bonurile de hârtie au fost trimise prin curier.

## <a name="process-expenses-for-domestic-vat-recovery"></a>Cheltuieli de proces pentru recuperarea TVA internă

Arnie trebuie să verifice dacă tranzacțiile raportului de cheltuieli sunt eligibile pentru recuperarea TVA și că chitanțele digitale sunt atașate rapoartelor. Pentru a începe procesarea cheltuielilor eligibile pentru recuperarea internă, Arnie deschide pagina **Recuperarea cheltuielilor fiscale** și selectează raportul de cheltuieli care necesită verificare. El verifică dacă chitanțele sunt în numele companiei în locul angajatului. (Pentru recuperarea TVA, chitanțele trebuie să fie pe numele companiei.) Arnie verifică apoi că toate chitanțele necesare sunt atașate și că au fost introduse codurile corecte ale taxei de vânzare și articolului.

Când Arnie primește chitanțele pe hârtie, el schimbă starea raportului de cheltuieli în **Gata pentru recuperare**. Apoi poate depune declarația la autoritatea fiscală competentă. În acest caz, autoritatea fiscală corespunzătoare din Statele Unite este Internal Revenue Service (IRS).


[!INCLUDE[footer-include](../includes/footer-banner.md)]