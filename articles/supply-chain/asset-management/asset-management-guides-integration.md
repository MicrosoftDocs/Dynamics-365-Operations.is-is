---
title: Samþætta Dynamics 365 Supply Chain Management (eignastýringu) við Dynamics 365 Guides
description: Í þessu efnisatriði er útskýrt hvernig á að samþætta einingu eignastýringar í Microsoft Dynamics 365 Supply Chain Management við Dynamics 365 Guides til að nýta leiðarvísa blandaðs veruleika í daglegum þjónustu- og viðhaldsverkflæðum.
author: kamaybac
manager: tfehr
ms.date: 04/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2020-04-28
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: f9ee7f1af8e88f56589c84bfaa063ea005aa353a
ms.sourcegitcommit: 88b4a9d19d16b0ef6543adf7c378a08bf0e07b3a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/29/2020
ms.locfileid: "3311782"
---
# <a name="integrate-dynamics-365-supply-chain-management-asset-management-with-dynamics-365-guides"></a><span data-ttu-id="d3cd3-103">Samþætta Dynamics 365 Supply Chain Management (eignastýringu) við Dynamics 365 Guides</span><span class="sxs-lookup"><span data-stu-id="d3cd3-103">Integrate Dynamics 365 Supply Chain Management (Asset management) with Dynamics 365 Guides</span></span>

<span data-ttu-id="d3cd3-104">Hægt er að samþætta eininguna **Eignastýring** í Microsoft Dynamics 365 Supply Chain Management við Dynamics 365 Guides til að nýta leiðarvísa blandaðs veruleika í daglegum þjónustu- og viðhaldsverkflæðum.</span><span class="sxs-lookup"><span data-stu-id="d3cd3-104">You can integrate the **Asset management** module in Microsoft Dynamics 365 Supply Chain Management with Dynamics 365 Guides to take advantage of mixed-reality guides in your day-to-day service and maintenance workflows.</span></span> <span data-ttu-id="d3cd3-105">Ef leiðarvísir er tengdur verkbeiðni eignastýringar, sér starfsmaður sem opnar viðhaldsgátlista verkbeiðni í farsímaforriti Supply Chain Management (Dynamics 365) að leiðarvísir er í boði.</span><span class="sxs-lookup"><span data-stu-id="d3cd3-105">If a guide is associated with an Asset Management work order, a worker who opens the work order's maintenance checklist in the Supply Chain Management (Dynamics 365) mobile app sees that a guide is available.</span></span> <span data-ttu-id="d3cd3-106">Starfsmaðurinn getur þá fundið og opnað leiðarvísinn í Dynamics 365 Guides HoloLens forritinu.</span><span class="sxs-lookup"><span data-stu-id="d3cd3-106">The worker can then find and open the guide in the Dynamics 365 Guides HoloLens app.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="d3cd3-107">Forkröfur</span><span class="sxs-lookup"><span data-stu-id="d3cd3-107">Prerequisites</span></span>

<span data-ttu-id="d3cd3-108">Áður en hægt er að hengja leiðarvísa við verkbeiðnir eignastýringar þarf að uppfylla þessi skilyrði:</span><span class="sxs-lookup"><span data-stu-id="d3cd3-108">Before you can attach guides to Asset management work orders, you must complete these prerequisites:</span></span>

- <span data-ttu-id="d3cd3-109">[Setja upp Dynamics 365 Supply Chain Management](../../fin-ops-core/fin-ops/index.md) útgáfa 10.0.9 eða nýrri.</span><span class="sxs-lookup"><span data-stu-id="d3cd3-109">[Set up Dynamics 365 Supply Chain Management](../../fin-ops-core/fin-ops/index.md) version 10.0.9 or later.</span></span>
- <span data-ttu-id="d3cd3-110">[Kveikja á tvískiptum skrifum fyrir forrit Supply Chain Management](../../fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write.md).</span><span class="sxs-lookup"><span data-stu-id="d3cd3-110">[Turn on dual-write for Supply Chain Management apps](../../fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write.md).</span></span>
- <span data-ttu-id="d3cd3-111">[Kveikja á forútgáfu](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md#features-flighted-in-data-management-and-enabling-flighted-features) fyrir eiginleikann **MRGuidesFeature**.</span><span class="sxs-lookup"><span data-stu-id="d3cd3-111">[Turn on flight](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md#features-flighted-in-data-management-and-enabling-flighted-features) for the **MRGuidesFeature** feature.</span></span> <span data-ttu-id="d3cd3-112">(Fyrir vinnsluumhverfi þarf fyrst að senda inn þjónustubeiðni til að leigjandanum þínum verði bætt við forútgáfuhópinn.)</span><span class="sxs-lookup"><span data-stu-id="d3cd3-112">(For production environments, you must first submit a support ticket to have your tenant added to the flighting group.)</span></span>
- <span data-ttu-id="d3cd3-113">[Kveikja á eftirfarandi skilgreiningarlyklum](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/license-code-and-configuration-key-reference) á síðunni **Leyfisskilgreining**:</span><span class="sxs-lookup"><span data-stu-id="d3cd3-113">[Turn on the following configuration keys](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/license-code-and-configuration-key-reference) on the **License configuration** page:</span></span>

    - <span data-ttu-id="d3cd3-114">Bandaður veruleiki eignarstýringar fyrir \> eignastýringu</span><span class="sxs-lookup"><span data-stu-id="d3cd3-114">Asset management \> Asset management mixed reality</span></span>
    - <span data-ttu-id="d3cd3-115">Leiðarvísir blandaðs veruleika fyrir blandaðan veruleika \></span><span class="sxs-lookup"><span data-stu-id="d3cd3-115">Mixed reality \> Mixed reality guide</span></span>

- <span data-ttu-id="d3cd3-116">[Setja upp Dynamics 365 Guides](https://docs.microsoft.com/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution) útgáfa 200.0.0.96 eða nýrri.</span><span class="sxs-lookup"><span data-stu-id="d3cd3-116">[Set up Dynamics 365 Guides](https://docs.microsoft.com/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution) version 200.0.0.96 or later.</span></span>

## <a name="use-dynamics-365-guides-with-asset-management"></a><span data-ttu-id="d3cd3-117">Nota Dynamics 365 Guides með eignastýringu</span><span class="sxs-lookup"><span data-stu-id="d3cd3-117">Use Dynamics 365 Guides with Asset management</span></span>

<span data-ttu-id="d3cd3-118">Til að tengja leiðarvísi er notuð lína viðhaldsgátlista í eignastýringu.</span><span class="sxs-lookup"><span data-stu-id="d3cd3-118">To associate a guide, you use a maintenance checklist line in Asset management.</span></span> <span data-ttu-id="d3cd3-119">Hægt er að stofna tenginguna í gegnum sniðmát viðhaldsgátlista, gerð viðhaldsverks eða verkbeiðni af því að þetta þrennt inniheldur línur viðhaldsgátlista.</span><span class="sxs-lookup"><span data-stu-id="d3cd3-119">You can create the association through a maintenance checklist template, a maintenance job type, or a work order, because all three contain maintenance checklist lines.</span></span> <span data-ttu-id="d3cd3-120">Hægt er að spara tíma með því að nota sniðmát því að hægt er að tengja sniðmát við allar gerðir viðhaldsverka sem nota það.</span><span class="sxs-lookup"><span data-stu-id="d3cd3-120">You can save time by using a template, because a template can be associated with all the maintenance job types that use it.</span></span> <span data-ttu-id="d3cd3-121">Til dæmis er leiðarvísi sem tengist viðhaldsverkgerð sjálfkrafa tengdur við allar verkbeiðnir sem heyra undir þessa verkgerð.</span><span class="sxs-lookup"><span data-stu-id="d3cd3-121">For example, a guide that is associated with a maintenance job type is automatically associated with all work orders that specify that job type.</span></span> <span data-ttu-id="d3cd3-122">Hins vegar er leiðarvísi sem tengist ákveðinni verkbeiðni aðeins til fyrir þá verkbeiðni.</span><span class="sxs-lookup"><span data-stu-id="d3cd3-122">On the other hand, a guide that is associated directly with a work order exists only for that work order.</span></span>

### <a name="associate-a-guide-with-a-maintenance-checklist-template"></a><span data-ttu-id="d3cd3-123">Tengja leiðarvísi við sniðmát viðhaldsgátlista</span><span class="sxs-lookup"><span data-stu-id="d3cd3-123">Associate a guide with a maintenance checklist template</span></span>

<span data-ttu-id="d3cd3-124">Til að tengja leiðarvísi við sniðmát viðhaldsgátlista skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="d3cd3-124">To associate a guide with a maintenance checklist template, follow these steps.</span></span>

1. <span data-ttu-id="d3cd3-125">Búðu til leiðarvísi með því að nota Dynamics 365 Guides tölvuna og HoloLens forritin.</span><span class="sxs-lookup"><span data-stu-id="d3cd3-125">Create a guide by using the Dynamics 365 Guides PC and HoloLens apps.</span></span> <span data-ttu-id="d3cd3-126">Nánari upplýsingar um hvernig á að búa til leiðarvísi er að finna í eftirfarandi efnisatriðum:</span><span class="sxs-lookup"><span data-stu-id="d3cd3-126">For information about how to create a guide, see the following topics:</span></span>

    - [<span data-ttu-id="d3cd3-127">Notaðu tölvuforritið til að búa til leiðarvísi</span><span class="sxs-lookup"><span data-stu-id="d3cd3-127">Use the PC app to create a guide</span></span>](https://docs.microsoft.com/dynamics365/mixed-reality/guides/pc-app-overview)
    - [<span data-ttu-id="d3cd3-128">Nota HoloLens-forritið til að staðsetja heilmyndirnar</span><span class="sxs-lookup"><span data-stu-id="d3cd3-128">Use the HoloLens app to place your holograms</span></span>](https://docs.microsoft.com/dynamics365/mixed-reality/guides/hololens-app-overview)

1. <span data-ttu-id="d3cd3-129">Í Supply Chain Management skal [búa til sniðmát viðhaldsgátlista](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-checklist-template).</span><span class="sxs-lookup"><span data-stu-id="d3cd3-129">In Supply Chain Management, [create a maintenance checklist template](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-checklist-template).</span></span>
1. <span data-ttu-id="d3cd3-130">Tengið leiðarvísinn sem var búinn til við línu viðhaldsgátlista í nýju sniðmáti viðhaldsgátlista:</span><span class="sxs-lookup"><span data-stu-id="d3cd3-130">Associate the guide that you created with a maintenance checklist line in the new maintenance checklist template:</span></span>

    1. <span data-ttu-id="d3cd3-131">Í flýtiflipanum **Línur viðhaldsgátlista** skal velja línuna sem á að tengjast leiðarvísinum.</span><span class="sxs-lookup"><span data-stu-id="d3cd3-131">On the **Maintenance checklist lines** FastTab, select the line that you want to associate the guide with.</span></span>
    1. <span data-ttu-id="d3cd3-132">Í flýtiflipanum **Tengdir leiðarvísar** skal velja **Bæta við leiðarvísi**.</span><span class="sxs-lookup"><span data-stu-id="d3cd3-132">On the **Associated guides** FastTab, select **Add Guide**.</span></span>

        <span data-ttu-id="d3cd3-133">![Tengja leiðarvísi við línu viðhaldsgátlista](media/am-guides-integration-add-guide.png "Tengja leiðarvísi við línu viðhaldsgátlista")</span><span class="sxs-lookup"><span data-stu-id="d3cd3-133">![Associate a guide with a maintenance checklist line](media/am-guides-integration-add-guide.png "Associate a guide with a maintenance checklist line")</span></span>

    1. <span data-ttu-id="d3cd3-134">Í reitnum **Heiti** skal velja leiðarvísi og síðan velja **Vista**.</span><span class="sxs-lookup"><span data-stu-id="d3cd3-134">In the **Name** field, select a guide, and then select **Save**.</span></span>

        <span data-ttu-id="d3cd3-135">![Velja leiðarvísi í reitnum Heiti](media/am-guides-integration-select-guide.png "Velja leiðarvísi í reitnum Heiti")</span><span class="sxs-lookup"><span data-stu-id="d3cd3-135">![Select a guide in the Name field](media/am-guides-integration-select-guide.png "Select a guide in the Name field")</span></span>

1. <span data-ttu-id="d3cd3-136">Tengið sniðmát viðhaldsgátlista við gerð verks:</span><span class="sxs-lookup"><span data-stu-id="d3cd3-136">Associate the maintenance checklist template with a job type:</span></span>

    1. <span data-ttu-id="d3cd3-137">[Búa til gerð viðhaldsverks](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-job-type) eða velja fyrirliggjandi gerð viðhaldsverks.</span><span class="sxs-lookup"><span data-stu-id="d3cd3-137">[Create a maintenance job type](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-job-type), or select an existing maintenance job type.</span></span>
    1. <span data-ttu-id="d3cd3-138">Á aðgerðasvæðinu skal velja **Sjálfgefnar gerðir viðhaldsverks**.</span><span class="sxs-lookup"><span data-stu-id="d3cd3-138">On the Action Pane, select **Maintenance job type defaults**.</span></span>

        <span data-ttu-id="d3cd3-139">![Hnappur fyrir sjálfgefna gerð viðhaldsverks](media/am-guides-integration-job-defaults.png "Hnappur sjálfgildis gerða viðhaldsverks")</span><span class="sxs-lookup"><span data-stu-id="d3cd3-139">![Maintenance job type defaults button](media/am-guides-integration-job-defaults.png "Maintenance job type defaults button")</span></span>

    1. <span data-ttu-id="d3cd3-140">Stofnaðu línu og veldu síðan **Vista**.</span><span class="sxs-lookup"><span data-stu-id="d3cd3-140">Create a line, and then select **Save**.</span></span>

        <span data-ttu-id="d3cd3-141">![Stofna línu](media/am-guides-integration-add-line.png "Stofna línu")</span><span class="sxs-lookup"><span data-stu-id="d3cd3-141">![Create a line](media/am-guides-integration-add-line.png "Create a line")</span></span>

    1. <span data-ttu-id="d3cd3-142">Á aðgerðasvæðinu skal velja **Viðhaldsgátlisti**.</span><span class="sxs-lookup"><span data-stu-id="d3cd3-142">On the Action Pane, select **Maintenance checklist**.</span></span>

        <span data-ttu-id="d3cd3-143">![Viðhaldsgátlistahnappur](media/am-guides-integration-maintenance-checklist.png "Viðhaldsgátlistahnappur")</span><span class="sxs-lookup"><span data-stu-id="d3cd3-143">![Maintenance checklist button](media/am-guides-integration-maintenance-checklist.png "Maintenance checklist button")</span></span>

    1. <span data-ttu-id="d3cd3-144">Í flýtiflipanum **Viðhaldsgátlisti** skal bæta við línu og síðan breyta gildinu í reitnum **Gerð** í **Sniðmát**.</span><span class="sxs-lookup"><span data-stu-id="d3cd3-144">On the **Maintenance checklist lines** FastTab, add a line, and then change the value of the **Type** field to **Template**.</span></span>

        <span data-ttu-id="d3cd3-145">![Breyta gildisgerð](media/am-guides-integration-checklist-lines.png "Breyta gildisgerð")</span><span class="sxs-lookup"><span data-stu-id="d3cd3-145">![Change the Type value](media/am-guides-integration-checklist-lines.png "Change the Type value")</span></span>

    1. <span data-ttu-id="d3cd3-146">Í flýtiflipanum **Upplýsingar um línu**, í reitnum **Sniðmát**, skal velja sniðmátið sem þú tengdir leiðarvísinn við og velja síðan **Vista**.</span><span class="sxs-lookup"><span data-stu-id="d3cd3-146">On the **Line details** FastTab, in the **Template** field, select the template that you associated the guide with, and then select **Save**.</span></span>

        <span data-ttu-id="d3cd3-147">![Velja sniðmát](media/am-guides-integration-checklist-line-details.png "Velja sniðmát")</span><span class="sxs-lookup"><span data-stu-id="d3cd3-147">![Select the template](media/am-guides-integration-checklist-line-details.png "Select the template")</span></span>

1. <span data-ttu-id="d3cd3-148">[Búa til verkbeiðni](work-orders/manually-created-workorders.md#create-work-order) og veldu síðan gerð viðhaldsverks sem notar sniðmát viðhaldsgátlista sem þú tengdir leiðarvísinn við.</span><span class="sxs-lookup"><span data-stu-id="d3cd3-148">[Create a work order](work-orders/manually-created-workorders.md#create-work-order), and then select the maintenance job type that uses the maintenance checklist template that you associated the guide with.</span></span> <span data-ttu-id="d3cd3-149">Leiðarvísirinn tengist sjálfkrafa verkbeiðninni.</span><span class="sxs-lookup"><span data-stu-id="d3cd3-149">The guide is automatically associated with the work order.</span></span>

    <span data-ttu-id="d3cd3-150">![Velja gerð viðhaldsverks](media/am-guides-integration-create-work-order.png "Velja gerð viðhaldsverks")</span><span class="sxs-lookup"><span data-stu-id="d3cd3-150">![Select a maintenance job type](media/am-guides-integration-create-work-order.png "Select a maintenance job type")</span></span>

1. <span data-ttu-id="d3cd3-151">Skoðaðu leiðarvísinn sem tengist verkbeiðni og starfmönnum:</span><span class="sxs-lookup"><span data-stu-id="d3cd3-151">View the guide that is associated with the work order and workers:</span></span>

    1. <span data-ttu-id="d3cd3-152">Opnaðu [Fartækjavinnusvæði eignastýringar](asset-management-mobile-workspace.md) til að fá aðgang að verkbeiðninni.</span><span class="sxs-lookup"><span data-stu-id="d3cd3-152">Open the [Asset management mobile workspace](asset-management-mobile-workspace.md) to access the work order.</span></span>
    1. <span data-ttu-id="d3cd3-153">[Opnaðu viðhaldsgátlistann](asset-management-mobile-workspace.md#view-maintenance-checklist-on-a-work-order-job) fyrir verkbeiðnina.</span><span class="sxs-lookup"><span data-stu-id="d3cd3-153">[Open the maintenance checklist](asset-management-mobile-workspace.md#view-maintenance-checklist-on-a-work-order-job) for the work order.</span></span>
    1. <span data-ttu-id="d3cd3-154">Veldu gátlistalínu til að sjá tengdan leiðarvísi.</span><span class="sxs-lookup"><span data-stu-id="d3cd3-154">Select a checklist line to see the associated guide.</span></span>

        <span data-ttu-id="d3cd3-155">![Leiðarvísir sem tengist gátlistalínu](media/am-guides-integration-show-guide.png "Leiðbeiningar sem tengjast gátlistalínu")</span><span class="sxs-lookup"><span data-stu-id="d3cd3-155">![Guide associated with a checklist line](media/am-guides-integration-show-guide.png "Guide associated with a checklist line")</span></span>

    1. <span data-ttu-id="d3cd3-156">Opna leiðarvísi á HoloLens.</span><span class="sxs-lookup"><span data-stu-id="d3cd3-156">Open the guide on HoloLens.</span></span>

        <span data-ttu-id="d3cd3-157">![Opna leiðarvísi á HoloLens](media/am-guides-integration-hololens-select.png "Opna leiðarvísi á HoloLens")</span><span class="sxs-lookup"><span data-stu-id="d3cd3-157">![Open the guide on HoloLens](media/am-guides-integration-hololens-select.png "Open the guide on HoloLens")</span></span>

> [!NOTE]
> <span data-ttu-id="d3cd3-158">Einnig er hægt að tengja leiðarvísi beint í viðhaldsgátlista verkbeiðni eða verkgerðar.</span><span class="sxs-lookup"><span data-stu-id="d3cd3-158">You can also associate a guide directly in the maintenance checklist of a work order or a job type.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d3cd3-159">Þekkt vandamál er til staðar þar sem sniðmát fyrir viðhaldsgátlista er tengt við sjálfgefna viðhaldsverkgerð, leiðarvísirinn sem tengist sniðmátinu birtist ekki í flýtiflipanum **Tengdir leiðarvísar** á síðunni **Sjálfgefnar gerðir viðhaldsverks**.</span><span class="sxs-lookup"><span data-stu-id="d3cd3-159">There is a known issue where, when you associate a maintenance checklist template with a default maintenance job type, the guide that is linked to the template doesn't appear on the **Associated guides** FastTab of the **Maintenance job type defaults** page.</span></span> <span data-ttu-id="d3cd3-160">Leiðarvísirinn birtist hins vegar eftir að verkgerð er sett á verkbeiðni í flýtiflipanum **Tengdir leiðarvísar**.</span><span class="sxs-lookup"><span data-stu-id="d3cd3-160">However, the guide will appear after that job type is applied to a work order on the **Associated guides** FastTab.</span></span>

## <a name="see-also"></a><span data-ttu-id="d3cd3-161">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="d3cd3-161">See also</span></span>

- [<span data-ttu-id="d3cd3-162">Tvöföld skrif – yfirlit</span><span class="sxs-lookup"><span data-stu-id="d3cd3-162">Dual-write overview</span></span>](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview.md)
- [<span data-ttu-id="d3cd3-163">Yfirlit eignastýringar</span><span class="sxs-lookup"><span data-stu-id="d3cd3-163">Asset management overview</span></span>](index.md)
