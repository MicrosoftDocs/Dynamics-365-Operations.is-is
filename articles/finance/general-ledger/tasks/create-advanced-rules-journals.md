---
title: Stofna ítarlegar reglur fyrir færslubækur
description: Þetta ferli fer í gegnum hvernig stofnaðar eru ítarlegar reglur fyrir færslubækur.
author: aprilolson
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalControl, CompanyLookup, LedgerJournalPostControl
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ea6ca24d27bb5b00bbe31060ce2f7e40bf2fb335
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145216"
---
# <a name="create-advanced-rules-for-journals"></a><span data-ttu-id="d97a5-103">Stofna ítarlegar reglur fyrir færslubækur</span><span class="sxs-lookup"><span data-stu-id="d97a5-103">Create advanced rules for journals</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d97a5-104">Þetta ferli fer í gegnum hvernig stofnaðar eru ítarlegar reglur fyrir færslubækur.</span><span class="sxs-lookup"><span data-stu-id="d97a5-104">This procedure steps through creating advanced rules for journals.</span></span> <span data-ttu-id="d97a5-105">Þar á meðal uppsetningu færslubókareftirlits og bókunartakmarkana notanda.</span><span class="sxs-lookup"><span data-stu-id="d97a5-105">This includes setting up journal control and user posting restrictions.</span></span> <span data-ttu-id="d97a5-106">Þessi aðferð notar sýnifyrirtækið USMF.</span><span class="sxs-lookup"><span data-stu-id="d97a5-106">This procedure uses the USMF demo data company.</span></span>


## <a name="set-up-journal-control"></a><span data-ttu-id="d97a5-107">Setja upp færslubókaeftirlit</span><span class="sxs-lookup"><span data-stu-id="d97a5-107">Set up journal control</span></span>
1. <span data-ttu-id="d97a5-108">Í **skoðunarrúðunni** ferðu í **Kerfiseiningar > Fjárhagur > Færslubókaruppsetning > Færslubókaheiti**.</span><span class="sxs-lookup"><span data-stu-id="d97a5-108">In the **Navigation pane**, go to **Modules > General ledger > Journal setup > Journal names**.</span></span>
2. <span data-ttu-id="d97a5-109">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="d97a5-109">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="d97a5-110">Í **aðgerðasvæðinu** er smellt á **Færslubókarstýring**.</span><span class="sxs-lookup"><span data-stu-id="d97a5-110">On the **Action pane**, click **Journal control**.</span></span>
4. <span data-ttu-id="d97a5-111">Á flýtiflipanum **Hvaða lyklagerðir er hægt að bóka** smellirðu á **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="d97a5-111">In the **Which account types can be posted** fastTab, click **Add**.</span></span>
5. <span data-ttu-id="d97a5-112">Í reitnum **Fyrirtækjalyklar** skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="d97a5-112">In the **Company accounts** field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="d97a5-113">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="d97a5-113">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="d97a5-114">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="d97a5-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="d97a5-115">Á flýtiflipanum **Hvaða hlutagildi eru gild fyrir þessa færslubók** smellirðu á **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="d97a5-115">In the **Which segment values are valid for this journal** fastTab, click **Add**.</span></span>
9. <span data-ttu-id="d97a5-116">Í reitnum **Lykilskipulag** skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="d97a5-116">In the **Account structure** field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="d97a5-117">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="d97a5-117">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="d97a5-118">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="d97a5-118">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="d97a5-119">Í reitnum **Hluti** skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="d97a5-119">In the **Segment** field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="d97a5-120">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="d97a5-120">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="d97a5-121">Í reitnum **Frá gildi** skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="d97a5-121">In the **From value** field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="d97a5-122">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="d97a5-122">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="d97a5-123">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="d97a5-123">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="d97a5-124">Í reitnum **Til gildis** skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="d97a5-124">In the **To value** field, click the drop-down button to open the lookup.</span></span>
18. <span data-ttu-id="d97a5-125">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="d97a5-125">In the list, find and select the desired record.</span></span>
19. <span data-ttu-id="d97a5-126">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="d97a5-126">In the list, click the link in the selected row.</span></span>

## <a name="set-up-posting-restrictions"></a><span data-ttu-id="d97a5-127">Setja upp bókunartakmarkanir</span><span class="sxs-lookup"><span data-stu-id="d97a5-127">Set up posting restrictions</span></span>
1. <span data-ttu-id="d97a5-128">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="d97a5-128">Close the page.</span></span>
2. <span data-ttu-id="d97a5-129">Smellt er á **Bókunartakmarkanir**.</span><span class="sxs-lookup"><span data-stu-id="d97a5-129">Click **Posting restrictions**.</span></span>
3. <span data-ttu-id="d97a5-130">Í reitnum **Hvernig á að setja upp bókunartakmarkanir** skal velja „Eftir notendaflokkum“.</span><span class="sxs-lookup"><span data-stu-id="d97a5-130">In the **How do you want to set up posting restrictions** field, select 'By user group'.</span></span>
4. <span data-ttu-id="d97a5-131">Í trénu skal kanna ‚flokkinn sem á að leyfa bókanir fyrir þetta heiti færslubókar‘.</span><span class="sxs-lookup"><span data-stu-id="d97a5-131">In the tree, check 'the group that you want to allow posting for this journal name.'.</span></span>
5. <span data-ttu-id="d97a5-132">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="d97a5-132">Click **OK**.</span></span>

