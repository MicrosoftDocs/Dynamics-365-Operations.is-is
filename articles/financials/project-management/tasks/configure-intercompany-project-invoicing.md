---
title: Skilgreina reikningagerð fyrir verk innan samstæðu
description: Þessi efni sýnir hvernig á að setja upp reikningsfærslu verkefnis á milli tveggja fyrirtækja innan fyrirtækis.
author: KimANelson
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, InterCompanyTradingRelationSetupVendor, SysDataAreaSelectLookup, ProjParameters, ProjPosting, ProjTransferPrice
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c89b17c09a4f145b5a4ca9cdd127b4e635447d4b
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867320"
---
# <a name="configure-intercompany-project-invoicing"></a><span data-ttu-id="a0b85-103">Skilgreina reikningagerð fyrir verk innan samstæðu</span><span class="sxs-lookup"><span data-stu-id="a0b85-103">Configure intercompany project invoicing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a0b85-104">Þessi efni sýnir hvernig á að setja upp reikningsfærslu verkefnis á milli tveggja fyrirtækja innan fyrirtækis.</span><span class="sxs-lookup"><span data-stu-id="a0b85-104">This topic shows how to set up project invoicing between two companies in your organization.</span></span> <span data-ttu-id="a0b85-105">Þetta verkefni notar USSI-gagnasafn.</span><span class="sxs-lookup"><span data-stu-id="a0b85-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="a0b85-106">Í skoðunarrúðunni ferðu í **Kerfiseiningar > Viðskiptaskuldir > Lánardrottnar > Allir lánardrottnar**.</span><span class="sxs-lookup"><span data-stu-id="a0b85-106">In the navigation pane, go to **Modules > Accounts payable > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="a0b85-107">Á listanum **Allir lánardrottnar** finnurðu og velur þá færslu sem þú óskar.</span><span class="sxs-lookup"><span data-stu-id="a0b85-107">In the **All vendors** list, find and select the desired record.</span></span>
3. <span data-ttu-id="a0b85-108">Í aðgerðasvæðinu velurðu **Almennt**.</span><span class="sxs-lookup"><span data-stu-id="a0b85-108">On the Action Pane, select **General**.</span></span>
4. <span data-ttu-id="a0b85-109">Veldu **Innan samstæðu**.</span><span class="sxs-lookup"><span data-stu-id="a0b85-109">Select **Intercompany**.</span></span>
5. <span data-ttu-id="a0b85-110">Stilltu **Virkt** á **Já** til að virkja viðskipti innan samstæðu.</span><span class="sxs-lookup"><span data-stu-id="a0b85-110">Set **Active** to **Yes** to enable intercompany trading.</span></span>
6. <span data-ttu-id="a0b85-111">Í reitnum **Fyrirtæki viðskiptavinar** skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="a0b85-111">In the **Customer company** field, enter or select a value.</span></span>
7. <span data-ttu-id="a0b85-112">Sláið inn eða veljið gildi í ritnum **Reikningurinn minn**.</span><span class="sxs-lookup"><span data-stu-id="a0b85-112">In the **My account** field, enter or select a value.</span></span>
8. <span data-ttu-id="a0b85-113">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="a0b85-113">Select **Save**.</span></span>
9. <span data-ttu-id="a0b85-114">Lokið síðunum til að fara aftur á heimasíðuna.</span><span class="sxs-lookup"><span data-stu-id="a0b85-114">Close the pages to return to the home page.</span></span>
10. <span data-ttu-id="a0b85-115">Í skoðunarrúðunni ferðu í **Kerfiseiningar > Verkefnastjórnun og bókhald > Uppsetning > Færibreytur verkefnastjórnunar og bókhalds**.</span><span class="sxs-lookup"><span data-stu-id="a0b85-115">In the navigation pane, go to **Modules > Project management and accounting > Setup > Project management and accounting parameters**.</span></span>
11. <span data-ttu-id="a0b85-116">Veldu flipann **Innan samstæðu**.</span><span class="sxs-lookup"><span data-stu-id="a0b85-116">Select the **Intercompany** tab.</span></span>
12. <span data-ttu-id="a0b85-117">Færið sleðann á **Já** til að virkja áætlunargerð og vinnukort fyrir tilföng innan samstæðu.</span><span class="sxs-lookup"><span data-stu-id="a0b85-117">Move the slider to **Yes** to enable intercompany resource scheduling and timesheets.</span></span>
13. <span data-ttu-id="a0b85-118">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="a0b85-118">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="a0b85-119">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="a0b85-119">Select **New**.</span></span>
15. <span data-ttu-id="a0b85-120">Í reitnum **Lögaðili sem fær lánað** skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="a0b85-120">In the **Borrowing legal entity** field, enter or select a value.</span></span>
16. <span data-ttu-id="a0b85-121">Veljið gátreitinn **Safna upp veltu**.</span><span class="sxs-lookup"><span data-stu-id="a0b85-121">Select the **Accrue revenue** check box.</span></span>
17. <span data-ttu-id="a0b85-122">Í reitinn **Sjálfgefinn vinnukortaflokkur** skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="a0b85-122">In the **Default timesheet category** field, enter or select a value.</span></span>
18. <span data-ttu-id="a0b85-123">Í reitinn **Sjálfgefinn kostnaðarflokkur** skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="a0b85-123">In the **Default expense category** field, enter or select a value.</span></span>
19. <span data-ttu-id="a0b85-124">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="a0b85-124">Select **Save**.</span></span>
20. <span data-ttu-id="a0b85-125">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="a0b85-125">Close the page.</span></span>
21. <span data-ttu-id="a0b85-126">Í skoðunarrúðunni ferðu í **Kerfiseiningar > Verkefnastjórnun og bókhald > Uppsetning > Bókun > Uppsetning fjárhagsbókunar**.</span><span class="sxs-lookup"><span data-stu-id="a0b85-126">In the navigation pane, go to **Modules > Project management and accounting > Setup > Posting > Ledger posting setup**.</span></span>
22. <span data-ttu-id="a0b85-127">Í reitnum **Fjárhagslyklagerðir** er valinn valkostur.</span><span class="sxs-lookup"><span data-stu-id="a0b85-127">In the **Ledger account types** field, select an option.</span></span>
23. <span data-ttu-id="a0b85-128">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="a0b85-128">Select **New**.</span></span>
24. <span data-ttu-id="a0b85-129">Í reitnum **Aðallykill** í nýrri línu skal skilgreina æskileg gildi.</span><span class="sxs-lookup"><span data-stu-id="a0b85-129">In the **Main account** field of the new row, specify the desired values.</span></span>
25. <span data-ttu-id="a0b85-130">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="a0b85-130">Select **Save**.</span></span>
26. <span data-ttu-id="a0b85-131">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="a0b85-131">Close the page.</span></span>
27. <span data-ttu-id="a0b85-132">Í skoðunarrúðunni ferðu í **Kerfiseiningar > Verkefnastjórnun og bókhald > Uppsetning > Verð > Flutningskostnaður**.</span><span class="sxs-lookup"><span data-stu-id="a0b85-132">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Transfer price**.</span></span>
28. <span data-ttu-id="a0b85-133">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="a0b85-133">Select **New**.</span></span>
29. <span data-ttu-id="a0b85-134">Í reitnum **Gildisdagsetning** skal slá inn dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="a0b85-134">In the **Effective date** field, enter a date.</span></span>
30. <span data-ttu-id="a0b85-135">Í reitnum **Lögaðili sem fær lánað** skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="a0b85-135">In the **Borrowing legal entity** field, enter or select a value.</span></span>
31. <span data-ttu-id="a0b85-136">Í reitnum **Flutningsverðslíkan** er valinn valkostur.</span><span class="sxs-lookup"><span data-stu-id="a0b85-136">In the **Transfer price model** field, select an option.</span></span>
32. <span data-ttu-id="a0b85-137">Sláðu inn tölu í retinn **Verðlagning**.</span><span class="sxs-lookup"><span data-stu-id="a0b85-137">In the **Pricing** field, enter a number.</span></span>
33. <span data-ttu-id="a0b85-138">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="a0b85-138">Select **Save**.</span></span>

