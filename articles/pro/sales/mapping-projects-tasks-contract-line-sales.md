---
title: Maparea proiectelor și activităților într-o linie de contract bazată pe proiect - simplificat
description: Acest subiect oferă informații despre adăugarea și eliminarea de proiecte și sarcini pe o linie de contract.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 30a74f683a032d5bd6caed347f4d0a948376d267
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177661"
---
# <a name="map-projects-and-tasks-to-a-project-based-contract-line---lite"></a>Maparea proiectelor și activităților într-o linie de contract bazată pe proiect - simplificat

_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_

Pe liniile de contract bazate pe proiecte, puteți asocia sarcini specifice dintr-un proiect la linia de contract.

Când asociați sarcini specifice la o linie de contract, metoda de facturare, opțiunile de taxare, limitele care nu trebuie depășite și clienții definiți pe linia de contract vor fi aplicabile numai acelor sarcini specifice.

Dacă aveți un scenariu în care o fază a unui proiect, de exemplu faza prototip, este un preț fix și toate celelalte faze sunt timp și material, veți putea asocia faza prototip și toate sarcinile secundare asociate liniei contractuale pentru faza respectivă cu o metodă de facturare cu preț fix.

Toate celelalte faze din structura de defalcare a lucrărilor de proiect (WBS) pot fi asociate liniei contractuale bazate pe timp și material.

## <a name="associate-tasks-to-project-based-contract-lines"></a>Activități asociate liniilor de contract bazate pe proiect

Activitățile pot fi asociate liniilor contractuale din fila **Activități facturabile** de pe pagina **Linie de contract** sau de pe fila **Facturarea activităților** de pe pagina **Proiect**.

### <a name="from-the-contract-line-page"></a>De pe pagina linie de contract

Parcurgeți pașii următori pentru a asocia sarcinile proiectului la linia contractuală din fila **Activități facturabile** din pagina **Linie de contract**.

1. Pe fila **General** unei linii de contract bazate pe proiect, verificați dacă este completat câmpul **Proiect**.
2. În câmpul **Activități incluse** selectați **Numai activități selectate**.
3. Salvați modificările. Formularul se va reîmprospăta și fila **Activități facturabile** va fi vizibilă.
4. Selectați fila **Activități facturabile** și, în subgrilă, selectați **Adăugați o activitate de linie de contract**.
5. Pe pagina **Activități de linie de contract**, în lista verticală **Activități**, selectați activitatea. 
6. Introduceți informații în câmpul **Tipul de facturare**, apoi selectați **Salvați și închideți**. Activitatea selectată este asociată liniei de contract.

> [!NOTE]
> Aceasta nu este cea mai optimă experiență pentru asocierea sarcinilor proiectului la liniile contractuale. Fiecare proiect va trebui asociat manual în această experiență. Modul preferat este de la fila **Facturarea activității** de pe pagina **Proiect**.

### <a name="from-the-project-page"></a>De pe pagina de proiect

Aceasta este metoda optimă de asociere a sarcinilor la liniile contractuale. Puteți selecta mai multe sarcini și le puteți asocia pe toate și sarcinile secundare lor la linia contractuală selectată. Parcurgeți pașii următori pentru a asocia sarcinile liniei de contract de la pagina **Proiect**.

1. Pe fila **General** unei linii de contract bazate pe proiect, verificați dacă este completat câmpul **Proiect**.
2. Pe câmpul **Activități incluse** selectați **Numai activități selectate**.
3. Salvați linia de contract bazată pe proiect. Formularul se va reîmprospăta și fila **Activități facturabile** va fi vizibilă. Aceasta este doar pentru verificare.
4. Pe fila **General** a liniei de contract bazate pe proiect, în câmpul **Proiect**, selectați linkul de proiect.
5. Pe pagina **Proiect** pagina, selectați fila **Configurarea facturării activităților**.
6. Există două grile. O grilă este pentru liniile contractuale care se aplică întregului proiect. A doua grilă se aplică configurării de facturare specifice activităților. În a doua grilă, selectați una sau mai multe sarcini, apoi selectați **Asociați linii de contract**.
7. În pagina de dialog care se deschide, selectați o linie de contract din meniul derulant.
8. Utilizați lista derulantă **Tipul de facturare** pentru a marca activitățile drept facturabile sau nefacturabile.
9. Bifați caseta de selectare pentru a indica dacă asocierea ar trebui să includă și activități secundare ale activităților selectate. Bifând caseta va asocia, de asemenea, activitățile secundare ale activităților selectate la linia de contract.
10. Selectați **OK** pentru a închide dialogul.

## <a name="unassociate-tasks-from-project-based-contract-lines"></a>Dezasociați activități din liniile de contract bazate pe proiect

### <a name="from-the-contract-line-page"></a>De pe pagina linie contract

Parcurgeți pașii următori pentru a dezasocia activitățile proiectului de pe linia de contract pe fila **Activități facturabile** din pagina **Linie de contract**.

1. Pe fila **Activități facturabile**, selectați **Ștergeți o activități de linie de contract**.
2. Un mesaj de avertizare indică faptul că eliminarea acestei asocieri ar putea duce la inversarea oricăror date înregistrate anterior în activitate. Selectați **OK** în caseta de dialog pentru a elimina asocierea dintre activitate și linia de contract bazată pe proiect. 

> [!NOTE]
> Aceasta nu șterge activitatea din proiect. În schimb, elimină asocierea activității din linia de contract bazată pe proiect.

### <a name="from-the-project-page"></a>De pe pagina de proiect

Aceasta este experiența mai optimă pentru dezasocierea activităților din liniile de contract. Puteți selecta mai multe sarcini și le puteți dezasocia pe toate și sarcinile secundare lor din linia contractuală selectată. Parcurgeți pașii următori pentru a dezasocia sarcinile liniei de contract din linia de contract.

1. De pe fila **General** a liniei de contract bazate pe proiect, în câmpul **Proiect**, faceți clic pe linia de proiect.
2. Pe pagina **Proiect** pagina, selectați fila **Configurarea facturării activităților**.
3. Există două grile pe pagină. O grilă este pentru liniile contractuale care se aplică întregului proiect, iar a doua se aplică configurării facturării specifice activităților. În a doua grilă, selectați una sau mai multe activități și apoi selectați **Dezasociați linii de contract**.
4. În pagina de dialog care se deschide, selectați o linie de contract din meniul derulant.
5. Bifați caseta de selectare pentru a indica dacă asocierea ar trebui să fie eliminată din alte activități secundare ale activităților selectate. Bifând caseta va dezasocia, de asemenea, activitățile secundare ale activităților selectate din linia de contract.
6. Selectați **OK**. Un mesaj de avertizare indică faptul că eliminarea acestei asocieri ar putea duce la inversarea oricăror date înregistrate anterior pe activitate. Selectați **OK** în caseta de avertizare pentru a elimina asocierea dintre activitate și linia de contract bazată pe proiect.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]