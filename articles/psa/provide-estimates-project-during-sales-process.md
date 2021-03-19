---
title: Furnizați estimări de lucru pentru un proiect în timpul procesului de vânzare
description: Cum să furnizați estimări de lucru pentru un proiect în timpul procesului de vânzări în Project Service
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 49ea8327ae34a69eba1585f1b1b4e557fd4eac93
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5283563"
---
# <a name="provide-work-estimates-for-a-project-during-the-sales-process-project-service"></a>Furnizați estimări de lucru pentru un proiect în timpul procesului de vânzare (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

În timpul procesului de vânzare, puteți efectua estimări de vânzări de la zero cu linii de ofertă. Capacitățile de servicii de proiecte [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] din [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] oferă o modalitate mai științifică și mai deterministă de a realiza estimări de vânzare prin defalcarea elementelor de lucru și asocierea de atribute relevante care contribuie la estimările privind proiectul în structura detaliată a proiectului.  
  
 Odată ce ați câștigat vânzarea, puteți utiliza structura detaliată a proiectului în planul de proiect, rafinând-o după cum este necesar pentru o finalizare cu succes a proiectului.  
  
## <a name="link-a-project-to-a-quote-line"></a>Legați un proiect la o linie de ofertă  
 Atunci când creați o linie de ofertă pe baza proiectului, puteți să creați un proiect nou din linia de ofertă. Puteți utiliza apoi șabloane de proiect, care sunt fie planuri de proiect standard preconfigurate și estimări financiare comune organizației dumneavoastră, fie o copie a unui plan de proiect și estimări de la un proiect de trecut. Atunci când creați un proiect, alegerea unui șablon de proiect oferă o bază pentru a rafina planul de proiect, estimări și cerințe de rol. Prin crearea proiectului din ofertă, proiectul este asociat automat cu linia de ofertă.  
  
## <a name="project-estimate-components"></a>Componente estimării de proiect  
 Structură detaliată a proiectului dintr-un proiect oferă o modalitate de a împărți proiectul în activități, de a menține o ierarhie de activități și de a atribui o estimare a efortului necesar pentru a finaliza fiecare activitate. De asemenea, puteți asocia roluri la o activitate, pentru a indica o estimare a tipului de resursă necesar pentru a finaliza o activitate și un program.  
  
 Structură detaliată a proiectului vă ajută să determinați efortul de lucru și estimările de planificare. În mod implicit, proiectul utilizează liste de prețuri implicite pe care le-ați definit anterior. Costurile și prețurile de vânzări definite în listele de prețuri vă ajută să determinați estimările financiare pentru componentele de lucru ale proiectului.  
  
 Dacă proiectul dumneavoastră este asociat cu o ofertă, iar oferta are o altă listă de prețuri decât cea implicită, lista de prețuri a ofertei este folosită pentru estimări financiare.  
  
## <a name="import-estimates-from-a-project-into-a-quote"></a>Importați estimările dintr-un proiect într-o ofertă  
 După ce aveți estimările de proiect în proiect, aveți posibilitatea să importați aceste estimări în linia de ofertă:  
  
-   În **Detalii linie de ofertă**, faceți clic pe **Import de la estimări**. 

-   Selectați dacă să importați estimările proiectului rezumate după tipul tranzacției, rol sau nivel de nod de structură detaliată a proiectului.  
  
### <a name="see-also"></a>Consultați și  
 [Ghidul Managerului de proiect](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]