---
title: Stofna skilgreiningarveitendur og merkja þá sem virka
description: Eftirfarandi skref útskýra hvernig notanda úthlutað á hlutverk Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stofnað skilgreiningarveitu fyrir rafræna skýrslugerð (ER).
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERVendorTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a4b1cd7a02cdf4c650af50199f4425eb53cef0a8
ms.sourcegitcommit: 574d4dda83dcab94728a3d35fc53ee7e2b90feb0
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/22/2019
ms.locfileid: "1595396"
---
# <a name="create-configuration-providers-and-mark-them-as-active"></a><span data-ttu-id="23c63-103">Stofna skilgreiningarveitendur og merkja þá sem virka</span><span class="sxs-lookup"><span data-stu-id="23c63-103">Create configuration providers and mark them as active</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="23c63-104">Eftirfarandi skref útskýra hvernig notanda úthlutað á hlutverk Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stofnað skilgreiningarveitu fyrir rafræna skýrslugerð (ER).</span><span class="sxs-lookup"><span data-stu-id="23c63-104">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can create a configuration provider for Electronic reporting (ER).</span></span> <span data-ttu-id="23c63-105">Hverja skilgreiningu rafrænnar skýrslugerðar vísar til veitu sem höfund skilgreiningar.</span><span class="sxs-lookup"><span data-stu-id="23c63-105">Each ER configuration will refer to the provider as the author of the configuration.</span></span> <span data-ttu-id="23c63-106">Í þessu dæmi, verður að stofna skilgreiningu fyrir dæmi um fyrirtæki, Litware, Inc. Þessi skref má framkvæma í hvaða fyrirtæki sem er þar sem ER skilgreiningar eru samnýttar á milli fyrirtækja.</span><span class="sxs-lookup"><span data-stu-id="23c63-106">In this example, you will create a configuration provider for sample company, Litware, Inc. These steps can be performed in any company as ER configuration providers are shared among all companies.</span></span>


## <a name="create-a-provider"></a><span data-ttu-id="23c63-107">Búa til veitu</span><span class="sxs-lookup"><span data-stu-id="23c63-107">Create a provider</span></span>
1. <span data-ttu-id="23c63-108">Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="23c63-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="23c63-109">Smelltu á skilgreiningaveitur.</span><span class="sxs-lookup"><span data-stu-id="23c63-109">Click Configuration providers.</span></span>
3. <span data-ttu-id="23c63-110">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="23c63-110">Click New.</span></span>
    * <span data-ttu-id="23c63-111">Skrá veitu er einkvæmt hvað varðar heiti og vefslóð.</span><span class="sxs-lookup"><span data-stu-id="23c63-111">A provider record has a unique name and URL.</span></span> <span data-ttu-id="23c63-112">Yfirfarið innihald þessarar síðu og sleppið ferlinu ef færsla fyrir Litware, Inc. (https://www.litware.com) er þegar til.</span><span class="sxs-lookup"><span data-stu-id="23c63-112">Review the content of this page and skip this procedure if a record for Litware, Inc. (https://www.litware.com) already exists.</span></span>  
4. <span data-ttu-id="23c63-113">Í svæðið Heiti, færðu inn 'Litware, Inc.'.</span><span class="sxs-lookup"><span data-stu-id="23c63-113">In the Name field, type 'Litware, Inc.'.</span></span>
    * <span data-ttu-id="23c63-114">Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="23c63-114">Litware, Inc.</span></span>  
5. <span data-ttu-id="23c63-115">Í reitinn Veffang skal slá inn „https://www.litware.com“.</span><span class="sxs-lookup"><span data-stu-id="23c63-115">In the Internet address field, type 'https://www.litware.com'.</span></span>
    * https://www.litware.com  
6. <span data-ttu-id="23c63-116">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="23c63-116">Click Save.</span></span>
7. <span data-ttu-id="23c63-117">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="23c63-117">Close the page.</span></span>

## <a name="select-as-an-active-provider"></a><span data-ttu-id="23c63-118">Veljið sem virka veitu</span><span class="sxs-lookup"><span data-stu-id="23c63-118">Select as an active provider</span></span>
1. <span data-ttu-id="23c63-119">Velja “Litware, Inc.” veitu</span><span class="sxs-lookup"><span data-stu-id="23c63-119">Select the Litware, Inc. provider.</span></span>
2. <span data-ttu-id="23c63-120">Smellt á Stilla sem virkt.</span><span class="sxs-lookup"><span data-stu-id="23c63-120">Click Set active.</span></span>

