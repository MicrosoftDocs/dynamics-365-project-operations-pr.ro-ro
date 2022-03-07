---
title: Aplicație mobilă pentru foaia de pontaj a proiectului
description: Acest subiect oferă informații despre aplicația mobilă Microsoft Dynamics 365 Project Timesheet. Aplicația mobilă Project Timesheet permite utilizatorilor să trimită și să aprobe foi de pontaj pentru proiecte pe dispozitivul lor mobil.
author: abruer
ms.date: 04/08/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: df6d286b6d5716fb0ea908ed71c2257b4db21ecfd35148fea65dfd96e058ac9a
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/06/2021
ms.locfileid: "6997216"
---
# <a name="project-timesheet-mobile-application"></a>Aplicație mobilă pentru foaia de pontaj a proiectului

[!include [banner](../includes/banner.md)]

## <a name="overview"></a>Prezentare generală

Aplicația mobilă Microsoft Dynamics 365 Project Timesheet permite utilizatorilor să trimită și să aprobe foi de pontaj pentru proiecte pe dispozitivul lor mobil (iPhone sau Android). Această aplicație mobilă prezintă funcționalitatea foii de pontaj care se află în zona de management de proiect și contabilitate a Dynamics 365 Finance, îmbunătățind productivitatea și eficiența utilizatorilor, precum și permițând intrarea și aprobarea în timp util a fișelor de pontaj ale proiectului.

## <a name="download-and-install-the-mobile-app"></a>Descărcați și instalați aplicația mobilă

Descărcați și instalați fișierul Microsoft Dynamics 365 Project Timesheet aplicație mobilă pentru Android sau iPhone din magazinul mobil pentru dispozitivul dvs.

## <a name="enable-the-app"></a>Activați aplicația 

În Finanțe, aplicația mobilă Project Timesheet trebuie să fie activată. Pentru a activa funcționalitatea, accesați **Managementul proiectului și parametrii contabili \>Fișă de pontaj** și selectați parametrul **Activați Microsoft Dynamics 365 Project Timesheet**.

## <a name="sign-in-to-the-app"></a>Conectați-vă la aplicație

1.  Deschideți aplicația pe dispozitivul mobil.

2.  Introduceți adresa URL Finance.

3.  Prima dată când vă conectați, vi se solicită numele de utilizator și parola. Introduceți acreditările.

4.  Veți fi conectat la compania dvs. implicită.

## <a name="submit-a-project-timesheet"></a>Trimiteți o foaie de pontaj a proiectului

Puteți crea și trimite o foaie de pontaj a proiectului în aplicație. Puteți baza o nouă foaie de pontaj pe informații dintr-o foaie de pontaj anterioară, linii salvate sau atribuții de proiect. Dacă sunteți desemnat ca delegat, puteți introduce și o foaie de pontaj pentru un alt lucrător. Pentru a crea o foaie de timp ca delegat, selectați butonul **Meniu** și apoi selectați un nume de resursă.

Pagina cu fișa de timp va crea o nouă foaie de pontaj pentru perioada de timp, pe baza datei curente. Se va afișa săptămâna de lucru. Dacă perioada fișei de timp acoperă mai multe săptămâni, puteți selecta o altă săptămână de lucru din filele săptămâna de lucru.
Dacă există o foaie de pontaj pentru data curentă, aceasta va fi afișată. Dacă trebuie să creați o nouă foaie de timp într-o altă perioadă de foaie de timp, selectați butonul **Meniul** și apoi selectați **Foaie de pontaj nouă**.

Puteți introduce informații despre proiect făcând clic pe acțiunea **Adăugați timp** sau acțiunea **Copiați timpul din**. Acțiunea **Copiați timpul din** va copia informațiile despre linia proiectului, dar nu și orele. Meniul **Copiați timpul din** include următoarele opțiuni:

- **Copiați din foaia de pontaj existentă** - Copiați liniile de foaie de timp dintr-o foaie de pontaj existentă.

- **Copiază din favorit** - Creați noi linii ale foii de pontaj utilizând setările foii de pontaj pe care le-ați selectat ca favorite.

- **Copiază din sarcină** - Creați noi linii de foaie de pontaj din proiectele alocate.

Informațiile despre proiect care sunt afișate depind de parametrii mobili pe care i-ați definit pe pagina **Managementul proiectului și parametrii contabili**.

În câmpul **Entitate legală**, selectați entitatea juridică pentru care ați efectuat lucrări de proiect. Câmpul **Entitate legală** este disponibil numai dacă suportul pentru foaia de pontaj între companii este activat pentru entitatea dvs. juridică.

Selectați clientul care este asociat cu proiectul pentru foaia de pontaj. Pentru lansarea inițială pe Android, intrarea de către client nu este acceptată, deoarece trebuie să selectați mai întâi proiectul. Dacă ați selectat proiectul mai întâi, câmpul **Client** este completat automat.

În câmpul **Proiect**, proiectul pentru care introduceți timpul. Câmpul **Client** este completat automat.

Căutările de clienți și proiecte permit căutarea atât în clienți, cât și în proiecte.

Selectați informații în câmpurile **Categorie**, **Activitate**, **Proprietate de linie**, **Grup de impozite pe vânzări** și **Grup de taxe pe vânzări de articole** , după cum este necesar. Aceste câmpuri pot fi suprascrise.

Câmpul **Proprietate de linie** va fi setat la o valoare implicită, pe baza parametrilor de management și contabilitate a proiectului. Când parametrii proiectului/categoriei și categoriei/resurselor sunt activate, valoarea **Proprietate de linie** va fi setată la valoarea implicită pe care ați definit-o pentru această validare. Când parametrii proiectului/categoriei și categoriei/resurselor nu sunt activați, fișierul **Proprietate de linie** valoarea va fi implicită conform câmpului **Activați proprietatea implicită a liniei** pe pagina **Managementul proiectului și parametrii contabili**. Valoarea **Proprietate de linie** poate fi suprascrisă.

Selectați o zi pentru a adăuga timp. Introduceți numărul de ore pe care le-ați lucrat în fiecare zi.

Pentru a adăuga comentarii despre orele pe care le introduceți, faceți clic pe **Adaugă comentarii**, apoi introduceți comentarii pentru un public intern, un public de clienți sau ambele.
Comentariile interne pot fi vizualizate de managerii de proiect. Comentariile clienților sunt incluse pe facturi.

Pentru a salva linia ca favorit, bifați caseta de selectare, apoi faceți clic pe **Salvați ca favorit**.

Dimensiunea financiară și suportul pentru atașament nu sunt furnizate în aplicația mobilă.

Continuați să adăugați linii de proiect după cum este necesar pentru a vă completa fișa de pontaj.

Clic **Trimitere** pentru a trimite foaia de pontaj la fluxul de lucru de aprobare.

## <a name="review-timesheets"></a>Examinați fișele de pontaj

O listă a foilor de pontaj care trebuie revizuite este disponibilă în meniu. Această opțiune este disponibilă numai dacă ați fost desemnat ca aprobator al fluxului de lucru. Sunt acceptate atât aprobarea antetului, cât și a liniei. Aprobarea la nivel de linie oferă posibilitatea de a marca una sau mai multe linii pentru aprobare. După examinarea informațiilor din foaia de timp, faceți clic pe **Aprobare**, **Delegare** sau **Întoarcere** pentru a continua fluxul de lucru.


[!INCLUDE[footer-include](../includes/footer-banner.md)]