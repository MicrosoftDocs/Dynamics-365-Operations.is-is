---
title: Bæta afurðaráðleggingum við sölustað
description: Þessi grein lýsir notkun vöruráðlegginga á sölustað (POS) tæki.
author: bebeale
ms.date: 09/08/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 170e2bf18aefc79a796620818c7100ff8e6e689a
ms.sourcegitcommit: f88273627ba105ede27f28fe67ccec2d7f78261c
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/09/2022
ms.locfileid: "9460057"
---
# <a name="add-product-recommendations-on-pos"></a>Bæta afurðaráðleggingum við sölustað

[!include [banner](includes/banner.md)]

Í kjarna þess eru tillögur vöru umbreytandi viðskiptaumsóknar sem spannar öll viðskiptarými til að skapa ríka, grípandi og sérsniðna vöruuppgötvun. Fylgdu skrefunum til að framkvæma þennan eiginleika í POS [hvernig á að bæta ráðleggingum við POS tækin þín.](add-recommendations-control-pos-screen.md) 

Nánari upplýsingar um ráðleggingareiginleika vöru er að finna í [yfirliti yfir ráðleggingar um vörur í POS-skjölum.](../commerce/product-recommendations.md) 

## <a name="scenarios"></a>Sviðsmyndir

Vöruráðleggingar eru virkjaðar fyrir eftirfarandi aðstæður sölustaðar. Þær eru tiltækar í sölukerfi í skýinu eða Modern POS (MPOS).

1. Á síðunni **Upplýsingar um afurð**:

    - Ef verslunaraðili heimsækir a **Upplýsingar um vöru** síðu þegar þeir eru að skoða fyrri viðskipti á mismunandi rásum, bendir ráðleggingaþjónustan á fleiri hluti sem líklegt er að verði keyptir saman. Það fer eftir viðbótum fyrir þjónustuna, smásalar geta sýnt **Verslaðu svipað útlit** og **Verslun svipað lýsing** ráðleggingar um vörur, auk sérsniðinna ráðlegginga fyrir notendur sem hafa fyrri kaupsögu.

    [![Meðmæli á upplýsingasíðu afurðar.](./media/proddetails.png)](./media/proddetails.png)

2. Á síðunni **Færsla**:

    - Ráðgjafarvélin leggur til hluti sem byggja á öllum listanum yfir hluti í körfunni sem oft eru keyptir saman.

    > [!NOTE]
    > Til að birta ráðleggingar á síðunni **Færsla** þarf smásöluaðilinn að uppfæra skjáútlitið í Dynamics 365 Commerce. Sleppa verður stýringunni **Ráðleggingar** á síðuna **Færsla**.

    [![Meðmæli á færslusíðunni.](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)

## <a name="configure-commerce-to-enable-pos-recommendations"></a>Skilgreina Commerce til að virkja ráðleggingar sölustaðar 

Til að setja upp vörutillögur skaltu staðfesta að þú hafir lokið úthlutunarferlinu fyrir Commerce vöruráðleggingar með því að fylgja skrefunum í [Virkjaðu vörutillögur](../commerce/enable-product-recommendations.md). Sjálfgefið er að tillögur birtast á báðum **Upplýsingar um vöru** síðu og **Upplýsingar um viðskiptavini** síðu eftir að þú hefur lokið úthlutunarskrefunum og gögnin hafa verið elduð. 

## <a name="add-recommendations-to-the-transaction-screen"></a>Bæta tillögum við færsluskjáinn

1. Til að bæta tilmælum við viðskiptaskjáinn skaltu fylgja skrefunum í [Bættu tilmælum við viðskiptaskjáinn](add-recommendations-control-pos-screen.md).
1. Til að endurspegla breytingar sem gerðar voru í útlitshönnuði POS skjás skaltu keyra rásarstillingarvinnu **1070** í höfuðstöðvum verslunar.

> [!NOTE] 
> Ef þú vilt virkja POS ráðleggingar með því að nota RecoMock comma-separated values (CSV) skrána, verður þú að dreifa CSV skránni á Microsoft Dynamics Lifecycle Services (LCS) eignasafn áður en þú stillir útlitsstjórann. Ef þú notar RecoMock CSV skrána þarftu ekki að virkja tillögur. CSV skráin er aðeins tiltæk í kynningarskyni. Það er mælt með því fyrir viðskiptavini eða lausnaarkitekta sem vilja líkja eftir útliti meðmælalista í kynningarskyni án þess að þurfa að kaupa viðbótarbirgðahaldseiningu (SKU).

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit yfir afurðarráðleggingar](product-recommendations.md)

[Virkja Azure Data Lake Storage í Dynamics 365 Commerce-umhverfi](enable-adls-environment.md)

[Virkja ráðleggingar um afurðir](enable-product-recommendations.md)

[Kveikja á sérsniðnum tillögum](personalized-recommendations.md)

[Afþakka sérsniðnar tillögur](personalization-gdpr.md)

[Virkja tillögur um að kaupa svipaða vöru](shop-similar-looks.md)

[Bæta tillögum við færsluskjáinn](add-recommendations-control-pos-screen.md)

[Aðlagaðu niðurstöður AI-ML](modify-product-recommendation-results.md)

[Búðu til handvirkt myndaðar ráðleggingar](create-editorial-recommendation-lists.md)

[Búðu til tillögur með kynningargögnum](product-recommendations-demo-data.md)

[Algengar spurningar um afurðaráðleggingar](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
