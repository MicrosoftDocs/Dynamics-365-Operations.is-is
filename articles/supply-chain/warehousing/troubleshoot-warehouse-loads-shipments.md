---
title: Úrræðaleit fyrir hleðsluáætlun og sendingar
description: Þetta efnisatriði lýsir hvernig á að leysa algeng vandamál sem kunna að koma upp þegar unnið er með hleðsluáætlun og sendingar í Microsoft Dynamics 365 Supply Chain Management.
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
ms.openlocfilehash: f49a91afe9281f912d6d3579ac8e52cb1d8e5b5d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994030"
---
# <a name="troubleshoot-load-building-and-shipments"></a><span data-ttu-id="7ea53-103">Úrræðaleit fyrir hleðsluáætlun og sendingar</span><span class="sxs-lookup"><span data-stu-id="7ea53-103">Troubleshoot load building and shipments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7ea53-104">Þetta efnisatriði lýsir hvernig á að leysa algeng vandamál sem kunna að koma upp þegar unnið er með hleðsluáætlun og sendingar í Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="7ea53-104">This topic describes how to fix common issues that you might encounter while you work with load building and shipments in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-you-cant-create-a-load-line-for-this-order-line-because-it-contains-inventory-dimensions-that-are-invalid"></a><span data-ttu-id="7ea53-105">Ég fæ eftirfarandi villuboð: „Ekki er hægt að stofna farmlínu fyrir þessa pöntunarlínu vegna þess að hún inniheldur ógildar birgðavíddir...“</span><span class="sxs-lookup"><span data-stu-id="7ea53-105">I receive the following error message: "You can't create a load line for this order line because it contains inventory dimensions that are invalid..."</span></span>

### <a name="issue-description"></a><span data-ttu-id="7ea53-106">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="7ea53-106">Issue description</span></span>

<span data-ttu-id="7ea53-107">Eftirfarandi villuboð birtast þegar reynt er að losa skilapöntun í vöruhúsið:</span><span class="sxs-lookup"><span data-stu-id="7ea53-107">You receive the following error message when you try to release a return sales order to the warehouse:</span></span>

> <span data-ttu-id="7ea53-108">Ekki er hægt að stofna hleðslulínu fyrir þessa pöntunarlínu vegna þess að hún inniheldur ógildar birgðavíddir.</span><span class="sxs-lookup"><span data-stu-id="7ea53-108">You can't create a load line for this order line because it contains inventory dimensions that are invalid.</span></span> <span data-ttu-id="7ea53-109">Ekki er hægt að vísa til birgðavídda sem eru staðsettar fyrir neðan staðsetningarvíddina í frátekningarstigveldinu.</span><span class="sxs-lookup"><span data-stu-id="7ea53-109">You can't reference inventory dimensions that are located below the location dimension in the reservation hierarchy.</span></span> <span data-ttu-id="7ea53-110">Fjarlægðu ógildu víddirnar úr pöntunarlínunni.</span><span class="sxs-lookup"><span data-stu-id="7ea53-110">Remove the invalid dimensions from the order line.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="7ea53-111">Úrlausn úrlausnaratriðis</span><span class="sxs-lookup"><span data-stu-id="7ea53-111">Issue resolution</span></span>

<span data-ttu-id="7ea53-112">Því miður styður afurðin ekki hleðsluvinnslu fyrir söluskilaferli.</span><span class="sxs-lookup"><span data-stu-id="7ea53-112">Unfortunately, the product doesn't support load processing for a sales return process.</span></span> <span data-ttu-id="7ea53-113">Þar af leiðandi er ekki hægt að losa sölupöntun aftur í vöruhúsið.</span><span class="sxs-lookup"><span data-stu-id="7ea53-113">Therefore, you can't release the return sales order to the warehouse.</span></span>

<span data-ttu-id="7ea53-114">Í sölupöntunarfærslum er ekki hægt að vísa til birgðavídda sem eru staðsettar fyrir neðan víddina **Staðsetning** í frátekningarstigveldinu.</span><span class="sxs-lookup"><span data-stu-id="7ea53-114">On sales order transactions, you can't reference inventory dimensions that are located below the **Location** dimension in the reservation hierarchy.</span></span> <span data-ttu-id="7ea53-115">Lausnin við slíku er að fjarlægja ógildu víddirnar úr pöntunarlínunni.</span><span class="sxs-lookup"><span data-stu-id="7ea53-115">The resolution is to remove the invalid dimensions from the order line.</span></span>

## <a name="i-receive-the-following-error-message-one-of-the-lines-is-already-on-a-load-unable-to-release-to-warehouse"></a><span data-ttu-id="7ea53-116">Ég fær eftirfarandi villuboð: „Ein línanna er þegar í farmi.</span><span class="sxs-lookup"><span data-stu-id="7ea53-116">I receive the following error message: "One of the lines is already on a load.</span></span> <span data-ttu-id="7ea53-117">Ekki er hægt að losa í vöruhús“.</span><span class="sxs-lookup"><span data-stu-id="7ea53-117">Unable to release to warehouse."</span></span>

### <a name="issue-description"></a><span data-ttu-id="7ea53-118">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="7ea53-118">Issue description</span></span>

<span data-ttu-id="7ea53-119">Þegar farmur er búinn til handvirkt, eða þú setur upp ferlið þannig að farmur er þegar búinn til áður en færsla sölupöntunarlínunnar á sér stað, er gert ráð fyrir því að þar á eftir fari losun fram handvirkt og notast verði við leið og flokkun farmsins.</span><span class="sxs-lookup"><span data-stu-id="7ea53-119">If you manually create loads, or if you set up the process so that loads are already created before sales order line entry occurs, the assumption is that the subsequent release will be done manually, and that the route and rating from the load will be used.</span></span>

<span data-ttu-id="7ea53-120">Við aðrar hugsanlega aðstæður reynir þú sjálfvirka losun í vöruhúsið en bylgjuferlinu mistókst að stofna vinnu.</span><span class="sxs-lookup"><span data-stu-id="7ea53-120">In another possible scenario, you're trying to do an automatic release to the warehouse, but the wave process failed to create work.</span></span> <span data-ttu-id="7ea53-121">Þar af leiðandi er opin sending eða opinn farmur samt sem áður búin til.</span><span class="sxs-lookup"><span data-stu-id="7ea53-121">Therefore, an open shipment or load is still created.</span></span> <span data-ttu-id="7ea53-122">Slík opin sending eða opinn farmur loka síðan á tilraunir þar á eftir til að losa sjálfkrafa pöntunina þar til þú annað hvort eyðir opnu sendingunni eða opna farminum eða endurvinnur bylgjuna handvirkt.</span><span class="sxs-lookup"><span data-stu-id="7ea53-122">This open shipment or load then blocks subsequent attempts to automatically release the order until you either delete the open shipment or load, or manually reprocess the wave.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="7ea53-123">Úrlausn úrlausnaratriðis</span><span class="sxs-lookup"><span data-stu-id="7ea53-123">Issue resolution</span></span>

<span data-ttu-id="7ea53-124">Þú getur losað frá sölupöntunarsíðunni eða losað sjálfvirkt á sölupöntunarsíðu losunar, en einungis ef enginn farmur er fyrir hendi áður en losað er í vöruhúsið.</span><span class="sxs-lookup"><span data-stu-id="7ea53-124">You can release from the sales order page, or automatic release can be done from the release sales order page, only if no load exists before the release to the warehouse.</span></span> <span data-ttu-id="7ea53-125">Farmurinn verður sjálfkrafa búinn til eftir að úrvinnslu bylgjunnar er lokið.</span><span class="sxs-lookup"><span data-stu-id="7ea53-125">The load will automatically be created after the wave is processed.</span></span>

## <a name="i-receive-the-following-error-message-the-delivery-note-correction-cant-be-processed-the-delivery-note-only-contains-items-that-are-subject-to-warehouse-management-processes-as-these-are-not-supported-by-delivery-note-correction"></a><span data-ttu-id="7ea53-126">Ég fæ eftirfarandi villuboð: „Ekki er hægt að vinna úr leiðréttingu fylgiseðilsins.</span><span class="sxs-lookup"><span data-stu-id="7ea53-126">I receive the following error message: "The delivery note correction can't be processed.</span></span> <span data-ttu-id="7ea53-127">Fylgiseðillinn inniheldur eingöngu atriði sem falla undir vöruhúsakerfisferli, vegna þess að slík atriði eru ekki studd af leiðréttingu fylgiseðilsins“.</span><span class="sxs-lookup"><span data-stu-id="7ea53-127">The delivery note only contains items that are subject to warehouse management processes, as these are not supported by Delivery Note correction."</span></span>

### <a name="issue-description"></a><span data-ttu-id="7ea53-128">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="7ea53-128">Issue description</span></span>

<span data-ttu-id="7ea53-129">Þegar lokið er við að bóka fylgiseðil er ekki hægt að hætta við hann vegna þess að hnappurinn **Hætta við** er ekki tiltækur.</span><span class="sxs-lookup"><span data-stu-id="7ea53-129">After you post a delivery note, you can't cancel it, because the **Cancel** button is unavailable.</span></span> <span data-ttu-id="7ea53-130">Ennfremur er ekki hægt að leiðrétta fylgiseðilinn.</span><span class="sxs-lookup"><span data-stu-id="7ea53-130">You also can't correct the delivery note.</span></span> <span data-ttu-id="7ea53-131">Eftirfarandi villuboð birtast ef þú reynir slíkt.</span><span class="sxs-lookup"><span data-stu-id="7ea53-131">If you try, you receive this error message.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="7ea53-132">Úrlausn úrlausnaratriðis</span><span class="sxs-lookup"><span data-stu-id="7ea53-132">Issue resolution</span></span>

<span data-ttu-id="7ea53-133">Þú verður að bóka af farminum en ekki beint af pöntuninni til að leiðrétta bókaða fylgiseðla fyrir atriði sem eru virk í ítarlegu vöruhúsakerfi (WMS).</span><span class="sxs-lookup"><span data-stu-id="7ea53-133">To correct posted packing slips for items that are enabled for advanced warehouse management (WMS), you must do the posting from the load, not directly from the order.</span></span>

## <a name="how-can-i-create-work-from-outbound-loads-instead-of-waves"></a><span data-ttu-id="7ea53-134">Hvernig stofna ég vinnu í farmi á útleið í stað bylgja?</span><span class="sxs-lookup"><span data-stu-id="7ea53-134">How can I create work from outbound loads instead of waves?</span></span>

### <a name="issue-description"></a><span data-ttu-id="7ea53-135">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="7ea53-135">Issue description</span></span>

<span data-ttu-id="7ea53-136">Hér er ein leið til að endurskapa þetta vandamál.</span><span class="sxs-lookup"><span data-stu-id="7ea53-136">Here is one way to reproduce this issue.</span></span>

1. <span data-ttu-id="7ea53-137">Búðu til farm á útleið úr sölupöntun eða flutningspöntun.</span><span class="sxs-lookup"><span data-stu-id="7ea53-137">Create an outbound load by using a sales order or transfer order.</span></span>
2. <span data-ttu-id="7ea53-138">Losið hleðsluna í vöruhúsið.</span><span class="sxs-lookup"><span data-stu-id="7ea53-138">Release the load to the warehouse.</span></span>
3. <span data-ttu-id="7ea53-139">Taktu eftir því að engin tiltekt hefur enn verið mynduð.</span><span class="sxs-lookup"><span data-stu-id="7ea53-139">Notice that no picking work has yet been generated.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="7ea53-140">Úrlausn úrlausnaratriðis</span><span class="sxs-lookup"><span data-stu-id="7ea53-140">Issue resolution</span></span>

<span data-ttu-id="7ea53-141">Þegar mynda skal vinnu um leið og farmur er losaður verður þú að grunnstilla bylgjusniðmátið því til samræmis.</span><span class="sxs-lookup"><span data-stu-id="7ea53-141">If work must be generated immediately when the load is released, you must configure the wave template accordingly.</span></span> <span data-ttu-id="7ea53-142">Stilltu eftirfarandi valkosti á *Já* á bylgjusniðmátinu:</span><span class="sxs-lookup"><span data-stu-id="7ea53-142">On the wave template, set the following options to *Yes*:</span></span>

- <span data-ttu-id="7ea53-143">Gera stofnun bylgju sjálfvirka</span><span class="sxs-lookup"><span data-stu-id="7ea53-143">Automate wave creation</span></span>
- <span data-ttu-id="7ea53-144">Vinna úr bylgju við losun í vörugeymslu</span><span class="sxs-lookup"><span data-stu-id="7ea53-144">Process wave at release to warehouse</span></span>
- <span data-ttu-id="7ea53-145">Gera losun bylgju sjálfvirka</span><span class="sxs-lookup"><span data-stu-id="7ea53-145">Automate wave release</span></span>

## <a name="i-cant-re-release-a-partially-shipped-load"></a><span data-ttu-id="7ea53-146">Ég get ekki losað aftur um farm sem hefur verið sendur að hluta til.</span><span class="sxs-lookup"><span data-stu-id="7ea53-146">I can't re-release a partially shipped load.</span></span>

### <a name="issue-description"></a><span data-ttu-id="7ea53-147">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="7ea53-147">Issue description</span></span>

<span data-ttu-id="7ea53-148">Þú getur ekki losað um farm í vöruhúsið sem hefur verið sendur að hluta til.</span><span class="sxs-lookup"><span data-stu-id="7ea53-148">You can't release a partially shipped load to the warehouse.</span></span> <span data-ttu-id="7ea53-149">Þegar þú losar í vöruhúsið birtast skilaboðin „Aðgerðinni er lokið“ en ekkert gerist og engin vinna er mynduð fyrir magnið sem eftir er.</span><span class="sxs-lookup"><span data-stu-id="7ea53-149">When you do the release to the warehouse, an "Operation complete" message appears, but nothing happens, and no work is created for the remaining quantity.</span></span> <span data-ttu-id="7ea53-150">Þetta vandamál á sér stað þegar þú notar virkni farmflutnings og frátekning er ekki fullfrágengin.</span><span class="sxs-lookup"><span data-stu-id="7ea53-150">This issue occurs when you use transport load functionality and there is an incomplete reservation.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="7ea53-151">Úrlausn úrlausnaratriðis</span><span class="sxs-lookup"><span data-stu-id="7ea53-151">Issue resolution</span></span>

<span data-ttu-id="7ea53-152">[KB vandamál 470069](https://fix.lcs.dynamics.com/Issue/Details?kb=4574490&bugId=470069&dbType=3&qc=84ce1e09d7032d8b8ef86f5a0c68b86badf3dfaf29686c5ebbe97c53c0957b5f) („Farmur sem hefur verið sendur að hluta til er hægt að setja í aðra bylgju og aðra úrvinnslu“) er leyst í [útgáfu 10.0.15](../get-started/whats-new-scm-10-0-15.md).</span><span class="sxs-lookup"><span data-stu-id="7ea53-152">[KB issue 470069](https://fix.lcs.dynamics.com/Issue/Details?kb=4574490&bugId=470069&dbType=3&qc=84ce1e09d7032d8b8ef86f5a0c68b86badf3dfaf29686c5ebbe97c53c0957b5f) ("Partially shipped loads can be re-waved and re-processed") is fixed in [release 10.0.15](../get-started/whats-new-scm-10-0-15.md).</span></span>
