---
title: Nota stillingar mælieiningar
description: Í efnisatriði er fjallað um stillingar mælieininga og útskýrt hvernig á að nota þær í Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: d1fba966434b80c9b64c1f4d9b6b87993d59c0bf
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022375"
---
# <a name="apply-unit-of-measure-settings"></a>Nota stillingar mælieiningar

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Í efnisatriði er fjallað um stillingar mælieininga og útskýrt hvernig á að nota þær í Microsoft Dynamics 365 Commerce.

Hægt er að selja vöru í mismunandi einingum, eins og „hver“, „par“ og „tugir“. Í Commerce Headquarters er hægt að skilgreina hverja mælieiningu fyrir sig fyrir vöru og sýna hana á svæði fyrir rafræn viðskipti. Ef söluaðili selur vöru bæði í stökum einingum og í tugum er hægt að sýna tiltækar mælieiningar ásamt öðrum vöruupplýsingum.

Í dæminu á eftirfarandi mynd hefur verið stillt á vöru í mælieiningu **ea** (hverjr) í Commerce Headquarters.

![Dæmi um vöru sem er stillt með mælieiningu í Commerce Headquarters](./media/Productunit-headquarters.PNG)

> [!NOTE]
> Stuðningur við að sækja og sýna mælieininguna er tiltækur frá og með Commerce útgáfu 10.0.19.

## <a name="unit-of-measure-settings"></a>Stillingar mælieiningar

Skjástillingar mælieininga eru skilgreindar í vefsmið Commerce á **Stillingar vefsvæðis \> Viðbætur \> Birta mælieiningu fyrir afurðir**. Þrjár stillingar eru studdar:

- **Ekki birta** – Þegar þessi stillingu er valin mun vefsvæði netverslunar ekki sýna mælieiningu vörunnar. Þessi hegðun er sjálfgefin hegðun.
- **Birta í kaupupplifun afurðar** – Þegar þessi stilling er valin er mælieiningin sýnd á síðum afurðaupplýsinga, körfu, greiðsluferlis, pöntunarferils og pöntunarupplýsinga.
- **Birta í afurðaflettingu og kaupupplifun** – Þegar þessi stilling er valin er mælieiningin sýnd á síðum kaupupplifunar fyrir afurð og einnig í flettingarupplifun afurðar. Mælieiningar eru sýndar í leitarniðurstöðum og vörusafnseiningum sem hluti af þessari hegðun.

> [!IMPORTANT]
> Skjástillingar mælieiningar er í boði frá og með Commerce útgáfu 10.0.19. Ef verið er að uppfæra úr eldri útgáfu af Commerce verður að uppfæra appsettings.json-skrána handvirkt. Leiðbeiningar er að finna í [Uppfærslur á SDK og einingasafni](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).

## <a name="modules-that-use-unit-of-measure-settings"></a>Einingar sem nota stillingar mælieiningar

Einingar sem nota mælieiningarstillingarnar eru kaupkassar, óskalisti, karfa, körfutákn, leitarniðurstöðuílát, vörusöfnun, greiðslu- og pöntunarupplýsingaeiningar.

Í dæminu á eftirfarandi mynd sýnir upplýsingar um afurð (PDP) mælieininguna (**ea**) fyrir vöru.

![Dæmi um vörusafnseiningu sem sýnir mælieininguna](./media/Productunit-PDP.png)

Í dæminu á eftirfarandi mynd sýnir vörusafnseining mælieininguna (**ea**) fyrir vöru.

![Dæmi um vörusafnseiningu sem sýnir mælieininguna](./media/Productunit-productcollection.png)

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit einingasafns](starter-kit-overview.md)

[Körfueining](add-cart-module.md)

[Kaupgluggaeining](add-buy-box.md)

[Síður og einingar fyrir stjórnun reikninga](account-management.md)

[Uppfærslur á SDK og einingasafni](e-commerce-extensibility/sdk-updates.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
