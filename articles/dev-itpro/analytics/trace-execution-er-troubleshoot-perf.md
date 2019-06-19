---
title: Rekja framkvæmd á sniði rafrænnar skýrslugerðar til að úrræðaleita vandamál sem tengjast afköstum
description: Þetta efnisatriði veitir upplýsingar um hvernig á að nota eiginleika fyrir rakningu afkasta í rafrænni skýrslugerð til að úrræðaleita vandamál er varða afköst.
author: NickSelin
manager: AnnBe
ms.date: 05/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: aa71db2752889bc905c22bab1cf2fa46d7ee07c7
ms.sourcegitcommit: 67d00b95952faf0db580d341249d4e50be59119c
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1576547"
---
# <a name="trace-the-execution-of-er-formats-to-troubleshoot-performance-issues"></a>Rekja framkvæmd á sniðum rafrænnar skýrslugerðar til að úrræðaleita vandamál sem tengjast afköstum

[!include[banner](../includes/banner.md)]

Sem hluti af hönnunarferlinu fyrir skilgreiningar rafrænnar skýrslugerðar til að búa til rafræn skjöl, skilgreinir þú aðferðina sem er notuð til að ná í göng úr Microsoft Dynamics 365 for Finance and Operations og færa þau inn í úttak sem er myndað. Eiginleikinn fyrir rakningu á afköstum rafrænnar skýrslugerðar auðveldar að draga umtalsvert úr tíma og kostnaði sem eru hluti af því að safna saman upplýsingum um framkvæmd rafrænnar skýrslugerðar og nota þau til að úrræðaleita vandamál er varða afköst. Þessi leiðsögn veitir leiðbeiningar um hvernig á að gera rakningar á afköstum fyrir snið rafrænnar skýrslugerðar sem eru keyrð í Finance and Operations og hvernig á að nota upplýsingarnar úr þessum rakningum til að hjálpa til við að bæta afköst.

## <a name="prerequisites"></a>Forkröfur

Til að ljúka dæmunum í þessari leiðsögn þarftu að hafa eftirfarandi aðgang:

- Aðgangur að Finance and Operations fyrir eitt af eftirtöldum hlutverkum:

    - Þróunaraðili rafrænnar skýrslulausnar
    - Hagnýtur ráðgjafi vegna rafrænnar skýrslugerðar
    - Kerfisstjóri

- Aðgang að tilviki Skilgreiningarþjónustu reglugerðar (RCS) sem hefur verið úthlutað fyrir sama leigjandann og fyrir Finance and Operations, fyrir eitt af eftirfarandi hlutverkum:

    - Þróunaraðili rafrænnar skýrslulausnar
    - Hagnýtur ráðgjafi vegna rafrænnar skýrslugerðar
    - Kerfisstjóri

Einnig verður að sækja og geyma staðbundið eftirfarandi skrár.

| Skrá                                  | Efni                               |
|---------------------------------------|---------------------------------------|
| Afkastarakning model.version.1     | [Sýnishorn af skilgreiningu gagnalíkans rafrænnar skýrslugerðar](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)    |
| Afkastarakning metadata.version.1  | [Sýnishorn af skilgreiningu lýsigagna rafrænnar skýrslugerðar](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)      |
| Afkastarakning mapping.version.1.1 | [Sýnishorn af skilgreiningu líkanavörpunar rafrænnar skýrslugerðar](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| Afkastarakning format.version.1.1  | [Sýnishorn af skilgreiningu á sniði rafrænnar skýrslugerðar](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)       |

### <a name="configure-er-parameters"></a>Skilgreina færibreytur Rafræn skýrslugerðar

Hver afkastarakning rafrænnar skýrslugerðar sem er búin til í Finance and Operations er geymd sem viðhengi skráar fyrir aðgerðarskráningu. Rammi skjalastjórnunar í Finance and Operations er notað til að stjórna þessum viðhengjum. Skilgreina verður færibreytur rafrænnar skýrslugerðar fyrirfram til að tilgreina skjalagerð skjalastjórnunar sem á að nota til að hengja afkastarakningar við. Í Finance and Operation, á vinnusvæðinu **Rafræn skýrslugerð** skal velja **Færibreytur rafrænnar skýrslugerðar**. Síðan, á síðunni **Færibreytur rafrænnar skýrslugerðar**, í flipanum **Viðhengi**, í reitnum **Annað**, skal velja skjalagerð skjalastjórnunar til að nota fyrir afkastarakningar.

![Síða rafrænna skýrslufæribreyta í Finance and Operations](./media/GER-PerfTrace-GER-Parameters-DocumentType.png)

Til að vera tiltækt í uppflettingarreitnum **Annað** verður skjalagerð skjalastjórnunar að vera skilgreind á eftirfarandi hátt á síðunni **Skjalagerðir** (**Fyrirtækisstjórnun \> Skjalastjórnun \> Skjalagerðir**):

- **Klasi:** Hengja skrá við
- **Flokkur:** Skrá

![Síða skjalagerða í Finance and Operations](./media/GER-PerfTrace-DM-DocumentType.png)

> [!NOTE]
> Valin skjalagerð verður að vera tiltæk í öllum fyrirtækjum í núverandi tilviki Finance and Operations vegna þess að viðhengi skjalastjórnunar miðast við fyrirtæki.

### <a name="configure-rcs-parameters"></a>Skilgreina færibreytur RCS

Afkastarakningar rafrænnar skýrslugerðar sem eru myndaðar í Finance and Operations verða fluttar inn í RCS til greiningar með því að nota sniðshönnuð rafrænnar skýrslugerðar og hönnuð fyrir vörpun rafrænnar skýrslugerðar. Vegna þess að afkastarakningar rafrænnar skýrslugerðar eru geymdar sem viðhengi fyrir skrá aðgerðarskráningar sem tengist sniði rafrænnar skýrslugerðar er nauðsynlegt að skilgreina færibreytur RCS fyrirfram til að tilgreina skjalagerð skjalastjórnunar sem á að nota til að hengja afkastarakningar við. Í tilfelli RCS sem hefur verið úthlutað fyrir fyrirtækið þitt, á vinnusvæðinu **Rafræn skýrslugerð**, skal velja **Rafrænar skýrslugerðarfæribreytur**. Síðan, á síðunni **Færibreytur rafrænnar skýrslugerðar**, í flipanum **Viðhengi**, í reitnum **Annað**, skal velja skjalagerð skjalastjórnunar til að nota fyrir afkastarakningar.

![Síða rafrænna skýrslugerðarfæribreyta í RCS](./media/GER-PerfTrace-RCS-Parameters-DocumentType.png)

Til að vera tiltækt í uppflettingarreitnum **Annað** verður skjalagerð skjalastjórnunar að vera skilgreind á eftirfarandi hátt á síðunni **Skjalagerðir** (**Fyrirtækisstjórnun \> Skjalastjórnun \> Skjalagerðir**):

- **Klasi:** Hengja skrá við
- **Flokkur:** Skrá

## <a name="design-an-er-solution"></a>Hanna lausn rafrænnar skýrslugerðar

Gerum ráð fyrir að þú hafir byrjað að hanna nýja lausn rafrænnar skýrslugerðar til að búa til nýja skýrslu sem sýnir lánardrottnafærslur. Eins og er geturðu fundið færslurnar fyrir valinn lánardrottin á síðunni **Lánardrottnafærslur** (opnaðu **Viðskiptaskuldir \> Lánardrottnar \> Allir lánardrottnar**, veldu lánardrottin og síðan, í aðgerðarúðunni, í flipanum **Lánardrottinn**, í flokknum **Færslur**, skal velja **Færslur**). Hins vegar viltu hafa allar lánardrottnafærslur á sama tíma í einu rafrænu skjali á XML-sniði. Þessi lausn mun samanstanda af nokkrum skilgreiningum rafrænnar skýrslugerðar sem innihalda nauðsynlegt gagnalíkan, lýsigögn, líkanavörpun og sniðseiningar.

1. Skráðu þig inn á tilvik RCS sem hefur verið úthlutað fyrir fyrirtækið þitt.
2. Í þessari leiðsögn býrðu til og breytir skilgreiningum fyrir sýnifyrirtækið **Litware, Inc.**. Gakktu því úr skugga um að þessari skilgreiningarveitu hafi verið bætt við RCS og verið valin sem virk. Fyrir leiðbeiningar skal sjá ferlið [Stofna skilgreiningarveitendur og merkja þá sem virka](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11).
3. Á vinnusvæðinu **Rafræn skýrslugerð** skal velja reitinn **Skilgreiningar skýrslugerðar**.
4. Á síðunni **Skilgreiningar**, skal flytja inn skilgreiningar rafrænnar skýrslugerðar sem voru sóttar sem forkröfur í RCS, í eftirfarandi röð: gagnalíkan, lýsigögn, líkanavörpun, snið. Fyrir hverja skilgreiningu skal fylgja þessum skrefum:

    1. Í aðgerðarúðunni skal velja **Skipta út \> Hlaða úr XML-skrá**.
    2. Veljið **Vafra** til að velja viðeigandi skrá fyrir nauðsynlega skilgreiningu rafrænnar skýrslugerðar á XML-sniði.
    3. Veljið **Í lagi**.

    ![Skilgreiningarsíða í RCS](./media/GER-PerfTrace-RCS-ImportedConfigurations.png)

## <a name="run-the-er-solution-to-trace-execution"></a>Keyra lausn rafrænnar skýrslugerðar til að rekja framkvæmd

Gerum ráð fyrir að þú hafir lokið við að hanna fyrstu útgáfu af lausn rafrænnar skýrslugerðar. Núna viltu prófa hana í tilviki Finance and Operations og greina afköst keyrslu.

### <a id='import-configuration'></a>Flytja inn skilgreiningu rafrænnar skýrslugerðar úr RCS í Finance and Operations

1. Skráðu þig in í tilvik Finance and Operations.
2. Fyrir þessa leiðsögn flytur þú inn skilgreiningar úr RCS-tilvikinu þínu (þar sem þú hannar þætti rafrænnar skýrslugerðar) í tilvik Finance and Operations (þar sem þú prófar og að lokum notar þær). Þess vegna verður þú að ganga úr skugga um að allir nauðsynlegir gervingar hafi verið undirbúnir. Til að fá leiðbeiningar skal sjá ferlið [Flytja inn skilgreiningar rafrænnar skýrslugerðar úr Skilgreiningarþjónustu reglugerðar (RCS)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/analytics/rcs-download-configurations).
3. Fylgið þessum skrefum til að flytja inn skilgreiningar úr RCS í Finance and Operations:

    1. Á vinnusvæðinu **Rafræn skýrslugerð**, í reitnum fyrir skilgreiningarveituna **Litware, Inc.**, skal velja **Geymslur**.
    2. Á síðunni **Skilgreiningageymsla** skal velja geymslu af gerðinni **RCS** og síðan velja **Opna**.
    3. Í flýtiflipanum **Skilgreiningar** skal velja skilgreininguna **Snið afkastarakningar**.
    4. Í flýtiflipanum **Útgáfur** skal velja útgáfuna **1.1** af valdri skilgreiningu og síðan velja **Flytja inn**.

    ![Síða skilgreiningageymslu í Finance and Operations](./media/GER-PerfTrace-GER-ImportedConfigurations.png)

Samsvarandi útgáfur af skilgreiningum gagnalíkans og líkanavörpunar eru fluttar inn sjálfvirkt sem forkröfur fyrir innflutta skilgreiningu á sniði rafrænnar skýrslugerðar.

### <a name="turn-on-the-er-performance-trace"></a>Kveikja á afkastarakningu rafrænnar skýrslugerðar

1. Í Finance and Operations skal opna **Fyrirtækisstjórnun \> Rafræn skýrslugerð \> Skilgreiningar**.
2. Á síðunni **Skilgreiningar**, í aðgerðarúðunni, í flipanum **Skilgreiningar**, í flokknum **Ítarlegar stillingar**, skal velja **Færibreytur notanda**.
3. Í svarglugganum **Færibreytur notanda**, í hlutanum **Rakning keyrslu**, skal fylgja þessum skrefum:

    1. Í reitnum **Snið framkvæmdarakningar** skal velja **Kemba rakningasnið** til að byrja að safna saman upplýsingum um framkvæmd á sniði rafrænnar skýrslugerðar. Þegar þetta gildi er valið safnar afkastarakningin upplýsingum um tímann sem eftirfarandi aðgerðir taka:

        - Að keyra hvern gagnagjafa í líkanavörpuninni sem er kallað á til að ná í gögn
        - Úrvinnsla á öllum sniðsatriðum til að færa gögn inn í frálagið sem myndast

        Notaður er reiturinn **Snið framkvæmdarakningar** til að tilgreina snið fyrir myndaða afkastarakningu sem upplýsingar um framkvæmd eru geymdar í fyrir snið rafrænnar skýrslugerðar og einingar vörpunar. Með því að velja **Kemba sniðsrakningu** sem gildið geturðu greint innihald rakningarinnar í aðgerðarhönnuði rafrænnar skýrslugerðar og séð snið rafrænnar skýrslugerðar eða einingar vörpunar sem minnst er á í rakningunni.

    2. Stillið eftirfarandi valkosti á **Já** til að safna saman ákveðnum upplýsingum um framkvæmdina á líkanavörpun rafrænnar skýrslugerðar og sniðseiningum rafrænnar skýrslugerðar:

        - **Safna saman tölfræði um fyrirspurnir** - Þegar kveikt er á þessum valkosti safnar afkastarakningin saman eftirfarandi upplýsingum:

            - Fjölda gagnagrunnsköllum sem voru gerð eftir gagnaveitum
            - Fjölda afrita af köllum á gagnagrunninn
            - Upplýsingar um SQL-yrðingar sem voru notaðar til að gera gagnagrunnsköll

        - **Rekja aðgang að skyndiminni** - Þegar kveikt er á þessum valkosti safnar afkastarakningin saman upplýsingum um notkun á skyndiminni líkanavörpunar rafrænnar skýrslugerðar.
        - **Rekja gagnaaðgang** - Þegar kveikt er á þessum valkosti safnar afkastarakningin saman upplýsingum um fjölda kalla á gagnagrunninn fyrir framkvæmdar gagnaveitur af færslulistagerðinni.
        - **Rekja tölusetningarlista** - Þegar kveikt er á þessum valkosti safnar afkastarakningin saman upplýsingum um fjölda færslna sem gagnaveitur af færslulistagerðinni óska eftir.

    > [!NOTE]
    > Færibreyturnar í svarglugganum **Færibreytur notanda** eru sérstaklega fyrir notandann og núverandi fyrirtæki.

    ![Nota svarglugga færibreyta í Finance and Operations](./media/GER-PerfTrace-GER-UserParameters.png)

### <a id='run-format'></a>Keyra snið rafrænnar skýrslugerðar

1. Í Finance and Operations skal velja fyrirtækið **DEMF**.
2. Opnið **Fyrirtækisstjórnun \> Rafræn skýrslugerð \> Skilgreiningar**.
3. Á síðunni **Skilgreiningar**, í skilgreiningartrénu, skal velja atriðið **Snið afkastarakningar**.
4. Í aðgerðarúðunni skal velja **Keyra**.

Takið eftir að skráin sem er búin til veitir upplýsingar um 265 færslur fyrir sex lánardrottna.

## <a name="review-the-execution-trace"></a>Yfirfara framkvæmdarakningu

### <a id='export-trace'></a>Flytja út myndaða rakningu úr Finance and Operations

Afkastarakningar eru aftengdar frá upprunasniði rafrænnar skýrslugerðar og er hægt að númera við utanaðkomandi zip-skrá.

1. Í Finance and Operations skal opna **Fyrirtækisstjórnun \> Rafræn skýrslugerð \> Kembingarkladdar skilgreiningar**.
2. Á síðunni **Keyrslukladdar rafrænnar skýrslugjafar**, í vinstri rúðunni, í reitnum **Heiti skilgreiningar**, skal velja **Snið afkastarakningar** til að finna kladdafærslur sem framkvæmdin hefur búið til í skilgreiningunni **Snið afkastarakningar**.
3. Veljið hnappinn **Viðhengi** (bréfaklemmutáknið) efst í hægra horni síðunnar eða ýtið á **Ctrl+Shift+A**.

    ![Hnappur viðhengis í keyrslukladdasíðu rafrænnar skýrslugerðar í Finance and Operations](./media/GER-PerfTrace-GER-DebugLog.png)

4. Á síðunni **Viðhengi fyrir keyrslukladda rafrænnar skýrslugerðar**, í aðgerðarúðunni, skal velja **Opna** til að ná í afkastarakninguna sem zip-skrá og geyma hana staðbundið.

    ![Viðhengi fyrir keyrslukladdasíðu rafrænnar skýrslugerðar í Finance and Operations](./media/GER-PerfTrace-GER-DebugLog-AttachedTrace.png)

> [!NOTE]
> Rakningin sem er búin til er með tilvísun í upprunaskýrslu rafrænnar skýrslugerðar í gegnum einkvæmt kennimerki skýrslu aðeins á sniðinu **GUID**. Númeraúthlutun fyrir útgáfu sniðsins er ekki tekin með í reikninginn.

Takið eftir að tengingin milli afkastarakningar sem hefur verið búin til fyrir framkvæmt snið rafrænnar skýrslugerðar og líkanavörpun rafrænnar skýrslugerðar byggist á rótarlýsingu sem var notuð og algenga gagnalíkanið. Númeraúthlutun fyrir útgáfu sniðsins og líkanavörpunar eru ekki teknar með í reikninginn. Stillingin á flagginu **Sjálfgefið fyrir líkanavörpun** fyrir líkanavörpunina er einnig ekki tekin með í reikninginn.

### <a id='import-trace'></a>Flytja inn mynda rakningu í RCS

1. Í RCS, á vinnusvæðinu **Rafræn skýrslugerð**, skal velja reitinn **Skilgreiningar skýrslugerðar**.
2. Á síðunni **Skilgreiningar**, í skilgreiningartrénu, skal stækka atriðið **Líkan afkastarakningar** og velja atriðið **Snið afkastarakningar**.
3. Í aðgerðarúðunni skal velja **Hönnuður**.
4. Á síðunni **Sniðshönnuður**, í aðgerðarúðunni, skal velja **Afkastarakning**.
5. Í svarglugganum **Stillingar fyrir niðurstöðu afkastarakningar** skal velja **Flytja inn afkastarakningu**.
6. Veljið **Vafra** til að velja zip-skrána sem flutt var út úr Finance and Operations á undan.
7. Veljið **Í lagi**.

    ![Svargluggi stillinga fyrir niðurstöðu afkastarakningar í RCS](./media/GER-PerfTrace-RCS-ImportedPerfTrace.png)

### <a name="use-the-performance-trace-for-analysis-in-rcs--format-execution"></a>Nota afkastarakningu fyrir greiningu í RCS - framkvæmd sniðs

1. Í RCS, á síðunni **Sniðshönnuður**, skal velja **Stækka/fella saman** til að stækka efni allra sniðsatriða.

    Takið eftir að frekari upplýsingar eru sýndar fyrir sum atriði núverandi sniðs:

    - Raunverulegur tími sem fór í að færa gögn inn í myndað frálag með því að nota sniðsatriðið
    - Sami tími sýndur sem prósenta af heildartímanum sem fór í að búa til allt frálagið

    ![Síða sniðshönnuðar í RCS](./media/GER-PerfTrace-RCS-TraceInfoInFormat.png)

2. Lokaðu síðunni **Sniðshönnuður**.

### <a id='use-trace'></a>Nota afkastarakningu fyrir greiningu í RCS - Líkanavörpun

1. Í RCS, á síðunni **Skilgreiningar**, í skilgreiningartrénu, skal velja atriðið **Vörpun afkastarakningar**.
2. Í aðgerðarúðunni skal velja **Hönnuður**.
3. Veljið **Hönnuður**.
4. Á síðunni **Hönnuður líkanavörpunar**, í aðgerðarúðunni, skal velja **Afkastarakning**.
5. Veljið rakninguna sem var flutt inn áður.
6. Veljið **Í lagi**.

Takið eftir að nýjar upplýsingar verða tiltækar fyrir sum atriði gagnaveitu fyrir núverandi líkanavörpun:

- Raunverulegur tími sem fór í að ná í gögn með því að nota gagnagjafann
- Sami tími sýndur sem prósenta af heildartímanum sem fór í að keyra alla líkanavörpunina

Takið eftir því að rafræn skýrslugerð segir þér að núverandi líkanavörpun afritar beiðnir gagnagrunns á meðan VendTable/\<Relations/VendTrans.VendTable\_AccountNum gagnagjafi er keyrður. Þessi tvítekning á sér stað vegna þess að kallað er á listann yfir lánardrottnafærslur tvisvar sinnum fyrir hverja endurtekna lánardrottnafærslu:

- Eitt kall er framkvæmt til að færa upplýsingar um hverja færslu inn í gagnalíkanið, sem byggist á skilgreindum bindingum.
- Eitt kall er framkvæmt til að færa reiknaðan fjölda færslna á hvern lánardrottin inn í gagnalíkanið.

![Skilaboð um tvítekna gagnagrunnsbeiðni á hönnunarsíðu líkanavörpunar í RCS](./media/GER-PerfTrace-RCS-TraceInfoInMapping1.png)

Gildið **\[Q:530\]** gefur til kynna að kallað var á VendTrans-töfluna 530 sinnum til að skila færslu úr þeirri töflu yfir í VendTable/\<Relations/VendTrans.VendTable\_AccountNum gagnagjafann. Gildið **\[530\]** gefur til kynna að kallað var á VendTable/\<Relations/VendTrans.VendTable\_AccountNum gagnagjafann 530 sinnum til að skila færslu úr þeim gagnagjafa og færa inn upplýsingarnar úr henni inn í gagnalíkanið.

Við mælum með að þú notir vistun í skyndiminni fyrir VendTable/\<Relations/VendTrans.VendTable\_AccountNum gagnagjafann til að fækka fjölda kalla sem eru gerð til að ná í upplýsingar fyrir 265 færslur og hjálpa til við að bæta afköst líkanavörpunar.

Hún getur einnig verið gagnleg til að fækka fjölda kalla til LedgerTransTypeList gagnagjafann. Þessi gagnagjafi er notaður til að tengja hvert gildi tölusetningarinnar **LedgerTransType** við merkið sitt. Með því að nota þennan gagnagjafa geturðu fundið viðeigandi merki og fært það inn í gagnalíkanið fyrir hverja lánardrottnafærsla. Núverandi fjöldi kalla á þennan gagnagjafa (9027) er frekar hár fyrir 265 færslur.

![Hönnunarsíða líkanavörpunar í RCS sýnir 9027 köll á gagnagjafa](./media/GER-PerfTrace-RCS-TraceInfoInMapping1a.png)

## <a name="improve-the-model-mapping-based-on-information-from-the-execution-trace"></a>Bæta líkanavörpun á grundvelli upplýsinga úr framkvæmdarakningu

### <a name="modify-the-logic-of-the-model-mapping"></a>Breyta reiknireglu líkanavörpunar

1. Fylgið þessum skrefum til að nota vistun í skyndiminni, til að hjálpa til við koma í veg fyrir tvítekin köll á gagnagrunn:

    1. Í RCS, á síðunni **Hönnuður líkanavörpunar**, í rúðunni **Gagnagjafar**, skal velja atriðið **VendTable**.
    2. Veljið **Skyndiminni**.
    3. Stækkið atriðið **VendTable**, stækkið listann yfir einn í mörg tengsl fyrir VendTable gagnagjafann (atriðið **\<Tengsl**) og veljið atriðið **VendTrans.VendTable\_AccountNum**.
    4. Veljið **Skyndiminni**.

    ![Uppsetning á vistun í skyndiminni til að hjálpa til við að koma í veg fyrir tvítekin köll](./media/GER-PerfTrace-RCS-ChangeMapping-Cache.png)

2. Fylgið þessum skrefum til að færa LedgerTransTypeList gagnagjafann inn í umfang VendTable gagnagjafans:

    1. Í rúðunni **Gerðir gagnagjafa** skal stækka atriðið **Virknir** og velja atriðið **Reiknaður reitur**.
    2. Í rúðunni **Gagnagjafar** skal velja atriðið **VendTable**.
    3. Veljið **Bæta við**.
    4. Í reitinn **Heiti** skal færa inn **\$TransType**.
    5. Veljið **Breyta formúlu**.
    6. Í reitinn **Formúla** skal færa inn **LedgerTransTypeList**.
    7. Veljið **Vista**.
    8. Lokið síðunni **Formúluritill**.
    9. Smellt er á **OK**.

3. Fylgið þessum skrefum til að vista í skyndiminni á reitnum **\$TransType**:

    1. Veljið atriðið **LedgerTransTypeList**.
    2. Veljið **Skyndiminni**.
    3. Veljið atriðið **VendTable.\$TransType**.
    4. Veljið **Skyndiminni**.

    ![Uppsetning á vistun í skyndiminni fyrir reitinn $TransType](./media/GER-PerfTrace-RCS-ChangeMapping-Cache2.png)

4. Fylgið þessum skrefum til að breyta reitnum **\$TransTypeRecord** svo hann byrji að nota skyndiminni reitsins **\$TransType**:

    1. Í rúðunni **Gagnagjafar** skal stækka atriðið **VendTable**, stækka atriðið **\<Tengsl**, stækka atriðið **VendTrans.VendTable\_AccountNum** og velja atriðið **VendTable. VendTrans.VendTable\_AccountNum.\$TransTypeRecord**.
    2. Veljið **Breyta**.
    3. Veljið **Breyta formúlu**.
    4. Í reitnum **Formúla** skal finna eftirfarandi segð:

        FIRSTORNULL (WHERE (LedgerTransTypeList, LedgerTransTypeList.Enum = \@.TransType))

    5. Í reitnum **Formúla** skal færa inn eftirfarandi segð:

        FIRSTORNULL (WHERE (VendTable.'\$TransType', VendTable.'\$TransType'.Enum = \@.TransType)).

    6. Veljið **Vista**.
    7. Lokið síðunni **Formúluritill**.
    8. Veljið **Í lagi**.

5. Veljið **Vista**.
6. Lokið síðunni **Hönnuður líkanavörpunar**.
7. Lokið síðunni **Líkanavarpanir**.

### <a name="complete-the-modified-version-of-the-er-model-mapping"></a>Ljúka við breyttu útgáfuna af líkanavörpun rafrænnar skýrslugerðar

1. Í RCS, á síðunni **Skilgreiningar**, í flýtiflipanum **Útgáfur**, skal velja útgáfuna **1.2** af skilgreiningunni **Vörpun afkastarakningar**.
2. Veljið **Breyta stöðu**.
3. Velja **Lokið**.

### <a name="import-the-modified-er-model-mapping-configuration-from-rcs-into-finance-and-operations"></a>Flytja inn breytta skilgreiningu á líkanavörpun rafrænnar skýrslugerðar úr RCS í Finance and Operations

Endurtakið skrefin í hlutanum [Flytja inn skilgreiningu rafrænnar skýrslugerðar úr RCS í Finance and Operations](#import-configuration) fyrr í þessu efnisatriði til að flytja inn útgáfu 1.2 af skilgreiningunni **Vörpun afkastarakningar** í Finance and Operations.

## <a name="run-the-modified-er-solution-to-trace-execution"></a>Keyra breytta lausn rafrænnar skýrslugerðar til að rekja framkvæmd

### <a name="run-the-er-format"></a>Keyra snið rafrænnar skýrslugerðar

Endurtakið skrefin í hlutanum [Keyra snið rafrænnar skýrslugerðar](#run-format) fyrr í þessu efnisatriði til að búa til nýja afkastarakningu.

## <a name="review-the-execution-trace"></a>Yfirfara framkvæmdarakningu

### <a name="export-the-generated-trace-from-finance-and-operations"></a>Flytja út myndaða rakningu úr Finance and Operations

Endurtakið skrefin í hlutanum [Flytja út myndaða rakningu úr Finance and Operations](#export-trace) fyrr í þessu efnisatriði til að vista nýja afkastarakningu staðbundið.

### <a name="import-the-generated-trace-into-rcs"></a>Flytja inn myndaða rakningu í RCS

Endurtakið skrefin í hlutanum [Flytja inn myndaða rakningu í RCS](#import-trace) fyrr í þessu efnisatriði til að flytja inn nýja afkastarakningu í RCS.

### <a name="use-the-performance-trace-for-analysis-in-rcs--model-mapping"></a>Nota afkastarakningu fyrir greiningu í RCS - Líkanavörpun

Endurtakið skrefin í hlutanum [Nota afkastarakningu fyrir greiningu í RCS - Líkanavörpun](#use-trace) fyrr í þessu efnisatriði til að greina síðustu afkastarakningu.

Takiði eftir að leiðréttingar sem voru gerðar á líkanavörpun hafa eytt tvíteknum fyrirspurnum til gagnagrunns. Fjöldi kalla í gagnagrunnstöflur og gagnagjafa fyrir þessa líkanavörpun hefur einnig verið fækkað. Afköst á allri lausn rafrænnar skýrslugerðar hefur þar af leiðandi verið endurbætt.

![Rakningarupplýsingar fyrir VendTable gagnagjafann á hönnunarsíðu líkanavörpunar í RCS](./media/GER-PerfTrace-RCS-TraceInfoInMapping2.png)

Í rakningarupplýsingunum gefur gildið **\[12\]** fyrir VendTable gagnagjafa til kynna að kallað hafi verið á þennan gagnagjafa 12 sinnum. Gildið **\[Q:6\]** gefur til kynna að sex köll hafi verið þýdd yfir á gagnagrunnsköll til VendTable-töflunnar. Gildið **\[C:6\]** gefur til kynna að færslurnar sem voru sóttar úr gagnagrunninum hafi verið skyndiminni og unnið hafi verið úr sex öðrum köllum með því að nota skyndiminnið.

Athugið að fjöldi kalla á LedgerTransTypeList gagnagjafann hefur fækkað úr 9027 í 240.

![Rakningarupplýsingar fyrir LedgerTransTypeList gagnagjafann á hönnunarsíðu líkanavörpunar í RCS](./media/GER-PerfTrace-RCS-TraceInfoInMapping2a.png)

## <a name="review-the-execution-trace-in-finance-and-operations"></a>Yfirfara framkvæmdarakningu í Finance and Operations

Auk RCS kunna sumar útgáfur af Finance and Operations að bjóða upp á möguleika fyrir hönnunarupplifun á ramma rafrænnar skýrslugerðar. Þessar útgáfur af Finance and Operations eru með valkostinn **Virkja hönnunarsnið** sem hægt er að kveikja á. Hægt er að finna þennan valkost í flipanum **Almennt** á síðunni **Rafrænar skýrslugerðarfæribreytur** sem hægt er að opna úr vinnusvæðinu **Rafræn skýrslugerð**.

![Virkja valkost hönnunarsniðs á síðu rafrænna skýrslugerðarfæribreyta í Finance and Operations](./media/GER-PerfTrace-GER-Parameters-DesignMode.png)

Ef þú notar eina af þessum útgáfum af Finance and Operations geturðu greint upplýsingar á mynduðum afkastarakningum beint í Finance and Operations. Ekki þarf að flytja þær út úr Finance and Operation og flytja inn í RCS.

## <a name="review-the-execution-trace-by-using-external-tools"></a>Yfirfara framkvæmdarakningu með utanaðkomandi verkfærum

### <a name="configure-user-parameters"></a>Skilgreina færibreytur notanda

1. Í Finance and Operations skal opna **Fyrirtækisstjórnun \> Rafræn skýrslugerð \> Skilgreiningar**.
2. Á síðunni **Skilgreiningar**, í aðgerðarúðunni, í flipanum **Skilgreiningar**, í flokknum **Ítarlegar stillingar**, skal velja **Færibreytur notanda**.
3. Í svarglugganum **Færibreytur notanda**, í hlutanum **Rakning keyrslu**, í reitnum **Snið framkvæmdarakningar**, skal velja **Perfview XML**.

### <a name="run-the-er-format"></a>Keyra snið rafrænnar skýrslugerðar

Endurtakið skrefin í hlutanum [Keyra snið rafrænnar skýrslugerðar](#run-format) fyrr í þessu efnisatriði til að búa til nýja afkastarakningu.

Athugið að netvafrinn býður upp á zip-skrá fyrir niðurhal. Þessi skrá inniheldur afkastarakningu á PerfView-sniði. Síðan er hægt að nota greiningarverkfæri fyrir verkfæri PerfView-afkastagreiningar til að greina upplýsingarnar fyrir framkvæmd á sniði rafrænnar skýrslugerðar.