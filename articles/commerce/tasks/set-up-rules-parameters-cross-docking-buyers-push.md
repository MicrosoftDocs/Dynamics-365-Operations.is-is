---
title: " Setja upp reglur og færibreytur fyrir dreifingu frá dreifingarstöð og lager"
description: Þetta ferli sýnir skrefum til að stofna áfyllingarreglur.
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailReplenishmentRuleTable, RetailReplenishmentTreeLookup
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3d4cd276283483340f1dc0bc995cc9073a8aa9c0
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5232690"
---
# <a name="set-up-rules-and-parameters-for-cross-docking-and-buyers-push"></a><span data-ttu-id="50193-103"> Setja upp reglur og færibreytur fyrir dreifingu frá dreifingarstöð og lager</span><span class="sxs-lookup"><span data-stu-id="50193-103">Set up rules and parameters for cross docking and buyer's push</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="50193-104">Þetta ferli sýnir skrefum til að stofna áfyllingarreglur.</span><span class="sxs-lookup"><span data-stu-id="50193-104">This procedure demonstrates the steps to create Replenishment rules.</span></span> <span data-ttu-id="50193-105">Áfyllingarreglur má nota til að stýra hvernig vörur eru dreift á verslanir þegar notuð eru Dreifing frá dreifingarstöð og dreifingar frá lager.</span><span class="sxs-lookup"><span data-stu-id="50193-105">Replenishment rules can be used to control how products are distributed to stores when using Cross-docking and Buyer´s push.</span></span> <span data-ttu-id="50193-106">Áfyllingarreglur er hægt er að setja upp fyrir verslanir eða verslunarflokka.</span><span class="sxs-lookup"><span data-stu-id="50193-106">Replenishment rules can be set up for stores or store groups.</span></span> <span data-ttu-id="50193-107">Þyngd sem er skilgreint fyrir hverja línu í reglu stjórnar því hvernig magn afurða verður dreift á milli verslana þegar notaðar eru áfyllingarreglur sem dreifingaraðferðina dreifing frá dreifingarstöð eða dreifing frá lager.</span><span class="sxs-lookup"><span data-stu-id="50193-107">The weight defined for each line in a rule will control how the quantities of products will get distributed between the stores when using Replenishment rules as the distribution method in Cross-docking or Buyer´s push.</span></span> <span data-ttu-id="50193-108">Þessi aðferð notar sýnigögn USRT fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="50193-108">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="50193-109">Fara á áfyllingarregla</span><span class="sxs-lookup"><span data-stu-id="50193-109">Go to Replenishment rules.</span></span>
2. <span data-ttu-id="50193-110">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="50193-110">Click New.</span></span>
3. <span data-ttu-id="50193-111">Í reitinn áfyllingarregla skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="50193-111">In the Replenishment rule field, type a value.</span></span>
4. <span data-ttu-id="50193-112">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="50193-112">In the Description field, type a value.</span></span>
5. <span data-ttu-id="50193-113">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="50193-113">Click Save.</span></span>
6. <span data-ttu-id="50193-114">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="50193-114">Click Add.</span></span>
7. <span data-ttu-id="50193-115">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="50193-115">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="50193-116">Hægt er að velja áfyllingarstigveldi eða Rásar fyrir gerðina.</span><span class="sxs-lookup"><span data-stu-id="50193-116">You can choose Replenishment hierarchy or Channel for the type.</span></span> <span data-ttu-id="50193-117">Gildi stjórnar því hvort valinu í Heiti verði stigveldi rása eða tiltekin rás.</span><span class="sxs-lookup"><span data-stu-id="50193-117">The value controls whether the selection in Name will be a hierarchy of channels or a specific channel.</span></span>  <span data-ttu-id="50193-118">Í þessu dæmi skal hafa stillt á áfyllingarstigveldi.</span><span class="sxs-lookup"><span data-stu-id="50193-118">For this example, leave it set as Replenishment hierarchy.</span></span>  
8. <span data-ttu-id="50193-119">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="50193-119">In the Name field, select a value.</span></span>
    * <span data-ttu-id="50193-120">sjálfgefna Þyngd gildið er sótt úr þyngd sem er skilgreint í vöruhúsið.</span><span class="sxs-lookup"><span data-stu-id="50193-120">The default weight value is populated from the weight defined on the warehouse.</span></span>  <span data-ttu-id="50193-121">Þetta þyngd er hægt að nota fyrir áfyllingarreglu eða hægt er að færa inn nýja þyngd í svæðinu Þyngd.</span><span class="sxs-lookup"><span data-stu-id="50193-121">This weight can be used for the Replenishment rule or you can enter a new weight in the Weight field.</span></span>  
9. <span data-ttu-id="50193-122">Í reitinn þyngd skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="50193-122">In the Weight field, enter a number.</span></span>
10. <span data-ttu-id="50193-123">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="50193-123">Click Add.</span></span>
11. <span data-ttu-id="50193-124">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="50193-124">In the list, mark the selected row.</span></span>
12. <span data-ttu-id="50193-125">Í reitnum Tegund skal velja Rás.</span><span class="sxs-lookup"><span data-stu-id="50193-125">In the Type field, select 'Channel'.</span></span>
13. <span data-ttu-id="50193-126">Sláið inn eða veldu gildi í reitnum heiti.</span><span class="sxs-lookup"><span data-stu-id="50193-126">In the Name field, enter or select a value.</span></span>
14. <span data-ttu-id="50193-127">Í reitinn þyngd skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="50193-127">In the Weight field, enter a number.</span></span>
15. <span data-ttu-id="50193-128">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="50193-128">Click Save.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]