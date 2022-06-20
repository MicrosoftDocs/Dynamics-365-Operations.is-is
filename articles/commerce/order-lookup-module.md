---
title: Uppflettieining pantana
description: Þessi grein fjallar um pöntunareininguna og útskýrir hvernig á að stilla hana í Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: c83463d9a0ece9605b0d22bee2a1c76057c8ed05
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8869431"
---
# <a name="order-lookup-module"></a>Uppflettieining pantana

[!include [banner](includes/banner.md)]

Þessi grein fjallar um pöntunareininguna og útskýrir hvernig á að stilla hana í Microsoft Dynamics 365 Commerce.

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
