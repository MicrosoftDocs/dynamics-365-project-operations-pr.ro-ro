---
title: Spațiu de lucru mobil pentru gestionarea cheltuielilor
description: Acest subiect oferă informații despre spațiul de lucru mobil pentru gestionarea cheltuielii. Acest spațiu de lucru permite utilizatorilor să captureze și să încarce o chitanță, astfel încât să o poată atașa la un raport de cheltuieli ulterior. De asemenea, utilizatorii pot crea rapid o linie de cheltuieli utilizând o chitanță atașată și pot crea și gestiona rapoartele de cheltuieli.
author: suvaidya
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: suvaidya
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 2d257ced3dadb320c501bfd5f64dcd8f21c1a4d3
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272043"
---
# <a name="expense-management-mobile-workspace"></a>Spațiu de lucru mobil pentru gestionarea cheltuielilor

Acest subiect oferă informații despre spațiul de lucru mobil pentru **Gestionarea cheltuielii**. Acest spațiu de lucru permite utilizatorilor să captureze și să încarce o chitanță, astfel încât să o poată atașa la un raport de cheltuieli ulterior. De asemenea, utilizatorii pot crea rapid o linie de cheltuieli utilizând o chitanță atașată și pot crea și gestiona rapoartele de cheltuieli. În plus, aprobatorii pot utiliza spațiul de lucru mobil **Gestionarea cheltuielilor** pentru a vizualiza rapoartele de cheltuieli care le sunt atribuite și pentru a aproba sau respinge rapoartele de cheltuieli respective.


Acest spațiu de lucru mobil este destinat să fie utilizat cu aplicația mobilă Dynamics 365 Unified Ops.


## <a name="overview"></a>Prezentare generală

Multe organizații solicită ca o copie a chitanței să fie atașată unui raport de cheltuieli legate de călătorie sau de afaceri pe care un angajat îl trimite pentru rambursare. Spațiul de lucru mobil **Gestionarea cheltuielilor** permite utilizatorilor să creeze rapid noi linii de cheltuieli pe dispozitivul mobil la alegere, utilizând o fotografie atașată a unei chitanțe. Alternativ, utilizatorii pot captura o fotografie a unei chitanțe și apoi o pot atașa la un raport de cheltuieli ulterior. Angajații își pot crea și gestiona rapoartele de cheltuieli, apoi le pot trimite pentru aprobare și rambursare utilizând dispozitivul lor mobil.


Mai exact, spațiul de lucru mobil **Managementul cheltuielilor** permite utilizatorilor să efectueze următoarele sarcini:

- Faceți o fotografie a unei chitanțe și încărcați-o în Dynamics 365 Finance. Apoi, puteți atașa imaginea respectivă la un raport de cheltuieli ulterior.
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

## <a name="prerequisites"></a>Cerințe preliminare
Cerințele preliminare variază, în funcție de versiunea care a fost implementată pentru organizația dvs.

### <a name="prerequisites-if-you-use-dynamics-365-finance"></a>Condiții preliminare dacă utilizați Dynamics 365 Finance 
Dacă Finanța a fost implementată pentru organizația dvs., administratorul de sistem trebuie să publice fișierul spațiu de lucru mobil **Gestionarea cheltuielii**. Pentru instrucțiuni, consultați [Publicați spații de lucru mobile](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace).

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a>Condiții preliminare dacă utilizați versiunea 1611 cu platforma de 3 actualizare sau o versiune ulterioară
Dacă versiunea 1611 cu actualizarea platformei 3 sau o versiune ulterioară a fost implementată pentru organizația dvs., administratorul de sistem trebuie să îndeplinească următoarele condiții prealabile. 

<table>
<thead>
<tr class="header">
<th>Cerințe preliminare</th>
<th>Rol</th>
<th>Descriere</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Implementați KB 4019015.</td>
<td>Administrator de sistem</td>
<td>KB 4019015 este o actualizare X++ sau metadate remediere rapidă care conține spațiu de lucru mobil <strong>Gestionarea cheltuielii</strong>. Pentru a implementa KB 4019015, administratorul de sistem trebuie să urmeze acești pași.
<ol>
<li><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package#download-the-hotfix-from-lcs">Descărcați remedierea rapidă a metadatelor de la Microsoft Dynamics Lifecycle Services (LCS)</a>.</li>
<li><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package#install-the-metadata-hotfix-package">Instalați remedierea rapidă a metadatelor</a>.</li>
<li><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Creați un pachet implementabil</a> care conține modele <strong>ApplicationSuite</strong> și <strong>ExpenseMobile</strong> și apoi încărcați pachetul implementabil la LCS.</li>
<li><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Aplicați pachetul implementabil</a>.</li>
</ol></td>
</tr>
<tr class="even">
<td>Publicați fișierul spațiu de lucru mobil <strong>Gestionarea cheltuielilor</strong>.</td>
<td>Administrator de sistem</td>
<td>Consultați <a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Publicați un spațiu de lucru mobil</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-dynamics-365-for-operations-mobile-app"></a>Descărcați și instalați aplicația mobilă Dynamics 365 for Operations
Descărcați și instalați aplicația mobilă Dynamics 365 Unified Ops:

- [Pentru telefoane Android](https://go.microsoft.com/fwlink/?linkid=850662)
- [Pentru telefoane iPhone](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Conectați-vă la aplicația mobilă
1. Deschideți aplicația pe dispozitivul mobil.
2. Introduceți adresa URL Dynamics 365.
4. Prima dată când vă conectați, vi se solicită numele de utilizator și parola. Introduceți acreditările.
5. După ce vă conectați, sunt afișate spațiile de lucru disponibile pentru compania dvs. Rețineți că, dacă administratorul de sistem publică mai târziu un spațiu de lucru nou, va trebui să reîmprospătați lista spațiilor de lucru mobile.


[![Trageți pentru a reîmprospăta](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="capture-a-receipt-by-using-the-expense-management-mobile-workspace"></a>Capturați o chitanță utilizând spațiul de lucru mobil pentru gestionarea cheltuielilor

1. Pe dispozitivul dvs. mobil, deschideți spațiul de lucru **Gestionarea cheltuielilor**.
2. Selectați **Captură chitanță**.
3. Selectați **Faceți o fotografie** sau **Alegeți imaginea**.
4. Urmați unul dintre acești pași:

    - Dacă ați selectat **Faceți o fotografie**, urmați acești pași:

        1. Sunteți condus la camera de pe dispozitivul dvs. mobil, astfel încât să puteți face o fotografie a chitanței. După ce ați terminat de făcut o fotografie, selectați **OK** pentru a accepta fotografia.
        2. Opțional: introduceți un nume pentru fotografie și introduceți orice notă.

    - Dacă ați selectat **Alegeți imagine**, urmați acești pași:

        1. Selectaţi o imagine din listă.
        2. Opțional: introduceți un nume pentru imagine și introduceți orice notă.

5. Selectați **Terminat**.

## <a name="quickly-enter-expenses-by-using-the-expense-management-mobile-workspace"></a>Introduceți repede cheltuieli utilizând spațiul de lucru mobil pentru gestionarea cheltuielilor
1. Pe dispozitivul dvs. mobil, deschideți spațiul de lucru **Gestionarea cheltuielilor**.
2. Selectați **Intrare rapidă a cheltuielilor**.
3. Selectați categoria pentru cheltuială. Vedeți o listă de categorii de cheltuieli care sunt încărcate în aplicația dvs. pentru a fi utilizate offline. În mod implicit, sunt încărcate 50 de articole, dar un dezvoltator poate schimba acest număr. Pentru informații suplimentare, dezvoltatorii ar trebui să consulte [Platforma mobilă](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Dacă categoria dvs. nu se află în listă, selectați **Căutare** pentru a face o căutare online. Căutați după categoria de cheltuială sau comutați la căutarea după tipul de cheltuială.
4. Introduceți data tranzacției pentru cheltuială.
5. Opțional: introduceți comerciantul pentru cheltuială.
6. Introduceţi valoarea monetară a cheltuielii.
7. Selectați moneda cheltuielii. Vedeți o listă de coduri de monede care sunt încărcate în aplicația dvs. pentru a fi utilizate offline. În mod implicit, sunt încărcate 400 de monede, dar un dezvoltator poate schimba acest număr. Pentru informații suplimentare, dezvoltatorii ar trebui să consulte [Platforma mobilă](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Dacă moneda dvs. nu se află în listă, selectați **Căutare** pentru a face o căutare online. Căutați după monedă sau comutați la căutare după nume.
8. Selectați **Faceți o fotografie** sau **Alegeți imaginea**.
9. Urmați unul dintre acești pași:

    - Dacă ați selectat **Faceți fotografie**, sunteți conduși la camera de pe dispozitivul mobil, astfel încât puteți face o fotografie a chitanței. După ce ați terminat de făcut o fotografie, selectați **OK** pentru a accepta fotografia.
    - Dacă ați selectat **Alegeți imaginea**, selectați o imagine din listă.

10. Selectați **Terminat**.

## <a name="approve-an-expense-report-by-using-the-expense-management-mobile-workspace-if-you-use-the-july-2017-update"></a>Aprobați un raport de cheltuieli utilizând spațiul de lucru mobil pentru gestionarea cheltuielilor (dacă utilizați actualizarea din iulie 2017)
1. Pe dispozitivul dvs. mobil, deschideți spațiul de lucru **Gestionarea cheltuielilor**.
2. **Aprobări de cheltuieli** afișează numărul de rapoarte de cheltuieli care vi se atribuie spre aprobare. Numărul este actualizat aproximativ la fiecare 30 de minute. Selectați **Aprobări de cheltuieli**.

    Este afișată lista de rapoarte de cheltuieli care vi se atribuie spre aprobare.
    
3. Selectați un raport de cheltuieli pentru a vizualiza detaliile cheltuielilor pentru acesta.
4. Selectați o cheltuială pentru a vizualiza detaliile pentru acesta. Informațiile afișate pentru o cheltuială includ orice chitanță, invitat și detalii de detaliere.
5. Înapoi pe pagina **Raport de cheltuieli**, selectați pentru a aproba sau respinge raportul de cheltuieli.
6. Introduceți orice comentariu pentru acțiunea de aprobare.
7. Selectați **Terminat**.

## <a name="create-a-new-expense-report-and-submit-it-for-approval-by-using-the-expense-management-mobile-workspace-if-you-use-the-july-2017-update"></a>Creați un nou raport de cheltuieli și trimiteți-l pentru aprobare utilizând spațiul de lucru mobil de gestionare a cheltuielilor (dacă utilizați actualizarea din 2017)
1. Pe dispozitivul dvs. mobil, deschideți spațiul de lucru **Gestionarea cheltuielilor**.
2. Selectați **Introducere de cheltuieli**.
3. Selectați **Raport nou** sau selectați un raport de cheltuieli existent în listă.
4. Pentru rapoarte de cheltuieli noi, introduceți scopul și orice informații suplimentare disponibile. Aceste informații variază, în funcție de modul în care gestionarea cheltuielilor este configurată pentru compania dvs.
5. Selectați **Terminat**.
6. Pentru a adăuga cheltuielile existente, cum ar fi tranzacțiile cu cardul de credit, la raportul de cheltuieli, selectați **Atașați**.
7. Selectați una sau mai multe cheltuieli în listă.
8. Selectați **Terminat**.
9. Pentru a adăuga o nouă cheltuială la raportul de cheltuieli, selectați **Cheltuială nouă**.
10. Selectați categoria pentru cheltuială. Vedeți o listă de categorii de cheltuieli care sunt încărcate în aplicația dvs. pentru a fi utilizate offline. În mod implicit, sunt încărcate 50 de articole, dar un dezvoltator poate schimba acest număr. Pentru informații suplimentare, dezvoltatorii ar trebui să consulte [Platforma mobilă](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Dacă categoria dvs. nu se află în listă, selectați **Căutare** pentru a face o căutare online. Căutați după categoria de cheltuială sau comutați la căutarea după tipul de cheltuială.
11. Opțional: introduceți comerciantul pentru cheltuială.
12. Introduceți data tranzacției pentru cheltuială.
13. Introduceţi valoarea monetară a cheltuielii.
14. Selectați moneda cheltuielii. Vedeți o listă de coduri de monede care sunt încărcate în aplicația dvs. pentru a fi utilizate offline. În mod implicit, sunt încărcate 400 de monede, dar un dezvoltator poate schimba acest număr. Pentru informații suplimentare, dezvoltatorii ar trebui să consulte [Platforma mobilă](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Dacă moneda dvs. nu se află în listă, selectați **Căutare** pentru a face o căutare online. Căutați după monedă sau comutați la căutare după nume.
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

            3.  Selectați **Terminat**.

        - Dacă ați selectat **Atașați chitanța**, urmați acești pași:

            1.  Selectați una sau mai multe imagini în listă.
            2.  Selectați **Terminat**.

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

            1. Selectați unul sau mai mulți oaspeți anteriori din listă. Vedeți o listă de invitați anteriori pe care i-ați adăugat la rapoartele de cheltuieli anterioare care sunt încărcate în aplicația dvs. pentru utilizare offline. În mod implicit, sunt încărcate 50 de articole, dar un dezvoltator poate schimba acest număr. Pentru informații suplimentare, dezvoltatorii ar trebui să consulte [Platforma mobilă](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Dacă invitatul dvs. anterior nu se află în listă, selectați **Căutare** pentru a face o căutare online. Căutați după nume sau comutați la căutare după organizație, țară sau titlu.
            2. Selectați **Terminat**.

        - Dacă ați selectat **Colegi**, urmați acești pași:

            1. Selectați unul sau mai mulți colegi din listă. Vedeți o listă de colegi care sunt încărcați în aplicația dvs. pentru a fi utilizați offline. În mod implicit, sunt încărcate 50 de articole, dar un dezvoltator poate schimba acest număr. Pentru informații suplimentare, dezvoltatorii ar trebui să consulte [Platforma mobilă](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Dacă colegul dvs. nu se află în listă, selectați **Căutare** pentru a face o căutare online. Căutați după nume sau comutați la căutare după companie sau titlu.
            2. Selectați **Terminat**.

    3. Selectați butonul **Înapoi** pentru a reveni la detaliile cheltuielilor.

19. Dacă politica companiei cere detalierea cheltuielii, selectați **Detaliere** și apoi urmați acești pași:

    1. Selectați prima dată pe care doriți să o detaliați.
    2. Selectați **Adăugați detalii**.
    3. Selectați subcategoria pentru detalierea cheltuielii. Vedeți o listă de subcategorii de cheltuieli care sunt încărcate în aplicația dvs. pentru a fi utilizate offline. În mod implicit, sunt încărcate 50 de articole, dar un dezvoltator poate schimba acest număr. Pentru informații suplimentare, dezvoltatorii ar trebui să consulte [Platforma mobilă](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Dacă subcategoria dvs. nu se află în listă, selectați **Căutare** pentru a face o căutare online. Căutare după numele subcategorii cheltuieli.
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


[!INCLUDE[footer-include](../includes/footer-banner.md)]