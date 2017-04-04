---
title: "Yfirlit yfir leiðbeiningar sérsniðinn afurðar"
description: "Í Dynamics 365 aðgerða ráðleggingar afurðar er hægt að birta on the point of tækið sölustað. Leiðbeiningar sem eru vörur sem viðskiptavinurinn kann að vera áhuga á grundvelli sögu innkaupapantanir, vara á óskalista þeirra og vörur sem keyptar annarra viðskiptavina netinu og í stað og mortar verslanir. Fyrir smásala með stórum vörulista, hjálp ráðleggingar viðskiptavinar með discovery afurðar. Showcasing ætlaðar áhugamál viðskiptavinarins og veitta habits afurðir, afurð leiðbeiningar létta smásala söluviðauka og krosssölu og hægt er að auka varðveislu viðskiptavinar. Í Dynamics 365 fyrir Aðgerðir, afurð ráðleggingar rafhlöðu cognitive services og Microsoft Azure vél nám."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: af1f4ba1ed5efe0e35d08d37d09e7ada4a4c1b7a
ms.lasthandoff: 03/31/2017


---

# <a name="personalized-product-recommendations-overview"></a>Yfirlit yfir leiðbeiningar sérsniðinn afurðar

Í Dynamics 365 aðgerða ráðleggingar afurðar er hægt að birta on the point of tækið sölustað. Leiðbeiningar sem eru vörur sem viðskiptavinurinn kann að vera áhuga á grundvelli sögu innkaupapantanir, vara á óskalista þeirra og vörur sem keyptar annarra viðskiptavina netinu og í stað og mortar verslanir. Fyrir smásala með stórum vörulista, hjálp ráðleggingar viðskiptavinar með discovery afurðar. Showcasing ætlaðar áhugamál viðskiptavinarins og veitta habits afurðir, afurð leiðbeiningar létta smásala söluviðauka og krosssölu og hægt er að auka varðveislu viðskiptavinar. Í Dynamics 365 fyrir Aðgerðir, afurð ráðleggingar rafhlöðu cognitive services og Microsoft Azure vél nám.

<a name="scenarios"></a>Sviðsmyndir
---------

Afurð leiðbeiningar eru virkjaðar fyrir eftirfarandi aðstæður Sölustaðar. Þær eru tiltækar í Skýinu POS eða Modern POS (MPOS).

1.  Á við **afurðarupplýsingar** síðu:

-   Ef tengja verslun heimsóknum í **afurðarupplýsingar** síðu þegar líta á fyrri færslur þvert á mismunandi rásum vélar ráðlögð stingur fleiri vörur sem eru líklegt að vera keypt saman.
-   Ef verslunin tengja bætir viðskiptavini við færsluna og síðan heimsókna í **afurðarupplýsingar** síðu vél ráðlögð veitir sérsniðinn leiðbeiningar með því að nota færslusögu viðskiptavinar.

[![proddetails](./media/proddetails.png)](./media/proddetails.png)

1.  Á við **Færslu** síðu:

-   Ráðlögð vél stingur byggt á allan listann yfir vörur í í innkaupakörfuna.
-   Ef verslunin tengja bætir viðskiptavini við færsluna, vélar ráðlögð veitir persónulegar leiðbeiningar með færslusögu viðskiptavinar og lista yfir vörur í innkaupakörfuna.

**Athugasemd** til Að birta leiðbeiningar í **Færslu** síðu retailer sem þarf að uppfæra skjásins í Dynamics 365 fyrir Aðgerðir. Í **Ráðleggingar** stýringu verður sleppt í í **Færslu** síðu. [![transactionscreenmultipleproductslargemessengersbag 5](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)

1.  Á í **upplýsingar um Viðskiptavin** síðu:
    -   Ráðlögð vél stingur byggt á Kenni notanda og vara á óskalista viðskiptavinar.

[![customerdetailsrecommendations](./media/customerdetailsrecommendations.png)](./media/customerdetailsrecommendations.png)

## <a name="configure-dynamics-365-for-operations-to-enable-pos-recommendations"></a>Skilgreina Dynamics 365 aðgerða til að virkja leiðbeiningar Sölustaðar
Til að setja upp ráðleggingar afurð, þarf að gera eftirfarandi.

1.  Gangið úr skugga um að sem var valin rétta **lögaðila**.
2.  Fara í **Einingar verslun**, veljið **Retail vsk**, og smellið síðan á **Endurnýja**. ** ** Þetta mun nota sýnigögnin (eða gögnin) úr rekstraráætlanagerðar gagnagrunns og flytja í verslun Einingar.
3.  Valfrjálst: Til Að birta leiðbeiningar á skjánum færsluna, er farið ** Útlit Skjás **velja skal útlit afgreiðsluskjás, kemur í **útlitshönnuður afgreiðsluskjás**,** ** og sleppa svo í ** stýringu leiðbeiningar ** þar sem þarf.
4.  Fara í **færibreytur Retail**, veljið **Vél nám**, veljið ** Já ** undir **POS Virkja ráðleggingar**.
5.  Sjá leiðbeiningar á Sölustað, að keyra vinnsluna altæk skilgreining **1110**. Til að endurspegla breytingar á Sölustað útlitshönnuður afgreiðsluskjás, keyra vinnsluna skilgreining rásar **1070**.

## <a name="how-does-it-work"></a>[]()Hvernig það virkar?
Þegar endurnýja á **Einingar verslun** einingar, eru eftirfarandi aðgerðir eiga sér stað.

-   Gögn á sniði sem krafist er af Cognitive þjónustu er fenginn úr Dynamics 365 fyrir gagnagrunn um Aðgerðir og senda í verslunina Einingar.
-   Gögn sem er notaður með Azure Gögn Verksmiðjugólfinu (ADF) cleanse gögn með Hive forskriftir sem hluti af ADF verkþætti. Cleansed gögn séu geymd í geymslu blob.
-   Gögn úr geymslu blob notar Cognitive services API til að þjálfa ráðlögð líkan.

Þegar kveikt er á **Virkja ráðleggingar** og keyra skilgreiningu vinnslum, eru eftirfarandi aðgerðir eiga sér stað.

-   Líkan skilríki Kenni eru sótt úr API og geymd í Dynamics 365 fyrir gagnagrunn um Aðgerðir í web.config aos og einnig í retail-þjóns.
-   Líkan skilríki og Kenni gerðar tiltækar CRT þannig köll fyrir ráðleggingar afurðar úr Skýinu POS og MPOS í nettengda stillingu getur verið samþykktur.


<a name="see-also"></a>Sjá einnig
--------

[Bæta stýringu ráðleggingar síðu færslu á POS-tæki](add-recommendations-control-pos-screen.md)


