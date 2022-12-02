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
# <a name="organizational-units-overview"></a>Descriere generală a unităților organizaționale

În Microsoft Dynamics 365 Project Operations, o *unitate organizațională* este un grup distinct sau o divizie distinctă într-o companie de servicii profesionale care angajează resurse facturabile care au rate de cost.

Pentru companiile de servicii profesionale care utilizează resurse tehnice în diferite domenii de activitate sau linii de afaceri, costul pentru ocuparea unui rol poate varia, în funcție de zona de practică sau linia de activitate în care este ocupat rolul. În acest scenariu, conceptul de unități organizaționale ajută prin furnizarea unei modalități de grupare a unui set de roluri facturabile într-o divizie a unei companii care are o structură de costuri distinctă pentru aceste roluri.

## <a name="the-concept-of-organizational-units-in-project-operations"></a>Conceptul de unități organizaționale în Project Operations

În Project Operations, o unitate organizațională are o anumită monedă și liste de prețuri de cost specifice.

Moneda unei unități organizaționale este moneda principală care este utilizată pentru a urmări costurile.

Una sau mai multe liste de prețuri de cost pot fi atașate la fiecare unitate organizațională. Project Operations impune următoarele limitări pentru listele de prețuri care pot fi atașate la o unitate organizațională:

- Listele de preț trebuie să fie în moneda unității organizaționale.
- Listele de preț trebuie să fie liste de prețuri de cost.

În plus, entitatea Resursă include un atribut pentru unitatea organizatorică. Fiecare resursă poate fi atribuită unei singure unități organizaționale.

### <a name="roles-of-organizational-units"></a>Rolurile unităților organizaționale

Unitatea organizațională joacă două roluri în Project Operations:

- **Unitate contractantă** – unitatea organizațională care reprezintă grupul de firme sau divizia care este principalul responsabil cu câștigarea vânzării și cu gestionarea livrării de lucrări și servicii către client. Unitatea contractantă este identificată de câmpul **Unitate contractantă** din secțiunea antet a paginilor **Oportunitate**, **Ofertă**, **Contract de proiect** și **Proiect**.
- **Unitate resursă** – unitatea organizațională căreia îi aparține sau îi este atribuită o resursă. Această unitate organizațională poate furniza resursele sale pentru unele roluri pe specificațiile de lucru (SL) și proiecte care sunt deținute de unitatea contractantă.

![Unități contractante și unități de resurse.](media/OrgUnits.png)

### <a name="organizational-unit-faq"></a>Întrebări frecvente despre unitatea organizațională

Vă prezentăm răspunsurile la câteva dintre cele mai frecvente întrebări despre unitățile organizaționale.

#### <a name="how-is-the-organizational-unit-entity-in-project-operations-related-to-the-organization-entity-that-already-exists-in-dynamics-365"></a>Cum este entitatea Unitate organizațională din Project Operations legată de entitatea Organizație care există deja în Dynamics 365?

Entitatea Organizație din Dynamics 365 reprezintă numele unei instanțe globale Dynamics 365. Acest nume este, de obicei, numele întreprinderii globale.

Entitatea Unitate organizațională reprezintă un grup sau o divizie din întreprinderea globală. Acest grup sau divizie are un set de roluri și o listă de prețuri de cost pentru acele roluri, iar acele roluri și lista de prețuri diferă de rolurile și lista de prețuri ale altor grupuri sau divizii din întreprindere.

Când este instalat Project Operations, o unitate organizațională implicită este creată pe baza organizației. Toate resursele existente sunt atribuite unității organizaționale implicite. Dacă orice utilizatori sau resurse noi din Active Directory sunt importate în Dynamics 365, procesul de import al utilizatorilor le atribuie unității organizaționale implicite din Project Operations.

#### <a name="how-does-the-organizational-unit-entity-differ-from-the-business-unit-entity"></a>Cum diferă entitatea Unitate organizațională de entitatea Unitate de afaceri?

În Dynamics 365, entitatea Unitate de business este o construcție de securitate. Asocierea unui utilizator cu o unitate de business determină entitățile și înregistrările de entități la care utilizatorul are acces. De asemenea, stabilește permisiunile (Creare, Citire, Scriere, Ștergere, Adăugare, Adăugare la, Atribuire sau Partajare) pe care utilizatorul le are pentru acele înregistrări de entități.

Entitatea Unitate organizațională reprezintă un grup de companii sau o divizie care are rate de cost distincte pentru angajații care îi sunt atribuiți. Asocierea unei resurse cu o unitate organizațională determină costul resursei la un angajament de proiect.

Atunci când implementați Dynamics 365, optimizați autorizarea de securitate pentru ierarhia unităților de business și atribuirea de utilizatori unităților de business. Atribuiți toți utilizatorii care trebuie să acceseze de obicei același set de înregistrări aceleiași unități de business. Unitatea organizațională nu are niciun efect asupra autorizării sau accesului de securitate.

**Exemplu care arată o diferență potențială în modelarea unităților organizaționale și a unităților de afaceri**

Contoso, Ltd. are o practică înfloritoare de tehnologie Microsoft. Daniel și Vera sunt amândoi dezvoltatori C\#, dar Vera este în Statele Unite, în timp ce Daniel este în India. Majoritatea angajamentelor de proiect necesită resurse atât din Contoso India, cât și din Contoso US, iar Prakash și Tricia necesită același nivel de acces de securitate la proiectele din această zonă de practică. Cu toate acestea, costul dezvoltatorilor din Contoso India diferă în mod semnificativ de costul dezvoltatorilor din Contoso SUA.

Iată o modalitate optimă de a concepe acest scenariu utilizând Dynamics 365 și Project Operations.

1. Creați practica tehnologiei Microsoft ca unitate de business și asociați-i pe Daniel și Vera cu ea. În acest fel, veți contribui la asigurarea faptului că ambii angajați au același nivel de acces de securitate la orice proiecte din acest domeniu de activitate. Ambii vor putea să verifice progresul și să raporteze timpul, cheltuielile, utilizarea de materiale și actualizările sarcinilor.
2. Crearea a două unități organizaționale pentru a asigura reflectarea corectă a costurilor proiectului.
3. Asociați-o pe Tricia cu Contoso US și asociați-l pe Prakash cu Contoso India.
4. Atribuiți listele de prețuri corespunzătoare ambelor unități organizaționale. În acest fel, contribuiți la asigurarea faptului că costurile care sunt înregistrate în proiect pentru Prakash și Tricia reflectă cu exactitate diferența de costuri dintre Contoso SUA și Contoso India.

#### <a name="are-organizational-units-related-to-sales-territories-in-dynamics-365"></a>Sunt unitățile organizaționale legate de teritoriile de vânzări în Dynamics 365?

Nu există nicio asociere sau relație între teritoriile de vânzări și unitățile organizaționale. Un teritoriu de vânzări este de obicei o zonă geografică în care au loc vânzările. O listă de prețuri de vânzare poate fi asociată cu fiecare teritoriu de vânzări.

O unitate organizațională este un grup intern sau o divizie internă din companie, care urmărește costurile pentru un set de roluri pe care le vinde altor divizii sau clienților externi.

**Exemplu care arată o diferență potențială în modelarea unităților organizaționale și a teritoriilor de vânzare**

Contoso, Ltd. are două centre de dezvoltare: Contoso SUA și Contoso India. Costul resurselor diferă foarte mult între aceste două centre de dezvoltare. Contoso își vinde serviciile de tehnologie a informației (IT) pe multe piețe internaționale, cum ar fi America Latină, America de Nord, Asia-Pacific, Europa de Vest și Orientul Mijlociu. Ratele de facturare pentru aceleași roluri de proiect pot varia considerabil pe aceste piețe. Contoso SUA și Contoso India ar trebui configurate ca unități organizaționale, și fiecare unitate organizațională ar trebui să aibă propria listă de prețuri de cost. Asia-Pacific, America Latină, America de Nord, Europa de Vest și Orientul Mijlociu ar trebui configurate ca teritorii de vânzări, și fiecare teritoriu de vânzări ar trebui să aibă propria listă de prețuri de vânzare.

#### <a name="why-is-there-a-restriction-on-the-association-of-price-lists-with-organizational-units"></a>De ce există o restricție privind asocierea listelor de prețuri cu unitățile organizaționale?

Prețurile de vânzări sunt de obicei unice pentru zonele geografice sau pentru piețele în care sunt vândute serviciile. Diviziile interne ale unei companii nu au de obicei propriile lor prețuri de vânzări pentru același tip de servicii. Cu toate acestea, diviziile interne au un cost diferit al bunurilor vândute (COGS), în funcție de competențele persoanelor pe care le angajează și de condițiile de muncă din regiunea în care operează. Deoarece unitățile organizaționale sunt modelate ca divizii interne ale unei companii, ele pot avea doar liste de prețuri de cost.

#### <a name="why-cant-we-associate-sales-price-lists-with-organizational-units"></a>De ce nu putem asocia listele de prețuri de vânzări cu unitățile organizaționale?

În Project Operations, listele de prețuri de vânzări pot fi asociate cu clienții și teritoriile de vânzări. Entități tranzacționale, cum ar fi Oportunitate, Ofertă, Contract de proiect și Proiect, utilizează listele de prețuri de vânzări care sunt atașate la contul de client sau la teritoriul de vânzare pentru a determina ratele de facturare și venitul potențial pentru angajamentul de proiect.

Listele de prețuri de cost sunt asociate cu unitățile organizaționale. Entități tranzacționale precum Oportunitate, Ofertă, Contract de proiect și Proiect utilizează listele de preț de cost care sunt atașate la unitatea contractantă pentru a determina costurile pentru un angajament de proiect.

#### <a name="are-organizational-units-hierarchical-in-project-operations"></a>Sunt unitățile organizaționale ierarhice în Project Operations?

Nu. În actuala versiune a Project Operations, unitățile organizaționale nu sunt ierarhice. Prin urmare, nu puteți realiza următoarele activități:

- Configura un model pentru introducerea prețurilor de cost implicite care traversează o ierarhie.
- Raporta venituri sau costuri care sunt cumulate la diferite niveluri ale ierarhiei unității organizaționale.

#### <a name="were-a-big-multinational-firm-that-has-a-complex-multilevel-hierarchy-of-cost-centers-divisions-and-billing-offices-how-can-we-best-use-the-concept-of-organizational-units-in-the-current-version-of-project-operations"></a>Suntem o firmă multinațională mare care are o ierarhie complexă, pe mai multe niveluri, de centre de cost, divizii și birouri de facturare. Cum putem folosi cel mai bine conceptul de unități organizaționale în versiunea actuală de Project Operations?

Când aveți o ierarhie complexă a centrelor de cost, diviziilor, birourilor de facturare ș.a.m.d., configurați nodurile frunză din ierarhia respectivă ca unități organizaționale distincte.

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

Dacă ierarhia dvs. este similară cu acest exemplu, trebuie să o configurați ca listă plată, așa cum se arată aici:

- Contoso India – Practică SAP – Consultanți tehnici
- Contoso India – Practică SAP – Consultanți funcționali
- Contoso India – Practică tehnologii Microsoft – Consultanți funcționali
- Contoso India – Practică tehnologii Microsoft – Consultanți funcționali
- Contoso SUA – Practică SAP – Consultanți tehnici
- Contoso SUA – Practică SAP – Consultanți funcționali
- Contoso SUA – Practică tehnologii Microsoft – Consultanți tehnici
- Contoso SUA – Practică tehnologii Microsoft – Consultanți funcționali

#### <a name="were-a-small-professional-services-company-that-operates-as-only-one-division-how-can-we-best-use-the-concept-of-organizational-units-in-the-current-version-of-project-operations"></a>Suntem o companie de servicii profesionale mică, care operează ca o singură divizie. Cum putem folosi cel mai bine conceptul de unități organizaționale în versiunea actuală de Project Operations?

Dacă compania dumneavoastră operează ca o singură unitate care are o listă de prețuri de cost, nu trebuie să configurați nicio unitate organizațională. Instalarea Project Operations creează o unitate organizațională implicită care are același nume ca organizația. În mod implicit, toți utilizatorii sunt atribuiți acestei unități organizaționale. De fiecare dată când sistemul solicită ca o unitate organizațională să fie selectată, această unitate organizațională este selectată în mod implicit.

#### <a name="when-a-project-is-created-from-a-quote-or-project-contract-line-the-default-contracting-unit-comes-from-the-quote-or-project-contract-what-is-the-default-contracting-unit-if-a-project-is-created-before-sales-entities-such-as-quote-or-project-contract"></a>Când se creează un proiect dintr-o ofertă sau o linie de contract de proiect, unitatea contractantă implicită provine din ofertă sau din contractul de proiect. Care este unitatea de contractare implicită dacă un proiect este creat înaintea entităților de vânzare, cum ar fi Oferta sau Contractul de proiect?

Când un proiect este creat pe cont propriu, unitatea contractantă implicită a proiectului se bazează pe utilizatorul care îl creează. Acest utilizator este, de asemenea, managerul de proiect implicit. Dacă proiectul este mapat la o entitate de vânzări, cum ar fi o ofertă sau un contract de proiect, unitatea contractantă a proiectului se bazează, în schimb, pe entitatea de vânzări. În acest caz, estimările proiectului pot fi recalculate, deoarece lista de prețuri de cost este utilizată pentru a calcula modificările costului estimat dacă unitatea contractantă este schimbată. Lista de prețuri de vânzare este utilizată pentru a calcula estimările de vânzări care vor fi modificate astfel încât să fie sincronizate cu lista de prețuri a proiectului din ofertă.

Câmpurile **Unitate contractantă** și **Monedă** ale proiectului sunt blocate pentru editare, deoarece acestea trebuie să fie sincronizate cu valorile entitatății de vânzări (ofertă sau contract de proiect) la care este mapat proiectul.

## <a name="create-and-maintain-organizational-units-in-project-operations"></a>Crearea și menținerea unităților organizaționale în Project Operations

Pentru a crea o unitate organizațională în Project Operations, urmați acești pași.

1. Accesați **Setări \> Unități organizaționale**.
2. Selectați **Nou**.
3. În zona **General**, în câmpul **Nume**, introduceți un nume pentru unitatea organizațională. Apoi, setați celelalte câmpuri după cum este necesar.
4. Selectați **Salvare** pentru a crea înregistrarea, astfel încât să o puteți edita în continuare.
5. Sub **Liste de prețuri de cost**, faceți clic pe semnul plus (**+**) pentru a adăuga o listă de prețuri. Puteți adăuga doar liste de prețuri care au contextul **Cost** aici.
6. În câmpul **Nume**, selectați butonul **Căutare** și selectați o listă de prețuri pe care doriți să o faceți disponibilă pentru această unitate organizațională. Continuați să adăugați liste de prețuri după cum este necesar.
7. Când ați terminat adăugarea de liste de preț, selectați **Salvare** în colțul din dreapta jos a paginii.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
