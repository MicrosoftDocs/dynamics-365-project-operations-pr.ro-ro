---
title: Aplicația Cheltuieli mobile
description: Acest articol oferă informații despre spațiul de lucru mobil pentru Gestionarea cheltuielor.
author: suvaidya
ms.date: 11/15/2021
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 1ba7ccae04fbb02252e3ceb01f123ce1e85375b7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930241"
---
# <a name="mobile-expense-app"></a>Aplicația Cheltuieli mobile

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Acest articol oferă informații despre spațiul de lucru mobil pentru **Gestionarea cheltuielor**. Acest spațiu de lucru permite utilizatorilor să captureze și să încarce o chitanță, astfel încât să o poată atașa la un raport de cheltuieli ulterior. De asemenea, utilizatorii pot crea rapid o linie de cheltuieli utilizând o chitanță atașată și pot crea și gestiona rapoartele de cheltuieli. În plus, aprobatorii pot utiliza spațiul de lucru mobil **Gestionarea cheltuielilor** pentru a vizualiza rapoartele de cheltuieli care le sunt atribuite și pentru a aproba sau respinge rapoartele de cheltuieli respective.

Acest spațiu de lucru mobil este destinat să fie utilizat cu aplicația mobilă Dynamics 365 Unified Ops.

Multe organizații solicită ca o copie a chitanței să fie atașată unui raport de cheltuieli legate de călătorie sau de afaceri pe care un angajat îl trimite pentru rambursare. Spațiul de lucru mobil **Gestionarea cheltuielilor** permite utilizatorilor să creeze rapid noi linii de cheltuieli pe dispozitivul mobil la alegere, utilizând o fotografie atașată a unei chitanțe. Alternativ, utilizatorii pot captura o fotografie a unei chitanțe și apoi o pot atașa la un raport de cheltuieli ulterior. Angajații își pot crea și gestiona rapoartele de cheltuieli, apoi le pot trimite pentru aprobare și rambursare utilizând dispozitivul lor mobil.

Mai exact, spațiul de lucru mobil **Managementul cheltuielilor** permite utilizatorilor să efectueze următoarele sarcini:

- Faceți o fotografie a unei chitanțe. Încărcați fotografia chitanței și atașați-o ulterior la un raport de cheltuieli.
- Încărcați un fișier ca chitanță capturată. Apoi, puteți atașa fișierul respectiv la un raport de cheltuieli ulterior.
- Creați o nouă linie de cheltuieli utilizând o chitanță atașată. Apoi puteți adăuga elementul rând la un raport de cheltuieli ulterior și îl puteți trimite pentru aprobare și rambursare.

De asemenea, aveţi posibilitatea să utilizaţi aceste caracteristici:

- Creați un nou raport de cheltuială.
- Atașați tranzacțiile cu cardul de credit și alte cheltuieli create anterior la un raport de cheltuieli.
- Creați cheltuieli noi pentru un raport de cheltuieli.
- Atașați o chitanță la orice cheltuială pentru un raport de cheltuieli, fie făcând o fotografie a chitanței, fie încărcând un fișier ca chitanță capturată.
- În funcție de politica de cheltuieli a companiei, adăugați lista invitaților la o cheltuială.
- În funcție de politica de cheltuieli a companiei, detaliați cheltuielile.
- Trimiteți un raport de cheltuieli pentru aprobare și rambursare.
- Aprobați sau respingeți rapoartele de cheltuieli pentru care sunteți aprobator desemnat.

## <a name="prerequisites-if-you-use-dynamics-365-finance"></a>Cerințe preliminare dacă utilizați Dynamics 365 Finance

Dacă Finanța a fost implementată pentru organizația dvs., administratorul de sistem trebuie să publice fișierul spațiu de lucru mobil **Gestionarea cheltuielii**. 

## <a name="download-and-install-the-dynamics-365-unified-ops-mobile-app"></a>Descărcați și instalați aplicația mobilă Dynamics 365 Unified Ops
Descărcați și instalați aplicația mobilă Dynamics 365 Unified Ops:

- [Pentru telefoane Android](https://go.microsoft.com/fwlink/?linkid=850662)
- [Pentru telefoane iPhone](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Conectați-vă la aplicația mobilă
1. Deschideți aplicația pe dispozitivul mobil.
2. Introduceți adresa URL Dynamics 365.
4. Prima dată când vă conectați, vi se solicită numele de utilizator și parola. Introduceți acreditările.
5. După ce vă conectați, sunt afișate spațiile de lucru disponibile pentru compania dvs. Dacă administratorul de sistem publică mai târziu un spațiu de lucru nou, va trebui să reîmprospătați lista spațiilor de lucru mobile.

## <a name="capture-a-receipt-by-using-the-expense-management-mobile-workspace"></a>Capturați o chitanță utilizând spațiul de lucru mobil pentru gestionarea cheltuielilor

1. Pe dispozitivul dvs. mobil, deschideți spațiul de lucru **Gestionarea cheltuielilor**.
2. Selectați **Captură chitanță**.
3. Selectați **Faceți o fotografie** sau **Alegeți imaginea**.
4. Urmați unul dintre acești pași:

    - Dacă ați selectat **Faceți o fotografie**, urmați acești pași:

        1. Sunteți condus la camera de pe dispozitivul dvs. mobil, astfel încât să puteți face o fotografie a chitanței. 
        2. După ce ați terminat de făcut o fotografie, selectați **OK** pentru a accepta fotografia.
        3. Opțional: introduceți un nume pentru fotografie și introduceți orice notă.

    - Dacă ați selectat **Alegeți imagine**, urmați acești pași:

        1. Selectaţi o imagine din listă.
        2. Opțional: introduceți un nume pentru imagine și introduceți orice notă.

5. Selectați **Terminat**.

## <a name="quickly-enter-expenses-by-using-the-expense-management-mobile-workspace"></a>Introduceți repede cheltuieli utilizând spațiul de lucru mobil pentru gestionarea cheltuielilor

1. Pe dispozitivul dvs. mobil, deschideți spațiul de lucru **Gestionarea cheltuielilor**.
2. Selectați **Intrare rapidă a cheltuielilor**.
3. Selectați categoria de cheltuială. Vedeți o listă de categorii de cheltuieli care sunt încărcate în aplicația dvs. pentru a fi utilizate offline. În mod implicit, sunt încărcate 50 de articole, dar un dezvoltator poate schimba acest număr. Pentru informații suplimentare, dezvoltatorii ar trebui să consulte [Platforma mobilă](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Dacă categoria dvs. nu se află în listă, selectați **Căutare** pentru a face o căutare online. Căutați după categoria de cheltuială sau comutați la căutarea după tipul de cheltuială.
4. Introduceți data tranzacției pentru cheltuială.
5. Opțional: introduceți comerciantul pentru cheltuială.
6. Introduceţi valoarea monetară a cheltuielii.
7. Selectați moneda cheltuielii. Vedeți o listă de coduri de monede care sunt încărcate în aplicația dvs. pentru a fi utilizate offline. În mod implicit, sunt încărcate 400 de monede, dar un dezvoltator poate schimba acest număr. Pentru informații suplimentare, dezvoltatorii ar trebui să consulte [Platforma mobilă](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Dacă moneda dvs. nu se află în listă, selectați **Căutare** pentru a face o căutare online. Căutați după monedă sau comutați la căutare după nume.
8. Selectați **Faceți o fotografie** sau **Alegeți imaginea**.
9. Urmați unul dintre acești pași:

    - Dacă ați selectat **Faceți fotografie**, sunteți conduși la camera de pe dispozitivul mobil, astfel încât puteți face o fotografie a chitanței. După ce ați terminat de făcut o fotografie, selectați **OK** pentru a accepta fotografia.
    - Dacă ați selectat **Alegeți imaginea**, selectați o imagine din listă.

10. Selectați **Terminat**.

## <a name="approve-an-expense-report-by-using-the-expense-management-mobile-workspace"></a>Aprobați un raport de cheltuieli utilizând spațiul de lucru mobil pentru Gestionarea cheltuielilor

1. Pe dispozitivul dvs. mobil, deschideți spațiul de lucru **Gestionarea cheltuielilor**.
2. **Aprobări de cheltuieli** afișează numărul de rapoarte de cheltuieli care vi se atribuie spre aprobare. Numărul este actualizat aproximativ la fiecare 30 de minute. Selectați **Aprobări de cheltuieli**.

    Este afișată lista de rapoarte de cheltuieli care vi se atribuie spre aprobare.

3. Selectați un raport de cheltuieli pentru a vizualiza detaliile cheltuielilor pentru acesta.
4. Selectați o cheltuială pentru a vizualiza detaliile pentru acesta. Informațiile afișate pentru o cheltuială includ orice chitanță, invitat și detalii de detaliere.
5. Înapoi pe pagina **Raport de cheltuieli**, selectați pentru a aproba sau respinge raportul de cheltuieli.
6. Introduceți orice comentariu pentru acțiunea de aprobare.
7. Selectați **Terminat**.

## <a name="create-a-new-expense-report-and-submit-it-for-approval-by-using-the-expense-management-mobile-workspace"></a>Creați un nou raport de cheltuieli și trimiteți-l pentru aprobare utilizând spațiul de lucru mobil de Gestionare a cheltuielilor

1. Pe dispozitivul dvs. mobil, deschideți spațiul de lucru **Gestionarea cheltuielilor**.
2. Selectați **Introducere de cheltuieli**.
3. Selectați **Raport nou** sau selectați un raport de cheltuieli existent în listă.
4. Pentru rapoarte de cheltuieli noi, introduceți scopul și orice informații suplimentare disponibile. Aceste informații variază, în funcție de modul în care gestionarea cheltuielilor este configurată pentru compania dvs.
5. Selectați **Terminat**.
6. Pentru a adăuga cheltuielile existente, cum ar fi tranzacțiile cu cardul de credit, la raportul de cheltuieli, selectați **Atașați**.
7. Selectați una sau mai multe cheltuieli în listă.
8. Selectați **Terminat**.
9. Pentru a adăuga o nouă cheltuială la raportul de cheltuieli, selectați **Cheltuială nouă**.
10. Selectați categoria pentru cheltuială. Vedeți o listă de categorii de cheltuieli care sunt încărcate în aplicația dvs. pentru a fi utilizate offline. În mod implicit, sunt încărcate 50 de articole, dar un dezvoltator poate schimba acest număr. Pentru informații suplimentare, dezvoltatorii ar trebui să consulte [Platforma mobilă](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Dacă categoria dvs. nu se află în listă, selectați **Căutare** pentru a face o căutare online. Căutați după categoria de cheltuială sau comutați la căutarea după tipul de cheltuială.
11. Opțional: introduceți comerciantul pentru cheltuială.
12. Introduceți data tranzacției pentru cheltuială.
13. Introduceţi valoarea monetară a cheltuielii.
14. Selectați moneda cheltuielii. Vedeți o listă de coduri de monede care sunt încărcate în aplicația dvs. pentru a fi utilizate offline. În mod implicit, sunt încărcate 400 de monede, dar un dezvoltator poate schimba acest număr. Pentru informații suplimentare, dezvoltatorii ar trebui să consulte [Platforma mobilă](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Dacă moneda dvs. nu se află în listă, selectați **Căutare** pentru a face o căutare online. Căutați după monedă sau comutați la căutare după nume.
15. Selectați **Terminat**.
16. Pentru a adăuga mai multe detalii la cheltuială, selectați **Adăugați mai multe detalii**. Câmpurile disponibile depind de configurația gestionării cheltuielilor pentru compania dvs.
17. Dacă politica companiei necesită o chitanță pentru cheltuială, selectați **Chitanțe**, apoi urmați acești pași:

    1. Selectați **Captură chitanță** sau **Atașați chitanța**.
    2. Urmați unul dintre acești pași:

        - Dacă ați selectat **Capturați chitanță**, urmați acești pași:

            1. Selectați **Faceți o fotografie** sau **Alegeți imaginea**.
            2. Urmați unul dintre acești pași:

                - Dacă ați selectat **Faceți o fotografie**, urmați acești pași:

                    1. Sunteți condus la camera de pe dispozitivul dvs. mobil, astfel încât să puteți face o fotografie a chitanței. După ce ați terminat de făcut o fotografie, selectați **OK** pentru a accepta fotografia.
                    2. Opțional: introduceți un nume pentru fotografie și introduceți orice notă.

                - Dacă ați selectat **Alegeți imagine**, urmați acești pași:

                    1. Selectaţi o imagine din listă.
                    2. Opțional: introduceți un nume pentru imagine și introduceți orice notă.

            3. Selectați **Terminat**.

        - Dacă ați selectat **Atașați chitanța**, urmați acești pași:

            1. Selectați una sau mai multe imagini în listă.
            2. Selectați **Terminat**.

    3. Selectați butonul **Înapoi** pentru a reveni la detaliile cheltuielilor.

18. Dacă politica companiei cere invitaților cheltuiala, selectați **Invitați**, apoi urmați acești pași:

    1. Selectați **Invitat**, **Invitați anteriori**, sau **Colegi de muncă**.
    2. Urmați unul dintre acești pași:

        - Dacă ați selectat **Invitat**, urmați acești pași:

            1. Introduceţi numele invitatului.
            2. Opțional: introduceți organizația și/sau țara oaspetelui.
            3. Opțional: introduceți titlul invitatului.
            4. Selectați **Terminat**.

        - Dacă ați selectat **Oaspeți anteriori**, urmați acești pași:

            1. Selectați unul sau mai mulți oaspeți anteriori din listă. Vedeți o listă de invitați anteriori pe care i-ați adăugat la rapoartele de cheltuieli anterioare care sunt încărcate în aplicația dvs. pentru utilizare offline. În mod implicit, sunt încărcate 50 de articole, dar un dezvoltator poate schimba acest număr. Pentru informații suplimentare, dezvoltatorii ar trebui să consulte [Platforma mobilă](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Dacă invitatul dvs. anterior nu se află în listă, selectați **Căutare** pentru a face o căutare online. Căutați după nume sau comutați la căutare după organizație, țară sau titlu.
            2. Selectați **Terminat**.

        - Dacă ați selectat **Colegi**, urmați acești pași:

            1. Selectați unul sau mai mulți colegi din listă. Vedeți o listă de colegi care sunt încărcați în aplicația dvs. pentru a fi utilizați offline. În mod implicit, sunt încărcate 50 de articole, dar un dezvoltator poate schimba acest număr. Pentru informații suplimentare, dezvoltatorii ar trebui să consulte [Platforma mobilă](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Dacă colegul dvs. nu se află în listă, selectați **Căutare** pentru a face o căutare online. Căutați după nume sau comutați la căutare după companie sau titlu.
            2. Selectați **Terminat**.

    3. Selectați butonul **Înapoi** pentru a reveni la detaliile cheltuielilor.

19. Dacă politica companiei cere detalierea cheltuielii, selectați **Detaliere** și apoi urmați acești pași:

    1. Selectați prima dată pe care doriți să o detaliați.
    2. Selectați **Adăugați detalii**.
    3. Selectați subcategoria pentru detalierea cheltuielii. Vedeți o listă de subcategorii de cheltuieli care sunt încărcate în aplicația dvs. pentru a fi utilizate offline. În mod implicit, sunt încărcate 50 de articole, dar un dezvoltator poate schimba acest număr. Pentru informații suplimentare, dezvoltatorii ar trebui să consulte [Platforma mobilă](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Dacă subcategoria dvs. nu se află în listă, selectați **Căutare** pentru a face o căutare online. Căutare după numele subcategorii cheltuieli.
    4. Introduceți suma tranzacției pentru detaliere.
    5. Modificați data tranzacției dacă este necesară.
    6. Selectați **Terminat**.
    7. Repetați pașii anteriori până când ați terminat de adăugat toate elementele pentru data selectată.
    8. Pentru zile suplimentare, puteți selecta **Copiază în ziua următoare** pentru a copia detaliile în ziua următoare. Alternativ, puteți selecta data de detaliere și apoi adăugați detaliere așa cum ați făcut pentru prima dată.
    9. După ce ați terminat de specificat cheltuielile, selectați butonul **Înapoi** pentru a reveni la detaliile cheltuielilor.

20. Selectați butonul **Înapoi** pentru a reveni la pagina **Raport de cheltuială**.
21. Repetați pașii anteriori până când ați terminat de adăugat toate cheltuielile.
22. Selectați **Remitere**.
23. Introduceți orice comentariu pentru aprobator.
24. Selectați **Terminat**.

## <a name="frequently-asked-questions"></a>Întrebări frecvente

### <a name="why-doesnt-the-expense-mobile-app-enter-the-payment-method-by-default"></a>De ce aplicația mobilă Expense nu introduce implicit metoda de plată?

Organizațiile pot personaliza setarea **Metodă de plată implicită** pentru fiecare categorie de cheltuieli așa cum este creată. În plus, atunci când configurați metode de plată, puteți seta câmpul **Metodă de plată implicită** la **Numai import**.

Când setarea **Numai import** este activată pentru o metodă de plată, metoda de plată nu este introdusă în mod implicit. Va fi necompletat în categoriile de cheltuieli în care este configurată această metodă de plată. Acest comportament este consecvent, atât în experiența web, cât și în cea mobilă.
    
Când setarea **Numai import** nu este activată pentru o metodă de plată, valoarea setată este introdusă implicit pentru categoriile de cheltuieli în care este configurată această metodă de plată. Cu toate acestea, există o problemă cunoscută în care valoarea implicită nu este introdusă în aplicația mobilă Expense. Pentru a rezolva această problemă, selectați manual o metodă de plată înainte de a salva raportul de cheltuieli. 

### <a name="why-cant-i-add-or-edit-financial-dimensions-in-the-expense-mobile-app"></a>De ce nu pot adăuga sau edita dimensiuni financiare în aplicația mobilă Expense?

Introducerea dimensiunilor și a distribuirilor nu este acceptată. Pentru a evita această limitare, puteți avea aceste câmpuri setate în mod implicit în aplicația mobilă, setând dimensiunile financiare implicite pentru fiecare proiect sau angajat.

### <a name="why-do-i-sometimes-see-a-synchronization-error-in-the-expense-mobile-app"></a>De ce văd uneori o eroare de sincronizare în aplicația mobilă Expense?

Dacă liniile de cheltuieli nu îndeplinesc cerințele politicii și utilizatorul trimite raportul de cheltuieli fără a lua în considerare avertismentul de politică, datele mobile nu sunt sincronizate cu serverul și are loc o eroare de sincronizare. Toate rapoartele de cheltuieli care sunt trimise după producerea unei erori de sincronizare vor rămâne într-o stare eșuată și vor cauza mai multe erori de sincronizare. Singura modalitate de a remedia această situație este să ștergeți manual notificările de sincronizare. Această problemă a fost rezolvată prin oprirea trimiterii rapoartelor de cheltuieli atunci când avertismentele de politică nu au fost abordate, astfel încât erorile de sincronizare să fie evitate.

### <a name="why-isnt-project-and-category-validation-correctly-reflected-in-the-expense-mobile-app"></a>De ce validarea proiectelor și a categoriilor nu este reflectată corect în aplicația mobilă Expense?

Această validare nu este acceptată în prezent. Cu toate acestea, este posibil să se adauge asistență în viitor. 

### <a name="what-document-types-are-supported-in-the-expense-mobile-app"></a>Ce tipuri de documente sunt acceptate în aplicația mobilă Expense?

Aplicația mobilă Expense acceptă numai imagini. În prezent, nu acceptă PDF-uri sau alte documente.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
