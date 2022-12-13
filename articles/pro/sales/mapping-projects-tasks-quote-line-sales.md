---
title: Hartați proiecte și sarcini la liniile de cotație de proiect
description: Acest articol oferă informații despre cum să mapați proiecte și sarcini la liniile de cotație de proiect.
author: rumant
ms.date: 10/05/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b276e7fb6ec8b98188c9396aca5092d19848afcc
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824362"
---
# <a name="map-projects-and-tasks-to-project-quote-lines"></a>Hartați proiecte și sarcini la liniile de cotație de proiect

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Pe liniile de oferta de proiect, puteți mapa sarcinile specifice ale unui proiect care este deja asociat unei linii de oferta.

Când asociați sarcinile la o linie de ofertă, următoarele elemente definite pe linia de ofertă se vor aplica numai acelor activități:

- Metoda de facturare
- Opțiuni de posibilitate de tarifare
- Limite de nedepășire
- Clienți

De exemplu, s-ar putea să aveți un proiect în care o fază este cu preț fix și toate celelalte faze sunt timp și materiale. În acest caz, puteți asocia prima fază și toate sarcinile sale secundare liniei de ofertă pentru acea fază cu o metodă de facturare cu preț fix. Apoi, puteți asocia toate celelalte faze liniei de ofertă bazate pe timp și materiale.

## <a name="associate-tasks-to-project-based-quote-lines"></a>Asociați activități la linii de ofertă bazate pe proiect

Puteți asocia sarcini cu liniile de ofertă din următoarele locații:

- Pagina **Proiect** > fila **Facturarea activităților** (optim)
- Pagina **Linie de ofertă** fila > **Activități taxabile** 

### <a name="from-the-project-page"></a>De pe pagina de proiect

Pagina **Proiect** oferă experiența optimă pentru asocierea activităților la liniile de ofertă. Puteți utiliza această pagină pentru a selecta mai multe activități și a le asocia pe toate, plus sarcinile secundare, la linia de ofertă selectată.

1. Pe fila **General** unei linii de ofertă de estimare bazate pe proiect, verificați dacă câmpul **Proiect** este completat.
2. În câmpul **Activități incluse**, selectați **Numai activități selectate**.
3. Salvați linia de ofertă bazată de proiect. Când formularul se reîmprospătează, se afișează fila **Activități taxabile**.
4. Pe fila **General**, selectați linkul pentru proiect din câmpul **Proiect**.
5. Pe pagina **Proiect** selectați fila **Facturare activități**.
6. În a doua grilă, care se aplică configurării de facturare specifice sarcinilor, selectați una sau mai multe sarcini și apoi selectați **Asociați liniile de ofertă**.
7. În pagina de dialog care apare, selectați o linie de ofertă care afișează liniile de ofertă bazate pe proiect.
8. În câmpul **Tipul de facturare**, indicați dacă aceste sarcini sunt taxabile sau neimpozabile.
9. Bifați caseta de selectare pentru a indica dacă asocierea ar trebui să includă sarcini secundare ale sarcinilor selectate. Bifând caseta se vor asocia sarcinile secundare ale sarcinilor selectate la linia de ofertă.
10. Selectați **OK** pentru a închide dialogul.

### <a name="from-the-quote-line-page"></a>Din pagina liniei de ofertă

Puteți asocia sarcinile proiectului pentru a oferta linii din fila **Activități taxabile** pe pagina **Linie de ofertă**.

>[!NOTE]
>Locul optim pentru asocierea sarcinilor proiectului la liniile de ofertă este pe fila **Facturarea sarcinilor** pe pagina **Proiect**. Dacă asociați sarcini din fila **Sarcini taxabile** pe pagina **Linie de ofertă**, trebuie să asociați manual fiecare proiect.

1. Pe fila **General** a unei linii de ofertă de estimare bazate pe proiect, verificați că este un proiect selectat în câmpul **Proiect**.
2. În câmpul **Activități incluse**, selectați **Numai activități selectate**.
3. Salvați linia de ofertă bazată de proiect. Când formularul se reîmprospătează, se afișează fila **Activități taxabile**.
4. Pe fila **Sarcini taxabile**, selectați **Adăugați o sarcină de linie de ofertă**.
5. Pe pagina **Activitatea liniei de ofertă**, în câmpul **Activități**, selectați sarcina și în câmpul **Tipul de facturare**, selectați **Salvare**. 
6. Închideți pagina. Activitatea selectată este acum asociată liniei de ofertă.

## <a name="disassociate-tasks-from-projectbased-quote-lines"></a>Dezasociați activități din linii de ofertă bazate pe proiect

### <a name="from-the-project-page"></a>De pe pagina de proiect

Această metodă oferă cea mai optimă experiență pentru dezasocierea activităților din linii de ofertă. Puteți selecta mai multe activități și le puteți dezasocia pe toate, plus activitățile lor secundare, din linia de ofertă selectată.

1. Pe fila **General** a unei linii de ofertă de estimare bazate pe proiect, în câmpul **Proiect**, selectați linkul de proiect.
2. Pe pagina **Proiect** selectați fila **Facturare activități**.
3. În a doua grilă, care se aplică configurării de facturare specifice sarcinilor, selectați una sau mai multe sarcini și apoi selectați **Dezasociați liniile de ofertă**.
4. În pagina de dialog care apare, selectați o linie de ofertă.
5. Bifați caseta de selectare pentru a indica dacă asocierea ar trebui să fie eliminată din activitățile secundare ale activităților selectate. Bifând caseta se vor dezasocia sarcinile secundare ale sarcinilor selectate la linia de ofertă.
6. Selectați **OK**. Un mesaj de avertizare vă informează că, dacă eliminați această asociere, orice realitate înregistrată anterior în activitate ar putea fi inversată. 
7. Selectați **OK** pentru a continua și a elimina asocierea dintre activitate și linia de ofertă bazată pe proiect.

### <a name="from-the-quote-line-page"></a>Din pagina liniei de ofertă

Puteți dezasocia sarcinile proiectului pentru a oferta linii din fila **Activități taxabile** pe pagina **Linie de ofertă**.

1. Pe fila **Sarcini taxabile**, selectați **Ștergeți o activitate de linie de ofertă**.
2. Selectați **OK**. Un mesaj de avertizare vă informează că, dacă eliminați această asociere, orice realitate înregistrată anterior în activitate ar putea fi inversată. 
3. Selectați **OK** pentru a continua și a elimina asocierea dintre activitate și linia de ofertă bazată pe proiect.

>[!NOTE]
> Această procedură nu șterge activtiatea din proiect. Elimină doar asocierea activității din linia de ofertă bazată pe proiect.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
