---
title: Unități și grupuri de unități
description: Acest subiect oferă informații despre unități și grupuri de unități.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 6620c99563394d1f3881d6bfdb72d01c1c4e8d6f
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145598"
---
# <a name="unit-groups-and-units"></a>Unități și grupuri de unități

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Grupurile de unități și unitățile sunt entități de bază în Microsoft Dynamics 365. O unitate este o singură unitate de măsură și mai multe unități pot fi grupate în grupuri de unități. Un grup de unități este denumit uneori planificare a unităților în interfața cu utilizatorul (IU) Dynamics 365. 

Iată câteva exemple de unități și grupuri de unități:
 
- **Grup de unități**: Distanță 
    - **Unități**: Milă, Kilometru și așa mai departe.
- **Grup de unități**: Timp
    - **Unități**: oră, zi, săptămână și așa mai departe. 

Când configurați mai multe unități într-un grup de unități, trebuie să configurați și un factor de conversie între ele, desemnând prima unitate pe care ați configurat-o ca unitatea implicită sau principală pentru grupul de unități. 

De exemplu, într-un grup de unități **Timp**, dacă configurați **Oră** ca prima unitate, sistemul desemnează **Oră** drept unitatea implicită. Dacă unitatea următoare pe care ați configurat-o este **Zi**, trebuie să configurați un factor de conversie pentru **Zi** la **Oră**. Dacă apoi adăugați **Săptămână** ca o a treia unitate, trebuie să configurați un factor de conversie pentru **Săptămână** în termeni de **Zi** sau de **Oră**. 

Următoarea imagine afișează un exemplu de configurare pentru unitatea **Zi**, unde câmpul **Cantitate** afișează numărul de ore dintr-o zi, și pentru **Săptămână**, unde câmpul **Cantitate** afișează numărul de zile care sunt într-o săptămână.

> ![Grup de unități: Pagina de informații](media/advanced-2.png)

## <a name="using-units-and-unit-groups"></a>Utilizarea unităților și grupurilor de unități

Dynamics 365 Project Service Automation utilizează unități și grupuri de unități pentru a procesa estimări și intrări atât pentru cheltuieli, cât și pentru timp. 

Pentru cheltuieli, fiecare categorie de cheltuieli are un grup de unități și o unitate implicite. Aceste valori sunt introduse ca valori implicite în intrările listei de prețuri pentru categoriile de cheltuieli. 

De exemplu, aveți o categorie de cheltuieli care este numită **Kilometraj**. Ea are un grup de unități care este numit **Distanță** și o unitate implicită, care este numită **Kilometru**. Dacă ați configurat grupul de unități **Distanță** astfel încât acesta are două unități (**Kilometru** și **Milă**), puteți seta două prețuri pentru categoria **Kilometraj** pe o listă de prețuri: prețul pe kilometru și prețul pe milă.

| Categorie de cheltuieli  | Grup de unități  | Unitate      | Metodă de stabilire a prețului  | Preț unitar  |
|-------------------|---------------|-----------|-------------------|-------------------|
| Kilometraj           | Distanța      | Milă      | Preț unitar    | 10 USD            |
| Kilometraj           | Distanța      | Kilometru | Preț unitar    |  6 USD            |

Când introduceți o cheltuială pe un proiect, sistemul stabilește prețul prin combinarea categoriei și a unității de pe cheltuială. 

| Descriere cheltuială        | Categorie de cheltuieli  | Unitate  | Cantitate  | Preț unitar   |
|----------------------------|---------------------|-------|-----------|----------------|
| Condu la locația clientului | Kilometraj             | Milă  | 10        | 10 USD         |

Pentru timp, fiecare antet de listă de prețuri are un câmp **Unitate de timp implicită**. Valoarea este setată atunci când creați antetul listei de prețuri. Această unitate este apoi utilizată pentru a seta toate prețurile bazate pe roluri de pe acea listă de prețuri.

Liniile de estimare pentru câmpul **Timp în ofertă** pot fi exprimate în orice unitate de timp. Cu toate acestea, liniile de estimare pe proiecte și intrările de timp pentru proiecte pot utiliza numai unitatea de timp **Oră**. Dacă unitatea din intrarea de timp sau linia de estimare nu corespunde unității din linia listei de prețuri pentru rolul respectiv, sistemul convertește prețul la unitățile care sunt definite în estimarea proiectului sau în tranzacția efectivă a proiectului.

Următorul exemplu arată modul în care PSA utilizează grupul de unități, unitățile și factorii de conversie.
- Unităţi

   - **Grup de unități**: Timp 
   - **Unități**: Oră 
    
    - **Zi** – factor de conversie: 8 ore       
    - **Săptămână** – factor de conversie: 40 de ore  
        
- Configurare listă de prețuri pe proiectul A:

    - **Nume**: prețurile de vânzare în Regatul Unit pe 2016 
    - **Unitate de timp implicită**: Zi 
    - **Monedă**: GBP

| Rol      | Grup de unități | Unitate | Unitate organizațională | Preț   |
|-----------|------------|------|---------------------|---------|
| Dezvoltator | Time       | Day  | Contoso Regatul Unit          | 800 GBP |

### <a name="time-entry"></a>Intrare de timp

Următorul tabel afișează tranzacția de pe partea de vânzări rezultată, creată de PSA pentru un proiect de trei ore.


| Proiect   | Sarcină    | Rol      | Cantitate | Unitate  | Preț unitar | Volum de vânzări nefacturate |
|-----------|---------|-----------|----------|-------|------------|-----------------------|
| Proiect A | Proiect  | Dezvoltator | 3        | Hour  | 100 GBP    | 300 GBP               |

## <a name="time-unit-faq"></a>Întrebări frecvente despre unitatea de timp

### <a name="does-psa-convert-to-different-units-in-the-case-of-expenses"></a>PSA convertește în diferite unități în cazul cheltuielilor?
Nu. Conversia unităților funcționează doar pentru timp. Pentru cheltuieli, în cazul în care sistemul nu poate găsi un preț pentru combinația dintre categoria de cheltuieli și unitate, prețul este setat la 0,00 în mod implicit.

### <a name="why-does-psa-convert-time-units"></a>De ce convertește PSA unitățile de timp?
În unele țări sau regiuni, există o cerință legală ca ratele de facturare să fie configurate în zile. Negocierea prețurilor și reducerea lor în timpul ciclului de ofertă se face prin utilizarea ratelor zilnice pentru fiecare rol facturabil. Estimarea planificării și intrarea de timp sunt realizate în ore. Pentru a sprijini această diferență în unități de timp, PSA convertește unități de timp.

### <a name="can-time-units-be-changed-on-project-estimates"></a>Pot fi schimbate unitățile de timp pe estimările proiectului?
Nu. Estimarea planificării este momentan limitată la ore și nu poate fi schimbată.

### <a name="can-units-and-unit-groups-be-edited-deleted-and-added"></a>Pot fi editate, șterse și adăugate unitățile și grupurile de unități?
Da. Cu excepția grupului de unități **Timp** și a unității **Oră**, toate unitățile pot fi șterse sau editate, iar unitățile noi pot fi adăugate. În PSA, grupul de unități **Timp** și unitatea **Oră** nu pot fi șterse. Cu toate acestea, ele pot fi actualizate cu un text tradus pentru câmpul **Nume**.
