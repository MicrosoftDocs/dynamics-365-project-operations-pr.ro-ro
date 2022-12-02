---
title: Procese vânzări
description: Acest articol oferă informații despre procesele de vânzări de bază.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: rumant
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
ms.openlocfilehash: 18a5ca0592dfefb611094685087351149a0f5e3b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923525"
---
# <a name="sales-processes"></a>Procese vânzări

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Procesele de vânzări care sunt utilizate într-o organizație bazată pe proiecte diferă de procesele de vânzări care sunt utilizate într-o organizație bazată pe produse. Această diferență apare deoarece ciclurile de vânzări pentru organizațiile bazate pe proiecte sunt mai lungi și necesită tehnici de estimare particularizate pentru a analiza și a crea oferte pentru fiecare tranzacție. Dynamics 365 Project Service Automation utilizează o parte din aceeași funcționalitate care este utilizată în procesul de vânzări pentru Dynamics 365 Sales. Iată câteva exemple:

- O entitate Client potențial este utilizată pentru a urmări procesul de vânzări.
- Clienții potențiali care se califică sunt urmăriți ca oportunități. Procesul de vânzări poate începe, de asemenea, cu oportunitatea.
- Toate artefactele corelate pentru o oportunitate sunt accesate. Aceste artefacte includ echipa de vânzări, participanții direct interesați, probabilitatea, evaluarea, etapele vânzărilor și procesele de afaceri.
- Mai multe oferte sunt create pentru o oportunitate.
- O ofertă este marcată ca **Închisă drept câștigată** pentru a crea o comandă de vânzări. În PSA, comanda de vânzări este particularizată și se numește contract de proiect.

Următoarea ilustrație arată un proces tipic de vânzări într-o organizație bazată pe proiecte.

> ![Procesul de vânzări într-o organizație bazată pe proiecte.](media/basic-guide-1.png)

## <a name="estimating-a-sale"></a>Estimarea unei vânzări
Valoarea unei vânzări poate fi estimată pe baza proiectelor care au fost livrate anterior și a complexității proiectelor. Pentru proiectele care implică extensii la proiecte anterioare sau proiectele în care expertiza furnizorului este mare și sunt utilizate șabloane de lucru bine cunoscute, puteți utiliza un proces de estimare mai simplu. Proiectele mai complexe au de obicei un proces de achiziție mai lung. Prin urmare, există mai multe etape în procesul de estimare a vânzărilor. La începutul procesului, echipa de vânzări utilizează contribuția administratorilor de cont și a experților în materie (EM) pentru a începe să creeze o estimare la nivel înalt pentru fiecare componentă distinctă a lucrărilor care este ofertată. Aceste componente ale lucrărilor sunt reprezentate prin linii de ofertă. 

Aveți posibilitatea să creați o estimare la nivel înalt a ofertei. În cele din urmă, această estimare la nivel înalt va fi înlocuită cu o estimare mai detaliată care se bazează pe un plan de proiect pe care îl creați utilizând șabloanele de proiect standardizate. Aceste șabloane vă ajută să construiți o planificare și să determinați valorile monetare pe ofertă și pe componentele sale (linii de ofertă). 

Aveți posibilitatea să creați mai multe oferte pentru un proiect și să le grupați sub un singur tip de entitate oportunitate. În cele din urmă, una dintre aceste oferte este marcată ca **Închisă drept câștigată** și se creează un contract de proiect sau o specificație de lucru (SL). Un contract de proiect deține valoarea contractată pentru fiecare componentă (linie de contract) care este acceptată de client pentru livrare. O SL este de obicei creată ca document Microsoft Word. Toate facturile trimise clientului pe parcursul livrării proiectului fac referire la contractul de proiect sau la SL.

De asemenea, aveți posibilitatea să creați oferte alternative sub un tip de entitate oportunitate sau să configurați sistemul astfel încât să se creeze un contract de proiect atunci când se câștigă o ofertă. În acest caz, aveți posibilitatea să atașați un document Word care reprezintă SL la înregistrarea de contract de proiect.

![Închiderea unei oferte pentru a crea un contract de proiect.](media/basic-guide-2.png)

## <a name="configuring-the-sales-process"></a>Configurarea procesului de vânzări
Aveți posibilitatea să utilizați fluxurile de business (FB) în Microsoft Dynamics 365 pentru a configura procesul de vânzări. FB-urile oferă personalului dvs. de vânzări o interfață vizuală ghidată pe care acesta o poate folosi pentru a face tranzacțiile să avanseze prin etapele care sunt tipice pentru compania dvs.

De exemplu, compania dvs. poate avea următoarele șase etape în procesul de vânzări:

1. Calificare
2. Estimat
3. Recenzie internă
4. Contract
5. Livrare
6. Închidere

Aceste șase etape sunt reprezentate de ghilimelele unghiulare (\>) pe care le selectați pentru a extinde în fiecare oportunitate tipul de entitate pe care îl creați.

![Configurarea proceselor comerciale în Dynamics 365.](media/basic-guide-3.png)
 
Organizația dvs. poate utiliza entități diferite pentru a reprezenta aceeași tranzacție, pe măsură ce aceasta evoluează. La începutul procesului de vânzări, o tranzacție este reprezentată de entitatea Oportunitate. Pe măsură ce trece timpul și apar mai multe detalii, este posibil să utilizați estimări de nivel înalt pentru a crea una sau mai multe oferte. Dacă una dintre aceste oferte este revizuită de către participanții direct interesați interni și ai clienților, entitatea Ofertă reprezintă tranzacția. După ce clientul acceptă oferta, un contract de proiect sau o SL reprezintă tranzacția. Pentru a sprijini acest comportament, FB-urile sunt structurate astfel încât fiecare etapă din proces este legată la un tabel de baze de date diferit.

Etapa **Calificare** din procesul de vânzări poate fi susținută de o entitate Oportunitate. Etapele **Estimare** și **Recenzie internă** pot fi susținute de o entitate Ofertă. Etapele **Contract**, **Livrare** și **Închidere** pot fi susținute de o entitate Contract de proiect.

Pe măsură ce faceți tranzacțiile să avanseze prin etape, vi se solicită să creați înregistrarea de entitate corespunzătoare pentru a vă ajuta și ghida prin proces. Etapele pot fi condiționate. De exemplu, dacă aveți nevoie de o revizuire internă a unei oferte numai dacă oferta utilizează o listă de prețuri particularizată, aveți posibilitatea să configurați această condiție în stadiul corespunzător al procesului de afaceri. Etapa **Recenzie internă** este apoi afișată numai pentru ofertele care utilizează o listă de prețuri personalizată. Pentru toate celelalte tranzacții și oferte, etapa **Estimare** este urmată de etapa **Contract**.

> [!NOTE]
> PSA are anumite pagini pentru entitățile Oportunitate, Ofertă, Comandă și Factură. Trebuie să creați oportunități de servicii de proiecte, oferte, comenzi și facturi utilizând paginile de informații ale proiectului pentru aceste entități. Dacă utilizați o altă pagină pentru a crea o înregistrare, nu veți putea deschide înregistrarea din pagina **Informații proiect**. Dacă doriți să deschideți o înregistrare din pagina **Informații proiect**, trebuie să ștergeți înregistrarea și să o recreați utilizând pagina **Informații proiect**. În pagina **Informații proiect**, logica de business pentru fiecare dintre aceste tipuri de entități asigură faptul că câmpul **Tip** al înregistrării este setat corect și toate conceptele obligatorii sunt inițializate corect.

> ![Informații despre proiect pentru o nouă comandă.](media/basic-guide-4.png)
 
## <a name="differences-between-project-service-automation-and-sales"></a>Diferențele dintre Project Service Automation și Sales
Deși procesul de vânzări în PSA utilizează capacitățile de bază ale procesului de vânzări din Sales, acesta prezintă unele diferențe cheie din cauza variațiilor în practicile de afaceri ale organizațiilor bazate pe proiecte. Iată câteva exemple:

- **Oferte proiect** – în Project Service Automation, o ofertă este închisă după ce un contract de proiect este creat dintr-o ofertă. În Sales, puteți să păstrați o ofertă deschisă după ce ați câștigat-o. Motivul pentru această diferență este că o potrivire între o ofertă și un contract de proiect este mai bună pentru organizațiile bazate pe proiecte. 
- **Activarea și revizuirile** – în PSA, activarea și revizuirile nu sunt acceptate pentru ofertele de proiect. În Sales, o ofertă poate fi blocată pentru a preveni editările suplimentare.
- **Închiderea unei oferte ca pierdută sau câștigată** – în PSA, când o ofertă de proiect este închisă ca câștigată sau pierdută, oportunitatea rămâne deschisă. Toate celelalte oferte din oportunitate sunt închise ca pierdute. În Sales, când o ofertă este închisă ca câștigată sau pierdută, utilizatorului i se solicită să ia o măsură cu privire la oportunitate. În funcție de contribuția utilizatorului, oportunitatea de bază poate fi închisă sau lăsată deschisă.

## <a name="tracking-revisions-to-quotes-and-project-plans-in-the-sales-cycle"></a>Urmărirea revizuirilor la oferte și planuri de proiect în ciclul de vânzări
În PSA, nu puteți urmări revizuirile care sunt făcute la o ofertă. În schimb, trebuie să marcați oferta existentă ca **Închisă drept pierdută** și apoi să creați o ofertă nouă. Aveți posibilitatea să copiați o ofertă sau să clonați o ofertă bazată pe proiect utilizând PSA.

## <a name="tracking-comments-and-approvals-of-quotes-and-project-contracts"></a>Urmărirea comentariilor și aprobărilor de oferte și contracte de proiect
Puteți gestiona revizuirea și aprobarea ofertelor și a contractelor de proiect utilizând peretele de înregistrări și postările. Organizația dvs. poate crea fluxuri de lucru și inserturi particularizate pentru a atribui, redirecționa, escalada și gestiona notificările de elemente de lucru de revizuire și aprobare.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
