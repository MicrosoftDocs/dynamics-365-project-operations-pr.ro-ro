---
title: Lucrul cu cheltuieli personale pe un raport de cheltuieli
description: Acest subiect oferă informații despre cum să lucrați cu cheltuielile personale suportate de angajați în timp efectuează deplasări în interes de serviciu.
author: suvaidya
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 5e1162133eec5a85675bf686855d420c50de0eaf045d81c4b417b6fe66ee19fe
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/06/2021
ms.locfileid: "6993166"
---
# <a name="work-with-personal-expenses-on-an-expense-report"></a>Lucrul cu cheltuieli personale pe un raport de cheltuieli

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

În timpul deplasărilor în interes de serviciu, un angajat poate realiza cheltuieli personale pe cardul lor de credit corporativ. Dacă nu a fost definit un proces pentru gestionarea cheltuielilor personale, procesul de aprobare a raportului de cheltuieli ar putea fi întrerupt atunci când un angajat prezintă raportul de cheltuieli detaliat.

Există două metode pe care le puteți utiliza pentru a lucra cu cheltuielile personale ale unui angajat:

  - **Plătit de angajat**: Organizația dvs. nu plătește cheltuielile personale care apar pe factura pentru cardul de credit al companiei. În schimb, angajatul plătește direct furnizorului cardului de credit pentru cheltuieli. 
  - **Plătit de companie**: Organizația dvs. plătește factura completă pentru cardul de credit corporativ și apoi debitează contul angajatului pentru cheltuielile personale.

Puteți selecta metoda pe care organizația dvs. o folosește pe pagina **Parametrii de gestionare a cheltuielilor**.


## <a name="enable-split-expense-function-when-personal-amount-field-has-value-defined"></a>Activați funcția de cheltuială divizată atunci când câmpul cu sumă personală are valoarea definită

Caracteristica, **Activați funcția de cheltuială divizată atunci când câmpul cu sumă personală are valoarea definită** se aplică numai rapoartelor de cheltuieli care sunt aprobate utilizând un flux de lucru la nivel de linie. Rapoartele sunt aprobate accesând **Procesați rapoarte de cheltuieli** > **Rapoarte de cheltuieli care mi-au fost atribuite** > **Raport de cheltuieli deschis**. 

Pentru a activa această caracteristică, accesați **Spații de lucru** > **Managementul caracteristicilor**, selectați **Activați funcția de cheltuială divizată atunci când câmpul cu sumă personală are valoarea definită**, apoi selectați **Activați acum**. 

Când funcția este activată, liniile de cheltuieli care utilizează această funcționalitate generează două linii atunci când raportul este trimis. Sunt generate două linii, astfel încât aprobatorul să poată aproba fiecare linie separat.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
