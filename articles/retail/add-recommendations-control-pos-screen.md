---
title: "Bæta stýringu ráðleggingar á færslusíðu á sölustaðartæki"
description: "Þetta efnisatriði lýsir hvernig á að bæta ráðleggingarstjórnun við færsluskjáinn á sölustaðartæki (POS) og nota til þess útlitshönnun skjás í Microsoft Dynamics 365 for Retail."
author: ashishmsft
manager: AnnBe
ms.date: 02/05/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailStoreTable, RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 16bdf2176869e5822ddf8732c829b65f1e60632c
ms.openlocfilehash: b99d1d30fc320bca5c49921b7c4ccdd7e977f67c
ms.contentlocale: is-is
ms.lasthandoff: 02/07/2018

---

# <a name="add-a-recommendations-control-to-the-transaction-page-on-a-pos-device"></a>Bæta stýringu ráðleggingar á færslusíðu á sölustaðartæki

[!INCLUDE [banner](includes/banner.md)]

> [!NOTE]
> Núverandi útgáfa af ráðleggingaþjónustu vörunnar verður fjarlægð og eiginleikinn endurhannaður með betra reikniriti og nýrri smásölumiðuðum möguleikum. Sjá [Fjarlægðir eða úreltir eiginleikar](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/migration-upgrade/deprecated-features) fyrir frekari upplýsingar. 

Þetta efnisatriði lýsir hvernig á að bæta ráðleggingarstjórnun við færsluskjáinn á sölustaðartæki (POS) og nota til þess útlitshönnun skjás í Microsoft Dynamics 365 for Retail.

Hægt er að birta afurðarráðleggingar í POS-tæki þegar Microsoft Dynamics 365 for Retail er notað. *Ráðleggingar* eru vörur sem viðskiptavinurinn kann að hafa áhuga á grundvelli sögu innkaupapantanir, vara á óskalista þeirra og vörur sem aðrir viðskiptavinir keyptu á netinu og í verslunum. Til að birta vöruráðleggingar þarf að bæta við stýringu á færsluskjáinn með útlitshönnuður afgreiðsluskjás.

## <a name="open-layout-designer"></a>Opnaðu Útlitshönnuður afgreiðsluskjás
1.  Farðu í **Smásala** &gt; **Uppsetning rásar** &gt; **Uppsetning POS** &gt; **POS** &gt; **Skjáútlit**.
2.  Notaðu flýtiafmörkun til að finna skjáinn sem á að bæta stýringunni við. Til dæmis notar sían í svæðinu **Útlitskenni afgreiðsluskjás** gildið 'F2CP16:9M'.
3.  Í listanum skal finna og velja þá skráningu sem óskað er eftir. Til dæmis veldu ‘Nafn: F2CP16:9M Útlitskenni afgreiðsluskjás: F2CP16:9M’.
4.  Smellt er á **Útlitshönnuður**.
5.  Fylgdu kvaðningum til að hefja Útlitshönnuðinn. Þegar beðið er um skilríki skal slá inn sömu skilríki og voru notuð þegar Útlitshönnuður var opnaður af síðunni **Skjáútlit**.
6.  Þegar þú skráir þig inn birtist síða sem er svipuð þeirra sem er fyrir neðan. Útlitið verður mismunandi eftir þeim sérstillingum sem voru gerðar fyrir verslunina.

[![screenlayout-pic-1](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png) Veljið birta valkostur
-----------------------

Tvær skilgreiningar eru í boði: Veldu valkostinn sem virkar best fyrir verslunina og fylgdu eftirstöðvum leiðbeininga til að ljúka uppsetningu stýringarinnar. Valkostirnir tveir eru:
-   Ráðleggingar eru alltaf sýnilegar.
-   Flipinn **Ráðleggingar** birtist í hnitanetinu hægra megin á skjánum.

#### <a name="to-make-recommendations-always-visible"></a>Til að gera ráðleggingar alltaf sýnilegar

1.  Dragðu úr hæð upplýsingasvæðis færslulína svo að það sé í sömu hæð og svæði viðskiptamanns til vinstri.[](./media/pic-2.png)[![screenlayout-pic-2](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)
2.  Frá valmynd til vinstri skal draga og sleppa ráðleggingarstýringu á milli upplýsingasvæðis færslulína og hnappahnita í neðst á miðjan færsluskjáinn. Breyta stærð stýringar svo að hún passi í það bil.[](./media/pic-3.png)[![screenlayout-pic-3](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)
3.  Smellt er á **X++** til að vista og fara úr Útlitshönnuði.
4.  Í Dynamics 365 for Retail er farið í **Smásala** &gt; **Upplýsingatækni smásölu** &gt; **Dreifingaráætlanir**.
5.  Á listanum velurðu **1090 afgreiðslukassar**.
6.  Smellt er á **Keyra núna**.

#### <a name="to-add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a>Til að bæta við ráðleggingaflipa í hnitanetið hægra megin á skjánum

1.  Hægrismelltu í tómt bil undir síðasta flipanum á hnappahnitinu hægra megin á síðunni.
2.  Smellt er á **Sérstilla**.[![pic-5](./media/pic-5.png)](./media/pic-5.png)
3.  Smellt er á **Nýr flipi**.
4.  Finndu nýja flipann sem þú varst að bæta við. Þörf getur verið á því að skruna niður.
5.  Í fellilistanum **Efni** skal velja **Ráðlögð afurð**. [![pic-6](./media/pic-6.png)](./media/pic-6.png)
6.  Á svæðinu **Merkimiði** skal færa inn heiti sniðsins. Til dæmis, ritarðu ‚Ráðlagðar vörur‘.
7.  Í svæðinu **Mynd** velurðu myndina sem á að birtast á flipanum.
8.  Smellt er á **OK**. Nýi flipinn birtist í hnappahnitunum.
9.  Smellt er á **X++** til að vista og fara úr Útlitshönnuði.
10. Í Dynamics 365 for Retail er farið í **Smásala** &gt; **Upplýsingatækni smásölu** &gt; **Dreifingaráætlanir**.
11. Á listanum velurðu **1090 afgreiðslukassar**.
12. Smellt er á **Keyra núna**.


<a name="see-also"></a>Sjá einnig
--------

[Yfirlit yfir sérsniðnar afurðarráðleggingar](personalized-product-recommendations.md)




