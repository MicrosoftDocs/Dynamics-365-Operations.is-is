---
title: Útreikningur fastakostnaður
description: Þetta efnisatriði lýsir dæmigerðum ferlum til að reikna út og úthluta rekstrarkostnaði.
author: AndersGirke
ms.date: 10/04/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMActualVersion, CAMBudgetVersion, CAMOverheadCalculation, CAMOverheadRateCalculationJournalEntry, CAMFormulaAllocationBase
audience: Application User
ms.reviewer: roschlom
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roschlom
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 09d4516c40833771d27db13eac8228bd8c5e0e4a
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/06/2021
ms.locfileid: "6355036"
---
# <a name="overhead-calculation"></a>Útreikningur fastakostnaður

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir dæmigerðum ferlum til að reikna út og úthluta rekstrarkostnaði.

## <a name="term-definition"></a>Skýrsluskilgreining

Stjórnunarkostnaður er sá kostnaður sem stofnað er til fyrir rekstur fyrirtækis, en sem ekki er hægt að rekja beint til neinna sérstakrar starfsemi, vöru eða þjónustu. Stjórnunarkostnaður veitir mikilvægan stuðning við myndun hagnaðarmyndandi verkþátta. Hér eru nokkur dæmi um skilyrði:

-   Leiga
-   Rafmagn
-   Stjórnunarkostnaður

## <a name="overhead-calculation-overview"></a>Yfirlit yfir útreikning fastakostnaðar
Útreikningur fastakostnaðar keyrir reglur kostnaðarbókhalds í réttri röð. Hægt er að keyra útreikning fastakostnaðar margsinnis fyrir sama fjárhagstímabil ef reglum kostnaðarbókhalds hefur verið breytt eða ákveðnar villur hafa fundist. Hver keyrsla á útreikningi fastakostnaðar er geymd og fær einkvæmt útgáfukenni sem gerir kleift að bera saman útreikning í mismunandi útgáfum. Kostnaðarfærslur sem útreikningur fastakostnaðar mynda fá dagsetningu reikningsskila. Dagsetningin bókhald samsvarar lokadagsetning fjárhagstímabilsins sem er dagsetning reikningsskiladagsetning reikningsskila notað í útreikningnum. Einkvæmt útgáfukenni samanstendur af eftirfarandi þáttum:

-   Gerð útgáfu
-   Dagsetning og tími
-   Fjárhagur kostnaðarbókhalds
-   Fjárhagsár
-   Reikningstímabil

Útreikningur fastakostnaðar er keyrður óháð því hver útgáfan er. Þess vegna er hægt að reikna út áætlaða útgáfu á undan raunútgáfu. Útreikningur fastakostnaðar samanstendur af fjórum skrefum, eins og sýnt er á eftirfarandi mynd. Í hverju skrefi er færslubókarhaus stofnaður með bókarfærslum. Þessi færslubókarhaus geymir inntaksgögn fyrir hvert útreikningsþrep. Stefnur og reglur eru notaðar í hverri færslulínu og kostnaðarfærslur eru myndaðar sem úttak. Þess vegna hefurðu ávallt fullan rekjanleika. 

[![Útreikningur fastakostnaðar.](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a>Reikna og úthluta sameiginlegur kostnaði vegna rafmagns
Í Fjárhagsbókhaldi er ákveðinn kostnaður, eins og rafmagn, skráður sem eingreiðsla. Þar af leiðandi er nákvæmar innsýn rekstrarfélags ekki veitt fyrir kostnaðarbókhald. Í kostnaðarbókhaldi verður kostnaður að flæða í gegnum fyrirtækiseiningar til að veita rétta innsýn rekstrarfélags þvert á allar fyrirtækiseiningar og stig. Þetta flæði verður að byggja á annaðhvort nákvæmri færslu notkunar eða sanngjarnri matsreglu. Í fjárhagnum er hægt að bóka rafmagnskostnað eins og sýnt er í eftirfarandi töflu.

<table>
<thead>
<tr>
<th>Dagsetning reikningsskila</th>
<th colspan="2">Kostnaðarstaður</th>
<th colspan="2">Aðallykill</th>
<th>Upphæð í bókhaldsgjaldmiðli</th>
</tr>
</thead>
<tbody>
<tr>
<td>3. janúar 2017</td>
<td>CC099</td>
<td>Sjálfgefin hlutverkamiðstöð</td>
<td>10001</td>
<td>Rafmagn</td>
<td>10.000,00</td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a>Skref 1: Keyra útreikning kostnaðarhegðunar

Sjálfvirkt er að þegar kostnaðarfærslur eru fluttar úr grunngögnum fái þær flokkun kostnaðarhegðunar **Óflokkað** í kostnaðarbókhaldi. Með því að nota stefnureglur kostnaðarhegðunar er hægt að endurflokka kostnaðarfærslur sem annaðhvort **Fastan kostnað** eða **Breytilegan kostnað**.

#### <a name="define-the-cost-behavior-rule"></a>Tilgreinið reglu kostnaðarhegðunar

Í sumum tilfellum er hluti af kostnaði föst þóknun og eftirstandandi kostnaður byggist á notkun. Rafmagnsreikningar stemma oft við þessa skilgreiningu. Þegar tiltekin föst þóknun hefur verið greidd, er greitt fyrir notkun á kílóvattklukkustund (Kwh). Til dæmis ef föst kostnaðarþóknun er 1000.00 sýnir þetta hvernig regla kostnaðarhegðunar er skilgreind:

-   Föst upphæð 1.000,00
    -   0 &lt;= 1.000,00 = Fast
    -   1000.01 &lt; N = Breyta

##### <a name="journal"></a>Færslubók

<table>
<thead>
<tr>
<th>Færslubók</th>
<th>Færslubókargerð</th>
<th colspan="3">Fjárhagsdagatalstímabil</th>
<th>Útgáfa</th>
</tr>
</thead>
<tbody>
<tr>
<td>00001</td>
<td>Færslubók útreiknings fyrir kostnaðarhegðun</td>
<td>Fjárhagur</td>
<td>2017</td>
<td>1. tímabil</td>
<td>Útreikningur fastakostnaðar / 01-02-2017 11:51:00 PM / Fjárhagur /2017 / Tímabil 1</td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a>Færslubókarfærslur (Færslubókarfærslur stöðu kostnaðarhlutar)

<table>
<thead>
<tr>
<th>Dagsetning reikningsskila</th>
<th colspan="2">Kostnaðarhlutur</th>
<th colspan="2">Kostnaðareining</th>
<th>Kostnaðarhegðun</th>
<th>Upphæð</th>
</tr>
</thead>
<tbody>
<tr>
<td>3. janúar 2017</td>
<td>CC099</td>
<td>Sjálfgefin hlutverkamiðstöð</td>
<td>10001</td>
<td>Rafmagn</td>
<td>Óflokkað</td>
<td>10.000,00</td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a>Kostnaðarfærslur

<table>
<thead>
<tr>
<th colspan="2">Kostnaðarhlutur</th>
<th colspan="2">Kostnaðareining</th>
<th>Kostnaðarhegðun</th>
<th>Upphæð</th>
<th>Dagsetning reikningsskila</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC099</td>
<td>Sjálfgefin hlutverkamiðstöð</td>
<td>10001</td>
<td>Rafmagn</td>
<td>Óflokkað</td>
<td>10.000,00</td>
<td>3. janúar 2017</td>
</tr>
<tr>
<td>CC099</td>
<td>Sjálfgefin hlutverkamiðstöð</td>
<td>10001</td>
<td>Rafmagn</td>
<td>Óflokkað</td>
<td>-10.000,00</td>
<td>31. janúar 2017</td>
</tr>
<tr>
<td>CC099</td>
<td>Sjálfgefin hlutverkamiðstöð</td>
<td>10001</td>
<td>Rafmagn</td>
<td>Fastur kostnaður</td>
<td>1.000,00</td>
<td>31. janúar 2017</td>
</tr>
<tr>
<td>CC099</td>
<td>Sjálfgefin hlutverkamiðstöð</td>
<td>10001</td>
<td>Rafmagn</td>
<td>Breytilegur kostnaður</td>
<td>9,000.00</td>
<td>31. janúar 2017</td>
</tr>
</tbody>
</table>

Nánari upplýsingar er að finna í [Stofna og úthluta kostnaðarhegðunarreglu fyrir kostnaðarstýringareiningu](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).
### <a name="step-2-process-the-cost-distribution-calculation"></a>Skref 2: Keyra útreikning kostnaðardreifingar

Kostnaðardreifing er notuð til að endurúthluta kostnaði frá einum kostnaðarhlut til annars eða fleiri kostnaðarhluta með því að nota viðeigandi úthlutunargrunn. Kostnaðardreifing og kostnaðarúthlutun eru ólíkar að því leyti að kostnaðardreifing kemur alltaf upp á stigi aðalkostnaðareiningar upphaflegs verðs.

#### <a name="define-the-cost-distribution-rule"></a>Tilgreinið kostnaðardreifingarreglu

Í Fjárhagsbókhaldi er rafmagnskostnaður oft skráður sem eingreiðsla. Í kostnaðarbókhaldi er þessi nálgun ekki nógu nákvæm. Breytilegur kostnaði þarf að dreifa á staka kostnaðarhluti á sanngjörnum grunni. Rökréttasti úthlutunargrunnurinn er notkun á rafmagni (Kwh). Stofnað er tölfræðilegt víddarstak sem er nefnt Rafmagn og rafmagnsnotkun er skráð. Sjálfgefið er að öll tölfræðileg víddarstök verða tiltæk sem úthlutunargrunnur.

<table>
<thead>
<tr>
<th colspan="2">Kostnaðarhlutur</th>
<th>Kwh</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC001</td>
<td>Mannauður</td>
<td>1.000</td>
</tr>
<tr>
<td>CC002</td>
<td>Fjármál</td>
<td>6,000</td>
</tr>
<tr>
<td>CC003</td>
<td>Smölun</td>
<td>0</td>
</tr>
</tbody>
</table>

Eftirfarandi tafla sýnir niðurstöður þegar rafmagnsnotkun er beitt sem úthlutunargrunni fyrir breytilegan kostnað.

<table>
<thead>
<tr>
<th colspan="2">Kostnaðarhlutur</th>
<th>Mæligildi</th>
<th>Úthlutunarþáttur</th>
<th>Upphæð</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC001</td>
<td>Mannauður</td>
<td>1.000</td>
<td>(1.000 ÷ 7.000) × 9.000,00</td>
<td>1,285.71</td>
</tr>
<tr>
<td>CC002</td>
<td>Fjármál</td>
<td>6,000</td>
<td>(6.000 ÷ 7.000) × 9.000,00</td>
<td>7,714.29</td>
</tr>
<tr>
<td>CC003</td>
<td>Smölun</td>
<td>0</td>
<td>(0 ÷ 7.000) × 9.000,00</td>
<td>0,00</td>
</tr>
</tbody>
</table>

Föstum kostnaði þarf að dreifa jafnt á staka kostnaðarhluti sem hafa notað rafmagn. Hægt er að ná þessa niðurstöðu með því að nota tölfræðilegt víddarstakið Rafmagn í úthlutunargrunni reikniformúlu: (Rafmagn &gt; 0,00) Eftirfarandi tafla sýnir niðurstöður þegar rafmagnsnotkun er beitt sem úthlutunargrunn fyrir breytilegan kostnað.

<table>
<thead>
<tr>
<th colspan="2">Kostnaðarhlutur</th>
<th>Formúla</th>
<th>Mæligildi</th>
<th>Úthlutunarþáttur</th>
<th>Upphæð</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC001</td>
<td>Mannauður</td>
<td>(1.000 &gt; 0,00)</td>
<td>1</td>
<td>(1 ÷ 2) × 1.000,00</td>
<td>500,00</td>
</tr>
<tr>
<td>CC002</td>
<td>Fjármál</td>
<td>(6.000 &gt; 0,00)</td>
<td>1</td>
<td>(1 ÷ 2) × 1.000,00</td>
<td>500,00</td>
</tr>
<tr>
<td>CC003</td>
<td>Smölun</td>
<td>(0 &gt; 0,00)</td>
<td>0</td>
<td>(0 ÷ 2) × 1.000,00</td>
<td>0,00</td>
</tr>
</tbody>
</table>

##### <a name="journal"></a>Færslubók

<table>
<thead>
<tr>
<th>Færslubók</th>
<th>Færslubókargerð</th>
<th colspan="3">Fjárhagsdagatalstímabil</th>
<th>Útgáfa</th>
</tr>
</thead>
<tbody>
<tr>
<td>00002</td>
<td>Útreikningabók kostnaðardreifingar</td>
<td>Fjárhagur</td>
<td>2017</td>
<td>1. tímabil</td>
<td>Útreikningur fastakostnaðar / 01-02-2017 11:51:00 PM / Fjárhagur /2017 / Tímabil 1</td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a>Færslubókarfærslur (Færslubókarfærslur stöðu kostnaðarhlutar)

<table>
<thead>
<tr>
<th>Dagsetning reikningsskila</th>
<th colspan="2">Kostnaðarhlutur</th>
<th colspan="2">Kostnaðareining</th>
<th>Kostnaðarhegðun</th>
<th>Upphæð</th>
</tr>
</thead>
<tbody>
<tr>
<td>31. janúar 2017</td>
<td>CC099</td>
<td>Sjálfgefin hlutverkamiðstöð</td>
<td>10001</td>
<td>Rafmagn</td>
<td>Fastur kostnaður</td>
<td>1.000,00</td>
</tr>
<tr>
<td>31. janúar 2017</td>
<td>CC099</td>
<td>Sjálfgefin hlutverkamiðstöð</td>
<td>10001</td>
<td>Rafmagn</td>
<td>Breytilegur kostnaður</td>
<td>9,000.00</td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a>Kostnaðarfærslur

<table>
<thead>
<tr>
<th colspan="2">Kostnaðarhlutur</th>
<th colspan="2">Kostnaðareining</th>
<th>Kostnaðarhegðun</th>
<th>Upphæð</th>
<th>Dagsetning reikningsskila</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC099</td>
<td>Sjálfgefin hlutverkamiðstöð</td>
<td>10001</td>
<td>Rafmagn</td>
<td>Fastur kostnaður</td>
<td>-1.000,00</td>
<td>31. janúar 2017</td>
</tr>
<tr>
<td>CC001</td>
<td>Mannauður</td>
<td>10001</td>
<td>Rafmagn</td>
<td>Fastur kostnaður</td>
<td>500,00</td>
<td>31. janúar 2017</td>
</tr>
<tr>
<td>CC002</td>
<td>Fjármál</td>
<td>10001</td>
<td>Rafmagn</td>
<td>Fastur kostnaður</td>
<td>500,00</td>
<td>31. janúar 2017</td>
</tr>
<tr>
<td>CC099</td>
<td>Sjálfgefin hlutverkamiðstöð</td>
<td>10001</td>
<td>Rafmagn</td>
<td>Breytilegur kostnaður</td>
<td>-9.000,00</td>
<td>31. janúar 2017</td>
</tr>
<tr>
<td>CC001</td>
<td>Mannauður</td>
<td>10001</td>
<td>Rafmagn</td>
<td>Breytilegur kostnaður</td>
<td>1,285.71</td>
<td>31. janúar 2017</td>
</tr>
<tr>
<td>CC002</td>
<td>Fjármál</td>
<td>10001</td>
<td>Rafmagn</td>
<td>Breytilegur kostnaður</td>
<td>7,714.29</td>
<td>31. janúar 2017</td>
</tr>
</tbody>
</table>

Nánari upplýsingar er að finna í [Stofna og úthluta kostnaðardreifingarreglu fyrir kostnaðarstýringareiningu](tasks/create-assign-cost-distribution-policy-cost-control-unit.md). 

### <a name="step-3-process-the-overhead-rate-calculation"></a>Skref 3: Keyra útreikning sameiginlegs kostnaðar

Sameiginlegur kostnaður er notaður til að rukka einn eða fleiri tilgreinda kostnaðarhluti. Gjöldin byggjast á fyrirframákveðnu kostnaðarhlutfalli og mæligildi úr úthlutuðum úthlutunargrunni. 

#### <a name="define-the-overhead-rate"></a>Skilgreina sameiginlegan kostnað

Kostnaðarhlutur CC001 Mannauður stuðlar að safni innri verka. Stofnað er tölfræðilegt víddarstak sem kallast Mannauðsverk til að mæla notkun mæligilda.

<table>
<thead>
<tr>
<th colspan="2">Kostnaðarhlutur</th>
<th>Tímar</th>
</tr>
</thead>
<tbody>
<tr>
<td>Verk 1</td>
<td>Verk 1</td>
<td>3</td>
</tr>
<tr>
<td>Verk 2</td>
<td>Verk 2</td>
<td>1</td>
</tr>
</tbody>
</table>

Fyrirframákveðið kostnaðarhlutfall fyrir kostnaðarframlag verk hefur verið skilgreint.

<table>
<thead>
<tr>
<th colspan="2">Kostnaðarhlutur</th>
<th>Kostnaðareining</th>
<th>Kostnaðarhegðun</th>
<th>Einingar</th>
<th>Taxti</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC001</td>
<td>Mannauður</td>
<td>10001</td>
<td>Breytilegur kostnaður</td>
<td>1</td>
<td>10</td>
</tr>
</tbody>
</table>

Eftirfarandi tafla sýnir niðurstöður þegar Mannauðsverk eru notuð sem grunnur við úthlutun.

<table>
<thead>
<tr>
<th colspan="2">Kostnaðarhlutur</th>
<th>Mæligildi</th>
<th>Kostnaðareining</th>
<th>Úthlutunarþáttur</th>
<th>Upphæð</th>
</tr>
</thead>
<tbody>
<tr>
<td>Verk 1</td>
<td>Verk 1</td>
<td>3</td>
<td>10001</td>
<td>(3 ÷ 1) × 10,00</td>
<td>30,00</td>
</tr>
<tr>
<td>Verk 2</td>
<td>Verk 2</td>
<td>1</td>
<td>10001</td>
<td>(1 ÷ 1) × 10,00</td>
<td>10,00</td>
</tr>
</tbody>
</table>

##### <a name="journal"></a>Færslubók

<table>
<thead>
<tr>
<th>Færslubók</th>
<th>Færslubókargerð</th>
<th colspan="3">Fjárhagsdagatalstímabil</th>
<th>Útgáfa</th>
</tr>
</thead>
<tbody>
<tr>
<td>00003</td>
<td>Færslubók fyrir útreikning sameiginlegs kostnaðar</td>
<td>Fjárhagur</td>
<td>2017</td>
<td>1. tímabil</td>
<td>Útreikningur fastakostnaðar / 01-02-2017 11:51:00 PM / Fjárhagur /2017 / Tímabil 1</td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a>Bókarfærslur (Bókarfærslur fyrir útreikning sameiginlegs kostnaðar)

<table>
<thead>
<tr>
<th>Dagsetning reikningsskila</th>
<th colspan="2">Kostnaðarhlutur</th>
<th>Mæligildi</th>
</tr>
</thead>
<tbody>
<tr>
<td>31. janúar 2017</td>
<td>Verk 1</td>
<td>Innanhúsverk 1</td>
<td>3,00</td>
</tr>
<tr>
<td>31. janúar 2017</td>
<td>Verk 2</td>
<td>Innanhúsverk 2</td>
<td>1,00</td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a>Kostnaðarfærslur

<table>
<thead>
<tr>
<th colspan="2">Kostnaðarhlutur</th>
<th colspan="2">Kostnaðareining</th>
<th>Kostnaðarhegðun</th>
<th>Upphæð</th>
<th>Dagsetning reikningsskila</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC0001</td>
<td>Mannauður</td>
<td>10001</td>
<td>Rafmagn</td>
<td>Breytilegur kostnaður</td>
<td>-30,00</td>
<td>31. janúar 2017</td>
</tr>
<tr>
<td>Verk 1</td>
<td>Innanhúsverk 1</td>
<td>10001</td>
<td>Rafmagn</td>
<td>Breytilegur kostnaður</td>
<td>30,00</td>
<td>31. janúar 2017</td>
</tr>
<tr>
<td>CC001</td>
<td>Mannauður</td>
<td>10001</td>
<td>Rafmagn</td>
<td>Breytilegur kostnaður</td>
<td>-10,00</td>
<td>31. janúar 2017</td>
</tr>
<tr>
<td>Verk 2</td>
<td>Innanhúsverk 2</td>
<td>10001</td>
<td>Rafmagn</td>
<td>Breytilegur kostnaður</td>
<td>10,00</td>
<td>31. janúar 2017</td>
</tr>
</tbody>
</table>

Nánari upplýsingar er að finna í [Framkvæma útreikning fastakostnaðar](cost-rollup.md#perform-overhead-calculation).

### <a name="step-4-process-the-cost-allocation-calculation"></a>Skref 4: Keyra útreikning kostnaðarúthlutunar

Úthlutun er notuð til að úthluta stöðu kostnaðarhlutar í öðrum kostnaðarhlutum með því að nota úthlutunargrunn. Finance styður gagnvirka úthlutunaraðferð. Í gagnvirkri úthlutunaraðferð er sú sameiginlega þjónusta sem hjálparkostnaðarhlutir skiptast á viðurkennd að fullu. Kerfið ákvarðar sjálfkrafa rétta röð til að framkvæma úthlutun eftir. Stöðu kostnaðarhluta er úthlutað með einum úthlutunargrunni. Úthlutanir þvert á víddir kostnaðarhluta og viðkomandi stök þeirra eru studdar. Úthlutun pöntunarinnar er stjórnað af stýrieiningu kostnaðar. 

[![Gagnkvæm aðferð.](./media/reciprocal-method.png)](./media/reciprocal-method.png)

#### <a name="define-the-cost-allocation"></a>Tilgreinið kostnaðarúthlutun

Hér er einfalt dæmi sem útskýrir hvernig hægt er að rekja flæði kostnaðar. Kostnaðarhlutir CC001 Mannauður leggur til nokkra kostnaðarhluti. Stofnað er tölfræðilegt víddarstak sem kallast Mannauðsþjónusta til að mæla notkun mæligilda.

<table>
<thead>
<tr>
<th colspan="2">Kostnaðarhlutur</th>
<th>Mannauðsþjónusta</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC002</td>
<td>Fjármál</td>
<td>35</td>
</tr>
<tr>
<td>CC003</td>
<td>Smölun</td>
<td>55</td>
</tr>
<tr>
<td>CC004</td>
<td>Pakkning</td>
<td>10</td>
</tr>
</tbody>
</table>

Kostnaðarhlutir CC002 Fjármál leggur til nokkra kostnaðarhluti. Stofnað er tölfræðilegt víddarstak sem kallast Fjármálaþjónusta til að mæla notkun mæligilda.

<table>
<thead>
<tr>
<th colspan="2">Kostnaðarhlutur</th>
<th>Fjármálaþjónusta</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC003</td>
<td>Smölun</td>
<td>65</td>
</tr>
<tr>
<td>CC004</td>
<td>Pakkning</td>
<td>35</td>
</tr>
</tbody>
</table>

Kostnaðarhlutir CC003 Samsetning leggur til nokkra kostnaðarhluti. Meðlimur tölfræðilega víddar sem kallast Mannauður verk er stofnað til að mælvíddarstaka notuðum magnitude.

<table>
<thead>
<tr>
<th colspan="2">Kostnaðarhlutur</th>
<th>Samsetningarþjónusta (tímar)</th>
</tr>
</thead>
<tbody>
<tr>
<td>Afurð 1</td>
<td>Afurð 1</td>
<td>60</td>
</tr>
<tr>
<td>Afurð 2</td>
<td>Afurð 2</td>
<td>20</td>
</tr>
</tbody>
</table>

Kostnaðarhlutir CC004 Umbúðir leggur til nokkra kostnaðarhluti. Stofnað er tölfræðilegt víddarstak sem kallast Umbúðaþjónusta til að mæla notkun mæligilda.

<table>
<thead>
<tr>
<th colspan="2">Kostnaðarhlutur</th>
<th>Umbúðaþjónusta (tímar)</th>
</tr>
</thead>
<tbody>
<tr>
<td>Afurð 1</td>
<td>Afurð 1</td>
<td>80</td>
</tr>
<tr>
<td>Afurð 2</td>
<td>Afurð 2</td>
<td>15</td>
</tr>
</tbody>
</table>

> [!NOTE]
> Hægt er að afleiða tölfræðiaðgerðir eins og framleiðslutíma sem vara notar frá upprunagögnum. Nánari upplýsingar er að finna í [Veitusniðmát tölfræðiaðgerðar](statistical-measure-provider-template.md#statistical-measure-provider-template). Eftirfarandi tafla sýnir niðurstöður þegar mannauðsþjónusta er notuð sem úthlutunargrunnur fyrir heildarkostnað (fastan kostnað og breytilegan kostnað).

<table>
<thead>
<tr>
<th colspan="2">Kostnaðarhlutur</th>
<th>Mæligildi</th>
<th>Úthlutunarþáttur</th>
<th>Upphæð</th>
<th>Kostnaðarhegðun</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC002</td>
<td>Fjármál</td>
<td>35</td>
<td>(35 ÷ 100) × 500,00</td>
<td>175.00</td>
<td>Fastur kostnaður</td>
</tr>
<tr>
<td>CC003</td>
<td>Smölun</td>
<td>55</td>
<td>(55 ÷ 100) × 500,00</td>
<td>275.00</td>
<td>Fastur kostnaður</td>
</tr>
<tr>
<td>CC004</td>
<td>Pakkning</td>
<td>10</td>
<td>(10 ÷ 100) × 500,00</td>
<td>50,00</td>
<td>Fastur kostnaður</td>
</tr>
<tr>
<td>CC002</td>
<td>Fjármál</td>
<td>35</td>
<td>(35 ÷ 100) × 1.245,71</td>
<td>436.00</td>
<td>Breytilegur kostnaður</td>
</tr>
<tr>
<td>CC003</td>
<td>Smölun</td>
<td>55</td>
<td>(55 ÷ 100) × 1.245,71</td>
<td>685.14</td>
<td>Breytilegur kostnaður</td>
</tr>
<tr>
<td>CC004</td>
<td>Pakkning</td>
<td>10</td>
<td>(10 ÷ 100) × 1.245,71</td>
<td>124.57</td>
<td>Breytilegur kostnaður</td>
</tr>
</tbody>
</table>

Eftirfarandi tafla sýnir niðurstöður þegar Fjármálaþjónusta er notuð sem úthlutunargrunnur fyrir heildarkostnað (fastan kostnað og breytilegan kostnað).

<table>
<thead>
<tr>
<th colspan="2">Kostnaðarhlutur</th>
<th>Mæligildi</th>
<th>Úthlutunarþáttur</th>
<th>Upphæð</th>
<th>Kostnaðarhegðun</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC003</td>
<td>Smölun</td>
<td>65</td>
<td>(65 ÷ 100) × (500,00 + 175,00)</td>
<td>438.75</td>
<td>Fastur kostnaður</td>
</tr>
<tr>
<td>CC004</td>
<td>Pakkning</td>
<td>35</td>
<td>(35 ÷ 100) × (500,00 + 175,00)</td>
<td>236.25</td>
<td>Fastur kostnaður</td>
</tr>
<tr>
<td>CC003</td>
<td>Smölun</td>
<td>65</td>
<td>(65 ÷ 100) × (7.714,29 + 436,00)</td>
<td>5,297.69</td>
<td>Breytilegur kostnaður</td>
</tr>
<tr>
<td>CC004</td>
<td>Pakkning</td>
<td>35</td>
<td>(35 ÷ 100) × (7.714,29 + 436,00)</td>
<td>2,852.60</td>
<td>Breytilegur kostnaður</td>
</tr>
</tbody>
</table>

Eftirfarandi tafla sýnir niðurstöður þegar Samsetningarþjónusta er notuð sem úthlutunargrunnur fyrir heildarkostnað (fastan kostnað og breytilegan kostnað).

<table>
<thead>
<tr>
<th colspan="2">Kostnaðarhlutur</th>
<th>Mæligildi</th>
<th>Úthlutunarþáttur</th>
<th>Upphæð</th>
<th>Kostnaðarhegðun</th>
</tr>
</thead>
<tbody>
<tr>
<td>Afurð 1</td>
<td>Afurð 1</td>
<td>60</td>
<td>(60 ÷ 80) × (275,00 + 438,75)</td>
<td>535.31</td>
<td>Fastur kostnaður</td>
</tr>
<tr>
<td>Afurð 2</td>
<td>Afurð 2</td>
<td>20</td>
<td>(20 ÷ 80) × (275,00 + 438,75)</td>
<td>178.44</td>
<td>Fastur kostnaður</td>
</tr>
<tr>
<td>Afurð 1</td>
<td>Afurð 1</td>
<td>60</td>
<td>(60 ÷ 80) × (5.297,69 + 685,14)</td>
<td>4,487.12</td>
<td>Breytilegur kostnaður</td>
</tr>
<tr>
<td>Afurð 2</td>
<td>Afurð 2</td>
<td>20</td>
<td>(20 ÷ 80) × (5.297,69 + 685,14)</td>
<td>1,495.71</td>
<td>Breytilegur kostnaður</td>
</tr>
</tbody>
</table>

Eftirfarandi tafla sýnir niðurstöður þegar Umbúðaþjónusta er notuð sem úthlutunargrunnur fyrir heildarkostnað (fastan kostnað og breytilegan kostnað).

<table>
<thead>
<tr>
<th colspan="2">Kostnaðarhlutur</th>
<th>Mæligildi</th>
<th>Úthlutunarþáttur</th>
<th>Upphæð</th>
<th>Kostnaðarhegðun</th>
</tr>
</thead>
<tbody>
<tr>
<td>Afurð 1</td>
<td>Afurð 1</td>
<td>80</td>
<td>(80 ÷ 95) × (50,00 + 236,25)</td>
<td>241.05</td>
<td>Fastur kostnaður</td>
</tr>
<tr>
<td>Afurð 2</td>
<td>Afurð 2</td>
<td>15</td>
<td>(15 ÷ 95) × (50,00 + 236,25)</td>
<td>45.20</td>
<td>Fastur kostnaður</td>
</tr>
<tr>
<td>Afurð 1</td>
<td>Afurð 1</td>
<td>80</td>
<td>(80 ÷ 95) × (2.852,60 + 124,57)</td>
<td>2,507.09</td>
<td>Breytilegur kostnaður</td>
</tr>
<tr>
<td>Afurð 2</td>
<td>Afurð 2</td>
<td>15</td>
<td>(15 ÷ 95) × (2.852,60 + 124,57)</td>
<td>470.08</td>
<td>Breytilegur kostnaður</td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a>Færslubókarfærslur (Færslubókarfærslur stöðu kostnaðarhlutar)

<table>
<thead>
<tr>
<th>Færslubók</th>
<th>Færslubókargerð</th>
<th colspan="3">Fjárhagsdagatalstímabil</th>
<th>Útgáfa</th>
</tr>
</thead>
<tbody>
<tr>
<td>00004</td>
<td>Færslubók kostnaðarúthlutunar</td>
<td>Fjárhagur</td>
<td>2017</td>
<td>1. tímabil</td>
<td>Útreikningur fastakostnaðar / 01-02-2017 11:51:00 PM / Fjárhagur /2017 / Tímabil 1</td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a>Færslubókarlínur

<table>
<thead>
<tr>
<th>Dagsetning reikningsskila</th>
<th colspan="2">Kostnaðarhlutur</th>
<th colspan="2">Kostnaðareining</th>
<th>Kostnaðarhegðun</th>
<th>Upphæð</th>
</tr>
</thead>
<tbody>
<tr>
<td>31. janúar 2017</td>
<td>CC001</td>
<td>Mannauður</td>
<td>10001</td>
<td>Rafmagn</td>
<td>Fastur kostnaður</td>
<td>500,00</td>
</tr>
<tr>
<td>31. janúar 2017</td>
<td>CC001</td>
<td>Mannauður</td>
<td>10001</td>
<td>Rafmagn</td>
<td>Breytilegur kostnaður</td>
<td>1,245.71</td>
</tr>
<tr>
<td>31. janúar 2017</td>
<td>CC002</td>
<td>Fjármál</td>
<td>10001</td>
<td>Rafmagn</td>
<td>Fastur kostnaður</td>
<td>675.00</td>
</tr>
<tr>
<td>31. janúar 2017</td>
<td>CC002</td>
<td>Fjármál</td>
<td>10001</td>
<td>Rafmagn</td>
<td>Breytilegur kostnaður</td>
<td>8,150.29</td>
</tr>
<tr>
<td>31. janúar 2017</td>
<td>CC003</td>
<td>Smölun</td>
<td>10001</td>
<td>Rafmagn</td>
<td>Fastur kostnaður</td>
<td>713.75</td>
</tr>
<tr>
<td>31. janúar 2017</td>
<td>CC003</td>
<td>Smölun</td>
<td>10001</td>
<td>Rafmagn</td>
<td>Breytilegur kostnaður</td>
<td>5,982.83</td>
</tr>
<tr>
<td>31. janúar 2017</td>
<td>CC003</td>
<td>Pakkning</td>
<td>10001</td>
<td>Rafmagn</td>
<td>Fastur kostnaður</td>
<td>286.25</td>
</tr>
<tr>
<td>31. janúar 2017</td>
<td>CC003</td>
<td>Pakkning</td>
<td>10001</td>
<td>Rafmagn</td>
<td>Breytilegur kostnaður</td>
<td>2,977.17</td>
</tr>
<tr>
<td>31. janúar 2017</td>
<td>Afurð 1</td>
<td>Afurð 1</td>
<td>10001</td>
<td>Rafmagn</td>
<td>Fastur kostnaður</td>
<td>776.36</td>
</tr>
<tr>
<td>31. janúar 2017</td>
<td>Afurð 1</td>
<td>Afurð 1</td>
<td>10001</td>
<td>Rafmagn</td>
<td>Breytilegur kostnaður</td>
<td>6,994.21</td>
</tr>
<tr>
<td>31. janúar 2017</td>
<td>Afurð 2</td>
<td>Afurð 1</td>
<td>10001</td>
<td>Rafmagn</td>
<td>Fastur kostnaður</td>
<td>223.64</td>
</tr>
<tr>
<td>31. janúar 2017</td>
<td>Afurð 2</td>
<td>Afurð 1</td>
<td>10001</td>
<td>Rafmagn</td>
<td>Breytilegur kostnaður</td>
<td>1,965.79</td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a>Kostnaðarfærslur

<table>
<thead>
<tr>
<th colspan="2">Kostnaðarhlutur</th>
<th colspan="2">Kostnaðareining</th>
<th>Kostnaðarhegðun</th>
<th>Upphæð</th>
<th>Dagsetning reikningsskila</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC001</td>
<td>Mannauður</td>
<td>10001</td>
<td>Rafmagn</td>
<td>Fastur kostnaður</td>
<td>-500,00</td>
<td>31. janúar 2017</td>
</tr>
<tr>
<td>CC002</td>
<td>Fjármál</td>
<td>10001</td>
<td>Rafmagn</td>
<td>Fastur kostnaður</td>
<td>175.00</td>
<td>31. janúar 2017</td>
</tr>
<tr>
<td>CC003</td>
<td>Smölun</td>
<td>10001</td>
<td>Rafmagn</td>
<td>Fastur kostnaður</td>
<td>275.00</td>
<td>31. janúar 2017</td>
</tr>
<tr>
<td>CC004</td>
<td>Pakkning</td>
<td>10001</td>
<td>Rafmagn</td>
<td>Fastur kostnaður</td>
<td>50,00</td>
<td>31. janúar 2017</td>
</tr>
<tr>
<td>CC001</td>
<td>Mannauður</td>
<td>10001</td>
<td>Rafmagn</td>
<td>Breytilegur kostnaður</td>
<td>-1.245,71</td>
<td>31. janúar 2017</td>
</tr>
<tr>
<td>CC002</td>
<td>Fjármál</td>
<td>10001</td>
<td>Rafmagn</td>
<td>Breytilegur kostnaður</td>
<td>436.00</td>
<td>31. janúar 2017</td>
</tr>
<tr>
<td>CC003</td>
<td>Smölun</td>
<td>10001</td>
<td>Rafmagn</td>
<td>Breytilegur kostnaður</td>
<td>685.14</td>
<td>31. janúar 2017</td>
</tr>
<tr>
<td>CC004</td>
<td>Pakkning</td>
<td>10001</td>
<td>Rafmagn</td>
<td>Breytilegur kostnaður</td>
<td>124.57</td>
<td>31. janúar 2017</td>
</tr>
<tr>
<td>CC002</td>
<td>Fjármál</td>
<td>10001</td>
<td>Rafmagn</td>
<td>Fastur kostnaður</td>
<td>-675,00</td>
<td>31. janúar 2017</td>
</tr>
<tr>
<td>CC003</td>
<td>Smölun</td>
<td>10001</td>
<td>Rafmagn</td>
<td>Fastur kostnaður</td>
<td>438.75</td>
<td>31. janúar 2017</td>
</tr>
<tr>
<td>CC004</td>
<td>Pakkning</td>
<td>10001</td>
<td>Rafmagn</td>
<td>Fastur kostnaður</td>
<td>236.25</td>
<td>31. janúar 2017</td>
</tr>
<tr>
<td>CC002</td>
<td>Fjármál</td>
<td>10001</td>
<td>Rafmagn</td>
<td>Breytilegur kostnaður</td>
<td>-8.150,29</td>
<td>31. janúar 2017</td>
</tr>
<tr>
<td>CC003</td>
<td>Smölun</td>
<td>10001</td>
<td>Rafmagn</td>
<td>Breytilegur kostnaður</td>
<td>5,297.69</td>
<td>31. janúar 2017</td>
</tr>
<tr>
<td>CC004</td>
<td>Pakkning</td>
<td>10001</td>
<td>Rafmagn</td>
<td>Breytilegur kostnaður</td>
<td>2,852.60</td>
<td>31. janúar 2017</td>
</tr>
<tr>
<td>CC003</td>
<td>Smölun</td>
<td>10001</td>
<td>Rafmagn</td>
<td>Fastur kostnaður</td>
<td>-713,75</td>
<td>31. janúar 2017</td>
</tr>
<tr>
<td>Afurð 1</td>
<td>Afurð 1</td>
<td>10001</td>
<td>Rafmagn</td>
<td>Fastur kostnaður</td>
<td>535.31</td>
<td>31. janúar 2017</td>
</tr>
<tr>
<td>Afurð 2</td>
<td>Afurð 2</td>
<td>10001</td>
<td>Rafmagn</td>
<td>Fastur kostnaður</td>
<td>178.44</td>
<td>31. janúar 2017</td>
</tr>
<tr>
<td>CC003</td>
<td>Smölun</td>
<td>10001</td>
<td>Rafmagn</td>
<td>Breytilegur kostnaður</td>
<td>-5.982,83</td>
<td>31. janúar 2017</td>
</tr>
<tr>
<td>Afurð 1</td>
<td>Afurð 1</td>
<td>10001</td>
<td>Rafmagn</td>
<td>Breytilegur kostnaður</td>
<td>4,487.12</td>
<td>31. janúar 2017</td>
</tr>
<tr>
<td>Afurð 2</td>
<td>Afurð 2</td>
<td>10001</td>
<td>Rafmagn</td>
<td>Breytilegur kostnaður</td>
<td>1,495.71</td>
<td>31. janúar 2017</td>
</tr>
<tr>
<td>CC003</td>
<td>Smölun</td>
<td>10001</td>
<td>Rafmagn</td>
<td>Fastur kostnaður</td>
<td>-286,25</td>
<td>31. janúar 2017</td>
</tr>
<tr>
<td>Afurð 1</td>
<td>Afurð 1</td>
<td>10001</td>
<td>Rafmagn</td>
<td>Fastur kostnaður</td>
<td>241.05</td>
<td>31. janúar 2017</td>
</tr>
<tr>
<td>Afurð 2</td>
<td>Afurð 2</td>
<td>10001</td>
<td>Rafmagn</td>
<td>Fastur kostnaður</td>
<td>45.20</td>
<td>31. janúar 2017</td>
</tr>
<tr>
<td>CC003</td>
<td>Smölun</td>
<td>10001</td>
<td>Rafmagn</td>
<td>Breytilegur kostnaður</td>
<td>-2.977,17</td>
<td>31. janúar 2017</td>
</tr>
<tr>
<td>Afurð 1</td>
<td>Afurð 1</td>
<td>10001</td>
<td>Rafmagn</td>
<td>Breytilegur kostnaður</td>
<td>2,507.09</td>
<td>31. janúar 2017</td>
</tr>
<tr>
<td>Afurð 2</td>
<td>Afurð 2</td>
<td>10001</td>
<td>Rafmagn</td>
<td>Breytilegur kostnaður</td>
<td>470.08</td>
<td>31. janúar 2017</td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a>Niðurstaða
Í Fjárhagsbókhaldi er kostnaður upp á 10.000,00 fyrir rafmagn bókaður á kenni leppkostnaðarstaðar. Þar af leiðandi munu kostnaðarbókarar vita að það þarf að úthluta þessum kostnaði. Í kostnaðarbókhaldi streymir kostnaður þvert á fyrirtækiseiningar og stig, samkvæmt þeim stefnum og reglum sem eru notaðar. Hver kostnaður hefur verið tengdur úthlutunargrunni sem veitir besta mat á úthlutun á kostnaði.

<table>
<thead>
<tr>
<th colspan="2" rowspan="2">Kostnaðareining</th>
<th colspan="9">Kostnaðarhlutur</th>
<th rowspan="2">Samtala</th>
</tr>
<tr>
<th>CC099</th>
<th>CC001</th>
<th>CC002</th>
<th>CC003</th>
<th>CC004</th>
<th>Verk 1</th>
<th>Verk 2</th>
<th>Afurð 1</th>
<th>Afurð 2</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2">10001 Rafmagn</td>
<td style="text-align: right;"><strong>0.00</strong></td>
<td style="text-align: right;"><strong>0.00</strong></td>
<td style="text-align: right;"><strong>0.00</strong></td>
<td style="text-align: right;"><strong>0.00</strong></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><strong>30.00</strong></td>
<td style="text-align: right;"><strong>10.00</strong></td>
<td style="text-align: right;"><strong>7,770.57</strong></td>
<td style="text-align: right;"><strong>2,189.43</strong></td>
<td style="text-align: right;"><strong>10,000.00</strong></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;">Óflokkað</td>
<td style="text-align: right;">0,00</td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;">Fastur kostnaður</td>
<td style="text-align: right;">0,00</td>
<td style="text-align: right;">0,00</td>
<td style="text-align: right;">0,00</td>
<td style="text-align: right;">0,00</td>
<td style="text-align: right;">0,00</td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;">776.36</td>
<td style="text-align: right;">223.64</td>
<td style="text-align: right;"><strong>1,000.00</strong></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;">Breytilegur kostnaður</td>
<td style="text-align: right;">000</td>
<td style="text-align: right;">0,00</td>
<td style="text-align: right;">0,00</td>
<td style="text-align: right;">0,00</td>
<td style="text-align: right;">0,00</td>
<td style="text-align: right;">30,00</td>
<td style="text-align: right;">10,00</td>
<td style="text-align: right;">6,994.21</td>
<td style="text-align: right;">1,965.79</td>
<td style="text-align: right;"><strong>9,000.00</strong></td>
</tr>
</tbody>
</table>

> [!NOTE]
> Þetta efnisatriði sýnir hvernig fyrir aðalkostnaðareiningin 10001 Rafmagn flæðir í gegnum kostnaðarhluti. Þar af leiðandi er þessum sameiginlega kostnaði úthlutað á lægsta stigið í fyrirtækinu. Með öðrum orðum bera kostnaðarhlutir á lægsta stiginu kostnaðinn. Ef þú þarft sjónrænt flæði kostnaðar á milli kostnaðarhluta er hægt að nota stefnureglur samantekins kostnaðar til að gera kostnaðarflæðið sýnilegt. Fyrir frekari upplýsingar skal sjá [Stefna fyrir samantekt kostnaðar og útreikning sameiginlegs kostnaðar](cost-rollup.md).





[!INCLUDE[footer-include](../../includes/footer-banner.md)]