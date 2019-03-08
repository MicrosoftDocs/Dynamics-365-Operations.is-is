---
title: Gera upp fyrirframdagsetta ávísun fyrir lánardrottin
description: Jafna fyrirframdagsetta ávísun til lánardrottins þegar bankinn hefur afgreitt ávísunarfærsla eftir ávísun hefur verið í vanskilum og afgreidd af bankanum.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPostDatedChecks, LedgerJournalTable, LedgerJournalTransDaily, LedgerTransVoucher
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e46b419ab613425ae2d758f80105ac94f1ec5cc2
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "324331"
---
# <a name="settle-a-postdated-check-for-a-vendor"></a><span data-ttu-id="56571-103">Gera upp fyrirframdagsetta ávísun fyrir lánardrottin</span><span class="sxs-lookup"><span data-stu-id="56571-103">Settle a postdated check for a vendor</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="56571-104">Jafna fyrirframdagsetta ávísun til lánardrottins þegar bankinn hefur afgreitt ávísunarfærsla eftir ávísun hefur verið í vanskilum og afgreidd af bankanum.</span><span class="sxs-lookup"><span data-stu-id="56571-104">Settle a postdated check issued to a vendor when the bank has cleared the check transaction after the check has been overdue and cleared by the bank.</span></span> 

<span data-ttu-id="56571-105">Ljúka skal eftirfarandi aðgerðum áður en hann þessi er hafin.</span><span class="sxs-lookup"><span data-stu-id="56571-105">Complete the following procedures before you start this one.</span></span>

1) <span data-ttu-id="56571-106">Setja upp fyrirframdagsettar ávísanir</span><span class="sxs-lookup"><span data-stu-id="56571-106">Set up postdated checks</span></span>

2) <span data-ttu-id="56571-107">Skrá og bóka fyrirframdagsetta ávísun fyrir lánardrottinn</span><span class="sxs-lookup"><span data-stu-id="56571-107">Register and post a postdated check for a vendor</span></span>



<span data-ttu-id="56571-108">Hlutverk þessa ferlis er fjárreiðustjóri.</span><span class="sxs-lookup"><span data-stu-id="56571-108">The role of this procedure is Treasurer.</span></span> <span data-ttu-id="56571-109">Þessi aðferð notar sýnigögn USMF fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="56571-109">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="56571-110">Fara í Viðskiptaskuldir > Greiðslur > Fyrirframdagsettar ávísanir lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="56571-110">Go to Accounts payable > Payments > Vendor postdated checks.</span></span>
2. <span data-ttu-id="56571-111">Smellt er á Gera upp.</span><span class="sxs-lookup"><span data-stu-id="56571-111">Click Settle.</span></span>
3. <span data-ttu-id="56571-112">Smellt er á Gera upp jöfnunarfærslur.</span><span class="sxs-lookup"><span data-stu-id="56571-112">Click Settle clearing entries.</span></span>
    * <span data-ttu-id="56571-113">Jafna lykil lánardrottins fyrir ávísunarfærsla.</span><span class="sxs-lookup"><span data-stu-id="56571-113">Settle the vendor account for the check transaction.</span></span>  
4. <span data-ttu-id="56571-114">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="56571-114">Close the page.</span></span>
5. <span data-ttu-id="56571-115">Fara í fjárhag > Færslubókarfærslur > Almennar færslubækur.</span><span class="sxs-lookup"><span data-stu-id="56571-115">Go to General ledger > Journal entries > General journals.</span></span>
6. <span data-ttu-id="56571-116">Í svæði Sýna, velja 'Allt'.</span><span class="sxs-lookup"><span data-stu-id="56571-116">In the Show field, select 'All'.</span></span>
7. <span data-ttu-id="56571-117">Veldu eða hreinsaðu gátreitinn Sýna aðeins notanda-stofnað.</span><span class="sxs-lookup"><span data-stu-id="56571-117">Select or clear the Show user-created only check box.</span></span>
8. <span data-ttu-id="56571-118">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="56571-118">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="56571-119">Smellið á Línur.</span><span class="sxs-lookup"><span data-stu-id="56571-119">Click Lines.</span></span>
10. <span data-ttu-id="56571-120">Smellt er á Fylgiskjalið.</span><span class="sxs-lookup"><span data-stu-id="56571-120">Click Voucher.</span></span>
11. <span data-ttu-id="56571-121">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="56571-121">Close the page.</span></span>

