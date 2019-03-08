---
title: Skilgreina reikningagerð fyrir verk innan samstæðu
description: Þessi verklýsing sýnir hvernig á að setja upp reikningsfærslu verkefnis á milli tveggja fyrirtækja innan fyrirtækis.
author: KimANelson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, InterCompanyTradingRelationSetupVendor, SysDataAreaSelectLookup, ProjParameters, ProjPosting, ProjTransferPrice
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2fe06978d3a1c41a1133a568cca61df05b49d235
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "352759"
---
# <a name="configure-intercompany-project-invoicing"></a><span data-ttu-id="68585-103">Skilgreina reikningagerð fyrir verk innan samstæðu</span><span class="sxs-lookup"><span data-stu-id="68585-103">Configure intercompany project invoicing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="68585-104">Þessi verklýsing sýnir hvernig á að setja upp reikningsfærslu verkefnis á milli tveggja fyrirtækja innan fyrirtækis.</span><span class="sxs-lookup"><span data-stu-id="68585-104">This procedure shows how to set up project invoicing between two companies in your organization.</span></span> <span data-ttu-id="68585-105">Þetta verkefni notar USSI-gagnasafn.</span><span class="sxs-lookup"><span data-stu-id="68585-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="68585-106">Farið í Viðskiptaskuldir > Lánardrottnar > Allir lánardrottnar.</span><span class="sxs-lookup"><span data-stu-id="68585-106">Go to Accounts payable > Vendors > All vendors.</span></span>
2. <span data-ttu-id="68585-107">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="68585-107">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="68585-108">Í aðgerðasvæðinu er smellt á Almennt.</span><span class="sxs-lookup"><span data-stu-id="68585-108">On the Action Pane, click General.</span></span>
4. <span data-ttu-id="68585-109">Smellt er á Innan samstæðu.</span><span class="sxs-lookup"><span data-stu-id="68585-109">Click Intercompany.</span></span>
5. <span data-ttu-id="68585-110">Stillið Virkt á Já til að virkja verslun innan samstæðu.</span><span class="sxs-lookup"><span data-stu-id="68585-110">Set Active to Yes to enable intercompany trading.</span></span>
6. <span data-ttu-id="68585-111">Í svæði Fyrirtæki viðskiptavinar skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="68585-111">In the Customer company field, enter or select a value.</span></span>
7. <span data-ttu-id="68585-112">Sláið inn eða veljið gildi í svæði Reikningurinn minn.</span><span class="sxs-lookup"><span data-stu-id="68585-112">In the My account field, enter or select a value.</span></span>
8. <span data-ttu-id="68585-113">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="68585-113">Click Save.</span></span>
9. <span data-ttu-id="68585-114">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="68585-114">Close the page.</span></span>
10. <span data-ttu-id="68585-115">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="68585-115">Close the page.</span></span>
11. <span data-ttu-id="68585-116">Farið á Verkefnastjórnun og bókhald > Uppsetning > Færibreytur verkefnastjórnunar og bókhalds.</span><span class="sxs-lookup"><span data-stu-id="68585-116">Go to Project management and accounting > Setup > Project management and accounting parameters.</span></span>
12. <span data-ttu-id="68585-117">Smellt er á flipann Innan samstæðu.</span><span class="sxs-lookup"><span data-stu-id="68585-117">Click the Intercompany tab.</span></span>
13. <span data-ttu-id="68585-118">Færið sleðann á Já til að virkja áætlunargerð og vinnukort fyrir tilföng innan samstæðu.</span><span class="sxs-lookup"><span data-stu-id="68585-118">Move the slider to Yes to enable intercompany resource scheduling and timesheets.</span></span>
14. <span data-ttu-id="68585-119">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="68585-119">In the list, mark the selected row.</span></span>
15. <span data-ttu-id="68585-120">Smellið á Nýtt.</span><span class="sxs-lookup"><span data-stu-id="68585-120">Click New.</span></span>
16. <span data-ttu-id="68585-121">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="68585-121">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="68585-122">Í svæði Lögaðili sem fær lánað skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="68585-122">In the Borrowing legal entity field, enter or select a value.</span></span>
18. <span data-ttu-id="68585-123">Veljið gátreitur Safna upp tekjum.</span><span class="sxs-lookup"><span data-stu-id="68585-123">Select the Accrue revenue check box.</span></span>
19. <span data-ttu-id="68585-124">Í svæði Sjálfgefinn vinnukortaflokkur skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="68585-124">In the Default timesheet category field, enter or select a value.</span></span>
20. <span data-ttu-id="68585-125">Í svæði Sjálfgefinn kostnaðarflokkur skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="68585-125">In the Default expense category field, enter or select a value.</span></span>
21. <span data-ttu-id="68585-126">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="68585-126">Click Save.</span></span>
22. <span data-ttu-id="68585-127">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="68585-127">Close the page.</span></span>
23. <span data-ttu-id="68585-128">Farið á Verkefnastjórnun og bókhald > Uppsetning > Bókun > Uppsetning fjárhagsbókunar.</span><span class="sxs-lookup"><span data-stu-id="68585-128">Go to Project management and accounting > Setup > Posting > Ledger posting setup.</span></span>
24. <span data-ttu-id="68585-129">Í svæði Fjárhagslyklagerðir er valinn valkostur.</span><span class="sxs-lookup"><span data-stu-id="68585-129">In the Ledger account types field, select an option.</span></span>
25. <span data-ttu-id="68585-130">Smellt er á Nýtt.</span><span class="sxs-lookup"><span data-stu-id="68585-130">Click New.</span></span>
26. <span data-ttu-id="68585-131">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="68585-131">In the list, mark the selected row.</span></span>
27. <span data-ttu-id="68585-132">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="68585-132">In the list, mark the selected row.</span></span>
28. <span data-ttu-id="68585-133">Í reitnum aðallykill skal tilgreina gildi sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="68585-133">In the Main account field, specify the desired values.</span></span>
29. <span data-ttu-id="68585-134">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="68585-134">Click Save.</span></span>
30. <span data-ttu-id="68585-135">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="68585-135">Close the page.</span></span>
31. <span data-ttu-id="68585-136">Smellt er á Verkefnastjórnun og bókhald > Uppsetning > Verð > Innanhússverð.</span><span class="sxs-lookup"><span data-stu-id="68585-136">Go to Project management and accounting > Setup > Prices > Transfer price.</span></span>
32. <span data-ttu-id="68585-137">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="68585-137">Click New.</span></span>
33. <span data-ttu-id="68585-138">Í reitnum Gildisdagsetning skal slá inn dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="68585-138">In the Effective date field, enter a date.</span></span>
34. <span data-ttu-id="68585-139">Í svæði Lögaðili sem fær lánað skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="68585-139">In the Borrowing legal entity field, enter or select a value.</span></span>
35. <span data-ttu-id="68585-140">Í svæði Flutningsverðslíkan er valinn valkostur.</span><span class="sxs-lookup"><span data-stu-id="68585-140">In the Transfer price model field, select an option.</span></span>
36. <span data-ttu-id="68585-141">Sláðu inn tölu í svæði Verðlagning.</span><span class="sxs-lookup"><span data-stu-id="68585-141">In the Pricing field, enter a number.</span></span>
37. <span data-ttu-id="68585-142">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="68585-142">Click Save.</span></span>

