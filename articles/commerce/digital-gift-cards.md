---
title: Stafræn gjafakort rafrænna viðskipta
description: Þetta efnisatriði lýsir því hvernig stafræn gjafakort virka í innleiðingu rafrænna viðskipta Microsoft Dynamics 365 Commerce. Það veitir einnig yfirlit yfir mikilvæg skilgreiningarskref.
author: anupamar-ms
ms.date: 05/27/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: de8811b3265bc582a055aaad1f3dea32def552f4
ms.sourcegitcommit: d38d2fe85dc2497211ba5731617f590029d07145
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/27/2022
ms.locfileid: "8809588"
---
# <a name="e-commerce-digital-gift-cards"></a>Stafræn gjafakort rafrænna viðskipta

[!include [banner](includes/banner.md)]

Þetta efnisatriði lýsir því hvernig stafræn gjafakort virka í innleiðingu rafrænna viðskipta Microsoft Dynamics 365 Commerce. Það veitir einnig yfirlit yfir mikilvæg skilgreiningarskref.

Í Dynamics 365 Commerce fylgja kaup stafrænna gjafakorta sama ferli og kaup á öðrum afurðum í kerfinu. Engar viðbótareiningar verða að vera skilgreindar. Ef mörgum gjafakortum er bætt við körfuna, er vörum gjafakortsins ekki safnað saman í eina sölulínu. Þessi hegðun er nauðsynleg vegna þess að hver sölulína er reikningsfærð með því að nota aðskilið gjafakortsnúmer.

Kaup á stafrænum gjafakortum eru studd í Dynamics 365 Commerce 10.0.16 útgáfu og nýrri.

Eftirfarandi mynd sýnir dæmi um upplýsingasíðu afurðar fyrir stafrænt gjafakort á Fabrikam-svæði fyrir rafræn viðskipti.

![Dæmi um upplýsingasíðu stafræns gjafakorts á Fabrikam-svæði fyrir rafræn viðskipti.](./media/GiftcardPDP.PNG)

## <a name="turn-on-the-digital-gift-card-feature-in-commerce-headquarters"></a>Kveikja á eiginleika stafræns gjafakorts í Commerce Headquarters

Fyrir innkaupaferli stafrænna gjafakorta í Dynamics 365 Commerce verður að vera kveikt á eiginleikanum **Gjafakort keypt í rafrænum viðskiptum** í Commerce Headquarters. Hægt er að finna eiginleikann á vinnusvæðinu **Eiginleikastjórnun** í Commerce Headquarters eins og sýnt er á eftirfarandi mynd.

![Vinnusvæði eiginleikastjórnunar í Commerce Headquarters.](./media/Featureflag.PNG)

## <a name="configure-a-digital-gift-card-in-commerce-headquarters"></a>Skilgreina stafrænt gjafakort í Commerce Headquarters

Stafrænar afurðir gjafakorta ættu að vera skilgreindar í Commerce Headquarters. Ferlið svipar til ferlis annarra afurða. Eftirfarandi mikilvæg skref eiga hins vegar við skilgreiningu gjafakorta vegna kaupa. Frekari upplýsingar um hvernig á að stofna og skilgreina afurðir er að finna í [Stofna nýja afurð í Commerce](create-new-product-commerce.md).

- Þegar afurðir stafrænna gjafakorta eru skilgreindar í svarglugganum **Ný afurð** skal stilla reitinn **Gerð afurðar** á **Þjónusta**. (Til að opna svargluggann er farið í **Smásala og viðskipti \> Afurðir og flokkar \> Afurðir eftir flokki** og valið **Ný**.) Birgðir til ráðstöfunar fyrir afurð af gerðinni **Þjónusta** eru ekki athugaðar áður en pöntun er gerð. Frekari upplýsingar er að finna í [Stofna nýja afurð](create-new-product-commerce.md#create-a-new-product).
- Á síðunni **Commerce-færibreytur**, í flipanum **Bókun**, verður að stilla reitinn **Gjafakortsafurð** á **Stafrænt gjafakort** eins og sýnt er á eftirfarandi mynd. Ef afurðin er utanaðkomandi gjafakort skal skoða [Stuðningur við utanaðkomandi gjafakort](./dev-itpro/gift-card.md) til að fá frekari upplýsingar.

    ![Reitur gjafakortsafurðar í Commerce Headquarters.](./media/PostGiftcard.png)

- Ef gjafakort verður að styðja margar fyrirframskilgreindar upphæðir (til dæmis, $25, $50 og $100) ætti að nota víddina **Stærð** til að setja upp þessar fyrirframskilgreindu upphæðir. Hvert fyrirfram skilgreint magn verður vöruafbrigði. Frekari upplýsingar er að finna í [Afurðarvíddir](../supply-chain/pim/product-dimensions.md?toc=%2fdynamics365%2fretail%2ftoc.json).
- Ef viðskiptavinir verða að geta tilgreint sérsniðna upphæð fyrir gjafakort til viðbótar við fyrirfram skilgreindar upphæðir skaltu fyrst setja upp afbrigði sem gerir ráð fyrir sérsniðinni upphæð. The **Stærð** eiginleiki styður sérsniðin magnafbrigði. Næst skaltu opna vöruna frá **Gefnar vörur í flokki** síðu og síðan á **Verslun** flýtiflipann, stilltu **Sláðu inn verð** sviði til **Þarf að slá inn nýtt verð**, eins og sýnt er í eftirfarandi dæmi. Þessi stilling tryggir að viðskiptavinir geti fært inn verð þegar þeir fletta upp afurðinni á upplýsingasíðu hennar.

    ![Reitur fyrir innslátt verðs í Commerce Headquarters.](./media/KeyInPrice.png)
    
    Eftirfarandi dæmi sýnir lista yfir afbrigði af stafrænum gjafakortum í höfuðstöðvum Commerce, þar á meðal tvö sérsniðin verðafbrigði.
    ![Stafræn gjafakortavöruafbrigði með sérsniðnu verðafbrigði dæmi](./media/DigitalGiftCards_ProductVariantsWithCustom.png)

- Afhendingarmáti fyrir stafrænt gjafakort verður að vera stilltur á **Rafrænn**. Á síðunni **Afhendingarmáti** (**Smásala og viðskipti \> Uppsetning rásar \> Afhendingarmáti**) skal velja afhendingarmátann **Rafrænn** á listasvæðinu og síðan bæta stafrænni gjafakortsafurð við hnitanetið í flýtiflipanum **Afurðir** eins og sýnt er á eftirfarandi mynd. Frekari upplýsingar er að finna í [Setja upp afhendingarmáta](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).

    ![Stafrænar gjafakortsafurðir á síðu afhendingarmáta í Commerce Headquarters.](./media/ElectronicMode.PNG)
    
- Ganga skal úr skugga um að virkniforstilling á netinu hafi verið búin til og tengd við netverslunina í Commerce Headquarters. Í virkniforstillingunni skal stilla valkostinn **Safna saman afurðum** á **Já**. Þessi stilling tryggir að allar vörur að frátöldum gjafakortum séu lagðar saman. Frekari upplýsingar er að finna í [Búa til virkniforstillingu á netinu](online-functionality-profile.md).
- Til að tryggja að viðskiptavinir fái tölvupóst eftir að gjafakort er reikningsfært skal stofna nýja gerð tilkynningar í tölvupósti á síðunni **Forstillingar tilkynningar í tölvupósti** og stilla reitinn **Gerð tilkynningar í tölvupósti** á **Gefa út gjafakort**. Frekari upplýsingar er að finna í [Setja upp forstillingu tilkynningar í tölvupósti](email-notification-profiles.md).

## <a name="add-product-images-to-the-commerce-site-builder-media-library"></a>Bæta myndum afurðar við miðlunarsafn Commerce-vefsmiðs

Bæta verður myndum afurðar fyrir stafrænar gjafakortsafurðir við miðlunarsafn Commerce-vefsmiðs. Gangið úr skugga um að skráarheiti fyrir myndaskrár gjafakortsins fylgi nafnavenju svæðisins fyrir myndir afurðar. Frekari upplýsingar er að finna í [Hlaða upp myndum](dam-upload-images.md).

## <a name="configure-a-custom-amount-for-a-digital-gift-card-in-commerce-site-builder"></a>Skilgreina sérsniðna upphæð fyrir stafrænt gjafakort í Commerce-vefsmið

Ef stafrænt gjafakort er skilgreint til að leyfa sérsniðna upphæð, verður þessi hegðun einnig að vera virkjuð í [kaupgluggaeiningunni](add-buy-box.md) sem er notuð á upplýsingasíðu afurðar á svæðinu. Kaupgluggaeiningin styður skilgreiningu einingar til að leyfa sérsniðnar upphæðir. Einnig er hægt að skilgreina lágmarks- og hámarksupphæðirnar sem leyfðar eru fyrir sérsniðnar upphæðir.

Til að skilgreina sérsniðna upphæð fyrir stafrænt gjafakort í Commerce-vefsmið skal fylgja þessum skrefum.

1. Farið í kaupgluggaeininguna sem er notuð á upplýsingasíðu afurðar á svæðinu. Þessi kaupgluggaeining gæti verið innleidd í broti, sniðmáti eða á síðu.
1. Veljið **Breyta**.
1. Í eiginleikastikunni hægra megin skal velja gátreitinn **Leyfa sérsniðið verð**.
1. Valfrjálst: Til að skilgreina lágmarks- og hámarksupphæð fyrir sérsniðnar upphæðir skal slá inn upphæðir undir **Lágmarksverð** og **Hámarksverð**.
1. Veljið **Ljúka við breytingar** og síðan **Birta**.

## <a name="additional-resources"></a>Frekari upplýsingar

[Kaupgluggaeining](add-buy-box.md)

[Greiðsluferliseining](add-checkout-module.md)

[Körfueining](add-cart-module.md)

[Stofna nýja afurð í Commerce](create-new-product-commerce.md)

[Setja upp afhendingarmáta](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)

[Afurðarvíddir](../supply-chain/pim/product-dimensions.md?toc=%2fdynamics365%2fretail%2ftoc.json)

[Setja upp forstillingu tilkynningar í tölvupósti](email-notification-profiles.md)

[Búa til virkniforstillingu á netinu](online-functionality-profile.md)

[Stuðningur við utanaðkomandi gjafakort](./dev-itpro/gift-card.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
