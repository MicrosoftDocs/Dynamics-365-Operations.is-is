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
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3bb190e720e5040d446d75a2e8c39cb360019d42
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5256878"
---
# <a name="define-loyalty-reward-points"></a><span data-ttu-id="a4186-103">Skilgreina vildarpunkta smásölu</span><span class="sxs-lookup"><span data-stu-id="a4186-103">Define loyalty reward points</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a4186-104">Þetta ferli fer í gegnum skilgreina vildarpunkta.</span><span class="sxs-lookup"><span data-stu-id="a4186-104">This procedure walks through defining loyalty reward points.</span></span> <span data-ttu-id="a4186-105">Setja ætti upp vildarpunkta áður en að setja upp vildarkerfis.</span><span class="sxs-lookup"><span data-stu-id="a4186-105">You should set up loyalty reward points before you set up a loyalty program.</span></span> <span data-ttu-id="a4186-106">Þessi aðferð notar USRT sýnigögn fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="a4186-106">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="a4186-107">Fara í Retail og Commerce > Viðskiptamenn > Vild > Vildarpunktar.</span><span class="sxs-lookup"><span data-stu-id="a4186-107">Go to Retail and Commerce > Customers > Loyalty > Loyalty reward points.</span></span>
2. <span data-ttu-id="a4186-108">Smellið á Nýtt.</span><span class="sxs-lookup"><span data-stu-id="a4186-108">Click New.</span></span>
3. <span data-ttu-id="a4186-109">Færa inn gildi í svæðið fyrir Kenni Vildarpunkts.</span><span class="sxs-lookup"><span data-stu-id="a4186-109">In the Reward point ID field, type a value.</span></span>
4. <span data-ttu-id="a4186-110">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="a4186-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="a4186-111">Í svæðinu fyrir verð vildarpunkta, skal velja valkost.</span><span class="sxs-lookup"><span data-stu-id="a4186-111">In the Reward point type field, select an option.</span></span>
    * <span data-ttu-id="a4186-112">Veljið Magn ef þú vilt að vildarpunktar til að slétta í næsta heiltala.</span><span class="sxs-lookup"><span data-stu-id="a4186-112">Select Quantity if you want the reward points to be rounded to the nearest integer.</span></span> <span data-ttu-id="a4186-113">Velja Upphæð ef vildarpunktar eiga að vera sléttaðir samkvæmt sléttunarreglum gjaldmiðils.</span><span class="sxs-lookup"><span data-stu-id="a4186-113">Select Amount if you want the reward points to be rounded according to currency rounding rules.</span></span> <span data-ttu-id="a4186-114">Ef valið er Magn, sleppa næsta skref í þessu ferli ...</span><span class="sxs-lookup"><span data-stu-id="a4186-114">If you select Quantity, skip the next step of this procedure..</span></span>  
6. <span data-ttu-id="a4186-115">Í reitinn Gjaldmiðill skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="a4186-115">In the Currency field, type a value.</span></span>
    * <span data-ttu-id="a4186-116">Fyrir vildarpunktar af gerðinni upphæð, munu allar útgefinna punkta hafa völdum gjaldmiðli.</span><span class="sxs-lookup"><span data-stu-id="a4186-116">For Amount type reward points, all points issued will have the selected currency.</span></span> <span data-ttu-id="a4186-117">Vildarpunktar af gerð Magni, á þetta svæði ekki við — sleppa þessu þrepi.</span><span class="sxs-lookup"><span data-stu-id="a4186-117">For Quantity type reward points, this field doesn't apply—skip this step.</span></span>  
7. <span data-ttu-id="a4186-118">Merkið eða afmerkið reitinn innleysanlegt.</span><span class="sxs-lookup"><span data-stu-id="a4186-118">Check or uncheck the Redeemable checkbox.</span></span>
8. <span data-ttu-id="a4186-119">Í reitinn innleysa röðun skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="a4186-119">In the Redeem ranking field, enter a number.</span></span>
    * <span data-ttu-id="a4186-120">Innleysa röðun er notaður þegar tvær eða fleiri innleysanlega vildarpunkta er hægt að nota til að greiða fyrir afurðir.</span><span class="sxs-lookup"><span data-stu-id="a4186-120">Redeem ranking is used when two or more redeemable reward points can be used to pay for products.</span></span> <span data-ttu-id="a4186-121">Ef tvö vildarpunktar hafa sama innleysa vægi, svo það eina sem þarf í neðri fjölda stiga sem verður notað.</span><span class="sxs-lookup"><span data-stu-id="a4186-121">If the two reward points have the same redeem ranking, then the one that needs to lower number of points will be used.</span></span>  
9. <span data-ttu-id="a4186-122">Í reitinn gildistími skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="a4186-122">In the Expiration time value field, enter a number.</span></span>
    * <span data-ttu-id="a4186-123">Vildarpunktar renna út eftir tilgreindan fjölda daga, mánaða eða ára eftir þegar punkta eru gefin út.</span><span class="sxs-lookup"><span data-stu-id="a4186-123">The reward points will expire the specified number of days, months, or years after when the points are issued.</span></span> <span data-ttu-id="a4186-124">Gildið „0” þýðir vildarumbun vildarpunkta rennur aldrei út.</span><span class="sxs-lookup"><span data-stu-id="a4186-124">A value of '0' means the loyalty reward points will never expire.</span></span>  
10. <span data-ttu-id="a4186-125">Veljið valkost í reitnum eining Gildistíma.</span><span class="sxs-lookup"><span data-stu-id="a4186-125">In the Expiration time unit field, select an option.</span></span>
11. <span data-ttu-id="a4186-126">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="a4186-126">Click Save.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]