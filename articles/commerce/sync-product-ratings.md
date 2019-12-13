---
title: Samstilla vörueinkunnagjöf í Dynamics 365 Retail
description: Þetta efni lýsir því hvernig á að samstilla vörueinkunnir í Microsoft Dynamics 365 Retail.
author: gvrmohanreddy
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: db5a4e1f78797d20ded2274cc99bef422fd50acc
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698166"
---
# <a name="sync-product-ratings-in-dynamics-365-retail"></a>Samstilla vörueinkunnagjöf í Dynamics 365 Retail

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Þetta efni lýsir því hvernig á að samstilla vörueinkunnir í Microsoft Dynamics 365 Retail.

## <a name="overview"></a>Yfirlit

Til að nota afurðaeinkunnir í alhliða rásum, svo sem á sölustað (POS) og í símaverum, verður að flytja afurðareinkunnir úr einkunna- og umsagnarþjónustunni inn í gagnagrunn verslunarrásarinnar. Þegar afurðaeinkunnir eru gerðar aðgengilegar í alhliða rásum geta þær hjálpað viðskiptavinum óbeint við samskipti sín við söluaðila.

Þetta efni lýsir eftirfarandi verkum:

1. Stilla runuvinnslu Retail til að flytja inn afurðaeinkunn.
1. Staðfestu að runuvinnslan fyrir samstillingu afurðaeinkunna hafi gengið.
1. Gerðu afurðaeinkunnir tiltækar í POS.

## <a name="configure-a-retail-batch-job-to-import-product-ratings"></a>Stilla runuvinnslu Retail til að flytja inn afurðaeinkunnir

> [!IMPORTANT]
> Áður en þú hefst handa skaltu ganga úr skugga um að útgáfa 10.0.6 eða nýrri af Retail sé uppsett.

### <a name="initialize-the-retail-scheduler"></a>Frumstilla Retail-verkraðara

Fylgið eftirfarandi skrefum til að frumstilla Retail verkraðara.

1. Farðu í **Retail \> Uppsetning höfuðstöðva \> Retail verkraðari \> Frumstilla Retail verkraðara**. Að öðrum kosti leitarðu að „Frumstilla smásöluáætlun.“
1. Í valmyndinni **Frumstilla Retail verkraðara** skaltu ganga úr skugga um að valkosturinn **Eyða fyrirliggjandi stillingum** sé stilltur á **Nei** og veldu síðan **Í lagi**.

### <a name="verify-the-retailproductrating-subjob"></a>Staðfestu undirvinnsluna RetailProductRating

Til að sannreyna að undirvinnslan **RetailProductRating** sé til fylgirðu þessum skrefum.

1. Farðu í **Retail \> Uppsetning höfuðstöðva \> Retail verkraðari \> Undirvinnslur verkraðara**. Að öðrum kosti leitarðu að „Undirvinnslur verkraðara.“
1. Í undirvinnslulistanum finnurðu eða leitar að undirvinnslunni **RetailProductRating**.

Eftirfarandi mynd sýnir dæmi um undirvinnsluupplýsingar í Retail.

![Upplýsingar um undirvinnsluna RetailProductRating](media/rnr-hq-ratings-sub-job.png)

> [!NOTE]
> Ef þú finnur ekki undirvinnsluna **RetailProductRating** gæti verið að þú hafir þegar keyrt vinnsluna **Samstilla afurðaeinkunnir** og vinnsluna **1040 CDX** áður en þú frumstilltir Retail verkraðara. Í þessu tilfelli skaltu fylgja þessum skrefum til að keyra vinnsluna **Full samstilling gagna**.
>
> 1. Farðu í **Retail \> Uppsetning höfuðstöðva \> Retail verkraðari \> Gagnagrunnur rásar**. Að öðrum kosti, leitaðu að „Rásagagnagrunni.“
> 1. Veldu gagnagrunn rásarinnar sem á að samstilla.
> 1. Í aðgerðaglugganum velurðu **Samstilling allra gagna**.
> 1. Í fellivalmyndinni **Velja dreifingaráætlun** velurðu **1040 - afurðir** og velur síðan **Í lagi**.
> 1. Endurtaktu skrefin í fyrri aðferð til að staðfesta að undirvinnslan **RetailProductRating** hafi verið stofnuð.

### <a name="import-product-ratings"></a>Flytja inn afurðareinkunnir

Til að flytja afurðaeinkunnir inn í Retail úr einkunna- og umsagnaþjónustunni skaltu fylgja þessum skrefum.

1. Farðu í **Retail \> Uppsetning höfuðstöðva \> Retail verkraðari \> Vinnslan Samstilla afurðaeinkunnir**. Að öðrum kosti leitarðu að „Vinnslan Samstilla afurðaeinkunnir.“
1. Í valmyndinni **Sækja afurðaeinkunnir**, á flýtifipanum **Keyra í bakgrunni**, velurðu **Endurtekning**.
1. Í valmyndinni **Skilgreina endurtekningu** seturðu upp endurtekningarmynstur. (Ráðlagt gildi er tvær klukkustundir.) Ekki tímasetja endurtekningu sem er minna en ein klukkustund.
1. Veljið **Í lagi**.
1. Stilltu valkostinn **Runuvinnsla** á **Já**. Þessi stilling hjálpar til við að tryggja að þú getir gert úttekt á klöddum og sannreynt stöðu runuvinnslukeyrslna.
1. Veldu **Í lagi** til að áætla runuvinnsluna.

Eftirfarandi mynd sýnir dæmi um stillingar runuvinnslu í Retail.

![Stilling á runuvinnslunni Samstilla afurðaeinkunnir](media/rnr-hq-batchjob-recurrence.png)

## <a name="verify-that-the-batch-job-for-product-rating-synchronization-was-successful"></a>Staðfestu að runuvinnslan fyrir samstillingu afurðaeinkunna hafi gengið

Til að sannreyna að runuvinnslan **Samstilla afurðaeinkunnir** hafi tekist skaltu fylgja þessum skrefum.

1. Farðu í **Retail \> Kerfisstjóri \> Fyrirspurnir \> Runuvinnslur** eða, ef þú ert að nota Retail-sértæka birgðahaldseiningu (SKU), **Retail \> Fyrirspurnir og skýrslur \> Runuvinnslur** í staðinn. Að öðrum kosti leitarðu að „Runuvinnslum“.
1. Til að skoða upplýsingar um runuvinnsluna, í runuvinnslulistanum, í dálkinum **Vinnslulýsing**, leitarðu að lýsingu sem inniheldur „Sækja afurðaeinkunnir.“
1. Veldu vinnslukennið til að skoða upplýsingar um runuvinnsluna, svo sem áætlaðan upphafsdag/-tíma og endurtekningatexta.

Eftirfarandi mynd sýnir dæmi um upplýsingar um runuvinnsluna í Retail þegar áætlað er að runuvinnslan gangi með tveggja tíma millibili.

![Upplýsingar um runuvinnsluna Samstilla afurðaeinkunnir](media/rnr-hq-batchjob-status-checking.png)

## <a name="make-product-ratings-available-at-the-pos"></a>Gerðu afurðaeinkunnir tiltækar í POS

Leiðbeiningar fyrir einkunnir og umsagnir í Dynamics 365 Commerce er alhliða lausn. Hins vegar eru afurðaeinkunnir ekki sjálfgefið sýndar í POS. Til að hjálpa viðskiptavinum í verslunum að sjá einkunnir og umsagnir þegar þeir fá hjálp við söluaðilum verður þú að kveikja á afurðaeinkunnum í POS.

Til að kveikja á afurðaeinkunnum á sölustað skal fylgja þessum skrefum.

1. Opnið **Retail \> Uppsetning Retail \> Færibreytur \> Smásölufæribreytur**. Einnig er hægt að leita að „Smásölubreytum“.
1. Á flipanum **Stillingafæribreytur** velurðu **Nýtt**.
1. Sláðu inn heiti eins og **RatingsAndReviews.EnableProductRatingsForRetailStores** og stilltu gildið á **satt**.
1. Veljið **Vista**.
1. Farðu í **Retail \> Upplýsingatækni smásölu \> Dreifingaráætlun**. Að öðrum kosti leitarðu að „Dreifingaráætlun.“
1. Á vinnslulistanum velurðu **1110** (**Altækar stillingar**) og velur síðan **Keyra núna**.
1. Þegar vinnslan hefur keyrt skaltu staðfesta að afurðaeinkunnir séu núna sýndar á sölustað.

Eftirfarandi mynd sýnir dæmi um stillingu Retail-færibreytanna til að kveikja á afurðaeinkunnum á sölustað.

![Stillingar Retail-færibreytanna fyrir afurðaeinkunnir á sölustað](media/rnr-hq-enable-ratings-in-pos.png)

Eftirfarandi skýringarmynd sýnir dæmi um afurðaeinkunnir á sölustað.

![Afurðaeinkunnir á sölustað](media/rnr-pos-catalog-ratings.png)

Eftirfarandi skýringarmynd sýnir dæmi um afurðaeinkunnir á rásum símavera.

![Afurðaeinkunnir í rás símaþjónustuvers](media/rnr-call-center-ratings.png)

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit yfir einkunnir og umsagnir](ratings-reviews-overview.md)

[Velja að nota einkunnir og umsagnir](opt-in-ratings-reviews.md)

[Stjórna einkunnum og umsögnum](manage-reviews.md)

[Skilgreina einkunnir og umsagnir](configure-ratings-reviews.md)
