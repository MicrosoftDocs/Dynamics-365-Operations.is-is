---
title: Stofna og meðhöndla ósamkvæmi
description: Þetta efnisatriði lýsir því hvernig á að nota framkvæma stjórnun ósamkvæmis, samkvæmt fyrirliggjandi gæðapöntun.
author: perlynne
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 06a56a694f7a80d65cb46d08744e78d8361cee3b
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956207"
---
# <a name="create-and-process-nonconformances"></a><span data-ttu-id="da872-103">Stofna og meðhöndla ósamkvæmi</span><span class="sxs-lookup"><span data-stu-id="da872-103">Create and process nonconformances</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="da872-104">Þetta efnisatriði lýsir því hvernig á að nota framkvæma stjórnun ósamkvæmis, samkvæmt fyrirliggjandi gæðapöntun.</span><span class="sxs-lookup"><span data-stu-id="da872-104">This topic describes how to perform nonconformance management based on an existing quality order.</span></span> <span data-ttu-id="da872-105">Yfirleitt er stjórnun ósamkvæmi framkvæmd af eftirlitsaðila.</span><span class="sxs-lookup"><span data-stu-id="da872-105">Typically, nonconformance management is done by a quality clerk.</span></span> <span data-ttu-id="da872-106">Þess er krafist að hægt sé að panta gæðapöntun.</span><span class="sxs-lookup"><span data-stu-id="da872-106">As a prerequisite, you must have a quality order available.</span></span> <span data-ttu-id="da872-107">(Nánari upplýsingar um hvernig á að stofna gæðapöntun eru í [Skoða gæði vara](inspect-quality-goods.md).)</span><span class="sxs-lookup"><span data-stu-id="da872-107">(For information about how to create a quality order, see [Inspect the quality of goods](inspect-quality-goods.md).)</span></span>

<span data-ttu-id="da872-108">Áður en notandi getur unnið úr samþykki ósamkvæmis verður að úthluta honum starfsmanni í reitnum **Einstaklingur** á síðunni **Notendur**.</span><span class="sxs-lookup"><span data-stu-id="da872-108">Before a user can process the approval of a nonconformance, a worker must be assigned to them in the **Person** field on the **Users** page.</span></span> <span data-ttu-id="da872-109">Auk þess, áður en notandinn getur notað athugasemdir skjalsins, verður að stilla valkostinn **Virkja skjalastjórnun** á *Já* í valkostum notanda.</span><span class="sxs-lookup"><span data-stu-id="da872-109">Additionally, before the user can use the document notes, the **Enable document handling** option must be set to *Yes* in their user options.</span></span>

## <a name="create-a-nonconformance"></a><span data-ttu-id="da872-110">Stofna ósamkvæmistilvik</span><span class="sxs-lookup"><span data-stu-id="da872-110">Create a nonconformance</span></span>

<span data-ttu-id="da872-111">Til að búa til ósamkvæmi skal fylgja eftirfarandi skrefum.</span><span class="sxs-lookup"><span data-stu-id="da872-111">To create a nonconformance, follow these steps.</span></span>

1. <span data-ttu-id="da872-112">Farðu í **Birgðastjórnun \> Reglubundin verk \> Gæðastjórnun \> Ósamkvæmnistilvik**.</span><span class="sxs-lookup"><span data-stu-id="da872-112">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="da872-113">Í aðgerðarúðunni velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="da872-113">On the Action pane, select **New**.</span></span>
1. <span data-ttu-id="da872-114">Í svarglugganum **Búa til ósamkvæmni**, í reitnum **Gerð vandamáls**, skal velja gerð vandamálsins sem var fundið í skoðunarferlinu.</span><span class="sxs-lookup"><span data-stu-id="da872-114">In the **Create non conformance** dialog box, in **Problem type** field, select the type of problem that was found during the inspection process.</span></span>
1. <span data-ttu-id="da872-115">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="da872-115">Select **OK**.</span></span>

## <a name="approve-or-reject-a-nonconformance"></a><span data-ttu-id="da872-116">Samþykkja eða hafna ósamkvæmistilviki</span><span class="sxs-lookup"><span data-stu-id="da872-116">Approve or reject a nonconformance</span></span>

<span data-ttu-id="da872-117">Fylgið eftirfarandi skrefum til að samþykkja eða hafna ósamkvæmi.</span><span class="sxs-lookup"><span data-stu-id="da872-117">To approve or reject a nonconformance, follow these steps.</span></span>

1. <span data-ttu-id="da872-118">Farðu í **Birgðastjórnun \> Reglubundin verk \> Gæðastjórnun \> Ósamkvæmnistilvik**.</span><span class="sxs-lookup"><span data-stu-id="da872-118">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="da872-119">Á listanum skal velja það ósamkvæmi sem á að uppfæra.</span><span class="sxs-lookup"><span data-stu-id="da872-119">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="da872-120">Einungis er hægt að bæta leiðréttingu við ósamkvæmi sem er samþykkt.</span><span class="sxs-lookup"><span data-stu-id="da872-120">You can add a correction only to nonconformances that are approved.</span></span>

1. <span data-ttu-id="da872-121">Á aðgerðarsvæðinu skal velja **Aðgerðir \> Samþykkja ósamkvæmni** til að samþykkja ósamkvæmnina eða **Aðgerðir \> Hafna ósamkvæmni** til að hafna henni.</span><span class="sxs-lookup"><span data-stu-id="da872-121">On the Action Pane, select **Functions \> Approve non conformance** to approve the nonconformance or **Functions \> Refuse non conformance** to reject it.</span></span> <span data-ttu-id="da872-122">Hægt er að tengja samþykkt ósamkvæmi við [tengdar aðgerðir](../quality-operations.md).</span><span class="sxs-lookup"><span data-stu-id="da872-122">You can associate approved nonconformances with [related operations](../quality-operations.md).</span></span> <span data-ttu-id="da872-123">Á þennan hátt er hægt að skrá vinnu sem er gerð sem hluti af meðhöndlun ósamkvæmi og úrvinnslu leiðréttingarmeðhöndlunar.</span><span class="sxs-lookup"><span data-stu-id="da872-123">In this way, you can record work that is done as part of the nonconformance handling and the processing of correction handling.</span></span>
1. <span data-ttu-id="da872-124">Beðið er um staðfestingu á valinu.</span><span class="sxs-lookup"><span data-stu-id="da872-124">You're prompted to confirm your selection.</span></span> <span data-ttu-id="da872-125">Veldu **Já** til að halda áfram.</span><span class="sxs-lookup"><span data-stu-id="da872-125">Select **Yes** to continue.</span></span>

## <a name="add-operations-and-other-details-to-nonconformances"></a><span data-ttu-id="da872-126">Bættu við aðgerðum og öðrum upplýsingum um ósamkvæmi</span><span class="sxs-lookup"><span data-stu-id="da872-126">Add operations and other details to nonconformances</span></span>

<span data-ttu-id="da872-127">Þegar ósamkvæmi hefur verið stofnuð er hægt að byrja að bæta við tengdum aðgerðum og tilgreina viðbótarupplýsingar fyrir þær aðgerðir.</span><span class="sxs-lookup"><span data-stu-id="da872-127">After you've created a nonconformance, you can start to add related operations and specify additional information about those operations.</span></span> <span data-ttu-id="da872-128">Þú getur aðeins bætt tengdum aðgerðum við ósamkvæmi sem er samþykkt.</span><span class="sxs-lookup"><span data-stu-id="da872-128">You can add related operations only to nonconformances that are approved.</span></span>

<span data-ttu-id="da872-129">Auk grunnupplýsinganna er hægt að bæta eftirfarandi upplýsingum við aðgerð:</span><span class="sxs-lookup"><span data-stu-id="da872-129">Besides the basic information, you can add the following details to an operation:</span></span>

- <span data-ttu-id="da872-130">**Vörur** – Hægt er að búa til lista yfir vörur sem eru notaðar til að framkvæma leiðréttinguna.</span><span class="sxs-lookup"><span data-stu-id="da872-130">**Items** – You can create a list of items that are consumed to perform the correction.</span></span> <span data-ttu-id="da872-131">Til dæmis gætu vörurnar verið vörur sem eru nauðsynlegar til viðgerðar á búnaði eða innihaldsefnum sem þarf til að endurvinna tilbúna afurð.</span><span class="sxs-lookup"><span data-stu-id="da872-131">For example, the items might be products that are required to repair equipment or ingredients that are required to rework a finished product.</span></span>
- <span data-ttu-id="da872-132">**Gæðagjöld** – Hægt er að stofna lista af gjöldum sem myndast eða eru reikningsfærð til ytri aðila.</span><span class="sxs-lookup"><span data-stu-id="da872-132">**Quality charges** – You can create a list of charges that are incurred or billed out to external sources.</span></span>
- <span data-ttu-id="da872-133">**Vinnukort** – Hægt er að búa til kladda yfir þann tíma sem hver starfsmaður eyðir í aðgerðina.</span><span class="sxs-lookup"><span data-stu-id="da872-133">**Timesheet** – You can create a log of the time that each worker spends on the operation.</span></span>

<span data-ttu-id="da872-134">Aðrar stillingar eru valfrjálsar.</span><span class="sxs-lookup"><span data-stu-id="da872-134">The remaining settings are optional.</span></span> <span data-ttu-id="da872-135">Kostnaður fyrir hverja vöru, gæðagjöld og vinnukortið er tekið saman og sýnt á aðgerðinni.</span><span class="sxs-lookup"><span data-stu-id="da872-135">The cost for each item, quality charges, and the timesheet are summed and shown on the operation.</span></span> <span data-ttu-id="da872-136">Þú getur ekki breytt reitnum **Kostnaður** beint í aðgerðinni.</span><span class="sxs-lookup"><span data-stu-id="da872-136">You can't directly edit the **Cost** field on the operation.</span></span>

### <a name="create-an-operation-for-a-nonconformance"></a><span data-ttu-id="da872-137">Búa til aðgerð fyrir ósamkvæmni</span><span class="sxs-lookup"><span data-stu-id="da872-137">Create an operation for a nonconformance</span></span>

<span data-ttu-id="da872-138">Fylgja skal eftirfarandi skrefum til að búa til aðgerð vegna ósamkvæmi.</span><span class="sxs-lookup"><span data-stu-id="da872-138">To create an operation for a nonconformance, follow these steps.</span></span>

1. <span data-ttu-id="da872-139">Farðu í **Birgðastjórnun \> Reglubundin verk \> Gæðastjórnun \> Ósamkvæmnistilvik**.</span><span class="sxs-lookup"><span data-stu-id="da872-139">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="da872-140">Á listanum skal velja það ósamkvæmi sem á að uppfæra.</span><span class="sxs-lookup"><span data-stu-id="da872-140">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="da872-141">Aðeins er hpægt að bæta við eða uppfæra aðgerðir fyrir ósamræmi sem eru samþykkt.</span><span class="sxs-lookup"><span data-stu-id="da872-141">You can add or update operations only for nonconformances that are approved.</span></span>

1. <span data-ttu-id="da872-142">Á aðgerðasvæðinu skal velja **Tengdar aðgerðir**.</span><span class="sxs-lookup"><span data-stu-id="da872-142">On the Action Pane, select **Related operations**.</span></span>
1. <span data-ttu-id="da872-143">Á síðunni **Tengdar aðgerðir**, á aðgerðasvæðinu, skal velja **Ný** til að bæta nýrri línu við hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="da872-143">On the **Related operations** page, on the Action pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="da872-144">Stillið svo eftirfarandi reiti fyrir nýju línuna:</span><span class="sxs-lookup"><span data-stu-id="da872-144">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="da872-145">**Aðgerð** – Veldu kóða aðgerðarinnar sem verður framkvæmd vegna ósamkvæminnar.</span><span class="sxs-lookup"><span data-stu-id="da872-145">**Operation** – Select the code of the operation that will be performed for the nonconformance.</span></span>
    - <span data-ttu-id="da872-146">**Ástæða** – Færið inn ítarlega lýsingu sem skýrir hvers vegna aðgerð er nauðsynleg.</span><span class="sxs-lookup"><span data-stu-id="da872-146">**Reason** – Enter a detailed description that explains why the operation is required.</span></span>
    - <span data-ttu-id="da872-147">**Sölupöntun** – Ef valinn aðgerðarkóði tengist gerð sölupöntunar skal velja sölupöntunina sem aðgerðin er tengd við.</span><span class="sxs-lookup"><span data-stu-id="da872-147">**Sales order** – If the selected operation code is related to the sales order type, select the sales order that you're linking the operation to.</span></span>
    - <span data-ttu-id="da872-148">**Innkaupapöntun** – Ef valinn aðgerðarkóði tengist gerð innkaupapöntunar skal velja innkaupapöntunina sem tengja á við aðgerðina.</span><span class="sxs-lookup"><span data-stu-id="da872-148">**Purchase order** – If the selected operation code is related to the purchase order type, select the purchase order that you're linking the operation to.</span></span>

1. <span data-ttu-id="da872-149">Lokaðu síðunum.</span><span class="sxs-lookup"><span data-stu-id="da872-149">Close the pages.</span></span>

### <a name="add-items-to-an-operation"></a><span data-ttu-id="da872-150">Bæta vörum við aðgerð</span><span class="sxs-lookup"><span data-stu-id="da872-150">Add items to an operation</span></span>

<span data-ttu-id="da872-151">Fylgja skal eftirfarandi skrefum til að bæta atriðum við aðgerð.</span><span class="sxs-lookup"><span data-stu-id="da872-151">To add items to an operation, follow these steps.</span></span>

1. <span data-ttu-id="da872-152">Farðu í **Birgðastjórnun \> Reglubundin verk \> Gæðastjórnun \> Ósamkvæmnistilvik**.</span><span class="sxs-lookup"><span data-stu-id="da872-152">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="da872-153">Á listanum skal velja það ósamkvæmi sem á að uppfæra.</span><span class="sxs-lookup"><span data-stu-id="da872-153">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="da872-154">Aðeins er hpægt að bæta við eða uppfæra aðgerðir fyrir ósamræmi sem eru samþykkt.</span><span class="sxs-lookup"><span data-stu-id="da872-154">You can add or update operations only for nonconformances that are approved.</span></span>

1. <span data-ttu-id="da872-155">Á aðgerðasvæðinu skal velja **Tengdar aðgerðir**.</span><span class="sxs-lookup"><span data-stu-id="da872-155">On the Action Pane, select **Related operations**.</span></span>
1. <span data-ttu-id="da872-156">Á síðunni **Tengdar aðgerðir** er valin aðgerðin sem bæta á vörum við.</span><span class="sxs-lookup"><span data-stu-id="da872-156">On the **Related operations** page, select the operation that you want to add items to.</span></span>
1. <span data-ttu-id="da872-157">Á aðgerðasvæðinu skal velja **Vörur**.</span><span class="sxs-lookup"><span data-stu-id="da872-157">On the Action Pane, select **Items**.</span></span>
1. <span data-ttu-id="da872-158">Á síðunni **Tengdar aðgerðir**, á aðgerðasvæðinu, skal velja **Ný** til að bæta nýrri línu við hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="da872-158">On the **Related operations** page, on the Action pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="da872-159">Stillið síðan eftirtalin svæði fyrir nýja röð:</span><span class="sxs-lookup"><span data-stu-id="da872-159">Then set the following fields for new row:</span></span>

    - <span data-ttu-id="da872-160">**Vörunúmer** – Veldu vöruna sem verður notuð sem hluti af völdu aðgerðinni.</span><span class="sxs-lookup"><span data-stu-id="da872-160">**Item number** – Select the product that will be consumed as part of the selected operation.</span></span>
    - <span data-ttu-id="da872-161">**Magn** – Færið inn fjölda vara sem verða notaðar.</span><span class="sxs-lookup"><span data-stu-id="da872-161">**Quantity** – Enter the number of items that will be consumed.</span></span>

    > [!NOTE]
    > <span data-ttu-id="da872-162">Hægt er að skoða kostnað á vörunni í reitnum **Kostnaður** í flipanum **Almennt**. Kostnaðurinn sem er sýndur þar kemur frá kostnaðinum sem er settur upp á síðunni **Útgefin afurð**.</span><span class="sxs-lookup"><span data-stu-id="da872-162">You can view the cost for the item in the **Cost** field on the **General** tab. The cost that is shown there comes from the cost that is set up on the **Released product** page.</span></span> <span data-ttu-id="da872-163">Ekki er hægt að uppfæra kostnaðinn beint á síðuna **Tengdar aðgerðir**.</span><span class="sxs-lookup"><span data-stu-id="da872-163">The cost can't be updated directly on the **Related operation item** page.</span></span> <span data-ttu-id="da872-164">Kostnaður á öllum vörum sem bætt er við síðuna **Vörur tengdrar aðgerðar** er sjálfkrafa bætt við reitinn **Kostnaður** á síðunni **Tengdar aðgerðir**.</span><span class="sxs-lookup"><span data-stu-id="da872-164">The cost of all items that are added on the **Related operation items** page is automatically added to the **Cost** field on the **Related operations** page.</span></span>

1. <span data-ttu-id="da872-165">Endurtaka skal fyrri skref fyrir hvern viðbótarhlut sem þú verður að bæta við.</span><span class="sxs-lookup"><span data-stu-id="da872-165">Repeat the previous step for each additional item that you must add.</span></span>
1. <span data-ttu-id="da872-166">Lokaðu síðunum.</span><span class="sxs-lookup"><span data-stu-id="da872-166">Close the pages.</span></span>

### <a name="add-quality-charges-to-an-operation"></a><span data-ttu-id="da872-167">Bæta gæðagjöldum við aðgerð</span><span class="sxs-lookup"><span data-stu-id="da872-167">Add quality charges to an operation</span></span>

<span data-ttu-id="da872-168">Fylgja skal eftirfarandi skrefum til að bæta gæðagjöldum við aðgerð.</span><span class="sxs-lookup"><span data-stu-id="da872-168">To add quality charges to an operation, follow these steps.</span></span>

1. <span data-ttu-id="da872-169">Farðu í **Birgðastjórnun \> Reglubundin verk \> Gæðastjórnun \> Ósamkvæmnistilvik**.</span><span class="sxs-lookup"><span data-stu-id="da872-169">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="da872-170">Á listanum skal velja það ósamkvæmi sem á að uppfæra.</span><span class="sxs-lookup"><span data-stu-id="da872-170">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="da872-171">Aðeins er hpægt að bæta við eða uppfæra aðgerðir fyrir ósamræmi sem eru samþykkt.</span><span class="sxs-lookup"><span data-stu-id="da872-171">You can add or update operations only for nonconformances that are approved.</span></span>

1. <span data-ttu-id="da872-172">Á aðgerðasvæðinu skal velja **Tengdar aðgerðir**.</span><span class="sxs-lookup"><span data-stu-id="da872-172">On the Action Pane, select **Related operations**.</span></span>
1. <span data-ttu-id="da872-173">Á síðunni **Tengdar aðgerðir** er valin aðgerðin sem bæta á gæðagjöldum við.</span><span class="sxs-lookup"><span data-stu-id="da872-173">On the **Related operations** page, select the operation that you want to add quality charges to.</span></span>
1. <span data-ttu-id="da872-174">Á aðgerðasvæðinu skal velja **Gæðagjöld**.</span><span class="sxs-lookup"><span data-stu-id="da872-174">On the Action Pane, select **Quality charges**.</span></span>
1. <span data-ttu-id="da872-175">Á síðunni **Gjöld tengdrar aðgerðar**, á aðgerðasvæðinu, skal velja **Ný** til að bæta línu við hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="da872-175">On the **Related operation charges** page, on the Action pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="da872-176">Stillið svo eftirfarandi reiti fyrir nýju línuna:</span><span class="sxs-lookup"><span data-stu-id="da872-176">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="da872-177">**Gjaldakóði** – Veljið gæðagjaldið sem bæta á við.</span><span class="sxs-lookup"><span data-stu-id="da872-177">**Charges code** – Select the quality charge that you want to add.</span></span>
    - <span data-ttu-id="da872-178">**Lýsing** – Færið inn ítarlega lýsingu á gjaldinu.</span><span class="sxs-lookup"><span data-stu-id="da872-178">**Description** – Enter a detailed description of the charge.</span></span>
    - <span data-ttu-id="da872-179">**Gildi gjalda** – Færið inn upphæð gjaldsins.</span><span class="sxs-lookup"><span data-stu-id="da872-179">**Charges value** – Enter the amount of the charge.</span></span>

1. <span data-ttu-id="da872-180">Endurtaka skal fyrri skref fyrir hver viðbótargjöld sem þú þarft að bæta við.</span><span class="sxs-lookup"><span data-stu-id="da872-180">Repeat the previous step for each additional charge that you must add.</span></span>
1. <span data-ttu-id="da872-181">Lokaðu síðunum.</span><span class="sxs-lookup"><span data-stu-id="da872-181">Close the pages.</span></span>

> [!NOTE]
> <span data-ttu-id="da872-182">Upphæðin í reitnum **Gildi gjalds** er sjálfkrafa tekin saman fyrir öll gæðagjöld og bætt við allar aðrar upphæðir í reitnum **Kostnaður** á síðunni **Tengdar aðgerðir**.</span><span class="sxs-lookup"><span data-stu-id="da872-182">The amount in the **Charges value** field is automatically summed for all quality charges and added to any other amounts in the **Cost** field on the **Related operations** page.</span></span>

### <a name="create-a-timesheet-on-an-operation"></a><span data-ttu-id="da872-183">Búa til vinnukort á aðgerð</span><span class="sxs-lookup"><span data-stu-id="da872-183">Create a timesheet on an operation</span></span>

<span data-ttu-id="da872-184">Fylgja skal eftirfarandi skrefum til að bæta vinnukorti við aðgerð.</span><span class="sxs-lookup"><span data-stu-id="da872-184">To add a timesheet to an operation, follow these steps.</span></span>

1. <span data-ttu-id="da872-185">Farðu í **Birgðastjórnun \> Reglubundin verk \> Gæðastjórnun \> Ósamkvæmnistilvik**.</span><span class="sxs-lookup"><span data-stu-id="da872-185">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="da872-186">Á listanum skal velja það ósamkvæmi sem á að uppfæra.</span><span class="sxs-lookup"><span data-stu-id="da872-186">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="da872-187">Aðeins er hpægt að bæta við eða uppfæra aðgerðir fyrir ósamræmi sem eru samþykkt.</span><span class="sxs-lookup"><span data-stu-id="da872-187">You can add or update operations only for nonconformances that are approved.</span></span>

1. <span data-ttu-id="da872-188">Á aðgerðasvæðinu skal velja **Tengdar aðgerðir**.</span><span class="sxs-lookup"><span data-stu-id="da872-188">On the Action Pane, select **Related operations**.</span></span>
1. <span data-ttu-id="da872-189">Á síðunni **Tengdar aðgerðir** er valin aðgerðin sem bæta á vinnukorti við.</span><span class="sxs-lookup"><span data-stu-id="da872-189">On the **Related operations** page, select the operation that you want to add a timesheet to.</span></span>
1. <span data-ttu-id="da872-190">Á aðgerðasvæðinu skal velja **Tímablað**.</span><span class="sxs-lookup"><span data-stu-id="da872-190">On the Action Pane, select **Timesheet**.</span></span>
1. <span data-ttu-id="da872-191">Á síðunni **Vinnuskýrslur tengdrar aðgerðar**, á aðgerðasvæðinu, skal velja **Ný** til að bæta nýrri línu við hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="da872-191">On the **Related operation time sheets** page, on the Action pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="da872-192">Stillið svo eftirfarandi reiti fyrir nýju línuna:</span><span class="sxs-lookup"><span data-stu-id="da872-192">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="da872-193">**Dagsetning** – Tilgreinið dagsetninguna þegar verkið var unnið.</span><span class="sxs-lookup"><span data-stu-id="da872-193">**Date** – Specify the date when work was done.</span></span> <span data-ttu-id="da872-194">Reiturinn er sjálfgefið stilltur á núgildandi dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="da872-194">By default, this field is set to the current date.</span></span>
    - <span data-ttu-id="da872-195">**Starfskraftur** – Veljið starfskraft sem vann vinnuna.</span><span class="sxs-lookup"><span data-stu-id="da872-195">**Worker** – Select the worker who did the work.</span></span> <span data-ttu-id="da872-196">Þessi reitur er sjálfgefið stilltur á starfskraftinn sem er úthlutað á núverandi notanda.</span><span class="sxs-lookup"><span data-stu-id="da872-196">By default, this field is set to the worker that is assigned to the current user.</span></span>
    - <span data-ttu-id="da872-197">**Aðgerðartímar** – Færið inn þann fjölda klukkustunda sem voru notaðar fyrir valda aðgerð.</span><span class="sxs-lookup"><span data-stu-id="da872-197">**Operation hours** – Enter the number of hours that were worked on the selected operation.</span></span>
    - <span data-ttu-id="da872-198">**Reikningsfært** – Veljið þennan gátreit ef tíminn hefur verið skuldfærður viðskiptavin eða lánardrottinn á reikningi.</span><span class="sxs-lookup"><span data-stu-id="da872-198">**Invoiced** – Select this check box if the time has been charged to a customer or vendor on an invoice.</span></span>

    > [!NOTE]
    > <span data-ttu-id="da872-199">Hægt er að skoða kostnaðinn í reitnum **Kostnaður** í flipanum **Almennt**. Kostnaðurinn er reiknaður með því að nota taxtann sem þú skilgreinir á síðunni **Færibreytur birgðastjórnunar**.</span><span class="sxs-lookup"><span data-stu-id="da872-199">You can view the cost in the **Cost** field on the **General** tab. The cost is calculated by using the rate that you define on the **Inventory management parameters** page.</span></span>

1. <span data-ttu-id="da872-200">Endurtaka skal fyrri skref fyrir hverja vinnukortslínu til viðbótar sem þú verður að bæta við.</span><span class="sxs-lookup"><span data-stu-id="da872-200">Repeat the previous step for each additional timesheet line that you must add.</span></span>
1. <span data-ttu-id="da872-201">Lokaðu síðunum.</span><span class="sxs-lookup"><span data-stu-id="da872-201">Close the pages.</span></span>

> [!NOTE]
> <span data-ttu-id="da872-202">Upphæðin í reitnum **Kostnaður** er tekin saman fyrir allar vinnukortslínur og bætt við allar aðrar upphæðir í reitnum **Kostnaður** á síðunni **Tengdar aðgerðir**.</span><span class="sxs-lookup"><span data-stu-id="da872-202">The amount in the **Cost** field is summed for all timesheet lines and added to any other amounts in the **Cost** field on the **Related operations** page.</span></span>

## <a name="add-a-correction-to-a-nonconformance"></a><span data-ttu-id="da872-203">Bæta leiðréttingu við ósamkvæmni</span><span class="sxs-lookup"><span data-stu-id="da872-203">Add a correction to a nonconformance</span></span>

<span data-ttu-id="da872-204">Fylgja skal eftirfarandi skrefum til að bæta leiðréttingu við ósamkvæmi.</span><span class="sxs-lookup"><span data-stu-id="da872-204">To add a correction to a nonconformance, follow these steps.</span></span>

1. <span data-ttu-id="da872-205">Farðu í **Birgðastjórnun \> Reglubundin verk \> Gæðastjórnun \> Ósamkvæmnistilvik**.</span><span class="sxs-lookup"><span data-stu-id="da872-205">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="da872-206">Á listanum skal velja það ósamkvæmi sem á að uppfæra.</span><span class="sxs-lookup"><span data-stu-id="da872-206">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="da872-207">Einungis er hægt að bæta leiðréttingu við ósamkvæmi sem er samþykkt.</span><span class="sxs-lookup"><span data-stu-id="da872-207">You can add a correction only to nonconformances that are approved.</span></span>

1. <span data-ttu-id="da872-208">Á aðgerðasvæðinu skal velja **Lagfæringar**.</span><span class="sxs-lookup"><span data-stu-id="da872-208">On the Action Pane, select **Corrections**.</span></span>
1. <span data-ttu-id="da872-209">Á síðunni **Leiðréttingar**, á aðgerðasvæðinu, skal velja **Nýtt** til að bæta við röð við hnitið.</span><span class="sxs-lookup"><span data-stu-id="da872-209">On the **Corrections** page, on the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="da872-210">Stillið svo eftirfarandi reiti fyrir nýju línuna:</span><span class="sxs-lookup"><span data-stu-id="da872-210">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="da872-211">**Greining** – Veljið þá gerð greiningar sem auðkennir þá gerð leiðréttingar sem verið er að búa til.</span><span class="sxs-lookup"><span data-stu-id="da872-211">**Diagnostic** – Select the diagnostic type that identifies the type of correction that you're creating.</span></span>
    - <span data-ttu-id="da872-212">**Starfskraftur** – Veljið einstaklinginn sem er ábyrgur fyrir leiðréttingunni.</span><span class="sxs-lookup"><span data-stu-id="da872-212">**Worker** – Select the person who is responsible for the correction.</span></span>
    - <span data-ttu-id="da872-213">**Forgangur leiðréttingar** – Veljið valkost til að tilgreina hvernig forgangsraða á leiðréttingu (*Lág*, *Miðlungs* eða *Há*).</span><span class="sxs-lookup"><span data-stu-id="da872-213">**Correction priority** – Select an option to indicate how the correction should be prioritized (*Low*, *Normal*, or *High*).</span></span>
    - <span data-ttu-id="da872-214">**Umbeðin dagsetning** – Færið inn dagsetninguna þegar óskað var eftir leiðréttingu.</span><span class="sxs-lookup"><span data-stu-id="da872-214">**Requested date** – Enter the date when the corrective action was requested.</span></span>
    - <span data-ttu-id="da872-215">**Áætluð dagsetning** – Færa inn dagsetninguna þegar búist er við að leiðréttingunni verði lokið.</span><span class="sxs-lookup"><span data-stu-id="da872-215">**Planned date** – Enter the date when the correction is expected to be completed.</span></span>
    - <span data-ttu-id="da872-216">**Skammtímalausn** – Veljið þennan gátreit ef leiðréttingaraðgerðin leiðréttir einungis ósamkvæmið í stuttan tíma.</span><span class="sxs-lookup"><span data-stu-id="da872-216">**Short term solution** – Select this check box if the corrective action corrects the nonconformance only for a short time.</span></span>

1. <span data-ttu-id="da872-217">Lokaðu síðunum.</span><span class="sxs-lookup"><span data-stu-id="da872-217">Close the pages.</span></span>

## <a name="mark-a-correction-as-completed"></a><span data-ttu-id="da872-218">Merkja leiðréttingu sem lokið</span><span class="sxs-lookup"><span data-stu-id="da872-218">Mark a correction as completed</span></span>

<span data-ttu-id="da872-219">Fylgið eftirfarandi skrefum til að merkja leiðréttingu ósamkvæmi sem lokið.</span><span class="sxs-lookup"><span data-stu-id="da872-219">To mark a nonconformance correction as completed, follow these steps.</span></span>

1. <span data-ttu-id="da872-220">Farðu í **Birgðastjórnun \> Reglubundin verk \> Gæðastjórnun \> Ósamkvæmnistilvik**.</span><span class="sxs-lookup"><span data-stu-id="da872-220">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="da872-221">Á listanum skal velja það ósamkvæmi sem á að uppfæra.</span><span class="sxs-lookup"><span data-stu-id="da872-221">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="da872-222">Einungis er hægt að bæta leiðréttingu við ósamkvæmi sem er samþykkt.</span><span class="sxs-lookup"><span data-stu-id="da872-222">You can add a correction only to nonconformances that are approved.</span></span>

1. <span data-ttu-id="da872-223">Á aðgerðasvæðinu skal velja **Lagfæringar**.</span><span class="sxs-lookup"><span data-stu-id="da872-223">On the Action Pane, select **Corrections**.</span></span>
1. <span data-ttu-id="da872-224">Á síðunni **Leiðréttingar** í hnitanetinu skal velja leiðréttinguna sem á að merkja sem lokkna.</span><span class="sxs-lookup"><span data-stu-id="da872-224">On the **Corrections** page, in the grid, select the correction that you want to mark as completed.</span></span>
1. <span data-ttu-id="da872-225">Á aðgerðasvæðinu skal velja **Merkja sem lokið**.</span><span class="sxs-lookup"><span data-stu-id="da872-225">On the Action Pane, select **Mark complete**.</span></span>
1. <span data-ttu-id="da872-226">Beðið er um staðfestingu á valinu.</span><span class="sxs-lookup"><span data-stu-id="da872-226">You're prompted to confirm your selection.</span></span> <span data-ttu-id="da872-227">Veldu **Í lagi** til að halda áfram.</span><span class="sxs-lookup"><span data-stu-id="da872-227">Select **OK** to continue.</span></span> <span data-ttu-id="da872-228">Reiturinn **Dagsetning og tími sem tilbúið er** er stilltur á núverandi dagsetningu og tíma og gátreiturinn **Lokið** er valinn.</span><span class="sxs-lookup"><span data-stu-id="da872-228">The **Completion date and time** field is set to the current date and time, and the **Completed** check box is selected.</span></span>
1. <span data-ttu-id="da872-229">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="da872-229">Close the page.</span></span>

## <a name="reopen-a-completed-correction"></a><span data-ttu-id="da872-230">Enduropna lokna leiðréttingu</span><span class="sxs-lookup"><span data-stu-id="da872-230">Reopen a completed correction</span></span>

<span data-ttu-id="da872-231">Til að opna aftur lokinni leiðréttingu skal fylgja eftirfarandi skrefum.</span><span class="sxs-lookup"><span data-stu-id="da872-231">To reopen a completed correction, follow these steps.</span></span>

1. <span data-ttu-id="da872-232">Farðu í **Birgðastjórnun \> Reglubundin verk \> Gæðastjórnun \> Ósamkvæmnistilvik**.</span><span class="sxs-lookup"><span data-stu-id="da872-232">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="da872-233">Á listanum skal velja það ósamkvæmi sem á að uppfæra.</span><span class="sxs-lookup"><span data-stu-id="da872-233">In the list, select the nonconformance that you want to update.</span></span>
1. <span data-ttu-id="da872-234">Á aðgerðasvæðinu skal velja **Lagfæringar**.</span><span class="sxs-lookup"><span data-stu-id="da872-234">On the Action pane, select **Corrections**.</span></span>
1. <span data-ttu-id="da872-235">Á síðunni **Leiðréttingar** í hnitanetinu skal velja leiðréttinguna sem á að opna aftur.</span><span class="sxs-lookup"><span data-stu-id="da872-235">On the **Corrections** page, in the grid, select the correction that you want to reopen.</span></span>
1. <span data-ttu-id="da872-236">Á aðgerðasvæðinu skal velja **Enduropna**.</span><span class="sxs-lookup"><span data-stu-id="da872-236">On the Action Pane, select **Reopen**.</span></span>
1. <span data-ttu-id="da872-237">Beðið er um staðfestingu á valinu.</span><span class="sxs-lookup"><span data-stu-id="da872-237">You're prompted to confirm your selection.</span></span> <span data-ttu-id="da872-238">Veldu **Í lagi** til að halda áfram.</span><span class="sxs-lookup"><span data-stu-id="da872-238">Select **OK** to continue.</span></span> <span data-ttu-id="da872-239">Gildið er hreinsað úr reitnum **Dagsetning og tími verkloka** og gátreiturinn **Lokið** er hreinsaður.</span><span class="sxs-lookup"><span data-stu-id="da872-239">The value is cleared from the **Completion date and time** field, and the **Completed** check box is cleared.</span></span>
1. <span data-ttu-id="da872-240">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="da872-240">Close the page.</span></span>

<span data-ttu-id="da872-241">Nú er hægt að gera frekari breytingar eða uppfærslur á leiðréttingunni.</span><span class="sxs-lookup"><span data-stu-id="da872-241">You can now make additional edits or updates to the correction.</span></span> <span data-ttu-id="da872-242">Þegar því er lokið er hægt að merkja leiðréttinguna sem lokið aftur.</span><span class="sxs-lookup"><span data-stu-id="da872-242">When you've finished, you can mark the correction as completed again.</span></span>

## <a name="close-a-nonconformance"></a><span data-ttu-id="da872-243">Loka ósamkvæmistilviki</span><span class="sxs-lookup"><span data-stu-id="da872-243">Close a nonconformance</span></span>

<span data-ttu-id="da872-244">Til að loka ósamkvæmni skal fylgja eftirfarandi skrefum.</span><span class="sxs-lookup"><span data-stu-id="da872-244">To close a nonconformance, follow these steps.</span></span>

1. <span data-ttu-id="da872-245">Farðu í **Birgðastjórnun \> Reglubundin verk \> Gæðastjórnun \> Gæðapantanir**.</span><span class="sxs-lookup"><span data-stu-id="da872-245">Go to **Inventory management \> Periodic tasks \> Quality management \> Quality orders**.</span></span>
1. <span data-ttu-id="da872-246">Veljið gæðaröð í hnitanetinu.</span><span class="sxs-lookup"><span data-stu-id="da872-246">Select a quality order in the grid.</span></span>
1. <span data-ttu-id="da872-247">Veljið **Fyrirspurnir \> Ósamkvæmni** á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="da872-247">On the Action Pane, select **Inquiries \> Non conformances**.</span></span>
1. <span data-ttu-id="da872-248">Á síðunni **Ósamkvæmi** skal velja markmið ósamkvæmis í hnitanetinu.</span><span class="sxs-lookup"><span data-stu-id="da872-248">On the **Non conformances** page, select the target nonconformance in the grid.</span></span>
1. <span data-ttu-id="da872-249">Á aðgerðasvæðinu skal velja **Aðgerðir \> Loka ósamkvæmni**.</span><span class="sxs-lookup"><span data-stu-id="da872-249">On the Action Pane, select **Functions \> Close non conformance**.</span></span>
1. <span data-ttu-id="da872-250">Beðið er um staðfestingu á valinu.</span><span class="sxs-lookup"><span data-stu-id="da872-250">You're prompted to confirm your selection.</span></span> <span data-ttu-id="da872-251">Veldu **Já** til að halda áfram.</span><span class="sxs-lookup"><span data-stu-id="da872-251">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="da872-252">Lokaðu síðunum.</span><span class="sxs-lookup"><span data-stu-id="da872-252">Close the pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="da872-253">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="da872-253">Additional resources</span></span>

- [<span data-ttu-id="da872-254">Gæðastjórnunaryfirlit</span><span class="sxs-lookup"><span data-stu-id="da872-254">Quality management overview</span></span>](../quality-management-processes.md)
- [<span data-ttu-id="da872-255">Virkja stjórnun gæða og ósamkvæmni</span><span class="sxs-lookup"><span data-stu-id="da872-255">Enable quality and nonconformance management</span></span>](../enable-quality-management.md)
- [<span data-ttu-id="da872-256">Starfsmenn ábyrgir fyrir samþykki ósamkvæmni</span><span class="sxs-lookup"><span data-stu-id="da872-256">Workers responsible for approving nonconformances</span></span>](../quality-responsible-workers.md)
- [<span data-ttu-id="da872-257">Biðgeymslusvæði fyrir ósamkvæmi</span><span class="sxs-lookup"><span data-stu-id="da872-257">Quarantine zones for nonconformances</span></span>](../quality-quarantine-zones.md)
- [<span data-ttu-id="da872-258">Gerðir greininga fyrir ósamkvæmni</span><span class="sxs-lookup"><span data-stu-id="da872-258">Diagnostic types for nonconformances</span></span>](../quality-diagnostic-types.md)
- [<span data-ttu-id="da872-259">Gæðagjöld fyrir ósamkvæmi</span><span class="sxs-lookup"><span data-stu-id="da872-259">Quality charges for nonconformances</span></span>](../quality-charges.md)
- [<span data-ttu-id="da872-260">Aðgerðir fyrir ósamkvæmni.</span><span class="sxs-lookup"><span data-stu-id="da872-260">Operations for nonconformances</span></span>](../quality-operations.md)
- [<span data-ttu-id="da872-261">Gæðastjórnun fyrir vöruhúsaferli</span><span class="sxs-lookup"><span data-stu-id="da872-261">Quality management for warehouse processes</span></span>](../quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
