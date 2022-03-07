---
title: Confirmarea unei facturi proforma - simplificat
description: Acest subiect furnizează informații despre confirmarea facturilor proforma în Project Operations.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3b1818f20a0d54848939b689f87986154943c57a
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274293"
---
# <a name="confirm-a-proforma-invoice---lite"></a>Confirmarea unei facturi proforma - simplificat

_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_


După confirmarea unei facturi proforma, starea facturii proiectului se actualizează la **Confirmat**. Când o factură este confirmată, aceasta devine doar în citire. În continuare, factura poate fi corectată numai dacă există corecții sau credite inițiate de clienți sau dacă factura este marcată ca plătită.

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
O valoare reală de vânzări nefacturate a unei sume negative a onorariului sau avansului care urmează a fi utilizată pentru reconciliere.
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
O nouă valoare reală a vânzărilor nefacturate care nu se taxează pentru orele rămase și suma după deducerea cifrelor corectate din detaliile modificate ale liniei de facturare, o inversare a vânzărilor reale și o facturare echivalentă efectivă.
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
O valoare reală de vânzări facturate pentru cantitatea și suma conform aprobării inițiale a cheltuielii </p>
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
        <tr>
            <td width="216" valign="top">
                <p>
Facturarea unei linii contractuale pe bază de produse.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
O valoare reală de vânzări facturate pentru linia de produse cu cantitatea și suma provenite din linia de contract pe bază de produs.
                </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]