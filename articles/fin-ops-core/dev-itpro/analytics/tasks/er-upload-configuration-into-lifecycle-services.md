---
title: Hlaða upp skilgreiningu í Lifecycle Services
description: Í þessu efnisatriði er útskýrt hvernig á að stofna nýja skilgreiningu rafrænnar skýrslugerðar og hlaða hana upp í Microsoft Dynamics Lifecycle Services (LCS).
author: NickSelin
ms.date: 09/14/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0211fea7af303fe1dd7dce26f887bed4ed3b0f1e
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744916"
---
# <a name="upload-a-configuration-into-lifecycle-services"></a>Hlaða upp skilgreiningu í Lifecycle Services

[!include [banner](../../includes/banner.md)]

Þetta efnisatriði útskýrir hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stofnað [Skilgreiningarsnið fyrir rafræna skýrslugerð (ER)](../general-electronic-reporting.md#Configuration) og hlaðið því upp í [Eignasafn á verkefnastigi](../../lifecycle-services/asset-library.md) í Microsoft Dynamics Lifecycle Services (LCS).

Í þessu dæmi stofnarðu skilgreiningu og hleður henni upp í LCS fyrir sýnifyrirtæki sem kallast Litware, Inc. Þessi skref má framkvæma í hvaða fyrirtæki sem er þar sem ER skilgreiningar eru samnýttar á milli fyrirtækja. Til að ljúka þessum skrefum verður fyrst að ljúka við skrefin í [Stofna skilgreiningarveitendur og merkja þá sem virka](er-configuration-provider-mark-it-active-2016-11.md). Aðgangur að LCS er einnig nauðsynlegur.

1. Skráðu þig inn í forritið með því að nota eitt af eftirfarandi hlutverkum:

    - Þróunaraðili rafrænnar skýrslulausnar
    - Kerfisstjóri

2. Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.
3. Veljið **Litware, Inc.** og merkið það sem **Virkt**.
4. Velja **Skilgreiningar**.

<a name="accessconditions"></a>
> [!NOTE]
> Ganga skal úr skugga um að núverandi Dynamics 365 Finance notandi sé aðili að LCS-verki sem inniheldur [Eignasafnið](../../lifecycle-services/asset-library.md#asset-library-support) sem er notað til að flytja inn skilgreiningar rafrænnar skýrslugerðar.
>
> Ekki er hægt að opna LCS-verk úr rafrænni gagnageymslu sem stendur fyrir annað lén en lénið sem er notað í Finance. Ef það er reynt verður tæmandi listi yfir LCS-verk sýndur og ekki er hægt að flytja inn skilgreiningar rafrænnar skýrslugerðar úr verkstigi eignasafns í LCS. Til að fá aðgang að eignasöfnum verks úr geymslu sem er notuð til að flytja inn skilgreining rafrænnar skýrslugerðar skal skrá sig inn í Finance með því að nota skilríki notanda sem tilheyrir leigjandanum (léninu) sem gildandi Finance tilviki hefur verið úthlutað til.

## <a name="create-a-new-data-model-configuration"></a>Stofna nýjan skilgreiningu gagnalíkans

1. Opnið **Fyrirtækisstjórnun \> Rafræn skýrslugerð \> Skilgreiningar**.
2. Í **Skilgreiningar** skal velja **Stofna skilgreiningu** til að opna fellilistagluggann.

    Í þessu dæmi muntu stofna skilgreiningu sem inniheldur dæmi um gagnalíkan fyrir rafræn skjöl. Skilgreining gagnalíkans verður hlaðið upp í LCS síðar.

3. Í svæðið **Heiti** skal færa inn **Dæmi um skilgreining líkans**.
4. Í svæðið **Lýsing** skal færa **Dæmi um líkanaskilgreiningu**.
5. Veljið **Stofna skilgreiningu**.
6. Veljið **Hönnuður líkana**.
7. Veljið **Nýtt**.
8. Í reitinn **Heiti** skal færa inn **Aðgangsstaður**.
9. Veljið **Bæta við**.
10. Veljið **Vista**.
11. Lokið síðunni.
12. Veljið **Breyta stöðu**.
13. Velja **Lokið**.
14. Veljið **Í lagi**.
15. Lokið síðunni.

## <a name="register-a-new-repository"></a>Skrá nýtt gagnasafn

1. Fara í **Fyrirtækisstjórnun \> Vinnusvæði \> Rafræn skýrslugerð**.

2. Í **veitandi skilgreininga** hlutanum, veljið gluggareitinn **Litware, Inc**.

3. Í **Litware, Inc.** reitnum, skal velja **Geymslur**.

    Nú getur þú opnað lista yfir gagnasöfn fyrir skilgreiningarveitur fyrir Litware, Inc.

4. Veljið **Bæta við** til að opna fellilistagluggann.

    Nú er hægt að bæta við nýrri gagnageymslu.

5. Í reitnum **færa inn gagnasafn fyrir skilgreiningar** skal velja **LCS**.
6. Veljið **Stofna geymslu**.
7. Færa inn eða veljið gildi í svæðinu **Verk**.

    Í þessu dæmi skal velja viðeigandi LCS-verk. Þú verður að hafa [aðgang](#accessconditions) að verkinu.

8. Veljið **Í lagi**.

    Ljúka við nýja færslu í gagnasafni.

9. Í listanum skal merkja valda línu.

    Í þessu dæmi skal velja **LCS-færslu** gagnasafns.

    Athugið að skráð geymsla er merkt af núverandi veitu. Með öðrum orðum er aðeins hægt að setja upp skilgreiningar sem eru í eigu viðkomandi veitu í þessa geymslu og hlaða þeim upp í valið LCS-verk.

10. Veljið **Opna**.

    Þú opnar gagnasafn til að skoða lista yfir skilgreiningar Rafræn skýrslugerð. Ef valið verk hefur ekki enn verið notað fyrir samnýtingu á skilgreiningum rafrænnar skýrslugerðar er listinn auður.

11. Lokið síðunni.
12. Lokið síðunni.

## <a name="upload-a-configuration-into-lcs"></a>Hlaða skilgreiningu upp í LCS

1. Opnið **Fyrirtækisstjórnun \> Rafræn skýrslugerð \> Skilgreiningar**.
2. Á síðunni **Skilgreiningar**, í skilgreiningartrénu, skal velja **Dæmi um skilgreiningu líkans**.

    Þú verður að velja stofnaða skilgreiningu sem þegar hefur verið lokið.

3. Í listanum skal finna og velja þá skráningu sem óskað er eftir.

    Í þessu dæmi skal velja útgáfu þessarar skilgreiningar sem hefur stöðuna **Lokið**.

4. Veljið **Breyta stöðu**.
5. Veldu **Deila**.

    Stöðu skilgreiningar er breytt úr **Lokið** í **Samnýtt** þegar skilgreiningin er birt í LCS.

6. Veljið **Í lagi**.
7. Í listanum skal finna og velja þá skráningu sem óskað er eftir.

    Í þessu dæmi skal velja skilgreiningarútgáfu sem hefur stöðuna **Samnýtt**.

    Athugið að staða valda útgáfu hefur breyst úr **Lokið** í **Samnýttar**.

8. Lokið síðunni.
9. Veldu **Geymslur**.

    Nú getur þú opnað lista yfir gagnasöfn fyrir skilgreiningarveitur fyrir Litware, Inc.

10. Veljið **Opna**.

    Veldu **LCS**-gagnasafnið í þessu dæmi og opnaðu það.

    Athugið að valin skilgreining er sýnd sem eign valins LCS verks.

11. Opnaðu LCS með því að fara á <https://lcs.dynamics.com>.
12. Opna verk sem var notað áður fyrir geymsluskráningu.
13. Opnið eignasafnið fyrir verkið.
14. Veljið eignagerðin **GER-skilgreining**.

    Skilgreining rafrænnar skýrslugerðar sem var hlaðið upp ætti að vera á listanum.

    Athugaðu að upphalaðri LCS skilgreiningu er hægt að flytja inn í annað tilvik ef veiturnar hafa aðgang að þessu LCS verki.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]