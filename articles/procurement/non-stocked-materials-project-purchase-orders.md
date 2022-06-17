---
title: Comandarea unor materiale care nu sunt pe stoc pentru un proiect, folosind comenzi de achiziție pentru proiecte
description: Acest articol explică modul în care puteți comanda materiale care nu sunt stocate pentru un proiect folosind comenzile de achiziție ale proiectului.
author: sigitac
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: fe24faa143869af2396f3b0f28aae31417cadda7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929827"
---
# <a name="order-procurement-categories-or-non-stocked-materials-for-a-project-using-project-purchase-orders"></a>Comandați categorii de achiziții sau materiale nestocizate pentru un proiect utilizând comenzile de achiziție ale proiectului

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

S-ar putea ca departamentul de achiziții din organizația dvs. să utilizeze [comenzi de achiziție](/dynamics365/supply-chain/procurement/purchase-order-overview) pentru a urmări comenzile de bunuri și servicii. Comenzile de achiziție pentru categoriile de achiziții sau materialele care nu sunt în stoc pot fi atribuite unui proiect. Facturarea acestor comenzi de achiziție înregistrează costul în raport cu proiectul.

## <a name="prerequisites"></a>Cerințe preliminare
Parcurgeți pașii următori pentru a activa funcționalitatea comenzilor de achiziție a proiectului.

1. În Dynamics 365 Finance, accesați **Managementul caracteristicilor** spațiu de lucru.
2. În lista de funcții, găsiți și selectați caracteristica, **Activați comenzile de achiziție a proiectului în Project Operations pentru scenarii bazate pe resurse/ne-stocate**.
3. Selectați **Activare**.
4. Configurați materialele care nu sunt stocate și facturile de vânzător în așteptare, așa cum este descris în [Configurați materialele care nu sunt stocate și facturile de vânzător în așteptare](configure-materials-nonstocked.md).
5. Configurați categoriile de achiziții așa cum este descris în [Utilizați categorii de achiziții cu comenzile de achiziție de proiect și facturile furnizorilor în așteptare](configure-procurement-categories.md).

## <a name="create-a-project-purchase-order-from-the-project-purchase-order-list"></a>Creați o comandă de achiziție a proiectului din lista comenzilor de achiziție a proiectului

1. În Finanțe, accesați **Management de proiect și contabilitate** > **Proiecte** > **Toate proiectele** și selectați un proiect.
2. Pe panoul de acțiune, pe fila **Gestionați** în grupul **Nou**, selectați **Activitatea elementului** > **Comandă de achiziție**.
3. Pe pagina **Creați comanda de achiziție**, selectați furnizorul cu care doriți să plasați comanda de cumpărare, introduceți alte informații după caz, apoi selectați **OK**.
4. Pe pagina **Comandă de achiziție**, în grila **Linii de comandă de cumpărare**, selectați **Adăugați linie**.
5. Introduceți un număr de articol sau o categorie de achiziție, cantitate, unitate, preț unitar și alte informații, după caz.

    > [!NOTE]
    > Doar categoriile de achiziții, articolele care nu sunt stocate și serviciile pot fi utilizate cu comenzile de achiziție de proiect. Articolele stocate nu sunt acceptate.

6. Continuați să adăugați articole sau categorii de achiziții după cum este necesar și confirmați comanda de cumpărare.

    Chitanțele de bunuri și servicii pot fi înregistrate prin crearea și postarea unei chitanțe de produs.

    > [!NOTE]
    > Chitanțele de produs nu sunt înregistrate în realitatea proiectului în Microsoft Dataverse și nu influențați subregistrul proiectului.

    După ce un furnizor trimite factura pentru articolele și serviciile din comanda de achiziție, departamentul de achiziții poate genera o factură pentru comanda de cumpărare accesând **Factură** > **Generare** > **Factură** pe panoul de acțiune. Pentru mai multe informații despre facturile în așteptare ale furnizorului, consultați [Achiziționați materiale ne-stocate utilizând o factură de vânzător în așteptare](pending-vendor-invoices.md).
