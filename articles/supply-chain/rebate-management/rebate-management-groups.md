---
title: Hópa fyrir stjórnun eftirágreidds afsláttar
description: Í þessu efnisatriði er lýst hvernig á að setja upp hópa fyrir stjórnun eftirágreidds afsláttar. Hægt er að nota hópa fyrir stjórnun eftirágreidds afsláttar í útreikningum eftirágreidds afsláttar og hengja þá við aðalfærslu.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TAMRebateGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: ee5a195b3d2881ff70fb1f0d4063ed681e874648
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271078"
---
# <a name="rebate-management-groups"></a><span data-ttu-id="b9bbb-104">Hópar fyrir stjórnun eftirágreidds afsláttar</span><span class="sxs-lookup"><span data-stu-id="b9bbb-104">Rebate management groups</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b9bbb-105">Hópar geta keyrt útreikninga á eftirágreiddum afslætti.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-105">Rebate management calculations can be driven by groups.</span></span> <span data-ttu-id="b9bbb-106">Hægt er að búa til hópa fyrir stjórnun eftirágreidds afsláttar fyrir viðskiptavini, lánardrottna og vörur.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-106">Rebate management groups can be created for customers, vendors, and items.</span></span> <span data-ttu-id="b9bbb-107">Hægt er að hengja þá við aðalfærslu.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-107">They can be attached to a master record.</span></span>

## <a name="rebate-management-customer-groups"></a><span data-ttu-id="b9bbb-108">Viðskiptavinahópar fyrir stjórnun eftirágreidds afsláttar</span><span class="sxs-lookup"><span data-stu-id="b9bbb-108">Rebate management customer groups</span></span>

<span data-ttu-id="b9bbb-109">Útreikningurinn fyrir hóp viðskiptavina er oft stofnaður fyrir fyrirtækjakeðju á borð við verslunarkeðju eða vörumerki.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-109">The calculation for a group of customers is often created for a chain of companies, such as a supermarket chain or a franchise company.</span></span> <span data-ttu-id="b9bbb-110">Þessi gerð útreiknings tengist yfirleitt eftirágreiddum afslætti.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-110">This type of calculation is usually related to a rebate.</span></span>

<span data-ttu-id="b9bbb-111">Lækkun er oftast reiknuð án þess að taka til greina hverjum pöntunin er seld til.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-111">A deduction is often calculated without considering who the qualifying order was sold to.</span></span> <span data-ttu-id="b9bbb-112">Hins vegar eru til undantekningar.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-112">However, there are exceptions.</span></span> <span data-ttu-id="b9bbb-113">Til dæmis gæti leyfishafi búið til lækkunarskema þar sem viðskiptavinaflokkur A fær 4 prósent en viðskiptavinaflokkur B fær aðeins 3 prósent.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-113">For example, a licensee might create a deduction scheme where customer group A will receive 4 percent, but customer group B will receive only 3 percent.</span></span>

### <a name="set-up-customer-groups"></a><span data-ttu-id="b9bbb-114">Setja upp viðskiptavinaflokka</span><span class="sxs-lookup"><span data-stu-id="b9bbb-114">Set up customer groups</span></span>

<span data-ttu-id="b9bbb-115">Til að vinna með viðskiptavinaflokka fyrir stjórnun eftirágreidds afsláttar skal fara í **Stjórnun eftirágreidds afsláttar \> Uppsetning hóps fyrir stjórnun eftirágreidds afsláttar \> Viðskiptavinaflokkar**.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-115">To work with Rebate management customer groups, go to **Rebate management \> Rebate management groups setup \> Customer groups**.</span></span> <span data-ttu-id="b9bbb-116">Hægt er að nota hnappana í aðgerðarúðunni til að bæta við eða fjarlægja hópa eins og þörf er á.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-116">You can use the buttons on the Action Pane to add and remove groups as required.</span></span> <span data-ttu-id="b9bbb-117">Fyrir hvern hóp skal stilla eftirfarandi reiti:</span><span class="sxs-lookup"><span data-stu-id="b9bbb-117">For each group, set the following fields:</span></span>

- <span data-ttu-id="b9bbb-118">**Hópur fyrir stjórnun eftirágreidds afsláttar** – Sláið inn einkvæmt heiti fyrir hópinn.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-118">**Rebate management group** – Enter a unique name for the group.</span></span>
- <span data-ttu-id="b9bbb-119">**Lýsing** – Sláið inn lýsingu hópsins til að veita frekari upplýsingar um hvernig á að setja hann upp.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-119">**Description** – Enter a description of the group to provide more information about how it should be used.</span></span>

### <a name="manage-customer-group-assignments"></a><span data-ttu-id="b9bbb-120">Stjórna úthlutunum viðskiptavinaflokka</span><span class="sxs-lookup"><span data-stu-id="b9bbb-120">Manage customer group assignments</span></span>

<span data-ttu-id="b9bbb-121">Hver viðskiptavinur getur tilheyrt fjölda flokka í stjórnun eftirágreidds afsláttar.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-121">Each customer can belong to any number of Rebate management groups.</span></span> <span data-ttu-id="b9bbb-122">Til að skoða og úthluta hópmeðlimum er hægt að byrja á hópalistanum eða viðskiptavinalistanum.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-122">To view and assign group members, you can start from either the group list or the customer list.</span></span>

<span data-ttu-id="b9bbb-123">Til að skoða, bæta við eða fjarlægja lánardrottna fyrir valinn hóp skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-123">To view, add, or remove customers for a selected group, follow these steps.</span></span>

1. <span data-ttu-id="b9bbb-124">Farið í **Stjórnun eftirágreidds afsláttar \> Uppsetning hóps fyrir stjórnun eftirágreidds afsláttar \> Viðskiptavinaflokkar**.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-124">Go to **Rebate management \> Rebate management groups setup \> Customer groups**.</span></span>
1. <span data-ttu-id="b9bbb-125">Veljið hópinn sem á að stjórna.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-125">Select the group to manage.</span></span>
1. <span data-ttu-id="b9bbb-126">Í aðgerðarúðunni skal velja **Viðskiptavinir**.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-126">On the Action Pane, select **Customers**.</span></span> <span data-ttu-id="b9bbb-127">Síðan **Hópar fyrir stjórnun eftirágreidds afsláttar** birtist og sýnir lista yfir viðskiptavini sem eru þegar meðlimir í völdum hópi.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-127">The **Rebate management groups** page appears and shows a list of customers that are already members of the selected group.</span></span>
1. <span data-ttu-id="b9bbb-128">Til að bæta nýjum viðskiptavini við hópinn skal velja **Nýr** á aðgerðasvæðinu til að bæta línu við hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-128">To add a new customer to the group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="b9bbb-129">Stillið svo eftirfarandi reit fyrir nýju línuna:</span><span class="sxs-lookup"><span data-stu-id="b9bbb-129">Then set the following field for the new row:</span></span>

    - <span data-ttu-id="b9bbb-130">**Viðskiptavinalykill** – Veljið kenni viðskiptavinalykils.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-130">**Customer account** – Select the customer account ID.</span></span>

1. <span data-ttu-id="b9bbb-131">Til að fjarlægja viðskiptavin úr hópnum skal velja viðskiptavin og velja svo **Eyða** á aðgerðasvæðinu.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-131">To remove a customer from the group, select the customer, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="b9bbb-132">Til að skoða, bæta við eða fjarlægja hópverkefni fyrir valinn viðskiptavin skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-132">To view, add, or remove group assignments for a selected customer, follow these steps.</span></span>

1. <span data-ttu-id="b9bbb-133">Farðu í **Viðskiptakröfur \> Viðskiptavinir \> Alla viðskiptavini**.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-133">Go to **Accounts receivable \> Customers \> All customers**.</span></span>
1. <span data-ttu-id="b9bbb-134">Veljið viðskiptavin til að vinna með.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-134">Select the customer to work with.</span></span>
1. <span data-ttu-id="b9bbb-135">Á aðgerðasvæðinu, í flipanum **Viðskiptavinur**, í flokknum **Stjórnun eftirágreidds afsláttar**, skal velja **Hópar fyrir stjórnun eftirágreidds afsláttar**.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-135">On the Action Pane, on the **Customer** tab, in the **Rebate management** group, select **Rebate management groups**.</span></span> <span data-ttu-id="b9bbb-136">Síðan **Hópar fyrir stjórnun eftirágreidds afsláttar** birtist og sýnir lista yfir hópa sem valinn viðskiptavinur tilheyrir.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-136">The **Rebate management groups** page appears and shows a list of groups that the selected customer already belongs to.</span></span>
1. <span data-ttu-id="b9bbb-137">Til að bæta viðskiptavininum við hópinn skal velja **Nýr** á aðgerðasvæðinu til að bæta línu við hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-137">To add the customer to a new group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="b9bbb-138">Stillið svo eftirfarandi reit fyrir nýju línuna:</span><span class="sxs-lookup"><span data-stu-id="b9bbb-138">Then set the following field for the new row:</span></span>

    - <span data-ttu-id="b9bbb-139">**Hópur fyrir stjórnun eftirágreidds afsláttar** – Veljið hópinn til að bæta viðskiptavini við hann.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-139">**Rebate management group** – Select the group to add the customer to.</span></span>

1. <span data-ttu-id="b9bbb-140">Til að fjarlægja viðskiptavin úr hópi skal velja hópinn og velja síðan **Eyða** á aðgerðasvæðinu.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-140">To remove a customer from a group, select the group, and then select **Delete** on the Action Pane.</span></span>

## <a name="rebate-management-vendor-groups"></a><span data-ttu-id="b9bbb-141">Lánardrottnaflokkar fyrir stjórnun eftirágreidds afsláttar</span><span class="sxs-lookup"><span data-stu-id="b9bbb-141">Rebate management vendor groups</span></span>

<span data-ttu-id="b9bbb-142">Útreikningurinn fyrir hóp lánardrottna er oft búinn til fyrir hóp afhendingarstaða.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-142">The calculation for a group of vendors is often created for a group of delivery points.</span></span> <span data-ttu-id="b9bbb-143">Þessi gerð útreiknings tengist yfirleitt eftirágreiddum afslætti.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-143">This type of calculation is usually related to a rebate.</span></span>

### <a name="set-up-vendor-groups"></a><span data-ttu-id="b9bbb-144">Uppsetning lánardrottnaflokka</span><span class="sxs-lookup"><span data-stu-id="b9bbb-144">Set up vendor groups</span></span>

<span data-ttu-id="b9bbb-145">Til að vinna með lánardrottnaflokk fyrir stjórnun eftirágreidds afsláttar skal fara í **Stjórnun eftirágreidds afsláttar \> Uppsetning hóps fyrir stjórnun eftirágreidds afsláttar \> Lánardrottnaflokkar**.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-145">To work with Rebate management vendor groups, go to **Rebate management \> Rebate management groups setup \> Vendor groups**.</span></span> <span data-ttu-id="b9bbb-146">Hægt er að nota hnappana í aðgerðarúðunni til að bæta við eða fjarlægja hópa eins og þörf er á.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-146">You can use the buttons on the Action Pane to add and remove groups as required.</span></span> <span data-ttu-id="b9bbb-147">Fyrir hvern hóp skal stilla eftirfarandi reiti:</span><span class="sxs-lookup"><span data-stu-id="b9bbb-147">For each group, set the following fields:</span></span>

- <span data-ttu-id="b9bbb-148">**Hópur fyrir stjórnun eftirágreidds afsláttar** – Sláið inn einkvæmt heiti fyrir hópinn.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-148">**Rebate management group** – Enter a unique name for the group.</span></span>
- <span data-ttu-id="b9bbb-149">**Lýsing** – Sláið inn lýsingu hópsins til að veita frekari upplýsingar um hvernig á að setja hann upp.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-149">**Description** – Enter a description of the group to provide more information about how it should be used.</span></span>

### <a name="manage-vendor-group-assignments"></a><span data-ttu-id="b9bbb-150">Stjórna úthlutunum lánardrottnaflokka</span><span class="sxs-lookup"><span data-stu-id="b9bbb-150">Manage vendor group assignments</span></span>

<span data-ttu-id="b9bbb-151">Hver lánardrottinn getur tilheyrt fjölda hópa í stjórnun eftirágreidds afsláttar.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-151">Each vendor can belong to any number of Rebate management groups.</span></span> <span data-ttu-id="b9bbb-152">Til að skoða og úthluta hópmeðlimum er hægt að byrja á hópalistanum eða lánardrottnalistanum.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-152">To view and assign group members, you can start from either the group list or the vendor list.</span></span>

<span data-ttu-id="b9bbb-153">Til að skoða, bæta við eða fjarlægja lánardrottna fyrir valinn hóp skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-153">To view, add, or remove vendors for a selected group, follow these steps.</span></span>

1. <span data-ttu-id="b9bbb-154">Farið í **Stjórnun eftirágreidds afsláttar \> Uppsetning hóps fyrir stjórnun eftirágreidds afsláttar \> Lánardrottnaflokkar**.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-154">Go to **Rebate management \> Rebate management groups setup \> Vendor groups**.</span></span>
1. <span data-ttu-id="b9bbb-155">Veljið hópinn sem á að stjórna.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-155">Select the group to manage.</span></span>
1. <span data-ttu-id="b9bbb-156">Á aðgerðasvæðinu velurðu **Lánardrottnar**.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-156">On the Action Pane, select **Vendors**.</span></span> <span data-ttu-id="b9bbb-157">Síðan **Hópar fyrir stjórnun eftirágreidds afsláttar** birtist og sýnir lista yfir lánardrottna sem eru þegar meðlimir í völdum hópi.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-157">The **Rebate management groups** page appears and shows a list of vendors that are already members of the selected group.</span></span>
1. <span data-ttu-id="b9bbb-158">Til að bæta nýjum lánardrottni við hópinn skal velja **Nýr** á aðgerðasvæðinu til að bæta línu við hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-158">To add a new vendor to the group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="b9bbb-159">Stillið svo eftirfarandi reit fyrir nýju línuna:</span><span class="sxs-lookup"><span data-stu-id="b9bbb-159">Then set the following field for the new row:</span></span>

    - <span data-ttu-id="b9bbb-160">**Lánardrottnalykill** – Veljið kenni lánardrottnalykils.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-160">**Vendor account** – Select the vendor account ID.</span></span>

1. <span data-ttu-id="b9bbb-161">Til að fjarlægja lánardrottin úr hópnum skal velja lánardrottin og velja svo **Eyða** á aðgerðasvæðinu.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-161">To remove a vendor from the group, select the vendor, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="b9bbb-162">Til að skoða, bæta við eða fjarlægja hópverkefni fyrir valinn lánardrottinn skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-162">To view, add, or remove group assignments for a selected vendor, follow these steps.</span></span>

1. <span data-ttu-id="b9bbb-163">Farið í **Viðskiptaskuldir \> Lánardrottnar \> Allir lánardrottnar**.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-163">Go to **Accounts payable \> Vendors \> All vendors**.</span></span>
1. <span data-ttu-id="b9bbb-164">Veljið lánardrottin til að vinna með.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-164">Select the vendor to work with.</span></span>
1. <span data-ttu-id="b9bbb-165">Á aðgerðasvæðinu, í flipanum **Lánardrottinn**, í flokknum **Stjórnun eftirágreidds afsláttar**, skal velja **Hópar fyrir stjórnun eftirágreidds afsláttar**.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-165">On the Action Pane, on the **Vendor** tab, in the **Rebate management** group, select **Rebate management groups**.</span></span> <span data-ttu-id="b9bbb-166">Síðan **Hópar fyrir stjórnun eftirágreidds afsláttar** birtist og sýnir lista yfir hópa sem valinn lánardrottinn tilheyrir.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-166">The **Rebate management groups** page appears and shows a list of groups that the selected vendor already belongs to.</span></span>
1. <span data-ttu-id="b9bbb-167">Til að bæta lánardrottni við hópinn skal velja **Nýr** á aðgerðasvæðinu til að bæta línu við hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-167">To add the vendor to a new group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="b9bbb-168">Stillið svo eftirfarandi reit fyrir nýju línuna:</span><span class="sxs-lookup"><span data-stu-id="b9bbb-168">Then set the following field for the new row:</span></span>

    - <span data-ttu-id="b9bbb-169">**Hópur fyrir stjórnun eftirágreidds afsláttar** – Veljið hópinn til að bæta lánardrottni við hann.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-169">**Rebate management group** – Select the group to add the vendor to.</span></span>

1. <span data-ttu-id="b9bbb-170">Til að fjarlægja lánardrottin úr hópi skal velja hópinn og velja síðan **Eyða** á aðgerðasvæðinu.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-170">To remove a vendor from a group, select the group, and then select **Delete** on the Action Pane.</span></span>

## <a name="item-rebate-groups"></a><span data-ttu-id="b9bbb-171">Flokkar atriða eftirágreidds afsláttar</span><span class="sxs-lookup"><span data-stu-id="b9bbb-171">Item rebate groups</span></span>

<span data-ttu-id="b9bbb-172">Með því að flokka vörur eykst sveigjanleiki þegar eftirágreiddur afsláttur og lækkanir eru reiknaðar út.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-172">By grouping items, you have more flexibility when rebates and deductions are calculated.</span></span> <span data-ttu-id="b9bbb-173">Þessi nálgun er oft hagkvæmari leið til að setja upp eftirágreiddan afslátt og lækkanir fyrir viðskiptavini og lánardrottna.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-173">This approach is often a more efficient way to set up rebates and deductions for customers and vendors.</span></span>

### <a name="set-up-item-groups"></a><span data-ttu-id="b9bbb-174">Setja upp vöruflokka</span><span class="sxs-lookup"><span data-stu-id="b9bbb-174">Set up item groups</span></span>

<span data-ttu-id="b9bbb-175">Til að vinna með vöruflokka fyrir stjórnun eftirágreidds afsláttar skal fara í **Stjórnun eftirágreidds afsláttar \> Uppsetning hóps fyrir stjórnun eftirágreidds afsláttar \> Vöruflokkar**.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-175">To work with Rebate management item groups, go to **Rebate management \> Rebate management groups setup \> Item groups**.</span></span> <span data-ttu-id="b9bbb-176">Hægt er að nota hnappana í aðgerðarúðunni til að bæta við eða fjarlægja hópa eins og þörf er á.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-176">You can use the buttons on the Action Pane to add and remove groups as required.</span></span> <span data-ttu-id="b9bbb-177">Fyrir hvern hóp skal stilla eftirfarandi reiti:</span><span class="sxs-lookup"><span data-stu-id="b9bbb-177">For each group, set the following fields:</span></span>

- <span data-ttu-id="b9bbb-178">**Hópur fyrir stjórnun eftirágreidds afsláttar** – Sláið inn einkvæmt heiti fyrir hópinn.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-178">**Rebate management group** – Enter a unique name for the group.</span></span>
- <span data-ttu-id="b9bbb-179">**Lýsing** – Sláið inn lýsingu hópsins til að veita frekari upplýsingar um hvernig á að setja hann upp.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-179">**Description** – Enter a description of the group to provide more information about how it should be used.</span></span>

### <a name="manage-item-group-assignments"></a><span data-ttu-id="b9bbb-180">Stjórna úthlutunum vöruflokks</span><span class="sxs-lookup"><span data-stu-id="b9bbb-180">Manage item group assignments</span></span>

<span data-ttu-id="b9bbb-181">Hver vara getur tilheyrt fjölda hópa í stjórnun eftirágreidds afsláttar.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-181">Each item can belong to any number of Rebate management groups.</span></span> <span data-ttu-id="b9bbb-182">Til að skoða og úthluta hópmeðlimum er hægt að byrja á hópalistanum eða vörulistanum.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-182">To view and assign group members, you can start from either the group list or the item list.</span></span> <span data-ttu-id="b9bbb-183">Einnig er hægt að bæta við vörum samkvæmt tegundastigveldinu.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-183">You can also add items based on your category hierarchy.</span></span>

<span data-ttu-id="b9bbb-184">Til að skoða, bæta við eða fjarlægja vörur fyrir valinn hóp skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-184">To view, add, or remove items for a selected group, follow these steps.</span></span>

1. <span data-ttu-id="b9bbb-185">Farið í **Stjórnun eftirágreidds afsláttar \> Uppsetning hóps fyrir stjórnun eftirágreidds afsláttar \> Vöruflokkar**.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-185">Go to **Rebate management \> Rebate management groups setup \> Item groups**.</span></span>
1. <span data-ttu-id="b9bbb-186">Veljið hópinn sem á að stjórna.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-186">Select the group to manage.</span></span>
1. <span data-ttu-id="b9bbb-187">Á aðgerðasvæðinu skal velja **Vörur**.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-187">On the Action Pane, select **Items**.</span></span> <span data-ttu-id="b9bbb-188">Síðan **Hópar fyrir stjórnun eftirágreidds afsláttar** birtist og sýnir lista yfir vörur sem eru þegar meðlimir í völdum hópi.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-188">The **Rebate management groups** page appears and shows a list of items that are already members of the selected group.</span></span>
1. <span data-ttu-id="b9bbb-189">Til að bæta nýrri vöru við hópinn skal velja **Ný** á aðgerðasvæðinu til að bæta línu við hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-189">To add a new item to the group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="b9bbb-190">Stillið svo eftirfarandi reit fyrir nýju línuna:</span><span class="sxs-lookup"><span data-stu-id="b9bbb-190">Then set the following field for the new row:</span></span>

    - <span data-ttu-id="b9bbb-191">**Vörureikningur** – Veljið kenni vörureiknings.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-191">**Item account** – Select the item account ID.</span></span>

1. <span data-ttu-id="b9bbb-192">Til að fjarlægja vöru úr hópi skal velja vöruna og velja **Eyða** á aðgerðasvæðinu.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-192">To remove an item from the group, select the item, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="b9bbb-193">Til að skoða, bæta við eða fjarlægja hópverkefni fyrir valda vöru skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-193">To view, add, or remove group assignments for a selected item, follow these steps.</span></span>

1. <span data-ttu-id="b9bbb-194">Opna **Afurðaupplýsingastjórnun \> Afurðir \> Útgefnar afurðir**.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-194">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="b9bbb-195">Veljið vöruna til að vinna með.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-195">Select the item to work with.</span></span>
1. <span data-ttu-id="b9bbb-196">Á aðgerðasvæðinu, í flipanum **Afurð**, í flokknum **Stjórnun eftirágreidds afsláttar**, skal velja **Hópar fyrir stjórnun eftirágreidds afsláttar**.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-196">On the Action Pane, on the **Product** tab, in the **Rebate management** group, select **Rebate management groups**.</span></span> <span data-ttu-id="b9bbb-197">Síðan **Hópar fyrir stjórnun eftirágreidds afsláttar** birtist og sýnir lista yfir hópa sem valin vara tilheyrir.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-197">The **Rebate management groups** page appears and shows a list of groups that the selected item already belongs to.</span></span>
1. <span data-ttu-id="b9bbb-198">Til að bæta vöru við hópinn skal velja **Ný** á aðgerðasvæðinu til að bæta línu við hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-198">To add the item to a new group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="b9bbb-199">Stillið svo eftirfarandi reit fyrir nýju línuna:</span><span class="sxs-lookup"><span data-stu-id="b9bbb-199">Then set the following field for the new row:</span></span>

    - <span data-ttu-id="b9bbb-200">**Hópur fyrir stjórnun eftirágreidds afsláttar** – Veljið hópinn til að bæta vöru við hann.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-200">**Rebate management group** – Select the group to add the item to.</span></span>

1. <span data-ttu-id="b9bbb-201">Til að fjarlægja vöru úr hópi skal velja hópinn og velja **Eyða** á aðgerðasvæðinu.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-201">To remove an item from a group, select the group, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="b9bbb-202">Til að bæta vörum við hóp samkvæmt tegundastigveldinu skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-202">To add items to a group based on your category hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="b9bbb-203">Farið í **Stjórnun eftirágreidds afsláttar \> Uppsetning hóps fyrir stjórnun eftirágreidds afsláttar \> Vöruflokkar**.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-203">Go to **Rebate management \> Rebate management groups setup \> Item groups**.</span></span>
1. <span data-ttu-id="b9bbb-204">Veljið hópinn sem á að stjórna.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-204">Select the group to manage.</span></span>
1. <span data-ttu-id="b9bbb-205">Á aðgerðasvæðinu skal velja **Bæta við vörum**.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-205">On the Action Pane, select **Add items**.</span></span>
1. <span data-ttu-id="b9bbb-206">Í svarglugganum **Bæta við vörum**, í reitnum **Tegundastigveldi**, skal velja hóp á hæsta stigi.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-206">In the **Add items** dialog box, in the **Category hierarchy** field, select a top-level category.</span></span>
1. <span data-ttu-id="b9bbb-207">Stigveldi vöru er opnað á svæðinu til vinstri.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-207">The item hierarchy is opened in the left pane.</span></span> <span data-ttu-id="b9bbb-208">Veldu stigveldi sem þú ert að leita að.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-208">Select the hierarchy level that you're looking for.</span></span> 
1. <span data-ttu-id="b9bbb-209">Vörur úr völdu stigveldi og stig stigveldis er nú sýnt á svæðinu til hægri.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-209">Items from the selected hierarchy and hierarchy level are now listed in the right pane.</span></span> <span data-ttu-id="b9bbb-210">Fylgið þessum skrefum til að vinna með svæðið:</span><span class="sxs-lookup"><span data-stu-id="b9bbb-210">Follow these steps to work with the pane:</span></span>

    - <span data-ttu-id="b9bbb-211">Veljið gátreitinn fyrir hverja vöru sem á að bæta við.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-211">Select the check box for each item that you want to add.</span></span>
    - <span data-ttu-id="b9bbb-212">Veljið gátreitinn í haus hnitanetsins til að velja allar vörurnar sem eru sýndar.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-212">Select the check box on the grid header to select all the items that are listed.</span></span>
    - <span data-ttu-id="b9bbb-213">Veljið hnappinn **Sýna valið** til að sía hnitanetið þannig að það sýni aðeins vörurnar sem hafa verið valdar fram að þessu.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-213">Select the **Show selected** button to filter the grid so that it shows only the items that you've selected so far.</span></span> <span data-ttu-id="b9bbb-214">Veljið hnappinn aftur til að fara aftur í heildarlistann.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-214">Select the button again to return to the full list.</span></span>

1. <span data-ttu-id="b9bbb-215">Veljið **Í lagi** til að færa vöruvalið yfir í valinn hóp.</span><span class="sxs-lookup"><span data-stu-id="b9bbb-215">Select **OK** to apply your item selection to the selected group.</span></span>
