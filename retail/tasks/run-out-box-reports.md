--- 
title: " Mynda og keyra tilbúnar skýrslur"
description: "Notið þessa verkleiðbeiningar til að keyra út úr kassa skýrslur í höfuðstöðvum frá mismunandi vinnusvæðum og Fyrirspurnir & Söluskýrslur staðsettar undir smásölu & viðskipti."
author: ashishmsft
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 9ba616550120e273429e348ea9cddf7c9e8baee4
ms.contentlocale: is-is
ms.lasthandoff: 08/29/2017

---
# <a name="generate-and-run-out-of-box-reports"></a><span data-ttu-id="bff88-103"> Mynda og keyra tilbúnar skýrslur</span><span class="sxs-lookup"><span data-stu-id="bff88-103">Generate and run out-of-box reports</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="bff88-104">Notið þessa verkleiðbeiningar til að keyra út úr kassa skýrslur í höfuðstöðvum frá mismunandi vinnusvæðum og Fyrirspurnir & Söluskýrslur staðsettar undir smásölu & viðskipti.</span><span class="sxs-lookup"><span data-stu-id="bff88-104">Use this task guide to run out of box reports in headquarters from different workspaces and Inquiries & Sales reports located under Retail & Commerce.</span></span>



<span data-ttu-id="bff88-105">Sýnigögn gögn fyrirtækisins til að stofna þetta skráning er USRT.</span><span class="sxs-lookup"><span data-stu-id="bff88-105">The demo data company used to create this recording is USRT.</span></span> <span data-ttu-id="bff88-106">Þessi skrá er ætluð fyrir kerfisstjórahlutverk.</span><span class="sxs-lookup"><span data-stu-id="bff88-106">This recording is intended for the System administrator role.</span></span>


## <a name="launch-reports-from-workspaces"></a><span data-ttu-id="bff88-107">Ræsa skýrslur úr vinnusvæði</span><span class="sxs-lookup"><span data-stu-id="bff88-107">Launch reports from workspaces</span></span>
1. <span data-ttu-id="bff88-108">Fara í Smásölu og viðskipti > Afurðir og tegundir > Stjórnun tegunda og afurða.</span><span class="sxs-lookup"><span data-stu-id="bff88-108">Go to Retail and commerce > Products and categories > Category and product management.</span></span>
2. <span data-ttu-id="bff88-109">Með því að smella á örina má stækka eða fella saman skýrsluhlutann.</span><span class="sxs-lookup"><span data-stu-id="bff88-109">Click the arrow to expand or collapse the Reports section.</span></span>
3. <span data-ttu-id="bff88-110">Smelltu á Skýrsla yfir mest seldu vörurnar</span><span class="sxs-lookup"><span data-stu-id="bff88-110">Click Top products report.</span></span>
4. <span data-ttu-id="bff88-111">Dagsetning er rituð í reitinn Frá dags.</span><span class="sxs-lookup"><span data-stu-id="bff88-111">In the From date field, enter a date.</span></span>
5. <span data-ttu-id="bff88-112">Í reitinn Til dagsetningar skal slá inn dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="bff88-112">In the To date field, enter a date.</span></span>
6. <span data-ttu-id="bff88-113">Í reitnum rás skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="bff88-113">In the Channel field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="bff88-114">Veljið 'Contoso smásala\Contoso Retail USA\Central\Houston', í trénu.</span><span class="sxs-lookup"><span data-stu-id="bff88-114">In the tree, select 'Contoso Retail\Contoso Retail USA\Central\Houston'.</span></span>
    * <span data-ttu-id="bff88-115">Þetta sýnir sem sjálfgefið stigveldi fyrirtækis fyrir Smásölu skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="bff88-115">This shows the default retail organization hierarchy for Retail reporting purpose.</span></span>   <span data-ttu-id="bff88-116">Fara á fyrirtækisstjórnun > fyrirtæki > stigveldi Fyrirtækis í upplýsingarskyni og velja skýrslugerð Smásölu og undir Tengdar stigveldi, athuga stigveldisheiti sem Sjálfgefna dálkurinn er skráð.</span><span class="sxs-lookup"><span data-stu-id="bff88-116">Go to Organization administration >Organizations >Organization hierarchy purposes and choose Retail reporting and under Assigned hierarchies, check the hierarchy name for which Default column is checked.</span></span>      <span data-ttu-id="bff88-117">Sem hluti af sýnigögn (notað fyrir þennan verkskráningu) tekurðu eftir, Smásöluverslanir eftir Svæði er sjálfgefið stigveldi fyrirtækis fyrir Smásölu skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="bff88-117">As part of demo data (used for this task recording) you would notice, Retail Stores by Region, is the default organization hierarchy for the Retail reporting purpose.</span></span>     
8. <span data-ttu-id="bff88-118">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="bff88-118">Click OK.</span></span>
9. <span data-ttu-id="bff88-119">Í reitnum Skoða skal velja valkost.</span><span class="sxs-lookup"><span data-stu-id="bff88-119">In the View field, select an option.</span></span>
10. <span data-ttu-id="bff88-120">Í reitnum Samkvæmt skal velja valkost.</span><span class="sxs-lookup"><span data-stu-id="bff88-120">In the By field, select an option.</span></span>
11. <span data-ttu-id="bff88-121">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="bff88-121">Click OK.</span></span>

## <a name="launch-reports-from-the-inquiries-and-sales-reports-located-under-retail--commerce-app-link"></a><span data-ttu-id="bff88-122">Ræsa skýrslur úr fyrirspurnir og söluskýrslur staðsett undir Smásala & Viðskipti tengill í smáforrit.</span><span class="sxs-lookup"><span data-stu-id="bff88-122">Launch reports from the inquiries and sales reports located under Retail & Commerce app link.</span></span>
1. <span data-ttu-id="bff88-123">Fara í Smásala og viðskipti > Fyrirspurnir og skýrslur > Söluskýrslur > Flokkar söluskýrsla.</span><span class="sxs-lookup"><span data-stu-id="bff88-123">Go to Retail and commerce > Inquiries and reports > Sales reports > Category sales report.</span></span>
2. <span data-ttu-id="bff88-124">Dagsetning er rituð í reitinn Frá dags.</span><span class="sxs-lookup"><span data-stu-id="bff88-124">In the From date field, enter a date.</span></span>
3. <span data-ttu-id="bff88-125">Í reitinn Til dagsetningar skal slá inn dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="bff88-125">In the To date field, enter a date.</span></span>
4. <span data-ttu-id="bff88-126">Í reitnum rás skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="bff88-126">In the Channel field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="bff88-127">Veljið 'Contoso Retail\Contoso Retail USA\West\Seattle', í trénu.</span><span class="sxs-lookup"><span data-stu-id="bff88-127">In the tree, select 'Contoso Retail\Contoso Retail USA\West\Seattle'.</span></span>
    * <span data-ttu-id="bff88-128">Þetta sýnir sem sjálfgefið stigveldi fyrirtækis fyrir Smásölu skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="bff88-128">This shows the default retail organization hierarchy for Retail reporting purpose.</span></span>   <span data-ttu-id="bff88-129">Fara á fyrirtækisstjórnun > fyrirtæki > stigveldi Fyrirtækis í upplýsingarskyni og velja skýrslugerð Smásölu og undir Tengdar stigveldi, athuga stigveldisheiti sem Sjálfgefna dálkurinn er skráð.</span><span class="sxs-lookup"><span data-stu-id="bff88-129">Go to Organization administration >Organizations >Organization hierarchy purposes and choose Retail reporting and under Assigned hierarchies, check the hierarchy name for which Default column is checked.</span></span>      <span data-ttu-id="bff88-130">Sem hluti af sýnigögn (notað fyrir þennan verkskráningu) tekurðu eftir, Smásöluverslanir eftir Svæði er sjálfgefið stigveldi fyrirtækis fyrir Smásölu skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="bff88-130">As part of demo data (used for this task recording) you would notice, Retail Stores by Region, is the default organization hierarchy for the Retail reporting purpose.</span></span>     
6. <span data-ttu-id="bff88-131">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="bff88-131">Click OK.</span></span>
7. <span data-ttu-id="bff88-132">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="bff88-132">Click OK.</span></span>

## <a name="export-an-hq-reports"></a><span data-ttu-id="bff88-133">Flytja út HQ skýrslur</span><span class="sxs-lookup"><span data-stu-id="bff88-133">Export an HQ reports</span></span>
1. <span data-ttu-id="bff88-134">Fara í Smásala og viðskipti > Fyrirspurnir og skýrslur > Söluskýrslur > Fyrirtæki söluskýrsla.</span><span class="sxs-lookup"><span data-stu-id="bff88-134">Go to Retail and commerce > Inquiries and reports > Sales reports > Organization sales report.</span></span>
2. <span data-ttu-id="bff88-135">Dagsetning er rituð í reitinn Frá dags.</span><span class="sxs-lookup"><span data-stu-id="bff88-135">In the From date field, enter a date.</span></span>
3. <span data-ttu-id="bff88-136">Í reitinn Til dagsetningar skal slá inn dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="bff88-136">In the To date field, enter a date.</span></span>
4. <span data-ttu-id="bff88-137">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="bff88-137">Click OK.</span></span>
5. <span data-ttu-id="bff88-138">Smellt er á Útflutning.</span><span class="sxs-lookup"><span data-stu-id="bff88-138">Click Export.</span></span>
6. <span data-ttu-id="bff88-139">Smellið á PDF.</span><span class="sxs-lookup"><span data-stu-id="bff88-139">Click PDF.</span></span>


