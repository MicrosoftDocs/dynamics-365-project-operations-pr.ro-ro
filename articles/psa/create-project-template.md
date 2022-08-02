---
title: Crearea unui șablon de proiect
description: Cum să creați un șablon de proiect în Project Service
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 07/19/2022
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 8159e0390441e5029f9beb0228cffcbc4d683479
ms.sourcegitcommit: 278740b352f1ed9618ee5c79597c8f449984d6f4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 07/19/2022
ms.locfileid: "9177441"
---
# <a name="create-a-project-template-project-service"></a>Crearea unui șablon de proiect (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Șabloanele de proiect vă economisesc timp în cazul în care compania dvs. licitează regulat pentru tipuri similare de proiecte. Acestea oferă un set standard de roluri și ore estimate pentru un tip de proiect. Managerii de cont și managerii de proiect pot crea proiecte bazate pe un șablon de proiect sau pot să copieze șablonul și să creeze unul propriu.  
  
## <a name="components-of-project-template"></a>Componentele șablonului de proiect
 Un șablon de proiect constă în trei componente:  
  
- **Structura detaliată a proiectului**: O structură de defalcare a proiectului dintr-un șablon de proiect are același set de elemente ca în proiect. Puteți crea o ierarhie de sarcini, puteți asocia roluri la sarcină, puteți defini atribute de planificare, puteți stabili dependențe și puteți vizualiza toate datele din Gantt. Structura de defalcare a lucrărilor din șabloanele de proiect acceptă și moduri de activitate pentru fiecare sarcină. Nu există nicio diferență între un șablon de proiect și un proiect atunci când creați un program de lucru.  
  
- **Estimările de proiect**: estimările de proiect din șabloane funcționează la fel ca în proiecte, cu excepția faptului că listele de prețuri pentru costurile și prețurile de vânzare implicite sunt întotdeauna costurile implicit și listele de prețuri de vânzare definite în parametrii [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Restul funcționalității este la fel ca într-un proiect.  
  
- **Formarea echipei de proiect**: atunci când se formează o echipă de proiect pentru un șablon de proiect, nu se poate rezerva o resursă denumită într-un șablon. Puteți utiliza opțiunea **Generați echipa de proiect** în structura detaliată a proiectului pentru a genera un set de resurse generice. De asemenea, puteți specifica abilitățile și expertizele necesare pentru resursele generice. Nu puteți substitui o resursă generică cu o resursă ce se poate rezerva din șabloanele de proiect.  

## <a name="create-a-project-template-from-an-existing-project"></a>Creați un șablon de proiect dintr-un proiect existent
Puteți crea un șablon de proiect dintr-un proiect în următoarele moduri:

- **Structura de defalcare a muncii** : O structură de defalcare a lucrării într-un șablon care este derivat dintr-un proiect va copia toate sarcinile și dependențele. Misiunile care sunt create se vor baza pe membrii echipei generice care sunt adăugați echipei de proiect atunci când este creat șablonul de proiect.
- **Estimări de proiect** : Când un șablon de proiect este creat dintr-un proiect existent, estimările din proiectul sursă sunt copiate în șablonul de proiect.
- **Membrii echipei de proiect** : Când un șablon este creat dintr-un proiect existent, toți membrii echipei numiți sunt înlocuiți cu resursa generică a organizației. Toate numele posturilor și rolurile sunt păstrate.

## <a name="create-a-project-from-a-template"></a>Creați un proiect dintr-un șablon  
 Puteți crea un proiect dintr-un șablon în următoarele moduri:  
  
-   La crearea unui proiect din ofertă, puteți alege un șablon de proiect în formularul de creare rapidă proiect.  
  
-   Atunci când creați un proiect făcând clic pe **Proiect nou**, formularul de proiect se afișează înainte de a salva înregistrarea. De aici, puteți face clic pe câmpul **Alegeți un șablon** pentru a alege din lista de șabloane de proiect predefinite din organizația dvs.  
  
-   Faceți clic pe **Creați proiectul dintr-un șablon** pe pagina **Șablon de proiect** pentru a crea un proiect din șablon.  
  
## <a name="copying-components-of-a-template-to-a-project"></a>Copierea componentelor unui șablon într-un proiect  
 Când copiați componentele unui șablon într-un proiect, există câteva lucruri pe care trebuie să le știți.  
  
 **Copierea unei structuri detaliate a proiectului**: Când copiați structura detaliată a proiectului dintr-un șablon de proiect, dacă proiectul are un alt calendar de proiect decât șablonul, orele de lucru din calendarul proiectului se vor aplica la programul activităților. Acest lucru ajustează planificarea la calendarul proiectului. În mod similar, prima activitate din structura detaliată a proiectului ia data de începere a proiectului, astfel încât restul planificării ierarhice a activităților se actualizează pe baza duratei și a dependențelor specificate în structura de detaliere a proiectului.  
  
 **Copierea estimărilor de proiect**: Când copiați peste liniile de estimare a proiectului, listele de prețuri sunt actualizate pe baza unității deținătoare a proiectului pentru lista de prețuri de cost și lista de clienți pentru prețul de vânzare. Costul unitar și prețurile de vânzare sunt determinate din aceste liste de prețuri pentru proiectele asociate cu o entitate de vânzări.  
  
 **Copierea unei echipe de proiect**: Când copiați echipa proiectului din șablon într-un proiect, resursele generice sunt copiate, împreună cu abilitățile și expertizele definite în șablon. Atribuirile de resurse generice sunt păstrate ca în șablonul de proiect.  
  
### <a name="see-also"></a>Consultați și  
 [Ghidul Managerului de proiect](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
