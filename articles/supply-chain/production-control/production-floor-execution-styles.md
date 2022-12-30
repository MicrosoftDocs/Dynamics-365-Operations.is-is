---
title: Hanna viðmót fyrir framkvæmd á framleiðslugólfi
description: Þessi grein útskýrir hvernig á að skilgreina skjámyndastýringar þannig að sjálfgefnir stílar fyrir framkvæmd framleiðslugólfs eru notaðir í þeim.
author: johanhoffmann
ms.date: 11/08/2021
ms.topic: article
ms.search.form: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-02-22
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: ad6ecd591353fe8ddc1a5b9049d65491fb58e98a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8859141"
---
# <a name="style-the-production-floor-execution-interface"></a>Hanna viðmót fyrir framkvæmd á framleiðslugólfi

[!include [banner](../includes/banner.md)]

Þessi grein útskýrir hvernig á að skilgreina skjámyndastýringar þannig að sjálfgefnir stílar fyrir framkvæmd framleiðslugólfs eru notaðir í þeim.

## <a name="forms-and-dialogs"></a>Eyðublöð og gluggar

Aðeins er hægt að nota stíla á skjámynd eða svarglugga ef eftirfarandi kröfur eru uppfylltar:

- Ef skjámyndin á að líkjast fyrirliggjandi skjámynd framvinduskýrslu, þá verður heiti skjámyndarinnar eða svargluggans að byrja á `JmgProductionFloorExecutionCustomInputDialog`.
- Skjámyndin eða svarglugginn getur innihaldið upplýsingahluta skjámyndar. Til að nota stíla í henni verður heiti upplýsingaskjámyndar að byrja á `JmgProductionFloorExecutionCustomDetailsDialog`.
- Ef skjámyndin eða svarglugginn á að vera með einfalt yfirlit verður heiti einfalda yfirlitsins að byrja á `JmgProductionFloorExecutionCustomDialog`. Dæmi um skjámyndir sem eru með einfalt yfirlit eru til að mynda upphafsskjámyndin og skjámynd óbeinna verkþátta.
- Allar stýringar í svarglugganum verða að vera skilgreindar eins og lýst er í þessari grein.

> [!IMPORTANT]
> Eiginleikarnir sem eru nefndir í fyrstu áherslupunktunum í þessum lista þurfa útgáfu 10.0.19 af Supply Chain Management eða nýrri.

Aðeins er hægt að nota stíla á hnappinn **Í lagi** í svarglugga ef eftirfarandi kröfur eru uppfylltar:

- Hnappurinn er geymdur í skjámyndaflokki.
- Heiti flokksins byrjar á `OkButtonGroup`.

Aðeins er hægt að nota stíla á hnappinn **Hætta við** í svarglugga ef eftirfarandi kröfur eru uppfylltar:

- Hnappurinn er geymdur í skjámyndaflokki.
- Heiti flokksins byrjar á `CancelButtonGroup`.

### <a name="header"></a>Haus

Eftirfarandi mynd sýnir dæmigerðan haus skjámyndar eða svarglugga.

![Hefðbundið form eða haus glugga](media/pfe-styles-header.png "Hefðbundið form eða haus glugga")

Í Visual Studio eru hausar búnir til með því að nota uppbyggingu eins og þá sem er sýnd á eftirfarandi mynd.

![Hefðbundin uppbygging kóða til að búa til haus.](media/pfe-styles-header-code-structure.png "Hefðbundin uppbygging kóða til að búa til haus")

Til að bæta texta við haus þinn skaltu nota kóða eins og í eftirfarandi dæmi.

```xpp
private void setCaption()
{
    HeaderFieldWithSeparatorText1.text("Report Progress");
    HeaderFieldWithSeparatorText2.text(ProdId);

    …

    HeaderFieldText.text(OprNum);
}
```

Þegar hausakóðinn er skrifaður skal nota eftirfarandi reglur:

- Nafn aðalflokks þarf að vera `TableRowHeaderGroup`.
- Hver textablokk (aðskilin með táknum) verður að byrja á `HeaderFieldWithSeparatorText`.
- Eftirnafnið verður að byrja á `HeaderFieldText`.
- `CaptionImage` hægt að sleppa.

### <a name="progress-indicator"></a>Framvinduvísir

Þú getur látið fylgja með framvinduvísi, sem birtist hægra megin við hausinn. Eftirfarandi mynd sýnir framvinduvísi.

![Dæmigerður framvinduvísir.](media/pfe-styles-header-progress.png "Dæmigerður framvinduvísir")

Til að sýna framvinduvísinn þarf að geta textareitnum heitið `ShowProgress`.

## <a name="grid"></a>Hnitanet

Stílar eru sjálfkrafa notaðir. Engin sérstök stilling er nauðsynleg.

Hnitanetið á að vera með `TabularView` stíl og skrifa þarf yfir `run()` aðferðina í sérsniðnu skjámyndinni því að nýja hnitanetið er ekki stutt enn sem komið er. Bættu við eftirfarandi kóða.

```xpp
public void run()
{
    super();
    // To opt out a page from the new grid
    this.forceLegacyGrid();
}
```

Til að endurhlaða gögn í aðalyfirliti gætirðu viljað nota eitthvað eins og `this.parmParentForm().updateLayout();` í `click` aðferð aðgerðarinnar. (Skoðaðu t.d. `JmgProductionFloorExecutionReportFeedbackAction` klasann.) Gakktu bara úr skugga um að `parmDataSource` sé stillt í `init` aðferðinni í nýju skjámyndinni (`formCaller.parmDataSource(this.dataSource(1));`). Skoðið til dæmis `JmgProductionFloorExecutionMainGrid` eyðublaðið.

## <a name="card-view"></a>Spjaldyfirlit

Aðeins er hægt að nota stíla á stýringar spjaldyfirlits ef eftirfarandi kröfur eru uppfylltar:

- Hvert spjaldyfirlit er geymt í skjámyndaflokki.
- Heiti flokksins byrjar á `CardGroup` (til dæmis `CardGroupJobsView`).

Eftirfarandi mynd sýnir spjaldyfirlit sem er með engar stýringar innan þess.

![Spjaldyfirlit án eininga.](media/pfe-styles-empty-card.png)

Eftirfarandi skýringarmyndir sýna spjaldyfirlit sem eru með stýringar innan þeirra.

![Spjald með einingum sem sýna Hz.](media/pfe-styles-elements.png)

![Spjald með einingum fyrir viðhaldsbeiðni.](media/pfe-styles-elements-maintenance.png)

## <a name="business-card"></a>Nafnspjald

Aðeins er hægt að nota stíla á stýringar nafnspjalds ef eftirfarandi kröfur eru uppfylltar:

- Hvert nafnspjald er geymt í skjámyndaflokki.
- Heiti flokksins byrjar á `BusinessCardGroup` (til dæmis `BusinessCardGroupJobsList`).

Stilltu eftirfarandi eiginleika á nafnspjaldinu:

- **Stíll:** *listi*
- **Útvíkkaður stíll:** *cardList*
- **Fjölval:** *Nei*
- **Sýna litamerki:** *Nei*

![Nafnspjald.](media/pfe-styles-business-card.png)

## <a name="radio-button"></a>Hringhnappur

Aðeins er hægt að nota stíla á hringhnappa ef eftirfarandi kröfur eru uppfylltar:

- Hver hringhnappur er geymdur í skjámyndaflokki.
- Heiti flokksins byrjar á `RadioTextBelow` eða `RadioTextRight`, eftir því hvar textinn á að birtast.

Stilltu eftirfarandi eiginleika á hringhnappnum:

- **Breytihnappur**: *Haka við*
- **Breytigildi**: *Kveikt* ef velja á hringhnappinn; annars *Slökkt*

Eftirfarandi mynd sýnir dæmi þar sem textinn birtist fyrir neðan hringhnappinn.

![Hringhnappar með texta fyrir neðan.](media/pfe-styles-radio-text-below.png)

Eftirfarandi mynd sýnir dæmi þar sem textinn birtist hægra megin við hringhnappinn.

![Hringhnappar með texta hægra megin.](media/pfe-styles-radio-text-right.png)

### <a name="radio-buttons-in-internet-explorer"></a>Hringhnappar í Internet Explorer

Stílar hringhnappa eru ekki studdir í Internet Explorer. Eftirfarandi skýringarmynd sýnir hvernig hringhnappar líta út í Internet Explorer.

![Hringhnappar í Internet Explorer.](media/pfe-styles-browser.png)

## <a name="buttons"></a>Hnappar

Aðeins er hægt að nota stíla á hnappa ef eftirfarandi kröfur eru uppfylltar:

- Hver hópur af hnöppum er geymdur í skjámyndaflokki. Allir hnappar í hópnum eru með sama stílinn.
- Engar kröfur eru gerðar um heiti hópsins.

Stilltu eftirfarandi eiginleika hnappa:

- **Útlit hnapps:** *TextWithImageLeft*.
- **Venjuleg mynd:** Þessi eiginleiki má ekki vera auður. Notaðu t.d. *CoffeeScript*.
- **Texti**: Þessi eiginleiki má ekki vera auður. Notaðu t.d. *Hefja vinnuhlé*.
- **Breidd:** *Sjálfvirkt* eða *SizeToContent*
- **Hæð:** *Sjálfvirkt* eða *SizeToContent*

### <a name="primary-button"></a>Aðalhnappur

Aðeins er hægt að nota stíla á aðalhnappa ef eftirfarandi kröfur eru uppfylltar:

- Hnappurinn er geymdur í skjámyndaflokki.
- Heiti hópsins byrjar á `DefaultButtonGroup` eða `PrimaryButtonGroup` (til dæmis`DefaultButtonGroup10`).

![Aðalhnappur.](media/pfe-styles-first.png)

### <a name="secondary-button"></a>Aukahnappur

Aðeins er hægt að nota stíla á aukahnappa ef eftirfarandi kröfur eru uppfylltar:

- Hnappurinn er geymdur í skjámyndaflokki.
- Hópurinn er nefndur **Hægra svæði** eða heiti hópsins byrjar á `SecondaryButtonGroup`.

![Aukahnappur.](media/pfe-styles-second.png)

### <a name="third-group-button"></a>Hnappur þriðja hóps

Aðeins er hægt að nota stíla á hnappa þriðja hóps ef eftirfarandi kröfur eru uppfylltar:

- Hnappurinn er geymdur í skjámyndaflokki.
- Hópurinn er nefndur **Vinstra svæði** eða heiti hópsins byrjar á `ThirdButtonGroup`.

![Hnappur þriðja hóps.](media/pfe-styles-third.png)

### <a name="fourth-group-button"></a>Hnappur fjórða hóps

Aðeins er hægt að nota stíla á hnappa fjórða hóps ef eftirfarandi kröfur eru uppfylltar:

- Hnappurinn er geymdur í skjámyndaflokki.
- Heiti flokksins byrjar á `FourthButtonGroup`.

Stilltu eftirfarandi eiginleika hnappsins:

- **Útlit hnapps:** *TextOnly*.
- **Venjuleg mynd:** Þessi eiginleiki verður að vera auður.
- **Texti**: Þessi eiginleiki má ekki vera auður. Notaðu t.d. *Skoða* eða *Breyta*.
- **Breidd:** *Sjálfvirk*.
- **Hæð:** *Sjálfvirk*.

![Hnappur fjórða hóps.](media/pfe-styles-fourth.png)

### <a name="flat-button"></a>Sléttur hnappur

Aðeins er hægt að nota stíla á slétta hnappa ef eftirfarandi kröfur eru uppfylltar:

- Hnappurinn er geymdur í skjámyndaflokki.
- Heiti flokksins byrjar á `FlatButtonGroup`.

Stilltu eftirfarandi eiginleika hnappsins:

- **Útlit hnapps:** *ImageOnly*.
- **Venjuleg mynd:** Þessi eiginleiki má ekki vera auður. Notaðu t.d. *CoffeeScript*.
- **Texti**: Þessi eiginleiki verður að vera auður.
- **Breidd:** *Sjálfvirkt* eða *SizeToContent*
- **Hæð:** *Sjálfvirkt* eða *SizeToContent*

![Sléttur hnappur.](media/pfe-styles-flat-button.png)

### <a name="continue-button"></a>Hnappur til að halda áfram

Aðeins er hægt að nota stíla á framhaldshnappa ef eftirfarandi kröfur eru uppfylltar:

- Hnappurinn er geymdur í skjámyndaflokki.
- Heiti flokksins byrjar á `ContinueButtonGroup`.

Stilltu eftirfarandi eiginleika hnappsins:

- **Útlit hnapps:** *ImageOnly*.
- **Venjuleg mynd:** *Áfram*
- **Texti**: Þessi eiginleiki verður að vera auður.
- **Breidd:** *Sjálfvirkt* eða *SizeToContent*
- **Hæð:** *Sjálfvirkt* eða *SizeToContent*

![Hnappur til að halda áfram.](media/pfe-styles-continue-button.png)

## <a name="combo-box"></a>Samtvinnaður listi

Samsettur gluggi er samsetning þriggja stýringa: innsláttarstýringar, hnapps sem hreinsar innsláttarstýringu og hnapps sem keyrir leit.

Aðeins er hægt að nota stíla á samsetta glugga ef eftirfarandi kröfur eru uppfylltar:

- Samsetti glugginn er geymdur í skjámyndaflokki.
- Heiti flokksins byrjar á `Combobox`.
- Innan hópsins er fyrsta stýringin `AxFormStringControl` stýring. Þessi stýring sýnir núverandi gildi og það er þar sem notandinn slær inn nauðsynlegt gildi.
- Önnur stýringin er `CommonButton` stýring og nafnið byrjar á `ClearButton`. Þessi hnappur verður að innihalda kóða sem notar eiginleikann `enable` til að sýna eða fela hnappinn. Til dæmis til að sýna eða fela hnappinn **Hreinsa** meðan notandinn er að slá inn upplýsingar í innsláttarstýringuna geturðu notað eftirfarandi kóða.

    ```xpp
    public void textChange()
    {
        super();
        ClearButtonSerial.enabled(this.text()? true : false);
    }
    ```

    Þú ættir að hafa eina aðferð þar sem gögnin eru stillt í innsláttarstýringunni. Virkjaðu hnappinn **Hreinsa** í þeirri aðferð. Eftirfarandi er dæmi.

    ```xpp
    public void setSerialId(str _serialId)
    {
        JmgTmpJobBundleProdFeedback.InventSerial = _serialId;
        ClearButtonSerial.enabled(_serialId? true : false);

        if (_serialId)
        {
            this.addSerialNumber();
        }
    }
    ```

    Notið eftirfarandi kóða fyrir aðferðina `clicked` fyrir hnappinn **Hreinsa**.

    ```xpp
    public void clicked()
    {
        element.setSerialId('');
        InventSerialId.setFocus(); // set focus back to the input box
    }
    ```

    Stilltu gildi inntaksstýringarinnar, `AxFormStringControl`, þegar skjámyndin er frumstillt með því að nota `init`-aðferðina. Ef gildið er ekki autt skaltu virkja hnappinn **Hreinsa**. Ef gildið er autt skaltu gera hnappinn **Hreinsa** óvirkan.

- Þriðja stýringin er `CommonButton`stýring og nafnið byrjar á `SearchButton`.

Eftirfarandi mynd sýnir tvær stýringar fyrir samsettan glugga. Samsetti glugginn vinstra megin er með auðan textareit og hnappurinn **Hreinsa** er óvirkur. Samsetti glugginn hægra megin er með texta í textareitnum og hnappurinn **Hreinsa** er virkur.

![Samsettir gluggar með og án hreinsunarhnapps.](media/pfe-styles-combo.png)

## <a name="quick-filter"></a>Hraðsía

Stýring flýtiafmörkun bætir leitarreiti við síðuna. Hægt er að nota stíla á flýtiafmörkun ef eftirfarandi kröfur eru uppfylltar:

- Flýtiafmörkunin er geymd í skjámyndaflokki.
- Heiti flokksins byrjar á `SearchInputGroup`.
- Innan hópsins er fyrsta stýringin `QuickFilter` stýring. (Í þessa stýringu slær notandinn inn leitarstrenginn.)
- Önnur stýringin er `FormStaticTextControl` sem kallast `NumberOfResults`. (Þessi stýring er valfrjáls. Ef það er innifalið sýnir það fjölda fundinna hluta.)
- Þriðja stýringin er `CommonButton`stýring og nafnið byrjar á `ClearButton`.

Eftirfarandi mynd sýnir tvær stýringar flýtiafmörkunar. Flýtiafmörkunin vinstra megin er með auða flýtiafmörkun og fjöldi niðurstaðna er ekki sýnileg. Flýtiafmörkunin til hægri inniheldur leitarstreng og sýnir fjölda niðurstaðna.

![Dæmi um stýringu flýtiafmörkunar með og án leitarstrengs.](media/pfe-styles-quick-filter.png "Dæmi um stýringu flýtiafmörkunar með og án leitarstrengs")

## <a name="center-align-elements-on-a-tab"></a>Miðjujafna einingar í flipa

Til að miðjujafna einingar í flipa verður heiti hópsins að byrja á `TabContentGroup` og hópurinn verður að vera með eftirfarandi eiginleika:

- **Breiddarstilling:** `SizeToAvailable`
- **Hæðarstilling:** `SizeToAvailable`

## <a name="align-a-grid-detail-part-and-quick-filter"></a>Jafna hnitanet, upplýsingahluta og flýtiafmörkun

Til að raða upp sérsniðnu hnitaneti, upplýsingahluta og flýtiafmörkun þannig að það líkist staðlaðri hönnun skal hafa eftirfarandi punkta í huga þegar allt er sett saman:

- Ef hnitanetið er með flýtisíu ætti bæði netið og flýtisían að vera inni í hópnum sem er með heiti sem byrjar á `GridGroup`.
- Til að setja stíla á upplýsingahluta verður heiti hópsins að byrja á `DetailInformationGroup`,

Eftirfarandi mynd sýnir dæmigert net sem inniheldur flýtisíu og upplýsingahluta hægra megin.

![Dæmigert hnitanet sem inniheldur flýtiafmörkun og upplýsingahluta.](media/pfe-styles-align-grid.png "Dæmigert hnitanet sem inniheldur flýtiafmörkun og upplýsingahluta")

Í Visual Studio er hægt að búa til hnitanet, upplýsingahluta og flýtiafmörkun með því að nota skipulag eins og það sem er sýnt á eftirfarandi mynd.

![Dæmigerð kóðauppsetning sem jafnar hnitanet, upplýsingahluta og flýtiafmörkun.](media/pfe-styles-header-code-structure2.png "Dæmigerð kóðauppsetning sem jafnar hnitanet, upplýsingahluta og flýtiafmörkun")

## <a name="additional-resources"></a>Frekari upplýsingar

- [Sérsníða viðmót fyrir framkvæmd á framleiðslugólfi](production-floor-execution-customize.md)
- [Hanna viðmótið fyrir framkvæmd á framleiðslugólfi](production-floor-execution-tabs.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
