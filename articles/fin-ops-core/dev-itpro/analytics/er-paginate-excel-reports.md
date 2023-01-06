---
title: Hanna snið rafrænnar skýrslugerðar til að skipta skjölum mynduðum í Excel á síður
description: Þessi grein útskýrir hvernig á að hanna snið rafrænnar skýrslugerðar sem skiptir mynduðum skjölum í Microsoft Excel á síður.
author: kfend
ms.date: 09/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2021-08-01
ms.dyn365.ops.version: Version 10.0.22
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.form: EROperationDesigner
ms.openlocfilehash: e4a34dffda9e9b95f5d6c7ee382723663817ec6b
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285002"
---
# <a name="design-an-er-format-to-paginate-generated-documents-in-excel"></a>Hanna snið rafrænnar skýrslugerðar til að skipta skjölum mynduðum í Excel á síður

[!include [banner](../includes/banner.md)]

Í þessari grein er útskýrt hvernig notandi í hlutverki kerfisstjóra eða í hagnýtu ráðgjafahlutverki rafrænnar skýrslugerðar getur stillt snið [Rafrænnar skýrslugerðar](general-electronic-reporting.md) tila ð mynda skjöl á útleið í Microsoft Excel og stjórna síðuskiptingu skjals.

Í þessu dæmi breytir þú rafrænu skýrslugerðarsniði frá Microsoft sem er notað til að prenta eftirlitsskýrsluna þegar Intrastat-skattskýrslan er [mynduð](../../../finance/localizations/tasks/eur-00002-eu-intrastat-declaration.md). Þessi skýrsla gerir þér kleift að fylgjast með tilkynntum Intrastat-færslum. Breytingarnar þínar gera þér kleift að stjórna síðuskiptingu á eftirlitsskýrslum sem eru búnar til.

Hægt er að ljúka ferlunum í þessari grein í fyrirtækinu **USMF**. Ekki er þörf á neinni kóðun. Áður en hafist er handa skal sækja og vista eftirfarandi skrár.

| lýsing       | Skrárnafn |
|-------------------|-----------| 
| Skýrslusniðmát 1 | [ERIntrastatReportDemo1.xlsx](https://download.microsoft.com/download/7/2/a/72ae292a-8bb2-4b9d-8397-9764218f6fa8/ERIntrastatReportDemo1%20.xlsx) |
| Skýrslusniðmát 2 | [ERIntrastatReportDemo2.xlsx](https://download.microsoft.com/download/7/d/1/7d15858d-6260-4afa-9dda-d8b955e59b1a/ERIntrastatReportDemo2.xlsx) |

## <a name="configure-the-er-framework"></a>Skilgreina ramma rafrænnar skýrslugerðar

Fylgdu skrefunum í [Skilgreina ramma rafrænnar skýrslugerðar](er-quick-start2-customize-report.md#ConfigureFramework) til að setja upp lágmarksfjölda af færibreytum rafrænnar skýrslugerðar. Þú verður að ljúka þessari uppsetningu áður en þú byrjar að nota ramma rafrænnar skýrslugerðar til að hanna sérsniðna útgáfu af stöðluðu sniði rafrænnar skýrslugerðar.

## <a name="import-the-standard-er-format-configuration"></a>Flytja inn staðlaða skilgreiningu rafræns skýrslugerðarsniðs

Fylgdu skrefunum í [Flytja inn staðlaða skilgreiningu rafræns skýrslugerðarsniðs](er-quick-start2-customize-report.md#ImportERSolution1) til að bæta stöðluðum skilgreiningum rafrænnar skýrslugerðar við núverandi tilvik af Dynamics 365 Finance. Flyttu inn útgáfu **1.9** af sniðsskilgreiningu **Intrastat-skýrslu**. Grunnútgáfa 1 af grunnstillingu **Intrastat-líkans** er sjálfkrafa flutt inn úr gagnageymslunni.

## <a name="customize-the-standard-er-format"></a>Sérsníða staðlað snið rafrænnar skýrslugerðar

### <a name="create-the-custom-er-format"></a>Búa til sérstillt snið rafrænnar skýrslugerðar

Í þessum aðstæðum ert þú fulltrúi Litware, Inc sem hefur verið valið sem virkur þjónustuaðili rafrænnar skýrslugerðarskilgreiningar. Þú verður að búa til nýja skilgreiningu rafræns skýrslugerðarsniðs með því að nota skilgreiningu **Intrastat-skýrslu** sem grunn.

1. Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.
2. Á síðunni **Skilgreiningar**, í skilgreiningatrénu á svæðinu til vinstri, skal stækka **Intrastat-líkan** og velja **Intrastat-skýrsla**. Litware, Inc. notar útgáfu 1.9 af þessari skilgreiningu rafrænnar skýrslugerðar sem grunn fyrir sérsniðnu útgáfuna.
3. Veljið **Stofna skilgreiningu** til að opna fellilistagluggann. Hægt er að nota þennan glugga til að stofna nýja skilgreiningu fyrir sérstillt greiðslusnið.
4. Í reitahópnum **Nýtt** skal velja **Afleiða af heiti: Intrastat-skýrsla, Microsoft**.
5. Í reitnum **Heiti** skal færa inn **Intrastat-skýrsla Litware**.
6. Veljið **Stofna skilgreiningu** til að stofna nýtt snið.

Útgáfa 1.9.1 af skilgreiningu rafræns skýrslugerðarsniðs fyrir **Intrastat-skýrslu Litware** er stofnuð. Þessi útgáfa er með stöðuna **Drög** og er hægt að breyta. Núverandi efni af sérstilltu sniði rafrænnar skýrslugerðar samsvarar efni sniðsins sem Microsoft býður upp á.

### <a name="make-the-custom-format-runnable"></a>Gera sérstillta sniðið keyranlegt

Nú þegar fyrsta útgáfa af sérstilltu sniði hefur verið stofnuð og er með stöðuna **Drög**, er hægt að prufukeyra hana. Til að keyra skýrsluna skal vinna úr greiðslu lánardrottins með því að nota greiðslumátann sem vísar til sérstillts sniðs rafrænnar skýrslugerðar. Sjálfgefið er að þegar kallað er á snið rafrænnar skýrslugerðar úr forritinu, eru aðeins útgáfur sem eru með stöðuna **Lokið** eða **Samnýtt** teknar til greina. Þessi leið hjálpar til við að koma í veg fyrir að snið rafrænnar skýrslugerðar með ókláraðri hönnun verði notuð. Fyrir prufukeyrslur er hinsvegar hægt að þvinga forritið til að nota sniðsútgáfu rafrænnar skýrslugerðar sem er með stöðuna **Drög**. Á þennan hátt er hægt að leiðrétta núverandi sniðsútgáfu ef gera þarf einhverjar breytingar. Frekari upplýsingar er að finna í [Nothæfni](electronic-reporting-destinations.md#applicability).

Til að nota útgáfudrög af sniði rafrænnar skýrslugerðar þarf sérstaklega að merkja rafræna skýrslugerðarsniðið.

1. Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.
2. Á síðunni **Skilgreiningar**, í aðgerðarúðunni, í flipanum **Skilgreiningar**, í flokknum **Ítarlegar stillingar**, skal velja **Færibreytur notanda**.
3. Í glugganum **Færibreytur notanda** skal stilla valkostinn **Keyra stillingar** á **Já** og síðan velja **Í lagi**.
4. Veljið **Breyta** til að gera núverandi síðu breytanlega ef þörf krefur.
5. Í skilgreiningartrénu á svæðinu til vinstri skal velja **Intrastat-skýrsla Litware**.
6. Stillið valkostinn **Keyra drög** á **Já** og veljið svo **Vista**.

    ![Keyra valkostinn fyrir drög á skilgreiningarsíðunni.](./media/er-paginate-excel-reports-derived-format-configuration.png)

## <a name="set-up-foreign-trade-parameters-to-use-the-custom-er-format"></a>Setja upp færibreytur erlendra viðskipta til að nota sérstillt snið rafrænnar skýrslugerðar

Fylgdu þessum skrefum til að stilla færibreytur erlendra viðskipta þannig að þú getir notað sérstillta sniðið.

1. Fara í **Skattur** \> **Uppsetningu** \> **Erlend viðskipta** \> **færibreytur erlendra viðskipta**.
2. Á síðunni **Færibreytur erlendra viðskipta**, í flýtiflipanum **Rafræn skýrslugerð**, í reitnum **Vörpun skráarsniðs**, skal velja **Intrastat-skýrsla Litware**.
3. Í reitnum **Vörpun skýrslusniðs** skal velja **Intrastat-skýrslu Litware**.
4. Veldu **Vista**.

## <a name="configure-the-custom-format-to-use-the-downloaded-report-template"></a>Skilgreina sérstillt snið til að nota sótt skýrslusniðmát

### <a name="review-the-first-downloaded-excel-template"></a>Fara yfir fyrsta sótta Excel-sniðmátið

1. Í skjáborðsforriti Excel skal opna sniðmátsskrána **ERIntrastatReportDemo1.xlsx** sem var sótt hér áður.
2. Gakktu úr skugga um að sniðmátið innihaldi nefnd svið til að búa til skýrsluhaus, upplýsingar um skýrslu og síðufætur skýrslu í mynduðum skjölum.

    ![Útlit Excel sniðmáts 1 í skjáborðsforritinu.](./media/er-paginate-excel-reports-template1.gif)

### <a name="replace-the-current-excel-template-in-the-custom-er-format"></a><a id="replace-template"></a>Skipta út núverandi Excel-sniðmáti á sérstilltu sniði rafrænnar skýrslugerðar

Þú verður að bæta nýju Excel-sniðmáti við sérstillt snið rafrænnar skýrslugerðar.

1. Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.
2. Á síðunni **Skilgreiningar**, í skilgreiningartrénu á svæðinu til vinstri, skal stækka **Intrastat-líkan** \> **Intrastat-skýrsla** og velja skilgreininguna **Intrastat-skýrsla Litware**.
3. Veljið **Hönnuður**.
4. Á síðunni **Sniðshönnuður**, í aðgerðarúðunni, skal velja **Sýna upplýsingar**.
5. Gakktu úr skugga um að rótarsniðsþátturinn **Intrastat: Excel** sé valinn og síðan á aðgerðasvæðinu, í flipanum **Flytja inn**, í flokknum **Flytja inn**, skal velja **Uppfæra úr Excel**.
6. Í svarglugganum **Uppfæra úr Excel** skal velja **Uppfæra sniðmát**.
7. Í svarglugganum **Opna** skal hafa upp á og velja skrána **ERIntrastatReportDemo1.xlsx** sem var sótt hér áður og síðan velja **Opna**.
8. Veldu **Í lagi**.
9. Veldu **Vista**.

![Sniðsskipulag í hönnuði rafræns skýrslugerðarsniðs eftir að nýja Excel-sniðmátinu er bætt við.](./media/er-paginate-excel-reports-format1.png)

## <a name="change-the-data-binding-to-show-the-item-description-on-a-generated-report"></a>Breyta gagnabindingu til að sýna vörulýsingu í myndaðri skýrslu

1. Á síðunni **Sniðshönnuður** skal velja flipann **Vörpun**.
2. Stækkaðu **Intrastat** \> **Skýrslulínur** og veldu hlutann **Vörukóði**.
3. Veljið **Breyta formúlu**.
4. Breyttu bindingarformúlu úr `@.CommodityCode` í `CONCATENATE(@.CommodityCode, " ", @.ProductName)`.
5. Veldu **Vista**.

![Skilgreindu bindingu til að sýna vörulýsingu í hönnuði rafræns skýrslugerðarsniðs.](./media/er-paginate-excel-reports-format1a.png)

## <a name="generate-an-intrastat-declaration-control-report"></a><a id="generate-intrastat-control-report"></a>Búa til eftirlitsskýrslu Intrastat-skattskýrslu

Gakktu fyrst úr skugga um að þú sért með Intrastat-færslur til að tilkynna á síðunni **Intrastat**.

![Færslur á Intrastat-síðunni.](./media/er-paginate-excel-reports-transactions1.gif)

Notaðu síðan sérstillt snið rafrænnar skýrslugerðar til að búa til eftirlitsskýrslu Intrastat-skattskýrslu.

1. Farðu í **Skattur** \> **Skattskýrslur** \> **Erlend viðskipti** \> **Intrastat**.
2. Á síðunni **Intrastat** á aðgerðasvæðinu skal velja **Úttak** \> **Skýrsla**.
3. Í svarglugganum **Intrastat-skýrsla** skal fylgja þessum skrefum til að keyra skýrsluna:

    1. Stilltu reitina **Frá dagsetningu** og **Til dagsetningar** til að hafa með tilteknar Intrastat-færslur í skýrslunni.
    2. Stilltu valkostinn **Búa til skrá** á **Nei**.
    3. Stilltu valkostinn **Mynda skýrslu** á **Já**.
    4. Veldu **Í lagi**.

4. Sæktu og vistaðu skjalið sem er búið til.
5. Opnaðu skjalið í Excel og farðu yfir það.

    ![Excel-skjal búið til í skjáborðsforriti.](./media/er-paginate-excel-reports-document1.png)

## <a name="configure-the-custom-format-to-paginate-generated-documents"></a>Skilgreina sérstillt snið til að skipta mynduðum skjölum á síður

### <a name="review-the-second-downloaded-excel-template"></a>Yfirfara næsta sótta Excel-sniðmát

1. Í Excel skal opna sniðmátsskrána **ERIntrastatReportDemo2.xlsx** sem þú sóttir hér áður.
2. Berðu þetta sniðmát saman við sniðmátið **ERIntrastatReportDemo1.xlsx** og staðfestu að það innihaldi nokkur ný Excel-heiti til að búa til og fylla í hluta sem tilheyra síðum í mynduðum skjölum:

    - Sviðið **ReportPageHeader** er bætt við til að búa til síðuhausa.
    - Sviðinu **ReportPageFooter** er bætt við til að búa til síðufætur.
    - Hólfið **ReportPageFooter\_PageLines** er stillt til að sýna færslufjölda hverrar síðu.
    - Hólfið **ReportPageFooter\_PageAmount** er stillt til að sýna heildarupphæð færslna á hverri síðu.
    - Hólfið **ReportPageFooter\_PageWeight** er stillt til að sýna heildarþyngd færslna á hverri síðu.
    - Hólfið **ReportPageFooter\_RunningCounterLines** er stillt til að sýna hlaupandi talningu á færslum frá upphafi skýrslu og í gegnum núverandi síðu.
    - Hólfið **ReportPageFooter\_RunningTotalAmount** er stillt til að sýna hlaupandi talningu upphæðar fyrir allar færslur frá upphafi skýrslu og í gegnum núverandi síðu.
    - Hólfið **ReportPageFooter\_RunningTotalWeight** er stillt til að sýna hlaupandi talningu þyngdar fyrir færslur frá upphafi skýrslu og í gegnum núverandi síðu.

    ![Útlit Excel sniðmáts 2 í skjáborðsforritinu.](./media/er-paginate-excel-reports-template2a.gif)

    Hólfið **CommodityCode** í þessu sniðmáti er stillt til að þjappa texta í hólfi. Þar sem lína færsluupplýsinga er stillt þannig að hún passi sjálfkrafa við hæð línunnar, verður hæð allrar línunnar að breytast sjálfkrafa þegar textanum í hólfinu **CommodityCode** er þjappað.

    ![Hólf CommodityCode stillt til að þjappa texta í hólfi.](./media/er-paginate-excel-reports-template2b.gif)

### <a name="repeat-the-replacement-of-the-current-excel-template-in-the-custom-er-format"></a>Endurtaktu skiptingu á núverandi Excel-sniðmáti í sérstilltu sniði rafrænnar skýrslugerðar

1. Fylgdu skrefunum í hlutanum [Skipta út núverandi Excel-sniðmáti í sérstilltu sniði rafrænnar skýrslugerðar](#replace-template) í þessari grein. Í skrefi 7 skal hinsvegar velja skrána **ERIntrastatReportDemo2.xlsx**.
2. Á síðunni **Sniðshönnuður** skal stækka **Intrastat**.
3. Gefðu upp sniðsþátt [Sviðs](er-fillable-excel.md#range-component) sem hefur verið bætt við breytanlegt snið rafrænnar skýrslugerðar til að samstilla skipulagið við skipulag Excel-sniðmátsins sem er notað:

    1. Veldu **Sviðsþáttinn** sem tengist Excel-heitinu **ReportPageHeader**.
    2. Í flipanum **Snið**, í reitnum **Heiti**, skal færa inn **Síðuhaus skýrslu**.
    3. Veldu **Sviðsþáttinn** sem tengist Excel-heitinu **ReportPageFooter**.
    4. Í flipanum **Snið**, í reitnum **Heiti**, skal færa inn **Síðufótur skýrslu**.

4. Veldu **Vista**.

![Sniðsskipulag í hönnuði rafræns skýrslugerðarsniðs eftir að Excel-sniðmátinu er skipt út.](./media/er-paginate-excel-reports-format2.png)

### <a name="change-the-format-structure-to-implement-document-pagination"></a>Breyta sniðskipulagi til að innleiða síðuskiptingu skjals

1. Á síðunni **Sniðshönnuður**, í sniðstrénu vinstra megin, skal velja rótarþáttinn **Intrastat**.
2. Veljið **Bæta við**.
3. Í svarglugganum **Bæta við** skal velja þáttinn [Síða](er-fillable-excel.md#page-component) í flokknum **Excel** yfir þætti.
4. Í svarglugganum **Eiginleikar hlutar**, í reitinn **Heiti**, skal færa inn **Skýrslusíðu**. Veljið síðan **Í lagi**.
5. Til að nota þáttinn **Síðuhaus skýrslu** sem síðuhaus á öllum mynduðum síðum skal fylgja þessum skrefum:

    1. Veldu þáttinn **Síðuhaus skýrslu** og veldu svo **Klippa**.
    2. Veldu þáttinn **Skýrslusíða** og veldu svo **Líma**.
    3. Stækkaðu **Skýrslusíðu**.
    4. Til að þvinga **Síðuþáttinn** til að [taka líta á](er-fillable-excel.md#page-component-structure) þetta svið sem síðuhaus skal velja **Síðuhaus skýrslu** og síðan í flipanum **Snið** í reitnum **Eftirlíkingarátt** skal velja **Engin eftirlíking**.

6. Til að skipta mynduðu skjali á síður þannig að efnið í skýrslulínum sé tekið tilgreina skal fylgja þessum skrefum:

    1. Veldu þáttinn **Skýrslulínur** og veldu svo **Klippa**.
    2. Veldu þáttinn **Skýrslusíða** og veldu svo **Líma**.

7. Til að hafa með síðufót skýrslu eftir skýrslulínur en á undan síðasta síðufæti skal fylgja þessum skrefum:

    1. Smelltu á þáttinn **Síðufótur skýrslu** og veldu svo **Klippa**.
    2. Veldu þáttinn **Skýrslusíða** og veldu svo **Líma**.

8. Til að nota þáttinn **Síðufótur skýrslu** sem síðufót á öllum mynduðum síðum skal fylgja þessum skrefum:

    1. Veldu þáttinn **Síðufótur skýrslu** og veldu svo **Klippa**.
    2. Veldu þáttinn **Skýrslusíða** og veldu svo **Líma**.
    3. Til að þvinga **Síðuþáttinn** til að [líta á](er-fillable-excel.md#page-component-structure) þetta svið sem síðufót skal velja **Síðufótur skýrslu** og síðan í flipanum **Snið** í reitnum **Eftirlíkingarátt** skal velja **Engin eftirlíking**.

![Sniðsskipulag í hönnuði rafræns skýrslugerðarsniðs eftir að síðuskipting skjals er innleidd.](./media/er-paginate-excel-reports-format3.png)

### <a name="add-data-sources-to-calculate-page-footer-totals"></a>Bæta við gagnagjöfum til að reikna út samtölur síðufótar

Þú verður að stilla nýja gagnagjafa til að reikna út samtölu síðu, hlaupandi talningu og hlaupandi heildargildi og til að sýna þetta í hluta síðufótar. Mælt er með því að nota gagnagjafana [Gagnasöfnun](er-data-collection-data-sources.md) í þessum tilgangi.

1. Á síðunni **Sniðshönnuður** skal velja flipann **Vörpun**.
2. Veldu **Bæta við rót** og fylgdu síðan eftirfarandi skrefum:

    1. Í svarglugganum **Bæta við gagnagjafa**, í hlutanum **Almennt**, skal velja **Tómt hólf**.
    2. Í svargluggann **Eiginleikar gagnagjafa fyrir „Tómt hólf“**, í reitinn **Heiti**, skal færa inn **Samtala**.
    3. Veldu **Í lagi**.

3. Veldu gagnagjafann **Samtala**, veldu **Bæta við** og fylgdu þessum skrefum:

    1. Í svarglugganum **Bæta við gagnagjafa**, í hlutanum **Almennt**, skal velja **Tómt hólf**.
    2. Í svargluggann **Eiginleikar gagnagjafa fyrir „Tómt hólf“**, í reitinn **Heiti**, skal færa inn **Síða**.
    3. Veldu **Í lagi**.

4. Veldu aftur **Bæta við** og fylgdu síðan þessum skrefum:

    1. Í svarglugganum **Bæta við gagnagjafa**, í hlutanum **Almennt**, skal velja **Tómt hólf**.
    2. Í svargluggann **Eiginleikar gagnagjafa fyrir „Tómt hólf“**, í reitinn **Heiti**, skal færa inn **Hlaupandi**.
    3. Veldu **Í lagi**.

5. Veldu gagnagjafann **Total.Page**, veldu **Bæta við** og fylgdu þessum skrefum:

    1. Í svarglugganum **Bæta við gagnagjafa**, í hlutanum **Virkni**, skal velja **Gagnasöfnun**.
    2. Í svargluggann **Eiginleikar gagnagjafa fyrir „Gagnasöfnun“**, í reitinn **Heiti**, skal færa inn **Upphæð**.
    3. Í reitnum **Gerð vöru** velurðu **Rauntala**.
    4. Stilltu valkostinn **Safna öllum gildum** á **Já**.
    5. Veldu **Í lagi**.

6. Veldu aftur **Bæta við** og fylgdu síðan þessum skrefum:

    1. Í svarglugganum **Bæta við gagnagjafa**, í hlutanum **Virkni**, skal velja **Gagnasöfnun**.
    2. Í svargluggann **Eiginleikar gagnagjafa fyrir „Gagnasöfnun“**, í reitinn **Heiti**, skal færa inn **Þyngd**.
    3. Í reitnum **Gerð vöru** velurðu **Rauntala**.
    4. Stilltu valkostinn **Safna öllum gildum** á **Já**.
    5. Veldu **Í lagi**.

7. Veldu gagnagjafann **Total.Running**, veldu **Bæta við** og fylgdu þessum skrefum:

    1. Í svarglugganum **Bæta við gagnagjafa**, í hlutanum **Virkni**, skal velja **Gagnasöfnun**.
    2. Í svargluggann **Eiginleikar gagnagjafa fyrir „Gagnasöfnun“**, í reitinn **Heiti**, skal færa inn **Upphæð**.
    3. Í reitnum **Gerð vöru** velurðu **Rauntala**.
    4. Stilltu reitinn **Safna öllum gildum** á **Já**.
    5. Veldu **Í lagi**.

8. Veldu aftur **Bæta við** og fylgdu síðan þessum skrefum:

    1. Í svarglugganum **Bæta við gagnagjafa**, í hlutanum **Virkni**, skal velja **Gagnasöfnun**.
    2. Í svargluggann **Eiginleikar gagnagjafa fyrir „Gagnasöfnun“**, í reitinn **Heiti**, skal færa inn **Þyngd**.
    3. Í reitnum **Gerð vöru** velurðu **Rauntala**.
    4. Stilltu reitinn **Safna öllum gildum** á **Já**.
    5. Veldu **Í lagi**.

9. Veldu aftur **Bæta við** og fylgdu síðan þessum skrefum:

    1. Í svarglugganum **Bæta við gagnagjafa**, í hlutanum **Virkni**, skal velja **Gagnasöfnun**.
    2. Í svargluggann **Eiginleikar gagnagjafa fyrir „Gagnasöfnun“**, í reitinn **Heiti**, skal færa inn **Línur**.
    3. Velja **Heiltala** í svæðinu **gerð Vöru**.
    4. Stilltu reitinn **Safna öllum gildum** á **Já**.
    5. Veldu **Í lagi**.

10. Veldu **Vista**.

### <a name="add-data-sources-to-control-page-footer-visibility"></a>Bæta við gagnagjöfum til að stýra sýnileika síðufótar

Ef þú ætlar að stýra sýnileika síðufóta og ætlar ekki að hafa síðufótinn með á lokasíðunni ef hún inniheldur færslur skaltu stilla nýjan gagnagjafa til að reikna út nauðsynlega hlaupandi talningu.

1. Á síðunni **Sniðshönnuður** skal velja flipann **Vörpun**.
2. Veldu gagnagjafann **Total.Running**, veldu **Bæta við**.
3. Í svarglugganum **Bæta við gagnagjafa**, í hlutanum **Virkni**, skal velja **Gagnasöfnun**.
4. Í svargluggann **Eiginleikar gagnagjafa fyrir „Gagnasöfnun“**, í reitinn **Heiti**, skal færa inn **Lines2**.
5. Velja **Heiltala** í svæðinu **gerð Vöru**.
6. Stilltu valkostinn **Safna öllum gildum** á **Já**.
7. Veldu **Í lagi**.
8. Veldu **Vista**.

![Gagnagjöfum sem bætt hefur verið við í sniðshönnuði rafrænnar skýrslugerðar.](./media/er-paginate-excel-reports-format4.png)

### <a name="configure-bindings-to-collect-total-values"></a>Stilla bindingar til að safna heildargildum

1. Á síðunni **Sniðshönnuður**, í sniðstrénu, skaltu stækka þáttinn **Skýrslulínur** og velja faldaða þáttinn **Reikningsvirði**.
2. Veljið **Breyta formúlu**.
3. Breyttu bindiformúlu úr `NUMBERVALUE(NUMBERFORMAT(@.InvoiceValue, "F"&TEXT(model.Parameters.IntrastatAmountDecimals)), ".", "")` í `Total.Page.Amount.Collect(NUMBERVALUE(NUMBERFORMAT(@.InvoiceValue, "F"&TEXT(model.Parameters.IntrastatAmountDecimals)), ".", ""))`.

    > [!NOTE]
    > Auk þess að setja gildi upphæðar í Excel-hólf fyrir hverja endurtekna færslu, safnar þessi binding gildinu í gagnasafn gagnagjafans **Total.Page.Amount**.

4. Veldu faldaða íhlutinn **Þyngd**.
5. Veljið **Breyta formúlu**.
6. Breyttu bindiformúlu úr `@.'$RoundedWeight'` í `Total.Page.Weight.Collect(@.'$RoundedWeight')`.

    > [!NOTE]
    > Auk þess að setja gildi þyngdar í Excel-hólf fyrir hverja endurtekna færslu, safnar þessi binding gildinu í gagnagjafann **Total.Page.Weight**.

![Skilgreindar bindingar fyrir söfnun á heildargildum í hönnuði rafræns skýrslugerðarsniðs.](./media/er-paginate-excel-reports-format5.png)

### <a name="configure-bindings-to-fill-in-page-footer-totals"></a>Skilgreina bindingar til að fylla út samtölur síðufóta

1. Á síðunni **Sniðshönnuður**, í sniðstrénu, skal stækka þáttinn **Síðufótur skýrslu**, velja faldaða **Sviðsþáttinn** sem vísar í Excel-hólfið **ReportPageFooter\_PageAmount** og síðan fylgja þessum skrefum:

    1. Í tréi gagnagjafanna hægra megin skal velja atriðið **Total.Page.Amount.Sum()**.
    2. Veldu **Binda**.
    3. Veljið **Breyta formúlu**.
    4. Uppfærðu formúluna í `Total.Page.Amount.Sum(false)`.

    > [!NOTE]
    > Þú verður að tilgreina frumbreytu þessarar aðgerðar sem **Ósatt** til að halda söfnuðum gögnum fyrir núverandi síðu, þar sem þessi gögn eru nauðsynleg til að reikna út hlaupandi samtölu upphæðar í línum á hverri síðu og hlaupandi talningar á línum.

2. Í sniðstrénu skal velja faldaða **Sviðsþáttinn** sem vísar í Excel-hólfið **ReportPageFooter\_PageWeight** og síðan fylgja þessum skrefum:

    1. Í tréi gagnagjafanna hægra megin skal velja atriðið **Total.Page.Weight.Sum()**.
    2. Veldu **Binda**.
    3. Veljið **Breyta formúlu**.
    4. Uppfærðu formúluna í `Total.Page.Weight.Sum(false)`.

### <a name="configure-bindings-to-fill-in-page-running-totals"></a>Skilgreina bindingar til að fylla út hlaupandi samtölur síðu

1. Á síðunni **Sniðshönnuður**, í sniðstrénu, skal stækka þáttinn **Síðufótur skýrslu**, velja faldaða **Sviðsþáttinn** sem vísar í Excel-hólfið **ReportPageFooter\_RunningTotalAmount** og síðan fylgja þessum skrefum:

    1. Í tréi gagnagjafanna hægra megin skal velja atriðið **Total.Running.Amount.Collect()**.
    2. Veldu **Binda**.
    3. Veljið **Breyta formúlu**.
    4. Uppfærðu formúluna í `Total.Running.Amount.Sum(false)+Total.Running.Amount.Collect(Total.Page.Amount.Sum(true))`.

    > [!NOTE]
    > Viðfangið `Total.Running.Amount.Sum(false)` skilar áður safnaðri hlaupandi samtölu upphæðar. Viðfangið `Total.Running.Amount.Collect(Total.Page.Amount.Sum(true))` skilar heildarupphæð núverandi síðu. Þú verður að tilgreina frumbreytu faldaðrar aðgerðar næsta viðfangs sem **Satt** til að endurstilla `Total.Page.Amount` gagnasöfnunina um leið og þetta gildi er sett inn í samantekt `Total.Running.Amount` hlaupandi samtölu. Uppgefin frumbreyta verður að byrja á því að safna saman samtölu næstu síðu frá 0 (núlli).
    >
    > Kallað er á aðgerðina `Total.Running.Amount.Sum(false)` til að færa inn hlaupandi samtölu upphæðar í Excel-hólfinu **ReportPageFooter\_RunningTotalAmount** á núverandi síðu.

2. Í sniðstrénu skal velja faldaða **Sviðsþáttinn** sem vísar í Excel-hólfið **ReportPageFooter\_RunningTotalWeight** og síðan fylgja þessum skrefum:

    1. Í tréi gagnagjafanna hægra megin skal velja atriðið **Total.Running.Weight.Collect()**.
    2. Veldu **Binda**.
    3. Veljið **Breyta formúlu**.
    4. Uppfærðu formúluna í `Total.Running.Weight.Sum(false)+Total.Running.Weight.Collect(Total.Page.Weight.Sum(true))`.

### <a name="configure-bindings-to-fill-in-the-page-running-counter"></a>Skilgreina bindingar til að fylla út hlaupandi talningu síðu

1. Á síðunni **Sniðshönnuður**, í sniðstrénu, skal stækka þáttinn **Síðufótur skýrslu** og velja faldaða **Sviðsþáttinn** sem vísar í Excel-hólfið **ReportPageFooter\_RunningCounterLines**.
2. Veljið **Breyta formúlu**.
3. Bæta við formúlunni `Total.Running.Lines.Collect(COUNT(Total.Page.Amount.Result))`.

    > [!NOTE]
    > Þessi formúla skilar fjölda safnaðra gilda fyrir upphæð fyrir alla skýrsluna. Þessi tala jafngildir fjölda færslna sem hafa verið endurteknar fram að þessu. Á að sama tíma skilar formúlan skilaða gildinu í safnið **Total.Running.Lines**.

### <a name="configure-bindings-to-fill-in-the-page-footer-counter"></a>Skilgreina bindingar til að fylla út talningu síðufótar

1. Á síðunni **Sniðshönnuður**, í sniðstrénu, skal stækka þáttinn **Síðufótur skýrslu** og velja faldaða **Sviðsþáttinn** sem vísar í Excel-hólfið **ReportPageFooter\_PageLines**.
2. Veljið **Breyta formúlu**.
3. Bæta við formúlunni `COUNT(Total.Page.Amount.Result)-Total.Running.Lines.Sum(false)`.

    > [!NOTE]
    > Þessi formúla reiknar út fjölda færslna á núverandi síðu sem mismuninn á milli fjölda færslna sem var safnað í **Total.Page.Amount.Result** fyrir alla skýrsluna og fjölda færslna sem hafa verið geymdar á þessu stigi í **Total.Running.Lines.Sum**. Þar sem fjöldi færslna fyrir núverandi síðu er geymdur í **Total.Running.Lines** í bindingu **Sviðsþáttarins** sem vísar í Excel-hólfið **ReportPageFooter\_RunningCounterLines**, er fjöldi færslna á núverandi síðu ekki hafður með enn sem komið er. Því jafngildir þessi munur fjölda færslna á núverandi síðu.

![Skilgreindar bindingar fyrir útfyllingu á talningu síðufótar í hönnuði rafræns skýrslugerðarsniðs.](./media/er-paginate-excel-reports-format6.png)

### <a name="configure-component-visibility"></a>Skilgreina sýnileika þáttar

Þú getur breytt sýnileika síðuhauss og síðufótar á tiltekinni síðu myndaðs skjals til að fela eftirfarandi einingar:

- Síðuhausinn á fyrstu síðunni vegna þess að síðuhaus skýrslu inniheldur nú þegar dálkatitla
- Síðuhaus einhverrar síðu sem er ekki með færslur sem geta komið upp á síðustu síðunni
- Síðufótur einhverrar síðu sem er ekki með færslur sem geta komið upp á síðustu síðunni

Til að breyta sýnileikanum skal uppfæra eiginleikann **Virkjað** fyrir þættina **Síðuhaus skýrslu** og **Síðufótur skýrslu**.

1. Á síðunni **Sniðshönnuður**, í sniðstrénu, skal stækka þáttinn **Skýrslusíða**, velja faldaða þáttinn **Síðuhaus skýrslu** og síðan fylgja þessum skrefum:

    1. Veldu **Breyta** fyrir reitinn **Virkjað**.
    2. Á síðunni **Formúluhönnuður**, í reitinn **Formúla**, skal slá inn eftirfarandi segð:

        `AND(`<br>
        `COUNT(Total.Page.Amount.Result)<>0,`<br>
        `COUNT(Total.Page.Amount.Result)<>COUNT(model.CommodityRecord)`<br>
        `)`

2. Í sniðstrénu skal velja faldaða þáttinn **Síðufótur skýrslu** og síðan fylgja þessum skrefum:

    1. Veldu **Breyta** fyrir reitinn **Virkjað**.
    2. Á síðunni **Formúluhönnuður**, í reitinn **Formúla**, skal slá inn eftirfarandi segð:

        `(`<br>
        `COUNT(Total.Page.Amount.Result)-Total.Running.Lines2.Sum(false)+`<br>
        `0*Total.Running.Lines2.Collect(COUNT(Total.Page.Amount.Result))`<br>
        `)<>0`

    > [!NOTE]
    > Skipulagningin `COUNT(Total.Page.Amount.Result)-Total.Running.Lines2.Sum(false)` er notuð til að reikna út fjölda færslna á núverandi síðu. Skipulagningin `0*Total.Running.Lines2.Collect(COUNT(Total.Page.Amount.Result)` er notuð til að bæta fjölda færslna á núverandi síðu við safnið til að meðhöndla sýnileikann á næsta síðufæti á réttan hátt.
    >
    > Ekki er hægt að endurnota `Total.Running.Lines` safnið hér vegna þess að eiginleikinn **Virkja** fyrir grunnþátt er afgreiddur **eftir** að búið er að vinna úr bindingum faldaðra þátta. Þegar unnið hefur verið úr eiginleikanum **Virkjað** er `Total.Running.Lines` safnið þegar hækkað um því sem nemur færslufjöldanum á núverandi síðu.

3. Veldu **Vista**.

## <a name="generate-an-intrastat-declaration-control-report-updated"></a>Búa til Intrastat-skattskýrslu (uppfærð)

1. Gakktu úr skugga um að þú sért með 24 færslur á **Intrastat-síðunni**. Endurtaktu skrefin í hlutanum [Búa til eftirlitsskýrslu Intrastat-skattskýrslu](#generate-intrastat-control-report) í þessari grein til að búa til og fara yfir eftirlitsskýrsluna.

    Allar færslur koma fram á fyrstu síðunni. Samtölur og teljarar síðunnar jafngilda samtölum og teljurum skýrslunnar. Svið síðuhaussins er falið á fyrstu síðunni vegna þess að síðuhaus skýrslu inniheldur nú þegar dálkatitla. Síðuhaus og síðufótur eru faldir á næstu síðu vegna þess að síðan inniheldur engar færslur.

    ![Excel-skjal búið til í skjáborðsforriti.](./media/er-paginate-excel-reports-document2.gif)

2. Uppfærðu tvær færslur á **Intrastat-síðunni** með því að breyta kóðanum **Vörunúmer** úr **D00006** í **L0010**. Takið eftir að afurðarheiti nýju vörunnar, **Par af virkum steríóhátölurum**, er ekki lengur afurðarheiti upprunalegrar vöru, **Venjulegur hátalari**. Þessi staða þvingar textaskrið í samsvarandi hólfi myndaðs skjals. Nú þarf að uppfæra síðuskiptingu skjals og samlagningu og talningu á síðu. Endurtaktu skrefin í hlutanum [Búa til eftirlitsskýrslu Intrastat-skattskýrslu](#generate-intrastat-control-report) til að búa til og fara yfir eftirlitsskýrsluna.

    Sem stendur eru færslur sýndar á tveimur síðum og samtölur og teljarar síðu eru reiknaðir á réttan hátt. Svið síðuhauss er falið á réttan hátt á fyrstu síðunni og sýnilegt á næstu síðu. Síðufóturinn er sýnilegur á báðum síðunum vegna þess að þær innihalda færslur.

    ![Myndað Excel-skjal uppfært í skjáborðsforritinu.](./media/er-paginate-excel-reports-document3.gif)

## <a name="frequently-asked-questions"></a>Algengar spurningar

### <a name="is-there-any-way-to-recognize-when-the-final-page-is-processed-by-the-page-format-component"></a>Er einhver leið til að sjá hvenær sniðsþáttur síðu vinnur úr síðustu síðunni?

**Síðuþátturinn** [sýnir ekki](er-fillable-excel.md#page-component-limitations) upplýsingar um afgreiddan síðufjölda og heildarsíðufjölda í mynduðu skjali. Aftur á móti geturðu stillt [formúlur](er-formula-language.md) rafrænnar skýrslugerðar til að bera kennsl á síðustu síðuna. Eftirfarandi er dæmi:

- Reiknaðu út heildarfjölda færslna sem hefur þegar verið afgreiddur með því að nota þáttinn **Skýrslusíða**. Hægt er að gera þennan útreikning með því að nota formúluna `COUNT(Total.Page.Amount.Result)`. 
- Reiknaðu út heildarfjölda færslna sem þarf að afgreiða samkvæmt `model.CommodityRecord` bindingunni sem er skilgreind fyrir þáttinn **Skýrslulínur**. Hægt er að gera þennan útreikning með því að nota formúluna `COUNT(model.CommodityRecord)`.
- Bera saman tvær tölur til að greina lokasíðuna. Þegar bæði gildin eru jöfn er lokasíðan búin til.

> [!NOTE]
> Við mælum með því að þú notir aðeins þessa aðferð þegar eiginleikinn **Virkjað** fyrir þáttinn **Skýrslulínur** inniheldur enga formúlu sem gæti skilað [Ósatt](er-formula-supported-data-types-primitive.md#boolean) á keyrslutíma fyrir sumar endurteknu [færslurnar](er-formula-supported-data-types-composite.md#record) í bundna [Færslulistanum](er-formula-supported-data-types-composite.md#record-list).

## <a name="additional-resources"></a>Frekari upplýsingar

- [Hanna skilgreiningu fyrir myndun skjala á Excel-sniði](er-fillable-excel.md)
- [Nota gagnagjafa GAGNASÖFNUNAR í rafrænum skýrslugerðarsniðum](er-data-collection-data-sources.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
