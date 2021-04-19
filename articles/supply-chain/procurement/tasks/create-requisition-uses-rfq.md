---
title: Stofna beiðni sem notar tilboðsbeiðni
description: Þetta efni útskýrir hvernig á að bæta verð og upplýsingar um lánardrottin við innkaupabeiðni úr Tilboðsbeiðniferli.
author: kamaybac
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchReqTableListPage, PurchReqCreate, PurchReqTable, PurchReqLineRelatedDocuments, EcoResCategorySingleLookup, PurchReqWorkflowDropDialog, WorkflowSubmitDialog, WorkflowStatus, WorkflowWorkItemActionDialog, WorkflowUserListLookup, PurchReqCopyRFQ, SysDataAreaSelectLookup, PurchRFQCaseTable, PurchRFQEditLines, PurchRFQReplyTable, UnitOfMeasureLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6083afe0e2bfafd337d572863a198330e8cb6cc8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5812135"
---
# <a name="create-a-requisition-that-uses-an-rfq"></a><span data-ttu-id="27e08-103">Stofna beiðni sem notar tilboðsbeiðni</span><span class="sxs-lookup"><span data-stu-id="27e08-103">Create a requisition that uses an RFQ</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="27e08-104">Þetta efni útskýrir hvernig á að bæta verð og upplýsingar um lánardrottin við innkaupabeiðni úr Tilboðsbeiðniferli.</span><span class="sxs-lookup"><span data-stu-id="27e08-104">This topic explains how to add price and vendor information to a purchase requisition from an RFQ process.</span></span> <span data-ttu-id="27e08-105">Dæmi sem sýnd eru í þessari handbók má nota í USMF fyrirtækisins sýnigögnum og þú verður að vera skráður inn sem Kerfisstjóra til að ljúka við skrefin.</span><span class="sxs-lookup"><span data-stu-id="27e08-105">The example shown in this guide can be used in the USMF demo data company, and you must be logged in as an Admin to complete all the steps.</span></span> <span data-ttu-id="27e08-106">Verkin í þessari handbók væri yfirleitt gert af innkaupasérfræðingum.</span><span class="sxs-lookup"><span data-stu-id="27e08-106">The tasks in this guide would typically be done by procurement professionals.</span></span>


## <a name="create-a-requisition"></a><span data-ttu-id="27e08-107">Stofna nýja beiðni</span><span class="sxs-lookup"><span data-stu-id="27e08-107">Create a requisition</span></span>
1. <span data-ttu-id="27e08-108">Í skoðunarrúðunni ferðu í **Kerfiseiningar > Innkaup og aðföng > Innkaupabeiðnir > Innkaupabeiðnir sem ég hef búið til**.</span><span class="sxs-lookup"><span data-stu-id="27e08-108">In the navigation pane, go to **Modules > Procurement and sourcing > Purchase requisitions > Purchase requisitions prepared by me**.</span></span>
2. <span data-ttu-id="27e08-109">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="27e08-109">Select **New**.</span></span>
3. <span data-ttu-id="27e08-110">Í reitinn **Heiti** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="27e08-110">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="27e08-111">Í reitinn **Umbeðin dagsetning** slærðu inn dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="27e08-111">In the **Requested date** field, enter a date.</span></span>
5. <span data-ttu-id="27e08-112">Í reitinn **Dagsetning reikningsskila** slærðu inn dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="27e08-112">In the **Accounting date** field, enter a date.</span></span>
6. <span data-ttu-id="27e08-113">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="27e08-113">Select **OK**.</span></span>
7. <span data-ttu-id="27e08-114">Í reitinn **Ástæða** skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="27e08-114">In the **Reason** field, enter or select a value.</span></span>
8. <span data-ttu-id="27e08-115">Veldu **Bæta við línu**.</span><span class="sxs-lookup"><span data-stu-id="27e08-115">Select **Add line**.</span></span>
9. <span data-ttu-id="27e08-116">Í reitnum **Innkaupategund** skal velja flokk í trénu og velja síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="27e08-116">In the **Procurement category** field, select a category in the tree, and then select **OK**.</span></span>
10. <span data-ttu-id="27e08-117">Í reitinn **Afurðarheiti** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="27e08-117">In the **Product name** field, type a value.</span></span>
11. <span data-ttu-id="27e08-118">Í reitnum **Magn** slærðu inn tölu.</span><span class="sxs-lookup"><span data-stu-id="27e08-118">In the **Quantity** field, enter a number.</span></span>
12. <span data-ttu-id="27e08-119">Í reitinn **Eining** skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="27e08-119">In the **Unit** field, enter or select a value.</span></span>
13. <span data-ttu-id="27e08-120">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="27e08-120">Select **Save**.</span></span>
14. <span data-ttu-id="27e08-121">Veldu **Verkflæði** til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="27e08-121">Select **Workflow** to open the drop dialog.</span></span>
15. <span data-ttu-id="27e08-122">Veldu **Senda**.</span><span class="sxs-lookup"><span data-stu-id="27e08-122">Select **Submit**.</span></span>
16. <span data-ttu-id="27e08-123">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="27e08-123">Close the page.</span></span>
17. <span data-ttu-id="27e08-124">Veldu **Senda**.</span><span class="sxs-lookup"><span data-stu-id="27e08-124">Select **Submit**.</span></span>

## <a name="reassign-a-workflow-task"></a><span data-ttu-id="27e08-125">Endurúthluta verkflæðisverki</span><span class="sxs-lookup"><span data-stu-id="27e08-125">Reassign a workflow task</span></span>
<span data-ttu-id="27e08-126">Næsta verki er að stofna beiðni um TILBOÐ til að fá tilboð frá lánardrottnum fyrir afurðina.</span><span class="sxs-lookup"><span data-stu-id="27e08-126">The next task is to create an RFQ to get bids from vendors for the product.</span></span> <span data-ttu-id="27e08-127">Í sýnigögn USMF, er verkflæði fyrir beiðni sett upp með reglu þannig að ef lánardrottinn er ekki valinn, eða einingarverð er 0 fyrir línu, er verki úthlutað á tiltekinn starfsmann til að stofna beiðni um TILBOÐ.</span><span class="sxs-lookup"><span data-stu-id="27e08-127">In USMF demo data, the requisition workflow is set up with a rule so that if a vendor is not selected, or the unit price is 0 for a line, a task is assigned to a specific worker to create an RFQ.</span></span> <span data-ttu-id="27e08-128">Til að halda áfram með þessari handbók, þarf að úthluta því verki til annars notanda (sjálfur).</span><span class="sxs-lookup"><span data-stu-id="27e08-128">To continue with this guide, you need to re-assign that task to another user (yourself).</span></span> <span data-ttu-id="27e08-129">Það er aðeins mögulegt ef notandi er innskráður sem er Admin.</span><span class="sxs-lookup"><span data-stu-id="27e08-129">You can only do this if you are logged in as an Admin.</span></span>  

1. <span data-ttu-id="27e08-130">Veldu **Verkflæði** til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="27e08-130">Select **Workflow** to open the drop dialog.</span></span>
2. <span data-ttu-id="27e08-131">Veldu **Skoða sögu**.</span><span class="sxs-lookup"><span data-stu-id="27e08-131">Select **View history**.</span></span>
3. <span data-ttu-id="27e08-132">Endurhlaðið síðuna.</span><span class="sxs-lookup"><span data-stu-id="27e08-132">Refresh the page.</span></span>
4. <span data-ttu-id="27e08-133">Útvíkkaðu kaflann **Rakningarupplýsingar**.</span><span class="sxs-lookup"><span data-stu-id="27e08-133">Expand the **Tracking details** section.</span></span>
5. <span data-ttu-id="27e08-134">Í trénu velurðu línuna sem hefst á „Línuverkflæði virkjað þann“.</span><span class="sxs-lookup"><span data-stu-id="27e08-134">In the tree, select the line that starts with "Line workflow activated on".</span></span>
6. <span data-ttu-id="27e08-135">Veldu **Skoða upplýsingar um verkflæði**.</span><span class="sxs-lookup"><span data-stu-id="27e08-135">Select **View workflow details**.</span></span>
7. <span data-ttu-id="27e08-136">Útvíkkaðu kaflann **Vinnuliðir**.</span><span class="sxs-lookup"><span data-stu-id="27e08-136">Expand the **Work items** section.</span></span>
8. <span data-ttu-id="27e08-137">Velja **Endurúthluta**.</span><span class="sxs-lookup"><span data-stu-id="27e08-137">Select **Reassign**.</span></span>
9. <span data-ttu-id="27e08-138">Í reitnum **Notandi** velurðu **Stjórnandi**.</span><span class="sxs-lookup"><span data-stu-id="27e08-138">In the **User** field, select **Admin**.</span></span>
10. <span data-ttu-id="27e08-139">Velja **Endurúthluta**.</span><span class="sxs-lookup"><span data-stu-id="27e08-139">Select **Reassign**.</span></span>
11. <span data-ttu-id="27e08-140">Lokaðu síðunum tveimur.</span><span class="sxs-lookup"><span data-stu-id="27e08-140">Close the two pages.</span></span>

## <a name="create-an-rfq"></a><span data-ttu-id="27e08-141">Búa til beiðni um tilboð</span><span class="sxs-lookup"><span data-stu-id="27e08-141">Create an RFQ</span></span>

1. <span data-ttu-id="27e08-142">Endurhlaðið síðuna.</span><span class="sxs-lookup"><span data-stu-id="27e08-142">Refresh the page.</span></span>
2. <span data-ttu-id="27e08-143">Veldu **Beiðni um tilboð**.</span><span class="sxs-lookup"><span data-stu-id="27e08-143">Select **Request for quotation**.</span></span>
3. <span data-ttu-id="27e08-144">Í reitnum **Innkaupalögaðili** velurðu **USMF**.</span><span class="sxs-lookup"><span data-stu-id="27e08-144">In the **Buying legal entity** field, select **USMF**.</span></span> <span data-ttu-id="27e08-145">Velja þarf sama lögaðila sem er í innkaupabeiðnilínunni.</span><span class="sxs-lookup"><span data-stu-id="27e08-145">You must select the same legal entity that's on the requisition line.</span></span>  
4. <span data-ttu-id="27e08-146">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="27e08-146">In the list, mark the selected row.</span></span> <span data-ttu-id="27e08-147">Hafirðu haft margar línur á innkaupabeiðni þinni, veldu allar línur sem þú vilt bæta við beiðni um tilboð.</span><span class="sxs-lookup"><span data-stu-id="27e08-147">If you had multiple lines on your purchase requisition, select all the lines that you want to add to the RFQ.</span></span>  
5. <span data-ttu-id="27e08-148">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="27e08-148">Select **OK**.</span></span>
6. <span data-ttu-id="27e08-149">Endurhlaðið síðuna.</span><span class="sxs-lookup"><span data-stu-id="27e08-149">Refresh the page.</span></span>
7. <span data-ttu-id="27e08-150">Passaðu að upplýsingareiturinn sé opinn og útvíkkaðu síðan hlutann **Tengd skjöl**.</span><span class="sxs-lookup"><span data-stu-id="27e08-150">Ensure that the FactBox is open, then expand the **Related documents** section.</span></span>
8. <span data-ttu-id="27e08-151">Veldu tengilinn í reitnum **Beiðni um tilboð** til að opna beiðni um tilboð sem verið var að stofna.</span><span class="sxs-lookup"><span data-stu-id="27e08-151">Select the link in the **Request for quotation** field to open the RFQ that was just created.</span></span>
9. <span data-ttu-id="27e08-152">Veldu **Haus**.</span><span class="sxs-lookup"><span data-stu-id="27e08-152">Select **Header**.</span></span>
10. <span data-ttu-id="27e08-153">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="27e08-153">Select **Add**.</span></span>
11. <span data-ttu-id="27e08-154">Í reitinn **Lánardrottnalykill** skal færa inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="27e08-154">In the **Vendor account** field, enter or select a value.</span></span>
12. <span data-ttu-id="27e08-155">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="27e08-155">Select **Add**.</span></span>
13. <span data-ttu-id="27e08-156">Í reitinn **Lánardrottnalykill** skal færa inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="27e08-156">In the **Vendor account** field, enter or select a value.</span></span>
14. <span data-ttu-id="27e08-157">Veljið **Senda**.</span><span class="sxs-lookup"><span data-stu-id="27e08-157">Select **Send**.</span></span>
15. <span data-ttu-id="27e08-158">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="27e08-158">Select **OK**.</span></span>
16. <span data-ttu-id="27e08-159">Veldu **Færa inn svar**.</span><span class="sxs-lookup"><span data-stu-id="27e08-159">Select **Enter reply**.</span></span>
17. <span data-ttu-id="27e08-160">Í aðgerðarúðunni skal velja **Svara**.</span><span class="sxs-lookup"><span data-stu-id="27e08-160">On the Action Pane, select **Reply**.</span></span>
18. <span data-ttu-id="27e08-161">Veldu **Afrita gögn í svar**.</span><span class="sxs-lookup"><span data-stu-id="27e08-161">Select **Copy data to reply**.</span></span> <span data-ttu-id="27e08-162">Þetta afritar gögn, eins og magn og dagsetningar, frá beiðni um TILBOÐ í svarið.</span><span class="sxs-lookup"><span data-stu-id="27e08-162">This copies data, such as the quantity and dates, from the RFQ to the reply.</span></span>  
19. <span data-ttu-id="27e08-163">Í reitnum **Einingarverð** skal slá inn tölu.</span><span class="sxs-lookup"><span data-stu-id="27e08-163">In the **Unit price** field, enter a number.</span></span> <span data-ttu-id="27e08-164">Þetta er verðið sem þú hefur fengið frá lánardrottni.</span><span class="sxs-lookup"><span data-stu-id="27e08-164">This is the price that you've received from the vendor.</span></span> <span data-ttu-id="27e08-165">Þú gætir einnig viljað færið inn viðbótarupplýsingar frá lánardrottni.</span><span class="sxs-lookup"><span data-stu-id="27e08-165">You might also want to enter additional information from the vendor.</span></span>  
20. <span data-ttu-id="27e08-166">Veljið **Samþykkja**.</span><span class="sxs-lookup"><span data-stu-id="27e08-166">Select **Accept**.</span></span>
21. <span data-ttu-id="27e08-167">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="27e08-167">Select **OK**.</span></span>

## <a name="verify-that-vendor-and-price-have-been-transferred-to-the-requisition"></a><span data-ttu-id="27e08-168">Staðfestið að verð og lánardrottinn hafa verið fluttar í beiðni.</span><span class="sxs-lookup"><span data-stu-id="27e08-168">Verify that vendor and price have been transferred to the requisition</span></span>
1. <span data-ttu-id="27e08-169">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="27e08-169">Close the page.</span></span>
2. <span data-ttu-id="27e08-170">Veldu **Línur**.</span><span class="sxs-lookup"><span data-stu-id="27e08-170">Select **Lines**.</span></span>
3. <span data-ttu-id="27e08-171">Veldu **Tengdar upplýsingar**.</span><span class="sxs-lookup"><span data-stu-id="27e08-171">Select **Related information**.</span></span>
4. <span data-ttu-id="27e08-172">Veldu **Innkaupabeiðni**.</span><span class="sxs-lookup"><span data-stu-id="27e08-172">Select **Purchase requisition**.</span></span>
5. <span data-ttu-id="27e08-173">Veldu sú lína sem var flutt á beiðni um tilboð.</span><span class="sxs-lookup"><span data-stu-id="27e08-173">Select the line that was transferred to the RFQ.</span></span> <span data-ttu-id="27e08-174">Staðfestið að verð og lánardrottinn hafa verið afritaðar í beiðni.</span><span class="sxs-lookup"><span data-stu-id="27e08-174">Verify that the price and vendor have been copied to the requisition.</span></span>  
6. <span data-ttu-id="27e08-175">Veldu **Verkflæði** til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="27e08-175">Select **Workflow** to open the drop dialog.</span></span>
7. <span data-ttu-id="27e08-176">Velja Lokið.</span><span class="sxs-lookup"><span data-stu-id="27e08-176">Select Complete.</span></span>
8. <span data-ttu-id="27e08-177">Veldu síðuna.</span><span class="sxs-lookup"><span data-stu-id="27e08-177">Select the page.</span></span>
9. <span data-ttu-id="27e08-178">Velja Lokið.</span><span class="sxs-lookup"><span data-stu-id="27e08-178">Select Complete.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]