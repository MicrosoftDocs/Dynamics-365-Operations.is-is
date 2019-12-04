---
title: Hlaða niður Grunnstillingar fyrir rafræna skýrslugerð úr Lifecycle Services
description: Þetta kennsluefni útskýrir hvernig á að hlaða niður forstillingum Rafrænnar skýrslugerðar (ER) úr Microsoft Dynamics Lifecycle Services (LCS).
author: NickSelin
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionImport, ERWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 49785835ee2da911d7b8d1360e1c42f850f1153f
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/06/2019
ms.locfileid: "2771494"
---
# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a>Niðurhal skilgreininga fyrir rafræna skýrslugerð af Lifecycle Services

[!include [banner](../includes/banner.md)]

Þetta kennsluefni útskýrir hvernig á að hlaða niður forstillingum Rafrænnar skýrslugerðar (ER) úr Microsoft Dynamics Lifecycle Services (LCS).

Þetta kennsluefni leiðbeinir þér við ferli til að sækja nýjustu útgáfu forstillinga Rafræna skýrslugerð (ER) úr Microsoft Dynamics Lifecycle Services (LCS).

1. Skráðu þig inn í forritið með því að nota eitt af eftirfarandi hlutverkum:

    - Þróunaraðili rafrænnar skýrslulausnar
    - Hagnýtur ráðgjafi vegna rafrænnar skýrslugerðar
    - Kerfisstjóri

2. Farðu í **Fyrirtækisstjórnun** &gt; **Rafræn skýrslugerð**.
3. Í **veitandi skilgreininga** hlutanum, veljið gluggareitinn **Microsoft**
4. Á **Microsoft** gluggareit, er smellt á **gagnasöfn**.

    [![update-er-from-lcs-for-ms-open-ms-repositories-list](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)

5. Á **gagnasöfn skilgreininga** síðu í hnitanetinu skal velja fyrirliggjandi gagnasafn af gerðinni **LCS** . Ef þessi gagnasafn birtist ekki í hnitanetinu skal fylgja þessum skrefum:

    1. Smelltu á **Bæta við** til að bæta við nýju gagnasafni.
    2. Veljið **LCS** sem gerð gagnasafns.
    3. Smellið á **Stofna gagnasafn**.
    4. Ef beðið er um það skal fylgja heimildarleiðbeiningunum.
    5. Færa skal inn heiti og lýsingu fyrir gagnasafn.
    6. Smellið á **í lagi** til að staðfesta nýja færslu gagnasafns.
    7. Í hnitanetinu, veljið nýtt gagnasafn af gerðinni **LCS** .

6. Smellið á **Opna** til að skoða lista yfir skilgreiningar rafrænnar skýrslugerðar (ER) fyrir valda gagnasafn.

    [![update-er-from-lcs-for-ms-make-lcs-repository](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)

7. Í skilgreiningatrénu í vinstri rúðunni er valið skilgreining ER sem þig vantar.
8. Á flýtiflipanum **Útgáfur** skal velja nauðsynlega útgáfu skilgreiningar rafrænnar skýrslugerðar.
9. Smellið á **Innflutning** til að sækja valda útgáfu úr LCS í núverandi tilviki.

    > [!NOTE]
    > Hnappurinn **Innflutningur** er ekki tiltækur fyrir útgáfur skilgreininga rafrænnar skýrslugerðar sem þegar eru til staðar í gildandi tilviki.

    [![update-er-from-lcs-for-ms-download-configuration](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)

> [!NOTE]
> Það fer eftir stillingum rafrænnar skýrslugerðar hvernig skilgreiningar eru villuleitaðar eftir að þær eru fluttar inn. Notandi gæti verið látinn vita um vandamál ósamræmi sem fundust. Leysa þarf úr vandamálunum áður en hægt er að nota innflutta útgáfu skilgreiningu. Nánari upplýsingar, sjá lista yfir tengdar greinum fyrir þetta efni.

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit yfir rafræna skýrslugerð (ER)](general-electronic-reporting.md)
