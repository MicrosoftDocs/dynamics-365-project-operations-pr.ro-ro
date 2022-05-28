---
title: Creați o echipă de proiect
description: Acest subiect oferă informații despre cum să creați și să gestionați echipe de proiect.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f134d7566954e640eea8ff8af98e184273ad570c
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 05/04/2022
ms.locfileid: "8683047"
---
# <a name="create-a-project-team"></a>Crearea unei echipe de proiect

[!include [banner](../includes/banner.md)]

Pentru a utiliza rolurile care au fost configurate anterior într-un proiect, un manager de proiect trebuie să asocieze rolurile cu proiectul. Pentru un proiect pot fi atribuite mai multe roluri. Pentru a preveni confuzia, aceste roluri sunt etichetate automat în timpul rezervării. De exemplu, dacă managerul de proiect necesită trei ingineri software, trei roluri de inginer software care au etichetele **inginer software 1**, **inginer software 2**, și **inginer software 3** sunt generate automat. Când caracteristicile rolului au fost setate anterior pentru rol, acestea sunt aplicate ca filtru în timpul căutărilor unei resurse. Pot fi adăugate caracteristici suplimentare, după cum este necesar, pentru a rafina în continuare căutarea.

Setările de vizualizare pot fi, de asemenea, personalizate pentru a oferi o imagine mai bună a disponibilității resurselor. Există opțiuni pentru a afișa disponibilitatea orară, zilnică, săptămânală, lunară, trimestrială și anuală. Există, de asemenea, o opțiune pentru a arăta capacitatea disponibilă și rămasă pentru resurse. Această opțiune este utilă pentru gestionarea timpului, atunci când estimați timpul disponibil pentru activități sau disponibilitatea resurselor.

Managerul de proiect poate selecta un rol pe pagină și apoi, dacă există o resursă disponibilă care se potrivește cerinței, selectează să rezerve o resursă pentru a ocupa rolul. Rețineți că resursele nu trebuie rezervate în acest moment în etapa de planificare. Când creați un WBS, puteți înlocui rolurile cu resurse de personal pentru proiect. Dacă rolurile sunt înlocuite cu resurse de personal în WBS, configurarea resurselor actualizează automat lista și programarea echipei de proiect.

[![Listarea echipei de proiect care include atât roluri, cât și resurse reale.](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

Managerul de proiect are diverse opțiuni pentru rezervarea unei resurse pentru un proiect, cum ar fi **Capacitate rămasă**, **Capacitate completă**, **Procent de capacitate**, și **Specificare ore**. Aceste opțiuni de rezervare pot fi anulate în orice moment în cazul în care se schimbă atribuirea resurselor. Sunt acceptate două tipuri de rezervări:

- **Rezervare fermă** - Rezervarea resurselor a fost aprobată și confirmată pentru a lucra la implicare pe durata specificată.
- **Rezervare provizorie** - Rezervarea resurselor a fost stabilită provizoriu pentru a lucra la implicare pe durata specificată.

Următoarea procedură explică cum se creează o echipă de proiect.

## <a name="create-a-project-team"></a>Crearea unei echipe de proiect

1. Din pagina listă **Toate proiectele**, selectați un proiect, apoi selectați **Editare**.
2. Din fila **Echipa proiectului și planificarea**, în câmpul **Data de încheiere a planificării**, introduceți data de începere a planificării plus o lună. De exemplu, dacă data de începere a planificării este 24 iunie 2017 (24/06/2017), introduceți **24/07/2017**.
3. Selectați **Adăugare**.
4. În panoul **Adăugare roluri la proiect**, în câmpul **Rol**, selectați **Manager de proiect senior**.
5. Selectați **Competențe necesare**.
6. Din pagina **Alegere caracteristici**, caracteristicile pe care le-ați setat anterior pentru rolul de manager de proiect senior sunt selectate în mod implicit. Selectați **OK**.
7. Din pagina **Adăugare roluri la proiect**, în câmpul **Număr de resurse**, introduceți **1**.
8. În câmpul **Resursă**, căutarea arată toate resursele care au competențele necesare. Selectați **Daniel Goldschmidt**, apoi selectați **Creare**.
9. În pagina **Proiect**, selectați **Adăugare**.
10. În panoul **Adăugare roluri la proiect**, în câmpul **Rol**, selectați **Membru al echipei**. În câmpul **Număr de resurse**, introduceți **5**.
11. Selectați **Creare**.
12. Din pagina **Proiecte**, selectați **Completați resursa**.

## <a name="monitor-project-teams"></a>Monitorizarea echipelor de proiect
1. Din pagina **Toate proiectele**, selectați linkul **ID proiect** pentru proiectul **Faza 2 de upgrade XYZ**.
2. Din fila rapidă **Echipa proiectului și planificarea**, verificați dacă resursele proiectului ce sunt listate sunt corecte.


[!INCLUDE[footer-include](../includes/footer-banner.md)]