---
title: Stjórna SEO-lýsigögnum
description: Þetta efnisatriði lýsir því hvernig hægt er að stjórna lýsigögnum um SEO (SEO) í Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: b69d9d2769023967e2b94fef1b8fcf6b5b3357c5
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698350"
---
# <a name="manage-seo-metadata"></a>Stjórna SEO-lýsigögnum

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Þetta efnisatriði lýsir því hvernig hægt er að stjórna lýsigögnum um SEO (SEO) í Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Yfirlit

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
1. Í aðgerðasvæðinu velurðu **Skrá út**.
1. Í eiginleikaglugganum til hægri stækkarðu **Sjálfgild lýsimerki**.
1. Til að bæta við nýju lýsimerki **Bæta við** og sláðu síðan inn merkið í reitinn.

    Til að fjarlægja fyrirliggjandi lýsimerki velurðu ruslatunnutáknið hægra megin við það.

1. Veldu **Vista** og síðan **Skrá inn**.
1. Í reitnum **Athugasemdir** slærðu inn **Uppfærð lýsimerki** og velur síðan **Í lagi**.
1. Veldu **Forskoðun** til að forskoða síðuna. Þegar þú hefur lokið því skaltu loka forskoðunarflipanum til að fara aftur í höfundatólið.
1. Velja **Birta**.

## <a name="additional-resources"></a>Frekari upplýsingar

[Breyta síðu svæðis sem þegar er til](modify-existing-page.md)

[Bæta við nýrri síðu á svæði](add-new-page.md)

[Velja síðuútlit](select-page-layouts.md)

[Vista, forskoða og birta síðu](save-preview-publish-page.md)

[Bæta vörusíðu](enrich-product-page.md)

[Bæta lendingarsíðu flokks](enrich-category-page.md)

