---
title: Utilizarea categoriei de tranzacții ca dimensiune de preț
description: Acest articol oferă informații despre utilizarea unei categorii de tranzacții ca dimensiune de preț.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 1a1c2dc17c2092e5364d90e7efc1f13aee80703e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915751"
---
# <a name="use-transaction-category-as-a-pricing-dimension"></a>Utilizarea categoriei de tranzacții ca dimensiune de preț

[!include [banner](../includes/psa-now-project-operations.md)]

Acest articol arată cum să utilizați o categorie de tranzacție ca dimensiune de preț. Înainte de a începe, dacă nu ați creat deja o soluție de dimensiune de preț, va trebui să creați una nouă. Dacă aveți deja o soluție de dimensiune de preț, atunci puteți face modificările în această soluție. Dacă nu ați creat o nouă soluție de dimensiune de preț pentru organizația dvs., finalizați procedurile din [Creați câmpuri și entități personalizate](create-custom-fields-entities.md) articol.

## <a name="add-transaction-category-to-forms-and-views"></a>Adăugați o categorie de tranzacții la formulare și vizualizări
Pentru a face categoria de tranzacții vizibilă în interfața cu utilizatorul în soluția de dimensiune de preț, va trebui să parcurgeți toate formularele și vizualizările entităților cheie și să adăugați aceste câmpuri la formularele și vizualizările acelor entități.
Următorul tabel este o listă cuprinzătoare a formularelor și vizualizărilor predefinite, listate per entitate, care vor trebui actualizate cu noile câmpuri. Dacă există vizualizări sau formulare suplimentare în particularizările acestor entități, adăugați noile câmpuri și la acelea.

|  Entitate        | Formulare     |Vizualizări        |
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

## <a name="set-up-transaction-category-as-a-pricing-dimension"></a>Configurarea categoriei de tranzacții ca dimensiune de preț

1. În interfața web, accesați **Project Service** > **Setări** > **Parametri**. 
2. Pa pagina **Parametri**, pe fila **Dimensiuni prețuri bazate pe sumă**, observați că grila de pe filă afișează înregistrările din entitatea **Dimensiuni preț**.
3. Adăugați **Categorie de tranzacții** la această listă și setați câmpurile **Aplicabil la cost** și **Aplicabil la vânzare** la **Da**.
4. În câmpul **Tip dimensiune** selectați **Bazat pe sumă**, apoi selectați prioritatea pentru **Categoria de tranzacții** referitoare la cost și vânzări.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
