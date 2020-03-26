---
title: Bæta afurðaráðleggingum við sölustað
description: Þetta efni lýsir notkun ráðlegginga um vöru á sölustað (POS) tæki.
author: bebeale
manager: AnnBe
ms.date: 03/12/20
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 48533596c5bdc73dd8c815166e7dde0ca2f3cb4d
ms.sourcegitcommit: 1e7e7c4bc197b0a42e4d53d2a54600a2fb125b69
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/13/2020
ms.locfileid: "3127814"
---
# <a name="add-product-recommendations-on-pos"></a>Bæta afurðaráðleggingum við sölustað

[!include [banner](includes/banner.md)]

Í kjarna þess eru tillögur vöru umbreytandi viðskiptaumsóknar sem spannar öll viðskiptarými til að skapa ríka, grípandi og sérsniðna vöruuppgötvun. Fylgdu skrefunum til að framkvæma þennan eiginleika í POS [hvernig á að bæta ráðleggingum við POS tækin þín.](add-recommendations-control-pos-screen.md) 

Nánari upplýsingar um ráðleggingareiginleika vöru er að finna í [yfirliti yfir ráðleggingar um vörur í POS-skjölum.](../commerce/product-recommendations.md) 

## <a name="scenarios"></a>Sviðsmyndir

Vöruráðleggingar eru virkjaðar fyrir eftirfarandi aðstæður sölustaðar. Þær eru tiltækar í sölukerfi í skýinu eða Modern POS (MPOS).

1. Á síðunni **Upplýsingar um afurð**:

    - Ef aðili tengdur verslun fer á síðuna **Upplýsingar um afurð** þegar hann skoðar fyrri færslur þvert á mismunandi rásir stingur þjónustan upp á fleiri vörum sem eru líklegar til að vera keyptar saman.

    [![Meðmæli á upplýsingasíðu afurðar](./media/proddetails.png)](./media/proddetails.png)

2. Á síðunni **Færsla**:

    - Ráðgjafarvélin leggur til hluti sem byggja á öllum listanum yfir hluti í körfunni sem oft eru keyptir saman.

    > [!NOTE]
    > Til að birta ráðleggingar á síðunni **Færsla** þarf smásöluaðilinn að uppfæra skjáútlitið í Dynamics 365 Commerce. Sleppa verður stýringunni **Ráðleggingar** á síðuna **Færsla**.

    [![Meðmæli á færslusíðunni](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)

## <a name="configure-commerce-to-enable-pos-recommendations"></a>Skilgreina Commerce til að virkja ráðleggingar sölustaðar

Til að setja upp vöruráðleggingar skal fylgja þessum skrefum:

1. Gakktu úr skugga um að þjónusta þín hafi verið uppfærð í **10.0.6 bygging.**
2. Fylgdu leiðbeiningunum um hvernig á að gera [virkja tillögur um vöru](../commerce/enable-product-recommendations.md) fyrir fyrirtæki þitt.
3. Valfrjálst: Til Að birta ráðleggingar á færsluskjánum, er farið í **Útlit Skjás**útlit skjás valið **Útlitshönnuður afgreiðsluskjás** opnaður, og svo sleppt stýringunni **leiðbeiningar** þar sem þarf.
4. Farið í **Færibreytur Commerce**, veljið **Vélnám** svo **Já** undir **virkja ráðleggingar sölustaðar**.
5. Til að sjá ráðleggingar á sölustað skal keyra altæku vinnsluna **1110**. Til að endurspegla breytingar á útlitshönnuði sölustaðar skal keyra skilgreiningarvinnslu rásar **1070**.

## <a name="troubleshoot-issues-where-you-have-product-recommendations-already-enabled"></a>Finna úrræði á vandamálum þar sem ráðleggingar um vörur hafa þegar verið virkjaðar

- Flettið upp á **Færibreytur Commerce** \> **Ráðleggingalistar** \> **Slökkva á ráðleggingum um vörur** og keyrið **Altæka skilgreiningarvinnslu \[9999\]**. 
- Ef **Stýringu ráðleggingar** var bætt við færsluskjáinn með því að nota **Útlitshönnun afgreiðsluskjás** skaltu fjarlægja hana líka.
- Ef þú hefur frekari spurningar skaltu skoða [Algengar spurningar um afurðaráðleggingar](../commerce/faq-recommendations.md) fyrir meiri upplýsingar.

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit yfir afurðarráðleggingar](product-recommendations.md)

[Virkja ADLS í Dynamics 365 Commerce umhverfi](enable-adls-environment.md)

[Virkja ráðleggingar um afurðir](enable-product-recommendations.md)

[Kveikja á sérsniðnum tillögum](personalized-recommendations.md)

[Afþakka sérsniðnar tillögur](personalization-gdpr.md)

[Bæta við tillögulistum við vefsvæði fyrir rafræn viðskipti](add-reco-list-to-page.md)

[Bæta við tillögum á færsluskjáinn](add-recommendations-control-pos-screen.md)

[Aðlagaðu niðurstöður AI-ML](modify-product-recommendation-results.md)

[Búðu til handvirkt myndaðar ráðleggingar](create-editorial-recommendation-lists.md)

[Búðu til tillögur með kynningargögnum](product-recommendations-demo-data.md)

[Algengar spurningar um afurðaráðleggingar](faq-recommendations.md)
