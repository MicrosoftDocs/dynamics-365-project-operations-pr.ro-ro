---
title: Cerințe de articole pentru contractele de proiect cu mai multe surse de finanțare
description: Acest articol oferă informații despre cum să configurați și să utilizați cerințele pentru articole cu mai multe surse de finanțare.
author: sigitac
ms.date: 05/04/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 079856e7cf2ffa9b80ab31ebad1c1b5dbe36a4ad
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028503"
---
# <a name="item-requirements-for-project-contracts-with-multiple-funding-sources"></a>Cerințe de articole pentru contractele de proiect cu mai multe surse de finanțare

_**Se aplică la:** Project Operations pentru scenariile bazate pe stocuri/producție_

Unele acorduri contractuale pentru livrabile bazate pe proiecte ar putea necesita surse multiple de finanțare. Acest articol explică cum să selectați și să configurați sursele de finanțare dorite atunci când sunt necesare mai multe surse pentru un proiect sau un contract de proiect.

## <a name="terminology"></a>Terminologie

- **Sursă de finanțare** – Entitatea care finanțează lucrările contractului de proiect. Această entitate poate fi o organizație internă sau un cont extern de factură (client sau grant).
- **Client de proiect** – Entitatea căreia i se livrează lucrarea proiectului.
- **Cont de factură** – Entitatea externă care plătește pentru lucrarea proiectului.

## <a name="example"></a>Exemplu

Contoso a câștigat un contract de reînnoire a echipamentelor cu doi dintre clienții săi: Adatum US și Adatum Corporate. Contractul include hardware și servicii de instalare care vor fi livrate către Adatum US (clientul proiectului). Hardware-ul va fi finanțat de Adatum Corporate (contul de factură 1), iar lucrările de instalare vor fi finanțate de Adatum US (contul de factură 2).

## <a name="set-up-invoice-account-defaulting-rules-for-item-requirements"></a>Configurați regulile implicite ale contului de factură pentru cerințele articolului

### <a name="prerequisites"></a>Cerințe preliminare

- Microsoft Dynamics 365 Finante **versiunea 10.0.27 sau mai recentă** este necesar să utilizeze cerințe pentru articole care au mai multe conturi de factură.
- Administratorul dvs. de sistem trebuie să activeze **Permiteți cerințele articolului cu mai multe surse de finanțare pentru scenariile stocate/bazate pe producție pentru Operațiuni de proiect** caracteristică în **Managementul caracteristicilor** spațiu de lucru.

### <a name="set-up-the-invoice-account-defaulting-rules"></a>Configurați regulile implicite ale contului de factură

Pentru a configura regulile implicite pentru contul de factură, urmați acești pași.

1. Accesați **Gestionarea proiectelor și contabilitate** \> **Configurare** \> **Gestionarea proiectelor și parametrii contabili**.
1. Pe **General** fila, în **Comenzi de vânzări și cerințe pentru articole** secțiunea, setați **Permite proiecte cu mai multe surse de finanțare** opțiunea pentru **da**.
1. În **Client implicit** câmp, specificați de unde provine în mod prestabilit clientul de livrare a proiectului privind cerințele articolului:

    - **Din sursa de finanțare** – Clientul implicit de livrare a proiectului provine din sursa de finanțare. Dacă cu contractul de proiect sunt asociate mai multe surse de finanțare, se va folosi prima sursă de finanțare din listă.
    - **Din proiect** – Clientul implicit de livrare a proiectului provine de la clientul care este selectat în **Contul de înregistrare a proiectului** camp.

1. Opțional: setați sau modificați contul de factură implicit în înregistrările proiectului:

    1. Mergi la **Management de proiect si contabilitate** \> **Proiecte** \> **Toate proiectele** și deschideți detaliile înregistrării proiectului.
    2. Pe **General** filă, setați sau actualizați **Cont de factură implicit** camp. Contul pe care îl specificați va fi utilizat ca cont de factură implicit pentru cerințele de articole noi care sunt create pentru proiect. Dacă lăsați câmpul necompletat, contul de factură al primei surse de finanțare a contractului de proiect va fi utilizat în mod implicit. Cu toate acestea, utilizatorii vor putea schimba contul atunci când salvează înregistrarea.

### <a name="select-the-invoice-account-to-use-when-you-create-an-item-requirement"></a>Selectați contul de factură pe care să îl utilizați atunci când creați o cerință de articol

Pentru a selecta contul de factură de utilizat atunci când creați o cerință de articol, urmați acești pași.

1. Mergi la **Management de proiect si contabilitate** \> **Proiecte** \> **Toate proiectele** și selectați înregistrarea proiectului.
1. Pe **Plan** filă, selectați **Cerințe pentru articole**.
1. Creați o nouă înregistrare a cerințelor de articol.

    - În mod implicit, **Cont de factură** câmpul din înregistrare este setat la contul de factură care este setat pentru proiect. Puteți modifica valoarea **Cont de factură** câmp și apoi salvați înregistrarea. După ce înregistrarea este salvată, nu mai puteți actualiza **Cont de factură** valoare. Dacă trebuie să actualizați **Cont de factură** valoare pentru cerința de articol, ștergeți cerința de articol existentă și apoi creați una nouă care are valoarea dorită.
    - În mod implicit, **Client** câmpul pentru cerința articolului este setat pe baza **Client implicit** valoarea care este setată pe **Management de proiect și parametri contabili** pagină.

    Când înregistrarea cerințelor articolului este salvată, sistemul o asociază cu **Cerința articolului comandă de vânzare** înregistrare antet. Dacă niciun antet de comandă de vânzare deschisă nu are contul de factură selectat, sistemul va crea unul și va asocia linia de cerințe de articol cu acesta.

> [!NOTE]
> Cerințele pentru articole sunt întotdeauna facturate integral în contul de factură care este setat în înregistrare. Sistemul nu acceptă în prezent regulile de alocare a fondurilor care au cerințe pentru articole și nu va împărți postarea pe baza setării regulilor de alocare a finanțării.

### <a name="create-an-item-requirement-from-an-item-forecast-record"></a>Creați o cerință de articol dintr-o înregistrare de prognoză a articolului

Pentru a crea o cerință de articol dintr-o înregistrare de prognoză a articolului, urmați acești pași.

1. Mergi la **Management de proiect si contabilitate** \> **Proiecte** \> **Toate proiectele** și selectați înregistrarea proiectului.
1. Pe **Plan** filă, selectați **Previziunile articolului**.
1. Creați o nouă înregistrare de prognoză a articolului.
1. Opțional: pe **Proiect** fila, în **Sursă de finanțare** câmp, selectați contul de factură dorit.
1. Selectați **Creați cerințe de articol** și confirmați mesajul pe care îl primiți.

    > [!NOTE]
    > Sistemul copiază **Sursă de finanțare** valoarea de la înregistrarea de prognoză a articolului până la înregistrarea de cerințe de articol nou creată.

### <a name="default-invoice-account-when-the-system-automatically-creates-an-item-requirement-from-a-purchase-order-line"></a>Cont de factură implicit când sistemul creează automat o cerință de articol dintr-o linie de comandă de achiziție

Dacă **Creați cerințe de articol** opțiunea este setată la **da** pe **Management de proiect și parametri contabili** pagina, sistemul creează automat o cerință de articol atunci când este salvată o nouă linie de comandă de achiziție de proiect. În mod implicit, **Cont de factură** și **Cerința articolului** câmpurile sunt setate la valoarea lui **Cont de factură implicit** câmp din fișa proiectului. Sistemul nu acceptă în prezent actualizarea sau modificarea contului de factură pentru înregistrările de acest tip.
