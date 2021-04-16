---
title: Hlaða niður Grunnstillingar fyrir rafræna skýrslugerð úr Lifecycle Services
description: Þetta kennsluefni útskýrir hvernig á að hlaða niður forstillingum Rafrænnar skýrslugerðar (ER) úr Microsoft Dynamics Lifecycle Services (LCS).
author: NickSelin
ms.date: 08/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionImport, ERWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 418586113c038c3227f0704495a561eac319bdc9
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745088"
---
# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a>Niðurhal skilgreininga fyrir rafræna skýrslugerð af Lifecycle Services

[!include [banner](../includes/banner.md)]

Þetta kennsluefni útskýrir hvernig á að hlaða niður nýjustu útgáfu [Rafrænnar skýrslugerðar (ER)](general-electronic-reporting.md#Configuration) úr [Samnýtt eignasafn](../lifecycle-services/asset-library.md) í Microsoft Dynamics Lifecycle Services (LCS).

1. Skráðu þig inn í forritið með því að nota eitt af eftirfarandi hlutverkum:

    - Þróunaraðili rafrænnar skýrslulausnar
    - Hagnýtur ráðgjafi vegna rafrænnar skýrslugerðar
    - Kerfisstjóri

2. Farðu í **Fyrirtækisstjórnun** &gt; **Vinnusvæði** &gt; **Rafræn skýrslugerð**.
3. Í **veitandi skilgreininga** hlutanum, veljið gluggareitinn **Microsoft**
4. Í reitnum **Microsoft** skal velja **Geymslur**.

    [![Microsoft reitur á Skilgreiningasíðu staðfæringar](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)

5. Á **gagnasöfn skilgreininga** síðu í hnitanetinu skal velja fyrirliggjandi gagnasafn af gerðinni **LCS** . Ef þessi gagnasafn birtist ekki í hnitanetinu skal fylgja þessum skrefum:

    1. Smellið á **Bæta við** til að bæta við geymslu.
    2. Veljið **LCS** sem gerð gagnasafns.
    3. Veljið **Stofna geymslu**.
    4. Ef þú ert beðinn um heimild skaltu fylgja leiðbeiningunum á skjánum.
    5. Færa skal inn heiti og lýsingu fyrir gagnasafn.
    6. Veldu **Í lagi** til að staðfesta nýja færslu gagnasafns.
    7. Í hnitanetinu, veljið nýtt gagnasafn af gerðinni **LCS** .

6. Smellið á **Opna** til að skoða lista yfir skilgreiningar rafrænnar skýrslugerðar fyrir valda gagnageymslu.

    [![Gagnageymslusíða skilgreininga](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)

    > [!TIP]
    > Ef þú í vandræðum með að nota LCS-geymsluna til að sækja skilgreiningar úr samnýttu eignasafni í LCS er hægt að sækja grunnstillingar úr [Altæk geymsla](er-download-configurations-global-repo.md) í staðinn.

7. Í skilgreiningatrénu í vinstri rúðunni er nauðsynleg ER skilgreining valin.
8. Á flýtiflipanum **Útgáfur** skal velja nauðsynlega útgáfu skilgreiningar rafrænnar skýrslugerðar.
9. Veljið **Flytja inn** til að sækja valda útgáfu úr LCS í núverandi tilvik.

    > [!NOTE]
    > Hnappurinn **Innflutningur** er ekki tiltækur fyrir útgáfur skilgreininga rafrænnar skýrslugerðar sem þegar eru til staðar í gildandi tilviki.

    [![Síðan Skilgreiningagagnasafn](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)

> [!NOTE]
> Það fer eftir stillingum rafrænnar skýrslugerðar hvernig skilgreiningar eru villuleitaðar eftir að þær eru fluttar inn. Notandi gæti verið látinn vita um vandamál ósamræmi sem fundust. Leysa þarf úr vandamálunum áður en hægt er að nota innflutta útgáfu skilgreiningu. Frekari upplýsingar er að finna í lista yfir tengd efnisatriði fyrir þetta efnisatriði.

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit yfir rafræna skýrslugerð](general-electronic-reporting.md)

[Sækja skilgreiningar rafrænnar skýrslugerðar úr altækri geymslu skilgreiningarþjónustu](er-download-configurations-global-repo.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]