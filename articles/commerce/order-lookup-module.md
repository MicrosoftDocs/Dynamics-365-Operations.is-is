---
title: Uppflettieining pantana
description: Þetta efnisatriði fjallar um uppflettieiningu pantana og útskýrir hvernig á að skilgreina hana í Microsoft Dynamics 365 Commerce.
author: stuharg
ms.date: 09/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2021-08-15
ms.dyn365.ops.version: Release 10.0.22
ms.openlocfilehash: fa61a20ffd9a31f800c48b71832be7547952119f
ms.sourcegitcommit: d420b96d37093c26f0e99c548f036eb49a15ec30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/03/2021
ms.locfileid: "7472625"
---
# <a name="order-lookup-module"></a>Uppflettieining pantana

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Þetta efnisatriði fjallar um uppflettieiningu pantana og útskýrir hvernig á að skilgreina hana í Microsoft Dynamics 365 Commerce.

Uppflettieining pantana býður upp á skjámynd sem viðskiptavinir geta notað til að fletta upp á pöntunum sem þeir gera á vefsvæði rafrænna viðskipta. Hún er notuð sem hluti af eiginleikanum [Virkja uppflettingu pöntunar fyrir gestakaup](order-lookup-guest.md). Uppflettieining pantana er hægt að nota til að fletta upp á pöntunum sem voru sendar inn gegnum vefsvæði rafrænna viðskipta, sölustað smásölu eða símaver. Skjámyndin getur sótt pantanir sem bæði gestanotendur og skráðir notendur sendu inn.

Eftirfarandi mynd sýnir dæmi um skjámyndina sem uppflettieining pöntunar setur fram á myndrænan hátt. Þegar viðskiptavinir fylla út skjámyndina og velja **Finna pöntun** eru þeir áframsendir á upplýsingasíðu pöntunar.

![Skjámynd fyrir uppflettieiningu pantana á síðu.](./media/OrderLookup_module.PNG)

## <a name="order-lookup-module-properties"></a>Eiginleikar uppflettieiningar pantana

| Nafn eiginleika     | Virði     | lýsing |
|-------------------|-----------|-------------|
| Haus           | Texti      | Fyrirsögnin sem birtist efst í skjámyndinni (til dæmis „Finna pöntun“). |
| Sniðinn texti         | Sniðinn texti | Valfrjáls skýringartexti sem birtist fyrir neðan fyrirsögnina. |
| Gerð pöntunarstöðu | Upptalning      | <p>Veldu hvers konar upplýsingar skjámyndin biður viðskiptavininn um ásamt auðkenni pöntunarstaðfestingar. Eftirfarandi gildi eru studd sem stendur:</p><ul><li><b>Tölvupóstur</b> – Skjámyndin mun innihalda reit þar sem viðskiptavinir geta fært inn netfangið sem þeir notuðu þegar þeir gerðu pöntunina.</li><li><b>Engar upplýsingar</b> – Skjámyndin mun ekki biðja um neinar upplýsingar fyrir utan auðkenni pöntunarstaðfestingar.</li></ul> |

## <a name="add-an-order-lookup-module-to-a-page"></a>Bæta uppflettieiningu pantana við síðu

Hægt er að bæta uppflettieiningu pantana við meginmál hvaða síðu sem er á vefsvæði rafrænna viðskipta. Ef þú vilt nota uppflettieiningu pantana til að virkja uppflettingu pantana fyrir greiðsluferli gesta skaltu ganga úr skugga um að bæta henni við síðu sem krefst þess ekki að notandinn skrái sig inn. Til að finna stillinguna **Krefst innskráningar?** á síðu trjáyfirlits í vefsmið rafrænna viðskipta skal velja hólfið **Sjálfgefin síða (áskilið)** og kíkja neðst á svæðið hægra megin.

## <a name="additional-resources"></a>Frekari upplýsingar

[Virkja uppflettingu pöntunar fyrir gestakaup](order-lookup-guest.md)

[Yfirlit einingasafns](starter-kit-overview.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
