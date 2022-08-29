---
title: Setja upp útlitshönnuð sölustaðar
description: Nota má eins-smells hönnuð til að hanna mismunandi Modern POS (MPOS) og Cloud POS útlit, í hamnum lárétt eða lóðrétt, fyrir verslanir, afreiðslukassa, gjaldkerar og stjórnendur.
author: josaw1
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.custom: 219684
ms.assetid: 2e2c4eea-c6e2-4912-9832-a6b22416e39f
ms.search.industry: Retail
ms.search.form: RetailTillLayout
ms.openlocfilehash: a610dbb9db63236ae7d182692f45f21c56982c69
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274260"
---
# <a name="install-the-pos-layout-designer"></a>Setja upp útlitshönnuð sölustaðar

[!include [banner](includes/banner.md)]

Nota má eins-smells hönnuð til að hanna mismunandi Modern POS (MPOS) og Cloud POS útlit, í hamnum lárétt eða lóðrétt, fyrir verslanir, afreiðslukassa, gjaldkerar og stjórnendur.

Grafískri hönnun Retail POS viðmótsins er stýrt af Útliti skúffu. Útlit stýrir staðsetningu mismunandi hluta. Dæmi eru útliti samtalna, útliti vöruhnits, útliti viðskiptavinar, útlit greiðslu og útlit ýmsum valmyndarhnöppum. Útlit innifelur einnig heildar útliti söluviðmóts sem birtist starfsmenn.

## <a name="install-the-one-click-designer"></a>Setja upp eins-smells hönnuð

1. Í Commerce skal nota valmyndina efst til vinstri til að fletta að **Retail og Commerce** &gt; **Uppsetning rásar** &gt; **Uppsetning sölustaðar** &gt; **Sölustaður** &gt; **Útlit skjás**.
2. Veljið hvaða útlit sem er sem er með gerð forrits **Modern POS fyrir Windows** eða **Cloud POS**, og smellið síðan á **útlitshönnuður**.
3. Á Tilkynningarslá sem mun birtast neðst í Internet Explorer glugganum , smellið á **Opna** til að setja upp eins-smells hönnuð. (Tilkynningaslá gætu birst í aðra Staður í öðrum vöfrum).
4. Í **Keyra Forritið - Öryggisviðvörun** skilaboð sem birtast skal smella á **Keyra** til að setja upp hýsil fyrir smásöluhönnuð. Framvinduvísir sem sýnir framvindu uppsetningar.
5. Eftir að uppsetningu er lokið á síðunni **Innskráning** skal færa inn notandanafn og aðgangsorð í Commerce, og smellið svo á **Innskráningu** til að hefja hönnuðurinn.
6. Eftir að skilríkin þín eru villuleitaðar og hönnuður hefst er hægt að hanna þitt eigið útlit eða breyta fyrirliggjandi útliti.

    [![Útlit í hönnuði með einum smelli.](./media/screenlayoutdesign_mposdownload-1024x664.png)](./media/screenlayoutdesign_mposdownload.png)

## <a name="troubleshoot-the-installation-of-the-layout-designer"></a>Úrræðaleit vegna uppsetningar á útlitshönnuður

- Þegar smellt er á **Hönnuður**, birtist ekki kvaðningin sækja (eða keyra) uppsetningarforrits eða gildandi öryggisstillingar leyfa þér ekki að sækja skrána. 

    **Lausnir**

    - Gangið úr skugga loka séð á hindrun sprettiglugga fyrir þessa síðu í Internet Explorer. Smellið á **Stillingar** &gt; **Valkostir** &gt; **Persónuvernd** &gt; **Finna sprettigluggablokk** og breyta þeirri stillingu ef breytinga er krafist.
    - Í Internet Explorer skaltu bæta við vefslóð Commerce á lista yfir traust vefsvæði. Smellið á **Stillingar** &gt; **Valkostir** &gt; **Öryggi** &gt; **Traust svæði** &gt; **Svæði** &gt; **Bæta við**.

- Forritið ræsist ekki og sagt er að hafa samband við lánardrottinn.

    **Lausn:** Í Internet Explorer skal bæta Commerce-vefslóðinni við traust vefsvæði. Smellið á **Stillingar** &gt; **Valkostir** &gt; **Öryggi** &gt; **Traust svæði** &gt; **Svæði** &gt; **Bæta við**.

**Þekkt vandamál:** hönnuðurinn vinnur ekki rétt í Google Chrome og Mozilla Firefox vöfrum. Við höfum unnið til að laga þetta vandamál.

## <a name="additional-resources"></a>Frekari upplýsingar

[Skilgreina, setja upp og virkja Retail Modern POS (MPOS)](retail-modern-pos-device-activation.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
