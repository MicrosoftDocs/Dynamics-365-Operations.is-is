---
title: Áætlanagerð og fjölsvæðiseiginleikinn
description: Aðalröðun tekur tillit til stillinga svæðis og vöruhúsabirgðavídda.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventLocation, InventSite
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2434
ms.assetid: 7f05c031-a446-4168-8cce-03a6305f5c4d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 10981e0fe201566c83fd28c792000865bc533cd3
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "317431"
---
# <a name="master-planning-and-multisite-functionality"></a><span data-ttu-id="3aacc-103">Áætlanagerð og fjölsvæðiseiginleikinn</span><span class="sxs-lookup"><span data-stu-id="3aacc-103">Master planning and multisite functionality</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3aacc-104">Aðalröðun tekur tillit til stillinga svæðis og vöruhúsabirgðavídda.</span><span class="sxs-lookup"><span data-stu-id="3aacc-104">Master planning takes the settings of the site and warehouse inventory dimensions into account.</span></span> 

<span data-ttu-id="3aacc-105">Svæðisvíddin er áskilin og hægt er að stilla vöruhúsavíddina til að vera áskilin.</span><span class="sxs-lookup"><span data-stu-id="3aacc-105">The site dimension is mandatory, and you can set the warehouse dimension to be mandatory.</span></span>

<span data-ttu-id="3aacc-106">Þegar vídd er skyldubundin verður að færa víddargildi í allar birgðafærslur.</span><span class="sxs-lookup"><span data-stu-id="3aacc-106">When a dimension is mandatory, a dimension value must be entered on all inventory transactions.</span></span> <span data-ttu-id="3aacc-107">Í aðaláætlanagerð eru svæði og vöruhús fyrir upphaflegu þörfina þar með þekkt.</span><span class="sxs-lookup"><span data-stu-id="3aacc-107">Therefore, during master planning, the site and the warehouse for the initial demand are known.</span></span> <span data-ttu-id="3aacc-108">Svæðisvídd er jafnframt stöðug, og svæðisgildi breytist þar af leiðandi ekki þegar neðra-stigs krafa er brotin niður.</span><span class="sxs-lookup"><span data-stu-id="3aacc-108">The site dimension is also consistent so that during the explosion of lower-level demand, the site value does not change.</span></span>

<span data-ttu-id="3aacc-109">Ef stilling á vöruhúsi er ekki skyldubundin þekkist það ekki í upphaflegu þörfinni.</span><span class="sxs-lookup"><span data-stu-id="3aacc-109">When the warehouse is not set to mandatory, it may not be known from the initial demand.</span></span> <span data-ttu-id="3aacc-110">Áætlunarforritið verður að ákvarða hvaða vöruhús á að nota, byggt á stillingum sem eru skilgreindar fyrir vöru, einstökum vöruhúsum og upplýsingum pöntunarlínu.</span><span class="sxs-lookup"><span data-stu-id="3aacc-110">The planning engine must determine which warehouse to use based on the settings that are defined for the item, individual warehouses, and the details of the order line.</span></span>

<span data-ttu-id="3aacc-111">Eftirfarandi efnisatriði lýsa því hvernig áætlunarforritið vinnur, þegar mismunandi stillingar eru skilgreindar til þess að ákvarða hvaða vöruhús verður notað.</span><span class="sxs-lookup"><span data-stu-id="3aacc-111">The following topics describe how the planning engine works, when different settings are defined, to determine the warehouse to use.</span></span>

[<span data-ttu-id="3aacc-112">Aðaláætlanagerð - trygging svæðis og vöruhúss, vöruhús lögbundið</span><span class="sxs-lookup"><span data-stu-id="3aacc-112">Master planning - site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="3aacc-113">Aðaláætlanagerð - trygging svæðis, vöruhús lögbundið</span><span class="sxs-lookup"><span data-stu-id="3aacc-113">Master planning - site coverage, warehouse mandatory</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="3aacc-114">Aðaláætlanagerð - trygging svæðis og vöruhúss, vöruhús ekki lögbundið</span><span class="sxs-lookup"><span data-stu-id="3aacc-114">Master planning - site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="3aacc-115">Aðaláætlanagerð- trygging svæðis,  vöruhús ekki lögbundið</span><span class="sxs-lookup"><span data-stu-id="3aacc-115">Master planning - site coverage, warehouse not mandatory</span></span>](master-plan-site-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="3aacc-116">Aðaláætlanagerð - Hvernig uppskriftaútgáfan er ákvörðuð</span><span class="sxs-lookup"><span data-stu-id="3aacc-116">Master planning - How the BOM version is determined</span></span>](master-plan-bom-version-determined.md)



