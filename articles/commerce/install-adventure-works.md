---
title: Setja upp Adventure Works-þemað
description: Þessi grein lýsir því hvernig á að setja upp Adventure Works þemað í Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 12/10/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 18c2612b8b6b4ed8195ff8e71d6e0495f7e80950
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8854898"
---
# <a name="install-the-adventure-works-theme"></a>Setja upp Adventure Works-þemað

[!include [banner](includes/banner.md)]

Þessi grein lýsir því hvernig á að setja upp Adventure Works þemað í Microsoft Dynamics 365 Commerce. 

> [!IMPORTANT]
> Þema Adventure Works og einingar eru í boði frá og með Dynamics 365 Commerce útgáfu 10.0.20. Það er í boði frá Microsoft AppSource.

## <a name="prerequisites"></a>Forkröfur

Áður en þema Adventure Works er sett upp verður þú að vera með Dynamics 365 Commerce umhverfi (Commerce-útgáfu 10.0.20 eða nýrri) sem inniheldur Retail Cloud Scale Unit (RCSU), hugbúnaðarþróunarpakka (SDK) á netinu fyrir Commerce og einingasafn Commerce. Fyrir upplýsingar um hvernig á að setja upp Commerce SDK og einingasafnið, sjá [Settu upp þróunarumhverfi](e-commerce-extensibility/setup-dev-environment.md). 

## <a name="installation-steps"></a>Uppsetningarskref

### <a name="install-the-adventure-works-theme-in-your-application"></a>Setja upp þema Adventure Works í forritinu

Þemapakki Adventure Works er í boði í straumnum **dynamics365-commerce** sem **@msdyn365-commerce-theme/adventureworks-theme-kit**. Þó að þemapakki Adventure Works sé hluti af því straumnum er hann undir öðru nafnabili. Þess vegna verður að fylgja þessum skrefum til að bæta við stýriskráarfærslum fyrir nafnabilið.

1. Uppfærðu skrána **.npmrc** þannig að hún innihaldi eftirfarandi stýriskráarfærslu (ef færslan er ekki þegar innifalin):

    `@msdyn365-commerce-theme:registry=https://pkgs.dev.azure.com/commerce-partner/Registry/_packaging/dynamics365-commerce/npm/registry/`

1. Uppfærðu skrána **.yarnrc** þannig að hún innihaldi eftirfarandi stýriskráarfærslu (ef færslan er ekki þegar innifalin):

    `"@msdyn365-commerce-theme:registry" "https://pkgs.dev.azure.com/commerce-partner/Registry/_packaging/dynamics365-commerce/npm/registry/"`  
    
Til að setja upp pakkann í þínu staðbundnu umhverfi skaltu keyra`yarn add THEME_PACKAGE@VERSION` skipun frá skipanalínunni, hvar **THEME_PACKAGE** er þemapakkinn (@msdyn365-commerce-theme/adventureworks-theme-kit) og **ÚTGÁFA** er útgáfunúmer einingarsafnsins sem verið er að nota. Það er mikilvægt að útgáfur þemapakkans og einingasafnsins passi saman. Til að finna rétta útgáfunúmer einingasafns til að nota skaltu opna package.json skrána og finna **byrjendapakki** gildi undir **ósjálfstæði** kafla. Í eftirfarandi dæmi notar package.json skráin útgáfu 9.32 af einingasafninu sem varpar til Dynamics 365 Commerce útgáfu 10.0.22 útgáfu.  

```json
"dependencies": {
    "@msdyn365-commerce-modules/starter-pack": "9.32",
}
```

Eftirfarandi dæmi sýnir hvernig á að keyra`yarn add` skipun til að bæta við útgáfu 9.32 af Adventure Works þemanu. Skipunin uppfærir sjálfkrafa package.json skrána þannig að hún innihaldi ósjálfstæði.

`yarn add @msdyn365-commerce-theme/adventureworks-theme-kit@9.32`

Fyrir frekari upplýsingar um uppfærslu á útgáfu einingasafns, sjá [SDK og mát bókasafn uppfærslur](e-commerce-extensibility/sdk-updates.md). 

> [!IMPORTANT]
> - Þemaútgáfan á að passa við útgáfu einingasafnsins til að tryggja að allir eiginleikar virki sem skyldi. 
> - Lágmarksútgáfa fyrir einingasafn Commerce og SDK á að vera 10.0.20 (9.31). 

### <a name="add-the-font-files-for-the-adventure-works-theme"></a>Bæta við leturgerðarskrám fyrir þema Adventure Works

Þegar þema Adventure Works hefur verið sett upp í forritinu þarf að bæta við nauðsynlegum leturgerðarskrám. Til að ljúka þessu skrefi skaltu afrita allar leturgerðarskrárnar úr **\node_modules@msdyn365-commerce-theme\adventureworks-theme-kit\src\modules\adventureworks\public\webfonts** yfir á opinbera slóð skráasafns í forriti samstarfsaðila: **\public\webfonts**.

### <a name="set-up-the-resources-for-the-adventure-works-theme"></a>Setja upp tilföng fyrir þema Adventure Works

Næsta skrefið er að uppfæra nauðsynlegt sjálfgefið tilfang fyrir þemað. Til að ljúka þessu skrefi skaltu afrita efnið úr global.json skránni undir **\node_modules@msdyn365-commerce-theme\adventureworks-theme-kit\src\modules\adventureworks\resources\modules** yfir í global.json skrá í forriti samstarfsaðila undir **\src\resources\modules**. Ef viðtökuskráasafnið **\src\resources** er ekki til, er hægt að afrita það í heild sinni úr upprunaskráasafninu **\node_modules@msdyn365-commerce-theme\adventureworks-theme-kit\src\modules\adventureworks** yfir í viðtökuskráasafnið **\src**.

### <a name="pull-updates-and-validate-the-theme"></a>Draga fram uppfærslur og villuleita þemað

Upplýsingar um hvernig á að draga fram nýjasta SDK, einingasafnið og aðrar tengdar uppfærslur er að finna í hlutanum „Draga fram uppfærslur“ í [Uppfærslur á SDK og einingasafni](e-commerce-extensibility/sdk-updates.md#pull-updates).

Eftir að nýjustu tengslunum er ýtt niður, er hægt að keyra skipunina **Upphaf þráðar** til að ræsa hnútaþjóninn í þróunarumhverfinu og prófa nýja þema Adventure Works. Skoðaðu forritið staðbundið með því að nota færibreytu fyrirspurnarstrengur `?theme=adventureworks` (til dæmis `https://localhost:4000/?theme=adventureworks`).

## <a name="additional-resources"></a>Frekari upplýsingar

[Þema Adventure Works](adventure-works-theme.md)

[Yfirlit einingasafns](starter-kit-overview.md)

[Uppfærslur á SDK og einingasafni](e-commerce-extensibility/sdk-updates.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
