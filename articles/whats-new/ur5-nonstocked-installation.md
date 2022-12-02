---
title: Actualizați Project Operations în mediul dvs. de Finanțe
description: Acest articol oferă informații despre cum să actualizați Project Operations în mediul dvs. Dynamics 365 Finance.
author: ruhercul
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: aedfd815521054d58944496500aa03a27be9267b
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/18/2022
ms.locfileid: "9030050"
---
# <a name="update-project-operations-in-your-finance-environment"></a>Actualizați Project Operations în mediul dvs. de Finanțe

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_


Acest articol oferă informații despre cum să actualizați Dynamics 365 Project Operations în mediul dvs. Dynamics 365 Finance. Există trei proceduri care sunt necesare pentru a actualiza Project Operations la Actualizarea 5 (UR5):

- [Importați pachetul în proiectul dvs. de previzualizare](#import)
- [Aplicați actualizarea](#apply)
- [Actualizați mediul Dataverse](#update)

## <a name="import-the-package-into-your-lcs-project"></a><a name="import"></a>Importați pachetul în proiectul dvs. LCS

1. Conectați-vă la [Lifecycle Services (LCS)](https://lcs.dynamics.com/) ca proprietar de proiect sau manager de mediu.
2. Din lista de proiecte, selectați proiectul dvs. LCS.
3. Pe pagina **Proiect**, la grupul **Medii**, deschideți mediul pe care doriți să îl actualizați.
4. Verificați dacă mediul rulează. Dacă nu este pornit, porniți mediul.
5. În secțiunea **Noua versiune**, la **Actualizări disponibile**, selectați **Vizualizați actualizarea** pentru 10.0.15.

![Vizualizați butonul de actualizare.](media/view-update.png)

6. Pe pagina **Actualizări binare**, selectați **Salvați pachetul**.
7. Pe pagina **Revizuiți și salvați actualizări**, selectați **Salvați pachetul**.
8. Pe panoul care se deschide **Salvați pachetul în biblioteca de active**, introduceți numele pachetului și apoi selectați **Salvați pachetul**.
9. Când LCS a terminat de salvat pachetul, se va activa butonul **Terminat**. Selectați **Terminat**. LCS va verifica pachetul. Verificarea poate dura câteva minute sau până la o oră.


## <a name="apply-the-package-update"></a><a name="apply"></a>Aplicați actualizarea pachetului

1. În LCS, pe pagina **Detalii despre mediu**, selectați **Menţineți** > **Aplicați actualizări**.
2. Din listă, selectați pachetul pe care l-ați salvat mai devreme, apoi selectați **Aplicați**.
3. Selectați **Da** pentru a confirma că doriți să implementați pachetul.

![Casetă de dialog de confirmare a implementării pachetului.](media/confirm-package-deployment.png)

4. Selectați **Da** pentru a confirma că doriți să actualizați aplicația.

![Casetă de dialog de confirmare a actualizării aplicației.](media/confirm-application-update.png)

Implementarea și actualizarea aplicației vor începe. 

Pe pagina **Detalii despre mediu**, în colțul din dreapta sus, starea mediului se va actualiza la **Service**. În aproximativ două ore, actualizarea va fi completă. Informațiile privind lansarea aplicației se vor actualiza la **Microsoft Dynamics 365 for Finance and Operations 10.0.15)** iar starea mediului se va actualiza la **Implementat**.


## <a name="update-your-dataverse-environment"></a><a name="update"></a>Actualizați mediul Dataverse

1. Conectați-vă la [Centrul de administrare Power Platform](https://admin.powerplatform.com/).
2. În listă, găsiți și deschideți mediul pe care l-ați folosit pentru a instala Project Operations.
3. Pe pagina **Medii**, selectați **Resursă** > **Aplicații Dynamics 365**.
4. În listă, localizați **Microsoft Dynamics 365 Project Operations**, și în coloana **Stare**, selectați **Actualizare disponibilă**.
5. Bifați caseta de selectare **Sunt de acord cu termenele serviciului**, apoi selectați **Actualizați**. Va fi instalată cea mai recentă versiune a soluției.

După finalizarea instalării, veți avea instalată versiunea 4.5.0.134.

## <a name="configure-new-features"></a>Configurați caracteristici noi

### <a name="enable-dual-write-mapping"></a>Activați maparea cu scriere duală

După ce finalizați actualizarea pentru mediile Finanțe și Dataverse, puteți activa mapările necesare cu scriere duală. Realizați următoarele proceduri pentru a activa mapările cu scriere duală.

- [Actualizați setările de securitate din mediul Customer Engagement](#security)
- [Reîmprospătarea entităților de date](#refresh)
- [Actualizați și rulați mapările cu scriere duală](#run)

### <a name="update-security-settings-on-the-dataverse-environment"></a><a name="security"></a>Actualizați setările de securitate pe mediul Dataverse

Următoarele actualizări ale privilegiilor de securitate pentru entități sunt necesare ca parte a actualizării la UR5.

1. In mediul dvs. Dataverse, accesați **Setări**, iar în grupul **Sistem**, selectați **Securitate**.

![Setări de mediu Dataverse.](media/Picture21.png)

2. Selectare **roluri de securitate**.
3. Din lista de roluri, selectați **utilizator de aplicație cu scriere duală** și selectați fila **Entități personalizate**. 
4. Verificați dacă rolul are permisiunile **Citit** și **Adăugați la** pentru:

      - **Tipul cursului de schimb valutar**
      - **Plan de conturi** 
      - **Calendar fiscal** 
      - **Registru**

5. După actualizarea rolului de securitate, accesați **Setări** > **Securitate** > **Echipe**. Verificați dacă rolul de **utilizator de aplicație cu scriere duală** a fost aplicat echipei. 

### <a name="refresh-data-entities-from-the-update"></a><a name="refresh"></a>Reîmprospătați entitățile de date din actualizare

1. În mediul dvs. financiar, deschideți spațiul de lucru **Management de date**, apoi deschideți pagina **Parametrii cadru**.
2. Pe fila **Setări entitate**, selectați **Reîmprospătați lista entităților**.
3. Selectați **Închideți** pentru a confirma reîmprospătarea entității.

 > [!NOTE]
 > Aceste proces va dura aproximativ 20 de minute până la finalizare. Veți fi notificat când actualizarea este finalizată.

### <a name="update-dual-write-mappings"></a><a name="run"></a>Actualizați mapările cu scriere duală

1. În spațiul de lucru **Management de date**, selectați **Scriere duală**.
2. Selectați **Aplicați soluții**, selectați ambele soluții din listă, apoi selectați **Aplicați**.
3. Pe pagina **Scriere duală**, selectați următoarele hărți de tabel, apoi selectați **Oprire**.

    - **Integrare valori reale Project Operations (msdyn_actuals)**
    - **Integrarea categoriilor de cheltuieli de proiect Project Operations (msdyn_expensecategories)**
    - **Integrarea entității de export a valorilor reale ale cheltuielilor pentru proiect în Project Operations (msdyn_expensecategories)**

4. Pe pagina **Versiunea hărții tabelului**, aplicați o nouă versiune a hărții fiecăreia dintre cele trei entități.
5. Pe pagina **Scriere duală**, selectați rulare pentru a reporni hărțile.
6. Din lista de hărți, selectați harta **Registru (msdyn_ledgers)** cu toate premisele si selectați caseta de bifare **Sincronizare inițială**. 
7. În câmpul **Master pentru sincronizarea inițială**. selectați **Aplicații pentru finanțe și operațiuni** și apoi selectați **Rulare**.
 
 ![Sincronizarea hărții registrului contabil.](media/DW6.png)
 


[!INCLUDE[footer-include](../includes/footer-banner.md)]