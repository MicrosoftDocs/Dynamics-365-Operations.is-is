---
title: Frestaðu framkvæmd raðarþátta á ER sniði
description: Þetta efni útskýrir hvernig á að fresta framkvæmd raðarþáttar á rafrænni skýrslugerð (ER) sniði.
author: NickSelin
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-07-01
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 19d1cf0aa6e9b40a0e72a3a74acda6e2579d6ee2
ms.sourcegitcommit: d5d6b81bd8b08de20cc018c2251436065982489e
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 02/17/2022
ms.locfileid: "8323691"
---
# <a name="defer-the-execution-of-sequence-elements-in-er-formats"></a>Frestaðu framkvæmd raðarþátta á ER sniði

[!include [banner](../includes/banner.md)]

## <a name="overview"></a>Yfirlit

Þú getur notað rekstrarhönnuðinn á [Rafræn skýrsla (ER)](general-electronic-reporting.md) ramma til [stilla](tasks/er-format-configuration-2016-11.md) sniðhluti ER lausnar sem er notaður til að búa til skjöl á útleið á textasniði. Stigveldi uppsetts sniðhlutans samanstendur af sniðþáttum af ýmsum gerðum. Þessir sniðþættir eru notaðir til að fylla mynda skjöl með tilskildum upplýsingum á keyrslutíma. Sjálfgefið að þegar þú keyrir ER-snið eru sniðþættirnir keyrðir í sömu röð og þeir eru settir fram í sniðveldinu: eitt af öðru, frá toppi til botns. Hins vegar er á hönnunartíma hægt að breyta framkvæmdaröð fyrir hvaða röð þætti í samstillta sniðihlutanum.

Með því að kveikja á valkostinum <a name="DeferredSequenceExecution"></a>**Frestuð framkvæmd** fyrir þáttaröð í röð sem er stillt á stillta sniði, þú getur frestað (frestað) framkvæmd þess þáttar. Í þessu tilfelli er þátturinn ekki keyrður fyrr en allir aðrir þættir yfirhluta hans hafa verið keyrðir.

Til að fá frekari upplýsingar um þennan eiginleika skaltu ljúka dæminu í þessu efni.

## <a name="limitations"></a>Takmarkanir

Valkosturinn **Frestuð framkvæmd** er aðeins studdur fyrir raðarþætti sem eru stilltir fyrir ER-snið sem er notað til að búa til skjöl **á útleið** á textasniði.

Valkosturinn **Frestuð framkvæmd** á ekki við um raðir sem hafa verið stilltar sem snyrtar raðir þar sem hámarkslengd er takmörkuð.

## <a name="example-defer-the-execution-of-a-sequence-element-in-an-er-format"></a><a name="Example"></a>Dæmi: Frestaðu framkvæmd raðarþáttar á ER-sniði

Eftirfarandi skref útskýra hvernig notandi í kerfisstjóra eða rafrænni skýrslugerð virkur ráðgjafi [hlutverk](../sysadmin/tasks/assign-users-security-roles.md) getur stillt ER snið sem inniheldur röð frumefnis þar sem framkvæmd röð er frábrugðin röðinni í snið stigveldisins.

Hægt er að framkvæma þessum skrefum í **USMF** fyrirtæki í Microsoft Dynamics 365 Finance.

### <a name="prerequisites"></a>Forkröfur

Til að ljúka þessu dæmi verður þú að hafa aðgang að **USMF** fyrirtæki í Finance fyrir eitt af eftirfarandi hlutverkum:

- Hagnýtur ráðgjafi vegna rafrænnar skýrslugerðar
- Kerfisstjóri

Ef þú hefur ekki enn lokið dæminu í [Frestaðu framkvæmd XML-þátta á ER sniði](er-defer-xml-element.md#Example) efni, hlaðið niður eftirfarandi [stillingar](general-electronic-reporting.md#Configuration) af ER lausninni.

| Lýsing á efni            | Skrárnafn |
|--------------------------------|-----------|
| Skilgreining á gagnalíkani í ER    | [Líkan til að læra frestaða elements.version.1.xml](https://download.microsoft.com/download/7/6/0/760933ca-4ac3-4f50-bc0c-c35e596ee066/Modeltolearndeferredelements.version.1.xml) |
| Stilling vörpunar ER-líkans | [Vörpun til að læra frestaða elements.version.1.1.xml](https://download.microsoft.com/download/c/9/c/c9c4b9dd-b700-4385-a087-a84ce9fc1d0f/Mappingtolearndeferredelements.version.1.1.xml) |

Áður en þú byrjar verður þú einnig að hlaða niður og vista eftirfarandi stillingar á sýnishornum ER lausnarinnar.

| Lýsing á efni     |Skrárnafn |
|-------------------------|----------|
| ER Sníða skilgreiningu | [Sniðmát til að læra frestaða sequences.version.1.1.xml](https://download.microsoft.com/download/0/f/5/0f55c341-8285-4d92-a46d-475d9a010927/Formattolearndeferredsequences.version.1.1.xml) |

### <a name="import-the-sample-er-configurations"></a>Flytja inn sýnishorn af ER-stillingum

1. Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.
2. Veldu **Skilgreiningar skýrslugerðar**.
3. Á síðunni **Stillingar**, ef stillingin **Líkan til að læra frestaða þætti** er ekki fáanleg í stillingatrénu, flytjið upp ER-gagnalíkanstillingar:

    1. Veldu **Skipta** og veldu síðan **Hlaða úr XML skrá**.
    2. Veldu **Fletta**, finndu og veldu skrána **Líkan til að læra frestaða þætti.1.xml** og veldu síðan **Í lagi**.

4. Ef stillingar **Vörpun til að læra frestaða þætti** er ekki fáanleg í stillingatrénu, flytjið upp vörpunarstillingar ER-gagnalíkans:

    1. Veldu **Skipta** og veldu síðan **Hlaða úr XML skrá**.
    2. Veldu **Fletta**, finndu og veldu skrána **Vörpun til að læra frestaða þætti.1.1.xml** og veldu síðan **Í lagi**.

5. Flytja inn skilgreiningu ER-sniðs:

    1. Veldu **Skipta** og veldu síðan **Hlaða úr XML skrá**.
    2. Veldu **Fletta**, finndu og veldu skrána **Snið til að læra frestaðar raðir.1.1.xml** og veldu síðan **Í lagi**.

6. Stækkaðu í stillingartrénu **Líkan til að læra frestaða þætti**.
7. Skoðaðu listann yfir innfluttar ER stillingar í stillingartrénu.

    ![Innfluttar ER grunnstillingar á skilgreiningasíðunni.](./media/ER-DeferredSequence-Configurations.png)

### <a name="activate-a-configurations-provider"></a>Kveikja á stillingaveitu

1. Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.
2. Á síðunni **Skilgreiningar staðsetningar**, í hlutanum **Skilgreiningaveitur**, skaltu passa að [skilgreiningaveitan](general-electronic-reporting.md#Provider) fyrir sýnifyrirtækið Litware, Inc. (`http://www.litware.com`) sé skráð og að hún sé merkt sem virk. Ef þessi stillingarþjónusta er ekki á listanum, eða ef hún er ekki merkt sem virk, fylgirðu skrefunum í efninu [Stofna skilgreiningaveitu og merkja hana sem virka](./tasks/er-configuration-provider-mark-it-active-2016-11.md).

    ![Litware, Inc. sýnifyrirtæki á skilgreiningasíðu staðfæringar.](./media/ER-DeferredSequence-ElectronicReportingWorkspace.png)

### <a name="review-the-imported-model-mapping"></a>Yfirfara innflutta líkanavörpun

Skoðaðu stillingar kortagerðarhlutans fyrir ER-gerðina sem er stilltur til að fá aðgang að skattafærslum og afhjúpa aðgengileg gögn ef óskað er.

1. Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.
2. Veldu **Skilgreiningar skýrslugerðar**.
3. Á síðunni **Stillingar** í stillingatrénu stækkarðu **Líkan til að læra frestuðum þætti**.
4. Veldu stillingarnar **Vörpun til að læra frestuðum þáttum**.
5. Veldu **Hönnuður** til að opna lista yfir varpanir.
6. Veldu **Hönnuður** til að fara yfir upplýsingar um varpanir.
7. Veljið **Sýna upplýsingar**.
8. Skoðaðu gagnagjafana sem eru stilltir til að fá aðgang að skattafærslum:

    - Gagnagjafinn **Færslur** af gerðinni *Töfluskrá* er stillt til að fá aðgang að skrám forritstöflunnar **TaxTrans**.
    - Gagnagjafinn **Fylgiskjöl** af gerðinni *Reiknaður reitur* er stilltur til að skila tilskildum kóðum fylgiskjala (**INV-10000349** og **INV-10000350**) sem lista yfir skrár.
    - Gagnagjafinn **Síað** af gerðinni *Reiknaður reitur* er stilltur til að velja, úr gagnagjafanum **Færslur**, aðeins skattafærslur í nauðsynlegum fylgiskjölum.
    - Reitnum **\$TaxAmount** af gerðinni *Reiknaður reitur* er bætt við fyrir gagnagjafann **Síað** til að afhjúpa skattagildi sem hefur hið gagnstæða merki.
    - Gagnagjafinn **Hópað** af gerðinni *Hópa eftir* er stillt til að flokka síaðar skattafærslur í gagnagjafanum **Síað**.
    - Uppsöfnunarreiturinn **TotalSum** í gagnagjafanum **Hópað** er stilltur til að draga saman gildi í reitnum **\$TaxAmount** í gagnagjafanum **Síað** fyrir allar síaðar skattafærslur þess gagnagjafa.

        ![Uppsöfnunarreiturinn TotalSum á færibreytusíðunni Breyta „GroupBy“.](./media/ER-DeferredSequence-GroupByParameters.png)

9. Skoðaðu hvernig stilltir gagnagjafar eru bundnir við gagnalíkanið og hvernig þeir afhjúpa aðgangsgögn til að gera þau aðgengileg á ER sniði:

    - Gagnagjafinn **Síað** er bundinn við reitinn **Data.List** í gagnalíkaninu.
    - Reiturinn **\$TaxAmount** í gagnagjafanum **Síað** er bundinn við reitinn **Data.List.Value** í gagnalíkaninu.
    - Reiturinn **TotalSum** í gagnagjafanum **Hópað** er bundinn við reitinn **Data.Summary.Total** í gagnalíkaninu.

    ![Hönnuðarsíða líkanavörpunar.](./media/ER-DeferredSequence-ModelMapping.png)

10. Lokaðu síðunum **Hönnuður líkanavörpunar** og **Líkanavarpanir**.

### <a name="review-the-imported-format"></a>Yfirfara innflutt snið

1. Á síðunni **Stillingar** í stillingatrénu, velurðu stillingarnar **Snið til að læra frestuðum röðum**.
2. Veldu **Hönnuður** til að fara yfir upplýsingar um sniðmát.
3. Veljið **Sýna upplýsingar**.
4. Skoðaðu stillingar á ER sniði íhlutum sem eru stilltir til að búa til útgagnaskjal á textasniði sem inniheldur upplýsingar um skattaviðskipti:

    - Þáttur raðsniðmáts **Skýrsla\\Línur** er stilltur til að fylla skjalið á útleið með einni línu sem er búin til úr ívöfðum raðþáttum (**Haus**, **Skrá** og **Yfirlit**).

        ![Sniðseining og faldaðar einingar línuraða á sniðshönnunarsíðunni.](./media/ER-DeferredSequence-Format.png)

    - Þáttur raðsniðmáts **Skýrsla\\Línur\\Haus** er stilltur til að fylla skjalið á útleið með stakri hauslínu sem sýnir dagsetningu og tíma þegar vinnsla hefst.
    - Þáttur raðsniðmáts **Skýrsla \\Línur\\Skrá** er stilltur til að fylla skjalið á útleið með stakri línu sem sýnir upplýsingar um stakar skattafærslur. Þessar skattafærslur eru aðgreindar með semíkommu.

        ![Sniðseining færsluraðar sem notar semíkommu sem skiltákn.](./media/ER-DeferredSequence-Format1.png)

    - Þáttur raðsniðmáts **Skýrsla\\Línur\\Yfirlit** er stilltur til að fylla skjalið á útleið með einni yfirlitslínu sem inniheldur summan af skattagildunum úr unnum skattafærslum.

4. Á flipanum **Vörðun** skoðarðu eftirfarandi upplýsingar:

    - Þátturinn **Skýrsla\\Línur\\Haus** þarf ekki að vera bundið við gagnagjafa til að búa til einn línu í skjali sem er á útleið.
    - Þátturinn **Prefix1** myndar **P1**-tákn til að gefa til kynna að línan sem er bætt við sé hauslínan á skýrslunni.
    - Þátturinn **ExecutionDateTime** myndar dagsetningu og tíma (þ.m.t. millisekúndur) þegar hauslínunni er bætt við.
    - Þátturinn **Skýrsla\\Línur\\Skrá** er bundinn við listann **model.Data.List** til að mynda staka línu fyrir hverja skrá af bundna listanum.
    - Þátturinn **Prefix2** myndar **P2**-tákn til að gefa til kynna að línan sem er bætt við sé fyrir upplýsingar skattafærslu.
    - Þátturinn **TaxAmount** er bundin við **model.Data.List.Value** (sem er sýnt sem **\@.Value** í sýn tengdrar slóðar) til að búa til skattverðmæti núverandi skattafærslna.
    - Þátturinn **RunningTotal** er staðgengill fyrir hlaupandi samtölu skattagilda. Sem stendur hefur þessi þáttur ekkert úttak, því hvorki bindandi né sjálfgefið gildi er stillt fyrir það.
    - Þátturinn **ExecutionDateTime** myndar dagsetningu og tíma (þ.m.t. millisekúndur) þegar núverandi færsla er unnin í þessari skýrslu.
    - Þátturinn **Skýrsla\\Línur\\Yfirlit** þarf ekki að vera bundið við gagnagjafa til að búa til einn línu í skjali sem er á útleið.
    - Þátturinn **Prefix3** myndar **P3**-tákn til að gefa til kynna að línan sem er bætt við innihaldi samtals skattagildi.
    - Þátturinn **TotalTaxAmount** er bundinn við **model.Data.Summary.Total** til að mynda summuna af skattagildum á unnum skattafærslum.
    - Þátturinn **ExecutionDateTime** myndar dagsetningu og tíma (þ.m.t. millisekúndur) þegar yfirlitslínunni er bætt við.

    ![Vörpunarflipi á sniðshönnunarsíðunni.](./media/ER-DeferredSequence-Format2.png)

### <a name="run-the-imported-format"></a>Keyrðu innflutta sniðið

1. Á síðunni **Sniðshönnuður** skal velja **Keyra**.
2. Sæktu skrána sem vefskoðarinn býður upp á og opnaðu hana til skoðunar.

    ![Sótt skrá sýniskýrslu.](./media/ER-DeferredSequence-Run.png)

Taktu eftir að yfirlitslína 22 sýnir summuna af skattagildum fyrir unnar færslur. Vegna þess að sniðið er stillt til að nota **model.Data.Summary.Total** bindandi til að skila þessari fjárhæð, er summan reiknuð með því að kalla í uppsöfnunina **TotalSum** á gagnagjafann **Flokkað** af gerðinni *GroupBy* sem notar líkanavörpunina. Til að reikna þessa uppsöfnun endurtekur líkanavörpunin yfir allar færslur sem hafa verið valdar í gagnagjafanum **Síað**. Með því að bera saman framkvæmdartíma línanna 21 og 22 er hægt að ákvarða að útreikningur á summan hafi tekið 10 millisekúndur (ms). Með því að bera saman framkvæmdartíma línanna 2 og 21 er hægt að ákvarða að myndun á öllum færslulínum taki 7 ms. Þess vegna var krafist alls 17 ms.

### <a name="modify-the-format-so-that-the-summing-is-based-on-generated-output"></a>Breyttu sniði þannig að samlagningin byggist á mynduðu úttaki

Ef magn færslna er miklu stærra en rúmmálið í núverandi dæmi gæti samlagningartíminn aukist og valdið afkomuvandamálum. Með því að breyta stillingum sniðsins geturðu hjálpað til við að koma í veg fyrir þessi frammistöðuvandamál. Vegna þess að þú hefur aðgang að skattagildum til að fela þau í skýrsluna sem myndað er, getur þú notað þessar upplýsingar til að leggja saman skattgildi. Fyrir frekari upplýsingar, sjá [Stilla snið til að gera talningu og samlagningu](./tasks/er-format-counting-summing-1.md).

1. Á síðunni **Sniðmátshönnuður**, á flipanum **Snið**, veldu skráarþáttinn **Skýrsla** í sniðmátstrénu.
2. Stilltu valkostinn **Safna saman úttaksupplýsingum** á **Já**. Þú getur nú stillt þetta snið með því að nota innihald fyrirliggjandi skýrslu sem gagnagjafinn sem hægt er að nálgast með því að nota innbyggðu ER aðgerðirnar í flokknum [Gagnasafn](er-functions-category-data-collection.md).
3. Á flipanum **Vörpun** velurðu raðþáttinn **Skýrsla\\Línur**.
4. Stilltu segðina **Heiti lykils fyrir söfnuð gögn** sem `WsColumn`.
5. Stilltu segðina **Gildi lykils fyrir söfnuð gögn** sem `WsRow`.

    ![Eining línuraðar á síðu sniðshönnuðar.](./media/ER-DeferredSequence-Format3.png)

6. Veldu tölugildið **Report\\Lines\\Record\\TaxAmount**.
7. Stilltu segðina **Heiti lykils fyrir söfnuð gögn** sem `SummingAmountKey`.

    ![Tölustafaeining TaxAmount á síðu sniðshönnuðar.](./media/ER-DeferredSequence-Format4.png)

    Þú getur íhugað þessa stillingu efndir á sýndarverkefnisblaði, þar sem verðmæti hólfs A1 er bætt við verðmæti skattafjárhæðarinnar frá hverri afgreiddri skattafærslu.

8. Veldu töluþáttinn **Skýrsla\\Línur\\Skrá\\RunningTotal** og veldu síðan **Breyta formúlu**.
9. Stilltu segðina `SUMIF(SummingAmountKey, WsColumn, WsRow)` með því að nota innbyggða [SUMIF](er-functions-datacollection-sumif.md) ER-aðgerð.
10. Veldu **Vista**.

    ![SUMIF-segð.](./media/ER-DeferredSequence-FormulaDesigner.png)

11. Lokaðu síðunni **Formúluhönnuður**.
12. Veldu **Vista** og síðan **Keyra**.
13. Sæktu og farðu yfir skrána sem vefskoðarinn býður upp á og opnaðu hana til skoðunar.

    ![Sótt skrá - Samanlögð skattagildi.](./media/ER-DeferredSequence-Run1.png)

    Lína 21 inniheldur hlaupandi samtölu skattagilda sem eru reiknuð fyrir öll afgreidd viðskipti með því að nota myndaða framleiðsluna sem gagnagjafa. Þessi gagnagjafi hefst á byrjun skýrslunnar og heldur áfram í gegnum síðustu skattafærslu. Lína 22 inniheldur summan af skattagildum fyrir allar unnar færslur sem eru reiknaðar út í líkanavörpun með því að nota gagnagjafa af gerðinni *GroupBy*. Taktu eftir að þessi gildi eru jöfn. Þess vegna er hægt að nota samlagningu sem byggir á úttaki í staðinn fyrir **GroupBy**. Með því að bera saman framkvæmdartíma línanna 2 og 21 er hægt að ákvarða að myndun á öllum færslulínum og samlagningu taki 9 ms. Þess vegna er breytta sniðið um það bil tvisvar sinnum hraðara en upprunalega sniðið varðandi myndun sundurliðaðra lína og summan af skattagildum.

14. Veldu töluþáttinn **Skýrsla\\Línur\\Yfirlit\\TotalTaxAmount** og veldu síðan **Breyta formúlu**.
15. Sláðu inn segðina `SUMIF(SummingAmountKey, WsColumn, WsRow)` í stað núverandi segðar.
16. Veldu **Vista** og síðan **Keyra**.
17. Sæktu og farðu yfir skrána sem vefskoðarinn býður upp á og opnaðu hana til skoðunar.

    ![Skrá sótt með breyttri formúlu.](./media/ER-DeferredSequence-Run2.png)

    Taktu eftir því að hlaupandi samtala skattagilda í síðustu upplýsingalínu færslu er nú jafnhá samtölu yfirlitslínunnar.

### <a name="put-values-of-output-based-summing-in-the-report-header"></a>Settu gildi framleiðslutengdrar summunar í haus skýrslunnar

Ef þú til dæmis verður að setja summan af skattagildum í haus skýrslunnar geturðu breytt sniði þínu.

1. Á síðunni **Sniðmátshönnuður**, á flipanum **Snið**, veldu raðþáttinn **Skýrsla\\Línur\\Yfirlit**.
2. Veldu **Færa upp**.
3. Veldu **Vista** og síðan **Keyra**.
4. Sæktu og farðu yfir skrána sem vefskoðarinn býður upp á og opnaðu hana til skoðunar.

    ![Skrá sótt fyrir samtölu í skýrsluhaus.](./media/ER-DeferredSequence-Run3.png)

    Taktu eftir að summan af skattagildum í yfirlitslínu 2 er nú jöfn 0 (núll), vegna þess að þessi summa er nú reiknuð út frá mynduðu úttaki. Þegar lína 2 er mynduð inniheldur myndað úttak ekki enn línur sem hafa upplýsingar um færslur. Þú getur stillt þetta snið til að fresta framkvæmd á raðþættinum **Skýrsla\\Línur\\Yfirlit** þar til að raðþátturinn **Skýrsla\\Línur\\Skrá** hefur verið keyrður fyrir allar skattafærslur.

### <a name="defer-the-execution-of-the-summary-sequence-so-that-the-calculated-total-is-used"></a>Frestaðu framkvæmd samantektar raðþáttarins þannig að reiknuð samtala sé notuð

1. Á síðunni **Sniðmátshönnuður**, á flipanum **Snið**, veldu raðþáttinn **Skýrsla\\Línur\\Yfirlit**.
2. Stillið valkostinn **Frestuð framkvæmd** á **Já**.

    ![Valkostur frestaðrar framkvæmdar á einingu samantektarraðar á síðu sniðshönnuðar.](./media/ER-DeferredSequence-Format5.png)

3. Veldu **Vista** og síðan **Keyra**.
4. Sæktu og farðu yfir skrána sem vefskoðarinn býður upp á og opnaðu hana til skoðunar.

    ![Skrá sótt - frestuð framkvæmd.](./media/ER-DeferredSequence-Run4.png)

    Raðþátturinn **Skýrsla\\Línur\\Yfirlit** er nú aðeins keyrður þegar allir aðrir hlutir sem eru ívafðir undir yfirþættinum **Skýrsla\\Línur** hafa verið keyrðir. Þess vegna er hann keyrður þegar raðþátturinn **Skýrsla\\Línur\\Skrá** hefur verið keyrður fyrir allar skattafærslur í gagnagjafanum **model.Data.List**. Framkvæmdartímar lína 1, 2 og 3 og síðustu línunnar, 22, sýna þessa staðreynd.

## <a name="additional-resources"></a>Frekari upplýsingar

- [Skilgreina snið til að gera talningu og samlagningu](./tasks/er-format-counting-summing-1.md)
- [Rekja framkvæmd á sniði rafrænnar skýrslugerðar til að úrræðaleita vandamál sem tengjast afköstum](trace-execution-er-troubleshoot-perf.md)
- [Frestaðu framkvæmd XML-þátta á ER sniði](er-defer-xml-element.md#Example)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
