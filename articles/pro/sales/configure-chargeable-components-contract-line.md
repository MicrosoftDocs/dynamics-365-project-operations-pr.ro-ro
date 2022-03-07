---
title: Configurarea componentelor tarifabile ale unei linii de contract bazate pe proiect
description: Acest subiect oferă informații despre cum să adăugați componente taxabile la liniile contractuale în Project Operations.
author: rumant
ms.date: 10/08/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d18e56f29457151e07636b67ff8d9b184bf5014ef0ceeef9bb9d322672be4335
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/06/2021
ms.locfileid: "7003471"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a>Configurarea componentelor tarifabile ale unei linii de contract bazate pe proiect

_**Se aplică la:** Implementare Lite - tratarea facturării proforma, Project Operations pentru resurse/scenarii bazate pe altceva decât stocuri_

O linie de contract bazată pe proiecte are componente *incluse* și componente *taxabile*.

Componentele incluse sunt componente care fac obiectul:

  - Metoda de facturare și împărțirea clienților
  - Limite de nedepășire 
  - Setările frecvenței facturilor definite pe linia de contract bazată pe proiect

Un subset al componentelor incluse poate fi marcat ca taxabil folosind câmpul **Tip de facturare**. Câmpul **Tip de facturare** este un set de opțiuni care permite următoarele valori în contextul unei linii contractuale:

  - Taxabil
  - Netaxabil

Componentele taxabile pot fi definite pe sarcini, roluri și categorii de tranzacții.

Taxabilitatea este definită pentru sarcinile pentru o linie de contract de proiect și se aplică tuturor claselor de tranzacții incluse pe linie. Dacă câmpul **Includeți activități** de pe o linie de contract este necompletat sau setat la **Întregul proiect**, fila **Sarcini taxabile** nu va fi disponibilă.

Taxabilitatea definită pe roluri pentru o linie de contract de proiect se aplică numai pentru clasa tranzacției **Timp**. Dacă câmpul **Includeți timpul** de pe o linie de contract este setat la **Nu**, fila **Roluri tarifabile** nu va fi disponibilă.

Taxabilitatea definită pe categorii de tranzacții pentru o linie de contract de proiect se aplică numai pentru clasa tranzacției **Cheltuială**. Dacă câmpul **Includeți cheltuielile** este setat la **Nu**, fila **Categorii tarifabile** nu va fi disponibilă.

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a>Actualizați o sarcină de proiect ca fiind taxabilă sau netaxabilă

O sarcină de proiect poate fi taxabilă sau netaxabilă pe o anumită linie contractuală, ceea ce face posibilă următoarea configurare:

Dacă o linie de contract bazată pe proiect include **Timp** și o anumită sarcină, **T1** este asociat acesteia ca taxabil. Dacă există o a doua linie de contract care include **Cheltuieli**, puteți asocia sarcina T1 pe linia contractului ca netaxabilă. Rezultatul este că tot timpul înregistrat în sarcină este taxabil și toate cheltuielile sunt netaxabile.

Tipul de facturare al unei activități poate fi configurat pe fila **Activități facturabile** liniei contractului prin actualizarea câmpului **Tip de facturare** pe subgrila activități linie contract. Alternativ, puteți actualiza câmpul **Tip de facturare** pe subgrila sarcinii Configurarea facturării unui proiect care arată liniile contractuale asociate unei activități.

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a>Actualizați un rol ca fiind taxabil sau netaxabil

Un rol poate fi taxabil sau netaxabil pe o anumită linie contractuală.

Tipul de facturare al unui rol poate fi configurat pe fila **Roluri tarifabile** al unei linii contractuale. Pentru a face acest lucru, actualizați câmpul **Tipul de facturare** pe subgrila **Roluri facturabile**.

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a>Actualizați o categorie de tranzacții ca fiind taxabilă sau netaxabilă

O categorie de tranzacție poate fi taxabilă sau netaxabilă pe o anumită linie contractuală.

Tipul de facturare al unei tranzacții poate fi configurat pe fila **Categorii tarifabile** a unei linii de contract bazate pe proiect. Pentru a face acest lucru, actualizați câmpul **Tipul de facturare** pe subgrila **Categorii facturabile**.

### <a name="resolve-chargeability"></a>Rezolvați taxarea

O estimare sau o valoare reală creată pentru timp este considerată taxabilă numai dacă:

   - **Timp** este inclus pe linia de contract.
   - **Rol** este configurat ca taxabil pe linia de contract.
   - **Sarcini incluse** este setat la **Sarcini selectate** pe linia de contract.
 
 Dacă aceste trei lucruri sunt adevărate, sarcina este și ea configurată ca taxabilă. 

O estimare sau o valoare reală creată pentru cheltuieli este considerată taxabilă numai dacă:

   - **Cheltuieli** este inclus pe linia de contract
   - **Categoria tranzacției** este configurat ca taxabil pe linia de contract
   - **Sarcini incluse** este setat la **Sarcină selectată** pe linia de contract
  
 Dacă aceste trei lucruri sunt adevărate, **Sarcină** este și ea configurată ca taxabilă. 

O estimare sau o valoare reală creată pentru materiale este considerată taxabilă numai dacă:

   - **Materiale** este inclus pe linia de contract
   - **Sarcini incluse** este setat la **Sarcini selectate** pe linia de contract

Dacă aceste două lucruri sunt adevărate, **Sarcină** este și ea configurată ca taxabilă. 

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>Include timpul</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>Include cheltuielile</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>Includere Materiale</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
                    <strong>Activități incluse</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Rol</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Categorie</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Activitate</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
                    <strong>Impactul taxării</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Da </p>
            </td>
            <td width="78" valign="top">
                <p>
Da </p>
            </td>
            <td width="63" valign="top">
                <p>
Da </p>
            </td>
            <td width="75" valign="top">
                <p>
Întregul proiect </p>
            </td>
            <td width="65" valign="top">
                <p>
Taxabil </p>
            </td>
            <td width="70" valign="top">
                <p>
Taxabil </p>
            </td>
            <td width="65" valign="top">
                <p>
Nu se poate seta </p>
            </td>
            <td width="350" valign="top">
                <p>
Facturare la un timp real: <strong>Taxabil</strong>
                </p>
                <p>
Tipul de facturare pe cheltuieli reale: <strong>Taxabil</strong>
                </p>
                <p>
Tipul de facturare pe materialul real: <strong>Taxabil</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Da </p>
            </td>
            <td width="78" valign="top">
                <p>
Da </p>
            </td>
            <td width="63" valign="top">
                <p>
Da </p>
            </td>
            <td width="75" valign="top">
                <p>
Numai activități selectate </p>
            </td>
            <td width="65" valign="top">
                <p>
Taxabil </p>
            </td>
            <td width="70" valign="top">
                <p>
Taxabil </p>
            </td>
            <td width="65" valign="top">
                <p>
Taxabil </p>
            </td>
            <td width="350" valign="top">
                <p>
Facturare la un timp real: <strong>Taxabil</strong>
                </p>
                <p>
Tipul de facturare pe cheltuieli reale: <strong>Taxabil</strong>
                </p>
                <p>
Tipul de facturare pe materialul real: <strong>Taxabil</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Da </p>
            </td>
            <td width="78" valign="top">
                <p>
Da </p>
            </td>
            <td width="63" valign="top">
                <p>
Da </p>
            </td>
            <td width="75" valign="top">
                <p>
Numai activități selectate </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Netaxabil</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
Taxabil </p>
            </td>
            <td width="65" valign="top">
                <p>
Taxabil </p>
            </td>
            <td width="350" valign="top">
                <p>
Facturare la un timp real: <strong>Netaxabil</strong>
                </p>
                <p>
Tipul de facturare pentru cheltuieli reale: Taxabil </p>
                <p>
Tipul de facturare pentru materialul real: Taxabil </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Da </p>
            </td>
            <td width="78" valign="top">
                <p>
Da </p>
            </td>
            <td width="63" valign="top">
                <p>
Da </p>
            </td>
            <td width="75" valign="top">
                <p>
Numai activități selectate </p>
            </td>
            <td width="65" valign="top">
                <p>
Taxabil </p>
            </td>
            <td width="70" valign="top">
                <p>
Taxabil </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Netaxabil</strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
Facturare la un timp real: <strong>Netaxabil</strong>
                </p>
                <p>
Tip de facturare pe cheltuieli reale: <strong>Netaxabil</strong>
                </p>
                <p>
Tip de facturare pe materiale reale: <strong>Netaxabil</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Da </p>
            </td>
            <td width="78" valign="top">
                <p>
Da </p>
            </td>
            <td width="63" valign="top">
                <p>
Da </p>
            </td>
            <td width="75" valign="top">
                <p>
Numai activități selectate </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Netaxabil</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
Taxabil </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Netaxabil</strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
Facturare la un timp real: <strong>Netaxabil</strong>
                </p>
                <p>
Tip de facturare pe cheltuieli reale: <strong>Netaxabil</strong>
                </p>
                <p>
Tip de facturare pe materiale reale: <strong>Netaxabil</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Da </p>
            </td>
            <td width="78" valign="top">
                <p>
Da </p>
            </td>
            <td width="63" valign="top">
                <p>
Da </p>
            </td>
            <td width="75" valign="top">
                <p>
Numai activități selectate </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Netaxabil</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Netaxabil</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Taxabil </p>
            </td>
            <td width="350" valign="top">
                <p>
Facturare la un timp real: <strong>Netaxabil</strong>
                </p>
                <p>
Tip de facturare pe cheltuieli reale: <strong>Netaxabil</strong>
                </p>
                <p>
Tipul de facturare pentru materialul real: Taxabil </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
Da </p>
            </td>
            <td width="63" valign="top">
                <p>
Da </p>
            </td>
            <td width="75" valign="top">
                <p>
Întregul proiect </p>
            </td>
            <td width="65" valign="top">
                <p>
Nu se poate seta </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Taxabil</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Nu se poate seta </p>
            </td>
            <td width="350" valign="top">
                <p>
Facturare pe un timp real: <strong>Indisponibil</strong>
                </p>
                <p>
Tipul de facturare pentru cheltuieli reale: Taxabil </p>
                <p>
Tipul de facturare pentru materialul real: Taxabil </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
Da </p>
            </td>
            <td width="63" valign="top">
                <p>
Da </p>
            </td>
            <td width="75" valign="top">
                <p>
Întregul proiect </p>
            </td>
            <td width="65" valign="top">
                <p>
Nu se poate seta </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Netaxabil</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Nu se poate seta </p>
            </td>
            <td width="350" valign="top">
                <p>
Facturare pe un timp real: <strong>Indisponibil</strong>
                </p>
                <p>
Tip de facturare pe cheltuieli reale: <strong>Netaxabil</strong>
                </p>
                <p>
Tipul de facturare pentru materialul real: Taxabil </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Da </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
Da </p>
            </td>
            <td width="75" valign="top">
                <p>
Întregul proiect </p>
            </td>
            <td width="65" valign="top">
                <p>
Taxabil </p>
            </td>
            <td width="70" valign="top">
                <p>
Nu se poate seta </p>
            </td>
            <td width="65" valign="top">
                <p>
Nu se poate seta </p>
            </td>
            <td width="350" valign="top">
                <p>
Facturare la un timp real: Taxabil </p>
                <p>
Tipul de facturare pe cheltuieli reale:<strong> Indisponibil</strong>
                </p>
                <p>
Tipul de facturare pentru materialul real: Taxabil </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Da </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
Da </p>
            </td>
            <td width="75" valign="top">
                <p>
Întregul proiect </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Netaxabil</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
Nu se poate seta </p>
            </td>
            <td width="65" valign="top">
                <p>
Nu se poate seta </p>
            </td>
            <td width="350" valign="top">
                <p>
Facturare la un timp real: <strong>Netaxabil</strong>
                </p>
                <p>
Tipul de facturare pe cheltuieli reale:<strong> Indisponibil</strong>
                </p>
                <p>
Tipul de facturare pentru materialul real: Taxabil </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Da </p>
            </td>
            <td width="78" valign="top">
                <p>
Da </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
Întregul proiect </p>
            </td>
            <td width="65" valign="top">
                <p>
Taxabil </p>
            </td>
            <td width="70" valign="top">
                <p>
Taxabil </p>
            </td>
            <td width="65" valign="top">
                <p>
Nu se poate seta </p>
            </td>
            <td width="350" valign="top">
                <p>
Facturare la un timp real: Taxabil </p>
                <p>
Tipul de facturare pentru cheltuieli reale: Taxabil </p>
                <p>
Tipul de facturare pe materiale reale:<strong> Indisponibil</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Da </p>
            </td>
            <td width="78" valign="top">
                <p>
Da </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
Întregul proiect </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Netaxabil</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Netaxabil</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Nu se poate seta </p>
            </td>
            <td width="350" valign="top">
                <p>
Facturare la un timp real: <strong>Netaxabil</strong>
                </p>
                <p>
Tip de facturare pe cheltuieli reale: <strong>Netaxabil</strong>
                </p>
                <p>
Tipul de facturare pe materiale reale:<strong> Indisponibil</strong>
                </p>
            </td>
        </tr>
    </tbody>
</table>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
