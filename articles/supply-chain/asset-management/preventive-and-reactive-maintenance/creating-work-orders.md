---
title: Verkbeiðnir stofnaðar
description: Þetta efni útskýrir hvernig á að stofna verkbeiðnir í eignastýringu.
author: johanhoffmann
manager: tfehr
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 876aef9f3f470490bb385e1861c837dcfa82db69
ms.sourcegitcommit: 1e615288db245f83c5d5e0cd45315400f8946beb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/08/2021
ms.locfileid: "5131794"
---
# <a name="creating-work-orders"></a><span data-ttu-id="825b6-103">Verkbeiðnir stofnaðar</span><span class="sxs-lookup"><span data-stu-id="825b6-103">Creating work orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="825b6-104">Þegar fyrirbyggjandi viðhaldsverk hafa verið tímasett er næsta skref að stofna verkbeiðnir fyrir þau.</span><span class="sxs-lookup"><span data-stu-id="825b6-104">After you've scheduled preventive maintenance jobs, the next step is to create work orders for them.</span></span> <span data-ttu-id="825b6-105">Hægt er að ljúka þessu skrefi með því að nota eina af viðhaldsáætlunum.</span><span class="sxs-lookup"><span data-stu-id="825b6-105">You can complete this step by using one of the maintenance schedules.</span></span> <span data-ttu-id="825b6-106">Áætlaðar vinnslur í viðhaldsáætlun geta haft mismunandi tilvísunargerðir eins og lýst er í eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="825b6-106">The scheduled jobs in a maintenance schedule can have different reference types, as described in the following table.</span></span>

| <span data-ttu-id="825b6-107">Gerð tilvísunar</span><span class="sxs-lookup"><span data-stu-id="825b6-107">Reference type</span></span> | <span data-ttu-id="825b6-108">lýsing</span><span class="sxs-lookup"><span data-stu-id="825b6-108">Description</span></span> |
|---|---|
| <span data-ttu-id="825b6-109">Viðhaldsáætlanir</span><span class="sxs-lookup"><span data-stu-id="825b6-109">Maintenance plans</span></span> | <span data-ttu-id="825b6-110">Fyrirbyggjandi viðhaldsverk sem byggja á viðhaldsáætlunargerðinni *Tími* eða *Teljari*.</span><span class="sxs-lookup"><span data-stu-id="825b6-110">Preventive maintenance jobs that are based on the *Time* or *Counter* maintenance plan type.</span></span> |
| <span data-ttu-id="825b6-111">Viðhaldslotur</span><span class="sxs-lookup"><span data-stu-id="825b6-111">Maintenance rounds</span></span> | <span data-ttu-id="825b6-112">Fyrirbyggjand viðhaldsverk sem innihalda nokkrar eignir sem þurfa sams konar viðhald.</span><span class="sxs-lookup"><span data-stu-id="825b6-112">Preventive maintenance jobs that contain several assets that require a similar type of maintenance.</span></span> |
| <span data-ttu-id="825b6-113">Viðhaldsbeiðni</span><span class="sxs-lookup"><span data-stu-id="825b6-113">Maintenance request</span></span> | <span data-ttu-id="825b6-114">Handvirk stofnun beiðni um viðhald eða viðgerð á eign.</span><span class="sxs-lookup"><span data-stu-id="825b6-114">A manually created request for maintenance or repair of an asset.</span></span> <span data-ttu-id="825b6-115">Hægt er að umreikna þessa beiðni í verkbeiðni.</span><span class="sxs-lookup"><span data-stu-id="825b6-115">This request can be converted to a work order.</span></span> |

## <a name="create-work-orders-based-on-your-maintenance-schedule"></a><span data-ttu-id="825b6-116">Stofna verkbeiðnir út frá viðhaldsáætluninni</span><span class="sxs-lookup"><span data-stu-id="825b6-116">Create work orders based on your maintenance schedule</span></span>

<span data-ttu-id="825b6-117">Til að stofna verkbeiðnir sem byggja á viðhaldsáætluninni skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="825b6-117">To create work orders that are based on your maintenance schedule, follow these steps.</span></span>

1. <span data-ttu-id="825b6-118">Opnið eina af eftirfarandi síðum, allt eftir því hvernig velja á áætlunarvörur fyrir verkbeiðnir:</span><span class="sxs-lookup"><span data-stu-id="825b6-118">Open one of the following pages, depending on how you want to select schedule items for your work orders:</span></span>

    - <span data-ttu-id="825b6-119">Öll viðhaldsáætlun (**Eignastýring \> Áætlun stjórnunar \> Öll viðhaldsáætlun**)</span><span class="sxs-lookup"><span data-stu-id="825b6-119">All maintenance schedule (**Asset management \> Management schedule \> All maintenance schedule**)</span></span>
    - <span data-ttu-id="825b6-120">Opna viðhaldsáætlunarlínur (**Eignastýring \> Áætlun stjórnunar \> Opna áætlunarlínur viðhalds**)</span><span class="sxs-lookup"><span data-stu-id="825b6-120">Open maintenance schedule lines (**Asset management \> Management schedule \> Open maintenance schedule lines**)</span></span>
    - <span data-ttu-id="825b6-121">Opna viðhaldsáætlunarhópa (**Eignastýring \> Áætlun stjórnunar \> Opna áætlunarhópa viðhalds**)</span><span class="sxs-lookup"><span data-stu-id="825b6-121">Open maintenance schedule pools (**Asset management \> Management schedule \> Open maintenance schedule pools**)</span></span>

1. <span data-ttu-id="825b6-122">Í hnitanetinu skal velja gátreitinn fyrir hvert verk viðhaldsáætlunar sem á að stofna verkbeiðni fyrir.</span><span class="sxs-lookup"><span data-stu-id="825b6-122">In the grid, select the check box for every scheduled maintenance job that you want to create a work order for.</span></span> <span data-ttu-id="825b6-123">Á aðgerðasvæðinu skal síðan velja **Verkbeiðni**.</span><span class="sxs-lookup"><span data-stu-id="825b6-123">Then, on the Action Pane, select **Work order**.</span></span>

    <span data-ttu-id="825b6-124">Gátreiturinn **Stofna verkbeiðnir** birtist.</span><span class="sxs-lookup"><span data-stu-id="825b6-124">The **Create work orders** dialog box appears.</span></span> <span data-ttu-id="825b6-125">Reiturinn **Vinnustundir viðhaldsspár** sýnir heildarfjölda vinnustunda fyrir spá fyrir valdar línur.</span><span class="sxs-lookup"><span data-stu-id="825b6-125">The **Maintenance forecast hours** field shows the total number of forecast hours for the selected lines.</span></span>

    ![Búa til svarglugga verkbeiðna](media/18-preventive-maintenance.png)

1. <span data-ttu-id="825b6-127">Í hlutanum **Færibreytur** skal tilgreina þann fjölda verkbeiðna sem á að stofna.</span><span class="sxs-lookup"><span data-stu-id="825b6-127">In the **Parameters** section, specify the number of work orders that should be created.</span></span> <span data-ttu-id="825b6-128">Veldu einn af eftirfarandi valkostum:</span><span class="sxs-lookup"><span data-stu-id="825b6-128">Select one of the following options:</span></span>

    - <span data-ttu-id="825b6-129">**Ein verkbeiðni á línu** – Stofnið eina verkbeiðni á hverja viðhaldsáætlunarlínu.</span><span class="sxs-lookup"><span data-stu-id="825b6-129">**One work order per line** – Create one work order per maintenance schedule line.</span></span>
    - <span data-ttu-id="825b6-130">**Ein verkbeiðni á** – Stofnið verkbeiðnir sem eru flokkaðar samkvæmt stillingum hinna valkostanna sem verða tiltækir þegar þessi valkostur er valinn.</span><span class="sxs-lookup"><span data-stu-id="825b6-130">**One work order per** – Create work orders that are grouped according to the settings of the other options that become available when you select this option.</span></span>

1. <span data-ttu-id="825b6-131">Í reitnum **Gerð verkbeiðni** skal velja verkbeiðnigerðina sem á að nota fyrir allar verkbeiðnir sem eru stofnaðar.</span><span class="sxs-lookup"><span data-stu-id="825b6-131">In the **Work order type** field, select the work order type to use for all the work orders that you create.</span></span>
1. <span data-ttu-id="825b6-132">Veljið **Í lagi** til að stofna verkbeiðnir samkvæmt stillingunum.</span><span class="sxs-lookup"><span data-stu-id="825b6-132">Select **OK** to create the work orders according to your settings.</span></span>

## <a name="group-work-order-lines-that-are-automatically-created-while-a-maintenance-plan-runs"></a><span data-ttu-id="825b6-133">Flokka verkbeiðnilínur sem eru sjálfkrafa stofnaðar meðan á viðhaldsáætlun stendur</span><span class="sxs-lookup"><span data-stu-id="825b6-133">Group work order lines that are automatically created while a maintenance plan runs</span></span>

> [!IMPORTANT]
> <span data-ttu-id="825b6-134">Virkni sem lýst er í þessum hluta er tiltæk sem hluti af sérstakri prufuútgáfu.</span><span class="sxs-lookup"><span data-stu-id="825b6-134">The functionality that is described in this section is available as part of a preview release.</span></span> <span data-ttu-id="825b6-135">Innihald og virkni geta tekið breytingum.</span><span class="sxs-lookup"><span data-stu-id="825b6-135">The content and the functionality are subject to change.</span></span> <span data-ttu-id="825b6-136">Frekari upplýsingar um forútgáfur er að finna í hlutanum [Algengar spurningar um uppfærslureglur fyrir „Ein útgáfa“](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/one-version).</span><span class="sxs-lookup"><span data-stu-id="825b6-136">For more information about preview releases, see [One version service updates FAQ](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/one-version).</span></span>

<span data-ttu-id="825b6-137">Þessi eiginleiki gerir kleift að skilgreina reglur fyrir flokkun verkbeiðnilína undir einni verkbeiðni þegar kerfið er stillt á að búa sjálfkrafa til verkbeiðnir sem byggja á viðhaldsáætlun.</span><span class="sxs-lookup"><span data-stu-id="825b6-137">This feature lets you define rules for grouping work order lines under a single work order when the system is set up to generate work orders automatically, based on a maintenance plan.</span></span> <span data-ttu-id="825b6-138">Áður gátu sjálfkrafa myndaðar verkbeiðnir aðeins innihaldið eina línu.</span><span class="sxs-lookup"><span data-stu-id="825b6-138">Previously, automatically generated work orders could contain only one line.</span></span> <span data-ttu-id="825b6-139">Nú er hins vegar hægt að flokka verkbeiðnir eftir til dæmis eign, eignagerð eða virkri staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="825b6-139">However, you can now group work orders by, for example, asset, asset type, or functional location.</span></span> <span data-ttu-id="825b6-140">(Handvirkt myndaðar verkbeiðnir var aðeins hægt að flokka á þennan hátt eins og lýst er í hlutanum hér á undan í þessu efnisatriði.)</span><span class="sxs-lookup"><span data-stu-id="825b6-140">(Manually generated work orders could already be grouped in this way, as described in the previous section of this topic.)</span></span>

### <a name="enable-grouping-for-automatically-generated-work-orders"></a><span data-ttu-id="825b6-141">Virkja flokkun fyrir sjálfkrafa myndaðar verkbeiðnir</span><span class="sxs-lookup"><span data-stu-id="825b6-141">Enable grouping for automatically generated work orders</span></span>

<span data-ttu-id="825b6-142">Áður en hægt er að nota þennan eiginleika þarf að kveikja á honum í kerfinu.</span><span class="sxs-lookup"><span data-stu-id="825b6-142">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="825b6-143">Stjórnendur geta notað stillingarnar [eiginleikastjórnun](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og kveikja á honum.</span><span class="sxs-lookup"><span data-stu-id="825b6-143">Admins can use the [feature management](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="825b6-144">Á vinnusvæðinu **Eiginleikastjórnun** er eiginleikinn tilgreindur á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="825b6-144">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="825b6-145">**Eining:** *Eignastjórnun*</span><span class="sxs-lookup"><span data-stu-id="825b6-145">**Module:** *Asset Management*</span></span>
- <span data-ttu-id="825b6-146">**Heiti eiginleika:** *(Forskoðun) Notið reglur fyrir flokkun verkbeiðna á meðan viðhaldsáætlun er keyrð*</span><span class="sxs-lookup"><span data-stu-id="825b6-146">**Feature name:** *(Preview) Apply rules for grouping work orders while running a maintenance plan*</span></span>

### <a name="set-up-grouping-for-automatically-generated-work-orders"></a><span data-ttu-id="825b6-147">Setja upp flokkun fyrir sjálfkrafa myndaðar verkbeiðnir</span><span class="sxs-lookup"><span data-stu-id="825b6-147">Set up grouping for automatically generated work orders</span></span>

<span data-ttu-id="825b6-148">Til að setja upp flokkun fyrir sjálfkrafa myndaðar verkbeiðnir skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="825b6-148">To set up grouping for automatically generated work orders, follow these steps.</span></span>

1. <span data-ttu-id="825b6-149">Farið í **Eignastýring \> Uppsetning \> Fyrirbyggjandi viðhald \> Viðhaldsáætlanir**.</span><span class="sxs-lookup"><span data-stu-id="825b6-149">Go to **Asset management \> Setup \> Preventative maintenance \> Maintenance plans**.</span></span>
1. <span data-ttu-id="825b6-150">Fyrir hverja áætlun þar sem á að mynda flokkaðar verkbeiðnir skal fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="825b6-150">For each plan where you want to generate grouped work orders, follow these steps:</span></span>

    1. <span data-ttu-id="825b6-151">Velja skal áætlunina á listasvæðinu.</span><span class="sxs-lookup"><span data-stu-id="825b6-151">Select the plan in the list pane.</span></span>
    1. <span data-ttu-id="825b6-152">Í flýtiflipanum **Línur** skal ganga úr skugga um að gátreiturinn **Stofna sjálfvirkt** sé valinn í hverri línu.</span><span class="sxs-lookup"><span data-stu-id="825b6-152">On the **Lines** FastTab, make sure that the **Auto create** check box is selected on every line.</span></span>

1. <span data-ttu-id="825b6-153">Farið í **Eignastýring \> Reglubundið \> Fyrirbyggjandi viðhald \> Tímasetja viðhaldsáætlanir**.</span><span class="sxs-lookup"><span data-stu-id="825b6-153">Go to **Asset management \> Periodic \> Preventive maintenance \> Schedule maintenance plans**.</span></span>
1. <span data-ttu-id="825b6-154">Í svarglugganum **Tímasetja viðhaldsáætlanir**, í hlutanum **Tímabil**, skal tilgreina hámarkstíma fyrir áætlunina (hversu langt fram í tímann er horft þegar fundin eru verk viðhaldsáætlunar til að mynda vinnu fyrir).</span><span class="sxs-lookup"><span data-stu-id="825b6-154">In the **Schedule maintenance plans** dialog box, in the **Period** section, specify the time horizon for the plan (how far to look ahead when finding scheduled maintenance jobs to generate work for).</span></span>
1. <span data-ttu-id="825b6-155">Stillið valkostinn **Stofna verkbeiðni sjálfkrafa úr áætlun** á *Já*.</span><span class="sxs-lookup"><span data-stu-id="825b6-155">Set the **Automatically create work order from schedule** option to *Yes*.</span></span>
1. <span data-ttu-id="825b6-156">Veldu einn af eftirfarandi valkostum í hlutanum **Verkbeiðni**:</span><span class="sxs-lookup"><span data-stu-id="825b6-156">In the **Work order** section, select one of the following options:</span></span>

    - <span data-ttu-id="825b6-157">**Ein verkbeiðni á línu** – Stofnið eina verkbeiðni á hverja viðhaldsáætlunarlínu.</span><span class="sxs-lookup"><span data-stu-id="825b6-157">**One work order per line** – Create one work order per maintenance schedule line.</span></span> <span data-ttu-id="825b6-158">(Þessi valkostur veitir sömu virkni og er tiltæk þegar slökkt er á eiginleikanum *Nota reglur fyrir flokkun verkbeiðna á meðan viðhaldsáætlun er keyrð*.)</span><span class="sxs-lookup"><span data-stu-id="825b6-158">(This option provides the same functionality that is available when the *Apply rules for grouping work orders while running a maintenance plan* feature is turned off.)</span></span>
    - <span data-ttu-id="825b6-159">**Ein verkbeiðni á** – Stofnið verkbeiðnir sem eru flokkaðar samkvæmt stillingum hinna valkostanna sem verða tiltækir þegar þessi valkostur er valinn.</span><span class="sxs-lookup"><span data-stu-id="825b6-159">**One work order per** – Create work orders that are grouped according to the settings of the other options that become available when you select this option.</span></span>

1. <span data-ttu-id="825b6-160">Ef ætlunin er að valkostirnir séu notaðir þegar aðeins sumar viðhaldsáætlanir eru keyrðar skal í flýtiflipanum **Færslur til að taka með** sía eftir þörfum, rétt eins og yrði gert fyrir aðrar runuvinnslur í Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="825b6-160">If you want the options to apply when you run only some of your maintenance plans, on the **Records to include** FastTab, add filters as you require, just as you might do for other batch jobs in Microsoft Dynamics 365 Supply Chain Management.</span></span>
1. <span data-ttu-id="825b6-161">Í flýtiflipanum **Keyra í bakgrunni** skal setja upp runu og áætlunarvalkosti eftir þörfum, rétt eins og yrði gert fyrir aðrar runuvinnslur í Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="825b6-161">On the **Run in the background** FastTab, set up batch and scheduling options as you require, just as you might do for other batch jobs in Supply Chain Management.</span></span>
1. <span data-ttu-id="825b6-162">Veljið **Í lagi** til að keyra og/eða tímasetja valdar viðhaldsáætlanir.</span><span class="sxs-lookup"><span data-stu-id="825b6-162">Select **OK** to run and/or schedule the selected maintenance plans.</span></span>
