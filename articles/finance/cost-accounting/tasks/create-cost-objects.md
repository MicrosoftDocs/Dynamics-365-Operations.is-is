---
title: Stofna kostnaðarhluti
description: Þessi verklýsing sýnir hvernig á að stofna kostnaðarhluti með því að flytja inn fjárhagsvídd kostnaðarstaðar inn í kostnaðarbókhald í gegnum gagnatengi.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension, CAMAXFinancialDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2616e5275f9f59b962d4e456684073aea2c654ea
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/30/2019
ms.locfileid: "2249679"
---
# <a name="create-cost-objects"></a><span data-ttu-id="03de0-103">Stofna kostnaðarhluti</span><span class="sxs-lookup"><span data-stu-id="03de0-103">Create cost objects</span></span> 

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="03de0-104">Þessi verklýsing sýnir hvernig á að stofna kostnaðarhluti með því að flytja inn fjárhagsvídd kostnaðarstaðar inn í kostnaðarbókhald í gegnum gagnatengi.</span><span class="sxs-lookup"><span data-stu-id="03de0-104">This procedure shows how to create cost objects by importing the cost center financial dimension into Cost accounting via a data connector.</span></span> <span data-ttu-id="03de0-105">USMF sýnifyrirtækið var notað til að stofna þetta ferli.</span><span class="sxs-lookup"><span data-stu-id="03de0-105">The USMF demo company was used to create this procedure.</span></span> 


## <a name="create-new-cost-objects"></a><span data-ttu-id="03de0-106">Stofna nýjar kostnaðarhluti</span><span class="sxs-lookup"><span data-stu-id="03de0-106">Create new cost objects</span></span>
1. <span data-ttu-id="03de0-107">Fara í kostnaðarbókhald > Víddir > víddir kostnaðarhlutar.</span><span class="sxs-lookup"><span data-stu-id="03de0-107">Go to Cost accounting > Dimensions > Cost object dimensions.</span></span>
2. <span data-ttu-id="03de0-108">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="03de0-108">Click New.</span></span>
3. <span data-ttu-id="03de0-109">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="03de0-109">In the Name field, type a value.</span></span>
4. <span data-ttu-id="03de0-110">Í reitinn gagnatengi fyrir víddarstök skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="03de0-110">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="03de0-111">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="03de0-111">In the Description field, type a value.</span></span>
6. <span data-ttu-id="03de0-112">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="03de0-112">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="03de0-113">Stilla gagnatengi</span><span class="sxs-lookup"><span data-stu-id="03de0-113">Configure the data connector</span></span>
1. <span data-ttu-id="03de0-114">Smelltu á Skilgreina víddarstakaveitu</span><span class="sxs-lookup"><span data-stu-id="03de0-114">Click Configure dimension member provider.</span></span>
    * <span data-ttu-id="03de0-115">Veljið CostCenter að flytja inn víddir CostCenter í kostnaðarbókhald.</span><span class="sxs-lookup"><span data-stu-id="03de0-115">Select CostCenter to import the CostCenter dimension into Cost accounting.</span></span>  
2. <span data-ttu-id="03de0-116">Í reitnum heiti víddar skal velja kostnaðarstað.</span><span class="sxs-lookup"><span data-stu-id="03de0-116">In the Dimension name field, select Cost center.</span></span>
3. <span data-ttu-id="03de0-117">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="03de0-117">Click OK.</span></span>

## <a name="import-cost-centers"></a><span data-ttu-id="03de0-118">Flytja inn kostnaðarstaði</span><span class="sxs-lookup"><span data-stu-id="03de0-118">Import cost centers</span></span>
1. <span data-ttu-id="03de0-119">Smelltu á Flytja inn víddarstök.</span><span class="sxs-lookup"><span data-stu-id="03de0-119">Click Import dimension members.</span></span>
2. <span data-ttu-id="03de0-120">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="03de0-120">Click OK.</span></span>

## <a name="view-the-imported-cost-centers"></a><span data-ttu-id="03de0-121">Skoða innflutta kostnaðarstaði</span><span class="sxs-lookup"><span data-stu-id="03de0-121">View the imported cost centers</span></span>
1. <span data-ttu-id="03de0-122">Smelltu á Skoða víddarstök.</span><span class="sxs-lookup"><span data-stu-id="03de0-122">Click View dimension members.</span></span>

