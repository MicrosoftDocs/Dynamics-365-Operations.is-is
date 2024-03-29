---
title: Bæta tillögum við færsluskjáinn
description: Þessi grein lýsir því hvernig á að bæta ráðleggingarstýringu við færsluskjáinn á sölustað (POS) tæki með því að nota skjáútlitshönnuðinn í Microsoft Dynamics 365 Commerce.
author: bebeale
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 4748ade8d6693666b58cbded2123d3449d191509
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8862073"
---
# <a name="add-recommendations-to-the-transaction-screen"></a>Bæta tillögum við færsluskjáinn

[!include [banner](includes/banner.md)]


Þessi grein lýsir því hvernig á að bæta ráðleggingarstýringu við færsluskjáinn á sölustað (POS) tæki með því að nota skjáútlitshönnuðinn í Microsoft Dynamics 365 Commerce. Nánari upplýsingar um ráðleggingar um vöru er að finna í [ráðleggingar um vörur í POS-skjölum](product.md).


Hægt er að sýna vöruráðleggingar í POS-tækinu þegar þú notar Commerce. Til að birta vöruráðleggingar þarf að bæta við stýringu á færsluskjáinn með útlitshönnuður afgreiðsluskjás. 

## <a name="open-layout-designer"></a>Opnaðu Útlitshönnuður afgreiðsluskjás

1. Farðu í **Retail og Commerce** &gt; **Uppsetningu rásar** &gt; **Uppsetning POS** &gt; **POS** &gt; **Skjáútlit**.
2. Notaðu flýtiafmörkun til að finna skjáinn sem á að bæta stýringunni við. Til dæmis notar sían í svæðinu **Útlitskenni afgreiðsluskjás** gildið **F2CP16:9M**.
3. Í listanum skal finna og velja þá skráningu sem óskað er eftir. Til dæmis veldu **Nafn: F2CP16:9M Útlitskenni afgreiðsluskjás: F2CP16:9M**.
4. Smellt er á **Útlitshönnuður**.
5. Fylgdu kvaðningum til að hefja Útlitshönnuðinn. Þegar beðið er um skilríki skal slá inn sömu skilríki og voru notuð þegar Útlitshönnuður var opnaður af síðunni **Skjáútlit**.
6. Þegar þú skráir þig inn birtist síða sem er svipuð þeirra sem er fyrir neðan. Útlitið verður mismunandi eftir þeim sérstillingum sem voru gerðar fyrir verslunina.


    [![Útlitshönnuður.](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png)

## <a name="choose-a-display-option"></a>Veldu valkost skjás

Tvær skilgreiningar eru í boði: Veldu valkostinn sem virkar best fyrir verslunina og fylgdu eftirstöðvum leiðbeininga til að ljúka uppsetningu stýringarinnar. Valkostirnir tveir eru:

- Ráðleggingar eru alltaf sýnilegar.
- Flipinn **Ráðleggingar** birtist í hnitanetinu hægra megin á skjánum.

### <a name="make-recommendations-always-visible"></a>Gera ráðleggingar alltaf sýnilegar


1. Dragðu úr hæð upplýsingasvæðis færslulína svo að það sé í sömu hæð og svæði viðskiptamanns til vinstri .


    [![Hæð á upplýsingasvæði fyrir færslulínur minnkuð.](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)

2. Frá valmynd til vinstri skal draga og sleppa ráðleggingarstýringu á milli upplýsingasvæðis færslulína og hnappahnita í neðst á miðjan færsluskjáinn. Breyta stærð stýringar svo að hún passi í það bil.

    [![Ráðleggingarstýringu bætt við útlitið.](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)


3. Smellt er á **X++** til að vista og fara úr Útlitshönnuði.
4. Í Commerce er farið í **Retail og Commerce** &gt; **upplýsingatækni í Retail og Commerce** &gt; **dreifingaráætlun**.
5. Á listanum velurðu **1090 afgreiðslukassar**.
6. Smellt er á **Keyra núna**.


### <a name="add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a>Bæta ráðleggingaflipa við hnitanetið hægra megin á skjánum

1. Hægrismelltu í tómt bil undir síðasta flipanum á hnappahnitinu hægra megin á síðunni.

2. Smelltu á **Sérstilla**.

    [![Sérstilling - Svargluggi flipastýringar.](./media/pic-5.png)](./media/pic-5.png)

3. Smellt er á **Nýr flipi**.
4. Finndu nýja flipann sem þú varst að bæta við. Hugsanlega þarf að skruna niður.
5. Í fellilistanum **Efni** skal velja **Ráðlögð afurð**.

    [![Val á vörum sem mælt er með í efnisreitnum.](./media/pic-6.png)](./media/pic-6.png)

6. Í svæðinu **Merki** skal færa inn heiti á ráðleggingaflipanum. Færðu til dæmis inn „Ráðlagðar afurðir“.
7. Í svæðinu **Mynd** velurðu myndina sem á að birtast á flipanum.
8. Smellt er á **OK**. Nýi flipinn birtist í hnappahnitunum.
9. Smellt er á **X++** til að vista og fara úr Útlitshönnuði.
10. Í Commerce er farið í **Retail og Commerce** &gt; **upplýsingatækni í Retail og Commerce** &gt; **dreifingaráætlun**.
11. Á listanum velurðu **1090 afgreiðslukassar**.
12. Smellt er á **Keyra núna**.

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit yfir afurðarráðleggingar](product-recommendations.md)

[Virkja Azure Data Lake Storage í Dynamics 365 Commerce-umhverfi](enable-adls-environment.md)

[Virkja ráðleggingar um afurðir](enable-product-recommendations.md)

[Kveikja á sérsniðnum tillögum](personalized-recommendations.md)

[Afþakka sérsniðnar tillögur](personalization-gdpr.md)

[Virkja tillögur um að kaupa svipaða vöru](shop-similar-looks.md)

[Bæta við afurðatillögum á sölustað](product.md)

[Aðlagaðu niðurstöður AI-ML](modify-product-recommendation-results.md)

[Búðu til handvirkt myndaðar ráðleggingar](create-editorial-recommendation-lists.md)

[Búðu til tillögur með kynningargögnum](product-recommendations-demo-data.md)

[Algengar spurningar um afurðaráðleggingar](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]