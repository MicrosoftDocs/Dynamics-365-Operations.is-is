---
title: "Rauntölur bornar saman við fjárhagsáætlun - Power BI-efni"
description: "Þetta efnisatriði lýsir Power BI-efninu Rauntölur bornar saman við fjárhagsáætlun. Það lýsir einnig hvernig eigi að fara í skýrslur sem eru hafðar með í efnispakkanum og veitir upplýsingar um gagnalíkan og einingar sem voru notaðar til að búa til efnið."
author: ryansandness
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application user, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 6e64337f19600b18320550d91c134949c33af7b0
ms.openlocfilehash: 2a0ad5af4e4d7da09690331dc9d1a51d2e97a664
ms.contentlocale: is-is
ms.lasthandoff: 12/01/2017

---

# <a name="actual-vs-budget-power-bi-content"></a><span data-ttu-id="37c99-104">Rauntölur bornar saman við fjárhagsáætlun - Power BI-efni</span><span class="sxs-lookup"><span data-stu-id="37c99-104">Actual vs budget Power BI content</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="37c99-105">Þetta efnisatriði lýsir Microsoft Power BI-efninu **Rauntölur bornar saman við fjárhagsáætlun**.</span><span class="sxs-lookup"><span data-stu-id="37c99-105">This topic describes the **Actual vs budget** Microsoft Power BI content.</span></span> <span data-ttu-id="37c99-106">Það lýsir einnig hvernig eigi að fara í Power BI-skýrslur og veitir upplýsingar um gagnalíkan og einingar sem notaðar voru til að búa til efnið.</span><span class="sxs-lookup"><span data-stu-id="37c99-106">It explains how to access the Power BI reports, and provides information about the data model and entities that were used to build the content.</span></span> 

# <a name="overview"></a><span data-ttu-id="37c99-107">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="37c99-107">Overview</span></span>

<span data-ttu-id="37c99-108">Power BI-efnið **Rauntölur bornar saman við fjárhagsáætlun** var stofnað fyrir einstaklinga sem bera ábyrgð á því að fylgjast með rauntölum bornum saman við áætluð afköst í fyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="37c99-108">The **Actual vs budget** Power BI content was created for individuals who are responsible for monitoring actual versus budget performance in their organization.</span></span> <span data-ttu-id="37c99-109">Power BI-efnið **Rauntölur bornar saman við fjárhagsáætlun** gefur sýnileika í frávik í fjárhagsáætlun.</span><span class="sxs-lookup"><span data-stu-id="37c99-109">The **Actual vs budget** Power BI content provides visibility into your budget variances.</span></span> <span data-ttu-id="37c99-110">Hægt er að greina áætlun fyrir gildandi ár eftir tegund lykils, áætlunarkóða, aðallykli, lýsingu aðallykils eða fjárhagstímabili til að öðlast betri skilning á orsökum frávika.</span><span class="sxs-lookup"><span data-stu-id="37c99-110">You can analyze budget for the current year by account category, budget code, main account, main account descriptions, or fiscal period to get a better understanding of the cause of any variances.</span></span> 

# <a name="accessing-the-power-bi-content"></a><span data-ttu-id="37c99-111">Farið í Power BI-efni</span><span class="sxs-lookup"><span data-stu-id="37c99-111">Accessing the Power BI content</span></span>
<span data-ttu-id="37c99-112">Skýrslur úr **Raunverulegt samanb. v. áætlun** Power BI efni eru birtar á vinnusvæðunum **Fjárhagsáætlun og spár** og **CFO vinnusvæði**.</span><span class="sxs-lookup"><span data-stu-id="37c99-112">Reports from the **Actual vs budget** Power BI content are shown in the **Ledger budget and forecasts** and **CFO** workspaces.</span></span>

# <a name="reports-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="37c99-113">Skýrslur sem eru hafðir með í Power BI-efni</span><span class="sxs-lookup"><span data-stu-id="37c99-113">Reports that are included in the Power BI content</span></span>
<span data-ttu-id="37c99-114">Eftirfarandi tafla veitir upplýsingar um mælikvarða sem eru á hverri skýrslusíðu í Power BI-efninu **Rauntölur bornar saman við fjárhagsáætlun**.</span><span class="sxs-lookup"><span data-stu-id="37c99-114">The following table provides details about the metrics that are found on each report page in the **Actual vs budget** Power BI content.</span></span>

| <span data-ttu-id="37c99-115">Skýrsla</span><span class="sxs-lookup"><span data-stu-id="37c99-115">Report</span></span>                      | <span data-ttu-id="37c99-116">Einingar</span><span class="sxs-lookup"><span data-stu-id="37c99-116">Metrics</span></span> |
|-----------------------------|---------|
| <span data-ttu-id="37c99-117">Útgjöld - rauntölur bornar saman við áætlun</span><span class="sxs-lookup"><span data-stu-id="37c99-117">Expenses - Actual vs budget</span></span> | <ul><li><span data-ttu-id="37c99-118">Heildarkostnaður á þessu ári</span><span class="sxs-lookup"><span data-stu-id="37c99-118">Total expenses this year</span></span></li><li><span data-ttu-id="37c99-119">Áætlaður heildarkostnaður á þessu ári</span><span class="sxs-lookup"><span data-stu-id="37c99-119">Budget total expenses this year</span></span></li></ul> |
| <span data-ttu-id="37c99-120">Tekjur - Rauntölur bornar saman við áætlun</span><span class="sxs-lookup"><span data-stu-id="37c99-120">Revenue - Actual vs budget</span></span>  | <ul><li><span data-ttu-id="37c99-121">Heildartekjur á þessu ári</span><span class="sxs-lookup"><span data-stu-id="37c99-121">Total revenue this year</span></span></li><li><span data-ttu-id="37c99-122">Áætlaðar heildartekjur á þessu ári</span><span class="sxs-lookup"><span data-stu-id="37c99-122">Budget total revenue this year</span></span></li><ul> |
| <span data-ttu-id="37c99-123">Útgjöld</span><span class="sxs-lookup"><span data-stu-id="37c99-123">Expense</span></span>                     | <ul><li><span data-ttu-id="37c99-124">Heildarkostnaður á þessu ári</span><span class="sxs-lookup"><span data-stu-id="37c99-124">Total expenses this year</span></span></li><li><span data-ttu-id="37c99-125">Kostnaðarmarkmið eftir áætlun</span><span class="sxs-lookup"><span data-stu-id="37c99-125">Goal for expenses based on budget</span></span> </li><ul> |
| <span data-ttu-id="37c99-126">Tekjur</span><span class="sxs-lookup"><span data-stu-id="37c99-126">Revenue</span></span>                     | <ul><li><span data-ttu-id="37c99-127">Heildartekjur á þessu ári</span><span class="sxs-lookup"><span data-stu-id="37c99-127">Total revenue this year</span></span></li><li><span data-ttu-id="37c99-128">Tekjumarkmið eftir áætlun</span><span class="sxs-lookup"><span data-stu-id="37c99-128">Goal for revenue based on budget</span></span> </li><ul> |
| <span data-ttu-id="37c99-129">Nettótekjur</span><span class="sxs-lookup"><span data-stu-id="37c99-129">Net income</span></span>                  | <ul><li><span data-ttu-id="37c99-130">Nettótekjur á þessu ári</span><span class="sxs-lookup"><span data-stu-id="37c99-130">Net income this year</span></span></li><li><span data-ttu-id="37c99-131">Nettó tekjumarkmið eftir áætlun</span><span class="sxs-lookup"><span data-stu-id="37c99-131">Goal for net income based on budget</span></span> </li><ul> |

## <a name="extending-the-power-bi-content"></a><span data-ttu-id="37c99-132">Stækkun efnis Power BI</span><span class="sxs-lookup"><span data-stu-id="37c99-132">Extending the Power BI content</span></span>
<span data-ttu-id="37c99-133">Með því að nota þjónustupakka sem eru í boði í Microsoft Dynamics Lifecycle Services (LCS) er hægt að veita fólki sem skráir sig ekki inn í Microsoft Dynamics 365 öflugri greiningu.</span><span class="sxs-lookup"><span data-stu-id="37c99-133">By using the content packs that are available in Microsoft Dynamics Lifecycle Services (LCS), you can provide great analytics to people who don't sign in to Microsoft Dynamics 365.</span></span> <span data-ttu-id="37c99-134">Hægt er að breyta þessum þjónustupökkum þannig að þeir innihaldi skýrslur eða myndræna framsetningu og afhenda svo leigjanda Power BI.com þjónustupakkana.</span><span class="sxs-lookup"><span data-stu-id="37c99-134">You can modify these content packs so that they include other reports or visuals, and then publish the content packs to your Power BI.com tenant for analysis.</span></span> 

<span data-ttu-id="37c99-135">Hægt er að finna Power BI-efnið **Rauntölur bornar saman við fjárhagsáætlun** í safninu Samnýttar eignir í LCS.</span><span class="sxs-lookup"><span data-stu-id="37c99-135">You can find the **Actual vs budget** Power BI content in the Shared assets library in LCS.</span></span> <span data-ttu-id="37c99-136">Upplýsingar um hvernig á að sækja efnið og innleiða það í fyrirtæki er að finna í [Power BI-efni í LCS frá Microsoft og viðskiptaaðilum þínum](power-bi-content-microsoft-partners.md).</span><span class="sxs-lookup"><span data-stu-id="37c99-136">For more information about how to download the content and implement it in your organization, see [Power BI content in LCS from Microsoft and your partners](power-bi-content-microsoft-partners.md).</span></span> <span data-ttu-id="37c99-137">Til að sjá sýningarmyndband um hvernig innleiða á Power BI-efnið, sjá [Power BI-efni frá Microsoft og samstarfsaðilum þínum í Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) í Office Mix.</span><span class="sxs-lookup"><span data-stu-id="37c99-137">To watch a demo that shows how to implement the Power BI content, see the [Power BI content from Microsoft and your partners in Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) Office Mix.</span></span>

# <a name="understanding-the-data-model-and-entities"></a><span data-ttu-id="37c99-138">Skilja gagnalíkan og einingar</span><span class="sxs-lookup"><span data-stu-id="37c99-138">Understanding the data model and entities</span></span>

| <span data-ttu-id="37c99-139">Eining</span><span class="sxs-lookup"><span data-stu-id="37c99-139">Entity</span></span>                    | <span data-ttu-id="37c99-140">Innihald</span><span class="sxs-lookup"><span data-stu-id="37c99-140">Contents</span></span> |
|---------------------------|----------|
| <span data-ttu-id="37c99-141">Fjárhagsaðgerðir</span><span class="sxs-lookup"><span data-stu-id="37c99-141">General Ledger Activities</span></span> | <span data-ttu-id="37c99-142">Færsluupphæðir fyrir fjárhag</span><span class="sxs-lookup"><span data-stu-id="37c99-142">Transaction amounts for the general ledger</span></span> |
| <span data-ttu-id="37c99-143">Fjárhagsáætlunaraðgerðir</span><span class="sxs-lookup"><span data-stu-id="37c99-143">Budget Activities</span></span>         | <span data-ttu-id="37c99-144">Færsluupphæðir fyrir áætlunarskrá</span><span class="sxs-lookup"><span data-stu-id="37c99-144">Transaction amounts for the budget register</span></span> |
| <span data-ttu-id="37c99-145">Aðallyklar</span><span class="sxs-lookup"><span data-stu-id="37c99-145">Main Accounts</span></span>             | <span data-ttu-id="37c99-146">Aðallyklar til að sía skýrslur eftir</span><span class="sxs-lookup"><span data-stu-id="37c99-146">Main accounts to filter reports by</span></span> |
| <span data-ttu-id="37c99-147">Fjárhagsdagatöl</span><span class="sxs-lookup"><span data-stu-id="37c99-147">Fiscal Calendars</span></span>          | <span data-ttu-id="37c99-148">Fjárhagsdagatöl til að sía skýrslur eftir</span><span class="sxs-lookup"><span data-stu-id="37c99-148">Fiscal calendars to filter reports by</span></span> |
| <span data-ttu-id="37c99-149">Fjárhagur</span><span class="sxs-lookup"><span data-stu-id="37c99-149">Ledgers</span></span>                   | <span data-ttu-id="37c99-150">Fjárhagur sem hægt er að nota til að sía skýrslu eftir núverandi fjárhag</span><span class="sxs-lookup"><span data-stu-id="37c99-150">Ledgers that can be used to filter the report to the current ledger</span></span> |
| <span data-ttu-id="37c99-151">Fjárhagsáætlunarkóðar</span><span class="sxs-lookup"><span data-stu-id="37c99-151">Budget Codes</span></span>              | <span data-ttu-id="37c99-152">Fjárhagsáætlunarkóðar til að sía skýrslur eftir</span><span class="sxs-lookup"><span data-stu-id="37c99-152">Budget codes to filter reports by</span></span> |
| <span data-ttu-id="37c99-153">Lögaðilar</span><span class="sxs-lookup"><span data-stu-id="37c99-153">Legal Entities</span></span>            | <span data-ttu-id="37c99-154">Lögaðilar sem hægt er að nota til að sía skýrslur eftir núverandi lögaðila</span><span class="sxs-lookup"><span data-stu-id="37c99-154">Legal entities that can be used to filter the report to the current legal entity</span></span> |

