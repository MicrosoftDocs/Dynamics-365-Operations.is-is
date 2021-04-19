---
title: Tilgreint hvernig losa eigi skilaðar vörur
description: Tilgreina hvernig losa eigi skilavörur.
author: ShylaThompson
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventQuarantineOrder
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3eaeb2589329809e57ac01aba85067e94c15477c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817486"
---
# <a name="specify-how-to-dispose-of-returned-items"></a><span data-ttu-id="6f5ec-103">Tilgreint hvernig losa eigi skilaðar vörur</span><span class="sxs-lookup"><span data-stu-id="6f5ec-103">Specify how to dispose of returned items</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="6f5ec-104">Þegar skilapöntun er meðhöndluð þarf að tilgreina ástæðukóða skila til að taka það fram af hverju verið er að skila.</span><span class="sxs-lookup"><span data-stu-id="6f5ec-104">When you handle a return order, you must specify a reason return code to identify why the product is being returned.</span></span> <span data-ttu-id="6f5ec-105">Einnig þarf að tilgreina ráðstöfunarkóða og ráðstöfunaraðgerð til að ákvarða hvað gera skal við sjálfa skiluðu afurðina.</span><span class="sxs-lookup"><span data-stu-id="6f5ec-105">You must also specify a disposition code and a disposition action to determine what should be done with the returned product itself.</span></span>

<span data-ttu-id="6f5ec-106">Hægt er að nota ráðstöfunarkóða þegar stofnuð er skilapöntun, koma skráningarvöru eða þegar vörukoma er fylgiseðilsuppfærð og endi er bundinn á biðgeymslupöntun.</span><span class="sxs-lookup"><span data-stu-id="6f5ec-106">A disposition code can be applied when you create the return order, register item arrival or packing-slip update an item arrival, and end a quarantine order.</span></span>

<span data-ttu-id="6f5ec-107">Hægt er að skilgreina alla ráðstöfunarkóða sem þarf til að styðja viðskiptaferlin.</span><span class="sxs-lookup"><span data-stu-id="6f5ec-107">You can define any disposition codes that you need in order to support the business processes.</span></span> <span data-ttu-id="6f5ec-108">Eftirfarandi tafla veitir safn af mikið notuðum kóðum til að úthluta ráðstöfun skilavöru.</span><span class="sxs-lookup"><span data-stu-id="6f5ec-108">The following table provides a set of typically used codes to assign return-item disposition.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6f5ec-109">Ráðstöfunargerð</span><span class="sxs-lookup"><span data-stu-id="6f5ec-109">Disposition type</span></span></p></th>
<th><p><span data-ttu-id="6f5ec-110">Algengur kóði</span><span class="sxs-lookup"><span data-stu-id="6f5ec-110">Common code</span></span></p></th>
<th><p><span data-ttu-id="6f5ec-111">lýsing</span><span class="sxs-lookup"><span data-stu-id="6f5ec-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6f5ec-112">Losun</span><span class="sxs-lookup"><span data-stu-id="6f5ec-112">Disposal</span></span></p></td>
<td><p><span data-ttu-id="6f5ec-113">RE</span><span class="sxs-lookup"><span data-stu-id="6f5ec-113">SC</span></span></p></td>
<td><p><span data-ttu-id="6f5ec-114">Rýra/Eyða</span><span class="sxs-lookup"><span data-stu-id="6f5ec-114">Scrap/Destroy</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6f5ec-115">Losun</span><span class="sxs-lookup"><span data-stu-id="6f5ec-115">Disposal</span></span></p></td>
<td><p><span data-ttu-id="6f5ec-116">GL</span><span class="sxs-lookup"><span data-stu-id="6f5ec-116">DC</span></span></p></td>
<td><p><span data-ttu-id="6f5ec-117">Gefa til líknarmála</span><span class="sxs-lookup"><span data-stu-id="6f5ec-117">Donate to Charity</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6f5ec-118">Losun</span><span class="sxs-lookup"><span data-stu-id="6f5ec-118">Disposal</span></span></p></td>
<td><p><span data-ttu-id="6f5ec-119">LA</span><span class="sxs-lookup"><span data-stu-id="6f5ec-119">TD</span></span></p></td>
<td><p><span data-ttu-id="6f5ec-120">Losun þriðja aðila</span><span class="sxs-lookup"><span data-stu-id="6f5ec-120">Third-Party Disposal</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6f5ec-121">Losun</span><span class="sxs-lookup"><span data-stu-id="6f5ec-121">Disposal</span></span></p></td>
<td><p><span data-ttu-id="6f5ec-122">HR</span><span class="sxs-lookup"><span data-stu-id="6f5ec-122">SL</span></span></p></td>
<td><p><span data-ttu-id="6f5ec-123">Hrak</span><span class="sxs-lookup"><span data-stu-id="6f5ec-123">Salvage</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6f5ec-124">Losun</span><span class="sxs-lookup"><span data-stu-id="6f5ec-124">Disposal</span></span></p></td>
<td><p><span data-ttu-id="6f5ec-125">SA</span><span class="sxs-lookup"><span data-stu-id="6f5ec-125">TS</span></span></p></td>
<td><p><span data-ttu-id="6f5ec-126">Sala þriðja aðila (aukamarkaðir)</span><span class="sxs-lookup"><span data-stu-id="6f5ec-126">Third-Party Sale (Secondary Markets)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6f5ec-127">Laga/Breyta</span><span class="sxs-lookup"><span data-stu-id="6f5ec-127">Repair/Modify</span></span></p></td>
<td><p><span data-ttu-id="6f5ec-128">EN</span><span class="sxs-lookup"><span data-stu-id="6f5ec-128">RW</span></span></p></td>
<td><p><span data-ttu-id="6f5ec-129">Endurvinna</span><span class="sxs-lookup"><span data-stu-id="6f5ec-129">Rework</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6f5ec-130">Laga/Breyta</span><span class="sxs-lookup"><span data-stu-id="6f5ec-130">Repair/Modify</span></span></p></td>
<td><p><span data-ttu-id="6f5ec-131">EL</span><span class="sxs-lookup"><span data-stu-id="6f5ec-131">RF</span></span></p></td>
<td><p><span data-ttu-id="6f5ec-132">Endurframleiða/Laga</span><span class="sxs-lookup"><span data-stu-id="6f5ec-132">Remanufacture/Refurbish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6f5ec-133">Laga/Breyta</span><span class="sxs-lookup"><span data-stu-id="6f5ec-133">Repair/Modify</span></span></p></td>
<td><p><span data-ttu-id="6f5ec-134">BR</span><span class="sxs-lookup"><span data-stu-id="6f5ec-134">MD</span></span></p></td>
<td><p><span data-ttu-id="6f5ec-135">Breyta</span><span class="sxs-lookup"><span data-stu-id="6f5ec-135">Modify</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6f5ec-136">Laga/Breyta</span><span class="sxs-lookup"><span data-stu-id="6f5ec-136">Repair/Modify</span></span></p></td>
<td><p><span data-ttu-id="6f5ec-137">LG</span><span class="sxs-lookup"><span data-stu-id="6f5ec-137">RP</span></span></p></td>
<td><p><span data-ttu-id="6f5ec-138">Laga</span><span class="sxs-lookup"><span data-stu-id="6f5ec-138">Repair</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6f5ec-139">Laga/Breyta</span><span class="sxs-lookup"><span data-stu-id="6f5ec-139">Repair/Modify</span></span></p></td>
<td><p><span data-ttu-id="6f5ec-140">SL</span><span class="sxs-lookup"><span data-stu-id="6f5ec-140">RV</span></span></p></td>
<td><p><span data-ttu-id="6f5ec-141">Skila til lánadrottins</span><span class="sxs-lookup"><span data-stu-id="6f5ec-141">Return to Vendor</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6f5ec-142">Annað</span><span class="sxs-lookup"><span data-stu-id="6f5ec-142">Other</span></span></p></td>
<td><p><span data-ttu-id="6f5ec-143">NE</span><span class="sxs-lookup"><span data-stu-id="6f5ec-143">AI</span></span></p></td>
<td><p><span data-ttu-id="6f5ec-144">Nota eins og er</span><span class="sxs-lookup"><span data-stu-id="6f5ec-144">Use as is</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6f5ec-145">Annað</span><span class="sxs-lookup"><span data-stu-id="6f5ec-145">Other</span></span></p></td>
<td><p><span data-ttu-id="6f5ec-146">ES</span><span class="sxs-lookup"><span data-stu-id="6f5ec-146">RS</span></span></p></td>
<td><p><span data-ttu-id="6f5ec-147">Endursala</span><span class="sxs-lookup"><span data-stu-id="6f5ec-147">Resale</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6f5ec-148">Annað</span><span class="sxs-lookup"><span data-stu-id="6f5ec-148">Other</span></span></p></td>
<td><p><span data-ttu-id="6f5ec-149">GE</span><span class="sxs-lookup"><span data-stu-id="6f5ec-149">EX</span></span></p></td>
<td><p><span data-ttu-id="6f5ec-150">Gengi</span><span class="sxs-lookup"><span data-stu-id="6f5ec-150">Exchange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6f5ec-151">Annað</span><span class="sxs-lookup"><span data-stu-id="6f5ec-151">Other</span></span></p></td>
<td><p><span data-ttu-id="6f5ec-152">YM</span><span class="sxs-lookup"><span data-stu-id="6f5ec-152">MS</span></span></p></td>
<td><p><span data-ttu-id="6f5ec-153">Ýmislegt</span><span class="sxs-lookup"><span data-stu-id="6f5ec-153">Miscellaneous</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6f5ec-154">Fyrir hvern ráðstöfunarkóða sem skilgreindur er verður að velja ráðstöfunaraðgerð.</span><span class="sxs-lookup"><span data-stu-id="6f5ec-154">For each disposition code that you define, you must select a disposition action.</span></span> <span data-ttu-id="6f5ec-155">Ráðstöfunaraðgerðin ákvarðar efnisleg og fjárhagsleg áhrif af ráðstöfunarkóða.</span><span class="sxs-lookup"><span data-stu-id="6f5ec-155">The disposition action determines the physical and financial implications of the disposition codes.</span></span> <span data-ttu-id="6f5ec-156">Til dæmis ákvarðar ráðstöfunaraðgerðin efnislega meðhöndlun skiluðu vörunnar, fjárhagsleg áhrif skiluðu vörunnar og hvort senda verði skiptivöru til viðskiptamanns.</span><span class="sxs-lookup"><span data-stu-id="6f5ec-156">For example, the disposition action determines the physical handling of the returned item, the financial effect of the returned item, and if a replacement item must be sent to the customer.</span></span> <span data-ttu-id="6f5ec-157">Hægt er að skilgreina ótakmarkaðan fjölda ráðstöfunarkóða, allt eftir rekstrarþörfum, en einungis er hægt að velja úr sex fyrirfram skilgreindum ráðstöfunaraðgerðum.</span><span class="sxs-lookup"><span data-stu-id="6f5ec-157">You can define an unlimited number of disposition codes according to your business needs, but there are only six predefined disposition actions that you can select from.</span></span> <span data-ttu-id="6f5ec-158">Eftirfarandi tafla sýnir ráðstöfunaraðgerðirnar og skilgreiningar þeirra.</span><span class="sxs-lookup"><span data-stu-id="6f5ec-158">The following table provides the disposition actions and their definitions.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6f5ec-159">Ráðstöfunaraðgerð</span><span class="sxs-lookup"><span data-stu-id="6f5ec-159">Disposition action</span></span></p></th>
<th><p><span data-ttu-id="6f5ec-160">lýsing</span><span class="sxs-lookup"><span data-stu-id="6f5ec-160">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6f5ec-161"><strong>Kredit</strong></span><span class="sxs-lookup"><span data-stu-id="6f5ec-161"><strong>Credit</strong></span></span></p></td>
<td><p><span data-ttu-id="6f5ec-162">Skila vörunni í birgðir og tekjufæra viðskiptamann.</span><span class="sxs-lookup"><span data-stu-id="6f5ec-162">Return the item to inventory and credit the customer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6f5ec-163"><strong>Aðeins kredit</strong></span><span class="sxs-lookup"><span data-stu-id="6f5ec-163"><strong>Credit only</strong></span></span></p></td>
<td><p><span data-ttu-id="6f5ec-164">viðskiptamanns tekjufærður án þess að þess sé krafist eða vænst að vörunni sé skilað.</span><span class="sxs-lookup"><span data-stu-id="6f5ec-164">Credit the customer without requiring or expecting the item to be returned.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6f5ec-165"><strong>Rýrnun</strong></span><span class="sxs-lookup"><span data-stu-id="6f5ec-165"><strong>Scrap</strong></span></span></p></td>
<td><p><span data-ttu-id="6f5ec-166">Rýra vöruna og tekjufæra viðskiptamann.</span><span class="sxs-lookup"><span data-stu-id="6f5ec-166">Scrap the item and credit the customer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6f5ec-167"><strong>Skrifa yfir og setja í kredit</strong></span><span class="sxs-lookup"><span data-stu-id="6f5ec-167"><strong>Replace and credit</strong></span></span></p></td>
<td><p><span data-ttu-id="6f5ec-168">Skila vörunni í birgðir, stofna skiptipöntun og tekjufæra viðskiptamanninn.</span><span class="sxs-lookup"><span data-stu-id="6f5ec-168">Return the item to inventory, create a replacement order, and credit the customer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6f5ec-169"><strong>Skrifa yfir og eyða</strong></span><span class="sxs-lookup"><span data-stu-id="6f5ec-169"><strong>Replace and scrap</strong></span></span></p></td>
<td><p><span data-ttu-id="6f5ec-170">Rýra vöruna, stofna skiptipöntun og tekjufæra viðskiptamanninn.</span><span class="sxs-lookup"><span data-stu-id="6f5ec-170">Scrap the item, create a replacement order, and credit the customer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6f5ec-171"><strong>Skila til viðskiptavinar</strong></span><span class="sxs-lookup"><span data-stu-id="6f5ec-171"><strong>Return to customer</strong></span></span></p></td>
<td><p><span data-ttu-id="6f5ec-172">Hafna skilavörunni og skila henni aftur til viðskiptamannsins.</span><span class="sxs-lookup"><span data-stu-id="6f5ec-172">Reject the returned item and return it to the customer.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="select-a-disposition-code-for-a-quarantine-order"></a><span data-ttu-id="6f5ec-173">Veljið ráðstöfunarkóða fyrir biðgeymslupöntun</span><span class="sxs-lookup"><span data-stu-id="6f5ec-173">Select a disposition code for a quarantine order</span></span>

1.  <span data-ttu-id="6f5ec-174">Smelltu á **Birgðastjórnun** \> **Reglubundið** \> **Gæðastjórnun** \> **Biðgeymslupantanir**.</span><span class="sxs-lookup"><span data-stu-id="6f5ec-174">Click **Inventory management** \> **Periodic** \> **Quality management** \> **Quarantine orders**.</span></span>

2.  <span data-ttu-id="6f5ec-175">Fyrir núverandi biðgeymslupöntun skal velja aðgerð í reitnum **Ráðstöfunarkóði** á flipanum **Yfirlit**.</span><span class="sxs-lookup"><span data-stu-id="6f5ec-175">For an existing quarantine order, select an action from the **Disposition code** field on the **Overview** tab.</span></span>



## <a name="see-also"></a><span data-ttu-id="6f5ec-176">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="6f5ec-176">See also</span></span>

<span data-ttu-id="6f5ec-177">[Biðgeymslupöntun (skjámynd)](https://technet.microsoft.com/library/aa554073(v=ax.60))</span><span class="sxs-lookup"><span data-stu-id="6f5ec-177">[Quarantine order (form)](https://technet.microsoft.com/library/aa554073(v=ax.60))</span></span>

<span data-ttu-id="6f5ec-178">[Ráðstöfunarkóðar (skjámynd)](https://technet.microsoft.com/library/hh597113\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="6f5ec-178">[Disposition codes (form)](https://technet.microsoft.com/library/hh597113\(v=ax.60\))</span></span>

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]