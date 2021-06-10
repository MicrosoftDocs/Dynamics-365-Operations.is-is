---
title: Úthluta skrefatáknum og titlum fyrir Warehouse Management farsímaforritið
description: Í þessu efnisatriði er því lýst hvernig á að úthluta skrefatáknum og titlum fyrir ný eða sérstillt verkflæði fyrir Warehouse Management farsímaforritið.
author: MarkusFogelberg
ms.date: 05/17/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2021-05-17
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 9523492d766669e6c38579fba7b5ddd6b3d282fc
ms.sourcegitcommit: c53de2c09b9296b41653e739178edf29f79e0679
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/17/2021
ms.locfileid: "6049365"
---
# <a name="assign-step-icons-and-titles-for-the-warehouse-management-mobile-app"></a><span data-ttu-id="b54fd-103">Úthluta skrefatáknum og titlum fyrir Warehouse Management farsímaforritið</span><span class="sxs-lookup"><span data-stu-id="b54fd-103">Assign step icons and titles for the Warehouse Management mobile app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b54fd-104">Í þessu efnisatriði er því lýst hvernig á að úthluta skrefatáknum og skrefatitlum fyrir ný eða sérstillt verkflæði fyrir Warehouse Management farsímaforritið.</span><span class="sxs-lookup"><span data-stu-id="b54fd-104">This topic describes how to assign step icons and step titles for new or customized task flows for the Warehouse Management mobile app.</span></span>

<span data-ttu-id="b54fd-105">Eftirfarandi mynd sýnir hvernig skrefatákn og titlar birtast í Warehouse Management farsímaforritinu.</span><span class="sxs-lookup"><span data-stu-id="b54fd-105">The following illustrations shows how step icons and titles appear in the Warehouse Management mobile app.</span></span>

<span data-ttu-id="b54fd-106">![Dæmi um skrefatákn og skrefatitil í Warehouse Management farsímaforritinu](media/step-icon-example.png "Dæmi um skrefatákn og skrefatitil í Warehouse Management farsímaforritinu")</span><span class="sxs-lookup"><span data-stu-id="b54fd-106">![Example of a step icon and a step title in the Warehouse Management mobile app](media/step-icon-example.png "Example of a step icon and a step title in the Warehouse Management mobile app")</span></span>

## <a name="turn-on-this-feature-in-your-system"></a><span data-ttu-id="b54fd-107">Kveikja á þessum eiginleika í kerfinu</span><span class="sxs-lookup"><span data-stu-id="b54fd-107">Turn on this feature in your system</span></span>

<span data-ttu-id="b54fd-108">Áður en hægt er að nota þennan eiginleika þarf að kveikja á honum í kerfinu.</span><span class="sxs-lookup"><span data-stu-id="b54fd-108">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="b54fd-109">Stjórnendur geta notað stillingarnar [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og kveikt á honum.</span><span class="sxs-lookup"><span data-stu-id="b54fd-109">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="b54fd-110">Á vinnusvæðinu **Eiginleikastjórnun** er eiginleikinn tilgreindur á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="b54fd-110">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="b54fd-111">**Eining:** *Vöruhúsakerfi*</span><span class="sxs-lookup"><span data-stu-id="b54fd-111">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="b54fd-112">**Heiti eiginleika:** *Notandastillingar, tákn og titlar skrefa fyrir nýja vöruhúsaforritið*</span><span class="sxs-lookup"><span data-stu-id="b54fd-112">**Feature name:** *User settings, icons, and step titles for the new warehouse app*</span></span>

## <a name="standard-step-ids-classes-and-icons"></a><span data-ttu-id="b54fd-113">Stöðluð kenni, klasar og tákn skrefa</span><span class="sxs-lookup"><span data-stu-id="b54fd-113">Standard step IDs, classes, and icons</span></span>

<span data-ttu-id="b54fd-114">Hvert skref í verkflæði er auðkennt með skrefakenni og hvert skrefakenni er með samsvarandi skrefaklasa.</span><span class="sxs-lookup"><span data-stu-id="b54fd-114">Each step in a task flow is identified by a step ID, and each step ID has a corresponding step class.</span></span> <span data-ttu-id="b54fd-115">Tákn og titill skrefsins eru tilgreind í hverjum skrefaklasa.</span><span class="sxs-lookup"><span data-stu-id="b54fd-115">The step icon and title are specified in each step class.</span></span>

### <a name="step-ids-and-step-classes"></a><a name="step-ids-classes"></a><span data-ttu-id="b54fd-116">Skrefakenni og skrefaklasar</span><span class="sxs-lookup"><span data-stu-id="b54fd-116">Step IDs and step classes</span></span>

<span data-ttu-id="b54fd-117">Eftirfarandi tafla sýnir hvert skrefakenni sem er í boði eins og er og samsvarandi skrefaklasa.</span><span class="sxs-lookup"><span data-stu-id="b54fd-117">The following table lists every step ID that is currently available, and its corresponding step class.</span></span> <span data-ttu-id="b54fd-118">Stýringarheiti aðalfærslureitsins er notað sem skrefakennið.</span><span class="sxs-lookup"><span data-stu-id="b54fd-118">The control name of the primary input field is used as the step ID.</span></span>

<span data-ttu-id="b54fd-119">Fyrir dæmi sem sýnir hvernig þessi skrefakenni og -klasar eru notuð skal sjá innleiðingu `WHSMobileAppStepInfoBuilder.stepId()` aðferðarinnar í hlutanum [Dæmi: Úthluta táknum og titlum skrefa fyrir sérstillt flæði](#example) síðar í þessu efnisatriði.</span><span class="sxs-lookup"><span data-stu-id="b54fd-119">For an example that shows how these step IDs and classes are used, see the implementation of the `WHSMobileAppStepInfoBuilder.stepId()` method in the [Example: Assign step icons and titles for a custom flow](#example) section later in this topic.</span></span>

| <span data-ttu-id="b54fd-120">Kenni skrefs</span><span class="sxs-lookup"><span data-stu-id="b54fd-120">Step ID</span></span> | <span data-ttu-id="b54fd-121">Klasi skrefs</span><span class="sxs-lookup"><span data-stu-id="b54fd-121">Step Class</span></span> |
|-|-|
| <span data-ttu-id="b54fd-122">BatchDisposition</span><span class="sxs-lookup"><span data-stu-id="b54fd-122">BatchDisposition</span></span> | <span data-ttu-id="b54fd-123">WHSMobileAppStepBatchDisposition</span><span class="sxs-lookup"><span data-stu-id="b54fd-123">WHSMobileAppStepBatchDisposition</span></span> |
| <span data-ttu-id="b54fd-124">Flutningsaðili</span><span class="sxs-lookup"><span data-stu-id="b54fd-124">Carrier</span></span> | <span data-ttu-id="b54fd-125">WHSMobileAppStepCarrier</span><span class="sxs-lookup"><span data-stu-id="b54fd-125">WHSMobileAppStepCarrier</span></span> |
| <span data-ttu-id="b54fd-126">CatchWeight</span><span class="sxs-lookup"><span data-stu-id="b54fd-126">CatchWeight</span></span> | <span data-ttu-id="b54fd-127">WHSMobileAppStepCatchWeight</span><span class="sxs-lookup"><span data-stu-id="b54fd-127">WHSMobileAppStepCatchWeight</span></span> |
| <span data-ttu-id="b54fd-128">CatchWeightQtyOutboundWeight</span><span class="sxs-lookup"><span data-stu-id="b54fd-128">CatchWeightQtyOutboundWeight</span></span> | <span data-ttu-id="b54fd-129">WHSMobileAppStepCatchWeight</span><span class="sxs-lookup"><span data-stu-id="b54fd-129">WHSMobileAppStepCatchWeight</span></span> |
| <span data-ttu-id="b54fd-130">CatchWeightTag</span><span class="sxs-lookup"><span data-stu-id="b54fd-130">CatchWeightTag</span></span> | <span data-ttu-id="b54fd-131">WHSMobileAppStepCatchWeightTag</span><span class="sxs-lookup"><span data-stu-id="b54fd-131">WHSMobileAppStepCatchWeightTag</span></span> |
| <span data-ttu-id="b54fd-132">CatchWeightTagWeight</span><span class="sxs-lookup"><span data-stu-id="b54fd-132">CatchWeightTagWeight</span></span> | <span data-ttu-id="b54fd-133">WHSMobileAppStepCatchWeightTagWeight</span><span class="sxs-lookup"><span data-stu-id="b54fd-133">WHSMobileAppStepCatchWeightTagWeight</span></span> |
| <span data-ttu-id="b54fd-134">ChangeWarehouseSuccess</span><span class="sxs-lookup"><span data-stu-id="b54fd-134">ChangeWarehouseSuccess</span></span> | <span data-ttu-id="b54fd-135">WHSMobileAppStepChangeWarehouseSuccess</span><span class="sxs-lookup"><span data-stu-id="b54fd-135">WHSMobileAppStepChangeWarehouseSuccess</span></span> |
| <span data-ttu-id="b54fd-136">CheckDigit</span><span class="sxs-lookup"><span data-stu-id="b54fd-136">CheckDigit</span></span> | <span data-ttu-id="b54fd-137">WHSMobileAppStepCheckDigit</span><span class="sxs-lookup"><span data-stu-id="b54fd-137">WHSMobileAppStepCheckDigit</span></span> |
| <span data-ttu-id="b54fd-138">ClusterId</span><span class="sxs-lookup"><span data-stu-id="b54fd-138">ClusterId</span></span> | <span data-ttu-id="b54fd-139">WHSMobileAppStepClusterId</span><span class="sxs-lookup"><span data-stu-id="b54fd-139">WHSMobileAppStepClusterId</span></span> |
| <span data-ttu-id="b54fd-140">ClusterPickQtyVerification</span><span class="sxs-lookup"><span data-stu-id="b54fd-140">ClusterPickQtyVerification</span></span> | <span data-ttu-id="b54fd-141">WHSMobileAppStepQtyVerification</span><span class="sxs-lookup"><span data-stu-id="b54fd-141">WHSMobileAppStepQtyVerification</span></span> |
| <span data-ttu-id="b54fd-142">ClusterPosition</span><span class="sxs-lookup"><span data-stu-id="b54fd-142">ClusterPosition</span></span> | <span data-ttu-id="b54fd-143">WHSMobileAppStepClusterPosition</span><span class="sxs-lookup"><span data-stu-id="b54fd-143">WHSMobileAppStepClusterPosition</span></span> |
| <span data-ttu-id="b54fd-144">ConfigId</span><span class="sxs-lookup"><span data-stu-id="b54fd-144">ConfigId</span></span> | <span data-ttu-id="b54fd-145">WHSMobileAppStepConfigId</span><span class="sxs-lookup"><span data-stu-id="b54fd-145">WHSMobileAppStepConfigId</span></span> |
| <span data-ttu-id="b54fd-146">Staðfesting</span><span class="sxs-lookup"><span data-stu-id="b54fd-146">Confirmation</span></span> | <span data-ttu-id="b54fd-147">WHSMobileAppStepConfirmation</span><span class="sxs-lookup"><span data-stu-id="b54fd-147">WHSMobileAppStepConfirmation</span></span> |
| <span data-ttu-id="b54fd-148">ConsolidateFromLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="b54fd-148">ConsolidateFromLicensePlateId</span></span> | <span data-ttu-id="b54fd-149">WHSMobileAppStepConsolidateFromLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="b54fd-149">WHSMobileAppStepConsolidateFromLicensePlateId</span></span> |
| <span data-ttu-id="b54fd-150">ConsolidateLPConfirmation</span><span class="sxs-lookup"><span data-stu-id="b54fd-150">ConsolidateLPConfirmation</span></span> | <span data-ttu-id="b54fd-151">WHSMobileAppStepConsolidateLPConfirmation</span><span class="sxs-lookup"><span data-stu-id="b54fd-151">WHSMobileAppStepConsolidateLPConfirmation</span></span> |
| <span data-ttu-id="b54fd-152">ConsolidateToLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="b54fd-152">ConsolidateToLicensePlateId</span></span> | <span data-ttu-id="b54fd-153">WHSMobileAppStepConsolidateToLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="b54fd-153">WHSMobileAppStepConsolidateToLicensePlateId</span></span> |
| <span data-ttu-id="b54fd-154">ContainerType</span><span class="sxs-lookup"><span data-stu-id="b54fd-154">ContainerType</span></span> | <span data-ttu-id="b54fd-155">WHSMobileAppStepContainerType</span><span class="sxs-lookup"><span data-stu-id="b54fd-155">WHSMobileAppStepContainerType</span></span> |
| <span data-ttu-id="b54fd-156">CountingReasonCode</span><span class="sxs-lookup"><span data-stu-id="b54fd-156">CountingReasonCode</span></span> | <span data-ttu-id="b54fd-157">WHSMobileAppStepCountingReasonCode</span><span class="sxs-lookup"><span data-stu-id="b54fd-157">WHSMobileAppStepCountingReasonCode</span></span> |
| <span data-ttu-id="b54fd-158">CycleCountingAddLPOrFinish</span><span class="sxs-lookup"><span data-stu-id="b54fd-158">CycleCountingAddLPOrFinish</span></span> | <span data-ttu-id="b54fd-159">WHSMobileAppStepCycleCountingAddLPOrFinish</span><span class="sxs-lookup"><span data-stu-id="b54fd-159">WHSMobileAppStepCycleCountingAddLPOrFinish</span></span> |
| <span data-ttu-id="b54fd-160">CycleCountQty1</span><span class="sxs-lookup"><span data-stu-id="b54fd-160">CycleCountQty1</span></span> | <span data-ttu-id="b54fd-161">WHSMobileAppStepCycleCountQty</span><span class="sxs-lookup"><span data-stu-id="b54fd-161">WHSMobileAppStepCycleCountQty</span></span> |
| <span data-ttu-id="b54fd-162">CycleCountQty2</span><span class="sxs-lookup"><span data-stu-id="b54fd-162">CycleCountQty2</span></span> | <span data-ttu-id="b54fd-163">WHSMobileAppStepCycleCountQty</span><span class="sxs-lookup"><span data-stu-id="b54fd-163">WHSMobileAppStepCycleCountQty</span></span> |
| <span data-ttu-id="b54fd-164">CycleCountQty3</span><span class="sxs-lookup"><span data-stu-id="b54fd-164">CycleCountQty3</span></span> | <span data-ttu-id="b54fd-165">WHSMobileAppStepCycleCountQty</span><span class="sxs-lookup"><span data-stu-id="b54fd-165">WHSMobileAppStepCycleCountQty</span></span> |
| <span data-ttu-id="b54fd-166">CycleCountQty4</span><span class="sxs-lookup"><span data-stu-id="b54fd-166">CycleCountQty4</span></span> | <span data-ttu-id="b54fd-167">WHSMobileAppStepCycleCountQty</span><span class="sxs-lookup"><span data-stu-id="b54fd-167">WHSMobileAppStepCycleCountQty</span></span> |
| <span data-ttu-id="b54fd-168">Förgun</span><span class="sxs-lookup"><span data-stu-id="b54fd-168">Disposition</span></span> | <span data-ttu-id="b54fd-169">WHSMobileAppStepDisposition</span><span class="sxs-lookup"><span data-stu-id="b54fd-169">WHSMobileAppStepDisposition</span></span> |
| <span data-ttu-id="b54fd-170">DriverCheckInConfirmation</span><span class="sxs-lookup"><span data-stu-id="b54fd-170">DriverCheckInConfirmation</span></span> | <span data-ttu-id="b54fd-171">WHSMobileAppStepDriverCheckInConfirmation</span><span class="sxs-lookup"><span data-stu-id="b54fd-171">WHSMobileAppStepDriverCheckInConfirmation</span></span> |
| <span data-ttu-id="b54fd-172">DriverCheckInId</span><span class="sxs-lookup"><span data-stu-id="b54fd-172">DriverCheckInId</span></span> | <span data-ttu-id="b54fd-173">WHSMobileAppStepDriverCheckInId</span><span class="sxs-lookup"><span data-stu-id="b54fd-173">WHSMobileAppStepDriverCheckInId</span></span> |
| <span data-ttu-id="b54fd-174">DriverCheckOutConfirmation</span><span class="sxs-lookup"><span data-stu-id="b54fd-174">DriverCheckOutConfirmation</span></span> | <span data-ttu-id="b54fd-175">WHSMobileAppStepDriverCheckOutConfirmation</span><span class="sxs-lookup"><span data-stu-id="b54fd-175">WHSMobileAppStepDriverCheckOutConfirmation</span></span> |
| <span data-ttu-id="b54fd-176">DriverCheckOutId</span><span class="sxs-lookup"><span data-stu-id="b54fd-176">DriverCheckOutId</span></span> | <span data-ttu-id="b54fd-177">WHSMobileAppStepDriverCheckOutId</span><span class="sxs-lookup"><span data-stu-id="b54fd-177">WHSMobileAppStepDriverCheckOutId</span></span> |
| <span data-ttu-id="b54fd-178">ExpDate</span><span class="sxs-lookup"><span data-stu-id="b54fd-178">ExpDate</span></span> | <span data-ttu-id="b54fd-179">WHSMobileAppStepExpDate</span><span class="sxs-lookup"><span data-stu-id="b54fd-179">WHSMobileAppStepExpDate</span></span> |
| <span data-ttu-id="b54fd-180">FromBatchDisposition</span><span class="sxs-lookup"><span data-stu-id="b54fd-180">FromBatchDisposition</span></span> | <span data-ttu-id="b54fd-181">WHSMobileAppStepFromBatchDisposition</span><span class="sxs-lookup"><span data-stu-id="b54fd-181">WHSMobileAppStepFromBatchDisposition</span></span> |
| <span data-ttu-id="b54fd-182">FromInventoryStatus</span><span class="sxs-lookup"><span data-stu-id="b54fd-182">FromInventoryStatus</span></span> | <span data-ttu-id="b54fd-183">WHSMobileAppStepInventoryStatusFrom</span><span class="sxs-lookup"><span data-stu-id="b54fd-183">WHSMobileAppStepInventoryStatusFrom</span></span> |
| <span data-ttu-id="b54fd-184">FullQty</span><span class="sxs-lookup"><span data-stu-id="b54fd-184">FullQty</span></span> | <span data-ttu-id="b54fd-185">WHSMobileAppStepFullQty</span><span class="sxs-lookup"><span data-stu-id="b54fd-185">WHSMobileAppStepFullQty</span></span> |
| <span data-ttu-id="b54fd-186">InboundPut</span><span class="sxs-lookup"><span data-stu-id="b54fd-186">InboundPut</span></span> | <span data-ttu-id="b54fd-187">WHSMobileAppStepInboundPut</span><span class="sxs-lookup"><span data-stu-id="b54fd-187">WHSMobileAppStepInboundPut</span></span> |
| <span data-ttu-id="b54fd-188">InventBatchId</span><span class="sxs-lookup"><span data-stu-id="b54fd-188">InventBatchId</span></span> | <span data-ttu-id="b54fd-189">WHSMobileAppStepBatch</span><span class="sxs-lookup"><span data-stu-id="b54fd-189">WHSMobileAppStepBatch</span></span> |
| <span data-ttu-id="b54fd-190">InventColorId</span><span class="sxs-lookup"><span data-stu-id="b54fd-190">InventColorId</span></span> | <span data-ttu-id="b54fd-191">WHSMobileAppStepInventColorId</span><span class="sxs-lookup"><span data-stu-id="b54fd-191">WHSMobileAppStepInventColorId</span></span> |
| <span data-ttu-id="b54fd-192">InventLocation</span><span class="sxs-lookup"><span data-stu-id="b54fd-192">InventLocation</span></span> | <span data-ttu-id="b54fd-193">WHSMobileAppStepInventLocation</span><span class="sxs-lookup"><span data-stu-id="b54fd-193">WHSMobileAppStepInventLocation</span></span> |
| <span data-ttu-id="b54fd-194">InventLocationId</span><span class="sxs-lookup"><span data-stu-id="b54fd-194">InventLocationId</span></span> | <span data-ttu-id="b54fd-195">WHSMobileAppStepWarehouse</span><span class="sxs-lookup"><span data-stu-id="b54fd-195">WHSMobileAppStepWarehouse</span></span> |
| <span data-ttu-id="b54fd-196">InventSerialId</span><span class="sxs-lookup"><span data-stu-id="b54fd-196">InventSerialId</span></span> | <span data-ttu-id="b54fd-197">WHSMobileAppStepInventSerialId</span><span class="sxs-lookup"><span data-stu-id="b54fd-197">WHSMobileAppStepInventSerialId</span></span> |
| <span data-ttu-id="b54fd-198">InventSizeId</span><span class="sxs-lookup"><span data-stu-id="b54fd-198">InventSizeId</span></span> | <span data-ttu-id="b54fd-199">WHSMobileAppStepInventSizeId</span><span class="sxs-lookup"><span data-stu-id="b54fd-199">WHSMobileAppStepInventSizeId</span></span> |
| <span data-ttu-id="b54fd-200">InventStatusId</span><span class="sxs-lookup"><span data-stu-id="b54fd-200">InventStatusId</span></span> | <span data-ttu-id="b54fd-201">WHSMobileAppStepInventStatus</span><span class="sxs-lookup"><span data-stu-id="b54fd-201">WHSMobileAppStepInventStatus</span></span> |
| <span data-ttu-id="b54fd-202">InventStyleId</span><span class="sxs-lookup"><span data-stu-id="b54fd-202">InventStyleId</span></span> | <span data-ttu-id="b54fd-203">WHSMobileAppStepInventStyleId</span><span class="sxs-lookup"><span data-stu-id="b54fd-203">WHSMobileAppStepInventStyleId</span></span> |
| <span data-ttu-id="b54fd-204">InventVersionId</span><span class="sxs-lookup"><span data-stu-id="b54fd-204">InventVersionId</span></span> | <span data-ttu-id="b54fd-205">WHSMobileAppStepInventVersionId</span><span class="sxs-lookup"><span data-stu-id="b54fd-205">WHSMobileAppStepInventVersionId</span></span> |
| <span data-ttu-id="b54fd-206">ItemId</span><span class="sxs-lookup"><span data-stu-id="b54fd-206">ItemId</span></span> | <span data-ttu-id="b54fd-207">WHSMobileAppStepItem</span><span class="sxs-lookup"><span data-stu-id="b54fd-207">WHSMobileAppStepItem</span></span> |
| <span data-ttu-id="b54fd-208">ITMContainerID</span><span class="sxs-lookup"><span data-stu-id="b54fd-208">ITMContainerID</span></span> | <span data-ttu-id="b54fd-209">ITMMobileAppStepContainerId</span><span class="sxs-lookup"><span data-stu-id="b54fd-209">ITMMobileAppStepContainerId</span></span> |
| <span data-ttu-id="b54fd-210">ITMShipmentID</span><span class="sxs-lookup"><span data-stu-id="b54fd-210">ITMShipmentID</span></span> | <span data-ttu-id="b54fd-211">ITMMobileAppStepShipmentId</span><span class="sxs-lookup"><span data-stu-id="b54fd-211">ITMMobileAppStepShipmentId</span></span> |
| <span data-ttu-id="b54fd-212">KanbanCardId</span><span class="sxs-lookup"><span data-stu-id="b54fd-212">KanbanCardId</span></span> | <span data-ttu-id="b54fd-213">WHSMobileAppStepKanbanCard</span><span class="sxs-lookup"><span data-stu-id="b54fd-213">WHSMobileAppStepKanbanCard</span></span> |
| <span data-ttu-id="b54fd-214">KanbanCardToEmpty</span><span class="sxs-lookup"><span data-stu-id="b54fd-214">KanbanCardToEmpty</span></span> | <span data-ttu-id="b54fd-215">WHSMobileAppStepKanbanCardToEmpty</span><span class="sxs-lookup"><span data-stu-id="b54fd-215">WHSMobileAppStepKanbanCardToEmpty</span></span> |
| <span data-ttu-id="b54fd-216">KanbanOrCardId</span><span class="sxs-lookup"><span data-stu-id="b54fd-216">KanbanOrCardId</span></span> | <span data-ttu-id="b54fd-217">WHSMobileAppStepKanbanCard</span><span class="sxs-lookup"><span data-stu-id="b54fd-217">WHSMobileAppStepKanbanCard</span></span> |
| <span data-ttu-id="b54fd-218">LicensePlateId</span><span class="sxs-lookup"><span data-stu-id="b54fd-218">LicensePlateId</span></span> | <span data-ttu-id="b54fd-219">WHSMobileAppStepLicensePlate</span><span class="sxs-lookup"><span data-stu-id="b54fd-219">WHSMobileAppStepLicensePlate</span></span> |
| <span data-ttu-id="b54fd-220">LoadId</span><span class="sxs-lookup"><span data-stu-id="b54fd-220">LoadId</span></span> | <span data-ttu-id="b54fd-221">WHSMobileAppStepLoadId</span><span class="sxs-lookup"><span data-stu-id="b54fd-221">WHSMobileAppStepLoadId</span></span> |
| <span data-ttu-id="b54fd-222">LocationLicensePlatePosition</span><span class="sxs-lookup"><span data-stu-id="b54fd-222">LocationLicensePlatePosition</span></span> | <span data-ttu-id="b54fd-223">WHSMobileAppStepLocationLicensePlatePosition</span><span class="sxs-lookup"><span data-stu-id="b54fd-223">WHSMobileAppStepLocationLicensePlatePosition</span></span> |
| <span data-ttu-id="b54fd-224">LocOrLP</span><span class="sxs-lookup"><span data-stu-id="b54fd-224">LocOrLP</span></span> | <span data-ttu-id="b54fd-225">WHSMobileAppStepLocOrLP</span><span class="sxs-lookup"><span data-stu-id="b54fd-225">WHSMobileAppStepLocOrLP</span></span> |
| <span data-ttu-id="b54fd-226">LocOrLP_From</span><span class="sxs-lookup"><span data-stu-id="b54fd-226">LocOrLP_From</span></span> | <span data-ttu-id="b54fd-227">WHSMobileAppStepLocOrLPFrom</span><span class="sxs-lookup"><span data-stu-id="b54fd-227">WHSMobileAppStepLocOrLPFrom</span></span> |
| <span data-ttu-id="b54fd-228">LocOrLP_To</span><span class="sxs-lookup"><span data-stu-id="b54fd-228">LocOrLP_To</span></span> | <span data-ttu-id="b54fd-229">WHSMobileAppStepLocOrLPTo</span><span class="sxs-lookup"><span data-stu-id="b54fd-229">WHSMobileAppStepLocOrLPTo</span></span> |
| <span data-ttu-id="b54fd-230">LocOrLPCheck</span><span class="sxs-lookup"><span data-stu-id="b54fd-230">LocOrLPCheck</span></span> | <span data-ttu-id="b54fd-231">WHSMobileAppStepLocOrLPCheck</span><span class="sxs-lookup"><span data-stu-id="b54fd-231">WHSMobileAppStepLocOrLPCheck</span></span> |
| <span data-ttu-id="b54fd-232">LocVerification</span><span class="sxs-lookup"><span data-stu-id="b54fd-232">LocVerification</span></span> | <span data-ttu-id="b54fd-233">WHSMobileAppStepLocVerification</span><span class="sxs-lookup"><span data-stu-id="b54fd-233">WHSMobileAppStepLocVerification</span></span> |
| <span data-ttu-id="b54fd-234">LPAdjustIn</span><span class="sxs-lookup"><span data-stu-id="b54fd-234">LPAdjustIn</span></span> | <span data-ttu-id="b54fd-235">WHSMobileAppStepLPAdjustIn</span><span class="sxs-lookup"><span data-stu-id="b54fd-235">WHSMobileAppStepLPAdjustIn</span></span> |
| <span data-ttu-id="b54fd-236">LPBreakChildLP</span><span class="sxs-lookup"><span data-stu-id="b54fd-236">LPBreakChildLP</span></span> | <span data-ttu-id="b54fd-237">WHSMobileAppStepLPBreakChildLP</span><span class="sxs-lookup"><span data-stu-id="b54fd-237">WHSMobileAppStepLPBreakChildLP</span></span> |
| <span data-ttu-id="b54fd-238">LPBreakParentLP</span><span class="sxs-lookup"><span data-stu-id="b54fd-238">LPBreakParentLP</span></span> | <span data-ttu-id="b54fd-239">WHSMobileAppStepLPBreakParentLP</span><span class="sxs-lookup"><span data-stu-id="b54fd-239">WHSMobileAppStepLPBreakParentLP</span></span> |
| <span data-ttu-id="b54fd-240">LPBuildChildLP</span><span class="sxs-lookup"><span data-stu-id="b54fd-240">LPBuildChildLP</span></span> | <span data-ttu-id="b54fd-241">WHSMobileAppStepLPBuildChildLP</span><span class="sxs-lookup"><span data-stu-id="b54fd-241">WHSMobileAppStepLPBuildChildLP</span></span> |
| <span data-ttu-id="b54fd-242">LPBuildParentLP</span><span class="sxs-lookup"><span data-stu-id="b54fd-242">LPBuildParentLP</span></span> | <span data-ttu-id="b54fd-243">WHSMobileAppStepLPBuildParentLP</span><span class="sxs-lookup"><span data-stu-id="b54fd-243">WHSMobileAppStepLPBuildParentLP</span></span> |
| <span data-ttu-id="b54fd-244">LPVerification</span><span class="sxs-lookup"><span data-stu-id="b54fd-244">LPVerification</span></span> | <span data-ttu-id="b54fd-245">WHSMobileAppStepLPVerification</span><span class="sxs-lookup"><span data-stu-id="b54fd-245">WHSMobileAppStepLPVerification</span></span> |
| <span data-ttu-id="b54fd-246">MergeContainerId</span><span class="sxs-lookup"><span data-stu-id="b54fd-246">MergeContainerId</span></span> | <span data-ttu-id="b54fd-247">WHSMobileAppStepMergeContainerId</span><span class="sxs-lookup"><span data-stu-id="b54fd-247">WHSMobileAppStepMergeContainerId</span></span> |
| <span data-ttu-id="b54fd-248">MixedLPLineNum</span><span class="sxs-lookup"><span data-stu-id="b54fd-248">MixedLPLineNum</span></span> | <span data-ttu-id="b54fd-249">WHSMobileAppStepMixedLPLineNum</span><span class="sxs-lookup"><span data-stu-id="b54fd-249">WHSMobileAppStepMixedLPLineNum</span></span> |
| <span data-ttu-id="b54fd-250">MobileDeviceQueueMessageCollectionIdentifierId</span><span class="sxs-lookup"><span data-stu-id="b54fd-250">MobileDeviceQueueMessageCollectionIdentifierId</span></span> | <span data-ttu-id="b54fd-251">WHSMobileAppStepSelectOrder</span><span class="sxs-lookup"><span data-stu-id="b54fd-251">WHSMobileAppStepSelectOrder</span></span> |
| <span data-ttu-id="b54fd-252">MovementConfirmCancel</span><span class="sxs-lookup"><span data-stu-id="b54fd-252">MovementConfirmCancel</span></span> | <span data-ttu-id="b54fd-253">WHSMobileAppStepMovementConfirmCancel</span><span class="sxs-lookup"><span data-stu-id="b54fd-253">WHSMobileAppStepMovementConfirmCancel</span></span> |
| <span data-ttu-id="b54fd-254">NewCaptureWeight</span><span class="sxs-lookup"><span data-stu-id="b54fd-254">NewCaptureWeight</span></span> | <span data-ttu-id="b54fd-255">WHSMobileAppStepCatchWeight</span><span class="sxs-lookup"><span data-stu-id="b54fd-255">WHSMobileAppStepCatchWeight</span></span> |
| <span data-ttu-id="b54fd-256">NewQty</span><span class="sxs-lookup"><span data-stu-id="b54fd-256">NewQty</span></span> | <span data-ttu-id="b54fd-257">WHSMobileAppStepNewQty</span><span class="sxs-lookup"><span data-stu-id="b54fd-257">WHSMobileAppStepNewQty</span></span> |
| <span data-ttu-id="b54fd-258">OutboundCatchWeightTag</span><span class="sxs-lookup"><span data-stu-id="b54fd-258">OutboundCatchWeightTag</span></span> | <span data-ttu-id="b54fd-259">WHSMobileAppStepCatchWeightTag</span><span class="sxs-lookup"><span data-stu-id="b54fd-259">WHSMobileAppStepCatchWeightTag</span></span> |
| <span data-ttu-id="b54fd-260">OutboundPut</span><span class="sxs-lookup"><span data-stu-id="b54fd-260">OutboundPut</span></span> | <span data-ttu-id="b54fd-261">WHSMobileAppStepOutboundPut</span><span class="sxs-lookup"><span data-stu-id="b54fd-261">WHSMobileAppStepOutboundPut</span></span> |
| <span data-ttu-id="b54fd-262">OutboundWeight</span><span class="sxs-lookup"><span data-stu-id="b54fd-262">OutboundWeight</span></span> | <span data-ttu-id="b54fd-263">WHSMobileAppStepCatchWeight</span><span class="sxs-lookup"><span data-stu-id="b54fd-263">WHSMobileAppStepCatchWeight</span></span> |
| <span data-ttu-id="b54fd-264">OverridePutNewLocation</span><span class="sxs-lookup"><span data-stu-id="b54fd-264">OverridePutNewLocation</span></span> | <span data-ttu-id="b54fd-265">WHSMobileAppStepOverridePutNewLocation</span><span class="sxs-lookup"><span data-stu-id="b54fd-265">WHSMobileAppStepOverridePutNewLocation</span></span> |
| <span data-ttu-id="b54fd-266">PieceByPieceConfirmation</span><span class="sxs-lookup"><span data-stu-id="b54fd-266">PieceByPieceConfirmation</span></span> | <span data-ttu-id="b54fd-267">WHSMobileAppStepQtyVerification</span><span class="sxs-lookup"><span data-stu-id="b54fd-267">WHSMobileAppStepQtyVerification</span></span> |
| <span data-ttu-id="b54fd-268">POLineNum</span><span class="sxs-lookup"><span data-stu-id="b54fd-268">POLineNum</span></span> | <span data-ttu-id="b54fd-269">WHSMobileAppStepPOLineNum</span><span class="sxs-lookup"><span data-stu-id="b54fd-269">WHSMobileAppStepPOLineNum</span></span> |
| <span data-ttu-id="b54fd-270">Innkaupanúmer</span><span class="sxs-lookup"><span data-stu-id="b54fd-270">PONum</span></span> | <span data-ttu-id="b54fd-271">WHSMobileAppStepPONum</span><span class="sxs-lookup"><span data-stu-id="b54fd-271">WHSMobileAppStepPONum</span></span> |
| <span data-ttu-id="b54fd-272">PositionFull</span><span class="sxs-lookup"><span data-stu-id="b54fd-272">PositionFull</span></span> | <span data-ttu-id="b54fd-273">WHSMobileAppStepPositionFull</span><span class="sxs-lookup"><span data-stu-id="b54fd-273">WHSMobileAppStepPositionFull</span></span> |
| <span data-ttu-id="b54fd-274">PositionFullQty</span><span class="sxs-lookup"><span data-stu-id="b54fd-274">PositionFullQty</span></span> | <span data-ttu-id="b54fd-275">WHSMobileAppStepPositionFullQty</span><span class="sxs-lookup"><span data-stu-id="b54fd-275">WHSMobileAppStepPositionFullQty</span></span> |
| <span data-ttu-id="b54fd-276">Styrkleiki</span><span class="sxs-lookup"><span data-stu-id="b54fd-276">Potency</span></span> | <span data-ttu-id="b54fd-277">WHSMobileAppStepPotency</span><span class="sxs-lookup"><span data-stu-id="b54fd-277">WHSMobileAppStepPotency</span></span> |
| <span data-ttu-id="b54fd-278">PrinterName</span><span class="sxs-lookup"><span data-stu-id="b54fd-278">PrinterName</span></span> | <span data-ttu-id="b54fd-279">WHSMobileAppStepPrinterName</span><span class="sxs-lookup"><span data-stu-id="b54fd-279">WHSMobileAppStepPrinterName</span></span> |
| <span data-ttu-id="b54fd-280">ProdId</span><span class="sxs-lookup"><span data-stu-id="b54fd-280">ProdId</span></span> | <span data-ttu-id="b54fd-281">WHSMobileAppStepProdId</span><span class="sxs-lookup"><span data-stu-id="b54fd-281">WHSMobileAppStepProdId</span></span> |
| <span data-ttu-id="b54fd-282">ProdLastPalletConfirmation</span><span class="sxs-lookup"><span data-stu-id="b54fd-282">ProdLastPalletConfirmation</span></span> | <span data-ttu-id="b54fd-283">WHSMobileAppStepProdLastPalletConfirmation</span><span class="sxs-lookup"><span data-stu-id="b54fd-283">WHSMobileAppStepProdLastPalletConfirmation</span></span> |
| <span data-ttu-id="b54fd-284">ProductConfirmation</span><span class="sxs-lookup"><span data-stu-id="b54fd-284">ProductConfirmation</span></span> | <span data-ttu-id="b54fd-285">WHSMobileAppStepProductConfirmation</span><span class="sxs-lookup"><span data-stu-id="b54fd-285">WHSMobileAppStepProductConfirmation</span></span> |
| <span data-ttu-id="b54fd-286">ProductionScrapConfirmation</span><span class="sxs-lookup"><span data-stu-id="b54fd-286">ProductionScrapConfirmation</span></span> | <span data-ttu-id="b54fd-287">WHSMobileAppStepProductionScrapConfirmation</span><span class="sxs-lookup"><span data-stu-id="b54fd-287">WHSMobileAppStepProductionScrapConfirmation</span></span> |
| <span data-ttu-id="b54fd-288">Frágangur</span><span class="sxs-lookup"><span data-stu-id="b54fd-288">Put</span></span> | <span data-ttu-id="b54fd-289">WHSMobileAppStepPut</span><span class="sxs-lookup"><span data-stu-id="b54fd-289">WHSMobileAppStepPut</span></span> |
| <span data-ttu-id="b54fd-290">PutawayClusterId</span><span class="sxs-lookup"><span data-stu-id="b54fd-290">PutawayClusterId</span></span> | <span data-ttu-id="b54fd-291">WHSMobileAppStepPutawayClusterId</span><span class="sxs-lookup"><span data-stu-id="b54fd-291">WHSMobileAppStepPutawayClusterId</span></span> |
| <span data-ttu-id="b54fd-292">Magn</span><span class="sxs-lookup"><span data-stu-id="b54fd-292">Qty</span></span> | <span data-ttu-id="b54fd-293">WHSMobileAppStepQty</span><span class="sxs-lookup"><span data-stu-id="b54fd-293">WHSMobileAppStepQty</span></span> |
| <span data-ttu-id="b54fd-294">QtyAdjust</span><span class="sxs-lookup"><span data-stu-id="b54fd-294">QtyAdjust</span></span> | <span data-ttu-id="b54fd-295">WHSMobileAppStepQtyAdjust</span><span class="sxs-lookup"><span data-stu-id="b54fd-295">WHSMobileAppStepQtyAdjust</span></span> |
| <span data-ttu-id="b54fd-296">QtyShort</span><span class="sxs-lookup"><span data-stu-id="b54fd-296">QtyShort</span></span> | <span data-ttu-id="b54fd-297">WHSMobileAppStepQtyShort</span><span class="sxs-lookup"><span data-stu-id="b54fd-297">WHSMobileAppStepQtyShort</span></span> |
| <span data-ttu-id="b54fd-298">QtyToConsume</span><span class="sxs-lookup"><span data-stu-id="b54fd-298">QtyToConsume</span></span> | <span data-ttu-id="b54fd-299">WHSMobileAppStepQtyToConsume</span><span class="sxs-lookup"><span data-stu-id="b54fd-299">WHSMobileAppStepQtyToConsume</span></span> |
| <span data-ttu-id="b54fd-300">QtyToPick</span><span class="sxs-lookup"><span data-stu-id="b54fd-300">QtyToPick</span></span> | <span data-ttu-id="b54fd-301">WHSMobileAppStepQtyToPick</span><span class="sxs-lookup"><span data-stu-id="b54fd-301">WHSMobileAppStepQtyToPick</span></span> |
| <span data-ttu-id="b54fd-302">QtyToPut</span><span class="sxs-lookup"><span data-stu-id="b54fd-302">QtyToPut</span></span> | <span data-ttu-id="b54fd-303">WHSMobileAppStepQtyToPut</span><span class="sxs-lookup"><span data-stu-id="b54fd-303">WHSMobileAppStepQtyToPut</span></span> |
| <span data-ttu-id="b54fd-304">QtyToScrap</span><span class="sxs-lookup"><span data-stu-id="b54fd-304">QtyToScrap</span></span> | <span data-ttu-id="b54fd-305">WHSMobileAppStepQtyToScrap</span><span class="sxs-lookup"><span data-stu-id="b54fd-305">WHSMobileAppStepQtyToScrap</span></span> |
| <span data-ttu-id="b54fd-306">QtyVerification</span><span class="sxs-lookup"><span data-stu-id="b54fd-306">QtyVerification</span></span> | <span data-ttu-id="b54fd-307">WHSMobileAppStepQtyVerification</span><span class="sxs-lookup"><span data-stu-id="b54fd-307">WHSMobileAppStepQtyVerification</span></span> |
| <span data-ttu-id="b54fd-308">QtyWithScanningLimit</span><span class="sxs-lookup"><span data-stu-id="b54fd-308">QtyWithScanningLimit</span></span> | <span data-ttu-id="b54fd-309">WHSMobileAppStepQtyAdjust</span><span class="sxs-lookup"><span data-stu-id="b54fd-309">WHSMobileAppStepQtyAdjust</span></span> |
| <span data-ttu-id="b54fd-310">ReasonString</span><span class="sxs-lookup"><span data-stu-id="b54fd-310">ReasonString</span></span> | <span data-ttu-id="b54fd-311">WHSMobileAppStepReasonString</span><span class="sxs-lookup"><span data-stu-id="b54fd-311">WHSMobileAppStepReasonString</span></span> |
| <span data-ttu-id="b54fd-312">RecvLocationId</span><span class="sxs-lookup"><span data-stu-id="b54fd-312">RecvLocationId</span></span> | <span data-ttu-id="b54fd-313">WHSMobileAppStepRecvLocationId</span><span class="sxs-lookup"><span data-stu-id="b54fd-313">WHSMobileAppStepRecvLocationId</span></span> |
| <span data-ttu-id="b54fd-314">RemoveContainerId</span><span class="sxs-lookup"><span data-stu-id="b54fd-314">RemoveContainerId</span></span> | <span data-ttu-id="b54fd-315">WHSMobileAppStepRemoveContainerId</span><span class="sxs-lookup"><span data-stu-id="b54fd-315">WHSMobileAppStepRemoveContainerId</span></span> |
| <span data-ttu-id="b54fd-316">ReprintLabelConfirmation</span><span class="sxs-lookup"><span data-stu-id="b54fd-316">ReprintLabelConfirmation</span></span> | <span data-ttu-id="b54fd-317">WHSMobileAppStepReprintLabelConfirmation</span><span class="sxs-lookup"><span data-stu-id="b54fd-317">WHSMobileAppStepReprintLabelConfirmation</span></span> |
| <span data-ttu-id="b54fd-318">RMANum</span><span class="sxs-lookup"><span data-stu-id="b54fd-318">RMANum</span></span> | <span data-ttu-id="b54fd-319">WHSMobileAppStepRMANum</span><span class="sxs-lookup"><span data-stu-id="b54fd-319">WHSMobileAppStepRMANum</span></span> |
| <span data-ttu-id="b54fd-320">ShortPickReason</span><span class="sxs-lookup"><span data-stu-id="b54fd-320">ShortPickReason</span></span> | <span data-ttu-id="b54fd-321">WHSMobileAppStepShortPickReason</span><span class="sxs-lookup"><span data-stu-id="b54fd-321">WHSMobileAppStepShortPickReason</span></span> |
| <span data-ttu-id="b54fd-322">SortConOrLP</span><span class="sxs-lookup"><span data-stu-id="b54fd-322">SortConOrLP</span></span> | <span data-ttu-id="b54fd-323">WHSMobileAppStepSortConOrLP</span><span class="sxs-lookup"><span data-stu-id="b54fd-323">WHSMobileAppStepSortConOrLP</span></span> |
| <span data-ttu-id="b54fd-324">SortLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="b54fd-324">SortLicensePlateId</span></span> | <span data-ttu-id="b54fd-325">WHSMobileAppStepSortLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="b54fd-325">WHSMobileAppStepSortLicensePlateId</span></span> |
| <span data-ttu-id="b54fd-326">SortPositionId</span><span class="sxs-lookup"><span data-stu-id="b54fd-326">SortPositionId</span></span> | <span data-ttu-id="b54fd-327">WHSMobileAppStepSortPositionId</span><span class="sxs-lookup"><span data-stu-id="b54fd-327">WHSMobileAppStepSortPositionId</span></span> |
| <span data-ttu-id="b54fd-328">SortVerification</span><span class="sxs-lookup"><span data-stu-id="b54fd-328">SortVerification</span></span> | <span data-ttu-id="b54fd-329">WHSMobileAppStepSortVerification</span><span class="sxs-lookup"><span data-stu-id="b54fd-329">WHSMobileAppStepSortVerification</span></span> |
| <span data-ttu-id="b54fd-330">StartLocationId</span><span class="sxs-lookup"><span data-stu-id="b54fd-330">StartLocationId</span></span> | <span data-ttu-id="b54fd-331">WHSMobileAppStepStartLocationId</span><span class="sxs-lookup"><span data-stu-id="b54fd-331">WHSMobileAppStepStartLocationId</span></span> |
| <span data-ttu-id="b54fd-332">StartProdOrderConfirmation</span><span class="sxs-lookup"><span data-stu-id="b54fd-332">StartProdOrderConfirmation</span></span> | <span data-ttu-id="b54fd-333">WHSMobileAppStepStartProdOrderConfirmation</span><span class="sxs-lookup"><span data-stu-id="b54fd-333">WHSMobileAppStepStartProdOrderConfirmation</span></span> |
| <span data-ttu-id="b54fd-334">TargetLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="b54fd-334">TargetLicensePlateId</span></span> | <span data-ttu-id="b54fd-335">WHSMobileAppStepTargetLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="b54fd-335">WHSMobileAppStepTargetLicensePlateId</span></span> |
| <span data-ttu-id="b54fd-336">TOLineNum</span><span class="sxs-lookup"><span data-stu-id="b54fd-336">TOLineNum</span></span> | <span data-ttu-id="b54fd-337">WHSMobileAppStepTOLineNum</span><span class="sxs-lookup"><span data-stu-id="b54fd-337">WHSMobileAppStepTOLineNum</span></span> |
| <span data-ttu-id="b54fd-338">ToLocation</span><span class="sxs-lookup"><span data-stu-id="b54fd-338">ToLocation</span></span> | <span data-ttu-id="b54fd-339">WHSMobileAppStepToLocation</span><span class="sxs-lookup"><span data-stu-id="b54fd-339">WHSMobileAppStepToLocation</span></span> |
| <span data-ttu-id="b54fd-340">TONum</span><span class="sxs-lookup"><span data-stu-id="b54fd-340">TONum</span></span> | <span data-ttu-id="b54fd-341">WHSMobileAppStepTONum</span><span class="sxs-lookup"><span data-stu-id="b54fd-341">WHSMobileAppStepTONum</span></span> |
| <span data-ttu-id="b54fd-342">ToWarehouse</span><span class="sxs-lookup"><span data-stu-id="b54fd-342">ToWarehouse</span></span> | <span data-ttu-id="b54fd-343">WHSMobileAppStepWarehouseTo</span><span class="sxs-lookup"><span data-stu-id="b54fd-343">WHSMobileAppStepWarehouseTo</span></span> |
| <span data-ttu-id="b54fd-344">TransportLoadId</span><span class="sxs-lookup"><span data-stu-id="b54fd-344">TransportLoadId</span></span> | <span data-ttu-id="b54fd-345">WHSMobileAppStepTransportLoadId</span><span class="sxs-lookup"><span data-stu-id="b54fd-345">WHSMobileAppStepTransportLoadId</span></span> |
| <span data-ttu-id="b54fd-346">WaveLabelId</span><span class="sxs-lookup"><span data-stu-id="b54fd-346">WaveLabelId</span></span> | <span data-ttu-id="b54fd-347">WHSMobileAppStepWaveLabelId</span><span class="sxs-lookup"><span data-stu-id="b54fd-347">WHSMobileAppStepWaveLabelId</span></span> |
| <span data-ttu-id="b54fd-348">WaveLblQty</span><span class="sxs-lookup"><span data-stu-id="b54fd-348">WaveLblQty</span></span> | <span data-ttu-id="b54fd-349">WHSMobileAppStepWaveLblQty</span><span class="sxs-lookup"><span data-stu-id="b54fd-349">WHSMobileAppStepWaveLblQty</span></span> |
| <span data-ttu-id="b54fd-350">Vægi</span><span class="sxs-lookup"><span data-stu-id="b54fd-350">Weight</span></span> | <span data-ttu-id="b54fd-351">WHSMobileAppStepWeight</span><span class="sxs-lookup"><span data-stu-id="b54fd-351">WHSMobileAppStepWeight</span></span> |
| <span data-ttu-id="b54fd-352">WeightToConsume</span><span class="sxs-lookup"><span data-stu-id="b54fd-352">WeightToConsume</span></span> | <span data-ttu-id="b54fd-353">WHSMobileAppStepWeightToConsume</span><span class="sxs-lookup"><span data-stu-id="b54fd-353">WHSMobileAppStepWeightToConsume</span></span> |
| <span data-ttu-id="b54fd-354">WHSAdjustmentType</span><span class="sxs-lookup"><span data-stu-id="b54fd-354">WHSAdjustmentType</span></span> | <span data-ttu-id="b54fd-355">WHSMobileAppStepWHSAdjustmentType</span><span class="sxs-lookup"><span data-stu-id="b54fd-355">WHSMobileAppStepWHSAdjustmentType</span></span> |
| <span data-ttu-id="b54fd-356">WHSReceivingException</span><span class="sxs-lookup"><span data-stu-id="b54fd-356">WHSReceivingException</span></span> | <span data-ttu-id="b54fd-357">WHSMobileAppStepWHSReceivingException</span><span class="sxs-lookup"><span data-stu-id="b54fd-357">WHSMobileAppStepWHSReceivingException</span></span> |
| <span data-ttu-id="b54fd-358">WHSWorkException</span><span class="sxs-lookup"><span data-stu-id="b54fd-358">WHSWorkException</span></span> | <span data-ttu-id="b54fd-359">WHSMobileAppStepWHSWorkException</span><span class="sxs-lookup"><span data-stu-id="b54fd-359">WHSMobileAppStepWHSWorkException</span></span> |
| <span data-ttu-id="b54fd-360">WHSWorkLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="b54fd-360">WHSWorkLicensePlateId</span></span> | <span data-ttu-id="b54fd-361">WHSMobileAppStepWorkLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="b54fd-361">WHSMobileAppStepWorkLicensePlateId</span></span> |
| <span data-ttu-id="b54fd-362">WMSLocationId</span><span class="sxs-lookup"><span data-stu-id="b54fd-362">WMSLocationId</span></span> | <span data-ttu-id="b54fd-363">WHSMobileAppStepLocation</span><span class="sxs-lookup"><span data-stu-id="b54fd-363">WHSMobileAppStepLocation</span></span> |
| <span data-ttu-id="b54fd-364">WorkId</span><span class="sxs-lookup"><span data-stu-id="b54fd-364">WorkId</span></span> | <span data-ttu-id="b54fd-365">WHSMobileAppStepWorkId</span><span class="sxs-lookup"><span data-stu-id="b54fd-365">WHSMobileAppStepWorkId</span></span> |
| <span data-ttu-id="b54fd-366">WorkIdToCancel</span><span class="sxs-lookup"><span data-stu-id="b54fd-366">WorkIdToCancel</span></span> | <span data-ttu-id="b54fd-367">WHSMobileAppStepWorkIdToCancel</span><span class="sxs-lookup"><span data-stu-id="b54fd-367">WHSMobileAppStepWorkIdToCancel</span></span> |
| <span data-ttu-id="b54fd-368">WorkLPIdPutawayCluster</span><span class="sxs-lookup"><span data-stu-id="b54fd-368">WorkLPIdPutawayCluster</span></span> | <span data-ttu-id="b54fd-369">WHSMobileAppStepWorkLPIdPutawayCluster</span><span class="sxs-lookup"><span data-stu-id="b54fd-369">WHSMobileAppStepWorkLPIdPutawayCluster</span></span> |
| <span data-ttu-id="b54fd-370">WorkPoolId</span><span class="sxs-lookup"><span data-stu-id="b54fd-370">WorkPoolId</span></span> | <span data-ttu-id="b54fd-371">WHSMobileAppStepWorkPoolId</span><span class="sxs-lookup"><span data-stu-id="b54fd-371">WHSMobileAppStepWorkPoolId</span></span> |
| <span data-ttu-id="b54fd-372">ZoneId</span><span class="sxs-lookup"><span data-stu-id="b54fd-372">ZoneId</span></span> | <span data-ttu-id="b54fd-373">WHSMobileAppStepZoneId</span><span class="sxs-lookup"><span data-stu-id="b54fd-373">WHSMobileAppStepZoneId</span></span> |

### <a name="available-step-icons"></a><a name="step-icons"></a><span data-ttu-id="b54fd-374">Tiltæk skrefatákn</span><span class="sxs-lookup"><span data-stu-id="b54fd-374">Available step icons</span></span>

<span data-ttu-id="b54fd-375">Kerfið inniheldur safn staðlaðra skrefatákna sem er einnig hægt að nota fyrir sérstilltu skrefin.</span><span class="sxs-lookup"><span data-stu-id="b54fd-375">The system includes a collection of standard step icons that you can also use for your custom steps.</span></span> <span data-ttu-id="b54fd-376">Ekki er hægt að hlaða upp sérsniðnum skrefatáknum eins og er.</span><span class="sxs-lookup"><span data-stu-id="b54fd-376">You can't currently upload custom step icons.</span></span> <span data-ttu-id="b54fd-377">Því þarf alltaf að velja eitt af stöðluðu skrefatáknunum.</span><span class="sxs-lookup"><span data-stu-id="b54fd-377">Therefore, you must always select one of the standard step icons.</span></span>

<span data-ttu-id="b54fd-378">Eftirfarandi tafla sýnir hvert staðlað skrefatákn sem er í boði sem stendur og heiti þess.</span><span class="sxs-lookup"><span data-stu-id="b54fd-378">The following table shows every standard step icon that is currently available, and its name.</span></span>

<table>
<tbody>
<tr>
<td><img src="media/step-icons-about.png" alt="About step icon" title="Um skrefatákn"><br><span data-ttu-id="b54fd-380">Um</span><span class="sxs-lookup"><span data-stu-id="b54fd-380">About</span></span></td>
<td><img src="media/step-icons-add-lp.png" alt="Add license plate or item step icon" title="Bæta við númeraplötu eða skrefatákni atriðis"><br><span data-ttu-id="b54fd-382">AddLpOrItem</span><span class="sxs-lookup"><span data-stu-id="b54fd-382">AddLpOrItem</span></span></td>
<td><img src="media/step-icons-batch-disposition.png" alt="Batch disposition step icon" title="Skrefatákn ráðstöfunarrunu"><br><span data-ttu-id="b54fd-384">BatchDisposition</span><span class="sxs-lookup"><span data-stu-id="b54fd-384">BatchDisposition</span></span></td>
<td><img src="media/step-icons-carrier.png" alt="Carrier step icon" title="Skrefatákn flutningsaðila"><br><span data-ttu-id="b54fd-386">Flutningsaðili</span><span class="sxs-lookup"><span data-stu-id="b54fd-386">Carrier</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-cw-tag.png" alt="Catch weight tag step icon" title="Skrefatákn framleiðsluþyngdarmerkis"><br><span data-ttu-id="b54fd-388">CatchWeightTag</span><span class="sxs-lookup"><span data-stu-id="b54fd-388">CatchWeightTag</span></span></td>
<td><img src="media/step-icons-cw-tag-weight.png" alt="Catch weight tag weight step icon" title="Skrefatákn þyngdarmerkingar framleiðsluþyngdar"><br><span data-ttu-id="b54fd-390">CatchWeightTagWeight</span><span class="sxs-lookup"><span data-stu-id="b54fd-390">CatchWeightTagWeight</span></span></td>
<td><img src="media/step-icons-check-digit.png" alt="Check digit step icon" title="Skrefatákn vartölu"><br><span data-ttu-id="b54fd-392">CheckDigit</span><span class="sxs-lookup"><span data-stu-id="b54fd-392">CheckDigit</span></span></td>
<td><img src="media/step-icons-check-in-out.png" alt="Check in or out ID step icon" title="Skrefatákn inn- eða útskráningarkennis"><br><span data-ttu-id="b54fd-394">CheckInOutId</span><span class="sxs-lookup"><span data-stu-id="b54fd-394">CheckInOutId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-child-lp.png" alt="Child license plate step icon" title="Skrefatákn undireiningar númeraplötu"><br><span data-ttu-id="b54fd-396">ChildLP</span><span class="sxs-lookup"><span data-stu-id="b54fd-396">ChildLP</span></span></td>
<td><img src="media/step-icons-cluster-id.png" alt="Cluster ID step icon" title="Skrefatákn klasakennis"><br><span data-ttu-id="b54fd-398">ClusterId</span><span class="sxs-lookup"><span data-stu-id="b54fd-398">ClusterId</span></span></td>
<td><img src="media/step-icons-cluster-position.png" alt="Cluster position step icon" title="Skrefatákn klasastaðsetningar"><br><span data-ttu-id="b54fd-400">ClusterPosition</span><span class="sxs-lookup"><span data-stu-id="b54fd-400">ClusterPosition</span></span></td>
<td><img src="media/step-icons-config-id.png" alt="Config ID step icon" title="Skrefatákn skilgreiningarkennis"><br><span data-ttu-id="b54fd-402">ConfigId</span><span class="sxs-lookup"><span data-stu-id="b54fd-402">ConfigId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-configured-field.png" alt="Configured field step icon" title="Skrefatákn skilgreinds reits"><br><span data-ttu-id="b54fd-404">ConfiguredField</span><span class="sxs-lookup"><span data-stu-id="b54fd-404">ConfiguredField</span></span></td>
<td><img src="media/step-icons-con-lp.png" alt="Con or LP step icon" title="Skrefatákn gáms eða númeraplötu"><br><span data-ttu-id="b54fd-406">ConOrLP</span><span class="sxs-lookup"><span data-stu-id="b54fd-406">ConOrLP</span></span></td>
<td><img src="media/step-icons-consolidate-from-LP.png" alt="Consolidate from license plate ID step icon" title="Skrefatákn sameiningar frá númeraplötukenni"><br><span data-ttu-id="b54fd-408">ConsolidateFromLicensePlateID</span><span class="sxs-lookup"><span data-stu-id="b54fd-408">ConsolidateFromLicensePlateID</span></span></td>
<td><img src="media/step-icons-consolidate-to-LP.png" alt="Consolidate to license plate ID step icon" title="Skrefatákn sameiningar til númeraplötukennis"><br><span data-ttu-id="b54fd-410">ConsolidateToLicensePlateID</span><span class="sxs-lookup"><span data-stu-id="b54fd-410">ConsolidateToLicensePlateID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-container-type.png" alt="Container type step icon" title="Skrefatákn gámagerðar"><br><span data-ttu-id="b54fd-412">ContainerType</span><span class="sxs-lookup"><span data-stu-id="b54fd-412">ContainerType</span></span></td>
<td><img src="media/step-icons-counting.png" alt="Counting step icon" title="Skrefatákn talningar"><br><span data-ttu-id="b54fd-414">Talning</span><span class="sxs-lookup"><span data-stu-id="b54fd-414">Counting</span></span></td>
<td><img src="media/step-icons-counting-reason.png" alt="Counting reason code step icon" title="Skrefatákn ástæðukóða talningar"><br><span data-ttu-id="b54fd-416">CountingReasonCode</span><span class="sxs-lookup"><span data-stu-id="b54fd-416">CountingReasonCode</span></span></td>
<td><img src="media/step-icons-country-origin.png" alt="Country of origin code step icon" title="Skrefatákn kóða upprunalands"><br><span data-ttu-id="b54fd-418">CountryOfOrigin</span><span class="sxs-lookup"><span data-stu-id="b54fd-418">CountryOfOrigin</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-disposition.png" alt="Disposition step icon" title="Skrefatákn förgunar"><br><span data-ttu-id="b54fd-420">Förgun</span><span class="sxs-lookup"><span data-stu-id="b54fd-420">Disposition</span></span></td>
<td><img src="media/step-icons-done.png" alt="Done step icon" title="Skrefatákn lokaskrefs"><br><span data-ttu-id="b54fd-422">Lokið</span><span class="sxs-lookup"><span data-stu-id="b54fd-422">Done</span></span></td>
<td><img src="media/step-icons-driver-check-in-confirmation.png" alt="Driver check in confirmation step icon" title="Skrefatákn staðfestingar á innskráningu ökumanns"><br><span data-ttu-id="b54fd-424">DriverCheckInConfirmation</span><span class="sxs-lookup"><span data-stu-id="b54fd-424">DriverCheckInConfirmation</span></span></td>
<td><img src="media/step-icons-driver-check-in-id.png" alt="Driver check in ID step icon" title="Skrefatákn innskráningarkennis ökumanns"><br><span data-ttu-id="b54fd-426">DriverCheckInId</span><span class="sxs-lookup"><span data-stu-id="b54fd-426">DriverCheckInId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-driver-check-out-id.png" alt="Driver check out ID step icon" title="Skrefatákn útskráningarkennis ökumanns"><br><span data-ttu-id="b54fd-428">DriverCheckOutId</span><span class="sxs-lookup"><span data-stu-id="b54fd-428">DriverCheckOutId</span></span></td>
<td><img src="media/step-icons-exp-date.png" alt="Expiration date step icon" title="Skrefatákn lokadagsetningar"><br><span data-ttu-id="b54fd-430">ExpDate</span><span class="sxs-lookup"><span data-stu-id="b54fd-430">ExpDate</span></span></td>
<td><img src="media/step-icons-field.png" alt="Field step icon" title="Skrefatákn svæðis"><br><span data-ttu-id="b54fd-432">Svæði</span><span class="sxs-lookup"><span data-stu-id="b54fd-432">Field</span></span></td>
<td><img src="media/step-icons-from-batch.png" alt="From batch disposition step icon" title="Skrefatákn frá ráðstöfunarrunu"><br><span data-ttu-id="b54fd-434">FromBatchDisposition</span><span class="sxs-lookup"><span data-stu-id="b54fd-434">FromBatchDisposition</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-from-inventory-status.png" alt="From inventory status step icon" title="Skrefatákn frá birgðastöðu"><br><span data-ttu-id="b54fd-436">FromInventoryStatus</span><span class="sxs-lookup"><span data-stu-id="b54fd-436">FromInventoryStatus</span></span></td>
<td><img src="media/step-icons-id-attribute.png" alt="ID attribute step icon" title="Skrefatákn eigindarkennis"><br><span data-ttu-id="b54fd-438">IdAttribute</span><span class="sxs-lookup"><span data-stu-id="b54fd-438">IdAttribute</span></span></td>
<td><img src="media/step-icons-invent-batch-id.png" alt="Inventory batch ID step icon" title="Skrefatákn birgðarrunukennis"><br><span data-ttu-id="b54fd-440">InventBatchID</span><span class="sxs-lookup"><span data-stu-id="b54fd-440">InventBatchID</span></span></td>
<td><img src="media/step-icons-invent-color-id.png" alt="Inventory color ID step icon" title="Skrefatákn litakennis birgða"><br><span data-ttu-id="b54fd-442">InventColorID</span><span class="sxs-lookup"><span data-stu-id="b54fd-442">InventColorID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-invent-location.png" alt="Inventory location step icon" title="Skrefatákn birgðastaðsetningar"><br><span data-ttu-id="b54fd-444">InventLocation</span><span class="sxs-lookup"><span data-stu-id="b54fd-444">InventLocation</span></span></td>
<td><img src="media/step-icons-invent-serial-id.png" alt="Inventory serial ID step icon" title="Skrefatákn raðnúmerakennis birgða"><br><span data-ttu-id="b54fd-446">InventSerialID</span><span class="sxs-lookup"><span data-stu-id="b54fd-446">InventSerialID</span></span></td>
<td><img src="media/step-icons-invent-size-id.png" alt="Inventory size ID step icon" title="Skrefatákn stærðarkennis birgða"><br><span data-ttu-id="b54fd-448">InventSizeID</span><span class="sxs-lookup"><span data-stu-id="b54fd-448">InventSizeID</span></span></td>
<td><img src="media/step-icons-invent-status-id.png" alt="Inventory status ID step icon" title="Skrefatákn birgðastöðukennis"><br><span data-ttu-id="b54fd-450">InventStatusID</span><span class="sxs-lookup"><span data-stu-id="b54fd-450">InventStatusID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-invent-style-id.png" alt="Inventory style ID step icon" title="Skrefatákn birgðastílkennis"><br><span data-ttu-id="b54fd-452">InventStyleID</span><span class="sxs-lookup"><span data-stu-id="b54fd-452">InventStyleID</span></span></td>
<td><img src="media/step-icons-invent-version-id.png" alt="Inventory version ID step icon" title="Skrefatákn útgáfukennis birgða"><br><span data-ttu-id="b54fd-454">InventVersionID</span><span class="sxs-lookup"><span data-stu-id="b54fd-454">InventVersionID</span></span></td>
<td><img src="media/step-icons-item-id.png" alt="Item ID step icon" title="Skrefatákn vörukennis"><br><span data-ttu-id="b54fd-456">ItemID</span><span class="sxs-lookup"><span data-stu-id="b54fd-456">ItemID</span></span></td>
<td><img src="media/step-icons-itm-contianer-id.png" alt="ITM container ID step icon" title="Skrefatákn ITM-gáms"><br><span data-ttu-id="b54fd-458">ITMContainerID</span><span class="sxs-lookup"><span data-stu-id="b54fd-458">ITMContainerID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-itm-shipment-id.png" alt="ITM shipment ID step icon" title="Skrefatákn ITM-sendingarkennis"><br><span data-ttu-id="b54fd-460">ITMShipmentID</span><span class="sxs-lookup"><span data-stu-id="b54fd-460">ITMShipmentID</span></span></td>
<td><img src="media/step-icons-kanban-card-id.png" alt="Kanban card ID step icon" title="Skrefatákn kanban-spjaldkennis"><br><span data-ttu-id="b54fd-462">KanbanCardID</span><span class="sxs-lookup"><span data-stu-id="b54fd-462">KanbanCardID</span></span></td>
<td><img src="media/step-icons-kanban-or-card-id.png" alt="Kanban or card ID step icon" title="Skrefatákn kanban- eða spjaldkennis"><br><span data-ttu-id="b54fd-464">KanbanOrCardID</span><span class="sxs-lookup"><span data-stu-id="b54fd-464">KanbanOrCardID</span></span></td>
<td><img src="media/step-icons-license-plate-id.png" alt="License plate ID step icon" title="Skrefatákn númeraplötukennis"><br><span data-ttu-id="b54fd-466">LicensePlateID</span><span class="sxs-lookup"><span data-stu-id="b54fd-466">LicensePlateID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-load-id.png" alt="Load ID step icon" title="Skrefatákn hleðslukennis"><br><span data-ttu-id="b54fd-468">LoadId</span><span class="sxs-lookup"><span data-stu-id="b54fd-468">LoadId</span></span></td>
<td><img src="media/step-icons-location-lp-pos.png" alt="Location license plate position step icon" title="Skrefatákn númeraplötustaðsetningar"><br><span data-ttu-id="b54fd-470">LocationLicensePlatePosition</span><span class="sxs-lookup"><span data-stu-id="b54fd-470">LocationLicensePlatePosition</span></span></td>
<td><img src="media/step-icons-location-or-lp.png" alt="Location or license plate step icon" title="Skrefatákn staðsetningar eða númeraplötu"><br><span data-ttu-id="b54fd-472">LocOrLP</span><span class="sxs-lookup"><span data-stu-id="b54fd-472">LocOrLP</span></span></td>
<td><img src="media/step-icons-location-or-lp-check.png" alt="Location or license plate check step icon" title="Skrefatákn athugunar staðsetningar eða númeraplötu"><br><span data-ttu-id="b54fd-474">LocOrLPCheck</span><span class="sxs-lookup"><span data-stu-id="b54fd-474">LocOrLPCheck</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-location-or-lp-from.png" alt="Location or license plate from step icon" title="Skrefatákn staðsetningar eða númeraplötu frá"><br><span data-ttu-id="b54fd-476">LocOrLPFrom</span><span class="sxs-lookup"><span data-stu-id="b54fd-476">LocOrLPFrom</span></span></td>
<td><img src="media/step-icons-location-or-lp-to.png" alt="Location or license plate to step icon" title="Skrefatákn staðsetningar eða númeraplötu til"><br><span data-ttu-id="b54fd-478">LocOrLPTo</span><span class="sxs-lookup"><span data-stu-id="b54fd-478">LocOrLPTo</span></span></td>
<td><img src="media/step-icons-long-process-complete.png" alt="Long process completed step icon" title="Skrefatákn langs ferlis lokið"><br><span data-ttu-id="b54fd-480">LongProcessCompleted</span><span class="sxs-lookup"><span data-stu-id="b54fd-480">LongProcessCompleted</span></span></td>
<td><img src="media/step-icons-lp-break-parent.png" alt="LP break parent LP step icon" title="Skrefatákn sundurliðunar á yfirnúmeraplötu"><br><span data-ttu-id="b54fd-482">LPBreakParentLP</span><span class="sxs-lookup"><span data-stu-id="b54fd-482">LPBreakParentLP</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-merge-container.png" alt="Merge container ID step icon" title="Skrefatákn sameiningar gámakennis"><br><span data-ttu-id="b54fd-484">MergeContainerId</span><span class="sxs-lookup"><span data-stu-id="b54fd-484">MergeContainerId</span></span></td>
<td><img src="media/step-icons-mixed-lp-line.png" alt="Mixed license plate line number step icon" title="Skrefatákn línunúmers blandaðrar númeraplötu"><br><span data-ttu-id="b54fd-486">MixedLPLineNum</span><span class="sxs-lookup"><span data-stu-id="b54fd-486">MixedLPLineNum</span></span></td>
<td><img src="media/step-icons-outbound-weight.png" alt="Outbound weight step icon" title="Skrefatákn þyngdar á útleið"><br><span data-ttu-id="b54fd-488">OutboundWeight</span><span class="sxs-lookup"><span data-stu-id="b54fd-488">OutboundWeight</span></span></td>
<td><img src="media/step-icons-owner.png" alt="Owner step icon" title="Skrefatákn eiganda"><br><span data-ttu-id="b54fd-490">Eigandi</span><span class="sxs-lookup"><span data-stu-id="b54fd-490">Owner</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-parent-lp.png" alt="Parent license plate step icon" title="Skrefatákn yfirnúmeraplötu"><br><span data-ttu-id="b54fd-492">ParentLP</span><span class="sxs-lookup"><span data-stu-id="b54fd-492">ParentLP</span></span></td>
<td><img src="media/step-icons-please-confirm.png" alt="Please confirm step icon" title="Skrefatákn staðfestingar"><br><span data-ttu-id="b54fd-494">PleaseConfirm</span><span class="sxs-lookup"><span data-stu-id="b54fd-494">PleaseConfirm</span></span></td>
<td><img src="media/step-icons-po-line-num.png" alt="Purchase order line number step icon" title="Skrefatákn innkaupapöntunarlínunúmers"><br><span data-ttu-id="b54fd-496">POLineNum</span><span class="sxs-lookup"><span data-stu-id="b54fd-496">POLineNum</span></span></td>
<td><img src="media/step-icons-po-num.png" alt="Purchase order number step icon" title="Skrefatákn innkaupapöntunarnúmers"><br><span data-ttu-id="b54fd-498">Innkaupanúmer</span><span class="sxs-lookup"><span data-stu-id="b54fd-498">PONum</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-position-full.png" alt="Position full step icon" title="Skrefatákn fullrar staðsetningar"><br><span data-ttu-id="b54fd-500">PositionFull</span><span class="sxs-lookup"><span data-stu-id="b54fd-500">PositionFull</span></span></td>
<td><img src="media/step-icons-potency.png" alt="Potency step icon" title="Skrefatákn styrkleika"><br><span data-ttu-id="b54fd-502">Styrkleiki</span><span class="sxs-lookup"><span data-stu-id="b54fd-502">Potency</span></span></td>
<td><img src="media/step-icons-printer-name.png" alt="Printer name step icon" title="Skrefatákn prentaraheitis"><br><span data-ttu-id="b54fd-504">PrinterName</span><span class="sxs-lookup"><span data-stu-id="b54fd-504">PrinterName</span></span></td>
<td><img src="media/step-icons-prod-id.png" alt="Prod ID step icon" title="Skrefatákn framleiðslukennis"><br><span data-ttu-id="b54fd-506">ProdId</span><span class="sxs-lookup"><span data-stu-id="b54fd-506">ProdId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-product-confirm.png" alt="Product confirmation step icon" title="Skrefatákn afurðarstaðfestingar"><br><span data-ttu-id="b54fd-508">ProductConfirmation</span><span class="sxs-lookup"><span data-stu-id="b54fd-508">ProductConfirmation</span></span></td>
<td><img src="media/step-icons-put.png" alt="Put step icon" title="Skrefatákn frágangs"><br><span data-ttu-id="b54fd-510">Frágangur</span><span class="sxs-lookup"><span data-stu-id="b54fd-510">Put</span></span></td>
<td><img src="media/step-icons-putaway-cluster-id.png" alt="Putaway cluster ID step icon" title="Skrefatákn frágangsklasakennis"><br><span data-ttu-id="b54fd-512">PutawayClusterId</span><span class="sxs-lookup"><span data-stu-id="b54fd-512">PutawayClusterId</span></span></td>
<td><img src="media/step-icons-qty.png" alt="Quantity step icon" title="Skrefatákn magns"><br><span data-ttu-id="b54fd-514">Magn</span><span class="sxs-lookup"><span data-stu-id="b54fd-514">Qty</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-qty-adjust-in.png" alt="Quantity adjust in step icon" title="Skrefatákn magnleiðréttingar á innleið"><br><span data-ttu-id="b54fd-516">QtyAdjustIn</span><span class="sxs-lookup"><span data-stu-id="b54fd-516">QtyAdjustIn</span></span></td>
<td><img src="media/step-icons-qty-short.png" alt="Quantity short step icon" title="Skrefatákn of lítils magns"><br><span data-ttu-id="b54fd-518">QtyShort</span><span class="sxs-lookup"><span data-stu-id="b54fd-518">QtyShort</span></span></td>
<td><img src="media/step-icons-qty-to-consume.png" alt="Quantity to consume step icon" title="Skrefatákn notkunarmagns"><br><span data-ttu-id="b54fd-520">QtyToConsume</span><span class="sxs-lookup"><span data-stu-id="b54fd-520">QtyToConsume</span></span></td>
<td><img src="media/step-icons-qty-to-put.png" alt="Quantity to put step icon" title="Skrefatákn frágangsmagns"><br><span data-ttu-id="b54fd-522">QtyToPut</span><span class="sxs-lookup"><span data-stu-id="b54fd-522">QtyToPut</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-qty-to-scrap.png" alt="Quantity to scrap step icon" title="Skrefatákn rýrnunarmagns"><br><span data-ttu-id="b54fd-524">QtyToScrap</span><span class="sxs-lookup"><span data-stu-id="b54fd-524">QtyToScrap</span></span></td>
<td><img src="media/step-icons-qty-confirmation.png" alt="Quantity confirmation step icon" title="Skrefatákn staðfestingarmagns"><br><span data-ttu-id="b54fd-526">QuantityConfirmation</span><span class="sxs-lookup"><span data-stu-id="b54fd-526">QuantityConfirmation</span></span></td>
<td><img src="media/step-icons-raf-end-job.png" alt="Report as finished end job step icon" title="Skrefatákn tilkynningar um lok vinnslu"><br><span data-ttu-id="b54fd-528">RAFEndJob</span><span class="sxs-lookup"><span data-stu-id="b54fd-528">RAFEndJob</span></span></td>
<td><img src="media/step-icons-recv-loc-id.png" alt="Receive location ID step icon" title="Skrefatákn staðsetningarkennis móttöku"><br><span data-ttu-id="b54fd-530">RecvLocationID</span><span class="sxs-lookup"><span data-stu-id="b54fd-530">RecvLocationID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-remove-container-id.png" alt="Remove container ID step icon" title="Skrefatákn gámafjarlægingar"><br><span data-ttu-id="b54fd-532">RemoveContainerID</span><span class="sxs-lookup"><span data-stu-id="b54fd-532">RemoveContainerID</span></span></td>
<td><img src="media/step-icons-rma-no.png" alt="RMA number step icon" title="Skrefatákn RMA-númers"><br><span data-ttu-id="b54fd-534">RMANum</span><span class="sxs-lookup"><span data-stu-id="b54fd-534">RMANum</span></span></td>
<td><img src="media/step-icons-select-order.png" alt="Select order step icon" title="Skrefatákn pöntunarvals"><br><span data-ttu-id="b54fd-536">SelectOrder</span><span class="sxs-lookup"><span data-stu-id="b54fd-536">SelectOrder</span></span></td>
<td><img src="media/step-icons-short-pick-reason.png" alt="Short pick reason step icon" title="Skrefatákn ástæðu of lítillar tiltektar"><br><span data-ttu-id="b54fd-538">ShortPickReason</span><span class="sxs-lookup"><span data-stu-id="b54fd-538">ShortPickReason</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-sort-position-id.png" alt="Sort position ID step icon" title="Skrefatákn staðsetningarkennis röðunar"><br><span data-ttu-id="b54fd-540">SortPositionId</span><span class="sxs-lookup"><span data-stu-id="b54fd-540">SortPositionId</span></span></td>
<td><img src="media/step-icons-target-lp-id.png" alt="Target license plate ID step icon" title="Skrefatákn númeraplötukennis markmiðs"><br><span data-ttu-id="b54fd-542">TargetLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="b54fd-542">TargetLicensePlateId</span></span></td>
<td><img src="media/step-icons-to-line-no.png" alt="To line number step icon" title="Skrefatákn til línunúmers"><br><span data-ttu-id="b54fd-544">ToLineNum</span><span class="sxs-lookup"><span data-stu-id="b54fd-544">ToLineNum</span></span></td>
<td><img src="media/step-icons-to-location.png" alt="To location step icon" title="Skrefatákn til staðsetningar"><br><span data-ttu-id="b54fd-546">ToLocation</span><span class="sxs-lookup"><span data-stu-id="b54fd-546">ToLocation</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-to-number.png" alt="To number step icon" title="Skrefatákn til númers"><br><span data-ttu-id="b54fd-548">ToNum</span><span class="sxs-lookup"><span data-stu-id="b54fd-548">ToNum</span></span></td>
<td><img src="media/step-icons-to-warehouse.png" alt="To warehouse step icon" title="Skrefatákn til vöruhúss"><br><span data-ttu-id="b54fd-550">ToWarehouse</span><span class="sxs-lookup"><span data-stu-id="b54fd-550">ToWarehouse</span></span></td>
<td><img src="media/step-icons-tranport-load-id.png" alt="Transport load ID step icon" title="Skrefatákn farmflutningskennis"><br><span data-ttu-id="b54fd-552">TransportLoadId</span><span class="sxs-lookup"><span data-stu-id="b54fd-552">TransportLoadId</span></span></td>
<td><img src="media/step-icons-vendor-batch-id.png" alt="Vendor batch ID step icon" title="Skrefatákn runukennis lánardrottins"><br><span data-ttu-id="b54fd-554">VendBatchId</span><span class="sxs-lookup"><span data-stu-id="b54fd-554">VendBatchId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-wave-label-id.png" alt="Wave label ID step icon" title="Skrefatákn kennis bylgjumerkis"><br><span data-ttu-id="b54fd-556">WaveLabelId</span><span class="sxs-lookup"><span data-stu-id="b54fd-556">WaveLabelId</span></span></td>
<td><img src="media/step-icons-wave-label-qty.png" alt="Wave label quantity step icon" title="Skrefatákn magns bylgjumerkis"><br><span data-ttu-id="b54fd-558">WaveLblQty</span><span class="sxs-lookup"><span data-stu-id="b54fd-558">WaveLblQty</span></span></td>
<td><img src="media/step-icons-weight.png" alt="Weight step icon" title="Skrefatákn þyngdar"><br><span data-ttu-id="b54fd-560">Vægi</span><span class="sxs-lookup"><span data-stu-id="b54fd-560">Weight</span></span></td>
<td><img src="media/step-icons-weight-to-consume.png" alt="Weight to consume step icon" title="Skrefatákn notkunarþyngdar"><br><span data-ttu-id="b54fd-562">WeightToConsume</span><span class="sxs-lookup"><span data-stu-id="b54fd-562">WeightToConsume</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-whs-adjustment-type.png" alt="WHS adjustment type step icon" title="Skrefatákn leiðréttingargerðar vöruhúsakerfis"><br><span data-ttu-id="b54fd-564">WHSAdjustmentType</span><span class="sxs-lookup"><span data-stu-id="b54fd-564">WHSAdjustmentType</span></span></td>
<td><img src="media/step-icons-whs-receiving-exception.png" alt="WHS receiving exception step icon" title="Skrefatákn móttökufráviks vöruhúsakerfis"><br><span data-ttu-id="b54fd-566">WHSReceivingException</span><span class="sxs-lookup"><span data-stu-id="b54fd-566">WHSReceivingException</span></span></td>
<td><img src="media/step-icons-wms-location-id.png" alt="WMS location ID step icon" title="Skrefatákn staðsetningarkennis vöruhúsakerfis"><br><span data-ttu-id="b54fd-568">WMSLocationID</span><span class="sxs-lookup"><span data-stu-id="b54fd-568">WMSLocationID</span></span></td>
<td><img src="media/step-icons-work-id.png" alt="Work ID step icon" title="Skrefatákn vinnukennis"><br><span data-ttu-id="b54fd-570">WorkId</span><span class="sxs-lookup"><span data-stu-id="b54fd-570">WorkId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-work-id-to-cancel.png" alt="Work ID to cancel step icon" title="Skrefatákn vinnukennis sem á að hætta við"><br><span data-ttu-id="b54fd-572">WorkIdToCancel</span><span class="sxs-lookup"><span data-stu-id="b54fd-572">WorkIdToCancel</span></span></td>
<td><img src="media/step-icons-work-lp-id.png" alt="Work license plate ID step icon" title="Skrefatákn númeraplötukennis vinnu"><br><span data-ttu-id="b54fd-574">WorkLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="b54fd-574">WorkLicensePlateId</span></span></td>
<td><img src="media/step-icons-work-lp-putaway-cluster.png" alt="Work license plate ID putaway cluster step icon" title="Skrefatákn frágangsklasa fyrir númeraplötukenni vinnu"><br><span data-ttu-id="b54fd-576">WorkLPIDPutawayCluster</span><span class="sxs-lookup"><span data-stu-id="b54fd-576">WorkLPIDPutawayCluster</span></span></td>
<td><img src="media/step-icons-work-pool-id.png" alt="Work pool ID step icon" title="Skrefatákn vinnuhópakennis"><br><span data-ttu-id="b54fd-578">WorkPoolID</span><span class="sxs-lookup"><span data-stu-id="b54fd-578">WorkPoolID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-zone-pool-id.png" alt="Zone ID step icon" title="Skrefatákn svæðiskennis"><br><span data-ttu-id="b54fd-580">ZoneID</span><span class="sxs-lookup"><span data-stu-id="b54fd-580">ZoneID</span></span></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

## <a name="example-assign-step-icons-and-titles-for-a-custom-flow"></a><a name="example"></a><span data-ttu-id="b54fd-581">Dæmi: Úthluta táknum og titlum skrefa fyrir verkflæði</span><span class="sxs-lookup"><span data-stu-id="b54fd-581">Example: Assign step icons and titles for a custom flow</span></span>

<span data-ttu-id="b54fd-582">Þetta dæmi útskýrir hvernig á að setja upp tákn og titla skrefa fyrir sérsniðið verkflæði.</span><span class="sxs-lookup"><span data-stu-id="b54fd-582">This example explains how to set up step icons and titles for a custom task flow.</span></span> <span data-ttu-id="b54fd-583">Aðstæðurnar byggjast á dæmi um sérsniðið verkflæði sem er kynnt og kannað nánar í eftirfarandi bloggfærslu: [Farsímaforrit vöruhúsakerfis sérstillt](https://cloudblogs.microsoft.com/dynamics365/it/2017/07/06/customizing-the-warehousing-mobile-app).</span><span class="sxs-lookup"><span data-stu-id="b54fd-583">The scenario is built on an example of a custom task flow that is presented and explored in more detail in the following blog post: [Customizing the Warehousing Mobile App](https://cloudblogs.microsoft.com/dynamics365/it/2017/07/06/customizing-the-warehousing-mobile-app).</span></span> <span data-ttu-id="b54fd-584">Verkflæðið virkar á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="b54fd-584">The task flow works in the following way:</span></span>

1. <span data-ttu-id="b54fd-585">Forritið sýnir síðu sem biður starfsmann að gefa upp gámakenni (t.d. með því að skanna strikamerki).</span><span class="sxs-lookup"><span data-stu-id="b54fd-585">The app shows a page that prompts the worker to provide a container ID (for example, by scanning a bar code).</span></span>
1. <span data-ttu-id="b54fd-586">Ef gámakennið er gilt opnar forritið nýja síðu sem biður starfsmanninn um þyngdina.</span><span class="sxs-lookup"><span data-stu-id="b54fd-586">If the container ID is valid, the app opens a new page that prompts the worker for the weight.</span></span> <span data-ttu-id="b54fd-587">(Ef gámakennið er ógilt er starfsmanninum vísað á fyrstu síðuna.)</span><span class="sxs-lookup"><span data-stu-id="b54fd-587">(If the container ID isn't valid, the worker is returned to the first page.)</span></span>
1. <span data-ttu-id="b54fd-588">Þegar starfsmaðurinn slær inn gilda þyngd, geymir kerfið þyngdina og flytur starfsmanninn aftur á fyrstu síðuna.</span><span class="sxs-lookup"><span data-stu-id="b54fd-588">When the worker enters a valid weight, the system stores the weight and returns the worker to the first page.</span></span>

<span data-ttu-id="b54fd-589">Eftirfarandi mynd sýnir þetta verkflæði.</span><span class="sxs-lookup"><span data-stu-id="b54fd-589">The following illustration shows this task flow.</span></span>

<span data-ttu-id="b54fd-590">![Skýringarmynd verkflæðis](media/step-icons-example-task-flow.png "Skýringarmynd verkflæðis")</span><span class="sxs-lookup"><span data-stu-id="b54fd-590">![Task flow diagram](media/step-icons-example-task-flow.png "Task flow diagram")</span></span>

### <a name="create-a-step-class-for-the-container-input-page"></a><span data-ttu-id="b54fd-591">Stofna skrefaklasa fyrir innsláttarsíðu gámsins</span><span class="sxs-lookup"><span data-stu-id="b54fd-591">Create a step class for the container input page</span></span>

<span data-ttu-id="b54fd-592">Innsláttarsíða gámsins gerir starfsmanni kleift að skanna eða færa inn gámakenni.</span><span class="sxs-lookup"><span data-stu-id="b54fd-592">The container input page lets the worker scan or enter a container ID.</span></span>

<span data-ttu-id="b54fd-593">![Innsláttarsíða gáms](media/step-icons-example-container-input.png "Innsláttarsíða gáms")</span><span class="sxs-lookup"><span data-stu-id="b54fd-593">![Container input page](media/step-icons-example-container-input.png "Container input page")</span></span>

<span data-ttu-id="b54fd-594">Á innsláttarsíðu gámsins er stýringarheiti færslureitsins `ContainerId`.</span><span class="sxs-lookup"><span data-stu-id="b54fd-594">On the container input page, the control name of the input field is `ContainerId`.</span></span> <span data-ttu-id="b54fd-595">Þar sem þetta stýringarheiti er ekki í [lista yfir skrefakenni](#step-ids-classes) verður ekki hægt að finna fyrirliggjandi skref sem byggir á því.</span><span class="sxs-lookup"><span data-stu-id="b54fd-595">Because this control name isn't in the [list of step IDs](#step-ids-classes), you won't find an existing step that is based on it.</span></span> <span data-ttu-id="b54fd-596">Því þarf að stofna skrefaklasa sem stendur fyrir skrefið.</span><span class="sxs-lookup"><span data-stu-id="b54fd-596">Therefore, you must create a step class that represents the step.</span></span> <span data-ttu-id="b54fd-597">Eftirfarandi er dæmi.</span><span class="sxs-lookup"><span data-stu-id="b54fd-597">Here is an example.</span></span>

```xpp
[WHSMobileAppStepId('ContainerId')]
final internal class WHSMobileAppStepContainerId extends WHSMobileAppStep
{
    private const WHSMobileAppStepIcon PopulationIcon = 'InventBatchID';
    private const WHSMobileAppStepTitle InputNotFilledTitle = "@WAX:WHSMobileAppStepContainerID_InputNotFilled"; //Scan a container
    protected void initValues()
    {
        defaultStepIcon = PopulationIcon;
        defaultStepTitle = InputNotFilledTitle;
    }
}
```

<span data-ttu-id="b54fd-598">Kennimerki skrefatáknsins er geymt í `defaultStepIcon` klasameðlimnum og titill skrefsins er geymt í `defaultStepTitle` klasameðlimnum.</span><span class="sxs-lookup"><span data-stu-id="b54fd-598">The identifier of the step icon is stored in the `defaultStepIcon` class member, and the step title is stored in the `defaultStepTitle` class member.</span></span>

<span data-ttu-id="b54fd-599">Til að úthluta skrefatákni skal stilla `defaultStepIcon` á eitt af kennum táknsins sem eru sýnd í hlutanum [Tiltæk skrefatákn](#step-icons) fyrr í þessu efnisatriði.</span><span class="sxs-lookup"><span data-stu-id="b54fd-599">To assign a step icon, set `defaultStepIcon` to one of the icon IDs that are listed in the [Available step icons](#step-icons) section earlier in this topic.</span></span>

### <a name="use-a-standard-or-custom-step-icon-and-title-for-the-weight-input"></a><span data-ttu-id="b54fd-600">Nota staðlað eða sérstillt tákn og titil skrefs fyrir innslátt þyngdar</span><span class="sxs-lookup"><span data-stu-id="b54fd-600">Use a standard or custom step icon and title for the weight input</span></span>

<span data-ttu-id="b54fd-601">Innsláttarsíða þyngdar gerir starfsmanni kleift að slá inn þyngd.</span><span class="sxs-lookup"><span data-stu-id="b54fd-601">The weight input page lets the worker enter a weight.</span></span>

<span data-ttu-id="b54fd-602">![Innsláttarsíða þyngdar](media/step-icons-example-weight-input.png "Innsláttarsíða þyngdar")</span><span class="sxs-lookup"><span data-stu-id="b54fd-602">![Weight input page](media/step-icons-example-weight-input.png "Weight input page")</span></span>

<span data-ttu-id="b54fd-603">Á innsláttarsíðu þyngdar er stýringarheiti færslureitsins `Weight`, sem er í [listanum yfir skrefakenni](#step-ids-classes).</span><span class="sxs-lookup"><span data-stu-id="b54fd-603">On the weight input page, the control name of the input field is `Weight`, which is in the [list of step IDs](#step-ids-classes).</span></span> <span data-ttu-id="b54fd-604">Þar af leiðandi þarf ekki að breyta neinu fyrir þetta skref ef tákn og titill skrefsins sem eru skilgreind í `WHSMobileAppStepWeight` klasanum reynast í lagi.</span><span class="sxs-lookup"><span data-stu-id="b54fd-604">Therefore, if the step icon and title that are defined in the `WHSMobileAppStepWeight` class are acceptable to you, you don't have to change anything for this step.</span></span>

<span data-ttu-id="b54fd-605">Ef hinsvegar kosið er að nota annað tákn eða titil fyrir þetta skref er hægt að hnekkja annaðhvort `stepId()` aðferðinni eða `stepInfo()` aðferðinni í smiðsklasanum.</span><span class="sxs-lookup"><span data-stu-id="b54fd-605">However, if you prefer to use a different icon or title for this step, you can override either the `stepId()` method or the `stepInfo()` method in the builder class.</span></span> <span data-ttu-id="b54fd-606">Hvert verkflæði er með sinn eigin smið skrefaupplýsinga.</span><span class="sxs-lookup"><span data-stu-id="b54fd-606">Each task flow has its own step info builder.</span></span>

#### <a name="override-the-stepid-method"></a><span data-ttu-id="b54fd-607">Hnekkja stepId() aðferðinni</span><span class="sxs-lookup"><span data-stu-id="b54fd-607">Override the stepId() method</span></span>

<span data-ttu-id="b54fd-608">Eftirfarandi dæmi sýnir eina leið sem til að breyta smiðsklasa með því að hnekkja `stepId()` aðferðinni.</span><span class="sxs-lookup"><span data-stu-id="b54fd-608">The following example shows one way that you can modify a builder class by overriding the `stepId()` method.</span></span>

```xpp
[WHSWorkExecuteMode(WHSWorkExecuteMode:: WeighContainer)]
public class WHSMobileAppStepInfoBuilderWeighContainer extends WHSMobileAppStepInfoBuilder
{
    protected WHSMobileAppStepId stepId()
    {
        WHSMobileAppStepId stepIdLocal = super();
        if (stepIdLocal == 'Weight')
        {
            return 'NewWeight';
        }
        return stepIdLocal;
    }
}
```

<span data-ttu-id="b54fd-609">Þú býrð svo til skrefflokk fyrir `NewWeight` skrefið.</span><span class="sxs-lookup"><span data-stu-id="b54fd-609">You then create a step class for the `NewWeight` step.</span></span> <span data-ttu-id="b54fd-610">Kóðinn ætti að líkjast kóðanum fyrir `ContainerId` dæmið sem sýnt var fyrr í þessu efnisatriði.</span><span class="sxs-lookup"><span data-stu-id="b54fd-610">The code should resemble the code for the `ContainerId` example that was shown earlier in this topic.</span></span>

#### <a name="override-the-stepinfo-method"></a><span data-ttu-id="b54fd-611">Hnekkja stepInfo() aðferðinni</span><span class="sxs-lookup"><span data-stu-id="b54fd-611">Override the stepInfo() method</span></span>

<span data-ttu-id="b54fd-612">Eftirfarandi dæmi sýnir eina leið sem til að breyta smiðsklasa með því að hnekkja `stepInfo()` aðferðinni.</span><span class="sxs-lookup"><span data-stu-id="b54fd-612">The following example shows one way that you can modify a builder class by overriding the `stepInfo()` method.</span></span>

```xpp
[WHSWorkExecuteMode(WHSWorkExecuteMode:: WeighContainer)]
public class WHSMobileAppStepInfoBuilderWeighContainer extends WHSMobileAppStepInfoBuilder
{
    protected WHSMobileAppStepInfo stepInfo()
    {
        if (stepId != 'Weight')
        {
            return super();
        }
        WHSMobileAppStepInfo stepInfo = WHSMobileAppStepInfo::construct();
        stepInfo.parmStepIcon('NewIcon');
        stepInfo.parmStepTitle('NewTitle');
        return stepInfo;
    }
}
```

<span data-ttu-id="b54fd-613">Þú smíðar síðan `WHSMobileAppStepInfo` hlut og stillir táknið og/eða titilinn beint.</span><span class="sxs-lookup"><span data-stu-id="b54fd-613">You then construct a `WHSMobileAppStepInfo` object, and set the icon and/or title directly.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b54fd-614">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="b54fd-614">Additional resources</span></span>

- [<span data-ttu-id="b54fd-615">Setja upp og tengja farsímaforrit vöruhúsakerfis</span><span class="sxs-lookup"><span data-stu-id="b54fd-615">Install and connect the Warehouse Management mobile app</span></span>](install-configure-warehouse-management-app.md)
- [<span data-ttu-id="b54fd-616">Notandastillingar fartækis</span><span class="sxs-lookup"><span data-stu-id="b54fd-616">Mobile device user settings</span></span>](mobile-device-user-settings.md)
