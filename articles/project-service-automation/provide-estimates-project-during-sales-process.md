---
title: Furnizați estimări de lucru pentru un proiect în timpul procesului de vânzare
description: Cum să furnizați estimări de lucru pentru un proiect în timpul procesului de vânzări în Project Service
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 8e6fbba8-2908-4555-9470-43c37e66efea
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8edb91010dd1227bc7947b59664d08430c219638
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754803"
---
# <a name="provide-work-estimates-for-a-project-during-the-sales-process-project-service"></a>Furnizați estimări de lucru pentru un proiect în timpul procesului de vânzare (Project Service)

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
 [Ghidul Managerului de proiect](../project-service/project-manager-guide.md)
