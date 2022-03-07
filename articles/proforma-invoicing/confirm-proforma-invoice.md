---
title: Confirmarea unei facturi proforma bazate pe proiect
description: Acest subiect oferă informații despre confirmarea unei facturi proforme bazate pe proiect.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 88dccb63247fe6937240921de7bc7a30a3737dad3f62c6c441d732c046aaddc3
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/06/2021
ms.locfileid: "6985876"
---
# <a name="confirm-a-proforma-project-based-invoice"></a>Confirmarea unei facturi proforma bazate pe proiect

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

După confirmarea unei facturi proforma, starea facturii proiectului se actualizează la **Confirmat**. Când o factură este confirmată, aceasta devine doar în citire. În continuare, factura poate fi corectată numai dacă există corecții sau credite inițiate de client.

Următorul tabel listează datele efective create de sistem. Aceste date reale sunt create atunci când anumite operațiuni sunt efectuate pe schița facturii proiectului înainte de a fi confirmată.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p>
                    <strong>Scenariu</strong>
                </p>
            </td>
            <td width="808" valign="top">
                <p>
                    <strong>Date reale create la confirmare</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Facturarea unui avans sau onorariu </p>
            </td>
            <td width="408" valign="top">
                <p>
O valoare reală de vânzări facturate de tip <strong>Onorariu</strong> este creată pentru suma de pe avans sau onorariu.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
O vânzare nefacturată reală, cu o sumă negativă a reținerii sau avansului care urmează a fi utilizată pentru reconciliere.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
După reconcilierea completă a unui onorariu sau avans pe o factură.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
O inversare nefacturată a vânzărilor de onorariu sau avans care a fost creată pentru reconciliere. Această sumă este pozitivă, deoarece este menită să anuleze negativul care a fost creat atunci când a fost facturat onorariul sau avansul.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
O valoare reală de vânzări facturate pentru suma de pe această factură.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
După reconcilierea parțială a unui onorariu sau avans pe o factură.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
O inversare nefacturată a vânzărilor de onorariu sau avans care a fost creată pentru reconciliere. Această sumă este pozitivă, deoarece este menită să anuleze negativul care a fost creat atunci când a fost facturat onorariul sau avansul.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
O valoare reală de vânzări facturate pentru suma de pe această factură.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
O valoare negativă reală de vânzări nefacturate a sumei restante a onorariului sau avansului care urmează a fi utilizată pentru reconciliere pe facturile viitoare.
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
O nouă valoare reală a vânzărilor nefacturate care se taxează pentru orele și suma din detaliile modificate ale liniei de facturare, o inversare a vânzărilor reale și o facturare echivalentă efectivă.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
O nouă valoare reală de vânzare nefacturată care este netaxabilă pentru restul orelor și sumei după scăderea cifrelor corectate pe detaliile modificate ale liniei de factură, o inversare a valorii reale a vânzărilor și o valoare reală de vânzare echivalentă.
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
O nouă valoare reală a vânzărilor nefacturate care nu se taxează pentru cantitatea rămasă și suma după deducerea cifrelor corectate din detaliile modificate ale liniei de facturare, o inversare a vânzărilor nefacturate reale și un echivalent al vânzărilor facturate efective.
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
O nouă valoare reală a vânzărilor nefacturate care se taxează pentru orele și suma din detaliile modificate ale liniei de facturare, o inversare a vânzărilor nefacturate reale și o facturare echivalentă efectivă. 
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Facturarea unei tranzacții de materiale fără nicio modificare pe proiectul de factură.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
O inversare de vânzări nefacturate pentru cantitatea și suma din detaliile aprobării inițiale de utilizare a materialelor.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
O valoare reală de vânzări facturată pentru cantitatea și suma din detaliile aprobării inițiale de utilizare a materialelor.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Facturarea unei tranzacții de materiale care a fost editată pentru a reduce cantitatea.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
O inversare de vânzări nefacturate pentru cantitatea și suma din detaliile aprobării inițiale de timp.
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
O nouă valoare reală a vânzărilor nefacturate care nu se taxează pentru cantitatea rămasă și suma după deducerea cifrelor corectate din detaliile modificate ale liniei de facturare, o inversare a vânzărilor nefacturate reale și un echivalent al vânzărilor facturate efective.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Facturarea unei tranzacții de materiale care a fost editată pentru a crește cantitatea.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
O inversare de vânzări nefacturate pentru cantitatea și suma din detaliile aprobării inițiale de utilizare a materialelor.
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
