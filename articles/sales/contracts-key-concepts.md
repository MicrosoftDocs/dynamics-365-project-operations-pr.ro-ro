---
title: Contracte de proiect - concepte cheie
description: Acest subiect furnizează informații despre conceptele cheie ale contractelor de proiect în Project Operations.
author: rumant
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b0e0280cb94e6f0186f59024c233e8fcb9e86abf
ms.sourcegitcommit: df30839484ef278675c5c712af0f7ba66ed9cdd3
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 03/17/2021
ms.locfileid: "5663742"
---
# <a name="concepts-unique-to-project-based-contracts"></a>Concepte unice pentru contractele bazate pe proiecte

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Acest subiect oferă conceptele cheie de care trebuie să fiți conștient înainte de a începe să utilizați contractele de proiect în Dynamics 365 Project Operations:

## <a name="owning-company"></a>Firmă proprietară

Compania deținătoare este entitatea juridică din modulul **Management de proiect și contabilitate** pentru Project Operations din Dynamics 365 Finance. Compania deținătoare reprezintă entitatea juridică care va contabiliza costurile și veniturile care rezultă dintr-o tranzacție.

## <a name="contracting-unit"></a>Unitate contractantă

Unitatea contractantă reprezintă divizia sau practica care deține livrarea proiectului. Puteți seta costurile resurselor pentru fiecare unitate contractantă. Când specificați costul resursei pentru o resursă, veți putea, de asemenea, să setați diferite tarife de cost pentru resurse. Această unitate contractantă împrumută aceste resurse de la alte divizii sau practici din cadrul întreprinderii. Tarifele de cost pentru resurse sunt denumite ca prețuri de transfer, împrumuturi de resurse sau prețuri de schimb. Când setați tarifele de cost pentru resursele de împrumut de la alte divizii, utilizați moneda diviziei de împrumut.

## <a name="cost-currency"></a>Monedă de cost

Moneda costurilor este moneda în care costurile sunt raportate pe ecran.. Această monedă este derivată din moneda atașată de câmpul **Unitatea contractantă** pe contract și proiect. Costurile pot fi înregistrate în orice valută pentru un proiect. Cu toate acestea, există o conversie valutară de la costurile valutare în care au fost înregistrate, la moneda de cost a proiectului când este afișată pe ecran.

Datorită faptului că ratele de schimb din platforma Common Data Service (CDS) nu pot fi eficiente la dată, totalele de pe ecran pentru costuri se pot modifica în timp, dacă actualizați ratele de schimb valutar. Cu toate acestea, costurile așa cum au fost înregistrate în baza de date rămân neschimbate deoarece sumele sunt stocate în moneda în care au fost suportate.

## <a name="sales-currency"></a>Monedă de vânzare

Moneda vânzărilor în Project Operations este moneda în care sunt înregistrate și afișate sumele estimate și reale ale vânzărilor. Moneda vânzărilor este de asemenea moneda în care clientul este facturat pentru tranzacție. Într-un contract de proiect, moneda de vânzări este implicită din înregistrarea clientului sau a contului și poate fi modificată atunci când este creat contractul. Atunci când un contract este creat prin închiderea unei oferte câștigate, moneda din contract este implicită din moneda ofertei.

Când creați un contract de proiect de la zero, câmpul **Monedă de vânzare** nu poate fi editat. Listele de prețuri ale produselor și proiectelor sunt implicite în funcție de această monedă din contract.

Spre deosebire de costuri, valorile vânzărilor pot fi înregistrate numai în moneda de vânzări.

## <a name="billing-method"></a>Metodă de facturare

Există în mod obișnuit două tipuri de modele de contracte pentru proiecte, tarif fix și bazat pe consum. Aceste modele sunt reprezentate în Project Operations ca metode de facturare cu două valori posibile:

- Timp și material: Un model de contractare bazat pe consum în care fiecare cost suportat este susținut de venituri corespunzătoare. Pe măsură ce estimați sau suportați mai multe costuri, vânzările corespunzătoare estimate și reale cresc, de asemenea. Specificați limite care nu trebuie depășite pentru liniile de contract care au această metodă de facturare, care limitează venitul real. Veniturile estimate nu sunt afectate de limitele care nu trebuie depășite.
- Preț fix: Un model de contractare cu taxă fixă care indică faptul că valorile vânzărilor vor fi independente de costurile suportate. Valoarea vânzărilor este fixă și nu se modifică pe măsură ce estimați sau suportați mai multe costuri.

## <a name="project-price-lists"></a>Liste de prețuri pentru proiecte

Listele de prețuri ale proiectelor sunt folosite la prețuri implicite, nu la costuri, pentru timp, cheltuială și alte componente legate de proiect. Pot exista mai multe liste de prețuri. Fiecare listă de prețuri are data sa de efectivitate pentru fiecare contract de proiect. Eficacitatea datei suprapuse pe listele de prețuri a proiectului nu este acceptată în Project Operations.

Atunci când un contract de proiect este creat prin câștigarea unei oferte de proiect, listele de prețuri ale proiectului sunt copiate cu numele și data contractului incluse. Copierea acestor informații constituie prețuri personalizate pentru componentele proiectului din acest contract de proiect.

## <a name="transaction-classes"></a>Clase de tranzacții

Project Operations acceptă patru tipuri de clase de tranzacții:

- Timp
- Cheltuială
- Material
- Taxă

Costurile și valorile vânzărilor pot fi estimate și suportate în clasele de tranzacții Timp, Cheltuieli și Materiale. Taxa este o clasă de tranzacții numai pentru venituri.

## <a name="work-entities-and-billing-entities"></a>Entități de muncă și entități de facturare

Entitățile care reprezintă munca sunt proiecte și sarcini. Entitățile care reprezintă aspecte de facturare sunt linii contractuale. Puteți lega diferite entități de lucru la opțiunile de facturare, legându-le la liniile contractuale.

## <a name="multi-customer-deals"></a>Oferte multi-clienți

Ofertele cu mai mulți clienți trebuie să factureze mai mult de un client pentru o ofertă. Exemplele obișnuite includ:

- Întreprinderi OEM și partenerii lor: partenerii și distribuitorii vând un produs cu unele servicii cu valoare adăugată, implicând de obicei o anumită afacere cu un client. OEM se oferă să finanțeze o parte din proiect. 

- Proiecte din sectorul public: mai multe departamente ale unei autorități locale sunt de acord să finanțeze un proiect și sunt facturate conform unei împărțiri convenite anterior. De exemplu, districtul școlar și guvernul local sunt de acord să finanțeze construirea unei piscine.

## <a name="invoice-schedules"></a>Planificări factură

Programele de facturare sunt specifice fiecărei linii de contract și sunt necesare pentru ca facturarea automată să funcționeze. Planificările facturilor sunt create în funcție de anumite date de început și de terminare și de frecvența facturilor. Planificările sunt utilizate în etapa contractului atunci când procesul de creare automată a facturilor este configurat. Atunci când un contract de proiect este creat dintr-o ofertă, programul de facturare este copiat în contractul de proiect din ofertă.

## <a name="changes-from-dynamics-365-sales-orders"></a>Modificările din comenzile Dynamics 365 Sales

Contractele în Project Operations sunt construite pe comenzi în Dynamics 365 Sales. Cu toate acestea, există abateri importante și diferențe de funcționalitate. Contractele au propriile lor elemente de formă și de interfață, reguli de afaceri, logică de afaceri în inserturi și scripturi de partea clientului care le fac unice din Comenzi. Din aceste motive, nu utilizați în mod interschimbabil o Comandă de vânzare și un contract Project Operations.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
