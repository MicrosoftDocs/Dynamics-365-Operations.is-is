---
title: Sérsniðnar afurðaráðleggingar
description: Þetta efnisatriði inniheldur upplýsingar ráðleggingar fyrir Dynamics 365 for Retail vörur sem hægt er að birta í sölustaðartæki.
author: ashishmsft
manager: AnnBe
ms.date: 02/05/2018
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
ms.openlocfilehash: d6706cbb7630aeb230bc9eb1c187397897c9de68
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "326470"
---
# <a name="personalized-product-recommendations"></a>Sérsniðiðnar vöruráðleggingar

[!include [banner](includes/banner.md)]

> [!NOTE]
> Núverandi útgáfa af ráðleggingaþjónustu vörunnar verður fjarlægð og eiginleikinn endurhannaður með betra reikniriti og nýrri smásölumiðuðum möguleikum. Sjá [Fjarlægðir eða úreltir eiginleikar](../dev-itpro/migration-upgrade/deprecated-features.md) fyrir frekari upplýsingar.

Í Dynamics 365 for Retail er hægt að birta ráðleggingar um vörur í sölustaðartæki. Ráðleggingar eru vörur sem viðskiptavinurinn kann að hafa áhuga á grundvelli sögu innkaupapantanir, vara á óskalista þeirra og vörur sem aðrir viðskiptavinir keyptu á netinu og í verslunum. Fyrir smásala með stóra vörulista hjálpa sérsniðnar ráðleggingar viðskiptavinum að finna vörur. Með því að sýna afurðir miðað við áhugamál viðskiptavinarins og innkaupavenjur geta vöruráðleggingar aðstoðað smásala við viðbótarsölu og krosssölu og hægt er að auka varðveislu viðskiptavinar. Í Dynamics 365 for Retail eru vöruráðleggingar keyrðar af vitsmunaþjónustu og Microsoft Azure vélnámi.

## <a name="scenarios"></a>Sviðsmyndir

Vöruráðleggingar eru virkjaðar fyrir eftirfarandi aðstæður sölustaðar. Þær eru tiltækar í sölukerfi í skýinu eða Modern POS (MPOS).

1. Á síðunni **Upplýsingar um afurð**:

    - Ef aðili tengdur verslun opnar í **Upplýsingar um afurð** síðuna þegar hann skoðar fyrri færslur þvert á mismunandi rásir stingur vélin upp á fleiri vörum sem eru líklegar til að vera keyptar saman.
    - Ef aðili tengdur versluninni bætir viðskiptavini við færsluna og hann heimsækir síðuna **Upplýsingar um afurð** stingur vélin upp á persónubundnum efni byggt á viðskiptaferli viðskiptavinarins.

    [![proddetails](./media/proddetails.png)](./media/proddetails.png)

2. Á síðunni **Færsla**:

    - Ráðlögð vél stingur upp á vörum byggt á öllum vörum í körfunni.
    - Ef aðili tengdur versluninni bætir viðskiptavini við færsluna stingur vélin upp á persónubundnu efni byggt á viðskiptaferli viðskiptavinarins og vörum í körfunni.

    > [!NOTE]
    > Til að birta ráðleggingar á síðunni **Færsla** þarf smásöluaðilinn að uppfæra skjáútlitið í Dynamics 365 for Retail. Sleppa verður stýringunni **Ráðleggingar** á síðunni **Færsla**.

    [![transactionscreenmultipleproductslargemessengersbag-5](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)

3. Á síðunni **Upplýsingar um viðskiptamann**:

    - Vélin stingur upp á vörum byggt á notandakenninu og vörum á óskalista viðskiptavinarins.

    [![customerdetailsrecommendations](./media/customerdetailsrecommendations.png)](./media/customerdetailsrecommendations.png)

## <a name="configure-dynamics-365-for-retail-to-enable-pos-recommendations"></a>Skilgreina Dynamics 365 for Retail til að virkja ráðleggingar sölustaðar

Til að setja upp ráðleggingar vöru þarf að gera eftirfarandi.

1. Gangið úr skugga um að réttur **Lögaðili** sé valinn.
2. Farið í **Einingaverslun** veljið **Smásala** og smellið á **Uppfæra**. Þá eru sýnigögn (eða þín eigin gögn) notuð úr virknifyrirtækisins og þau færð í einingaverslun.
3. Valfrjálst: Til Að birta ráðleggingar á færsluskjánum, er farið í **Útlit Skjás**útlit skjás valið **Útlitshönnuður afgreiðsluskjás** opnaður, og svo sleppt stýringunni **leiðbeiningar** þar sem þarf.
4. Farið í **Smásölufæribreytir**, veljið **Vélnám** svo **Já** undir **virkja ráðleggingar sölustaðar**.
5. Til að sjá ráðleggingar á sölustað skal keyra altæku vinnsluna **1110**. Til að endurspegla breytingar á útlitshönnuði sölustaðar skal keyra skilgreiningarvinnslu rásar **1070**.

## <a name="how-does-it-work"></a>Hvernig virkar það?

Þegar **Einingarverslun** einingin er uppfær eiga eftirfarandi aðgerðir sér stað.

- Gögn á sniði sem krafist er af vitsmunaþjónustu eru fengin úr Dynamics 365 for Retail virknigagnagrunni og send í einingaverslunina.
- Gögnin eru notuð af Azure Data Factory (ADF) til að hreinsa gögnin með Hive-forskriftum sem hluta af ADF verkþáttum. Hreinsuð gögn eru geymd í blob-geymslu.
- Gögn úr blob-geymslu eru notuð af API vitsmunaþjónustu til að þjálfa ráðlögð líkan.

Þegar kveikt er á **Virkja ráðleggingar** og skilgreiningarvinnslur eru keyrðar eiga eftirfarandi aðgerðir sér stað.

- Líkanaskilríki og kenni eru sótt úr API og geymd í Dynamics 365 for Retail virknigagnagrunni í web.config for AOS og einnig á smásöluþjóni.
- Líkanaskilríki og kenni eru gerð tiltæk á CRT þannig að hægt sé að vinna ráðleggingarbeiðnir vara úr sölukerfi í skýinu og MPOS í nettengdri stillingu.

## <a name="troubleshoot-issues-where-you-have-product-recommendations-already-enabled"></a>Finna úrræði á vandamálum þar sem ráðleggingar um vörur hafa þegar verið virkjaðar

- Flettið upp á **Smásölufæribreytur** \> **Vélnám** \> **Slökkva á ráðleggingum um vörur** og keyrið **Altæka skilgreiningarvinnslu \[1110\]**. Ef ekki er hægt að finna flipann **Vélnám** skal hafa samband við Dynamics Support.
- Ef **Stýringu ráðleggingar** var bætt við færsluskjáinn með því að nota **Útlitshönnun afgreiðsluskjás** skaltu fjarlægja hana líka.

## <a name="additional-resources"></a>Frekari upplýsingar

[Bæta stýringu ráðleggingar á færslusíðu á sölustaðartæki](add-recommendations-control-pos-screen.md)
