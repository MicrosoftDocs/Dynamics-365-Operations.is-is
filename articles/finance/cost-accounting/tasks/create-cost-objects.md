---
title: Stofna kostnaðarhluti
description: Þessi verklýsing sýnir hvernig á að stofna kostnaðarhluti með því að flytja inn fjárhagsvídd kostnaðarstaðar inn í kostnaðarbókhald í gegnum gagnatengi.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CAMDimension, CAMAXFinancialDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1219cb15ecec7c156579c5cf7c3a3511a141e00b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810055"
---
# <a name="create-cost-objects"></a><span data-ttu-id="52440-103">Stofna kostnaðarhluti</span><span class="sxs-lookup"><span data-stu-id="52440-103">Create cost objects</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="52440-104">Þessi verklýsing sýnir hvernig á að stofna kostnaðarhluti með því að flytja inn fjárhagsvídd kostnaðarstaðar inn í kostnaðarbókhald í gegnum gagnatengi.</span><span class="sxs-lookup"><span data-stu-id="52440-104">This procedure shows how to create cost objects by importing the cost center financial dimension into Cost accounting via a data connector.</span></span> <span data-ttu-id="52440-105">USMF sýnifyrirtækið var notað til að stofna þetta ferli.</span><span class="sxs-lookup"><span data-stu-id="52440-105">The USMF demo company was used to create this procedure.</span></span> 


## <a name="create-new-cost-objects"></a><span data-ttu-id="52440-106">Stofna nýjar kostnaðarhluti</span><span class="sxs-lookup"><span data-stu-id="52440-106">Create new cost objects</span></span>
1. <span data-ttu-id="52440-107">Fara í kostnaðarbókhald > Víddir > víddir kostnaðarhlutar.</span><span class="sxs-lookup"><span data-stu-id="52440-107">Go to Cost accounting > Dimensions > Cost object dimensions.</span></span>
2. <span data-ttu-id="52440-108">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="52440-108">Click New.</span></span>
3. <span data-ttu-id="52440-109">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="52440-109">In the Name field, type a value.</span></span>
4. <span data-ttu-id="52440-110">Í reitinn gagnatengi fyrir víddarstök skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="52440-110">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="52440-111">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="52440-111">In the Description field, type a value.</span></span>
6. <span data-ttu-id="52440-112">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="52440-112">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="52440-113">Stilla gagnatengi</span><span class="sxs-lookup"><span data-stu-id="52440-113">Configure the data connector</span></span>
1. <span data-ttu-id="52440-114">Smelltu á Skilgreina víddarstakaveitu</span><span class="sxs-lookup"><span data-stu-id="52440-114">Click Configure dimension member provider.</span></span>
    * <span data-ttu-id="52440-115">Veljið CostCenter að flytja inn víddir CostCenter í kostnaðarbókhald.</span><span class="sxs-lookup"><span data-stu-id="52440-115">Select CostCenter to import the CostCenter dimension into Cost accounting.</span></span>  
2. <span data-ttu-id="52440-116">Í reitnum heiti víddar skal velja kostnaðarstað.</span><span class="sxs-lookup"><span data-stu-id="52440-116">In the Dimension name field, select Cost center.</span></span>
3. <span data-ttu-id="52440-117">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="52440-117">Click OK.</span></span>

## <a name="import-cost-centers"></a><span data-ttu-id="52440-118">Flytja inn kostnaðarstaði</span><span class="sxs-lookup"><span data-stu-id="52440-118">Import cost centers</span></span>
1. <span data-ttu-id="52440-119">Smelltu á Flytja inn víddarstök.</span><span class="sxs-lookup"><span data-stu-id="52440-119">Click Import dimension members.</span></span>
2. <span data-ttu-id="52440-120">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="52440-120">Click OK.</span></span>

## <a name="view-the-imported-cost-centers"></a><span data-ttu-id="52440-121">Skoða innflutta kostnaðarstaði</span><span class="sxs-lookup"><span data-stu-id="52440-121">View the imported cost centers</span></span>
1. <span data-ttu-id="52440-122">Smelltu á Skoða víddarstök.</span><span class="sxs-lookup"><span data-stu-id="52440-122">Click View dimension members.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]