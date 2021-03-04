---
title: Confirmarea unei facturi proforma
description: Acest subiect oferă informații despre confirmarea unei facturi proforma.
author: rumant
manager: AnnBe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: fa1e6c17fbda76a283c2ec68760a00e846decf83
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128118"
---
# <a name="confirm-a-proforma-invoice"></a>Confirmarea unei facturi proforma

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

După confirmarea unei facturi proforma, starea facturii proiectului se actualizează la **Confirmat**. Când o factură este confirmată, aceasta devine doar în citire. În continuare, factura poate fi corectată numai dacă există corecții sau credite inițiate de clienți sau când este marcată ca plătită.

Următorul tabel listează datele efective create de sistem. Aceste date reale sunt create atunci când anumite operațiuni sunt efectuate pe schița facturii proiectului înainte de a fi confirmată.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="416" valign="top">
                <p>
                    <strong>Scenariu</strong>
                </p>
            </td>
            <td width="608" valign="top">
                <p>
                    <strong>Date reale create la confirmare</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Facturarea unei tranzacții de timp fără modificări pe schița de factură.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
O inversare a vânzărilor nefacturate pentru ore și sumă conform aprobării inițiale a timpului.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
O valoare reală de vânzări facturate pentru ore și sumă conform aprobării inițiale a timpului.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Facturarea unei tranzacții în timp care a fost editată pentru a reduce cantitatea.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
O inversare a vânzărilor nefacturate pentru ore și sumă conform aprobării inițiale a timpului.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
O nouă vânzare nefacturată efectivă care se taxează pentru orele și suma din detaliile modificate ale liniei de facturare, o inversare a vânzărilor nefacturate efective și o facturare echivalentă efectivă.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
O nouă vânzare nefacturată efectivă care nu se taxează pentru orele rămase și suma după deducerea cifrelor corectate din detaliile modificate ale liniei de facturare, o inversare a vânzărilor nefacturate efective și o facturare echivalentă efectivă.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Facturarea unei tranzacții în timp care a fost editată pentru a mări cantitatea.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
O inversare a vânzărilor nefacturate pentru ore și sumă conform aprobării inițiale a timpului.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
O nouă vânzare nefacturată efectivă care se taxează pentru orele și suma din detaliile modificate ale liniei de facturare, o inversare a vânzărilor nefacturate efective și o facturare echivalentă efectivă.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Facturarea unei tranzacții pentru o cheltuială fără modificări pe schița de factură.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
O inversare a vânzărilor nefacturate pentru cantitatea și suma conform aprobării inițiale a cheltuielii.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
O valoare reală de vânzări nefacturate care se taxează pentru cantitatea și suma din detaliile modificate ale liniei de facturare, o inversare a vânzărilor nefacturate efective și o facturare echivalentă efectivă.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Facturarea unei tranzacții pentru o cheltuială care a fost editată pentru a reduce cantitatea.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
O inversare a vânzărilor nefacturate pentru cantitatea și suma conform aprobării inițiale a cheltuielii.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
O nouă vânzare nefacturată efectivă care se taxează pentru orele și suma din detaliile modificate ale liniei de facturare, o inversare a vânzărilor nefacturate efective și o facturare echivalentă efectivă. 
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
O nouă vânzare nefacturată efectivă care nu se taxează pentru cantitatea rămasă și suma după deducerea cifrelor corectate din detaliile modificate ale liniei de facturare, o inversare a vânzărilor nefacturate efective și un echivalent al vânzărilor facturate efective.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Facturarea unei tranzacții pentru o cheltuială care a fost editată pentru a mări cantitatea.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
O inversare a vânzărilor nefacturate pentru cantitatea și suma conform aprobării inițiale a cheltuielii.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
O nouă vânzare nefacturată efectivă care se taxează pentru orele și suma din detaliile modificate ale liniei de facturare, o inversare a vânzărilor nefacturate efective și o facturare echivalentă efectivă.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Facturarea unei taxe.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
O inversare a vânzărilor nefacturate pentru valoarea taxei pe linia de jurnal originală.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
O valoare reală de vânzări facturate pentru cantitatea și suma din linia de jurnal de taxă inițială.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Facturarea unui jalon.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
O vânzare facturată efectivă pentru suma de jalon de pe jalonul original de pe linia contractului de proiect.
                </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]