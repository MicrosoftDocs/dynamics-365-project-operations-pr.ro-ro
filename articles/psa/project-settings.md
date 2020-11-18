---
title: Setări de proiect
description: Acest subiect furnizează informații despre setările de management de proiect.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: c9b8659f3b7ee81d2e21ef52743debd521fa9bb9
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082959"
---
# <a name="project-settings"></a>Setări de proiect

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Utilizați următoarele setări pentru a accesa caracteristicile de planificare a proiectului.

## <a name="work-template"></a>Șablon de lucru

Pentru a crea o planificare de proiect, creați un șablon de calendar de proiect care definește numărul de ore de lucru pe zi și orice închideri de firmă. Pentru a crea un șablon de calendar de proiect, asociați un șablon de lucru cu câmpul **Șablon de calendar** pentru proiect. Urmați acești pași pentru a crea un șablon de lucru.

1. În PSA, în panoul de navigare din stânga, faceți clic pe **Resurse**. 
2. Pe pagina listei **Resurse** , deschideți o înregistrare de utilizator și apoi selectați **Afișați ore de lucru**.

  > [!NOTE]
  > Asigurați-vă că permiteți ferestrele pop-up pe pagina browserului. Acest lucru vă permite să vedeți orele de lucru setate pentru resursă.
  
3. Pe fila **Vizualizare lunară** , faceți clic pe **Configurați**. Apare o listă cu trei opțiuni: 

  - Planificare săptămânală nouă
  - Planificare lucru pentru o zi
  - Întrerupere

> ![Configurați opțiuni](media/project-13.png)

4. Selectați **Programul săptămânal nou** , apoi setați opțiunile pentru această planificare de resurse. Puteți seta o planificare săptămânală recurentă, parametri de oră pe zi, închideri de afaceri și multe altele.
5. Setați intervalul de date, selectați **Salvare** , apoi faceți clic pe **Închidere**. 
6. Reveniți la pagina listă **Resurse** și selectați resursa pentru care setați orele de lucru. 
7. Selectați **Configurați calendarul ca** pentru a seta șablonul de lucru. 
8. În caseta de dialog **Șablon de lucru** , introduceți un nume pentru șablonul de lucru și apoi selectați **Aplicați**. 

Acum aveți posibilitatea să asociați șablonul de lucru cu un șablon de calendar de proiect.

## <a name="resource-roles"></a>Roluri de resursă

Termenul *rol de resursă* se referă la setul de aptitudini, competențe și certificări pe care o persoană trebuie să le aibă pentru a efectua un anumit set de activități într-un proiect. PSA vă permite să stabiliți costul și să facturați timpul unei resurse pe baza rolului cu care este asociată o resursă. Fiecare organizație trebuie să configureze aceste roluri utilizând navigarea din partea stângă a meniului **Project Service**.

Fiecare organizație trebuie să configureze aceste roluri pe pagina **Categorii resursă activă**. Pentru a deschide această pagină, în panoul de navigare din stânga, selectați **Roluri resursă**.

## <a name="price-lists"></a>Liste de prețuri

Listele de prețuri vă permit să configurați costurile și prețurile de vânzări pentru rolurile de resurse, categoriile de cheltuieli, produse și alte elemente dintr-o organizație. Înainte să configurați estimări financiare pentru lucrul care trebuie livrat pentru un proiect, ar trebui să creați un cost de rezervă și o listă de prețuri de vânzări. În secțiunea parametri, ar trebui să configurați, de asemenea, un cost implicit și lista de prețuri de vânzări care se aplică tuturor proiectelor care sunt create în organizație. Pe pagina **Parametri proiect activi** , asigurați-vă că configurați un cost implicit și o listă de prețuri de vânzări.