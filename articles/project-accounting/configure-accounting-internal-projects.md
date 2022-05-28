---
title: Configurați contabilitatea pentru proiectele interne
description: Acest subiect oferă informații despre modul de configurare a practicilor contabile pentru proiecte interne în Project Operations.
author: sigitac
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 9da72d8dbf720e380a49a1010caca472ee024783
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8597859"
---
# <a name="configure-accounting-for-internal-projects"></a>Configurați contabilitatea pentru proiectele interne

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

Proiectele interne permit companiilor să urmărească costurile legate de activitățile care nu sunt facturate unui client. Exemple de proiecte interne includ:

- Dezvoltarea unui produs, cum ar fi o aplicație mobilă și urmărirea costurilor asociate dezvoltării.
- Gestionarea timpului și a cheltuielilor de pre-vânzare. Acest proiect intern de pre-vânzare poate fi transformat ulterior într-un proiect facturabil dacă se câștigă o ofertă.

Orice proiect care nu este asociat cu un contract în Dynamics 365 Project Operations este tratat ca intern. Costul de proiect și profilele de venituri nu sunt folosite pentru a determina regulile de contabilitate pentru proiect. Costul intern al proiectului este întotdeauna înregistrat utilizând principiile de profit și pierdere. Conturile contabile pentru înregistrări sunt definite pe pagina **Configurare înregistrare contabilitate**.

- Tranzacțiile în timp sunt înregistrate prin debitarea contului **Cost** și prin creditarea contului **Alocarea salarizării**.
- Tranzacțiile de cheltuieli sunt înregistrate prin debitarea contului **Cost** și prin creditarea **Cont compensat pentru cheltuieli**.
- Tranzacțiile articolelor sunt postate prin debitarea contului **Cost** și creditarea contului **Cost - Articol**.

După ce tranzacțiile sunt înregistrate în proiect, dacă proiectul este asociat cu un contract de proiect, sistemul anulează toate tranzacțiile acumulate și creează noi tranzacții facturabile. Tranzacțiile facturabile respectă regulile contabile definite în costul proiectului respectiv și în profilul de venituri.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
