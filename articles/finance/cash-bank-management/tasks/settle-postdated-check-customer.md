---
title: Gera upp fyrirframdagsetta ávísun frá viðskiptavini
description: Hægt er að gera upp fyrirframdagsetta ávísun eftir ávísunin hefur verið samþykkt af bankanum.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPostDatedChecks, SystemDate, LedgerJournalTable, LedgerJournalTransDaily, LedgerTransVoucher
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 635a1c50390bca59cd1c9ba0cf0421c510b2998c
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2178293"
---
# <a name="settle-a-postdated-check-from-a-customer"></a><span data-ttu-id="d67ca-103">Gera upp fyrirframdagsetta ávísun frá viðskiptavini</span><span class="sxs-lookup"><span data-stu-id="d67ca-103">Settle a postdated check from a customer</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d67ca-104">Hægt er að gera upp fyrirframdagsetta ávísun eftir ávísunin hefur verið samþykkt af bankanum.</span><span class="sxs-lookup"><span data-stu-id="d67ca-104">You can settle a postdated check after the check has been cleared by the bank.</span></span> <span data-ttu-id="d67ca-105">Þessi fjárhagsfærsla samþykkir einnig millifærslur fyrir fyrirframdagsettu ávísunina.</span><span class="sxs-lookup"><span data-stu-id="d67ca-105">This financial transaction also clears the bridge account transaction for the postdated check.</span></span> 

<span data-ttu-id="d67ca-106">Ljúka þarf eftirfarandi verkum áður en þetta er ræst.</span><span class="sxs-lookup"><span data-stu-id="d67ca-106">The following tasks must be complete before you start this one.</span></span>

1) <span data-ttu-id="d67ca-107">Setja upp fyrirframdagsettar ávísanir</span><span class="sxs-lookup"><span data-stu-id="d67ca-107">Set up postdated checks</span></span>

2) <span data-ttu-id="d67ca-108">Skrá og bóka fyrirframdagsetta ávísun fyrir viðskiptavin</span><span class="sxs-lookup"><span data-stu-id="d67ca-108">Register and post a postdated check for a customer</span></span> 



<span data-ttu-id="d67ca-109">Hlutverk þetta leiðbeiningar fyrir verk er Gjaldkera.</span><span class="sxs-lookup"><span data-stu-id="d67ca-109">The role of this task guides is Treasurer.</span></span>



<span data-ttu-id="d67ca-110">Þessi aðferð notar sýnigögn USMF fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="d67ca-110">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="d67ca-111">Fara í Skuldir og innheimta > Fyrirspurnir og skýrslur > Greiðslur > Fyrirframdagsettar ávísanir viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="d67ca-111">Go to Credit and collections > Inquiries and reports > Payments > Customer postdated checks.</span></span>
2. <span data-ttu-id="d67ca-112">Smellt er á Gera upp.</span><span class="sxs-lookup"><span data-stu-id="d67ca-112">Click Settle.</span></span>
3. <span data-ttu-id="d67ca-113">Smellt er á Gera upp jöfnunarfærslur.</span><span class="sxs-lookup"><span data-stu-id="d67ca-113">Click Settle clearing entries.</span></span>
    * <span data-ttu-id="d67ca-114">Gera upp viðskiptavinalykil fyrir ávísunarfærsluna.</span><span class="sxs-lookup"><span data-stu-id="d67ca-114">Settle the customer account for the check transaction.</span></span>  
4. <span data-ttu-id="d67ca-115">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="d67ca-115">Close the page.</span></span>
5. <span data-ttu-id="d67ca-116">Fara í fjárhag > Færslubókarfærslur > Almennar færslubækur.</span><span class="sxs-lookup"><span data-stu-id="d67ca-116">Go to General ledger > Journal entries > General journals.</span></span>
6. <span data-ttu-id="d67ca-117">Í reitnum Sýna skal velja valkost.</span><span class="sxs-lookup"><span data-stu-id="d67ca-117">In the Show field, select an option.</span></span>
7. <span data-ttu-id="d67ca-118">Veldu eða hreinsaðu gátreitinn Sýna aðeins notanda-stofnað.</span><span class="sxs-lookup"><span data-stu-id="d67ca-118">Select or clear the Show user-created only check box.</span></span>
8. <span data-ttu-id="d67ca-119">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="d67ca-119">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="d67ca-120">Smellið á Línur.</span><span class="sxs-lookup"><span data-stu-id="d67ca-120">Click Lines.</span></span>
10. <span data-ttu-id="d67ca-121">Smellt er á Fylgiskjalið.</span><span class="sxs-lookup"><span data-stu-id="d67ca-121">Click Voucher.</span></span>
11. <span data-ttu-id="d67ca-122">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="d67ca-122">Close the page.</span></span>
