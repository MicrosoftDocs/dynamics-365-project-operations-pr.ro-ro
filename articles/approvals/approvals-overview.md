---
title: Prezentare generală a aprobărilor
description: Acest subiect oferă informații despre lucrul cu aprobări în Project Operations.
author: stsporen
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 37994422e9146765076fdbb77f5c763b4f1d0802
ms.sourcegitcommit: 2cf93d8bf0be5b61a739195a41334c34d910e9ba
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961181"
---
# <a name="approvals-overview"></a>Prezentare generală a aprobărilor

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Trimiterile de timp și cheltuieli se deplasează printr-un flux de lucru de aprobare. După ce înregistrările sunt aprobate, tranzacțiile sunt înregistrate în realitate sau timpul este înregistrat în planificare.

## <a name="approvals-workflow"></a>Flux de lucru de aprobări
Când creați și trimiteți o înregistrare de timp sau cheltuială, se creează o înregistrare de aprobare. Aprobatorul proiectului sau managerul dvs. vă examinează și aprobă intrarea. Dacă intrarea este legată de un proiect, atunci când este aprobat, vor fi create datele reale. Acest lucru permite urmărirea costurilor și a facturării. 

## <a name="approve-an-entry"></a>Aprobă o intrare
Formularul **Aprobări** vă permite să comutați între diferite vizualizări, astfel încât să puteți vizualiza diferitele tipuri de aprobări.
  
1. Accesați formularul **Aprobări** și selectați **Cheltuieli**, **Timp**, sau **Retrageri**.
2. Examinați fiecare aprobare și selectați-le pe care doriți să le aprobați.
3. Selectați **Aprobare** pentru a aproba intrările selectate.
Sistemul va procesa aceste intrări și va crea date reale sau o rezervare.

## <a name="reject-an-entry"></a>Respingeți o intrare
În calitate de aprobator de proiect, poate fi necesar să trimiteți o intrare înapoi unui utilizator pentru corectare.
  
1. Accesați formularul **Aprobări** și selectați intrarea de respins. 
2. Selectați **Respinge**.
3. Opțional - Adăugați un comentariu în caseta de dialog **Comentarii de respingere** pentru a informa utilizatorul de ce este respinsă intrarea.
4. Selectați **OK**. Intrarea va fi returnată utilizatorului.
  
## <a name="recall-entries"></a>Retragerea intrărilor
La un moment dat, poate fi necesar să vă amintiți o intrare trimisă. Dacă înregistrarea nu a fost aprobată, va fi returnată imediat. Cu toate acestea, o înregistrare aprobată poate avea un impact material. Aprobatorul proiectului este obligat să aprobe rechemarea pentru a inversa tranzacția în Date reale.

## <a name="specify-project-approvers"></a>Specificați aprobatori de proiect
Fiecare proiect are un număr de membri ai echipei de proiect. Puteți specifica ce membri ai echipei sunt, de asemenea, aprobatori de proiect.

1. Accesați formularul **Proiecte** și deschideți proiectul din listă.
2. Pe fila **Echipă**, selectați membrul echipei care va fi aprobator de proiect și apoi selectați **Editați**.
3. Configurați câmpul **Aprobator de proiect** la **Da**.
4. Selectați **Salvare**.
5. Repetați pașii 2-4 pentru a adăuga aprobatori de proiect adiționali.

## <a name="configure-the-users-manager"></a>Configurați managerul utilizatorului

1. Accesați **Setări** > **Securitate** > **Utilizatori**.
2. Selectați utilizatorul căruia îi atribuiți un manager și în zona **Informații despre organizație**, selectați managerul din listă. 
3. Selectați **Salvare**.


