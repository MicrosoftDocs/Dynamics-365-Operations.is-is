--- 
title: "Stofna kostnaðarhluti  "
description: "Þetta ferli sýnir hvernig á að stofna kostnaðarhluti með því að flytja inn Dynamics 365 for Finance and Operations, Enterprise edition fjárhagsvídd kostnaðarstaðar inn í kostnaðarbókhald í gegnum gagnatengi."
author: ShylaThompson
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMDimension, CAMAXFinancialDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 52b5fe092048cd7efe7b0a697cd7061ee0f65103
ms.contentlocale: is-is
ms.lasthandoff: 09/11/2018

---
# <a name="create-cost-objects"></a><span data-ttu-id="420ce-103">Stofna kostnaðarhluti  </span><span class="sxs-lookup"><span data-stu-id="420ce-103">Create cost objects</span></span> 

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="420ce-104">Þetta ferli sýnir hvernig á að stofna kostnaðarhluti með því að flytja inn Dynamics 365 for Finance and Operations, Enterprise edition fjárhagsvídd kostnaðarstaðar inn í kostnaðarbókhald í gegnum gagnatengi.</span><span class="sxs-lookup"><span data-stu-id="420ce-104">This procedure shows how to create cost objects by importing the Dynamics 365 for Finance and Operations, Enterprise edition cost center financial dimension into Cost accounting via a data connector.</span></span> <span data-ttu-id="420ce-105">USMF sýnifyrirtækið var notað til að stofna þetta ferli.</span><span class="sxs-lookup"><span data-stu-id="420ce-105">The USMF demo company was used to create this procedure.</span></span> <span data-ttu-id="420ce-106">Þetta ferli er fyrir Kostnaðarbókhald eiginleika sem var bætt við í Dynamics 365 for Operations útgáfu 1611.</span><span class="sxs-lookup"><span data-stu-id="420ce-106">This procedure is for a Cost accounting feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="create-new-cost-objects"></a><span data-ttu-id="420ce-107">Stofna nýjar kostnaðarhluti</span><span class="sxs-lookup"><span data-stu-id="420ce-107">Create new cost objects</span></span>
1. <span data-ttu-id="420ce-108">Fara í kostnaðarbókhald > Víddir > víddir kostnaðarhlutar.</span><span class="sxs-lookup"><span data-stu-id="420ce-108">Go to Cost accounting > Dimensions > Cost object dimensions.</span></span>
2. <span data-ttu-id="420ce-109">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="420ce-109">Click New.</span></span>
3. <span data-ttu-id="420ce-110">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="420ce-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="420ce-111">Í reitinn gagnatengi fyrir víddarstök skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="420ce-111">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="420ce-112">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="420ce-112">In the Description field, type a value.</span></span>
6. <span data-ttu-id="420ce-113">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="420ce-113">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="420ce-114">Stilla gagnatengi</span><span class="sxs-lookup"><span data-stu-id="420ce-114">Configure the data connector</span></span>
1. <span data-ttu-id="420ce-115">Smelltu á Skilgreina víddarstakaveitu</span><span class="sxs-lookup"><span data-stu-id="420ce-115">Click Configure dimension member provider.</span></span>
    * <span data-ttu-id="420ce-116">Veljið CostCenter að flytja inn víddir CostCenter í kostnaðarbókhald.</span><span class="sxs-lookup"><span data-stu-id="420ce-116">Select CostCenter to import the CostCenter dimension into Cost accounting.</span></span>  
2. <span data-ttu-id="420ce-117">Í reitnum heiti víddar skal velja kostnaðarstað.</span><span class="sxs-lookup"><span data-stu-id="420ce-117">In the Dimension name field, select Cost center.</span></span>
3. <span data-ttu-id="420ce-118">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="420ce-118">Click OK.</span></span>

## <a name="import-cost-centers"></a><span data-ttu-id="420ce-119">Flytja inn kostnaðarstaði</span><span class="sxs-lookup"><span data-stu-id="420ce-119">Import cost centers</span></span>
1. <span data-ttu-id="420ce-120">Smelltu á Flytja inn víddarstök.</span><span class="sxs-lookup"><span data-stu-id="420ce-120">Click Import dimension members.</span></span>
2. <span data-ttu-id="420ce-121">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="420ce-121">Click OK.</span></span>

## <a name="view-the-imported-cost-centers"></a><span data-ttu-id="420ce-122">Skoða innflutta kostnaðarstaði</span><span class="sxs-lookup"><span data-stu-id="420ce-122">View the imported cost centers</span></span>
1. <span data-ttu-id="420ce-123">Smelltu á Skoða víddarstök.</span><span class="sxs-lookup"><span data-stu-id="420ce-123">Click View dimension members.</span></span>


