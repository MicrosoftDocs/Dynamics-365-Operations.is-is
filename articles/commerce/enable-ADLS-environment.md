---
title: Virkja ADLS í Dynamics 365 Commerce umhverfi
description: Þetta efni útskýrir hvernig á að virkja og prófa Azure Data Lake Storage (ADLS) fyrir Dynamics 365 Commerce umhverfi, sem er forsenda þess að hægt sé að gera ráð fyrir afurð.
author: bebeale
manager: AnnBe
ms.date: 03/19/2020
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
ms.openlocfilehash: 3c037f5603af5af84917084eefa1edd508891c0d
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154437"
---
# <a name="enable-adls-in-a-dynamics-365-commerce-environment"></a>Virkja ADLS í Dynamics 365 Commerce umhverfi

[!include [banner](includes/banner.md)]

Þetta efni útskýrir hvernig á að virkja og prófa Azure Data Lake Storage (ADLS) fyrir Dynamics 365 Commerce umhverfi, sem er forsenda þess að hægt sé að gera ráð fyrir afurð.

## <a name="overview"></a>Yfirlit

Í Dynamics 365 Commerce-lausn eru allar upplýsingar um vöru og viðskipti raktar í Entity verslun umhverfisins. Til að gera þessi gögn aðgengileg öðrum Dynamics 365 þjónustu, svo sem gagnagreiningum, viðskiptagreind og persónulegum ráðleggingum, er nauðsynlegt að tengja umhverfið við viðskiptavini í eigu Azure Data Lake Storage Gen 2 (ADLS) lausn.

Þar sem ADLS er stillt í umhverfi eru öll nauðsynleg gögn spegluð úr Entity versluninni meðan þau eru enn vernduð og undir stjórn viðskiptavinarins.

Ef tillögur um vöru eða sérsniðnar ráðleggingar eru einnig gerðar virkar í umhverfinu, þá mun vöruframkvæmdastakkanum fá aðgang að sérstaka möppu í ADLS til að sækja gögn viðskiptavinarins og reikna meðmæli byggða á þeim.

## <a name="prerequisites"></a>Forkröfur

Viðskiptavinir þurfa að hafa ADLS stillt í Azure áskrift sem þeir eiga. Þetta efni fjallar ekki um kaup á Azure áskrift eða uppsetningu ADLS-geymslureiknings.

Nánari upplýsingar um ADLS er að finna í [ADLS opinberum fylgiskjölum](https://azure.microsoft.com/pricing/details/storage/data-lake).
  
## <a name="configuration-steps"></a>Skref skilgreiningar

Þessi hluti fjallar um nauðsynlegar stillingar til að gera ADLS kleift í umhverfi.

### <a name="enable-adls-in-the-environment"></a>Virkja ADLS í umhverfinu

1. Skráðu þig inn á bakgagnasafn umhverfisins.
1. Leitapu að **Kerfisfæribreytum** og farðu á flipann **Gagnatengingar**. 
1. Stilltu **Virkja samþættingu Data Lake** á **Já**.
1. Stilltu **Hlutauppfærsla Data Lake** á **Já**.
1. Næst færirðu inn eftirfarandi áskildar upplýsingar:
    1. **Auðkenni forrits** // **Leynilykill forrits** // **DNS-heiti** - Nauðsynlegt til að tengjast KeyVault þar sem ADLS-leynilykillinn er geymdur.
    1. **Leyniheiti** - Leyniheitið sem geymt er í KeyVault og notað til að sannvotta með ADLS.
1. Vistaðu breytingarnar þínar efst í vinstra horninu á síðunni.

Eftirfarandi mynd sýnir dæmi um ADLS-stillingu.

![Dæmi um ADLS-stillingu](./media/exampleADLSConfig1.png)

### <a name="test-the-adls-connection"></a>Prófa ADLS-tengingu

1. Prófaðu tenginguna við KeyVault með því að nota tengilinn **Prófa Azure-lykil**.
1. Prófaðu tenginguna við ADLS með því að nota tengilinn **Prófa Azure-geymslu**.

> [!NOTE]
> Ef prófunin tekst ekki skaltu athuga aftur hvort allar viðbættar KeyVault-upplýsingar hér að ofan séu réttar og reyna síðan aftur.

Þegar tengiprófin hafa gengið, verður þú að gera sjálfvirka endurnýjun fyrir Entity verslunina.

Fylgdu þessum skrefum til að gera sjálfvirka endurnýjun fyrir Entity verslun.

1. Leita að **Entity-verslun**.
1. Á listanum til vinstri ferðu í færsluna **RetailSales** og velur **Breyta**.
1. Gakktu úr skugga um að **Sjálfvirk uppfærsla virk** sé stillt á **Já**, veldu **Endurnýja** og veldu síðan **Vista**.

Eftirfarandi mynd sýnir dæmi um Entity verslun með sjálfvirka endurnýjun virka.

![Dæmi um verslun Entity með sjálfvirka endurnýjun virka](./media/exampleADLSConfig2.png)

ADLS er nú stillt fyrir umhverfið. 

Ef ekki er lokið þegar, fylgdu skrefunum fyrir [sem gerir ráð fyrir vöru og sérstillingu](enable-product-recommendations.md) fyrir umhverfið.

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit yfir afurðarráðleggingar](product-recommendations.md)

[Virkja ráðleggingar um afurðir](enable-product-recommendations.md)

[Kveikja á sérsniðnum tillögum](personalized-recommendations.md)

[Afþakka sérsniðnar tillögur](personalization-gdpr.md)

[Bæta afurðaráðleggingum við sölustað](product.md)

[Bæta við tillögum á færsluskjáinn](add-recommendations-control-pos-screen.md)

[Aðlagaðu niðurstöður AI-ML](modify-product-recommendation-results.md)

[Búðu til handvirkt myndaðar ráðleggingar](create-editorial-recommendation-lists.md)

[Búðu til tillögur með kynningargögnum](product-recommendations-demo-data.md)

[Algengar spurningar um afurðaráðleggingar](faq-recommendations.md)


