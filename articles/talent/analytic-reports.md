---
title: Notaðu greiningarskýrslur í Attract
description: Þetta efni lýsir greiningarskýrslum fyrir ráðningu á ferli í Microsoft Dynamics 365 Talent - Attract
author: fewatson
manager: AnnBe
ms.date: 04/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: fewatson
ms.search.validFrom: 2019-04-30
ms.dyn365.ops.version: Talent April 2019 update
ms.openlocfilehash: 081988e8b8cfe1e2ddb533247b678ba38a07f5f1
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092224"
---
# <a name="use-analytic-reports-in-attract"></a><span data-ttu-id="89dde-103">Notaðu greiningarskýrslur í Attract</span><span class="sxs-lookup"><span data-stu-id="89dde-103">Use analytic reports in Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="89dde-104">Greiningarskýrslur í Microsoft Dynamics 365 Talent: Attract veita tilbúna lausn fyrir innsýn í ráðningarferlin.</span><span class="sxs-lookup"><span data-stu-id="89dde-104">Analytic reports in Microsoft Dynamics 365 Talent: Attract provide an out-of-the-box (OOTB) solution for hiring process insights.</span></span> <span data-ttu-id="89dde-105">Tiltækar aðgerðir eru meðal annars:</span><span class="sxs-lookup"><span data-stu-id="89dde-105">Availabe features include:</span></span>

- <span data-ttu-id="89dde-106">**Starfsgreiningar** Smellið á flipann **Greiningar** innan starfs fyrir mæligildi umsækjenda starfs.</span><span class="sxs-lookup"><span data-stu-id="89dde-106">**Job analytics:** Click the **Analytics** tab within a job for metrics on the job's applicants.</span></span>
- <span data-ttu-id="89dde-107">**Greiningarmiðstöð** Smellið á **Greiningar** vinstra megin á yfirlitinu fyrir samantekin mæligildi allra starfa.</span><span class="sxs-lookup"><span data-stu-id="89dde-107">**Analytics hub:** Click **Analytics** on the left navigation for aggregated metrics across jobs.</span></span>
- <span data-ttu-id="89dde-108">**Notandamiðað öryggi** - Aðgangur að skýrslum er stjórnað af Attract [hlutverki](security-attract.md) og hlutverki þátttakanda í starfi.</span><span class="sxs-lookup"><span data-stu-id="89dde-108">**User-specific security:** Access to reports is controlled by Attract [role](security-attract.md) and job participant role.</span></span>
- <span data-ttu-id="89dde-109">**Krosssíun** Smellið á myndefni innan skýrslu til að skoða önnur síuð mæligildi valdra gagna.</span><span class="sxs-lookup"><span data-stu-id="89dde-109">**Cross-filtering:** Click visuals within a report to view other metrics filtered by selected data.</span></span>

>[!NOTE] 
>- <span data-ttu-id="89dde-110">Þessi eiginleiki er í [forútgáfu](access-preview-feature.md) sem stendur.</span><span class="sxs-lookup"><span data-stu-id="89dde-110">This feature is currently in [preview](access-preview-feature.md).</span></span> <span data-ttu-id="89dde-111">Til að reyna hana er nauðsynlegt að vera með [**Viðbót við alhliða ráðningar**](attract-comprehensive-hiring.md).</span><span class="sxs-lookup"><span data-stu-id="89dde-111">To try it, you must have the [**Comprehensive Hiring Add-On**](attract-comprehensive-hiring.md).</span></span>
>- <span data-ttu-id="89dde-112">Allar opinberar forskoðunarskýrslur birtast á ensku.</span><span class="sxs-lookup"><span data-stu-id="89dde-112">All public preview reports are displayed in English.</span></span>
>- <span data-ttu-id="89dde-113">Skýrslur endurhlaðast á 3 tíma fresti.</span><span class="sxs-lookup"><span data-stu-id="89dde-113">Reports refresh every 3 hours.</span></span> <span data-ttu-id="89dde-114">Tími síðustu endurhleðslu (í staðbundnu tímabelti) er að finna efst í skýrslunni.</span><span class="sxs-lookup"><span data-stu-id="89dde-114">The last refresh time (in the local timezone) is located at the top of the report.</span></span> <span data-ttu-id="89dde-115">Endurhleðslutímar eru ekki nákvæmir og eru breytilegir út af gagnamagni og tilfangahleðslu í þínu svæði.</span><span class="sxs-lookup"><span data-stu-id="89dde-115">Refresh times are an approximation and vary based on data volume and resource load in your region.</span></span>

## <a name="job-analytics"></a><span data-ttu-id="89dde-116">Greining starfs</span><span class="sxs-lookup"><span data-stu-id="89dde-116">Job Analytics</span></span>

<span data-ttu-id="89dde-117">Starfsgreiningaskýrslur eru skyndimynd af ráðningarferli fyrir starf.</span><span class="sxs-lookup"><span data-stu-id="89dde-117">Job Analytics reports are a snapshot of the hiring process for a job.</span></span>  <span data-ttu-id="89dde-118">Helstu mæligildi eru:</span><span class="sxs-lookup"><span data-stu-id="89dde-118">Key metrics include:</span></span>

- <span data-ttu-id="89dde-119">Virkir umsækjendur eftir stigi</span><span class="sxs-lookup"><span data-stu-id="89dde-119">Active applicants by stage</span></span>
- <span data-ttu-id="89dde-120">Uppruni umsækjanda</span><span class="sxs-lookup"><span data-stu-id="89dde-120">Applicant source</span></span>
- <span data-ttu-id="89dde-121">Gerð umsækjanda (innan eða utan fyrirtækis)</span><span class="sxs-lookup"><span data-stu-id="89dde-121">Applicant type (internal or external)</span></span>

## <a name="analytics-hub"></a><span data-ttu-id="89dde-122">Greiningarmiðstöð</span><span class="sxs-lookup"><span data-stu-id="89dde-122">Analytics Hub</span></span>

<span data-ttu-id="89dde-123">Skýrslur greiningarmiðstöðvar taka saman gögn frá öllum störfum til að bera kennsl á mynstur í ráðningarferlinu.</span><span class="sxs-lookup"><span data-stu-id="89dde-123">Analytics Hub reports aggregate data across jobs to surface trends in the hiring process.</span></span> <span data-ttu-id="89dde-124">Attract inniheldur tvær tilbúnar skýrslur: Sölukeðjuyfirlit og trektargreining.</span><span class="sxs-lookup"><span data-stu-id="89dde-124">Attract includes two OOTB reports: Pipeline Summary and Funnel Analysis.</span></span>

### <a name="pipeline-summary"></a><span data-ttu-id="89dde-125">Sölukeðjuyfirlit</span><span class="sxs-lookup"><span data-stu-id="89dde-125">Pipeline Summary</span></span>

<span data-ttu-id="89dde-126">Skýrsla sölukeðjuyfirlits safnar saman gögnum fyrir opin störf.</span><span class="sxs-lookup"><span data-stu-id="89dde-126">The Pipeline Summary report aggregates data for open jobs.</span></span> <span data-ttu-id="89dde-127">Helstu mæligildi eru:</span><span class="sxs-lookup"><span data-stu-id="89dde-127">Key metrics include:</span></span>

- <span data-ttu-id="89dde-128">Umsækjendur í öllum störfum eftir stigi</span><span class="sxs-lookup"><span data-stu-id="89dde-128">Applicants across all jobs by stage</span></span>
- <span data-ttu-id="89dde-129">Uppruni umsækjanda</span><span class="sxs-lookup"><span data-stu-id="89dde-129">Applicant source</span></span>
- <span data-ttu-id="89dde-130">Laus störf eftir starfsaldri</span><span class="sxs-lookup"><span data-stu-id="89dde-130">Open jobs by seniority level</span></span>

### <a name="funnel-analysis"></a><span data-ttu-id="89dde-131">Trektargreining</span><span class="sxs-lookup"><span data-stu-id="89dde-131">Funnel Analysis</span></span>

<span data-ttu-id="89dde-132">Skýrsla trektargreiningar safnar saman gögnum fyrir störf sem hafa verið lokuð sem útfyllt.</span><span class="sxs-lookup"><span data-stu-id="89dde-132">The Funnel Analysis report aggregates data for jobs that have been closed as filled.</span></span> <span data-ttu-id="89dde-133">Helstu mæligildi eru:</span><span class="sxs-lookup"><span data-stu-id="89dde-133">Key metrics include:</span></span>

- <span data-ttu-id="89dde-134">Tími fyrir ráðningu</span><span class="sxs-lookup"><span data-stu-id="89dde-134">Time to hire</span></span>
- <span data-ttu-id="89dde-135">Mælikvarðar breytinga (þegar bendli er haldið yfir)</span><span class="sxs-lookup"><span data-stu-id="89dde-135">Conversion metrics (on hover)</span></span>
- <span data-ttu-id="89dde-136">Tíðni tilboðssamþykktar</span><span class="sxs-lookup"><span data-stu-id="89dde-136">Offer acceptance rate</span></span>

<span data-ttu-id="89dde-137">Til athugunar: Skýrslugerð um nákvæmasta tíma til að ráða er mælt með því að þú notir [Tilboðsstjórnun](offer-setup.md), eiginleiki sem er í boði sem hluti af viðbót við alhliða ráðningar.</span><span class="sxs-lookup"><span data-stu-id="89dde-137">Note: For the most accurate time to hire reporting, it is recommended that you use [Offer management](offer-setup.md), a feature available as part of the Comprehensive Hiring Add-On.</span></span>

>[!TIP] 
><span data-ttu-id="89dde-138">Prófaðu að halda bendli yfir myndefni fyrir frekari upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="89dde-138">Try hovering over visuals for additional information.</span></span> <span data-ttu-id="89dde-139">Dæmi: Að halda bendli yfir myndefninu **Virkir umsækjendur** birtir meðalfjölda daga á stigi.</span><span class="sxs-lookup"><span data-stu-id="89dde-139">For example, hovering over **Active applicants** visuals will display the average days in stage.</span></span> <span data-ttu-id="89dde-140">Að greina þessar upplýsingar getur veitt mikilvæga innsýn í að draga úr tíma til að ráða og gert ráðningaraðilum kleift að einblína á leiðir til að draga úr tímanum sem fer í hvert stig.</span><span class="sxs-lookup"><span data-stu-id="89dde-140">Analyzing this information can provide insights critical to reducing time to hire and enable recruiters to focus on ways to reduce the time spent in each stage.</span></span>

## <a name="user-specific-security"></a><span data-ttu-id="89dde-141">Öryggi sem miðast við notanda</span><span class="sxs-lookup"><span data-stu-id="89dde-141">User-specific security</span></span>

<span data-ttu-id="89dde-142">Attract-skýrslur eru aðgengilegar fyrir stjórnanda, Lesa allt, Ráðningaraðila og Ráðningarstjóra [hlutverk](security-attract.md).</span><span class="sxs-lookup"><span data-stu-id="89dde-142">Attract reports are accessible for Admin, Read All, Recruiter, and Hiring Manager [roles](security-attract.md).</span></span> <span data-ttu-id="89dde-143">Óúthlutaðir notendur hafa ekki aðgang að síðum greiningarskýrslunnar (Starfsgreiningar eða Starfsgreiningarmiðstöðvar).</span><span class="sxs-lookup"><span data-stu-id="89dde-143">Unassigned users do not have access to either of the analytic report pages (Job Analytics or Analytics Hub).</span></span>

<span data-ttu-id="89dde-144">Skýrslur starfsgreiningar sýna gögn fyrir valið starf.</span><span class="sxs-lookup"><span data-stu-id="89dde-144">Job Analytics reports display data for the selected job.</span></span> <span data-ttu-id="89dde-145">Skýrslur starfsgreiningarmiðstöðvar safna saman gögnum frá öllum störfum sem notandi getur skoðað.</span><span class="sxs-lookup"><span data-stu-id="89dde-145">Analytics Hub reports aggregate data across all jobs a user can view.</span></span> <span data-ttu-id="89dde-146">Notendur sem geta skoðað bæði Mín störf og Öll störf á starfasíðunni eru með sömu yfirlitin tiltæk í Starfsgreiningarmiðstöðinni.</span><span class="sxs-lookup"><span data-stu-id="89dde-146">Users that can view both My jobs and All jobs on the Jobs page have the same views available in the Analytics Hub.</span></span>

## <a name="cross-filter"></a><span data-ttu-id="89dde-147">Krosssíun</span><span class="sxs-lookup"><span data-stu-id="89dde-147">Cross-filter</span></span>

<span data-ttu-id="89dde-148">Einn af frábærum eiginleikum Power BI er hvernig allt myndefni á skýrslusíðu er tengt innbyrðis.</span><span class="sxs-lookup"><span data-stu-id="89dde-148">One of the great features of Power BI is the way all visuals on a report page are interconnected.</span></span> <span data-ttu-id="89dde-149">Ef gagnapunktur er valinn í einu myndefnanna, breytist allt annað myndefni á síðunni sem inniheldur þessi gögn, á grunni þessa vals.</span><span class="sxs-lookup"><span data-stu-id="89dde-149">If you select a data point on one of the visuals, all the other visuals on the page that contain that data change, based on that selection.</span></span> <span data-ttu-id="89dde-150">Fáðu að vita meira og sjáðu dæmi í [Hvernig myndefni krosssía hvert annað í Power BI-skýrslu](https://docs.microsoft.com/power-bi/consumer/end-user-interactions).</span><span class="sxs-lookup"><span data-stu-id="89dde-150">Find out more and see an example in [How visuals cross-filter each other in a Power BI report](https://docs.microsoft.com/power-bi/consumer/end-user-interactions).</span></span>

## <a name="export-to-excel"></a><span data-ttu-id="89dde-151">Flytja út í Excel</span><span class="sxs-lookup"><span data-stu-id="89dde-151">Export to Excel</span></span>

<span data-ttu-id="89dde-152">Til að skoða skýrslugögn í Excel er hægt að smella á valmyndina fyrir valkosti (þrír punktar) í myndefni og velja **Flytja út undirliggjandi gögn**.</span><span class="sxs-lookup"><span data-stu-id="89dde-152">To view report data in Excel, you can click the options menu (three dots) on a visual and select **Export underlying data**.</span></span> <span data-ttu-id="89dde-153">Útflutt gögn flytjast út sem síuð, tekur mið af heimildum notanda í Attract.</span><span class="sxs-lookup"><span data-stu-id="89dde-153">Exported data will export as filtered, respecting user permissions in Attract.</span></span> <span data-ttu-id="89dde-154">Frekari upplýsingar eru í [Flytja gögn út úr myndrænum framsetningum](https://docs.microsoft.com/power-bi/visuals/power-bi-visualization-export-data).</span><span class="sxs-lookup"><span data-stu-id="89dde-154">For more information, see [Export data from visualizations](https://docs.microsoft.com/power-bi/visuals/power-bi-visualization-export-data).</span></span>
