---
title: Stjórna SEO-lýsigögnum
description: Þessi grein lýsir því hvernig á að stjórna leitarvélabestun (SEO) lýsigögnum í Microsoft Dynamics 365 Commerce.
author: psimolin
ms.date: 04/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 99c28c2bff7b683f3e92dea4ba24d8bead556443
ms.sourcegitcommit: 6616b969afd6beb11a79d8e740560bf00016ea7f
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/17/2022
ms.locfileid: "9027310"
---
# <a name="manage-seo-metadata"></a>Stjórna SEO-lýsigögnum

[!include [banner](includes/banner.md)]

Þessi grein lýsir því hvernig á að stjórna leitarvélabestun (SEO) lýsigögnum í Microsoft Dynamics 365 Commerce.

Hægt er að stjórna SEO lýsigögnum fyrir síðu með því að nota svæðiskort og lýsigögn síðna.
    
## <a name="site-maps"></a>Svæðiskort

Vefkort er vélalæsilegur listi, á XML sniði, af síðunum á vefsíðunni þinni. Það er ætlað að notkunar leitarvéla, svo að þær geti veitt betri leitarniðurstöður frá vefsvæðinu þínu. Leitarvélar geta tekið vefkort upp handvirkt eða gefa út í robots.txt skrá.

Dynamics 365 Commerce styður sjálfvirka myndun á vefkortum. Vefkort eru uppfærð sjálfkrafa þegar síður eru birtar og óbirtar.

### <a name="turn-on-site-map-generation"></a>Kveiktu á myndun vefkorts

1. Skráðu þig inn á höfundatólið.
1. Undir **Svæði** velurðu **Fabrikam** (eða heiti svæðisins).
1. Í stýriglugganum vinstra megin velurðu **Svæðisstjórnun**.
1. Gakktu úr skugga um að kveikt sé á valkostinum **Vefkort virkjuð**.

## <a name="page-metadata"></a>Lýsigögn síðu

Dynamics 365 Commerce gerir þér kleift að stjórna lýsigögnum SEO fyrir einstakar síður. Þú getur skoðað og breytt þessum upplýsingum í hlutanum **SEO eiginleikar** í síðugámi. Eftirfarandi lýsigagnaeiginleikar SEO eru studdir:

- Titill
- Lýsing
- SEO lykilorð
- Aria merki
- noindex
- nofollow
- noarchive
- nocache
- noOpenDirectoryProject
- nosnippet
- noImageIndex
- unavailableAfter

### <a name="modify-page-metadata"></a>Breyta lýsigögnum síðna

Til að breyta lýsigögnum síðu skal fylgja þessum skrefum.
1. Undir **Svæði** velurðu **Fabrikam** (eða heiti svæðisins).
1. Í stýriglugganum vinstra megin velurðu **Síður**.
1. Veldu heimasíðuna til að opna hana í ritlinum.
1. Á skipanastikunni velurðu **Breyta**.
1. Í síðuritlinum, efst á útlínurstýringu síðunnar til vinstri, veldu **Útlínur hamur valkostur** (gírtákn) og veldu síðan **Ítarleg yfirlitsmynd**.
1. Í yfirlitsskjánum skaltu stækka tréstýringarnar til að sýna innihald **HTML höfuð** rifa.
1. Í **HTML höfuð** rauf, veldu þá SEO einingu sem þú vilt (til dæmis, **Yfirlit síðu**, **vörusíðu**, **yfir flokkasíðu**, eða **Lýsimerki**).
1. Í eiginleikarúðunni hægra megin, breyttu viðkomandi SEO gögnum fyrir valda SEO einingu (til dæmis, **Titill**, **·**, eða **Deilir mynd**).
1. Veldu **Vista** og síðan **Ljúka við breytingar**.
1. Í **Athugasemdir** reit, slá inn **Uppfærð SEO gögn**, og veldu síðan **Allt í lagi**.
1. Veldu **Forskoðun** til að forskoða síðuna. Þegar þú hefur lokið því skaltu loka forskoðunarflipanum til að fara aftur í höfundatólið.
1. Velja **Birta**.

> [!TIP]
> Höfundar geta notað **Útlínur hamur valkostur** (gírtákn) efst á vinstri útlínumstýringu í síðuritlinum til að skipta á milli **Grunnyfirlit** og **Ítarleg yfirlitsmynd**. **Grunnyfirlit** er sjálfgefin stilling og síar útlínurnar þannig að þær sýni aðeins einingar í **Líkami** HTML rauf fyrir síðu. **Ítarleg yfirlitsmynd** sýnir alla síðueininguna, þar á meðal **HTML höfuð**, **byrjar**, og **Líkamslok** rifa. Þetta útsýni er gagnlegt þegar höfundar verða að breyta tilteknum stillingum fyrir SEO eða forskriftareiningu fyrir síðu.

## <a name="additional-resources"></a>Frekari upplýsingar

[Breyta síðu svæðis sem þegar er til](modify-existing-page.md)

[Bæta við nýrri síðu á svæði](add-new-page.md)

[Velja síðuútlit](select-page-layouts.md)

[Vista, forskoða og birta síðu](save-preview-publish-page.md)

[Bæta vörusíðu](enrich-product-page.md)

[Bæta lendingarsíðu flokks](enrich-category-page.md)

[Staðfesta aðgengi að efni síðu](verify-accessibility.md)

[Búa til gagnvirkar síður fyrir rafræn viðskipti sem byggja á færibreytum vefslóða](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
