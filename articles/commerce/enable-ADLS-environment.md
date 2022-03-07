---
title: Virkja Azure Data Lake Storage í Dynamics 365 Commerce-umhverfi
description: Í þessu efnisatriði eru leiðbeiningar um hvernig á að tengja Azure Data Lake Storage Gen 2 lausn við einingaverslun Dynamics 365 Commerce umhverfis. Þetta er nauðsynlegt skref áður en tillögur um afurðir eru virkjaðar.
author: bebeale
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: c96c29a4d9639b02e6a60ad938b7e06f7d500c68
ms.sourcegitcommit: 98061a5d096ff4b9078d1849e2ce6dd7116408d1
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/01/2021
ms.locfileid: "7466293"
---
# <a name="enable-azure-data-lake-storage-in-a-dynamics-365-commerce-environment"></a>Virkja Azure Data Lake Storage í Dynamics 365 Commerce-umhverfi

[!include [banner](includes/banner.md)]

Í þessu efnisatriði eru leiðbeiningar um hvernig á að tengja Azure Data Lake Storage Gen2 lausn við einingaverslun Dynamics 365 Commerce umhverfis. Þetta er nauðsynlegt skref áður en tillögur um afurðir eru virkjaðar.

Í Dynamics 365 Commerce lausninni er gögnum sem eru nauðsynleg til að reikna út tillögur, afurðir og færslur safnað saman í einingaverslun umhverfisins. Til að gera þessi gögn aðgengileg öðrum þjónustum Dynamics 365, t.d. gagnagreiningu, viðskiptagreind og sérsniðnum tillögum, er nauðsynlegt að tengja umhverfið við Azure Data Lake Storage Gen 2 lausn í eigu viðskiptavinar.

Eftir að ofangreindum skrefum hefur verið lokið eru öllum gögnum viðskiptavinar í einingaverslun umhverfisins sjálfkrafa speglað í Azure Data Lake Storage Gen 2 lausn viðskiptavinar. Þegar eiginleikar tillagna eru virkjaðir í gegnum vinnusvæði eiginleikastjórnunar í Commerce Headquarters verður tillögustaflanum veittur aðgangur að sömu Azure Data Lake Storage Gen2 lausninni.

Meðan á öllu ferlinu stendur eru gögn viðskiptavinar áfram vernduð og undir stjórn þeirra.

## <a name="prerequisites"></a>Forkröfur

Einingaverslun Dynamics 365 Commerce umhverfis verður að vera tengd við Azure Data Lake Gen Storage Gen2 reikning og tilheyrandi þjónustur.

Frekari upplýsingar um Azure Data Lake Storage Gen2 og hvernig á að setja það upp er að finna í [Azure Data Lake Storage Gen2 opinber fylgigögn](https://azure.microsoft.com/pricing/details/storage/data-lake).
  
## <a name="configuration-steps"></a>Skref skilgreiningar

Þessi hluti nær yfir skilgreiningarskrefin sem nauðsynleg eru til að virkja Azure Data Lake Storage Gen2 í umhverfi því að það tengist afurðartillögum.
Fyrir ítarlegra yfirlit yfir skrefin sem þarf til að virkja Azure Data Lake Storage Gen2 skal skoða [Gera einingaverslun tiltæka sem Data Lake](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).

### <a name="enable-azure-data-lake-storage-in-the-environment"></a>Gera Azure Data Lake Storage virkt í umhverfinu

1. Skráðu þig inn á bakgagnasafn umhverfisins.
1. Leitapu að **Kerfisfæribreytum** og farðu á flipann **Gagnatengingar**. 
1. Stilltu **Virkja samþættingu Data Lake** á **Já**.
1. Næst færirðu inn eftirfarandi áskildar upplýsingar:
    1. **Forritsauðkenni** // **Leynilykill forrits** // **DNS-heiti** - Nauðsynlegt til að tengjast við KeyVault þar sem Azure Data Lake Storage-leynilykillinn er geymdur.
    1. **Leyniheiti** - Leyniheitið sem geymt er í KeyVault og notað til að sannvotta við Azure Data Lake Storage.
1. Vistaðu breytingarnar þínar efst í vinstra horninu á síðunni.

Eftirfarandi mynd sýnir dæmi um skilgreiningu Azure Data Lake Storage.

![Dæmi um skilgreiningu Azure Data Lake Storage.](./media/exampleADLSConfig1.png)

### <a name="test-the-azure-data-lake-storage-connection"></a>Prófa Azure Data Lake Storage-tenginguna

1. Prófaðu tenginguna við KeyVault með því að nota tengilinn **Prófa Azure-lykil**.
1. Prófið tenginguna við Azure Data Lake Storage með því að nota tengilinn **Azure Storage**.

> [!NOTE]
> Ef annaðhvort prófið hér að ofan mistekst skaltu staðfesta að allar upplýsingar lyklageymslu sem bætt er við hér að ofan séu réttar og reyndu síðan aftur.

Þegar tengiprófin hafa gengið, verður þú að gera sjálfvirka endurnýjun fyrir Entity verslunina.

Fylgdu þessum skrefum til að gera sjálfvirka endurnýjun fyrir Entity verslun.

1. Leita að **Entity-verslun**.
1. Á listanum til vinstri ferðu í færsluna **RetailSales** og velur **Breyta**.
1. Gakktu úr skugga um að **Sjálfvirk uppfærsla virk** sé stillt á **Já**, veldu **Endurnýja** og veldu síðan **Vista**.

Eftirfarandi mynd sýnir dæmi um Entity verslun með sjálfvirka endurnýjun virka.

![Dæmi um einingaverslun með sjálfvirka uppfærslu virka.](./media/exampleADLSConfig2.png)

Azure Data Lake Storage er nú skilgreint fyrir umhverfið. 

Ef ekki er lokið þegar, fylgdu skrefunum fyrir [sem gerir ráð fyrir vöru og sérstillingu](enable-product-recommendations.md) fyrir umhverfið.

## <a name="additional-resources"></a>Frekari upplýsingar

[Gera einingaverslun tiltæka sem Data Lake](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md)

[Yfirlit yfir afurðarráðleggingar](product-recommendations.md)

[Virkja ráðleggingar um afurðir](enable-product-recommendations.md)

[Kveikja á sérsniðnum tillögum](personalized-recommendations.md)

[Afþakka sérsniðnar tillögur](personalization-gdpr.md)

[Virkja tillögur um að kaupa svipaða vöru](shop-similar-looks.md)

[Bæta við afurðatillögum á sölustað](product.md)

[Bæta tillögum við færsluskjáinn](add-recommendations-control-pos-screen.md)

[Aðlagaðu niðurstöður AI-ML](modify-product-recommendation-results.md)

[Búðu til handvirkt myndaðar ráðleggingar](create-editorial-recommendation-lists.md)

[Búðu til tillögur með kynningargögnum](product-recommendations-demo-data.md)

[Algengar spurningar um afurðaráðleggingar](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
