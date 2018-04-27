--- 
title: "Flytja inn skilgreiningu úr Lifecycle Services fyrir rafræna skýrslugerð (ER)"
description: "Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur flutt inn nýja útgáfu af skilgreiningarsnið fyrir rafræna skýrslugerð (ER) úr Microsoft Lifecycle Services (LCS)."
author: NickSelin
manager: AnnBe
ms.date: 05/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 9eb4f54897c84b98828c927f0f93613583fd4599
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="import-a-configuration-from-lifecycle-services-for-electronic-reporting-er"></a>Flytja inn skilgreiningu úr Lifecycle Services fyrir rafræna skýrslugerð (ER)

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur flutt inn nýja útgáfu af skilgreiningarsnið fyrir rafræna skýrslugerð (ER) úr Microsoft Lifecycle Services (LCS).

Í þessu dæmi velurðu þá útgáfu af skilgreiningu fyrir Rafræna skýrslugerð sem þér hugnast, og flytur hana inn fyrir sýnifyrirtæki, Litware, Inc. Þessi skref má framkvæma í hvaða fyrirtæki sem er þar sem ER skilgreiningar eru samnýttar á milli fyrirtækja. Til að ljúka þessum skrefum, verður fyrst að ljúka við skrefin í ferlinu „Hlaða upp Hlaða upp skilgreiningu Rafræn skýrslugerð í Lifecycle Services". Aðgangur að LCS er einnig nauðsynlegur til að ljúka þessum skrefum.

1. Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.
2. Smellt er á Skilgreiningum.

## <a name="delete-a-shared-version-of-data-model-configuration"></a>Eyða samnýttu útgáfu skilgreiningar gagnalíkans.
1. Veljið 'dæmi um skilgreiningu líkans', í trénu.
    * Fyrsta útgáfa af dæmi um skilgreiningu gagnalíkans hefur verið stofnuð og birt í LVS á meðan á ferlinu "hlaða upp skilgreiningu Rafræn skýrslugerð í Lifecycle Services" stóð. Í þessu ferli verður að eyða þessi útgáfa skilgreiningar Rafræn skýrslugerð. Þessi útgáfa af dæmi um skilgreiningu gagnalíkans verður flutt inn síðar úr LCS.  
2. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
    * Veljið útgáfu þessarar skilgreiningar sem er í stöðunni "samnýtt". Þessi staða tilgreinir að skilgreiningin sé nú birt í LCS.  
3. Smellið á „Breyta stöðu“.
4. Smellið á hætta notkun.
    * Breyta stöðu valda útgáfu úr 'Samnýttum' til 'hætt í notkun" til að gera tiltækt fyrir eyðingu.  
5. Smellið á „Í lagi“.
6. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
    * Veljið útgáfu þessarar skilgreiningar sem hefur stöðuna "hætt í notkun".  
7. Smellið á Eyða.
8. Smella á Já.
    * Athugið að eina drög að útgáfu 2 hinnar völdu skilgreiningar gagnalíkans er tiltækt.  
9. Lokið síðunni.

## <a name="import-a-shared-version-of-data-model-configuration-from-lcs"></a>Flytja inn samnýttu útgáfu skilgreiningar gagnalíkans.
1. Í listanum skal merkja valda línu.
    * Opna lista yfir geymslur fyrir „Litware, Inc.“ veitandi skilgreiningar  
2. Smella á Geymslur.
3. Smellt er á Opin.
    * Velja lcs-gagnasafn og opna hana.  
4. Í listanum skal merkja valda línu.
    * Veljið fyrsta útgáfa "dæmi um skilgreiningu líkans" í útgáfulistanum.  
5. Smelltu á Flytja inn.
6. Smella á Já.
    * Staðfesta innflutning valda útgáfu úr LCS.  
    * Athugið að upplýsingaskilaboð (ofan skjámyndin) staðfestir að tókst að flytja inn valda útgáfu.  
7. Lokið síðunni.
8. Lokið síðunni.
9. Smellt er á Skilgreiningum.
10. Veljið 'dæmi um skilgreiningu líkans', í trénu.
11. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
    * Veljið útgáfu þessarar skilgreiningar sem hefur stöðuna "samnýtt".  
    * Athugið að samnýtt útgáfu 1 hinnar völdu skilgreiningar gagnalíkans er tiltækt nú líka.  


