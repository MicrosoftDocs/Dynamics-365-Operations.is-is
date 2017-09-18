---
title: "Vinnusvæði kostnaðarstýringar"
description: "Þetta efnisatriði veitir upplýsingar um vinnusvæðið Kostnaðarstýring. Þetta vinnusvæði er miðlægur punktur þar sem stjórnendur sem bera ábyrgð á stýringu kostnaðarhlutar eða safni kostnaðarhluta innan víddar eða milli vídda geta sótt skýrslur."
author: AndersGirke
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMCostControlWorkspaceConfiguration, CAMCostControlWorkspace
audience: Application User
ms.reviewer: yuyus
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: YuyuScheller
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 63160b9473c7f45b0eb0ca7139f9ed47c8e1446f
ms.openlocfilehash: 5c5f06d1a518963738e446b5032261059d98bf13
ms.contentlocale: is-is
ms.lasthandoff: 06/20/2017

---

# <a name="cost-control-overview"></a>Yfirlit yfir kostnaðarstýringu 

[!include[banner](../includes/banner.md)]

Vinnusvæðið **Kostnaðarstýring** er miðlægur punktur þar sem stjórnendur sem bera ábyrgð á stýringu kostnaðarhlutar eða safni kostnaðarhluta innan víddar eða milli vídda (til dæmis kostnaðarstaðir og afurðahópar), geta sótt skýrslur. Kostnaðarbókarar stýra skýrslum algjörlega á vinnusvæði, þannig að útlit og gögn skýrslugerðarinnar séu eins í öllu fyrirtækinu.

## <a name="cost-control-workspace-configuration"></a>Skilgreining vinnusvæðis kostnaðarstýringar

Kostnaðarbókarar geta skilgreint eins margar skýrslustillingar og þörf er á fyrir æskilega gagnasamsetningu eða útlit. Skilgreining skýrslu samanstendur af sex hlutum, sem hver og einn hefur sitt að segja um annaðhvort val á tilætlaðri gagnasamsetningu eða útlit.

Ef skilgreina á vinnusvæði kostnaðarstýringar, smelltu á **Kostnaðarbókhald** \> **Uppsetning** \> **Skilgreining vinnusvæðis kostnaðarstýringar**.

### <a name="general"></a>Almennt

Á flýtiflipanum **Almennt** er hægt að stofna einstakt skýrsluútlit. Heiti skýrslunnar er einkvæmt auðkenni sem notendur geta þekkt á vinnusvæðinu **Kostnaðarstýring**. Einnig er hægt að tilgreina hvort skýrslan eigi að vera samnýtt eða aðgangur takmarkaður við kostnaðarbókara.

| Svæði       | lýsing |
|-------------|-------------|
| Nafn        | Sláðu inn einkvæmt heiti fyrir útlitið. |
| lýsing | Sláðu inn ítarlega lýsingu. |
| Útgefið   | Ef þessi reitur er stilltur á **Já**, getur notandi sem er úthlutað einu af eftirtöldum hlutverkum séð skýrsluna á vinnusvæðinu **Kostnaðarstýring**:<ul><li>Aðalbókari kostnaðarbókhalds</li><li>Kostnaðarbókari</li><li>Starfsmaður kostnaðarbókara</li><li>Stjórnborð kostnaðarhlutar</li></ul>Ef þessi reitur er stilltur á **Nei**, geta aðeins notendur sem er úthlutað einu af eftirtöldum hlutverkum séð skýrsluna á vinnusvæðinu **Kostnaðarstýring**:<ul><li>Aðalbókari kostnaðarbókhalds</li><li>Kostnaðarbókari</li><li>Starfsmaður kostnaðarbókara</li></ul> |

### <a name="data-filtering"></a>Gagnasíun

Á flýtiflipanum **Gagnasíun** geturðu skilgreint gagnagrunn fyrir skýrsluna. Notendur þessarar skýrslu munu sjá gildin í skýrsluna eftir að unnið hefur verið úr upprunagögnum.

| Svæði                                                             | lýsing |
|-------------------------------------------------------------------|-------------|
| Fjárhagur kostnaðarbókhalds                                            | **Fjárhagur kostnaðarbókhalds** sem skýrslan byggir á. Gildið er sótt í reitinn **Stýrieining kostnaðar**. |
| Stýrieining kostnaðar                                                 | Gildið sem þú velur ákvarðar fjárhag kostnaðarbókhalds og kostnaðarhluti sem þessi skýrsla byggir á. |
| Tölfræðilegt víddarstigveldi, víddarstigveldi kostnaðareiningar | Skilgreiningarfærslur vinnusvæðisins **Kostnaðarstýring** geta annaðhvort skráð ópeningaleg eða peningaleg gildi, en ekki í sama útlitinu. Veldu gildi í reitnum **Víddarstigveldi kostnaðareiningar** til að skrá peningaleg gildi. Veldu gildi í reitnum **Tölfræðilegt víddarstigveldi** til að skrá ópeningaleg gildi. Sú skráning víddarstigveldis sem þú velur ákvarðar uppbyggingu skýrslugerðar og flokkunarstig.<blockquote>[!NOTE]<br>Til að skoða ópeningaleg og peningaleg gildi hlið við hlið, getur þú flutt út gögn í Microsoft Excel fyrir Microsoft Power BI efnispakkann.</blockquote> |
| Víddarstigveldi kostnaðarhlutar                                   | Veldu það víddarstigveldi kostnaðarhlutarvíddar sem hæfir þeirri skýrslugerð sem þú ert að skilgreina. |
| Upprunaleg útgáfa fjárhagsáætlunar                                           | Veldu það auðkenni útgáfu fjárhagsáætlunar sem þjónar hlutverki upphaflegrar fjárhagsáætlunar í samhengi þessarar skýrslu. |
| Endurskoðuð útgáfa fjárhagsáætlunar                                            | Veldu það auðkenni útgáfu fjárhagsáætlunar sem þjónar hlutverki endurskoðaðrar fjárhagsáætlunar í samhengi þessarar skýrslu. |

### <a name="assign-calculation-records"></a>Úthluta útreikningsfærslum

Útreikningur sameiginlegs kostnaðar framkvæmir nokkur skref útreiknings á upprunagögnunum, eins og flokk kostnaðarhegðunar, kostnaðardreifingu og kostnaðarúthlutun. Hægt er að framkvæma marga útreikninga á sameiginlegum kostnaði fyrir sama fjárhagstímabil, ef ske kynni að týnd upprunagögn finnist eða það þurfi að uppfæra reglur. Hver útreikningur á sameiginlegum kostnaði er vistaður með einkvæmu auðkenni. Kostnaðarbókari getur valið tiltekið auðkenni útreiknings á sameiginlegum kostnaði. Notendur skýrslunnar, eins og stjórnendur, geta séð niðurstöður útreiknings á sameiginlegum kostnaði á vinnusvæðinu **Kostnaðarstýring**.

| Svæði                  | lýsing |
|------------------------|-------------|
| Fjárhagsdagatalstímabil | Veldu tímabil fjárhagsdagatals sem á að úthluta auðkenni útreiknings á sameiginlegum kostnaði.<blockquote>[!NOTE]<br>Þau fjárhagstímabil sem eru útlistuð í reitnum koma úr fjárhagsdagatalinu sem tengist fjárhagi kostnaðarbókhalds.</blockquote> |
| Raunútgáfa         | Veldu viðeigandi auðkenni útreiknings á sameiginlegum kostnaði. |
| Útgáfa fjárhagsáætlunar         | Veldu viðeigandi auðkenni útreiknings á sameiginlegum kostnaði. |
| Endurskoðuð útgáfa fjárhagsáætlunar | Veldu viðeigandi auðkenni útreiknings á sameiginlegum kostnaði. |

### <a name="fiscal-periods-per-column"></a>Fjárhagstímabil í dálki

Á flýtiflipanum **Fjárhagstímabil í dálki** ákveður kostnaðarbókari hvaða fjárhagstímabil á að birta í skýrsluútliti.

Gildin í völdum dálkum margfaldast með þeim gildum sem valin eru í flýtiflipanum **Fjárhagstímabil í dálki**.

| Svæði                | lýsing |
|----------------------|-------------|
| Gildandi tímabil       | Staða gildandi fjárhagstímabils er birt.<blockquote>[!NOTE]<br>Sjálfgefið er að gildandi tímabil ákvarðast af setudagsetningu. Í vinnusvæðinu **Kostnaðarstýring** er hægt að velja tiltekið fjárhagstímabil. Gildið sem er valið stendur svo fyrir gildandi tímabil.</blockquote> |
| Fyrra tímabil      | Staða fyrra fjárhagstímabils er birt. Eftirfarandi formúla er notuð:<br>Gildandi fjárhagstímabil - 1<blockquote>[!NOTE]<br>Það er sjálfgefið að fyrra tímabil byggist á setudagsetningu. Í vinnusvæðinu **Kostnaðarstýring** er hægt að velja tiltekið fjárhagstímabil sem gildandi tímabil. **Fyrra tímabil** er svo endurreiknað samkvæmt því.</blockquote> |
| Það sem af er ári         | Meðaltalið fyrir það sem af er ári er birt. Eftirfarandi formúla er notuð:<br>YearToDate (gildandi fjárhagstímabil)<blockquote>[!NOTE]<br>Sjálfgefið er að gildandi tímabil ákvarðast af setudagsetningu. Í vinnusvæðinu **Kostnaðarstýring** er hægt að velja tiltekið fjárhagstímabil. Valið gildi stendur svo fyrir gildandi tímabil og gildið **Það sem af er ári** verður uppfært samkvæmt því.</blockquote> |
| Það sem af er ári, meðaltal | Meðaltalið fyrir það sem af er ári er birt. Eftirfarandi formúla er notuð:<br>(YearToDate [Gildandi fjárhagstímabil]) ÷ (Talning [Gildandi fjárhagstímabil])<p><strong>Dæmi</strong></p><ul><li>**Tölfræðilegt víddarstak:** Starfsmenn í fullu starfi</li><li>**Núverandi dagsetning:** 21-3-2017</li><li>**Tímabil:** Fjárhagstímabil 1, fjárhagstímabil 2, fjárhagstímabil 3</li><li>**Mæligildi:** 10, 10, 12</li></ul>Í þessu tilfelli, **Meðaltal það sem af er ári** = (10 + 10 + 12) ÷ 3 = 10,67<p>Hægt er að reikna gildið **Meðaltal það sem af er ári** fyrir víddarstök kostnaðareiningar og tölfræðileg víddarstök.</p><blockquote>[!NOTE]<br>Sjálfgefið er að gildandi tímabil ákvarðast af setudagsetningu. Í vinnusvæðinu **Kostnaðarstýring** er hægt að velja tiltekið fjárhagstímabil. Þau gildi sem eru valin standa svo fyrir núverandi tímabil og gildin **Það sem af er ári** og **Meðaltal það sem af er ári** eru uppfærð samkvæmt því.</blockquote> |

### <a name="columns-to-display-for-costs"></a>Dálkar sem á að sýna fyrir kostnað

Á flýtiflipanum **Dálkar sem á að sýna fyrir kostnað** ákveður kostnaðarbókari hvaða dálka skýrsluútlitið á að innihalda. Það eru 3 flokkar: Fastur kostnaður, breytilegur kostnaður og óflokkaður kostnaður.

| Svæði                 | lýsing |
|-----------------------|-------------|
| Fastur kostnaður            | Þessi dálkagerð sýnir fastan kostnað á grundvelli þess auðkennis útreiknings sameiginlegs kostnaðar sem valið er.<blockquote>[!NOTE]<br>Þessi dálkagerð sýnir aðeins stöðu þegar auðkenni útreiknings á sameiginlegum kostnaði er valið fyrir fjárhagstímabilið.</blockquote> |
| Breytilegur kostnaður         | Þessi dálkagerð sýnir breytilegan kostnað á grundvelli þess auðkennis útreiknings sameiginlegs kostnaðar sem valið er.<blockquote>[!NOTE]<br>Þessi dálkagerð sýnir aðeins stöðu þegar auðkenni útreiknings á sameiginlegum kostnaði er valið fyrir fjárhagstímabilið.</blockquote> |
| Fastur + breytilegur kostnaður | Þessi dálkagerð sýnir fastan og breytilegan kostnað á grundvelli þess auðkennis útreiknings sameiginlegs kostnaðar sem valið er.<blockquote>[!NOTE]<br>Þessi dálkagerð sýnir aðeins stöðu þegar auðkenni útreiknings á sameiginlegum kostnaði er valið fyrir fjárhagstímabilið.</blockquote> |
| Heildarkostnaður            | Þessi dálkagerð sýnir heildarkostnað (óflokkaðan kostnað, fastan kostnað og breytilegan kostnað).<blockquote>[!NOTE]<br>Dálkagerðin sýnir stöðuna alltaf.</blockquote> |
| Óflokkaður kostnaður     | Þessi dálkagerð sýnir óflokkaðan kostnað.<blockquote>[!NOTE]<br>Þennan dálk er hægt að nota til að sannreyna að allur kostnaður hafi verið rétt flokkaður af útreikningi á sameiginlegum kostnaði eða hvort þurfi að stilla reglur kostnaðarhegðunar.</blockquote> |

### <a name="columns-to-display-for-budgeted-costs"></a>Dálkar sem á að sýna fyrir áætlaðan kostnað

Á flýtiflipanum **Dálkar sem á að sýna fyrir áætlaðan kostnað** ákveður kostnaðarbókari hvaða dálka á að sýna fyrir þær útgáfur fjárhagsáætlunar sem valdar eru. Hægt er að velja staka valkosti úr upphaflegri og endurskoðaðri fjárhagsáætlun.

> [!NOTE]
> Þar sem eftirtaldir reitir haga sér á sama hátt fyrir upphaflega og endurskoðaða fjárhagsáætlun eru þeir aðeins útskýrðir einu sinni.

| Svæði                     | lýsing |
|---------------------------|-------------|
| Fjárhagsáætlun                    | Áætlunarstöður verða sýndar eftir völdum dálkum.<blockquote>[!NOTE]<br>Stöður byggjast á þeim útgáfum fjárhagsáætlunar sem eru valdar á flýtiflipanum **Gagnasíun**.</blockquote> |
| Frávik fjárhagsáætlunar           | Reiknaðu og sýndu muninn milli áætlunar og rauntalna. Eftirfarandi formúla er notuð:<br>Staða fjárhagsáætlunar – Raunstaða |
| Frávik fjárhagsáætlunar í %      | Reiknaðu og sýndu muninn í prósentum milli áætlunar og rauntalna. Eftirfarandi formúla er notuð:<br>(Áætlunarstaða – Raunstaða) ÷ Staða fjárhagsáætlunar |
| Þröskuldur frávikstímabils | Settu upp þröskuld fyrir frávik í peningalegum upphæðum fyrir gildandi tímabil. Ef farið er yfir þröskuldinn er línan auðkennd með rauðu á vinnusvæðinu **Kostnaðarstýring**.<blockquote>[!NOTE]<br>Þessi reitur á aðeins við um þær kostnaðareiningar sem standa fyrir útgjöld.</blockquote> |
| Þröskuldur fráviksárs   | Settu upp þröskuld fyrir frávik í peningalegum upphæðum fyrir árið. Ef farið er yfir þröskuldinn er línan auðkennd með rauðu á vinnusvæðinu **Kostnaðarstýring**. |
| Fráviksþröskuldur %      | Settu upp þröskuld fyrir frávik í prósentum. Ef farið er yfir þröskuldinn er línan auðkennd með rauðu á vinnusvæðinu **Kostnaðarstýring**.<blockquote>[!NOTE]<br>Sama þröskuldarprósenta á við um gildandi tímabil og ár.</blockquote> |

## <a name="cost-control-workspace"></a>Vinnusvæði kostnaðarstýringar

Vinnusvæðið **Kostnaðarstýring** er hannað sem vefskýrsla. Þar af leiðandi er hægt að veita öllum stjórnendum aðgang sem bera ábyrgð á kostnaðarhlut eins og lýst er í [Skilgreining aðgangsréttinda stjórnborða kostnaðarhlutar](access-rights-cost-object-controller.md).

Listi yfir skýrslur sem eru tiltækar notendum, svo sem stjórnendum, ræðst af stillingunum í valkostinum **Útgefið** á síðunni **Grunnstillingar vinnusvæðis kostnaðarstýringar**.

![Skýrsla sem notendur geta skoðað í vinnusvæði kostnaðarstýringar](./media/report-cost-control.png)

Stjórnandi getur valið tímabil fjárhagsdagatals sem á að skoða. Setudagsetningin er notuð til að ákvarða sjálfgefið gildandi tímabil.

Gildin í tímabili fjárhagsdagatals ákvarðast af því skýrsluheiti og fjárhagsdagatali sem er valið fyrir fjárhag kostnaðarbókhalds sem tengist skýrsluheitinu á síðunni **Skilgreining vinnusvæðis kostnaðarstýringar**.

Í víddarstigveldi kostnaðarhlutar geta notendur valið það uppsöfnunarstig þar sem sýna á stöður. Með því að virkja öryggi á aðgangsstigi verður að stjórna heimildum þannig að notendur geti aðeins valið stigveldi sem þeir hafa aðgang að. Þar af leiðandi geta þeir aðeins séð uppsafnaðar stöður sem þeir hafa fengið aðgang að.

### <a name="add-or-remove-columns"></a>Bæta við eða fjarlægja dálka

Notendur geta sérsniðið dálkana í skýrslu þannig að þeir hæfi þörfum.

### <a name="view-details"></a>Skoða upplýsingar

Notendur geta kafað ofan í upplýsingar að baki stöðum sem eru birtar á vinnusvæðinu. Ef notendur velja víddarstigveldishnút kostnaðareiningar og smella svo á **Skoða upplýsingar**, sýnir svarglugginn **Upplýsingar um kostnaðareiningu** ítarlegar upplýsingar um hnútinn.

Hnitanet sýnir hverja kostnaðareiningu sem tengist víddarstigveldishnút kostnaðareiningar og gildi hennar. Dálkarnir sem birtast í hnitanetinu stemma við stillingar vinnusvæðisins.

Tvö gröf sýna samantekt rauntalna samanbornar við áætlun og áætlunarfrávik eftir tímabilum.

![Gröf sem sýna samantekt rauntalna samanbornar við áætlun og áætlunarfrávik eftir tímabilum.](./media/cost-element-details-operations.png)

Notendur geta smellt á **Kostnaðarfærslur** til að kafa niður í upplýsingar um færslu eins og þörf er á.

![Kostnaðarfærslur](./media/cost-entries.png)

Til dæmis er leiga útgjöld sem dreifist á kostnaðarstaði. Notandi sem vill öðlast skilning á leigukostnaði sem kostnaðarstaður hans eða hennar verður að bera getur kafað niður til að sjá hvernig leiga hefur verið reiknuð.

Ef notendur smella á **Úthlutunargrunnur** á síðunni **Kostnaðarfærslur** birtist svargluggi. Notendur geta svo úthlutað reglunni úthlutunargrunni og skoðað samsvarandi tölfræðilegar mælingar sem eru skráðar á því tímabili.

Í eftirfarandi dæmi er úthlutunargrunnur af gerðinni **Formúla úthlutunargrunns** og formúlan er sýnd. Þeir þættir sem skilgreina formúluna eru útlistaðir. Þar að auki sýnir hnitanetið útreikninginn sem er framkvæmdur á hvern kostnaðarhlut.

![Útreikningar á hvern kostnaðarhlut](./media/cost-entries-allocation-base.png)

Sjá einnig 

[Skilgreining aðgangsréttinda stjórnborða kostnaðarhlutar](access-rights-cost-object-controller.md)



