--- 
title: "Stofna veitanda skilgreiningar og merkja sem virkan fyrir rafræna skýrslugerð (ER)"
description: "Eftirfarandi skref útskýra hvernig notanda úthlutað á hlutverk Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stofnað skilgreiningarveitu fyrir rafræna skýrslugerð (ER)."
author: NickSelin
manager: AnnBe
ms.date: 10/18/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: bdb3a3857a7293828a7766b6988c123a43e0673c
ms.contentlocale: is-is
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-configuration-providand-mark-it-as-active-for-electronic-reporting-er"></a><span data-ttu-id="af853-103">Stofna veitanda skilgreiningar og merkja sem virkan fyrir rafræna skýrslugerð (ER)</span><span class="sxs-lookup"><span data-stu-id="af853-103">Create a configuration providand mark it as active for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="af853-104">Eftirfarandi skref útskýra hvernig notanda úthlutað á hlutverk Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stofnað skilgreiningarveitu fyrir rafræna skýrslugerð (ER).</span><span class="sxs-lookup"><span data-stu-id="af853-104">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can create a configuration provider for Electronic reporting (ER).</span></span> <span data-ttu-id="af853-105">Hverja skilgreiningu rafrænnar skýrslugerðar vísar til veitu sem höfund skilgreiningar.</span><span class="sxs-lookup"><span data-stu-id="af853-105">Each ER configuration will refer to the provider as the author of the configuration.</span></span> <span data-ttu-id="af853-106">Í þessu dæmi, verður að stofna skilgreiningu fyrir dæmi um fyrirtæki, Litware, Inc. Þessi skref má framkvæma í hvaða fyrirtæki sem er þar sem ER skilgreiningar eru samnýttar á milli fyrirtækja.</span><span class="sxs-lookup"><span data-stu-id="af853-106">In this example, you will create a configuration provider for sample company, Litware, Inc. These steps can be performed in any company as ER configuration providers are shared among all companies.</span></span>


## <a name="create-a-provider"></a><span data-ttu-id="af853-107">Búa til veitu</span><span class="sxs-lookup"><span data-stu-id="af853-107">Create a provider</span></span>
1. <span data-ttu-id="af853-108">Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="af853-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="af853-109">Smelltu á skilgreiningaveitur.</span><span class="sxs-lookup"><span data-stu-id="af853-109">Click Configuration providers.</span></span>
3. <span data-ttu-id="af853-110">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="af853-110">Click New.</span></span>
    * <span data-ttu-id="af853-111">Skrá veitu er einkvæmt hvað varðar heiti og vefslóð.</span><span class="sxs-lookup"><span data-stu-id="af853-111">A provider record has a unique name and URL.</span></span> <span data-ttu-id="af853-112">Athuga innihald þessarar síðu og sleppa þessu ferli ef færsla fyrir Litware, Inc. (http://www.litware.com) er þegar til staðar.</span><span class="sxs-lookup"><span data-stu-id="af853-112">Review the content of this page and skip this procedure if a record for Litware, Inc. (http://www.litware.com) already exists.</span></span>  
4. <span data-ttu-id="af853-113">Í svæðið Heiti, færðu inn 'Litware, Inc.'.</span><span class="sxs-lookup"><span data-stu-id="af853-113">In the Name field, type 'Litware, Inc.'.</span></span>
    * <span data-ttu-id="af853-114">Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="af853-114">Litware, Inc.</span></span>  
5. <span data-ttu-id="af853-115">Færðu inn 'http://www.litware.com' í svæði vefsetur.</span><span class="sxs-lookup"><span data-stu-id="af853-115">In the Internet address field, type 'http://www.litware.com'.</span></span>
    * <span data-ttu-id="af853-116">http://www.litware.com</span><span class="sxs-lookup"><span data-stu-id="af853-116">http://www.litware.com</span></span>  
6. <span data-ttu-id="af853-117">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="af853-117">Click Save.</span></span>
7. <span data-ttu-id="af853-118">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="af853-118">Close the page.</span></span>

## <a name="select-as-an-active-provider"></a><span data-ttu-id="af853-119">Veljið sem virka veitu</span><span class="sxs-lookup"><span data-stu-id="af853-119">Select as an active provider</span></span>
1. <span data-ttu-id="af853-120">Velja “Litware, Inc.” veitu</span><span class="sxs-lookup"><span data-stu-id="af853-120">Select the Litware, Inc. provider.</span></span>
2. <span data-ttu-id="af853-121">Smellt á Stilla sem virkt.</span><span class="sxs-lookup"><span data-stu-id="af853-121">Click Set active.</span></span>


