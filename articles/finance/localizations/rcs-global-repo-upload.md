---
title: Stofna skilgreiningar rafrænnar skýrslugerðar í RCS og hlaða þeim upp í altæka geymslu
description: Þetta efnisatriði útskýrir hvernig á að stofna rafræna skýrslugerð (ER) í Microsoft Regulatory Configuration Services (RCS) og hlaða henni upp í altæku geymsluna.
author: JaneA07
manager: AnnBe
ms.date: 05/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace, RCS
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 0e194a8b777f984412d81e315f92ab4bb8a3b0c9
ms.sourcegitcommit: 204cec8ca2a6c4474d21dbcd408e369131a47856
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/13/2020
ms.locfileid: "3371251"
---
# <a name="create-er-configurations-in-regulatory-configuration-services-rcs-and-upload-them-to-the-global-repository"></a>Stofna skilgreiningar rafrænnar skýrslugerðar í Regulatory Configuration Services (RCS) og hlaða þeim upp í altæka geymslu

[!include [banner](../includes/banner.md)]

Hægt er að nota Microsoft Regulatory Configuration Services (RCS) til að hanna skilgreiningar rafrænnar skýrslugerðar (ER) og birta þær þannig að hægt sé að nota þær í fyrirtækinu.

Eftirfarandi ferli útskýra hvernig notandi í hlutverki kerfisstjóra eða þróunaraðila rafrænnar skýrslugerðar getur stofnað afleidda útgáfu af skilgreiningu rafrænnar skýrslugerðar sem hefur verið grunnstillt í RCS-tilviki og hlaðið síðan upp afleiddri skilgreiningu í altæku geymsluna. 

Áður en hægt er að ljúka við þessar aðgerðir verður að ljúka við eftirfarandi skilyrði:

- Opna RCS-tilvik.
- Stofna veitanda virkrar skilgreiningar. Nánari upplýsingar er að finna í [Stofna skilgreiningarveitendur og merkja þá sem virka](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).

Einnig þarf að ganga úr skugga um að RCS-umhverfi sé úthlutað fyrir fyrirtækið.

1. Í Finance and Operations forriti skal opna **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.
2. Ef engu RCS-umhverfi er úthlutað fyrir fyrirtækið skaltu velja **Regulatory Services – ytri skilgreining** og fylgja svo leiðbeiningunum til að úthluta einu slíku.

Ef RCS-umhverfi hefur þegar verið útvegað fyrir þitt fyrirtæki, notaðu slóðina á síðunni til að fá aðgang að því með því að velja innskráningarvalkostinn.

## <a name="create-a-derived-version-of-a-configuration-in-rcs"></a>Búa til afleidda útgáfu af skilgreiningu í RCS

1. Á vinnusvæðinu **Rafræn skýrslugerð** skal ganga úr skugga um að notandi sé með virka skilgreiningarveitu fyrir fyrirtækið. 
2. Veldu **Skilgreiningar skýrslugerðar**.
3. Veldu skilgreininguna sem ætlunin er að fá nýja útgáfu úr. Hægt er að nota síureitinn fyrir ofan tréð til að þrengja leitina.
4. Veljið **Stofna skilgreiningu** \> **Leiða af nafni**.
5. Sláið inn heiti og lýsingu og veljið svo **Stofna skilgreiningu** til að búa til nýja afleidda útgáfu.
6. Velja skal nýlega afleidda skilgreiningu, bæta við lýsingu á útgáfunni og velja síðan **Í lagi**. Stöðu skilgreiningarinnar er breytt í **Lokið**.

![Nýjar skilgreiningarútgáfur í RCS](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/RCS_CompleteConfig.JPG)

> [!NOTE]
> Þegar stöðu skilgreiningarinnar er breytt gæti notandi fengið villuboð við villuleit sem tengjast tengdu forritunum. Til að slökkva á villuleit, á aðgerðasvæði á flipanum **Skilgreiningar**, skal velja **Færibreytur notanda** og stilla síðan **Sleppa villuprófun við stöðubreytingu skilgreiningarinnar og endurreikning grunns** valkostinn á **Já** 

## <a name="upload-a-configuration-to-the-global-repository"></a>Hlaða skilgreiningu upp í altæku geymsluna

Til að deila nýrri eða afleiddri skilgreiningu með fyrirtækinu er hægt að hlaða henni upp í altæku geymsluna.

1. Velja skal lokna útgáfu af skilgreiningunni og síðan velja **Hlaða upp í gagnageymslu**.
2. Veldu **Altækt (Microsoft)** valkostinn og veldu síðan **Hlaða upp**.

    ![Valkostir fyrir upphleðslu í gagnageymslu](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/RCS_Upload_to_GlobalRepo_options.JPG)

3. Í staðfestingarglugganum velurðu **Já**. 
4. Uppfæra skal lýsinguna á útgáfunni þar sem þess er krafist og velja **Í lagi**. 

Staða skilgreiningarinnar er uppfærð í **Deila** og grunnstillingunni er hlaðið upp í altæku geymsluna. Þaðan er hægt að vinna með hana á eftirfarandi hátt:

- Flytja hana inn í Dynamics 365-tilvik. Frekari upplýsingar er að finna í [(Rafræn skýrslugerð) Flytja inn skilgreiningar úr RCS](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md).
- Deilið með þriðja aðila eða ytra fyrirtæki, sjá [Grunnstillingar RCS-samnýttrar rafrænnar skýrslugerðar (ER) með ytri fyrirtækjum](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/rcs-global-share-configuration.md)

![Afleidd skilgreiningarútgáfa af Intrastat Contoso í altæku geymslunni](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/RCS_Config_upload_GlobalRepo.JPG)
