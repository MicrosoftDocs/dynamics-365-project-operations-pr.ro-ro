---
title: Implementați câmpuri personalizate pentru aplicație mobilă Microsoft Dynamics 365 Project Timesheet pe iOS și Android
description: Acest articol oferă modele comune pentru utilizarea extensiilor pentru a implementa câmpuri personalizate.
author: Yowelle
ms.date: 05/29/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.3
ms.search.validFrom: 2019-05-29
ms.openlocfilehash: 03b79d58d1f91e07034b8c9efb408e6d7a9c29a8
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913727"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a>Implementați câmpuri personalizate pentru aplicație mobilă Microsoft Dynamics 365 Project Timesheet pe iOS și Android

[!include [banner](../includes/banner.md)]

Acest articol oferă modele comune pentru utilizarea extensiilor pentru a implementa câmpuri personalizate. Sunt abordate următoarele articole:

- Diferitele tipuri de date acceptate de cadrul de câmp personalizat
- Cum se afișează câmpuri numai în citire sau editabile în intrările din foaia de pontaj și cum se salvează valorile furnizate de utilizator în baza de date
- Cum se afișează câmpuri numai în citire în antetul foii de pontaj
- Cum se integrează alte logici de afaceri personalizate pentru a introduce valorile implicite în câmpuri și pentru a efectua validări suplimentare

## <a name="audience"></a>Public

Acest articol este destinat dezvoltatorilor care își integrează câmpurile personalizate în aplicație mobilă Microsoft Dynamics 365 Project Timesheet disponibilă pentru Apple iOS și Google Android. Ipoteza este că cititorii sunt familiarizați cu dezvoltarea X++ și funcționalitatea foii de timp a proiectului.

## <a name="data-contract--tstimesheetcustomfield-x-class"></a>Contract de date - clasa TSTimesheetCustomField X++

Clasa **TSTimesheetCustomField** este clasa contractului de date X++ care reprezintă informații despre un câmp personalizat pentru funcționalitatea foii de pontaj. Listele obiectelor de câmp personalizate sunt transmise atât în contractul de date TSTimesheetDetails, cât și în contractul de date TSTimesheetEntry pentru a afișa câmpuri personalizate în aplicația mobilă.

- **TSTimesheetDetails** - Contractul antetului de foaie de pontaj.
- **TSTimesheetEntry** - Contractul de tranzacție cu foaie de pontaj. Grupuri de aceste obiecte care au aceleași informații despre proiect și valoarea **timesheetLineRecId** constituie o linie.

### <a name="fieldbasetype-types"></a>fieldBaseType (Tipuri)

Proprietatea **FieldBaseType** pe obiectul **TsTimesheetCustom** determină tipul câmpului care apare în aplicație. Următoarele valori de **Tipuri** care sunt acceptate.

| Tipuri de valoare | Tip              | Note |
|-------------|-------------------|-------|
| 0           | Șir (și Enum) | Câmpul apare ca un câmp de text. |
| 1           | Integer           | Valoarea este afișată ca un număr fără zecimale. |
| 2           | Real              | Valoarea este afișată ca un număr care are zecimale.<p>Pentru a afișa valoarea reală ca monedă în aplicație, utilizați proprietatea **fieldExtenededType**. Puteți utiliza proprietatea **numberOfDecimals** pentru a seta numărul de zecimale care sunt afișate.</p> |
| 3           | Data              | Formatele de dată sunt determinate de setarea utilizatorului **Data, orele și formatul numerelor** care este specificată la **Limba și preferința țării/regiunii** în **Opțiuni utilizator**. |
| 4           | Boolean           | |
| 15          | GUID              | |
| 16          | Int64             | |

- Dacă proprietatea **stringOptions** nu este furnizată pe obiectul **TSTimesheetCustomField**, un câmp de text liber este furnizat utilizatorului.

    Proprietatea **stringLength** poate fi utilizată pentru a seta lungimea maximă a șirului pe care utilizatorii o pot introduce.

- Dacă proprietatea **stringOptions** este furnizată pe obiectul **TSTimesheetCustomField**, acele elemente de listă sunt singurele valori pe care utilizatorii le pot selecta folosind butoanele de opțiune (butoanele radio).

    În acest caz, câmpul șir poate acționa ca o valoare enum în scopul intrării utilizatorului. Pentru a salva valoarea în baza de date ca o enumerare, mapați manual valoarea șirului înapoi la valoarea enumerată înainte de a salva în baza de date utilizând lanțul de comandă (consultați secțiunea „Utilizați lanțul de comandă din clasa TSTimesheetEntryService pentru a salva o intrare din foaia de pontaj din aplicație înapoi în baza de date" de mai târziu din acest articol pentru o exemplificare).

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a>fieldExtendedType (TSCustomFieldExtendedType)

Puteți utiliza această proprietate pentru a formata valorile reale ca monedă. Această abordare este aplicabilă numai atunci când valoarea **fieldBaseType** este **Reală**.

- **TSCustomFieldExtendedType:None** – Nu se aplică nicio formatare.
- **TSCustomFieldExtendedType::Currency** – Formatați valoarea ca monedă.

    Când formatarea monedei este activă, câmpul **stringValue** poate fi folosit dincolo de codul monedei care ar trebui să fie afișat în aplicație. Valoarea este o valoare numai în citire.

    Câmpul **realValue** conține suma de bani care trebuie salvată în baza de date.

### <a name="fieldsection-tscustomfieldsection"></a>fieldSection (TSCustomFieldSection)

Puteți utiliza această proprietate, specificați unde ar trebui să apară câmpul personalizat în aplicație.

- **Antetul TSCustomFieldSection::** – Câmpul va apărea în secțiunea **Vizualizați mai multe detalii** din aplicație. Aceste câmpuri sunt întotdeauna numai în citire.
- **Linia TSCustomFieldSection::** - Câmpul va apărea după toate câmpurile de linie predefinite de pe intrările de foaie de pontaj. Aceste câmpuri pot fi modificabile sau doar în citire.

### <a name="fieldname-fieldnameshort"></a>fieldName (FieldNameShort)

Această proprietate identifică câmpul atunci când valorile pe care le oferă aplicația sunt salvate înapoi în baza de date.

### <a name="tablename-tablenameshort"></a>tableName (TableNameShort)

Această proprietate identifică câmpul atunci când valorile pe care le oferă aplicația sunt salvate înapoi în baza de date.

### <a name="iseditable-noyes"></a>isEditable (NoYes)

Setați această proprietate la **Da** pentru a specifica că câmpul din secțiunea de introducere a foii de pontaj ar trebui să fie modificabil de către utilizatori. Setați proprietatea la **Nu** pentru a trece câmpul numai în citire.

### <a name="ismandatory-noyes"></a>isMandatory (NoYes)

Setați această proprietate la **Da** pentru a specifica că câmpul din secțiunea de introducere a foii de pontaj ar trebui să fie obligatoriu.

### <a name="label-str"></a>label (str)

Această proprietate specifică eticheta care este afișată lângă câmpul din aplicație.

### <a name="stringoptions-list-of-strings"></a>stringOptions (Lista de șiruri)

Această proprietate este aplicabilă numai atunci când **fieldBaseType** este setat la **Șir**. Dacă **stringOptions** este setat, valorile șirurilor disponibile pentru selectare prin butoanele de opțiune (butoanele radio) sunt specificate de șirurile din listă. Dacă nu sunt furnizate șiruri, este permisă introducerea textului liber în câmpul șirului (consultați secțiunea „Utilizați lanțul de comandă din clasa TSTimesheetEntryService pentru a salva o intrare din foaia de pontaj din aplicație înapoi în baza de date" mai târziu în acest articol pentru exemplificare) .

### <a name="stringlength-int"></a>stringLength (int)

Această proprietate specifică lungimea maximă pentru un câmp șir. Aceasta se aplică numai atunci când **fieldBaseType** este setat la **Șir**.

### <a name="numberofdecimals-int"></a>numberOfDecimals (int)

Această proprietate specifică numărul de zecimale care sunt afișate pentru un câmp real. Aceasta se aplică numai atunci când **fieldBaseType** este setat la **Real**.

### <a name="ordersequence-int"></a>orderSequence (int)

Această proprietate controlează ordinea în care câmpurile personalizate sunt afișate în aplicație atunci când sunt specificate mai multe câmpuri personalizate. Câmpurile care au numere mai mici sunt afișate mai întâi.

### <a name="booleanvalue-boolean"></a>booleanValue (boolean)

Pentru câmpurile de tipul **Boolean**, această proprietate trece valoarea booleană a câmpului dintre server și aplicație.

### <a name="guidvalue-guid"></a>guidValue (guid)

Pentru câmpurile de tipul **GUID**, această proprietate trece valoarea identificator unic global (GUID) a câmpului dintre server și aplicație.

### <a name="int64value-int64"></a>int64Value (int64)

Pentru câmpurile de tipul **Int64**, această proprietate trece valoarea Int64 a câmpului dintre server și aplicație.

### <a name="intvalue-int"></a>intValue (int)

Pentru câmpurile de tipul **Int**, această proprietate trece valoarea Int a câmpului dintre server și aplicație.

### <a name="realvalue-real"></a>realValue (reală)

Pentru câmpurile de tipul **Reală**, această proprietate trece valoarea reală a câmpului dintre server și aplicație.

### <a name="stringvalue-str"></a>stringValue (str)

Pentru câmpurile de tipul **Șir**, această proprietate trece valoarea șirului câmpului dintre server și aplicație. Este, de asemenea, utilizat pentru câmpurile de tipul **Real** care sunt formatate ca monedă. Pentru acele câmpuri, proprietatea este utilizată pentru a transmite codul monedei aplicației.

### <a name="datevalue-date"></a>dateValue (data)

Pentru câmpurile de tipul **Data**, această proprietate trece valoarea datei câmpului dintre server și aplicație.

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a>Afișați și salvați un câmp personalizat în secțiunea de introducere a foii de pontaj

Mai jos este o captură de ecran din aplicația mobilă a unei creații de intrare a foii de pontaj. Afișează câmpurile predefinite și un câmp personalizat în secțiunea „Intrare pontaj” numită „Șir de testare”, cu o valoare enum de „A doua opțiune” deja setată.

![Testați câmpul personalizat al șirului în aplicație.](media/timesheet-entry.jpg)



Mai jos este o captură de ecran din aplicația mobilă a utilizatorului care selectează una dintre opțiunile de enum disponibile pentru câmpul personalizat „Șir de testare”.  Cele două opțiuni sunt „Prima opțiune” și „A doua opțiune” afișate ca butoane radio. În prezent, este selectată a doua opțiune.

![Butoane de opțiune (butoane radio) pentru câmpul personalizat Șir de testare.](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a>Extindeți tabelul TSTimesheetLine astfel încât să aibă un câmp personalizat

În scenarii tipice, este probabil ca datele pentru un câmp personalizat din secțiunea de intrare a foii de pontaj să fie salvate în tabelul TSTimesheetLine. Cu toate acestea, se pot utiliza și alte tabele dacă datele pot fi recuperate pe baza unei înregistrări TSTimesheetTrans furnizate sau dacă nu au un context de înregistrare specific (de exemplu, dacă câmpul este setat ca numai în citire în parametrii proiectului) .

Rețineți că câmpurile personalizate nu trebuie să aibă nicio înregistrare de bază de date. Ele pot fi generate dinamic pe baza logicii X++. Această abordare poate fi utilă în scenarii doar de citire (consultați secțiunea „Utilizați lanțul de comandă din clasa TSTimesheetDetails, metoda buildCustomFieldListForHeader pentru a completa detaliile foii de pontaj” pentru un exemplu de valori ale câmpurilor personalizate generate dinamic.)

Mai jos este o captură de ecran din Visual Studio din arborele obiectelor aplicației. Afișează o extensie a tabelului TSTimesheetLine cu câmpul TestLineString adăugat ca un câmp personalizat.

![Șir de linie.](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a>Utilizați lanțul de comandă pe metoda buildCustomFieldList a clasei TSTimesheetSettings pentru a afișa un câmp în secțiunea de intrare a foii de pontaj

Acest cod controlează setările de afișare pentru câmpul din aplicație. De exemplu, controlează tipul de câmp, eticheta, dacă câmpul este obligatoriu și în ce secțiune apare câmpul.

Următorul exemplu arată un câmp șir la intrările de timp. Acest câmp are două opțiuni, **Prima opțiune** și **A doua opțiune**, care sunt disponibile prin intermediul butoanelor de opțiune (butoane radio). Câmpul din aplicație este asociat cu câmpul **TestLineString** care este adăugat la tabelul TSTimesheetLine.

Rețineți utilizarea metodei **TSTimesheetCustomField::newFromMetatdata()** pentru simplificarea inițializării proprietăților câmpului personalizat: **fieldBaseType**, **tableName**, **fieldname**, **eticheta**, **isEditable**, **isMandatory**, **stringLength** și **numberOfDecimals**. De asemenea, puteți seta acești parametri manual, după cum doriți.

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('Second option');
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a>Utilizați lanțul de comandă pe metoda buildCustomFieldListForEntry a clasei TSTimesheetEntry pentru a introduce valori într-o intrare de foaie de pontaj

Metoda **buildCustomFieldListForEntry** este utilizată pentru a introduce valori pe liniile de foaie de pontaj salvate în aplicația mobilă. Este nevoie de o înregistrare TSTimesheetTrans ca parametru. Câmpurile din acea înregistrare pot fi folosite pentru a completa valoarea câmpului personalizat din aplicație.

```xpp
...
[ExtensionOf(classStr(TsTimesheetEntry))]
final class TsTimesheetEntry_Extension
{
    protected List buildCustomFieldListForEntry(TSTimesheetTrans _tsTimesheetTrans)
    {
        List customFieldList = next buildCustomFieldListForEntry(_tsTimesheetTrans);
        TSTimesheetLine tsTimesheetLine = _tsTimesheetTrans.timesheetLine();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        tsTimesheetCustomField.parmStringValue(tsTimesheetLine.TestLineString);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('second option;);
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a>Utilizați lanțul de comandă din clasa TSTimesheetEntryService pentru a salva o intrare din foaia de pontaj din aplicație înapoi în baza de date

Pentru a salva un câmp personalizat înapoi în baza de date în utilizarea obișnuită, trebuie să extindeți mai multe metode:

- Metoda **timesheetLineNeedsUpdating** este utilizată pentru a determina dacă înregistrarea de linie a fost modificată de utilizator în aplicație și trebuie salvată în baza de date. Dacă performanța nu este o problemă, această metodă poate fi simplificată astfel încât să returneze întotdeauna **true**.
- Metodele **populateTimesheetLineFromEntryDuringCreate** și **populateTimesheetLineFromEntryDuringUpdate** pot fi extinse astfel încât să introducă valori în înregistrarea bazei de date TSTimesheetLine din înregistrarea contractului de date TSTimesheetEntry care este furnizat. În exemplul care urmează, observați cum maparea între câmpul bazei de date și câmpul de intrare se face manual prin codul X++.
- Metoda **populateTimesheetWeekFromEntry** poate fi extinsă și în cazul în care câmpul personalizat care este mapat la obiectul **TSTimesheetEntry** trebuie să proceseze datele în tabelul bazei de date TSTimesheetLineweek.

> [!NOTE]
> Următorul exemplu salvează valoarea **firstOption** sau **secondOption** pe care utilizatorul o selectează în baza de date ca valoare brută a șirului. Dacă câmpul bazei de date este un câmp de tipul **Enum**, acele valori pot fi mapate manual la o valoare enum și apoi salvate într-un câmp enum de pe tabelul bazei de date.

```xpp
...
[ExtensionOf(classStr(TSTimesheetEntryService))]
final class TSTimesheetEntryService_Extension
{
    protected boolean timesheetLineNeedsUpdating(TSTimesheetLine _tsTimesheetLine,
    TsTimesheetEntry _tsTimesheetEntry)
    {
        boolean ret = next timesheetLineNeedsUpdating(_tsTimesheetLine,
        _tsTimesheetEntry);
        if (!ret)
        {
            */ Loop through custom fields to see if value needs updating*/
            ListEnumerator enumerator =  _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    */ If Custom field value for TestLineString field has changed, We need to update the timesheet line.*/
                    if (_tsTimesheetLine.TestLineString != customField.parmStringValue())
                    {
                        ret = true;
                    }
                }
            }
        }
        return ret;
    }
    protected void populateTimesheetLineFromEntryDuringCreate(TSTimesheetLine
    _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
    {
        next populateTimesheetLineFromEntryDuringCreate(_tsTimesheetLine,
        _tsTimesheetEntry);
        this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
        _tsTimesheetEntry);
        }
        protected void populateTimesheetLineFromEntryDuringUpdate(TSTimesheetLine
        \_tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            next populateTimesheetLineFromEntryDuringUpdate(_tsTimesheetLine,
            _tsTimesheetEntry);
            this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
            _tsTimesheetEntry);
        }
        private void populateTimesheetLineFromCustomFields(TSTimesheetLine
        _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            ListEnumerator enumerator =
            _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    _tsTimesheetLine.TestLineString = customField.parmStringValue();
                }
            }
        }
    }
...
```

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a>Afișați un câmp personalizat în secțiunea de antet a foii de pontaj

Mai jos este o captură de ecran din aplicația mobilă a unui utilizator care vizualizează o foaie de pontaj. Butonul „Mai multe informații” a fost selectat în colțul din dreapta sus pentru a afișa opțiunea „Vizualizați mai multe detalii”.  

![Afișați mai multe detalii de comandă.](media/show-more.png)

Mai jos este o captură de ecran din aplicația mobilă care arată secțiunea „Mai multe” a unei foi de pontaj. Un câmp personalizat numit „Rata de utilizare a acestei foi de pontaj (câmp personalizat calculat)” a fost adăugat la secțiunea de antet a foii de pontaj. O valoare de numai în citire „0.667” este setată în câmpul personalizat.

![Mai multe secțiuni.](media/more-section.jpg)

### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a>Extindeți tabelul TSTimesheetTable astfel încât să aibă un câmp personalizat

În scenarii tipice, este probabil ca datele pentru un câmp personalizat din secțiunea de antet să fie extrase din tabelul TSTimesheetTable. Cu toate acestea, se pot utiliza și alte tabele dacă datele pot fi recuperate pe baza unei înregistrări TSTimesheetTable furnizate sau dacă nu au un context de înregistrare specific (de exemplu, dacă câmpul este setat ca numai în citire în parametrii proiectului) .

Rețineți că câmpurile personalizate nu trebuie să aibă nicio înregistrare de bază de date. Ele pot fi generate dinamic pe baza logicii X++. Exemplul care urmează arată această abordare.

Câmpurile din secțiunea antet sunt întotdeauna numai în citire în aplicație.

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a>Utilizați lanțul de comandă pe metoda buildCustomFieldList a clasei TSTimesheetSettings pentru a afișa un câmp în secțiunea de antet

Acest cod controlează setările de afișare pentru câmpul din aplicație. De exemplu, controlează tipul de câmp, eticheta, dacă câmpul este obligatoriu și în ce secțiune apare câmpul.

Următorul exemplu arată o valoare calculată în secțiunea antet din aplicație.

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a>Utilizați lanțul de comandă pe metoda buildCustomFieldListForHeader a clasei TSTimesheetDetails pentru a completa detaliile foii de pontaj

Metoda **buildCustomFieldListForHeader** este utilizată pentru a completa detaliile antetului foii de pontaj în aplicația mobilă. Este nevoie de o înregistrare TSTimesheetTable ca parametru. Câmpurile din acea înregistrare pot fi folosite pentru a completa valoarea câmpului personalizat din aplicație. Următorul exemplu nu citește nicio valoare din baza de date. În schimb, folosește logica X++ pentru a genera o valoare calculată care este apoi afișată în aplicație.


```xpp
...
[ExtensionOf(classStr(TSTimesheetDetails))]
final class TSTimesheetDetails_Extension
{
    protected List buildCustomFieldListForHeader(TSTimesheetTable
    _tsTimesheetTable)
    {
        List customFieldList = next buildCustomFieldListForHeader(_tsTimesheetTable);
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        real utilizationRate = 0;
        if (_tsTimesheetTable.totalHours() != 0)
        {
            utilizationRate = _tsTimesheetTable.totalHoursBillable() /
            _tsTimesheetTable.totalHours();
        }
        tsTimesheetCustomField.parmRealValue(utilizationRate);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

## <a name="other-configurabilityextensibility-opportunities"></a>Alte posibilități de configurabilitate/extensibilitate

### <a name="adding-additional-validation-for-the-app"></a>Adăugarea unei validări suplimentare pentru aplicație

Logica existentă pentru funcționalitatea foii de pontaj la nivelul bazei de date va funcționa în continuare așa cum era de așteptat. Pentru a întrerupe finalizarea operațiilor de salvare sau trimitere și pentru a afișa un anumit mesaj de eroare, puteți adăuga **eroare de returnare („mesaj către utilizator”)** către cod printr-un lanț de extensie de comandă. Iată trei exemple de metode extensibile utile:

- Dacă **validateWrite** în tabelul TSTimesheetLine returnează **fals** în timpul unei operații de salvare pentru o linie de foaie de pontaj, un mesaj de eroare este afișat în aplicația mobilă.
- Dacă **validateSubmit** în tabelul TSTimesheetTable returnează **fals** în timpul trimiterii foii de pontaj în aplicație, un mesaj de eroare este afișat în aplicația mobilă.
- Logica care completează câmpuri (de exemplu, **Linia de proprietate**) în timpul metodei **inserare** de pe tabelul TSTimesheetLine va rula în continuare.

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a>Ascunderea și marcarea câmpurilor predefinite ca doar citire prin configurare

Din parametrii proiectului, puteți crea câmpuri predefinite doar în citire sau ascunse în aplicația mobilă. Setați opțiunile din secțiunea **Fișe de pontaj mobile** de pe fila **Fișă de pontaj** din pagina **Managementul proiectului și parametrii contabili**.

![Parametri proiect.](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a>Schimbarea activităților disponibile pentru selectare prin extensii

Activitățile disponibile pentru selectarea unui proiect sunt completate prin intermediul metodelor **getActivitiesForProject()** și **getActivityQuery()** în clasa **TsTimesheetProjectService**. Puteți utiliza lanțul de comandă pentru a modifica acest comportament pentru a se potrivi scenariului dvs. de afaceri pentru activitățile disponibile pentru selectare pentru un anumit proiect.

### <a name="entering-a-default-project-category-on-timesheet-entries"></a>Introducerea unei categorii de proiect implicite la intrările din foaia de pontaj

Introducerea unei categorii de proiect implicite la intrările din foaia de pontaj are loc la trei niveluri. Puteți utiliza lanțul de comandă pentru a extinde comportamentul la oricare sau la toate aceste niveluri pentru a atinge comportamentul dorit. Se utilizează următoarea ierarhie:

1. Aplicația încearcă să plaseze categoria implicită din resursa proiectului. Această categorie implicită este setată în metodele **getCurrentUserResource** și **getDelegatedResourcesForCurrentUser** în clasa **TSTimesheetSettingsService**.
2. Dacă categoria implicită nu este furnizată la nivelul resurselor proiectului, aplicația încearcă să o retragă din activitatea proiectului. Această categorie implicită este setată în metoda **getActivitiesForProject** în clasa **TSTimesheetProjectService**.
3. Dacă categoria implicită nu este furnizată la nivelul activității proiectului, categoria implicită a fost luată din parametrii proiectului. Această categorie implicită este setată în metoda **getProjectDetailsbyRule** în clasa **TSTimesheetProjectService**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]