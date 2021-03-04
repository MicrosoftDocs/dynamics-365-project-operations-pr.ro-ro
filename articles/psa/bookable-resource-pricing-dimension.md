---
title: Utilizați resursa care se poate rezerva ca dimensiune de tarifare
description: Acest subiect furnizează informații despre utilizarea unei resurse rezervabile ca dimensiune de tarifare.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: d9b25a768f892d83c09d37ce76291d6c8e75b1be
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145013"
---
# <a name="use-bookable-resource-as-a-pricing-dimension"></a>Utilizați resursa care se poate rezerva ca dimensiune de tarifare

[!include [banner](../includes/psa-now-project-operations.md)]

Acest subiect furnizează informații despre utilizarea unei resurse rezervabile ca dimensiune de tarifare. Înainte de a începe, dacă nu ați creat deja o soluție de dimensiune de preț, va trebui să creați una nouă. Dacă aveți deja o soluție de dimensiune de preț, atunci puteți face modificările în această soluție. Dacă nu ați creat o nouă soluție de dimensiune de preț pentru organizația dvs., finalizați procedurile din subiectul [Creare câmpuri și entități particularizate](create-custom-fields-entities.md).

## <a name="add-bookable-resource-to-forms-and-views"></a>Adăugați o resursă rezervabilă la formulare și vizualizări
Pentru a face câmpurile vizibile în interfața cu utilizatorul în soluția de dimensiune de tarifare, va trebui să parcurgeți toate formularele și vizualizările entităților cheie Project Service și să adăugați aceste câmpuri la formularele și vizualizările acelor entități.
Următorul tabel este o listă cuprinzătoare a formularelor și vizualizărilor predefinite, enumerate după entitate, care vor trebui actualizate. Dacă există vizualizări sau formulare suplimentare în particularizările acestor entități, adăugați noile câmpuri și la acelea.
Deschideți exploratorul de soluții pentru soluția de dimensiune de tarifare și apoi faceți clic pe **Publicare toate particularizările**.


|   Entitate        | Formulare   |Vizualizări        |
| ------------------------------|---------------------------------|----------------------------------|
|  Preț pentru rol|• Informații |• Prețuri categorii de resurse active<br> • Vizualizare asociată prețuri categorii de resurse|
|  Adaos de preț pentru rol|• Informații|• Adaos la prețul de rol activ<br>• Vizualizare asociată adaosului la prețurile de rol|
|  Detaliu linie de ofertă|• Informații proiect<br>• Creare rapidă proiect|• Detaliu linie de ofertă activă<br>• Detalii de linie ofertă combinate<br>• Vizualizare asociată a detaliilor de linie ofertă|
|  Detaliu linie contract pentru proiect|• Informații proiect<br>• Creare rapidă proiect|• Detalii din linie de contract combinate<br>• Detalii linie de contract active<br>• Vizualizare asociată pentru detalii din linia de contract|
|  Activitate de proiect|• Informații<br>• Formular nou||
|  Membru echipă de proiect|• Informații<br>• Formular nou|• Membri echipă de proiect activi<br>• Membri echipă de proiect<br>• Vizualizare asociată membri echipă de proiect|
|  Intrare de timp|• Informații<br>• Creare intrare de timp|• Intrările mele de timp după dată<br>• Intrările mele de timp pentru această săptămână<br>• Intrări de timp pentru aprobare.|
|  Linie de jurnal|• Informații<br>• Creare rapidă|• Linii de jurnal active<br>• Vizualizare asociată linie de jurnal|
|  Detaliu linie factură|• Informații<br>• Creare rapidă|• Detalii de linie factură active<br>• Tranzacții de factură facturabile<br>• Tranzacții de factură gratuite<br>• Vizualizare asociată a detaliilor de linie factură<br>• Tranzacție de factură nefacturabilă|
|  Real|• Informații<br>• Valori reale active|• Vizualizare asociată valori reale|

## <a name="set-up-bookable-resource-as-a-pricing-dimension"></a>Configurați resursa care se poate rezerva ca dimensiune de tarifare

1. În interfața web, accesați **Project Service** > **Setări** > **Parametri**. Pa pagina **Parametri**, în fila **Dimensiuni de tarifare bazate pe sumă**, observați că grila de pe filă afișează înregistrările din entitatea Dimensiuni de tarifare. 
2. Adăugați **Resursă rezervabilă** la această listă de dimensiuni de tarifare ca **msdyn_bookableresource**. 
3. Indicați contextul în care resursa care se poate rezerva funcționează ca dimensiune de tarifare și setați valorile **Aplicabilă costurilor** și **Aplicabilă vânzărilor**.
4. În câmpul **Tip dimensiune**, selectați **Pe bază de sumă**. 
5. Selectați prioritatea de cost și de vânzări pentru resursa care se poate rezerva. De obicei, atunci când este inclusă ca o dimensiune de tarifare, o resursă care se poate rezerva are cea mai mare prioritate, așa că setarea acesteia la **1** (sau **0**, în funcție de modul în care numerotați prioritatea) ar asigura acel comportament.

## <a name="set-up-pricing-dimension-field-names"></a>Configurați numele de câmpuri pentru dimensiunea de tarifare

Când numele câmpului unei dimensiuni de tarifare din tabelul **Preț pentru rol** este diferit de numele său de câmp în oricare dintre celelalte entități unde trebuie să funcționeze valoarea implicită a prețului, înregistrarea dimensiunii de tarifare trebuie să fie informată cu privire la numele diferite.    
Pentru resursa care poate fi rezervată, entitatea **Membri echipă de proiect** are un nume de câmp ușor diferit (**msdyn_bookableresourceid**) față de denumirea din entitatea **Preț pentru rol** (**msdyn_ bookableresource**). Înregistrarea dimensiunii de tarifare pentru **msydn_bookableresource** trebuie să fie informată despre acest lucru. 
1. Pentru aceasta, faceți dublu clic pe rândul din grila de **Dimensiuni de tarifare** pentru a deschide pagina de dimensiuni a **msdyn_bookableresource**.
2. Pe pagina de dimensiuni, în fila **Corelate**, faceți clic pe **Nume câmpuri de dimensiune de tarifare**.

 ![Fila Nume câmpuri de dimensiune de tarifare](media/PD-fieldname.png)

4. În vizualizarea asociată care se deschide, faceți clic pe **Adăugare nume câmp dimensiune de tarifare nou**.

 ![Adăugați nume de câmpuri de dimensiune de tarifare noi](media/Add-NewPD-fieldname.png)


Acest lucru deschide pagina **Nume câmp dimensiune de tarifare nou** pentru **msdyn_bookableresource**. 

5. Adăugați **msdyn_projectteam** la câmpul **Nume logic al entității** și **msdyn_bookableresourceid** la câmpul **Nume câmp**. Salvaţi înregistrarea.

 ![Formular pentru nume de câmpuri de dimensiune de tarifare noi](media/PD-fieldname-Added.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]