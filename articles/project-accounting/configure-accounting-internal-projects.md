---
title: Configurați contabilitatea pentru proiectele interne
description: Acest subiect oferă informații despre modul de configurare a practicilor contabile pentru proiecte interne în Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 504e7481cb2aee6310cb4ace2d0791d1c7fe360d
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082730"
---
# <a name="configure-accounting-for-internal-projects"></a>Configurați contabilitatea pentru proiectele interne

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

Proiectele interne permit companiilor să urmărească costurile legate de activitățile care nu sunt facturate unui client. Exemple de proiecte interne includ:

- Dezvoltarea unui produs, cum ar fi o aplicație mobilă și urmărirea costurilor asociate dezvoltării.
- Gestionarea timpului și a cheltuielilor de pre-vânzare. Acest proiect intern de pre-vânzare poate fi transformat ulterior într-un proiect facturabil dacă se câștigă o ofertă.

Orice proiect care nu este asociat cu un contract în Dynamics 365 Project Operations este tratat ca intern. Costul de proiect și profilele de venituri nu sunt folosite pentru a determina regulile de contabilitate pentru proiect. Costul intern al proiectului este întotdeauna înregistrat utilizând principiile de profit și pierdere. Conturile contabile pentru înregistrări sunt definite pe pagina **Configurare înregistrare contabilitate**.

- Tranzacțiile în timp sunt înregistrate prin debitarea contului **Cost** și prin creditarea contului **Alocarea salarizării**.
- Tranzacțiile de cheltuieli sunt înregistrate prin debitarea contului **Cost** și prin creditarea **Cont compensat pentru cheltuieli**.

După ce tranzacțiile sunt înregistrate în proiect, dacă proiectul este asociat cu un contract de proiect, sistemul anulează toate tranzacțiile acumulate și creează noi tranzacții facturabile. Tranzacțiile facturabile respectă regulile contabile definite în costul proiectului respectiv și în profilul de venituri.


