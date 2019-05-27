---
title: Skilgreina samnýtingu fjárhagslegra gagna milli fyrirtækja
description: Þessi verklýsing sýnir hvernig á að skilgreina virkja, villuleita og leysa úr árekstrum við samnýtingu gagna á milli fyrirtækja.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DataManagementWorkspace, DMFQuickImportExportRnr, DMFExecutionHistoryWorkspace, DMFExecutionHistorySummary, DMFExecutionHistoryEntities,  SysDataSharingConfiguration, SysDataSharingDiscrepencies
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 784a925fa06148cad780b494c88b9a7af1809c9d
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1551031"
---
# <a name="configure-financial-cross-company-data-sharing"></a><span data-ttu-id="45678-103">Skilgreina samnýtingu fjárhagslegra gagna milli fyrirtækja</span><span class="sxs-lookup"><span data-stu-id="45678-103">Configure financial cross-company data sharing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="45678-104">Þessi verklýsing sýnir hvernig á að skilgreina virkja, villuleita og leysa úr árekstrum við samnýtingu gagna á milli fyrirtækja.</span><span class="sxs-lookup"><span data-stu-id="45678-104">This procedure shows how to configure, enable, validate, and resolve conflicts when sharing data between companies.</span></span> <span data-ttu-id="45678-105">Það notar USMF fyrirtæki og samnýtingarsniðmát fjárhagsgagna.</span><span class="sxs-lookup"><span data-stu-id="45678-105">It uses the USMF company and the Financial data sharing template.</span></span>



<span data-ttu-id="45678-106">Þessi leiðarvísir fyrir verk krefst AX útgáfu 7.1 eða nýrri.</span><span class="sxs-lookup"><span data-stu-id="45678-106">This task guide requires Dynamics AX platform 7.1 or later.</span></span>

1. <span data-ttu-id="45678-107">Farið í Kerfisstjórnun > Vinnusvæði > Gagnastjórnun.</span><span class="sxs-lookup"><span data-stu-id="45678-107">Go to System administration > Workspaces > Data management.</span></span>
2. <span data-ttu-id="45678-108">Smelltu á Flytja inn.</span><span class="sxs-lookup"><span data-stu-id="45678-108">Click Import.</span></span>
3. <span data-ttu-id="45678-109">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="45678-109">In the Name field, type a value.</span></span>
4. <span data-ttu-id="45678-110">Í reitnum snið upprunagagna skal slá velja gerð pakka,</span><span class="sxs-lookup"><span data-stu-id="45678-110">In the Source data format field, select the Package type.</span></span>
    * <span data-ttu-id="45678-111">Smelltu á Senda inn.</span><span class="sxs-lookup"><span data-stu-id="45678-111">Click Upload.</span></span> <span data-ttu-id="45678-112">Fara í staðsetningu pakkaskrár fyrir samnýtingarsniðmát fjárhagsgagna og veljið þá skrá.</span><span class="sxs-lookup"><span data-stu-id="45678-112">Navigate to the location of the Financial data sharing template package file and select that file.</span></span>  
5. <span data-ttu-id="45678-113">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="45678-113">Click Save.</span></span>
6. <span data-ttu-id="45678-114">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="45678-114">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="45678-115">Velja samnýtingarregla gagna sem verið var að stofna.</span><span class="sxs-lookup"><span data-stu-id="45678-115">Select the data sharing policy that was just created.</span></span>  
7. <span data-ttu-id="45678-116">Smelltu á Flytja inn.</span><span class="sxs-lookup"><span data-stu-id="45678-116">Click Import.</span></span>
8. <span data-ttu-id="45678-117">Smellið á „Loka“.</span><span class="sxs-lookup"><span data-stu-id="45678-117">Click Close.</span></span>
9. <span data-ttu-id="45678-118">Endurhlaðið síðuna.</span><span class="sxs-lookup"><span data-stu-id="45678-118">Refresh the page.</span></span>
10. <span data-ttu-id="45678-119">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="45678-119">Close the page.</span></span>
11. <span data-ttu-id="45678-120">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="45678-120">Close the page.</span></span>
12. <span data-ttu-id="45678-121">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="45678-121">Close the page.</span></span>
13. <span data-ttu-id="45678-122">Farið í kerfisstjórnun > Uppsetningu > Skilgreina samnýtingu gagna á milli fyrirtækja.</span><span class="sxs-lookup"><span data-stu-id="45678-122">Go to System administration > Setup > Configure cross-company data sharing.</span></span>
14. <span data-ttu-id="45678-123">Á listanum finna og velja vöru greiðsludaga.</span><span class="sxs-lookup"><span data-stu-id="45678-123">In the list, find and select Payment days.</span></span>
15. <span data-ttu-id="45678-124">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="45678-124">Click Add.</span></span>
16. <span data-ttu-id="45678-125">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="45678-125">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="45678-126">Í reitinn fyrirtæki skal slá inn „USSI“.</span><span class="sxs-lookup"><span data-stu-id="45678-126">In the Company field, type 'USSI'.</span></span>
18. <span data-ttu-id="45678-127">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="45678-127">Click Add.</span></span>
19. <span data-ttu-id="45678-128">Í reitinn fyrirtæki skal slá inn „USMF“.</span><span class="sxs-lookup"><span data-stu-id="45678-128">In the Company field, type 'USMF'.</span></span>
20. <span data-ttu-id="45678-129">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="45678-129">Click Save.</span></span>
21. <span data-ttu-id="45678-130">Smella á Virkja.</span><span class="sxs-lookup"><span data-stu-id="45678-130">Click Enable.</span></span>
22. <span data-ttu-id="45678-131">Smella á Já.</span><span class="sxs-lookup"><span data-stu-id="45678-131">Click Yes.</span></span>
23. <span data-ttu-id="45678-132">Smella á Finna vandamál í samnýtingu</span><span class="sxs-lookup"><span data-stu-id="45678-132">Click Find sharing issues.</span></span>
24. <span data-ttu-id="45678-133">Smella á Já.</span><span class="sxs-lookup"><span data-stu-id="45678-133">Click Yes.</span></span>
25. <span data-ttu-id="45678-134">Smellið á Uppfæra gildi svæðisins.</span><span class="sxs-lookup"><span data-stu-id="45678-134">Click Update field value.</span></span>
26. <span data-ttu-id="45678-135">Smellið á Nota gildi frá fyrirtæki 1.</span><span class="sxs-lookup"><span data-stu-id="45678-135">Click Use value from company 1.</span></span>
27. <span data-ttu-id="45678-136">Endurhlaðið síðuna.</span><span class="sxs-lookup"><span data-stu-id="45678-136">Refresh the page.</span></span>
28. <span data-ttu-id="45678-137">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="45678-137">Close the page.</span></span>

