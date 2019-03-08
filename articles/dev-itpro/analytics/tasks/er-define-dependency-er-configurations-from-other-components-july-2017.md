---
title: Skilgreina hversu mikil áhrif ER grunnstillingar hafa á aðra hluta
description: Til að ljúka þessum skrefum, verður fyrst að ljúka við skrefin í verkefnaleiðbeiningar, Rafræn skýrslugerð Stýring grunnstillinga vörpunar líkans, og hafa aðgang að Microsoft Dynamics Lifecycle Services (LCS).
author: NickSelin
manager: AnnBe
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 18eb8de7c851e5477d93a00f744fe56929c43ca2
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "365087"
---
# <a name="define-the-dependency-of-er-configurations-on-other-components"></a>Skilgreina hversu mikil áhrif ER grunnstillingar hafa á aðra hluta

[!include [task guide banner](../../includes/task-guide-banner.md)]

Til að ljúka þessum skrefum, verður fyrst að ljúka við skrefin í verkefnaleiðbeiningar, Rafræn skýrslugerð Stýring grunnstillinga vörpunar líkans, og hafa aðgang að Microsoft Dynamics Lifecycle Services (LCS).

Þetta ferli sýnir hvernig skal hanna grunnstillingar fyrir Rafræna skýrslugerð og tilgreina fylgni við aðra hugbúnaðarhluta, svo þú getir hjálpað til við að tryggja að grunnstillingu sé rétt hlaðið niður á sérstaka útgáfu af Microsoft Dynamics 365 for Finance and Operations. Í þessu dæmi muntu stofna nauðsynlega grunnstillingar Rafræn skýrslugerð fyrir sýnifyrirtækið, Litware, Inc. 

Þetta ferli er hugsað fyrir þá notendur sem hefur verið úthlutað hlutverkum Kerfisstjóra eða Þróunaraðila rafrænnar skýrslugerðar. Þessi skref er hægt að framkvæma í hvaða fyrirtæki er, þar sem grunnstillingar rafrænnar skýrslugerðar eru samnýttar á milli fyrirtækja. 

1. Fara í Fyrirtækisstjórnun > Rafræn skýrslugerð > Grunnstillingar.
    * Gangið úr skugga um að grunnstillingatréð innihaldi „Sýnigagnalíkanið“ grunnstillinguna og undirstig atriða. Að öðrum kosti skal ljúka við skrefin í verkefnaleiðbeiningunum, Rafræn skýrslugerð Stjórna grunnstillingum fyrir vörpun líkans, og svo byrja svo aftur á þessum leiðbeiningum.   

## <a name="define-the-dependency-of-er-configurations-from-other-components"></a>Skilgreina fylgni grunnstillinga rafrænnar skýrslugerðar við aðra hluta
1. Stækkið „Sýnigagnalíkan“, í trénu.
2. Veljið „Sýnigagnalíkan/Sýnivörpun“, í trénu.
    * Við völdum útgáfu drög að grunnstillingum „Sýnivörpun“ vörpun líkans. Nú munum við skilgreina fylgni þess við aðra hluti hugbúnaðarins. Þetta skref er hugsað sem skilyrði fyrir stjórnun niðurhals á þessari útgáfu grunnstillinga frá Rafræn skýrslugerð Geymsla og allri frekari notkun á þessari útgáfu.   
3. Stækka hlutann Skilyrði
    * Athugið að skilyrðaflokkur „Framkvæmdir“ hefur á þessu stigi verið bætt sjálfkrafa við. Flokkurinn inniheldur skilyrðahlutana sem taka til grunnstillingar gagnalíkansins og er merkt sem Framkvæmd. Þessi merking þýðir að „Sýnivörpun“ grunnstillingar vörpunar er talið samsvara því að setja „Sýnigagnalíkan“ gagnalíkanið í framkvæmd. Þar af leiðandi mun þessi hluti neyða Rafræn skýrslugerð til að hlaða niður grunnstillingum vörpunarinnar, „Sýnivörpun“ frá geymslu Rafræn skýrslugerð í hvert sinn sem grunnstillingar líkans „Sýnigagnalíkan“ er hlaðið niður.   
4. Smellið á „Breyta“.
    * Hægt er að tilgreina staka fylgni núverandi útgáfu grunnstillingar hugbúnaðarhluta með því að nota skilgreiningu tegundar hlutans, og annað hvort útgáfu af hlutanum eða flokk útgáfna af hlutanum.  
    * Ákjósanlega fylgni er hægt að setja saman í flokk. Þegar „Allir“ tegundaflokkar eru valdir, er fylgniskilyrði þessa flokks talið uppfyllt þegar hvert fylgniskilyrði frá þessum flokki og undirstigsflokki er uppfyllt. Þegar „Einn af“ tegundaflokkum er valinn, er fylgniskilyrði þessa flokks talið uppfyllt þegar að minnsta kosti eitt fylgniskilyrði frá þessum flokki er uppfyllt.   
5. Smellið á „Nýtt“.
6. Veljið Hluti afurðaskilyrða
7. Velja Microsoft Dynamics 365 for Operations (1611).
8. Í reitinn Útgáfa skal slá inn „[7.1.1541.3036,8)“.
    * [7.1.1541.3036,8)  
    * Fylgni sem þú færir inn verður metin þegar þessi grunnstilling er hlaðið niður frá einhverri Rafræn skýrslugerð geymslu. Þessi útgáfa grunnstillingu verður halað niður frá Rafræn skýrslugerð geymslu þegar útgáfa 1 af „Sýnigagnalíkani“ grunnstillingu er annað hvort þegar til staðar eða fyrirfram hlaðið niður. Ef henni er fyrirfram hlaðið niður, verður að ljúka því í Finance and Operations, útgáfu 7.1.1541.3036 eða síðar, en má ekki fara fram úr útgáfu 8.   
9. Smellið á „Vista“.
10. Lokið síðunni.
11. Smellið á „Breyta stöðu“.
12. Smelltu á Ljúka.
13. Smellið á „Í lagi“.
14. Veljið „Sýnigagnalíkan/Sýnivörpun (valkostur)“, í trénu.
15. Smellið á „Breyta“.
16. Smellið á „Nýtt“.
17. Veljið Hluti afurðaskilyrða
18. Velja Microsoft Dynamics AX 7.0 RTW.
19. Í reitinn Útgáfa skal slá inn „[7.0.1265.3015,7.1)“.
    * [7.0.1265.3015,7.1)  
    * Fylgni verður metin þegar grunnstillingu er hlaðið niður frá einhverri Rafræn skýrslugerð geymslu. Þessi útgáfa grunnstillingu verður halað niður frá Rafræn skýrslugerð geymslu þegar útgáfa 1 af „Sýnigagnalíkani“ grunnstillingu er annað hvort þegar til staðar eða fyrirfram hlaðið niður. Ef henni er fyrirfram hlaðið niður, verður að ljúka því í Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, útgáfu 7.0.1265.3015 eða síðar, en má ekki fara fram úr útgáfu 1.   
20. Smellið á „Vista“.
21. Lokið síðunni.
22. Smellið á „Breyta stöðu“.
23. Smelltu á Ljúka.
24. Smellið á „Í lagi“.

## <a name="configure-the-er-repository"></a>Skilgreina geymsla Rafræn skýrslugerðar
1. Lokið síðunni.
2. Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.
    * Opna lista yfir geymslur fyrir núverandi veitu Rafræn skýrslugerð, Litware, Inc.  
3. Í listanum skal merkja valda línu.
4. Smella á Geymslur.
5. Smellt er á Sýna síur.
6. Sláðu inn síugildi „LCS“ í „Heiti tegundar“ reitnum með því að nota „inniheldur“ síuvirknitáknið
    * Ef LCS geymslan er þegar skráð fyrir núverandi veitu Rafræn skýrsla, geturðu sleppt þeim skrefum sem eftir eru í þessu undirverkefni. Ef LCS geymslan er ekki þegar skráð, skal ljúka þeim skrefum sem eftir eru.   
7. Smelltu á Bæta við til að opna felligluggann.
8. Í reitnum gerð geymslu fyrir grunnstillingar, færðu inn "LCS".
9. Smellið á Stofna gagnasafn.
10. Færa inn eða veljið gildi í svæðinu verk.
    * Veljið viðeigandi LCS-verk úr uppflettingu í reitnum „Verk“.  
11. Smellið á „Í lagi“.
12. Lokið síðunni.

## <a name="upload-configurations-to-lcs"></a>Hlaða upp Grunnstillingar í LCS
1. Smelltu á Grunnstillingar skýrslugerðar
2. Veljið „Sýnigagnalíkan“, í trénu.
3. Velja lokinni útgáfu af núgildandi grunnstillingu.
4. Smellið á „Breyta stöðu“.
5. Smellt er á samnýta.
6. Smellið á „Í lagi“.
    * Útgáfa 1 af þessum grunnstillingum líkans hefur verið hlaðið upp í LCS með því að nota LCS verk fyrir Rafræn skýrslugerð geymslu sem áður var grunnstillt.   
7. Stækkið „Sýnigagnalíkan“, í trénu.
8. Veljið „Sýnigagnalíkan/Sýnivörpun“, í trénu.
9. Velja lokinni útgáfu af núgildandi grunnstillingu.
10. Smellið á „Breyta stöðu“.
11. Smellt er á samnýta.
12. Smellið á „Í lagi“.
    * Útgáfa 1.1 af þessum grunnstillingum vörpun líkans hefur verið hlaðið upp í LCS með því að nota LCS verk fyrir Rafræn skýrslugerð geymslu sem áður var grunnstillt.   
13. Veljið „Sýnigagnalíkan/Sýnivörpun (valkostur)“, í trénu.
14. Velja lokinni útgáfu af núgildandi grunnstillingu.
15. Smellið á „Breyta stöðu“.
16. Smellt er á samnýta.
17. Smellið á „Í lagi“.
    * Útgáfa 1.1 af þessum grunnstillingum vörpun líkans hefur verið hlaðið upp í LCS með því að nota LCS verk fyrir Rafræn skýrslugerð geymslu sem áður var grunnstillt.   

## <a name="evaluate-er-configuration-dependencies"></a>Meta fylgni grunnstillinga Rafræn skýrslugerð
    * Við munum eyða stofnuðum grunnstillingum úr kerfinu og hlaða þeim aftur niður úr LCS geymslunni.  
1. Veljið „Sýnigagnalíkan/Sýnivörpun“, í trénu.
2. Smellið á Eyða.
3. Smella á Já.
4. Veljið „Sýnigagnalíkan/Sýnivörpun (valkostur)“, í trénu.
5. Smellið á Eyða.
6. Smella á Já.
7. Veljið „Sýnigagnalíkan/Sýnisnið“, í trénu.
8. Smellið á Eyða.
9. Smella á Já.
10. Veljið „Sýnigagnalíkan“, í trénu.
11. Smellið á Eyða.
12. Smella á Já.
13. Lokið síðunni.
    * Opna lista yfir geymslur fyrir núverandi veitu Rafræn skýrslugerð, Litware, Inc.  
14. Smella á Geymslur.
15. Smellt er á Sýna síur.
16. Sláðu inn síugildi „LCS“ í „Heiti tegundar“ reitnum með því að nota „inniheldur“ síuvirknitáknið
17. Smellt er á Opin.
18. Veljið „Sýnigagnalíkan“, í trénu.
    * Athugið að hægt er að skoða mat á því hvort frumskilyrði hafi verið uppfyllt fyrir hverja útgáfu af Rafræn skýrslugerð grunnstillingar fyrir núgildandi geymslu. Til að skoða þetta mat, smellið á Athuga frumskilyrði.   
19. Smella á Prófa frumskilyrði
20. Smelltu á Flytja inn.
21. Smella á Já.
22. Lokið síðunni.
23. Lokið síðunni.
24. Lokið síðunni.
25. Fara í Fyrirtækisstjórnun > Rafræn skýrslugerð > Grunnstillingar.
26. Stækkið „Sýnigagnalíkan“, í trénu.
    * Athugið að grunnstillingum líkans „Sýnivörpun“ vörpun hefur verið hlaðið niður með völdum grunnstillingum gagnalíkans. Þessum tveimur skrám er hlaðið saman niður vegna þess að „Sýnivörpun“ hefur verið skilgreind sem framkvæmd valins gagnalíkans, og vegna þess að þær eru nothæfar í Finance and Operations. Grunnstillingu „Sýnivörpun (valmöguleiki)“ hefur ekki verið hlaðið niður vegna þess að skilyrði fyrir útgáfu forritsins sem er krafist eru ekki uppfyllt.   
    * Ef þú skráir þig inn í Dynamics 365 for Finance and Operations, Enterprise edition, skráir sömu veitu, færð aðgang að sama LCS verkinu, og hleður niður sömu grunnstillingum fyrir gagnalíkan, mun „Sýnivörpun (valmöguleiki)“ grunnstillingar hlaðast niður, en „Sýnivörpun“ grunnstillingar verður sleppt.  

