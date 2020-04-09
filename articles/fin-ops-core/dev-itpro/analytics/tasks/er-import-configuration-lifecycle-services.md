---
title: Rafræn skýrslugerð Flytja inn skilgreiningu úr Lifecycle Services
description: Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur flutt inn nýja útgáfu af skilgreiningarsnið fyrir rafræna skýrslugerð (ER) úr Microsoft Lifecycle Services (LCS).
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable,  ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 67e09e3187ac49e12727116f55066b64a386e2de
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142387"
---
# <a name="er-import-a-configuration-from-lifecycle-services"></a>Rafræn skýrslugerð Flytja inn skilgreiningu úr Lifecycle Services

[!include [banner](../../includes/banner.md)]

Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur flutt inn nýja útgáfu af skilgreiningarsnið fyrir rafræna skýrslugerð (ER) úr Microsoft Lifecycle Services (LCS).

Í þessu dæmi velurðu þá útgáfu af skilgreiningu fyrir Rafræna skýrslugerð sem þér hugnast, og flytur hana inn fyrir sýnifyrirtæki, Litware, Inc. Þessi skref má framkvæma í hvaða fyrirtæki sem er þar sem ER skilgreiningar eru samnýttar á milli fyrirtækja. Til að ljúka þessum skrefum, verður fyrst að ljúka við skrefin í ferlinu „Hlaða upp Hlaða upp skilgreiningu Rafræn skýrslugerð í Lifecycle Services". Aðgangur að LCS er einnig nauðsynlegur til að ljúka þessum skrefum.

1. Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.
2. Smellt er á Skilgreiningum.

## <a name="delete-a-shared-version-of-data-model-configuration"></a>Eyða samnýttu útgáfu skilgreiningar gagnalíkans.
1. Veljið 'dæmi um skilgreiningu líkans', í trénu.
    * Fyrsta útgáfa af dæmi um skilgreiningu gagnalíkans hefur verið stofnuð og birt í LVS á meðan á ferlinu „Hlaða upp skilgreiningu Rafræn skýrslugerð í Lifecycle Services” stóð. Í þessu ferli verður að eyða þessi útgáfa skilgreiningar Rafræn skýrslugerð. Þessi útgáfa af dæmi um skilgreiningu gagnalíkans verður flutt inn síðar úr LCS.  
2. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
    * Veljið útgáfu þessarar skilgreiningar sem er í stöðunni „Samnýtt”. Þessi staða tilgreinir að skilgreiningin sé nú birt í LCS.  
3. Smellið á „Breyta stöðu“.
4. Smellið á hætta notkun.
    * Breyta stöðu valinnar útgáfu úr „Samnýtt” í „Hætt í notkun” til að gera tiltækt fyrir eyðingu.  
5. Smellt er á Í lagi.
6. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
    * Veljið útgáfu þessarar skilgreiningar sem hefur stöðuna „Hætt í notkun”.  
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
    * Veljið útgáfu þessarar skilgreiningar sem hefur stöðuna "Samnýtt".  
    * Athugið að samnýtt útgáfu 1 hinnar völdu skilgreiningar gagnalíkans er tiltækt nú líka.  

