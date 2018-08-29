---
title: "Sérsniðiðnar vöruráðleggingar"
description: "Þetta efnisatriði inniheldur upplýsingar ráðleggingar fyrir Dynamics 365 for Retail vörur sem hægt er að birta í sölustaðartæki."
author: ashishmsft
manager: AnnBe
ms.date: 02/05/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
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
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: 368468a1c1cd023862f1405dddf3a90574edce22
ms.contentlocale: is-is
ms.lasthandoff: 08/09/2018

---

# <a name="personalized-product-recommendations"></a>Sérsniðiðnar vöruráðleggingar

[!include [banner](includes/banner.md)]

> [!NOTE]
> Núverandi útgáfa af ráðleggingaþjónustu vörunnar verður fjarlægð og eiginleikinn endurhannaður með betra reikniriti og nýrri smásölumiðuðum möguleikum. Sjá [Fjarlægðir eða úreltir eiginleikar](../dev-itpro/migration-upgrade/deprecated-features.md) fyrir frekari upplýsingar. Farið neðst á síðuna ef vandamál koma upp vegna ráðleggingar um vörur sem þegar hafa verið virkjaðar fyrir umhverfið þitt. 

Í Dynamics 365 for Retail er hægt að birta ráðleggingar um vörur í sölustaðartæki. Ráðleggingar eru vörur sem viðskiptavinurinn kann að hafa áhuga á grundvelli sögu innkaupapantanir, vara á óskalista þeirra og vörur sem aðrir viðskiptavinir keyptu á netinu og í verslunum. Fyrir smásala með stóra vörulista hjálpa sérsniðnar ráðleggingar viðskiptavinum að finna vörur. Með því að sýna afurðir miðað við áhugamál viðskiptavinarins og innkaupavenjur geta vöruráðleggingar aðstoðað smásala við viðbótarsölu og krosssölu og hægt er að auka varðveisla viðskiptavinar. Í Dynamics 365 for Retail eru ráðleggingar um vörur knúnar með Cognitive Services og vélanámi Microsoft Azure.


<a name="scenarios"></a>Sviðsmyndir
---------

Vöruráðleggingar eru virkjaðar fyrir eftirfarandi aðstæður sölustaðar. Þær eru tiltækar í sölukerfi í skýinu eða Modern POS (MPOS).

1.  Á síðunni **Upplýsingar um afurð**:

-   Ef aðili tengdur verslun opnar í **Upplýsingar um afurð** síðuna þegar hann skoðar fyrri færslur þvert á mismunandi rásir stingur vélin upp á fleiri vörum sem eru líklegar til að vera keyptar saman.
-   Ef aðili tengdur versluninni bætir viðskiptavini við færsluna og hann heimsækir síðuna **Upplýsingar um afurð** stingur vélin upp á persónubundnum efni byggt á viðskiptaferli viðskiptavinarins.

[![proddetails](./media/proddetails.png)](./media/proddetails.png)

2.  Á síðunni **Færsla**:

-   Ráðlögð vél stingur upp á vörum byggt á öllum vörum í körfunni.
-   Ef aðili tengdur versluninni bætir viðskiptavini við færsluna stingur vélin upp á persónubundnum efni byggt á viðskiptaferli viðskiptavinarins og vörum í körfunni.

> [!NOTE]
> Til að birta ráðleggingar á síðunni **Færsla** þarf smásöluaðilinn að uppfæra skjáútlitið í Dynamics 365 for Retail. Sleppa verður stýringunni **Ráðleggingar** á síðunni **Færsla**. [![transactionscreenmultipleproductslargemessengersbag-5](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)

3.  Á síðunni **Upplýsingar um viðskiptamann**:
    -   Ráðlögð vél stingur stingur upp á vörum byggt á notandakenninu og vörum á óskalista viðskiptavinarins.

[![customerdetailsrecommendations](./media/customerdetailsrecommendations.png)](./media/customerdetailsrecommendations.png)

## <a name="configure-dynamics-365-for-retail-to-enable-pos-recommendations"></a>Skilgreina Dynamics 365 for Retail þannig að kveikt sé á ráðleggingum á sölustað
Til að setja upp ráðleggingar vöru þarf að gera eftirfarandi.

1.  Gangið úr skugga um að réttur **Lögaðili** sé valinn.
2.  Farið í **Einingaverslun** veljið **Smásala** og smellið á **Uppfæra**. Þá eru sýnigögn (eða þín eigin gögn) notuð úr virknifyrirtækisins og þau færð í einingaverslun.
3.  Valfrjálst: Til Að birta ráðleggingar á færsluskjánum, er farið í **Útlit Skjás**útlit skjás valið **Útlitshönnuður afgreiðsluskjás** opnaður, og svo sleppt stýringunni **leiðbeiningar** þar sem þarf.

4.  Farið í **Smásölufæribreytir**, veljið **Vélnám** svo **Já** undir **virkja ráðleggingar sölustaðar**.
5.  Til að sjá ráðleggingar á sölustað skal keyra altæku vinnsluna **1110**. Til að endurspegla breytingar á útlitshönnuði sölustaðar skal keyra skilgreiningarvinnslu rásar **1070**.

## <a name="how-does-it-work"></a>Hvernig virkar það?
Þegar **Einingarverslun** einingin er uppfær eiga eftirfarandi aðgerðir sér stað.

-   Gögn á sniði sem krafist er af Cognitive Services eru fengin úr Dynamics 365 for Retail virknigagnagrunninum og send í einingaverslunina.
-   Gögnin eru notuð af Azure Data Factory (ADF) til að hreinsa gögnin með Hive-forskriftum sem hluta af ADF verkþáttum. Hreinsuð gögn eru geymd í blob-geymslu.
-   Gögn úr blob-geymslu eru notuð af API vitsmunaþjónustu til að þjálfa ráðlögð líkan.

Þegar kveikt er á **Virkja ráðleggingar** og skilgreiningarvinnslur eru keyrðar eiga eftirfarandi aðgerðir sér stað.

-   Líkanaskilríki og kenni eru sótt úr API og geymd í Dynamics 365 for Retail virknigagnagrunninum í web.config -skránni fyrir AOS og einnig á smásöluþjóni.
-   Líkanaskilríki og kenni eru gerð tiltæk á CRT þannig að hægt sé að vinna ráðleggingarbeiðnir vara úr sölukerfi í skýinu og MPOS í nettengdri stillingu.

> ## <a name="troubleshoot-issues-where-you-have-product-recommendations-already-enabled"></a>Finna úrræði á vandamálum þar sem ráðleggingar um vörur hafa þegar verið virkjaðar 
> - Flettið upp á **Retail færibreytum** > **Vélnám** > **Slökkva á ráðleggingum um vörur** og keyra **Altæka skilgreiningarvinnslu [1110]**. Ef ekki er hægt að finna flipann **Vélnám** skal hafa samband við Dynamics Support. 
> 
> - Ef **Stýringu ráðleggingar** var bætt við færsluskjáinn með því að nota **Útlitshönnun afgreiðsluskjás** skaltu fjarlægja hana líka. 



<a name="additional-resources"></a>Frekari upplýsingar
--------

[Bæta stýringu ráðleggingar á færslusíðu á sölustaðartæki](add-recommendations-control-pos-screen.md)




