---
title: Deila skilgreiningum rafrænnar skýrslugerðar í RCS/altækri geymslu með utanaðkomandi fyrirtækjum
description: Þessi grein útskýrir hvernig á að deila skilgreiningum rafrænnar skýrslugerðar í Microsoft Regulatory Configuration Services (RCS)/altækri geymslu beint með ytri fyrirtækjum.
author: kfend
ms.date: 05/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.custom: 97423
ms.assetid: ''
ms.search.form: ERSolutionTable, ERWorkspace, RCS
ms.openlocfilehash: d9400ffcede9924a01391a433b570651d3f0c5e4
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9284816"
---
# <a name="share-electronic-reporting-er-configurations-in-regulatory-configuration-services-rcs-global-repository-with-external-organizations"></a>Deila skilgreiningum rafrænnar skýrslugerðar í altækri geymslu Regulatory Configuration Services (RCS) með ytri fyrirtækjum

[!include [banner](../includes/banner.md)]

Hægt er að nota Microsoft Regulatory Configuration Services (RCS) til að deila skilgreiningum rafrænnar skýrslugerðar og gefa þær út til ytri fyrirtækja.

Eftirfarandi ferli útskýra hvernig RCS-notandi getur deilt útgáfu af skilgreiningu rafrænnar skýrslugerðar sem hefur verið grunnstillt í RCS-tilviki með ytra fyrirtæki. Áður en hægt er að ljúka við þessar aðgerðir verður að ljúka við eftirfarandi skilyrði:

- Opna RCS-tilvik.
- Stofna veitanda virkrar skilgreiningar. Nánari upplýsingar er að finna í [Stofna skilgreiningarveitendur og merkja þá sem virka](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).
- Stofna og hlaða upp nýrri útgáfu af skilgreiningu rafrænnar skýrslugerðar. Frekari upplýsingar er að finna í [Stofna og hlaða upp nýrri útgáfu af skilgreiningu rafrænnar skýrslugerðar](rcs-global-repo-upload.md).

Einnig þarf að ganga úr skugga um að RCS-umhverfi sé úthlutað fyrir fyrirtækið.

1. Í forriti fjármála- og reksturs skal opna **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.
2. Ef engu RCS-umhverfi er úthlutað fyrir fyrirtækið skaltu velja **Regulatory Services – ytri skilgreining** og fylgja svo leiðbeiningunum til að úthluta einu slíku.

Ef RCS-umhverfi hefur þegar verið útvegað fyrir þitt fyrirtæki, notaðu slóðina á síðunni til að fá aðgang að því með því að velja innskráningarvalkostinn.

## <a name="verify-the-configuration-that-you-want-to-share"></a>Staðfestu skilgreininguna sem á að deila

Fylgið eftirfarandi skrefum til að staðfesta að skilgreiningunni sem á að nota hafi þegar verið hlaðið upp í altæku geymsluna.

1. Á vinnusvæðinu **Rafræn skýrslugerð** skal velja **Gagnaeymslur** fyrir skilgreiningarveitu.

    ![Skilgreiningaveitur.](media/1_RCS_Repo_for_config_provider.JPG)

2. Veldu **Altæk geymsla** \> **Opna**.
3. Leita að skilgreiningunni sem á að deila. Hægt er að nota síureitinn til að þrengja leitina. Ef ekki er hægt að finna skilgreininguna í altæku geymslunni skal fylgja skrefunum í [Stofna og hlaða upp nýrri útgáfu af skilgreiningu rafrænnar skýrslugerðar](rcs-global-repo-upload.md).

## <a name="share-er-configurations-with-external-organizations"></a>Deila skilgreiningum rafrænnar skýrslugerðar með utanaðkomandi fyrirtækjum

Eftir að skilgreining hefur verið stofnuð í skilgreiningarveitu er hægt að samnýta hana beint með ytri fyrirtækjum með því að nota flýtiflipann **Samnýtt með** á síðunni **Altæk skilgreiningargeymsla**.

1. Á vinnusvæðinu **Rafræn skýrslugerð** skal velja **Gagnaeymslur** fyrir skilgreiningarveitu.
2. Veldu **Altæk geymsla** \> **Opna**. 
3. Veldu skilgreininguna sem á að deila.
4. Í **Samnýtt með** flýtiflipanum, veldu **Fyrirtæki**.

    ![Flýtiflipinn Samnýtt með.](media/1_RCS_Repo_for_Share_with_org.JPG)

5. Í svarglugganum er fært inn lénsheiti ytra fyrirtækis og síðan valið **Í lagi**.

    ![Samnýta skilgreiningarútgáfu með svarglugga ytra fyrirtækis.](media/1_RCS_Repo_for_Share_with_form.JPG)

Skilgreiningunni er deilt með ytra fyrirtækinu og er aðgengileg fyrir það fyrirtæki í altæku geymslunni. Þaðan er hægt að flytja hana inn í tilvik fyrirtækisins í RCS eða í tilvik forrita fjármála- og reksturs.

6. Til að stöðva samnýtingu skilgreiningar sem áður hefur verið deilt með ytra fyrirtæki skal velja skilgreininguna og smella á **Stöðva samnýtingu** og velja síðan **Í lagi**


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
