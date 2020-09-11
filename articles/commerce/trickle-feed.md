---
title: Stofnun hlutastraumspöntunar fyrir færslur smásöluverslunar
description: Þetta efnisatriði lýsir stofnun hlutastraumspöntunar fyrir færslur verslunar í Microsoft Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 06/08/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 6e097ead7cacb3f71452323656546a4be661457f
ms.sourcegitcommit: 7061a93f9f2b54aec4bc4bf0cc92691e86d383a6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/20/2020
ms.locfileid: "3710284"
---
# <a name="trickle-feed-based-order-creation-for-retail-store-transactions"></a>Stofnun hlutastraumspöntunar fyrir færslur smásöluverslunar

[!include [banner](includes/banner.md)]

Í Dynamics 365 Retail, útgáfu 10.0.4 og eldri útgáfum, er uppgjör bókað í lok dags og allar færslur eru bókfærðar í lok dags. Vinna verður úr háum færslum innan takmarkaðs tímaramma sem leiðir stundum til álags, læsingar og vandamála við bókun á uppgjöri. Einnig kemur það í veg fyrir að söluaðilar geti skráð tekjur og greiðslur í bókhaldið yfir daginn.

Með stofnun hlutastraumspöntunar sem er hluti af Retail, útgáfu 10.0.5, er hægt að vinna úr færslum yfir daginn og eiga einungis eftir að vinna úr fjárhagslegri afstemmingu greiðslumáta og öðrum reiðufjárstjórnunarfærslum í lok dags. Þessi eiginleiki jafnar álagið af því að búa til sölupantanir, reikninga og framkvæma greiðslur yfir daginn. Þetta veitir betri skilning á afkomu og gefur kost á að skrá tekjur og greiðslur í bókhald nánast í rauntíma. 


## <a name="how-to-use-trickle-feed-based-posting"></a>Hvernig á að nota bókun með hlutastraum
  
1. Til að virkja bókun með hlutastraum fyrir færslur skal fara í **Kerfisstjórnun > Uppsetning > Skilgreining leyfis** og gera lykillinn fyrir **Uppgjör** óvirkan.

2. Á sömu síðu skal virkja leyfislykilinn fyrir **Uppgjör (hlutastraum) - Forskoðun**. Þegar þessi lykill er virkjaður skal ganga úr skugga um að engin uppgjör bíði þess að vera bókuð. 

    > [!Important]
    > Áður en leyfislykillinn fyrir **Uppgjör (hlutastraumur) - Forskoðun** er virkjaður skal ganga úr skugga um að engin uppgjör bíði þess að vera bókuð.

3. Núverandi uppgjörsskjali verður skipt upp í tvær mismunandi tegundir, færsluuppgjör og fjárhagsskýrslu.

      - Færsluuppgjörið mun taka til allra óbókaðra og villuleitaðra færslna og stofna sölupantanir, sölureikninga, færslubækur fyrir greiðslur og afslætti og tekju-/útgjaldafærslur með þeim takti sem er grunnstilltur. Grunnstilla ætti ferlið til að keyra á hárri tíðni svo fylgiskjöl séu búin til þegar færslunum er hlaðið upp í höfuðstöðvum í gegnum P-verkið. Með færsluuppgjöri sem býr sjálft til sölupantanir og sölureikninga er engin þörf á að grunnstilla runuvinnsluna **Bóka birgðir**. Hins vegar er enn hægt að nota hana til að uppfylla tilteknar viðskiptaþarfir sem notandinn kann að hafa.  
      
     - Fjárhagsskýrslan er stillt á þann hátt að hún er búin til í lok dags og styður aðeins lokunaraðferðina **Vakt**. Þessi skýrsla takmarkast við fjárhagslega afstemmingu og býr eingöngu til færslubækur fyrir upphæðamismun á milli talinnar upphæðar og færsluupphæðar fyrir mismunandi greiðslumáta ásamt færslubókum fyrir aðrar reiðufjárstjórnunarfærslur.   

4. Til að reikna út færsluuppgjörið skal smella á **Smásala og viðskipti > Upplýsingatækni smásölu og viðskipta > Sölustaðarbókun > Reikna færsluuppgjör í runu**. Til að bóka yfirlit færsluuppgjörs í runu skal smella á **Smásala og viðskipti > Upplýsingatækni smásölu og viðskipta > Sölustaðarbókun > Bóka færsluuppgjör í runu**.

5. Til að reikna út fjárhagsskýrsluna skal smella á **Smásala og viðskipti > Upplýsingatækni smásölu og viðskipta > Sölustaðarbókun > Reikna fjárhagsskýrslur í runu**. Til að bóka fjárhagsskýrslurnar í runu skal smella á **Smásala og viðskipti > Upplýsingatækni smásölu og viðskipta > Sölustaðarbókun > Bóka fjárhagsskýrslur í runu**.

> [!NOTE]
> Valmyndaratriðin **Smásala og viðskipti > Upplýsingatækni smásölu og viðskipta > Sölustaðarbókun > Reikna uppgjör í runu** og **Smásala og viðskipti > Upplýsingatækni smásölu og viðskipta > Sölustaðarbókun > Bóka uppgjör í runu** verða fjarlægð með tilkomu þessa nýja eiginleika.

Einnig er hægt að búa til gerðir af færsluuppgjörum og fjárhagsskýrslum handvirkt. Opnið **Smásala og viðskipti > Rásir > Verslanir** og smellið á **Uppgjör**. Smella skal á **Nýtt** og velja svo þá gerð uppgjörs sem stofna á. Svæðin á síðunni **Uppgjör** og aðgerðir í hlutanum **Uppgjörsflokkur** á síðunni birta gögn og aðgerðir í samræmi við valda gerð uppgjörs.
