---
title: Virkja Azure Data Lake Storage í Dynamics 365 Commerce-umhverfi
description: Þetta efnisatriði útskýrir hvernig á að virkja og prófa Azure Data Lake Storage fyrir Dynamics 365 Commerce-umhverfi, sem er forsenda fyrir því að virkja afurðartillögur.
author: bebeale
manager: AnnBe
ms.date: 04/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 27e4f1c751ee865b0df536f3c1912cb1d8946032
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4413070"
---
# <a name="enable-azure-data-lake-storage-in-a-dynamics-365-commerce-environment"></a>Virkja Azure Data Lake Storage í Dynamics 365 Commerce-umhverfi

[!include [banner](includes/banner.md)]

Þetta efnisatriði útskýrir hvernig á að virkja og prófa Azure Data Lake Storage fyrir Dynamics 365 Commerce-umhverfi, sem er forsenda fyrir því að virkja afurðartillögur.

## <a name="overview"></a>Yfirlit

Í Dynamics 365 Commerce-lausn eru allar upplýsingar um vöru og viðskipti raktar í Entity verslun umhverfisins. Til að gera þessi gögn aðgengileg öðrum þjónustum Dynamics 365, t.d. gagnagreiningu, viðskiptagreind og sérsniðnum tillögum, er nauðsynlegt að tengja umhverfið við Azure Data Lake Storage Gen 2 lausn í eigu viðskiptavinar.

Þar sem Azure Data Lake Storage er skilgreint í umhverfi eru öll nauðsynleg gögn spegluð úr einingaversluninni og á sama tíma vernduð og undir stjórn viðskiptavinar.

Ef afurðartillögur eða sérsniðnar tillögur eru einnig virkjaðar í umhverfinu verður stafli afurðartillagna gefin aðgangur að sérstakri möppu í Azure Data Lake Storage til að sækja gögn viðskiptavinar og reikna út tillögur byggt á þeim.

## <a name="prerequisites"></a>Forkröfur

Viðskiptavinir verða að hafa Azure Data Lake Storage skilgreint í Azure-áskrift sem þeir eru með. Þetta efnisatriði nær ekki yfir kaup á Azure-áskrift eða uppsetningu Azure Data Lake Storage-virkjaðs geymslulykils.

Frekari upplýsingar um Azure Data Lake Storage eru í [Azure Data Lake Storage Gen2 opinberum skjölum](https://azure.microsoft.com/pricing/details/storage/data-lake).
  
## <a name="configuration-steps"></a>Skref skilgreiningar

Þessi hluti nær yfir skilgreiningarskrefin sem nauðsynleg eru til að virkja Azure Data Lake Storage í umhverfi því að það tengist afurðartillögum.
Fyrir ítarlegra yfirlit yfir skrefin sem þarf til að virkja Azure Data Lake Storage skal skoða [Gera einingaverslun tiltæka sem Data Lake](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).

### <a name="enable-azure-data-lake-storage-in-the-environment"></a>Gera Azure Data Lake Storage virkt í umhverfinu

1. Skráðu þig inn á bakgagnasafn umhverfisins.
1. Leitapu að **Kerfisfæribreytum** og farðu á flipann **Gagnatengingar**. 
1. Stilltu **Virkja samþættingu Data Lake** á **Já**.
1. Stilltu **Hlutauppfærsla Data Lake** á **Já**.
1. Næst færirðu inn eftirfarandi áskildar upplýsingar:
    1. **Forritsauðkenni** // **Leynilykill forrits** // **DNS-heiti** - Nauðsynlegt til að tengjast við KeyVault þar sem Azure Data Lake Storage-leynilykillinn er geymdur.
    1. **Leyniheiti** - Leyniheitið sem geymt er í KeyVault og notað til að sannvotta við Azure Data Lake Storage.
1. Vistaðu breytingarnar þínar efst í vinstra horninu á síðunni.

Eftirfarandi mynd sýnir dæmi um skilgreiningu Azure Data Lake Storage.

![Dæmi um skilgreiningu Azure Data Lake Storage](./media/exampleADLSConfig1.png)

### <a name="test-the-azure-data-lake-storage-connection"></a>Prófa Azure Data Lake Storage-tenginguna

1. Prófaðu tenginguna við KeyVault með því að nota tengilinn **Prófa Azure-lykil**.
1. Prófið tenginguna við Azure Data Lake Storage með því að nota tengilinn **Azure Storage**.

> [!NOTE]
> Ef prófunin tekst ekki skaltu athuga aftur hvort allar viðbættar KeyVault-upplýsingar hér að ofan séu réttar og reyna síðan aftur.

Þegar tengiprófin hafa gengið, verður þú að gera sjálfvirka endurnýjun fyrir Entity verslunina.

Fylgdu þessum skrefum til að gera sjálfvirka endurnýjun fyrir Entity verslun.

1. Leita að **Entity-verslun**.
1. Á listanum til vinstri ferðu í færsluna **RetailSales** og velur **Breyta**.
1. Gakktu úr skugga um að **Sjálfvirk uppfærsla virk** sé stillt á **Já**, veldu **Endurnýja** og veldu síðan **Vista**.

Eftirfarandi mynd sýnir dæmi um Entity verslun með sjálfvirka endurnýjun virka.

![Dæmi um verslun Entity með sjálfvirka endurnýjun virka](./media/exampleADLSConfig2.png)

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