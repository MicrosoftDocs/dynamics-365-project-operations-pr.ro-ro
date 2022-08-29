---
title: Sincronizați starea proiectului pentru a preveni intrarea împotriva proiectelor închise
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
# <a name="sync-project-status-to-prevent-entry-against-closed-projects"></a>Sincronizați starea proiectului pentru a preveni intrarea împotriva proiectelor închise

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

## <a name="scenario"></a>Scenariu

Contoso este live cu Microsoft Dynamics 365 Project Operations pentru scenarii de resurse/neaprovizionate. Ca parte a activităților normale de afaceri, proiectele pot fi finalizate sau suspendate. Puteți dezactiva proiectul pentru a vă asigura că nu sunt generate cheltuieli sau facturi.

## <a name="solution"></a>Soluție

### <a name="prerequisites"></a>Cerințe preliminare

-   Microsoft Dynamics Trebuie instalat 365 Finance 10.0.29 sau o versiune ulterioară.
-   Hartă Dual Write 1.0.0.3 pentru Projects V2 (msdyn\_ proiecte) trebuie să fie instalate sau configurate manual după cum este descris mai jos.

### <a name="create-an-updated-version-of-the-project-operations-integration-projects-v2-dual-write-map"></a>Creați o versiune actualizată a hărții de scriere duală Projects V2 de integrare cu operațiunile de proiect

Pentru a actualiza harta cu scriere duală a Project Operations Projects V2:

1. Du-te la **Management de date** spațiu de lucru și selectați **Scriere dublă**.
2. Selectează **Scriere dublă** ţiglă.
3. De la T **Harta tabelului** coloană, localizați și selectați **Proiect V2 (msdyn\_ proiecte)**, apoi selectați Oprire.
4. Selectați numele hărții pentru a deschide harta și apoi selectați **[Nici unul]**.
5. Din caseta de dialog Selectare coloană, selectați **cod de stat\[ Starea proiectului\]** apoi selectați OK. Puteți tasta **stat** în valoarea filtrului pentru a restrânge lista.
6.  Selectați **Adăugați sau editați transformarea** în **tip de hartă** coloană pentru a edita transformarea.
7.  Din **Tip de transformare** Selectați **ValueMap**.
8.  Selectați **Maparea valorii adăugate**, apoi adăugați următoarele **Chei** și **Valori**:

   Tastă       | Valoare 
   ----------|-------
   In proces | 0     
   finalizată | 1     

![Captură de ecran care arată maparea cu scriere duală](media/projectstage-dw-mapping.png)

9. Selectați **Salvare**.
10. Din partea de sus a **Dual-write > Projects V2 (msdyn_projects)** pagina, selectați **Salvează ca**.
11. Din **Adăugați un tabel** în **Editor** câmp, selectați **Editor implicit CDS**.
12. Seteaza **Versiune** câmp la 1.0.0.3.
13. Tastați a **Descriere**, apoi selectați **Salvați**.
14. Din partea de sus a **Dual-write > Projects V2 (msdyn_projects)** pagina, selectați **Alerga** pentru a începe harta, apoi sekect **da** dacă vi se cere să confirme înainte de rulare. 

### <a name="close-a-newly-completed-project"></a>Închideți un proiect nou finalizat

Dynamics 365 Finance folosește **etapa de proiect** domeniu pentru a face diferența între proiecte **in proces** sau **terminat**. **Terminat** proiectele nu pot suporta cheltuieli sau pot fi facturate clienților.

1. Deschide un proiect pentru dezactivare.
2. Din panglică, selectați **Dezactivați**.

> [!NOTE]
> Puteți fie să dezactivați, fie să închideți un proiect, deoarece ambele se vor comporta la fel în contextul Finanțelor.

3. În Finanțe, deschideți **Lista cu toate proiectele** pagină.
4. Confirmați că proiectul dezactivat nu apare în listă.
5. În **arata proiecte** filtrați deasupra listei, modificați valoarea de la **Activ** la **Toate**.
6. Veți vedea acum proiectul dezactivat.

Dacă încercați să înregistrați timp sau cheltuieli pentru acest proiect în Finanțe, nu ar trebui să vedeți proiectul pentru selecție. Dacă introduceți manual numărul proiectului pentru o cheltuială, veți vedea un mesaj precum „Etapa de proiect finalizată nu permite înregistrarea în proiect”. Facturarea și alte funcții de facturare ar trebui să fie dezactivate, deoarece vor fi în contextul unui proiect închis.

