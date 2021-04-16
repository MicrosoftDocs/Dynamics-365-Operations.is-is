---
title: Gera upp fyrirframdagsetta ávísun fyrir lánardrottin
description: Jafna fyrirframdagsetta ávísun til lánardrottins þegar bankinn hefur afgreitt ávísunarfærsla eftir ávísun hefur verið í vanskilum og afgreidd af bankanum.
author: kweekley
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendPostDatedChecks, LedgerJournalTable, LedgerJournalTransDaily, LedgerTransVoucher
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 89acad0c9421960ff4d07ed8eec798b9068424d5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834572"
---
# <a name="settle-a-postdated-check-for-a-vendor"></a><span data-ttu-id="7e818-103">Gera upp fyrirframdagsetta ávísun fyrir lánardrottin</span><span class="sxs-lookup"><span data-stu-id="7e818-103">Settle a postdated check for a vendor</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7e818-104">Jafna fyrirframdagsetta ávísun til lánardrottins þegar bankinn hefur afgreitt ávísunarfærsla eftir ávísun hefur verið í vanskilum og afgreidd af bankanum.</span><span class="sxs-lookup"><span data-stu-id="7e818-104">Settle a postdated check issued to a vendor when the bank has cleared the check transaction after the check has been overdue and cleared by the bank.</span></span> 

<span data-ttu-id="7e818-105">Ljúka skal eftirfarandi aðgerðum áður en hann þessi er hafin.</span><span class="sxs-lookup"><span data-stu-id="7e818-105">Complete the following procedures before you start this one.</span></span>

1) <span data-ttu-id="7e818-106">Setja upp fyrirframdagsettar ávísanir</span><span class="sxs-lookup"><span data-stu-id="7e818-106">Set up postdated checks</span></span>

2) <span data-ttu-id="7e818-107">Skrá og bóka fyrirframdagsetta ávísun fyrir lánardrottinn</span><span class="sxs-lookup"><span data-stu-id="7e818-107">Register and post a postdated check for a vendor</span></span>



<span data-ttu-id="7e818-108">Hlutverk þessa ferlis er fjárreiðustjóri.</span><span class="sxs-lookup"><span data-stu-id="7e818-108">The role of this procedure is Treasurer.</span></span> <span data-ttu-id="7e818-109">Þessi aðferð notar sýnigögn USMF fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="7e818-109">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="7e818-110">Fara í Viðskiptaskuldir > Greiðslur > Fyrirframdagsettar ávísanir lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="7e818-110">Go to Accounts payable > Payments > Vendor postdated checks.</span></span>
2. <span data-ttu-id="7e818-111">Smellt er á Gera upp.</span><span class="sxs-lookup"><span data-stu-id="7e818-111">Click Settle.</span></span>
3. <span data-ttu-id="7e818-112">Smellt er á Gera upp jöfnunarfærslur.</span><span class="sxs-lookup"><span data-stu-id="7e818-112">Click Settle clearing entries.</span></span>
    * <span data-ttu-id="7e818-113">Jafna lykil lánardrottins fyrir ávísunarfærsla.</span><span class="sxs-lookup"><span data-stu-id="7e818-113">Settle the vendor account for the check transaction.</span></span>  
4. <span data-ttu-id="7e818-114">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="7e818-114">Close the page.</span></span>
5. <span data-ttu-id="7e818-115">Fara í fjárhag > Færslubókarfærslur > Almennar færslubækur.</span><span class="sxs-lookup"><span data-stu-id="7e818-115">Go to General ledger > Journal entries > General journals.</span></span>
6. <span data-ttu-id="7e818-116">Í svæði Sýna, velja 'Allt'.</span><span class="sxs-lookup"><span data-stu-id="7e818-116">In the Show field, select 'All'.</span></span>
7. <span data-ttu-id="7e818-117">Veldu eða hreinsaðu gátreitinn Sýna aðeins notanda-stofnað.</span><span class="sxs-lookup"><span data-stu-id="7e818-117">Select or clear the Show user-created only check box.</span></span>
8. <span data-ttu-id="7e818-118">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="7e818-118">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="7e818-119">Smellið á Línur.</span><span class="sxs-lookup"><span data-stu-id="7e818-119">Click Lines.</span></span>
10. <span data-ttu-id="7e818-120">Smellt er á Fylgiskjalið.</span><span class="sxs-lookup"><span data-stu-id="7e818-120">Click Voucher.</span></span>
11. <span data-ttu-id="7e818-121">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="7e818-121">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]