---
title: Noutăți sau modificări în Project Operations, mai 2021, pentru scenarii bazate pe stocuri/producție
description: Acest subiect oferă informații despre actualizările de calitate disponibile în versiunea Project Operations din iulie 2021 pentru scenarii bazate pe stocuri/producție.
author: andchoi
ms.date: 07/01/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: andchoi
ms.openlocfilehash: db5bb27650d65bb68f45f95cb2562f4b773ddcea
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8597077"
---
# <a name="whats-new-or-changed-in-project-operations-july-2021-for-stockedproduction-based-scenarios"></a>Noutăți sau modificări în Project Operations, mai 2021, pentru scenarii bazate pe stocuri/producție

_**Se aplică la:** Project Operations pentru scenariile bazate pe stocuri/producție_

Acest subiect se aplică următoarelor componente și versiuni Dynamics 365 Project Operations:

- Management de proiect și contabilitate în mediul Dynamics 365 Finance versiunea 10.0.20
 
### <a name="quality-updates"></a>Actualizări de calitate
                                                                                                                                                                                  
| Zonă de caracteristici                      | Număr de referință| Actualizare de calitate                                                                                                                                                                          |
|-----------------------------------|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Management de proiect și contabilitate | [485394](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485394) | Înregistrările de angajament de cost dintr-o cerere de achiziție sunt șterse de îndată ce comanda de achiziție este eliberată de la problema legată de cererea de achiziție.                                                                           |
| Management de proiect și contabilitate | [529602](https://fix.lcs.dynamics.com/Issue/Details/?bugId=529602) | Validarea bugetului are loc de două ori la o cerere de achiziție. Această dublare înseamnă că solicitarea nu poate fi închisă și nu se creează comanda de achiziție corespunzătoare.                                                                                                                        |
| Management de proiect și contabilitate | [539439](https://fix.lcs.dynamics.com/Issue/Details/?bugId=539439) | Regula de facturare **Procent de facturare** nu a putut fi finalizată din cauza unei probleme de rotunjire.                                                                              |
| Management de proiect și contabilitate | [540023](https://fix.lcs.dynamics.com/Issue/Details/?bugId=540023) | Când ajustați tranzacția și procentul are zecimale, costul și prețul de vânzare nu sunt ajustate corect.                                      |
| Management de proiect și contabilitate | [540927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=540927) | Exploratorul sursei de contabilitate afișează ore pentru o singură linie de orar pentru linii multiple de orar cu activități diferite.                                      |
| Management de proiect și contabilitate | [541471](https://fix.lcs.dynamics.com/Issue/Details/?bugId=541471) | Vizualizările salvate și personalizarea detaliilor liniei din orar determină sistemul să deschidă întotdeauna detaliile pentru primul orar din listă atunci când încearcă să deschidă un orar.  |
| Management de proiect și contabilitate | [548677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548677) | Nodul rădăcină al proiectului dispare și înregistrările structurii detaliate a proiectului sunt șterse după import.                                                                                             |
| Management de proiect și contabilitate | [548999](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548999) | Când articolele sunt primite și emise parțial din cerința articolului, sistemul actualizează soldul greșit al consumului bugetar. |
| Management de proiect și contabilitate | [550959](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550959) | Comenzile de achiziție cu rezerve de proiecte nu afișează corect totalurile în panoul **Totaluri** sau în grila **Factură în așteptare**.                                                                  |
| Management de proiect și contabilitate | [554593](https://fix.lcs.dynamics.com/Issue/Details/?bugId=554593) | La închiderea inventarului, ajustările costurilor articolului de proiect sunt înregistrate în contul de sold în loc de contul de profit și pierdere.                                                            |
| Management de proiect și contabilitate | [557394](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557394) | Un voucher de tranzacție postat pentru un proiect și un voucher estimativ utilizează USD ca monedă contabilă, dar suma indică care ar fi echivalentul în CAD.              |
| Management de proiect și contabilitate | [560140](https://fix.lcs.dynamics.com/Issue/Details/?bugId=560140) | Costurile angajate cu o cerință de articol și o comandă de achiziție sunt greșite în procesul de facturare a comenzii de achiziție, cu chitanța produsului și facturarea parțială.       |
| Management de proiect și contabilitate | [560567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=560567) | Ajustarea proiectului nu actualizează corect valoarea vânzărilor cu costuri indirecte.                                                                                    |
| Management de proiect și contabilitate | [561137](https://fix.lcs.dynamics.com/Issue/Details/?bugId=561137) | Tabelul **Orar** nu conține o relație definită cu vizualizarea **Lucrător/Resursă**.                                                                                   |
| Management de proiect și contabilitate | [563330](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563330) | Imposibil de completat câmpul **Numărul activității** când îl selectați din meniul derulant pentru un orar între companii.                                                                 |
| Management de proiect și contabilitate | [563840](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563840) | Nu puteți adăuga un câmp personalizat **Scop** sau **Descrierea activității** la următoarele pagini: **Tranzacție de proiect postată**, **Crearea propunerii de factură** sau **Propunere de factură**.  |
| Management de proiect și contabilitate | [566348](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566348) | Controlul greșit al datei de livrare este furnizat atunci când creați cerințele articolului utilizând gestionarea datelor (**ProjSalesItemRequirementEntity**).                                              |
| Management de proiect și contabilitate | [566544](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566544) | Când selectați un ID de contract de proiect în Finanțe, mediul integrat Project Operations deschide pagina pentru a crea o nouă înregistrare în loc să deschidă contractul de proiect existent.                                                                                                                 |
| Management de proiect și contabilitate | [567300](https://fix.lcs.dynamics.com/Issue/Details/?bugId=567300) |  Eticheta „@SYS4083080” („Nu se poate găsi o înregistrare unică a lucrătorului corespunzătoare valorilor introduse”) nu este tradusă în daneză.                                |
| Management de proiect și contabilitate | [569901](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569901) | Câmpul **Grup de taxe pe vânzări de articole** nu poate fi modificat într-o propunere de factură.                                                                               |
| Management de proiect și contabilitate | [557049](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557049) | Costul angajat este supraevaluat cu impozite nedeductibile.                                                                                                    |
| Management de proiect și contabilitate | [565080](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565080) | Postarea unui orar între companii cu mai multe proiecte și dimensiuni financiare diferite generează valori neașteptate în registrul general.                             |
| Management de proiect și contabilitate | [567962](https://fix.lcs.dynamics.com/Issue/Details/?bugId=567962) | Liniile de propunere de factură sunt duplicate din cauza mai multor instanțe ale procesului periodic **Import din etapă** care rulează în același timp.                                      |
| Management de proiect și contabilitate | [571339](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571339) | Există o eroare la afișarea propunerii de factură a notei de credit, astfel încât tranzacțiile de pe voucher nu echivalează.    |
| Management de proiect și contabilitate | [573567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573567) | Costurile angajate ale proiectului devin incorecte după eliberarea facturilor în așteptare.                                                                             |
| Management de proiect și contabilitate | [573886](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573886) | Nu se poate crea o notă de credit pentru o comandă de vânzare a proiectului atunci când taxa este într-o monedă diferită de moneda companiei.                                      |
| Management de proiect și contabilitate | [582329](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582329) | Când ștergeți un contract, se șterge și adresa asociată clientului.                                                                                     |
| Management de proiect și contabilitate | [585811](https://fix.lcs.dynamics.com/Issue/Details/?bugId=585811) | O propunere de factură care rezultă dintr-o corecție negativă a tranzacției în timp nu poate fi postată.                                                                    |
| Deplasări și cheltuieli                  | [532075](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532075) | Impozitul este calculat diferit în rapoartele de cheltuieli.                                                                                                                  |
| Deplasări și cheltuieli                  | [546450](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546450) | Actualizarea de versiune **DB72_Expense.updateTrvExpTransProjTransId()** nu permite **trvExpTrans.ReferenceDataAreaId** să creeze noua secvență numerică.                    |
| Deplasări și cheltuieli                  | [568805](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568805) | Suma înregistrată nu apare în câmpul obligatoriu.                                                                                                             |
| Deplasări și cheltuieli                  | [568831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568831) | Îmbunătățiri în performanța atașării unei cheltuieli la raportul de cheltuieli utilizând interfața cu utilizatorul Cheltuieli reinventate.                                                            |
| Deplasări și cheltuieli                  | [570790](https://fix.lcs.dynamics.com/Issue/Details/?bugId=570790) | Puteți șterge rapoartele de cheltuieli postate.                                                                                           |
| Deplasări și cheltuieli                  | [571317](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571317) | Mesajul privind politica de cheltuieli este afișat de mai multe ori.                                                                                                       |
| Deplasări și cheltuieli                  | [573969](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573969) | Câmpul **Metodă de plată** este inclus în panoul **Cheltuială nouă**.                                                                                                      |
| Deplasări și cheltuieli                  | [523557](https://fix.lcs.dynamics.com/Issue/Details/?bugId=523557) | Instrumentul **Resetați starea documentului de cheltuieli** ar trebui să reseteze starea raportului de cheltuieli la starea **Proiect** dacă fluxul de lucru nu a fost găsit. 

### <a name="regulatory-updates"></a>Actualizări de reglementare
Pentru informații despre actualizările de reglementare pentru aplicațiile Finance and Operations, consultați [Actualizări de reglementare](/dynamics365/finance/localizations/regulatory-updates). De asemenea, vă puteți conecta la Lifecycle Services (LCS) și puteți vizualiza actualizările de reglementare planificate folosind instrumentul de căutare a problemelor. Căutarea problemelor vă permite să căutați în funcție de țară, tipul de funcție și eliberare.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
