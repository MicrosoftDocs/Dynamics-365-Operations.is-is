---
title: Skilgreina varpanir líkana rafrænnar skýrslugerðar sem háðar eru samhengi við lönd
description: Í þessari grein er útskýrt hvernig þú getur sett upp kortlagningar fyrir varpanir rafrænnar skýrslugerðar þannig að þær fari eftir landi/landssvæði þess lögaðila sem stýrir notkun þeirra.
author: kfend
ms.date: 11/11/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: Release 8.1.2
ms.custom: ''
ms.assetid: ''
ms.search.form: ERSolutionTable
ms.openlocfilehash: 5db0936682e0cc052622658ac14046013bc4fd87
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277757"
---
# <a name="configure-country-context-dependent-er-model-mappings"></a>Stilla landssamhengisháðar varpanir ER-líkans

[!include[banner](../includes/banner.md)]

Þú getur stillt kortlagningu rafrænnar skýrslugerðar þannig að þau útfæri almennt gagnalíkan fyrir rafræna skýrslugerð en séu sértæk fyrir Dynamics 365 Finance. Í þessari grein er útskýrt hvernig á að hanna margar líkanavarpanir rafrænnar skýrslugerðar fyrir gagnalíkan rafrænnar skýrslugerðar til að stjórna því hvernig þær eru notaðar af samsvarandi sniðum rafrænnar skýrslugerðar sem eru keyrð úr fyrirtækjum sem eru með mismunandi samhengi á landi/svæði.

## <a name="prerequisites"></a>Forkröfur

Til að ljúka dæmunum í þessari grein þarftu að hafa eftirfarandi aðgang:

- Aðgangur að Finance fyrir eitt af eftirfarandi hlutverkum:
    - Þróunaraðili rafrænnar skýrslulausnar
    - Hagnýtur ráðgjafi vegna rafrænnar skýrslugerðar
    - Kerfisstjóri

- Aðgang að tilviki Regulatory Configuration Service (RCS) sem hefur verið úthlutað fyrir sama leigjandann og fyrir Finance fyrir eitt af eftirfarandi hlutverkum:
    - Þróunaraðili rafrænnar skýrslulausnar
    - Hagnýtur ráðgjafi vegna rafrænnar skýrslugerðar
    - Kerfisstjóri

Sum skref í þessari grein krefjast keyrslu á sniði rafrænnar skýrslugerðar. Í sumum tilvikum verður framkvæmd á ER-sniði fyrir áhrifum af lands-/svæðissamhengi fyrirtækisins sem þú ert skráð (ur) inn á. Þú getur keyrt ER snið í núverandi RCS tilviki ef fyrirtækið sem hefur tilskilið lands-/svæðissamhengi er fáanlegt í RCS. Annars verður þú að hlaða upp lokinni útgáfu af stillingum á ER-líkanavörpunum og ER-sniðum sem nota ER-gagnalíkanið í tilviki þínu af Finance og keyra síðan ER sniðið í því tilviki af Finance. Nánari upplýsingar um hvernig á að flytja inn stillingar sem eru í RCS í tilvik af Finance er að finna í [Flytja inn stillingar úr RCS](rcs-download-configurations.md).

## <a name="single-model-mapping-case"></a>Stakt dæmi um líkanavörpun

Fylgið skrefunum í [viðauka 1](#appendix1) í þessari grein til að hanna nauðsynlega hluti rafrænnar skýrslugerðar. Núna ertu með stillingu líkanavörpunar **Vörpun (almennt)** sem inniheldur líkanavörpun fyrir skilgreininguna **Inngangsstaður 1**.

![Síða fyrir skilgreiningu rafrænnar skýrslugerðar, snið til að læra vörpunarskilgreiningar.](./media/RCS-Context-specific-mapping-Tree.PNG)

### <a name="run-the-configured-format"></a>Keyra skilgreinint snið

1.  Á síðunni **Skilgreiningar**, á flýtiflipanum **Útgáfur**, velurðu **Keyra**.
2.  Veljið **Í lagi**.

Taktu eftir að vafrinn býður upp á að hlaða niður textaskránni sem mynduð var með framkvæmdu ER sniði. Þar sem þetta snið var stillt til að nota skilgreininguna **Aðgangsstaður 1** og aðeins stök líkanavörpun er nú fáanleg fyrir grunnlíkanið sem inniheldur vörpun fyrir þessa skilgreiningu notaði keyrða ER-sniðið líkanavörpunina **Vörpun (almennt)** í skilgreiningunni **Vörpun (almennt)** sem gagnagjafa. Þess vegna inniheldur niðurflutt skrá textann **Almenn virkni 1**.

## <a name="multiple-shared-model-mappings-case"></a>Margvísleg samnýting á vörpunardæmi líkana

Fylgið skrefunum í [viðauka 2](#appendix2) í þessari grein til að hanna nauðsynlega hluti rafrænnar skýrslugerðar. Núna ertu með stillingar líkanavörpunar **Vörpun (almennt)** og **Vörpun (almennt) sérsnið** sem inniheldur hvor fyrir sig líkanavörpun fyrir skilgreininguna **Aðgangsstaður 1**.

![Síða fyrir skilgreiningu rafrænnar skýrslugerðar, kortlagning almennra og sérsniðinna stillinga.](./media/RCS-Context-specific-mapping-TreeCustom.PNG)

### <a name="run-the-configured-format"></a>Keyra skilgreinint snið

1.  Á síðunni **Skilgreiningar**, í skilgreiningartrénu, skal velja **Snið til að læra varpanir**.
2.  Á flýtiflipanum **Útgáfur** velurðu **Keyra**.
3.  Veljið **Í lagi**.

Taktu eftir að framkvæmd á völdu ER sniði tókst ekki. Villuboð upplýsa þig um að fleiri en ein gerð vörpunar er til fyrir líkanið **Líkan til að læra varpanir** og skilgreininguna **Aðgangsstaður 1** á stillingum líkanavarpana **Kortlagning (almennt)** og **Kortlagning (almenn) sérsniðin**. Skilaboðin mæla einnig með að þú veljir eina af þessum stillingum sem sjálfgefna stillingu.

![Síða fyrir skilgreiningu rafrænnar skýrslugerðar með villuboðum.](./media/RCS-Context-specific-mapping-FormatRunCustomFailed.PNG)

### <a name="define-a-default-mapping-configuration"></a>Skilgreindu sjálfgefna líkanavörpun

Fylgdu þessum skrefum til að skilgreina stillingu líkanavörpunar **Kortlagning (almenn) sérsniðin** sem sjálfgefna stillingu, svo að hægt sé að nota varpanir hennar sem gagnagjafa fyrir ER-sniðið **Snið til að læra vörpun**.

1.  Á síðunni **Skilgreiningar**, í skilgreiningartrénu, skal velja **Vörpun (almennt) sérsnið**.
2.  Veldu eftir þörfum **Breyta** til að gera þessa síðu tilbúna til að breyta.
3.  Stillið valkostinn **Sjálfgefið fyrir líkanavörpun** á **Já**.
4.  Veldu **Vista**.

![Síða fyrir skilgreiningu rafrænnar skýrslugerðar, sjálfgefið fyrir sleða vörpunar líkans á Já.](./media/RCS-Context-specific-mapping-MappingsCustomDefault.PNG)

### <a name="run-the-configured-format"></a>Keyra skilgreinint snið

1.  Á síðunni **Skilgreiningar**, í skilgreiningartrénu, skal velja **Snið til að læra varpanir**.
2.  Á flýtiflipanum **Útgáfur** velurðu **Keyra**.
3.  Veljið **Í lagi**.

Taktu eftir að framkvæmd á völdu ER sniði tókst. Vafrinn býður upp á að hlaða niður textaskránni sem mynduð var með framkvæmdu ER sniði. Þar sem þetta snið var stillt til að nota skilgreininguna **Aðgangsstaður 1** og stilling líkanavörpunar **Vörpun (almennt) sérsnið** var valin sem sjálfgefin stilling notaði keyrða ER-sniðið líkanavörpunina **Vörpun (almennt) afrit** í skilgreiningunni **Vörpun (almennt) sérsnið** sem gagnagjafa. Þess vegna inniheldur niðurflutt skrá textann **Almenn virkni 1 sérsnið**.

> [!NOTE]
> Ef þú skiptir um fyrirtæki sem þú ert skráð/ur inn í og keyrir þetta ER snið aftur, þá færðu sama innihaldið í myndinni, vegna þess að sjálfgefna uppsetning ER gerðanna inniheldur engar fyrirtækjaháðar hömlur.

## <a name="multiple-mixed-model-mappings-case"></a>Mörg blönduð vörpunardæmi líkana

Fylgið skrefunum í [viðauka 3](#appendix3) í þessari grein til að hanna nauðsynlega hluti rafrænnar skýrslugerðar. Núna ertu með stillingar **Vörpun (almennt)**, **Vörpun (almennt) sérsnið** og **Vörpun (FR) líkanavörpunar** sem innihalda líkanavörpun fyrir skilgreininguna **Aðgangsstaður 1**.

Taktu eftir að útgáfa 1 af stillingu líkanavörpunar **Vörpun (FR)** er þannig stillt að hún á aðeins við um ER-snið í líkaninu **Líkan til að læra varpanir** sem eru keyrði í fjármálafyrirtækjum sem hafa franskt lands-/svæðissamhengi.

![Síða fyrir skilgreiningu rafrænnar skýrslugerðar, vörpun líkans (FR) stilling.](./media/RCS-Context-specific-mapping-TreeFR.PNG)

### <a name="run-the-configured-format"></a>Keyra skilgreinint snið

1.  Breyttu fyrirtækinu í **FRSI**.
2.  Á síðunni **Skilgreiningar**, í skilgreiningartrénu, skal velja **Snið til að læra varpanir**.
3.  Á flýtiflipanum **Útgáfur** velurðu **Keyra**.
4.  Veljið **Í lagi**.

Taktu eftir að framkvæmd á völdu ER sniði tókst. Vafrinn býður upp á að hlaða niður textaskránni sem mynduð var með framkvæmdu ER sniði. Þar sem þetta snið var stillt til að nota skilgreininguna **Aðgangsstaður 1** og stilling líkanavörpunar **Vörpun (almennt) sérsnið** var valin sem sjálfgefin stilling notaði keyrða ER-sniðið líkanavörpunina **Vörpun (almennt) afrit** í skilgreiningunni **Vörpun (almennt) sérsnið** sem gagnagjafa. Þess vegna inniheldur niðurflutt skrá textann **Almenn virkni 1 sérsnið**.

### <a name="define-the-france-specific-mapping-configuration-as-the-default-configuration"></a>Tilgreindu líkanastillingar sem eru sértækar fyrir Frakkland sem sjálfgefna stillingu

Fylgdu þessum skrefum til að skilgreina sérsniðna líkanavörpunarstillingu **Vörpun (FR)** sem sjálfgefna stillingu. Athugaðu að vegna þess að þessi vörpun er sértæk fyrir Frakkland verður hún talin sjálfgefin vörpun milli allra stillinga líkanavarpana sem hafa landskóðann **FR** sem tilgreindur er í reitnum **ISO lands-/svæðiskóðar**.

1.  Á síðunni **Skilgreiningar**, í skilgreiningartrénu, skal velja **Vörpun (FR)**.
2.  Veldu eftir þörfum **Breyta** til að gera þessa síðu tilbúna til að breyta.
3.  Stillið valkostinn **Sjálfgefið fyrir líkanavörpun** á **Já**.
4.  Veldu **Vista**.

![Síða fyrir skilgreiningu rafrænnar skýrslugerðar, vörpun (FR) stilling, sjálfgefið fyrir sleða vörpunar líkans á Já.](./media/RCS-Context-specific-mapping-TreeFRDefault.PNG)

### <a name="run-the-configured-format"></a>Keyra skilgreinint snið

1.  Á síðunni **Skilgreiningar**, í skilgreiningartrénu, skal velja **Snið til að læra varpanir**.
2.  Á flýtiflipanum **Útgáfur** velurðu **Keyra**.
3.  Veljið **Í lagi**.

Taktu eftir að framkvæmd á völdu ER sniði tókst. Vafrinn býður upp á að hlaða niður textaskránni sem mynduð var með framkvæmdu ER sniði. Þar sem þetta snið var stillt til að nota skilgreininguna **Aðgangsstaður 1** og stilling líkanavörpunar **Vörpun (FR)** var valin sem sjálfgefin stilling notaði keyrða ER-sniðið líkanavörpunina **Vörpun (FR)** í skilgreiningunni **Vörpun (FR)** sem gagnagjafa. Þess vegna inniheldur niðurflutt skrá textann **FR virkni 1**.

> [!NOTE]
> Ef þú skiptir um fyrirtæki sem þú ert skráð/ur inn í og keyrir þetta ER snið aftur mun framleiðslan fara eftir samhengi lands-/svæðis valins fyrirtækis.

## <a name="other-model-mapping-cases"></a>Önnur dæmi um líkanavörpun

Eins og þú hefur séð virkar val á líkanavörpun til framkvæmdar á ER sniði á eftirfarandi hátt:

- Skilgreining líkanavörpunar sem snið rafrænnar skýrslugerðar notar er tilgreind (**Aðgangsstaður 1** í dæmunum í þessari grein).
- Allar skilgreiningar vörpunar sem innihalda vörpun sem er með tilgreinda skilgreiningu og sem uppfylla allar takmarkanir á samhengi lands/svæðis er mögulega hægt að nota til að keyra snið rafrænnar skýrslugerðar (**Vörpun (almenn)**, **Vörpun (almenn) sérsniðs** og **Vörpun (FR)** í dæmunum í þessari grein).
- Allar sjálfgefnar líkanavarpanir sem eru með takmarkanir á samhengi lands/svæðis eru með hæsta forgang fyrir val (**Vörpun (FR)** í dæmunum í þessari grein).
- Allar sjálfgefnar líkanavarpanir sem eru ekki með takmarkanir á samhengi lands/svæðis eru með næsthæsta forgang fyrir val (**Vörpun (almenn) sérsniðs** í dæmunum í þessari grein).
- Sérhver líkanakortlagning sem hefur takmarkanir á landi/svæðum hefur meiri forgang við val en vörpun líkana sem eru ekki með samhengi takmarkana á landi/svæðum.

Eftirfarandi tafla veitir upplýsingar um niðurstöður val á líkanavörpun fyrir öll möguleg tilvik fyrir líkanavarpanastillingar:

- Dálkur 1 gefur til kynna hvort fyrsta vörpun líkansins sem hefur ekki takmarkanir á samhengi landa/svæða (til dæmis samnýtta líkanið **Vörpun (almennt)**) er kynnt og, ef það er, hvort valkosturinn **Sjálfgefið fyrir líkanavörpun** er stilltur á **Já** fyrir það.
- Dálkur 2 gefur til kynna hvort önnur vörpun líkansins sem hefur ekki takmarkanir á samhengi landa/svæða (til dæmis samnýtta líkanið **Vörpun (almennt) sérsnið**) er kynnt og, ef það er, hvort valkosturinn **Sjálfgefið fyrir líkanavörpun** er stilltur á **Já** fyrir það.
- Dálkur 3 gefur til kynna hvort fyrsta vörpun líkansins sem hefur takmarkanir á samhengi landa/svæða A (til dæmis Frakklands-sértæka líkanið **Vörpun (FR)**) er kynnt og, ef það er, hvort valkosturinn **Sjálfgefið fyrir líkanavörpun** er stilltur á **Já** fyrir það.
- Dálkur 4 gefur til kynna hvort önnur vörpun líkansins sem hefur takmarkanir á samhengi landa/svæða A (til dæmis Frakklands-sértæka líkanið Vörpun (FR)) er kynnt og, ef það er, hvort valkosturinn **Sjálfgefið fyrir líkanavörpun** er stilltur á **Já** fyrir það.
- Dálkur 5 sýnir niðurstöðu úr vali á líkanavörpun fyrir framkvæmd á ER sniði undir stjórn fyrirtækis sem hefur lands-/svæðissamhengi A.
- Dálkur 6 sýnir niðurstöðu úr vali á líkanavörpun fyrir framkvæmd á ER sniði undir stjórn fyrirtækis sem hefur lands-/svæðissamhengi B.

Í töflunni bendir plúsmerki (+) til að til sé stilling líkanavörpunar í núverandi tilviki Microsoft Azure þjónustu sem er notuð til að keyra ER snið (annaðhvort Finance eða RCS).

| Tilvik | Líkanavörpun 1 án samhengis lands/svæðis (MM1) | Líkanavörpun 2 án samhengis lands/svæðis (MM2) | Líkanavörpun 1 með samhengi lands/svæðis A (MM1A) | Líkanavörpun 2 með samhengi lands/svæðis A (MM2A) | Keyra undir stjórn fyrirtækis sem hefur lands-/svæðissamhengi A | Keyra undir stjórn fyrirtækis sem hefur lands-/svæðissamhengi B |
|---------|---------|---------|---------|---------|---------------------------|----------------------------|
|         |     1   |     2   |    3    |    4    |           5               |            6               |
|     1   |         |         |         |         | Villa (vantar vörpun)   | Villa (vantar vörpun)    |
|     2   |     +   |         |         |         | MM1                       | MM1                        |
|     3   |     +   |     +   |         |         | Villa (margar varpanir) | Villa (margar varpanir)  |
|     4   |     +   |         |    +    |         | MM1A                      | MM1                        |
|     5   |     +   |         |    +    |    +    | Villa (margar varpanir) | MM1                        |
|     6   |     +   | sjálfgefið |    +    |    +    | MM2                       | MM2                        |
|     7   |     +   |         | sjálfgefið |         | MM1A                      | MM1                        |
|     8   |     +   |         | sjálfgefið |    +    | MM1A                      | MM1                        |
|     9   |     +   |         | sjálfgefið | sjálfgefið | Villa (margar varpanir) | MM1                        |
|    10   | sjálfgefið |         |         |         | MM1                       | MM1                        |
|    11   | sjálfgefið |    +    |         |         | MM1                       | MM1                        |
|    12   | sjálfgefið |         |    +    |         | MM1                       | MM1                        |
|    13   | sjálfgefið | sjálfgefið |         |         | Villa (margar varpanir) | Villa (margar varpanir)  |
|    14   | sjálfgefið |         | sjálfgefið |         | MM1A                      | MM1                        |
|    15   | sjálfgefið |         | sjálfgefið | sjálfgefið | MM1A                      | MM2A                       |
|    16   |         |         |    +    |    +    | MM1A                      | MM2A                       |
|    17   |         |         | sjálfgefið | sjálfgefið | MM1A                      | MM2A                       |

## <a name="learn-what-mapping-was-used-in-the-execution-of-an-er-format"></a>Lærðu hvaða vörpun var notuð við framkvæmd ER sniðs

### <a name="configure-er-user-parameters"></a>Skilgreina færibreytur notanda rafrænnar skýrslugerðar

1.  Á síðunni **Skilgreiningar**, í aðgerðarúðunni, á flipanum **CONFIGURATIONS**, velurðu **Færibreytur notanda**.
2.  Stilltu valkostinn **Keyra í kembistillingum** á **Já**.
4.  Veljið **Í lagi**.

### <a name="run-the-configured-format"></a>Keyra skilgreinint snið

1.  Á síðunni **Skilgreiningar**, í skilgreiningartrénu, skal velja **Snið til að læra varpanir**.
2.  Á flýtiflipanum **Útgáfur** velurðu **Keyra**.
3.  Veljið **Í lagi**.

### <a name="review-the-er-debug-log"></a>Skoðaðu villuleitarskrá ER

1.  Farðu í **Einingar \> Fyrirtækisstjórnun \> Rafræn skýrslugerð \> Kembingarkladdar skilgreiningar**.
2.  Veldu hnappinn **Endurhlaða þessa síðu**.

![Keyrslukladdasíða ER.](./media/RCS-Context-specific-mapping-DebugLog.PNG)

Taktu eftir að nýrri skrá hefur verið bætt við ER kembiforrit fyrir keyrð ER snið. Þar sem reiturinn **Stig** í þessari skrár er stilltur á **Upplýsingar** er skráin upplýsandi. Þar sem reiturinn Sniðsíhlutur er stilltur á **Vörpunarstilling** upplýsir skráin þig um líkanavörpun sem var notuð við framkvæmd á ER-sniðinu **Snið til að læra vörpun** (valið í reitnum **Stillingarheiti**). Innihald reitsins **Myndaður texti** upplýsir þig um að vörpunarhlutinn **Vörpun (FR)** sem er staðsett í stillingunni **Vörpun (FR)** hefur verið notaður til að keyra þessa skýrslu.

## <a name="appendix-1"></a><a name="appendix1"></a> Viðauki 1

### <a name="configure-a-sample-data-model"></a>Stilltu sýnishorn gagnalíkans

Skráðu þig inn á RCS tilvikið.

Í þessu dæmi mun notandi stofna skilgreiningu fyrir sýnifyrirtækið Litware, Inc. Til að ljúka þessum skrefum verður fyrst í RCS að ljúka skrefum ferlisins [Stofna skilgreiningaveitu og merkja hana sem virka](tasks/er-configuration-provider-mark-it-active-2016-11.md):

#### <a name="create-an-er-data-model-configuration"></a>Stofna nýjan skilgreiningu ER-gagnalíkans

1.  Veldu á sjálfgefna mælaborðinu **Rafræn skýrslugerð**.
2.  Veldu reitinn **Skilgreiningar skýrslugerðar**.
3.  Á síðunni **Skilgreiningar** skal velja **Stofna stillingu**.
4.  Í fellilistanum, í reitnum **Heiti**, slærðu inn **Líkan til að læra varpanir**.
5.  Veljið **Stofna skilgreiningu**.
6.  Veldu flýtiflipann **Stillingarhlutar**.

Taktu eftir að drög að útgáfu 1 af þessari ER stillingu eru tilbúin til breytinga. Þessi útgáfa inniheldur íhluta gagnalíkansins.

#### <a name="design-a-sample-data-model"></a>Hanna sýnishorn gagnalíkans

1.  Á síðunni **Síðan skilgreiningar** skal velja **Hönnuður**.
2.  Veljið **Nýtt**.
3.  Í fellilistanum, í reitnum **Heiti** slærðu inn **Aðgangsstaður 1**.
4.  Veljið **Bæta við**.
5.  Veljið **Nýtt**.
6.  Í fellilistanum, í reitnum **Heiti**, slærðu inn **Lýsing á virkni**.
7.  Veljið **Bæta við**.
8.  Veljið **Nýtt**.
9.  Í fellilistanum, í reitahópnum **Nýr hnútur**, velurðu **Líkanshnútur**.
10. Í reitinn **Heiti** slærðu inn **Aðgangsstaður 2**.
11. Veldu **Inngangsstaður 2**.
12. Veljið **Bæta við**.
13. Veljið **Nýtt**.
14. Í fellilistanum, í reitnum **Heiti**, slærðu inn **Lýsing á virkni**.
15. Veljið **Bæta við**.

    ![Hönnunarsíða ER-gagnalíkans.](./media/RCS-Context-specific-mapping-Model.PNG)

16. Veldu **Vista**.
17. Lokið síðunni.

#### <a name="complete-the-modified-version-of-the-model-configuration"></a>Ljúka við breyttu útgáfuna af líkanastillingu rafrænnar skýrslugerðar

1.  Á síðunni **Skilgreiningar**, á flýtiflipanum **Útgáfur**, velurðu **Breyta stöðu**.

    > Breyta stöðu hönnuðar líkanastillingar úr **Drög** í **Lokið** svo að hægt sé að nota hana til að hanna nauðsynlegar varpanir og snið líkansins.

2.  Velja **Lokið**.
3.  Veljið **Í lagi**.

Athugið að skilgreiningin sem þú stofnaðir er vistuð sem lokin útgáfa 1.

### <a name="configure-a-sample-model-mapping"></a>Stilltu sýnishorn líkanavörpunar

#### <a name="create-an-er-model-mapping-configuration"></a>Stofna grunnstillingu ER-líkansvörpunar

1.  Á síðunni **Skilgreiningar** skal velja **Stofna stillingu**.
2.  Í fellilistanum, í reitahópnum **Nýtt**, velurðu **Líkanavörpun byggð á gagnalíkaninu Líkan til að læra varpanir**.
3.  Í reitinn **Heiti** slærðu inn **Vörpun (almennt)**.
4.  Í reitnum **Skilgreining gagnalíkans** velurðu **Aðgangsstaður 1**.
5.  Veljið **Stofna skilgreiningu**.

Taktu eftir að drög að útgáfu 1 af þessari ER stillingu eru tilbúin til breytinga. Þessi útgáfa inniheldur íhluta líkanavörpunar.

#### <a name="design-a-sample-model-mapping"></a>Hanna sýnishorn líkanavörpunar

1.  Á síðunni **Skilgreiningar** skal velja **Hönnuður**.

    Taktu eftir því að kortlagning líkansins á stefnugerðinni **Til líkans** hefur sjálfkrafa verið bætt við þennan íhlut fyrir skilgreininguna **Aðgangsstaður 1**.
    
2.  Veldu **Hönnuður** til að byrja að breyta viðbættri líkanavörpun.
3.  Í hlutanum **Gagnalíkan** velurðu **Breyta**.
4.  Í reitinn **Formúla** skal færa inn **„Almenn virkni 1“**.
5.  Veljið **Vista**.
6.  Lokaðu síðunni **Formúluhönnuður**.

    ![Hönnuðarsíða ER-líkanavörpunar, aðgangsstaður 1 skilgreining.](./media/RCS-Context-specific-mapping-Mapping1.PNG)

7.  Veldu **Vista**.
8.  Lokið síðunni **Hönnuður líkanavörpunar**.
9.  Veljið **Nýtt**.
10. Í reitnum **Skilgreining** velurðu **Aðgangsstaður 2**.
11. Í reitinn **Heiti** slærðu inn **Vörpun (almennt) 2**.
12. Veljið **Hönnuður**.
13. Í hlutanum **Gagnalíkan** velurðu **Breyta**.
14. Í reitinn **Formúla** skal færa inn **„Almenn virkni 2“**.
15. Veljið **Vista**.
16. Lokaðu síðunni **Formúluhönnuður**.

    ![Hönnuðarsíða ER-líkanavörpunar, aðgangsstaður 2 skilgreining.](./media/RCS-Context-specific-mapping-Mapping2.PNG)

17. Veldu **Vista**.
18. Lokið síðunni **Hönnuður líkanavörpunar**.

    ![Síða ER-líkanavörpunar með skilgreiningar aðgangsstaðs.](./media/RCS-Context-specific-mapping-Mappings.PNG)

19. Lokið síðunni **Líkanavarpanir**.

#### <a name="complete-the-modified-version-of-the-model-mapping-configuration"></a>Ljúka við breyttu útgáfuna af stillingu líkanavörpunar

1.  Á síðunni **Skilgreiningar**, á flýtiflipanum **Útgáfur**, velurðu **Breyta stöðu**.

    > Breyta stöðu hönnuðar stillingar líkanavörpunar úr **Drög** í **Lokið** svo að hægt sé að nota hana til að í ER-sniðmátum.

2.  Velja **Lokið**.
3.  Veljið **Í lagi**.

Athugið að skilgreiningin sem var stofnað er vistuð sem lokin útgáfa 1.

### <a name="configure-a-sample-format"></a>Stilla sýnissnið

#### <a name="create-an-er-format-configuration"></a>Stofna skilgreiningu ER-sniðs

1.  Á síðunni **Skilgreiningar**, í skilgreiningartrénu, skal velja **Líkan til að læra varpanir**.
2.  Veljið **Stofna skilgreiningu**.
3.  Í fellilistanum, í reitahópnum **Nýtt**, velurðu **Sniðmát byggt á gagnalíkaninu Líkan til að læra varpanir**.
4.  Í reitnum **Heiti** slærðu inn **Sniðmát til að læra varpanir**.
5.  Í reitnum **Skilgreining gagnalíkans** velurðu **Aðgangsstaður 1**.
6.  Veljið **Stofna skilgreiningu**.

Taktu eftir að drög að útgáfu 1 af þessari ER stillingu eru tilbúin til breytinga. Þessi útgáfa inniheldur íhluta sniðsins.

#### <a name="design-a-sample-format"></a>Hanna sýnissnið

1.  Á síðunni **Skilgreiningar** skal velja **Hönnuður**.
2.  Veljið **Bæta við rót**.
3.  Í hópnum **Texti** velurðu liðinn **Strengur**.
4.  Veljið **Í lagi**.

#### <a name="bind-format-elements-to-a-data-source"></a>Binda sniðsþætti í gagnagjafa

1.  Á síðunni **Sniðahönnuður**, á flipanum **Vörpun**, stækkarðu gagnagjafa líkansins.
2.  Veldu reitinn **Lýsing á virkni**.
3.  Veldu **Binda**.

    ![Síða ER-sniðshönnuðar.](./media/RCS-Context-specific-mapping-Format.PNG)

4.  Veldu **Vista**.
5.  Lokið síðunni.

## <a name="appendix-2"></a><a name="appendix2"></a> Viðauki 2

### <a name="configure-a-sample-model-mapping-for-general-customization"></a>Stilla vörpun sýnislíkans fyrir almenna sérstillingu

Þú gætir viljað sérsníða líkanavörpun sem stillingarveita (samstarfsaðili) gaf þér og notað síðan sérsniðna útgáfu sem gagnagjafa fyrir ER sniðin þín. Í þessu tilfelli verður þú að stofna sérsniðna vörpunarstillingu ER-líkans til að gera nauðsynlegar breytingar á fyrirliggjandi vörpun. Aðferðirnar í þessum viðbæti nota líkanavörpunina **Vörpun (almennt)** sem dæmi.

#### <a name="create-an-er-model-mapping-configuration"></a>Stofna grunnstillingu ER-líkansvörpunar

1.  Á síðunni **Skilgreiningar**, í skilgreiningartrénu, skal velja **Vörpun (almennt)**.
2.  Veljið **Stofna skilgreiningu**.
3.  Í fellivalmyndinni í reitahópnum **Nýtt**, velurðu **Leiða af nafni: Vörpun (Almennt), Litware, Inc.**.
4.  Í reitinn **Heiti** slærðu inn **Vörpun (almennt) sérsnið**.
5.  Veljið **Stofna skilgreiningu**.

Taktu eftir að drög að útgáfu 1 af þessari ER stillingu eru tilbúin til breytinga.

#### <a name="design-a-sample-model-mapping"></a>Hanna sýnishorn líkanavörpunar

1.  Á síðunni **Skilgreiningar** skal velja **Hönnuður**.

    > Taktu eftir því að líkanavarpanir grunnstillingarinnar eru sjálfkrafa afritaðar í þessa stillingu.

2.  Veldu vörpunina **Vörpun (almennt) afrit**.
3.  Veljið **Hönnuður**.
4.  Í hlutanum **Gagnalíkan** velurðu **Breyta**.
5.  Í reitinn **Formúla** skal færa inn **„Almenn virkni 1 sérsnið“**.
6.  Veldu **Vista**.
7.  Lokið síðunni.

    ![Hönnuðarsíða ER-líkanavörpunar, almenn virkni 1 sérstillt formúla.](./media/RCS-Context-specific-mapping-Mapping1Custom.PNG)

8.  Veldu **Vista**.
9.  Lokið síðunni.
10. Veldu vörpunina **Vörpun 2 (almennt) afrit**.
11. Veljið **Hönnuður**.
12. Í hlutanum **Gagnalíkan** velurðu **Breyta**.
13. Í reitinn **Formúla** skal færa inn **„Almenn virkni 2 sérsnið“**.
14. Veldu **Vista**.
15. Lokið síðunni.

    ![Hönnuðarsíða ER-líkanavörpunar, almenn virkni 2 sérstillt formúla.](./media/RCS-Context-specific-mapping-Mapping2Custom.PNG)

16. Veldu **Vista**.
17. Lokið síðunni.

    ![ER-líkan í vörpunarsíðu gagnagjafa fyrir vörpun (almennt) afritunarvörpun.](./media/RCS-Context-specific-mapping-MappingsCustom.PNG)

18. Lokið síðunni.

#### <a name="complete-the-modified-version-of-the-model-mapping-configuration"></a>Ljúka við breyttu útgáfuna af stillingu líkanavörpunar

1.  Á síðunni **Skilgreiningar**, á flýtiflipanum **Útgáfur**, velurðu **Breyta stöðu**.

    > Breyta stöðu hönnuðar stillingar líkanavörpunar úr **Drög** í **Lokið** svo að hægt sé að nota hana til að í ER-sniðmátum.

2.  Velja **Lokið**.
3.  Veljið **Í lagi**.

Athugið að skilgreiningin sem var stofnað er vistuð sem lokin útgáfa 1.

## <a name="appendix-3"></a><a name="appendix3"></a> Viðauki 3

### <a name="configure-a-sample-model-mapping-for-countryregion-specific-customization"></a>Stilla vörpun sýnislíkans fyrir lands-/landsvæðissértæka sérstillingu

Fyrir sum ER snið geta verið lands-/svæðissértækar kröfur um undirbúning gagna. Í þessu tilfelli getur þú stjórnað sérstakri vörpun ER-líkana og einangrað framkvæmd þessara lands-/svæðisbundnu krafna frá almennri framkvæmd. Ferlin í þessum viðauka nota ER-sniðið **Snið til að læra varpanir** og franskar sértækar kröfur sem dæmi.

#### <a name="create-an-er-model-mapping-configuration"></a>Stofna grunnstillingu ER-líkansvörpunar

Í fyrsta lagi skaltu búa til nýja stillingu ER-líkanavörpunar til að innleiða lands-/svæðisbundnar kröfur. Notaðu sérsniðna stillingu ER-líkanavörpunar sem grunn.

1.  Á síðunni **Skilgreiningar**, í skilgreiningartrénu, skal velja **Vörpun (almennt) sérsnið**.
2.  Veljið **Stofna skilgreiningu**.
3.  Í fellivalmyndinni í reitahópnum **Nýtt**, velurðu **Leiða af nafni: Vörpun (Almennt) sérsnið, Litware, Inc.**.
4.  Í reitinn **Heiti** slærðu inn **Vörpun (FR)**.
5.  Veljið **Stofna skilgreiningu**.

Taktu eftir að drög að útgáfu 1 af þessari ER stillingu eru tilbúin til breytinga.

#### <a name="design-a-sample-model-mapping"></a>Hanna sýnishorn líkanavörpunar

1.  Á síðunni **Skilgreiningar** skal velja **Hönnuður**.

    > Taktu eftir því að líkanavarpanir grunnstillingarinnar eru sjálfkrafa afritaðar í þessa stillingu.

2.  Veldu vörpunina **Vörpun (almennt) afrit afrit**.
3.  Endurnefndu hana **Vörpun (FR)**.
4.  Veljið **Hönnuður**.
5.  Í hlutanum **Gagnalíkan** velurðu **Breyta**.
6.  Í reitinn **Formúla** skal færa inn **„FR-virkni 1“**.
7.  Veldu **Vista**.
8.  Lokið síðunni.

    ![Hönnuðarsíða ER-líkanavörpunar, FR-virkni 1 formúla.](./media/RCS-Context-specific-mapping-Mapping1FR.PNG)

9.  Veldu **Vista**.
10. Lokið síðunni.
11. Veldu vörpunina **Vörpun 2 (almennt) afrit afrit**.
12. Endurnefndu hana **Vörpun 2 (FR)**.
13. Veljið **Hönnuður**.
14. Í hlutanum **Gagnalíkan** velurðu **Breyta**.
15. Í reitinn **Formúla** skal færa inn **„FR-virkni 2“**.
16. Veldu **Vista**.
17. Lokið síðunni.

    ![Hönnuðarsíða ER-líkanavörpunar, FR-virkni 2 formúla.](./media/RCS-Context-specific-mapping-Mapping2FR.PNG)

18. Veldu **Vista**.
19. Lokið síðunni.

    ![ER-líkan í vörpunarsíðu gagnagjafa.](./media/RCS-Context-specific-mapping-MappingsFR.PNG)

20. Lokið síðunni.

#### <a name="specify-countryregion-context-restrictions-for-use"></a>Tilgreindu lands-/svæðisbundnar samhengistakmarkanir fyrir notkun

1.  Á síðunni **Skilgreiningar**, á flýtiflipanum **ISO lands-/svæðiskóðar** velurðu **Nýtt**.
2.  Í reitnum **ISO** er valið **FR**.
3.  Veljið **Vista**.

Athugaðu að þú verður að skrá þig inn á tiltekið fyrirtæki í Finance til að keyra ER-snið. Þess vegna getur þetta fyrirtæki talist aðili sem stjórnar bæði framkvæmd ER-sniða og vali á réttri vörpun ER-líkans af ER-grunngagnalíkani. Með því að bæta við landskóðanum **FR** tilgreinirðu að vörpun líkansins er tiltæk til vals með ER sniði grunngagnalíkansins aðeins þegar það snið er keyrt undir stjórn fyrirtækis sem hefur franskt lands-/svæðissamhengi.

Þú getur bætt við mörgum lands-/svæðiskóðum fyrir staka útgáfu af stillingum á ER-líkanavörpun. Þannig er hægt að nota líkanavarpanir sem búa í þeirri stillingu líkanavörpunar fyrir ER-snið sem er keyrt undir stjórn fyrirtækja sem hafa annað lands-/svæðissamhengi.

Athugaðu að listinn yfir lands-/svæðisnúmer er tilgreindur fyrir hverja útgáfu af stillingum ER-líkanavörpunar og getur verið breytilegur frá einnu útgáfu til annarrar.

#### <a name="complete-the-modified-version-of-the-model-mapping-configuration"></a>Ljúka við breyttu útgáfuna af stillingu líkanavörpunar

1.  Á síðunni **Skilgreiningar**, á flýtiflipanum **Útgáfur**, velurðu **Breyta stöðu**.

    > Breyta stöðu hönnuðar stillingar líkanavörpunar úr **Drög** í **Lokið** svo að hægt sé að nota hana til að í ER-sniðmátum.

2.  Velja **Lokið**.
3.  Veljið **Í lagi**.

Athugið að skilgreiningin sem var stofnað er vistuð sem lokin útgáfa 1.

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit yfir rafræna skýrslugerð (ER)](general-electronic-reporting.md)

[Stjórna vörpunarlíkani rafrænnar skýrslugerðar í aðskilinni skilgreiningu rafrænnar skýrslugerðar](./tasks/er-manage-model-mapping-configurations-july-2017.md)

[Nota lands-/svæðistengt samhengi](../lcs-solutions/apply-country-context.md)

## <a name="frequently-asked-questions"></a>Algengar spurningar

#### <a name="i-configured-two-shared-er-model-mapping-configurations-in-rcs-and-marked-one-of-them-as-the-default-model-mapping-configuration-i-successfully-ran-an-er-format-that-was-created-for-the-same-base-er-data-model-configuration-to-test-model-mappings-i-then-imported-the-whole-er-solution-er-data-model-two-er-model-mapping-configurations-and-er-format-configuration-into-finance-why-do-i-receive-an-error-message-when-i-try-to-run-the-same-er-format-in-finance"></a>Ég stillti tvær sameiginlegar stillingar ER-líkanavörpunar í RCS og merkti eina þeirra sem sjálfgefna stillingu líkanavörpunar. Mér tókst að keyra ER-snið sem var búið til fyrir sömu grunngerð ER-gagnalíkanastillingar, til að prófa líkanavörpun. Síðan flutti ég inn alla ER-lausnina (ER-gagnalíkan, tvær stillingar ER-líkanavarpana og stillingar á ER-sniði) í Finance. Af hverju fæ ég villuboð þegar ég reyni að keyra sama ER-snið í Finance?
Sjálfgefin stilling líkanavörpunar er umhverfissértæk. Hún er stillt í RCS en er ekki flutt til Finance. Til að keyra þetta ER-snið verður þú að merkja eina af stillingum ER-líkanavörpunar sem sjálfgefna stillingu líkanavörpunar í Finance líka.

#### <a name="i-configured-one-model-mapping-as-a-shared-model-mapping-and-completed-the-draft-version-of-it-i-then-added-a-new-model-mapping-configuration-for-same-data-model-and-configured-it-as-french-specific-why-is-the-shared-model-mapping-selected-when-i-run-an-er-format-even-though-this-er-format-uses-the-correct-root-definition-and-execution-is-done-under-the-control-of-the-company-that-has-french-countryregion-context"></a>Ég stillti eina líkanavörpun sem samnýtta líkanavörpun og kláraði drög að útgáfu hennar. Síðan bætti ég við nýrri gerð stillingar líkanavörpunar fyrir sama gagnalíkan og stillti það sem fransk-sértækt. Hvers vegna er sameiginleg líkanavörpun valin þegar ég keyri ER-snið, jafnvel þó að þetta ER-snið noti réttar rótarskilgreiningar og framkvæmd er gerð undir stjórn fyrirtækisins sem hefur franskt lands-/svæðissamhengi?
Gakktu úr skugga um að samnýtta stilling líkanavörpunar sé ekki merkt sem sjálfgefin stilling líkanavörpunar. Annars mun það hafa meiri forgang við val á vörpun. Gakktu einnig úr skugga um að stillt sé á franskar sértækar stillingar líkanavörpunar þegar vörpun er valin við framkvæmd ER sniðs. Stillingar á ER-líkanavörpun er aðeins tiltæk til vals ef að minnsta kosti eitt af eftirfarandi skilyrðum er uppfyllt:
- Að minnsta kosti ein útgáfa af stilligum ER-líkanavörpunar hefur annaðhvort stöðuna **Lokið** eða **Deilt**. Í þessu tilfelli verður útgáfan sem er með hæsta útgáfunúmerið notuð við framkvæmd ER sniðs.
- Kveikt er á valkostinum **Keyra drög** fyrir stillingu ER-líkanavörpunar. Í þessu tilfelli verður útgáfan sem er með stöðuna **Drög** notuð við framkvæmd ER sniðs.
> Valkosturinn **Keyra drög** verður í boði á síðunni **Stillingar** fyrir sérhverja stillingu ER-líkanavörpunar þegar kveikt er á ER-færibreytu notanda **Keyra stillingu**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
