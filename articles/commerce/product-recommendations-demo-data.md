---
title: Fá afurðartillögur með því að nota sýnigögn
description: Þetta skjal veitir leiðbeiningar um hvernig skuldsetja megi ráðleggingar um omni-rás vöru í Tier-1 umhverfi með einum reit með því að nota fyrirfram byggðar, sérhannaðar kynningargögn.
author: bebeale
manager: AnnBe
ms.date: 10/01/19
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 1456feb0665b6ec79a36a3704f17da80ffd759a0
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042781"
---
# <a name="get-product-recommendations-using-demo-data"></a>Fá afurðartillögur með því að nota sýnigögn
Þetta skjal veitir leiðbeiningar um hvernig skuldsetja megi ráðleggingar um omni-rás vöru í Tier-1 umhverfi með einum reit með því að nota fyrirfram byggðar, sérhannaðar kynningargögn.

Ráðleggingar með Omni-rásum bjóða upp á safn ritstjóralista eða forritaðs myndaðs lista yfir vörur. Hægt er að nota þessa lista í nokkrum tilfellum, allt eftir viðskiptaþörf. Nánari upplýsingar um afurðatillögur er að finna í [yfirliti yfir afurðatillögur í POS-skjölum](product-recommendations.md).

Fyrir Tier-2 og hærra umverfi Dynamics 365 eru afurðatillögur sjálfkrafa reiknaðar út frá gögnum viðskiptavina. Með því að nota kynningargögn um vörur er ekki gert ráð fyrir neinum lausnum sem hafa þegar verið veittar í umhverfinu og kostnaði sem tengist notkun þeirra.

Fyrir Tier-1 umhverfi eru afurðatillögur byggðar eingöngu á stöðluðum kynningu gagna sem geymd eru í .csv-skrá.

## <a name="enabling-product-recommendations-demo-data-in-an-environment"></a>Kveikir á kynningu gagna um kynningu í umhverfi
Til að virkja kynningargögn afurðatillagna þarftu að setja upp Dynamics 365 Commerce Forskoða kynningarviðbót í viðkomandi umhverfi. Með því að gera það sjálfkrafa er gert ráð fyrir kynningu gagna um afurðatillögur.

## <a name="default-demo-data"></a>Sjálfgefin sýndargögn
Hver umhverfisgerð Onebox er með forsóttu safni af kynningargögnum afurðatillagna sem eru geymd í kommuaðskildri 'reco_demo_data.csv' skrá, sem er staðsett í sömu möppu og þetta skjal á Commerce Scale Unit.

Gögnin eru byggð upp meðfram eftirfarandi dálkum.

| Heiti dálks         | Skylda          | Lýsing                                                                                                                                 | Möguleg gildi                                                              |
|---------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| RecoList            | :heavy_check_mark: | Sú sértæka gerð afurðatilmælalistans sem kynningargagnapunkturinn á að mynda.                                                    | <ul><li>RecoBestSelling</li><li>RecoNew</li><li>RecoTrending</li><li>RecoCart</li><li>RecoPeopleAlsoBuy</li></ul> |
| OperatingUnitNumber | :heavy_check_mark: | Sértækt númer rekstrareiningarinnar þar sem gert er ráð fyrir að yfirborð vöru tilmæli komi upp.                                        |                                                                              |
| Tegund            |                    |    Skila skal flokknum fyrir viðkomandi lista. Ef enginn flokkur er tilgreindur er listinn aðeins efst í stýriveldi.    |                                                                              |
| SeedItemId          |                    |    Fyrir lista sem þurfa fræ (RecoPeopleAlsoBuy og RecoCart) vöruna sem listarnir ættu að sýna viðbótarafurðir fyrir.            |                                                                              |
| ItemIds             | :heavy_check_mark: | Ein eða fleiri vörur sem á að skila í kjölfarið, aðskilin með ';'.                                                                  |                                                                              |

## <a name="customize-demo-data"></a>Sérsníða sýndargögn
Hægt er að breyta sjálfgefnum kynningargögnum með hvaða vöru- og flokkaupplýsingum sem eru stilltar í HQ. Þegar búið er að uppfæra .csv endurspegla afurðatillögurnar sem eru sendar til viðskiptavina strax breytingarnar.

Viðbyggingin hefur að geyma gagnapakka sem kallast RecoMockDataset.csv sem gerir þér kleift að stjórna gagnapakkanum sem er notað til að knýja fram niðurstöður ráðlegginga um spotta. Hægt er að stjórna skráarheitinu með viðbótarstillingum með því að nota stillinguna **ext.Recommendations.DemoFilePath**. Þetta gerir þér kleift að hafa mörg gagnapakkar tiltækar sem auðvelt er að skipta á milli í gegnum stillingar.


```xml
<settings>
    <add name="ext.Recommendations.DemoFilePath" value="RecoMockDataset.csv" />
</settings>
```

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit yfir afurðarráðleggingar](product-recommendations.md)

[Umhverfisskipulagning](../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md)
