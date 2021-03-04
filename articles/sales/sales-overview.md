---
title: Prezentare generală a procesului de vânzări
description: Acest subiect oferă informații despre procese de vânzări de bază.
author: rumant
manager: Annbe
ms.date: 10/29/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5da29d2959a6e49defa185630f45d280dba283c4
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177616"
---
# <a name="sales-process-overview"></a>Prezentare generală a procesului de vânzări

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Procesele de vânzări care sunt utilizate într-o organizație bazată pe proiecte diferă de procesele de vânzări care sunt utilizate într-o organizație bazată pe produse. Aceasta deoarece ciclurile de vânzări pentru organizațiile bazate pe proiecte sunt mai lungi și necesită tehnici de estimare particularizate pentru a analiza și a crea oferte pentru fiecare tranzacție. Dynamics 365 Project Operations utilizează una dintre următoarele funcționalități care este utilizată într-un proces de vânări:

- O înregistrare de client potențial este utilizată pentru a urmări procesul de vânzări.
- Clienții potențiali care se califică sunt urmăriți ca oportunități.
- Toate artefactele corelate pentru o oportunitate sunt accesibile. Aceste artefacte includ echipa de vânzări, participanții direct interesați, probabilitatea, evaluarea, etapele vânzărilor și procesele de afaceri.
- Mai multe oferte sunt create pentru o oportunitate.
- Starea este dată de o ofertă, **Închisă drept câștigată** pentru a crea o comandă de vânzare. În Project Operations, comanda de vânzări este particularizată și se numește contract de proiect.

## <a name="estimate-a-sale"></a>Estimați o vânzare
Valoarea unei vânzări poate fi estimată pe baza proiectelor care au fost livrate anterior și a complexității proiectelor. Pentru proiectele care implică extensii la proiecte anterioare sau proiectele în care expertiza furnizorului este mare și sunt utilizate șabloane de lucru bine cunoscute, puteți utiliza un proces de estimare mai simplu. Proiectele mai complexe au de obicei un proces de achiziție mai lung. Prin urmare, există mai multe etape în procesul de estimare a vânzărilor. La începutul procesului, echipa de vânzări utilizează contribuția administratorilor de cont și a experților în materie (EM) pentru a crea o estimare la nivel înalt pentru fiecare componentă distinctă a lucrărilor care este ofertată. Aceste componente ale lucrărilor sunt reprezentate prin linii de ofertă. 

Aveți posibilitatea să creați o estimare la nivel înalt a ofertei. În cele din urmă, această estimare la nivel înalt va fi înlocuită cu o estimare mai detaliată care se bazează pe un plan de proiect pe care îl creați utilizând șabloanele de proiect standardizate. Aceste șabloane vă ajută să construiți o planificare și să determinați valorile monetare pe ofertă și pe componentele sale (linii de ofertă). 

Aveți posibilitatea să creați mai multe oferte pentru un proiect și să le grupați sub un singur tip de înregistrare de oportunitate. În cele din urmă, una dintre oferte este marcată ca **Închisă drept câștigată** și se creează un contract de proiect sau o specificație de lucru (SL). Un contract de proiect deține valoarea contractată pentru fiecare componentă (linie de contract) care este acceptată de client pentru livrare. O SL este de obicei creată ca document Microsoft Word. Toate facturile trimise clientului pe parcursul livrării proiectului fac referire la contractul de proiect sau la SL.

De asemenea, aveți posibilitatea să creați oferte alternative sub un tip de înregistrare de oportunitate sau să configurați sistemul astfel încât să se creeze un contract de proiect atunci când se câștigă o ofertă. În acest caz, aveți posibilitatea să atașați un document Word care reprezintă SL la înregistrarea de contract de proiect.

## <a name="configure-the-sales-process"></a>Configurați procesul de vânzări
Aveți posibilitatea să utilizați fluxurile de business pentru a configura procesul de vânzări. Aceste fluxuri oferă o interfață vizuală ghidată pentru a avansa ofertele prin etapele procesului de vânzare.

De exemplu, compania dvs. poate avea următoarele șase etape în procesul de vânzări:

1. Calificare
2. Estimată
3. Recenzie internă
4. Contract
5. Livrare
6. Închideți
 
Organizația dvs. poate utiliza entități diferite pentru a reprezenta aceeași tranzacție, pe măsură ce aceasta evoluează. La începutul procesului de vânzări, o tranzacție este reprezentată de entitatea Oportunitate. Pe măsură ce trece timpul și apar mai multe detalii, este posibil să utilizați estimări de nivel înalt pentru a crea una sau mai multe oferte. Dacă una dintre aceste oferte este revizuită de către participanții direct interesați interni și ai clienților, entitatea Ofertă reprezintă tranzacția. După ce clientul acceptă oferta, un contract de proiect sau o SL reprezintă tranzacția. Pentru a sprijini acest comportament, FB-urile sunt structurate astfel încât fiecare etapă din proces este legată la un tabel de baze de date diferit.

Etapa **Calificare** din procesul de vânzări poate fi susținută de o entitate Oportunitate. Etapele **Estimare** și **Recenzie internă** pot fi susținute de o entitate Ofertă. Etapele **Contract**, **Livrare** și **Închidere** pot fi susținute de o entitate Contract de proiect.

Pe măsură ce faceți tranzacțiile să avanseze prin etape, vi se solicită să creați înregistrarea de entitate corespunzătoare pentru a vă ajuta și ghida prin proces. Etapele pot fi condiționate. De exemplu, dacă aveți nevoie de o revizuire internă a unei oferte numai dacă oferta utilizează o listă de prețuri particularizată, aveți posibilitatea să configurați această condiție în stadiul corespunzător al procesului de afaceri. Etapa **Recenzie internă** este apoi afișată numai pentru ofertele care utilizează o listă de prețuri personalizată. Pentru toate celelalte tranzacții și oferte, etapa **Estimare** este urmată de etapa **Contract**.

> [!NOTE]
> Project Operations conțin pagini specifice pentru înregistrările entității Oportunitate, Ofertă, Comandă și Factură. Trebuie să creați aceste înregistrări folosind paginile cu informații despre proiect pentru aceste entități. În caz contrar, nu veți putea deschide înregistrările din pagina **Informații despre proiect**. Dacă doriți să deschideți o înregistrare din pagina **Informații despre proiect**, trebuie să ștergeți înregistrarea și să o recreați folosind pagina **Informații despre proiect** în care logica de afaceri pentru fiecare dintre aceste tipuri de entități asigură faptul că câmpul **Tip** al înregistrării este setat corect și toate conceptele obligatorii sunt inițializate corespunzător.


## <a name="track-revisions-to-quotes-and-project-plans-in-the-sales-cycle"></a>Urmăriți revizuirile la oferte și planuri de proiect în ciclul de vânzări
În Project Operations nu puteți urmări revizuirile care sunt făcute la o ofertă. În schimb, trebuie să marcați oferta existentă ca **Închisă drept pierdută** și apoi să creați o ofertă nouă. Aveți posibilitatea să copiați o ofertă sau să clonați o ofertă bazată pe proiect.

## <a name="track-comments-and-approvals-of-quotes-and-project-contracts"></a>Urmăriți comentariile și aprobările de oferte și contracte de proiect
Puteți gestiona revizuirea și aprobarea ofertelor și a contractelor de proiect utilizând peretele de înregistrări și postările. Organizația dvs. poate crea fluxuri de lucru și inserturi particularizate pentru a atribui, redirecționa, escalada și gestiona notificările de elemente de lucru de revizuire și aprobare.


[!INCLUDE[footer-include](../includes/footer-banner.md)]