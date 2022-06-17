---
title: Capturați o chitanță utilizând OCR
description: Acest articol oferă informații despre procesarea recunoașterii optice a caracterelor (OCR) pentru chitanțe.
author: suvaidya
ms.date: 11/10/2021
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: ee16a43fa544af793676072f304d732359d3d9ec
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8917821"
---
# <a name="capture-a-receipt-using-ocr"></a>Capturați o chitanță utilizând OCR

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Introducerea cheltuielilor a fost îmbunătățită prin introducerea procesării de recunoaștere optică a caracterelor (OCR) pentru chitanțe. Această funcționalitate este concepută pentru a îmbunătăți experiența utilizatorului la crearea rapoartelor de cheltuieli.

## <a name="key-features"></a>Caracteristici cheie

- Sistemul extrage numele comerciantului, data și suma totală din chitanțe.
- Sistemul va încerca să potrivească chitanțele neatașate cu tranzacțiile de cheltuieli neatașate.
- Puteți crea tranzacții de cheltuieli introduse manual din chitanțe.

## <a name="attach-receipts-to-an-expense-report"></a>Atașați chitanțe la un raport de cheltuieli

Pentru a atașa automat chitanțe care includ tranzacții cu cardul de credit atunci când este creat un raport de cheltuieli, parcurgeți pașii următori.

  1. Deschideți spațiul de lucru **Gestionarea cheltuielilor**.
  2. Pe fila **Chitanțe**, verificați dacă există chitanțe neatașate. De asemenea, puteți încărca chitanțe pe fila **Chitanțe**.
  3. Pe fila **Cheltuieli**, verificați dacă există cheltuieli neatașate. De obicei, administratorul cheltuielilor importă aceste cheltuieli de la furnizorul cardului de credit.
  4. Selectați **Nou raport de cheltuieli**. Observați că puteți include cheltuieli și chitanțe și acum, atunci când creați un raport de cheltuieli. Dacă adăugați atât cheltuieli, cât și chitanțe, se declanșează corelarea automată a chitanțelor cu cheltuielile.

## <a name="create-or-match-receipts-to-an-expense-report"></a>Creați sau potriviți chitanțe la un raport de cheltuieli
Pentru a crea o cheltuială sau pentru a potrivi o cheltuială dintr-o chitanță, parcurgeți pașii următori.

  1. Pe un raport de cheltuieli, pe fila **Chitanțe**, atașați o chitanță selectând **Adăugați chitanțe**.
  2. Sub imaginea încărcată a chitanței, observați opțiunile **Creare** și **Potrivire**.

      - Selectați **Creare** pentru a crea o tranzacție de cheltuieli introdusă manual și pentru a completa valorile care sunt extrase din chitanță.
      - Dacă selectați sistemul **Potrivire**, sistemul încearcă să potrivească o cheltuială existentă cu chitanța.

## <a name="installation"></a>Instalare

Pentru a utiliza aceste capabilități avansate de cheltuieli, instalați programul de completare Expense Management Service pentru Microsoft Dynamics 365 Finance și activați funcțiile din instanța dvs. Puteți accesa programul de completare din proiectul dvs. din Microsoft Dynamics Lifecycle Services (LCS).

1. Conectați-vă la LCS și deschideți mediul dorit.
2. Accesați **Toate detaliile**.
3. Selectați **Menţine**, sau derulați în jos la FastTab **Programe de completare de mediu**.
4. Selectați **Instalați un nou program de completare**.
5. Selectați **Serviciu gestionare cheltuieli**.
6. Urmați ghidul de instalare și acceptați termenii și condițiile.
7. Selectați **Instalare**.

În spațiul de lucru **Managementul caracteristicilor**, activați următoarele caracteristici:

- Rapoarte de cheltuieli reimaginate
- Potriviți automat și creați cheltuieli de la primire

Când activați aceste funcții, au loc următoarele acțiuni:

- Spațiul de lucru existent **Gestionarea cheltuielilor** este înlocuit cu noul spațiu de lucru.
- Se adaugă un nou element de meniu pentru vizibilitatea câmpului de cheltuieli.
- Puteți deschide încă fosta pagină **Rapoarte de cheltuieli** accesând **Gestionarea cheltuielilor > Cheltuielile mele > Rapoarte de cheltuieli**.
- Fluxurile de lucru și orice aprobări vă duc în continuare la pagina de rapoarte de cheltuieli existente.
- Chitanțele vor fi procesate prin Microsoft Azure Cognitive Services și metadatele vor fi extrase și adăugate.
- Se adaugă o opțiune care vă permite să creați un raport de cheltuieli care include chitanțe neatașate potrivite.
- O opțiune care este adăugată la rapoartele de cheltuieli vă permite să creați o linie de cheltuieli dintr-o chitanță sau să încercați să potriviți o chitanță existentă cu o linie de cheltuieli existentă.

## <a name="frequently-asked-questions"></a>Întrebări frecvente

**Utilizează Microsoft datele mele pentru modelele sale?**

Nu, Microsoft a construit un model general învățare programată pentru serviciul său de procesare a chitanțelor. Acest model nu se bazează pe chitanțele pe care le încărcați.

**Unde este disponibilă și procesată această caracteristică?**

Disponibilitatea acestei caracteristici în diferite regiuni este listată în tabelul următor. Dacă regiunea dvs. nu este acceptată în prezent, trimiteți o solicitare pentru a acorda prioritate disponibilității serviciului OCR în regiunea dvs. 

| Regiunea | Acceptat                         |
|--------|-----------------------------------|
| STATELE UNITE ALE AMERICII    | Da                               |
| CAN    | Da                               |
| Regatul Unit     | Da                               |
| AUS    | Da                               |
| UE     | Parţial. Numai chitanțe în limba engleză. |
| Asia   | No                                |
| Japonia  | No                                |
| Africa | No                                |

**Unde merg chitanțele mele?**

Finance va contacta serviciile cognitive pentru a extrage datele din câmp. Serviciile cognitive vor păstra o copie a chitanței dvs. timp de până la 24 de ore în timp ce are loc procesarea. După finalizarea procesării, Cognitive Services va elimina chitanța. Chitanțele sunt încă stocate în Finanțe.

Pentru mai multe informații, consultați [Activați înțelegerea chitanței cu noua capacitate a Recunoscătorului de formulare](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
