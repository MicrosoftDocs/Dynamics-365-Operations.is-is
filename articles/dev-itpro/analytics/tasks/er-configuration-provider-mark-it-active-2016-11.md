--- 
title: "Stofna veitanda skilgreiningar og merkja sem virkan fyrir rafræna skýrslugerð (ER)"
description: "Eftirfarandi skref útskýra hvernig notanda úthlutað á hlutverk Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stofnað skilgreiningarveitu fyrir rafræna skýrslugerð (ER)."
author: NickSelin
manager: AnnBe
ms.date: 11/01/2017
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 8392e789f546e32a00736c02eccf47d00893cc8b
ms.contentlocale: is-is
ms.lasthandoff: 05/08/2018

---
# <a name="create-a-configuration-provider-and-mark-it-as-active-for-electronic-reporting-er"></a><span data-ttu-id="8a1f6-103">Stofna veitanda skilgreiningar og merkja sem virkan fyrir rafræna skýrslugerð (ER)</span><span class="sxs-lookup"><span data-stu-id="8a1f6-103">Create a configuration provider and mark it as active for electronic reporting (ER)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8a1f6-104">Eftirfarandi skref útskýra hvernig notanda úthlutað á hlutverk Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stofnað skilgreiningarveitu fyrir rafræna skýrslugerð (ER).</span><span class="sxs-lookup"><span data-stu-id="8a1f6-104">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can create a configuration provider for Electronic reporting (ER).</span></span> <span data-ttu-id="8a1f6-105">Hverja skilgreiningu rafrænnar skýrslugerðar vísar til veitu sem höfund skilgreiningar.</span><span class="sxs-lookup"><span data-stu-id="8a1f6-105">Each ER configuration will refer to the provider as the author of the configuration.</span></span> <span data-ttu-id="8a1f6-106">Í þessu dæmi, verður að stofna skilgreiningu fyrir dæmi um fyrirtæki, Litware, Inc. Þessi skref má framkvæma í hvaða fyrirtæki sem er þar sem ER skilgreiningar eru samnýttar á milli fyrirtækja.</span><span class="sxs-lookup"><span data-stu-id="8a1f6-106">In this example, you will create a configuration provider for sample company, Litware, Inc. These steps can be performed in any company as ER configuration providers are shared among all companies.</span></span>


## <a name="create-a-provider"></a><span data-ttu-id="8a1f6-107">Búa til veitu</span><span class="sxs-lookup"><span data-stu-id="8a1f6-107">Create a provider</span></span>
1. <span data-ttu-id="8a1f6-108">Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="8a1f6-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="8a1f6-109">Smelltu á skilgreiningaveitur.</span><span class="sxs-lookup"><span data-stu-id="8a1f6-109">Click Configuration providers.</span></span>
3. <span data-ttu-id="8a1f6-110">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="8a1f6-110">Click New.</span></span>
    * <span data-ttu-id="8a1f6-111">Skrá veitu er einkvæmt hvað varðar heiti og vefslóð.</span><span class="sxs-lookup"><span data-stu-id="8a1f6-111">A provider record has a unique name and URL.</span></span> <span data-ttu-id="8a1f6-112">Yfirfarið innihald þessarar síðu og sleppið ferlinu ef færsla fyrir Litware, Inc. (`http://www.litware.com`) er þegar til.</span><span class="sxs-lookup"><span data-stu-id="8a1f6-112">Review the content of this page and skip this procedure if a record for Litware, Inc. (`http://www.litware.com`) already exists.</span></span>  
4. <span data-ttu-id="8a1f6-113">Í svæðið Heiti, færðu inn 'Litware, Inc.'.</span><span class="sxs-lookup"><span data-stu-id="8a1f6-113">In the Name field, type 'Litware, Inc.'.</span></span>
    * <span data-ttu-id="8a1f6-114">Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="8a1f6-114">Litware, Inc.</span></span>  
5. <span data-ttu-id="8a1f6-115">Færðu inn `http://www.litware.com` í svæði vefseturs.</span><span class="sxs-lookup"><span data-stu-id="8a1f6-115">In the Internet address field, type `http://www.litware.com`.</span></span>
6. <span data-ttu-id="8a1f6-116">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="8a1f6-116">Click Save.</span></span>
7. <span data-ttu-id="8a1f6-117">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="8a1f6-117">Close the page.</span></span>

## <a name="select-as-an-active-provider"></a><span data-ttu-id="8a1f6-118">Veljið sem virka veitu</span><span class="sxs-lookup"><span data-stu-id="8a1f6-118">Select as an active provider</span></span>
1. <span data-ttu-id="8a1f6-119">Velja “Litware, Inc.” veitu</span><span class="sxs-lookup"><span data-stu-id="8a1f6-119">Select the Litware, Inc. provider.</span></span>
2. <span data-ttu-id="8a1f6-120">Smellt á Stilla sem virkt.</span><span class="sxs-lookup"><span data-stu-id="8a1f6-120">Click Set active.</span></span>


