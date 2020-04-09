---
title: Setja upp bónusafskriftir
description: Þessi ferli sýnir hvernig á að stofna sérstök heimild til afskriftar og tengja hana við eignabók.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBonus, AssetGroup, AssetGroupBookSetup, AssetGroupSetupBonus
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 91243a4cee44410a221902990d31a10f1805eb08
ms.sourcegitcommit: c69926b4285cb2ec2d9ce1ad72d1cb852024dd5e
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/18/2020
ms.locfileid: "3138254"
---
# <a name="set-up-bonus-depreciation"></a><span data-ttu-id="31d76-103">Setja upp bónusafskriftir</span><span class="sxs-lookup"><span data-stu-id="31d76-103">Set up bonus depreciation</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="31d76-104">Þessi ferli sýnir hvernig á að stofna sérstök heimild til afskriftar og tengja hana við eignabók.</span><span class="sxs-lookup"><span data-stu-id="31d76-104">This procedure shows how to create a special depreciation allowance and associate it with a fixed asset book.</span></span> <span data-ttu-id="31d76-105">Það notar Bókari hlutverk og sýnigögn fyrir USMF lögaðila.</span><span class="sxs-lookup"><span data-stu-id="31d76-105">It uses the accountant role and demo data for the USMF legal entity.</span></span>


## <a name="create-a-special-depreciation-allowance"></a><span data-ttu-id="31d76-106">Stofna Sérstök heimild Stofna til afskriftar</span><span class="sxs-lookup"><span data-stu-id="31d76-106">Create a special depreciation allowance</span></span>
1. <span data-ttu-id="31d76-107">Fara í Eignir > Uppsetning > Sérstök heimild til afskriftar.</span><span class="sxs-lookup"><span data-stu-id="31d76-107">Go to Fixed assets > Setup > Special depreciation allowance.</span></span>
2. <span data-ttu-id="31d76-108">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="31d76-108">Click New.</span></span>
3. <span data-ttu-id="31d76-109">Færa inn gildi í svæðinu sérstök heimild til afskriftar.</span><span class="sxs-lookup"><span data-stu-id="31d76-109">In the Special depreciation allowance field, type a value.</span></span>
4. <span data-ttu-id="31d76-110">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="31d76-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="31d76-111">Færið inn tölu í svæðinu prósenta.</span><span class="sxs-lookup"><span data-stu-id="31d76-111">In the Percentage field, enter a number.</span></span>
    * <span data-ttu-id="31d76-112">Setja inn upphæð ef ekki var tilgreint í prósentum.</span><span class="sxs-lookup"><span data-stu-id="31d76-112">If a percentage was not indicated, set an amount.</span></span>  

## <a name="associate-a-special-depreciation-allowance-with-a-fixed-asset-group-book"></a><span data-ttu-id="31d76-113">Tengja sérstök heimild til afskriftar við eignaflokk bókar</span><span class="sxs-lookup"><span data-stu-id="31d76-113">Associate a special depreciation allowance with a fixed asset group book</span></span>
1. <span data-ttu-id="31d76-114">Fara í Eignir > Uppsetning > Eignaflokkar.</span><span class="sxs-lookup"><span data-stu-id="31d76-114">Go to Fixed assets > Setup > Fixed asset groups.</span></span>
2. <span data-ttu-id="31d76-115">Veljið eignaflokk tengist sérstök heimild til afskriftar á listanum.</span><span class="sxs-lookup"><span data-stu-id="31d76-115">In the list, select the fixed asset group associated with the special depreciation allowance.</span></span>
3. <span data-ttu-id="31d76-116">Smelltu á bækur.</span><span class="sxs-lookup"><span data-stu-id="31d76-116">Click Books.</span></span>
4. <span data-ttu-id="31d76-117">Á listanum, veljið bók sem tengist sérstök heimild til afskriftar.</span><span class="sxs-lookup"><span data-stu-id="31d76-117">In the list, select the book that is associated with the special depreciation allowance.</span></span>
5. <span data-ttu-id="31d76-118">Smellt er á Sérstök heimild til afskriftar</span><span class="sxs-lookup"><span data-stu-id="31d76-118">Click Special depreciation allowance.</span></span>
6. <span data-ttu-id="31d76-119">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="31d76-119">Click New.</span></span>
7. <span data-ttu-id="31d76-120">Sláið inn eða veldu gildi í reitnum sérstök heimild til afskriftar.</span><span class="sxs-lookup"><span data-stu-id="31d76-120">In the Special depreciation allowance field, enter or select a value.</span></span>
    * <span data-ttu-id="31d76-121">Prósenta eða Upphæð er sjálfgefið úr uppsetningu sérstök heimild til afskriftar.</span><span class="sxs-lookup"><span data-stu-id="31d76-121">The default for Percentage or Amount comes from the special depreciation allowance setup.</span></span>  
8. <span data-ttu-id="31d76-122">Í reitinn forgangur skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="31d76-122">In the Priority field, enter a number.</span></span>

