---
title: Setja upp útlitshönnuð smásöluverslunar (POS)
description: Nota má eins-smells hönnuð til að hanna mismunandi Retail Modern POS POS (MPOS) og Cloud POS útlit, í hamnum lárétt eða lóðrétt, fyrir verslanir, afreiðslukassa, gjaldkerar og stjórnendur.
author: athinesh99
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 219684
ms.assetid: 2e2c4eea-c6e2-4912-9832-a6b22416e39f
ms.search.region: Global
ms.search.industry: Retail
ms.author: athinesh
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 98784c11c7393bb4c3e022d5bff4cca2daa1636e
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/24/2019
ms.locfileid: "2025448"
---
# <a name="install-the-retail-point-of-sale-pos-layout-designer"></a>Setja upp útlitshönnuð smásöluverslunar (POS)

[!include [banner](includes/banner.md)]

Nota má eins-smells hönnuð til að hanna mismunandi Retail Modern POS POS (MPOS) og Cloud POS útlit, í hamnum lárétt eða lóðrétt, fyrir verslanir, afreiðslukassa, gjaldkerar og stjórnendur.

Grafískri hönnun Retail POS viðmótsins er stýrt af Útliti skúffu. Útlit stýrir staðsetningu mismunandi hluta. Dæmi eru útliti samtalna, útliti vöruhnits, útliti viðskiptavinar, útlit greiðslu og útlit ýmsum valmyndarhnöppum. Útlit innifelur einnig heildar útliti söluviðmóts sem birtist starfsmenn.

## <a name="install-the-one-click-designer"></a>Setja upp eins-smells hönnuð

1. Í Retail skal nota valmyndina efst til vinstri til að fletta að **Retail** **og viðskipti** &gt; **Uppsetning rásar** &gt; **Uppsetning sölustaðar** &gt; **Sölustaður** &gt; **Útlit skjás**.
2. Veljið hvaða útlit sem er sem er með gerð forrits **Modern POS fyrir Windows** eða **Cloud POS**, og smellið síðan á **útlitshönnuður**.
3. Á Tilkynningarslá sem mun birtast neðst í Internet Explorer glugganum , smellið á **Opna** til að setja upp eins-smells hönnuð. (Tilkynningaslá gætu birst í aðra Staður í öðrum vöfrum).
4. Í **Keyra Forritið - Öryggisviðvörun** skilaboð sem birtast skal smella á **Keyra** til að setja upp hýsil fyrir smásöluhönnuð. Framvinduvísir sem sýnir framvindu uppsetningar.
5. Eftir að uppsetningu er lokið á síðunni **Innskráning** skal færa inn notandanafn og aðgangsorð í Retail, og smellið svo á **Innskráningu** til að hefja hönnuðurinn.
6. Eftir að skilríkin þín eru villuleitaðar og hönnuður hefst er hægt að hanna þitt eigið útlit eða breyta fyrirliggjandi útliti.

    [![Setja upp eins-smells hönnuð](./media/screenlayoutdesign_mposdownload-1024x664.png)](./media/screenlayoutdesign_mposdownload.png)

## <a name="troubleshoot-the-installation-of-the-layout-designer"></a>Úrræðaleit vegna uppsetningar á útlitshönnuður

- Þegar smellt er á **Hönnuður**, birtist ekki kvaðningin sækja (eða keyra) uppsetningarforrits eða gildandi öryggisstillingar leyfa þér ekki að sækja skrána. 

    **Lausnir**

    - Gangið úr skugga loka séð á hindrun sprettiglugga fyrir þessa síðu í Internet Explorer. Smellið á **Stillingar** &gt; **Valkostir** &gt; **Persónuvernd** &gt; **Finna sprettigluggablokk** og breyta þeirri stillingu ef breytinga er krafist.
    - Í Internet Explorer skaltu bæta við vefslóð Retail á lista yfir traust vefsvæði. Smellið á **Stillingar** &gt; **Valkostir** &gt; **Öryggi** &gt; **Traust svæði** &gt; **Svæði** &gt; **Bæta við**.

- Forritið ræsist ekki og sagt er að hafa samband við lánardrottinn.

    **Lausn:** Í Internet Explorer skal bæta Retail-vefslóðinni við traust vefsvæði. Smellið á **Stillingar** &gt; **Valkostir** &gt; **Öryggi** &gt; **Traust svæði** &gt; **Svæði** &gt; **Bæta við**.

**Þekkt vandamál:** hönnuðurinn vinnur ekki rétt í Google Chrome og Mozilla Firefox vöfrum. Við höfum unnið til að laga þetta vandamál.

## <a name="additional-resources"></a>Frekari upplýsingar

[Skilgreina, sækja, setja upp og virkja Retail Modern POS](retail-modern-pos-device-activation.md)
