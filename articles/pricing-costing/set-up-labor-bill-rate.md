---
title: Configurarea tarifelor facturii pentru muncă
description: Acest articol oferă informații despre cum să configurați tarifele de facturare a forței de muncă în Operațiuni de proiect.
author: rumant
ms.date: 04/07/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 0ad83e899030be480baed95597e1ccfc0e560e24
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924353"
---
# <a name="set-up-labor-bill-rates"></a>Configurarea tarifelor facturii pentru muncă

_ **Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc

Fiecare listă de prețuri are un set de prețuri de roluri sau rate ale forței de muncă, care sunt eficiente pentru context și intră în vigoare la data inclusă pe antetul listei de prețuri. Tarifele facturilor pentru timp în Dynamics 365 Project Operations pot fi configurate într-o singură monedă, care este moneda din antetul listei de prețuri.

1. Pentru a seta ratele facturii forței de muncă pentru o listă de prețuri de vânzare, accesați **Vânzări** > **Clienți** > **Liste de prețuri** și selectați **Nou** pentru a crea o nouă listă de prețuri. 
2. Pe fila **Prețuri de roluri**, în subgrilă, selectați **Preț nou de rol**. 
3. Pe panoul **Creare rapidă**, introduceți combinația de roluri și unități organizaționale pentru care trebuie să configurați rata facturării.

   Următorul tabel include câmpurile de pe fila **General** și panoul **Creare rapidă** dintr-o linie de preț de rol pe care trebuie să îl aveți în vedere atunci când creați prețuri de rol într-o listă de prețuri de vânzare:

    | Câmp | Locație | Descriere | Impactul din aval |
    | --- | --- | --- | --- |
    | Rol | Fila **General** și panoul **Creare rapidă** | Selectați rolul pentru care setați rata facturii. | Rolul din estimarea de intrare sau real va fi asortat cu această linie pentru a stabili implicit rata de facturare. |
    | Firmă de resurse | Fila **General** și panoul **Creare rapidă** | Selectați compania sau entitatea juridică de unde este rolul. De exemplu, un dezvoltator din Fabrikam India sau un dezvoltator din Fabrikam SUA. | Firma de resurse din estimarea de intrare sau real va fi asortat cu această linie pentru a stabili implicit rata de facturare a rolului. |
    | Unitate de finanțare | Fila **General** și panoul **Creare rapidă** | Selectați unitatea organizațională sau divizia companiei de unde este rolul. De exemplu, un dezvoltator din divizia Robotics din Fabrikam India sau un dezvoltator din divizia Software din Fabrikam USA. | Unitatea de resurse din estimarea de intrare sau real va fi asortat cu această linie pentru a stabili implicit rata de facturare a rolului. |
    | Preț | Fila **General** și panoul **Creare rapidă** | Configurați rata de facturare pentru rolul, compania de resurse și combinația de unități de resurse. De exemplu, un dezvoltator din Fabrikam India are o rată a facturii de 100 USD sau un dezvoltator din Fabrikam SUA are o rată a facturii de 150 USD. | Acest preț este rata de facturare implicită pentru prețul pe unitate al estimării primite sau al liniei reale pentru clasa tranzacției Timp. |
    | Monedă | Fila **General** și panoul **Creare rapidă**| În mod implicit, valoarea monedei provine din moneda din antetul listei de prețuri de vânzări. Într-o listă de prețuri de vânzare, moneda nu poate fi anulată. | Această monedă este moneda implicită pentru prețul pe unitate al liniei reale de vânzări pentru clasa tranzacției Timp. |
    | Planificare unitate | Fila **General** și panoul **Creare rapidă** | Această planificare de unitate este implicit Timp și nu poate fi modificat pe entitatea cu preț de rol, deoarece este utilizat tarifele expres pe unități de timp. | Nu există niciun impact în aval pentru acest câmp. |
    | Unitate | Fila **General** și panoul **Creare rapidă** | Valoarea de unitate vine de la câmpul **Unitate de timp** pe antetul listei de prețuri de vânzare. Dar valoarea poate fi anulată. De exemplu, un dezvoltator din Fabrikam India are rata de facturare de 1000 USD de **Zi de India**. Un dezvoltator din Fabrikam SUA are o rată de facturare de 1500 USD per **Zi SUA**. | Când prețul pe unitate este implicit pe o estimare de intrare sau o linie reală, sistemul utilizează sistemul de unități și conversia în unități de bază pentru a calcula un preț pe unitate. De exemplu, estimarea este pentru o valoare de 10 **Zile de India** de muncă pentru un dezvoltator din India și unitatea, Zi de India este definit ca 10 ore. La stabilirea prețului acelei linii de estimare, aplicația calculează prețul unitar pe estimare ca 1000 USD/10 ore = 100 USD pe oră. |

## <a name="transfer-pricing-or-set-up-bill-rates-for-resources-from-other-organizational-units-or-divisions"></a>Prețurile de transfer sau stabiliți rate de facturare pentru resurse de la alte unități sau divizii organizaționale 

Companiile bazate pe proiecte folosesc adesea angajați din diferite entități juridice și diferite divizii din cadrul entității juridice pentru a lucra la proiecte. Proiectele pot fi executate de la o anumită entitate și divizie juridică, în timp ce angajații sau consultanții care lucrează la proiecte ar putea proveni de la aceeași persoană juridică și divizie sau de la una diferită. Proiectul ar putea fi, de asemenea, alcătuit dintr-o combinație de oameni din diferite entități juridice și divizii. În Project Operations, entitatea juridică care deține livrarea proiectului se numește **Compania deținătoare** iar divizia care deține livrarea se numește **Unitatea Contractantă**. Toate celelalte entități juridice care furnizează resurse se numesc **Companii de resurse** și diviziile care furnizează resursele se numesc **Unități de resurse**. Datorită diferențelor dintre costurile forței de muncă între diverse geografii și piețe ale forței de muncă din întreaga lume, ratele facturilor pentru forța de muncă sunt, de asemenea, stabilite diferit pentru diferite geografii.

De exemplu, un dezvoltator de la divizia de Robotică a Fabrikam India care lucrează la un proiect din SUA este facturat la rata de 100 USD pe oră. Un dezvoltator de la divizia de robotică a Fabrikam US care lucrează la US Project este facturat la 150 USD pe oră. 

### <a name="example-set-up-a-bill-rate"></a>Exemplu: configurați o rată a facturii 

1. Creați o listă de prețuri de vânzare numită *Tarifele facturilor americane Fabrikam* și setați efectivitatea datei.
2. În lista de prețuri de vânzare, introduceți următoarele informații despre tarif:

    | Rol | Firmă de resurse | Unitate resursă | Rata de facturare |
    | --- | --- | --- | --- |
    | Dezvoltator | Fabrikam India | Fabrikam India - Robotics | $100 |
    | Dezvoltator | Fabrikam Filipine | Fabrikam Philippines - Robotics | $90 |
    | Dezvoltator | Fabrikam US | Fabrikam US - Robotics | $150 |

3. Atașați lista de prețuri de vânzare, **Ratele de facturare ale Fabrikam US** la lista de prețuri a proiectului a contractului de proiect sau la un anumit cont.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
