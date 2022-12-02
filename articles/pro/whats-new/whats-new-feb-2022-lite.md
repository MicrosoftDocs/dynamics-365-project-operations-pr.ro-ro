---
title: Ce este nou în februarie 2022 - Implementare simplificată Project Operations
description: Acest articol oferă informații despre actualizările de calitate care sunt disponibile în versiunea din februarie 2022 de implementare a Project Operations lite.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1203faa2dd53a8fb82cff0857a1725426ebff19a
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922835"
---
# <a name="whats-new-february-2022---project-operations-lite-deployment"></a>Ce este nou în februarie 2022 - Implementare simplificată Project Operations

_Se aplică pentru: implementare simplificată - înțelegere la emiterea facturii proforme_

Acest articol se aplică următoarelor componente și versiuni de Microsoft Dynamics 365 Project Operations:

- Project Operations într-un mediu Dataverse versiunea 4.28.0.120

## <a name="features-included-in-this-release"></a>Caracteristicile incluse în această versiune

Începând cu această versiune, puteți adăuga până la 300 de membri ai echipei la un singur proiect. Anterior, limita numărului de membri ai echipei era de 150. Pentru informaţii suplimentare, consultaţi [Limite de proiect](../../project-management/create-wbs.md#project-limitations).

## <a name="quality-updates"></a>Actualizări de calitate

| Zonă de caracteristici | Număr de referință | Actualizare de calitate |
| --- | --- | --- |
| Facturarea și stabilirea prețurilor | 2497369 | Corecția pentru materiale trebuie să urmeze valoarea datei din parametrii **Corecţie**. |
| Facturarea și stabilirea prețurilor | 2498697 | S-a îmbunătățit configurația de securitate pentru **Retragerea intrării de timp**. |
| Facturarea și stabilirea prețurilor | 2517455 | Acțiunea **Tranzacții pe linia de facturare reîmprospătată** nu trebuie să fie declanșată de mai multe ori simultan pentru aceeași factură. |
| Facturarea și stabilirea prețurilor | 2517465 | Acțiunea **Dezactivare detalii linie de factură** este blocată deoarece nu este acceptată. |
| Facturarea și stabilirea prețurilor | 2556660 | S-au remediat verificările de valabilitate a datei care se fac pe lista de prețuri care este atașată la o înregistrare a parametrilor proiectului. |
| Managementul oportunităților | 2369202 | S-a corectat logica de afaceri care verifică dacă listele de prețuri care au date de intrare în vigoare suprapuse pot fi atașate aceluiași contract de proiect. |
| Managementul oportunităților | 2385965 | S-a corectat comportamentul pe fila **Clienți** de pe pagina **Contract de proiect** când selectați **Salvare și închidere**. |
