---
title: Înregistrați-vă pentru versiunile de încercare Project Operations
description: Acest articol oferă informații despre cum să implementați o versiune de încercare a Dynamics 365 Project Operations.
author: ruhercul
ms.date: 01/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 6a6986cfd6c01d1c22d37a10c8d824730fad2e9e
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029315"
---
# <a name="sign-up-for-project-operations-trials"></a>Înregistrați-vă pentru versiunile de încercare Project Operations 

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/non-stoc, implementare simplificată - facturare de la ofertă la proforma, Project Operations pentru scenarii stocate/bazate pe producție_ 



Acest articol explică cum să vă abonați la oferta de partener de previzualizare și să implementați a Dynamics 365 Project Operations mediu inconjurator.

Cu noua versiune de încercare Project Operations, puteți implementa automat oricare dintre cele trei scenarii de implementare acceptate completând un chestionar care recomandă cea mai bună abordare de implementare. Acest articol oferă informații despre cum să:

- Vă valorificați oferta de încercare.
- Începeți pregătirea.
- Configurați scrierea duală.
- Aflați mai multe despre Project Operations. 

Următorul tabel prezintă detaliile noii oferte de încercare.

| **Articol ofertă**               | **Detalii**                                  |
|------------------------------|----------------------------------------------|
| Tip ofertă                   | Acest tip de ofertă este generată de administrator, deci este necesar un administrator de entitate găzduită pentru a-l valorifica. |
| Utilizarea ofertei                    | O dată per entitate găzduită                          |
| Durata ofertei               | 30 de zile calendaristice                             |
| Răscumpărări per entitate găzduită       | 1                                            |
| Extensie                    | 1 extensie, 30 de zile calendaristice               |
| Număr de medii de încercare | 3                                            |


## <a name="admin-trial-details"></a>Detalii despre versiune de încercare pentru administrator
Următorul tabel listează detaliile versiunii de încercare și modul în care se aplică fiecărui tip de implementare.

| **Element**                      | **Lite**                                     | **Pentru materiale fără stoc** | **Pentru materiale cu stoc** |
|-------------------------------|----------------------------------------------|---------------------------|-----------------------|
| Date de configurare furnizate           | Da                                          | Da                       | Da (USSI)            |
| Date tranzacționale            | No                                           | No                        | No                    |
| Timp de pregătire în minute  | 15                                           | 90                        | 30                    |
 
## <a name="prerequisites"></a>Cerințe preliminare
Pentru a implementa o versiune de încercare a Dynamics 365 Project Operations, sunt necesare următoarele cerințe preliminare.

- Înscrieți-vă la [Dynamics 365 Project Operations - Previzualizare versiune de încercare](https://www.aka.ms/try-po).
- Utilizatorul care implementează previzualizarea trebuie să aibă drepturi de administrator global entitate găzduită Azure.

> [!IMPORTANT]
> O singură persoană dintr-o organizație, administratorul entității găzduite, trebuie să îndeplinească această sarcină. Dacă nu sunteți abonatul la această versiune, așteptați până când organizația dvs. a fost înregistrată și ați primit acreditările dvs. de utilizator.

### <a name="dynamics-365-project-operations---preview-trial"></a>Dynamics 365 Project Operations - Previzualizare versiune de încercare 

Înainte de a începe, conectați-vă la un browser cu contul de lucru al utilizatorului în entitatea găzduită în care doriți previzualizarea Project Operations.

1. Valorificați primul cod de ofertă, **Dynamics 365 Project Operations - Previzualizare încercare** lipindu-l în URL-ul browserului.

    ![Valorificați oferta](./media/16RedeemFirstOfferNew.png)

2. Confirmați comanda.

    ![Confirmați comanda](./media/17ConfirmOrderNew.png)

  Veți vedea că oferta de confirmare a fost valorificată cu succes.

   ![Confirmare](./media/18OrderConfirmationNew.png)

  Veți fi redirecționat către [centrul de administrare Power Platform](https://admin.powerplatform.microsoft.com/projectoperationstrial).

## <a name="questionnaire-and-provisioning"></a>Chestionar și pregătire

1.  Accesați [centrul de administrare Power Platform=](https://admin.powerplatform.com/projectoperationstrial) și completați chestionarul.  
2.  Examinați tipul de implementare recomandat și selectați **Începeți configurarea** pentru a iniția pregătirea.
3.  Revizuiți termenii și condițiile, și apoi selectați **Start**.

   După începerea pregătirii, sunteți redirecționat către lista de medii din centrul de administrare Power Platform. În timp ce pregătirea este în curs, starea mediului dvs. este **PreparingInstance**.
 
  Când pregătirea este completă, starea mediului dvs. este **Pregătit**. Pregătirea mediului include implementarea datelor demo.
 
4.  Selectați respectivul Microsoft Dataverse URL și adresele URL ale aplicațiilor financiare și operaționale pentru a valida implementarea.

## <a name="configuring-dual-write"></a>Configurare scriere duală
- Pentru a configura rolurile de securitate pentru scriere duală, consultați [Actualizați setările de securitate pentru Operațiuni de proiect în Dataverse](resource-provision-new-environment.md#update-security-settings-on-project-operations-on-dataverse).
- Pentru a accesa configurația cu dublă scriere, navigați la instanța de finanțare și operațiuni, apoi navigați la **Management de date** > **Scriere dublă**.
- Pentru a configura hărți cu scriere duală, consultați [Rulați hărți cu scriere duală pentru Operațiuni de proiect](resource-provision-new-environment.md#run-project-operations-dual-write-maps).

## <a name="assign-licenses"></a>Atribuirea de licențe

Veți avea nevoie de acces administrativ la organizația dvs. Microsoft 365 Portal pentru a finaliza pașii următori.

1. Du-te la [Microsoft 365 centru de administrare](https://portal.office.com/) pentru a atribui licențele utilizatorilor dvs.

   ![Pagina principală a centrului de administrare](./media/14AdminPortal.png)

2. Pe pagina **Utilizatori activi**, selectați utilizatorii cărora doriți să le atribuiți o licență.

   ![Atribuiți licențe](./media/15AssignLicenses.png)

3. Verificați dacă a fost selectată licența **Previzualizare Dynamics 365 Project Operations**, apoi selectați **Salvare modificări**.

## <a name="additional-resources"></a>Resurse suplimentare

Următoarele resurse oferă îndrumări utile pe măsură ce vă începeți călătoria cu Project Operations:

- [Seria de videoclipuri Prezentare generală Project Operations prezintă caracteristici detaliate și foi de parcurs](https://youtube.com/playlist?list=PLcakwueIHoT_LJ3Fr1tHnkPk5lioqE6uH)
- [Dynamics 365 Project Operations](/learn/modules/examine-dynamics-365-project-operations/)
- [Determinarea tipului de implementare](determine-deployment-type.md)

## <a name="frequently-asked-questions"></a>Întrebări frecvente

### <a name="what-if-i-require-alm-or-elm-for-my-finance-and-operations-apps-environment"></a>Ce se întâmplă dacă am nevoie de ALM sau ELM pentru mediul meu de aplicații financiare și operaționale?

- Pentru partenerii care necesită capacități complete de gestionare a ciclului de viață al mediului, consultați [Solicitare de licență pentru Sandbox partener](https://experience.dynamics.com/requestlicense) pentru a revizui noua ofertă de partener. 
- Pentru partenerii care caută mai multe informații despre drepturile de utilizare internă, consultați [Cloud drepturi de utilizare internă și beneficii software (microsoft.com](https://partner.microsoft.com/membership/internal-use-software).

### <a name="can-i-extend-my-trial-beyond-30-days"></a>Pot să-mi prelungesc versiunea de încercare peste 30 de zile?
Pentru a vă prelungi perioada de încercare, parcurgeți pașii următori.

1. În **Microsoft 365 Centrul de administrare**, mergi la **Facturare** > **Produsele dvs**.
2. Selectați **Dynamics 365 Project Operations (CE) - Previzualizare versiune de încercare**.
3. Sub **Data expirării**, selectați **Prelungire dată**.

### <a name="can-i-upgrade-from-the-lite-deployment-to-the-resourcenon-stocked-based-scenario-deployment"></a>Pot face upgrade de la implementarea lite la implementarea scenariului bazat pe resurse/fără stoc?
În prezent, nu există suport pentru actualizarea unui mediu de la o versiune lite la o implementare bazată pe lipsă de stocuri.

### <a name="can-i-access-lifecycle-services-lcs-for-my-finance-environments"></a>Pot accesa Lifecycle Services (LCS) pentru mediile mele financiare?  
Nu. Pentru aceste versiuni de încercare, implementarea este gestionată prin centrul de administrare Power Platform. Accesul la mediul financiar este restricționat.

### <a name="can-i-install-my-trial-on-an-existing-environment"></a>Pot instala versiunea de încercare pe un mediu existent?
Dacă aveți un mediu existent, vi se va permite să instalați implementarea lite pe o un mediu existent Dataverse de vânzări din centrul de administrare Power Platform.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
