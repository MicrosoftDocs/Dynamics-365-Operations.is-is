---
title: Flytja inn skilgreiningu úr Lifecycle Services
description: Þessi grein lýsir því hvernig á að flytja inn nýja útgáfu af rafrænni skýrslugerð (ER) uppsetningu frá Microsoft Dynamics Lífsferilsþjónusta (LCS).
author: kfend
ms.date: 06/17/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionRepositoryTable, ERSolutionImport
ms.openlocfilehash: 92c5d010430b38cb6c11a87283a2f7d4c29484f8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290365"
---
# <a name="import-a-configuration-from-lifecycle-services"></a>Flytja inn skilgreiningu úr Lifecycle Services

[!include [banner](../../includes/banner.md)]

Þessi grein útskýrir hvernig notandi í hlutverki Kerfisstjóra eða þróunaraðila rafrænna skýrslugerðar getur flutt inn nýja útgáfu af [Uppsetning rafrænnar skýrslugerðar (ER).](../general-electronic-reporting.md#Configuration) frá [Eignasafn á verkefnastigi](../../lifecycle-services/asset-library.md) inn Microsoft Dynamics Lífsferilsþjónusta (LCS).

> [!IMPORTANT]
> Verið er að [úrelda](../../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release) notkun LCS sem gagnageymslu fyrir skilgreiningar rafrænnar skýrslugerðar. Frekari upplýsingar er að finna í [Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) úrelding á geymslu](../../../../finance/localizations/rcs-lcs-repo-dep-faq.md).

Í þessu dæmi velurðu þá útgáfu af skilgreiningu fyrir Rafræna skýrslugerð sem þér hugnast, og flytur hana inn fyrir sýnifyrirtæki sem kallast Litware, Inc. Þessum skrefum má ljúka í hvaða fyrirtæki sem er þar sem ER skilgreiningar eru samnýttar á milli fyrirtækja. Til að ljúka þessum skrefum verður fyrst að ljúka við skrefin í [Hlaða skilgreiningu upp í Lifecycle Services fyrir rafræna skýrslugerð](er-upload-configuration-into-lifecycle-services.md). Aðgangur að LCS er einnig nauðsynlegur.

1. Skráðu þig inn í forritið með því að nota eitt af eftirfarandi hlutverkum:

    - Þróunaraðili rafrænnar skýrslulausnar
    - Kerfisstjóri

2. Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.
3. Velja **Skilgreiningar**.

<a name="accessconditions"></a>
> [!NOTE]
> Gakktu úr skugga um að núverandi Dynamics 365 Finance notandi sé meðlimur í LCS verkefninu sem inniheldur eignasafnið sem notandinn vill [aðgangur](../../lifecycle-services/asset-library.md#asset-library-support) til að flytja inn ER stillingar.
>
> Ekki er hægt að opna LCS-verk úr rafrænni gagnageymslu sem stendur fyrir annað lén en lénið sem er notað í Finance. Ef það er reynt verður tæmandi listi yfir LCS-verk sýndur og ekki er hægt að flytja inn skilgreiningar rafrænnar skýrslugerðar úr verkstigi eignasafns í LCS. Til að fá aðgang að eignasöfnum verks úr geymslu sem er notuð til að flytja inn skilgreining rafrænnar skýrslugerðar skal skrá sig inn í Finance með því að nota skilríki notanda sem tilheyrir leigjandanum (léninu) sem gildandi Finance tilviki hefur verið úthlutað til.

## <a name="delete-a-shared-version-of-a-data-model-configuration"></a>Eyða samnýttri útgáfu skilgreiningar gagnalíkans

1. Á síðunni **Skilgreiningar**, í skilgreiningartrénu, skal velja **Dæmi um skilgreiningu líkans**.

    Fyrsta útgáfa af stillingum sýnigagnalíkansins var stofnuð og birt í LCS þegar lokið var við skrefin í [Hlaða skilgreiningu upp í Lifecycle Services fyrir rafræna skýrslugerð](er-upload-configuration-into-lifecycle-services.md). Í þessu ferli muntu eyða þeirri útgáfu á skilgreiningu rafrænnar skýrslugerðar. Þú munt síðan flytja þá útgáfu frá LCS síðar í þessari grein.

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
