---
title: Recuperarea TVA
description: Acest subiect explică modul de recuperare a rambursărilor pentru tranzacțiile cu taxa pe valoarea adăugată (TVA).
author: saraschi2
manager: AnnBe
ms.date: 02/26/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 187532281f6aba3cc3fb03428d93c8ebc4cf4a3d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271947"
---
# <a name="vat-recovery"></a>Recuperarea TVA 

Pentru a primi rambursări pentru tranzacțiile eligibile cu taxa pe valoarea adăugată (TVA), o companie sau organizație trebuie să identifice, să colecteze, să verifice și să transmită informații exacte. Acest proces include sarcini multiple și, în funcție de mărimea companiei dvs., poate include mai mulți angajați sau roluri.

Pentru a recupera TVA utilizând Gestionarea cheltuielilor, trebuie îndeplinite următoarele condiții prealabile:

- Trebuie create coduri fiscale pentru țările/regiunile care sunt alocate categoriilor de cheltuieli.
- Trebuie creat un grup de taxe pe vânzări pentru fiecare cod fiscal.
- Trebuie creat un cod de element de taxe pe vânzări pentru fiecare grup de taxe pe vânzări.

După finalizarea condițiilor prealabile, angajații parcurg următorii pași pentru a solicita rambursări pentru tranzacțiile cu TVA.

1. Într-un raport de cheltuieli, introduceți informații fiscale despre tranzacțiile cu cardul de credit pentru a identifica rambursările eligibile de TVA.
2. Asigurați-vă dacă toate informațiile fiscale sunt complete, apoi încărcați raportul de cheltuieli.
3. Procesați cheltuielile care sunt eligibile pentru recuperarea internațională a TVA.
4. Trimiteți date de recuperare TVA furnizorului terț pentru a depune declarații internaționale de recuperare.
5. Cheltuieli de proces pentru recuperarea TVA internă.

Următoarele secțiuni oferă exemple care arată modul în care angajații Contoso finalizează fiecare pas.

## <a name="on-an-expense-report-enter-tax-information-about-credit-card-transactions-to-identify-eligible-vat-refunds"></a>Într-un raport de cheltuieli, introduceți informații fiscale despre tranzacțiile cu cardul de credit pentru a identifica rambursările eligibile de TVA

Constanța, un reprezentant de vânzări Contoso, cu sediul în SUA, s-a întors recent dintr-o călătorie de vânzări în Regatul Unit. În timpul călătoriei sale, a suportat niște cheltuieli personale cu cardul de credit pentru mese. Constanța trebuie acum să creeze un raport de cheltuieli pentru a-și concilia cheltuielile.

Când Constanța introduce informații despre raportul său de cheltuieli, ea selectează **Regatul Unit** în câmpul **Țară/regiune** pe pagina **Editați raportul de cheltuieli**. Lista grupurilor de taxe pe vânzări este apoi filtrată astfel încât să afișeze numai grupurile care se aplică Regatului Unit. Cosntanța selectează grupul de taxe **Regatul Unit 001** pe vânzări și apoi selectează elementul **Mese** de grup de impozit pe vânzări. Apoi adaugă o nouă tranzacție pentru cazarea sa. Deoarece există un singur grup de taxe pe vânzări și grupul de taxe pe vânzări pentru un articol în Regatul Unit, aceste informații sunt completate automat în raportul de cheltuieli al Constanței.

Conform politicii Contoso, toate cheltuielile trebuie să aibă o chitanță corespunzătoare. Prin urmare, atunci când Constanța salvează raportul ei de cheltuieli, primește un mesaj care spune că trebuie să atașeze o chitanță pentru fiecare tranzacție pe care a enumerat-o în raportul de cheltuieli. Constanța verifică că a atașat o imagine digitală a fiecărei chitanțe de tranzacție la raportul de cheltuieli și apoi își trimite raportul pentru aprobare. Apoi trimite chitanțele de hârtie către echipa de procesare back-office. Această echipă va trimite datele de recuperare a TVA furnizorului terț care depune declarații internaționale de recuperare a TVA pentru Contoso.

## <a name="make-sure-that-all-tax-information-is-complete-and-then-post-the-expense-report"></a>Asigurați-vă dacă toate informațiile fiscale sunt complete, apoi încărcați raportul de cheltuieli

Înainte ca April, coordonatorul de conturi de furnizori pentru Contoso, trebuie să introducă orice informații fiscale lipsesc dintr-un raport de cheltuieli înainte ca raportul să poată fi publicat. Ea deschide pagina **Detalii raport cheltuieli** și vede raportul de cheltuieli aprobat de Constanța. April deschide apoi raportul de cheltuieli pentru a vizualiza detaliile tranzacțiilor. Ea vede că Constanța nu a intrat într-un grup de impozite pe vânzări pentru una dintre tranzacții. Deoarece aceste informații nu sunt furnizate, April nu poate posta raportul de cheltuieli. Prin urmare, April se uită la pagina **Configurații fiscale** din Gestionarea cheltuielilor și găsește grupul adecvat de impozitare pe vânzări pentru țară/regiune și tipul tranzacției. April poate posta acum raportul de cheltuieli la registrul general.

Când April publică raportul de cheltuieli, se creează un articol de lucru recuperabil din TVA. Acest articol de lucru este atribuit unui membru al echipei de procesare back-office. April primește un mesaj care confirmă că postarea a avut succes. Acest mesaj listează, de asemenea, numărul de tranzacții cu TVA care au fost identificate pentru recuperare.

## <a name="process-expenses-that-are-eligible-for-international-vat-recovery"></a>Procesați cheltuielile care sunt eligibile pentru recuperarea internațională a TVA

Arnie, membru al echipei de procesare back-office a Contoso, este responsabil pentru confirmarea faptului că toate informațiile necesare pentru recuperarea TVA sunt incluse în rapoartele de cheltuieli. El deschide pagina **Recuperarea cheltuielilor fiscale** și selectează raportul de cheltuieli trimis de Constanța. Arnie verifică că toate chitanțele necesare sunt atașate și că au fost introduse codurile corecte ale taxei de vânzare și articolului.

Când Arnie primește chitanțele pe hârtie de la Constanța, le verifică cu chitanțele de hârtie și apoi schimbă starea raportului de cheltuieli în **Gata pentru recuperare**.

## <a name="send-vat-recovery-data-to-the-third-party-vendor-to-file-international-recovery-returns"></a>Trimiteți date de recuperare TVA furnizorului terț pentru a depune declarații internaționale de recuperare

Când Arnie este gata să trimită datele raportului de cheltuieli furnizorului terț care va depune declarațiile de recuperare a TVA, acesta deschide pagina **Recuperarea cheltuielilor fiscale**. El filtrează pagina astfel încât să afișeze numai rapoartele de cheltuieli marcate ca **Gata pentru recuperare**. Arnie selectează apoi **Fişier** &gt; **Exportați în Excel**. Informațiile TVA din rapoartele de cheltuieli sunt exportate către o foaie de lucru Microsoft Excel. Arnie trimite această foaie de lucru furnizorului terță parte și include un mesaj care spune că bonurile de hârtie au fost trimise prin curier.

## <a name="process-expenses-for-domestic-vat-recovery"></a>Cheltuieli de proces pentru recuperarea TVA internă

Arnie trebuie să verifice dacă tranzacțiile raportului de cheltuieli sunt eligibile pentru recuperarea TVA și că chitanțele digitale sunt atașate rapoartelor. Pentru a începe procesarea cheltuielilor eligibile pentru recuperarea internă, Arnie deschide pagina **Recuperarea cheltuielilor fiscale** și selectează raportul de cheltuieli care necesită verificare. El verifică dacă chitanțele sunt în numele companiei în locul angajatului. Pentru recuperarea TVA, chitanțele trebuie să fie pe numele companiei. Arnie confirmă apoi că s-au aplicat codurile corecte de impozitare pe vânzări și grupul de taxe pe vânzări.

Când Arnie primește chitanțele pe hârtie, el schimbă starea raportului de cheltuieli în **Gata pentru recuperare**. Apoi poate depune declarația la autoritatea fiscală competentă. În acest caz, autoritatea fiscală corespunzătoare din SUA este Internal Revenue Service (IRS).


[!INCLUDE[footer-include](../includes/footer-banner.md)]