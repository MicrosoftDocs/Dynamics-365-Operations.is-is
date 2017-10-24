--- 
title: "Stofna ítarlegar reglur fyrir færslubækur"
description: "Þetta ferli fer í gegnum hvernig stofnaðar eru ítarlegar reglur fyrir færslubækur."
author: aprilolson
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 1bb1663b0f5d7e6a550e1ffd2ee2edf3771a13b3
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="create-advanced-rules-for-journals"></a><span data-ttu-id="c1ba0-103">Stofna ítarlegar reglur fyrir færslubækur</span><span class="sxs-lookup"><span data-stu-id="c1ba0-103">Create advanced rules for journals</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c1ba0-104">Þetta ferli fer í gegnum hvernig stofnaðar eru ítarlegar reglur fyrir færslubækur.</span><span class="sxs-lookup"><span data-stu-id="c1ba0-104">This procedure steps through creating advanced rules for journals.</span></span> <span data-ttu-id="c1ba0-105">Þar á meðal uppsetningu færslubókareftirlits og bókunartakmarkana notanda.</span><span class="sxs-lookup"><span data-stu-id="c1ba0-105">This includes setting up journal control and user posting restrictions.</span></span> <span data-ttu-id="c1ba0-106">Þessi aðferð notar sýnifyrirtækið USMF.</span><span class="sxs-lookup"><span data-stu-id="c1ba0-106">This procedure uses the USMF demo data company.</span></span>


## <a name="set-up-journal-control"></a><span data-ttu-id="c1ba0-107">Setja upp færslubókaeftirlit</span><span class="sxs-lookup"><span data-stu-id="c1ba0-107">Set up journal control</span></span>
1. <span data-ttu-id="c1ba0-108">Fara í Fjárhag > Færslubókaruppsetning > Heiti færslubókar.</span><span class="sxs-lookup"><span data-stu-id="c1ba0-108">Go to General ledger > Journal setup > Journal names.</span></span>
2. <span data-ttu-id="c1ba0-109">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="c1ba0-109">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="c1ba0-110">Smellt er á færslubókareftirlit.</span><span class="sxs-lookup"><span data-stu-id="c1ba0-110">Click Journal control.</span></span>
4. <span data-ttu-id="c1ba0-111">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="c1ba0-111">Click Add.</span></span>
5. <span data-ttu-id="c1ba0-112">Í reitnum Fyrirtækjalyklar skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="c1ba0-112">In the Company accounts field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="c1ba0-113">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="c1ba0-113">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="c1ba0-114">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="c1ba0-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="c1ba0-115">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="c1ba0-115">Click Add.</span></span>
9. <span data-ttu-id="c1ba0-116">Í reitnum Bókhaldsskipulag skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="c1ba0-116">In the Account structure field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="c1ba0-117">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="c1ba0-117">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="c1ba0-118">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="c1ba0-118">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="c1ba0-119">Í reitnum Hluti skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="c1ba0-119">In the Segment field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="c1ba0-120">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="c1ba0-120">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="c1ba0-121">Í reitnum Frá virði skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="c1ba0-121">In the From value field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="c1ba0-122">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="c1ba0-122">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="c1ba0-123">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="c1ba0-123">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="c1ba0-124">Í reitnum Til virðis skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="c1ba0-124">In the To value field, click the drop-down button to open the lookup.</span></span>
18. <span data-ttu-id="c1ba0-125">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="c1ba0-125">In the list, find and select the desired record.</span></span>
19. <span data-ttu-id="c1ba0-126">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="c1ba0-126">In the list, click the link in the selected row.</span></span>

## <a name="set-up-posting-restrictions"></a><span data-ttu-id="c1ba0-127">Setja upp bókunartakmarkanir</span><span class="sxs-lookup"><span data-stu-id="c1ba0-127">Set up posting restrictions</span></span>
1. <span data-ttu-id="c1ba0-128">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="c1ba0-128">Close the page.</span></span>
2. <span data-ttu-id="c1ba0-129">Smellt er á Bókunartakmarkanir.</span><span class="sxs-lookup"><span data-stu-id="c1ba0-129">Click Posting restrictions.</span></span>
3. <span data-ttu-id="c1ba0-130">Í Hvernig á að setja upp bókunartakmarkanir skal velja Eftir notendaflokkum.</span><span class="sxs-lookup"><span data-stu-id="c1ba0-130">In the How do you want to set up posting restrictions, select By user group.</span></span>
4. <span data-ttu-id="c1ba0-131">Í trénu skal kanna ‚flokkinn sem á að leyfa bókanir fyrir þetta heiti færslubókar‘.</span><span class="sxs-lookup"><span data-stu-id="c1ba0-131">In the tree, check 'the group that you want to allow posting for this journal name.'.</span></span>
5. <span data-ttu-id="c1ba0-132">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="c1ba0-132">Click OK.</span></span>


