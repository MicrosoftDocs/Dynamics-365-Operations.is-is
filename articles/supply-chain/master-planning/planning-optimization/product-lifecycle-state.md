---
title: Útiloka afurðir sem hafa tilteknar líftímastöður afurðar
description: Þetta efnisatriði útskýrir hvernig á að útiloka afurðir miðað við líftímastöðu þeirra þegar fínstilling skipulagningar er notuð.
author: ChristianRytt
manager: tfehr
ms.date: 11/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-11-13
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: a1e0c734db763ffa69e2d6540a07d5fa04c22ea1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5227819"
---
# <a name="exclude-products-that-have-specific-product-lifecycle-states"></a><span data-ttu-id="fe616-103">Útiloka afurðir sem hafa tilteknar líftímastöður afurðar</span><span class="sxs-lookup"><span data-stu-id="fe616-103">Exclude products that have specific product lifecycle states</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fe616-104">Útgefnar afurðir og útgefnar afurðarútgáfur innihalda svæðið **Líftímastaða afurðar**.</span><span class="sxs-lookup"><span data-stu-id="fe616-104">Released products and released product versions include a **Product lifecycle state** field.</span></span> <span data-ttu-id="fe616-105">Þessi svæði gera þér m.a. kleift að stjórna hvaða afurðir eru innifaldar við aðaláætlanagerð.</span><span class="sxs-lookup"><span data-stu-id="fe616-105">This field lets you control, among other things, which products are included during master planning.</span></span> <span data-ttu-id="fe616-106">Hægt er að bæta við, fjarlægja og breyta líftímastöðu eftir þörfum með því að opna **Afurðarupplýsingastjórnun \> Uppsetning \> Líftímastaða afurðar**.</span><span class="sxs-lookup"><span data-stu-id="fe616-106">You can add, remove, and edit lifecycle states as required by going to **Product information management \> Setup \> Product lifecycle state**.</span></span> <span data-ttu-id="fe616-107">Fyrir hverja líftímastöðu afurðar er valkosturinn **Er virk fyrir áætlunargerð** stilltur á *Já* ef taka skal með afurðir í slíkri stöðu með í aðaláætlanagerð.</span><span class="sxs-lookup"><span data-stu-id="fe616-107">For each product lifecycle state, set the **Is active for planning** option to *Yes* if products that have that state should be included during master planning.</span></span> <span data-ttu-id="fe616-108">Þegar valkosturinn er stilltur á *Nei* verða tengdar afurðir og vöruvíddasamsetningar útilokaðar úr öllum aðaláætlanagerðum og öllum útreikningum á uppskriftarstigi.</span><span class="sxs-lookup"><span data-stu-id="fe616-108">When the option is set to *No*, the associated products and variants will be excluded from all master planning and all calculations at the bill of materials (BOM) level.</span></span>

<span data-ttu-id="fe616-109">Útgefnar afurðir og vöruvíddasamsetningar þar sem svæðið **Líftímastaða afurðar** er hafður autt eru meðhöndlaðir eins og þeir séu með líftímastöðu afurðar þar sem valkosturinn **Er virk fyrir áætlunargerð** er stilltur á *Já*.</span><span class="sxs-lookup"><span data-stu-id="fe616-109">Released products and variants where the **Product lifecycle state** field is left blank are treated as though they have a product lifecycle state where the **Is active for planning** option is set to *Yes*.</span></span> <span data-ttu-id="fe616-110">Með öðrum orðum eru þær teknar með meðan á aðaláætlanagerð stendur.</span><span class="sxs-lookup"><span data-stu-id="fe616-110">In other words, they will be included during master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="fe616-111">Í því skyni að koma í veg fyrir of margar framboðspantanir er eindregið mælt með því að tengja allar úreltar útgefnar afurðir og vöruvíddasamsetningar við líftímastöðu afurðar þar sem valkosturinn **Er virk fyrir áætlunargerð** er stilltur á *Nei*.</span><span class="sxs-lookup"><span data-stu-id="fe616-111">To help avoid unnecessary supply suggestions, we strongly recommend that you associate all obsolete released products and variants with a product lifecycle state where the **Is active for planning** option is set to *No*.</span></span> <span data-ttu-id="fe616-112">Þessi aðferð er afar mikilvæg þegar unnið er með vöruvíddasamsetningar afurðarafbrigða sem eru ekki endurnýjanlegar, því slíkt aðstoðar við að koma í veg fyrir sóun.</span><span class="sxs-lookup"><span data-stu-id="fe616-112">This approach is especially important when you work with product configuration variants that aren't reusable, because it will help prevent waste.</span></span>

## <a name="related-resources"></a><span data-ttu-id="fe616-113">Tengd tilföng</span><span class="sxs-lookup"><span data-stu-id="fe616-113">Related resources</span></span>

<span data-ttu-id="fe616-114">Frekari upplýsingar um líftímastöður afurðar er að finna á [Yfirlit yfir líftímastöðu afurðar](../../pim/product-lifecycle.md).</span><span class="sxs-lookup"><span data-stu-id="fe616-114">For more information about product lifecycle states, see [Product lifecycle state overview](../../pim/product-lifecycle.md).</span></span>

<span data-ttu-id="fe616-115">Nánari ítarupplýsingar um hvernig á að nota lífferilsstöðu afurðar til að útiloka afurðir frá aðaláætlanagerð og útreikningum á BOM-stigi, spilaðu eða lesið verkefnaleiðbeiningarnar [Búðu til lífferilsstöðu afurðar til að útiloka afurðir frá aðaláætlanagerð](../../pim/tasks/exclude-products-master-planning.md).</span><span class="sxs-lookup"><span data-stu-id="fe616-115">For detailed information that includes steps for using product lifecycle states to exclude products from master planning and BOM-level calculations, see [Create a product lifecycle state to exclude products from Master planning](../../pim/tasks/exclude-products-master-planning.md).</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]