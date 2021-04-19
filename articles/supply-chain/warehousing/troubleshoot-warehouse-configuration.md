---
title: Úrræðaleit fyrir grunnstillingu vöruhúss
description: Þetta efnisatriði lýsir því hvernig á að laga almenn vandamál sem kunna að koma upp við stillingu Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 1dbd947f0740d22e0f79e6d5c272beb64715c8a5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5814393"
---
# <a name="troubleshoot-warehouse-configuration"></a><span data-ttu-id="809a9-103">Úrræðaleit fyrir grunnstillingu vöruhúss</span><span class="sxs-lookup"><span data-stu-id="809a9-103">Troubleshoot warehouse configuration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="809a9-104">Þetta efnisatriði lýsir því hvernig á að laga almenn vandamál sem kunna að koma upp við stillingu Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="809a9-104">This topic describes how to fix common issues that you might encounter while you configure Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-the-license-plate-or-location-is-not-valid"></a><span data-ttu-id="809a9-105">Ég fæ eftirfarandi villuboð: „Númeraplatan eða staðsetningin er ekki gild“.</span><span class="sxs-lookup"><span data-stu-id="809a9-105">I receive the following error message: "The license plate or location is not valid."</span></span>

### <a name="issue-description"></a><span data-ttu-id="809a9-106">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="809a9-106">Issue description</span></span>

<span data-ttu-id="809a9-107">Þessi villuboð birtast þegar kenni númeraplötu eða staðsetning er skönnuð.</span><span class="sxs-lookup"><span data-stu-id="809a9-107">You receive this error message when you scan a license plate ID or location.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="809a9-108">Úrlausn úrlausnaratriðis</span><span class="sxs-lookup"><span data-stu-id="809a9-108">Issue resolution</span></span>

<span data-ttu-id="809a9-109">Gangið úr skugga um að kenni númeraplötunnar sé ekki tekið frá eitthvað annað.</span><span class="sxs-lookup"><span data-stu-id="809a9-109">Make sure that the license plate ID isn't reserved by something else.</span></span> <span data-ttu-id="809a9-110">Þetta vandamál kom upp þegar gildið sem notandi skannaði í farsímaforriti vöruhúsakerfis var bæði gild staðsetning og gilt númerakenni.</span><span class="sxs-lookup"><span data-stu-id="809a9-110">This issue used to occur when the value that a user scanned in the Warehouse Management mobile app was both a valid location and a valid license plate ID.</span></span> <span data-ttu-id="809a9-111">Hins vegar var þetta vandamál leyst í útgáfu 10.0.11.</span><span class="sxs-lookup"><span data-stu-id="809a9-111">However, this issue was resolved in version 10.0.11.</span></span>

## <a name="i-receive-the-following-error-message-license-plate-must-be-specified-for-this-location"></a><span data-ttu-id="809a9-112">Ég fæ eftirfarandi villuboð: „Tilgreina þarf númeraplötu fyrir þessa staðsetningu“.</span><span class="sxs-lookup"><span data-stu-id="809a9-112">I receive the following error message: "License plate must be specified for this location."</span></span>

### <a name="issue-description"></a><span data-ttu-id="809a9-113">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="809a9-113">Issue description</span></span>

<span data-ttu-id="809a9-114">Þessi villuboð verða send ef flutningspöntun er stofnuð með því að nota vöruhús sem er virkt fyrir ítarlega vöruhúsastjórnun (WMS), og svo er reynt að staðfesta sendinguna eftir að vinnu er lokið.</span><span class="sxs-lookup"><span data-stu-id="809a9-114">You receive this error message if you create a transfer order by using a warehouse that is enabled for advanced warehouse management (WMS), and then, after the work is completed, you try to confirm the shipment.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="809a9-115">Úrlausn úrlausnaratriðis</span><span class="sxs-lookup"><span data-stu-id="809a9-115">Issue resolution</span></span>

<span data-ttu-id="809a9-116">Reiturinn **Sjálfgefin staðsetning innhreyfinga** er auður fyrir flutningsvöruhús „úr“ vöruhúsi.</span><span class="sxs-lookup"><span data-stu-id="809a9-116">The **Default receipt location** field is blank for a transit warehouse of the "from" warehouse.</span></span> <span data-ttu-id="809a9-117">Til að laga þetta vandamál þarf að tilgreina sjálfgefna staðsetningu móttöku í flutningsvöruhúsinu.</span><span class="sxs-lookup"><span data-stu-id="809a9-117">To fix this issue, specify a default receipt location in the transit warehouse.</span></span> <span data-ttu-id="809a9-118">Ganga skal úr skugga um að þessi staðsetning sé númeraplata – stjórnað.</span><span class="sxs-lookup"><span data-stu-id="809a9-118">Make sure that this location is license plate–controlled.</span></span>

## <a name="i-receive-the-following-error-message-you-cant-create-a-work-template-line-for-inventory-status-change-because-the-work-type-is-not-valid-select-a-different-work-type"></a><span data-ttu-id="809a9-119">Ég fæ eftirfarandi villuboð: Ekki er hægt að stofna vinnusniðmátslínu fyrir Breyting á birgðastöðu því að vinnutegundin er ógild.</span><span class="sxs-lookup"><span data-stu-id="809a9-119">I receive the following error message: "You can't create a work template line for Inventory status change because the work type is not valid.</span></span> <span data-ttu-id="809a9-120">Velja skal aðra vinnutegund.</span><span class="sxs-lookup"><span data-stu-id="809a9-120">Select a different work type."</span></span>

### <a name="issue-description"></a><span data-ttu-id="809a9-121">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="809a9-121">Issue description</span></span>

<span data-ttu-id="809a9-122">Fyrir vinnusniðmát er ekki hægt að velja *Breyting á birgðastöðu* í dálknum **Vinnusniðmát** í hlutanum **Upplýsingar um vinnusniðmát**.</span><span class="sxs-lookup"><span data-stu-id="809a9-122">For a work template, you can't select *Inventory status change* in the **Work type** column of the **Work template details** section.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="809a9-123">Úrlausn úrlausnaratriðis</span><span class="sxs-lookup"><span data-stu-id="809a9-123">Issue resolution</span></span>

<span data-ttu-id="809a9-124">Þessi hegðun er samkvæmt hönnuninni.</span><span class="sxs-lookup"><span data-stu-id="809a9-124">This behavior is by design.</span></span> <span data-ttu-id="809a9-125">Vinnutegundin *Breyting á birgðastöðu* er aðeins notuð af kerfisvinnslu.</span><span class="sxs-lookup"><span data-stu-id="809a9-125">The *Inventory status change* work type is used only by system processes.</span></span> <span data-ttu-id="809a9-126">Ekki er hægt að stilla þetta.</span><span class="sxs-lookup"><span data-stu-id="809a9-126">It can't be configured.</span></span> <span data-ttu-id="809a9-127">Vegna þess að listi yfir vinnugerðir er fastur sem tölusetning er ekki hægt að sía aukafærslur úr fellivalmyndinni **Vinnutegund**.</span><span class="sxs-lookup"><span data-stu-id="809a9-127">Because the list of work types is fixed as an enumeration, the extra entries can't be filtered out of the **Work type** drop-down menu.</span></span>

## <a name="i-receive-the-following-error-message-the-quantity-is-not-valid-for-unit-1"></a><span data-ttu-id="809a9-128">Ég fæ eftirfarandi villuskilaboð: „Magnið er ekki gilt fyrir einingu „Magnið er ekki gilt fyrir einingu 1%“.</span><span class="sxs-lookup"><span data-stu-id="809a9-128">I receive the following error message: "The Quantity is not valid for unit 1%."</span></span>

### <a name="issue-description"></a><span data-ttu-id="809a9-129">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="809a9-129">Issue description</span></span>

<span data-ttu-id="809a9-130">Magnið er ekki gilt fyrir *ea* eininguna þegar um er að ræða tiltektarvinnu sem er með margar númeraplötur á einni staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="809a9-130">The quantity isn't valid for the *ea* unit when there is picking work that has multiple license plates in one location.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="809a9-131">Úrlausn úrlausnaratriðis</span><span class="sxs-lookup"><span data-stu-id="809a9-131">Issue resolution</span></span>

<span data-ttu-id="809a9-132">Gangið úr skugga um að **Auðkenni röðunarflokks einingar** og **Einingaumreikningar** reitir á útgefnu afurðina eða afurðarafbrigðið séu rétt stillt.</span><span class="sxs-lookup"><span data-stu-id="809a9-132">Verify that the **Unit sequence group ID** and **Unit conversions** fields on the released product or product variant are set correctly.</span></span>

<span data-ttu-id="809a9-133">Athugið að villuboðin hafa verið endurbætt í útgáfu 10.0.15 (sjá [KB 4581627](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486531)).</span><span class="sxs-lookup"><span data-stu-id="809a9-133">Note that the error message has been improved in version 10.0.15 (see [KB 4581627](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486531)).</span></span> <span data-ttu-id="809a9-134">Nýju villuboðin eru, Magnið er ekki gilt.</span><span class="sxs-lookup"><span data-stu-id="809a9-134">The new error message is, "The quantity is not valid.</span></span> <span data-ttu-id="809a9-135">Væntanlegt %1 %2."</span><span class="sxs-lookup"><span data-stu-id="809a9-135">Expected %1 %2."</span></span>

## <a name="in-location-directives-for-sales-order-put-work-the-multiple-sku-option-doesnt-evaluate-multiple-location-directive-actions"></a><span data-ttu-id="809a9-136">Í staðsetningarleiðbeiningum fyrir frágang sölupöntunar metur valkostur birgðahaldseiningar ekki margar aðgerðir staðsetningarleiðbeininga.</span><span class="sxs-lookup"><span data-stu-id="809a9-136">In location directives for sales order put work, the multiple SKU option doesn't evaluate multiple location directive actions.</span></span>

### <a name="issue-description"></a><span data-ttu-id="809a9-137">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="809a9-137">Issue description</span></span>

<span data-ttu-id="809a9-138">Staðsetningarleiðbeiningar af vinnutegundinni *Sölupantanir* og *Frágangur* ekki meta margar aðgerðir staðsetningarleiðbeininga þegar valkosturinn **Margar birgðahaldseiningar** er valinn.</span><span class="sxs-lookup"><span data-stu-id="809a9-138">Location directives of the *Sales orders* work order type and the *Put* work type don't evaluate multiple location directive actions when the **Multiple SKU** option is selected.</span></span> <span data-ttu-id="809a9-139">Aðeins fyrsta aðgerð fyrir staðsetningarleiðbeiningar er metin.</span><span class="sxs-lookup"><span data-stu-id="809a9-139">Only the first location directive action is evaluated.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="809a9-140">Úrlausn úrlausnaratriðis</span><span class="sxs-lookup"><span data-stu-id="809a9-140">Issue resolution</span></span>

<span data-ttu-id="809a9-141">Nýr eiginleiki, *Meta allar aðgerðir fyrir staðsetningarleiðbeiningar margra birgðahaldseininga*, hefur verið bætt við útgáfu 10.0.15 (sjá [KB 4579866](https://fix.lcs.dynamics.com/Issue/Details?kb=4579866&bugId=475946&dbType=3&qc=1bc41a56de7a3ee419fa76397a6bf282fce5be9b93e427c08a6d916d1dfa3091)).</span><span class="sxs-lookup"><span data-stu-id="809a9-141">A new feature, *Evaluate all actions for Multi SKU location directives*, has been added in version 10.0.15 (see [KB 4579866](https://fix.lcs.dynamics.com/Issue/Details?kb=4579866&bugId=475946&dbType=3&qc=1bc41a56de7a3ee419fa76397a6bf282fce5be9b93e427c08a6d916d1dfa3091)).</span></span> <span data-ttu-id="809a9-142">Þessi eiginleiki metur allar aðgerðir fyrir staðsetningarleiðbeiningar margra birgðahaldseininga.</span><span class="sxs-lookup"><span data-stu-id="809a9-142">This feature evaluates all actions for multi-SKU location directives.</span></span> <span data-ttu-id="809a9-143">Ef þessi eiginleiki er nauðsynlegur skal nota [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að kveikja á honum.</span><span class="sxs-lookup"><span data-stu-id="809a9-143">If you require this feature, use [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn it on.</span></span>

## <a name="i-cant-use-the-warehouse-management-mobile-app-to-do-partial-picking"></a><span data-ttu-id="809a9-144">Ég get ekki notað farsímaforrit vöruhúsakerfis fyrir hlutatínslu.</span><span class="sxs-lookup"><span data-stu-id="809a9-144">I can't use the Warehouse Management mobile app to do partial picking.</span></span>

### <a name="issue-description"></a><span data-ttu-id="809a9-145">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="809a9-145">Issue description</span></span>

<span data-ttu-id="809a9-146">Fyrir sölu-og flutningspantanir er ekki hægt að sleppa vörum og gera hlutatiltekt.</span><span class="sxs-lookup"><span data-stu-id="809a9-146">For sales and transfer orders, you can't skip items and do partial picking.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="809a9-147">Úrlausn úrlausnaratriðis</span><span class="sxs-lookup"><span data-stu-id="809a9-147">Issue resolution</span></span>

<span data-ttu-id="809a9-148">Á síðunni **Valmyndaratriði fartækis**, fyrir hvert valmyndaratriði sem er sett upp til að vinna sölupantanirnar eða flutningspantanir, skal stilla **Leyfa skiptingu vinnu** á flipanum **Almennt** í *Já*.</span><span class="sxs-lookup"><span data-stu-id="809a9-148">On the **Mobile device menu items** page, for each menu item that is set up to process sales orders or transfer orders, set the **Allow splitting of work** option on the **General** FastTab to *Yes*.</span></span>

## <a name="how-can-i-do-an-inventory-status-change-for-partial-quantity-work"></a><span data-ttu-id="809a9-149">Hvernig get ég breytt birgðastöðu fyrir verk að hluta?</span><span class="sxs-lookup"><span data-stu-id="809a9-149">How can I do an inventory status change for partial quantity work?</span></span>

### <a name="issue-description"></a><span data-ttu-id="809a9-150">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="809a9-150">Issue description</span></span>

<span data-ttu-id="809a9-151">Ætlunin er að gera breytingu á birgðastöðu fyrir hlutamagn runu.</span><span class="sxs-lookup"><span data-stu-id="809a9-151">You want to do an inventory status change for a partial quantity of a batch.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="809a9-152">Úrlausn úrlausnaratriðis</span><span class="sxs-lookup"><span data-stu-id="809a9-152">Issue resolution</span></span>

<span data-ttu-id="809a9-153">Til að gera starfskröftum kleift að gera þessa breytingu er hægt að stofna valmyndaratriði fyrir farsímaforrit vöruhúsakerfis.</span><span class="sxs-lookup"><span data-stu-id="809a9-153">To enable workers to make this change, you can create a menu item for the Warehouse Management mobile app.</span></span> <span data-ttu-id="809a9-154">Á síðunni **Valmyndaratriði fartækis** skal stofna (eða breyta) valmyndaratriði sem er með eftirfarandi stillingum:</span><span class="sxs-lookup"><span data-stu-id="809a9-154">On the **Mobile device menu items** page, create (or edit) a menu item that has the following settings:</span></span>

- <span data-ttu-id="809a9-155">**Máti:** *Vinna*</span><span class="sxs-lookup"><span data-stu-id="809a9-155">**Mode:** *Work*</span></span>
- <span data-ttu-id="809a9-156">**Nota fyrirliggjandi vinnu:** *Nei*</span><span class="sxs-lookup"><span data-stu-id="809a9-156">**Use existing work:** *No*</span></span>
- <span data-ttu-id="809a9-157">**Ferli verkstofnunar:** *Hreyfing*</span><span class="sxs-lookup"><span data-stu-id="809a9-157">**Work creation process:** *Movement*</span></span>
- <span data-ttu-id="809a9-158">**Birta birgðastöðu:** *Já*</span><span class="sxs-lookup"><span data-stu-id="809a9-158">**Display inventory status:** *Yes*</span></span>

<span data-ttu-id="809a9-159">Hægt er að stilla aðra reiti á síðunni eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="809a9-159">You can set other fields on the page as you require.</span></span>

## <a name="the-dock-management-profile-of-a-location-profile-is-not-preventing-inventory-types-from-being-mixed"></a><span data-ttu-id="809a9-160">Forstilling dreifingarstjórnunar fyrir staðsetningarforstillingu hindrar ekki að tegundir birgða blandist saman.</span><span class="sxs-lookup"><span data-stu-id="809a9-160">The dock management profile of a location profile is not preventing inventory types from being mixed.</span></span>

### <a name="issue-description"></a><span data-ttu-id="809a9-161">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="809a9-161">Issue description</span></span>

<span data-ttu-id="809a9-162">Verið er að nota *samstæðureglur sendingar*.</span><span class="sxs-lookup"><span data-stu-id="809a9-162">You are using *shipment consolidation policies*.</span></span> <span data-ttu-id="809a9-163">Setja þarf upp *forstillingu dreifingarstjórnunar* fyrir *staðsetningarforstillingu*, en þegar vinna er stofnuð er tegundum birgða blandað saman á lokastaðsetningunni.</span><span class="sxs-lookup"><span data-stu-id="809a9-163">You have set up a *dock management profile* for a *location profile*, but when work is created, the inventory types are mixed at the final location.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="809a9-164">Úrlausn úrlausnaratriðis</span><span class="sxs-lookup"><span data-stu-id="809a9-164">Issue resolution</span></span>

<span data-ttu-id="809a9-165">Forstilling dreifingarstjórnunar krefst þess að vinnu sé skipt upp fyrirfram.</span><span class="sxs-lookup"><span data-stu-id="809a9-165">Dock management profiles require work to be split up front.</span></span> <span data-ttu-id="809a9-166">Með öðrum orðum býst forstilling dreifingarstjórnunar við því að vinnuhaus verði ekki með mörgum frágangsstaðsetningum.</span><span class="sxs-lookup"><span data-stu-id="809a9-166">In other words, the dock management profile expects that a work header won't have multiple put locations.</span></span>

<span data-ttu-id="809a9-167">Til að forstilling dreifingarstjórnunar geti haft umsjón með blöndun birgða, þarf að setja upp vinnuhausaskil.</span><span class="sxs-lookup"><span data-stu-id="809a9-167">For the dock management profile to effectively manage the mixing of inventory, a work header break must be set up.</span></span>

<span data-ttu-id="809a9-168">Í þessu dæmi er forstilling dreifingarstjórnunar skilgreind á þann hátt að **Birgðagerðir sem ætti ekki að blanda saman** er stillt á *Auðkenni sendingar* og við munum setja upp vinnuhausaskil fyrir hana:</span><span class="sxs-lookup"><span data-stu-id="809a9-168">In this example our dock management profile is configured such that **Inventory types that should not be mixed** is set to *Shipment ID*, and we'll set up a work header break for it:</span></span>

1. <span data-ttu-id="809a9-169">Farðu í **Vöruhúsakerfi \> Uppsetning \> Vinna \> Vinnusniðmát**.</span><span class="sxs-lookup"><span data-stu-id="809a9-169">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="809a9-170">Veljið **Gerð verkbeiðni** til að breyta (t.d. *Innkaupapantanir*).</span><span class="sxs-lookup"><span data-stu-id="809a9-170">Select the **Work order type** to edit (for example, *Purchase orders*).</span></span>
1. <span data-ttu-id="809a9-171">Velið vinnusniðmátið til að breyta.</span><span class="sxs-lookup"><span data-stu-id="809a9-171">Select the work template to edit.</span></span>
1. <span data-ttu-id="809a9-172">Á aðgerðasvæðinu skal velja **Breyta fyrirspurn**.</span><span class="sxs-lookup"><span data-stu-id="809a9-172">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="809a9-173">Opnið flipann **Röðun** og bætið við línu með eftirfarandi stillingum:</span><span class="sxs-lookup"><span data-stu-id="809a9-173">Open the **Sorting** tab and add a row with the following settings:</span></span>
    - <span data-ttu-id="809a9-174">**Tafla** - *Tímabundnar vinnufærslur*</span><span class="sxs-lookup"><span data-stu-id="809a9-174">**Table** - *Temporary work transactions*</span></span>
    - <span data-ttu-id="809a9-175">**Afleidd tafla:** - *Tímabundnar vinnufærslur*</span><span class="sxs-lookup"><span data-stu-id="809a9-175">**Derived table** - *Temporary work transactions*</span></span>
    - <span data-ttu-id="809a9-176">**Reitur** - *Auðkenni sendingar*</span><span class="sxs-lookup"><span data-stu-id="809a9-176">**Field** - *Shipment ID*</span></span>
1. <span data-ttu-id="809a9-177">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="809a9-177">Select **OK**.</span></span>
1. <span data-ttu-id="809a9-178">Þú ferð til baka á síðuna **Vinnusniðmát**.</span><span class="sxs-lookup"><span data-stu-id="809a9-178">You return to the **Work templates** page.</span></span> <span data-ttu-id="809a9-179">Á aðgerðasvæðinu skal velja **Vinnuhausaskil**.</span><span class="sxs-lookup"><span data-stu-id="809a9-179">On the Action Pane, select **Work header breaks**.</span></span>
1. <span data-ttu-id="809a9-180">Á aðgerðarúðunni skal velja **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="809a9-180">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="809a9-181">Veljið gátreitinn sem tengist **Heiti reits** *Auðkenni sendingar*.</span><span class="sxs-lookup"><span data-stu-id="809a9-181">Select the check box associated with the **Field name** *Shipment ID*.</span></span>
1. <span data-ttu-id="809a9-182">Í aðgerðarúðunni skal velja **Vista**.</span><span class="sxs-lookup"><span data-stu-id="809a9-182">On the Action Pane, select **Save**.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
