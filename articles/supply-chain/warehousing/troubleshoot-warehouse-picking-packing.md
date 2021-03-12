---
title: Úrræðaleit fyrir tiltekt og pöntun
description: Þetta efnisatriði lýsir því hvernig á að laga almenn vandamál sem kunna að koma upp við tínslu og frágang í Microsoft Dynamics 365 Supply Chain Management.
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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 2cce1038ed393fc8a7bb489a37fc0921b0ac755e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993933"
---
# <a name="troubleshoot-picking-and-packing"></a><span data-ttu-id="6897a-103">Úrræðaleit fyrir tiltekt og pöntun</span><span class="sxs-lookup"><span data-stu-id="6897a-103">Troubleshoot picking and packing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6897a-104">Þetta efnisatriði lýsir því hvernig á að laga almenn vandamál sem kunna að koma upp við tínslu og frágang í Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="6897a-104">This topic describes how to fix common issues that you might encounter while you pick and pack in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-dimension-location-cant-be-left-blank-if-dimension-serial-number-is-set"></a><span data-ttu-id="6897a-105">Ég fæ eftirfarandi villuboð: „Víddarstaðsetning má ekki vera skilin eftir auð ef raðnúmersvídd er stillt.“</span><span class="sxs-lookup"><span data-stu-id="6897a-105">I receive the following error message: "Dimension location can't be left blank if dimension serial number is set."</span></span>

### <a name="issue-description"></a><span data-ttu-id="6897a-106">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="6897a-106">Issue description</span></span>

<span data-ttu-id="6897a-107">Þessi villuboð birtast ef flutningspöntun fyrir vöru með raðnúmeri er stofnuð með því að nota vöruhús sem er virkt fyrir ítarlega vöruhúsastjórnun (WMS), og svp er reynt að staðfesta sendinguna eftir að vinnu er lokið.</span><span class="sxs-lookup"><span data-stu-id="6897a-107">You receive this error message if you create a transfer order for a serial item by using a warehouse that is enabled for advanced warehouse management (WMS), and then, after the work is completed, you try to confirm the shipment.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="6897a-108">Úrlausn úrlausnaratriðis</span><span class="sxs-lookup"><span data-stu-id="6897a-108">Issue resolution</span></span>

<span data-ttu-id="6897a-109">Reiturinn **Sjálfgefin staðsetning innhreyfinga** er auður fyrir flutningsvöruhús „úr“ vöruhúsi.</span><span class="sxs-lookup"><span data-stu-id="6897a-109">The **Default receipt location** field is blank for a transit warehouse of the "from" warehouse.</span></span> <span data-ttu-id="6897a-110">Til að laga þetta vandamál þarf að tilgreina sjálfgefna staðsetningu móttöku í flutningsvöruhúsinu.</span><span class="sxs-lookup"><span data-stu-id="6897a-110">To fix this issue, specify a default receipt location in the transit warehouse.</span></span> <span data-ttu-id="6897a-111">Ganga skal úr skugga um að þessi staðsetning sé númeraplata – stjórnað.</span><span class="sxs-lookup"><span data-stu-id="6897a-111">Make sure that this location is license plate–controlled.</span></span>

## <a name="i-receive-the-following-error-message-invalid-license-plate"></a><span data-ttu-id="6897a-112">Ég fæ eftirfarandi villuboð: „Ógild númeraplata.“</span><span class="sxs-lookup"><span data-stu-id="6897a-112">I receive the following error message: "Invalid license plate."</span></span>

### <a name="issue-description"></a><span data-ttu-id="6897a-113">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="6897a-113">Issue description</span></span>

<span data-ttu-id="6897a-114">Þessi villuboð birtast í vöruhúsaforritinu þegar kenni númeraplötu er skannað.</span><span class="sxs-lookup"><span data-stu-id="6897a-114">You receive this error message in the warehouse app when you scan a license plate ID.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="6897a-115">Úrlausn úrlausnaratriðis</span><span class="sxs-lookup"><span data-stu-id="6897a-115">Issue resolution</span></span>

<span data-ttu-id="6897a-116">Ganga skal úr skugga um að númeraplötukennið sé til staðar í töflu númeraplatna og að vörurnar og magnið í númeraplötunni sé tiltækt (þ.e. að ekki sé lokað á það).</span><span class="sxs-lookup"><span data-stu-id="6897a-116">Make sure that the license plate ID exists in the license plates table, and that the items and quantities on the license plate are available (in other words, they aren't blocked).</span></span>

## <a name="i-receive-the-following-error-message-field-load-weight-1-can-only-contain-positive-numbers-update-has-been-canceled"></a><span data-ttu-id="6897a-117">Ég fæ eftirfarandi villuboð: „Reitur „Hleðsluþyngd“(=-%1) getur aðeins innihaldið jákvæðar tölur.</span><span class="sxs-lookup"><span data-stu-id="6897a-117">I receive the following error message: "Field 'Load weight'(=-%1) can only contain positive numbers.</span></span> <span data-ttu-id="6897a-118">Hætt hefur verið við uppfærslu.</span><span class="sxs-lookup"><span data-stu-id="6897a-118">Update has been canceled."</span></span>

### <a name="issue-description"></a><span data-ttu-id="6897a-119">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="6897a-119">Issue description</span></span>

<span data-ttu-id="6897a-120">Þessi villuboð birtast ef verk er opið þegar unnið er úr vinnu úr pökkunarstaðsetningum í geymslustaðsetningar eða úr geymslustaðsetningum í innhlið.</span><span class="sxs-lookup"><span data-stu-id="6897a-120">You receive this error message if there is open work when you process work from packing locations to staging locations, or from staging locations to dock locations.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="6897a-121">Úrlausn úrlausnaratriðis</span><span class="sxs-lookup"><span data-stu-id="6897a-121">Issue resolution</span></span>

<span data-ttu-id="6897a-122">Til að laga þetta vandamál skal fara í **Kerfisstjórnun \> Reglubundin verk \> Gagnagrunnur \> Samræmisathugun** og keyra ferlið fyrir **Samræmisathugun á hleðsluþyngd vöruhúss**.</span><span class="sxs-lookup"><span data-stu-id="6897a-122">To fix this issue, go to **System administration \> Periodic tasks \> Database \> Consistency check**, and run the process for **Warehouse load weight consistency check**.</span></span>

## <a name="i-receive-the-following-error-message-the-quantity-is-not-valid-for-unit-1"></a><span data-ttu-id="6897a-123">Ég fæ eftirfarandi villuskilaboð: „Magnið er ekki gilt fyrir einingu %1“.</span><span class="sxs-lookup"><span data-stu-id="6897a-123">I receive the following error message: "The quantity is not valid for unit %1."</span></span>

### <a name="issue-description"></a><span data-ttu-id="6897a-124">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="6897a-124">Issue description</span></span>

<span data-ttu-id="6897a-125">Þessi villuboð birtast þegar reynt er að framkvæma *Skipta tiltekt* á mörgum runum.</span><span class="sxs-lookup"><span data-stu-id="6897a-125">You receive this error message when you try to perform a *split pick* across multiple batches.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="6897a-126">Úrlausn úrlausnaratriðis</span><span class="sxs-lookup"><span data-stu-id="6897a-126">Issue resolution</span></span>

<span data-ttu-id="6897a-127">Starfskraftur í vöruhúsi verður að nota ferlið *Stutt tiltekt* í vöruhúsaforritinu.</span><span class="sxs-lookup"><span data-stu-id="6897a-127">The warehouse worker must use the *Short picking* process in the warehouse app.</span></span> <span data-ttu-id="6897a-128">Ef reynt er að taka til margar runur úr sömu staðsetningunni er einnig hægt að nota valkostinn **Full** í vöruhúsaforritinu.</span><span class="sxs-lookup"><span data-stu-id="6897a-128">If you're trying to pick multiple batches from the same location, you can also use the **Full** option in the warehouse app.</span></span>

## <a name="i-cant-move-inventory-to-a-location-that-is-license-platecontrolled"></a><span data-ttu-id="6897a-129">Ég get ekki flutt birgðir á staðsetningu sem er númeraplata – stýrt.</span><span class="sxs-lookup"><span data-stu-id="6897a-129">I can't move inventory to a location that is license plate–controlled.</span></span>

### <a name="issue-description"></a><span data-ttu-id="6897a-130">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="6897a-130">Issue description</span></span>

<span data-ttu-id="6897a-131">Ekki er hægt að minnka tiltektarmagn í farmi.</span><span class="sxs-lookup"><span data-stu-id="6897a-131">You can't reduce picked quantities on a load.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="6897a-132">Úrlausn úrlausnaratriðis</span><span class="sxs-lookup"><span data-stu-id="6897a-132">Issue resolution</span></span>

<span data-ttu-id="6897a-133">Í fyrri útgáfum er ekki hægt að minnka tiltektarmagn farms.</span><span class="sxs-lookup"><span data-stu-id="6897a-133">In earlier versions, you can't reduce picked quantities on a load.</span></span> <span data-ttu-id="6897a-134">Hins vegar er nú hægt að taka tiltekt til baka á staðsetningu sem er númeraplötustýrð.</span><span class="sxs-lookup"><span data-stu-id="6897a-134">However, you can now unpick to a license plate–controlled location.</span></span> <span data-ttu-id="6897a-135">Tilgreina þarf bæði gildi fyrir **Staðsetningu** og **Númeraplötu** fyrir hleðslulínuna á síðunni **Minnka tiltektarmagn**.</span><span class="sxs-lookup"><span data-stu-id="6897a-135">You must specify both a **Location** value and a **License plate** value for the load line on the **Reduce picked quantity** page.</span></span>

## <a name="can-i-print-a-delivery-note-or-packing-content-by-warehouse"></a><span data-ttu-id="6897a-136">Get ég prentað út fylgiseðil eða efni eftir vöruhúsi?</span><span class="sxs-lookup"><span data-stu-id="6897a-136">Can I print a delivery note or packing content by warehouse?</span></span>

### <a name="issue-description"></a><span data-ttu-id="6897a-137">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="6897a-137">Issue description</span></span>

<span data-ttu-id="6897a-138">Þú vilt prenta afhendingarnótu eða fylgiseðil eftir vöruhúsi eða svæði á síðunni **Uppfærsla á línum í sniðmáti vinnuendurskoðunar** .</span><span class="sxs-lookup"><span data-stu-id="6897a-138">You want to print a delivery note or packing content by warehouse or site on the **Work audit template line update** page.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="6897a-139">Úrlausn úrlausnaratriðis</span><span class="sxs-lookup"><span data-stu-id="6897a-139">Issue resolution</span></span>

<span data-ttu-id="6897a-140">Þegar skjal er prentað með því að nota stillingar prentstýringar skal takmarka umfangið (svæði/vöruhús) í gegnum prentstýringu í stað þess að velja **Breyta prentstillingum** á síðunni **Uppfæra línu vinnuendurskoðunarsniðmáts**.</span><span class="sxs-lookup"><span data-stu-id="6897a-140">When you print a document by using Print management settings, limit the scope (site/warehouse) through Print management instead of by selecting **Edit print settings** on the **Work audit template line update** page.</span></span>

## <a name="i-cant-cancel-a-packing-slip-after-its-posted-from-a-sales-order"></a><span data-ttu-id="6897a-141">Ekki er hægt að hætta við fylgiseðil eftir að hann hefur verið bókaður úr sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="6897a-141">I can't cancel a packing slip after it's posted from a sales order.</span></span>

### <a name="issue-description"></a><span data-ttu-id="6897a-142">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="6897a-142">Issue description</span></span>

<span data-ttu-id="6897a-143">Þegar tiltektar- og afhendingarferlin eru virkjuð fyrir vöruhúsakerfi er ekki hægt að hætta við fylgiseðil þegar búið er að bóka hann í sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="6897a-143">When picking and shipping processes are enabled for WMS, you can't cancel a packing slip after it's posted from a sales order.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="6897a-144">Úrlausn úrlausnaratriðis</span><span class="sxs-lookup"><span data-stu-id="6897a-144">Issue resolution</span></span>

<span data-ttu-id="6897a-145">Til að leiðrétta bókaða fylgiseðla fyrir vörur sem eru virkar í vöruhúsakerfi þarf bókunin að gerast í hleðslunni, ekki pöntuninni.</span><span class="sxs-lookup"><span data-stu-id="6897a-145">To correct posted packing slips for items that are enabled for WMS, the posting must occur from the load, not from the order.</span></span> <span data-ttu-id="6897a-146">Microsoft hefur metið þetta mál og hefur ákvarðað að þetta sé takmörkun eiginleika.</span><span class="sxs-lookup"><span data-stu-id="6897a-146">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="6897a-147">Sölupöntun sem hefur verið tínd og send í gegnum vöruhúsakerfisferla er almennt hægt að uppfæra fylgiseðil fyrir í hleðslunni eða sendingunni og sjálfu sölupöntunarskjalinu.</span><span class="sxs-lookup"><span data-stu-id="6897a-147">In general, a sales order that has been picked and shipped through warehouse management processes can be packing slip–updated from the load or shipment and the sales order document itself.</span></span> <span data-ttu-id="6897a-148">Ef fylgiseðill í sölupöntun er hinsvegar uppfærður úr sölupöntunarskjalinu, verður samt ekki hægt að afturkalla fylgiseðil úr hleðslunni eða sölupöntuninni.</span><span class="sxs-lookup"><span data-stu-id="6897a-148">However, if you packing slip–update the sales order from the sales order document, packing slip reversal still can't be done from the load or sales order.</span></span> <span data-ttu-id="6897a-149">Þess vegna er mælt með því að bókun fylgiseðilsins sé notuð úr hleðslunni.</span><span class="sxs-lookup"><span data-stu-id="6897a-149">Therefore, we recommend that you use the packing slip posting from the load.</span></span> <span data-ttu-id="6897a-150">Í þessu tilfellum er bakfærslan sem verður að vera gerð úr hleðslunni gerð virk.</span><span class="sxs-lookup"><span data-stu-id="6897a-150">In this case, the reversal that must be done from the load will be enabled.</span></span>

## <a name="i-receive-the-following-error-message-not-enough-work-can-be-found-for-cluster"></a><span data-ttu-id="6897a-151">Ég fæ eftirfarandi villuboð „Ekki finnst nægileg vinna fyrir klasann“.</span><span class="sxs-lookup"><span data-stu-id="6897a-151">I receive the following error message: "Not enough work can be found for cluster."</span></span>

### <a name="issue-description"></a><span data-ttu-id="6897a-152">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="6897a-152">Issue description</span></span>

<span data-ttu-id="6897a-153">Þegar ferlið *Kerfisstýrð klasatiltekt* er notað, ef klasaforstilling er skilgreind þar sem t.d. hægt er að tína úr 10 staðsetningum, virkar ferlið samkvæmt áætlun þegar næg vinna er til að tína í 10 staðsetningum.</span><span class="sxs-lookup"><span data-stu-id="6897a-153">When you use the *System directed cluster picking* process, if you configure a cluster profile where, for example, 10 positions can be picked, the process works as planned when there is enough work to pick to 10 positions.</span></span> <span data-ttu-id="6897a-154">Ef hinsvegar aðeins átta staðsetningar eru til að tína úr, koma upp þessi villuboð vegna þess að ekki er nóg vinna fyrir einn klasa.</span><span class="sxs-lookup"><span data-stu-id="6897a-154">However, if there are only eight positions to pick, you receive this error message, because there isn't enough work for one cluster.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="6897a-155">Úrlausn úrlausnaratriðis</span><span class="sxs-lookup"><span data-stu-id="6897a-155">Issue resolution</span></span>

<span data-ttu-id="6897a-156">Til að laga þetta vandamál skal breyta klasaforstillingunni og stilla valkostinn **Virkja stöður** á *Nei*.</span><span class="sxs-lookup"><span data-stu-id="6897a-156">To fix this issue, edit the cluster profile, and set the **Activate positions** option to *No*.</span></span>
