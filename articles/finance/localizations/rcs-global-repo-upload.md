---
title: Stofna skilgreiningar rafrænnar skýrslugerðar í RCS og hlaða þeim upp í altæka geymslu
description: Þessi grein útskýrir hvernig á að stofna rafræna skýrslugerð (ER) í Microsoft Regulatory Configuration Services (RCS) og hlaða henni upp í altæku geymsluna.
author: kfend
ms.date: 01/11/2021
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
ms.openlocfilehash: 21e6ab3a7066fda23f1f5672f6f74bc6bd1ff1f6
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282994"
---
# <a name="create-er-configurations-in-regulatory-configuration-services-rcs-and-upload-them-to-the-global-repository"></a>Stofna skilgreiningar rafrænnar skýrslugerðar í Regulatory Configuration Services (RCS) og hlaða þeim upp í altæka geymslu

[!include [banner](../includes/banner.md)]

Hægt er að nota Microsoft Regulatory Configuration Services (RCS) til að hanna skilgreiningar rafrænnar skýrslugerðar (ER) og birta þær þannig að hægt sé að nota þær í fyrirtækinu.

Eftirfarandi ferli útskýra hvernig notandi í hlutverki kerfisstjóra eða þróunaraðila rafrænnar skýrslugerðar getur stofnað afleidda útgáfu af skilgreiningu rafrænnar skýrslugerðar sem hefur verið grunnstillt í RCS-tilviki og hlaðið síðan upp afleiddri skilgreiningu í altæku geymsluna. 

Áður en hægt er að ljúka við þessar aðgerðir verður að ljúka við eftirfarandi skilyrði:

- Vertu með aðgang að RCS-umhverfi fyrir fyrirtækið þitt.
- Búðu til virka skilgreiningarveitu og gerðu hana virka. Nánari upplýsingar er að finna í [Stofna skilgreiningarveitendur og merkja þá sem virka](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).

Ganga þarf úr skugga um að RCS-umhverfi sé úthlutað fyrir fyrirtækið. Ef ekki er búið að úthluta RCS-tilviki fyrir fyrirtækið er hægt að gera slíkt í eftirfarandi skrefum:

1. Í forriti fjármála- og reksturs skal opna **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.
2. Í **Tengdir tenglar / Ytri tenglar** skal velja **Regulatory Services – skilgreining** og síðan fylgja leiðbeiningum um **Nýskráningu** til að úthluta slíku.

Ef RCS-umhverfi hefur þegar verið úthlutað fyrir fyrirtækið skaltu nota vefslóð síðunnar til að fá aðgang að því og velja aðgerðina **innskráning**.

## <a name="create-a-derived-version-of-a-configuration-in-rcs"></a>Búa til afleidda útgáfu af skilgreiningu í RCS

> [!NOTE]
> Ef þetta er í fyrsta skipti sem þú hefur notað RCS verður engin skilgreining í boði til að leiða úr. Þú þarft að flytja inn skilgreiningu úr altækri geymslu. Frekari upplýsingar er að finna í [Sækja skilgreiningar rafrænnar skýrslugerðar úr altækri geymslu skilgreiningarþjónustu](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md).

1. **Skráðu þig inn** í RCS og veldu vinnusvæðið **Rafræn skýrslugerð**.
2. Staðfestu að þú sért með virka skilgreiningarveitu fyrir fyrirtækið sem er stillt á virk (sjá skilyrði). 
3. Veldu **Skilgreiningar skýrslugerðar**.
4. Veldu skilgreininguna sem ætlunin er að fá nýja útgáfu úr. Hægt er að nota síureitinn fyrir ofan tréð til að þrengja leitina.
5. Veljið **Stofna skilgreiningu** \> **Leiða af nafni**.
6. Færðu inn heiti og lýsingu og veldu síðan **Stofna skilgreiningu** til að búa til nýja afleidda útgáfu með stöðuna „Drög“.
7. Veljið nýlega afleidda skilgreiningu og gerður frekari breytingar á skilgreiningarsniðinu ef þörf krefur. 
8. Eftir að breytingunum er lokið þarf að stilla **Breyta stöðu** fyrir skilgreininguna á **Lokið** til að geta gefið hana út í gagnageymsluna. Veldu **Í lagi**.

![Ný skilgreiningarútgáfa í RCS.](media/RCS_CompleteConfig.JPG)

> [!NOTE]
> Þegar stöðu skilgreiningarinnar er breytt gæti notandi fengið villuboð við villuleit sem tengjast tengdu forritunum. Til að slökkva á villuleit, á aðgerðasvæði á flipanum **Skilgreiningar**, skal velja **Færibreytur notanda** og stilla síðan **Sleppa villuprófun við stöðubreytingu skilgreiningarinnar og endurreikning grunns** valkostinn á **Já** 

## <a name="upload-a-configuration-to-the-global-repository"></a>Hlaða skilgreiningu upp í altæku geymsluna

Til að deila nýrri eða afleiddri skilgreiningu með fyrirtækinu er hægt að hlaða henni upp í altæku geymsluna með því að fylgja þessum skrefum:

1. Velja skal lokna útgáfu af skilgreiningunni og síðan velja **Hlaða upp í gagnageymslu**.
2. Veldu **Altækt (Microsoft)** valkostinn og veldu síðan **Hlaða upp**.

    ![Valkostir fyrir upphleðslu í gagnageymslu.](media/RCS_Upload_to_GlobalRepo_options.JPG)

3. Í staðfestingarglugganum velurðu **Já**. 
4. Uppfæra skal lýsinguna á útgáfunni þar sem þess er krafist og velja **Í lagi**. Þú getur einnig hlaðið upp útgáfunni í tengdu forriti eða GIT-geymslu.  

Staða skilgreiningarinnar er uppfærð í **Deilt** og skilgreiningunni er hlaðið upp í altæku geymsluna. Drög af skilgreiningunni sem hlaðið var upp eru einnig búin til og er hægt að nota ef frekari breytinga er þörf.

Eftir að skilgreiningin hefur verið hlaðið upp í altæku geymsluna er hægt að vinna með hana þar á eftirfarandi hátt:

- Flytja hana inn í Dynamics 365-tilvik. Frekari upplýsingar er að finna í [(Rafræn skýrslugerð) Flytja inn skilgreiningar úr RCS](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md).
- Deilið með þriðja aðila eða ytra fyrirtæki, sjá [Grunnstillingar RCS-samnýttrar rafrænnar skýrslugerðar (ER) með ytri fyrirtækjum](rcs-global-repo-share-configuration.md)

    ![Afleidd skilgreiningarútgáfa af Intrastat Contoso í altæku geymslunni.](media/RCS_Config_upload_GlobalRepo.JPG)

## <a name="delete-a-configuration-from-the-global-repository"></a>Eyða skilgreiningu úr altæku geymslunni
Ljúkið eftirfarandi skrefum til að eyða skilgreiningu sem fyrirtækið hefur búið til.

1. Á vinnusvæðinu **Rafræn skýrslugerð** skal ganga úr skugga um að skilgreiningarveitan sé **Virk**. Nánari upplýsingar er að finna í [Stofna skilgreiningarveitendur og merkja þá sem virka](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).
2. Á virkri skilgreiningarveitu skal velja **geymslu**.
3. Velja skal geymslugerðina **Altæk** og velja **Opna**.
4. Í flýtiflipanum **Sía** skal finna skilgreininguna sem á að eyða með því að nota virknina **Sía**.
5. Í flýtiflipanum **Útgáfa** skal velja útgáfu skilgreiningarinnar sem á að eyða og síðan velja **Eyða**:

    ![Eyða skilgreiningu úr altækri geymslu.](media/RCS_Delete_from_GlobalRepo.JPG)

6. Í staðfestingarglugganum velurðu **Já**.

    ![Eyða staðfestingarboðum um útgáfu skilgreiningar.](media/RCS_Delete_from_GlobalRepo_Msg.JPG)
 
Skilgreiningarútgáfunni er eytt og staðfestingarboð eru sýnd. 

> [!NOTE]
> Aðeins er hægt að eyða skilgreiningum af skilgreiningarveitunni sem stofnaði þær. Ef skilgreiningunni hefur verið deilt með öðru fyrirtæki verður að stöðva samnýtingu hennar áður en henni er eytt.
 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

