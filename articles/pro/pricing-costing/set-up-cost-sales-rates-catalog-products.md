---
title: Configurarea tarifelor de cost și de vânzare pentru produsele din catalog - simplificat
description: Acest subiect oferă informații despre modul de configurare al ratei de cost și vânzări pentru elemente dintr-un catalog de produse.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: bfb28e710c7b6da17d94679a72659f81df7a58e376e4bad94b58c36de781b197
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/06/2021
ms.locfileid: "6996046"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a>Configurarea tarifelor de cost și de vânzare pentru produsele din catalog - simplificat

_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_


Configurarea prețurilor pentru articolele din catalogul de produse în Dynamics 365 Project Operations este la fel ca în Dynamics 365 Sales.

În Project Operations, produsele nu pot fi estimate sau utilizate în proiecte, astfel încât prețurile din catalogul de produse nu trebuie să fie stabilite pe listele de prețuri ale proiectelor pentru oferte și contracte.

Utilizați câmpul **Prețul produsului** al unei oferte, al unui contract sau al unui cont pentru a stabili prețurile din catalogul de produse. Nu setați prețurile din catalogul de produse în listele de prețuri ale proiectului. Listele de prețuri ale proiectului sunt exclusive pentru Project Operations. Logica de afaceri specifică aplicației copiază listele de preț dintr-o ofertă într-un contract. Rezultatul este o listă de prețuri de proiect specifică pentru un contract. Operația de copiere poate întârzia procesul de câștigare a ofertei dacă lista de prețuri a proiectului din ofertă devine prea mare. Listele de prețuri ale produselor nu sunt copiate pentru a crea liste de prețuri personalizate în contracte. Deoarece nu este implicată nicio operație de copiere, performanța procesului de ofertare nu este afectată.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]