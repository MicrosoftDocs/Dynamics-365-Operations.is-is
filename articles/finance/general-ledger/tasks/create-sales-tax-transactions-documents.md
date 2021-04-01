---
title: Búa til VSK-færslur í skjölum
description: Virðisaukaskattur á skjölum er reiknaður með því að gefa Vsk-flokk og vsk-flokk Vöru á línur upprunaskjals.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, TaxTmpWorkTrans
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3cc70915902863d85aa75af7f4c03e5b83c7cb22
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5240811"
---
# <a name="create-sales-tax-transactions-on-documents"></a><span data-ttu-id="a7940-103">Búa til VSK-færslur í skjölum</span><span class="sxs-lookup"><span data-stu-id="a7940-103">Create sales tax transactions on documents</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a7940-104">Virðisaukaskattur á skjölum er reiknaður með því að gefa Vsk-flokk og vsk-flokk Vöru á línur upprunaskjals.</span><span class="sxs-lookup"><span data-stu-id="a7940-104">Sales tax on documents is calculated by providing a Sales tax group and an Item sales tax group on document lines.</span></span> <span data-ttu-id="a7940-105">Þær eru sjálfgefnar úr aðalgögnum en því má breyta handvirkt ef þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="a7940-105">These default from master data but can be changed manually if necessary.</span></span> <span data-ttu-id="a7940-106">Hægt er að athuga reiknaðan virðisaukaskatt á stigi línu og skjals.</span><span class="sxs-lookup"><span data-stu-id="a7940-106">The calculated sales tax can be checked on a line and document level.</span></span> <span data-ttu-id="a7940-107">Þetta verkefni notar USMF-sýnifyrirtækið.</span><span class="sxs-lookup"><span data-stu-id="a7940-107">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="a7940-108">Farið í Viðskiptakröfur > Pantanir > Allar sölupantanir.</span><span class="sxs-lookup"><span data-stu-id="a7940-108">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="a7940-109">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="a7940-109">Click New.</span></span>
3. <span data-ttu-id="a7940-110">Í reitnum Reikningur viðskiptavina skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="a7940-110">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="a7940-111">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="a7940-111">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="a7940-112">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="a7940-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="a7940-113">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="a7940-113">Click OK.</span></span>
7. <span data-ttu-id="a7940-114">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="a7940-114">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="a7940-115">Í reitnum Vörunúmer skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="a7940-115">In the Item number field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="a7940-116">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="a7940-116">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="a7940-117">Í reitnum Einingarverð skal slá inn tölu.</span><span class="sxs-lookup"><span data-stu-id="a7940-117">In the Unit price field, enter a number.</span></span>
11. <span data-ttu-id="a7940-118">Útvíkka eða draga saman hluta upplýsingar Línu.</span><span class="sxs-lookup"><span data-stu-id="a7940-118">Expand or collapse the Line details section.</span></span>
12. <span data-ttu-id="a7940-119">Smellið á hnappinn „Uppsetning“.</span><span class="sxs-lookup"><span data-stu-id="a7940-119">Click the Setup tab.</span></span>
13. <span data-ttu-id="a7940-120">Í reitnum VSK-flokkur vöru skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="a7940-120">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="a7940-121">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="a7940-121">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="a7940-122">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="a7940-122">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="a7940-123">Smelltu á Fjárhagur.</span><span class="sxs-lookup"><span data-stu-id="a7940-123">Click Financials.</span></span>
17. <span data-ttu-id="a7940-124">Smellt er á vsk.</span><span class="sxs-lookup"><span data-stu-id="a7940-124">Click Sales tax.</span></span>
18. <span data-ttu-id="a7940-125">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="a7940-125">Click OK.</span></span>
19. <span data-ttu-id="a7940-126">Smellið á „Bæta við línu“.</span><span class="sxs-lookup"><span data-stu-id="a7940-126">Click Add line.</span></span>
20. <span data-ttu-id="a7940-127">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="a7940-127">In the list, mark the selected row.</span></span>
21. <span data-ttu-id="a7940-128">Í reitnum Vörunúmer skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="a7940-128">In the Item number field, click the drop-down button to open the lookup.</span></span>
22. <span data-ttu-id="a7940-129">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="a7940-129">In the list, find and select the desired record.</span></span>
23. <span data-ttu-id="a7940-130">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="a7940-130">In the list, click the link in the selected row.</span></span>
24. <span data-ttu-id="a7940-131">Í reitnum Einingarverð skal slá inn tölu.</span><span class="sxs-lookup"><span data-stu-id="a7940-131">In the Unit price field, enter a number.</span></span>
25. <span data-ttu-id="a7940-132">Í reitnum VSK-flokkur vöru skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="a7940-132">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
26. <span data-ttu-id="a7940-133">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="a7940-133">In the list, find and select the desired record.</span></span>
27. <span data-ttu-id="a7940-134">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="a7940-134">In the list, click the link in the selected row.</span></span>
28. <span data-ttu-id="a7940-135">Í aðgerðasvæðinu er smellt á selja.</span><span class="sxs-lookup"><span data-stu-id="a7940-135">On the Action Pane, click Sell.</span></span>
29. <span data-ttu-id="a7940-136">Smellt er á vsk.</span><span class="sxs-lookup"><span data-stu-id="a7940-136">Click Sales tax.</span></span>
30. <span data-ttu-id="a7940-137">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="a7940-137">Click OK.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]