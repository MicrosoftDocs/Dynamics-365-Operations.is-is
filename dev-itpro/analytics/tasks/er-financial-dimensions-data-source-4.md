--- 
title: "Keyra skýrslu sem notar fjárhagsvíddir sem gagnaveitu í rafrænni skýrslugerð (ER)"
description: "Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stillt líkan rafrænnar skýrslugerðar (ER) svo það noti fjárhagsvíddir sem gagnaveitu fyrir rafrænar skýrslur."
author: NickSelin
manager: AnnBe
ms.date: 10/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: e319c9d11ccc4311437ce1e74d4f6c8be0e0de35
ms.contentlocale: is-is
ms.lasthandoff: 08/29/2017

---
# <a name="run-a-report-that-uses-financial-dimensions-as-a-data-source-for-electronic-reporting-er"></a><span data-ttu-id="a79e8-103">Keyra skýrslu sem notar fjárhagsvíddir sem gagnaveitu í rafrænni skýrslugerð (ER)</span><span class="sxs-lookup"><span data-stu-id="a79e8-103">Run a report that uses financial dimensions as a data source for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a79e8-104">Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stillt líkan rafrænnar skýrslugerðar (ER) svo það noti fjárhagsvíddir sem gagnaveitu fyrir rafrænar skýrslur.</span><span class="sxs-lookup"><span data-stu-id="a79e8-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="a79e8-105">Hægt er að framkvæma þessum skrefum í DEMF fyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="a79e8-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="a79e8-106">Til að ljúka þessum skrefum, verður fyrst að ljúka við skrefin í á “Rafræn skýrslugerð notar fjárhagsvíddir sem gagnaveitu (Hluti 3: hanna skýrslu)” ferli.</span><span class="sxs-lookup"><span data-stu-id="a79e8-106">To complete these steps, you must first complete the steps in the “ER Use financial dimensions as a data source (Part 3: Design the report)” procedure.</span></span> <span data-ttu-id="a79e8-107">Einnig þarf að skilgreina sjálfgefnar gerðir skjala á færibreytusíðu Rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="a79e8-107">You must also configure default document types on the Electronic reporting parameters page.</span></span> <span data-ttu-id="a79e8-108">Sjálfgefið gerðir skjala eru einnig stilltar þegar þú sækir og flytja inn hvers kyns grunnstillingar ræfrænna skýrslna (ER).</span><span class="sxs-lookup"><span data-stu-id="a79e8-108">Default document types are also set when you download and import any ER configuration.</span></span> 


## <a name="run-report"></a><span data-ttu-id="a79e8-109">Keyra skýrslu.</span><span class="sxs-lookup"><span data-stu-id="a79e8-109">Run report</span></span>
1. <span data-ttu-id="a79e8-110">Fara í Fyrirtækisstjórnun > Rafræn skýrslugerð > Grunnstillingar.</span><span class="sxs-lookup"><span data-stu-id="a79e8-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="a79e8-111">Í trénu skal víkka út 'Financial dimensions sample model'.</span><span class="sxs-lookup"><span data-stu-id="a79e8-111">In the tree, expand 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="a79e8-112">Í trénu skal velja 'Financial dimensions sample model\Ledger journal report'.</span><span class="sxs-lookup"><span data-stu-id="a79e8-112">In the tree, select 'Financial dimensions sample model\Ledger journal report'.</span></span>
4. <span data-ttu-id="a79e8-113">Smella á Keyra.</span><span class="sxs-lookup"><span data-stu-id="a79e8-113">Click Run.</span></span>
5. <span data-ttu-id="a79e8-114">Í svæðinu heiti víddar, í svæðinu heiti víddar, skal færa inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="a79e8-114">In the Dimension name field, In the Dimension name field, enter or select a value..</span></span>
    * <span data-ttu-id="a79e8-115">Til að velja allar víddir fyrir núverandi fyrirtæki skal færa inn eftirfarandi:BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span><span class="sxs-lookup"><span data-stu-id="a79e8-115">To select all dimensions in the current company, enter the following:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span></span>  
6. <span data-ttu-id="a79e8-116">Útvíkka Færslur til að taka hluta.</span><span class="sxs-lookup"><span data-stu-id="a79e8-116">Expand the Records to include section.</span></span>
7. <span data-ttu-id="a79e8-117">Smellt er á Síu.</span><span class="sxs-lookup"><span data-stu-id="a79e8-117">Click Filter.</span></span>
8. <span data-ttu-id="a79e8-118">Velja línuna fyrir töflu færslubókar fjárhags og reitinn rununúmer bókarkeyrslu.</span><span class="sxs-lookup"><span data-stu-id="a79e8-118">Select the row for the Ledger journal table and the Journal batch number field.</span></span>
9. <span data-ttu-id="a79e8-119">Í svæðinu Skilyrði skal færa inn '00057'.</span><span class="sxs-lookup"><span data-stu-id="a79e8-119">In the Criteria field, type '00057'.</span></span>
10. <span data-ttu-id="a79e8-120">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="a79e8-120">Click OK.</span></span>
11. <span data-ttu-id="a79e8-121">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="a79e8-121">Click OK.</span></span>
    * <span data-ttu-id="a79e8-122">Fara yfir myndað úttak.</span><span class="sxs-lookup"><span data-stu-id="a79e8-122">Review the generated output.</span></span> <span data-ttu-id="a79e8-123">Athugið að fyrir hverja færslu fyrir valda runu eru birtar fjárhagsvíddir úr viðeigandi víddarmengjum.</span><span class="sxs-lookup"><span data-stu-id="a79e8-123">Note that for each transaction of the selected batch, the financial dimensions from the corresponding dimensions set are presented.</span></span> <span data-ttu-id="a79e8-124">Keyra þessa skýrslu og veljið mismunandi víddir til að sjá að skýrslan er ekki háð fjölda valinna vídda eða fjölda vídda sem skilgreint er fyrir þetta Dynamics 365 for Finance and Operations, Enterprise edition tilvik.</span><span class="sxs-lookup"><span data-stu-id="a79e8-124">Run this report and select different dimensions to see that the report is not dependent on the number of selected dimensions or the number of dimensions configured for this Dynamics 365 for Finance and Operations, Enterprise edition instance.</span></span>  


