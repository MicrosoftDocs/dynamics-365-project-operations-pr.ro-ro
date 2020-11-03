---
title: Creați un nou proiect
description: Acest subiect oferă informații despre cum să creați un proiect nou.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 727d287c571b2a64bf10b2393a87567093a420d2
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082931"
---
# <a name="create-a-new-project"></a>Creați un nou proiect

[!include [banner](../includes/banner.md)]

Parcurgeți pașii următori pentru a crea un nou proiect.

1. În pagina **Management de proiect** , selectați **Proiect nou** , și introduceți următoarele valori:

    - **Tipul proiectului:** Timp și material
    - **Denumirea proiectului:** Faza 2 de upgrade XYZ
    - **Grup de proiect:** TM\_WIP
    - **ID contract proiect:** 00000002

2. Selectați **Creați un proiect**.

## <a name="assign-a-resource-to-a-project"></a>Atribuirea unei resurse unui proiect

1. Din pagina **Angajați** , în lista **Angajați** , selectați înregistrarea pentru angajatul pentru care ați configurat anterior competențele, și deschideți înregistrarea angajatului.
2. În panoul de acțiuni, în fila **Proiect** , în grupul **Configurare** , selectați **Atribuire proiecte**.
3. Din pagina **Validarea resurselor pentru atribuiri în proiect** , din fila **Proiecte** , în câmpul **Adăugați proiectul la proiectele selectate** , filtrați pentru proiectul **Faza 2 de upgrade XYZ**.
4. În panoul **Proiecte rămase** , selectați un proiect, apoi selectați butonul săgeată pentru a-l adăuga la panoul **Proiecte selectate**.

De asemenea, puteți atribui categorii pentru o resursă după cum doriți. Tipul categoriei este fie **Cost** fie **Venit**. Tipul categoriei este determinat de organizația dvs. Dacă nu sunt alocate categorii pentru o resursă, Finanțele caută categoria implicită a prețurilor orare pentru costuri și venituri.

## <a name="set-up-project-resource-and-role-characteristics"></a>Configurați resursele proiectului și caracteristicile rolului

Un manager de proiect poate utiliza funcționalitatea de alocare de resurse proiectului pentru a crea rolurile necesare pentru proiect. Rolurile pot fi utilizate dacă resursele confirmate sunt încă necunoscute atunci când resursele sunt rezervate. Rolurile pot fi rezervate temporar ca resurse planificate, astfel încât să puteți continua etapele de planificare a proiectului.

[![Exemplu de rol](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Scenariu:** Contoso a fost angajat pentru a finaliza un proiect de timp și materiale care are o cartă de proiect aprobată. Managerul de proiect junior continuă să finalizeze domeniul de aplicare al proiectului. Managerul de resurse identifică în prezent resursele specifice care vor fi rezervate pentru a lucra la noul proiect. Datorită naturii critice a proiectului, sponsorul proiectului a solicitat managerul de proiect senior ca unul dintre roluri. Managerul de resurse trebuie să dobândească noua resursă și să definească rolul în sistem în cazul în care managerul de proiect junior are nevoie de informații despre resurse în timpul planificării proiectului.

Următorii pași arată modul în care managerul de resurse poate configura rolul de manager de proiect senior și poate asocia caracteristicile resursei acestuia. Ulterior, rolul poate fi folosit pentru a căuta resursele disponibile care corespund competențelor necesare pentru resursă.

1. În pagina **Configurare roluri** , selectați **Nou** , și introduceți următoarele valori:

    - **ID rol:** Manager de proiect senior
    - **Descriere:** Manager de proiect senior

2. Selectați **Creare**.
3. Selectați rolul **Manager de proiect senior** , apoi selectați **Configurare caracteristici**.
4. În câmpul **Tip caracteristici** , selectați **Abilitate**.
5. În câmpul **Caracteristici disponibile** , introduceți abilitatea de căutat.
6. În câmpul **Tip caracteristică** , selectați **Certificat**.
7. În câmpul **Caracteristici disponibile** , introduceți tipul de certificat de căutat.

## <a name="assign-a-project-resource-to-a-project"></a>Atribuirea unei resurse de proiect unui proiect

1. Din pagina **Toate proiectele** , selectați proiectul **Faza 2 de upgrade XYZ**.
2. Din fila **Echipa proiectului și planificarea** , selectați **Adăugare**.
3. În câmpul **Rol** , selectați **Membru al echipei**.
4. Selectați **Rezervare din calendar**.
5. Din pagina **Disponibilitate resurse** , selectați **Vizualizare setări**.
6. În pagina **Reglați setările de vizualizare** , introduceți următoarele valori:

    - **Format pentru vizualizarea intervalului de dată:** Zi
    - **Afișați descrierile disponibilității:** Da
    - **Afișați capacitatea rămasă:** Da

7. În lista de resurse, selectați o resursă.
8. Selectați **Rezervare fermă** și **Capacitate completă**.

## <a name="assign-a-resource-to-a-default-role"></a>Atribuirea unei resurse unui rol implicit

Pentru a ajuta managerii de proiect sau de resurse pentru drill down mai mult pentru resursele care pot fi rezervate pentru un proiect. Puteți asocia un rol implicit cu o resursă existentă sau cu o resursă nou achiziționată. De exemplu, când Daniel a fost angajat, avea experiența și abilitățile pentru a ocupa rolul de analist de afaceri. Managerul de resurse a atribuit acest rol ca rolul implicit al lui Daniel. Prin urmare, managerul de resurse l-a adăugat pe Daniel la un grup de analiști de afaceri care sunt disponibili să lucreze la proiecte.

În timpul rezervării resurselor, managerii de proiect pot filtra resursele de rol disponibile pentru a lucra la proiecte. Aceștia pot utiliza aceste informații ca un criteriu atunci când efectuează o analiză a deciziilor pe mai multe criterii în timpul îndeplinirii resurselor. De asemenea, pot adăuga alte caracteristici ale resurselor la filtru pentru a căuta resurse care au abilități, educație și experiență specifice pentru un anumit proiect.

**Scenariu:** A început un proiect aprobat, iar rolul Manager de proiect senior a fost rezervat ca resursă planificată în etapa de planificare a proiectului. Managerul de resurse a achiziționat acum o resursă pentru a îndeplini rolul de manager de proiect senior.

1. Din pagina **Lista resurselor** , selectați **Daniel Goldschmidt**.
2. În pagina **Rol resursă** , selectați **Nou** , și introduceți următoarele valori:

    - **În vigoare:** Introduceți data curentă.
    - **Expirare:** introduceți **Niciodată**.
    - **Rol:** introduceți **Manager de proiect senior**.

3. Selectați **Salvare** , apoi închideți pagina.
4. Din fila **Competențe** , adăugați abilitatea **ProjectMgmt** și certificatul **PMP**.
