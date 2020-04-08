---
title: Skilgreina vildarpunkta smásölu
description: Þetta ferli fer í gegnum skilgreina vildarpunkta.
author: scott-tucker
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailLoyaltyRewardPoints
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9557b25af0fba6429d34564e1a3e158b6258698a
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022899"
---
# <a name="define-loyalty-reward-points"></a><span data-ttu-id="9c078-103">Skilgreina vildarpunkta smásölu</span><span class="sxs-lookup"><span data-stu-id="9c078-103">Define loyalty reward points</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="9c078-104">Þetta ferli fer í gegnum skilgreina vildarpunkta.</span><span class="sxs-lookup"><span data-stu-id="9c078-104">This procedure walks through defining loyalty reward points.</span></span> <span data-ttu-id="9c078-105">Setja ætti upp vildarpunkta áður en að setja upp vildarkerfis.</span><span class="sxs-lookup"><span data-stu-id="9c078-105">You should set up loyalty reward points before you set up a loyalty program.</span></span> <span data-ttu-id="9c078-106">Þessi aðferð notar USRT sýnigögn fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="9c078-106">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="9c078-107">Fara í Retail og Commerce > Viðskiptamenn > Vild > Vildarpunktar.</span><span class="sxs-lookup"><span data-stu-id="9c078-107">Go to Retail and Commerce > Customers > Loyalty > Loyalty reward points.</span></span>
2. <span data-ttu-id="9c078-108">Smellið á Nýtt.</span><span class="sxs-lookup"><span data-stu-id="9c078-108">Click New.</span></span>
3. <span data-ttu-id="9c078-109">Færa inn gildi í svæðið fyrir Kenni Vildarpunkts.</span><span class="sxs-lookup"><span data-stu-id="9c078-109">In the Reward point ID field, type a value.</span></span>
4. <span data-ttu-id="9c078-110">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="9c078-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="9c078-111">Í svæðinu fyrir verð vildarpunkta, skal velja valkost.</span><span class="sxs-lookup"><span data-stu-id="9c078-111">In the Reward point type field, select an option.</span></span>
    * <span data-ttu-id="9c078-112">Veljið Magn ef þú vilt að vildarpunktar til að slétta í næsta heiltala.</span><span class="sxs-lookup"><span data-stu-id="9c078-112">Select Quantity if you want the reward points to be rounded to the nearest integer.</span></span> <span data-ttu-id="9c078-113">Velja Upphæð ef vildarpunktar eiga að vera sléttaðir samkvæmt sléttunarreglum gjaldmiðils.</span><span class="sxs-lookup"><span data-stu-id="9c078-113">Select Amount if you want the reward points to be rounded according to currency rounding rules.</span></span> <span data-ttu-id="9c078-114">Ef valið er Magn, sleppa næsta skref í þessu ferli ...</span><span class="sxs-lookup"><span data-stu-id="9c078-114">If you select Quantity, skip the next step of this procedure..</span></span>  
6. <span data-ttu-id="9c078-115">Í reitinn Gjaldmiðill skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="9c078-115">In the Currency field, type a value.</span></span>
    * <span data-ttu-id="9c078-116">Fyrir vildarpunktar af gerðinni upphæð, munu allar útgefinna punkta hafa völdum gjaldmiðli.</span><span class="sxs-lookup"><span data-stu-id="9c078-116">For Amount type reward points, all points issued will have the selected currency.</span></span> <span data-ttu-id="9c078-117">Vildarpunktar af gerð Magni, á þetta svæði ekki við — sleppa þessu þrepi.</span><span class="sxs-lookup"><span data-stu-id="9c078-117">For Quantity type reward points, this field doesn't apply—skip this step.</span></span>  
7. <span data-ttu-id="9c078-118">Merkið eða afmerkið reitinn innleysanlegt.</span><span class="sxs-lookup"><span data-stu-id="9c078-118">Check or uncheck the Redeemable checkbox.</span></span>
8. <span data-ttu-id="9c078-119">Í reitinn innleysa röðun skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="9c078-119">In the Redeem ranking field, enter a number.</span></span>
    * <span data-ttu-id="9c078-120">Innleysa röðun er notaður þegar tvær eða fleiri innleysanlega vildarpunkta er hægt að nota til að greiða fyrir afurðir.</span><span class="sxs-lookup"><span data-stu-id="9c078-120">Redeem ranking is used when two or more redeemable reward points can be used to pay for products.</span></span> <span data-ttu-id="9c078-121">Ef tvö vildarpunktar hafa sama innleysa vægi, svo það eina sem þarf í neðri fjölda stiga sem verður notað.</span><span class="sxs-lookup"><span data-stu-id="9c078-121">If the two reward points have the same redeem ranking, then the one that needs to lower number of points will be used.</span></span>  
9. <span data-ttu-id="9c078-122">Í reitinn gildistími skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="9c078-122">In the Expiration time value field, enter a number.</span></span>
    * <span data-ttu-id="9c078-123">Vildarpunktar renna út eftir tilgreindan fjölda daga, mánaða eða ára eftir þegar punkta eru gefin út.</span><span class="sxs-lookup"><span data-stu-id="9c078-123">The reward points will expire the specified number of days, months, or years after when the points are issued.</span></span> <span data-ttu-id="9c078-124">Gildið "0" þýðir vildarumbun vildarpunkta rennur aldrei út.</span><span class="sxs-lookup"><span data-stu-id="9c078-124">A value of ‘0’ means the loyalty reward points will never expire.</span></span>  
10. <span data-ttu-id="9c078-125">Veljið valkost í reitnum eining Gildistíma.</span><span class="sxs-lookup"><span data-stu-id="9c078-125">In the Expiration time unit field, select an option.</span></span>
11. <span data-ttu-id="9c078-126">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="9c078-126">Click Save.</span></span>
