---
title: Configurați subcontractanții ca resurse ce se pot rezerva
description: Acest subiect explică modul de configurare și de întreținere a resurselor pentru subcontractori care sunt create de la utilizatori și persoane de contact în sistem, astfel încât să poată fi asociate cu subcontractele din Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 07/28/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 6d2f250063afc24de99e308d8d7583d1822bcabb
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8597261"
---
# <a name="set-up-subcontractors-as-bookable-resources"></a>Configurați subcontractanții ca resurse ce se pot rezerva

[!include [banner](../../includes/dataverse-preview.md)]

_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_

Urmați acești pași pentru a configura subcontractanții ca resurse ce se pot rezerva în Microsoft Dynamics 365 Project Operations.

1. Accesați **Proiect** \> **Resurse**, și selectați **Nou**.
2. Pe pagina **Resursă nouă ce se poate rezerva**, în câmpul **Tipul resursei**, selectați una dintre următoarele opțiuni:

    - **Utilizator** - Selectați acest tip de resursă dacă subcontractantul trebuie să acceseze Project Operations pentru a introduce timp sau cheltuieli. Dacă selectați **Utilizator**, subcontractantul necesită o licență valabilă pentru a accesa sistemul.
    - **Persoană de contact** sau **Cont** - Selectați unul dintre aceste tipuri de resurse dacă subcontractorul nu necesită acces la Project Operations, dar trebuie să fie disponibil pentru atribuiri de sarcini sau rezervări la proiecte. Niciunul dintre aceste tipuri de resurse nu oferă acces la sistem. Selectați **Cont** pentru a reprezenta compania furnizorului ca resursă ce se poate rezerva. Selectați **Persoană de contact** pentru a reprezenta angajații individuali ai furnizorului.

3. În funcție de tipul de resursă selectat, vi se solicită să selectați utilizatorul, contul sau înregistrarea de persoană de contact corespunzătoare.
4. În câmpul **Tip de lucrător**, selectați „Lucrător contractual” pentru a configura subcontractorul ca resursă ce se poate rezerva.

    > [!NOTE]
    > Dacă lăsați necompletat câmpul **Tipul de lucrător** necompletat, resursa ce se poate rezerva va fi considerată ca un angajat.

5. Dacă ați selectat **Lucrător contractual** ca tip de lucrător, selectați furnizorul pentru care funcționează resursa.
6. Selectați fusul orar al resursei, apoi selectați **Salvare**. Pentru a atribui un șablon de ore de lucru la resursa ce se poate rezerva, puteți selecta **Setare calendar** pe pagina listei **Resursă ce se poate rezerva**.

Pentru a fi asociată cu o linie de subcontract, o resursă ce se poate rezerva trebuie să îndeplinească aceste condiții:

- Resursa ce se poate rezerva trebuie să fie un lucrător contractual.
- O resursă ce se poate rezerva de tip de resursă **Persoană de contact** trebuie să fie asociat cu contul furnizorului ca persoană de contact. O resursă ce se poate rezerva de tip de resursă **Utilizator** by trebuie să fie asociat cu contul furnizorului ca persoană de contact.
- Valoarea câmpului **Furnizor** pentru resursa ce se poate rezerva trebuie să corespundă valorii câmpului **Furnizor** pentru subcontractant.

## <a name="update-the-type-of-worker-and-vendor-mapping-for-bookable-resources"></a>Actualizați tipul de mapare a lucrătorului și a furnizorului pentru resurse ce se pot rezerva

Câmpul **Tipul de lucrător** pentru o resursă ce se poate rezerva determină dacă resursa ce se poate rezerva este un lucrător contractual sau un angajat. Câmpul **Furnizor** definește contul furnizor cu care este asociată resursa ce se poate rezerva. Prin asocierea unei resurse ce se pot rezerva cu un furnizor ca persoană de contact, indicați că persoana de contact este un angajat al companiei furnizor.

Dacă câmpurile **Tip de lucrător** și **Furnizor** pentru o resursă ce se poate rezerva sunt modificate, modificările afectează orice validări viitoare ale noilor înregistrări create de resursa ce se poate rezerva, cum ar fi intrările de timp. Cu toate acestea, modificările nu invalidează înregistrările existente.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
