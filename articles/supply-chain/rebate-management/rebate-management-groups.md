---
title: Hópa fyrir stjórnun eftirágreidds afsláttar
description: Í þessu efnisatriði er lýst hvernig á að setja upp hópa fyrir stjórnun eftirágreidds afsláttar. Hægt er að nota hópa fyrir stjórnun eftirágreidds afsláttar í útreikningum eftirágreidds afsláttar og hengja þá við aðalfærslu.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TAMRebateGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: cef7abbbf2a94e26b6b9e66492cd7347d3b4d1f2
ms.sourcegitcommit: 890a0b3eb3c1f48d786b0789e5bb8641e0b8455e
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920062"
---
# <a name="rebate-management-groups"></a><span data-ttu-id="4e893-104">Hópa fyrir stjórnun eftirágreidds afsláttar</span><span class="sxs-lookup"><span data-stu-id="4e893-104">Rebate management groups</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4e893-105">Hópar geta keyrt áfram útreikninga lækkunar.</span><span class="sxs-lookup"><span data-stu-id="4e893-105">Rebate and deduction calculations can be driven by groups.</span></span> <span data-ttu-id="4e893-106">Hægt er að búa til hópa fyrir stjórnun eftirágreidds afsláttar fyrir viðskiptavini, lánardrottna og vörur.</span><span class="sxs-lookup"><span data-stu-id="4e893-106">Rebate management groups can be created for customers, vendors, and items.</span></span> <span data-ttu-id="4e893-107">Hægt er að hengja þá við aðalfærslu.</span><span class="sxs-lookup"><span data-stu-id="4e893-107">They can be attached to a master record.</span></span>

## <a name="rebate-management-customer-groups"></a><span data-ttu-id="4e893-108">Viðskiptavinahópar fyrir stjórnun eftirágreidds afsláttar</span><span class="sxs-lookup"><span data-stu-id="4e893-108">Rebate management customer groups</span></span>

<span data-ttu-id="4e893-109">Útreikningurinn fyrir hóp viðskiptavina er oft stofnaður fyrir fyrirtækjakeðju á borð við verslunarkeðju eða vörumerki.</span><span class="sxs-lookup"><span data-stu-id="4e893-109">The calculation for a group of customers is often created for a chain of companies, such as a supermarket chain or a franchise company.</span></span> <span data-ttu-id="4e893-110">Þessi gerð útreiknings tengist yfirleitt eftirágreiddum afslætti.</span><span class="sxs-lookup"><span data-stu-id="4e893-110">This type of calculation is usually related to a rebate.</span></span>

<span data-ttu-id="4e893-111">Lækkun er oftast reiknuð án þess að taka til greina hverjum pöntunin er seld til.</span><span class="sxs-lookup"><span data-stu-id="4e893-111">A deduction is often calculated without considering who the qualifying order was sold to.</span></span> <span data-ttu-id="4e893-112">Hins vegar eru til undantekningar.</span><span class="sxs-lookup"><span data-stu-id="4e893-112">However, there are exceptions.</span></span> <span data-ttu-id="4e893-113">Til dæmis gæti leyfishafi búið til lækkunarskema þar sem viðskiptavinaflokkur A fær 4 prósent en viðskiptavinaflokkur B fær aðeins 3 prósent.</span><span class="sxs-lookup"><span data-stu-id="4e893-113">For example, a licensee might create a deduction scheme where customer group A will receive 4 percent, but customer group B will receive only 3 percent.</span></span>

### <a name="set-up-customer-groups"></a><span data-ttu-id="4e893-114">Setja upp viðskiptavinaflokka</span><span class="sxs-lookup"><span data-stu-id="4e893-114">Set up customer groups</span></span>

<span data-ttu-id="4e893-115">Til að vinna með viðskiptavinaflokka fyrir stjórnun eftirágreidds afsláttar skal fara í **Stjórnun eftirágreidds afsláttar \> Uppsetning hóps fyrir stjórnun eftirágreidds afsláttar \> Viðskiptavinaflokkar**.</span><span class="sxs-lookup"><span data-stu-id="4e893-115">To work with Rebate management customer groups, go to **Rebate management \> Rebate management groups setup \> Customer groups**.</span></span> <span data-ttu-id="4e893-116">Hægt er að nota hnappana í aðgerðarúðunni til að bæta við eða fjarlægja hópa eins og þörf er á.</span><span class="sxs-lookup"><span data-stu-id="4e893-116">You can use the buttons on the Action Pane to add and remove groups as required.</span></span> <span data-ttu-id="4e893-117">Fyrir hvern hóp skal stilla eftirfarandi reiti:</span><span class="sxs-lookup"><span data-stu-id="4e893-117">For each group, set the following fields:</span></span>

- <span data-ttu-id="4e893-118">**Hópur fyrir stjórnun eftirágreidds afsláttar** – Sláið inn einkvæmt heiti fyrir hópinn.</span><span class="sxs-lookup"><span data-stu-id="4e893-118">**Rebate management group** – Enter a unique name for the group.</span></span>
- <span data-ttu-id="4e893-119">**Lýsing** – Sláið inn lýsingu hópsins til að veita frekari upplýsingar um hvernig á að setja hann upp.</span><span class="sxs-lookup"><span data-stu-id="4e893-119">**Description** – Enter a description of the group to provide more information about how it should be used.</span></span>

### <a name="manage-customer-group-assignments"></a><span data-ttu-id="4e893-120">Stjórna úthlutunum viðskiptavinaflokka</span><span class="sxs-lookup"><span data-stu-id="4e893-120">Manage customer group assignments</span></span>

<span data-ttu-id="4e893-121">Hver viðskiptavinur getur tilheyrt fjölda flokka í stjórnun eftirágreidds afsláttar.</span><span class="sxs-lookup"><span data-stu-id="4e893-121">Each customer can belong to any number of Rebate management groups.</span></span> <span data-ttu-id="4e893-122">Til að skoða og úthluta hópmeðlimum er hægt að byrja á hópalistanum eða viðskiptavinalistanum.</span><span class="sxs-lookup"><span data-stu-id="4e893-122">To view and assign group members, you can start from either the group list or the customer list.</span></span>

<span data-ttu-id="4e893-123">Til að skoða, bæta við eða fjarlægja lánardrottna fyrir valinn hóp skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="4e893-123">To view, add, or remove customers for a selected group, follow these steps.</span></span>

1. <span data-ttu-id="4e893-124">Farið í **Stjórnun eftirágreidds afsláttar \> Uppsetning hóps fyrir stjórnun eftirágreidds afsláttar \> Viðskiptavinaflokkar**.</span><span class="sxs-lookup"><span data-stu-id="4e893-124">Go to **Rebate management \> Rebate management groups setup \> Customer groups**.</span></span>
1. <span data-ttu-id="4e893-125">Veljið hópinn sem á að stjórna.</span><span class="sxs-lookup"><span data-stu-id="4e893-125">Select the group to manage.</span></span>
1. <span data-ttu-id="4e893-126">Í aðgerðarúðunni skal velja **Viðskiptavinir**.</span><span class="sxs-lookup"><span data-stu-id="4e893-126">On the Action Pane, select **Customers**.</span></span> <span data-ttu-id="4e893-127">Síðan **Hópar fyrir stjórnun eftirágreidds afsláttar** birtist og sýnir lista yfir viðskiptavini sem eru þegar meðlimir í völdum hópi.</span><span class="sxs-lookup"><span data-stu-id="4e893-127">The **Rebate management groups** page appears and shows a list of customers that are already members of the selected group.</span></span>
1. <span data-ttu-id="4e893-128">Til að bæta nýjum viðskiptavini við hópinn skal velja **Nýr** á aðgerðasvæðinu til að bæta línu við hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="4e893-128">To add a new customer to the group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="4e893-129">Stillið svo eftirfarandi reiti fyrir nýju línuna:</span><span class="sxs-lookup"><span data-stu-id="4e893-129">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="4e893-130">**Viðskiptavinalykill** – Veljið kenni viðskiptavinalykils.</span><span class="sxs-lookup"><span data-stu-id="4e893-130">**Customer account** – Select the customer account ID.</span></span>
    - <span data-ttu-id="4e893-131">**Heiti** – Sláið inn heiti og/eða lýsingu á viðskiptavininum.</span><span class="sxs-lookup"><span data-stu-id="4e893-131">**Name** – Enter a name and/or description of the customer.</span></span>

1. <span data-ttu-id="4e893-132">Til að fjarlægja viðskiptavin úr hópnum skal velja viðskiptavin og velja svo **Eyða** á aðgerðasvæðinu.</span><span class="sxs-lookup"><span data-stu-id="4e893-132">To remove a customer from the group, select the customer, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="4e893-133">Til að skoða, bæta við eða fjarlægja hópverkefni fyrir valinn viðskiptavin skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="4e893-133">To view, add, or remove group assignments for a selected customer, follow these steps.</span></span>

1. <span data-ttu-id="4e893-134">Farðu í **Viðskiptakröfur \> Viðskiptavinir \> Alla viðskiptavini**.</span><span class="sxs-lookup"><span data-stu-id="4e893-134">Go to **Accounts receivable \> Customers \> All customers**.</span></span>
1. <span data-ttu-id="4e893-135">Veljið viðskiptavin til að vinna með.</span><span class="sxs-lookup"><span data-stu-id="4e893-135">Select the customer to work with.</span></span>
1. <span data-ttu-id="4e893-136">Á aðgerðasvæðinu, í flipanum **Viðskiptavinur**, í flokknum **Stjórnun eftirágreidds afsláttar**, skal velja **Hópar fyrir stjórnun eftirágreidds afsláttar**.</span><span class="sxs-lookup"><span data-stu-id="4e893-136">On the Action Pane, on the **Customer** tab, in the **Rebate management** group, select **Rebate management groups**.</span></span> <span data-ttu-id="4e893-137">Síðan **Hópar fyrir stjórnun eftirágreidds afsláttar** birtist og sýnir lista yfir hópa sem valinn viðskiptavinur tilheyrir.</span><span class="sxs-lookup"><span data-stu-id="4e893-137">The **Rebate management groups** page appears and shows a list of groups that the selected customer already belongs to.</span></span>
1. <span data-ttu-id="4e893-138">Til að bæta viðskiptavininum við hópinn skal velja **Nýr** á aðgerðasvæðinu til að bæta línu við hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="4e893-138">To add the customer to a new group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="4e893-139">Stillið svo eftirfarandi reiti fyrir nýju línuna:</span><span class="sxs-lookup"><span data-stu-id="4e893-139">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="4e893-140">**Hópur fyrir stjórnun eftirágreidds afsláttar** – Veljið hópinn til að bæta viðskiptavini við hann.</span><span class="sxs-lookup"><span data-stu-id="4e893-140">**Rebate management group** – Select the group to add the customer to.</span></span>
    - <span data-ttu-id="4e893-141">**Lýsing** – Sláið inn lýsingu á hópnum (til dæmis til að útskýra af hverju viðskiptavinurinn er meðlimur í honum).</span><span class="sxs-lookup"><span data-stu-id="4e893-141">**Description** – Enter a description of the group (for example, to explain why the customer is a member of it).</span></span>

1. <span data-ttu-id="4e893-142">Til að fjarlægja viðskiptavin úr hópi skal velja hópinn og velja síðan **Eyða** á aðgerðasvæðinu.</span><span class="sxs-lookup"><span data-stu-id="4e893-142">To remove a customer from a group, select the group, and then select **Delete** on the Action Pane.</span></span>

## <a name="rebate-management-vendor-groups"></a><span data-ttu-id="4e893-143">Lánardrottnaflokkar fyrir stjórnun eftirágreidds afsláttar</span><span class="sxs-lookup"><span data-stu-id="4e893-143">Rebate management vendor groups</span></span>

<span data-ttu-id="4e893-144">Útreikningurinn fyrir hóp lánardrottna er oft búinn til fyrir hóp afhendingarstaða.</span><span class="sxs-lookup"><span data-stu-id="4e893-144">The calculation for a group of vendors is often created for a group of delivery points.</span></span> <span data-ttu-id="4e893-145">Þessi gerð útreiknings tengist yfirleitt eftirágreiddum afslætti.</span><span class="sxs-lookup"><span data-stu-id="4e893-145">This type of calculation is usually related to a rebate.</span></span>

### <a name="set-up-vendor-groups"></a><span data-ttu-id="4e893-146">Uppsetning lánardrottnaflokka</span><span class="sxs-lookup"><span data-stu-id="4e893-146">Set up vendor groups</span></span>

<span data-ttu-id="4e893-147">Til að vinna með lánardrottnaflokk fyrir stjórnun eftirágreidds afsláttar skal fara í **Stjórnun eftirágreidds afsláttar \> Uppsetning hóps fyrir stjórnun eftirágreidds afsláttar \> Lánardrottnaflokkar**.</span><span class="sxs-lookup"><span data-stu-id="4e893-147">To work with Rebate management vendor groups, go to **Rebate management \> Rebate management groups setup \> Vendor groups**.</span></span> <span data-ttu-id="4e893-148">Hægt er að nota hnappana í aðgerðarúðunni til að bæta við eða fjarlægja hópa eins og þörf er á.</span><span class="sxs-lookup"><span data-stu-id="4e893-148">You can use the buttons on the Action Pane to add and remove groups as required.</span></span> <span data-ttu-id="4e893-149">Fyrir hvern hóp skal stilla eftirfarandi reiti:</span><span class="sxs-lookup"><span data-stu-id="4e893-149">For each group, set the following fields:</span></span>

- <span data-ttu-id="4e893-150">**Hópur fyrir stjórnun eftirágreidds afsláttar** – Sláið inn einkvæmt heiti fyrir hópinn.</span><span class="sxs-lookup"><span data-stu-id="4e893-150">**Rebate management group** – Enter a unique name for the group.</span></span>
- <span data-ttu-id="4e893-151">**Lýsing** – Sláið inn lýsingu hópsins til að veita frekari upplýsingar um hvernig á að setja hann upp.</span><span class="sxs-lookup"><span data-stu-id="4e893-151">**Description** – Enter a description of the group to provide more information about how it should be used.</span></span>

### <a name="manage-vendor-group-assignments"></a><span data-ttu-id="4e893-152">Stjórna úthlutunum lánardrottnaflokka</span><span class="sxs-lookup"><span data-stu-id="4e893-152">Manage vendor group assignments</span></span>

<span data-ttu-id="4e893-153">Hver lánardrottinn getur tilheyrt fjölda hópa í stjórnun eftirágreidds afsláttar.</span><span class="sxs-lookup"><span data-stu-id="4e893-153">Each vendor can belong to any number of Rebate management groups.</span></span> <span data-ttu-id="4e893-154">Til að skoða og úthluta hópmeðlimum er hægt að byrja á hópalistanum eða lánardrottnalistanum.</span><span class="sxs-lookup"><span data-stu-id="4e893-154">To view and assign group members, you can start from either the group list or the vendor list.</span></span>

<span data-ttu-id="4e893-155">Til að skoða, bæta við eða fjarlægja lánardrottna fyrir valinn hóp skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="4e893-155">To view, add, or remove vendors for a selected group, follow these steps.</span></span>

1. <span data-ttu-id="4e893-156">Farið í **Stjórnun eftirágreidds afsláttar \> Uppsetning hóps fyrir stjórnun eftirágreidds afsláttar \> Lánardrottnaflokkar**.</span><span class="sxs-lookup"><span data-stu-id="4e893-156">Go to **Rebate management \> Rebate management groups setup \> Vendor groups**.</span></span>
1. <span data-ttu-id="4e893-157">Veljið hópinn sem á að stjórna.</span><span class="sxs-lookup"><span data-stu-id="4e893-157">Select the group to manage.</span></span>
1. <span data-ttu-id="4e893-158">Á aðgerðasvæðinu velurðu **Lánardrottnar**.</span><span class="sxs-lookup"><span data-stu-id="4e893-158">On the Action Pane, select **Vendors**.</span></span> <span data-ttu-id="4e893-159">Síðan **Hópar fyrir stjórnun eftirágreidds afsláttar** birtist og sýnir lista yfir lánardrottna sem eru þegar meðlimir í völdum hópi.</span><span class="sxs-lookup"><span data-stu-id="4e893-159">The **Rebate management groups** page appears and shows a list of vendors that are already members of the selected group.</span></span>
1. <span data-ttu-id="4e893-160">Til að bæta nýjum lánardrottni við hópinn skal velja **Nýr** á aðgerðasvæðinu til að bæta línu við hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="4e893-160">To add a new vendor to the group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="4e893-161">Stillið svo eftirfarandi reiti fyrir nýju línuna:</span><span class="sxs-lookup"><span data-stu-id="4e893-161">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="4e893-162">**Lánardrottnalykill** – Veljið kenni lánardrottnalykils.</span><span class="sxs-lookup"><span data-stu-id="4e893-162">**Vendor account** – Select the vendor account ID.</span></span>
    - <span data-ttu-id="4e893-163">**Heiti** – Sláið inn heiti og/eða lýsingu á lánardrottni.</span><span class="sxs-lookup"><span data-stu-id="4e893-163">**Name** – Enter a name and/or description of the vendor.</span></span>

1. <span data-ttu-id="4e893-164">Til að fjarlægja lánardrottin úr hópnum skal velja lánardrottin og velja svo **Eyða** á aðgerðasvæðinu.</span><span class="sxs-lookup"><span data-stu-id="4e893-164">To remove a vendor from the group, select the vendor, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="4e893-165">Til að skoða, bæta við eða fjarlægja hópverkefni fyrir valinn lánardrottinn skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="4e893-165">To view, add, or remove group assignments for a selected vendor, follow these steps.</span></span>

1. <span data-ttu-id="4e893-166">Farið í **Viðskiptaskuldir \> Lánardrottnar \> Allir lánardrottnar**.</span><span class="sxs-lookup"><span data-stu-id="4e893-166">Go to **Accounts payable \> Vendors \> All vendors**.</span></span>
1. <span data-ttu-id="4e893-167">Veljið lánardrottin til að vinna með.</span><span class="sxs-lookup"><span data-stu-id="4e893-167">Select the vendor to work with.</span></span>
1. <span data-ttu-id="4e893-168">Á aðgerðasvæðinu, í flipanum **Lánardrottinn**, í flokknum **Stjórnun eftirágreidds afsláttar**, skal velja **Hópar fyrir stjórnun eftirágreidds afsláttar**.</span><span class="sxs-lookup"><span data-stu-id="4e893-168">On the Action Pane, on the **Vendor** tab, in the **Rebate management** group, select **Rebate management groups**.</span></span> <span data-ttu-id="4e893-169">Síðan **Hópar fyrir stjórnun eftirágreidds afsláttar** birtist og sýnir lista yfir hópa sem valinn lánardrottinn tilheyrir.</span><span class="sxs-lookup"><span data-stu-id="4e893-169">The **Rebate management groups** page appears and shows a list of groups that the selected vendor already belongs to.</span></span>
1. <span data-ttu-id="4e893-170">Til að bæta lánardrottni við hópinn skal velja **Nýr** á aðgerðasvæðinu til að bæta línu við hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="4e893-170">To add the vendor to a new group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="4e893-171">Stillið svo eftirfarandi reiti fyrir nýju línuna:</span><span class="sxs-lookup"><span data-stu-id="4e893-171">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="4e893-172">**Hópur fyrir stjórnun eftirágreidds afsláttar** – Veljið hópinn til að bæta lánardrottni við hann.</span><span class="sxs-lookup"><span data-stu-id="4e893-172">**Rebate management group** – Select the group to add the vendor to.</span></span>
    - <span data-ttu-id="4e893-173">**Lýsing** – Sláið inn lýsingu á hópnum (til dæmis til að útskýra af hverju lánardrottinn er meðlimur í honum).</span><span class="sxs-lookup"><span data-stu-id="4e893-173">**Description** – Enter a description of the group (for example, to explain why the vendor is a member of it).</span></span>

1. <span data-ttu-id="4e893-174">Til að fjarlægja lánardrottin úr hópi skal velja hópinn og velja síðan **Eyða** á aðgerðasvæðinu.</span><span class="sxs-lookup"><span data-stu-id="4e893-174">To remove a vendor from a group, select the group, and then select **Delete** on the Action Pane.</span></span>

## <a name="item-rebate-groups"></a><span data-ttu-id="4e893-175">Flokkar atriða eftirágreidds afsláttar</span><span class="sxs-lookup"><span data-stu-id="4e893-175">Item rebate groups</span></span>

<span data-ttu-id="4e893-176">Með því að flokka vörur eykst sveigjanleiki þegar eftirágreiddur afsláttur og lækkanir eru reiknaðar út.</span><span class="sxs-lookup"><span data-stu-id="4e893-176">By grouping items, you have more flexibility when rebates and deductions are calculated.</span></span> <span data-ttu-id="4e893-177">Þessi nálgun er oft hagkvæmari leið til að setja upp eftirágreiddan afslátt og lækkanir fyrir viðskiptavini og lánardrottna.</span><span class="sxs-lookup"><span data-stu-id="4e893-177">This approach is often a more efficient way to set up rebates and deductions for customers and vendors.</span></span>

### <a name="set-up-item-groups"></a><span data-ttu-id="4e893-178">Setja upp vöruflokka</span><span class="sxs-lookup"><span data-stu-id="4e893-178">Set up item groups</span></span>

<span data-ttu-id="4e893-179">Til að vinna með vöruflokka fyrir stjórnun eftirágreidds afsláttar skal fara í **Stjórnun eftirágreidds afsláttar \> Uppsetning hóps fyrir stjórnun eftirágreidds afsláttar \> Vöruflokkar**.</span><span class="sxs-lookup"><span data-stu-id="4e893-179">To work with Rebate management item groups, go to **Rebate management \> Rebate management groups setup \> Item groups**.</span></span> <span data-ttu-id="4e893-180">Hægt er að nota hnappana í aðgerðarúðunni til að bæta við eða fjarlægja hópa eins og þörf er á.</span><span class="sxs-lookup"><span data-stu-id="4e893-180">You can use the buttons on the Action Pane to add and remove groups as required.</span></span> <span data-ttu-id="4e893-181">Fyrir hvern hóp skal stilla eftirfarandi reiti:</span><span class="sxs-lookup"><span data-stu-id="4e893-181">For each group, set the following fields:</span></span>

- <span data-ttu-id="4e893-182">**Hópur fyrir stjórnun eftirágreidds afsláttar** – Sláið inn einkvæmt heiti fyrir hópinn.</span><span class="sxs-lookup"><span data-stu-id="4e893-182">**Rebate management group** – Enter a unique name for the group.</span></span>
- <span data-ttu-id="4e893-183">**Lýsing** – Sláið inn lýsingu hópsins til að veita frekari upplýsingar um hvernig á að setja hann upp.</span><span class="sxs-lookup"><span data-stu-id="4e893-183">**Description** – Enter a description of the group to provide more information about how it should be used.</span></span>

### <a name="manage-item-group-assignments"></a><span data-ttu-id="4e893-184">Stjórna úthlutunum vöruflokks</span><span class="sxs-lookup"><span data-stu-id="4e893-184">Manage item group assignments</span></span>

<span data-ttu-id="4e893-185">Hver vara getur tilheyrt fjölda hópa í stjórnun eftirágreidds afsláttar.</span><span class="sxs-lookup"><span data-stu-id="4e893-185">Each item can belong to any number of Rebate management groups.</span></span> <span data-ttu-id="4e893-186">Til að skoða og úthluta hópmeðlimum er hægt að byrja á hópalistanum eða vörulistanum.</span><span class="sxs-lookup"><span data-stu-id="4e893-186">To view and assign group members, you can start from either the group list or the item list.</span></span> <span data-ttu-id="4e893-187">Einnig er hægt að bæta við vörum samkvæmt tegundastigveldinu.</span><span class="sxs-lookup"><span data-stu-id="4e893-187">You can also add items based on your category hierarchy.</span></span>

<span data-ttu-id="4e893-188">Til að skoða, bæta við eða fjarlægja vörur fyrir valinn hóp skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="4e893-188">To view, add, or remove items for a selected group, follow these steps.</span></span>

1. <span data-ttu-id="4e893-189">Farið í **Stjórnun eftirágreidds afsláttar \> Uppsetning hóps fyrir stjórnun eftirágreidds afsláttar \> Vöruflokkar**.</span><span class="sxs-lookup"><span data-stu-id="4e893-189">Go to **Rebate management \> Rebate management groups setup \> Item groups**.</span></span>
1. <span data-ttu-id="4e893-190">Veljið hópinn sem á að stjórna.</span><span class="sxs-lookup"><span data-stu-id="4e893-190">Select the group to manage.</span></span>
1. <span data-ttu-id="4e893-191">Á aðgerðasvæðinu skal velja **Vörur**.</span><span class="sxs-lookup"><span data-stu-id="4e893-191">On the Action Pane, select **Items**.</span></span> <span data-ttu-id="4e893-192">Síðan **Hópar fyrir stjórnun eftirágreidds afsláttar** birtist og sýnir lista yfir vörur sem eru þegar meðlimir í völdum hópi.</span><span class="sxs-lookup"><span data-stu-id="4e893-192">The **Rebate management groups** page appears and shows a list of items that are already members of the selected group.</span></span>
1. <span data-ttu-id="4e893-193">Til að bæta nýrri vöru við hópinn skal velja **Ný** á aðgerðasvæðinu til að bæta línu við hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="4e893-193">To add a new item to the group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="4e893-194">Stillið svo eftirfarandi reiti fyrir nýju línuna:</span><span class="sxs-lookup"><span data-stu-id="4e893-194">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="4e893-195">**Vörureikningur** – Veljið kenni vörureiknings.</span><span class="sxs-lookup"><span data-stu-id="4e893-195">**Item account** – Select the item account ID.</span></span>
    - <span data-ttu-id="4e893-196">**Heiti afurðar** – Sláið inn heiti og/eða lýsingu á vörunni.</span><span class="sxs-lookup"><span data-stu-id="4e893-196">**Product name** – Enter a name and/or description of the item.</span></span>

1. <span data-ttu-id="4e893-197">Til að fjarlægja vöru úr hópi skal velja vöruna og velja **Eyða** á aðgerðasvæðinu.</span><span class="sxs-lookup"><span data-stu-id="4e893-197">To remove an item from the group, select the item, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="4e893-198">Til að skoða, bæta við eða fjarlægja hópverkefni fyrir valda vöru skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="4e893-198">To view, add, or remove group assignments for a selected item, follow these steps.</span></span>

1. <span data-ttu-id="4e893-199">Opna **Afurðaupplýsingastjórnun \> Afurðir \> Útgefnar afurðir**.</span><span class="sxs-lookup"><span data-stu-id="4e893-199">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="4e893-200">Veljið vöruna til að vinna með.</span><span class="sxs-lookup"><span data-stu-id="4e893-200">Select the item to work with.</span></span>
1. <span data-ttu-id="4e893-201">Á aðgerðasvæðinu, í flipanum **Afurð**, í flokknum **Stjórnun eftirágreidds afsláttar**, skal velja **Hópar fyrir stjórnun eftirágreidds afsláttar**.</span><span class="sxs-lookup"><span data-stu-id="4e893-201">On the Action Pane, on the **Product** tab, in the **Rebate management** group, select **Rebate management groups**.</span></span> <span data-ttu-id="4e893-202">Síðan **Hópar fyrir stjórnun eftirágreidds afsláttar** birtist og sýnir lista yfir hópa sem valin vara tilheyrir.</span><span class="sxs-lookup"><span data-stu-id="4e893-202">The **Rebate management groups** page appears and shows a list of groups that the selected item already belongs to.</span></span>
1. <span data-ttu-id="4e893-203">Til að bæta vöru við hópinn skal velja **Ný** á aðgerðasvæðinu til að bæta línu við hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="4e893-203">To add the item to a new group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="4e893-204">Stillið svo eftirfarandi reiti fyrir nýju línuna:</span><span class="sxs-lookup"><span data-stu-id="4e893-204">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="4e893-205">**Hópur fyrir stjórnun eftirágreidds afsláttar** – Veljið hópinn til að bæta vöru við hann.</span><span class="sxs-lookup"><span data-stu-id="4e893-205">**Rebate management group** – Select the group to add the item to.</span></span>
    - <span data-ttu-id="4e893-206">**Lýsing** – Sláið inn lýsingu á hópnum (til dæmis til að útskýra af hverju varan er meðlimur í honum).</span><span class="sxs-lookup"><span data-stu-id="4e893-206">**Description** – Enter a description of the group (for example, to explain why the item is a member of it).</span></span>

1. <span data-ttu-id="4e893-207">Til að fjarlægja vöru úr hópi skal velja hópinn og velja **Eyða** á aðgerðasvæðinu.</span><span class="sxs-lookup"><span data-stu-id="4e893-207">To remove an item from a group, select the group, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="4e893-208">Til að bæta vörum við hóp samkvæmt tegundastigveldinu skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="4e893-208">To add items to a group based on your category hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="4e893-209">Farið í **Stjórnun eftirágreidds afsláttar \> Uppsetning hóps fyrir stjórnun eftirágreidds afsláttar \> Vöruflokkar**.</span><span class="sxs-lookup"><span data-stu-id="4e893-209">Go to **Rebate management \> Rebate management groups setup \> Item groups**.</span></span>
1. <span data-ttu-id="4e893-210">Veljið hópinn sem á að stjórna.</span><span class="sxs-lookup"><span data-stu-id="4e893-210">Select the group to manage.</span></span>
1. <span data-ttu-id="4e893-211">Á aðgerðasvæðinu skal velja **Bæta við vörum**.</span><span class="sxs-lookup"><span data-stu-id="4e893-211">On the Action Pane, select **Add items**.</span></span>
1. <span data-ttu-id="4e893-212">Í svarglugganum **Bæta við vörum**, í reitnum **Tegundastigveldi**, skal velja hóp á hæsta stigi.</span><span class="sxs-lookup"><span data-stu-id="4e893-212">In the **Add items** dialog box, in the **Category hierarchy** field, select a top-level category.</span></span>
1. <span data-ttu-id="4e893-213">Stigveldi vöru er opnað á svæðinu til vinstri.</span><span class="sxs-lookup"><span data-stu-id="4e893-213">The item hierarchy is opened in the left pane.</span></span> <span data-ttu-id="4e893-214">Veldu stigveldi sem þú ert að leita að.</span><span class="sxs-lookup"><span data-stu-id="4e893-214">Select the hierarchy level that you're looking for.</span></span> 
1. <span data-ttu-id="4e893-215">Vörur úr völdu stigveldi og stig stigveldis er nú sýnt á svæðinu til hægri.</span><span class="sxs-lookup"><span data-stu-id="4e893-215">Items from the selected hierarchy and hierarchy level are now listed in the right pane.</span></span> <span data-ttu-id="4e893-216">Fylgið þessum skrefum til að vinna með svæðið:</span><span class="sxs-lookup"><span data-stu-id="4e893-216">Follow these steps to work with the pane:</span></span>

    - <span data-ttu-id="4e893-217">Veljið gátreitinn fyrir hverja vöru sem á að bæta við.</span><span class="sxs-lookup"><span data-stu-id="4e893-217">Select the check box for each item that you want to add.</span></span>
    - <span data-ttu-id="4e893-218">Veljið gátreitinn í haus hnitanetsins til að velja allar vörurnar sem eru sýndar.</span><span class="sxs-lookup"><span data-stu-id="4e893-218">Select the check box on the grid header to select all the items that are listed.</span></span>
    - <span data-ttu-id="4e893-219">Veljið hnappinn **Sýna valið** til að sía hnitanetið þannig að það sýni aðeins vörurnar sem hafa verið valdar fram að þessu.</span><span class="sxs-lookup"><span data-stu-id="4e893-219">Select the **Show selected** button to filter the grid so that it shows only the items that you've selected so far.</span></span> <span data-ttu-id="4e893-220">Veljið hnappinn aftur til að fara aftur í heildarlistann.</span><span class="sxs-lookup"><span data-stu-id="4e893-220">Select the button again to return to the full list.</span></span>

1. <span data-ttu-id="4e893-221">Veljið **Í lagi** til að færa vöruvalið yfir í valinn hóp.</span><span class="sxs-lookup"><span data-stu-id="4e893-221">Select **OK** to apply your item selection to the selected group.</span></span>
