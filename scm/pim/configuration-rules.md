---
title: "Afbrigðareglur"
description: "Þessi grein veitir almennar upplýsingar um skilgreiningarreglur. Skilgreiningarreglur skilgreina tengsl milli þátta í uppskrift (BOM) fyrir vörur sem nota skilgreiningartækni byggða á víddum."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMConfigRule
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19761
ms.assetid: e4c6622d-1e2d-4a4d-8047-c553a25d4f87
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: bd5b5acd9ae223c78aa28c6e63c1a85cf64e9a26
ms.contentlocale: is-is
ms.lasthandoff: 07/18/2017

---

# <a name="configuration-rules"></a><span data-ttu-id="d8189-104">Afbrigðareglur</span><span class="sxs-lookup"><span data-stu-id="d8189-104">Configuration rules</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="d8189-105">Þessi grein veitir almennar upplýsingar um skilgreiningarreglur.</span><span class="sxs-lookup"><span data-stu-id="d8189-105">This article provides general information about configuration rules.</span></span> <span data-ttu-id="d8189-106">Skilgreiningarreglur skilgreina tengsl milli þátta í uppskrift (BOM) fyrir vörur sem nota skilgreiningartækni byggða á víddum.</span><span class="sxs-lookup"><span data-stu-id="d8189-106">Configuration rules define relationships between items in a bill of materials (BOM) for products that use the dimension-based configuration technology.</span></span>

<span data-ttu-id="d8189-107">Skilgreiningareglur eru tiltækar þegar skilgreiningarlíkön byggð á víddum eru skilgreind.</span><span class="sxs-lookup"><span data-stu-id="d8189-107">Configuration rules are available when you define dimension-based configuration models.</span></span> <span data-ttu-id="d8189-108">Skilgreiningarreglur eru notaðar til þess annað hvort að framfylgja eða koma í veg fyrir ákveðnar vörusamsetningar í uppskrift.</span><span class="sxs-lookup"><span data-stu-id="d8189-108">Configuration rules are used to either enforce or prohibit specific item combinations in a bill of materials (BOM).</span></span> <span data-ttu-id="d8189-109">Eftir að uppskrift hefur verið stofnuð og viðeigandi atriðum hefur verið úthlutað í viðeigandi skilgreiningarflokka, er hægt að skilgreina eina eða fleiri skilgreiningareglur.</span><span class="sxs-lookup"><span data-stu-id="d8189-109">After a BOM has been created and the relevant items have been assigned to their respective configuration groups, one or more configuration rules can be defined.</span></span> <span data-ttu-id="d8189-110">Ef tvö atriði tilheyra saman er virknitáknið **Velja** notað til að tryggja að þau verði tekin saman.</span><span class="sxs-lookup"><span data-stu-id="d8189-110">If two items belong together, the **Select** operator is used to ensure inclusion.</span></span> <span data-ttu-id="d8189-111">Ef tvö atriði útiloka hvort annað er virknitáknið **Afvelja** notað til að tryggja að þau verði ekki tekin saman.</span><span class="sxs-lookup"><span data-stu-id="d8189-111">If two items are mutually exclusive, the **Deselect** operator is used to ensure exclusion.</span></span>  

<span data-ttu-id="d8189-112">**Ábending:** Þessar upplýsingar gilda aðeins í afurðarsniðmáti sem notar skilgreiningartækni byggða á víddum.</span><span class="sxs-lookup"><span data-stu-id="d8189-112">**Note:** This information applies only to product masters that use the dimension-based configuration technology.</span></span>  

<span data-ttu-id="d8189-113">Síðari breytingar á skilgreiningarreglum hafa ekki áhrif á fyrirliggjandi skilgreiningar.</span><span class="sxs-lookup"><span data-stu-id="d8189-113">Existing configurations aren't affected by subsequent changes to the configuration rules.</span></span> <span data-ttu-id="d8189-114">Samt sem áður er mikilvægt að setja reglur áður en ný skilgreining er sett fram, og að athuga reglurnar°ef talið er að þeim gæti hafa verið breytt.</span><span class="sxs-lookup"><span data-stu-id="d8189-114">However, it's important that you set the rules before you define a new configuration, and that you check the rules if you think they have been changed.</span></span>  

<span data-ttu-id="d8189-115">**Ábending:** Fyrir aðferðina **Velja** eru afleiddi skilgreiningaflokkurinn, vörunúmer og skilgreining sjálfkrafa valin.</span><span class="sxs-lookup"><span data-stu-id="d8189-115">**Note:** For the **Select** method, the derived configuration group, item number, and configuration are automatically selected.</span></span> <span data-ttu-id="d8189-116">Fyrir aðferðina **Afvelja** er ekki hægt að velja afleidda skilgreiningaflokkinn, vörunúmer og skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="d8189-116">For the **Deselect** method, the derived configuration group, item number, and configuration can't be selected.</span></span>

<a name="see-also"></a><span data-ttu-id="d8189-117">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="d8189-117">See also</span></span>
--------

[<span data-ttu-id="d8189-118">Afurðarafbrigði byggt á vídd</span><span class="sxs-lookup"><span data-stu-id="d8189-118">Dimension-based product configuration</span></span>](dimension-based-product-configuration.md)




