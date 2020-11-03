---
title: Adăugarea câmpurilor solicitate particularizate la configurarea prețurilor și la entitățile tranzacționale
description: Acest subiect oferă informații despre cum să adăugați referințe de câmp personalizate obligatorii la entități și la formulare și vizualizări.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: e589465eb98723b3b49c5d96e263eb3abf15eb2c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082836"
---
# <a name="add-required-custom-fields-to-price-setup-and-transactional-entities"></a>Adăugarea câmpurilor solicitate particularizate la configurarea prețurilor și la entitățile tranzacționale

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Acest subiect presupune că ați finalizat procedurile în subiect, [Creare câmpuri și entități particularizate pentru a fi utilizate ca dimensiuni de preț](create-custom-fields-entities-pricing-dimensions.md). Dacă nu ați finalizat aceste proceduri, reveniți și completați-le și apoi reveniți la acest subiect. 

În acest subiect, procedurile vă vor arăta cum să adăugați referințele câmpului particularizat necesar la entități și la elementele interfeței utilizator (UI), cum ar fi formulare și vizualizări.

## <a name="add-custom-pricing-dimension-fields"></a>Adăugarea câmpurilor de dimensiune a prețului particularizate 
După ce au fost create câmpuri și entități particularizate, următorul pas este de a face parametrizarea prețurilor și entitățile tranzacționale conștiente de orice entități particularizate sau seturi de opțiuni prin crearea de câmpuri de referință. În funcție de faptul dacă lista dimensiunilor prețurilor include dimensiunile setului de opțiuni sau dimensiunile entității sau ambele, urmați numai pașii din **Dimensiunile de prețuri particularizate bazate pe setul de opțiuni** de preț particularizate bazate pe set de opțiuni sau **Dimensiunile de prețuri particularizate bazate pe entitate** sau ambele, respectiv.

### <a name="option-set-based-custom-pricing-dimensions"></a>Dimensiunile de prețuri particularizate bazate pe setul de opțiuni
Atunci când o dimensiune de prețuri particularizată este bazată pe un set de opțiuni, adăugați-o ca un câmp la entități-cheie. În următoarea procedură **Locație de lucru resursă** și **Ore de lucru resursă** sunt utilizate ca dimensiuni de prețuri pe baza setului de opțiuni. Acestea trebuie mai întâi adăugate sub formă de câmpuri la entitățile tarifare **Preț pentru rol** și **Adaos de preț pentru rol**.

1. În Project Operations, selectați **Setări** > **Soluții** și faceți clic dublu pe **\<your organization name> dimensiuni de prețuri**. 
2. În Explorator soluții, în panoul de navigare din stânga, selectați **Entități > Preț de rol**.
3. Extindeți entitatea **Preț de rol** și selectați **Câmpuri**.
4. Selectați **Nou** pentru a crea un câmp nou denumit **Locație de lucru resursă** și selectați **Set de opțiuni** ca tip de câmp. 
5. Selectați **Se utilizează un set de opțiuni existent** , selectați setul de opțiuni **Locație de lucru resursă** , apoi selectați **Salvare**.
6. Repetați pașii 1-5 pentru a adăuga acest câmp la entitatea **Adaos de preț pentru rol**. 
7. Repetați pașii 1-5 pentru setul de opțiuni **Ore de lucru resursă**.

> [!IMPORTANT]
> Când adăugați un câmp la mai multe entități, utilizați același nume de câmp pentru toate entitățile. 

În fazele de vânzări și de estimare pentru un proiect, estimările efortului de lucru necesar pentru finalizarea lucrărilor **Locale** și **La fața locului** , în **Ore normale** și **Ore suplimentare** sunt utilizate pentru a estimarea valorii ofertei/proiectului. Câmpurile **Locația de lucru resursă** și **Ore de lucru resursă** vor fi adăugate la entități de estimare **Detaliu linie de ofertă** , **Detaliu linie de contract** , **Membru echipă de proiect** și **Linie estimată**.

1. În Project Operations, selectați **Setări** > **Soluții** și apoi faceți clic dublu pe **\<your organization name> dimensiuni de prețuri**. 
2. În Explorator soluții, din panoul de navigare din stânga, selectați **Entități > Detaliu linie de ofertă**.
3. Extindeți entitatea **Detaliu linie de ofertă** și selectați **Câmpuri**.
4. Selectați **Nou** pentru a crea un câmp nou denumit **Locație de lucru resursă** și selectați tipul de câmp, **Set de opțiuni**. 
5. Selectați **Se utilizează un set de opțiuni existent** și **Locație de lucru resursă** , apoi selectați **Salvare**.
6. Repetați pașii 1-5 pentru a adăuga acest câmp la **Detaliu linie contract pentru proiect** , **Membru echipă de proiect** și **Linie estimată**.
7. Repetați pașii 1-6 pentru setul de opțiuni **Ore de lucru resursă**. 

Pentru livrare și facturare, lucrarea finalizată trebuie să fie evaluate cu exactitate pentru a selecta dacă a fost efectuată **Local** sau **La fața locului** și dacă a fost finalizată în timpul **Orelor obișnuite** sau în timpul **Orelor suplimentare** cu privire la Valorile reale ale proiectului. Câmpurile **Locația de lucru resursă** și **Ore de lucru resursă** ar trebui adăugate la entitățile **Intrare de timp** , **Real** , **Detaliu linie factură** și **Linie de jurnal**.

1. Selectați **Setări** > **Soluții** și apoi faceți clic dublu pe **\<your organization name> dimensiuni de preț**.
2. În Explorator soluții, în panoul de navigare din stânga, selectați **Entități > Intrare de timp**.
3. Extindeți entitatea **Detaliu linie de ofertă** , iar apoi selectați **Câmpuri**.
4. Selectați **Nou** pentru a crea un câmp nou denumit **Locație de lucru resursă** și selectați **Set de opțiuni** ca tip de câmp. 
5. Selectați **Se utilizează un set de opțiuni existent** , selectați setul de opțiuni **Locație de lucru resursă** , apoi selectați **Salvare**.
6. Repetați pașii 1-5 pentru a adăuga acest câmp la entitățile **Real** , **Detaliu linie factură** și **Linie jurnal**.
7. Repetați pașii 1-6 pentru setul de opțiuni **Ore de lucru resursă**. 

Aceasta încheie modificările schemei necesare pentru dimensiunile particularizate bazate pe setul de opțiuni.

## <a name="entity-based-custom-pricing-dimensions"></a>Dimensiuni tarifare particularizate bazate pe entitate

Când dimensiunea de tarifare particularizată este o entitate, veți adăuga relații 1:N între entitatea de dimensiune și entitățile-cheie. Utilizând exemplul Titlu standard de sus, vă puteți aștepta ca fiecărui angajat i se atribuie un titlu standard. Drept urmare, veți avea nevoie de o relație 1:N de la Titlul standard la Resursă ce se poate rezerva sau o relație N:1 dacă s-au creat din Resursă ce se poate rezerva la Titlul standard.

1. În Project Operations, selectați **Setări** > **Soluții** și apoi faceți clic dublu pe **\<your organization name> dimensiuni de prețuri**. 
2. În Explorator soluții, în panoul de navigare din stânga, selectați **Entități > Titlu standard**.
3. Extindeți entitatea **Titlu standard** și selectați **Relații 1: N**.
4. Selectați **Nou** pentru a crea o relație nouă 1: N numită **Titlu standard pentru Resursă ce se poate rezerva**. Introduceți informațiile solicitate și apoi selectați **Salvare**.

Titlul standard va trebui adăugat, de asemenea, la entitățile de preț, **Preț pentru rol** și **Adaos de preț pentru rol**. Acest lucru este finalizat, de asemenea, utilizând relațiile 1: N între entitățile **Titlul standard** și **Preț pentru rol** și **Titlul standard** și **Adaos de preț pentru rol**.

1. În Explorator soluții, în panoul de navigare din stânga, selectați **Entități > Titlu standard**.
2. Extindeți entitatea **Titlu standard** și selectați **Relații 1: N**.
3. Selectați **Nou** pentru a crea o nouă relație 1:N numită **Titlu standard la Preț pentru rol**. Introduceți informațiile solicitate și apoi selectați **Salvare**.
4. Repetați pașii 1-4 pentru a crea relații 1:N între entitățile **Titlul standard** și **Adaos de preț pentru rol**.

În fazele de vânzări și estimare ale proiectului, la prețul Ofertei/Proiectului, sunt necesare estimări ale efortului de lucru pentru fiecare titlu standard. Aceasta înseamnă că sunt necesare relații 1:N din Titlul standard pentru fiecare dintre aceste entități de estimare: 

- **Detaliu linie de ofertă**
- **Detaliu linie contract pentru proiect**
- **Membru echipă de proiect**
- **Linie estimată**

5. Repetați pașii 1-5 pentru a crea relații 1:N din **Titlul standard** la **Detaliu linie de ofertă** , **Detaliu linie contract pentru proiect** , **Membru echipă de proiect** și **Linie estimată**.

  În fazele de livrare și facturare, lucrarea este finalizată de fiecare titlul standard trebuie evaluată cu acuratețe cu privire la Valorile reale ale proiectului. Aceasta înseamnă că trebuie să existe relații 1:N de la **Titlul standard** la **Intrarea de timp** , **Valori reale** , **Detaliu linie factură** și **entități Linie de jurnal**.

6. Repetați pașii 1-6 pentru a crea relații 1:N din **Titlul standard** la **Intrarea de timp** , **Valori reale** , **Detaliu linie factură** și **entități Linie de jurnal**.

### <a name="set-up-dimension-value-defaulting-using-the-mappings-features-of-the-platform"></a>Configurați Valoarea de dimensiune la valoarea implicită utilizând caracteristicile mapărilor platformei
Pentru Intrarea de timp, ar fi util să aveți setarea implicită de sistem Titlul standard la Intrarea de timp din Resursa ce se poate rezerva care este înregistrarea Intrării de timp. Utilizați pașii următori pentru a adăuga mapări de câmp la relația 1:N din **Resursa ce se poate rezerva** la **Intrarea de timp**.

1. În Explorator soluții, în panoul de navigare din stânga, selectați **Entități > Titlu standard**.
2. Extindeți entitatea **Titlu standard** și selectați **Relații 1: N**.
3. Faceți dublu clic pe **Resursă ce se poate rezerva la Intrarea de timp**. Pe pagina **Relație** , selectați **Utilizați mapări de câmp**. 
4. Selectați **Nou** pentru a crea o mapare de câmp între câmpul **Titlu standard** de pe entitatea **Resursă ce se poate rezerva** la câmpul de referință **Titlu standard** la entitatea **Intrare de timp**. 

Aceasta încheie modificările schemei necesare pentru dimensiunile particularizate bazate pe entitate.

##  <a name="add-custom-fields-to-forms-views-and-business-rules"></a>Adăugați câmpurile particularizate la formulare, vizualizări și reguli de afaceri

După ce ați făcut toate modificările schemei necesare, următorul pas este de a face câmpurile vizibile în interfața cu utilizatorul adăugând câmpurile la formulare și vizualizări.

1. Deschideți formularul sau vizualizarea. În panoul de navigare din dreapta, selectați câmpul și glisați-l pe pânza formularului. 
2. Dacă editați o vizualizare, utilizați panoul de navigare din dreapta, selectați **Adăugați câmpuri** , iar în caseta de dialog **Listare câmp** , selectați câmpurile de care aveți nevoie și selectați **OK**.

Următorul tabel oferă o listă cuprinzătoare de formulare și vizualizări predefinite, de entitate, care vor trebui actualizate cu noile câmpuri. Dacă există vizualizări sau formulare suplimentare în particularizările acestor entități, adăugați noile câmpuri și la acelea.

| Entity        | Formulare care necesită un câmp nou   |Vizualizări care au nevoie de noul câmp      |
| ------------------------------|---------------------------------|----------------------------------|
|  Preț pentru rol|• Informații |• Prețuri categorii de resurse active<br> • Vizualizare asociată prețuri categorii de resurse|
|  Adaos de preț pentru rol|• Informații|• Adaos la prețul de rol activ<br>• Vizualizare asociată adaosului la prețurile de rol|
|  Detaliu linie de ofertă|• Informații proiect<br>• Creare rapidă proiect|• Detaliu linie de ofertă activă<br>• Detalii de linie ofertă combinate<br>• Vizualizare asociată a detaliilor de linie ofertă|
|  Detaliu linie contract pentru proiect|• Informații proiect<br>• Creare rapidă proiect|• Detalii din linie de contract combinate<br>• Detalii linie de contract active<br>• Vizualizare asociată pentru detalii din linia de contract|
|  Membru echipă de proiect|• Informații<br>• Formular nou|• Membri echipă de proiect activi<br>• Membri echipă de proiect<br>• Vizualizare asociată membri echipă de proiect|
|  Intrare de timp|• Informații<br>• Creare intrare de timp|• Intrările mele de timp după dată<br>• Intrările mele de timp pentru această săptămână<br>• Intrări de timp pentru aprobare.|
|  Linie de jurnal|• Informații<br>• Creare rapidă|• Linii de jurnal active<br>• Vizualizare asociată linie de jurnal|
|  Detaliu linie factură|• Informații<br>• Creare rapidă|• Detalii de linie factură active<br>• Tranzacții de factură facturabile<br>• Tranzacții de factură gratuite<br>• Vizualizare asociată a detaliilor de linie factură<br>• Tranzacție de factură nefacturabilă|
|  Real|• Informații<br>• Valori reale active|• Vizualizare asociată valori reale|

Câmpurile particularizate pot fi, de asemenea, adăugate în reguli de business în funcție de ceea ce ați definit. Un exemplu predefinit este pentru regula de business **Editabilitatea intrării de timp bazate pe stare**. Această regulă definește câmpurile care trebuie blocate când Intrarea de timp este într-o stare non-editabilă, cum ar fi **Aprobat**. Adăugați câmpuri la această regulă de business, astfel încât câmpurile să fie blocate pentru editare atunci când Intrarea de timp este într-o altă stare decât **Schiță** sau **Returnat**.
