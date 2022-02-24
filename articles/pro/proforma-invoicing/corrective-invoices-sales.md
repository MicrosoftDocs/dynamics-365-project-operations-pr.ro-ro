---
title: Facturi corective pentru proiect
description: Acest subiect oferă informații despre cum să creați și să confirmați facturi corective în Project Operations.
author: rumant
manager: Annbe
ms.date: 04/05/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ae6d881e4e68b9f467478afe9735fc3186e6b0a8
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 04/07/2021
ms.locfileid: "5866606"
---
# <a name="corrective-project-invoices"></a>Facturi corective pentru proiect

_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_

O factură de proiect confirmată poate fi corectată pentru a procesa modificările sau creditele negociate cu clientul și managerul de proiect.

Pentru a face modificări la o factură confirmată, deschideți factura confirmată și selectați **Corectați această factură**. 

> [!NOTE]
> Această selecție nu este disponibilă decât dacă se confirmă factura proiectului.

O nouă schiță de factură este creată din factura confirmată. Toate detaliile liniei de facturare din factura confirmată anterior sunt copiate în noua schiță. Următoarele sunt câteva dintre punctele cheie pentru a înțelege detaliile liniei de pe noua factură corectată:

- Toate cantitățile sunt actualizate la zero. Aplicația presupune că toate articolele facturate sunt creditate integral. Dacă este necesar, puteți actualiza manual aceste cantități pentru a reflecta cantitatea care este facturată și nu cantitatea care este creditată. Pe baza cantității pe care o introduceți, aplicația calculează cantitatea creditată. Această sumă se reflectă în datele reale care se creează la confirmarea facturii corectate. Dacă modificați valoarea impozitului, trebuie să introduceți suma corectă a impozitului și nu valoarea impozitului care este creditată.
- Liniile contractuale bazate pe produse confirmate anterior nu sunt copiate. Procesarea corecțiilor pe o factură de proiect bazată pe produs nu este acceptată.
- Corecțiile de jalon sunt întotdeauna procesate ca credite complete.
- Sumele de onorariu sau avans pot fi corectate dacă clientul a fost facturat pentru o sumă incorectă.
- Reconcilierile onorariilor și avansurilor pot fi corectate dacă a fost utilizată o sumă incorectă pentru a se concilia cu taxele de pe o factură confirmată anterior.

> [!IMPORTANT]
> Detaliile liniei de facturare care sunt corecții la alte taxe deja facturate au câmpul **Corecție** setat la **Da**. Facturile care au corectat detaliile liniei de facturare au un câmp numit **Are corecții** care este, de asemenea, setat la **Da**.

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
            <td width="216" rowspan="4" valign="top">
                <p>
Confirmați corectarea unui avans sau a unui onorariu facturat.<strong></strong>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
O inversare nefacturată a vânzărilor de onorariu sau avans care a fost creată pentru reconciliere. Această sumă este pozitivă deoarece este menită să anuleze negativul care a fost creat atunci când a fost facturat onorariul sau avansul.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Se creează o inversare a datelor reale ale vânzărilor facturate pentru suma din onorariu sau avans pentru a inversa vânzările facturate inițial.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Se creează o nouă vânzare facturată actuală pentru suma corectată de pe onorariu sau linia de factură corectată pe bază de avans.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
O valoare reală de vânzări nefacturate cu sumă negativă a onorariului sau a liniei de factură corectate pe bază de avans, care va fi utilizată pentru reconciliere.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
O confirmare a corectării unui onorariu sau a unui avans reconciliat anterior.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
O inversare nefacturată a vânzărilor de onorariu sau avans care a fost creată pentru reconciliere. Această sumă este pozitivă și este menită să anuleze negativul care a fost creat atunci când a avut loc reconcilierea anterioară.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
O valoare reală de inversare a vânzărilor facturate pentru suma de pe factura anterioară.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
O nouă valoare reală a vânzărilor facturate pentru suma de onorariu corectată care se aplică pe factura corectată.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
O valoare reală de vânzări nefacturate cu o sumă negativă din onorariul sau avansul rămas corectat, care va fi utilizată pentru reconciliere pe facturile ulterioare.
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
Neacceptat </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Credite și corecții ale unei linii contractuale bazate pe produse facturate anterior.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Neacceptat </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
