---
title: Stofna ítarlegar reglur fyrir færslubækur
description: Þetta ferli fer í gegnum hvernig stofnaðar eru ítarlegar reglur fyrir færslubækur.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalControl, CompanyLookup, LedgerJournalPostControl
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e3fc764a6fa92a050084ae610a11acac46995d2a
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "326171"
---
# <a name="create-advanced-rules-for-journals"></a><span data-ttu-id="e3ca6-103">Stofna ítarlegar reglur fyrir færslubækur</span><span class="sxs-lookup"><span data-stu-id="e3ca6-103">Create advanced rules for journals</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e3ca6-104">Þetta ferli fer í gegnum hvernig stofnaðar eru ítarlegar reglur fyrir færslubækur.</span><span class="sxs-lookup"><span data-stu-id="e3ca6-104">This procedure steps through creating advanced rules for journals.</span></span> <span data-ttu-id="e3ca6-105">Þar á meðal uppsetningu færslubókareftirlits og bókunartakmarkana notanda.</span><span class="sxs-lookup"><span data-stu-id="e3ca6-105">This includes setting up journal control and user posting restrictions.</span></span> <span data-ttu-id="e3ca6-106">Þessi aðferð notar sýnifyrirtækið USMF.</span><span class="sxs-lookup"><span data-stu-id="e3ca6-106">This procedure uses the USMF demo data company.</span></span>


## <a name="set-up-journal-control"></a><span data-ttu-id="e3ca6-107">Setja upp færslubókaeftirlit</span><span class="sxs-lookup"><span data-stu-id="e3ca6-107">Set up journal control</span></span>
1. <span data-ttu-id="e3ca6-108">Fara í Fjárhag > Færslubókaruppsetning > Heiti færslubókar.</span><span class="sxs-lookup"><span data-stu-id="e3ca6-108">Go to General ledger > Journal setup > Journal names.</span></span>
2. <span data-ttu-id="e3ca6-109">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="e3ca6-109">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="e3ca6-110">Smellt er á færslubókareftirlit.</span><span class="sxs-lookup"><span data-stu-id="e3ca6-110">Click Journal control.</span></span>
4. <span data-ttu-id="e3ca6-111">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="e3ca6-111">Click Add.</span></span>
5. <span data-ttu-id="e3ca6-112">Í reitnum Fyrirtækjalyklar skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="e3ca6-112">In the Company accounts field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="e3ca6-113">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="e3ca6-113">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="e3ca6-114">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="e3ca6-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="e3ca6-115">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="e3ca6-115">Click Add.</span></span>
9. <span data-ttu-id="e3ca6-116">Í reitnum Bókhaldsskipulag skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="e3ca6-116">In the Account structure field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="e3ca6-117">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="e3ca6-117">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="e3ca6-118">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="e3ca6-118">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="e3ca6-119">Í reitnum Hluti skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="e3ca6-119">In the Segment field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="e3ca6-120">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="e3ca6-120">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="e3ca6-121">Í reitnum Frá virði skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="e3ca6-121">In the From value field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="e3ca6-122">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="e3ca6-122">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="e3ca6-123">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="e3ca6-123">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="e3ca6-124">Í reitnum Til virðis skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="e3ca6-124">In the To value field, click the drop-down button to open the lookup.</span></span>
18. <span data-ttu-id="e3ca6-125">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="e3ca6-125">In the list, find and select the desired record.</span></span>
19. <span data-ttu-id="e3ca6-126">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="e3ca6-126">In the list, click the link in the selected row.</span></span>

## <a name="set-up-posting-restrictions"></a><span data-ttu-id="e3ca6-127">Setja upp bókunartakmarkanir</span><span class="sxs-lookup"><span data-stu-id="e3ca6-127">Set up posting restrictions</span></span>
1. <span data-ttu-id="e3ca6-128">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="e3ca6-128">Close the page.</span></span>
2. <span data-ttu-id="e3ca6-129">Smellt er á Bókunartakmarkanir.</span><span class="sxs-lookup"><span data-stu-id="e3ca6-129">Click Posting restrictions.</span></span>
3. <span data-ttu-id="e3ca6-130">Í Hvernig á að setja upp bókunartakmarkanir skal velja Eftir notendaflokkum.</span><span class="sxs-lookup"><span data-stu-id="e3ca6-130">In the How do you want to set up posting restrictions, select By user group.</span></span>
4. <span data-ttu-id="e3ca6-131">Í trénu skal kanna ‚flokkinn sem á að leyfa bókanir fyrir þetta heiti færslubókar‘.</span><span class="sxs-lookup"><span data-stu-id="e3ca6-131">In the tree, check 'the group that you want to allow posting for this journal name.'.</span></span>
5. <span data-ttu-id="e3ca6-132">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="e3ca6-132">Click OK.</span></span>

