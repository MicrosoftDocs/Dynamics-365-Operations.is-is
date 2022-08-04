---
title: Flytja inn uppfærðar útgáfur skilgreininga rafrænnar skýrslugerðar
description: Þessi grein útskýrir hvernig á að flytja inn uppfærðar útgáfur af rafrænum skýrslum (ER) stillingum úr Alþjóðlegu geymslunni stillingarþjónustunnar.
author: NickSelin
ms.date: 06/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionImport, ERWorkspace, ERSolutionRepositoryTable
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 0dac106a592a6a70aae6b245bce74d21c98cad10
ms.sourcegitcommit: 3289478a05040910f356baf1995ce0523d347368
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 07/01/2022
ms.locfileid: "9108440"
---
# <a name="import-updated-versions-of-er-configurations"></a>Flytja inn uppfærðar útgáfur skilgreininga rafrænnar skýrslugerðar

[!include [banner](../includes/banner.md)]

[Geymslur](general-electronic-reporting.md#Repository) rafrænnar skýrslugerðar eru notaðar til að samnýta [Skilgreiningar rafrænnar skýrslugerðar](general-electronic-reporting.md#Configuration). Þú getur [flytja inn](download-electronic-reporting-configuration-lcs.md) ER stillingar frá mismunandi geymslum inn í dæmið þitt af Microsoft Dynamics 365 Fjármál. Þegar skilgreiningar rafrænnar skýrslugerðar eru fluttar inn, geta [skilgreiningarveitur](general-electronic-reporting.md#Provider) gefið út nýjar [útgáfur](general-electronic-reporting.md#component-versioning) af geymslum þannig að hægt sé að deila þeim.

Þessi grein útskýrir hvernig á að flytja inn uppfærðar útgáfur af ER stillingum úr alþjóðlegri geymslu stillingarþjónustunnar. Fyrir frekari upplýsingar, sjá [Microsoft Dynamics 365 Fjármál - eftirlitsþjónusta, stillingarþjónusta](/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration).

## <a name="review-the-available-updated-versions"></a>Yfirfara tiltækar uppfærðar útgáfur

1. Skráði ykkur inn í Fjármál með því að nota eitt af eftirfarandi hlutverkum:

    - Þróunaraðili rafrænnar skýrslulausnar
    - Hagnýtur ráðgjafi vegna rafrænnar skýrslugerðar
    - Kerfisstjóri

2. Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.
3. Á síðunni **Skilgreiningar þýðingar**, í hlutanum **Tengdir tenglar**, skal velja **Flytja inn uppfærslur fyrir skilgreiningarútgáfur**.

    ![Skilgreiningasíða staðfæringar.](./media/er-download-updated-versions-global-repo1.png)

4. Í svarglugganum **Flytja inn uppfærslur fyrir skilgreiningarútgáfur rafrænnar skýrslugerðar**, í reitnum **Keyrsluháttur** skal velja **Sýna aðeins uppfærslur sem eru í boði**. Veljið síðan **Í lagi**. 

    ![Reitur keyrsluháttar stilltur á Sýna aðeins uppfærslur sem eru í boði.](./media/er-download-updated-versions-global-repo2.png)

5. Farið yfir skilaboðin sem berast. Þessi skilaboð veita eftirfarandi upplýsingar um skilgreiningar rafrænnar skýrslugerðar í núverandi Fjármálatilviki og hvernig það er í samanburði við efnið í altæku geymslunni:

    - Heildarfjöldi skilgreininga rafrænnar skýrslugerðar
    - Skilgreiningar rafrænnar skýrslugerðar sem eru ekki til staðar í altæku geymslunni
    - Skilgreiningar rafrænnar skýrslugerðar þar sem nýjasta útgáfan er þegar í boði í núverandi Fjármálatilviki (Til að skoða heildarlistann yfir þessar skilgreiningar rafrænnar skýrslugerðar skal velja tengilinn **Upplýsingar um skilaboð**.)

        ![„Nýjustu útgáfur eftirfarandi skilgreininga hafa þegar verið fluttar inn“ skilaboðin og upplýsingar um skilaboð](./media/er-download-updated-versions-global-repo3.png)

    - Skilgreiningar rafrænnar skýrslugerðar þar sem nýjasta útgáfan er í boði í altæku geymslunni og hægt er að flytja inn í núverandi Fjármálatilvik (Til að skoða heildarlistann yfir þessar skilgreiningar rafrænnar skýrslugerðar skal velja tengilinn **Upplýsingar um skilaboð**.)

        ![„Uppfærslur í boði“ skilaboð og upplýsingar um skilaboð](./media/er-download-updated-versions-global-repo4.png)

## <a name="import-available-updated-versions"></a>Flytja inn uppfærðar útgáfur í boði

1. Skráði ykkur inn í Fjármál með því að nota eitt af eftirfarandi hlutverkum:

    - Þróunaraðili rafrænnar skýrslulausnar
    - Hagnýtur ráðgjafi vegna rafrænnar skýrslugerðar
    - Kerfisstjóri

2. Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.
3. Á síðunni **Skilgreiningar þýðingar**, í hlutanum **Tengdir tenglar**, skal velja **Flytja inn uppfærslur fyrir skilgreiningarútgáfur**.
4. Í svarglugganum **Flytja inn uppfærslur fyrir skilgreiningarútgáfur rafrænnar skýrslugerðar**, í reitnum **Keyrsluháttur**, skal velja **Flytja inn nýjustu uppfærslurnar** til að flytja inn nýjustu útgáfur skilgreininga rafrænnar skýrslugerðar úr altæku geymslunni og yfir í núverandi Fjármálatilvik.
5. Til að áætla runuvinnslu fyrir innflutninginn, í flýtiflipanum **Keyra í bakgrunni**, skal stilla valkostinn **Runuvinnsla** á **Já**. Ef ætlunin er að endurtaka innflutninginn reglulega skal skilgreina nauðsynlega endurtekningu.

    ![Reitur keyrsluháttar stilltur á Flytja inn nýjustu uppfærslur.](./media/er-download-updated-versions-global-repo5.png)

6. Veldu **Í lagi**.
7. Til að fá upplýsingar um það hvaða skilgreiningarútgáfur hafa verið fluttar inn skal fylgja einu af þessum skrefum:

    - Ef verið er að keyra innflutninginn gagnvirkt í stað þess að nota runuvinnslu, skal yfirfara skilaboðin sem eru móttekin.

        ![Skilaboð sem berast við gagnvirka innflutningskeyrslu.](./media/er-download-updated-versions-global-repo6.png)

    - Fylgdu þessum skrefum ef þú keyrir innflutninginn í runustillingu:

        1. Farið í **Almennt** \> **Fyrirspurnir** \> **Runuvinnslur** \> **Mínar runuvinnslur**.
        2. Finnið og veljið verkið **Flytja inn uppfærslur fyrir skilgreiningarútgáfur rafrænnar skýrslugerðar** og síðan, á aðgerðasvæðinu, í flipanum **Runuvinnsla**, skal velja **Runuvinnsluferill** til að skoða verkferilinn.
        3. Á síðunni **Runuvinnsluferill** skal velja **Kladdi**. Því næst, í skilaboðunum sem birtast, skal velja tengilinn **Upplýsingar um skilaboð** til að skoða verkkladdann.

        ![Verkkladdi.](./media/er-download-updated-versions-global-repo7.png)

> [!IMPORTANT]
> Ekki er mælt með því að áætla endurtekna runuvinnsla til að flytja inn uppfærðar útgáfur af skilgreiningum rafrænnar skýrslugerðar beint úr altæku geymslunni og yfir í vinnsluumhverfi, því að innfluttar útgáfur verður hægt að nota um leið. Þess í stað skal nota þessa nálgun til að setja upp útgáfur af skilgreiningum rafrænnar skýrslugerðar í sandkassaumhverfi. Hægt er að meta þær í sandkassaumhverfinu áður en þær eru virkjaðar í vinnsluumhverfi.

## <a name="additional-resources"></a>Frekari upplýsingar

- [Yfirlit yfir rafræna skýrslugerð](general-electronic-reporting.md)
- [Sækja skilgreiningar rafrænnar skýrslugerðar úr altækri geymslu skilgreiningarþjónustu](er-download-configurations-global-repo.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
