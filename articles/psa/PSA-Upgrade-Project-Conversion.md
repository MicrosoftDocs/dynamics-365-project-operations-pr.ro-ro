---
title: Procesul de conversie a programării proiectelor de la Project Service Automation în Project Operations
description: Acest articol oferă o prezentare generală a modificărilor caracteristicilor pentru Microsoft Dynamics 365 Project Service Automation la Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/07/2022
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
ms.openlocfilehash: 84a40fcc9a8561c4ade0be175b08f701f3196508
ms.sourcegitcommit: 28004d38800782540fa5642d41f8fe0f6e2d9fa5
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/08/2022
ms.locfileid: "9642584"
---
# <a name="project-service-automation-to-project-operations-project-scheduling-conversion-process"></a>Procesul de conversie a programării proiectelor de la Project Service Automation în Project Operations

După ce un proiect a fost actualizat cu succes de la Microsoft Dynamics 365 Project Service Automation 3.X la Dynamics 365 Project Operations Lite, nu este posibilă editarea sarcinilor de proiect în structura de defalcare a activității grilei de activități (WBS). Clienții vor putea examina WBS-urile în grila de urmărire unde au fost adăugate câmpuri noi pentru a furniza toate detaliile legate de sarcină. Pentru proiectele în care sunt necesare modificări ale WBS, puteți converti în mod selectiv proiectele eligibile în noul Proiect pentru experiența de programare web.

## <a name="project-conversion-process"></a>Procesul de conversie a proiectului

Pentru a converti un proiect, urmați acești pași.

1. Deschideți pagina principală a proiectului și selectați **Convertit** în panoul de acțiuni.
1. În caseta de mesaj de confirmare, selectați **O.K** pentru a începe conversia proiectului. Au loc următoarele acțiuni:

    1. O bară de mesaje care apare pe pagina principală a proiectului afirmă: „Programul proiectului este în curs de conversie. Nu puteți face modificări în proiect până la finalizarea conversiei.”
    1. Sunteți redirecționat către lista de proiecte.

    După finalizarea conversiei proiectului, au loc următoarele acțiuni:

    1. Managerul de proiect desemnat primește o notificare în partea dreaptă a aplicației.
    1. Bara de mesaje care afirmă că conversia este în curs este eliminată.
    1. The **Programa** fila arată noua experiență de programare cu Project pentru web. Orice utilizator care are licențele și rolurile de securitate adecvate poate edita WBS.
    1. The **Motor de programare** câmpul este actualizat la **Proiect pentru web**.
    1. The **Convertit** butonul este eliminat din panoul de acțiuni.

> [!IMPORTANT]
> Conversia în bloc a proiectelor nu este permisă. Orice încercare de a actualiza un volum mare de proiecte în același timp va fi redusă. Această limitare ajută la asigurarea unei performanțe ridicate pentru toți clienții.

## <a name="manual-tasks-vs-automatic-tasks"></a>Sarcini manuale versus sarcini automate

Când un mediu este actualizat de la Project Service Automation la Project Operations, toate sarcinile din WBS sunt considerate programate automat. Conceptul de sarcini programate manual nu este disponibil în Project pentru web. Cu toate acestea, puteți defini comportamentul de programare preferat pentru proiectele dvs. utilizând [modul de programare](/project-management/scheduling-modes.md) setarea când creați proiecte noi.

## <a name="restricted-operations-for-pre-conversion-projects"></a>Operațiuni restricționate pentru proiectele de pre-conversie

Această secțiune prezintă diferențele funcționale la care vă puteți aștepta atunci când proiectele nu au fost convertite.

### <a name="copy-project"></a>Copiați proiectul

The **Copie** funcționarea este acceptată numai pe proiectele convertite. Proiectele actualizate nu pot fi copiate înainte de conversie.

### <a name="move-project"></a>Mutați proiectul

O modificare a datei de începere a unui proiect nu va muta proporțional începutul sarcinilor decât dacă proiectul a fost convertit.

## <a name="frequently-asked-questions"></a>Întrebări frecvente

### <a name="what-are-the-differences-between-converted-projects-and-new-projects-that-are-created-after-the-upgrade-has-been-completed"></a>Care sunt diferențele dintre proiectele convertite și proiectele noi care sunt create după finalizarea upgrade-ului?

Pentru proiectele care sunt convertite după ce mediul a fost actualizat, va fi setat un steag care indică programului să respecte numai calendarul proiectului. Acest comportament se potrivește cu comportamentul din Project Service Automation. Cu toate acestea, marcajul nu va fi setat pentru proiectele noi care sunt create după actualizare. Prin urmare, programul va respecta orele de lucru ale resurselor atunci când acestea sunt alocate unei sarcini.

### <a name="what-should-i-do-if-my-project-fails-to-be-converted"></a>Ce ar trebui să fac dacă proiectul meu nu reușește să fie convertit?

Dacă proiectul dvs. nu reușește să fie convertit, primul pas este să examinați jurnalele de erori pentru a identifica orice probleme comune legate de WBS. Dacă jurnalele nu indică o eroare specifică asupra căreia puteți lua măsuri, contactați serviciul de asistență pentru clienți, astfel încât cazul dvs. să poată fi examinat în continuare.

### <a name="how-are-business-closures-handled-in-project-for-the-web"></a>Cum sunt gestionate închiderile de afaceri în Project pentru web?

Proiectul pentru web nu respectă închiderile de afaceri pe care întreprinderea le definește la nivel de organizație. Cu toate acestea, va respecta alte tipuri de zile libere care sunt definite într-un anumit model de oră de lucru.

### <a name="what-are-the-limitations-of-project-for-the-web"></a>Care sunt limitările Project pentru web?

Vedea [Creați o structură de defalcare a lucrărilor: Limitări de proiect](/project-management/create-wbs#project-limitations.md).

### <a name="can-i-expect-changes-to-my-cost-and-sales-estimates"></a>Mă pot aștepta la modificări ale estimărilor mele privind costurile și vânzările?

În cazuri rare în care contururile de alocare a resurselor sunt recalculate sau când acestea se încadrează la o limită de dată diferită de cea a proiectului sursă, este posibil să observați diferențe în estimările de vânzări și costuri. Ca parte a procesului de actualizare, clienții sunt așteptați să testeze un set reprezentativ de proiecte, astfel încât să poată înțelege orice modificări potențiale ale programului.
