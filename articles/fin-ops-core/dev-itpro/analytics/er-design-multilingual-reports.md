---
title: Hanna skýrslur á mörgum tungumálum í rafrænni skýrslugerð
description: Þessi grein útskýrir hvernig hægt er að nota merki rafrænnar skýrslugerðar til að hanna og búa til skýrslur á mörgum tungumálum.
author: kfend
ms.date: 05/31/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: ''
ms.assetid: ''
ms.search.form: ERDataModelDesigner, ERModelMappingDesigner, EROperationDesigner, ERExpressionDesignerFormula
ms.openlocfilehash: 5575ba3154521e3855ce6b97c5b37d3c4868e3e9
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285486"
---
# <a name="design-multilingual-reports-in-electronic-reporting"></a>Hanna skýrslur á mörgum tungumálum í rafrænni skýrslugerð

[!include[banner](../includes/banner.md)]

## <a name="overview"></a>Yfirlit

Sem fyrirtækisnotandi getur þú notað rammann [Rafræn skýrslugerð](general-electronic-reporting.md) til að skilgreina snið fyrir skjöl á útleið sem búa þarf til í samræmi við reglugerðir ýmissa landa eða svæða. Þegar þessar reglugerðir krefjast þess að skjöl á útleið verði búin til á mismunandi tungumálum fyrir mismunandi lönd eða svæði er hægt að skilgreina eitt snið rafrænnar skýrslugerðar sem inniheldur tungumálaháð tilföng. Þannig er hægt að endurnýta sniðið til að búa til skjöl á útleið fyrir ýmis lönd eða svæði. Þú gætir einnig viljað nota eitt snið rafrænnar skýrslugerðar til að búa til skjal á útleið á mismunandi tungumálum fyrir samsvarandi viðskiptavini, lánardrottna, dótturfélög eða aðra aðila.

Hægt er að skilgreina gagnalíkön og gagnavarpanir rafrænnar skýrslugerðar sem gagnagjafa skilgreindra sniða rafrænnar skýrslugerðar til að skilgreina gagnaflæði sem tilgreinir hvaða forritsgögn eru sett inn í mynduð skjöl. Sem [veitandi](general-electronic-reporting.md#Provider) skilgreiningar rafrænnar skýrslugerðar geturðu [gefið út](tasks/er-upload-configuration-into-lifecycle-services.md#upload-a-configuration-into-lcs) skilgreind gagnalíkön, líkanavarpanir og snið sem hluta fyrir lausn rafrænnar skýrslugerðar til að búa til ákveðin skjöl á útleið. Einnig er hægt að leyfa viðskiptavinum að [hlaða upp](general-electronic-reporting-manage-configuration-lifecycle.md) útgefinni lausn rafrænnar skýrslugerðar svo hægt sé að nota hana og sérstilla. Ef gert er ráð fyrir að viðskiptavinir tali önnur tungumál er hægt að stilla hluta rafrænnar skýrslugerðar þannig að þeir innihaldi tungumálaháð tilföng. Þannig er hægt að kynna efni breytanlegs hluta rafrænnar skýrslugerðar á kjörtungumáli viðskiptavinar á hönnunartíma.

Hægt er að stilla tungumálaháð tilföng sem merki rafrænnar skýrslugerðar. Þá er hægt að nota þessi merki til að stilla hluta rafrænnar skýrslugerðar af eftirfarandi ástæðu:

- Á hönnunartíma:

    - Kynna efni skilgreindra hluta rafrænnar skýrslugerðar á kjörtungumáli notanda.

- Á keyrslutíma:

    - Búa til tungumálaháð efni fyrir skjöl á útleið.
    - Bjóða upp á viðvaranir og villuboð á kjörtungumáli notanda.
    - Biðja um skyldusvæði á kjörtungumáli notanda.

Hægt er að stilla merki rafrænnar skýrslugerðar í öllum [skilgreiningum](general-electronic-reporting.md#Configuration) rafrænnar skýrslugerðar sem innihalda mismunandi hluta. Hægt er að vinna með merkin óháð skilgreindum reglum gagnalíkana og líkanavarpana rafrænnar skýrslugerðar og hluta rafræns skýrslugerðarsniðs.

Sérhvert merki rafrænnar skýrslugerðar þekkist á auðkenni sem er einkvæmt innan umfangs skilgreiningar rafrænnar skýrslugerðar sem er með merkið. Sérhvert merki getur innihaldið texta fyrir öll tungumál sem eru studd í núverandi tilviki af Microsoft Dynamics 365 Finance. Þessi studdu tungumál fela í sér tungumál uppsettra sérstillinga.

## <a name="entry"></a>Færsla

Þegar gagnalíkan, líkanavörpun eða snið rafrænnar skýrslugerðar er hannað er valkosturinn **Þýða** sýndur í hvert skipti sem valinn er reitur sem gæti innihaldið þýðanlega samhengið. Þegar þessi kostur er valinn er hægt að tengja valinn reit við merki rafrænnar skýrslugerðar á **svæði** <a name="TextTranslationPane">Textaþýðingar</a>. Hægt er að velja núverandi merki rafrænnar skýrslugerðar eða bæta við nýju merki ef það er ekki tiltækt. Þegar valið eða bætt er við merki rafrænnar skýrslugerðar er hægt að bæta við viðeigandi texta fyrir öll þau tungumál sem studd eru í núverandi tilviki af Finance.

Eftirfarandi skýringarmynd sýnir hvernig þessi þýðing er gerð í breytanlegu gagnalíkani rafrænnar skýrslugerðar. Í þessu dæmi er eigindin **Lýsing** í reitnum **PurchaseOrder** fyrir breytanlega **Reikningslíkanið** þýdd yfir á austurríska þýsku (DE-AT) og japönsku (JA).

![Boðið upp á þýðingu á merki rafrænnar skýrslugerðar í gagnalíkanshönnuði rafrænnar skýrslugerðar.](./media/er-multilingual-labels-refer.png)

Aðeins texta fyrir merki sem eru í breytanlegum hluta rafrænnar skýrslugerðar er hægt að þýða. Ef til dæmis er valið **Þýða** fyrir eigind merkis í gagnagjafa líkanavörpunar rafrænnar skýrslugerðar og síðan er merki rafrænnar skýrslugerðar valið sem er að finna í yfireiningu gagnalíkans rafrænnar skýrslugerðar verður hægt að sjá innihald merkisins, en ekki er hægt að breyta því. Í slíku tilfelli er reiturinn **Þýddur texti** ekki í boði eins og sýnt er á eftirfarandi skýringarmynd.

![Farið yfir þýðingu á merki rafrænnar skýrslugerðar í hönnuði líkanavörpunar rafrænnar skýrslugerðar.](./media/er-multilingual-labels-refer-mapping.png)

> [!NOTE]
> Ekki er hægt að nota hönnuðina til að eyða merki sem hefur verið fært inn í breytanlegan hluta rafrænnar skýrslugerðar.

## <a name="scope"></a>Gildissvið

Hægt er að vísa til merkja rafrænnar skýrslugerðar í nokkrum þýðanlegum eigindum í hlutum rafrænnar skýrslugerðar.

### <a name="data-model-component"></a>Þættir gagnalíkana

Þegar gagnalíkan rafrænnar skýrslugerðar er skilgreint er hægt að bæta við merkjum rafrænnar skýrslugerðar fyrir það. Eigindirnar **Merki** og **Lýsing** í líkanaeiningunni, alla reiti líkans og öll <a id="LinkModelEnum"></a>tölusetningargildi líkans er hægt að tengja við merki rafrænnar skýrslugerðar sem bætt er við gagnalíkan rafrænnar skýrslugerðar.

![Boðið upp á þýðingu á eigind lýsingar í gagnalíkanshönnuði rafrænnar skýrslugerðar.](./media/er-multilingual-labels-refer.png)

Þegar gagnalíkan rafrænnar skýrslugerðar er skilgreint á þennan hátt verður efni þess sýnt notendum gagnalíkanshönnuðar rafrænnar skýrslugerðar á öllum kjörtungumálum notenda. Þess vegna er vinna í kringum líkan einfölduð. Eftirfarandi skýringarmyndir sýna hvernig þessi virkni fer fram fyrir notendur sem eru með DE-AT og JA stillt sem þeirra kjörtungumál.

![Útlit gagnalíkanshönnuðar rafrænnar skýrslugerðar fyrir notanda með DE-AT stillt sem kjörtungumál.](./media/er-multilingual-labels-refer-de.png)

![Útlit gagnalíkanshönnuðar rafrænnar skýrslugerðar fyrir notanda með JA stillt sem kjörtungumál.](./media/er-multilingual-labels-refer-ja.png)

### <a name="model-mapping-component"></a>Hluti líkanavörpunar

Vegna þess að líkanavörpun rafrænnar skýrslugerðar er byggð á gagnalíkani rafrænnar skýrslugerðar, birtast gagnalíkanseiningarnar sem átt er við á kjörtungumáli notanda í hönnuði líkanavörpunar. Eftirfarandi skýringarmynd sýnir hvernig merking reitsins **PurchaseOrder** er útskýrð í breytanlegri líkanavörpun með því að nota merki eigindarinnar **Lýsing** sem bætt hefur verið við skilgreint gagnalíkan. Takið eftir að þetta merki er sýnt á kjörtungumáli notanda (DE-AT í þessu dæmi).

![Útlit hönnuðar líkanavörpunar rafrænnar skýrslugerðar fyrir notanda með DE-AT stillt sem kjörtungumál.](./media/er-multilingual-labels-show-mapping.png)

Þegar eigindin **Merki** í gagnagjafanum **Innsláttarfæribreyta notanda** er skilgreind sem tengd við merki rafrænnar skýrslugerðar er reitur færibreytu sem samsvarar þessum gagnagjafa sýndur í notendasvarglugga við keyrslu á kjörtungumáli notenda.

### <a name="format-component"></a>Sniðsþáttur

Þegar snið rafrænnar skýrslugerðar er skilgreint er hægt að bæta við merkjum rafrænnar skýrslugerðar fyrir það. Eigindirnar **Merki** og **Hjálpartexti** fyrir alla skilgreinda gagnagjafa er hægt að tengja við merki rafrænnar skýrslugerðar sem bætt er við snið rafrænnar skýrslugerðar. Eigindirnar **Merki** og **Lýsing** allra <a id="LinkFormatEnum"></a>tölusetningargilda sniðs er einnig hægt að tengja við merki rafrænnar skýrslugerðar sem er aðgengilegt úr breytanlegu sniði rafrænnar skýrslugerðar.

> [!NOTE]
> Einnig er hægt að tengja þessar eigindir við merki rafrænnar skýrslugerðar fyrir yfirgagnalíkan rafrænnar skýrslugerðar sem notar aftur merki líkansins í öllum sniðum rafrænnar skýrslugerðar sem skilgreint er fyrir þetta gagnalíkan rafrænnar skýrslugerðar.

Þegar snið rafrænnar skýrslugerðar er skilgreint á þennan hátt verður efni sniðsins sýnt notendum aðgerðarhönnuðar rafrænnar skýrslugerðar á öllum kjörtungumálum notenda. Þess vegna er vinna með snið og greining á skilgreindri reglu einfaldað.

Vegna þess að snið rafrænnar skýrslugerðar byggir á gagnalíkani rafrænnar skýrslugerðar eru merkin sem vísað er til í einingum gagnalíkansins sýnd í sniðshönnuði rafrænnar skýrslugerðar á kjörtungumáli notanda.

Þegar eigindin **Merki** í gagnagjafanum **Innsláttarfæribreyta notanda** er tengd við merki rafrænnar skýrslugerðar er reiturinn sem samsvarar færibreytunni í notendasvarglugga við keyrslu sýndur notanda sem kvaðning. Eftirfarandi skýringarmyndir sýna hvernig hægt er að tengja eigindina **Merki** fyrir gagnagjafann **Innsláttarfæribreyta notanda** við hönnun á merki rafrænnar skýrslugerðar þannig að notendur eru beðnir um færibreytuna á mismunandi kjörtungumálum notenda (sýnt fyrir bandaríska ensku (EN-US) og DE-AT) við keyrslu.

![Boðið upp á þýðingu á eigindum innsláttarfæribreytu notanda í aðgerðarhönnuði rafrænnar skýrslugerðar.](./media/er-multilingual-labels-refer-format.png)

![Úrvinnsla lánardrottnagreiðslu rafrænnar skýrslugerðar við keyrslu fyrir notendur með kjörtungumálið EN-US.](./media/er-multilingual-labels-show-runtime-en.png)

![Úrvinnsla lánardrottnagreiðslu rafrænnar skýrslugerðar við keyrslu fyrir notendur með kjörtungumálið DE-AT.](./media/er-multilingual-labels-show-runtime-de.png)

### <a name="expressions"></a>Svipbrigði

Til að nota merki í [segð](er-formula-language.md) rafrænnar skýrslugerðar þarf að nota skipunina **@"GER\_LABEL:X"** þar sem forskeytið **@** þýðir að viðfangið vísar til merkis, **GER\_LABEL** þýðir að merki rafrænnar skýrslugerðar á við og **X** er auðkenni merkis rafrænnar skýrslugerðar.

![Skilgreining á segð rafrænnar skýrslugerðar sem inniheldur tilvísun í merki rafrænnar skýrslugerðar í formúluhönnuði rafrænnar skýrslugerðar.](./media/er-multilingual-labels-expression1.png)

Til að vísa í merki kerfis (forrits) skal nota skipunina **@"X"** þar sem forskeytið **@** þýðir að viðfangið vísar til merkis og **X** er auðkenni kerfismerkisins.

![Skilgreining á segð rafrænnar skýrslugerðar sem inniheldur tilvísun í merki forrits í formúluhönnuði rafrænnar skýrslugerðar.](./media/er-multilingual-labels-expression2.png)

#### <a name="model-mapping"></a>Vörpun líkans

Segð líkanavörpunar rafrænnar skýrslugerðar er hægt að skilgreina með því að nota merki. Þegar snið rafrænnar skýrslugerðar, sem keyrt er til að búa til skjal á útleið, kallar á þessa vörpun, felur samhengi framkvæmdarinnar í sér tungumálakóða. Fyllt verður út í skilgreint merki segðar með texta merkis sem stillt hefur verið á tungumál þess samhengis.

Ef merki sem vísað er í er ekki með neina þýðingu fyrir tungumál keyrslusniðs þess samhengis sem kallar á líkanavörpunina, verður texti merkis á EN-US notað í staðinn.

#### <a name="format"></a>Snið

Hægt er að stilla segð rafrænnar skýrslugerðar fyrir snið rafrænnar skýrslugerðar með því að nota merki. Þegar þetta snið er keyrt til að búa til skjal á útleið felur samhengi keyrslunnar í sér tungumálakóða. Fyllt verður út í skilgreint merki segðar með texta merkis sem stillt hefur verið á tungumál þess samhengis.

![Boðið upp á þýðingu á merki rafrænnar skýrslugerðar fyrir breytanlega segð rafrænnar skýrslugerðar í formúluhönnuði rafrænnar skýrslugerðar.](./media/er-multilingual-labels-refer-in-expression.png)

![Sýnishorn af gagnabindingu sem vísar til merkis rafrænnar skýrslugerðar í aðgerðarhönnuði rafrænnar skýrslugerðar.](./media/er-multilingual-labels-refer-in-binding.png)

Hægt er að stilla hlutann **FILE** af sniði rafrænnar skýrslugerðar til að búa til skýrsluna á kjörtungumáli notandans.

![Setja upp FILE-hlutann í aðgerðarhönnuði rafrænnar skýrslugerðar til að búa til skýrsluna á kjörtungumáli notandans.](./media/er-multilingual-labels-language-context-user.png)

Ef snið rafrænnar skýrslugerðar er skilgreint á þennan hátt er skýrslan búin til með því að nota samsvarandi texta og er fyrir merki rafrænnar skýrslugerðar. Eftirfarandi skýringarmyndir sýna dæmi um skýrslur fyrir EN-US og DE-AT tungumál notanda.

![Forskoðun skýrslunnar sem búin hefur verið til á EN-US kjörtungumáli notanda.](./media/er-multilingual-labels-report-preview-en.png)

![Forskoðun skýrslunnar sem búin hefur verið til á DE-AT kjörtungumáli notanda.](./media/er-multilingual-labels-report-preview-de.png)

Ef merki sem vísað er í er ekki með neina þýðingu fyrir tungumál keyrslusniðs fyrir það samhengi verður texti merkis á EN-US notað í staðinn.

> [!TIP]
> Hægt er að nota **MÖPPU** og sérstakar gerðir af **SKRÁ** í breytanlegu sniði rafrænnar skýrslugerðar til að tilgreina hvernig á að búa til skrá á útleið. Til að nefna skrá sem er búin til skal skilgreina [segð](er-formula-language.md) rafrænnar skýrslugerðar fyrir færibreytuna **Skráarheiti** fyrir þáttinn. Hægt er að nota merkimiða í skilgreindu segðinni. Þar sem færibreytan **Skráarheiti** er sjálfgefið óháð tungumáli er öllum merkjum sem vísað er til í þessari segð sýnd á sjálfgefnu EN-US tungumáli við keyrslu. Í útgáfu 10.0.28 eða nýrri er aftur á móti hægt að virkja eiginleikann **Nota færibreytuna „Tungumálastillingar“ fyrir segðina „Skráarheiti“**. Segðin **Skráarheiti** tekur þá til greina færibreytuna **Kjörstillingar tungumáls** þegar hún er reiknuð út.

## <a name="language"></a>Tungumál

Rafræn skýrslugerð styður mismunandi leiðir til að tilgreina tungumál fyrir myndaða skýrslu. Í reitnum **Kjörstillingar tungumáls** í flipanum **Snið** er hægt að velja eftirfarandi gildi:

- **Kjörstillingar fyrirtækis** - Búa til skýrslu á tungumáli fyrirtækisins.

    ![Tilgreina í aðgerðarhönnuði rafrænnar skýrslugerðar kjörtungumál fyrirtækis sem tungumál myndaðrar skýrslu.](./media/er-multilingual-labels-language-context-company.png)

- **Kjörstilling notanda** - Búa til skýrslu á kjörtungumáli notanda.
- **Skilgreint skilmerkilega** - Búa til skýrslu á tungumáli sem tilgreint er við hönnun.

    ![Tilgreina í aðgerðarhönnuði rafrænnar skýrslugerðar skilgreint tungumál við hönnun sem tungumál myndaðrar skýrslu.](./media/er-multilingual-labels-language-context-fixed.png)

- **Skilgreint við keyrslu** - Búa til skýrslu á tungumáli sem tilgreint er við keyrslu. Ef þetta gildi er valið, í reitnum **Tungumál**, skal skilgreina segð rafrænnar skýrslugerðar sem skilar tungumálakóðanum fyrir tungumálið, á borð við tungumál samsvarandi viðskiptavinar.

    ![Tilgreina í aðgerðarhönnuði rafrænnar skýrslugerðar skilgreint tungumál við keyrslu sem tungumál myndaðrar skýrslu.](./media/er-multilingual-labels-language-context-runtime.png)

## <a name="culture-specific-formatting"></a>Menningarbundið snið

Rafræn skýrslugerð styður mismunandi leiðir til að tilgreina menningu fyrir myndaða skýrslu. Þess vegna er hægt að nota menningarbundið snið fyrir dagsetningu, tíma og tölugildi. Þegar snið rafrænnar skýrslugerðar er hannað er hægt í flipanum **Snið**, í reitnum **Kjörstillingar menningar**, að velja eitt af eftirfarandi gildum fyrir hvern sniðsþátt af gerðinni **Almenn\\Skrá**, **Excel\\Skrá**, **PDF\\Skrá** eða **PDF\\Samruni**:

- **Kjörstilling notanda** – Sníðið gildin samkvæmt æskilegri menningu notanda. Sú menning er skilgreind í reitnum **Dagsetning, tími og talnasnið** í flipanum **Kjörstillingar** á síðunni **Valkostir notanda**.

    ![Að skilgreina æskilega menningu notanda sem menningu myndaðrar skýrslu í aðgerðarhönnuði rafrænnar skýrslugerðar.](./media/er-multilingual-labels-culture-context-user-preferred.png)

- **Skilgreint skilmerkilega** – Sníðið gildin samkvæmt menningunni sem er tilgreind á hönnunartíma.

    ![Að skilgreina menninguna sem er tilgreind á hönnunartíma sem menningu myndaðrar skýrslu í aðgerðarhönnuði rafrænnar skýrslugerðar.](./media/er-multilingual-labels-culture-context-fixed.png)

- **Skilgreint á keyrslutíma** – Sníðið gildin samkvæmt menningunni sem er tilgreind við keyrslu. Ef þetta gildi er valið, í flipanum **Vörpun**, í reitnum **Dagsetning, tími og talnasnið**, skal skilgreina segð rafrænnar skýrslugerðar sem skilar mennignarkóðanum fyrir menninguna, á borð við menningu samsvarandi viðskiptavinar.

    ![Að skilgreina menninguna sem er skilgreind á keyrslutíma sem menningu myndaðrar skýrslu í aðgerðarhönnuði rafrænnar skýrslugerðar.](./media/er-multilingual-labels-culture-context-runtime.png)

> [!NOTE]
> Hluti rafrænnar skýrslugerðar sem þú skilgreinir ákveðna menningu fyrir gæti innihaldið undirhluta rafrænnar skýrslugerðar sem voru skilgreindir til að fylla í textagildi. Menning yfirhlutans er sjálfkrafa notuð til að sníða gildi þessara hluta. Hægt er að nota eftirfarandi innbyggðar aðgerðir rafrænnar skýrslugerðar til að skilgreina bindingar fyrir þessa hluta og nota aðra menningu fyrir snið gilda:
>
> - [DATEFORMAT](er-functions-datetime-dateformat.md#syntax-2)
> - [DATETIMEFORMAT](er-functions-datetime-datetimeformat.md#syntax-2)
> - [NUMBERFORMAT](er-functions-text-numberformat.md#syntax-2)
>
> Í útgáfu 10.0.20 og síðar er landsstaðall sniðshluta af gerðunum **Almenn\\Skrá** og **Excel\\Skrá** notaður til að sníða gildin við [Umbreytingu PDF-skjals](electronic-reporting-destinations.md#OutputConversionToPDF) á mynduðu skjali.

## <a name="translation"></a>Þýðing

Hægt er að bæta nauðsynlegum merkjum rafrænnar skýrslugerðar við breytanlegan hluta rafrænnar skýrslugerðar. Þegar merki rafrænnar skýrslugerðar er bætt við, er hægt að þýða það á tvenna vegu: handvirkt eða sjálfkrafa.

### <a name="manual-translation"></a>Handvirk þýðing

Þegar bætt er við merki rafrænnar skýrslugerðar í **svæði** [Textaþýðingar](#TextTranslationPane) er hægt að þýða það að sjálfsdáðum yfir á öll tungumál sem studd eru í núverandi tilviki Finance. Hægt er að velja kjörtungumálið í reitnum **Tungumál** í hlutanum **Tungumál kerfis** eða **Tungumál notanda**, slá inn viðeigandi texta í samsvarandi reit **Þýdds texta** og síðan velja **Þýða**. Þetta ferli verður að endurtaka fyrir hvert tungumál og merki sem bætt er við.

### <a name="automatic-translation"></a>Sjálfvirk þýðing

Skilgreining á hluta rafrænnar skýrslugerðar er gerð í útgáfudrögum fyrir skilgreiningu rafrænnar skýrslugerðar þar sem breytanlega hluta rafrænnar skýrslugerðar er að finna.

![Skilgreiningasíða rafrænnar skýrslugerðar sem veitir aðgang að útgáfu skilgreiningar með stöðuna drög.](./media/er-multilingual-labels-configurations.png)

Eins og lýst er fyrr í þessari grein er hægt er að bæta nauðsynlegum merkjum rafrænnar skýrslugerðar við breytanlegan hluta rafrænnar skýrslugerðar. Á þennan hátt er hægt að tilgreina texta fyrir merki rafrænnar skýrslugerðar á tungumálinu EN-US. Síðan er hægt að flytja út merki fyrir hluta rafrænnar skýrslugerðar með því að nota innbyggða virkni rafrænnar skýrslugerðar. Veljið útgáfudrög fyrir skilgreiningu rafrænnar skýrslugerðar sem inniheldur breytanlegan hluta rafrænnar skýrslugerðar og veljið síðan **Skipta út \> Flytja út merki**.

![Skilgreiningasíða rafrænnar skýrslugerðar sem gerir kleift að flytja út merki rafrænnar skýrslugerðar úr valdri skilgreiningarútgáfu.](./media/er-multilingual-labels-export.png)

Hægt er að flytja út annaðhvort öll merki eða merki fyrir ákveðið tungumál sem tilgreint er við upphaf útflutnings. Merki eru flutt út sem zip-skrá sem inniheldur Xml-skrár. Sérhver XML-skrá inniheldur merki fyrir eitt tungumál.

![Sýnishorn af útfluttu skránni sem inniheldur merki rafrænnar skýrslugerðar fyrir tungumálið DE-AT.](./media/er-multilingual-labels-in-xml.png)

Þetta snið er notað fyrir sjálfvirka þýðingu á merkjum sem gerð er af utanaðkomandi þýðingaþjónustu á borð við [Dynamics 365 Translation Service](../lifecycle-services/translation-service-overview.md). Þegar tekið er á móti þýddum merkjum er hægt að flytja þau aftur inn í útgáfudrög fyrir skilgreiningu rafrænnar skýrslugerðar sem inniheldur hluta rafrænnar skýrslugerðar sem eiga þessi merki. Veljið útgáfudrög fyrir skilgreiningu rafrænnar skýrslugerðar sem inniheldur breytanlegan hluta rafrænnar skýrslugerðar og veljið **Skipta út \> Hlaða merkjum**.

![Skilgreiningasíða rafrænnar skýrslugerðar sem gerir kleift að flytja inn merki rafrænnar skýrslugerðar í valda skilgreiningarútgáfu.](./media/er-multilingual-labels-load.png)

Þýdd merki verða flutt inn í valda skilgreiningu rafrænnar skýrslugerðar. Þýddum merkjum sem er að finna í þessari skilgreiningu rafrænnar skýrslugerðar er skipt út. Ef eitthvað þýtt merki vantar í skilgreiningu rafrænnar skýrslugerðar er því bætt við.

## <a name="lifecycle"></a>Stuðningstími

Merki fyrir hluta rafrænnar skýrslugerðar sem hægt er að breyta eru geymd, ásamt öðru efni fyrir þann hluta, í viðeigandi útgáfu fyrir skilgreiningu rafrænnar skýrslugerðar.

Merki grunnhluta rafrænnar skýrslugerðar er hægt að vísa til í afleiddri útgáfu af hluta rafrænnar skýrslugerðar sem búin er til til að kynna breytingarnar.

> [!TIP]
> Þegar rafræn skýrslugerðarlausn er hönnuð er hægt að búa til sinn eigin þátt af [gagnalíkani](er-overview-components.md#data-model-component) í rafrænni skýrslugerð úr einni sem boðið er upp á. Í þessu afleidda gagnalíkani geturðu komið með þín eigin merki rafrænnar skýrslugerðar og notað þau í öllum sniðum rafrænnar skýrslugerðar sem nota gagnalíkanið sem gagnagjafann. Síðan gerirðu þinn eigin þátt af [sniði](er-overview-components.md#format-component) rafrænnar skýrslugerðar úr einu af þeim sem boðið er upp á með því að velja afleidda gagnalíkanið í rafrænni skýrslugerð í stað þess sem gefið er upp. Í útgáfu 10.0.28 eða nýrri er hægt að virkja eiginleikann **Aukinn aðgangur að merkingum ráðandi gagnalíkans rafrænnar skýrslugerðar** fyrir aðgang að merkingum ráðandi gagnalíkans rafrænnar skýrslugerðar í afleiddum sniðshlutum rafrænnar skýrslugerðar jafnvel þegar valið gagnalíkan rafrænnar skýrslugerðar fyrir afleiddan hlut rafrænnar skýrslugerðar er öðruvísi en það sem var notað fyrir grunnhluta rafrænnar skýrslugerðar.
>
> Þegar sama merkjaheiti er notað í afleiddum þætti og ráðandi þáttum er þýðing þín á þessum merkjum notuð sem mest viðeigandi.

Útgáfustjórnun rafrænnar skýrslugerðar stýrir úthlutun merkja til allra eiginda í hluta rafrænnar skýrslugerðar. Breytingar á úthlutun merkis eru geymdar í lista yfir breytingar (delta) fyrir breytanlega hluta rafrænnar skýrslugerðar sem hefur verið búinn til sem afleidd útgáfa af uppgefnum hluta rafrænnar skýrslugerðar. Þessar breytingar verða staðfestar þegar afleidd útgáfa er flutt í nýja grunnútgáfu.

## <a name="functions"></a>Aðgerðir

Innbyggð [LISTOFFIELDS](er-functions-list-listoffields.md) aðgerð rafrænnar skýrslugerðar er með aðgang að merkjum rafrænnar skýrslugerðar sem hafa verið skilgreind fyrir sum atriði í hlutum rafrænnar skýrslugerðar.

Eins og lýst hefur verið hér áður í þessari grein er hægt að tengja eigindirnar **Merki** og **Lýsing** fyrir hvert tölusetningargildi [líkans](#LinkModelEnum) eða [sniðs](#LinkFormatEnum) rafrænnar skýrslugerðar við merki rafrænnar skýrslugerðar sem er aðgengilegt í viðeigandi hluta rafrænnar skýrslugerðar. Hægt er að skilgreina segð rafrænnar skýrslugerðar þar sem kallað er á aðgerðina **LISTOFFIELDS** með því að nota tölusetningu rafrænnar skýrslugerðar sem skipun. Þessi segð skilar lista sem inniheldur færslu fyrir hvert gildi tölusetningar rafrænnar skýrslugerðar sem hefur verið skilgreind sem skipun fyrir þessa aðgerð. Sérhver færsla inniheldur gildið fyrir merki rafrænnar skýrslugerðar sem er tengt við tölusetningargildi rafrænnar skýrslugerðar:

- Gildi fyrir merki rafrænnar skýrslugerðar sem er tengt við eigindirnar **Merki** er vistað í reitnum **Merki** fyrir færsluna sem var skilað.
- Gildi fyrir merki rafrænnar skýrslugerðar sem er tengt við eigindirnar **Lýsing** er vistað í reitnum **Lýsing** fyrir færsluna sem var skilað.

## <a name="performance"></a><a name=performance></a>Afköst

Þegar þú skilgreinir hlut rafræns skýrslugerðarsniðs til að búa til skýrslu á æskilegu [tungumáli](#language) eða til að flytja inn skjal á innleið þar sem innihaldið er þáttað eftir æskilegu tungumáli, mælum við með að þú virkir eiginleikann **Vista kjörtungumál núverandi notanda fyrir keyrslur rafrænna skýrslugerða í skyndiminni** á vinnusvæðinu [Eiginleikastjórnun](../../fin-ops/get-started/feature-management/feature-management-overview.md). Þessi eiginleiki hjálpar til við að bæta afköst, sérstaklega fyrir þætti rafræns skýrslugerðarsniðs sem innihalda margar tilvísanir í merki í formúlum rafrænnar skýrslugerðar og bindingar og margar [villuleitarreglur](general-electronic-reporting-formula-designer.md#TestFormula) til að búa til skilaboð notanda á kjörtungumáli þínu.

Þegar stöðu á skilgreiningarútgáfu rafrænnar skýrslugerðar er breytt úr **Drög** í **Lokið**, ef skilgreiningarútgáfan inniheldur merki rafrænnar skýrslugerðar, þá eru þessi merki geymd í gagnagrunni forritsins. Geymsluskemað fer eftir stöðu á eiginleikanum **Hraða geymslu merkja rafrænnar skýrslugerðar**:

- Ef eiginleikinn er ekki virkur eru öll merki geymd í reitnum **LABELXML** í töflunni **ERSOLUTIONVERSIONTABLE** sem einn XML-bútur.
- Ef eiginleikinn er virkjaður er búin til aðskilin færsla fyrir hvert tungumál í töflunni **ERSOLUTIONVERSIONLASSESTABLE**. Reiturinn **EFNI** fyrir þessa töflu geymir merki fyrir hvert tungumál sem þjappaðan XML-bút.

Mælt er með því að virkja eiginleikann **Hraða geymslu á merkjum rafrænnar skýrslugerðar** á vinnusvæðinu **Eiginleikastjórnun**. Þessi eiginleiki hjálpar til við að bæta nýtingu bandvíddar netsins og heildarafköst kerfisins því að í flestum tilfellum eru merki rafrænnar skýrslugerðar notuð á einu tungumáli þegar unnið er með eina skilgreiningu rafrænnar skýrslugerðar.

Til að nota valið geymsluskema til að geyma merki allra skilgreininga rafrænnar skýrslugerðar í núverandi Finance-tilviki skal ljúka eftirfarandi skrefum.

1. Opnið **Fyrirtækisstjórnun** > **Reglubundið** > **Nota valið geymsluskema fyrir merki allra skilgreininga rafrænnar skýrslugerðar**.
2. Veldu **Í lagi**.


## <a name="additional-resources"></a>Frekari upplýsingar

- [Yfirlit yfir rafræna skýrslugerð](general-electronic-reporting.md)
- [Aðgerðir rafrænnar skýrslugerðar](er-formula-language.md#Functions)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
