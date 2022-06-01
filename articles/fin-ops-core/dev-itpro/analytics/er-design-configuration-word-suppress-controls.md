---
title: Fela Word-efnisstýringar í mynduðum skýrslum
description: Í þessu efni er útskýrt hvernig á að skilgreina snið rafrænnar skýrslugerðar til að mynda skýrslur sem Microsoft Word-skrár þar sem efnisstýringar eru faldar.
author: NickSelin
ms.date: 02/11/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner,  LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-01-01
ms.dyn365.ops.version: Version 10.0.6
ms.openlocfilehash: 2c2d79c9ea36c42cfc0f6ba0d3c81d063d8d9446
ms.sourcegitcommit: 6c1bf233748c4bc70fc5a1a9711758cdfd9e07dc
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/19/2022
ms.locfileid: "8782177"
---
# <a name="suppress-word-content-controls-in-generated-reports"></a>Fela Word-efnisstýringar í mynduðum skýrslum

[!include [banner](../includes/banner.md)]

Til að búa til skýrslur sem Microsoft Word-skjöl þarf að hanna sniðmát fyrir skýrslurnar sem Word-skjal. Þetta sniðmát verður að innihalda Word-efnisstýringar sem staðgengla fyrir gögn sem verður fyllt út í við keyrslu. Til að nota Word-skjalið sem sniðmát sem er búið til sem sniðmát fyrir skýrslurnar er hægt að [skilgreina](er-design-configuration-word.md) nýja [rafræna skýrslugerðar](general-electronic-reporting.md) [lausn](er-quick-start1-new-solution.md). Lausnin verður að innihalda bráðamóttöku [stillingar](general-electronic-reporting.md#Configuration) sem inniheldur ER-sniðshluta. Þetta snið rafrænnar skýrslugerðar verður að vera skilgreint til að nota hannaða sniðmátið fyrir myndun skýrslu.

Í útgáfu 10.0.6 og síðar af Dynamics 365 Finance geturðu stillt formúlur á ER-sniði þínu til að bæla niður sumar innihaldsstýringar Word í mynduðum skjölum.

Eftirfarandi skref útskýra hvernig notandi sem er úthlutað hlutverki kerfisstjóra eða hagnýts ráðgjafa rafrænnar skýrslugerðar getur skilgreint snið rafrænnar skýrslugerðar sem myndar skýrslur sem Word-skrár og felur sumar efnisstýringarnar í mynduðum skýrslum sem hafa verið skilgreindar með því að nota Word-sniðmát.

Hægt er að ljúka þessum skrefum í GBSI-fyrirtækinu.

## <a name="prerequisites"></a>Forkröfur

Til að ljúka þessum skrefum þarf fyrst að ljúka skrefunum í eftirfarandi verkleiðbeiningum:

- [Hanna skilgreiningu til að mynda skýrslur á OPENXML-sniði](./tasks/er-design-reports-openxml-2016-11.md)
- [Endurnýta stillingar rafrænnar skýrslugerðar með Excel-sniðmátum til að búa til skýrslur á Word-sniði](./tasks/er-design-configuration-word-2016-11.md)

Þegar skrefum þessara verkleiðbeininga er lokið eru eftirfarandi atriði undirbúin:

- Rafrænt skýrslugerðarsnið fyrir **Dæmi um vinnublaðsskýrslu** sem er skilgreint til að búa til skjal á Word-sniði
- Útgáfa [draga](general-electronic-reporting.md#component-versioning) fyrir rafrænt skýrslugerðarsnið fyrir **Dæmi um vinnublaðsskýrslu** sem er merkt sem **Keyranlegt**
- **Rafræn** greiðslumáti sem er skilgreindur til að nota **Dæmi um vinnublaðsskýrslu** rafræns skýrslugerðarsniðs fyrir afgreiðslu lánardrottnagreiðslu

Einnig þarf að hlaða niður og vista eftirfarandi sniðmát fyrir sýnishorn skýrslu:

- [Afmarkað sniðmát 2 af greiðsluskýrslu (SampleVendPaymDocReportBounded2.docx)](https://download.microsoft.com/download/1/9/b/19b36e39-861a-414e-9150-9880d9d2487c/SampleVendPaymDocReportBounded2.docx)

## <a name="review-the-downloaded-word-template"></a><a id="tag-control"></a>Fara yfir sótt Word-sniðmát

1. Í Word-skjáborðsforritinu skal opna sniðmátsskrána **SampleVendPaymDocReportBounded2.docx** sem var sótt hér áður.
2. Gangið úr skugga um að sniðmátsskráin innihaldi yfirlitshluta sem sýnir samtals greiðsluupphæðir fyrir hvern gjaldmiðilskóða sem hefur verið uppfylltur í afgreiddum greiðslum.

    - Samantektarhlutann er að finna í aðskildri töflu Word-skjalsins.
    - Fyrsta lína töflunnar inniheldur fyrirsagnir töfludálka sem haus hlutans.
    - Önnur lína töflunnar inniheldur endurtekna efnisstýringu sem upplýsingar um hluta.
    - Þessari efnisstýringu er varpað í reitinn **SummaryLines** í sérsniðna XML-hlutanum **Skýrsla**.
    - Á grundvelli þessarar vörpunar tengist efnisstýringin einingunni **SummaryLines** í breytanlegu sniði rafrænnar skýrslugerðar.

    > [!NOTE]
    > Endurtekna efnisstýringin er merkt af lyklinum **SummaryLines** sem passar við reit sérsniðna XML-hlutans sem hefur verið varpað í.

    ![Útlit Word-sniðmáts.](./media/er-design-configuration-word-suppress-controls-image1.gif)

## <a name="select-the-existing-er-report-configuration"></a>Velja fyrirliggjandi grunnstilling skýrsla í Rafræn skýrslugerð

Fyrir eftirfarandi skref verður fyrirliggjandi skilgreining rafrænnar skýrslugerðar notuð aftur sem var skilgreind þegar lokið var við skrefin í áðurnefndum verkleiðbeiningum.

1. Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.
2. Veldu **Skilgreiningar skýrslugerðar**.
3. Á síðunni **Skilgreiningar**, í skilgreiningatrénu, skal stækka **Greiðslulíkan** og velja **Dæmi um vinnublaðsskýrslu**.
4. Veljið **Hönnuður** til að breyta útgáfudrögum valins sniðs rafrænnar skýrslugerðar.

## <a name="replace-the-current-template-with-the-new-template"></a>Skipta út núgildandi sniðmáti fyrir nýja sniðmátið

Núna er skráin SampleVendPaymDocReportBounded.docx notuð sem sniðmát til að búa til úttakið á Word-sniði. Í eftirfarandi skrefum verður þessu Word-sniðmáti skipt út fyrir nýja Word-sniðmátið, SampleVendPaymDocReportBounded2.docx, sem var sótt hér áður.

1. Á síðunni **Sniðshönnuður** skal velja **Viðhengi**.
2. Á síðunni **Viðhengi** skal velja **Eyða** til að fjarlægja fyrirliggjandi sniðmát.
3. Veljið **Já** til að staðfesta eyðinguna.
4. Veljið **Ný** \> **Skrá**.
5. Veljið **Fletta** og flettið síðan og veljið skrána **SampleVendPaymDocReportBounded2.docx** sem var sótt áður.
6. Veljið **Í lagi**.
7. Lokaðu síðunni **Viðhengi**.
8. Á síðunni **Sniðshönnuður**, í reitinn **Sniðmát**, skal færa inn eða velja skrána **SampleVendPaymDocReportBounded2.docx**.

## <a name="run-the-format-to-create-word-output"></a>Keyra sniðið til að búa til Word-úttak

1. Farðu í **Viðskiptaskuldir** \> **Greiðslur** \> **Greiðslubók**.
2. Á síðunni **Greiðslur lánardrottna**, í flipanum **Listi**, skal velja allar greiðslurnar.
3. Veljið **Greiðslustaða** \> **Engin**.
4. Veldu **Búa til greiðslur**.
5. Í reitnum **Greiðslumáti** skal velja **Rafrænn**.
6. Í reitnum **Bankareikningur** skal velja **GBSI OPER**.
7. Veljið **Í lagi**.
8. Í svargluggann **Rafrænar skýrslufæribreytur** skal velja **Í lagi** og greina myndað úttak.

    ![Greiðslur til úrvinnslu á greiðslusíðu lánardrottins.](./media/er-design-configuration-word-suppress-controls-image2.gif)

    Úttakið er sýnt á Word-sniði og inniheldur samantektarhlutann.

## <a name="configure-the-editable-format-to-suppress-the-summary-section"></a><a id="configure-to-suppress-control"></a>Skilgreina breytanlegt snið til að fela samantektarhlutann

Ef ætlunin er að fela samantektarhlutann í mynduðu skjali, samkvæmt beiðni notanda sem keyrir þetta rafræna skýrslugerðarsnið, þarf að lagfæra breytanlegt snið rafrænnar skýrslugerðar.

1. Farið í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð** og opnið útgáfudrög rafræns skýrslugerðarsniðs til að gera breytingar.
2. Veldu **Skilgreiningar skýrslugerðar**. 
3. Á síðunni **Skilgreiningar**, í skilgreiningatrénu, skal stækka **Greiðslulíkan** \> **Dæmi um vinnublaðsskýrslu**.
4. Veljið **Hönnuður**.
5. Á síðunni **Sniðshönnuður** skal stækka **Word** og velja **SummaryLines**.
6. Í flipanum **Vörpun** skal bæta við nýjum gagngjafa til að spyrja notendur á keyrslutíma hvort fela eigi samantektarhlutann:

    1. Veljið **Bæta við rót**.
    2. Í svarglugganum **Bæta við gagnagjafa** skal velja **Færibreyta slegin inn almennt\af notanda** til að opna svargluggann **Eiginleikar gagnagjafa „Innsláttarfæribreyta notanda“**.
    3. Í reitinn **Heiti** skal færa inn **uipSuppress**.
    4. Í reitinn **Merki** skal færa inn **Fela samantektarhluta**.
    5. Í reitnum **Heiti gagnaaðgerðar**, velja eða slá inn **NoYes**.
    6. Veljið **Í lagi**.

7. Bætið við nýjum gagnagjafa af **NoYes** upptalningargerðinni:

    1. Veljið **Bæta við rót**.
    2. Í svarglugganum **Bæta við gagnagjafa** skal velja **Dynamics 365 for Operations\Enumeration** til að opna svargluggann **Eiginleikar gagnagjafa „upptalningar“**.
    3. Í reitinn **Heiti** skal færa inn **enumNoYes**.
    4. Í reitinn **Merki** skal færa inn **Fela valkosti**.
    5. Í reitnum **Heiti gagnaaðgerðar**, velja eða slá inn **NoYes**.
    6. Veljið **Í lagi**.

8. Fyrir völdu sniðseininguna **SummaryLines** skal skilgreina formúluna til að tilgreina hvenær eigi að fela Word-efnisstýringuna sem tengist valdri sniðseiningu:

    1. Í flipanum **Vörpun**, í hlutanum **Fjarlægt**, skal velja **Breyta** til að opna síðuna **[Formúluhönnuður](general-electronic-reporting-formula-designer.md)**.
    2. Í reitnum **Formúla** skal færa inn formúluna `uipSuppress = enumNoYes.Yes`.
    3. Veljið **Vista** og lokið síðunni **Formúluhönnuður**.

        > [!NOTE]
        > Þessari formúlu verður beitt á myndað skjal **þegar búið er að keyra allar aðrar sniðseiningar**. Til að nota þessa formúlu finnst Word-efnisstýring sem er merkt sem sniðseining sem formúlan er skilgreind fyrir (**SummaryLines** í þessu tilfelli) í mynduðu skjali. Þessi efnisstýring er síðan fjarlægð að fullu ásamt línunni í Word-töflunni sem geymir hana. Upplýsingalína samantektarhlutans er fjarlægð úr mynduðu skjali.
        >
        > Á hönnunartíma mætti skilgreina formúluna **Fjarlægt** fyrir sniðseiningu, jafnvel þótt engin efnisstýring í Word-sniðmátinu sem verið er að nota sé með merki sem passar við heiti sniðseiningarinnar sem eiginleikinn **Fjarlægt** er skilgreindur fyrir. Þegar sniðið er villuleitað á hönnunartíma kemur upp [viðvörun](er-components-inspections.md#i14) um þetta ósamræmi.
        >
        > Við keyrslu er undantekning notuð ef engin efnisstýring í Word-sniðmátinu sem verið er að nota er með merki sem passar við heiti sniðseiningarinnar sem eiginleikinn **Fjarlægt** er skilgreindur fyrir.

    4. Í flipanum **Vörpun**, í hlutanum **Fjarlægt**, skal stilla valkostinn **Með yfireiningu** á **Já**.

        > [!NOTE]
        > Stilla þarf þennan valkost á **Já** til að fjarlægja alla Word-töfluna sem hluti yfireiningar línunnar sem geymir upplýsingar um samantektarhlutann. Ef þessi valkostur er stilltur á **Nei** verður hauslína hlutans áfram í myndaða skjalinu.

9. Smellið á **Vista** til að vista breytingarnar á breytanlega sniðinu.

    ![Myndað úttak á Word-sniði.](./media/er-design-configuration-word-suppress-controls-image3.gif)

## <a name="run-the-modified-format-to-create-word-output"></a>Keyra breytta sniðið til að búa til Word-úttak

1. Farðu í **Viðskiptaskuldir** \> **Greiðslur** \> **Greiðslubók**.
2. Veljið greiðslubókina sem var búin til og veljið síðan **Línur**.
3. Á síðunni **Greiðslur lánardrottna** skal velja allar línurnar og síðan velja **Greiðslustaða** \> **Engin**.
4. Veldu **Búa til greiðslur**.
5. Í reitnum **Greiðslumáti** skal velja **Rafrænn**.
6. Í reitnum **Bankareikningur** skal velja **GBSI OPER**.
7. Veljið **Í lagi**.
8. Í svarglugganum **Rafrænar skýrslufæribreytur**, í reitnum **Fela samantektarhluta**, skal velja **Já**.
9. Veljið **Í lagi** og skoðið myndað úttak.

    ![Myndað úttak á Word-sniði.](./media/er-design-configuration-word-suppress-controls-image4.gif)

    Takið eftir að úttakið inniheldur ekki samantektarhlutann vegna þess að hann hefur verið falinn.

## <a name="additional-resources"></a>Frekari upplýsingar

- [Hanna skilgreiningu til að mynda skýrslur á OPENXML-sniði](./tasks/er-design-reports-openxml-2016-11.md)
- [Hanna nýja skilgreiningu rafrænnar skýrslugerðar til að búa til skýrslur á Word-sniði](er-design-configuration-word.md)
- [Endurnýta stillingar rafrænnar skýrslugerðar með Excel-sniðmátum til að búa til skýrslur á Word-sniði](./tasks/er-design-configuration-word-2016-11.md)
- [Skoða grunnstilltan hlut rafrænnar skýrslugerðar til að koma í veg fyrir vandamál varðandi keyrslu](er-components-inspections.md#i14)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
