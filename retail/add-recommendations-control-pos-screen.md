---
title: "Bæta stýringu ráðleggingar síðu færslu á POS-tæki"
description: "Þetta efnisatriði lýsir hvernig á að bæta stýringu ráðleggingar færsluskjár á punktur sölustað tækis með útlitshönnuður afgreiðsluskjás í Microsoft Dynamics 365 fyrir Aðgerðir."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 2377b1639a3c95fe6bba4754c4069cc12043e3d3
ms.lasthandoff: 03/31/2017


---

# <a name="add-a-recommendations-control-to-the-transaction-page-on-a-pos-device"></a>Bæta stýringu ráðleggingar síðu færslu á POS-tæki

Þetta efnisatriði lýsir hvernig á að bæta stýringu ráðleggingar færsluskjár á punktur sölustað tækis með útlitshönnuður afgreiðsluskjás í Microsoft Dynamics 365 fyrir Aðgerðir.

Hægt er að birta ráðleggingar afurðar á POS-tæki þegar Microsoft Dynamics 365 um Aðgerðir. *Leiðbeiningar* eru vörur sem viðskiptavinurinn kann að vera áhuga á grundvelli sögu innkaupapantanir, vara á óskalista þeirra og vörur sem keyptar annarra viðskiptavina netinu og í stað og mortar verslanir. Til að birta ráðleggingar afurð, þarf að bæta stýringu skjánum færslan með útlitshönnuður afgreiðsluskjás.

## <a name="open-layout-designer"></a>Opna útlitshönnuður
1.  Fara í **Smásölu og commerce**&gt;**Rásar uppsetningu**&gt;**uppsetning Smásölustaðar**&gt;**POS**&gt;**Skjá útlit**.
2.  Nota Síu á Flýtiræsistikunni til að finna skjá sem á að bæta stýringunni við. Til dæmis sía á **Skjá Útlitskenni** svæðið með gildið 'F2CP16:9M'.
3.  Í listanum skal finna og velja þá skráningu sem óskað er eftir. Veljið til dæmis "Heiti: Kenni F2CP16:9M útlit Afgreiðsluskjás: F2CP16:9M'.
4.  Smellið á **útlitshönnuður**.
5.  Fylgja kvaðningar til að ræsa útlit hönnuður. Þegar beðið er um skilríki fyrir, að færa sömu skilríki voru í notkun í útlitshönnuður var ræstur úr **Skjá útlit** síðu.
6.  Þegar þú skráir þig, er svipuð eitt neðan birtist. Útlit verður mismunandi eftir breytingar sem gerðar voru fyrir verslunin.

[![screenlayout pic 1](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png) birtingarvalkostinn til að Velja
-----------------------

Tveir valkostir skilgreiningar eru tiltækar. Veljið valkostinn sem best fyrir verslunin og fylgið leiðbeiningunum eftir að ljúka uppsetningu stýringu. Tveir valkostir eru:
-   Leiðbeiningar eru alltaf sýnileg.
-   A **Ráðleggingar** birtist flipinn á hnitanetinu á hægri hlið á skjánum.

#### <a name="to-make-recommendations-always-visible"></a>Til að gera ráðleggingar fyrir alltaf sýnilegt

1.  Minnka hæð upplýsingarsvæðið línur færslu þannig að það er sama hæð sem viðskiptavinagluggi til vinstri hennar. [](./media/pic-2.png)[![screenlayout-pic-2](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)
2.  Draga og sleppa á ráðleggingar stýringu á milli upplýsingarsvæðið línu færslunnar og hnappahnit vinnustöðvar neðst á skjánum færslu úr valmyndinni vinstra megin. Breyta stærð stýringin svo það hentar í það bil. [](./media/pic-3.png)[![screenlayout pic 3](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)
3.  Smellið á **X** til að vista og loka útlitshönnuður.
4.  Í Dynamics 365 aðgerða, farið **Smásölu og commerce**&gt;**Retail ÞAÐ**&gt;**dreifingaráætlanir**.
5.  Á listanum, veljið **1090 Skráir**.
6.  Smellið á **Keyra nú**.

#### <a name="to-add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a>Til að bæta flipa Ráðleggingar hnappahnit hægra megin á skjánum

1.  Hægrismella á autt bil undir flipanum síðasta á hnappahnitið staðsett hægra megin á síðunni.
2.  Smellið á **Sérsníða**. [![pic-5](./media/pic-5.png)](./media/pic-5.png)
3.  Smellið á **Nýr flipi**.
4.  Nýr flipi sem verið er að bæta finna. Hugsanlega þarf að fletta niður.
5.  Í því **Innihald** fellilistann, veljið **Ráðlagt afurðir**. [![pic 6](./media/pic-6.png)](./media/pic-6.png)
6.  Í því **Merki** skal slá inn heiti fyrir ráðleggingar flipa. Til dæmis gerð 'Ráðlagt afurðir'.
7.  Í því **Myndina** skal velja myndina sem eiga að birtast á flipanum.
8.  Click **OK**. Nýr flipi birtist hnappahnitið.
9.  Smellið á **X** til að vista og loka útlitshönnuður.
10. Í Dynamics 365 aðgerða, farið **Smásölu og commerce**&gt;**Retail ÞAÐ**&gt;**dreifingaráætlanir**.
11. Á listanum, veljið **1090 Skráir**.
12. Smellið á **Keyra nú**.


<a name="see-also"></a>Sjá einnig
--------

[Yfirlit yfir leiðbeiningar sérsniðinn afurðar](personalized-product-recommendations.md)


