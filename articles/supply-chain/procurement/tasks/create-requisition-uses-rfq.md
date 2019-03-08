---
title: Stofna beiðni sem notar tilboðsbeiðni
description: Þessari handbók sýnir hvernig á að bæta verð og upplýsingar um lánardrottin við innkaupabeiðni úr Tilboðsbeiðniferli.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchReqTableListPage, PurchReqCreate, PurchReqTable, PurchReqLineRelatedDocuments, EcoResCategorySingleLookup, PurchReqWorkflowDropDialog, WorkflowSubmitDialog, WorkflowStatus, WorkflowWorkItemActionDialog, WorkflowUserListLookup, PurchReqCopyRFQ, SysDataAreaSelectLookup, PurchRFQCaseTable, PurchRFQEditLines, PurchRFQReplyTable, UnitOfMeasureLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8a9418b526f992008086f10ce78e95cb682bc164
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "344985"
---
# <a name="create-a-requisition-that-uses-an-rfq"></a><span data-ttu-id="f700a-103">Stofna beiðni sem notar tilboðsbeiðni</span><span class="sxs-lookup"><span data-stu-id="f700a-103">Create a requisition that uses an RFQ</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f700a-104">Þessari handbók sýnir hvernig á að bæta verð og upplýsingar um lánardrottin við innkaupabeiðni úr Tilboðsbeiðniferli.</span><span class="sxs-lookup"><span data-stu-id="f700a-104">This guide shows how to add price and vendor information to a purchase requisition from an RFQ process.</span></span> <span data-ttu-id="f700a-105">Dæmi sem sýnd eru í þessari handbók má nota í USMF fyrirtækisins sýnigögnum og þú verður að vera skráður inn sem Kerfisstjóra til að ljúka við skrefin.</span><span class="sxs-lookup"><span data-stu-id="f700a-105">The example shown in this guide can be used in the USMF demo data company, and you must be logged in as an Admin to complete all the steps.</span></span> <span data-ttu-id="f700a-106">Verkin í þessari handbók væri yfirleitt gert af innkaupasérfræðingum.</span><span class="sxs-lookup"><span data-stu-id="f700a-106">The tasks in this guide would typically be done by procurement professionals.</span></span>


## <a name="create-a-requisition"></a><span data-ttu-id="f700a-107">Stofna nýja beiðni</span><span class="sxs-lookup"><span data-stu-id="f700a-107">Create a requisition</span></span>
1. <span data-ttu-id="f700a-108">Fara í Innkaup og uppruni > Innkaupabeiðnir > Innkaupabeiðnir sem ég hef.</span><span class="sxs-lookup"><span data-stu-id="f700a-108">Go to Procurement and sourcing > Purchase requisitions > Purchase requisitions prepared by me.</span></span>
2. <span data-ttu-id="f700a-109">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="f700a-109">Click New.</span></span>
3. <span data-ttu-id="f700a-110">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="f700a-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="f700a-111">Dagsetning er rituð í reitinn umbeðin dagsetning:.</span><span class="sxs-lookup"><span data-stu-id="f700a-111">In the Requested date field, enter a date.</span></span>
5. <span data-ttu-id="f700a-112">Dagsetning er rituð í reitinn dagsetning reikningsskila.</span><span class="sxs-lookup"><span data-stu-id="f700a-112">In the Accounting date field, enter a date.</span></span>
6. <span data-ttu-id="f700a-113">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="f700a-113">Click OK.</span></span>
7. <span data-ttu-id="f700a-114">Í reitinn Ástæða skal slá inn eða veldu gildi.</span><span class="sxs-lookup"><span data-stu-id="f700a-114">In the Reason field, enter or select a value.</span></span>
8. <span data-ttu-id="f700a-115">Smellið á „Bæta við línu“.</span><span class="sxs-lookup"><span data-stu-id="f700a-115">Click Add line.</span></span>
9. <span data-ttu-id="f700a-116">Í reitnum Innkaupategund skal velja tegund í trénu og smella síðan á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="f700a-116">In the Procurement category field, select a category in the tree, and then click OK.</span></span>
10. <span data-ttu-id="f700a-117">Í reitinn Afurðarheiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="f700a-117">In the Product name field, type a value.</span></span>
11. <span data-ttu-id="f700a-118">Færið inn númer í reitnum „Magn“.</span><span class="sxs-lookup"><span data-stu-id="f700a-118">In the Quantity field, enter a number.</span></span>
12. <span data-ttu-id="f700a-119">Í reitinn eining skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="f700a-119">In the Unit field, enter or select a value.</span></span>
13. <span data-ttu-id="f700a-120">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="f700a-120">Click Save.</span></span>
14. <span data-ttu-id="f700a-121">Smellt er á Verkflæði til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="f700a-121">Click Workflow to open the drop dialog.</span></span>
15. <span data-ttu-id="f700a-122">Smelltu á Senda.</span><span class="sxs-lookup"><span data-stu-id="f700a-122">Click Submit.</span></span>
16. <span data-ttu-id="f700a-123">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="f700a-123">Close the page.</span></span>
17. <span data-ttu-id="f700a-124">Smelltu á Senda.</span><span class="sxs-lookup"><span data-stu-id="f700a-124">Click Submit.</span></span>

## <a name="reassign-a-workflow-task"></a><span data-ttu-id="f700a-125">Endurúthluta verkflæðisverki</span><span class="sxs-lookup"><span data-stu-id="f700a-125">Reassign a workflow task</span></span>
    * <span data-ttu-id="f700a-126">Næsta verki er að stofna beiðni um TILBOÐ til að fá tilboð frá lánardrottnum fyrir afurðina.</span><span class="sxs-lookup"><span data-stu-id="f700a-126">The next task is to create an RFQ to get bids from vendors for the product.</span></span> <span data-ttu-id="f700a-127">Í sýnigögn USMF, er verkflæði fyrir beiðni sett upp með reglu þannig að ef lánardrottinn er ekki valinn, eða einingarverð er 0 fyrir línu, er verki úthlutað á tiltekinn starfsmann til að stofna beiðni um TILBOÐ.</span><span class="sxs-lookup"><span data-stu-id="f700a-127">In USMF demo data, the requisition workflow is set up with a rule so that if a vendor is not selected, or the unit price is 0 for a line, a task is assigned to a specific worker to create an RFQ.</span></span> <span data-ttu-id="f700a-128">Til að halda áfram með þessari handbók, þarf að úthluta því verki til annars notanda (sjálfur).</span><span class="sxs-lookup"><span data-stu-id="f700a-128">To continue with this guide, you need to re-assign that task to another user (yourself).</span></span> <span data-ttu-id="f700a-129">Það er aðeins mögulegt ef notandi er innskráður sem er Admin.</span><span class="sxs-lookup"><span data-stu-id="f700a-129">You can only do this if you are logged in as an Admin.</span></span>  
1. <span data-ttu-id="f700a-130">Smellt er á Verkflæði til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="f700a-130">Click Workflow to open the drop dialog.</span></span>
2. <span data-ttu-id="f700a-131">Smella á Skoða sögu</span><span class="sxs-lookup"><span data-stu-id="f700a-131">Click View history.</span></span>
3. <span data-ttu-id="f700a-132">Endurhlaðið síðuna.</span><span class="sxs-lookup"><span data-stu-id="f700a-132">Refresh the page.</span></span>
4. <span data-ttu-id="f700a-133">Útvíkka hlutann rakningarupplýsingar.</span><span class="sxs-lookup"><span data-stu-id="f700a-133">Expand the Tracking details section.</span></span>
5. <span data-ttu-id="f700a-134">Veljið "línu sem byrjar á"Verkflæði virkjað á"" á trénu.</span><span class="sxs-lookup"><span data-stu-id="f700a-134">In the tree, select 'the line that starts with “Line workflow activated on”'.</span></span>
6. <span data-ttu-id="f700a-135">Smella á Skoða upplýsingar um verkflæði</span><span class="sxs-lookup"><span data-stu-id="f700a-135">Click View workflow details.</span></span>
7. <span data-ttu-id="f700a-136">Útvíkka hlutann vinnuliðir.</span><span class="sxs-lookup"><span data-stu-id="f700a-136">Expand the Work items section.</span></span>
8. <span data-ttu-id="f700a-137">Smellið á endurúthluta.</span><span class="sxs-lookup"><span data-stu-id="f700a-137">Click Reassign.</span></span>
9. <span data-ttu-id="f700a-138">Í notandareitnum, velurðu „Admin“.</span><span class="sxs-lookup"><span data-stu-id="f700a-138">In the User field, select Admin.</span></span>
10. <span data-ttu-id="f700a-139">Smellið á endurúthluta.</span><span class="sxs-lookup"><span data-stu-id="f700a-139">Click Reassign.</span></span>
11. <span data-ttu-id="f700a-140">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="f700a-140">Close the page.</span></span>
12. <span data-ttu-id="f700a-141">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="f700a-141">Close the page.</span></span>

## <a name="create-an-rfq"></a><span data-ttu-id="f700a-142">Búa til beiðni um tilboð</span><span class="sxs-lookup"><span data-stu-id="f700a-142">Create an RFQ</span></span>
1. <span data-ttu-id="f700a-143">Endurhlaðið síðuna.</span><span class="sxs-lookup"><span data-stu-id="f700a-143">Refresh the page.</span></span>
2. <span data-ttu-id="f700a-144">Smella á beiðni um tilboð</span><span class="sxs-lookup"><span data-stu-id="f700a-144">Click Request for quotation.</span></span>
3. <span data-ttu-id="f700a-145">Veldu USMF í reitnum lögaðili sem kaupir.</span><span class="sxs-lookup"><span data-stu-id="f700a-145">In the Buying legal entity field, select USMF.</span></span>
    * <span data-ttu-id="f700a-146">Velja þarf sama lögaðila sem er í innkaupabeiðnilína.</span><span class="sxs-lookup"><span data-stu-id="f700a-146">You must select the same legal entity that’s on the requisition line.</span></span>  
4. <span data-ttu-id="f700a-147">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="f700a-147">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="f700a-148">Hafirðu haft margar línur á innkaupabeiðni þinni, veldu allar línur sem þú vilt bæta við beiðni um tilboð.</span><span class="sxs-lookup"><span data-stu-id="f700a-148">If you had multiple lines on your purchase requisition, select all the lines that you want to add to the RFQ.</span></span>  
5. <span data-ttu-id="f700a-149">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="f700a-149">Click OK.</span></span>
6. <span data-ttu-id="f700a-150">Endurhlaðið síðuna.</span><span class="sxs-lookup"><span data-stu-id="f700a-150">Refresh the page.</span></span>
7. <span data-ttu-id="f700a-151">Opna Upplýsingakassa og útvíkka svo hlutann Tengd skjöl.</span><span class="sxs-lookup"><span data-stu-id="f700a-151">Open the FactBox and then expand the Related documents section.</span></span>
    * <span data-ttu-id="f700a-152">Þú gætir hugsanlega nú þegar verið með Upplýsingakassa opinn.</span><span class="sxs-lookup"><span data-stu-id="f700a-152">You may already have the FactBox open.</span></span> <span data-ttu-id="f700a-153">Leita að tákn með ör á, hægra megin við víxlhnappana Línur/Haus.</span><span class="sxs-lookup"><span data-stu-id="f700a-153">Look for the icon with an arrow on it, to the right of the Lines/Header toggle buttons.</span></span> <span data-ttu-id="f700a-154">Ef örin vísar til hægri er Upplýsingakassa þegar opinn.</span><span class="sxs-lookup"><span data-stu-id="f700a-154">If the arrow is pointing to the right, the FactBox is already open.</span></span> <span data-ttu-id="f700a-155">Ef ör vísar til vinstri, skal smella á til að opna Upplýsingakassa.</span><span class="sxs-lookup"><span data-stu-id="f700a-155">If the arrow points to the left, click it to open the FactBox.</span></span>  
8. <span data-ttu-id="f700a-156">Smelltu á tengil á svæðinu Beiðni um tilboð til að opna beiðni um TILBOÐ sem verið var að stofna.</span><span class="sxs-lookup"><span data-stu-id="f700a-156">Click the link in the Request for quotation field to open the RFQ that was just created.</span></span>
9. <span data-ttu-id="f700a-157">Smellið á Haus.</span><span class="sxs-lookup"><span data-stu-id="f700a-157">Click Header.</span></span>
10. <span data-ttu-id="f700a-158">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="f700a-158">Click Add.</span></span>
11. <span data-ttu-id="f700a-159">Færa inn eða veljið gildi í svæðinu lánardrottnalykill.</span><span class="sxs-lookup"><span data-stu-id="f700a-159">In the Vendor account field, enter or select a value.</span></span>
12. <span data-ttu-id="f700a-160">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="f700a-160">Click Add.</span></span>
13. <span data-ttu-id="f700a-161">Færa inn eða veljið gildi í svæðinu lánardrottnalykill.</span><span class="sxs-lookup"><span data-stu-id="f700a-161">In the Vendor account field, enter or select a value.</span></span>
14. <span data-ttu-id="f700a-162">Smellt er á Senda.</span><span class="sxs-lookup"><span data-stu-id="f700a-162">Click Send.</span></span>
15. <span data-ttu-id="f700a-163">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="f700a-163">Click OK.</span></span>
16. <span data-ttu-id="f700a-164">Smella á Færa inn svar</span><span class="sxs-lookup"><span data-stu-id="f700a-164">Click Enter reply.</span></span>
17. <span data-ttu-id="f700a-165">Smellið á Svara á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="f700a-165">On the Action Pane, click Reply.</span></span>
18. <span data-ttu-id="f700a-166">Smella á Afrita gögn til að svara.</span><span class="sxs-lookup"><span data-stu-id="f700a-166">Click Copy data to reply.</span></span>
    * <span data-ttu-id="f700a-167">Þetta afritar gögn, eins og magn og dagsetningar, frá beiðni um TILBOÐ í svarið.</span><span class="sxs-lookup"><span data-stu-id="f700a-167">This copies data, such as the quantity and dates, from the RFQ to the reply .</span></span>  
19. <span data-ttu-id="f700a-168">Færið inn númer í reitnum „Einingarverð“.</span><span class="sxs-lookup"><span data-stu-id="f700a-168">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="f700a-169">Þetta er verðið sem þú hefur fengið frá lánardrottni.</span><span class="sxs-lookup"><span data-stu-id="f700a-169">This is the price that you’ve received from the vendor.</span></span> <span data-ttu-id="f700a-170">Þú gætir einnig viljað færið inn viðbótarupplýsingar frá lánardrottni.</span><span class="sxs-lookup"><span data-stu-id="f700a-170">You might also want to enter additional information from the vendor.</span></span>  
20. <span data-ttu-id="f700a-171">Smellið á Samþykkja.</span><span class="sxs-lookup"><span data-stu-id="f700a-171">Click Accept.</span></span>
21. <span data-ttu-id="f700a-172">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="f700a-172">Click OK.</span></span>

## <a name="verify-that-vendor-and-price-have-been-transferred-to-the-requisition"></a><span data-ttu-id="f700a-173">Staðfestið að verð og lánardrottinn hafa verið fluttar í beiðni.</span><span class="sxs-lookup"><span data-stu-id="f700a-173">Verify that vendor and price have been transferred to the requisition</span></span>
1. <span data-ttu-id="f700a-174">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="f700a-174">Close the page.</span></span>
2. <span data-ttu-id="f700a-175">Smellið á „Línur“.</span><span class="sxs-lookup"><span data-stu-id="f700a-175">Click Lines.</span></span>
3. <span data-ttu-id="f700a-176">Smelltu á Tengdar upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="f700a-176">Click Related information.</span></span>
4. <span data-ttu-id="f700a-177">Smella á innkaupabeiðni</span><span class="sxs-lookup"><span data-stu-id="f700a-177">Click Purchase requisition.</span></span>
5. <span data-ttu-id="f700a-178">Veldu sú lína sem var flutt á beiðni um tilboð.</span><span class="sxs-lookup"><span data-stu-id="f700a-178">Select the line that was transferred to the RFQ.</span></span>
    * <span data-ttu-id="f700a-179">Staðfestið að verð og lánardrottinn hafa verið afritaðar í beiðni.</span><span class="sxs-lookup"><span data-stu-id="f700a-179">Verify that the price and vendor have been copied to the requisition.</span></span>  
6. <span data-ttu-id="f700a-180">Smellt er á Verkflæði til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="f700a-180">Click Workflow to open the drop dialog.</span></span>
7. <span data-ttu-id="f700a-181">Smelltu á Ljúka.</span><span class="sxs-lookup"><span data-stu-id="f700a-181">Click Complete.</span></span>
8. <span data-ttu-id="f700a-182">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="f700a-182">Close the page.</span></span>
9. <span data-ttu-id="f700a-183">Smelltu á Ljúka.</span><span class="sxs-lookup"><span data-stu-id="f700a-183">Click Complete.</span></span>

