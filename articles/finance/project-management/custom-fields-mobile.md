---
title: Innleiða sérstillta reiti fyrir Microsoft Dynamics 365 Project Timesheet-farsímaforritið í iOS og Android
description: Þetta efnisatriði býður upp á algeng mynstur til að nota viðbætur til að innleiða sérstillta reiti.
author: KimANelson
manager: AnnBe
ms.date: 05/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.dyn365.ops.version: 10.0.3
ms.search.validFrom: 2019-05-29
ms.openlocfilehash: c0c578ca44919671b67daeea51a9ec7687f755c9
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773646"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a>Innleiða sérstillta reiti fyrir Microsoft Dynamics 365 Project Timesheet-farsímaforritið í iOS og Android

[!include [banner](../includes/banner.md)]

Þetta efnisatriði býður upp á algeng mynstur til að nota viðbætur til að innleiða sérstillta reiti. Fjallað er um eftirfarandi efnisatriði:

- Hinar ýmsu gagnagerðir sem rammi sérstillts reits styður
- Hvernig á að sýna skrifvarða eða breytanlega reiti í færslum vinnukorts og vista gildi sem notandi hefur bætt við í gagnagrunninn
- Hvernig á að sýna skrifvarða reiti í haus vinnukortsins
- Hvernig á að samþætta annan sérstilltan viðskiptagrunn til að færa inn sjálfgildi í reitina og gera frekari villuleit

## <a name="audience"></a>Notendahópur

Þetta efnisatriði er ætlað þróunaraðilum sem eru að samþætta sérstillta reiti sína við Microsoft Dynamics 365 Project Timesheet-farsímaforritið sem er í boði fyrir Apple iOS og Google Android. Gert er ráð fyrir að lesendur séu kunnugir X++ þróun og virkni vinnukorts fyrir verk.

## <a name="data-contract--tstimesheetcustomfield-x-class"></a>Gagnasamningur - TSTimesheetCustomField X++ klasi

Klasinn **TSTimesheetCustomField** er X++ gagnasamningsklasinn sem veitir upplýsingar um sérstilltan reit fyrir virkni vinnukorts. Listar yfir hluti sérstillts reits eru bæði fluttir yfir í TSTimesheetDetails gagnasamning og TSTimesheetEntry gagnasamning til að sýna sérstillta reiti í farsímaforritinu.

- **TSTimesheetDetails** Síðuhaus vinnukortasamnings.
- **TSTimesheetEntry** - Færsla vinnukortasamnings. Flokkar þessara hluta sem eru með sömu verkupplýsingarnar og gildið **timesheetLineRecId** gera línu.

### <a name="fieldbasetype-types"></a>fieldBaseType (gerðir)

Eiginleikinn **FieldBaseType** í hlutnum **TsTimesheetCustom** ákvarðar gerð reitsins sem birtist í forritinu. Eftirfarandi gildin fyrir **Gerðir** sem eru studdar.

| Gildi gerða | Gerð              | Athugasemdir |
|-------------|-------------------|-------|
| 0           | Strengur (og fasttexti) | Reitinn birtist sem textareitur. |
| 1           | Heiltala           | Gildi er sýnt sem tala án aukastafa. |
| 2           | Rauntala              | Gildi er sýnt sem tala með aukastafi.<p>Til að sýna raunverulegt gildi sem gjaldmiðil í forritinu skal nota eiginleikann **fieldExtenededType**. Hægt er að nota eiginleikann **numberOfDecimals** til að stilla fjölda aukastafa sem á að sýna.</p> |
| 3           | Dagsetning              | Dagsetningarsnið eru ákvörðuð af stillingunum **Dagsetningar-, tíma- og númerasnið** sem notandi velur og eru tilgreind undir **Kjörstilling fyrir tungumál og land/svæði** í **Valkostir notanda**. |
| 4           | Boole           | |
| 15          | GUID              | |
| 16          | Int64             | |

- Ef eiginleikinn **stringOptions** er ekki gefinn upp í hlutnum **TSTimesheetCustomField** er notandanum útvegaður reitur með frjálsum texta.

    Hægt er að nota eiginleikann **stringLength** til að stilla hámarkslengd á streng sem notendur geta fært inn.

- Ef boðið er upp á eiginleikann **stringOptions** í hlutnum **TSTimesheetCustomField** eru þessar listaeiningar einu gildin sem notendur geta valið með því að nota valhnappa (valhringi).

    Í þessu tilviki getur strengjareiturinn virkað sem fasttextagildi gagngert fyrir færslu notanda. Til að vista gildið í gagnagrunninum sem fasttexta skal varpa strengjagildinu handvirkt aftur í fasttextagildið áður en vistað er í gagnagrunninn með því að nota boðleið (sjá kaflann „Nota boðleið í TSTimesheetEntryService-klasanum til að vista vinnukortafærslu úr forritinu aftur í gagnagrunninn“ seinna í þessu efnisatriði til að sjá dæmi).

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a>fieldExtendedType (TSCustomFieldExtendedType)

Hægt er að nota þennan eiginleika til að sníða raunveruleg gildi sem gjaldmiðil. Þessi nálgun á eingöngu við þegar gildið **fieldBaseType** er **Raunverulegt**.

- **TSCustomFieldExtendedType:None** - Ekkert snið er notað.
- **TSCustomFieldExtendedType::Gjaldmiðill** - Sníða gildið sem gjaldmiðil.

    Þegar snið gjaldmiðils er virkt er hægt að nota reitinnn **stringValue** til að flytja gjaldmiðilskóðann áfram sem á að birtast í forritinu. Gildið er skrifvarið gildi.

    Reiturinn **realValue** inniheldur peningaupphæðina sem á að vista í gagnagrunninn.

### <a name="fieldsection-tscustomfieldsection"></a>fieldSection (TSCustomFieldSection)

Hægt er að nota þennan eiginleika til að tilgreina hvar sérstillti reiturinn á að birtast í forritinu.

- **TSCustomFieldSection::Haus** - Reiturinn birtist í hlutanum **Skoða frekari upplýsingar** í forritinu. Þessir reitir eru alltaf skrifvarðir.
- **TSCustomFieldSection::Lína** - Reiturinn birtist á eftir öllum tilbúnum reitarlínum í vinnukortafærslum. Þessir reitir geta verið annaðhvort breytilegir eða skrifvarðir.

### <a name="fieldname-fieldnameshort"></a>fieldName (FieldNameShort)

Þessi eiginleiki ber kennsl á reitinn þegar gildi sem forritið veitir eru vistuð aftur í gagnagrunninn.

### <a name="tablename-tablenameshort"></a>tableName (TableNameShort)

Þessi eiginleiki ber kennsl á reitinn þegar gildi sem forritið veitir eru vistuð aftur í gagnagrunninn.

### <a name="iseditable-noyes"></a>isEditable (NoYes)

Stillið þennan eiginleika á **Já** til að tilgreina að reiturinn í hlutanum fyrir vinnukortafærslur eigi að vera breytanlegur fyrir notanda. Stillið eiginleikann á **Nei** til að gera reitinn skrifvarinn.

### <a name="ismandatory-noyes"></a>isMandatory (NoYes)

Stillið þennan eiginleika á **Já** til að tilgreina að reiturinn í hlutanum fyrir vinnukortafærslur eigi að vera áskilinn.

### <a name="label-str"></a>merki (str)

Þessi eiginleiki tilgreinir merkið sem er sýnt við hliðina á reitnum í forritinu.

### <a name="stringoptions-list-of-strings"></a>stringOptions (listi yfir strengi)

Þessi eiginleiki er eingöngu tiltækur þegar **fieldBaseType** er stillt á **Strengur**. Ef **stringOptions** er stillt eru strengjagildin sem hægt er að velja í gegnum valhnappa (valhringi) tilgreind af strengjunum í listanum. Ef engar strengir eru gefnir upp er innsláttur á frjálsum texta í strengjareitnum leyfður (sjá hlutann „Nota boðleið í TSTimesheetEntryService-klasanum til að vista vinnukortafærslur úr forritinu aftur í gagnagrunninn“ seinna í þessu efnisatriði til að sjá dæmi).

### <a name="stringlength-int"></a>stringLength (int)

Þessi eiginleiki tilgreinir hámarkslengd fyrir strengjareit. Hann er eingöngu tiltækur þegar **fieldBaseType** er stillt á **Strengur**.

### <a name="numberofdecimals-int"></a>numberOfDecimals (int)

Þessi eiginleiki tilgreinir fjölda aukastafa sem eru sýndir í raunverulegum reit. Hann er eingöngu tiltækur þegar **fieldBaseType** er stillt á **Raunverulegur**.

### <a name="ordersequence-int"></a>orderSequence (int)

Þessi eiginleiki stýrir röðinni á sérstilltu reitunum þegar þeir birtast í forritinu þegar fleiri en einn sérstilltur reitur er tilgreindur. Reitir með lægri tölu eru sýndir fyrst.

### <a name="booleanvalue-boolean"></a>booleanValue (boole-gildi)

Fyrir reiti af gerðinni **Boole-gildi** færir þessi eiginleiki boole-gildi reitsins á milli þjónsins og forritsins.

### <a name="guidvalue-guid"></a>guidValue (guid)

Fyrir reiti af gerðinni **GUID** færir þessi eiginleiki gildi fyrir reit alþjóðlegs einkvæms kennimerkis (GUID) á milli þjónsins og forritsins.

### <a name="int64value-int64"></a>int64Value (int64)

Fyrir reiti af gerðinni **Int64** færir þessi eiginleiki int64-gildi reitsins á milli þjónsins og forritsins.

### <a name="intvalue-int"></a>intValue (int)

Fyrir reiti af gerðinni **Int** færir þessi eiginleiki int-gildi reitsins á milli þjónsins og forritsins.

### <a name="realvalue-real"></a>realValue (raunverulegt)

Fyrir reiti af gerðinni **Raunverulegt** færir þessi eiginleiki raunverulegt gildi reitsins á milli þjónsins og forritsins.

### <a name="stringvalue-str"></a>stringValue (str)

Fyrir reiti af gerðinni **Strengur** færir þessi eiginleiki strengjagildi reitsins á milli þjónsins og forritsins. Hann er einnig notaður fyrir reiti af gerðinni **Raunverulegur** sem eru sniðnir sem gjaldmiðill. Fyrir þessa reiti er eiginleikinn notaður til að flytja gjaldmiðilskóða áfram í forritið.

### <a name="datevalue-date"></a>dateValue (dagsetning)

Fyrir reiti af gerðinni **Dagsetning** færir þessi eiginleiki dagsetningargildi reitsins á milli þjónsins og forritsins.

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a>Sýnið og vistið sérstilltan reit í hlutanum fyrir vinnukortafærslu

Hér fyrir neðan er skjámynd úr farsímaforritinu af stofnun vinnukortafærslu. Hún sýnir tilbúnu reitina og sérstilltan reit í hlutanum „Tímafærsla“ sem kallast „Prófunarstrengur“ með fasttextagildi sem „Annar valkostur“ nú þegar stilltan.

![Sérstilltur reitur prófunarstrengs í forritinu](media/timesheet-entry.jpg)



Hér að neðan er skjámynd úr farsímaforriti notandans sem velur einn af valmöguleikum fasttexta sem eru í boði fyrir sérstillta reitinn „Prófunarstrengur“.  Valkostirnir tveir eru „Fyrsti valkostur“ og „Annar valkostur“ sýndir sem valhringir. Annar valkosturinn er valinn.

![Valhnappar (valhringir) fyrir sérstilltan reit prófunarstrengs](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a>Stækka TSTimesheetLine-töfluna svo hún sé með sérstilltan reit

Í dæmigerðum tilfellum er líklegt að gögnin fyrir sérsniðin reit í hlutanum fyrir vinnukortafærslu verði vistuð í TSTimesheetLine-töflunni. Hinsvegar er hægt að nota aðrar töflur ef hægt er að sækja gögnin á grunni TSTimesheetTrans-færslu sem er gefin upp, eða ef hún er ekki með tiltekið færslusamhengi (t.d. ef reiturinn er stilltur sem skrifvarinn í færibreytum verksins).

Athugið að sérstilltu reitirnir eru ekki með nein öryggisafrit af færslum gagnagrunns. Hægt er að mynda þá gagnvirkt á grunni X++ rökfræði. Þessi nálgun getur reynst gagnleg í skrifvörðum aðstæðum (sjá hlutann „Nota boðleið í TSTimesheetDetails-klasanum, buildCustomFieldListForHeader-aðferðina til að fylla út í upplýsingar vinnukorts“ til að sjá dæmi um gagnvirka myndun á gildum sérstillts reits.)

Hér að neðan er skjámynd úr Visual Studio af hugbúnaðarhlutatrénu. Hún sýnir viðbót af TSTimesheetLine-töflunni með TestLineString-töflunni bættri við sem sérstilltur reitur.

![Strengjalína](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a>Notið boðleið í buildCustomFieldList-aðferðinni fyrir TSTimesheetSettings-klasann til að sýna reit í hluta vinnukortafærslunnar

Þessi kóði stýrir skjástillingum fyrir reitinn í forritinu. Hann stýrir t.d. gerð reitsins, merkinu, hvort reiturinn sé áskilinn, og í hvaða hluta reiturinn birtist.

Eftirfarandi dæmi sýnir strengjareit í tímafærslum. Þessi reitur hefur tvo valmöguleika, **Fyrsti valkostur** og **Annar valkostur**, sem eru í boði í gegnum valhnappa (valhringi). Reiturinn í forritinu tengist reitnum **TestLineString** sem er bætt við TSTimesheetLine-töfluna.

Athugið notkun á aðferðinni **TSTimesheetCustomField::newFromMetadata()** til að einfalda frumstillingu á eiginleikum sérstillts reits: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength** og **numberOfDecimals**. Einnig er hægt að stilla þessar færibreytur handvirkt eins og hentar.

```
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

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a>Nota boðleið í buildCustomFieldListForEntry-aðferðinni fyrir TSTimesheetEntry-klasann til að færa gildi inn í tímafærslu

Aðferðin **buildCustomFieldListForEntry** er notuð til að færa gildi í vistuðu vinnukortslínunum inn í farsímaforritið. Hún tekur TSTimesheetTrans-færslu sem færibreytu. Reiti úr þeirri færslu er hægt að nota til að setja inn gildið fyrir sérstilltan reit í forritinu.

```
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

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a>Nota boðleið í TSTimesheetEntryService-klasanum til að vista vinnukortafærslur úr forritinu aftur í gagnagrunninn

Til að vista sérstilltan reit aftur í gagnagrunninn við dæmigerða notkun, þarf að víkka út margar aðferðir:

- Aðferðin **timesheetLineNeedsUpdating** er notuð til að ákvarða hvort notandinn hafi breytt línufærslunni í forritinu og verði að vista hana í gagnagrunninum. Ef afköst eru ekki áhyggjuefni er hægt að einfalda þessa aðferð svo hún skili alltaf **satt**.
- Aðferðirnar **populateTimesheetLineFromEntryDuringCreate** og **populateTimesheetLineFromEntryDuringUpdate** er hægt að stækka svo þær færi gildi inn í færslu gagnagrunns TSTimesheetLine úr færslu TSTimesheetEntry-gagnasamnings sem gefin er upp. Takið eftir í eftirfarandi dæmi hvernig vörpun milli gagnagrunnsreits og færslureits er gerð handvirkt með X++ kóða.
- Einnig er hægt að stækka aðferðina **populateTimesheetWeekFromEntry** ef sérstilltur reitur sem er varpað í hlutinn **TSTimesheetEntry** verður að skrifa til baka til gagnagrunnstöflunnar TSTimesheetLineweek.

> [!NOTE]
> Eftirfarandi dæmi vistar gildið **firstOption** eða **secondOption** sem notandinn velur í gagnagrunninn sem óunnið strengjagildi. Ef gagnagrunnsreiturinn er reitur af gerðinni **Fasttexti** er hægt að varpa þessum gildum handvirkt í fasttextagildi og síðan vista þau í fasttextareit í gagnagrunnstöflunni.

```
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

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a>Sýna sérstilltan reit í hluta vinnukortahauss

Hér fyrir neðan er skjámynd úr farsímaforritinu af notanda að skoða vinnukort. Hnappurinn „Frekari upplýsingar“ hefur verið valinn efst í hægra horninu til að sýna valkostinn „Skoða frekari upplýsingar“.  

![Skipun fyrir að skoða frekari upplýsingar](media/show-more.png)

Hér fyrir neðan er skjámynd úr farsímaforritinu sem sýnir „Meira“ hlutann í vinnukorti. Sérstilltur reitur sem kallast „Nýtingarhlutfall á þessu vinnukorti (reiknaður sérstilltur reitur)“ hefur verið bætt við í haus vinnukortsins. Skrifvarið gildi upp á „0,667“ er stillt fyrir sérstillta reitinn.

![Meira](media/more-section.jpg)

### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a>Stækka TSTimesheetTable-töfluna svo hún sé með sérstilltan reit

Í dæmigerðum tilfellum er líklegt að gögnin fyrir sérsniðinn reit í hausnum verði sótt úr TSTimesheetHeader-töflunni. Hinsvegar er hægt að nota aðrar töflur ef hægt er að sækja gögnin á grunni TSTimesheetTable-færslu sem er gefin upp, eða ef hún er ekki með tiltekið færslusamhengi (t.d. ef reiturinn er stilltur sem skrifvarinn í færibreytum verksins).

Athugið að sérstilltu reitirnir eru ekki með nein öryggisafrit af færslum gagnagrunns. Hægt er að mynda þá gagnvirkt á grunni X++ rökfræði. Dæmið sem fylgir sýnir þessa nálgun.

Reitir í hausnum eru alltaf skrifvarðir í forritinu.

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a>Nota boðleið í buildCustomFieldList-aðferðinni fyrir TSTimesheetSettings-klasann til að sýna reit í hausnum

Þessi kóði stýrir skjástillingum fyrir reitinn í forritinu. Hann stýrir t.d. gerð reitsins, merkinu, hvort reiturinn sé áskilinn, og í hvaða hluta reiturinn birtist.

Eftirfarandi dæmi sýnir reiknað gildi í hausnum í forritinu.

```
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

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a>Nota boðleið fyrir aðferðina buildCustomFieldListForHeader í TSTimesheetDetails-klasanum til að fylla út upplýsingar um vinnukort

Aðferðin **buildCustomFieldListForHeader** er notuð til að fylla út upplýsingar vinnukortahauss í farsímaforritinu. Hún notar TSTimesheetTable-færslu sem færibreytu. Reiti úr þeirri færslu er hægt að nota til að setja inn gildið fyrir sérstilltan reit í forritinu. Eftirfarandi dæmi les ekki nein gildi úr gagnagrunninum. Þess í stað notar það X++ reikniaðgerðir til að búa til reiknað gildi sem síðan er sýnt í forritinu.


```
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

## <a name="other-configurabilityextensibility-opportunities"></a>Aðrir möguleikar á stillingum/stækkunarhæfni

### <a name="adding-additional-validation-for-the-app"></a>Bæta við frekari villuleit fyrir forritið

Núverandi reikniaðgerðir fyrir virkni vinnukorts á gagnagrunnsstigi virka enn eins og venjulega. Til að trufla málalyktir á aðgerðum vistunar og innsendingar og sýna tiltekin villuboð er hægt að bæta **sýna villu („skilaboð til notanda“)** við kóðann í gegnum viðbót boðleiðar. Hér eru þrjú dæmi um gagnlegar aðferðir fyrir stækkanleika:

- Ef **validateWrite** í TSTimesheetLine-töflunni skilar **rangt** við vistun á aðgerð fyrir vinnukortslínu birtast villuboð í farsímaforritinu.
- Ef **validateSubmit** í TSTimesheetTable-töflunni skilar **rangt** við innsendingu á vinnukorti í forritinu fær notandinn villuboð.
- Reikniaðgerð sem fyllir út reiti (t.d. **Línueiginleiki**) þegar aðferðin **setja inn** stendur yfir í TSTimesheetLine-töflunni mun halda áfram að keyra.

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a>Fela og merkja tilbúna reiti sem skrifvarða í gegnum grunnstillingu

Úr færibreytum verka er hægt að gera tilbúna reiti skrifvarða eða fela þá í farsímaforritinu. Stillið valmöguleikana í hlutanum **Vinnukort farsíma** í flipanum **Vinnukort** á síðunni **Verkefnastjórnun og bókhaldsfæribreytur**.

![Færibreytur verka](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a>Breyting á verkþáttum sem hægt er að velja í gegnum viðbætur

Verkþættirnir sem hægt er að velja fyrir verk eru fylltir út í gegnum aðferðirnar **getActivitiesForProject()** og **getActivityQuery()** í klasanum **TsTimesheetProjectService**. Hægt er að nota boðleið til að breyta þessari hegðun til að passa við rekstraraðstæður þínar fyrir verkþættina sem hægt er að velja fyrir tiltekið verk.

### <a name="entering-a-default-project-category-on-timesheet-entries"></a>Færa sjálfgefna verktegund inn í vinnukortafærslur

Færsla á sjálfgefinni verktegund inn í vinnukortafærslur gerist á þremur stigum. Hægt er að nota boðleið til að víkka út hegðunina á hvaða stigi sem er eða þeim öllum til að ná fram æskilegri hegðun. Eftirfarandi stigveldi er notað:

1. Forritið reynir að setja inn sjálfgefna tegund úr tilföngum verks. Þessi sjálfgefna tegund er stillt í aðferðunum **getCurrentUserResource** and **getDelegatedResourcesForCurrentUser** í klasanum **TSTimesheetSettingsService**.
2. Ef ekki er boðið upp á sjálfgefna tegund á stigi verktilfanga reynir forritið að sækja það úr verkþættinum. Þessi sjálfgefna tegund er stillt í aðferðinni **getActivitiesForProject** í klasanum **TSTimesheetProjectService**.
3. Ef ekki er boðið upp á sjálfgefna tegund á stigi verkþáttar er náð í sjálfgefnu tegundina úr færibreytum verks. Þessi sjálfgefna tegund er stillt í aðferðinni **fáProjectDetailsbyRule** í klasanum **TSTimesheetProjectService**.
