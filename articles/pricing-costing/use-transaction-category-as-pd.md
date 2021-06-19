---
title: Utilizarea categoriei de tranzacții ca dimensiune de preț
description: Acest subiect furnizează informații despre cum să utilizați câmpul Categorie de tranzacție ca dimensiune de preț.
author: rumant
ms.date: 11/05/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d956545e1ad38fb09660f107e085f38d099c2207
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004456"
---
# <a name="use-transaction-category-as-a-pricing-dimension"></a>Utilizarea categoriei de tranzacții ca dimensiune de preț


_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_


Acest subiect explică cum să utilizați câmpul **Categorie de tranzacție** ca dimensiune de preț. 

## <a name="prerequisites"></a>Cerințe preliminare
Înainte de a finaliza procedurile din acest subiect, trebuie să aveți o nouă soluție de dimensiune a prețurilor pentru organizația dvs. Dacă nu ați creat deja unul, consultați [Creați câmpuri și entități personalizate ca dimensiuni de preț](create-custom-fields-entities-pricing-dimensions.md).

## <a name="add-the-transaction-category-field-to-forms-and-views"></a>Adăugați câmpul Categorie de tranzacție la formulare și vizualizări
Pentru a face câmpul **Categoria tranzacției** vizibil în soluția de dimensiune a prețurilor, trebuie să adăugați câmpul la toate formularele și vizualizările ca entitate.

Următorul tabel listează toate formularele și vizualizările predefinite, după entitate. De asemenea, va trebui să adăugați noul câmp la orice formulare sau vizualizări suplimentare din entitățile dvs. personalizate.

|  Entity        | Formulare     |Vizualizări        |
| ------------------------------|---------------------------------|----------------------------------|
|  Preț pentru rol| Informaţii |- Prețuri categorii de resurse active<br> - Preț asociat de categorii de resurse |
|  Adaos de preț pentru rol| Informaţii|- Adaos la prețul de rol activ<br>- Adaos asociat la preț de rol |
|  Detaliu linie de ofertă|- Informații proiect<br>- Creare rapidă proiect| - Detaliu linie de ofertă activă<br>- Detalii de linie ofertă combinate<br>- Detaliu asociat de linie de ofertă |
|  Detaliu linie contract pentru proiect|- Informații proiect<br>- Creare rapidă proiect|- Detalii din linie de contract combinate<br>- Detalii linie de contract active<br>- Detaliu asociat din linia de contract |
|  Activitate de proiect|- Informaţii<br>- Formular nou| &nbsp; |
|  Membru echipă de proiect|- Informaţii<br>- Formular nou|- Membri echipă de proiect activi<br>- Membrii echipei de proiect<br>- Membri echipei de proiect asociate |
|  Intrare de timp|- Informaţii<br>- Creare intrare de timp|- Intrările mele de timp după dată<br>- Intrările mele de timp pentru această săptămână<br>- Intrări de timp pentru aprobare|
|  Linie de jurnal|- Informaţii<br>- Creare rapidă|- Linii de jurnal active<br>- Linie de jurnal asociată|
|  Detaliu linie factură|- Informaţii<br>- Creare rapidă|- Detalii de linie factură active<br>- Tranzacții de factură facturabile<br>- Tranzacții de factură gratuite<br>- Detalii asociate de linie de factură <br>- Tranzacții de factură nefacturabilă|
|  Real|- Informaţii<br>- Valori reale active| Valoare reală asociată |

## <a name="set-up-the-transaction-category-field-as-a-pricing-dimension"></a>Configurarea câmpului Categorie de tranzacție ca dimensiune de preț

1. Accesați **Setări** > **Parametri**. 
2. Pa pagina **Parametri**, pe fila **Dimensiuni prețuri bazate pe sumă**, verificați ca grila de pe filă afișează înregistrările din entitatea **Dimensiuni preț**.
3. Adăugați **Categorie de tranzacții** la această listă și setați câmpurile **Aplicabil la cost** și **Aplicabil la vânzare** la **Da**.
4. În câmpul **Tip dimensiune** selectați **Bazat pe sumă**, apoi selectați prioritatea pentru **Categoria de tranzacții** întrucât se referă la cost și vânzări.


[!INCLUDE[footer-include](../includes/footer-banner.md)]