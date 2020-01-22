---
title: Upplýsingar um kynningu á kynningu á afurðarásum
description: Þetta skjal miðar að því að veita leiðbeiningar um hvernig skuldsetja megi ráðleggingar um omni-rás vöru í Tier-1 umhverfi með einum reit með því að nota fyrirfram byggðar, sérhannaðar kynningargögn.
author: bebeale
manager: AnnBe
ms.date: 12/1/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-07-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 31aa5dbd2fa814fd572024a4ae36b9d9b46a2fb0
ms.sourcegitcommit: 398c0652acde12c953de007d06055456d6e0a516
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/02/2019
ms.locfileid: "2872327"
---
# <a name="omni-channel-product-recommendations-demo-data"></a>Upplýsingar um kynningu á kynningu á afurðarásum

Þetta skjal miðar að því að veita leiðbeiningar um hvernig skuldsetja megi ráðleggingar um omni-rás vöru í Tier-1 umhverfi með einum reit með því að nota fyrirfram byggðar, sérhannaðar kynningargögn.

Ráðleggingar með Omni-rásum bjóða upp á safn ritstjóralista eða forritaðs myndaðs lista yfir vörur. Hægt er að nota þessa lista í nokkrum tilfellum, allt eftir viðskiptaþörf. Nánari upplýsingar um ráðleggingarlista vöru er að finna í [yfirliti yfir ráðleggingar um vörur í POS-skjölum.](../commerce/product-recommendations.md)

Fyrir Tier-2 og hærra Dynamics Environments eru ráðleggingar sjálfkrafa reiknaðar út frá gögnum viðskiptavina.
Með því að nota kynningargögn um vörur er ekki gert ráð fyrir neinum lausnum sem hafa þegar verið veittar í umhverfinu og kostnaði sem tengist notkun þeirra.

Fyrir Tier-1 umhverfi eru tillögur vöru byggðar eingöngu á stöðluðum kynningu gagna sem geymd eru í csv skrá.

## <a name="enabling-product-recommendations-demo-data-in-an-environment"></a>Kveikir á kynningu gagna um kynningu í umhverfi

Viðskiptavinir þurfa að dreifa **Dynamics 365 Commerce Forskoða framlengingu á kynningu** í viðkomandi umhverfi, sem gerir sjálfkrafa kynningu á vöruupplýsingum kynningu gagna.

## <a name="default-demo-data"></a>Sjálfgefin sýndargögn
Hvert umhverfi gerð Onebox er með forhlaðnum safni af kynningum um vöruafmæli sem eru geymd í dái sem aðskilin eru **'reco_demo_data.csv'** skrá, sem er staðsett í sömu möppu og þetta skjal á smásöluþjóninum.

Þessi gögn eru byggð upp meðfram eftirfarandi dálkum

| Dálkheiti         | Skylda          | Lýsing                                                                                                                                 | Möguleg gildi                                                              |
|---------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| RecoList            | :heavy_check_mark: | Sértæk tegund vöru tilmæla listans sem kynningargagnapunkturinn er að búa til.                                                    | <ul><li>RecoBestSelling</li><li>RecoNew</li><li>RecoTrending</li><li>RecoCart</li><li>RecoPeopleAlsoBuy</li></ul> |
| OperatingUnitNumber | :heavy_check_mark: | Sértækt númer rekstrareiningarinnar þar sem gert er ráð fyrir að yfirborð vöru tilmæli komi upp.                                        |                                                                              |
| Tegund            |                    |    Skila skal flokknum fyrir viðkomandi lista. Ef enginn flokkur er tilgreindur er listinn aðeins efst í stýriveldi.    |                                                                              |
| SeedItemId          |                    |    Fyrir lista sem þurfa fræ (RecoPeopleAlsoBuy og RecoCart) vöruna sem listarnir ættu að sýna viðbótarafurðir fyrir.            |                                                                              |
| ItemIds             | :heavy_check_mark: | Ein eða fleiri vörur sem á að skila í kjölfarið, aðskilin með **';'**.                                                                  |                                                                              |


## <a name="customize-demo-data"></a>Sérsníða sýndargögn
Viðskiptavinir geta breytt sjálfgefnum kynningargögnum með hvaða vöru- og flokkaupplýsingum sem eru stilltar í HQ. Þegar búið er að uppfæra CSV endurspegla vörutillögurnar sem eru sendar til viðskiptavina strax breytingarnar.

Viðbyggingin hefur að geyma gagnapakka sem kallast RecoMockDataset.csv sem gerir viðskiptavininum kleift að stjórna gagnapakkanum sem er notað til að knýja fram niðurstöður ráðlegginga um spotta. Hægt er að stjórna skráarheitinu með viðbótarstillingum með því að nota stillinguna **ext.Recommendations.DemoFilePath**. Þetta gerir viðskiptavinum kleift að hafa mörg gagnapakkar tiltækar sem auðvelt er að skipta á milli í gegnum stillingar.

```
  <settings>
    <add name="ext.Recommendations.DemoFilePath" value="RecoMockDataset.csv" />
  </settings>
```

## <a name="additional-resources"></a>Frekari upplýsingar

[yfirlit yfir ráðleggingar um afurðir](../commerce/product-recommendations.md)

[Umhverfisskipulagning](../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md)
