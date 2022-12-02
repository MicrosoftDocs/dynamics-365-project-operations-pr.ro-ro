---
title: Sincronizarea stării proiectelor pentru a preveni introducerea de date în proiectele închise
description: Acest articol explică cum să sincronizați starea proiectului pentru a preveni intrarea împotriva proiectelor inactive sau închise.
author: ryansandnessMSFT
ms.date: 08/09/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ryansandnessMSFT
ms.openlocfilehash: 7a306da164235f36d9ed5e69196508dce6d257de
ms.sourcegitcommit: 6b6c2bfd04e3e613ed1f38355c7cd47c3a56748d
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/24/2022
ms.locfileid: "9348109"
---
# <a name="sync-project-status-to-prevent-entry-against-closed-projects"></a>Sincronizarea stării proiectelor pentru a preveni introducerea de date în proiectele închise

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

## <a name="scenario"></a>Scenariu

Contoso este disponibil cu Microsoft Dynamics 365 Project Operations pentru scenarii de resurse/neaprovizionate. Ca parte a activităților normale de afaceri, proiectele pot fi finalizate sau suspendate. Puteți dezactiva proiectul pentru a vă asigura că nu sunt generate cheltuieli sau facturi.

## <a name="solution"></a>Soluție

### <a name="prerequisites"></a>Cerințe preliminare

-   Trebuie instalat Microsoft Dynamics 365 Finance 10.0.29 sau o versiune ulterioară.
-   Trebuie instalat sau configurat manual Dual Write map 1.0.0.3 pentru Proiecte V2 (msdyn\_proiecte) după cum este descris mai jos.

### <a name="create-an-updated-version-of-the-project-operations-integration-projects-v2-dual-write-map"></a>Creați o versiune actualizată a hărții de scriere duală Proiecte V2 de integrare a Project Operations

Pentru a actualiza harta cu scriere duală Proiecte V2 a Project Operations:

1. Accesați spațiul de lucru **Management de date** și selectați **Scriere duală**.
2. Selectați dala **Scriere duală**.
3. Din coloana T **Harta tabelului**, localizați și selectați **Proiecte V2 (msdyn\_proiecte)**, apoi selectați Oprire.
4. Selectați numele hărții pentru a deschide harta și apoi selectați **[Niciuna]**.
5. Din caseta de dialog Selectare coloană, selectați **cod de stat \[Starea proiectului\]** și apoi selectați OK. Puteți tasta **stat** în valoarea filtrului pentru a restrânge lista.
6.  Selectați **Adăugați sau editați transformarea** în coloana **tip de hartă** pentru a edita transformarea.
7.  Din **Tip de transformare**, selectați **ValueMap**.
8.  Selectați **Adăugare mapare valoare** și apoi adăugați următoarele **Chei** și **Valori**:

   Tastă       | Valoare 
   ----------|-------
   InProcess | 0     
   finalizată | 1     

![Captură de ecran afișând maparea cu scriere duală](media/projectstage-dw-mapping.png)

9. Selectați **Salvare**.
10. Din partea de sus a paginii **Scriere duală > Protecte V2 (msdyn_projects)**, selectați **Salvare ca**.
11. Din **Adăugare tabel** în câmpul **Editor**, selectați **Editor CDS implicit**.
12. Setați câmpul **Versiune** la 1.0.0.3.
13. Tastați o **Descriere** și apoi selectați **Salvare**.
14. Din partea de sus a paginii **Scriere duală > Proiecte V2 (msdyn_projects)**, selectați **Executare** pentru a porni harta și apoi selectați **Da** dacă vi se cere să confirmați înainte de executare. 

### <a name="close-a-newly-completed-project"></a>Închideți un proiect nou finalizat

Dynamics 365 Finance utilizează câmpul **etapă de proiect** pentru a face diferența între proiectele **în curs** sau **finalizate**. Proiectele **Finalizate** nu pot implica cheltuieli sau să fie facturate clienților.

1. Deschideți un proiect pentru dezactivare.
2. Pe panglică, selectați **Dezactivare**.

> [!NOTE]
> Puteți fie să dezactivați, fie să închideți un proiect, deoarece ambele se vor comporta la fel în contextul Finanțelor.

3. În Finanțe, deschideți pagina **Lista tuturor proiectelor**.
4. Confirmați că proiectul dezactivat nu apare în listă.
5. În filtrul **afișare proiecte** aflat deasupra listei, modificați valoarea de la **Active** la **Toate**.
6. Veți vedea acum proiectul dezactivat.

Dacă încercați să înregistrați timp sau cheltuieli pentru acest proiect în Finanțe, nu ar trebui să vedeți proiectul pentru selecție. Dacă introduceți manual numărul proiectului pentru o cheltuială, veți vedea un mesaj precum „Etapa de proiect finalizată nu permite înregistrarea în proiect”. Facturarea și alte funcții de facturare trebuie dezactivate, deoarece vor fi în contextul unui proiect închis.

