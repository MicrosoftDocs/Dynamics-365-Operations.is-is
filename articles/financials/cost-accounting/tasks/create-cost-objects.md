---
title: 'Stofna kostnaðarhluti  '
description: Þessi verklýsing sýnir hvernig á að stofna kostnaðarhluti með því að flytja inn Dynamics 365 for Finance and Operations Enterprise Edition fjárhagsvídd kostnaðarstaðar inn í kostnaðarbókhald í gegnum gagnatengi.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension, CAMAXFinancialDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1e12de1d51658092fb19f652cef7c1cc78b255b5
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1543772"
---
# <a name="create-cost-objects"></a><span data-ttu-id="c5471-103">Stofna kostnaðarhluti  </span><span class="sxs-lookup"><span data-stu-id="c5471-103">Create cost objects</span></span> 

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c5471-104">Þessi verklýsing sýnir hvernig á að stofna kostnaðarhluti með því að flytja inn Dynamics 365 for Finance and Operations Enterprise Edition fjárhagsvídd kostnaðarstaðar inn í kostnaðarbókhald í gegnum gagnatengi.</span><span class="sxs-lookup"><span data-stu-id="c5471-104">This procedure shows how to create cost objects by importing the Dynamics 365 for Finance and Operations, Enterprise edition cost center financial dimension into Cost accounting via a data connector.</span></span> <span data-ttu-id="c5471-105">USMF sýnifyrirtækið var notað til að stofna þetta ferli.</span><span class="sxs-lookup"><span data-stu-id="c5471-105">The USMF demo company was used to create this procedure.</span></span> <span data-ttu-id="c5471-106">Þetta ferli er fyrir eiginleika kostnaðarbókhalds sem var bætt við í Dynamics 365 for Operations 1611 útgáfu.</span><span class="sxs-lookup"><span data-stu-id="c5471-106">This procedure is for a Cost accounting feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="create-new-cost-objects"></a><span data-ttu-id="c5471-107">Stofna nýjar kostnaðarhluti</span><span class="sxs-lookup"><span data-stu-id="c5471-107">Create new cost objects</span></span>
1. <span data-ttu-id="c5471-108">Fara í kostnaðarbókhald > Víddir > víddir kostnaðarhlutar.</span><span class="sxs-lookup"><span data-stu-id="c5471-108">Go to Cost accounting > Dimensions > Cost object dimensions.</span></span>
2. <span data-ttu-id="c5471-109">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="c5471-109">Click New.</span></span>
3. <span data-ttu-id="c5471-110">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="c5471-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="c5471-111">Í reitinn gagnatengi fyrir víddarstök skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="c5471-111">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="c5471-112">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="c5471-112">In the Description field, type a value.</span></span>
6. <span data-ttu-id="c5471-113">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="c5471-113">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="c5471-114">Stilla gagnatengi</span><span class="sxs-lookup"><span data-stu-id="c5471-114">Configure the data connector</span></span>
1. <span data-ttu-id="c5471-115">Smelltu á Skilgreina víddarstakaveitu</span><span class="sxs-lookup"><span data-stu-id="c5471-115">Click Configure dimension member provider.</span></span>
    * <span data-ttu-id="c5471-116">Veljið CostCenter að flytja inn víddir CostCenter í kostnaðarbókhald.</span><span class="sxs-lookup"><span data-stu-id="c5471-116">Select CostCenter to import the CostCenter dimension into Cost accounting.</span></span>  
2. <span data-ttu-id="c5471-117">Í reitnum heiti víddar skal velja kostnaðarstað.</span><span class="sxs-lookup"><span data-stu-id="c5471-117">In the Dimension name field, select Cost center.</span></span>
3. <span data-ttu-id="c5471-118">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="c5471-118">Click OK.</span></span>

## <a name="import-cost-centers"></a><span data-ttu-id="c5471-119">Flytja inn kostnaðarstaði</span><span class="sxs-lookup"><span data-stu-id="c5471-119">Import cost centers</span></span>
1. <span data-ttu-id="c5471-120">Smelltu á Flytja inn víddarstök.</span><span class="sxs-lookup"><span data-stu-id="c5471-120">Click Import dimension members.</span></span>
2. <span data-ttu-id="c5471-121">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="c5471-121">Click OK.</span></span>

## <a name="view-the-imported-cost-centers"></a><span data-ttu-id="c5471-122">Skoða innflutta kostnaðarstaði</span><span class="sxs-lookup"><span data-stu-id="c5471-122">View the imported cost centers</span></span>
1. <span data-ttu-id="c5471-123">Smelltu á Skoða víddarstök.</span><span class="sxs-lookup"><span data-stu-id="c5471-123">Click View dimension members.</span></span>

