---
title: Configurarea de roluri în șabloanele de structură detaliată a proiectului
description: Acest subiect oferă informații despre configurarea informațiilor despre roluri pe șabloanele structurii de defalcare a lucrului.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 143f1094c653fb7ac0e026b7875aa162a3eb83f7
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082776"
---
# <a name="set-up-roles-on-work-breakdown-structure-templates"></a>Configurarea de roluri în șabloanele de structură detaliată a proiectului

[!include [banner](../includes/banner.md)]

Managerii de proiect pot configura șabloanele structurii detaliate a proiectului (WBS) pe care le pot aplica atunci când creează un WBS pentru noi proiecte. Managerii de proiect pot adăuga roluri atunci când creează un șablon. Utilizați următoarea procedură pentru a atribui un rol unui șablon WBS.

1. Selectați **Gestionarea proiectului și contabilitate** > **Configurare** > **Proiecte** > **Șabloanee structurii detaliate a proiectului**.
2. Selectați **Detalii** pentru un șablon WBS selectat.
3. Selectați o sarcină din listă și apoi în câmpul **Rol** , selectați un rol pe care să îl atribuiți sarcinii.

## <a name="work-with-a-wbs"></a>Lucrul cu un WBS

Aveți posibilitatea să creați un nou WBS, sau puteți copia un WBS existent ca șablon WBS. Un manager de proiect poate gestiona cu ușurință resursele atribuind roluri noilor sarcini de pe WBS. Rolurile pot fi înlocuite fie după obținerea unei resurse, fie după identificarea unei resurse confirmate pentru a lucra la sarcină. Această flexibilitate permite managerilor de proiect să îndeplinească următoarele sarcini:

- Identificarea numărului de resurse necesare pachetelor de lucru WBS.
- Estimarea costurilor proiectelor.
- Determinarea unui buget preliminar.
- Estimarea duratei activității, pe baza rolurilor și resurselor.
- Elaborarea câtorva planuri de management de proiect, pe baza informațiilor disponibile despre proiect.

Opțiuni suplimentare au fost adăugate în WBS pentru a utiliza mai bine funcționalitatea de resurse.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Opțiune</th>
<th>Descriere</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Atribuiri de resurse</td>
<td>Vizualizați resursele alocate, datele, numărul de ore și tipul de rezervare pentru sarcini pe WBS.</td>
</tr>
<tr class="even">
<td>Generare automată echipă</td>
<td>Adăugați automat resurse planificate utilizând roluri asociate cu o sarcină. Finanțele sugerează automat resursele planificate utilizând analiza deciziilor cu mai multe criterii, care se bazează pe roluri. După ce rolurile și efortul (orele) au fost stabilite pentru sarcinile dintr-un WBS și după ce structura a fost lansată, selectați <strong>Generarea automată a echipei</strong>. Numărul necesar de resurse planificate este adăugat la WBS și la fila <strong>Planificarea proiectului și echipei</strong>.</td>
</tr>
<tr class="odd">
<td>Resursă (listă verticală)</td>
<td>Din pagina <strong>Lansare atribuire resurse</strong>, puteți selecta resurse pentru rezervare fermă sau rezervare provizorie, în funcție de durata specificată. Puteți ajusta setările de vizualizare pentru a vedea și seta durata activităților de resurse. Puteți selecta și atribui resurse la nivelul pachetului de lucru utilizând următoarele opțiuni:
<ul>
<li><strong>Accept</strong> - Confirmați modificările resursei care este atribuită unei sarcini.</li>
<li><strong>Anulare</strong> - Anulați modificările resursei care este atribuită unei sarcini.</li>
<li><strong>Alocare automată</strong> - O resursă de personal disponibilă care are un rol potrivit este selectată automat și atribuită sarcinii selectate.</li>
</ul></td>
</tr>
</tbody>
</table>

1. Din pagina **Toate proiectele** , selectați proiectul **Faza 2 de upgrade XYZ**.
2. Selectați **Plan** > **Activități** > **Structură detaliată a proiectului**.
3. Selectați **Nou** pentru a adăuga la WBS următoarele activități de nivel unu:

    - Inițiere
    - Se planifică
    - Se execută
    - Monitorizare și control
    - Închideți

4. Setați datele și efortul (orele), așa cum se arată în ilustrația următoare.

    [![Stabilirea datelor și efortului](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)

5. Selectați linia de sarcină **Inițiere** și apoi în câmpul **Rol** , selectați **Manager de proiect senior**.
6. Selectați **Publicare**.
7. Pe aceeași linie, în câmpul **Resursă** , selectați **Daniel Goldschmidt** , apoi selectați **Accept**.
8. Selectați linia de sarcină **Planificare** și apoi în câmpul **Rol** , selectați **Analist de afaceri**.
9. Selectați **Publicare** , apoi selectați **Generarea automată a echipei**.
10. În caseta de mesaj care apare, selectați **Da**.
11. În câmpul **Resursă** , verificați dacă valoarea este **Analist de afaceri 1**.
12. Pentru resursa **Analist de afaceri 1** , deschideți căutarea și selectați **Lansare atribuiri de resurse**. Apoi selectați un angajat pentru sarcină.
13. Selectați **Atribuire provizorie** &gt; **Capacitate completă**.

    > [!NOTE] 
    > Nu primiți un avertisment că resursa specificată este acum 2, deoarece numărul de resurse rămâne 1.

14. Din pagina **Structură detaliată a proiectului** , validați atribuirea resurselor pe WBS, apoi selectați **Salvare**.
