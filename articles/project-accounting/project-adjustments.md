---
title: Ajustări ale proiectelor
description: Acest articol oferă informații despre ajustările proiectului.
author: ryansandness
ms.date: 11/09/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ryansandness
ms.openlocfilehash: 52a262adce2bb624bc088e50858e25824f845e5c
ms.sourcegitcommit: bb03ac64e01112c93bb24035a51653a0a88cd5fc
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 11/18/2022
ms.locfileid: "9788372"
---
# <a name="project-adjustments"></a>Ajustări ale proiectelor

_**Se aplică la:** Project Operations pentru scenariile bazate pe stocuri/producție_

## <a name="adjustments-overview"></a>Prezentare generală a ajustărilor

Puteți configura Microsoft Dynamics 365 Project Operations astfel încât utilizatorii să poată face modificări tranzacțiilor publicate. Puteți ajusta tranzacțiile de proiect individual sau puteți selecta mai multe tranzacții simultan într-o listă cu toate tranzacțiile de proiect. Ajustările proiectului sunt utilizate, de exemplu, pentru a actualiza în masă starea facturabilă, a recalcula costul după o modificare a configurației sau pentru a actualiza sursele de finanțare.

Utilizatorii pot accesa funcționalitatea de ajustare a proiectului în mai multe moduri:

- Folosind pagina **Ajustați tranzacțiile** care poate fi accesată din **Gestionarea proiectelor și contabilitate** \> **Configurare**.
- Folosind butonul **Ajustare** de pe pagina **Tranzacții de proiect publicate** care poate fi accesată de pe **Management de proiect și contabilitate** \> **Tranzacții**.
- Folosind butonul **Ajustare** de pe pagina **Tranzacții de proiect publicate** în contextul unui proiect. Această pagină poate fi accesată din **Gestionarea proiectelor și contabilitate** \> **Toate proiectele**.

To allow for adjustments you must enable one or more transaction statuses from **Project Management and accounting** \> **Project Management and accounting paramaters** on the **General** tab under the section **Allow adjustment of transaction status**. Exemplele de stări ale tranzacțiilor includ tranzacții înregistrate, tranzacții facturate sau tranzacții eliminate. Orice stare a tranzacției care este setată la **Nu** va avea tranzacții în acea stare care nu vor apărea în procesul de ajustare ca fiind selectabile pentru ajustare.

O opțiune de configurare numită **Creați întotdeauna tranzacția de ajustare** este disponibilă în prezent în Managementul proiectelor și parametrii contabili. Puteți dezactiva această opțiune pentru a actualiza tranzacția inițială în loc să creați tranzacții noi în timpul ajustării într-un subset de scenarii. S-a anunțat că acest parametru va fi retras până la 1 martie 2023. După 1 martie 2023, sistemul se va comporta întotdeauna ca și cum opțiunea ar fi activată.

## <a name="adjustments-process-flow"></a>Fluxul procesului de ajustări

Următorii pași arată fluxul tipic pentru procesarea ajustărilor.

1. Deschideți pagina **Ajustări ale proiectului** .
2. Selectați **Selectați** pentru a căuta tranzacții care îndeplinesc criteriile așteptate pentru ajustare.
3. În lista de tranzacții, selectați toate tranzacțiile sau un subset de tranzacții pentru ajustare.
4. Selectați **Ajustați** și modificați atributele de pe linie. Alternativ, dacă valorile au fost specificate manual în timpul introducerii tranzacției, puteți selecta să introduceți valorile implicite de sistem.
5. Se returnează lista de tranzacții, iar o bifă apare în coloana **Ajustare în așteptare** pentru a indica locul în care s-au făcut modificări. Orice ajustări care au modificări în așteptare sunt afișate în jumătatea inferioară a paginii. Acolo, puteți face modificări suplimentare detaliate în afara celor afișate pe pagina anterioară.
6. Selectați **Încărcați** pentru a încărca tranzacțiile de ajustare.

În funcție de configurație, tranzacțiile noi sunt create de obicei pentru ajustare.

- Câmpul **Starea facturii** al tranzacției inițiale este setat la **Ajustat**.
- O tranzacție de anulare este creată pentru a inversa tranzacția inițială, iar câmpul **Stare** este setat la **Ajustat**.
- Este creată o nouă tranzacție care are modificările care au fost făcute în timpul procesului de ajustare.

### <a name="selecting-multiple-posted-project-transactions-at-a-time-for-adjustments-and-credit-notes"></a>Selectarea mai multor tranzacții de proiect înregistrate simultan pentru ajustări și note de credit

O nouă caracteristică care a fost introdusă în versiunea 10.0.30 permite selectarea mai multor tranzacții pentru ajustare simultan din pagina **Tranzacții de proiect publicate** .

Înainte de a putea utiliza această caracteristică, trebuie să fie activată în sistemul dumneavoastră. Administratorii pot folosi spațiul de lucru **Gestionarea funcțiilor** pentru a verifica starea funcției și a o activa dacă este necesar. În spațiul de lucru **Gestionarea funcțiilor**, căutați și selectați **Tranzacții de proiect publicate cu selecție multiplă pentru ajustări și note de credit**, apoi selectați **Activați acum**.

Această caracteristică permite următoarea funcționalitate cheie:

- Acesta poate fi accesat din pagina de tranzacție publicată în cadrul unui proiect utilizând butonul **Ajustare** existent.
- Activează un control de selectare pe mai multe rânduri pe pagina **Tranzacții de proiect publicate** . Puteți aplica filtre pe pagina cu listă și puteți selecta înregistrările înainte de a începe ajustările.
- Dezactivează butonul **Ajustare** dacă orice tranzacție nu poate fi ajustată sau dacă selectați o combinație de note de credit și jurnale împreună în loc de individual.
- Din cauza adăugării controlului de selectare pe mai multe rânduri, linkul **Cost angajat** din panglică nu mai este dezactivat dacă sunt selectate mai multe rânduri.
- Se adaugă următorul mesaj de avertizare: „Ați selectat mai mult de (număr selectat) înregistrări pentru ajustare. Continuarea acestei acțiuni poate dura ceva timp. Sunteți sigur că doriți să continuați cu această acțiune?"

Această caracteristică elimină, de asemenea, pasul 2 din fluxul de proces care a fost descris mai devreme în acest articol. Prin urmare, toate tranzacțiile care au fost selectate înainte ca pagina **Ajustare tranzacții** să fie deschisă vor fi incluse în lista de tranzacții pentru ajustare. Nu trebuie să utilizați butonul **Selectați** pentru a le căuta.

> [!NOTE] 
> Chiar dacă această caracteristică este dezactivată, puteți selecta în continuare mai multe înregistrări pentru ajustare. Cu toate acestea, o singură înregistrare va rămâne  *selectată*, iar caseta de dialog **Selectați tranzacții** va apărea imediat după ce selectați să ajustări deschise.

## <a name="adjustment-transaction-statuses-that-can-be-enabled-or-disabled-for-adjustments"></a>Stări ale tranzacțiilor de ajustare care pot fi activate sau dezactivate pentru ajustări

Următoarele stări pot fi activate sau dezactivate în fila **General** a paginii **Parametri de gestiune a proiectelor și contabilitate** :

- Publicată
- Propunere de factură
- Facturată
- Estimat
- Eliminat
- Sold de început (oră)

## <a name="adjustment-parameters"></a>Parametrii de ajustare

Acești parametri sunt listați în pagina **Parametrii de gestiune a proiectelor și contabilitate** din fila **General** sub fila **Ajustare** grup și va modifica comportamentul pentru modul în care sunt procesate ajustările. 

| Nume parametru | Descriere |
|----------------|-------------
| Creați întotdeauna tranzacția de ajustare | Dacă acest parametru este activat, procesul de ajustare va crea întotdeauna o nouă tranzacție de inversare și o nouă tranzacție ajustată atunci când există un impact financiar sau de raportare. Dacă parametrul este dezactivat, procesul de ajustare va actualiza tranzacția inițială în loc să creeze o inversare și o nouă tranzacție pentru un scenariu cum ar fi o actualizare a textului tranzacției. |
| Câmp de actualizare automată | Dacă acest parametru este activat, sistemul va recalcula prețul de cost și prețul de vânzare. |
| Utilizați data ajustării ca proiect nou | Acest parametru este utilizat pentru a muta tranzacțiile într-un viitor perioadă fiscală înainte ca sistemul să accepte această funcție. Nu vă recomandăm să îl utilizați, deoarece modifică data tranzacției și va fi depreciat într-o versiune viitoare. |
| Permite activități închise | De obicei, tranzacțiile nu pot fi create pentru activități închise. Dacă acest parametru este activat, comportamentul respectiv este suprascris. Prin urmare, pot fi create ajustări pentru activitățile închise. |
