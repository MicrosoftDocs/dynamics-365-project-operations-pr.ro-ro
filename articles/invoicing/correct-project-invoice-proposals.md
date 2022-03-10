---
title: Contabilitatea corectă a propunerilor schiță de facturi pentru proiect
description: Acest subiect explică modul de ajustare a informațiilor referitoare la contabilitate pe un proiect de propunere de factură.
author: sigitac
ms.date: 06/07/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 153a239d4b88906909ee0bfae8a18cabebc3766399290d83bb79f5d6375a942c
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/06/2021
ms.locfileid: "6999331"
---
# <a name="correct-the-accounting-on-draft-project-invoice-proposals"></a>Contabilitatea corectă a propunerilor schiță de facturi pentru proiect

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

*Detalii operaționale* pentru facturile de proiect sunt menținute de managerul de proiect pe o factură pro forma. Aceste detalii includ deciziile cu privire la orele, cheltuielile, materialele sau etapele care trebuie facturate, tarifele și aplicarea sumelor de avans și de reținere. După ce confirmați factura proforma originală, puteți ajusta detaliile operaționale prin crearea și confirmarea unei [facturi corective proforma](../proforma-invoicing/corrective-invoices.md).

*Detaliile contabile* pentru facturile de proiect sunt păstrate într-un document de facturare orientat către client. Aceste detalii includ calculul impozitului pe vânzări și dimensiunile financiare care se aplică facturii. Acest subiect oferă detalii despre modul în care aceste detalii contabile pot fi ajustate într-o propunere de factură proiect de proiect.

## <a name="adjust-sales-tax"></a>Ajustați impozitul pe vânzări

Grupurile de taxe de vânzare și facturile implicite de facturare pot fi ajustate direct pe documentul propunerii de facturare. Pentru a ajusta aceste grupuri, selectați **Editare**, apoi, pe fiecare linie de propunere de facturare a proiectului, introduceți o nouă valoare în câmpul **Grup de impozite pe vânzări** sau **Grup de taxe pe vânzări de articole**.

## <a name="adjust-financial-dimensions"></a>Ajustați dimensiunile financiare

Dimensiunile financiare nu pot fi editate direct pe o linie de propunere de factură de proiect. În schimb, urmați acești pași pentru a ajusta dimensiunile financiare pe o propunere de factură a proiectului.

1. În propunerea de facturare a proiectului, selectați **Ștergeți tot** pentru a elimina liniile de propunere de facturare a proiectului.

    > [!NOTE]
    > Butonul **Ștergeți tot** este disponibil numai după ce administratorul de sistem activează caracteristica **Ștergeți liniile de propunere de factură atunci când utilizați Project Operations pentru scenarii bazate pe resurse/nebazate pe stoc** în spațiu de lucru **Gestionarea caracteristicilor**.

2. Ajustați dimensiunile financiare:

    - **Tranzacții în cont (repere de facturare):** accesați **Toate proiectele** \> **Administrare** \> **Tranzacții în cont**, și selectați jalonul care necesită ajustare. Apoi, pe fila **Dimensiuni financiare**, actualizați valorile după cum este necesar.
    - **Timp, cheltuieli și tranzacții materiale:** Pe pagina **Tranzacții de proiect postate**, selectați **Ajustați contabilitatea** pentru a actualiza dimensiunile financiare.

3. După ce ați terminat de ajustat valorile dimensiunii financiare, accesați **Management de proiect și contabilitate** \> **Periodice** \> **Integrarea Project Operations** și selectați **Importați din tabelul de etapizare** pentru a rula procesul periodic. Acest proces utilizează valorile dimensiunii financiare actualizate pentru a recrea liniile de propunere de facturare a proiectului. Valorile actualizate sunt apoi utilizate în registrul general și în registrul general atunci când se înregistrează factura proiectului.
