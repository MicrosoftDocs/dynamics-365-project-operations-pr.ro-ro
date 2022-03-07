---
title: Planificarea de cheltuieli al anchetei Federal Awards
description: Acest subiect oferă informații despre ancheta privind planificarea de cheltuieli al Federal Awards.
author: velofog
ms.date: 04/2/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PSNProjSEFAinquiry
audience: Application User
ms.devlang: ''
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.tgt_pltfrm: ''
ms.custom: ''
ms.search.region: Global
ms.search.industry: public sector
ms.author: andchoi
ms.search.validFrom: 2020-4-01
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: d0cc3db3fd05fa809f707b15a50380753ac8f9f779f45c13f707321d2b0e0841
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007251"
---
# <a name="schedule-of-expenditures-of-federal-awards-inquiry"></a>Planificarea de cheltuieli al anchetei Federal Awards

[!include [banner](../includes/banner.md)]

Potrivit Circularei Biroului de Management și Buget A-133, agențiile care primesc fonduri federale sunt supuse cerințelor de audit, care sunt, de asemenea, cunoscute sub numele de audituri unice. Procesul de audit este utilizat pentru raportarea recurentă a veniturilor și cheltuielilor subvențiilor federale. O parte a raportului de audit unic include planificarea de cheltuieli al Federal Awards (SEFA).

Ancheta privind cheltuielile pentru Federal Awards include titlul și numărul Catalogului de asistență internă federală (CFDA), numărul grantului, anul acordării grantului, numele agenției federale care furnizează fondurile și numele permisului prin entitate. Ancheta este pentru o anumită perioadă. De obicei, acea perioadă este aceeași cu perioada situației financiare, care este un exercițiu financiar.

Ancheta include subvenții care au date de proiecție în intervalul de date selectat. Coloana **Agenția de finanțare** a anchetei arată clientul subvenționat sau, pentru o subvenție de trecere, agenția care acordă grantul. Pentru o subvenție de trecere, coloana **Agenție de trecere** arată clientul de grant. Dacă grantul nu este un grant de trecere, coloana **Agenție de trecere** este necompletată.

## <a name="set-up-the-cfda-clusters"></a>Configurați clusterele CFDA

Trebuie să configurați clusterele CFDA care pot fi asociate cu numerele CFDA în ancheta privind planificarea de cheltuieli a Federal Awards.

1. Accesați **Management de proiect și contabilitate \> Configurare \> granturi \> Catalogul grupurilor federale de asistență internă**.
2. Selectați **Nou** pentru a crea un cluster CFDA.
3. Introduceți numele clusterului.
4. Selectați **Salvare** pentru a vă salva modificările.

## <a name="set-up-cfda-numbers"></a>Configurați numerele CFDA

Trebuie să configurați numerele CFDA care pot fi adăugate granturile și incluse în ancheta de planificare a cheltuielilor a Federal Awards.

1. Accesați **Management de proiect și contabilitate \> Configurare \> granturi \> Catalogul numerelor federale de asistență internă**.
2. Selectați **Nou** pentru a crea un număr CFDA.
3. În coloana **Număr**, introduceți numărul CFDA.
4. Apăsați tasta **Tab**.
5. În coloana **Descriere**, introduceți titlu CFDA.
6. Apăsați tasta **Tab**.
7. Opțional: în câmpul **Cluster de program**, adăugați clusterul CFDA corespunzător.
8. Selectați **Salvare** pentru a vă salva modificările.

## <a name="set-up-grants-to-report-for-the-schedule-of-expenditures-of-federal-awards-inquiry"></a>Configurați granturi pentru a raporta pentru ancheta privind planificarea de cheltuieli al Federal Awards

1. Accesați **Management de proiect și contabilitate \> granturi \> granturi** și selectați o subvenție existentă.
2. Pe FilaRapidă **Configurare**, în câmpul **Catalogul asistenței interne federale**, atribuiți numărul CFDA. Numărul CFDA al grantului determină clusterul CFDA pentru raportare.
3. Pe FastTab **Informații de contact**, introduceți informațiile despre concedent urmând acești pași:

    1. În câmpul **Client de grant**, introduceți clientul care este responsabil pentru grant. Pentru un grant existent, aceste informații ar putea fi deja introduse.
    2. Indicați dacă clientul grantului este finanțatorul. Dacă clientul de grant este finanțatorul, lăsați caseta de selectare **Trecere** liberă. Dacă un alt client este finanțatorul, iar clientul de subvenție este responsabil pentru cheltuirea și urmărirea banilor, selectați caseta de bifare **Trecere**.

4. Dacă ați selectat caseta de bifare **Trecere** din pasul anterior, în câmpul **Agenția de finanțare**, introduceți clientul care a furnizat grantul. Agenția care acordă grantul și clientul care acordă grantul nu pot fi același client.

Iată un exemplu de subvenție de trecere:

Guvernul federal a finanțat un proiect de infrastructură pentru un stat. Guvernul federal a dat banii statului pentru a-i cheltui. În acest caz, guvernul federal este agenția care acordă, iar statul este clientul care acordă grantul.

> [!NOTE] 
> Când porniți prima dată funcția, numerele inițiale CFDA vor fi introduse utilizând numerele existente pe subvenții.

## <a name="exclude-grants-from-sefa-reporting-based-on-the-grant-type"></a>Excludeți subvențiile din raportarea SEFA pe baza tipului de subvenție

1. Accesați **Gestionarea proiectului și contabilitate \> Configurare \> Granturi \> Tipuri de granturi**.
2. Pe FilaRapidă **Informații implicite**, selectați caseta de bifat **Excludeți din planificarea de cheltuieli Granturile federale**.
3. Selectați **Salvare** pentru a vă salva modificările.

## <a name="run-the-schedule-of-expenditures-of-federal-awards-inquiry"></a>Rulați Planificarea de cheltuieli al anchetei Federal Awards

1. Accesați **Management de proiect și contabilitate \> Cereri și rapoarte \> Anchetă de grant \> Planificarea de cheltuieli al premiilor federale**.
2. În secțiunea **Parametri**, urmați acești pași:

    1. În câmpul **Interval de date**, selectați codul pentru intervalul de date. Alternativ, în câmpurile **Data de la** și **La data**, definiți intervalul de date.
    2. Opțional: pentru a include numai tranzacții facturate ca venituri în anchetă, setați **Includeți numai veniturile facturate** opțiune pentru **Da**.

## <a name="columns"></a>Coloane

Ancheta privind planificarea cheltuielilor pentru Federal Awards include următoarele coloane:

- Catalogul denumirii clusterului de asistență internă federală
- Agenția de finanțare
- Agenție de trecere
- Numele grantului
- ID-ul grantului
- ID-ul aplicației de grant
- Catalogul asistenței interne federale
- Chitanțe
- Cheltuieli


[!INCLUDE[footer-include](../includes/footer-banner.md)]