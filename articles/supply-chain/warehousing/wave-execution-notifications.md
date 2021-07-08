---
title: Tilkynningar bylgjukerslu
description: Í þessu efnisatriði eru tilkynningar bylgjukeyrslu útskýrðar og því lýst hvernig á að setja þær upp.
author: mirzaab
ms.date: 04/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WhsWaveNotificationPolicy, WHSParameters, WHSWaveTemplateTable, BusinessEventsWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.0
ms.openlocfilehash: 47f270b5fff37e8e231d8a9c4a011172df3d9385
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271378"
---
# <a name="wave-execution-notifications"></a><span data-ttu-id="a59f3-103">Tilkynningar bylgjukerslu</span><span class="sxs-lookup"><span data-stu-id="a59f3-103">Wave execution notifications</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a59f3-104">Eiginleikinn *Tilkynningar bylgjukeyrslu* notar viðskiptatilvik og aðgerðamiðstöð til að senda tilkynningar sem tengjast bylgjukeyrslunni.</span><span class="sxs-lookup"><span data-stu-id="a59f3-104">The *Wave execution notifications* feature uses business events and the Action center to deliver notifications that are related to wave execution.</span></span> <span data-ttu-id="a59f3-105">Hann gerir kleift að tilgreina tilviksgerðir sem búa til tilkynningar, vöruhúsin sem mynda þær og notendurna sem taka á móti þeim.</span><span class="sxs-lookup"><span data-stu-id="a59f3-105">It lets you specify the types of events that generate notifications, the warehouses that generate them, and the users who receive them.</span></span>

<span data-ttu-id="a59f3-106">Hnappurinn **Sýna skilaboð** (bjöllutáknið) hægra megin á yfirlitsstikunn gefur til kynna hvenær skilaboð aðgerðamiðstöðvar verða tiltæk fyrir núverandi notanda.</span><span class="sxs-lookup"><span data-stu-id="a59f3-106">The **Show messages** button (bell symbol) on the right side of the navigation bar indicates when an Action center message is available for the current user.</span></span> <span data-ttu-id="a59f3-107">Notandinn getur valið hnappinn **Sýna skilaboð** til að opna aðgerðamiðstöðina og fara yfir skilaboðin.</span><span class="sxs-lookup"><span data-stu-id="a59f3-107">The user can select the **Show messages** button to open the Action center and review the messages.</span></span>

<span data-ttu-id="a59f3-108">Viðskiptatilvik eiga sér stað þegar viðskiptaferli eru keyrð.</span><span class="sxs-lookup"><span data-stu-id="a59f3-108">Business events occur when business processes are run.</span></span> <span data-ttu-id="a59f3-109">Viðskiptaferli samanstanda af verkum.</span><span class="sxs-lookup"><span data-stu-id="a59f3-109">Business processes are made up of tasks.</span></span> <span data-ttu-id="a59f3-110">Í viðskiptaferli framkvæma notendur sem taka þátt í því viðskiptaaðgerðir til að ljúka þessum verkum.</span><span class="sxs-lookup"><span data-stu-id="a59f3-110">During a business process, the users who participate in it perform business actions to complete those tasks.</span></span> <span data-ttu-id="a59f3-111">Viðskiptatilvik bjóða upp leið sem gerir ytri kerfum kleift að taka við tilkynningum frá Finance and Operations forritum.</span><span class="sxs-lookup"><span data-stu-id="a59f3-111">Business events provide a mechanism that lets external systems receive notifications from Finance and Operations applications.</span></span> <span data-ttu-id="a59f3-112">Þannig geta kerfin framkvæmt viðskiptaaðgerðir til að bregðast við viðskiptatilvikunum.</span><span class="sxs-lookup"><span data-stu-id="a59f3-112">In this way, the systems can perform business actions in response to the business events.</span></span> <span data-ttu-id="a59f3-113">Frekari upplýsingar eru í [Yfirlit viðskiptatilvika](../../fin-ops-core/dev-itpro/business-events/home-page.md).</span><span class="sxs-lookup"><span data-stu-id="a59f3-113">For more information, see [Business events overview](../../fin-ops-core/dev-itpro/business-events/home-page.md).</span></span>

## <a name="turn-on-the-wave-execution-notifications-feature"></a><span data-ttu-id="a59f3-114">Kveikja á eiginleika fyrir tilkynningar bylgjukeyrslu</span><span class="sxs-lookup"><span data-stu-id="a59f3-114">Turn on the Wave execution notifications feature</span></span>

<span data-ttu-id="a59f3-115">Áður en hægt er að nota eiginleikann *Tilkynningar bylgjukeyrslu* verður að vera kveikt á honum í kerfinu.</span><span class="sxs-lookup"><span data-stu-id="a59f3-115">Before you can use the *Wave execution notifications* feature, it must be turned on in your system.</span></span> <span data-ttu-id="a59f3-116">Stjórnendur geta notað vinnusvæði [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og kveikt á honum ef þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="a59f3-116">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="a59f3-117">Þar er eiginleikinn sýndur á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="a59f3-117">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="a59f3-118">**Eining:** *Vöruhúsakerfi*</span><span class="sxs-lookup"><span data-stu-id="a59f3-118">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="a59f3-119">**Heiti eiginleika:** *Tilkynningar bylgjukeyrslu*</span><span class="sxs-lookup"><span data-stu-id="a59f3-119">**Feature name:** *Wave execution notifications*</span></span>

## <a name="scenario-send-wave-batch-execution-notifications-to-the-action-center"></a><span data-ttu-id="a59f3-120">Atburðarás: Senda tilkynningar um framkvæmd bylgjurunu til aðgerðamiðstöðvar</span><span class="sxs-lookup"><span data-stu-id="a59f3-120">Scenario: Send wave batch execution notifications to the Action center</span></span>

<span data-ttu-id="a59f3-121">Þessi atburðarás sýnir heildarverkflæðið þegar tilkynningar eru sendar um villur vegna framkvæmdar bylgjurunu á tiltekið hlutverk í gegnum aðgerðamiðstöðina.</span><span class="sxs-lookup"><span data-stu-id="a59f3-121">This scenario shows the end-to-end flow for sending notifications about wave batch execution errors to a specific role via the Action center.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="a59f3-122">Bjóða upp á sýnigögn</span><span class="sxs-lookup"><span data-stu-id="a59f3-122">Make demo data available</span></span>

<span data-ttu-id="a59f3-123">Til að fylgja þessari atburðarás verður þú að hafa sýnigögn sett upp og þú verður að velja lögaðilann **USMF**.</span><span class="sxs-lookup"><span data-stu-id="a59f3-123">To follow this scenario, you must have demo data installed, and you must select the **USMF** legal entity.</span></span>

### <a name="make-sure-that-waves-are-run-in-batch-mode"></a><span data-ttu-id="a59f3-124">Gangið úr skugga um að bylgjurnar séu keyrðar í runustillingu</span><span class="sxs-lookup"><span data-stu-id="a59f3-124">Make sure that waves are run in batch mode</span></span>

1. <span data-ttu-id="a59f3-125">Farðu í **vöruhúsakerfi \> Uppsetning \> Færibreytur vöruhúsakerfis**.</span><span class="sxs-lookup"><span data-stu-id="a59f3-125">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>
1. <span data-ttu-id="a59f3-126">Í flýtiflipanum **Bylgjuvinnsla** skal stilla valkostinn **Vinna bylgjur í runu** á *Já*.</span><span class="sxs-lookup"><span data-stu-id="a59f3-126">On the **Wave processing** FastTab, set the **Process waves in batch** option to *Yes*.</span></span>

> [!NOTE]
> <span data-ttu-id="a59f3-127">Ef ætluni slökkva á tilkynningum vegna framkvæmdar bylgjuruna skal stilla valkostinn **Gera tilkynningar um runu bylgjuvinnslu óvirkar** á *Já*.</span><span class="sxs-lookup"><span data-stu-id="a59f3-127">If you want to disable wave batch execution notifications, set the **Disable wave processing batch notifications** option to *Yes*.</span></span>

### <a name="configure-a-wave-notification-policy"></a><span data-ttu-id="a59f3-128">Skilgreina reglu um tilkynningu bylgju</span><span class="sxs-lookup"><span data-stu-id="a59f3-128">Configure a wave notification policy</span></span>

<span data-ttu-id="a59f3-129">Reglur bylgjutilkynningar skilgreina þær gerðir af tilkynningum sem eru sendar og notendurna sem fá tilkynningar.</span><span class="sxs-lookup"><span data-stu-id="a59f3-129">Wave notification policies define the types of notifications that are sent and the users who are notified.</span></span>

1. <span data-ttu-id="a59f3-130">Farið í **Vöruhúsakerfi \> Uppsetning \> Bylgjur \> Reglur bylgjutilkynningar**.</span><span class="sxs-lookup"><span data-stu-id="a59f3-130">Go to **Warehouse management \> Setup \> Waves \> Wave notification policies**.</span></span>
1. <span data-ttu-id="a59f3-131">Búið til færslu sem er með eftirfarandi stillingum:</span><span class="sxs-lookup"><span data-stu-id="a59f3-131">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="a59f3-132">**Regla um tilkynningu bylgju:** *24BatchError*</span><span class="sxs-lookup"><span data-stu-id="a59f3-132">**Wave notification policy:** *24BatchError*</span></span>
    - <span data-ttu-id="a59f3-133">**Lýsing:** *Vöruhús 24 villa bylgjurunu*</span><span class="sxs-lookup"><span data-stu-id="a59f3-133">**Description:** *Warehouse 24 wave batch error*</span></span>
    - <span data-ttu-id="a59f3-134">**Senda tilkynningu þann:** *Aðeins villa*</span><span class="sxs-lookup"><span data-stu-id="a59f3-134">**Send notification on:** *Error only*</span></span>
    - <span data-ttu-id="a59f3-135">**Á hlutverk:** *Kerfisstjóri*</span><span class="sxs-lookup"><span data-stu-id="a59f3-135">**To role:** *System administrator*</span></span>

        > [!NOTE]
        > <span data-ttu-id="a59f3-136">Vegna þess að þessi atburðarás notar sýnigögn er hlutverkið *Kerfisstjóri* valið til einföldunar.</span><span class="sxs-lookup"><span data-stu-id="a59f3-136">Because this scenario uses demo data, the *System administrator* role is selected for the sake of simplicity.</span></span> <span data-ttu-id="a59f3-137">Þar af leiðandi, vegna þess að þú ert skráð(ur) inn sem kerfisstjóri, færðu sendar tilkynningar.</span><span class="sxs-lookup"><span data-stu-id="a59f3-137">Therefore, because you're signed in as a system administrator user, you will receive the notifications.</span></span> <span data-ttu-id="a59f3-138">Hins vegar ætti undir venjulegum kringumstæðum að yfirleitt velja sértækara hlutverk til að senda tilkynningu um villu vegna framkvæmdar bylgjurunu, t.d. *Vöruhúsastjórnandi*.</span><span class="sxs-lookup"><span data-stu-id="a59f3-138">However, in practice, you should usually select a more specific role to notify about wave batch execution errors, such as *Warehouse manager*.</span></span>

1. <span data-ttu-id="a59f3-139">Í aðgerðarúðunni skal velja **Vista**.</span><span class="sxs-lookup"><span data-stu-id="a59f3-139">On the Action Pane, select **Save**.</span></span>

### <a name="configure-a-wave-template"></a><span data-ttu-id="a59f3-140">Skilgreina bylgjusniðmát</span><span class="sxs-lookup"><span data-stu-id="a59f3-140">Configure a wave template</span></span>

<span data-ttu-id="a59f3-141">Bylgjusniðmát leyfa þér að tengja sérstök tilvik af bylgjuaðferðum við samsvarandi bylgjumerkissniðmát.</span><span class="sxs-lookup"><span data-stu-id="a59f3-141">Wave templates let you link specific instances of wave methods to corresponding wave label templates.</span></span>

1. <span data-ttu-id="a59f3-142">Farðu í **Vöruhúsakerfi \> Uppsetning \> Bylgjur \> Bylgjusniðmát**.</span><span class="sxs-lookup"><span data-stu-id="a59f3-142">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="a59f3-143">Á listasvæðinu skal stilla reitinn **Bylgjusniðmátsgerð** á *Sending* og síðan velja bylgjusniðmátið *Sjálfgefin sending 24* fyrir vöruhús 24.</span><span class="sxs-lookup"><span data-stu-id="a59f3-143">In the list pane, set the **Wave template type** field to *Shipping*, and then select the *24 Shipping Default* wave template for warehouse 24.</span></span>
1. <span data-ttu-id="a59f3-144">Í flýtiflipanum **Almennt** skal stilla reitinn **Regla um tilkynningu bylgju** á *24BatchError*.</span><span class="sxs-lookup"><span data-stu-id="a59f3-144">On the **General** FastTab, set the **Wave notification policy** field to *24BatchError*.</span></span>

### <a name="configure-a-work-template"></a><span data-ttu-id="a59f3-145">Stilla vinnusnið</span><span class="sxs-lookup"><span data-stu-id="a59f3-145">Configure a work template</span></span>

<span data-ttu-id="a59f3-146">Vinnusniðmát eru notuð í við framkvæmd bylgjukeyrslu til að búa til vinnu.</span><span class="sxs-lookup"><span data-stu-id="a59f3-146">Work templates are used during wave execution to generate work.</span></span> <span data-ttu-id="a59f3-147">Í þessari atburðarás ætti framkvæmd bylgju að leiða til villu.</span><span class="sxs-lookup"><span data-stu-id="a59f3-147">For this scenario, wave execution should trigger an error.</span></span> <span data-ttu-id="a59f3-148">Með því að stilla fyrirspurn vinnusniðmáts á að nota vöruhús sem er ekki til, er gengið úr skugga um að framkvæmd bylgju mistakist og að tilkynning verði send.</span><span class="sxs-lookup"><span data-stu-id="a59f3-148">By setting the work template query to use a nonexistent warehouse, you will ensure that wave execution fails and therefore sends a notification.</span></span>

1. <span data-ttu-id="a59f3-149">Farðu í **Vöruhúsakerfi \> Uppsetning \> Vinna \> Vinnusniðmát**.</span><span class="sxs-lookup"><span data-stu-id="a59f3-149">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="a59f3-150">Á listasvæðinu skal stilla reitinn **Vinnusniðmátsgerð** á *Sölupantanir* og síðan velja vinnusniðmátið *24 stig sölupöntunar* fyrir vöruhús 24.</span><span class="sxs-lookup"><span data-stu-id="a59f3-150">In the list pane, set the **Work template type** field to *Sales orders* and then select the *24 SO Stage* work template for warehouse 24.</span></span>
1. <span data-ttu-id="a59f3-151">Á aðgerðasvæðinu skal velja **Breyta fyrirspurn**.</span><span class="sxs-lookup"><span data-stu-id="a59f3-151">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="a59f3-152">Í svarglugga fyrirspurnarritils, í flipanum **Svið**, skal breyta eftirfarandi línu (eða bæta henni við ef hún er ekki til):</span><span class="sxs-lookup"><span data-stu-id="a59f3-152">In the query editor dialog box, on the **Range** tab, edit the following row (or add it if it doesn't exist):</span></span>

    - <span data-ttu-id="a59f3-153">**Tafla:** *Tímabundnar vinnufærslur*</span><span class="sxs-lookup"><span data-stu-id="a59f3-153">**Table:** *Temporary work transactions*</span></span>
    - <span data-ttu-id="a59f3-154">**Afleidd tafla:** *Tímabundnar vinnufærslur*</span><span class="sxs-lookup"><span data-stu-id="a59f3-154">**Derived table:** *Temporary work transactions*</span></span>
    - <span data-ttu-id="a59f3-155">**Svæði:** *Vöruhús*</span><span class="sxs-lookup"><span data-stu-id="a59f3-155">**Field:** *Warehouse*</span></span>
    - <span data-ttu-id="a59f3-156">**Skilyrði:** Breytið gildinu úr *24* í *Villa*.</span><span class="sxs-lookup"><span data-stu-id="a59f3-156">**Criteria:** Change the value from *24* to *Error*.</span></span>

1. <span data-ttu-id="a59f3-157">Veldu **Í lagi** og staðfestu breytinguna.</span><span class="sxs-lookup"><span data-stu-id="a59f3-157">Select **OK**, and confirm the change.</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="a59f3-158">Stofna sölupöntun og losa hana í vöruhúsið.</span><span class="sxs-lookup"><span data-stu-id="a59f3-158">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="a59f3-159">Opnið **Sala og markaðssetning \> Sölupöntun \> Allar sölupantanir**.</span><span class="sxs-lookup"><span data-stu-id="a59f3-159">Go to **Sales and marketing \> Sales order \> All sales orders**.</span></span>
1. <span data-ttu-id="a59f3-160">Stofna sölupöntun sem er með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="a59f3-160">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="a59f3-161">**Viðskiptavinalykill:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="a59f3-161">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="a59f3-162">**Vöruhús:** *24*</span><span class="sxs-lookup"><span data-stu-id="a59f3-162">**Warehouse:** *24*</span></span>

1. <span data-ttu-id="a59f3-163">Í flýtiflipanum **Sölupöntunarlínur** skal bæta við sölupöntunarlínu sem er með eftirfarandi stillingum:</span><span class="sxs-lookup"><span data-stu-id="a59f3-163">On the **Sales order lines** FastTab, add a sales order line that has the following settings:</span></span>

    - <span data-ttu-id="a59f3-164">**Vörunúmer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="a59f3-164">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="a59f3-165">**Magn:** *10*</span><span class="sxs-lookup"><span data-stu-id="a59f3-165">**Quantity:** *10*</span></span>

    > [!NOTE]
    > <span data-ttu-id="a59f3-166">Þessi atriði og magn eru aðeins dæmi.</span><span class="sxs-lookup"><span data-stu-id="a59f3-166">These items and quantities are only examples.</span></span> <span data-ttu-id="a59f3-167">Tilgreint vöruhús verður að innihalda nóg af birgðum.</span><span class="sxs-lookup"><span data-stu-id="a59f3-167">The specified warehouse must contain enough stock.</span></span>

1. <span data-ttu-id="a59f3-168">Á meðan nýja línan er enn valin í flýtiflipanum **Sölupöntunarlínur** skal velja **Birgðir \> Frátekning** á tækjastikunni.</span><span class="sxs-lookup"><span data-stu-id="a59f3-168">While the new line is still selected on the **Sales order lines** FastTab, select **Inventory \> Reservation** on the toolbar.</span></span>
1. <span data-ttu-id="a59f3-169">Á síðunni **Frátekning**, á aðgerðasvæðinu, skal velja **Frátektarlota**.</span><span class="sxs-lookup"><span data-stu-id="a59f3-169">On the **Reservation** page, on the Action Pane, select **Reserve lot**.</span></span> <span data-ttu-id="a59f3-170">Því næst skal loka síðunni.</span><span class="sxs-lookup"><span data-stu-id="a59f3-170">Then close the page.</span></span>
1. <span data-ttu-id="a59f3-171">Á aðgerðasvæðinu, í flipanum **Vöruhús**, skal velja **Losa í vöruhús**.</span><span class="sxs-lookup"><span data-stu-id="a59f3-171">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

### <a name="notifications-from-wave-batch-job-execution"></a><span data-ttu-id="a59f3-172">Tilkynningar frá framkvæmd runuvinnslu bylgju</span><span class="sxs-lookup"><span data-stu-id="a59f3-172">Notifications from wave batch job execution</span></span>

<span data-ttu-id="a59f3-173">Það fer eftir uppsetningu viðskiptatilvikanna, en að lokum kemur tilkynning um að framkvæmd bylgju hafi mistekist.</span><span class="sxs-lookup"><span data-stu-id="a59f3-173">Depending on the setup of your business events, you will eventually receive a notification about wave execution failure.</span></span> <span data-ttu-id="a59f3-174">Skilaboð aðgerðamiðstöðvarinnar munu líkjast eftirfarandi dæmi og innihalda tengil á bylgjuna sem mistókst.</span><span class="sxs-lookup"><span data-stu-id="a59f3-174">The Action center message will resemble the following example and will include a link to the wave that failed.</span></span>

> <span data-ttu-id="a59f3-175">**Villa við keyrslu bylgju**</span><span class="sxs-lookup"><span data-stu-id="a59f3-175">**Error during wave execution**</span></span>  
> <span data-ttu-id="a59f3-176">Villa kom upp þegar bylgja var keyrð USMF-000000001.</span><span class="sxs-lookup"><span data-stu-id="a59f3-176">An error occurred while executing wave USMF-000000001.</span></span>  
> <span data-ttu-id="a59f3-177">Síðustu skilaboð: Engin vinna var stofnuð fyrir bylgju USMF-000000001.</span><span class="sxs-lookup"><span data-stu-id="a59f3-177">Last messages: No Work was created for Wave USMF-000000001.</span></span>
>
> <span data-ttu-id="a59f3-178">**STAÐA**</span><span class="sxs-lookup"><span data-stu-id="a59f3-178">**STATUS**</span></span>  
> <span data-ttu-id="a59f3-179">Í gangi</span><span class="sxs-lookup"><span data-stu-id="a59f3-179">Active</span></span>
>
> <span data-ttu-id="a59f3-180">Upplýsingar um opna bylgju</span><span class="sxs-lookup"><span data-stu-id="a59f3-180">Open wave details</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
