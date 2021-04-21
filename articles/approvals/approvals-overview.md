---
title: Prezentare generală a aprobărilor
description: Acest subiect oferă informații despre lucrul cu aprobări în Project Operations.
author: stsporen
manager: Annbe
ms.date: 03/31/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: b2da22e10cf6c40a2c84bcd32437b2830f830d07
ms.sourcegitcommit: b4a05c7d5512d60abdb0d05bedd390e288e8adc9
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 04/02/2021
ms.locfileid: "5852514"
---
# <a name="approvals-overview"></a>Prezentare generală a aprobărilor

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Trimiterile de timp, cheltuieli și utilizare a materialelor se deplasează printr-un flux de lucru de aprobare. După ce înregistrările sunt aprobate, tranzacțiile sunt înregistrate în realitate sau timpul este înregistrat în planificare.

## <a name="approvals-workflow"></a>Flux de lucru de aprobări
Când creați și trimiteți o intrare de timp, cheltuială sau utilizare a materialului, se creează o înregistrare de aprobare. Aprobatorul de proiect sau managerul examinează și aprobă intrarea. Dacă intrarea este legată de un proiect, valorile reale vor fi create atunci când sunt aprobate. Acest lucru permite urmărirea costurilor și a facturării.

## <a name="approve-an-entry"></a>Aprobă o intrare
Pagina **Aprobări** vă permite să comutați între diferite vizualizări, astfel încât să puteți vizualiza diferitele tipuri de aprobări.
  
1. Accesați pagina **Aprobări** și selectați **Cheltuieli**, **Timp**, **Utilizarea materialelor** sau **Retrageri**.
2. Examinați fiecare aprobare și selectați-le pe care doriți să le aprobați.
3. Selectați **Aprobare** pentru a aproba intrările selectate.
Sistemul procesează aceste intrări și creează date reale.

## <a name="reject-an-entry"></a>Respingeți o intrare
În calitate de aprobator de proiect, poate fi necesar să trimiteți o intrare înapoi unui utilizator pentru corectare.
  
1. Accesați pagina **Aprobări** și selectați intrarea de respins. 
2. Selectați **Respinge**.
3. Opțional, adăugați un comentariu în caseta de dialog **Comentarii de respingere** pentru a informa utilizatorul de ce este respinsă intrarea.
4. Selectați **OK**. Intrarea va fi returnată utilizatorului.
  
## <a name="cancel-approval"></a>Anulați aprobarea
În unele cazuri, poate fi necesar să anulați o înregistrare aprobată anterior. Anularea unei înregistrări aprobate anterior va avea un impact financiar. 

## <a name="approving-recall-requests"></a>Aprobarea solicitărilor de retragere
În unele cazuri, este posibil ca un consultant să trebuiască să retragă o înregistrare aprobată anterior. Anularea unei înregistrări aprobate anterior va avea un impact financiar. Aprobatorul de proiect este obligat să aprobe retragerea pentru a inversa tranzacția în Valori reale.

## <a name="specify-project-approvers"></a>Specificați aprobatori de proiect
Fiecare proiect are un număr de membri ai echipei de proiect. Puteți specifica ce membri ai echipei sunt, de asemenea, aprobatori de proiect.

1. Accesați pagina **Proiecte** și deschideți proiectul din listă.
2. Pe fila **Echipă**, selectați membrul echipei care va fi aprobator de proiect și apoi selectați **Editați**.
3. Configurați câmpul **Aprobator de proiect** la **Da**.
4. Selectați **Salvare**.
5. Repetați pașii 2-4 pentru a adăuga aprobatori de proiect adiționali.

## <a name="configure-the-users-manager"></a>Configurați managerul utilizatorului

1. Accesați **Setări** > **Securitate** > **Utilizatori**.
2. Selectați utilizatorul căruia îi atribuiți un manager și în zona **Informații despre organizație**, selectați managerul din listă. 
3. Selectați **Salvare**.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
