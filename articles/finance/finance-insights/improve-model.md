---
title: Bæta spálíkanið
description: Þetta efnisatriði lýsir eiginleikum sem hægt er að nota til að bæta afköst spálíkana.
author: ShivamPandey-msft
ms.date: 07/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 804c18c1b165fff99390db1fda22da0137249373
ms.sourcegitcommit: e40a9fac5bac9f57a6dcfe73a1f21856eab9b6a9
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 10/02/2021
ms.locfileid: "7595038"
---
# <a name="improve-the-prediction-model"></a>Bæta spálíkanið

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir eiginleikum sem hægt er að nota til að bæta afköst spálíkana. Þú byrjar á því að bæta líkanið á vinnusvæðinu **Greiðsluspár viðskiptavinar** í Microsoft Dynamics 365 Finance. Umbótaskrefunum er svo lokið í AI Builder.

## <a name="select-historical-outcomes"></a>Velja sögulegar niðurstöður

Þú velur fyrst eina eða fleiri af þremur mögulegum niðurstöðum fyrir reikninga: **Á réttum tíma**, **Seint** og **mjög seint**. Velja ætti allar þrjár niðurstöður. Þegar val niðurstaðnanna er hreinsað verða reikningar síaðir út úr þjálfunarferlinu og nákvæmni spárinnar minnkar.

[![Staðfestir niðurstöður.](./media/confirm-3-outcomes.png)](./media/confirm-3-outcomes.png)

Ef fyrirtækið krefst aðeins tveggja niðurstaðna skal breyta **Seint** og **Mjög seint** viðmiðunarmörkunum í 0 (núll) daga. Á þennan hátt er hægt að draga spána saman í tvíundarstöðuna **Á réttum tíma** eða **Seint**.

## <a name="select-fields"></a>Velja svæði

Þegar þú velur svæði til að taka með í líkaninu skaltu hafa í huga að listinn inniheldur öll tiltæk svæði í Microsoft Dataverse -töflunni sem er varpað í gögnin í Azure Data Lake. Suma þessa reiti ætti **ekki** að velja. Reitirnir sem ættu ekki að vera valdir falla undir einn af þremur flokkum:

- Reiturinn er áskilinn fyrir Dataverse töfluna en engin gögn eru til staðar fyrir það í Data Lake.
- Svæðið er auðkenni og er því óskiljanlegt fyrir vélnámseiginleika.
- Reiturinn sýnir upplýsingar sem verða ekki í boði við spá.

Eftirfarandi kaflar sýna svæðin sem eru tiltæk fyrir einingar reikninga og viðskiptavina og listi yfir svæðin sem ætti **ekki** að velja til þjálfunar. Flokkurinn sem er tilgreindur fyrir hvert þessara svæða vísar í flokkana í listanum þar á undan.
 
### <a name="invoice-dataverse-table"></a>Reikningur Dataverse tafla

Eftirfarandi mynd sýnir reitina sem eru í boði fyrir reikningstöfluna.

[![Tiltæk svæði fyrir reikningstöfluna.](./media/available-fields.png)](./media/available-fields.png)

Eftirfarandi reitir ættu ekki að vera valdir fyrir þjálfun:

- **Reikningslykill** (flokkur 2)
- **Er lokað** (flokkur 3) – Þetta svæði er notað til að sía reikninga fyrir þjálfun (lokað) og spá (ekki lokað).
- **Heiti** (flokkur 1)
- **Upprunakenni** (flokkur 2)
- **Upprunafærsla** (flokkur 2)
- **Upprunatafla** (flokkur 2)

### <a name="customer-dataverse-table"></a>Viðskiptavinur Dataverse tafla

Eftirfarandi mynd sýnir reitina sem eru í boði fyrir viðskiptavinatöfluna.

[![Tiltæk svæði fyrir viðskiptavinatöfluna.](./media/related-entities.png)](./media/related-entities.png)

Ekki ætti að velja eftirfarandi reit fyrir þjálfun:

- **Einkvæm lykillína** (flokkur 2)

## <a name="filters"></a>Síur

Hægt er að sía reikninga sem eru notaðir til þjálfunar með því að stilla síuskilyrðið fyrir reiti á reikningnum eða í viðskiptavinatöflunum. Til dæmis er hægt að setja þröskuld sem inniheldur aðeins reikninga þar sem heildarupphæðin er jöfn eða hærri en tiltekin upphæð. Einnig er hægt að útiloka reikninga sem tengjast viðskiptavinum í ákveðnum viðskiptavinahópi.

Frekari upplýsingar um síun gagna er að finna í [Búa til spálíkan](/ai-builder/prediction-create-model#filter-your-data).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
