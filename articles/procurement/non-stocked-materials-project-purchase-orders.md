---
title: Comandarea unor materiale care nu sunt pe stoc pentru un proiect, folosind comenzi de achiziție pentru proiecte
description: Acest subiect explică cum ar trebui să comandați materiale care nu sunt pe stoc pentru un proiect utilizând comenzi de achiziție pentru proiecte.
author: sigitac
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6e0307ad6474feef96fc8080877eccbbbc7259db
ms.sourcegitcommit: 2d96345fb3afc3b174530285f95271b5ccbdea03
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 09/29/2021
ms.locfileid: "7563037"
---
# <a name="order-non-stocked-materials-for-a-project-using-project-purchase-orders"></a>Comandarea unor materiale care nu sunt pe stoc pentru un proiect, folosind comenzi de achiziție pentru proiecte

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

S-ar putea ca departamentul de achiziții din organizația dvs. să utilizeze [comenzi de achiziție](/dynamics365/supply-chain/procurement/purchase-order-overview) pentru a urmări comenzile de bunuri și servicii. Comenzile de cumpărare pentru materiale care nu sunt stoc pot fi atribuite unui proiect. Facturarea acestor comenzi de achiziție înregistrează costul în raport cu proiectul.

## <a name="prerequisites"></a>Cerințe preliminare
Parcurgeți pașii următori pentru a activa funcționalitatea comenzilor de achiziție a proiectului.

1. În Dynamics 365 Finance, accesați spațiul de lucru **Gestionarea caracteristicilor**.
2. În lista de funcții, găsiți și selectați caracteristica, **Activați comenzile de achiziție a proiectului în Project Operations pentru scenarii bazate pe resurse/ne-stocate**.
3. Selectați **Activare**.
4. Configurați materialele care nu sunt stocate și facturile de vânzător în așteptare, așa cum este descris în [Configurați materialele care nu sunt stocate și facturile de vânzător în așteptare](configure-materials-nonstocked.md).

## <a name="create-a-project-purchase-order-from-the-project-purchase-order-list"></a>Creați o comandă de achiziție a proiectului din lista comenzilor de achiziție a proiectului

1. În Finanțe, accesați **Management de proiect și contabilitate** > **Proiecte** > **Toate proiectele** și selectați un proiect.
2. Pe panoul de acțiune, pe fila **Gestionați** în grupul **Nou**, selectați **Activitatea elementului** > **Comandă de achiziție**.
3. Pe pagina **Creați comanda de achiziție**, selectați furnizorul cu care doriți să plasați comanda de cumpărare, introduceți alte informații după caz, apoi selectați **OK**.
4. Pe pagina **Comandă de achiziție**, în grila **Linii de comandă de cumpărare**, selectați **Adăugați linie**.
5. Introduceți numărul articolului, cantitatea, unitatea, prețul unitar și alte informații, după caz.

    > [!NOTE]
    > Numai articolele și serviciile ne-stocate pot fi utilizate cu comenzile de achiziție ale proiectului. Articolele stocate și categoriile de achiziții nu sunt acceptate.

6. Continuați să adăugați articole după cum este necesar și să confirmați comanda de cumpărare.

    Chitanțele de bunuri și servicii pot fi înregistrate prin crearea și postarea unei chitanțe de produs.

    > [!NOTE]
    > Chitanțele de produs nu sunt înregistrate în realitatea proiectului în Microsoft Dataverse și nu influențați subregistrul proiectului.

    După ce un furnizor trimite factura pentru articolele și serviciile din comanda de achiziție, departamentul de achiziții poate genera o factură pentru comanda de cumpărare accesând **Factură** > **Generare** > **Factură** pe panoul de acțiune. Pentru mai multe informații despre facturile în așteptare ale furnizorului, consultați [Achiziționați materiale ne-stocate utilizând o factură de vânzător în așteptare](pending-vendor-invoices.md).