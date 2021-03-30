---
title: Bæta spálíkanið (forskoðun)
description: Þetta efnisatriði lýsir eiginleikum sem hægt er að nota til að bæta afköst spálíkana.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 1028af6e702f2118fabcbc71b17daca36072c691
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5208462"
---
# <a name="improve-the-prediction-model-preview"></a>Bæta spálíkanið (forskoðun)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Þetta efnisatriði lýsir eiginleikum sem hægt er að nota til að bæta afköst spálíkana. Þú byrjar á því að bæta líkanið á vinnusvæðinu **Greiðsluspár viðskiptavinar** í Microsoft Dynamics 365 Finance. Umbótaskrefunum er svo lokið í AI Builder.

## <a name="select-historical-outcomes"></a>Velja sögulegar niðurstöður

Þú velur fyrst eina eða fleiri af þremur mögulegum niðurstöðum fyrir reikninga: **Á réttum tíma**, **Seint** og **mjög seint**. Velja ætti allar þrjár niðurstöður. Þegar val niðurstaðnanna er hreinsað verða reikningar síaðir út úr þjálfunarferlinu og nákvæmni spárinnar minnkar.

[![Staðfestir niðurstöður](./media/confirm-3-outcomes.png)](./media/confirm-3-outcomes.png)

Ef fyrirtækið krefst aðeins tveggja niðurstaðna skal breyta **Seint** og **Mjög seint** viðmiðunarmörkunum í 0 (núll) daga. Á þennan hátt er hægt að draga spána saman í tvíundarstöðuna **Á réttum tíma** eða **Seint**.

## <a name="select-fields"></a>Velja svæði

Þegar þú velur svæði til að taka með í líkaninu skaltu hafa í huga að listinn inniheldur öll tiltæk svæði í Microsoft Dataverse -töflunni sem er varpað í gögnin í Azure Data Lake. Suma þessa reiti ætti **ekki** að velja. Reitirnir sem ættu ekki að vera valdir falla undir einn af þremur flokkum:

- Reiturinn er áskilinn fyrir Dataverse töfluna en engin gögn eru til staðar fyrir það í Data Lake.
- Svæðið er auðkenni og er því óskiljanlegt fyrir vélnámseiginleika.
- Reiturinn sýnir upplýsingar sem verða ekki í boði við spá.

Eftirfarandi kaflar sýna svæðin sem eru tiltæk fyrir einingar reikninga og viðskiptavina og listi yfir svæðin sem ætti **ekki** að velja til þjálfunar. Flokkurinn sem er tilgreindur fyrir hvert þessara svæða vísar í flokkana í listanum þar á undan.
 
### <a name="invoice-dataverse-table"></a>Reikningur Dataverse tafla

Eftirfarandi mynd sýnir reitina sem eru í boði fyrir reikningstöfluna.

[![Tiltæk svæði fyrir reikningstöfluna](./media/available-fields.png)](./media/available-fields.png)

Eftirfarandi reitir ættu ekki að vera valdir fyrir þjálfun:

- **Reikningslykill** (flokkur 2)
- **Er lokað** (flokkur 3) – Þetta svæði er notað til að sía reikninga fyrir þjálfun (lokað) og spá (ekki lokað).
- **Heiti** (flokkur 1)
- **Upprunakenni** (flokkur 2)
- **Upprunafærsla** (flokkur 2)
- **Upprunatafla** (flokkur 2)

### <a name="customer-dataverse-table"></a>Viðskiptavinur Dataverse tafla

Eftirfarandi mynd sýnir reitina sem eru í boði fyrir viðskiptavinatöfluna.

[![Tiltæk svæði fyrir viðskiptavinatöfluna](./media/related-entities.png)](./media/related-entities.png)

Ekki ætti að velja eftirfarandi reit fyrir þjálfun:

- **Einkvæm lykillína** (flokkur 2)

## <a name="filters"></a>Síur

Eins og er styðja síurnar ekki sviðsmynd fyrir spá um greiðslu viðskiptavinar. Þess vegna skal velja **Sleppa þessu skrefi** og halda áfram á samantektarsíðuna.

[![Fókusstilling með síum](./media/focus-model-with-filters.png)](./media/focus-model-with-filters.png)

#### <a name="privacy-notice"></a>Tilkynning um persónuvernd
Forútgáfur (1) kunna að nota minni persónuverndar- og öryggisráðstafanir og þjónusta Dynamics 365 Finance and Operations, (2) eru ekki hluti af þjónustustigssamningi fyrir þessa þjónustu, (3) ættu ekki að vera notaðar til að vinna úr persónulegum gögnum eða öðrum gögnum sem falla undir lögboðnar kröfur eða reglur um samræmi og (4) hafa takmarkaðan stuðning.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]