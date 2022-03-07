---
title: Configurarea componentelor tarifabile ale unei linii de ofertă
description: Acest subiect oferă informații despre configurarea componentelor taxabile și netaxabile pe o linie de ofertă bazată pe proiect.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ec8a999142fd9960c79ef981e499ae840642e57b269c83d201d2db006179de09
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/06/2021
ms.locfileid: "6996001"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a>Configurarea componentelor tarifabile ale unei linii de ofertă 

_**Se aplică la:** Implementare Lite - tratarea facturării proforma, Project Operations pentru resurse/scenarii bazate pe altceva decât stocuri_

O linie de ofertă bazată pe proiecte are conceptul de componente *incluse* și componente *taxabile*.

Componentele incluse sunt supuse la:

  - Metoda de facturare și împărțirea clienților
  - Limite de nedepășire 
  - Setările frecvenței facturilor definite pe linia de ofertă bazată pe proiect

Un subset al componentelor incluse poate fi marcat ca taxabil folosind câmpul **Tip de facturare**. Câmpul **Tip de facturare** este un set de opțiuni care permite următoarele valori în contextul unei linii de ofertă:

  - Taxabil
  - Netaxabil

Componentele taxabile pot fi definite pe sarcini, roluri și categorii de tranzacții.

Taxabilitatea este definită pentru sarcinile pentru linia de ofertă și se aplică tuturor claselor de tranzacții incluse pe acea linie. Dacă câmpul **Includeți activități** este setat la **Întregul proiect** sau este necompletat, fila **Sarcini taxabile** nu este disponibilă.

Taxabilitatea este definită pe roluri pentru o linie de ofertă și se aplică numai pentru clasa tranzacției **Timp**. Dacă câmpul **Includeți timpul** de pe o linie de ofertă de contract este setat la **Nu**, fila **Roluri tarifabile** nu este disponibilă.

Taxabilitatea este definită pe categorii de tranzacții pentru o linie de ofertă și se aplică numai pentru clasa tranzacției **Cheltuială**. Dacă câmpul **Includeți cheltuieli** de pe o linie de ofertă de contract este setat la **Nu**, fila **Categorii tarifabile** nu este disponibilă.

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a>Actualizați o sarcină de proiect pentru a fi taxabilă sau netaxabilă

O sarcină de proiect poate fi taxabilă sau netaxabilă în contextul unei linii specifice de ofertă bazate pe proiect, ceea ce face posibilă următoarea configurare.

Dacă o linie de ofertă bazată pe proiect include **Timp** și sarcina **T1**, sarcina este asociată liniei de ofertă ca taxabilă. Dacă există o a doua linie de ofertă care include **Cheltuieli**, puteți asocia sarcina **T1** pe linia de ofertă ca netaxabilă. Rezultatul este că tot timpul înregistrat în sarcină este taxabil și toate cheltuielile înregistrate în sarcină sunt netaxabile.

Un tip de facturare al activității poate fi configurat pe fila **Activități facturabile** al unei linii de ofertă bazată pe proiect actualizând câmpul **Tip de facturare** pe subgrila **Activități de linie de ofertă**. Alternativ, puteți actualiza tipul de facturare pentru o activitate de proiect în câmpul **Tip de facturare** pe subgrila activității de configurare a facturării unui proiect care arată liniile ofertei asociate unei activități.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Actualizați un rol pentru a fi taxabil sau netaxabil

Un rol poate fi taxabil sau netaxabil în contextul unei linii specifice de ofertă pe bază de proiect.

Tipul de facturare al unui rol poate fi configurat pe fila **Roluri facturabile** al unei linii de ofertă bazată pe proiect actualizând câmpul **Tip de facturare** pe subgrila **Roluri facturabile**.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Actualizați o categorie de tranzacții pentru a fi taxabilă sau netaxabilă

O categorie de tranzacție poate fi taxabilă sau netaxabilă pe o anumită linie de ofertă.

Tipul de facturare al unei tranzacții poate fi configurat pe fila **Categorii facturabile** al unei linii de ofertă actualizând câmpul **Tip de facturare** pe subgrila **Categorii facturabile**.

### <a name="resolve-chargeability"></a>Rezolvați taxarea
O estimare sau o valoare reală creată pentru timp va fi considerată taxabilă numai dacă:

   - **Timp** este inclus pe linia de ofertă.
   - **Rol** este configurat ca taxabil pe linia de ofertă.
   - **Sarcini incluse** este setat la **Sarcini selectate** pe linia de ofertă. 

Dacă aceste trei lucruri sunt adevărate, **Sarcină** este, de asemenea, configurat ca taxabil. 

O estimare sau o valoare reală creată pentru cheltuieli este considerată taxabilă numai dacă: 

   - **Cheltuieli** este inclus pe linia de ofertă.
   - **Categoria tranzacției** este configurat ca taxabil pe linia de ofertă.
   - **Sarcini incluse** este setat la **Sarcini selectate** pe linia de ofertă.

Dacă aceste trei lucruri sunt adevărate, **Sarcină** este, de asemenea, configurat ca taxabil. 

O estimare sau o valoare reală creată pentru material va fi considerată taxabilă numai dacă:

   - **Materiale** este inclus pe linia de ofertă.
   - **Sarcini incluse** este setat la **Sarcini selectate** pe linia de ofertă.

Dacă aceste două lucruri sunt adevărate, **Sarcină** ar trebui să fie configurat tot ca taxabil. 


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
Nu poate fi setat </p>
            </td>
            <td width="350" valign="top">
                <p>
Facturare la un timp real: Taxabil </p>
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
Taxabil </p>
            </td>
            <td width="350" valign="top">
                <p>
Facturare la un timp real: Taxabil </p>
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
Nu poate fi setat </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Taxabil</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Nu poate fi setat </p>
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
Nu poate fi setat </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Netaxabil</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Nu poate fi setat </p>
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
Nu poate fi setat </p>
            </td>
            <td width="65" valign="top">
                <p>
Nu poate fi setat </p>
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
Nu poate fi setat </p>
            </td>
            <td width="65" valign="top">
                <p>
Nu poate fi setat </p>
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
Nu poate fi setat </p>
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
Nu poate fi setat </p>
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
