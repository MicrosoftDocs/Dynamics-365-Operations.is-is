---
title: Búðu til tillögur með kynningargögnum
description: Þetta efni veitir leiðbeiningar um hvernig skuldsetja megi ráðleggingar um omni-rás vöru í Tier-1 umhverfi með einum reit með því að nota fyrirfram byggðar, sérhannaðar kynningargögn.
author: bebeale
manager: AnnBe
ms.date: 05/26/2020
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
ms.openlocfilehash: cca6913375eec2565852676f3c1da5a67f71e14f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4413031"
---
# <a name="create-recommendations-with-demo-data"></a>Búðu til tillögur með kynningargögnum

[!include [banner](includes/banner.md)]

Þetta efni veitir leiðbeiningar um hvernig skuldsetja megi ráðleggingar um omni-rás vöru í Tier-1 umhverfi með einum reit með því að nota fyrirfram byggðar, sérhannaðar kynningargögn.

Ráðleggingar með Omni-rásum bjóða upp á safn ritstjóralista eða forritaðs myndaðs lista yfir vörur. Hægt er að nota þessa lista í nokkrum tilfellum, allt eftir viðskiptaþörf. Nánari upplýsingar um afurðatillögur er að finna í [yfirliti yfir afurðatillögur í POS-skjölum](product-recommendations.md).

Fyrir Tier-2 og hærra umverfi Dynamics 365 eru afurðatillögur sjálfkrafa reiknaðar út frá gögnum viðskiptavina. Með því að nota kynningargögn um vörur er ekki gert ráð fyrir neinum lausnum sem hafa þegar verið veittar í umhverfinu og kostnaði sem tengist notkun þeirra.

Fyrir Tier-1 umhverfi eru afurðatillögur byggðar eingöngu á stöðluðum kynningu gagna sem geymd eru í .csv-skrá.

## <a name="enabling-product-recommendations-demo-data-in-an-environment"></a>Kveikir á kynningu gagna um kynningu í umhverfi
Til að virkja kynningargögn afurðatillagna þarftu að setja upp Dynamics 365 Commerce Forskoða kynningarviðbót í viðkomandi umhverfi. Með því að gera það sjálfkrafa er gert ráð fyrir kynningu gagna um afurðatillögur.

## <a name="default-demo-data"></a>Sjálfgefin sýndargögn
Hver umhverfisgerð OneBox er með forsóttu safni af kynningargögnum afurðatillagna sem eru geymd í kommuaðskildri 'reco_demo_data.csv' skrá, sem er staðsett í sömu möppu og þetta skjal á Commerce Scale Unit.

Gögnin eru byggð upp meðfram eftirfarandi dálkum.

| Dálkheiti         | Skylda          | lýsing                                                                                                                                 | Möguleg gildi                                                              |
|---------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| RecoList            | :heavy_check_mark: | Sú sértæka gerð afurðatilmælalistans sem kynningargagnapunkturinn á að mynda.                                                    | <ul><li>RecoBestSelling</li><li>RecoNew</li><li>RecoTrending</li><li>RecoCart</li><li>RecoPeopleAlsoBuy</li></ul> |
| OperatingUnitNumber | :heavy_check_mark: | Sértækt númer rekstrareiningarinnar þar sem gert er ráð fyrir að yfirborð vöru tilmæli komi upp.                                        |                                                                              |
| Tegund            |                    |    Skila skal flokknum fyrir viðkomandi lista. Ef enginn flokkur er tilgreindur er listinn aðeins efst í stýriveldi.    |                                                                              |
| SeedItemId          |                    |    Fyrir lista sem þurfa fræ (RecoPeopleAlsoBuy og RecoCart) vöruna sem listarnir ættu að sýna viðbótarafurðir fyrir.            |                                                                              |
| CustomerId          |                    |    Fyrir lista sem krefjast auðkenni viðskiptavina (RecoPicks).  Sjálfgefið gildi '0' á við um alla viðskiptavini.          |                                                                              |
| ItemIds             | :heavy_check_mark: | Ein eða fleiri vörur sem á að skila í kjölfarið, aðskilin með ';'.                                                                  |                                                                              |

## <a name="customize-demo-data"></a>Sérsníða sýndargögn
Hægt er að breyta sjálfgefnum kynningargögnum með hvaða vöru- og flokkaupplýsingum sem eru stilltar í HQ. Þegar búið er að uppfæra .csv endurspegla afurðatillögurnar sem eru sendar til viðskiptavina strax breytingarnar.

Viðbyggingin hefur að geyma gagnapakka sem kallast „RecoMockDataset.csv” sem gerir þér kleift að stjórna gagnapakkanum sem er notað til að knýja fram niðurstöður ráðlegginga um spotta. Hægt er að stjórna skráarheitinu með viðbótarstillingum með því að nota stillinguna **ext.Recommendations.DemoFilePath**. Þetta gerir þér kleift að hafa mörg gagnapakkar tiltækar sem auðvelt er að skipta á milli í gegnum stillingar.


```xml
<settings>
    <add name="ext.Recommendations.DemoFilePath" value="RecoMockDataset.csv" />
</settings>
```

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit yfir afurðarráðleggingar](product-recommendations.md)

[Virkja Azure Data Lake Storage í Dynamics 365 Commerce-umhverfi](enable-adls-environment.md)

[Virkja ráðleggingar um afurðir](enable-product-recommendations.md)

[Kveikja á sérsniðnum tillögum](personalized-recommendations.md)

[Afþakka sérsniðnar tillögur](personalization-gdpr.md)

[Virkja tillögur um að kaupa svipaða vöru](shop-similar-looks.md)

[Bæta við afurðatillögum á sölustað](product.md)

[Bæta tillögum við færsluskjáinn](add-recommendations-control-pos-screen.md)

[Aðlagaðu niðurstöður AI-ML](modify-product-recommendation-results.md)

[Búðu til handvirkt myndaðar ráðleggingar](create-editorial-recommendation-lists.md)

[Algengar spurningar um afurðaráðleggingar](faq-recommendations.md)
