---
title: Skilgreina samnýtingu fjárhagslegra gagna milli fyrirtækja
description: Þessi verklýsing sýnir hvernig á að skilgreina virkja, villuleita og leysa úr árekstrum við samnýtingu gagna á milli fyrirtækja.
author: aprilolson
manager: AnnBe
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DataManagementWorkspace, DMFQuickImportExportRnr, DMFExecutionHistoryWorkspace, DMFExecutionHistorySummary, DMFExecutionHistoryEntities,  SysDataSharingConfiguration, SysDataSharingDiscrepencies
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 167f43224591462a4db42d041487ff8f66b02cd9
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561075"
---
# <a name="configure-financial-cross-company-data-sharing"></a><span data-ttu-id="55e60-103">Skilgreina samnýtingu fjárhagslegra gagna milli fyrirtækja</span><span class="sxs-lookup"><span data-stu-id="55e60-103">Configure financial cross-company data sharing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="55e60-104">Þessi verklýsing sýnir hvernig á að skilgreina virkja, villuleita og leysa úr árekstrum við samnýtingu gagna á milli fyrirtækja.</span><span class="sxs-lookup"><span data-stu-id="55e60-104">This procedure shows how to configure, enable, validate, and resolve conflicts when sharing data between companies.</span></span> <span data-ttu-id="55e60-105">Það notar USMF fyrirtæki og samnýtingarsniðmát fjárhagsgagna.</span><span class="sxs-lookup"><span data-stu-id="55e60-105">It uses the USMF company and the Financial data sharing template.</span></span>

<span data-ttu-id="55e60-106">Þessi leiðarvísir fyrir verk krefst AX útgáfu 7.1 eða nýrri.</span><span class="sxs-lookup"><span data-stu-id="55e60-106">This task guide requires Dynamics AX platform 7.1 or later.</span></span>

1. <span data-ttu-id="55e60-107">Farðu í **Skoðunarrúðu > Kerfiseiningar > Kerfisstjórnun > Vinnusvæði > Gagnastýring**.</span><span class="sxs-lookup"><span data-stu-id="55e60-107">Go to **Navigation pane > Modules > System administration > Workspaces > Data management**.</span></span>
2. <span data-ttu-id="55e60-108">Smelltu á **Flytja inn**.</span><span class="sxs-lookup"><span data-stu-id="55e60-108">Click **Import**.</span></span>
3. <span data-ttu-id="55e60-109">Í reitinn **Heiti** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="55e60-109">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="55e60-110">Í reitnum **Snið upprunagagna** velurðu gerðina „Pakki“.</span><span class="sxs-lookup"><span data-stu-id="55e60-110">In the **Source data format** field, select the 'Package' type.</span></span> <span data-ttu-id="55e60-111">Smelltu á **Senda inn**.</span><span class="sxs-lookup"><span data-stu-id="55e60-111">Click **Upload**.</span></span> <span data-ttu-id="55e60-112">Fara í staðsetningu pakkaskrár fyrir samnýtingarsniðmát fjárhagsgagna og veljið þá skrá.</span><span class="sxs-lookup"><span data-stu-id="55e60-112">Navigate to the location of the Financial data sharing template package file and select that file.</span></span>
5. <span data-ttu-id="55e60-113">Smellt er á **Vista**.</span><span class="sxs-lookup"><span data-stu-id="55e60-113">Click **Save**.</span></span>
6. <span data-ttu-id="55e60-114">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="55e60-114">In the list, mark the selected row.</span></span> <span data-ttu-id="55e60-115">Velja samnýtingarregla gagna sem verið var að stofna.</span><span class="sxs-lookup"><span data-stu-id="55e60-115">Select the data sharing policy that was just created.</span></span>  
7. <span data-ttu-id="55e60-116">Smelltu á **Flytja inn**.</span><span class="sxs-lookup"><span data-stu-id="55e60-116">Click **Import**.</span></span>
8. <span data-ttu-id="55e60-117">Smellið á **Loka**.</span><span class="sxs-lookup"><span data-stu-id="55e60-117">Click **Close**.</span></span>
9. <span data-ttu-id="55e60-118">Endurhlaðið síðuna.</span><span class="sxs-lookup"><span data-stu-id="55e60-118">Refresh the page.</span></span>
10. <span data-ttu-id="55e60-119">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="55e60-119">Close the page.</span></span>
11. <span data-ttu-id="55e60-120">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="55e60-120">Close the page.</span></span>
12. <span data-ttu-id="55e60-121">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="55e60-121">Close the page.</span></span>
13. <span data-ttu-id="55e60-122">Farið í **Skoðunarrúðu > Kerfiseiningar > Kerfisstjórnun > Uppsetning > Skilgreina samnýtingu gagna á milli fyrirtækja**.</span><span class="sxs-lookup"><span data-stu-id="55e60-122">Go to **Navigation pane > Modules > System administration > Setup > Configure cross-company data sharing**.</span></span>
14. <span data-ttu-id="55e60-123">Á listanum skaltu finna og velja **Greiðsludaga**.</span><span class="sxs-lookup"><span data-stu-id="55e60-123">In the list, find and select **Payment days**.</span></span>
15. <span data-ttu-id="55e60-124">Smelltu á **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="55e60-124">Click **Add**.</span></span>
16. <span data-ttu-id="55e60-125">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="55e60-125">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="55e60-126">Í reitinn **Fyrirtæki** skal slá inn „USSI“.</span><span class="sxs-lookup"><span data-stu-id="55e60-126">In the **Company** field, type 'USSI'.</span></span>
18. <span data-ttu-id="55e60-127">Smelltu á **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="55e60-127">Click **Add**.</span></span>
19. <span data-ttu-id="55e60-128">Í reitinn **Fyrirtæki** skal slá inn „USMF“.</span><span class="sxs-lookup"><span data-stu-id="55e60-128">In the **Company** field, type 'USMF'.</span></span>
20. <span data-ttu-id="55e60-129">Smellt er á **Vista**.</span><span class="sxs-lookup"><span data-stu-id="55e60-129">Click **Save**.</span></span>
21. <span data-ttu-id="55e60-130">Smelltu á **Virkja**.</span><span class="sxs-lookup"><span data-stu-id="55e60-130">Click **Enable**.</span></span>
22. <span data-ttu-id="55e60-131">Smellið á **Já**.</span><span class="sxs-lookup"><span data-stu-id="55e60-131">Click **Yes**.</span></span>
23. <span data-ttu-id="55e60-132">Smelltu á **Finna vandamál í samnýtingu**.</span><span class="sxs-lookup"><span data-stu-id="55e60-132">Click **Find sharing issues**.</span></span>
24. <span data-ttu-id="55e60-133">Smellið á **Já**.</span><span class="sxs-lookup"><span data-stu-id="55e60-133">Click **Yes**.</span></span>
25. <span data-ttu-id="55e60-134">Smellið á **Uppfæra reitagildi**.</span><span class="sxs-lookup"><span data-stu-id="55e60-134">Click **Update field value**.</span></span>
26. <span data-ttu-id="55e60-135">Smelltu á **Nota gildi frá fyrirtæki 1**.</span><span class="sxs-lookup"><span data-stu-id="55e60-135">Click **Use value from company 1**.</span></span>
27. <span data-ttu-id="55e60-136">Endurhlaðið síðuna.</span><span class="sxs-lookup"><span data-stu-id="55e60-136">Refresh the page.</span></span>
28. <span data-ttu-id="55e60-137">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="55e60-137">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]