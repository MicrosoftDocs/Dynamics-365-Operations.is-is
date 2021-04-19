---
title: Búa til og keyra forsniðnar skýrslur
description: Notið þessa verkleiðbeiningar til að keyra út úr kassa skýrslur í höfuðstöðvum frá mismunandi vinnusvæðum og Fyrirspurnir & Söluskýrslur staðsettar undir Commerce.
author: ashishmsft
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailCategoryAndProductWorkspace, RetailOrgHierarchyTreeLookup, SrsReportViewerForm
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: db75b09f1ae1f83a88a5e5eaef0c8c1b8eab5901
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5804138"
---
# <a name="generate-and-run-out-of-box-reports"></a><span data-ttu-id="00970-103">Búa til og keyra forsniðnar skýrslur</span><span class="sxs-lookup"><span data-stu-id="00970-103">Generate and run out of box reports</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="00970-104">Notið þessa verkleiðbeiningar til að keyra út úr kassa skýrslur í höfuðstöðvum frá mismunandi vinnusvæðum og Fyrirspurnir & Söluskýrslur staðsettar undir Commerce.</span><span class="sxs-lookup"><span data-stu-id="00970-104">Use this task guide to run out of box reports in Headquarters from different workspaces and Inquiries & Sales reports located in Commerce.</span></span>

<span data-ttu-id="00970-105">Sýnigögn gögn fyrirtækisins til að stofna þetta skráning er USRT.</span><span class="sxs-lookup"><span data-stu-id="00970-105">The demo data company used to create this recording is USRT.</span></span> <span data-ttu-id="00970-106">Þessi skrá er ætluð fyrir kerfisstjórahlutverk.</span><span class="sxs-lookup"><span data-stu-id="00970-106">This recording is intended for the System administrator role.</span></span>

## <a name="launch-reports-from-workspaces"></a><span data-ttu-id="00970-107">Ræsa skýrslur úr vinnusvæði</span><span class="sxs-lookup"><span data-stu-id="00970-107">Launch reports from workspaces</span></span>
1. <span data-ttu-id="00970-108">Fara í Retail og Commerce > Afurðir og tegundir > Stjórnun tegunda og afurða.</span><span class="sxs-lookup"><span data-stu-id="00970-108">Go to Retail and Commerce > Products and categories > Category and product management.</span></span>
2. <span data-ttu-id="00970-109">Með því að smella á örina má stækka eða fella saman skýrsluhlutann.</span><span class="sxs-lookup"><span data-stu-id="00970-109">Click the arrow to expand or collapse the Reports section.</span></span>
3. <span data-ttu-id="00970-110">Smelltu á Skýrsla yfir mest seldu vörurnar</span><span class="sxs-lookup"><span data-stu-id="00970-110">Click Top products report.</span></span>
4. <span data-ttu-id="00970-111">Dagsetning er rituð í reitinn Frá dags.</span><span class="sxs-lookup"><span data-stu-id="00970-111">In the From date field, enter a date.</span></span>
5. <span data-ttu-id="00970-112">Í reitinn Til dagsetningar skal slá inn dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="00970-112">In the To date field, enter a date.</span></span>
6. <span data-ttu-id="00970-113">Í reitnum rás skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="00970-113">In the Channel field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="00970-114">Veljið 'Contoso smásala\Contoso Retail USA\Central\Houston', í trénu.</span><span class="sxs-lookup"><span data-stu-id="00970-114">In the tree, select 'Contoso Retail\Contoso Retail USA\Central\Houston'.</span></span>
    * <span data-ttu-id="00970-115">Þetta sýnir sem sjálfgefið stigveldi fyrirtækis fyrir Commerce skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="00970-115">This shows the default organization hierarchy for Commerce reporting purpose.</span></span>   <span data-ttu-id="00970-116">Fara á fyrirtækisstjórnun > fyrirtæki > stigveldi Fyrirtækis í upplýsingarskyni og velja skýrslugerð Commerce og undir Tengdar stigveldi, athuga stigveldisheiti sem Sjálfgefna dálkurinn er skráð.</span><span class="sxs-lookup"><span data-stu-id="00970-116">Go to Organization administration > Organizations > Organization hierarchy purposes and choose Commerce reporting and under Assigned hierarchies, check the hierarchy name for which Default column is checked.</span></span> <span data-ttu-id="00970-117">Sem hluti af sýnigögn (notað fyrir þennan verkskráningu) tekurðu eftir, Verslanir eftir Svæði er sjálfgefið stigveldi fyrirtækis fyrir skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="00970-117">As part of demo data (used for this task recording) you would notice, Stores by Region, is the default organization hierarchy for the reporting purpose.</span></span>     
8. <span data-ttu-id="00970-118">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="00970-118">Click OK.</span></span>
9. <span data-ttu-id="00970-119">Í reitnum Skoða skal velja valkost.</span><span class="sxs-lookup"><span data-stu-id="00970-119">In the View field, select an option.</span></span>
10. <span data-ttu-id="00970-120">Í reitnum Samkvæmt skal velja valkost.</span><span class="sxs-lookup"><span data-stu-id="00970-120">In the By field, select an option.</span></span>
11. <span data-ttu-id="00970-121">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="00970-121">Click OK.</span></span>

## <a name="launch-reports-from-the-inquiries-and-sales-reports"></a><span data-ttu-id="00970-122">Ræstu skýrslur frá fyrirspurnum og söluskýrslum</span><span class="sxs-lookup"><span data-stu-id="00970-122">Launch reports from the inquiries and sales reports</span></span>
1. <span data-ttu-id="00970-123">Fara í Retail og Commerce > Fyrirspurnir og skýrslur > Söluskýrslur > Flokkar söluskýrsla.</span><span class="sxs-lookup"><span data-stu-id="00970-123">Go to Retail and Commerce > Inquiries and reports > Sales reports > Category sales report.</span></span>
2. <span data-ttu-id="00970-124">Dagsetning er rituð í reitinn Frá dags.</span><span class="sxs-lookup"><span data-stu-id="00970-124">In the From date field, enter a date.</span></span>
3. <span data-ttu-id="00970-125">Í reitinn Til dagsetningar skal slá inn dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="00970-125">In the To date field, enter a date.</span></span>
4. <span data-ttu-id="00970-126">Í reitnum rás skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="00970-126">In the Channel field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="00970-127">Veljið 'Contoso Retail\Contoso Retail USA\West\Seattle', í trénu.</span><span class="sxs-lookup"><span data-stu-id="00970-127">In the tree, select 'Contoso Retail\Contoso Retail USA\West\Seattle'.</span></span>
    * <span data-ttu-id="00970-128">Þetta sýnir sem sjálfgefið stigveldi fyrirtækis fyrir Commerce skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="00970-128">This shows the default organization hierarchy for Commerce reporting purpose.</span></span> <span data-ttu-id="00970-129">Fara á fyrirtækisstjórnun > fyrirtæki > stigveldi Fyrirtækis í upplýsingarskyni og velja skýrslugerð Commerce og undir Tengdar stigveldi, athuga stigveldisheiti sem Sjálfgefna dálkurinn er skráð.</span><span class="sxs-lookup"><span data-stu-id="00970-129">Go to Organization administration > Organizations > Organization hierarchy purposes and choose Commerce reporting and under Assigned hierarchies, check the hierarchy name for which Default column is checked.</span></span> <span data-ttu-id="00970-130">Sem hluti af sýnigögn (notað fyrir þennan verkskráningu) tekurðu eftir, Verslanir eftir Svæði er sjálfgefið stigveldi fyrirtækis fyrir skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="00970-130">As part of demo data (used for this task recording) you would notice, Stores by Region, is the default organization hierarchy for the reporting purpose.</span></span>     
6. <span data-ttu-id="00970-131">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="00970-131">Click OK.</span></span>
7. <span data-ttu-id="00970-132">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="00970-132">Click OK.</span></span>

## <a name="export-an-hq-reports"></a><span data-ttu-id="00970-133">Flytja út HQ skýrslur</span><span class="sxs-lookup"><span data-stu-id="00970-133">Export an HQ reports</span></span>
1. <span data-ttu-id="00970-134">Fara í Retail og Commerce > Fyrirspurnir og skýrslur > Söluskýrslur > Fyrirtæki söluskýrsla.</span><span class="sxs-lookup"><span data-stu-id="00970-134">Go to Retail and Commerce > Inquiries and reports > Sales reports > Organization sales report.</span></span>
2. <span data-ttu-id="00970-135">Dagsetning er rituð í reitinn Frá dags.</span><span class="sxs-lookup"><span data-stu-id="00970-135">In the From date field, enter a date.</span></span>
3. <span data-ttu-id="00970-136">Í reitinn Til dagsetningar skal slá inn dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="00970-136">In the To date field, enter a date.</span></span>
4. <span data-ttu-id="00970-137">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="00970-137">Click OK.</span></span>
5. <span data-ttu-id="00970-138">Smellt er á Útflutning.</span><span class="sxs-lookup"><span data-stu-id="00970-138">Click Export.</span></span>
6. <span data-ttu-id="00970-139">Smellið á PDF.</span><span class="sxs-lookup"><span data-stu-id="00970-139">Click PDF.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]