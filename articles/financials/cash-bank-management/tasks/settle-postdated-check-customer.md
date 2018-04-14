--- 
title: "Gera upp fyrirframdagsetta ávísun frá viðskiptavini"
description: "Hægt er að gera upp fyrirframdagsetta ávísun eftir ávísunin hefur verið samþykkt af bankanum."
author: kweekley
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 92076bf8e57aae31f40411f82d04731d0f3b5477
ms.contentlocale: is-is
ms.lasthandoff: 04/13/2018

---
# <a name="settle-a-postdated-check-from-a-customer"></a><span data-ttu-id="5e02e-103">Gera upp fyrirframdagsetta ávísun frá viðskiptavini</span><span class="sxs-lookup"><span data-stu-id="5e02e-103">Settle a postdated check from a customer</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5e02e-104">Hægt er að gera upp fyrirframdagsetta ávísun eftir ávísunin hefur verið samþykkt af bankanum.</span><span class="sxs-lookup"><span data-stu-id="5e02e-104">You can settle a postdated check after the check has been cleared by the bank.</span></span> <span data-ttu-id="5e02e-105">Þessi fjárhagsfærsla samþykkir einnig millifærslur fyrir fyrirframdagsettu ávísunina.</span><span class="sxs-lookup"><span data-stu-id="5e02e-105">This financial transaction also clears the bridge account transaction for the postdated check.</span></span> 

<span data-ttu-id="5e02e-106">Ljúka þarf eftirfarandi verkum áður en þetta er ræst.</span><span class="sxs-lookup"><span data-stu-id="5e02e-106">The following tasks must be complete before you start this one.</span></span>

1) <span data-ttu-id="5e02e-107">Setja upp fyrirframdagsettar ávísanir</span><span class="sxs-lookup"><span data-stu-id="5e02e-107">Set up postdated checks</span></span>

2) <span data-ttu-id="5e02e-108">Skrá og bóka fyrirframdagsetta ávísun fyrir viðskiptavin</span><span class="sxs-lookup"><span data-stu-id="5e02e-108">Register and post a postdated check for a customer</span></span> 



<span data-ttu-id="5e02e-109">Hlutverk þetta leiðbeiningar fyrir verk er Gjaldkera.</span><span class="sxs-lookup"><span data-stu-id="5e02e-109">The role of this task guides is Treasurer.</span></span>



<span data-ttu-id="5e02e-110">Þessi aðferð notar sýnigögn USMF fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="5e02e-110">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="5e02e-111">Fara í Skuldir og innheimta > Fyrirspurnir og skýrslur > Greiðslur > Fyrirframdagsettar ávísanir viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="5e02e-111">Go to Credit and collections > Inquiries and reports > Payments > Customer postdated checks.</span></span>
2. <span data-ttu-id="5e02e-112">Smellt er á Gera upp.</span><span class="sxs-lookup"><span data-stu-id="5e02e-112">Click Settle.</span></span>
3. <span data-ttu-id="5e02e-113">Smellt er á Gera upp jöfnunarfærslur.</span><span class="sxs-lookup"><span data-stu-id="5e02e-113">Click Settle clearing entries.</span></span>
    * <span data-ttu-id="5e02e-114">Gera upp viðskiptavinalykil fyrir ávísunarfærsluna.</span><span class="sxs-lookup"><span data-stu-id="5e02e-114">Settle the customer account for the check transaction.</span></span>  
4. <span data-ttu-id="5e02e-115">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="5e02e-115">Close the page.</span></span>
5. <span data-ttu-id="5e02e-116">Fara í fjárhag > Færslubókarfærslur > Almennar færslubækur.</span><span class="sxs-lookup"><span data-stu-id="5e02e-116">Go to General ledger > Journal entries > General journals.</span></span>
6. <span data-ttu-id="5e02e-117">Í reitnum Sýna skal velja valkost.</span><span class="sxs-lookup"><span data-stu-id="5e02e-117">In the Show field, select an option.</span></span>
7. <span data-ttu-id="5e02e-118">Veldu eða hreinsaðu gátreitinn Sýna aðeins notanda-stofnað.</span><span class="sxs-lookup"><span data-stu-id="5e02e-118">Select or clear the Show user-created only check box.</span></span>
8. <span data-ttu-id="5e02e-119">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="5e02e-119">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="5e02e-120">Smellið á Línur.</span><span class="sxs-lookup"><span data-stu-id="5e02e-120">Click Lines.</span></span>
10. <span data-ttu-id="5e02e-121">Smellt er á Fylgiskjalið.</span><span class="sxs-lookup"><span data-stu-id="5e02e-121">Click Voucher.</span></span>
11. <span data-ttu-id="5e02e-122">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="5e02e-122">Close the page.</span></span>


