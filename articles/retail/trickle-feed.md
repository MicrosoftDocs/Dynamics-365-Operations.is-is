---
title: Stofnun hlutastraumspöntunar fyrir færslur smásöluverslunar
description: Þetta efnisatriði lýsir stofnun hlutastraumspöntunar fyrir færslur smásöluverslunar í Microsoft Dynamics 365 Retail.
author: josaw1
manager: AnnBe
ms.date: 10/14/2019
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
ms.openlocfilehash: deb8399aa401af16b6fe123a433eb21864e178c6
ms.sourcegitcommit: 92322167f57b66d2accc134aaf862e6b9931ec94
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/31/2019
ms.locfileid: "2693090"
---
# <a name="trickle-feed-based-order-creation-for-retail-store-transactions-public-preview"></a>Stofnun hlutastraumspöntunar fyrir færslur smásöluverslunar (opin forútgáfa)

[!include [banner](includes/banner.md)]

[!include [banner](includes/preview-banner.md)]

Í Dynamics 365 Retail útgáfu 10.0.4 og eldri útgáfum er smásöluuppgjör bókað í lok dags og allar færslur eru bókfærðar í lok dags. Vinna verður úr háum færslum innan takmarkaðs tímaramma sem leiðir stundum til álags, læsingar og vandamála við bókun á uppgjöri. Einnig kemur það í veg fyrir að söluaðilar geti skráð tekjur og greiðslur í bókhaldið yfir daginn.

Opin forútgáfa af stofnun hlutastraumspöntunar sem er hluti af Retail, útgáfu 10.0.5 gerir það kleift að vinna úr færslum yfir daginn og eiga einungis eftir að vinna úr fjárhagslegri afstemmingu greiðslumáta og öðrum reiðufjárstjórnunarfærslum við lok dags. Þessi eiginleiki jafnar álagið af því að búa til sölupantanir, reikninga og framkvæma greiðslur yfir daginn. Þetta veitir betri skilning á afkomu og gefur kost á að skrá tekjur og greiðslur í bókhald nánast í rauntíma. 


## <a name="how-to-use-trickle-feed-based-posting"></a>Hvernig á að nota bókun með hlutastraum
  
1. Til að virkja bókun með hlutastraum fyrir smásölufærslur skal fara í **Kerfisstjórnun > Uppsetning > Skilgreining leyfis** og gera lykillinn fyrir **smásöluuppgjör** óvirkan.

2. Á sömu síðu skal virkja leyfislykilinn fyrir **Smásöluuppgjör (hlutastraumur) - Forskoðun**. Þegar þessi lykill er virkjaður skal ganga úr skugga um að engin uppgjör bíði þess að vera bókuð. 

> [!Important]
> Áður en leyfislykillinn fyrir **Smásöluuppgjör (hlutastraumur) - Forskoðun** er virkjaður skal ganga úr skugga um að engin uppgjör bíði þess að vera bókuð.

3. Núverandi uppgjörsskjali verður skipt upp í tvær mismunandi tegundir, færsluuppgjör og fjárhagsskýrslu.

      - Færsluuppgjörið mun taka til allra óbókaðra og villuleitaðra smásölufærslna og stofna sölupantanir, sölureikninga, færslubækur fyrir greiðslur og afslætti og tekju-/útgjaldafærslur með þeim takti sem er grunnstilltur. Grunnstilla ætti ferlið til að keyra á hárri tíðni svo fylgiskjöl séu búin til þegar smásölufærslunum er hlaðið upp í Retail Headquarters í gegnum P-verkið. Með færsluuppgjöri sem býr sjálft til sölupantanir og sölureikninga er engin þörf á að grunnstilla runuvinnsluna **Bóka birgðir**. Hins vegar er enn hægt að nota hana til að uppfylla tilteknar viðskiptaþarfir sem notandinn kann að hafa.  
      
     - Fjárhagsskýrslan er stillt á þann hátt að hún er búin til í lok dags og styður aðeins lokunaraðferðina **Vakt**. Þessi skýrsla takmarkast við fjárhagslega afstemmingu og býr eingöngu til færslubækur fyrir upphæðamismun á milli talinnar upphæðar og færsluupphæðar fyrir mismunandi greiðslumáta ásamt færslubókum fyrir aðrar reiðufjárstjórnunarfærslur.   

4. Til að reikna út færsluuppgjörið skal smella á **Smásala > Upplýsingatækni smásölu > Sölustaðarbókun > Reikna færsluuppgjör í runu**. Til að bóka yfirlit færsluuppgjörs í runu skal smella á **Smásala > Upplýsingatækni smásölu > Sölustaðarbókun > Bóka færsluuppgjör í runu**.

5. Til að reikna út fjárhagsskýrsluna skal smella á **Smásala > Upplýsingatækni smásölu > Sölustaðarbókun > Reikna fjárhagsskýrslur í runu**. Til að bóka fjárhagsskýrslur í runu skal smella á **Smásala > Upplýsingatækni smásölu > Sölustaðarbókun > Bóka fjárhagsskýrslur í runu**.

> [!NOTE]
> Valmyndaratriðin **Smásala > Upplýsingatækni smásölu > Sölustaðarbókun > Reikna uppgjör í runu** og **Smásala > Upplýsingatækni smásölu > Sölustaðarbókun > Bóka uppgjör í runu** verða fjarlægð með tilkomu þessa nýja eiginleika.

Einnig er hægt að búa til gerðir af færsluuppgjörum og fjárhagsskýrslum handvirkt. Opna skal **Smásala > Rásir > Smásöluverslanir** og smella á **Smásöluuppgjör**. Smella skal á **Nýtt** og velja svo þá gerð uppgjörs sem stofna á. Svæðin á síðunni **Smásöluuppgjör** og aðgerðir í hlutanum **Uppgjörsflokkur** á síðunni birta gögn og aðgerðir í samræmi við valda gerð uppgjörs.
