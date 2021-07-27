---
title: Framkvæmd skattaútreiknings hefur áhrif á færslur
description: Í þessu efnisatriði eru gefnar upp upplýsingar um úrræðaleit sem tengist afköstum á skattaútreikningi og áhrif þeirra á færslur.
author: shtao
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 2bb1f22c33de52f9a7bc00b450ce131d4d58d200
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/06/2021
ms.locfileid: "6352835"
---
# <a name="tax-calculation-performance-affects-transactions"></a>Framkvæmd skattaútreiknings hefur áhrif á færslur

[!include [banner](../includes/banner.md)]

Stundum verður færsla fyrir áhrifum af afkastavandamálum skattaútreiknings. Til að leysa úr vandamálinu skal fylgja skrefunum í eftirfarandi hlutum eftir þörfum.

## <a name="review-the-transaction-line-count"></a>Farið yfir færslulínufjöldann

Ákvarða hvort færslan sé með mikinn fjölda lína (til dæmis fleiri en nokkur hundruð). Annars skaltu færa þig yfir í næsta hluta. Ef færsla er ekki með nokkur hundruð línur, skal fresta skattútreikningi. Frekari upplýsingar er að finna í [Virkja frestaðan skattaútreikning í færslubókum](enable-delayed-tax-calculation.md). 

Því næst er hægt að ákvarða hvort eftirfarandi skilyrði séu fyrir hendi:

- Það eru innflutningsfærslur úr stórum skrám.
- Margar lotur vinna úr sama skattaútreikningi á færslu samtímis.
- Færslan hefur margar línur og yfirlitin eru uppfærð í rauntíma. Til dæmis er reiturinn **Reiknuð upphæð virðisaukaskatts** á síðunni **Almenn færslubók** uppfærður í rauntíma þegar reitum línu er breytt.

   [![Reitur reiknaðrar upphæðar virðisaukaskatts á síðu fylgiskjals færslubókar.](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)

Séu einhverju þessara skilyrða til staðar skal fresta skattútreikningnum.

## <a name="review-the-call-stack"></a>Skoða kallastaflann

Farið yfir kallstaflann til að ákvarða hvort skattreikningur er kallaður mörgum sinnum. Annars skaltu færa þig yfir í næsta hluta. Ef kallað er á kallstaflann mörgum sinnum skal fylgja þessum skrefum til að hjálpa til við að stytta tíma skattaútreiknings.

1. Hafi færslubók tekið tillit til færslunnar skal fresta skattútreikningi. Frekari upplýsingar er að finna í [Virkja frestaðan skattaútreikning í færslubókum](enable-delayed-tax-calculation.md).
2. Ef færslan er innkaupapöntun og forritsútgáfan er eldri en 10.0.15 er hægt að fresta skattaútreikningi þar til kemur að endanlegum útreikningi með því að virkja forútgáfu fyrir **PurchTableChangeMgmtDistributionUpdateOnToggle_KillSwitch**.

## <a name="review-the-call-stack-timeline"></a>Farið yfir kallastaflann

Farið yfir tímalínu kallstaflans til að ákvarða hvort eftirfarandi vandamál séu til staðar. Ef svo er skaltu virkja forútgáfuna fyrir **TaxUncommittedDoIsolateScopeFlighting** til að laga vandamálið.

- Færslan veldur því að kerfið hættir að svara þar til lotunni lýkur. Þess vegna getur færslan ekki reiknað út niðurstöður skatts. Eftirfarandi skýringarmynd sýnir skilaboðagluggann „Lotu lauk“ sem þú fékkst.

    [![Skilaboð fyrir lok lotu.](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)

- Aðferðir **TaxUncommitted** taka lengri tíma en aðrar aðferðir. Á eftirfarandi mynd tekur til dæmis aðferðin **TaxUncommitted::updateTaxUncommitted()** 43.347,42 sekúndur, en hinar aðferðirnar taka 0,09 sekúndur.

    [![Tímalengd aðferðar.](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)

## <a name="customizing-and-calling-tax-calculation"></a>Sérstilling og kallað í skattaútreikning

Þegar gerðar eru sérstillingar skal ekki kalla á skattaútreikning með aðferðinni **insert()** eða **update()** fyrir hverja línu. Skattaútreikning ætti að framkalla á færslustigi.

## <a name="determine-whether-customization-exists"></a>Ákvarða hvort sérstilling sé til staðar

Ef þú hefur lokið við skrefin í fyrri hlutum en hefur ekki getað leyst vandamálið skaltu komast að því hvort sérstillingar séu til staðar. Ef engin sérstilling er til skal stofna þjónustubeiðni frá Microsoft til að fá frekari aðstoð.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
