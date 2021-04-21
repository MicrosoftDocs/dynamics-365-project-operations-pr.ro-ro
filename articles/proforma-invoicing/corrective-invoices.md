---
title: Facturi corective bazate pe proiect
description: Acest subiect oferă informații despre cum să creați și să confirmați facturi corective bazate pe proiect în Project Operations.
author: rumant
manager: Annbe
ms.date: 03/29/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: fc96bb40f5207efc381986d46a3e37dfc1dc111c
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 04/07/2021
ms.locfileid: "5867056"
---
# <a name="corrective-project-based-invoices"></a>Facturi corective bazate pe proiect

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

O factură de proiect confirmată poate fi corectată pentru a procesa modificările sau creditele negociate cu clientul și managerul de proiect.

Pentru a face modificări la o factură confirmată, deschideți factura confirmată și selectați **Corectați această factură**. 

> [!NOTE]
> Această selecție nu este disponibilă decât dacă o factură de proiect este confirmată sau dacă factura bazată pe proiect are avansuri sau rețineri sau reconcilieri de avansuri sau de rețineri.

O nouă schiță de factură este creată din factura confirmată. Toate detaliile liniei de facturare din factura confirmată anterior sunt copiate în noua schiță. Următoarele sunt câteva dintre punctele cheie pentru a înțelege detaliile liniei de pe noua factură corectată:

- Toate cantitățile sunt actualizate la zero. Dynamics 365 Project Operations presupune că toate articolele facturate sunt creditate integral. Dacă este necesar, puteți actualiza manual aceste cantități pentru a reflecta cantitatea care este facturată și nu cantitatea care este creditată. Pe baza cantității pe care o introduceți, aplicația calculează cantitatea creditată. Această sumă se reflectă în datele reale care se creează la confirmarea facturii corectate. Dacă modificați valoarea impozitului, trebuie să introduceți suma corectă a impozitului și nu valoarea impozitului care este creditată.
- Corecțiile de jalon sunt întotdeauna procesate ca credite complete.


> [!IMPORTANT]
> Pentru detaliile liniei de facturare care sunt corecții la alte taxe deja facturate, câmpul **Corecție** este setat la **Da**. Pentru facturile care au detalii ale liniei de facturare corectate, câmpul **Are corecții** este setat la **Da**.

## <a name="actuals-created-when-a-corrective-invoice-is-confirmed"></a>Date reale create când se confirmă o factură corectivă

Următorul tabel listează valorile reale care sunt create la confirmarea unei facturi corective.

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
Facturarea creditului integral al unei tranzacții temporare facturate anterior.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
O inversare a vânzărilor facturate pentru orele și suma din detaliile liniei de facturare inițiale pentru timp.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
O nouă valoare reală a vânzărilor nefacturate pentru orele și suma din detaliile liniei de facturare inițiale pentru timp.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Facturarea creditului parțial pe o tranzacție temporală.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
O inversare a vânzărilor facturate pentru orele și suma facturate din detaliile liniei de facturare inițiale pentru timp.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
O nouă valoare reală a vânzărilor nefacturate care se taxează pentru orele și suma din detaliile modificate ale liniei de facturare, o inversare a acestora și o facturare echivalentă efectivă.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
O nouă valoare reală a vânzărilor nefacturate care se taxează pentru orele și suma rămasă după deducerea cifrelor corectate pe detaliile liniei de facturare.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Facturarea creditului integral al unei tranzacții de cheltuială facturate anterior.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
O inversare a vânzărilor facturate pentru cantitatea și suma din detaliile liniei de facturare inițiale pentru cheltuială.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
O nouă valoare reală a vânzărilor nefacturate pentru cantitatea și suma din detaliile liniei de facturare inițiale pentru cheltuială.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Facturarea creditului parțial al unei tranzacții de cheltuială facturate anterior.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
O inversare a vânzărilor facturate pentru cantitatea și suma facturată din detaliile liniei de facturare inițiale pentru o cheltuială.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
O nouă valoare reală a vânzărilor nefacturate care se taxează pentru cantitatea și suma din detaliile corectate ale liniei de facturare, o inversare a acestora și o facturare echivalentă efectivă.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
O nouă valoare reală a vânzărilor nefacturate care se taxează pentru cantitatea și suma rămasă după deducerea cifrelor corectate pe detaliile liniei de facturare.
                </p>
            </td>
        </tr>
                <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Facturarea creditului integral al unei tranzacții de materiale facturate anterior.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
O inversare facturată a vânzărilor pentru cantitatea și suma din detaliile liniei inițiale de facturare pentru material.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
O valoare reală nefacturată nouă a vânzărilor pentru cantitatea și suma din detaliile liniei inițiale de facturare pentru material.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Facturarea creditului parțial pentru o tranzacție de materiale.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
O inversare de factură de vânzări pentru cantitatea și suma facturate pe detaliile liniei inițiale a facturii pentru material.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
O nouă valoare reală a vânzărilor nefacturate care este taxabilă pentru cantitatea și suma din detaliile editate ale liniei de facturare, o inversare a acesteia și o valoare reală echivalentă a vânzărilor facturate.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
O nouă valoare reală a vânzărilor nefacturate care se taxează pentru cantitatea și suma rămasă după deducerea cifrelor corectate pe detaliile liniei de facturare.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Facturarea creditului integral al taxei unei tranzacții facturate anterior.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
O inversare a vânzărilor facturate pentru cantitatea și suma din detaliile liniei de facturare inițiale pentru taxă.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
O nouă valoare reală a vânzărilor nefacturate pentru cantitatea și suma din detaliile liniei de facturare inițiale pentru taxă.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Facturarea creditului parțial al taxei unei tranzacții facturate anterior.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
O inversare a vânzărilor facturate pentru cantitatea și suma facturată din detaliile liniei de facturare inițiale pentru taxă.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
O nouă valoare reală a vânzărilor nefacturate care se taxează pentru cantitatea și suma din detaliile corective modificate ale liniei de facturare, o inversare a acestora și o facturare echivalentă efectivă.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Facturarea creditului integral al jalonului facturat anterior.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
O inversare a vânzărilor facturate pentru suma din detaliile liniei de facturare inițiale pentru jalon.
                </p>
                <p>
Starea facturii pentru reper este actualizată din <b>Factură client postată</b> în <b>Gata de facturare</b>.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Facturarea creditului parțial al jalonului facturat anterior.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Acest scenariu nu este acceptat.
                </p>
            </td>
        </tr>       
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
