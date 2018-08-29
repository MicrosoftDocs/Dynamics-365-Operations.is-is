--- 
title: "Stofna skilgreiningarveitendur og merkja þá sem virka"
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
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 37957f224cb57fd9f6c5014740bcea124a99a03a
ms.contentlocale: is-is
ms.lasthandoff: 08/09/2018

---
# <a name="create-configuration-providers-and-mark-them-as-active"></a><span data-ttu-id="1a65e-103">Stofna skilgreiningarveitendur og merkja þá sem virka</span><span class="sxs-lookup"><span data-stu-id="1a65e-103">Create configuration providers and mark them as active</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1a65e-104">Eftirfarandi skref útskýra hvernig notanda úthlutað á hlutverk Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stofnað skilgreiningarveitu fyrir rafræna skýrslugerð (ER).</span><span class="sxs-lookup"><span data-stu-id="1a65e-104">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can create a configuration provider for Electronic reporting (ER).</span></span> <span data-ttu-id="1a65e-105">Hverja skilgreiningu rafrænnar skýrslugerðar vísar til veitu sem höfund skilgreiningar.</span><span class="sxs-lookup"><span data-stu-id="1a65e-105">Each ER configuration will refer to the provider as the author of the configuration.</span></span> <span data-ttu-id="1a65e-106">Í þessu dæmi, verður að stofna skilgreiningu fyrir dæmi um fyrirtæki, Litware, Inc. Þessi skref má framkvæma í hvaða fyrirtæki sem er þar sem ER skilgreiningar eru samnýttar á milli fyrirtækja.</span><span class="sxs-lookup"><span data-stu-id="1a65e-106">In this example, you will create a configuration provider for sample company, Litware, Inc. These steps can be performed in any company as ER configuration providers are shared among all companies.</span></span>


## <a name="create-a-provider"></a><span data-ttu-id="1a65e-107">Búa til veitu</span><span class="sxs-lookup"><span data-stu-id="1a65e-107">Create a provider</span></span>
1. <span data-ttu-id="1a65e-108">Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="1a65e-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="1a65e-109">Smelltu á skilgreiningaveitur.</span><span class="sxs-lookup"><span data-stu-id="1a65e-109">Click Configuration providers.</span></span>
3. <span data-ttu-id="1a65e-110">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="1a65e-110">Click New.</span></span>
    * <span data-ttu-id="1a65e-111">Skrá veitu er einkvæmt hvað varðar heiti og vefslóð.</span><span class="sxs-lookup"><span data-stu-id="1a65e-111">A provider record has a unique name and URL.</span></span> <span data-ttu-id="1a65e-112">Yfirfarið innihald þessarar síðu og sleppið ferlinu ef færsla fyrir Litware, Inc. (`http://www.litware.com`) er þegar til.</span><span class="sxs-lookup"><span data-stu-id="1a65e-112">Review the content of this page and skip this procedure if a record for Litware, Inc. (`http://www.litware.com`) already exists.</span></span>  
4. <span data-ttu-id="1a65e-113">Í svæðið Heiti, færðu inn 'Litware, Inc.'.</span><span class="sxs-lookup"><span data-stu-id="1a65e-113">In the Name field, type 'Litware, Inc.'.</span></span>
    * <span data-ttu-id="1a65e-114">Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="1a65e-114">Litware, Inc.</span></span>  
5. <span data-ttu-id="1a65e-115">Færðu inn `http://www.litware.com` í svæði vefseturs.</span><span class="sxs-lookup"><span data-stu-id="1a65e-115">In the Internet address field, type `http://www.litware.com`.</span></span>
6. <span data-ttu-id="1a65e-116">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="1a65e-116">Click Save.</span></span>
7. <span data-ttu-id="1a65e-117">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="1a65e-117">Close the page.</span></span>

## <a name="select-as-an-active-provider"></a><span data-ttu-id="1a65e-118">Veljið sem virka veitu</span><span class="sxs-lookup"><span data-stu-id="1a65e-118">Select as an active provider</span></span>
1. <span data-ttu-id="1a65e-119">Velja “Litware, Inc.” veitu</span><span class="sxs-lookup"><span data-stu-id="1a65e-119">Select the Litware, Inc. provider.</span></span>
2. <span data-ttu-id="1a65e-120">Smellt á Stilla sem virkt.</span><span class="sxs-lookup"><span data-stu-id="1a65e-120">Click Set active.</span></span>


