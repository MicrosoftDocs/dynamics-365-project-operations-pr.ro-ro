---
title: Șabloane de proiect
description: Acest subiect furnizează informații despre modul de utilizare a șabloanelor de proiect pentru configurarea rapidă a proiectului.
author: ruhercul
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: db42c9ea7280274cdc9cc90f1487f27e08f892e5
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148073"
---
# <a name="project-templates"></a>Șabloane de proiect 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Un șablon de proiect este un cadru predefinit care vă ajută să începeți rapid și ușor un proiect. Aveți posibilitatea să utilizați un șablon predefinit pentru a crea un proiect nou cu un singur clic. În ceea ce privește proiectele, trebuie să definiți cerințele preliminare pentru șabloanele de proiect. Trebuie să definiți un calendar de proiect pentru fiecare șablon de proiect, iar rolurile și listele de prețuri trebuie să fie predefinite în organizație, astfel încât componentele șablonului să aibă date utile.

Un șablon de proiect constă din trei componente: o planificare, estimări de proiect și membri ai echipei de proiect.

## <a name="schedule"></a>Planificare

O planificare dintr-un șablon de proiect are același set de elemente ca o planificare într-un proiect. Puteți să creați o ierarhie de activități, să asociați roluri cu activități, să definiți atribute de program și să configurați dependențe. O planificare dintr-un șablon de proiect acceptă, de asemenea, modurile de activitate pentru fiecare activitate. Prin urmare, acesta acceptă motorul de planificare. Trebuie să asociați un calendar de proiect cu proiectul. Când creați o planificare de lucru, nu există nici o diferență între un șablon de proiect și un proiect.

## <a name="project-estimates"></a>Estimări de proiect

Estimările proiectului într-un șablon de proiect funcționează în același mod ca și estimările de proiect într-un proiect. Cu toate acestea, costul și prețurile de vânzare sunt extrase din costul implicit și listele de preț de vânzare care sunt definite în parametrii.

## <a name="creating-a-project-from-a-template"></a>Crearea unui proiect dintr-un șablon
 
Există mai multe modalități de a crea un proiect dintr-un șablon de proiect:

- Când creați un proiect dintr-o ofertă, puteți selecta un șablon de proiect în caseta de dialog **Creare rapidă: proiect**.

> ![Creare rapidă: casetă de dialog proiect](media/project-11.png)

- Când creați un proiect selectând **Proiect nou**, pagina **Proiect** apare înainte ca înregistrarea să fie salvată. În câmpul **Alegeți un șablon**, selectați unul dintre șabloanele de proiect predefinite din organizație.
- Utilizați **Creare proiect dintr-un șablon** de pe pagina **Entitate șablon**.

## <a name="copying-components-of-template-to-project"></a>Copierea componentelor unui șablon în proiect

Când copiați componentele unui șablon de proiect la un proiect, câteva suprascrieri pot apărea, în funcție de setările din proiect.

### <a name="copying-the-schedule"></a>Copierea planificării

Când copiați planificarea dintr-un șablon de proiect, dacă proiectul are un alt calendar de proiect decât șablonul, orele de lucru din calendarul proiectului se aplică la planificarea activităților. Astfel, planificarea este ajustată ca să se potrivească cu calendarul proiectului de rezervă. În mod similar, prima activitate din planificare ia data de începere a proiectului, iar restul planificării ierarhice a activităților se actualizează pe baza duratei și a dependențelor care sunt specificate în șablon. 

### <a name="copying-project-estimates"></a>Copierea estimărilor de proiect 

Când copiați pe linii de estimare proiect, listele de prețuri sunt actualizate. Pentru lista de prețuri de cost, aceste actualizări se bazează pe unitatea deținătoare a proiectului. Pentru lista de prețuri de vânzări, acestea se bazează pe client. Pentru proiecte asociate cu o unitate de vânzări, costul unitar și prețurile de vânzare sunt determinate pe baza acestor liste de prețuri.

### <a name="copying-a-project-team"></a>Copierea unei echipe de proiect

Când o echipă de proiect este copiată dintr-un șablon într-un proiect, resursele generice sunt copiate, împreună cu abilitățile și nivelurile de competență definite în șablon. Atribuirile de resurse generice sunt păstrate cum erau în șablonul de proiect. Resursele denumite nu sunt acceptate în șabloanele de proiect.
