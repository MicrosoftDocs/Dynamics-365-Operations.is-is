---
title: Bóka sem tilbúið úr verkspjaldstæki
description: Þetta efnisatriði lýsir því hvernig skilgreina á kerfið þannig að notendur verkspjaldtækis geti bókað tilbúnar afurðir úr framleiðslupöntun í birgðir.
author: johanhoffmann
manager: tfehr
ms.date: 05/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgRegistrationSetupTouch
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: f5d34893ddc8adc3785ec50dbd72438cf8f68c5d
ms.sourcegitcommit: 52ba8d3e6af72df5dab6c04b9684a61454d353ad
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/26/2020
ms.locfileid: "3403263"
---
# <a name="report-as-finished-from-the-job-card-device"></a><span data-ttu-id="d75c9-103">Bóka sem tilbúið úr verkspjaldstæki</span><span class="sxs-lookup"><span data-stu-id="d75c9-103">Report as finished from the job card device</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d75c9-104">Starfsmenn nota síðuna **Tilkynna um framvindu** í verkspjaldstækinu til að tilkynna magn sem hefur verið lokið fyrir framleiðsluverk.</span><span class="sxs-lookup"><span data-stu-id="d75c9-104">Workers use the **Report progress** page on the job card device to report quantities that have been completed for a production job.</span></span>

## <a name="control-whether-quantities-that-are-reported-as-finished-are-added-to-inventory"></a><span data-ttu-id="d75c9-105">Stjórna því hvort magn sem er tilkynnt sem lokið verði bætt við birgðir</span><span class="sxs-lookup"><span data-stu-id="d75c9-105">Control whether quantities that are reported as finished are added to inventory</span></span>

<span data-ttu-id="d75c9-106">Til að stjórna því hvort og hvernig magnið sem tilkynnt er sem lokið í síðustu aðgerð eigi að vera bætt við birgðir skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="d75c9-106">To control whether and how the quantities that are reported as finished on the last operation should be added to inventory, follow these steps.</span></span>

1. <span data-ttu-id="d75c9-107">Farið í **Framleiðslustjórnun \> Uppsetning \> Framkvæmd framleiðslu \> Sjálfgildi framleiðslupöntunar**.</span><span class="sxs-lookup"><span data-stu-id="d75c9-107">Go to **Product control \> Setup \> Manufacturing execution \> Production order defaults**.</span></span>
1. <span data-ttu-id="d75c9-108">Í flipanum **Tilkynna sem lokið** skal stilla reitinn **Uppfæra skýrslu um tilbúið á netinu** á eitt af eftirfarandi gildum:</span><span class="sxs-lookup"><span data-stu-id="d75c9-108">On the **Report as finished** tab, set the **Update finished report on-line** field to one of the following values:</span></span>

    - <span data-ttu-id="d75c9-109">**Ekkert** - Engu magni verður bætt við birgðir þegar magn er tilkynnt í síðustu aðgerðinni.</span><span class="sxs-lookup"><span data-stu-id="d75c9-109">**No** – No quantity will be added to inventory when quantities are reported on the last operation.</span></span> <span data-ttu-id="d75c9-110">Staða framleiðslupöntunar breytist aldrei.</span><span class="sxs-lookup"><span data-stu-id="d75c9-110">The status of the production order will never change.</span></span>
    - <span data-ttu-id="d75c9-111">**Staða + magn** – Staða framleiðslupöntunar breytist í *Tilkynna sem lokið* og magnið verður gefið upp sem lokið í birgðum.</span><span class="sxs-lookup"><span data-stu-id="d75c9-111">**Status + Quantity** – The status of the production order will change to *Reported as finished*, and the quantity will be reported as finished to inventory.</span></span>
    - <span data-ttu-id="d75c9-112">**Magn** - Magnið verður tilkynnt sem lokið í birgðum, en staða framleiðslupöntunarinnar breytist aldrei.</span><span class="sxs-lookup"><span data-stu-id="d75c9-112">**Quantity** – The quantity will be reported as finished to inventory, but the status of the production order will never change.</span></span>
    - <span data-ttu-id="d75c9-113">**Staða** - Aðeins staða framleiðslupöntunar breytist.</span><span class="sxs-lookup"><span data-stu-id="d75c9-113">**Status** – Only the status of the production order will change.</span></span> <span data-ttu-id="d75c9-114">Engu magni verður bætt við birgðir þegar magn er tilkynnt í síðustu aðgerð.</span><span class="sxs-lookup"><span data-stu-id="d75c9-114">No quantities will be added to inventory when quantities are reported on the last operation.</span></span>

> [!NOTE]
> <span data-ttu-id="d75c9-115">Magn er ekki rakið í birgðum ef aðgerðirnar sem það er skráð sem lokið í eru ekki skilgreindar sem síðasta aðgerð.</span><span class="sxs-lookup"><span data-stu-id="d75c9-115">Quantities aren't tracked in inventory if the operations that they are reported as finished on aren't defined as the last operation.</span></span> <span data-ttu-id="d75c9-116">Hins vegar er hægt að nota þetta magn til að skoða framvindu.</span><span class="sxs-lookup"><span data-stu-id="d75c9-116">However, those quantities can be used to view progress.</span></span> <span data-ttu-id="d75c9-117">Einnig er hægt að taka það með í reglur sem stjórna því hvort starfsmenn geti hafið næstu aðgerð áður en skilgreindum mörkum um tilkynnt magn úr síðustu aðgerð er náð.</span><span class="sxs-lookup"><span data-stu-id="d75c9-117">They can also be included in rules that control whether workers can start the next operation before a defined threshold of reported quantities on the previous operation is reached.</span></span> <span data-ttu-id="d75c9-118">Hægt er að skilgreina þessar reglur í flipanum **Staðfesting magns** á síðunni **Sjálfgildi framleiðslupöntunar**.</span><span class="sxs-lookup"><span data-stu-id="d75c9-118">You can define these rules on the **Quantity validation** tab of the **Production order defaults** page.</span></span>

<span data-ttu-id="d75c9-119">Frekari upplýsingar um hvernig á að vinna með síðuna **Sjálfgildi framleiðslupöntunar** er að finna í [Færibreytur framleiðslu í framkvæmd framleiðslu](production-parameters-manufacturing-execution.md).</span><span class="sxs-lookup"><span data-stu-id="d75c9-119">For more information about how to work with the **Production order defaults** page, see [Production parameters in Manufacturing execution](production-parameters-manufacturing-execution.md).</span></span>

## <a name="report-batch-controlled-items-as-finished"></a><span data-ttu-id="d75c9-120">Skrá runustýrðar vörur sem tilbúnar</span><span class="sxs-lookup"><span data-stu-id="d75c9-120">Report batch-controlled items as finished</span></span>

<span data-ttu-id="d75c9-121">Verkspjaldstækið styður þrjár atburðarásir fyrir tilkynningu á vörum með runu.</span><span class="sxs-lookup"><span data-stu-id="d75c9-121">The job card device supports three scenarios for reporting on batch items.</span></span> <span data-ttu-id="d75c9-122">Þessar atburðarásir eiga bæði við um vörur sem eru virkjaðar fyrir ítarlega vöruhúsaferla og vörur sem ekki eru virkjaðar fyrir ítarlega vöruhúsaferla.</span><span class="sxs-lookup"><span data-stu-id="d75c9-122">These scenarios apply both to items that are enabled for advanced warehouse processes and to items that aren't enabled for advanced warehouse processes.</span></span>

- <span data-ttu-id="d75c9-123">**Rununúmer úthlutuð handvirkt:** Starfsmenn slá inn sérsniðið rununúmer.</span><span class="sxs-lookup"><span data-stu-id="d75c9-123">**Manually assigned batch numbers:** Workers enter a custom batch number.</span></span> <span data-ttu-id="d75c9-124">Þetta rununúmer gæti komið frá ytri uppruna sem kerfið þekkir ekki.</span><span class="sxs-lookup"><span data-stu-id="d75c9-124">This batch number might come from an external source that isn't known to the system.</span></span>
- <span data-ttu-id="d75c9-125">**Fyrirframskilgreind rununúmer:** Starfsmenn velja rununúmer í lista yfir rununúmer sem kerfið myndar sjálfkrafa áður en framleiðslupöntunin er losuð í verkspjaldstækið.</span><span class="sxs-lookup"><span data-stu-id="d75c9-125">**Predefined batch numbers:** Workers select a batch number in a list of batch numbers that the system automatically generates before the production order is released to the job card device.</span></span>
- <span data-ttu-id="d75c9-126">**Föst rununúmer:** Starfsmenn slá ekki inn eða velja rununúmer.</span><span class="sxs-lookup"><span data-stu-id="d75c9-126">**Fixed batch numbers:** Workers don't enter or select a batch number.</span></span> <span data-ttu-id="d75c9-127">Þess í stað úthlutar kerfið sjálfkrafa rununúmeri á framleiðslupöntunina áður en hún er losuð.</span><span class="sxs-lookup"><span data-stu-id="d75c9-127">Instead, the system automatically assigns a batch number to the production order before it's released.</span></span>

<span data-ttu-id="d75c9-128">Til að virkja hverja atburðarás skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="d75c9-128">To enable each scenario, follow these steps.</span></span>

1. <span data-ttu-id="d75c9-129">Opna **Afurðaupplýsingastjórnun \> Afurðir \> Útgefnar afurðir**.</span><span class="sxs-lookup"><span data-stu-id="d75c9-129">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="d75c9-130">Veljið afurð til að skilgreina.</span><span class="sxs-lookup"><span data-stu-id="d75c9-130">Select the product to configure.</span></span>
1. <span data-ttu-id="d75c9-131">Í flýtiflipanum **Birgðastjórnun**, í reitnum **Rununúmeraflokkur**, skal velja flokk rakningarnúmera sem er settur upp til að styðja atburðarásina.</span><span class="sxs-lookup"><span data-stu-id="d75c9-131">On the **Manage inventory** FastTab, in the **Batch number group** field, select the tracking number group that is set up to support your scenario.</span></span>

> [!NOTE]
> <span data-ttu-id="d75c9-132">Ef engum flokki rununúmera er úthlutað á runustýrða afurð, býður verkspjaldstækið sjálfkrafa upp á handvirkan innslátt fyrir rununúmerið fyrir tilkynningu um lokið.</span><span class="sxs-lookup"><span data-stu-id="d75c9-132">By default, if no batch number group is assigned to a batch-controlled product, the job card device provides manual entry for the batch number during reporting as finished.</span></span>

<span data-ttu-id="d75c9-133">Eftirfarandi undirkaflar lýsa því hvernig á að setja upp flokka rakningarnúmera til að styðja hverja atburðarás fyrir tilkynningu um vörur með rununúmeri.</span><span class="sxs-lookup"><span data-stu-id="d75c9-133">The following subsections describe how to set up tracking number groups to support each of the three scenarios for reporting on batch items.</span></span>

### <a name="enable-batch-number-reporting-on-the-job-card-device"></a><span data-ttu-id="d75c9-134">Virkja tilkynningu um rununúmer í verkspjaldstækinu</span><span class="sxs-lookup"><span data-stu-id="d75c9-134">Enable batch number reporting on the job card device</span></span>

<span data-ttu-id="d75c9-135">Til að gera verkspjaldstæki kleift að samþykkja rununúmer við tilkynningu um lokið þarf að nota [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að kveikja á eftirfarandi eiginleikum (í þessari röð):</span><span class="sxs-lookup"><span data-stu-id="d75c9-135">To enable your job card devices to accept a batch number during reporting as finished, you must use [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn on the following features (in this order):</span></span>

1. <span data-ttu-id="d75c9-136">Enn notandavænni svargluggi fyrir gerð framvinduskýrslu á verkspjaldstækinu.</span><span class="sxs-lookup"><span data-stu-id="d75c9-136">Improved user experience for the Report progress dialog in the Job Card Device</span></span>
1. <span data-ttu-id="d75c9-137">Virkja til að færa inn runu og raðnúmer þegar skýrslugerð er lokið úr verkspjaldstækinu (forútgáfa).</span><span class="sxs-lookup"><span data-stu-id="d75c9-137">Enable to enter batch and serial numbers while reporting as finished from the Job Card Device (Preview)</span></span>

### <a name="set-up-a-tracking-number-group-that-lets-workers-manually-assign-a-batch-number"></a><span data-ttu-id="d75c9-138">Setja upp flokk rakningarnúmera sem gerir starfsmönnum kleift að úthluta rununúmeri handvirkt</span><span class="sxs-lookup"><span data-stu-id="d75c9-138">Set up a tracking number group that lets workers manually assign a batch number</span></span>

<span data-ttu-id="d75c9-139">Til að leyfa handvirka úthlutun rununúmera skal fylgja þessum skrefum til að setja upp flokk rakningarnúmera.</span><span class="sxs-lookup"><span data-stu-id="d75c9-139">To allow for manually assigned batch numbers, follow these steps to set up a tracking number group.</span></span>

1. <span data-ttu-id="d75c9-140">Farið í **Birgðastjórnun \> Uppsetning \> Víddir \> Flokkar rakningarnúmera**.</span><span class="sxs-lookup"><span data-stu-id="d75c9-140">Go to **Inventory management \> Setup \> Dimensions \> Tracking number groups**.</span></span>
1. <span data-ttu-id="d75c9-141">Stofna eða velja flokk rakningarnúmera sem á að setja upp.</span><span class="sxs-lookup"><span data-stu-id="d75c9-141">Create or select the tracking number group to set up.</span></span>
1. <span data-ttu-id="d75c9-142">Í flipanum **Almennt** skal stilla valkostinn **Handvirkt** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="d75c9-142">On the **General** FastTab, set the **Manual** option to **Yes**.</span></span>

    <span data-ttu-id="d75c9-143">![Síða rakningarnúmeraflokka](media/tracking-number-group-manual.png "Síðaa rakningarnúmeraflokka")</span><span class="sxs-lookup"><span data-stu-id="d75c9-143">![Tracking number groups page](media/tracking-number-group-manual.png "Tracking number groups page")</span></span>

1. <span data-ttu-id="d75c9-144">Stillið önnur gildi eftir þörfum og veljið síðan þennan flokk rakningarnúmera sem flokk rununúmera fyrir útgefnar afurðir sem á að nota í þessari atburðarás.</span><span class="sxs-lookup"><span data-stu-id="d75c9-144">Set other values as you require, and then select this tracking number group as the batch number group for released products that you want to use this scenario for.</span></span>

<span data-ttu-id="d75c9-145">Þegar þessi atburðarás er notuð er reiturinn **Rununúmer** sem síðan **Tilkynna framvindu** í verkspjaldstækinu býður upp á textareitur þar sem starfsmenn geta slegið inn hvaða gildi sem er.</span><span class="sxs-lookup"><span data-stu-id="d75c9-145">When you use this scenario, the **Batch number** field that the **Report progress** page on the job card device provides is a text box where workers can enter any value.</span></span>

<span data-ttu-id="d75c9-146">![Tilkynningarsíða framvindu með reit fyrir handvirk rununúmer](media/job-card-device-batch-manual.png "Tilkynningarsíða framvindu með reit fyrir handvirk rununúmer")</span><span class="sxs-lookup"><span data-stu-id="d75c9-146">![Report progress page with a field for manual batch numbers](media/job-card-device-batch-manual.png "Report progress page with a field for manual batch numbers")</span></span>

### <a name="set-up-a-tracking-number-group-that-provides-a-list-of-predefined-batch-numbers"></a><span data-ttu-id="d75c9-147">Setja upp flokk rakningarnúmera sem býður upp á lista af fyrirframskilgreindum rununúmerum</span><span class="sxs-lookup"><span data-stu-id="d75c9-147">Set up a tracking number group that provides a list of predefined batch numbers</span></span>

<span data-ttu-id="d75c9-148">Til að bjóða upp á lista af fyrirframskilgreindum rununúmerum skal fylgja þessum skrefum til að setja upp flokk rakningarnúmera.</span><span class="sxs-lookup"><span data-stu-id="d75c9-148">To provide a list of predefined batch numbers, follow these steps to set up a tracking number group.</span></span>

1. <span data-ttu-id="d75c9-149">Farið í **Birgðastjórnun \> Uppsetning > Víddir \> Flokkar rakningarnúmera**.</span><span class="sxs-lookup"><span data-stu-id="d75c9-149">Go to **Inventory management \> Setup > Dimensions \> Tracking number groups**.</span></span>
1. <span data-ttu-id="d75c9-150">Stofna eða velja flokk rakningarnúmera sem á að setja upp.</span><span class="sxs-lookup"><span data-stu-id="d75c9-150">Create or select the tracking number group to set up.</span></span>
1. <span data-ttu-id="d75c9-151">Í flipanum **Almennt** skal stilla valkostinn **Aðeins fyrir birgðafærslur** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="d75c9-151">On the **General** FastTab, set the **Only for inventory transactions** option to **Yes**.</span></span>
1. <span data-ttu-id="d75c9-152">Notið reitinn **Á magn** til að skipta rununúmerum eftir magni byggt á gildinu sem slegið er inn.</span><span class="sxs-lookup"><span data-stu-id="d75c9-152">Use the **Per qty.** field to split batch numbers per quantity, based on the value that you enter.</span></span> <span data-ttu-id="d75c9-153">Til dæmis er hægt að hafa framleiðslupöntun fyrir tíu stykki og reiturinn **Á magn** er stilltur á *2*.</span><span class="sxs-lookup"><span data-stu-id="d75c9-153">For example, you have a production order for ten pieces, and the **Per qty.** field is set to *2*.</span></span> <span data-ttu-id="d75c9-154">Í þessu tilfelli verður fimm rununúmerum úthlutað á framleiðslupöntunina þegar hún er stofnuð.</span><span class="sxs-lookup"><span data-stu-id="d75c9-154">In this case, five batch numbers will be assigned to the production order when it's created.</span></span>

    <span data-ttu-id="d75c9-155">![Síða rakningarnúmeraflokka](media/tracking-number-group-predefined.png "Síða rakningarnúmeraflokka")</span><span class="sxs-lookup"><span data-stu-id="d75c9-155">![Tracking number groups page](media/tracking-number-group-predefined.png "The Tracking number groups page")</span></span>

1. <span data-ttu-id="d75c9-156">Stillið önnur gildi eftir þörfum og veljið síðan þennan flokk rakningarnúmera sem flokk rununúmera fyrir útgefnar afurðir sem á að nota í þessari atburðarás.</span><span class="sxs-lookup"><span data-stu-id="d75c9-156">Set other values as you require, and then select this tracking number group as the batch number group for released products that you want to use this scenario for.</span></span>

<span data-ttu-id="d75c9-157">Þegar þessi atburðarás er notuð er reiturinn **Rununúmer** sem síðan **Tilkynna framvindu** í verkspjaldstækinu býður upp á fellilisti þar sem starfsmenn verða að velja fyrirframskilgreint gildi.</span><span class="sxs-lookup"><span data-stu-id="d75c9-157">When you use this scenario, the **Batch number** field that the **Report progress** page on the job card device provides is a drop-down list where workers must select a predefined value.</span></span>

<span data-ttu-id="d75c9-158">![Tilkynningarsíða framvindu með lista yfir fyrirframskilgreind rununúmer](media/job-card-device-batch-predefined.png "Tilkynningarsíða framvindu með lista yfir fyrirframskilgreind rununúmer")</span><span class="sxs-lookup"><span data-stu-id="d75c9-158">![Report progress page with a list of predefined batch numbers](media/job-card-device-batch-predefined.png "Report progress page with a list of predefined batch numbers")</span></span>

### <a name="set-up-a-tracking-number-group-that-automatically-assigns-batch-numbers"></a><span data-ttu-id="d75c9-159">Setja upp flokk rakningarnúmera sem sjálfkrafa úthluta rununúmerum</span><span class="sxs-lookup"><span data-stu-id="d75c9-159">Set up a tracking number group that automatically assigns batch numbers</span></span>

<span data-ttu-id="d75c9-160">Ef úthluta á rununúmerum sjálfkrafa, án innsláttar starfsmanns, skal fylgja þessum skrefum til að setja upp flokk rakningarnúmera.</span><span class="sxs-lookup"><span data-stu-id="d75c9-160">If batch numbers should be assigned automatically, without worker input, follow these steps to set up a tracking number group.</span></span>

1. <span data-ttu-id="d75c9-161">Farið í **Birgðastjórnun \> Uppsetning \> Víddir \> Flokkar rakningarnúmera**.</span><span class="sxs-lookup"><span data-stu-id="d75c9-161">Go to **Inventory management \> Setup \> Dimensions \> Tracking number groups**.</span></span>
1. <span data-ttu-id="d75c9-162">Stofna eða velja flokk rakningarnúmera sem á að setja upp.</span><span class="sxs-lookup"><span data-stu-id="d75c9-162">Create or select the tracking number group to set up.</span></span>
1. <span data-ttu-id="d75c9-163">Í flipanum **Almennt** skal stilla valkostinn **Aðeins fyrir birgðafærslur** á **Nei**.</span><span class="sxs-lookup"><span data-stu-id="d75c9-163">On the **General** FastTab, set the **Only for inventory transactions** option to **No**.</span></span>
1. <span data-ttu-id="d75c9-164">Stillið **Handvirkt** valkostinn á **Nei**.</span><span class="sxs-lookup"><span data-stu-id="d75c9-164">Set the **Manual** option to **No**.</span></span>

    <span data-ttu-id="d75c9-165">![Síða rakningarnúmeraflokka](media/tracking-number-group-fixed.png "Síðaa rakningarnúmeraflokka")</span><span class="sxs-lookup"><span data-stu-id="d75c9-165">![Tracking number groups page](media/tracking-number-group-fixed.png "Tracking number groups page")</span></span>

1. <span data-ttu-id="d75c9-166">Stillið önnur gildi eftir þörfum og veljið síðan þennan flokk rakningarnúmera sem flokk rununúmera fyrir útgefnar afurðir sem á að nota í þessari atburðarás.</span><span class="sxs-lookup"><span data-stu-id="d75c9-166">Set other values as you require, and then select this tracking number group as the batch number group for released products that you want to use this scenario for.</span></span>

<span data-ttu-id="d75c9-167">Þegar þessi atburðarás er notuð mun reiturinn **Rununúmer** sem síðan **Tilkynna framvindu** í verkspjaldstækinu býður upp á sýna gildi, en starfsmenn geta ekki breytt því.</span><span class="sxs-lookup"><span data-stu-id="d75c9-167">When you use this scenario, the **Batch number** field that the **Report progress** page on the job card device provides shows a value, but workers can't edit it.</span></span>

<span data-ttu-id="d75c9-168">![Tilkynningarsíða framvindu með ákveðnu rununúmeri](media/job-card-device-batch-fixed.png "Tilkynningarsíða framvindu með ákveðnu rununúmeri")</span><span class="sxs-lookup"><span data-stu-id="d75c9-168">![Report progress page with a fixed batch number](media/job-card-device-batch-fixed.png "Report progress page with a fixed batch number")</span></span>

## <a name="report-as-finished-to-a-license-plate"></a><span data-ttu-id="d75c9-169">Tilkynna sem lokið til númeraplötu</span><span class="sxs-lookup"><span data-stu-id="d75c9-169">Report as finished to a license plate</span></span>

<span data-ttu-id="d75c9-170">Ítarleg vöruhúsaferli geta notað númeraplötuvídd til að rekja birgðir í vöruhúsastaðsetningum sem hafa verið settar upp í þessum tilgangi.</span><span class="sxs-lookup"><span data-stu-id="d75c9-170">Advanced warehouse processes can use the license plate dimension to track inventory on warehouse locations that have been set up for this purpose.</span></span> <span data-ttu-id="d75c9-171">Í þessu tilvikum er krafist númer númeraplötu starfskraftur tilkynnir magn sem lokið.</span><span class="sxs-lookup"><span data-stu-id="d75c9-171">In this case, the license plate number is required when a worker reports quantities as finished.</span></span>

### <a name="enable-license-plate-reporting-and-label-printing"></a><span data-ttu-id="d75c9-172">Virkja tilkynningu númeraplötu og prentun merkis</span><span class="sxs-lookup"><span data-stu-id="d75c9-172">Enable license plate reporting and label printing</span></span>

<span data-ttu-id="d75c9-173">Til að nota eiginleikana sem lýst er í þessum hluta þarf að nota [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að kveikja á eftirfarandi eiginleikum (í þessari röð):</span><span class="sxs-lookup"><span data-stu-id="d75c9-173">To use the features that are described in this section, you must use [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn on the following features (in this order):</span></span>

1. <span data-ttu-id="d75c9-174">Númeraplata fyrir tilkynningu um lok var bætt við verkspjaldstækið</span><span class="sxs-lookup"><span data-stu-id="d75c9-174">License plate for reporting as finished added to the Job Card Device</span></span>
1. <span data-ttu-id="d75c9-175">Kveiktu á sjálfvirkri myndun á númeraplötunúmeri þegar tilkynnt er um lok í verkspjaldstækinu.</span><span class="sxs-lookup"><span data-stu-id="d75c9-175">Enable automatic generation of license plate number when reporting as finished in the job card device</span></span>
1. <span data-ttu-id="d75c9-176">Prenta merki úr verkspjaldstæki</span><span class="sxs-lookup"><span data-stu-id="d75c9-176">Print label from Job Card Device</span></span>

### <a name="set-up-reporting-as-finished-to-a-license-plate"></a><span data-ttu-id="d75c9-177">Setja upp tilkynna sem lokið til númeraplötu</span><span class="sxs-lookup"><span data-stu-id="d75c9-177">Set up reporting as finished to a license plate</span></span>

<span data-ttu-id="d75c9-178">Til að geta stjórnað því hvort starfsmenn ættu að endurnýta fyrirliggjandi númeraplötu eða mynda nýja númeraplöttu þegar þeir tilkynna að magn sé búið skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="d75c9-178">To control whether workers should reuse an existing license plate or generate a new license plate when they report quantities as finished, follow these steps.</span></span>

1. <span data-ttu-id="d75c9-179">Farið í **Framleiðslustjórnun \> Uppsetning \> Framkvæmd framleiðslu \> Skilgreina verkspjald fyrir tæki**.</span><span class="sxs-lookup"><span data-stu-id="d75c9-179">Go to **Production control \> Setup \> Manufacturing execution \> Configure job card for devices**.</span></span>
2. <span data-ttu-id="d75c9-180">Velja eftirfarandi valmöguleika fyrir hvert tæki:</span><span class="sxs-lookup"><span data-stu-id="d75c9-180">Set the following options for each device:</span></span>

    - <span data-ttu-id="d75c9-181">**Mynda númeraplötu** - Stillið þennan valkost á **Já** til að mynda nýja númeraplötu fyrir hverja tilkynningu um lokið.</span><span class="sxs-lookup"><span data-stu-id="d75c9-181">**Generate license plate** – Set this option to **Yes** to generate a new license plate for each report as finished.</span></span> <span data-ttu-id="d75c9-182">Stillið hann á **Nei** ef nota á fyrirliggjandi númeraplötu fyrir hverja tilkynningu um lokið.</span><span class="sxs-lookup"><span data-stu-id="d75c9-182">Set it to **No** if an existing license plate should be used for each report as finished.</span></span>
    - <span data-ttu-id="d75c9-183">**Prenta merki** – Stillið þennan valkost á **Já** ef starfsmaðurinn verður að prenta númeraplötumerki fyrir hverja tilkynningu um lokið.</span><span class="sxs-lookup"><span data-stu-id="d75c9-183">**Print label** – Set this option to **Yes** if the worker must print a license plate label for each report as finished.</span></span> <span data-ttu-id="d75c9-184">Stillið þetta á **Nei** ef engra merkinga er krafist.</span><span class="sxs-lookup"><span data-stu-id="d75c9-184">Set it to **No** if no label is required.</span></span> 

<span data-ttu-id="d75c9-185">![Síðan fyrir skilgreiningu verkspjalds fyrir tæki](media/config-job-card-raf.png "Síðan fyrir skilgreiningu verkspjalds fyrir tæki")</span><span class="sxs-lookup"><span data-stu-id="d75c9-185">![Configure job card for devices page](media/config-job-card-raf.png "Configure job card for devices page")</span></span>

> [!NOTE]
> <span data-ttu-id="d75c9-186">Til að skilgreina merkið skal fara í **Vöruhúsastjórnun \> Uppsetning \> Skjalaleið \> Skjalaleið**.</span><span class="sxs-lookup"><span data-stu-id="d75c9-186">To configure the label, go to **Warehouse management \> Setup \> Document routing \> Document routing**.</span></span> <span data-ttu-id="d75c9-187">Frekari upplýsingar er að finna í [Leyfa prentun númeraplötumerkis](../warehousing/tasks/license-plate-label-printing.md).</span><span class="sxs-lookup"><span data-stu-id="d75c9-187">For more information, see [Enable license plate label printing](../warehousing/tasks/license-plate-label-printing.md).</span></span>
