--- 
title: "Setja upp handvirka pökkun (aðeins febrúar og maí 2016)"
description: "Pökkunarferli gerir kleift að sannprófa og pakka afurðir í gáma."
author: ShylaThompson
manager: AnnBe
ms.date: 11/04/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 7f992a6a1655cd868d79228c490d59b46bfae715
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-manual-packing-february--may-2016-only"></a>Setja upp handvirka pökkun (aðeins febrúar og maí 2016)

[!include [task guide banner](../../includes/task-guide-banner.md)]

Pökkunarferli gerir kleift að sannprófa og pakka afurðir í gáma. Í þessu ferli starfsmenn vöruhússins taka vörur frá staðsetningum geymslu og flytja þær í pökkunarstöð þar sem þær athuga vörumagn og gerðir og úthluta þeim til viðeigandi gáma. Þegar gámur er alveg fullur, geta þeir loka honum og færa hana til úthliða, og vörurnar eru tilbúnar til sendingar. Þessi aðferð notar sýnigögn USMF fyrirtækisins.


## <a name="set-up-location-profiles"></a>Setja upp forstillingar staðsetningar
1. Fara í vöruhúsakerfi > Uppsetning > Vöruhús > Forstillingar staðsetningar.
2. Smellið á „Nýtt“.
    * Forstilling staðsetningar er notað fyrir pökkunarstöðvar og inniheldur upplýsingar um og reglur fyrir staðsetningu.  
3. Færa inn gildi í reitnum Kenni forstillingar staðsetningar.
4. Í reitinn Heiti skal slá inn gildi.
5. Sláðu inn eða veldu gildi í reitnum Staðsetningarsnið
6. Færa inn eða veljið gildi í svæðinu gerð staðsetningu.
7. Velja skal Já í svæðinu Leyfa blandaðar vörur.
8. Velja skal Já í svæðinu Leyfa blandað birgðastaða.
9. Velja skal Já í Hnekkja reglum fyrir runudaga svæði.
10. Lokið síðunni.

## <a name="set-up-warehouse-management-parameters"></a>Setja upp færibreytur vöruhúsastjórnunar 
1. Fara í vöruhúsakerfi > Uppsetning > Færibreytur vöruhúsakerfis.
2. Smella á pökkunarflipann
3. Veldu eða settu inn gildi í reitinn kenni forstillingar fyrir pökkunarstaðsetningu.
    * Velja forstillingu staðsetningar sem á að nota fyrir pökkun.  
4. Lokið síðunni.

## <a name="set-up-container-types"></a>Setja upp gámagerðir
1. Fara í vöruhúsakerfi  > Uppsetningu  > Gáma  > gámagerðir.
2. Smellið á „Nýtt“.
    * Hægt er að skilgreina gerðir gáma til að nota. Þú getur tilgreint efnisleg vídd ílátsins, þar á meðal töruþungi, hámarks þyngd, hámarksrúmmál, lengd, breidd og þyngd.  Eigindirnar eru sérsniðnir reitir sem leyfa þér að bæta fleiri víddum við gámagerð.     
3. Færa inn gildi í svæðinu kóði gámagerðar.
4. Sláið inn gildi í reitnum „Lýsing“.
5. Í reitinn Umbúðaþyngd skal slá inn númer.
6. Í reitinn hámarksþyngd skal slá inn númer.
7. Í reitinn Magn skal slá inn númer.
8. Í reitinn Lengd skal slá inn númer.
9. Færið númer inn í svæðið breidd.
10. Færið númer inn í svæðið hæð.
11. Smellið á „Vista“.
12. Lokið síðunni.

## <a name="set-up-packing-profiles"></a>Setja upp pökkunarforstillingar
1. Fara í vöruhúsakerfi > Uppsetning > Pökkun > Forstillingar umbúða.
2. Smellið á „Nýtt“.
3. Í reitinn auðkenni forstilling umbúða skal færa inn gildi.
4. Sláið inn gildi í reitnum „Lýsing“.
5. Færa inn eða veljið gildi í reit fyrir auðkenni lokunarreglu gáms.
    * Auðkenni lokunarreglu gáms er valfrjálst og er sjálfgefin forstillingu lokunar gáms fyrir þessa forstillingu umbúða.  
6. Í reitnum auðkennisstilling gáms velurðu valkost.
    * Þessi valkostur ákvarðar hvort kenni gáms verður sjálfkrafa myndað þegar gámur er stofnaður eða ef kenni gáms verður búið til handvirkt.  
7. Færa inn eða veljið gildi í svæðinu gerð gáms.
    * Gámagerð er notuð að sjálfgefnu þegar nýjum gámi er stofnuð.  
8. Velja Stofna sjálfkrafa gám við lokun gáms gátreitur.
9. Smellið á „Vista“.
10. Lokið síðunni.

## <a name="set-up-container-closing-profiles"></a>Setja upp lokunarreglu gáms
1. Fara í vöruhúsakerfi > Uppsetningu > Gáma > Lokunarregla gáms.
    * Lokunarreglur gáma skilgreina hvað gerist þegar gámi er lokað. Þú getur sett upp margar forstillingar fyrir lokun gáms.       
2. Smellið á „Nýtt“.
3. Færa inn gildi í reit fyrir auðkenni lokunarreglu gáms.
4. Sláið inn gildi í reitnum „Lýsing“.
5. Í reitnum Skrá skal velja valkost.
    * Tilgreina hvort skráning munu eiga sér stað þegar gáma er lokað eða þegar sending er staðfest. Athugið að skráning krefst flutningsstjórnun. Verður að innleiða skráningu í flutningsstjórnunarvélar til þess að virka  
6. Sláðu inn eða veldu gildi í reitnum Vöruhús.
7. Í reitinn sjálfgefin staðsetning lokasendingar skal slá inn eða velja gildi.
    * Þetta verður staðsetning sem vörur verða færð á eftir gámarnir eru lokaðar. Þessi staðsetningar þarf að hafa forstillingu fyrir staðsetningu skilgreinda í færibreytur vörugeymslu.  
8. Í reitinn þyngdareining skal slá inn eða velja gildi.
9. Smellið á „Vista“.


