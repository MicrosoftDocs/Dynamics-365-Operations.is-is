---
title: Yfirlit yfir aðaláætlanir og virkni á mörgum svæðum
description: Aðalröðun tekur tillit til stillinga svæðis og vöruhúsabirgðavídda.
author: roxanadiaconu
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventLocation, InventSite
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2434
ms.assetid: 7f05c031-a446-4168-8cce-03a6305f5c4d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2adbac35d556314b3ec9916e2b7b2706ce3528c9
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4430569"
---
# <a name="master-planning-and-multisite-functionality-overview"></a><span data-ttu-id="bb524-103">Yfirlit yfir aðaláætlanir og virkni á mörgum svæðum</span><span class="sxs-lookup"><span data-stu-id="bb524-103">Master planning and multisite functionality overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bb524-104">Aðalröðun tekur tillit til stillinga svæðis og vöruhúsabirgðavídda.</span><span class="sxs-lookup"><span data-stu-id="bb524-104">Master planning takes the settings of the site and warehouse inventory dimensions into account.</span></span> 

<span data-ttu-id="bb524-105">Svæðisvíddin er áskilin og hægt er að stilla vöruhúsavíddina til að vera áskilin.</span><span class="sxs-lookup"><span data-stu-id="bb524-105">The site dimension is mandatory, and you can set the warehouse dimension to be mandatory.</span></span>

<span data-ttu-id="bb524-106">Þegar vídd er skyldubundin verður að færa víddargildi í allar birgðafærslur.</span><span class="sxs-lookup"><span data-stu-id="bb524-106">When a dimension is mandatory, a dimension value must be entered on all inventory transactions.</span></span> <span data-ttu-id="bb524-107">Í aðaláætlanagerð eru svæði og vöruhús fyrir upphaflegu þörfina þar með þekkt.</span><span class="sxs-lookup"><span data-stu-id="bb524-107">Therefore, during master planning, the site and the warehouse for the initial demand are known.</span></span> <span data-ttu-id="bb524-108">Svæðisvídd er jafnframt stöðug, og svæðisgildi breytist þar af leiðandi ekki þegar neðra-stigs krafa er brotin niður.</span><span class="sxs-lookup"><span data-stu-id="bb524-108">The site dimension is also consistent so that during the explosion of lower-level demand, the site value does not change.</span></span>

<span data-ttu-id="bb524-109">Ef stilling á vöruhúsi er ekki skyldubundin þekkist það ekki í upphaflegu þörfinni.</span><span class="sxs-lookup"><span data-stu-id="bb524-109">When the warehouse is not set to mandatory, it may not be known from the initial demand.</span></span> <span data-ttu-id="bb524-110">Áætlunarforritið verður að ákvarða hvaða vöruhús á að nota, byggt á stillingum sem eru skilgreindar fyrir vöru, einstökum vöruhúsum og upplýsingum pöntunarlínu.</span><span class="sxs-lookup"><span data-stu-id="bb524-110">The planning engine must determine which warehouse to use based on the settings that are defined for the item, individual warehouses, and the details of the order line.</span></span>

<span data-ttu-id="bb524-111">Eftirfarandi efnisatriði lýsa því hvernig áætlunarforritið vinnur, þegar mismunandi stillingar eru skilgreindar til þess að ákvarða hvaða vöruhús verður notað.</span><span class="sxs-lookup"><span data-stu-id="bb524-111">The following topics describe how the planning engine works, when different settings are defined, to determine the warehouse to use.</span></span>

[<span data-ttu-id="bb524-112">Aðaláætlanagerð fyrir þekju svæðis og vöruhúss, vöruhús áskilið</span><span class="sxs-lookup"><span data-stu-id="bb524-112">Master planning for site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="bb524-113">Aðaláætlanagerð fyrir þekju svæðis, vöruhús áskilið</span><span class="sxs-lookup"><span data-stu-id="bb524-113">Master planning for site coverage, mandatory warehouse</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="bb524-114">Aðaláætlanagerð fyrir þekju svæðis og vöruhúss, vöruhús ekki áskilið</span><span class="sxs-lookup"><span data-stu-id="bb524-114">Master planning for site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="bb524-115">Aðaláætlanagerð fyrir þekju svæðis, vöruhús ekki áskilið</span><span class="sxs-lookup"><span data-stu-id="bb524-115">Master planning for site coverage, warehouse not mandatory</span></span>](master-plan-site-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="bb524-116">Uppskriftarútgáfa ákvörðuð</span><span class="sxs-lookup"><span data-stu-id="bb524-116">Determine the BOM version</span></span>](master-plan-bom-version-determined.md)



