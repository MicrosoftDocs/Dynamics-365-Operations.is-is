---
title: Afbrigðareglur
description: Þessi grein veitir almennar upplýsingar um skilgreiningarreglur. Skilgreiningarreglur skilgreina tengsl milli þátta í uppskrift (BOM) fyrir vörur sem nota skilgreiningartækni byggða á víddum.
author: cvocph
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMConfigRule
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19761
ms.assetid: e4c6622d-1e2d-4a4d-8047-c553a25d4f87
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ac3515837df45b65121ebec72a32ac98d740796a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5221872"
---
# <a name="configuration-rules"></a><span data-ttu-id="1ab57-104">Afbrigðareglur</span><span class="sxs-lookup"><span data-stu-id="1ab57-104">Configuration rules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1ab57-105">Þessi grein veitir almennar upplýsingar um skilgreiningarreglur.</span><span class="sxs-lookup"><span data-stu-id="1ab57-105">This article provides general information about configuration rules.</span></span> <span data-ttu-id="1ab57-106">Skilgreiningarreglur skilgreina tengsl milli þátta í uppskrift (BOM) fyrir vörur sem nota skilgreiningartækni byggða á víddum.</span><span class="sxs-lookup"><span data-stu-id="1ab57-106">Configuration rules define relationships between items in a bill of materials (BOM) for products that use the dimension-based configuration technology.</span></span>

<span data-ttu-id="1ab57-107">Skilgreiningareglur eru tiltækar þegar skilgreiningarlíkön byggð á víddum eru skilgreind.</span><span class="sxs-lookup"><span data-stu-id="1ab57-107">Configuration rules are available when you define dimension-based configuration models.</span></span> <span data-ttu-id="1ab57-108">Skilgreiningarreglur eru notaðar til þess annað hvort að framfylgja eða koma í veg fyrir ákveðnar vörusamsetningar í uppskrift.</span><span class="sxs-lookup"><span data-stu-id="1ab57-108">Configuration rules are used to either enforce or prohibit specific item combinations in a bill of materials (BOM).</span></span> <span data-ttu-id="1ab57-109">Eftir að uppskrift hefur verið stofnuð og viðeigandi atriðum hefur verið úthlutað í viðeigandi skilgreiningarflokka, er hægt að skilgreina eina eða fleiri skilgreiningareglur.</span><span class="sxs-lookup"><span data-stu-id="1ab57-109">After a BOM has been created and the relevant items have been assigned to their respective configuration groups, one or more configuration rules can be defined.</span></span> <span data-ttu-id="1ab57-110">Ef tvö atriði tilheyra saman er virknitáknið **Velja** notað til að tryggja að þau verði tekin saman.</span><span class="sxs-lookup"><span data-stu-id="1ab57-110">If two items belong together, the **Select** operator is used to ensure inclusion.</span></span> <span data-ttu-id="1ab57-111">Ef tvö atriði útiloka hvort annað er virknitáknið **Afvelja** notað til að tryggja að þau verði ekki tekin saman.</span><span class="sxs-lookup"><span data-stu-id="1ab57-111">If two items are mutually exclusive, the **Deselect** operator is used to ensure exclusion.</span></span>  

<span data-ttu-id="1ab57-112">**Ábending:** Þessar upplýsingar gilda aðeins í afurðarsniðmáti sem notar skilgreiningartækni byggða á víddum.</span><span class="sxs-lookup"><span data-stu-id="1ab57-112">**Note:** This information applies only to product masters that use the dimension-based configuration technology.</span></span>  

<span data-ttu-id="1ab57-113">Síðari breytingar á skilgreiningarreglum hafa ekki áhrif á fyrirliggjandi skilgreiningar.</span><span class="sxs-lookup"><span data-stu-id="1ab57-113">Existing configurations aren't affected by subsequent changes to the configuration rules.</span></span> <span data-ttu-id="1ab57-114">Samt sem áður er mikilvægt að setja reglur áður en ný skilgreining er sett fram, og að athuga reglurnar°ef talið er að þeim gæti hafa verið breytt.</span><span class="sxs-lookup"><span data-stu-id="1ab57-114">However, it's important that you set the rules before you define a new configuration, and that you check the rules if you think they have been changed.</span></span>  

<span data-ttu-id="1ab57-115">**Ábending:** Fyrir aðferðina **Velja** eru afleiddi skilgreiningaflokkurinn, vörunúmer og skilgreining sjálfkrafa valin.</span><span class="sxs-lookup"><span data-stu-id="1ab57-115">**Note:** For the **Select** method, the derived configuration group, item number, and configuration are automatically selected.</span></span> <span data-ttu-id="1ab57-116">Fyrir aðferðina **Afvelja** er ekki hægt að velja afleidda skilgreiningaflokkinn, vörunúmer og skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="1ab57-116">For the **Deselect** method, the derived configuration group, item number, and configuration can't be selected.</span></span>

<a name="additional-resources"></a><span data-ttu-id="1ab57-117">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="1ab57-117">Additional resources</span></span>
--------

[<span data-ttu-id="1ab57-118">Yfirlit yfir afurðarafbrigði sem byggja á víddum</span><span class="sxs-lookup"><span data-stu-id="1ab57-118">Dimension-based product configuration overview</span></span>](dimension-based-product-configuration.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]