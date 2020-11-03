---
title: Procesarea chitanțelor de cheltuieli
description: Acest subiect oferă informații despre procesarea recunoașterii optice a caracterelor (OCR) pentru chitanțe. Această caracteristică este concepută pentru a îmbunătăți experiența utilizatorului când sunt create rapoarte de cheltuieli în Microsoft Dynamics 365 Finance.
author: stsporen
manager: AnnBe
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: stsporen
ms.search.validFrom: 2019-11-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 31c08ea264e6caec3217f4b424275495f39123e3
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082954"
---
# <a name="expense-receipt-processing"></a>Procesarea chitanțelor de cheltuieli

[!include [banner](../includes/banner.md)]

Introducerea cheltuielilor a fost îmbunătățită prin introducerea procesării de recunoaștere optică a caracterelor (OCR) pentru chitanțe. Această caracteristică este concepută pentru a îmbunătăți experiența utilizatorului când sunt create rapoarte de cheltuieli.

## <a name="key-features"></a>Caracteristici cheie

- Numele comerciantului, data și suma totală sunt extrase din chitanțe.
- Caracteristica încercă să potrivească chitanțele neatașate cu tranzacțiile de cheltuieli neatașate.
- Utilizatorii pot crea tranzacții de cheltuieli introduse manual din chitanțe.

## <a name="usage-examples"></a>Exemple de utilizare

Pentru a atașa automat chitanțe care includ tranzacții cu cardul de credit atunci când este creat un raport de cheltuieli, parcurgeți pașii următori:

  1. Deschideți spațiul de lucru **Gestionarea cheltuielilor**.
  2. Pe fila **Chitanțe** , verificați dacă există chitanțe neatașate. De asemenea, puteți încărca chitanțe pe fila **Chitanțe**.
  3. Pe fila **Cheltuieli** , verificați dacă există cheltuieli neatașate. De obicei, administratorul cheltuielilor importă aceste cheltuieli de la furnizorul cardului de credit.
  4. Selectați **Nou raport de cheltuieli**. Observați că puteți include cheltuieli și chitanțe și acum, atunci când creați un raport de cheltuieli. Dacă adăugați atât cheltuieli, cât și chitanțe, se declanșează corelarea automată a chitanțelor cu cheltuielile.

Pentru a crea o cheltuială sau pentru a potrivi o cheltuială dintr-o chitanță, parcurgeți pașii următori:

  1. Pe un raport de cheltuieli, pe fila **Chitanțe** , atașați o chitanță selectând **Adăugați chitanțe**.
  2. Sub imaginea încărcată a chitanței, observați opțiunile **Creare** și **Potrivire**.

      - Selectați **Creare** pentru a crea o tranzacție de cheltuieli introdusă manual și pentru a completa valorile care sunt extrase din chitanță.
      - Dacă selectați sistemul **Potrivire** , sistemul încearcă să potrivească o cheltuială existentă cu chitanța.

## <a name="installation"></a>Instalare

Această caracteristică funcționează în combinație cu caracteristica **Rapoarte de cheltuieli reimaginate** pentru a simplifica experiența cheltuielilor. Această caracteristică este disponibilă numai pentru mediile Tier 2+, care sunt Sandbox și Production.

Pentru a utiliza aceste capabilități avansate de cheltuieli, instalați programul de completare Serviciul de gestionare a cheltuielilor pentru Microsoft Dynamics 365 Finance și activați funcțiile din instanța dvs. Puteți accesa programul de completare din proiectul dvs. din Microsoft Dynamics Lifecycle Services (LCS).

1. Conectați-vă la LCS și deschideți mediul dorit.
2. Accesați **Toate detaliile**.
3. Selectați **Menţine** , sau derulați în jos la FastTab **Programe de completare de mediu**.
4. Selectați **Instalați un nou program de completare**.
5. Selectați **Serviciu gestionare cheltuieli**.
6. Urmați ghidul de instalare și acceptați termenii și condițiile.
7. Selectați **Instalare**.

În spațiul de lucru **Managementul caracteristicilor** , activați următoarele caracteristici:

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

Pentru mai multe informații despre caracteristica reimaginată a rapoartelor de cheltuieli, consultați [Rapoarte de cheltuieli reimaginate](ExpenseWorkspaceNew.md).

## <a name="frequently-asked-questions"></a>Întrebări frecvente

**Utilizează Microsoft datele mele pentru modelele sale?**

Nu, Microsoft a construit un model general învățare programată pentru serviciul său de procesare a chitanțelor. Acest model nu se bazează pe chitanțele pe care le încărcați.

**Unde este disponibilă și procesată această caracteristică?**

În prezent, Statele Unite sunt acceptate.

**Unde merg chitanțele mele?**

Finance va contacta serviciile cognitive pentru a extrage datele din câmp. Serviciile cognitive vor păstra o copie a chitanței dvs. timp de până la 24 de ore în timp ce are loc procesarea. După finalizarea procesării, Cognitive Services va elimina chitanța. Chitanțele sunt încă stocate în Finanțe.

Pentru mai multe informații, consultați [Activați înțelegerea chitanței cu noua capacitate a Recunoscătorului de formulare](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).
