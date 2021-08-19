---
title: Utilizarea unei resurse care se poate rezerva ca dimensiune de preț
description: Acest subiect furnizează informații despre cum să utilizați o resursă care se poate rezerva ca dimensiune de tarifare.
author: Rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1e8487d3d32acab294bb2de16fb0278f357f774e62b553eb0c1ebd5b6246e332
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/06/2021
ms.locfileid: "6996271"
---
# <a name="use-a-bookable-resource-as-a-pricing-dimension"></a>Utilizarea unei resurse care se poate rezerva ca dimensiune de preț

 _**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_ 

Acest subiect furnizează informații despre cum să utilizați o resursă care se poate rezerva ca dimensiune de tarifare. Dacă strategia dvs. de stabilire a prețurilor este configurată astfel încât fiecare resursă rezervabilă să aibă un anumit preț sau o rată de cost, utilizați o resursă rezervabilă ca dimensiune de stabilire a prețurilor.

## <a name="prerequisites"></a>Cerințe preliminare
Înainte de a finaliza procedurile din acest subiect, trebuie să aveți o nouă soluție de dimensiune a prețurilor pentru organizația dvs. Dacă nu ați creat deja unul, consultați [Creați câmpuri și entități particularizate](../pricing-costing/create-custom-fields-entities-pricing-dimensions.md).

## <a name="add-the-bookable-resource-field-to-forms-and-views"></a>Adăugați câmpul Resursă care se poate rezerva la formulare și vizualizări
Pentru a face câmpul **Resursă care se poate rezerva** vizibil în soluția de dimensiune a prețurilor, trebuie să adăugați câmpul la toate formularele și vizualizările ca entitate.

Următorul tabel listează toate formularele și vizualizările predefinite, după entitate. De asemenea, va trebui să adăugați noul câmp la orice formulare sau vizualizări suplimentare din entitățile dvs. personalizate.

|   Entity        | Formulare   |Vizualizări        |
| ------------------------------|---------------------------------|----------------------------------|
|  Preț pentru rol| Informaţii | - Prețuri categorii de resurse active<br> - Preț asociat de categorii de resurse |
|  Adaos de preț pentru rol| Informaţii| - Adaos la prețul de rol activ<br>- Adaos asociat la preț de rol |
|  Detaliu linie de ofertă| - Informații proiect<br>- Creare rapidă proiect| - Detaliu linie de ofertă activă<br>- Detalii de linie ofertă combinate<br>- Detaliu asociat de linie de ofertă |
|  Detaliu linie contract pentru proiect| - Informații proiect<br>- Creare rapidă proiect| - Detalii din linie de contract combinate<br>- Detalii linie de contract active<br>- Detaliu asociat din linia de contract |
|  Activitate de proiect| - Informaţii<br>- Formular nou| &nbsp; |
|  Membru echipă de proiect| - Informaţii<br>- Formular nou| - Membri echipă de proiect activi<br>- Membrii echipei de proiect<br>- Membri asociați ai echipei de proiect |
|  Intrare de timp| - Informaţii<br>- Creare intrare de timp| - Intrările mele de timp după dată<br>- Intrările mele de timp pentru această săptămână<br>- Intrări de timp pentru aprobare|
|  Linie de jurnal| - Informaţii<br>- Creare rapidă| - Linii de jurnal active<br>- Linie de jurnal asociată |
|  Detaliu linie factură| - Informaţii<br>- Creare rapidă| - Detalii de linie factură active<br>- Tranzacții de factură facturabile<br>- Tranzacții de factură gratuite<br>- Detalii asociate de linie de factură <br>- Tranzacții de factură nefacturabilă|
|  Real| - Informaţii<br>- Valori reale active| Valoare reală asociată |

## <a name="set-up-a-bookable-resource-as-a-pricing-dimension"></a>Configurați o resursă care se poate rezerva ca dimensiune de tarifare
Pentru a configura o resursă care se poate rezerva ca dimensiune de tarifare, urmați acești pași:

1. Accesați **Setări** > **Parametri**. 
2. Pa pagina **Parametru**, pe fila **Dimensiuni prețuri bazate pe sumă**, verificați ca grila de pe filă afișează înregistrările din entitatea **Dimensiuni preț**. 
2. Adăugați **Resursă rezervabilă** la această listă de dimensiuni de tarifare ca **msdyn_bookableresource**. 
3. În **Aplicabil costurilor** și **Aplicabil vânzărilor**, selectați o valoare.
4. În **Tip dimensiune**, selectați **Pe bază de sumă**. 
5. Selectați prioritatea de cost și de vânzări pentru resursa care se poate rezerva. De obicei, o resursă care se poate rezerva are cea mai mare prioritate atunci când este inclusă ca dimensiune de stabilire a prețurilor. Setați prioritatea la **1** (sau **0** în funcție de modul în care numărați prioritatea) pentru a asigura acest comportament.

## <a name="set-up-pricing-dimension-field-names"></a>Configurați numele de câmpuri pentru dimensiunea de tarifare

Când numele câmpului unei dimensiuni de tarifare din tabelul **Preț pentru rol** este diferit de numele său de câmp în oricare dintre celelalte entități unde prețul implicit este utilizat, înregistrarea dimensiunii de preț trebuie să fie notificată de diferitele nume.  

Pentru o resursă care poate fi rezervată, entitatea **Membrii echipei de proiect** are un nume de câmp ușor diferit de denumirea din entitatea **Preț de rol**: 

 - Entitatea **Membrii echipei de proiect** = **msdyn_bookableresourceid**
 - Entitatea **Preț de rol** = **msdyn_bookableresource**

Înregistrarea dimensiunii de tarifare pentru **msydn_bookableresource** trebuie să fie notificată despre această diferență.

1. Faceți dublu clic pe rândul din grila de **Dimensiuni de tarifare** pentru a deschide pagina de dimensiuni a **msdyn_bookableresource**.
2. Pe pagina de dimensiuni, în fila **Corelate**, selectați **Nume câmpuri de dimensiune de tarifare**.

  ![Fila Nume câmpuri de dimensiune de tarifare.](media/PD-fieldname.png)

3. În vizualizarea asociată care se deschide, selectați **Adăugare nume câmp dimensiune de tarifare nou**.

  ![Adăugați nume de câmpuri de dimensiune de tarifare noi.](media/Add-NewPD-fieldname.png)

  Acest lucru deschide pagina **Nume câmp dimensiune de tarifare nou** pentru **msdyn_bookableresource**. 

4. Pe pagina **Nume câmp dimensiune dimensiune nouă**, adăugați **msdyn_projectteam** la **Nume logic al entității**.
5. Adăugați  **msdyn_bookableresourceid** la **Nume de câmp**.

 ![Formular pentru nume de câmpuri de dimensiune de tarifare noi.](media/PD-fieldname-Added.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]