---
title: Flytja inn skilgreiningu úr Lifecycle Services
description: Þetta efnisatriði útskýrir hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur flutt inn nýja útgáfu af skilgreiningarsnið fyrir rafræna skýrslugerð (ER) úr Microsoft Dynamics Lifecycle Services (LCS).
author: NickSelin
manager: AnnBe
ms.date: 09/14/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5c43cdce8d073f04a3158c8beb13a5376e669a4c
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684452"
---
# <a name="import-a-configuration-from-lifecycle-services"></a>Flytja inn skilgreiningu úr Lifecycle Services

[!include [banner](../../includes/banner.md)]

Þetta efnisatriði útskýrir hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur flutt inn nýja útgáfu af [Skilgreiningarsnið fyrir rafræna skýrslugerð (ER)](../general-electronic-reporting.md#Configuration) úr [Eignasafn á verkefnastigi](../../lifecycle-services/asset-library.md) í Microsoft Dynamics Lifecycle Services (LCS).

Í þessu dæmi velurðu þá útgáfu af skilgreiningu fyrir Rafræna skýrslugerð sem þér hugnast, og flytur hana inn fyrir sýnifyrirtæki sem kallast Litware, Inc. Þessum skrefum má ljúka í hvaða fyrirtæki sem er þar sem ER skilgreiningar eru samnýttar á milli fyrirtækja. Til að ljúka þessum skrefum verður fyrst að ljúka við skrefin í [Hlaða skilgreiningu upp í Lifecycle Services fyrir rafræna skýrslugerð](er-upload-configuration-into-lifecycle-services.md). Aðgangur að LCS er einnig nauðsynlegur.

1. Skráðu þig inn í forritið með því að nota eitt af eftirfarandi hlutverkum:

    - Þróunaraðili rafrænnar skýrslulausnar
    - Kerfisstjóri

2. Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.
3. Velja **Skilgreiningar**.

<a name="accessconditions"></a>
> [!NOTE]
> Ganga skal úr skugga um að núverandi Dynamics 365 Finance notandi sé aðili að LCS-verki sem inniheldur eignasafnið sem notandinn vill fá [aðgang](../../lifecycle-services/asset-library.md#asset-library-support) að til að flytja inn skilgreiningar rafrænnar skýrslugerðar.
>
> Ekki er hægt að opna LCS-verk úr rafrænni gagnageymslu sem stendur fyrir annað lén en lénið sem er notað í Finance. Ef það er reynt verður tæmandi listi yfir LCS-verk sýndur og ekki er hægt að flytja inn skilgreiningar rafrænnar skýrslugerðar úr verkstigi eignasafns í LCS. Til að fá aðgang að eignasöfnum verks úr geymslu sem er notuð til að flytja inn skilgreining rafrænnar skýrslugerðar skal skrá sig inn í Finance með því að nota skilríki notanda sem tilheyrir leigjandanum (léninu) sem gildandi Finance tilviki hefur verið úthlutað til.

## <a name="delete-a-shared-version-of-a-data-model-configuration"></a>Eyða samnýttri útgáfu skilgreiningar gagnalíkans

1. Á síðunni **Skilgreiningar**, í skilgreiningartrénu, skal velja **Dæmi um skilgreiningu líkans**.

    Fyrsta útgáfa af stillingum sýnigagnalíkansins var stofnuð og birt í LCS þegar lokið var við skrefin í [Hlaða skilgreiningu upp í Lifecycle Services fyrir rafræna skýrslugerð](er-upload-configuration-into-lifecycle-services.md). Í þessu ferli muntu eyða þeirri útgáfu á skilgreiningu rafrænnar skýrslugerðar. Þú munt síðan flytja inn þá útgáfu úr LCS síðar í þessu efnisatriði.

2. Í listanum skal finna og velja þá skráningu sem óskað er eftir.

    Í þessu dæmi skal velja útgáfu þessarar skilgreiningar sem hefur stöðuna **Samnýtt**. Þessi staða tilgreinir að skilgreiningin sé nú birt í LCS.

3. Veljið **Breyta stöðu**.
4. Veldu **Hætta**.

    Með því að breyta stöðu valinnar útgáfu úr **Samnýtt** í **Hætt** er hægt að eyða einingunni.

5. Veljið **Í lagi**.
6. Í listanum skal finna og velja þá skráningu sem óskað er eftir.

    Í þessu dæmi skal velja útgáfu skilgreiningarinnar sem hefur stöðuna **Hætt**.

7. Veljið **Eyða**.
8. Velja skal **Já**.

    Athugið að einu drögin að útgáfu 2 af hinni völdu skilgreiningu gagnalíkans eru nú tiltæk.

9. Lokið síðunni.

## <a name="import-a-shared-version-of-a-data-model-configuration-from-lcs"></a>Flytja inn samnýttu útgáfu skilgreiningar gagnalíkans úr LCS

1. Fara í **Fyrirtækisstjórnun \> Vinnusvæði \> Rafræn skýrslugerð**.

2. Í **veitandi skilgreininga** hlutanum, veljið gluggareitinn **Litware, Inc**.

3. Í **Litware, Inc.** reitnum, skal velja **Geymslur**.

    Nú getur þú opnað lista yfir gagnasöfn fyrir skilgreiningarveitur fyrir Litware, Inc.

4. Veljið **Opna**.

    Veldu **LCS**-gagnasafnið í þessu dæmi og opnaðu það. Þú verður að vera með [aðgang](#accessconditions) að LCS-verkinu og eignasafninu sem er opnað með því að velja ER-gagnageymsluna.

5. Í listanum skal merkja valda línu.

    Í þessu dæmi skal velja fyrstu útgáfu af **Dæmi um líkanaskilgreiningu** á útgáfulistanum.

6. Velja **Innflutningur**.
7. Veldu **Já** til að staðfesta innflutning valda útgáfu úr LCS.

    Upplýsingaskilaboð staðfesta að valin útgáfa hafi verið flutt inn.

8. Lokið síðunni.
9. Lokið síðunni.
10. Velja **Skilgreiningar**.
11. Veljið **Dæmi um skilgreiningu líkans** í trénu.
12. Í listanum skal finna og velja þá skráningu sem óskað er eftir.

    Í þessu dæmi skal velja útgáfu þessarar skilgreiningar sem hefur stöðuna **Samnýtt**.

    Athugið að samnýtt útgáfa 1 hinnar völdu skilgreiningar gagnalíkans er nú tiltæk.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]