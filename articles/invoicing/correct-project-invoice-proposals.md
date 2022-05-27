---
title: Contabilitatea corectă a propunerilor schiță de facturi pentru proiect
description: Acest subiect explică modul de ajustare a informațiilor referitoare la contabilitate pe un proiect de propunere de factură.
author: sigitac
ms.date: 01/05/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: bf0a3d6b97880920b133cb3b30389adf0c83111c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8575089"
---
# <a name="correct-the-accounting-on-draft-project-invoice-proposals"></a>Contabilitatea corectă a propunerilor schiță de facturi pentru proiect

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

*Detalii operaționale* pentru facturile de proiect sunt menținute de managerul de proiect pe o factură pro forma. Aceste detalii includ deciziile cu privire la orele, cheltuielile, materialele sau etapele care trebuie facturate, tarifele și aplicarea sumelor de avans și de reținere. După ce confirmați factura proforma originală, puteți ajusta detaliile operaționale prin crearea și confirmarea unei [facturi corective proforma](../proforma-invoicing/corrective-invoices.md).

*Detaliile contabile* pentru facturile de proiect sunt păstrate într-un document de facturare orientat către client. Aceste detalii includ calculul impozitului pe vânzări și dimensiunile financiare care se aplică facturii. Acest subiect oferă detalii despre modul în care aceste detalii contabile pot fi ajustate într-o propunere de factură proiect de proiect.

## <a name="adjust-sales-tax"></a>Ajustați impozitul pe vânzări

Grupurile de taxe de vânzare și facturile implicite de facturare pot fi ajustate direct pe documentul propunerii de facturare. Pentru a ajusta aceste grupuri, selectați **Editare**, apoi, pe fiecare linie de propunere de facturare a proiectului, introduceți o nouă valoare în câmpul **Grup de impozite pe vânzări** sau **Grup de taxe pe vânzări de articole**.

## <a name="adjust-financial-dimensions"></a>Ajustați dimensiunile financiare

### <a name="header-dimensions"></a>Dimensiunile antetului

În mod implicit, dimensiunile financiare ale facturii sunt derivate din înregistrările tranzacțiilor de proiect nefacturate care sunt facturate. Cu toate acestea, setările de sistem vă permit să utilizați dimensiunile financiare din antetul propunerilor de factură de proiect pentru a posta soldurile clienților. Pentru a activa această funcționalitate, selectați **Permite actualizări ale dimensiunilor proiectului pentru conturile de încasat** pe **Financiare** fila din **Management de proiect și parametri contabili** pagină.

Dimensiunile financiare de pe anteturile facturii pot fi editate înainte ca o factură să fie postată. Pe **Propunere de factura de proiect** pagina, comutați la **Antet** vizualizați și apoi editați valorile din **Dimensiunile financiare** fila.

The **Antet** vizualizarea este disponibilă numai după ce administratorul de sistem activează **Utilizați formularele de propunere de factură de proiect și jurnal de factură cu vizualizarea Antet și linii** caracteristică în **Managementul caracteristicilor** spațiu de lucru. Această caracteristică necesită actualizarea financiară 10.0.25 sau o versiune ulterioară.

### <a name="line-dimensions"></a>Dimensiunile liniei

Dimensiunile financiare nu pot fi editate direct pe o linie de propunere de factură de proiect. În schimb, urmați acești pași pentru a ajusta dimensiunile financiare pe o propunere de factură a proiectului.

1. În propunerea de facturare a proiectului, selectați **Ștergeți tot** pentru a elimina liniile de propunere de facturare a proiectului.

    Butonul **Ștergeți tot** este disponibil numai după ce administratorul de sistem activează caracteristica **Ștergeți liniile de propunere de factură atunci când utilizați Project Operations pentru scenarii bazate pe resurse/nebazate pe stoc** în spațiu de lucru **Gestionarea caracteristicilor**.

2. Ajustați dimensiunile financiare:

    - **Tranzacții în cont (repere de facturare):** accesați **Toate proiectele** \> **Administrare** \> **Tranzacții în cont**, și selectați jalonul care necesită ajustare. Apoi, pe fila **Dimensiuni financiare**, actualizați valorile după cum este necesar.
    - **Timp, cheltuieli și tranzacții materiale:** Pe pagina **Tranzacții de proiect postate**, selectați **Ajustați contabilitatea** pentru a actualiza dimensiunile financiare.

3. După ce ați terminat de ajustat valorile dimensiunii financiare, accesați **Management de proiect și contabilitate** \> **Periodice** \> **Integrarea Project Operations** și selectați **Importați din tabelul de etapizare** pentru a rula procesul periodic. Acest proces utilizează valorile dimensiunii financiare actualizate pentru a recrea liniile de propunere de facturare a proiectului. Valorile actualizate sunt apoi utilizate în registrul general și în registrul general atunci când se înregistrează factura proiectului.
