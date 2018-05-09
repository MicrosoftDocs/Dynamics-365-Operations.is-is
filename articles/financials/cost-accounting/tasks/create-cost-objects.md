--- 
title: "Stofna kostnaðarhluti  "
description: "Þetta ferli sýnir hvernig á að stofna kostnaðarhluti með því að flytja fjárhagsvídd kostnaðarstaðar í Dynamics 365 for Finance and Operations inn í kostnaðarbókhald í gegnum gagnatengi."
author: YuyuScheller
manager: AnnBe
ms.date: 10/25/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 2c76a26ea63d1fd44c20fbee271d2767b8ea68b1
ms.contentlocale: is-is
ms.lasthandoff: 05/08/2018

---
# <a name="create-cost-objects"></a><span data-ttu-id="73c6f-103">Stofna kostnaðarhluti  </span><span class="sxs-lookup"><span data-stu-id="73c6f-103">Create cost objects</span></span> 

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="73c6f-104">Þetta ferli sýnir hvernig á að stofna kostnaðarhluti með því að flytja fjárhagsvídd kostnaðarstaðar í Dynamics 365 for Finance and Operations inn í kostnaðarbókhald í gegnum gagnatengi.</span><span class="sxs-lookup"><span data-stu-id="73c6f-104">This procedure shows how to create cost objects by importing the Dynamics 365 for Finance and Operations cost center financial dimension into Cost accounting via a data connector.</span></span> <span data-ttu-id="73c6f-105">USMF sýnifyrirtækið var notað til að stofna þetta ferli.</span><span class="sxs-lookup"><span data-stu-id="73c6f-105">The USMF demo company was used to create this procedure.</span></span> <span data-ttu-id="73c6f-106">Þetta ferli er fyrir Kostnaðarbókhald eiginleika sem var bætt við í Dynamics 365 for Operations útgáfu 1611.</span><span class="sxs-lookup"><span data-stu-id="73c6f-106">This procedure is for a Cost accounting feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="create-new-cost-objects"></a><span data-ttu-id="73c6f-107">Stofna nýjar kostnaðarhluti</span><span class="sxs-lookup"><span data-stu-id="73c6f-107">Create new cost objects</span></span>
1. <span data-ttu-id="73c6f-108">Fara í kostnaðarbókhald > Víddir > víddir kostnaðarhlutar.</span><span class="sxs-lookup"><span data-stu-id="73c6f-108">Go to Cost accounting > Dimensions > Cost object dimensions.</span></span>
2. <span data-ttu-id="73c6f-109">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="73c6f-109">Click New.</span></span>
3. <span data-ttu-id="73c6f-110">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="73c6f-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="73c6f-111">Í reitinn gagnatengi fyrir víddarstök skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="73c6f-111">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="73c6f-112">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="73c6f-112">In the Description field, type a value.</span></span>
6. <span data-ttu-id="73c6f-113">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="73c6f-113">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="73c6f-114">Stilla gagnatengi</span><span class="sxs-lookup"><span data-stu-id="73c6f-114">Configure the data connector</span></span>
1. <span data-ttu-id="73c6f-115">Smelltu á Skilgreina víddarstakaveitu</span><span class="sxs-lookup"><span data-stu-id="73c6f-115">Click Configure dimension member provider.</span></span>
    * <span data-ttu-id="73c6f-116">Veljið CostCenter að flytja inn víddir CostCenter í kostnaðarbókhald.</span><span class="sxs-lookup"><span data-stu-id="73c6f-116">Select CostCenter to import the CostCenter dimension into Cost accounting.</span></span>  
2. <span data-ttu-id="73c6f-117">Í reitnum heiti víddar skal velja kostnaðarstað.</span><span class="sxs-lookup"><span data-stu-id="73c6f-117">In the Dimension name field, select Cost center.</span></span>
3. <span data-ttu-id="73c6f-118">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="73c6f-118">Click OK.</span></span>

## <a name="import-cost-centers"></a><span data-ttu-id="73c6f-119">Flytja inn kostnaðarstaði</span><span class="sxs-lookup"><span data-stu-id="73c6f-119">Import cost centers</span></span>
1. <span data-ttu-id="73c6f-120">Smelltu á Flytja inn víddarstök.</span><span class="sxs-lookup"><span data-stu-id="73c6f-120">Click Import dimension members.</span></span>
2. <span data-ttu-id="73c6f-121">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="73c6f-121">Click OK.</span></span>

## <a name="view-the-imported-cost-centers"></a><span data-ttu-id="73c6f-122">Skoða innflutta kostnaðarstaði</span><span class="sxs-lookup"><span data-stu-id="73c6f-122">View the imported cost centers</span></span>
1. <span data-ttu-id="73c6f-123">Smelltu á Skoða víddarstök.</span><span class="sxs-lookup"><span data-stu-id="73c6f-123">Click View dimension members.</span></span>


