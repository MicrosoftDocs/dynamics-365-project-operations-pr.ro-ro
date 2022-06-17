---
title: Configurarea tarifelor de cost și de vânzare pentru produsele din catalog - simplificat
description: Acest articol oferă informații despre cum să configurați costurile și tarifele de vânzare pentru articolele dintr-un catalog de produse.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 4689d6929e24ebaa992232f809a7ec60908ee517
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8917407"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a>Configurarea tarifelor de cost și de vânzare pentru produsele din catalog - simplificat

_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_


Configurarea prețurilor pentru articolele din catalogul de produse în Dynamics 365 Project Operations este la fel ca în Dynamics 365 Sales.

În Project Operations, produsele nu pot fi estimate sau utilizate în proiecte, astfel încât prețurile din catalogul de produse nu trebuie să fie stabilite pe listele de prețuri ale proiectelor pentru oferte și contracte.

Utilizați câmpul **Prețul produsului** al unei oferte, al unui contract sau al unui cont pentru a stabili prețurile din catalogul de produse. Nu setați prețurile din catalogul de produse în listele de prețuri ale proiectului. Listele de prețuri ale proiectului sunt exclusive pentru Project Operations. Logica de afaceri specifică aplicației copiază listele de preț dintr-o ofertă într-un contract. Rezultatul este o listă de prețuri de proiect specifică pentru un contract. Operația de copiere poate întârzia procesul de câștigare a ofertei dacă lista de prețuri a proiectului din ofertă devine prea mare. Listele de prețuri ale produselor nu sunt copiate pentru a crea liste de prețuri personalizate în contracte. Deoarece nu este implicată nicio operație de copiere, performanța procesului de ofertare nu este afectată.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]