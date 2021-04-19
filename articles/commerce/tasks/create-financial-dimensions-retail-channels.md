---
title: Stofna fjárhagsvíddir fyrir smásölurásir og skilgreina víddagildi í verslunum
description: Þetta ferli fer í gegnum hvernig á að stofna fjárhagsvíddir Commerce-rása með víddargildum og skref til að skilgreina gildi fjárhagsvídda á verslanir.
author: jashanno
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0212d3bd808b2a46fa30e8b2bdaa3c0b52ca0dd6
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5790933"
---
# <a name="create-financial-dimensions-for-retail-channels-and-configure-dimension-values-on-stores"></a><span data-ttu-id="7e4c3-103">Stofna fjárhagsvíddir fyrir smásölurásir og skilgreina víddagildi í verslunum</span><span class="sxs-lookup"><span data-stu-id="7e4c3-103">Create financial dimensions for retail channels and configure dimension values on stores</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7e4c3-104">Þetta ferli fer í gegnum hvernig á að stofna fjárhagsvíddir Commerce-rása með víddargildum og skref til að skilgreina gildi fjárhagsvídda á verslanir.</span><span class="sxs-lookup"><span data-stu-id="7e4c3-104">This procedure walks through creating a commerce channel financial dimension with dimension values and steps to configure financial dimension values on stores.</span></span> <span data-ttu-id="7e4c3-105">Efnið tekur ekki með önnur tengd skref, s.s. að stofna víddarsamstæður og lykilskipulag.</span><span class="sxs-lookup"><span data-stu-id="7e4c3-105">The topic does not include other related steps, such as creating dimension sets and account structures.</span></span> <span data-ttu-id="7e4c3-106">Þetta ferli notar sýnigögn fyrirtæki USRT.</span><span class="sxs-lookup"><span data-stu-id="7e4c3-106">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="7e4c3-107">Fara í fjárhag > Línurit yfir lykla > Víddir > Fjárhagsvíddir.</span><span class="sxs-lookup"><span data-stu-id="7e4c3-107">Go to General ledger > Chart of accounts > Dimensions > Financial dimensions.</span></span>
2. <span data-ttu-id="7e4c3-108">Smellið á Nýtt.</span><span class="sxs-lookup"><span data-stu-id="7e4c3-108">Click New.</span></span>
3. <span data-ttu-id="7e4c3-109">Veljið í svæðinu Nota gildi frá,veldu 'Commerce-rásir'.</span><span class="sxs-lookup"><span data-stu-id="7e4c3-109">In the Use values from field, select 'Commerce channels'.</span></span>
4. <span data-ttu-id="7e4c3-110">Í reitinn Heiti víddar skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="7e4c3-110">In the Dimension name field, type a value.</span></span>
5. <span data-ttu-id="7e4c3-111">Smellið á Virkja.</span><span class="sxs-lookup"><span data-stu-id="7e4c3-111">Click Activate.</span></span>
6. <span data-ttu-id="7e4c3-112">Smellið á „Loka“.</span><span class="sxs-lookup"><span data-stu-id="7e4c3-112">Click Close.</span></span>
7. <span data-ttu-id="7e4c3-113">Smellið á Virkja.</span><span class="sxs-lookup"><span data-stu-id="7e4c3-113">Click Activate.</span></span>
8. <span data-ttu-id="7e4c3-114">Smellt er á víddargildi.</span><span class="sxs-lookup"><span data-stu-id="7e4c3-114">Click Dimension values.</span></span>
9. <span data-ttu-id="7e4c3-115">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="7e4c3-115">Close the page.</span></span>
10. <span data-ttu-id="7e4c3-116">Smelltu á Vista.</span><span class="sxs-lookup"><span data-stu-id="7e4c3-116">Click Save.</span></span>
11. <span data-ttu-id="7e4c3-117">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="7e4c3-117">Close the page.</span></span>
12. <span data-ttu-id="7e4c3-118">Fara í Retail og Commerce > Rásir > Verslanir > Allar verslanir.</span><span class="sxs-lookup"><span data-stu-id="7e4c3-118">Go to Retail and Commerce > Channels > Stores > All stores.</span></span>
13. <span data-ttu-id="7e4c3-119">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="7e4c3-119">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="7e4c3-120">Víxla útvíkkun á liðnum fjárhagsvídd.</span><span class="sxs-lookup"><span data-stu-id="7e4c3-120">Toggle the expansion of the Financial dimensions section.</span></span>
15. <span data-ttu-id="7e4c3-121">Smella á Breyta.</span><span class="sxs-lookup"><span data-stu-id="7e4c3-121">Click Edit.</span></span>
16. <span data-ttu-id="7e4c3-122">Í reitnum Commerce-rás skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="7e4c3-122">In the Commerce channel field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="7e4c3-123">Á listanum, Finna og velja víddargildi fyrir verslunina sem verið er að uppfæra.</span><span class="sxs-lookup"><span data-stu-id="7e4c3-123">In the list, find and select the dimension value for the store being updated.</span></span>
18. <span data-ttu-id="7e4c3-124">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="7e4c3-124">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="7e4c3-125">Í reitnum CostCenter skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="7e4c3-125">In the CostCenter field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="7e4c3-126">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="7e4c3-126">In the list, find and select the desired record.</span></span>
21. <span data-ttu-id="7e4c3-127">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="7e4c3-127">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="7e4c3-128">Í reitnum Deild skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="7e4c3-128">In the Department field, click the drop-down button to open the lookup.</span></span>
23. <span data-ttu-id="7e4c3-129">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="7e4c3-129">In the list, find and select the desired record.</span></span>
24. <span data-ttu-id="7e4c3-130">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="7e4c3-130">In the list, click the link in the selected row.</span></span>
25. <span data-ttu-id="7e4c3-131">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="7e4c3-131">Click Save.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]