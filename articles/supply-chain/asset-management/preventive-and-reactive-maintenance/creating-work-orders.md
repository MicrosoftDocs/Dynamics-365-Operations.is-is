---
title: Verkbeiðnir stofnaðar
description: Þetta efni útskýrir hvernig á að stofna verkbeiðnir í eignastýringu.
author: johanhoffmann
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetMaintenancePlan, EntAssetObjectCalendarListPage, EntAssetObjectCalendarListPagePoolsOpen
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 3982232e5008d6f8c283d6cecfaf2fa6e66150a1
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5836735"
---
# <a name="creating-work-orders"></a><span data-ttu-id="2c0fe-103">Verkbeiðnir stofnaðar</span><span class="sxs-lookup"><span data-stu-id="2c0fe-103">Creating work orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2c0fe-104">Þegar fyrirbyggjandi viðhaldsverk hafa verið tímasett er næsta skref að stofna verkbeiðnir fyrir þau.</span><span class="sxs-lookup"><span data-stu-id="2c0fe-104">After you've scheduled preventive maintenance jobs, the next step is to create work orders for them.</span></span> <span data-ttu-id="2c0fe-105">Hægt er að ljúka þessu skrefi með því að nota eina af viðhaldsáætlunum.</span><span class="sxs-lookup"><span data-stu-id="2c0fe-105">You can complete this step by using one of the maintenance schedules.</span></span> <span data-ttu-id="2c0fe-106">Áætlaðar vinnslur í viðhaldsáætlun geta haft mismunandi tilvísunargerðir eins og lýst er í eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="2c0fe-106">The scheduled jobs in a maintenance schedule can have different reference types, as described in the following table.</span></span>

| <span data-ttu-id="2c0fe-107">Gerð tilvísunar</span><span class="sxs-lookup"><span data-stu-id="2c0fe-107">Reference type</span></span> | <span data-ttu-id="2c0fe-108">lýsing</span><span class="sxs-lookup"><span data-stu-id="2c0fe-108">Description</span></span> |
|---|---|
| <span data-ttu-id="2c0fe-109">Viðhaldsáætlanir</span><span class="sxs-lookup"><span data-stu-id="2c0fe-109">Maintenance plans</span></span> | <span data-ttu-id="2c0fe-110">Fyrirbyggjandi viðhaldsverk sem byggja á viðhaldsáætlunargerðinni *Tími* eða *Teljari*.</span><span class="sxs-lookup"><span data-stu-id="2c0fe-110">Preventive maintenance jobs that are based on the *Time* or *Counter* maintenance plan type.</span></span> |
| <span data-ttu-id="2c0fe-111">Viðhaldslotur</span><span class="sxs-lookup"><span data-stu-id="2c0fe-111">Maintenance rounds</span></span> | <span data-ttu-id="2c0fe-112">Fyrirbyggjand viðhaldsverk sem innihalda nokkrar eignir sem þurfa sams konar viðhald.</span><span class="sxs-lookup"><span data-stu-id="2c0fe-112">Preventive maintenance jobs that contain several assets that require a similar type of maintenance.</span></span> |
| <span data-ttu-id="2c0fe-113">Viðhaldsbeiðni</span><span class="sxs-lookup"><span data-stu-id="2c0fe-113">Maintenance request</span></span> | <span data-ttu-id="2c0fe-114">Handvirk stofnun beiðni um viðhald eða viðgerð á eign.</span><span class="sxs-lookup"><span data-stu-id="2c0fe-114">A manually created request for maintenance or repair of an asset.</span></span> <span data-ttu-id="2c0fe-115">Hægt er að umreikna þessa beiðni í verkbeiðni.</span><span class="sxs-lookup"><span data-stu-id="2c0fe-115">This request can be converted to a work order.</span></span> |

## <a name="create-work-orders-based-on-your-maintenance-schedule"></a><span data-ttu-id="2c0fe-116">Stofna verkbeiðnir út frá viðhaldsáætluninni</span><span class="sxs-lookup"><span data-stu-id="2c0fe-116">Create work orders based on your maintenance schedule</span></span>

<span data-ttu-id="2c0fe-117">Til að stofna verkbeiðnir sem byggja á viðhaldsáætluninni skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="2c0fe-117">To create work orders that are based on your maintenance schedule, follow these steps.</span></span>

1. <span data-ttu-id="2c0fe-118">Opnið eina af eftirfarandi síðum, allt eftir því hvernig velja á áætlunarvörur fyrir verkbeiðnir:</span><span class="sxs-lookup"><span data-stu-id="2c0fe-118">Open one of the following pages, depending on how you want to select schedule items for your work orders:</span></span>

    - <span data-ttu-id="2c0fe-119">Öll viðhaldsáætlun (**Eignastýring \> Áætlun stjórnunar \> Öll viðhaldsáætlun**)</span><span class="sxs-lookup"><span data-stu-id="2c0fe-119">All maintenance schedule (**Asset management \> Management schedule \> All maintenance schedule**)</span></span>
    - <span data-ttu-id="2c0fe-120">Opna viðhaldsáætlunarlínur (**Eignastýring \> Áætlun stjórnunar \> Opna áætlunarlínur viðhalds**)</span><span class="sxs-lookup"><span data-stu-id="2c0fe-120">Open maintenance schedule lines (**Asset management \> Management schedule \> Open maintenance schedule lines**)</span></span>
    - <span data-ttu-id="2c0fe-121">Opna viðhaldsáætlunarhópa (**Eignastýring \> Áætlun stjórnunar \> Opna áætlunarhópa viðhalds**)</span><span class="sxs-lookup"><span data-stu-id="2c0fe-121">Open maintenance schedule pools (**Asset management \> Management schedule \> Open maintenance schedule pools**)</span></span>

1. <span data-ttu-id="2c0fe-122">Í hnitanetinu skal velja gátreitinn fyrir hvert verk viðhaldsáætlunar sem á að stofna verkbeiðni fyrir.</span><span class="sxs-lookup"><span data-stu-id="2c0fe-122">In the grid, select the check box for every scheduled maintenance job that you want to create a work order for.</span></span> <span data-ttu-id="2c0fe-123">Á aðgerðasvæðinu skal síðan velja **Verkbeiðni**.</span><span class="sxs-lookup"><span data-stu-id="2c0fe-123">Then, on the Action Pane, select **Work order**.</span></span>

    <span data-ttu-id="2c0fe-124">Gátreiturinn **Stofna verkbeiðnir** birtist.</span><span class="sxs-lookup"><span data-stu-id="2c0fe-124">The **Create work orders** dialog box appears.</span></span> <span data-ttu-id="2c0fe-125">Reiturinn **Vinnustundir viðhaldsspár** sýnir heildarfjölda vinnustunda fyrir spá fyrir valdar línur.</span><span class="sxs-lookup"><span data-stu-id="2c0fe-125">The **Maintenance forecast hours** field shows the total number of forecast hours for the selected lines.</span></span>

    ![Búa til svarglugga verkbeiðna](media/18-preventive-maintenance.png)

1. <span data-ttu-id="2c0fe-127">Í hlutanum **Færibreytur** skal tilgreina þann fjölda verkbeiðna sem á að stofna.</span><span class="sxs-lookup"><span data-stu-id="2c0fe-127">In the **Parameters** section, specify the number of work orders that should be created.</span></span> <span data-ttu-id="2c0fe-128">Veldu einn af eftirfarandi valkostum:</span><span class="sxs-lookup"><span data-stu-id="2c0fe-128">Select one of the following options:</span></span>

    - <span data-ttu-id="2c0fe-129">**Ein verkbeiðni á línu** – Stofnið eina verkbeiðni á hverja viðhaldsáætlunarlínu.</span><span class="sxs-lookup"><span data-stu-id="2c0fe-129">**One work order per line** – Create one work order per maintenance schedule line.</span></span>
    - <span data-ttu-id="2c0fe-130">**Ein verkbeiðni á** – Stofnið verkbeiðnir sem eru flokkaðar samkvæmt stillingum hinna valkostanna sem verða tiltækir þegar þessi valkostur er valinn.</span><span class="sxs-lookup"><span data-stu-id="2c0fe-130">**One work order per** – Create work orders that are grouped according to the settings of the other options that become available when you select this option.</span></span>

1. <span data-ttu-id="2c0fe-131">Í reitnum **Gerð verkbeiðni** skal velja verkbeiðnigerðina sem á að nota fyrir allar verkbeiðnir sem eru stofnaðar.</span><span class="sxs-lookup"><span data-stu-id="2c0fe-131">In the **Work order type** field, select the work order type to use for all the work orders that you create.</span></span>
1. <span data-ttu-id="2c0fe-132">Veljið **Í lagi** til að stofna verkbeiðnir samkvæmt stillingunum.</span><span class="sxs-lookup"><span data-stu-id="2c0fe-132">Select **OK** to create the work orders according to your settings.</span></span>

## <a name="group-work-order-lines-that-are-automatically-created-while-a-maintenance-plan-runs"></a><span data-ttu-id="2c0fe-133">Flokka verkbeiðnilínur sem eru sjálfkrafa stofnaðar meðan á viðhaldsáætlun stendur</span><span class="sxs-lookup"><span data-stu-id="2c0fe-133">Group work order lines that are automatically created while a maintenance plan runs</span></span>

<span data-ttu-id="2c0fe-134">Þessi eiginleiki gerir kleift að skilgreina reglur fyrir flokkun verkbeiðnilína undir einni verkbeiðni þegar kerfið er stillt á að búa sjálfkrafa til verkbeiðnir sem byggja á viðhaldsáætlun.</span><span class="sxs-lookup"><span data-stu-id="2c0fe-134">This feature lets you define rules for grouping work order lines under a single work order when the system is set up to generate work orders automatically, based on a maintenance plan.</span></span> <span data-ttu-id="2c0fe-135">Áður gátu sjálfkrafa myndaðar verkbeiðnir aðeins innihaldið eina línu.</span><span class="sxs-lookup"><span data-stu-id="2c0fe-135">Previously, automatically generated work orders could contain only one line.</span></span> <span data-ttu-id="2c0fe-136">Nú er hins vegar hægt að flokka verkbeiðnir eftir til dæmis eign, eignagerð eða virkri staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="2c0fe-136">However, you can now group work orders by, for example, asset, asset type, or functional location.</span></span> <span data-ttu-id="2c0fe-137">(Handvirkt myndaðar verkbeiðnir var aðeins hægt að flokka á þennan hátt eins og lýst er í hlutanum hér á undan í þessu efnisatriði.)</span><span class="sxs-lookup"><span data-stu-id="2c0fe-137">(Manually generated work orders could already be grouped in this way, as described in the previous section of this topic.)</span></span>

### <a name="enable-grouping-for-automatically-generated-work-orders"></a><span data-ttu-id="2c0fe-138">Virkja flokkun fyrir sjálfkrafa myndaðar verkbeiðnir</span><span class="sxs-lookup"><span data-stu-id="2c0fe-138">Enable grouping for automatically generated work orders</span></span>

<span data-ttu-id="2c0fe-139">Áður en hægt er að nota þennan eiginleika þarf að kveikja á honum í kerfinu.</span><span class="sxs-lookup"><span data-stu-id="2c0fe-139">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="2c0fe-140">Stjórnendur geta notað stillingarnar [eiginleikastjórnun](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og kveikja á honum.</span><span class="sxs-lookup"><span data-stu-id="2c0fe-140">Admins can use the [feature management](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="2c0fe-141">Á vinnusvæðinu **Eiginleikastjórnun** er eiginleikinn tilgreindur á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="2c0fe-141">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="2c0fe-142">**Eining:** *Eignastjórnun*</span><span class="sxs-lookup"><span data-stu-id="2c0fe-142">**Module:** *Asset Management*</span></span>
- <span data-ttu-id="2c0fe-143">**Heiti eiginleika:** *Notið reglur fyrir flokkun verkbeiðna á meðan viðhaldsáætlun er keyrð*</span><span class="sxs-lookup"><span data-stu-id="2c0fe-143">**Feature name:** *Apply rules for grouping work orders while running a maintenance plan*</span></span>

### <a name="set-up-grouping-for-automatically-generated-work-orders"></a><span data-ttu-id="2c0fe-144">Setja upp flokkun fyrir sjálfkrafa myndaðar verkbeiðnir</span><span class="sxs-lookup"><span data-stu-id="2c0fe-144">Set up grouping for automatically generated work orders</span></span>

<span data-ttu-id="2c0fe-145">Til að setja upp flokkun fyrir sjálfkrafa myndaðar verkbeiðnir skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="2c0fe-145">To set up grouping for automatically generated work orders, follow these steps.</span></span>

1. <span data-ttu-id="2c0fe-146">Farið í **Eignastýring \> Uppsetning \> Fyrirbyggjandi viðhald \> Viðhaldsáætlanir**.</span><span class="sxs-lookup"><span data-stu-id="2c0fe-146">Go to **Asset management \> Setup \> Preventative maintenance \> Maintenance plans**.</span></span>
1. <span data-ttu-id="2c0fe-147">Fyrir hverja áætlun þar sem á að mynda flokkaðar verkbeiðnir skal fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="2c0fe-147">For each plan where you want to generate grouped work orders, follow these steps:</span></span>

    1. <span data-ttu-id="2c0fe-148">Velja skal áætlunina á listasvæðinu.</span><span class="sxs-lookup"><span data-stu-id="2c0fe-148">Select the plan in the list pane.</span></span>
    1. <span data-ttu-id="2c0fe-149">Í flýtiflipanum **Línur** skal ganga úr skugga um að gátreiturinn **Stofna sjálfvirkt** sé valinn í hverri línu.</span><span class="sxs-lookup"><span data-stu-id="2c0fe-149">On the **Lines** FastTab, make sure that the **Auto create** check box is selected on every line.</span></span>

1. <span data-ttu-id="2c0fe-150">Farið í **Eignastýring \> Reglubundið \> Fyrirbyggjandi viðhald \> Tímasetja viðhaldsáætlanir**.</span><span class="sxs-lookup"><span data-stu-id="2c0fe-150">Go to **Asset management \> Periodic \> Preventive maintenance \> Schedule maintenance plans**.</span></span>
1. <span data-ttu-id="2c0fe-151">Í svarglugganum **Tímasetja viðhaldsáætlanir**, í hlutanum **Tímabil**, skal tilgreina hámarkstíma fyrir áætlunina (hversu langt fram í tímann er horft þegar fundin eru verk viðhaldsáætlunar til að mynda vinnu fyrir).</span><span class="sxs-lookup"><span data-stu-id="2c0fe-151">In the **Schedule maintenance plans** dialog box, in the **Period** section, specify the time horizon for the plan (how far to look ahead when finding scheduled maintenance jobs to generate work for).</span></span>
1. <span data-ttu-id="2c0fe-152">Stillið valkostinn **Stofna verkbeiðni sjálfkrafa úr áætlun** á *Já*.</span><span class="sxs-lookup"><span data-stu-id="2c0fe-152">Set the **Automatically create work order from schedule** option to *Yes*.</span></span>
1. <span data-ttu-id="2c0fe-153">Veldu einn af eftirfarandi valkostum í hlutanum **Verkbeiðni**:</span><span class="sxs-lookup"><span data-stu-id="2c0fe-153">In the **Work order** section, select one of the following options:</span></span>

    - <span data-ttu-id="2c0fe-154">**Ein verkbeiðni á línu** – Stofnið eina verkbeiðni á hverja viðhaldsáætlunarlínu.</span><span class="sxs-lookup"><span data-stu-id="2c0fe-154">**One work order per line** – Create one work order per maintenance schedule line.</span></span> <span data-ttu-id="2c0fe-155">(Þessi valkostur veitir sömu virkni og er tiltæk þegar slökkt er á eiginleikanum *Nota reglur fyrir flokkun verkbeiðna á meðan viðhaldsáætlun er keyrð*.)</span><span class="sxs-lookup"><span data-stu-id="2c0fe-155">(This option provides the same functionality that is available when the *Apply rules for grouping work orders while running a maintenance plan* feature is turned off.)</span></span>
    - <span data-ttu-id="2c0fe-156">**Ein verkbeiðni á** – Stofnið verkbeiðnir sem eru flokkaðar samkvæmt stillingum hinna valkostanna sem verða tiltækir þegar þessi valkostur er valinn.</span><span class="sxs-lookup"><span data-stu-id="2c0fe-156">**One work order per** – Create work orders that are grouped according to the settings of the other options that become available when you select this option.</span></span>

1. <span data-ttu-id="2c0fe-157">Ef ætlunin er að valkostirnir séu notaðir þegar aðeins sumar viðhaldsáætlanir eru keyrðar skal í flýtiflipanum **Færslur til að taka með** sía eftir þörfum, rétt eins og yrði gert fyrir aðrar runuvinnslur í Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="2c0fe-157">If you want the options to apply when you run only some of your maintenance plans, on the **Records to include** FastTab, add filters as you require, just as you might do for other batch jobs in Microsoft Dynamics 365 Supply Chain Management.</span></span>
1. <span data-ttu-id="2c0fe-158">Í flýtiflipanum **Keyra í bakgrunni** skal setja upp runu og áætlunarvalkosti eftir þörfum, rétt eins og yrði gert fyrir aðrar runuvinnslur í Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="2c0fe-158">On the **Run in the background** FastTab, set up batch and scheduling options as you require, just as you might do for other batch jobs in Supply Chain Management.</span></span>
1. <span data-ttu-id="2c0fe-159">Veljið **Í lagi** til að keyra og/eða tímasetja valdar viðhaldsáætlanir.</span><span class="sxs-lookup"><span data-stu-id="2c0fe-159">Select **OK** to run and/or schedule the selected maintenance plans.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]