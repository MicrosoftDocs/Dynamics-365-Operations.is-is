---
title: Stofna skilgreiningar rafrænnar skýrslugerðar í RCS og hlaða þeim upp í altæka geymslu
description: Þessi grein útskýrir hvernig á að búa til rafræna skýrslugerð (ER) stillingar í Microsoft Regulatory Configuration Services (RCS) og hlaða henni upp í alþjóðlegu geymsluna.
author: JaneA07
ms.date: 01/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace, RCS
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 8cfbcfea3c6056d87eb600c9a2f9e0d1727c30ff
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8894744"
---
# <a name="create-er-configurations-in-regulatory-configuration-services-rcs-and-upload-them-to-the-global-repository"></a>Stofna skilgreiningar rafrænnar skýrslugerðar í Regulatory Configuration Services (RCS) og hlaða þeim upp í altæka geymslu

[!include [banner](../includes/banner.md)]

Hægt er að nota Microsoft Regulatory Configuration Services (RCS) til að hanna skilgreiningar rafrænnar skýrslugerðar (ER) og birta þær þannig að hægt sé að nota þær í fyrirtækinu.

Eftirfarandi ferli útskýra hvernig notandi í hlutverki kerfisstjóra eða þróunaraðila rafrænnar skýrslugerðar getur stofnað afleidda útgáfu af skilgreiningu rafrænnar skýrslugerðar sem hefur verið grunnstillt í RCS-tilviki og hlaðið síðan upp afleiddri skilgreiningu í altæku geymsluna. 

Áður en hægt er að ljúka við þessar aðgerðir verður að ljúka við eftirfarandi skilyrði:

- Hafa aðgang að RCS umhverfi fyrir fyrirtæki þitt.
- Búðu til virka stillingarveitu og gerðu hana virka. Nánari upplýsingar er að finna í [Stofna skilgreiningarveitendur og merkja þá sem virka](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).

Þú verður að ganga úr skugga um að RCS umhverfi sé útvegað fyrir fyrirtæki þitt. Ef þú ert ekki með RCS tilvik útvegað fyrir fyrirtæki þitt geturðu gert það með eftirfarandi skrefum:

1. Í Finance and Operations app, farðu til **Stjórn stofnunarinnar** \> **Vinnurými** \> **Rafræn skýrslugerð**.
2. Í **Tengdir tenglar / Ytri tenglar**, veldu **Eftirlitsþjónusta – Stillingar**, og fylgdu síðan leiðbeiningunum til **Skráðu þig** að ákvæði eitt.

Ef RCS umhverfi hefur þegar verið útvegað fyrir fyrirtæki þitt skaltu nota vefslóð síðunnar til að fá aðgang að því og velja **skráðu þig inn** valmöguleika.

## <a name="create-a-derived-version-of-a-configuration-in-rcs"></a>Búa til afleidda útgáfu af skilgreiningu í RCS

> [!NOTE]
> Ef þetta er í fyrsta skiptið sem þú notar RCS muntu ekki hafa neina uppsetningu tiltæka fyrir þig. Þú þarft að flytja inn stillingu úr alþjóðlegu geymslunni. Frekari upplýsingar er að finna í [Sækja skilgreiningar rafrænnar skýrslugerðar úr altækri geymslu skilgreiningarþjónustu](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md).

1. **Skráðu þig inn** til RCS og veldu **Rafræn skýrslugerð** vinnurými.
2. Staðfestu að þú sért með virka stillingaveitu fyrir fyrirtæki þitt sem er stillt á virk (sjá forsendur). 
3. Veldu **Skilgreiningar skýrslugerðar**.
4. Veldu skilgreininguna sem ætlunin er að fá nýja útgáfu úr. Hægt er að nota síureitinn fyrir ofan tréð til að þrengja leitina.
5. Veljið **Stofna skilgreiningu** \> **Leiða af nafni**.
6. Sláðu inn nafn og lýsingu og veldu síðan **Búðu til stillingar** til að búa til nýja afleidda útgáfu með stöðunni „Drög“.
7. Veldu nýafleidda stillinguna og gerðu frekari breytingar á stillingarsniðinu, ef þörf krefur. 
8. Eftir að breytingunum er lokið þarftu að stilla **Breyta stöðu** fyrir uppsetninguna til **Lokið** til að geta birt það í geymslunni. Veldu **Í lagi**.

![Ný skilgreiningarútgáfa í RCS.](media/RCS_CompleteConfig.JPG)

> [!NOTE]
> Þegar stöðu skilgreiningarinnar er breytt gæti notandi fengið villuboð við villuleit sem tengjast tengdu forritunum. Til að slökkva á villuleit, á aðgerðasvæði á flipanum **Skilgreiningar**, skal velja **Færibreytur notanda** og stilla síðan **Sleppa villuprófun við stöðubreytingu skilgreiningarinnar og endurreikning grunns** valkostinn á **Já** 

## <a name="upload-a-configuration-to-the-global-repository"></a>Hlaða skilgreiningu upp í altæku geymsluna

Til að deila nýrri eða afleiddri uppsetningu með fyrirtækinu þínu geturðu hlaðið henni upp í alþjóðlegu geymsluna með því að fylgja þessum skrefum:

1. Velja skal lokna útgáfu af skilgreiningunni og síðan velja **Hlaða upp í gagnageymslu**.
2. Veldu **Altækt (Microsoft)** valkostinn og veldu síðan **Hlaða upp**.

    ![Valkostir fyrir upphleðslu í gagnageymslu.](media/RCS_Upload_to_GlobalRepo_options.JPG)

3. Í staðfestingarglugganum velurðu **Já**. 
4. Uppfæra skal lýsinguna á útgáfunni þar sem þess er krafist og velja **Í lagi**. Þú getur líka valfrjálst hlaðið útgáfunni upp í tengt forrit eða í GIT geymslu.  

Staða stillingar er uppfærð í **Samnýtt**, og stillingunum er hlaðið upp í alþjóðlegu geymsluna. Drög að útgáfu af uppsetningunni sem þú hlóðst upp er einnig búið til og hægt er að nota það ef þörf er á síðari breytingum.

Eftir að uppsetningunni hefur verið hlaðið upp í Global repository geturðu unnið með hana þar á eftirfarandi hátt:

- Flytja hana inn í Dynamics 365-tilvik. Frekari upplýsingar er að finna í [(Rafræn skýrslugerð) Flytja inn skilgreiningar úr RCS](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md).
- Deilið með þriðja aðila eða ytra fyrirtæki, sjá [Grunnstillingar RCS-samnýttrar rafrænnar skýrslugerðar (ER) með ytri fyrirtækjum](rcs-global-repo-share-configuration.md)

    ![Afleidd Intrastat Contoso stillingarútgáfa í alþjóðlegu geymslunni.](media/RCS_Config_upload_GlobalRepo.JPG)

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
