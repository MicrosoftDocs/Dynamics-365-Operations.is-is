---
title: Fresta keyrslu XML-eininga á sniði rafrænnar skýrslugerðar
description: Þessi grein útskýrir hvernig á að fresta framkvæmd XML þáttar á rafrænu skýrslusniði (ER).
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
ms.search.validFrom: 2020-01-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 074b14cbb018a8e34b99124b8aaec3a5bdb30be2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8861846"
---
# <a name="defer-the-execution-of-xml-elements-in-er-formats"></a>Frestaðu framkvæmd XML-þátta á ER sniði

[!include [banner](../includes/banner.md)]

## <a name="overview"></a>Yfirlit

Þú getur notað rekstrarhönnuðinn á [Rafræn skýrslugerð (ER)](general-electronic-reporting.md) ramma til [stilla](./tasks/er-format-configuration-2016-11.md) sniðþáttur ER lausnar sem er notaður til að búa til skjöl á útleið á XML sniði. Stigveldi uppsetts sniðhlutans samanstendur af sniðþáttum af ýmsum gerðum. Þessir sniðþættir eru notaðir til að fylla mynda skjöl með tilskildum upplýsingum á keyrslutíma. Sjálfgefið að þegar þú keyrir ER-snið eru sniðþættirnir keyrðir í sömu röð og þeir eru settir fram í sniðveldinu: eitt af öðru, frá toppi til botns. Hins vegar er á hönnunartíma hægt að breyta framkvæmdaröðuninni fyrir hvaða XML-þætti sem er í samskiptahlutanum.

Með því að kveikja á valkostinum <a name="DeferredXmlElementExecution"></a>**Frestuð framkvæmd** fyrir XML-þátt í röð sem er stillt á stillta sniði, þú getur frestað (frestað) framkvæmd þess þáttar. Í þessu tilfelli er þátturinn ekki keyrður fyrr en allir aðrir þættir yfirhluta hans hafa verið keyrðir.

Til að læra meira um þennan eiginleika skaltu klára dæmið í þessari grein.

## <a name="limitations"></a>Takmarkanir

Valkosturinn **Frestuð framkvæmd** er aðeins studdur fyrir XML-þætti sem eru stilltir fyrir ER-snið sem er notað til að búa til skjöl **á útleið** á XML-sniði.

Valkosturinn **Frestuð framkvæmd** er aðeins studdur fyrir XML þætti sem eru aðeins í einum öðrum XML frumefni. Þess vegna gildir það ekki um XML þætti sem eru búsettir í öðrum gerðum sniðaþátta (til dæmis í þættinum **XML-röð**).

Valkosturinn **Frestuð framkvæmd** er ekki studdur fyrir XML þætti sem búa í sniðmátsþáttunum **Sameiginlegt\\Skrá** þegar valkosturinn **Skipta skrá** er stilltur á **Já**. Nánari upplýsingar um hvernig á að skipta XML-skrám er að finna í [Skipta mynduðum XML-skrám út frá stærð og efnismagni](er-split-files.md).

## <a name="example-defer-the-execution-of-an-xml-element-in-an-er-format"></a><a name="Example"></a>Dæmi: Frestaðu framkvæmd XML-þáttar á ER-sniði

Eftirfarandi skref útskýra hvernig notandi í kerfisstjóra eða rafrænni skýrslugerð virkur ráðgjafi [hlutverk](../sysadmin/tasks/assign-users-security-roles.md) getur stillt ER snið sem inniheldur XML-þátt þar sem framkvæmd röð er frábrugðin röðinni í snið stigveldisins.

Þessi skref er hægt að framkvæma í **USMF** fyrirtæki í Microsoft Dynamics 365 Fjármál.

### <a name="prerequisites"></a>Forkröfur

Til að ljúka þessu dæmi verður þú að hafa aðgang að **USMF** fyrirtæki í Finance fyrir eitt af eftirfarandi hlutverkum:

- Hagnýtur ráðgjafi vegna rafrænnar skýrslugerðar
- Kerfisstjóri

Ef þú hefur ekki enn lokið við dæmið í [Fresta framkvæmd röð þátta í ER sniðum](er-defer-sequence-element.md#Example) grein, hlaðið niður eftirfarandi [stillingar](general-electronic-reporting.md#Configuration) af ER-sýnislausninni.

| Lýsing á efni            | Skrárnafn |
|--------------------------------|-----------|
| Skilgreining á gagnalíkani í ER    | [Líkan til að læra frestaða elements.version.1.xml](https://download.microsoft.com/download/7/6/0/760933ca-4ac3-4f50-bc0c-c35e596ee066/Modeltolearndeferredelements.version.1.xml) |
| Stilling vörpunar ER-líkans | [Vörpun til að læra frestaða elements.version.1.1.xml](https://download.microsoft.com/download/c/9/c/c9c4b9dd-b700-4385-a087-a84ce9fc1d0f/Mappingtolearndeferredelements.version.1.1.xml) |

Áður en þú byrjar verður þú einnig að hlaða niður og vista eftirfarandi stillingar á sýnishornum ER lausnarinnar á tölvuna þína.

| Lýsing á efni     | Skrárnafn |
|-------------------------|-----------|
| ER Sníða skilgreiningu | [Sniðmát til að læra frestaða XML elements.version.1.1.xml](https://download.microsoft.com/download/4/7/8/478fa846-22e9-4fa0-89b1-d3aeae660067/FormattolearndeferredXMLelements.version.1.1.xml) |

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
    2. Veldu **Fletta**, finndu og veldu skrána **Snið til að læra frestaða XML-þætti.1.1.xml** og veldu síðan **Í lagi**.

6. Stækkaðu í stillingartrénu **Líkan til að læra frestaða þætti**.
7. Skoðaðu listann yfir innfluttar ER stillingar í stillingartrénu.

    ![Innfluttar ER grunnstillingar á skilgreiningasíðunni.](./media/ER-DeferredXml-Configurations.png)

### <a name="activate-a-configuration-provider"></a>Kveikja á stillingaveitu

1. Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.
2. Á síðunni **Skilgreiningar staðsetningar**, í hlutanum **Skilgreiningaveitur**, skaltu passa að [skilgreiningaveitan](general-electronic-reporting.md#Provider) fyrir sýnifyrirtækið Litware, Inc. (`http://www.litware.com`) sé skráð og að hún sé merkt sem virk. Ef þessi stillingarveita er ekki á listanum eða ef hún er ekki merkt sem virk skaltu fylgja skrefunum í [Búðu til stillingarveitu og merktu hana sem virka](./tasks/er-configuration-provider-mark-it-active-2016-11.md) grein.

    ![Litware, Inc. sýnifyrirtæki á skilgreiningasíðu staðfæringar.](./media/ER-DeferredXml-ElectronicReportingWorkspace.png)

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

        ![Uppsöfnunarreiturinn TotalSum á færibreytusíðunni Breyta „GroupBy“.](./media/ER-DeferredXml-GroupByParameters.png)

9. Skoðaðu hvernig stilltir gagnagjafar eru bundnir við gagnalíkanið og hvernig þeir afhjúpa aðgangsgögn til að gera þau aðgengileg á ER sniði:

    - Gagnagjafinn **Síað** er bundinn við reitinn **Data.List** í gagnalíkaninu.
    - Reiturinn **\$TaxAmount** í gagnagjafanum **Síað** er bundinn við reitinn **Data.List.Value** í gagnalíkaninu.
    - Reiturinn **TotalSum** í gagnagjafanum **Hópað** er bundinn við reitinn **Data.Summary.Total** í gagnalíkaninu.

    ![Hönnuðarsíða líkanavörpunar.](./media/ER-DeferredXml-ModelMapping.png)

10. Lokaðu síðunum **Hönnuður líkanavörpunar** og **Líkanavarpanir**.

### <a name="review-the-imported-format"></a>Yfirfara innflutt snið

1. Á síðunni **Stillingar** í stillingatrénu, velurðu stillingarnar **Snið til að læra frestuðum XML þætti**.
2. Veldu **Hönnuður** til að fara yfir upplýsingar um sniðmát.
3. Veljið **Sýna upplýsingar**.
4. Skoðaðu stillingar á ER sniði íhlutum sem eru stilltir til að búa til útgagnaskjal á XML sniði sem inniheldur upplýsingar um skattaviðskipti:

    - XML-þátturinn **Skýrsla\\Skilaboð** er stilltur til að fylla útleið skjals með einum hnút sem inniheldur ívafða XML-þætti (**Haus**, **Skrá** og **Yfirlit**).
    - XML-þátturinn **Skýrsla\\Skilaboð\\Haus** er stilltur til að fylla skjalið á útleið með einum haushnút sem sýnir dagsetningu og tíma þegar vinnsla hefst.
    - XML-þátturinn **Skýrsla \\Skilaboð\\Skrá** er stilltur til að fylla skjalið á útleið með einum skráarhnút sem sýnir upplýsingar um staka skattafærslu.
    - XML-þátturinn **Skýrsla\\Skilaboð\\Yfirlit** er stilltur til að fylla skjalið á útleið með einum yfirlitshnút sem inniheldur summan af skattagildunum úr unnum skattafærslum.

    ![Senda skilaboð til XML-einingar og faldaðrar XML-einingar á sniðshönnunarsíðunni.](./media/ER-DeferredXml-Format.png)

5. Á flipanum **Vörðun** skoðarðu eftirfarandi upplýsingar:

    - Þátturinn **Skýrsla\\Skilaboð\\Haus** þarf ekki að vera bundið við heimild til að búa til einn hnút í skjali sem er á útleið.
    - Eigindin **ExecutionDateTime** myndar dagsetningu og tíma (þ.m.t. millisekúndur) þegar haushnútnum er bætt við.
    - Þátturinn **Skýrsla\\Skilaboð\\Skrá** er bundinn við listann **model.Data.List** til að mynda stakan skráarhnút fyrir hverja skrá af bundna listanum.
    - Eigindin **TaxAmount** er bundin við **model.Data.List.Value** (sem er sýnt sem **\@.Value** í sýn tengdrar slóðar) til að búa til skattverðmæti núverandi skattafærslna.
    - Eigindin **RunningTotal** er staðgengill fyrir hlaupandi samtölu skattagilda. Sem stendur hefur þessi eigind ekkert úttak, því hvorki bindandi né sjálfgefið gildi er stillt fyrir það.
    - Eigindin **ExecutionDateTime** myndar dagsetningu og tíma (þ.m.t. millisekúndur) þegar núverandi færsla er unnin í þessari skýrslu.
    - Þátturinn **Skýrsla\\Skilaboð\\Yfirlit** þarf ekki að vera bundið við gagnagjafa til að búa til einn hnút í skjali sem er á útleið.
    - Eigindin **TotalTaxAmount** er bundin við **model.Data.Summary.Total** til að mynda summuna af skattagildum á unnum skattafærslum.
    - Eigindin **ExecutionDateTime** myndar dagsetningu og tíma (þ.m.t. millisekúndur) þegar yfirlitshnútnum er bætt við.

    ![Vörpunarflipi á sniðshönnunarsíðunni.](./media/ER-DeferredXml-Format2.png)

### <a name="run-the-imported-format"></a>Keyrðu innflutta sniðið

1. Á síðunni **Sniðshönnuður** skal velja **Keyra**.
2. Sæktu skrána sem vefskoðarinn býður upp á og opnaðu hana til skoðunar.

    ![Skrá yfir innflutt snið sótt.](./media/ER-DeferredXml-Run.png)

Taktu eftir að yfirlitshnúturinn sýnir summan af skattagildum fyrir unnar færslur. Vegna þess að sniðið er stillt til að nota **model.Data.Summary.Total** bindandi til að skila þessari fjárhæð, er summan reiknuð með því að kalla í uppsöfnunina **TotalSum** á gagnagjafann **Flokkað** af gerðinni *GroupBy* í líkanavörpuninni. Til að reikna þessa uppsöfnun endurtekur líkanavörpunin yfir allar færslur sem hafa verið valdar í gagnagjafanum **Síað**. Með því að bera saman framkvæmdartíma yfirlitshnútsins og síðasta skráningarhnút geturðu ákvarðað að útreikningur á summan tók 12 millisekúndur (ms). Með því að bera saman framkvæmdatíma fyrsta og síðasta skrána hnút, getur þú ákvarðað að kynslóð allra skránna hafi tekið 9 ms. Þess vegna var krafist alls 21 ms.

### <a name="modify-the-format-so-that-the-calculation-is-based-on-generated-output"></a>Breyttu sniði þannig að útreikningurinn byggist á mynduðum framleiðsla

Ef magn viðskipta er miklu stærra en rúmmálið í núverandi dæmi gæti útreikningstíminn aukist og valdið afkomuvandamálum. Með því að breyta stillingum sniðsins geturðu hjálpað til við að koma í veg fyrir þessi frammistöðuvandamál. Vegna þess að þú hefur aðgang að skattagildum til að fela þau í skýrsluna sem myndað er, getur þú notað þessar upplýsingar til að reikna út skattgildi. Fyrir frekari upplýsingar, sjá [Stilla snið til að gera talningu og samlagningu](./tasks/er-format-counting-summing-1.md).

1. Á síðunni **Sniðmátshönnuður**, á flipanum **Snið**, veldu skráarþáttinn **Skýrsla** í sniðmátstrénu.
2. Stilltu valkostinn **Safna saman úttaksupplýsingum** á **Já**. Þú getur nú stillt þetta snið með því að nota innihald myndaðrar skýrslu sem gagnagjafinn sem hægt er að nálgast með því að nota innbyggðu ER aðgerðirnar í flokknum [Gagnasafn](er-functions-category-data-collection.md).
3. Á flipanum **Vörpun** velurðu XML-þáttinn **Skýrsla\\Skilaboð\\Skrá**.
4. Stilltu segðina **Heiti lykils fyrir söfnuð gögn** sem `WsColumn`.
5. Stilltu segðina **Gildi lykils fyrir söfnuð gögn** sem `WsRow`.

    ![Skrá XML-einingu á síðu sniðshönnuðar.](./media/ER-DeferredXml-Format3.png)

6. Veldu eigindið **Skýrsla\\Skilaboð\\Skrá\\TaxAmount**.
7. Stilltu segðina **Heiti lykils fyrir söfnuð gögn** sem `SummingAmountKey`.

    ![TaxAmount-eigind á síðu sniðshönnuðar.](./media/ER-DeferredXml-Format4.png)

    Þú getur íhugað þessa stillingu efndir á sýndarverkefnisblaði, þar sem verðmæti hólfs A1 er bætt við verðmæti skattafjárhæðarinnar frá hverri afgreiddri skattafærslu.

8. Veldu eigindina **Skýrsla\\Skilaboð\\Skrá\\RunningTotal** og veldu síðan **Breyta formúlu**.
9. Stilltu segðina `SUMIF(SummingAmountKey, WsColumn, WsRow)` með því að nota innbyggða [SUMIF](er-functions-datacollection-sumif.md) ER aðgerð og veldu síðan **Vista**.

    ![SUMIF-segð.](./media/ER-DeferredXml-FormulaDesigner.png)

10. Lokaðu síðunni **Formúluhönnuður**.
11. Veldu **Vista** og síðan **Keyra**.
12. Sæktu og farðu yfir skrána sem vefskoðarinn býður upp á og opnaðu hana til skoðunar.

    ![Listi búinn til yfir skattagildi með hlaupandi samtölu.](./media/ER-DeferredXml-Run1.png)

    Síðasti skráningarhnúturinn inniheldur hlaupandi samtölu skattagilda sem eru reiknuð fyrir öll afgreidd viðskipti með því að nota myndaða framleiðsluna sem gagnagjafa. Þessi gagnagjafi hefst á byrjun skýrslunnar og heldur áfram í gegnum síðustu skattafærslu. Yfirlitshnúturinn inniheldur summan af skattagildum fyrir allar unnar færslur sem eru reiknaðar út í líkanavörpun með því að nota gagnagjafa af gerðinni *GroupBy*. Taktu eftir að þessi gildi eru jöfn. Þess vegna er hægt að nota samlagningu sem byggir á úttaki í staðinn fyrir **GroupBy**. Með því að bera saman framkvæmdatíma fyrsta skráarhnútsins og yfirlitshnútsins, getur þú ákvarðað að myndun allra skráarhnútanna og yfirlit hafi tekið 11 ms. Þess vegna er breytta sniðið um það bil tvisvar sinnum hraðara en upprunalega sniðið varðandi myndun skráarhnúta og summan af skattagildum.

13. Veldu eigindina **Skýrsla\\Skilaboð\\Yfirlit\\TotalTaxAmount** og veldu síðan **Breyta formúlu**.
14. Sláðu inn segðina `SUMIF(SummingAmountKey, WsColumn, WsRow)` í stað núverandi segðar.
15. Veldu **Vista** og síðan **Keyra**.
16. Sæktu og farðu yfir skrána sem vefskoðarinn býður upp á og opnaðu hana til skoðunar.

    ![Listi búinn til yfir skattagildi með breyttri formúlu.](./media/ER-DeferredXml-Run2.png)

    Taktu eftir því að hlaupandi samtala skattagilda í síðasta færsluhnút er nú jafnhá samtölu yfirlitshnútsins.

### <a name="put-values-of-output-based-summing-in-the-report-header"></a>Settu gildi framleiðslutengdrar summunar í haus skýrslunnar

Ef þú til dæmis verður að setja summan af skattagildum í haus skýrslunnar geturðu breytt sniði þínu.

1. Á síðunni **Sniðmátshönnuður**, á flipanum **Snið**, veldu XML-þáttinn **Skýrsla\\Skilaboð\\Yfirlit**.
2. Veldu **Færa upp**.
3. Veldu **Vista** og síðan **Keyra**.
4. Sæktu og farðu yfir skrána sem vefskoðarinn býður upp á og opnaðu hana til skoðunar.

    ![Skrá yfir skattagildi fyrir skýrsluhaus sótt.](./media/ER-DeferredXml-Run3.png)

    Taktu eftir að summan af skattagildum í yfirlitshnútnum er nú jöfn 0 (núll), vegna þess að þessi summa er nú reiknuð út frá mynduðu úttaki. Þegar fyrsti hnúturinn er myndaður inniheldur myndað úttak ekki enn skráarhnúta sem hafa upplýsingar um færslur. Þú getur stillt þetta snið til að fresta framkvæmd á þættinum **Skýrsla\\Skilaboð\\Yfirlit** þar til að þátturinn **Skýrsla\\Skilaboð\\Skrá** hefur verið keyrður fyrir allar skattafærslur.

### <a name="defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used"></a>Frestaðu framkvæmd samantektar XML-þáttarins þannig að reiknuð samtala sé notuð

1. Á síðunni **Sniðmátshönnuður**, á flipanum **Snið**, veldu XML-þáttinn **Skýrsla\\Skilaboð\\Yfirlit**.
2. Stillið valkostinn **Frestuð framkvæmd** á **Já**.

    ![Valkostur frestaðrar framkvæmdar á XML-einingu samantektar á síðu sniðshönnuðar.](./media/ER-DeferredXml-Format5.png)

3. Veldu **Vista** og síðan **Keyra**.
4. Sæktu og farðu yfir skrána sem vefskoðarinn býður upp á og opnaðu hana til skoðunar.

    ![Skrá frestaðrar framkvæmdar sótt.](./media/ER-DeferredXml-Run4.png)

    Þátturinn **Skýrsla\\Skilaboð\\Yfirlit** er nú aðeins keyrður þegar allir aðrir hlutir sem eru ívafðir undir yfirþættinum **Skýrsla\\Skilaboð** hafa verið keyrðir. Þess vegna er hann keyrður þegar þátturinn **Skýrsla\\Skilaboð\\Skrá** hefur verið keyrður fyrir allar skattafærslur í gagnagjafanum **model.Data.List**. Framkvæmdartímar fyrstu og síðustu skráarhnútanna og um haus og yfirlitshnúta sýna þessa staðreynd.

## <a name="additional-resources"></a>Frekari upplýsingar

- [Skilgreina snið til að gera talningu og samlagningu](./tasks/er-format-counting-summing-1.md)
- [Rekja framkvæmd á sniði rafrænnar skýrslugerðar til að úrræðaleita vandamál sem tengjast afköstum](trace-execution-er-troubleshoot-perf.md)
- [Frestaðu framkvæmd raðarþátta á ER sniði](er-defer-sequence-element.md#Example)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
