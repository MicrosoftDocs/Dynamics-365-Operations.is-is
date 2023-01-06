---
title: Skrá afskriftir afnotaréttar af eign (forskoðun)
description: Þessi grein útskýrir hvernig á að stofna bókarfærsluna fyrir þær afskriftir sem eru nauðsynlegar fyrir leigusamninga sem eru viðurkenndir á efnahagsreikningi fyrirtækis.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseAssetSchedule
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 93e521cf409af4c01d625f27bdd7a7564e471bd9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8903277"
---
# <a name="record-right-of-use-asset-depreciation-preview"></a>Skrá afskriftir afnotaréttar af eign (forskoðun)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]


Fyrir leigur sem eru viðurkenndar á efnahagsreikningi fyrirtækis er afnotaréttur af eign afskrifuð mánaðarlega. Þessi grein útskýrir hvernig á að stofna bókarfærsluna fyrir afskriftir. Afskrift debetfærir fjárhagslykil kostnaðar og kreditfærir uppsafnaða afskrift fjárhagslykils, byggt á uppsetningu bókunarreglu og gerðar leigusamnings. Hægt er að stofna þessar færslur fyrir hvern leigusamning, en einnig er hægt að stofna þær fyrir marga leigusamninga með því að nota runubókarvirkni.

## <a name="asset-depreciation-schedule"></a>Afskriftaráætlun eignar

1. Á síðunni **Samantekt leigu** skal velja leigusamning. Veljið síðan **Bækur \> Afskriftaráætlun eignar** til að opna síðuna **Afskriftaráætlun eignar**.

    Bókarfærsla afskriftarkostnaðar afnotaréttar af eign er byggð á upphæðinni í dálknum **Afskriftarkostnaður**. Dæmi um leiðbeiningar um reglufylgni við bókunarstaðla er að finna í [útreikningur á afskriftarkostnaði afnotaréttar á eign fyrir fjármögnunarleigusamninga](#calculation-of-rou-asset-amortization-expense-for-finance-leases) hlutanum síðar í þessari grein.
    
2. Veljið afskriftartímabil og síðan **Stofna færslubók**. Þú færð skilaboð sem segir til um að færslubókin sem verður notuð til að skrá afskriftir hafi verið stofnuð.
3. Veljið **Færslubækur \> Eignarleigufærslubækur** til að opna **Eignaleigufærslubók** , þar sem hægt er að skoða færslubókarfærsluna fyrir afskriftakostnað sem var stofnaður.

   Kerfið læsir tilteknum fjármálareitum frá því að vera breytt til að koma í veg fyrir frávik á milli færslanna og áætlana. Sumir reitir sem eru læstir eru m.a.: **Lykill**, **Upphæðir**, **Fjárhagsvíddir**, **Gjaldmiðill** og **Færslugerð**. Auk þess getur þú ekki bætt við eða eytt færslulínum færslubókar í neinum færslum eignarleigubókar því það gæti valdið frávikum á milli áætlana og færslnanna.

4. Veljið bókarfærsluna og síðan **Bóka** til að skrá afskriftafærsluna í fjárhag.

## <a name="calculation-of-rou-asset-amortization-expense-for-operating-leases"></a>Útreikningur á kostnaði við afskriftir eigna fyrir rekstrarleigusamninga

Afskriftarkostnaður vegna rekstrarleigusamninga er reiknaður sem mismunur mánaðarlegrar línulegrar leigutekna og mánaðarlegra vaxta á leiguskuldbindingu, í samræmi við efnisatriði um skráningarkerfi reikningsskilastaðla 842 (ASC 842), en það er staðall fyrir almennt samþykktar reikningsskilareglur í Bandaríkjunum (US GAAP). Línulega leigukostnaður er reiknaður sem samtala allra leigugreiðslna deilt með leigutíma í mánuðum. (Samtala leigugreiðslna felur í sér hvers kyns fyrirframgreiðslur, upphaflegur beinn kostnaður, kostnaður sundurhlutunar og leiguhvata.) Eftirfarandi tafla sýnir dæmi um afskriftarkostnað vegna rekstrarleigusamninga.

### <a name="example-of-rou-asset-amortization-expense-for-operating-leases"></a>Dæmi um afskriftarkostnað afnotaréttar af eign fyrir rekstrarleigusamninga

| Svæði                                          | Virði       |
|------------------------------------------------|-------------|
| Upphæð greiðslu                                 | 1.000       |
| Greiðslutíðni                              | Mánaðarlega     |
| Leigutími (mánuðir)                            | 24          |
| Leigugreiðslur alls                           | 24,000      |
| Vextir á nýju lánsfé                     | 5%          |
| Tegund afborgunar                                   | Framsettar afborganir |
| Samsett tímabil                           | Mánaðarlega     |
| Táknar núvirði á lágmarksgreiðslum á leigu í framtíðinni | 22,888.87   |

Eins og áður var getið er línulega leigukostnaður reiknaður sem samtala allra greiðslna deilt með leigutíma. Kerfið reiknar sjálfkrafa mánaðarlegan vaxtakostnað í áætlun um afskrift skulda. Vaxtakostnaðurinn er reiknaður með því að nota aðferðina með virkum vöxtum. Kerfið mun nota línulegan leigukostnað til að draga frá vaxtakostnað fyrir hvern mánuð. Gildið er notað til að minnka afnotarétt af eign.

| Mánuður | Línulegur leigukostnaður | Vaxtakostnaður                        | Útreikningur á afskriftarkostnaði afnotaréttar af eign |
|-------|--------------------------|-----------------------------------------|-----------------------------------------------|
| 1     | (24.000 ÷ 24) = 1.000,00 | (22.888,87 – 1.000) × (5% ÷ 12) = 91,20 | 1.000 – 91,20 = 908,80                        |
| 2     | (24.000 ÷ 24) = 1.000,00 | (21.980,08 – 1.000) × (5% ÷ 12) = 87,42 | 1.000 – 87,42 = 912,58                        |
| 3     | (24.000 ÷ 24) = 1.000,00 | (21.067,49 – 1.000) × (5% ÷ 12) = 83,62 | 1.000 – 83,62 = 916,39                        |

> [!NOTE]
> Samkvæmt ASC 842 er afskrift afnotaréttar af eign fyrir rekstrarleigusamning flokkuð sem leigukostnaður á rekstrarreikning. Fyrir sýnileika lýsir Eignarleiga færslunni sem afskrift á afnotarétti að eign. Hins vegar ætti að úthluta debetfærslunni á kostnaðarlykil fyrir rekstrarleigusamning og kreditfærslunni skal úthlutað beint á afnotaréttur af eign fyrir rekstrarleigusamning. Engu að síður, í færibreytum leigusamnings, er hægt að tilgreina að kreditfærslur eigi að vera gerðar á uppsöfnuðum afskriftarreikningi fyrir afnotaréttur af eign í rekstri.

Ef leiga er flokkaður sem rekstrarleiga verða mánaðarlegar afskriftir eftir skerðingu reiknaðar með línulegum afskriftum.

## <a name="calculation-of-rou-asset-amortization-expense-for-finance-leases"></a>Útreikningur á afskriftarkostnaði afnotaréttar af eign fyrir fjármögnunarleigusamninga

Fyrir leigusamninga sem eru með fjármálaflokkun reiknar kerfið afskriftir af afnotarétti á eign á línulegum grundvelli. Þess vegna verður afskriftarkostnaður sá sami fyrir hvern mánuð.

Í samræmi við alþjóðlegan reikningsskilastaðal 16 (IFRS 16) og ASC 842 verður eignin afskrifuð á annað hvort leigutímanum eða nýtingartíma eignarinnar, hvor sem er styttri. Að auki, ef kveikt er á **Flutningi eignarréttar** færibreytu fyrir leigusamning, verður leigusamningurinn sjálfkrafa afskrifuð yfir nýtingatíma eignarinnar.

### <a name="example-of-rou-asset-amortization-expense-for-finance-leases"></a>Dæmi um afskriftarkostnað afnotaréttar af eign fyrir fjármögnunarleigusamninga

| Svæði                                | Virði                                   |
|--------------------------------------|-----------------------------------------|
| Upphaf stöðu afnotaréttar af eign | 22,889.87                               |
| Leigutími (mánuðir)                  | 24                                      |
| Nýtingartími eignar (mánuðir)           | 36                                      |
| Mánuður                                | Afskriftarkostnaðar afnotaréttar af eign |
| 1                                    | 22.889.87 ÷ 24 = 953,74                 |
| 2                                    | 22.889.87 ÷ 24 = 953,74                 |
| 3                                    | 22.889.87 ÷ 24 = 953,74                 |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
