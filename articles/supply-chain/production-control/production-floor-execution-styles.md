---
title: Hanna viðmót fyrir framkvæmd á framleiðslugólfi
description: Greinin útskýrir hvernig á að stilla eyðublaðastýringar þannig að sjálfgefna framleiðslugólfsframkvæmdastíllinn sé notaður á þær.
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
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8859141"
---
# <a name="style-the-production-floor-execution-interface"></a>Hanna viðmót fyrir framkvæmd á framleiðslugólfi

[!include [banner](../includes/banner.md)]

Greinin útskýrir hvernig á að stilla eyðublaðastýringar þannig að sjálfgefna framleiðslugólfsframkvæmdastíllinn sé notaður á þær.

## <a name="forms-and-dialogs"></a>Eyðublöð og gluggar

Aðeins er hægt að nota stíla á skjámynd eða svarglugga ef eftirfarandi kröfur eru uppfylltar:

- Ef eyðublaðið ætti að líkjast núverandi eyðublaði fyrir framvindu skýrslu verður nafn eyðublaðsins eða gluggans að byrja á `JmgProductionFloorExecutionCustomInputDialog`.
- Skjámyndin eða svarglugginn getur innihaldið upplýsingahluta skjámyndar. Til að beita stílum á það verður nafn smáatriðahlutans að byrja á `JmgProductionFloorExecutionCustomDetailsDialog`.
- Ef eyðublaðið eða svarglugginn ætti að hafa einfalda yfirsýn, þá verður nafn einfalda yfirlitsins að byrja á `JmgProductionFloorExecutionCustomDialog`. Dæmi um skjámyndir sem eru með einfalt yfirlit eru til að mynda upphafsskjámyndin og skjámynd óbeinna verkþátta.
- Allar stýringar í glugganum verða að vera stilltar eins og lýst er í þessari grein.

> [!IMPORTANT]
> Eiginleikarnir sem eru nefndir í fyrstu áherslupunktunum í þessum lista þurfa útgáfu 10.0.19 af Supply Chain Management eða nýrri.

Aðeins er hægt að nota stíla á hnappinn **Í lagi** í svarglugga ef eftirfarandi kröfur eru uppfylltar:

- Hnappurinn er geymdur í skjámyndaflokki.
- Hópnafnið byrjar á `OkButtonGroup`.

Aðeins er hægt að nota stíla á hnappinn **Hætta við** í svarglugga ef eftirfarandi kröfur eru uppfylltar:

- Hnappurinn er geymdur í skjámyndaflokki.
- Hópnafnið byrjar á `CancelButtonGroup`.

### <a name="header"></a>Haus

Eftirfarandi mynd sýnir dæmigert eyðublað eða gluggahaus.

![Dæmigert form eða gluggahaus.](media/pfe-styles-header.png "Dæmigert form eða gluggahaus")

Í Visual Studio, hausar eru búnir til með því að nota uppbyggingu eins og þá sem er sýnd á eftirfarandi mynd.

![Dæmigerð kóðauppbygging til að búa til haus.](media/pfe-styles-header-code-structure.png "Dæmigerð kóðauppbygging til að búa til haus")

Til að bæta texta við hausinn þinn skaltu nota kóða eins og eftirfarandi dæmi.

```xpp
private void setCaption()
{
    HeaderFieldWithSeparatorText1.text("Report Progress");
    HeaderFieldWithSeparatorText2.text(ProdId);

    …

    HeaderFieldText.text(OprNum);
}
```

Þegar þú skrifar hauskóðann þinn skaltu nota eftirfarandi reglur:

- Nafn aðalhóps verður að vera `TableRowHeaderGroup`.
- Hver textablokk (aðskilin með byssukúlum) verður að byrja á `HeaderFieldWithSeparatorText`.
- Síðasta textanafnið verður að byrja á `HeaderFieldText`.
- `CaptionImage` hægt að sleppa.

### <a name="progress-indicator"></a>Framvinduvísir

Þú getur fylgt með framvinduvísi, sem sést hægra megin við hausinn. Eftirfarandi mynd sýnir framfaravísi.

![Dæmigerður framfaravísir.](media/pfe-styles-header-progress.png "Dæmigerður framfaravísir")

Til að sýna framvinduvísinn verður textareiturinn að vera nefndur `ShowProgress`.

## <a name="grid"></a>Hnitanet

Stílar eru sjálfkrafa notaðir. Engin sérstök stilling er nauðsynleg.

Ratið ætti að hafa a`TabularView` stíll, og`run()` aðferð á sérsniðnu eyðublaði verður að skrifa yfir, vegna þess að nýtt rist er ekki enn stutt. Bættu við eftirfarandi kóða.

```xpp
public void run()
{
    super();
    // To opt out a page from the new grid
    this.forceLegacyGrid();
}
```

Til að endurnýja gögn í aðalskjá gætirðu viljað nota eitthvað eins og`this.parmParentForm().updateLayout();` í`click` aðferð við aðgerð þína. (Til dæmis, skoðaðu`JmgProductionFloorExecutionReportFeedbackAction` bekk.) Gakktu úr skugga um það`parmDataSource` er sett í`init` aðferð við nýja eyðublaðið þitt (`formCaller.parmDataSource(this.dataSource(1));`). Til dæmis, skoðaðu`JmgProductionFloorExecutionMainGrid` formi.

## <a name="card-view"></a>Spjaldyfirlit

Aðeins er hægt að nota stíla á stýringar spjaldyfirlits ef eftirfarandi kröfur eru uppfylltar:

- Hvert spjaldyfirlit er geymt í skjámyndaflokki.
- Hópnafnið byrjar á`CardGroup` (til dæmis,`CardGroupJobsView`).

Eftirfarandi mynd sýnir spjaldyfirlit sem er með engar stýringar innan þess.

![Spjaldyfirlit án eininga.](media/pfe-styles-empty-card.png)

Eftirfarandi skýringarmyndir sýna spjaldyfirlit sem eru með stýringar innan þeirra.

![Spjald með einingum sem sýna Hz.](media/pfe-styles-elements.png)

![Spjald með einingum fyrir viðhaldsbeiðni.](media/pfe-styles-elements-maintenance.png)

## <a name="business-card"></a>Nafnspjald

Aðeins er hægt að nota stíla á stýringar nafnspjalds ef eftirfarandi kröfur eru uppfylltar:

- Hvert nafnspjald er geymt í skjámyndaflokki.
- Hópnafnið byrjar á`BusinessCardGroup` (til dæmis,`BusinessCardGroupJobsList`).

Stilltu eftirfarandi eiginleika á nafnspjaldinu:

- **Stíll:** *lista*
- **Útbreiddur stíll:** *kortalisti*
- **Fjölval:** *Nei*
- **Sýna Col merki:** *Nei*

![Nafnspjald.](media/pfe-styles-business-card.png)

## <a name="radio-button"></a>Hringhnappur

Aðeins er hægt að nota stíla á hringhnappa ef eftirfarandi kröfur eru uppfylltar:

- Hver hringhnappur er geymdur í skjámyndaflokki.
- Hópnafnið byrjar á`RadioTextBelow` eða`RadioTextRight`, eftir því hvar þú vilt að textinn birtist.

Stilltu eftirfarandi eiginleika á hringhnappnum:

- **Skiptahnappur:** *Athugaðu*
- **Skipta gildi:** *Á* ef valhnappur ætti að vera valinn; annars, *Af*

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

- **Hnappaskjár:** *TextWithImageLeft*
- **Venjuleg mynd:** Þessi eign má ekki vera auð. Notaðu t.d. *CoffeeScript*.
- **Texti:** Þessi eign má ekki vera auð. Notaðu t.d. *Hefja vinnuhlé*.
- **Breidd:** *Sjálfvirk* eða *SizeToContent*
- **Hæð:** *Sjálfvirk* eða *SizeToContent*

### <a name="primary-button"></a>Aðalhnappur

Aðeins er hægt að nota stíla á aðalhnappa ef eftirfarandi kröfur eru uppfylltar:

- Hnappurinn er geymdur í skjámyndaflokki.
- Hópnafnið byrjar á`DefaultButtonGroup` eða`PrimaryButtonGroup` (til dæmis,`DefaultButtonGroup10`).

![Aðalhnappur.](media/pfe-styles-first.png)

### <a name="secondary-button"></a>Aukahnappur

Aðeins er hægt að nota stíla á aukahnappa ef eftirfarandi kröfur eru uppfylltar:

- Hnappurinn er geymdur í skjámyndaflokki.
- Hópurinn er nefndur **Hægri spjaldið**, eða hópnafnið byrjar á `SecondaryButtonGroup`.

![Aukahnappur.](media/pfe-styles-second.png)

### <a name="third-group-button"></a>Hnappur þriðja hóps

Aðeins er hægt að nota stíla á hnappa þriðja hóps ef eftirfarandi kröfur eru uppfylltar:

- Hnappurinn er geymdur í skjámyndaflokki.
- Hópurinn er nefndur **Vinstri spjaldið**, eða hópnafnið byrjar á `ThirdButtonGroup`.

![Hnappur þriðja hóps.](media/pfe-styles-third.png)

### <a name="fourth-group-button"></a>Hnappur fjórða hóps

Aðeins er hægt að nota stíla á hnappa fjórða hóps ef eftirfarandi kröfur eru uppfylltar:

- Hnappurinn er geymdur í skjámyndaflokki.
- Hópnafnið byrjar á `FourthButtonGroup`.

Stilltu eftirfarandi eiginleika hnappsins:

- **Hnappaskjár:** *Aðeins texti*
- **Venjuleg mynd:** Þessi eign verður að vera auð.
- **Texti:** Þessi eign má ekki vera auð. Notaðu t.d. *Skoða* eða *Breyta*.
- **Breidd:** *Sjálfvirk*
- **Hæð:** *Sjálfvirk*

![Hnappur fjórða hóps.](media/pfe-styles-fourth.png)

### <a name="flat-button"></a>Sléttur hnappur

Aðeins er hægt að nota stíla á slétta hnappa ef eftirfarandi kröfur eru uppfylltar:

- Hnappurinn er geymdur í skjámyndaflokki.
- Hópnafnið byrjar á `FlatButtonGroup`.

Stilltu eftirfarandi eiginleika hnappsins:

- **Hnappaskjár:** *Aðeins mynd*
- **Venjuleg mynd:** Þessi eign má ekki vera auð. Notaðu t.d. *CoffeeScript*.
- **Texti:** Þessi eign verður að vera auð.
- **Breidd:** *Sjálfvirk* eða *SizeToContent*
- **Hæð:** *Sjálfvirk* eða *SizeToContent*

![Sléttur hnappur.](media/pfe-styles-flat-button.png)

### <a name="continue-button"></a>Halda áfram hnappur

Aðeins er hægt að nota stíla á hnappinn Halda áfram ef eftirfarandi kröfur eru uppfylltar:

- Hnappurinn er geymdur í skjámyndaflokki.
- Hópnafnið byrjar á `ContinueButtonGroup`.

Stilltu eftirfarandi eiginleika hnappsins:

- **Hnappaskjár:** *Aðeins mynd*
- **Venjuleg mynd:** *Áfram*
- **Texti:** Þessi eign verður að vera auð.
- **Breidd:** *Sjálfvirk* eða *SizeToContent*
- **Hæð:** *Sjálfvirk* eða *SizeToContent*

![Halda áfram hnappur.](media/pfe-styles-continue-button.png)

## <a name="combo-box"></a>Samtvinnaður listi

Samsettur gluggi er samsetning þriggja stýringa: innsláttarstýringar, hnapps sem hreinsar innsláttarstýringu og hnapps sem keyrir leit.

Aðeins er hægt að nota stíla á samsetta glugga ef eftirfarandi kröfur eru uppfylltar:

- Samsetti glugginn er geymdur í skjámyndaflokki.
- Hópnafnið byrjar á `Combobox`.
- Inni í hópnum er fyrsta stjórnin an`AxFormStringControl` stjórna. Þessi stýring sýnir núverandi gildi og það er þar sem notandinn slær inn nauðsynlegt gildi.
- Önnur stjórnin er a`CommonButton` stjórna, og nafn þess byrjar á `ClearButton`. Þessi hnappur verður að innihalda kóða sem notar`enable` eign til að sýna eða fela hnappinn. Til dæmis til að sýna eða fela hnappinn **Hreinsa** meðan notandinn er að slá inn upplýsingar í innsláttarstýringuna geturðu notað eftirfarandi kóða.

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

    Notaðu eftirfarandi kóða fyrir`clicked` aðferð við **Hreinsa** takki.

    ```xpp
    public void clicked()
    {
        element.setSerialId('');
        InventSerialId.setFocus(); // set focus back to the input box
    }
    ```

    Stilltu gildi inntaksstýringarinnar,`AxFormStringControl`, þegar eyðublaðið er frumstillt með því að nota`init` aðferð. Ef gildið er ekki autt skaltu virkja hnappinn **Hreinsa**. Ef gildið er autt skaltu gera hnappinn **Hreinsa** óvirkan.

- Þriðja stjórnin er a`CommonButton` stjórna, og nafn þess byrjar á `SearchButton`.

Eftirfarandi mynd sýnir tvær stýringar fyrir samsettan glugga. Samsetti glugginn vinstra megin er með auðan textareit og hnappurinn **Hreinsa** er óvirkur. Samsetti glugginn hægra megin er með texta í textareitnum og hnappurinn **Hreinsa** er virkur.

![Samsettir gluggar með og án hreinsunarhnapps.](media/pfe-styles-combo.png)

## <a name="quick-filter"></a>Hraðsía

Stýring flýtiafmörkun bætir leitarreiti við síðuna. Hægt er að nota stíla á flýtiafmörkun ef eftirfarandi kröfur eru uppfylltar:

- Flýtiafmörkunin er geymd í skjámyndaflokki.
- Hópnafnið byrjar á `SearchInputGroup`.
- Inni í hópnum er fyrsta stjórnin a`QuickFilter` stjórna. (Þessi stjórn er þar sem notandinn slær inn leitarstrenginn.)
- Önnur stjórnin er a`FormStaticTextControl` sem heitir `NumberOfResults`. (Þessi stjórn er valfrjáls. Ef það er innifalið sýnir það fjölda fundna hluta.)
- Þriðja stjórnin er a`CommonButton` stjórna, og nafn þess byrjar á `ClearButton`.

Eftirfarandi mynd sýnir tvær stýringar flýtiafmörkunar. Flýtiafmörkunin vinstra megin er með auða flýtiafmörkun og fjöldi niðurstaðna er ekki sýnileg. Flýtiafmörkunin til hægri inniheldur leitarstreng og sýnir fjölda niðurstaðna.

![Dæmi um stýringu flýtiafmörkunar með og án leitarstrengs.](media/pfe-styles-quick-filter.png "Dæmi um stýringu flýtiafmörkunar með og án leitarstrengs")

## <a name="center-align-elements-on-a-tab"></a>Miðjaðu þætti á flipa

Til að samræma þætti í miðju flipa verður hópnafnið að byrja á`TabContentGroup`, og hópurinn verður að hafa eftirfarandi eiginleika:

- **Breiddarstilling:**`SizeToAvailable`
- **Hæðarstilling:**`SizeToAvailable`

## <a name="align-a-grid-detail-part-and-quick-filter"></a>Samræmdu rist, smáatriði og hraðsíu

Til að raða sérsniðnu ristli, smáatriðum og hraðsíu þannig að þau líkist stöðluðu hönnuninni skaltu hafa eftirfarandi atriði í huga þegar þú setur þá alla saman:

- Ef ristið er með hraðsíu ættu bæði ristið og hraðsían að vera inni í hópnum sem hefur nafn sem byrjar á `GridGroup`.
- Til að beita stílum á smáatriði verður hópnafnið að byrja á`DetailInformationGroup`,

Eftirfarandi mynd sýnir dæmigert rist sem inniheldur hraðsíu og smáatriði til hægri.

![Dæmigert rist sem inniheldur fljótlega síu og smáatriði.](media/pfe-styles-align-grid.png "Dæmigert rist sem inniheldur fljótlega síu og smáatriði")

Í Visual Studio Hægt er að búa til rist, smáatriði og hraðsíu með því að nota uppbyggingu eins og þá sem sýnd er á eftirfarandi mynd.

![Dæmigert kóðauppbygging sem stillir saman rist, smáatriði og hraðsíu.](media/pfe-styles-header-code-structure2.png "Dæmigert kóðauppbygging sem stillir saman rist, smáatriði og hraðsíu")

## <a name="additional-resources"></a>Frekari upplýsingar

- [Sérsníða viðmót fyrir framkvæmd á framleiðslugólfi](production-floor-execution-customize.md)
- [Hanna viðmótið fyrir framkvæmd á framleiðslugólfi](production-floor-execution-tabs.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
