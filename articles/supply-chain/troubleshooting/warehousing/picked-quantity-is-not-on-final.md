---
title: Ekki er hægt að staðfesta sendingu vegna þess að ekki er búið að taka vörurnar til
description: Ekki er hægt að staðfesta sendingu vegna þess að ekki er búið að taka vörurnar til
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f3ebd47ffc85d4ca257b404579d60d679f7929b6
ms.sourcegitcommit: f9b145ef4a81cec81f420871b4130b05db4f4500
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/23/2021
ms.locfileid: "6301306"
---
# <a name="you-cant-confirm-a-shipment-because-items-havent-been-picked"></a><span data-ttu-id="09993-103">Ekki er hægt að staðfesta sendingu vegna þess að ekki er búið að taka vörurnar til</span><span class="sxs-lookup"><span data-stu-id="09993-103">You can't confirm a shipment because items haven't been picked</span></span>

<span data-ttu-id="09993-104">Villukóði: LoadNotPickedAndMovedToFinalShippingLocation</span><span class="sxs-lookup"><span data-stu-id="09993-104">Error code: LoadNotPickedAndMovedToFinalShippingLocation</span></span>

## <a name="symptoms"></a><span data-ttu-id="09993-105">Einkenni</span><span class="sxs-lookup"><span data-stu-id="09993-105">Symptoms</span></span>

<span data-ttu-id="09993-106">Þegar reynt er að staðfesta sendingu sýnir kerfið eftirfarandi villuboð:</span><span class="sxs-lookup"><span data-stu-id="09993-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="09993-107">Sumar vörurnar sem þarf að nota fyrir farm %1 hafa ekki enn verið teknar til og færðar á endanlegan sendingarstað.</span><span class="sxs-lookup"><span data-stu-id="09993-107">Some of the items that are needed for load %1 have not yet been picked and moved to the final shipping location.</span></span>

<span data-ttu-id="09993-108">Því er ekki hægt að staðfesta sendinguna fyrir farminn.</span><span class="sxs-lookup"><span data-stu-id="09993-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="09993-109">Orsök</span><span class="sxs-lookup"><span data-stu-id="09993-109">Cause</span></span>

<span data-ttu-id="09993-110">Ekki er hægt að staðfesta hleðsluna eða sendinguna í núverandi stöðu vegna þess að eitt eftirfarandi skilyrða gæti verið til staðar:</span><span class="sxs-lookup"><span data-stu-id="09993-110">The load or shipment can't be confirmed in its current state because one of the following conditions might exist:</span></span>

- <span data-ttu-id="09993-111">Tengt verk hefur ekki enn verið tínt og fært yfir á lokastaðsetningu sendingar.</span><span class="sxs-lookup"><span data-stu-id="09993-111">The related work hasn't yet been picked and moved to the final shipping location.</span></span>
- <span data-ttu-id="09993-112">Tiltekið vinnumagn passar ekki við vinnumagn sem var búið til á farmlínunni.</span><span class="sxs-lookup"><span data-stu-id="09993-112">The picked work quantity doesn't match the created work quantity on the load line.</span></span>
- <span data-ttu-id="09993-113">Staðsetningarleiðbeiningin hefur verið skilgreind með pökkunarstaðsetningu sem lokastaðsetning sendingar á meðan gámun bylgjusniðmáts var notuð.</span><span class="sxs-lookup"><span data-stu-id="09993-113">The location directive has been configured with packing location as the final shipping location while using Wave template containerization.</span></span>

## <a name="resolution"></a><span data-ttu-id="09993-114">Lausn</span><span class="sxs-lookup"><span data-stu-id="09993-114">Resolution</span></span>

<span data-ttu-id="09993-115">Hleðslan eða sendingin er í stöðu þar sem staðfesting á sendingu mistókst.</span><span class="sxs-lookup"><span data-stu-id="09993-115">The load or shipment is currently in a state where shipment confirmation fails.</span></span> <span data-ttu-id="09993-116">Til að leysa þetta vandamál þarf að ljúka við eitt af eftirfarandi verkum:</span><span class="sxs-lookup"><span data-stu-id="09993-116">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="09993-117">Farið yfir hleðslulínurnar og gangið úr skugga um að tengdu verki hafi verið lokið á lokastaðsetningu sendingar og að magnið stemmi.</span><span class="sxs-lookup"><span data-stu-id="09993-117">Review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>
- <span data-ttu-id="09993-118">Hættið við vinnukennin sem hafa verið stofnuð með pökkunarstaðsetningunni sem lokastaðsetning sendingar, endurstillið staðsetningarleiðbeininguna og losið hleðsluna aftur.</span><span class="sxs-lookup"><span data-stu-id="09993-118">Cancel the work IDs that have been created with the packing location as the final shipping location, reconfigure the location directive, and rerelease the load.</span></span>

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a><span data-ttu-id="09993-119">Farið yfir hleðslulínurnar og gangið úr skugga um að tengdu verki hafi verið lokið á lokastaðsetningu sendingar og að magnið stemmi</span><span class="sxs-lookup"><span data-stu-id="09993-119">Review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match</span></span>

<span data-ttu-id="09993-120">Notið eftirfarandi ferli til að yfirfara hleðslulínurnar og gangið úr skugga um að tengdu verki hafi verið lokið á lokastaðsetningu sendingar og að magnið stemmi.</span><span class="sxs-lookup"><span data-stu-id="09993-120">Use the following procedure to review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>

1. <span data-ttu-id="09993-121">Farðu í **Vöruhúsakerfi \> Hleðslur \> Allar hleðslur**.</span><span class="sxs-lookup"><span data-stu-id="09993-121">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="09993-122">Veljið hleðsluna sem ekki er hægt að staðfesta sendinguna fyrir.</span><span class="sxs-lookup"><span data-stu-id="09993-122">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="09993-123">Í flýtiflipanum **Hleðslulínur** skal velja hleðslulínu.</span><span class="sxs-lookup"><span data-stu-id="09993-123">On the **Load lines** FastTab, select the load line.</span></span>
1. <span data-ttu-id="09993-124">Gera skal athugasemd um gildið í reitnum **Magn stofnaðs verks**.</span><span class="sxs-lookup"><span data-stu-id="09993-124">Make a note of the value of the **Work created quantity** field.</span></span>
1. <span data-ttu-id="09993-125">Á aðgerðasvæðinu, í flipanum **Hleðslur**, í flokknum **Tengdar upplýsingar**, skal velja **Verk**.</span><span class="sxs-lookup"><span data-stu-id="09993-125">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="09993-126">Staðfestið að verkinu sé lokið á lokastaðsetningu sendingar og að tínt magn verksins stemmi við magn stofnaðs verks í hleðslulínunni.</span><span class="sxs-lookup"><span data-stu-id="09993-126">Verify that the work has been completed at the final shipping location, and that the picked work quantity matches the created work quantity on the load line.</span></span>
1. <span data-ttu-id="09993-127">Þetta ferli er endurtekið fyrir allar hleðslulínur til að ganga úr skugga um að öll viðmið séu uppfyllt.</span><span class="sxs-lookup"><span data-stu-id="09993-127">Repeat this procedure for all load lines to make sure that all criteria are met.</span></span>

### <a name="cancel-the-work-ids-that-have-been-created-with-the-packing-location-as-the-final-shipping-location-reconfigure-the-location-directive-and-rerelease-the-load"></a><span data-ttu-id="09993-128">Hættið við vinnukennin sem hafa verið stofnuð með pökkunarstaðsetningunni sem lokastaðsetning sendingar, endurstillið staðsetningarleiðbeininguna og losið hleðsluna aftur</span><span class="sxs-lookup"><span data-stu-id="09993-128">Cancel the work IDs that have been created with the packing location as the final shipping location, reconfigure the location directive, and rerelease the load</span></span>

<span data-ttu-id="09993-129">Notið eftirfarandi aðferð til að hætta við vinnukennin sem eru með pökkunarstaðsetninguna sem lokastaðsetning frágangs með sjálfvirka gámun í gangi.</span><span class="sxs-lookup"><span data-stu-id="09993-129">Use the following procedure to cancel the work IDs that have the packing location as the final put location with automated containerization in place.</span></span>

1. <span data-ttu-id="09993-130">Fara í **Vöruhússtjórn \> Reglubundin verkefni \> Hreinsa \> Hætta við vinnu**.</span><span class="sxs-lookup"><span data-stu-id="09993-130">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="09993-131">Svarglugginn **Hætta við vinnu** opnast.</span><span class="sxs-lookup"><span data-stu-id="09993-131">The **Cancel work** dialog opens.</span></span> <span data-ttu-id="09993-132">Tilgreinið kenni verksins sem á að hætta við í svæðinu **Vinnukenni**.</span><span class="sxs-lookup"><span data-stu-id="09993-132">In the **Work ID** field, specify the ID of the work that you want to cancel.</span></span> <span data-ttu-id="09993-133">Valið vinnukenni verður að vera með gildi fyrir **Staða verks** sem *Opin*, *Í vinnslu*, *Hætt við*, *Sameinað* eða *Lokað*.</span><span class="sxs-lookup"><span data-stu-id="09993-133">The selected work ID must have a **Work status** value of *Open*, *In progress*, *Canceled*, *Combined*, or *Closed*.</span></span>
1. <span data-ttu-id="09993-134">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="09993-134">Select **OK**.</span></span>
1. <span data-ttu-id="09993-135">Veljið **Já** til að staðfesta að hætta skuli við verkið.</span><span class="sxs-lookup"><span data-stu-id="09993-135">Select **Yes** to confirm that you want to cancel the work.</span></span>
1. <span data-ttu-id="09993-136">Endurtakið þetta ferli fyrir hin vinnukennin eftir því sem þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="09993-136">Repeat this procedure for the other work IDs as needed.</span></span>

<span data-ttu-id="09993-137">Frekari upplýsingar er að finna á [Hætta við vöruhúsavinnu vegna frábrigðameðhöndlunar](../../warehousing/cancel-warehouse-work.md).</span><span class="sxs-lookup"><span data-stu-id="09993-137">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>

<span data-ttu-id="09993-138">Notið eftirfarandi ferli til að endurstilla staðsetningarleiðbeininguna þannig að hún noti ekki pökkunarstaðsetninguna sem lokastaðsetningu sendingar þegar sjálfvirk gámun er uppsett fyrir bylgjusniðmátið.</span><span class="sxs-lookup"><span data-stu-id="09993-138">Use the following procedure to reconfigure the location directive so it won't use the packing location as the final shipping location when automated containerization is set up for the wave template.</span></span>

1. <span data-ttu-id="09993-139">Fara í **Vöruhúsakerfi \> Uppsetning \> Staðsetningarleiðbeiningar**.</span><span class="sxs-lookup"><span data-stu-id="09993-139">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="09993-140">Í reitnum **Gerð verkbeiðni** velurðu *Sölupantanir*.</span><span class="sxs-lookup"><span data-stu-id="09993-140">In the **Work order type** field, select *Sales orders*.</span></span>
1. <span data-ttu-id="09993-141">Veljið staðsetningarleiðbeininguna sem er verið að nota fyrir sjálfvirka gámun.</span><span class="sxs-lookup"><span data-stu-id="09993-141">Select the location directive you are using for automated containerization.</span></span>
1. <span data-ttu-id="09993-142">Í tækjastiku flýtiflipans **Aðgerðir í staðsetningarleiðbeiningum** skal velja **Breyta fyrirspurn**.</span><span class="sxs-lookup"><span data-stu-id="09993-142">On the **Location Directive Actions** FastTab toolbar, select **Edit query**.</span></span>
1. <span data-ttu-id="09993-143">Í glugga fyrirspurnarritilsins, í flipanum **Svið**, skal finna línuna þar sem **Reitur** er stilltur á *Staðsetningarforstilling* og staðfestið að reiturinn **Skilyrði** fyrir þá línu sé ekki stilltur á staðsetningarforstillingu sem er með **Staðsetningargerðina** *Pökkun*.</span><span class="sxs-lookup"><span data-stu-id="09993-143">In the query editor dialog, on the **Range** tab, find the row where **Field** is set to *Location profile*, and verify that the **Criteria** field for that row is not set to a location profile that has a **Location type** of *Packing*.</span></span> <span data-ttu-id="09993-144">Stillið reitinn **Skilyrði** til að leiðrétta lokastaðsetningu frágangs.</span><span class="sxs-lookup"><span data-stu-id="09993-144">Adjust the **Criteria** field to correct the final put location.</span></span>

<span data-ttu-id="09993-145">Notið eftirfarandi ferli til að losa hleðsluna aftur og stofna vinnukenni með réttri lokastaðsetningu sendingar.</span><span class="sxs-lookup"><span data-stu-id="09993-145">Use the following procedure to rerelease the load and create work IDs with the correct final shipping location.</span></span>

1. <span data-ttu-id="09993-146">Farið í **Vöruhúsakerfi \> Hleðsla \> Vinnusvæði hleðsluáætlunar**.</span><span class="sxs-lookup"><span data-stu-id="09993-146">Go to **Warehouse management \> Loads \> Load planning workbench**.</span></span>
1. <span data-ttu-id="09993-147">Í hlutanum **Hleðslur** skal finna hleðsluna sem þarf að losa.</span><span class="sxs-lookup"><span data-stu-id="09993-147">In the **Loads** section, find the load that needs to be released.</span></span>
1. <span data-ttu-id="09993-148">Í tækjastiku hlutans **Hleðslur** skal velja **Losa \> Losa í vöruhús** til að losa valda hleðslu í vöruhúsið.</span><span class="sxs-lookup"><span data-stu-id="09993-148">On the **Loads** section toolbar, select **Release \> Release to warehouse** to release the selected load to the warehouse.</span></span>
1. <span data-ttu-id="09993-149">Endurtakið þetta ferli fyrir hinar hleðslurnar eftir því sem þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="09993-149">Repeat this procedure for the other loads as needed.</span></span>
