---
title: Bæta við táknmynd
description: Þetta efni útskýrir hvernig á að bæta við táknmynd á vefsíðuna.
author: bicyclingfool
manager: annbe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 18e12cbe46650fcf024a56b6de9a8cb2903d2bf8
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914576"
---
# <a name="add-a-favicon"></a>Bæta við táknmynd

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Þetta efni útskýrir hvernig á að bæta við táknmynd á vefsíðuna.

## <a name="overview"></a>Yfirlit

Táknmynd er lítil myndaskrá sem er sýnd á flipa vafra, á heimilisfangsstikunni, í vafraferlinum og meðal annars í bókamerkjum eða uppáhaldi. Við mælum með að þú bætir táknmynd við vefinn þinn vegna þess að það táknar og styrkir vörumerkið þitt og hjálpar til við að greina vefsíðuna frá öðrum síðum sem viðskiptavinir þínir heimsækja.

Þó að þú getir bætt við mörgum táknmyndum af ýmsum stærðum og skráartegundum á vefsíðuna, sýnir þetta efni hvernig á að bæta einni táknmynd við. Hins vegar er sama ferli og staðsetning notuð til að bæta fleiri táknmyndum við.

## <a name="upload-a-favicon-to-your-sites-asset-collection"></a>Hladdu upp táknmynd í eignasafn vefsvæðisins

Til að hlaða upp táknmynd í eignasafn vefsvæðisins skaltu fylgja þessum skrefum.

1. Farðu í **Eignir \> Hlaða upp \> Hlaða upp eignum**.
1. Finndu og veldu táknmyndina í skráarkerfinu.
1. Sláðu inn titil og veldu síðan **Í lagi**. 
1. Afritaðu opinberu vefslóð hugbúnaðarins í eiginleikaglugganum til hægri.

> [!NOTE]
> Ef þú velur ekki valkostinn **Birta eignir eftir upphleðslu** verður þú að fara til baka á síðuna **Eignir** og birta táknmyndina handvirkt síðar.

## <a name="create-the-html-for-the-favicon"></a>Búðu til HTML fyrir táknmyndina

Notaðu eftirfarandi HTML bút til að búa til HTML fyrir táknmyndina. Fyrir **href**-eigindið skaltu skipta út **"Public\_URL\_for\_your\_favicon"** fyrir opinberu slóðina sem þú afritaðir áður.

`<link rel="shortcut icon" href="Public_URL_for_your_favicon">`

## <a name="add-the-html-for-the-favicon-to-the-head-element-of-your-pages"></a>Bættu við HTML fyrir táknmyndina við \<höfuð\>-hluta af vefsíðunum

Til að bæta táknmyndinni við vefsvæðið notarðu sömu aðferð og er notuð til að bæta hvers konar HTML eða handriti við **\<höfuð\>**-hlutann af vefsíðunum.

## <a name="additional-resources"></a>Frekari upplýsingar

[Bæta við lógói](add-logo.md)

[Velja þema svæðis](select-site-theme.md)

[Unnið með CSS hnekkiskrám](css-override-files.md)

[Bæta við opnunarkveðju](add-welcome-message.md)

[Bæta við yfirlýsingu um höfundarrétt](add-copyright-notice.md)

[Bæta tungumálum við síðuna](add-languages-to-site.md)

[Bæta skriftarkóða við síður vefsvæðis til að aðstoða við fjarmælingar](add-telemetry.md)

