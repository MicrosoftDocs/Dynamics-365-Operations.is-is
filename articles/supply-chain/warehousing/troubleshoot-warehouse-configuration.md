---
title: Úrræðaleit fyrir grunnstillingu vöruhúss
description: Þetta efnisatriði lýsir því hvernig á að laga almenn vandamál sem kunna að koma upp við stillingu Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 9bbe92627f53b3b4b04597be144d602b3cae7ed7
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/25/2020
ms.locfileid: "4646108"
---
# <a name="troubleshoot-warehouse-configuration"></a><span data-ttu-id="612be-103">Úrræðaleit fyrir grunnstillingu vöruhúss</span><span class="sxs-lookup"><span data-stu-id="612be-103">Troubleshoot warehouse configuration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="612be-104">Þetta efnisatriði lýsir því hvernig á að laga almenn vandamál sem kunna að koma upp við stillingu Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="612be-104">This topic describes how to fix common issues that you might encounter while you configure Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-the-license-plate-or-location-is-not-valid"></a><span data-ttu-id="612be-105">Ég fæ eftirfarandi villuboð: „Númeraplatan eða staðsetningin er ekki gild“.</span><span class="sxs-lookup"><span data-stu-id="612be-105">I receive the following error message: "The license plate or location is not valid."</span></span>

### <a name="issue-description"></a><span data-ttu-id="612be-106">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="612be-106">Issue description</span></span>

<span data-ttu-id="612be-107">Þessi villuboð birtast þegar kenni númeraplötu eða staðsetning er skönnuð.</span><span class="sxs-lookup"><span data-stu-id="612be-107">You receive this error message when you scan a license plate ID or location.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="612be-108">Úrlausn úrlausnaratriðis</span><span class="sxs-lookup"><span data-stu-id="612be-108">Issue resolution</span></span>

<span data-ttu-id="612be-109">Gangið úr skugga um að kenni númeraplötunnar sé ekki tekið frá eitthvað annað.</span><span class="sxs-lookup"><span data-stu-id="612be-109">Make sure that the license plate ID isn't reserved by something else.</span></span> <span data-ttu-id="612be-110">Þetta vandamál kom upp þegar gildið sem notandi skannaði í vöruhúsaforrotinu var bæði gild staðsetning og gilt númerakenni.</span><span class="sxs-lookup"><span data-stu-id="612be-110">This issue used to occur when the value that a user scanned in the warehouse app was both a valid location and a valid license plate ID.</span></span> <span data-ttu-id="612be-111">Hins vegar var þetta vandamál leyst í útgáfu 10.0.11.</span><span class="sxs-lookup"><span data-stu-id="612be-111">However, this issue was resolved in version 10.0.11.</span></span>

## <a name="i-receive-the-following-error-message-license-plate-must-be-specified-for-this-location"></a><span data-ttu-id="612be-112">Ég fæ eftirfarandi villuboð: „Tilgreina þarf númeraplötu fyrir þessa staðsetningu“.</span><span class="sxs-lookup"><span data-stu-id="612be-112">I receive the following error message: "License plate must be specified for this location."</span></span>

### <a name="issue-description"></a><span data-ttu-id="612be-113">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="612be-113">Issue description</span></span>

<span data-ttu-id="612be-114">Þessi villuboð verða send ef flutningspöntun er stofnuð með því að nota vöruhús sem er virkt fyrir ítarlega vöruhúsastjórnun (WMS), og svo er reynt að staðfesta sendinguna eftir að vinnu er lokið.</span><span class="sxs-lookup"><span data-stu-id="612be-114">You receive this error message if you create a transfer order by using a warehouse that is enabled for advanced warehouse management (WMS), and then, after the work is completed, you try to confirm the shipment.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="612be-115">Úrlausn úrlausnaratriðis</span><span class="sxs-lookup"><span data-stu-id="612be-115">Issue resolution</span></span>

<span data-ttu-id="612be-116">Reiturinn **Sjálfgefin staðsetning innhreyfinga** er auður fyrir flutningsvöruhús „úr“ vöruhúsi.</span><span class="sxs-lookup"><span data-stu-id="612be-116">The **Default receipt location** field is blank for a transit warehouse of the "from" warehouse.</span></span> <span data-ttu-id="612be-117">Til að laga þetta vandamál þarf að tilgreina sjálfgefna staðsetningu móttöku í flutningsvöruhúsinu.</span><span class="sxs-lookup"><span data-stu-id="612be-117">To fix this issue, specify a default receipt location in the transit warehouse.</span></span> <span data-ttu-id="612be-118">Ganga skal úr skugga um að þessi staðsetning sé númeraplata – stjórnað.</span><span class="sxs-lookup"><span data-stu-id="612be-118">Make sure that this location is license plate–controlled.</span></span>

## <a name="i-receive-the-following-error-message-you-cant-create-a-work-template-line-for-inventory-status-change-because-the-work-type-is-not-valid-select-a-different-work-type"></a><span data-ttu-id="612be-119">Ég fæ eftirfarandi villuboð: Ekki er hægt að stofna vinnusniðmátslínu fyrir Breyting á birgðastöðu því að vinnutegundin er ógild.</span><span class="sxs-lookup"><span data-stu-id="612be-119">I receive the following error message: "You can't create a work template line for Inventory status change because the work type is not valid.</span></span> <span data-ttu-id="612be-120">Velja skal aðra vinnutegund.</span><span class="sxs-lookup"><span data-stu-id="612be-120">Select a different work type."</span></span>

### <a name="issue-description"></a><span data-ttu-id="612be-121">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="612be-121">Issue description</span></span>

<span data-ttu-id="612be-122">Fyrir vinnusniðmát er ekki hægt að velja *Breyting á birgðastöðu* í dálknum **Vinnusniðmát** í hlutanum **Upplýsingar um vinnusniðmát**.</span><span class="sxs-lookup"><span data-stu-id="612be-122">For a work template, you can't select *Inventory status change* in the **Work type** column of the **Work template details** section.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="612be-123">Úrlausn úrlausnaratriðis</span><span class="sxs-lookup"><span data-stu-id="612be-123">Issue resolution</span></span>

<span data-ttu-id="612be-124">Þessi hegðun er samkvæmt hönnuninni.</span><span class="sxs-lookup"><span data-stu-id="612be-124">This behavior is by design.</span></span> <span data-ttu-id="612be-125">Vinnutegundin *Breyting á birgðastöðu* er aðeins notuð af kerfisvinnslu.</span><span class="sxs-lookup"><span data-stu-id="612be-125">The *Inventory status change* work type is used only by system processes.</span></span> <span data-ttu-id="612be-126">Ekki er hægt að stilla þetta.</span><span class="sxs-lookup"><span data-stu-id="612be-126">It can't be configured.</span></span> <span data-ttu-id="612be-127">Vegna þess að listi yfir vinnugerðir er fastur sem tölusetning er ekki hægt að sía aukafærslur úr fellivalmyndinni **Vinnutegund**.</span><span class="sxs-lookup"><span data-stu-id="612be-127">Because the list of work types is fixed as an enumeration, the extra entries can't be filtered out of the **Work type** drop-down menu.</span></span>

## <a name="i-receive-the-following-error-message-the-quantity-is-not-valid-for-unit-1"></a><span data-ttu-id="612be-128">Ég fæ eftirfarandi villuskilaboð: „Magnið er ekki gilt fyrir einingu „Magnið er ekki gilt fyrir einingu 1%“.</span><span class="sxs-lookup"><span data-stu-id="612be-128">I receive the following error message: "The Quantity is not valid for unit 1%."</span></span>

### <a name="issue-description"></a><span data-ttu-id="612be-129">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="612be-129">Issue description</span></span>

<span data-ttu-id="612be-130">Magnið er ekki gilt fyrir *ea* eininguna þegar um er að ræða tiltektarvinnu sem er með margar númeraplötur á einni staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="612be-130">The quantity isn't valid for the *ea* unit when there is picking work that has multiple license plates in one location.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="612be-131">Úrlausn úrlausnaratriðis</span><span class="sxs-lookup"><span data-stu-id="612be-131">Issue resolution</span></span>

<span data-ttu-id="612be-132">Gangið úr skugga um að **Auðkenni röðunarflokks einingar** og **Einingaumreikningar** reitir á útgefnu afurðina eða afurðarafbrigðið séu rétt stillt.</span><span class="sxs-lookup"><span data-stu-id="612be-132">Verify that the **Unit sequence group ID** and **Unit conversions** fields on the released product or product variant are set correctly.</span></span>

<span data-ttu-id="612be-133">Athugið að villuboðin hafa verið endurbætt í útgáfu 10.0.15 (sjá [KB 4581627](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486531)).</span><span class="sxs-lookup"><span data-stu-id="612be-133">Note that the error message has been improved in version 10.0.15 (see [KB 4581627](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486531)).</span></span> <span data-ttu-id="612be-134">Nýju villuboðin eru, Magnið er ekki gilt.</span><span class="sxs-lookup"><span data-stu-id="612be-134">The new error message is, "The quantity is not valid.</span></span> <span data-ttu-id="612be-135">Væntanlegt %1 %2."</span><span class="sxs-lookup"><span data-stu-id="612be-135">Expected %1 %2."</span></span>

## <a name="in-location-directives-for-sales-order-put-work-the-multiple-sku-option-doesnt-evaluate-multiple-location-directive-actions"></a><span data-ttu-id="612be-136">Í staðsetningarleiðbeiningum fyrir frágang sölupöntunar metur valkostur birgðahaldseiningar ekki margar aðgerðir staðsetningarleiðbeininga.</span><span class="sxs-lookup"><span data-stu-id="612be-136">In location directives for sales order put work, the multiple SKU option doesn't evaluate multiple location directive actions.</span></span>

### <a name="issue-description"></a><span data-ttu-id="612be-137">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="612be-137">Issue description</span></span>

<span data-ttu-id="612be-138">Staðsetningarleiðbeiningar af vinnutegundinni *Sölupantanir* og *Frágangur* ekki meta margar aðgerðir staðsetningarleiðbeininga þegar valkosturinn **Margar birgðahaldseiningar** er valinn.</span><span class="sxs-lookup"><span data-stu-id="612be-138">Location directives of the *Sales orders* work order type and the *Put* work type don't evaluate multiple location directive actions when the **Multiple SKU** option is selected.</span></span> <span data-ttu-id="612be-139">Aðeins fyrsta aðgerð fyrir staðsetningarleiðbeiningar er metin.</span><span class="sxs-lookup"><span data-stu-id="612be-139">Only the first location directive action is evaluated.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="612be-140">Úrlausn úrlausnaratriðis</span><span class="sxs-lookup"><span data-stu-id="612be-140">Issue resolution</span></span>

<span data-ttu-id="612be-141">Nýr eiginleiki, *Meta allar aðgerðir fyrir staðsetningarleiðbeiningar margra birgðahaldseininga*, hefur verið bætt við útgáfu 10.0.15 (sjá [KB 4579866](https://fix.lcs.dynamics.com/Issue/Details?kb=4579866&bugId=475946&dbType=3&qc=1bc41a56de7a3ee419fa76397a6bf282fce5be9b93e427c08a6d916d1dfa3091)).</span><span class="sxs-lookup"><span data-stu-id="612be-141">A new feature, *Evaluate all actions for Multi SKU location directives*, has been added in version 10.0.15 (see [KB 4579866](https://fix.lcs.dynamics.com/Issue/Details?kb=4579866&bugId=475946&dbType=3&qc=1bc41a56de7a3ee419fa76397a6bf282fce5be9b93e427c08a6d916d1dfa3091)).</span></span> <span data-ttu-id="612be-142">Þessi eiginleiki metur allar aðgerðir fyrir staðsetningarleiðbeiningar margra birgðahaldseininga.</span><span class="sxs-lookup"><span data-stu-id="612be-142">This feature evaluates all actions for multi-SKU location directives.</span></span> <span data-ttu-id="612be-143">Ef þessi eiginleiki er nauðsynlegur skal nota [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að kveikja á honum.</span><span class="sxs-lookup"><span data-stu-id="612be-143">If you require this feature, use [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn it on.</span></span>

## <a name="i-cant-use-the-warehouse-app-to-do-partial-picking"></a><span data-ttu-id="612be-144">Ég get ekki notað vöruhúsaforritið fyrir hlutatínslu.</span><span class="sxs-lookup"><span data-stu-id="612be-144">I can't use the warehouse app to do partial picking.</span></span>

### <a name="issue-description"></a><span data-ttu-id="612be-145">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="612be-145">Issue description</span></span>

<span data-ttu-id="612be-146">Fyrir sölu-og flutningspantanir er ekki hægt að sleppa vörum og gera hlutatiltekt.</span><span class="sxs-lookup"><span data-stu-id="612be-146">For sales and transfer orders, you can't skip items and do partial picking.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="612be-147">Úrlausn úrlausnaratriðis</span><span class="sxs-lookup"><span data-stu-id="612be-147">Issue resolution</span></span>

<span data-ttu-id="612be-148">Á síðunni **Valmyndaratriði fartækis**, fyrir hvert valmyndaratriði sem er sett upp til að vinna sölupantanirnar eða flutningspantanir, skal stilla **Leyfa skiptingu vinnu** á flipanum **Almennt** í *Já*.</span><span class="sxs-lookup"><span data-stu-id="612be-148">On the **Mobile device menu items** page, for each menu item that is set up to process sales orders or transfer orders, set the **Allow splitting of work** option on the **General** FastTab to *Yes*.</span></span>

## <a name="how-can-i-do-an-inventory-status-change-for-partial-quantity-work"></a><span data-ttu-id="612be-149">Hvernig get ég breytt birgðastöðu fyrir verk að hluta?</span><span class="sxs-lookup"><span data-stu-id="612be-149">How can I do an inventory status change for partial quantity work?</span></span>

### <a name="issue-description"></a><span data-ttu-id="612be-150">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="612be-150">Issue description</span></span>

<span data-ttu-id="612be-151">Ætlunin er að gera breytingu á birgðastöðu fyrir hlutamagn runu.</span><span class="sxs-lookup"><span data-stu-id="612be-151">You want to do an inventory status change for a partial quantity of a batch.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="612be-152">Úrlausn úrlausnaratriðis</span><span class="sxs-lookup"><span data-stu-id="612be-152">Issue resolution</span></span>

<span data-ttu-id="612be-153">Til að gera starfskröftum kleift að gera þessa breytingu er hægt að stofna valmyndaratriði fyrir vöruhúsaforritið.</span><span class="sxs-lookup"><span data-stu-id="612be-153">To enable workers to make this change, you can create a menu item for the warehouse app.</span></span> <span data-ttu-id="612be-154">Á síðunni **Valmyndaratriði fartækis** skal stofna (eða breyta) valmyndaratriði sem er með eftirfarandi stillingum:</span><span class="sxs-lookup"><span data-stu-id="612be-154">On the **Mobile device menu items** page, create (or edit) a menu item that has the following settings:</span></span>

- <span data-ttu-id="612be-155">**Máti:** *Vinna*</span><span class="sxs-lookup"><span data-stu-id="612be-155">**Mode:** *Work*</span></span>
- <span data-ttu-id="612be-156">**Nota fyrirliggjandi vinnu:** *Nei*</span><span class="sxs-lookup"><span data-stu-id="612be-156">**Use existing work:** *No*</span></span>
- <span data-ttu-id="612be-157">**Ferli verkstofnunar:** *Hreyfing*</span><span class="sxs-lookup"><span data-stu-id="612be-157">**Work creation process:** *Movement*</span></span>
- <span data-ttu-id="612be-158">**Birta birgðastöðu:** *Já*</span><span class="sxs-lookup"><span data-stu-id="612be-158">**Display inventory status:** *Yes*</span></span>

<span data-ttu-id="612be-159">Hægt er að stilla aðra reiti á síðunni eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="612be-159">You can set other fields on the page as you require.</span></span>
