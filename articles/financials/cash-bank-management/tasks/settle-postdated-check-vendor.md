--- 
title: "Gera upp fyrirframdagsetta ávísun fyrir lánardrottin"
description: "Jafna fyrirframdagsetta ávísun til lánardrottins þegar bankinn hefur afgreitt ávísunarfærsla eftir ávísun hefur verið í vanskilum og afgreidd af bankanum."
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: c2facae3de31b0a9a1d426b49c9ea5778adca8e6
ms.contentlocale: is-is
ms.lasthandoff: 05/08/2018

---
# <a name="settle-a-postdated-check-for-a-vendor"></a><span data-ttu-id="3b56c-103">Gera upp fyrirframdagsetta ávísun fyrir lánardrottin</span><span class="sxs-lookup"><span data-stu-id="3b56c-103">Settle a postdated check for a vendor</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3b56c-104">Jafna fyrirframdagsetta ávísun til lánardrottins þegar bankinn hefur afgreitt ávísunarfærsla eftir ávísun hefur verið í vanskilum og afgreidd af bankanum.</span><span class="sxs-lookup"><span data-stu-id="3b56c-104">Settle a postdated check issued to a vendor when the bank has cleared the check transaction after the check has been overdue and cleared by the bank.</span></span> 

<span data-ttu-id="3b56c-105">Ljúka skal eftirfarandi aðgerðum áður en hann þessi er hafin.</span><span class="sxs-lookup"><span data-stu-id="3b56c-105">Complete the following procedures before you start this one.</span></span>

1) <span data-ttu-id="3b56c-106">Setja upp fyrirframdagsettar ávísanir</span><span class="sxs-lookup"><span data-stu-id="3b56c-106">Set up postdated checks</span></span>

2) <span data-ttu-id="3b56c-107">Skrá og bóka fyrirframdagsetta ávísun fyrir lánardrottinn</span><span class="sxs-lookup"><span data-stu-id="3b56c-107">Register and post a postdated check for a vendor</span></span>



<span data-ttu-id="3b56c-108">Hlutverk þessa ferlis er fjárreiðustjóri.</span><span class="sxs-lookup"><span data-stu-id="3b56c-108">The role of this procedure is Treasurer.</span></span> <span data-ttu-id="3b56c-109">Þessi aðferð notar sýnigögn USMF fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="3b56c-109">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="3b56c-110">Fara í Viðskiptaskuldir > Greiðslur > Fyrirframdagsettar ávísanir lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="3b56c-110">Go to Accounts payable > Payments > Vendor postdated checks.</span></span>
2. <span data-ttu-id="3b56c-111">Smellt er á Gera upp.</span><span class="sxs-lookup"><span data-stu-id="3b56c-111">Click Settle.</span></span>
3. <span data-ttu-id="3b56c-112">Smellt er á Gera upp jöfnunarfærslur.</span><span class="sxs-lookup"><span data-stu-id="3b56c-112">Click Settle clearing entries.</span></span>
    * <span data-ttu-id="3b56c-113">Jafna lykil lánardrottins fyrir ávísunarfærsla.</span><span class="sxs-lookup"><span data-stu-id="3b56c-113">Settle the vendor account for the check transaction.</span></span>  
4. <span data-ttu-id="3b56c-114">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="3b56c-114">Close the page.</span></span>
5. <span data-ttu-id="3b56c-115">Fara í fjárhag > Færslubókarfærslur > Almennar færslubækur.</span><span class="sxs-lookup"><span data-stu-id="3b56c-115">Go to General ledger > Journal entries > General journals.</span></span>
6. <span data-ttu-id="3b56c-116">Í svæði Sýna, velja 'Allt'.</span><span class="sxs-lookup"><span data-stu-id="3b56c-116">In the Show field, select 'All'.</span></span>
7. <span data-ttu-id="3b56c-117">Veldu eða hreinsaðu gátreitinn Sýna aðeins notanda-stofnað.</span><span class="sxs-lookup"><span data-stu-id="3b56c-117">Select or clear the Show user-created only check box.</span></span>
8. <span data-ttu-id="3b56c-118">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="3b56c-118">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="3b56c-119">Smellið á Línur.</span><span class="sxs-lookup"><span data-stu-id="3b56c-119">Click Lines.</span></span>
10. <span data-ttu-id="3b56c-120">Smellt er á Fylgiskjalið.</span><span class="sxs-lookup"><span data-stu-id="3b56c-120">Click Voucher.</span></span>
11. <span data-ttu-id="3b56c-121">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="3b56c-121">Close the page.</span></span>


