---
title: Unități organizaționale
description: Acest articol descrie conceptul de unități organizaționale și explică cum să creați și să mențineți unități organizaționale în Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 1/31/2022
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
ms.reviewer: johnmichalak
ms.openlocfilehash: a20a37b61db68d70869a11e10bef5d30c422b1eb
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921639"
---
# <a name="organizational-units-overview"></a>Prezentare generală a unităților organizaționale

În Microsoft Dynamics 365 Project Operations, an *unitate organizationala* este un grup sau diviziune distinctă într-o companie de servicii profesionale care angajează resurse facturabile care au rate de cost.

Pentru companiile de servicii profesionale care angajează resurse tehnice în diferite domenii de practică sau linii de activitate, costul pentru ocuparea unui rol poate varia, în funcție de domeniul de practică sau linia de activitate în care este ocupat rolul. În acest scenariu, conceptul de unități organizaționale ajută oferind o modalitate de a grupa un set de roluri facturabile într-o divizie a unei companii care are o structură de costuri distinctă pentru acele roluri.

## <a name="the-concept-of-organizational-units-in-project-operations"></a>Conceptul de unități organizaționale în Operațiunile de Proiect

În Operațiuni de proiect, o unitate organizațională are o anumită monedă și liste de prețuri de cost specifice.

Moneda unei unități organizaționale este moneda principală care este utilizată pentru a urmări costurile.

Una sau mai multe liste de prețuri de cost pot fi atașate la fiecare unitate organizațională. Project Operations pune următoarele limitări asupra listelor de prețuri care pot fi atașate unei unități organizaționale:

- Listele de prețuri trebuie să fie în moneda unității organizatorice.
- Listele de prețuri trebuie să fie liste de prețuri de cost.

În plus, entitatea Resursă include un atribut pentru unitatea organizatorică. Fiecare resursă poate fi atribuită unei singure unități organizaționale.

### <a name="roles-of-organizational-units"></a>Rolurile unităților organizaționale

Unitatea organizatorică joacă două roluri în operațiunile de proiect:

- **Unitate contractantă** – unitatea organizațională care reprezintă grupul de firme sau divizia care este principalul responsabil cu câștigarea vânzării și cu gestionarea livrării de lucrări și servicii către client. Unitatea contractantă este identificată de câmpul **Unitate contractantă** din secțiunea antet a paginilor **Oportunitate**, **Ofertă**, **Contract de proiect** și **Proiect**.
- **Unitate resursă** – unitatea organizațională căreia îi aparține sau îi este atribuită o resursă. Această unitate organizațională poate furniza resursele sale pentru unele roluri pe specificațiile de lucru (SL) și proiecte care sunt deținute de unitatea contractantă.

![Unități contractante și unități de resurse.](media/OrgUnits.png)

### <a name="organizational-unit-faq"></a>Întrebări frecvente despre unitatea organizațională

Vă prezentăm răspunsurile la câteva dintre cele mai frecvente întrebări despre unitățile organizaționale.

#### <a name="how-is-the-organizational-unit-entity-in-project-operations-related-to-the-organization-entity-that-already-exists-in-dynamics-365"></a>Cum este legată entitatea Unitate organizațională din Operațiuni de proiect cu entitatea Organizație care există deja în Dynamics 365?

Entitatea Organizație din Dynamics 365 reprezintă numele unei instanțe globale Dynamics 365. Acest nume este, de obicei, numele întreprinderii globale.

Entitatea Unitate organizațională reprezintă un grup sau o divizie din întreprinderea globală. Acest grup sau divizie are un set de roluri și o listă de prețuri de cost pentru acele roluri, iar acele roluri și lista de prețuri diferă de rolurile și lista de prețuri ale altor grupuri sau divizii din întreprindere.

Când este instalată Project Operations, o unitate organizațională implicită este creată pe baza organizației. Toate resursele existente sunt atribuite unității organizaționale implicite. Dacă sunt importați utilizatori sau resurse noi Active Directory în Dynamics 365, procesul de importare a utilizatorilor le atribuie unității organizaționale implicite din Project Operations.

#### <a name="how-does-the-organizational-unit-entity-differ-from-the-business-unit-entity"></a>Cum diferă entitatea Unitatea Organizațională de entitatea Unitatea de afaceri?

În Dynamics 365, entitatea Unitate de business este o construcție de securitate. Asocierea unui utilizator cu o unitate de business determină entitățile și înregistrările de entități la care utilizatorul are acces. De asemenea, stabilește permisiunile (Creare, Citire, Scriere, Ștergere, Adăugare, Adăugare la, Atribuire sau Partajare) pe care utilizatorul le are pentru acele înregistrări de entități.

Entitatea Unitate organizațională reprezintă un grup de companii sau o divizie care are rate de cost distincte pentru angajații care îi sunt atribuiți. Asocierea unei resurse cu o unitate organizațională determină costul resursei la un angajament de proiect.

Atunci când implementați Dynamics 365, optimizați autorizarea de securitate pentru ierarhia unităților de business și atribuirea de utilizatori unităților de business. Atribuiți toți utilizatorii care trebuie să acceseze de obicei același set de înregistrări aceleiași unități de business. Unitatea organizațională nu are niciun efect asupra autorizării sau accesului de securitate.

**Exemplu care arată o diferență potențială în modelarea unităților organizaționale și a unităților de afaceri**

Contoso, Ltd. are o practică înfloritoare de tehnologie Microsoft. Daniel și Vera sunt amândoi dezvoltatori C\#, dar Vera este în Statele Unite, în timp ce Daniel este în India. Cele mai multe dintre angajamentele proiectelor necesită resurse atât din Contoso India, cât și din Contoso SUA, iar Prakash și Tricia necesită același nivel de securitate la proiectele din acest domeniu de practică. Cu toate acestea, costul dezvoltatorilor din Contoso India diferă în mod semnificativ de costul dezvoltatorilor din Contoso SUA.

Iată o modalitate optimă de proiectare pentru acest scenariu utilizând Dynamics 365 și Project Operations.

1. Creați practica tehnologiei Microsoft ca unitate de business și asociați-i pe Daniel și Vera cu ea. În acest fel, contribuiți la asigurarea faptului că ambii angajați au același nivel de acces de securitate la orice proiecte din acea zonă de practică. Ambii vor putea să verifice progresul și să raporteze timpul, cheltuielile, utilizarea materialelor și actualizările sarcinilor.
2. Creați două unități organizaționale pentru a vă asigura că costul proiectului este reflectat corect.
3. Asociați Tricia cu Contoso SUA și Prakash cu Contoso India.
4. Atribuiți listele de prețuri corespunzătoare ambelor unități organizaționale. În acest fel, vă asigurați că costurile care sunt înregistrate în proiect pentru Prakash și Tricia reflectă cu exactitate diferența de costuri dintre Contoso SUA și Contoso India.

#### <a name="are-organizational-units-related-to-sales-territories-in-dynamics-365"></a>Sunt unitățile organizaționale legate de teritoriile de vânzări în Dynamics 365?

Nu există nicio asociere sau relație între teritoriile de vânzări și unitățile organizaționale. Un teritoriu de vânzări este de obicei o zonă geografică în care au loc vânzările. O listă de prețuri de vânzare poate fi asociată cu fiecare teritoriu de vânzări.

O unitate organizațională este un grup intern sau o divizie internă din companie, care urmărește costurile pentru un set de roluri pe care le vinde altor divizii sau clienților externi.

**Exemplu care arată o diferență potențială în modelarea unităților organizaționale și a teritoriilor de vânzare**

Contoso, Ltd. are două centre de dezvoltare: Contoso SUA și Contoso India. Costul resurselor diferă foarte mult între aceste două centre de dezvoltare. Contoso își vinde serviciile de tehnologia informației (IT) pe multe piețe internaționale, cum ar fi America Latină, America de Nord, Asia-Pacific, Europa de Vest și Orientul Mijlociu. Ratele de facturare pentru aceleași roluri de proiect pot varia considerabil pe aceste piețe. Contoso SUA și Contoso India ar trebui configurate ca unități organizaționale, și fiecare unitate organizațională ar trebui să aibă propria listă de prețuri de cost. Asia-Pacific, America Latină, America de Nord, Europa de Vest și Orientul Mijlociu ar trebui configurate ca teritorii de vânzări, și fiecare teritoriu de vânzări ar trebui să aibă propria listă de prețuri de vânzare.

#### <a name="why-is-there-a-restriction-on-the-association-of-price-lists-with-organizational-units"></a>De ce există o restricție privind asocierea listelor de prețuri cu unitățile organizaționale?

Prețurile de vânzări sunt de obicei unice pentru zonele geografice sau pentru piețele în care sunt vândute serviciile. Diviziile interne ale unei companii nu au de obicei propriile lor prețuri de vânzări pentru același tip de servicii. Cu toate acestea, diviziile interne au un cost diferit al bunurilor vândute (COGS), în funcție de competențele persoanelor pe care le angajează și de condițiile de muncă din regiunea în care operează. Deoarece unitățile organizaționale sunt modelate ca divizii interne ale unei companii, ele pot avea doar liste de prețuri de cost.

#### <a name="why-cant-we-associate-sales-price-lists-with-organizational-units"></a>De ce nu putem asocia listele de prețuri de vânzare cu unitățile organizaționale?

În Operațiuni de proiect, listele de prețuri de vânzare pot fi asociate cu clienții și teritoriile de vânzare. Entitățile tranzacționale, cum ar fi Oportunitatea, Cotația, Contractul de proiect și Proiectul folosesc liste de prețuri de vânzare care sunt atașate contului clientului sau teritoriului de vânzare pentru a determina ratele de facturare și veniturile potențiale pentru implicarea proiectului.

Listele de prețuri de cost sunt asociate cu unitățile organizaționale. Entitățile tranzacționale, cum ar fi Oportunitatea, Cotația, Contractul de proiect și Proiectul folosesc liste de prețuri de cost care sunt atașate unității contractante pentru a determina costurile pentru o angajament de proiect.

#### <a name="are-organizational-units-hierarchical-in-project-operations"></a>Sunt unitățile organizaționale ierarhice în operațiunile de proiect?

Nu. În versiunea actuală a Operațiunilor de proiect, unitățile organizaționale nu sunt ierarhice. Prin urmare, nu puteți efectua următoarele sarcini:

- Configurați un model pentru introducerea prețurilor de cost implicite care traversează o ierarhie în sus.
- Raportați veniturile sau costurile acumulate la diferite niveluri ale ierarhiei unității organizaționale.

#### <a name="were-a-big-multinational-firm-that-has-a-complex-multilevel-hierarchy-of-cost-centers-divisions-and-billing-offices-how-can-we-best-use-the-concept-of-organizational-units-in-the-current-version-of-project-operations"></a>Suntem o mare firmă multinațională care are o ierarhie complexă, pe mai multe niveluri de centre de cost, divizii și birouri de facturare. Cum putem folosi cel mai bine conceptul de unități organizaționale în versiunea actuală a Operațiunilor de proiect?

Când aveți o ierarhie complexă de centre de cost, divizii, birouri de facturare și așa mai departe, configurați nodurile frunză ale acelei ierarhii ca unități organizaționale distincte.

Următorul exemplu arată o ierarhie tipică.

**Contoso India**

- Practică SAP

    - Consultanți tehnici
    - Consultanți funcționali

- Practică tehnologie Microsoft

    - Consultanți tehnici
    - Consultanți funcționali

**Contoso US**

- Practică SAP

    - Consultanți tehnici
    - Consultanți funcționali

- Practică tehnologie Microsoft

    - Consultanți tehnici
    - Consultanți funcționali

Dacă ierarhia dvs. seamănă cu acest exemplu, trebuie să o configurați ca o listă plată, așa cum se arată aici:

- Contoso India – Practică SAP – Consultanți tehnici
- Contoso India – Practică SAP – Consultanți funcționali
- Contoso India – Practică tehnologii Microsoft – Consultanți funcționali
- Contoso India – Practică tehnologii Microsoft – Consultanți funcționali
- Contoso SUA – Practică SAP – Consultanți tehnici
- Contoso SUA – Practică SAP – Consultanți funcționali
- Contoso SUA – Practică tehnologii Microsoft – Consultanți tehnici
- Contoso SUA – Practică tehnologii Microsoft – Consultanți funcționali

#### <a name="were-a-small-professional-services-company-that-operates-as-only-one-division-how-can-we-best-use-the-concept-of-organizational-units-in-the-current-version-of-project-operations"></a>Suntem o companie de servicii profesionale mică, care operează ca o singură divizie. Cum putem folosi cel mai bine conceptul de unități organizaționale în versiunea actuală a Operațiunilor de proiect?

Dacă compania dumneavoastră operează ca o singură unitate care are o listă de prețuri de cost, nu trebuie să configurați nicio unitate organizațională. Instalarea Project Operations creează o unitate organizațională implicită care are același nume cu organizația. În mod implicit, toți utilizatorii sunt atribuiți acestei unități organizaționale. De fiecare dată când sistemul solicită ca o unitate organizațională să fie selectată, această unitate organizațională este selectată în mod implicit.

#### <a name="when-a-project-is-created-from-a-quote-or-project-contract-line-the-default-contracting-unit-comes-from-the-quote-or-project-contract-what-is-the-default-contracting-unit-if-a-project-is-created-before-sales-entities-such-as-quote-or-project-contract"></a>Când se creează un proiect dintr-o ofertă sau o linie de contract de proiect, unitatea contractantă implicită provine din ofertă sau din contractul de proiect. Care este unitatea de contractare implicită dacă un proiect este creat înaintea entităților de vânzare, cum ar fi Cotația sau Contractul de proiect?

Când un proiect este creat pe cont propriu, unitatea contractantă implicită a proiectului se bazează pe utilizatorul care îl creează. Acest utilizator este, de asemenea, managerul de proiect implicit. Dacă proiectul este mapat la o entitate de vânzare, cum ar fi o ofertă sau un contract de proiect, unitatea contractantă a proiectului se bazează în schimb pe entitatea de vânzare. În acest caz, estimările proiectului pot fi recalculate, deoarece lista de prețuri de cost este utilizată pentru a calcula modificările costului estimat dacă unitatea contractantă este schimbată. Lista de prețuri de vânzare este utilizată pentru a calcula estimările de vânzări care vor fi modificate, astfel încât acestea să fie sincronizate cu lista de prețuri de proiect a ofertei.

The **Unitatea de Contractare** și **Valută** câmpurile proiectului sunt blocate pentru editare, deoarece trebuie să fie sincronizate cu valorile entității de vânzare (cotație sau contract de proiect) la care este mapat proiectul.

## <a name="create-and-maintain-organizational-units-in-project-operations"></a>Crearea și menținerea unităților organizaționale în Operațiuni de proiect

Pentru a crea o unitate organizațională în Operațiuni de proiect, urmați acești pași.

1. Mergi la **Setări \> Unități organizaționale**.
2. Selectați **Nou**.
3. În **General** zona, in **Nume** câmp, introduceți un nume pentru unitatea organizatorică. Apoi setați celelalte câmpuri după cum este necesar.
4. Selectați **Salvați** pentru a crea înregistrarea, astfel încât să puteți continua să o editați.
5. Sub **Liste de prețuri de cost**, selectați semnul plus (**+**) pentru a adăuga o listă de prețuri. Puteți adăuga numai liste de prețuri care au **Cost** context aici.
6. În **Nume** câmp, selectați **Căutare** butonul și selectați o listă de prețuri pe care doriți să o puneți la dispoziția unității organizaționale. Continuați să adăugați liste de prețuri după cum este necesar.
7. Când ați terminat de adăugat listele de prețuri, selectați **Salvați** în colțul din dreapta jos al paginii.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
