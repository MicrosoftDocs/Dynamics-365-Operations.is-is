---
title: Sækja skilgreiningar rafrænnar skýrslugerðar úr altækri geymslu skilgreiningarþjónustu
description: Í þessari grein er útskýrt hvernig á að sækja Skilgreiningar rafrænnar skýrslugerðar úr altækri geymslu skilgreiningarþjónustu.
author: kfend
ms.date: 06/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 10.0.5
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.form: ERSolutionImport, ERWorkspace, ERSolutionRepositoryTable
ms.openlocfilehash: 3bbc341d1668e54fcb4034263a7e142166a94b05
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273309"
---
# <a name="download-er-configurations-from-the-global-repository-of-configuration-service"></a>Sækja skilgreiningar rafrænnar skýrslugerðar úr altækri geymslu skilgreiningarþjónustu

[!include [banner](../includes/banner.md)]

Í þessari grein er útskýrt hvernig á að sækja [Skilgreiningar rafrænnar skýrslugerðar](general-electronic-reporting.md#Configuration) úr altækri geymslu skilgreiningarþjónustu. Frekari upplýsingar er að finna í [Microsoft Dynamics 365 Finance – Regulatory Services, Skilgreiningarþjónusta](/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration).

## <a name="open-configurations-repository"></a>Opna gagnageymslur skilgreininga

1. Skráðu þig inn í Dynamics 365 Finance-forritið með því að nota eitt af eftirfarandi hlutverkum:

    - Þróunaraðili rafrænnar skýrslulausnar
    - Hagnýtur ráðgjafi vegna rafrænnar skýrslugerðar
    - Kerfisstjóri

2. Fara í **Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð**.
3. Í **veitandi skilgreininga** hlutanum, veljið gluggareitinn **Microsoft**
3. Í reitnum **Microsoft** skal velja **Geymslur**.

    ![Vinnusvæði rafrænnar skýrslugerðar.](./media/er-download-configurations-global-repo-er-workspace.png)

4. Á síðunni **Gagnageymslur skilgreininga**, í hnitanetinu, skal velja fyrirliggjandi gagnageymslu af gerðinni **LCS**. Ef þessi gagnasafn birtist ekki í hnitanetinu skal fylgja þessum skrefum:

    1. Smellið á **Bæta við** til að bæta við nýrri gagnageymslu.
    2. Veljið **Altæk** sem gagngeymslugerð og veljið síðan **Búa til gagnageymslu**.
    3. Ef beðið er um það skal fylgja heimildarleiðbeiningunum.
    4. Sláið inn heiti og lýsingu fyrir gagnageymsluna og veljið síðan **Í lagi** til að staðfesta nýju gagnageymslufærsluna.
    5. Í hnitanetinu skal velja nýja gagnageymslu af gerðinni **Altæk**.

5. Smellið á **Opna** til að skoða lista yfir skilgreiningar rafrænnar skýrslugerðar fyrir valda gagnageymslu.

    ![Gagnageymslusíða skilgreininga.](./media/er-download-configurations-global-repo-repositories-list.png)

## <a name="import-a-single-configuration"></a>Flytja inn eina skilgreiningu

1. Á síðunni **Gagnageymslur skilgreininga**, í grunnstillingatrénu, skal velja skilgreiningu rafrænnar skýrslugerðar sem óskað er eftir.
2. Á flýtiflipanum **Útgáfur** skal velja nauðsynlega útgáfu skilgreiningar rafrænnar skýrslugerðar.
3. Veljið **Flytja inn** til að sækja valda útgáfu úr altækri geymslu í núverandi fjármálatilvik.

    > [!NOTE]
    > Hnappurinn **Flytja inn** er ekki tiltækur fyrir útgáfur skilgreininga rafrænnar skýrslugerðar sem þegar eru til staðar í núverandi fjármálatilviki.

    ![Gagnageymslusíða skilgreiningar, flýtiflipi grunnstillinga.](./media/er-download-configurations-global-repo-repository-content.png)

## <a name="import-filtered-configurations"></a>Flytja inn síaðar skilgreiningar

1. Á síðunni **Gagnageymslur skilgreininga**, í grunnstillingatrénu, skal stækka flýtiflipann **Sía**.
2. Í hnitanetinu **Merki** skal bæta við öllum nauðsynlegum merkjum.
3. Í reitnum **Land/svæði sem við á** skal velja viðeigandi lands-/svæðiskóði og síðan velja **Nota síu**.

    > [!NOTE]
    > Flýtiflipinn **Skilgreiningar** sýnir allar skilgreiningar sem uppfylla tilgreind skilyrði vals.

4. Í flýtiflipanum **Skilgreiningar** skal velja **Flytja inn** til að sækja síaðar skilgreiningar úr altæku geymslunni í núverandi tilvik.
5. Í flýtiflipanum **Skilgreiningar** skal velja **Endurstilla síu** til að hreinsa tilgreind skilyrði vals.

    ![Skilgreiningageymslusíða, flýtiflipi útgáfa, Flytja inn hnappur.](./media/er-download-configurations-global-repo-filtered-configurations.png)

> [!NOTE]
> Það fer eftir stillingum rafrænnar skýrslugerðar hvernig skilgreiningar eru villuleitaðar eftir að þær eru fluttar inn. Notandi gæti verið látinn vita um vandamál ósamræmi sem fundust. Áður en hægt er að nota innflutta útgáfu skilgreingar þarf að leysa úr vandamálunum. Frekari upplýsingar er að finna í lista yfir tengd tilföng í þessari grein.

> [!NOTE]
> Hægt er að stilla skilgreiningar rafrænnar skýrslugerðar sem háðar öðrum skilgreiningum. Þess vegna, ásamt valdri skilgreiningu, verða aðrar skilgreiningar hugsanlega fluttar inn sjálfkrafa. Meira um tengsl skilgreininga er að finna í [Skilgreina hversu mikil áhrif skilgreiningar rafrænnar skýrslugerðar hafa á aðra hluta](tasks/er-define-dependency-er-configurations-from-other-components-july-2017.md).

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit yfir rafræna skýrslugerð](general-electronic-reporting.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

