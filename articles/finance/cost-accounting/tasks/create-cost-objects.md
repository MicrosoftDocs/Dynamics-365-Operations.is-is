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
ms.openlocfilehash: ed020348e50158362fda7b6b36dcdb17c48b4532
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142318"
---
# <a name="create-cost-objects"></a><span data-ttu-id="59456-103">Stofna kostnaðarhluti</span><span class="sxs-lookup"><span data-stu-id="59456-103">Create cost objects</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="59456-104">Þessi verklýsing sýnir hvernig á að stofna kostnaðarhluti með því að flytja inn fjárhagsvídd kostnaðarstaðar inn í kostnaðarbókhald í gegnum gagnatengi.</span><span class="sxs-lookup"><span data-stu-id="59456-104">This procedure shows how to create cost objects by importing the cost center financial dimension into Cost accounting via a data connector.</span></span> <span data-ttu-id="59456-105">USMF sýnifyrirtækið var notað til að stofna þetta ferli.</span><span class="sxs-lookup"><span data-stu-id="59456-105">The USMF demo company was used to create this procedure.</span></span> 


## <a name="create-new-cost-objects"></a><span data-ttu-id="59456-106">Stofna nýjar kostnaðarhluti</span><span class="sxs-lookup"><span data-stu-id="59456-106">Create new cost objects</span></span>
1. <span data-ttu-id="59456-107">Fara í kostnaðarbókhald > Víddir > víddir kostnaðarhlutar.</span><span class="sxs-lookup"><span data-stu-id="59456-107">Go to Cost accounting > Dimensions > Cost object dimensions.</span></span>
2. <span data-ttu-id="59456-108">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="59456-108">Click New.</span></span>
3. <span data-ttu-id="59456-109">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="59456-109">In the Name field, type a value.</span></span>
4. <span data-ttu-id="59456-110">Í reitinn gagnatengi fyrir víddarstök skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="59456-110">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="59456-111">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="59456-111">In the Description field, type a value.</span></span>
6. <span data-ttu-id="59456-112">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="59456-112">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="59456-113">Stilla gagnatengi</span><span class="sxs-lookup"><span data-stu-id="59456-113">Configure the data connector</span></span>
1. <span data-ttu-id="59456-114">Smelltu á Skilgreina víddarstakaveitu</span><span class="sxs-lookup"><span data-stu-id="59456-114">Click Configure dimension member provider.</span></span>
    * <span data-ttu-id="59456-115">Veljið CostCenter að flytja inn víddir CostCenter í kostnaðarbókhald.</span><span class="sxs-lookup"><span data-stu-id="59456-115">Select CostCenter to import the CostCenter dimension into Cost accounting.</span></span>  
2. <span data-ttu-id="59456-116">Í reitnum heiti víddar skal velja kostnaðarstað.</span><span class="sxs-lookup"><span data-stu-id="59456-116">In the Dimension name field, select Cost center.</span></span>
3. <span data-ttu-id="59456-117">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="59456-117">Click OK.</span></span>

## <a name="import-cost-centers"></a><span data-ttu-id="59456-118">Flytja inn kostnaðarstaði</span><span class="sxs-lookup"><span data-stu-id="59456-118">Import cost centers</span></span>
1. <span data-ttu-id="59456-119">Smelltu á Flytja inn víddarstök.</span><span class="sxs-lookup"><span data-stu-id="59456-119">Click Import dimension members.</span></span>
2. <span data-ttu-id="59456-120">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="59456-120">Click OK.</span></span>

## <a name="view-the-imported-cost-centers"></a><span data-ttu-id="59456-121">Skoða innflutta kostnaðarstaði</span><span class="sxs-lookup"><span data-stu-id="59456-121">View the imported cost centers</span></span>
1. <span data-ttu-id="59456-122">Smelltu á Skoða víddarstök.</span><span class="sxs-lookup"><span data-stu-id="59456-122">Click View dimension members.</span></span>

