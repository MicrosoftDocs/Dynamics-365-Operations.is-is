---
title: Flytja inn uppfærðar útgáfur skilgreininga rafrænnar skýrslugerðar
description: Í þessu efnisatriði er útskýrt hvernig á að flytja inn uppfærðar útgáfur af Skilgreiningum rafrænnar skýrslugerðar úr altækri geymslu skilgreiningarþjónustu.
author: NickSelin
manager: AnnBe
ms.date: 06/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionImport, ERWorkspace, ERSolutionRepositoryTable
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 4f167a0209713b5bca0cefe0135abd46a149a515
ms.sourcegitcommit: 1e6a7b50596eaf9d965e0155f3f2c50f7f50747e
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/22/2020
ms.locfileid: "3498098"
---
# <a name="import-updated-versions-of-er-configurations"></a>Flytja inn uppfærðar útgáfur skilgreininga rafrænnar skýrslugerðar

[!include [banner](../includes/banner.md)]

[Geymslur](general-electronic-reporting.md#Repository) rafrænnar skýrslugerðar eru notaðar til að samnýta [Skilgreiningar rafrænnar skýrslugerðar](general-electronic-reporting.md#Configuration). Hægt er að [flytja inn](download-electronic-reporting-configuration-lcs.md) skilgreiningar rafrænnar skýrslugerðar úr öðrum geymslum og yfir í tilvikið þitt af Microsoft Dynamics 365 Finance. Þegar skilgreiningar rafrænnar skýrslugerðar eru fluttar inn, geta [skilgreiningarveitur](general-electronic-reporting.md#Provider) gefið út nýjar [útgáfur](general-electronic-reporting.md#component-versioning) af geymslum þannig að hægt sé að deila þeim.

Í þessu efnisatriði er útskýrt hvernig á að flytja inn uppfærðar útgáfur af Skilgreiningum rafrænnar skýrslugerðar úr altækri geymslu skilgreiningarþjónustu. Frekari upplýsingar er að finna í [Microsoft Dynamics 365 for Finance and Operations - Regulatory Services, Skilgreiningarþjónusta](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration).

## <a name="review-the-available-updated-versions"></a>Yfirfara tiltækar uppfærðar útgáfur

1. Skráði ykkur inn í Fjármál með því að nota eitt af eftirfarandi hlutverkum:

    - Þróunaraðili rafrænnar skýrslulausnar
    - Hagnýtur ráðgjafi vegna rafrænnar skýrslugerðar
    - Kerfisstjóri

2. Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.
3. Á síðunni **Skilgreiningar þýðingar**, í hlutanum **Tengdir tenglar**, skal velja **Flytja inn uppfærslur fyrir skilgreiningarútgáfur**.

    ![Skilgreiningasíða staðfæringar](./media/er-download-updated-versions-global-repo1.png)

4. Í svarglugganum **Flytja inn uppfærslur fyrir skilgreiningarútgáfur rafrænnar skýrslugerðar**, í reitnum **Keyrsluháttur** skal velja **Sýna aðeins uppfærslur sem eru í boði**. Veljið síðan **Í lagi**. 

    ![Reitur keyrsluháttar stilltur á Sýna aðeins uppfærslur sem eru í boði](./media/er-download-updated-versions-global-repo2.png)

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

    ![Reitur keyrsluháttar stilltur á Flytja inn nýjustu uppfærslur](./media/er-download-updated-versions-global-repo5.png)

6. Veljið **Í lagi**.
7. Til að fá upplýsingar um það hvaða skilgreiningarútgáfur hafa verið fluttar inn skal fylgja einu af þessum skrefum:

    - Ef verið er að keyra innflutninginn gagnvirkt í stað þess að nota runuvinnslu, skal yfirfara skilaboðin sem eru móttekin.

        ![Skilaboð sem berast við gagnvirka innflutningskeyrslu](./media/er-download-updated-versions-global-repo6.png)

    - Fylgdu þessum skrefum ef þú keyrir innflutninginn í runustillingu:

        1. Farið í **Almennt** \> **Fyrirspurnir** \> **Runuvinnslur** \> **Mínar runuvinnslur**.
        2. Finnið og veljið verkið **Flytja inn uppfærslur fyrir skilgreiningarútgáfur rafrænnar skýrslugerðar** og síðan, á aðgerðasvæðinu, í flipanum **Runuvinnsla**, skal velja **Runuvinnsluferill** til að skoða verkferilinn.
        3. Á síðunni **Runuvinnsluferill** skal velja **Kladdi**. Því næst, í skilaboðunum sem birtast, skal velja tengilinn **Upplýsingar um skilaboð** til að skoða verkkladdann.

        ![Verkkladdi](./media/er-download-updated-versions-global-repo7.png)

> [!IMPORTANT]
> Ekki er mælt með því að áætla endurtekna runuvinnsla til að flytja inn uppfærðar útgáfur af skilgreiningum rafrænnar skýrslugerðar beint úr altæku geymslunni og yfir í vinnsluumhverfi, því að innfluttar útgáfur verður hægt að nota um leið. Þess í stað skal nota þessa nálgun til að setja upp útgáfur af skilgreiningum rafrænnar skýrslugerðar í sandkassaumhverfi. Hægt er að meta þær í sandkassaumhverfinu áður en þær eru virkjaðar í vinnsluumhverfi.

## <a name="additional-resources"></a>Frekari upplýsingar

- [Yfirlit yfir rafræna skýrslugerð](general-electronic-reporting.md)
- [Sækja skilgreiningar rafrænnar skýrslugerðar úr altækri geymslu skilgreiningarþjónustu](er-download-configurations-global-repo.md)
