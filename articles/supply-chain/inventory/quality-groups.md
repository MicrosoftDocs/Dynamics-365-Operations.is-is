---
title: Vörugæðaflokkar
description: Í þessu efnisatriði er lýst hvernig á að nota og stofna gæðaflokka fyrir vörur til að flokka vörur rökrétt svo að hægt sé að úthluta þeim á gæðatengingar fyrir sjálfvirka myndun gæðapantana.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestQualityGroup, InventTestItemQualityGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3074a6a8cc054be045bf593b509e76a1043af0b7
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956695"
---
# <a name="item-quality-groups"></a><span data-ttu-id="4aacc-103">Vörugæðaflokkar</span><span class="sxs-lookup"><span data-stu-id="4aacc-103">Item quality groups</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4aacc-104">Gæðaflokkur stendur fyrir sameiginlegar prófunarkröfur fyrir vörur.</span><span class="sxs-lookup"><span data-stu-id="4aacc-104">A quality group represents common testing requirements for items.</span></span> <span data-ttu-id="4aacc-105">Í þessu efnisatriði er lýst hvernig á að nota og stofna gæðaflokka fyrir vörur til að flokka vörur rökrétt svo að hægt sé að úthluta þeim á gæðatengingar fyrir sjálfvirka myndun gæðapantana.</span><span class="sxs-lookup"><span data-stu-id="4aacc-105">This topic describes how to use and create item quality groups to logically group products so that they can be assigned to quality associations for the automatic generation of quality orders.</span></span>

<span data-ttu-id="4aacc-106">Til að setja upp, breyta og skoða vörur sem er úthlutað á gæðaflokk eða gæðaflokkarnir sem eru úthlutað á vöru skal fara í **Birgðastjórnun \> Uppsetning \> Gæðaflokkar**.</span><span class="sxs-lookup"><span data-stu-id="4aacc-106">To set up, edit, and view the items that are assigned to a quality group, or the quality groups that are assigned to an item, go to **Inventory management \> Setup \> Quality groups**.</span></span> <span data-ttu-id="4aacc-107">Þegar búið er að skilgreina kröfur fyrir prófun á síðunni **Prófunarflokkar** er hægt að skilgreina reglur fyrir sjálfvirka myndun gæðapantana.</span><span class="sxs-lookup"><span data-stu-id="4aacc-107">After you define the test requirements on the **Test groups** page, you can define the rules for automatically generating quality orders.</span></span> <span data-ttu-id="4aacc-108">Til að einfalda ferlið eru ekki skilgreindar reglur fyrir stakar vörur.</span><span class="sxs-lookup"><span data-stu-id="4aacc-108">To simplify the process, you don't define rules for individual items.</span></span> <span data-ttu-id="4aacc-109">Í staðinn er hægt að skilgreina reglur fyrir gæðaflokk á síðunni **Gæðatengingar**.</span><span class="sxs-lookup"><span data-stu-id="4aacc-109">Instead, you can define the rules for a quality group on the **Quality associations** page.</span></span>

## <a name="example-of-an-item-quality-group"></a><span data-ttu-id="4aacc-110">Dæmi um gæðaflokk vöru</span><span class="sxs-lookup"><span data-stu-id="4aacc-110">Example of an item quality group</span></span>

<span data-ttu-id="4aacc-111">Framleiðslufyrirtæki kaupir ýmislegt hráefni sem eru með sömu prófunarkröfur fyrir væntanlegt eftirlit.</span><span class="sxs-lookup"><span data-stu-id="4aacc-111">A manufacturing company purchases various raw materials that have the same testing requirements for incoming inspection.</span></span> <span data-ttu-id="4aacc-112">Fyrirtækið skilgreinir því gæðaflokk og úthlutar síðan vörunúmerum sem eru tengd hráefnum á þann flokk.</span><span class="sxs-lookup"><span data-stu-id="4aacc-112">Therefore, the company defines a quality group and then assigns the item numbers that are associated with the raw materials to that group.</span></span> <span data-ttu-id="4aacc-113">Síðar kaupir fyrirtækið nýja gerð hráefnis sem er með sömu prófunarkröfur.</span><span class="sxs-lookup"><span data-stu-id="4aacc-113">Later, the company purchases a new type of raw material that has the same testing requirements.</span></span> <span data-ttu-id="4aacc-114">Í stað þess að setja upp ný skilyrði um prófanir fyrir nýtt efni bætir við fyrirtækið vörunúmeri fyrir nýtt efni fyrirliggjandi gæðaflokk.</span><span class="sxs-lookup"><span data-stu-id="4aacc-114">Instead of setting up new testing requirements for the new material, the company adds the item number for the new material to the existing quality group.</span></span>

<span data-ttu-id="4aacc-115">Sama fyrirtæki framleiðir einnig vörur sem eru með sömu prófunarkröfur í framleiðslu og sendir vörur með sömu kröfur fyrir framkvæmd prófana fyrir sendingu.</span><span class="sxs-lookup"><span data-stu-id="4aacc-115">The same company also produces items that have the same production testing requirements and ships items that have the same requirement for pre-shipment testing.</span></span> <span data-ttu-id="4aacc-116">Fyrirtækið skilgreinir því tvo viðbótargæðaflokka og úthlutar síðan viðeigandi vörunúmerum í hvern gæðaflokk.</span><span class="sxs-lookup"><span data-stu-id="4aacc-116">Therefore, the company defines two additional quality groups and then assigns the relevant item numbers to each group.</span></span>

## <a name="create-a-quality-group"></a><span data-ttu-id="4aacc-117">Stofna gæðaflokk</span><span class="sxs-lookup"><span data-stu-id="4aacc-117">Create a quality group</span></span>

<span data-ttu-id="4aacc-118">Til að búa til gæðaflokk skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="4aacc-118">To create a quality group, follow these steps.</span></span>

1. <span data-ttu-id="4aacc-119">Fara í **birgðastjórnun \> Uppsetning \> Gæðastjórnun \> Gæðaflokkar**</span><span class="sxs-lookup"><span data-stu-id="4aacc-119">Go to **Inventory management \> Setup \> Quality control \> Quality groups**.</span></span>
1. <span data-ttu-id="4aacc-120">Á aðgerðasvæðinu skal velja **Ný** til að bæta línu við hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="4aacc-120">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="4aacc-121">Stillið svo eftirfarandi reiti fyrir nýju línuna:</span><span class="sxs-lookup"><span data-stu-id="4aacc-121">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="4aacc-122">**Gæðaflokkur** – Færið inn einkvæmt kenni eða heiti fyrir gæðaflokkinn.</span><span class="sxs-lookup"><span data-stu-id="4aacc-122">**Quality group** – Enter a unique ID or name for the quality group.</span></span>
    - <span data-ttu-id="4aacc-123">**Lýsing** – Færið inn ítarlega lýsingu á gæðaflokknum.</span><span class="sxs-lookup"><span data-stu-id="4aacc-123">**Description** – Enter a detailed description of the quality group.</span></span>

1. <span data-ttu-id="4aacc-124">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="4aacc-124">Close the page.</span></span>

## <a name="manually-add-items-to-a-quality-group"></a><span data-ttu-id="4aacc-125">Bæta vörum handvirkt við gæðaflokk</span><span class="sxs-lookup"><span data-stu-id="4aacc-125">Manually add items to a quality group</span></span>

<span data-ttu-id="4aacc-126">Fylgið eftirfarandi skrefum til að bæta hlutum handvirkt við gæðaflokk.</span><span class="sxs-lookup"><span data-stu-id="4aacc-126">To manually add items to a quality group, follow these steps.</span></span>

1. <span data-ttu-id="4aacc-127">Fara í **birgðastjórnun \> Uppsetning \> Gæðastjórnun \> Gæðaflokkar**</span><span class="sxs-lookup"><span data-stu-id="4aacc-127">Go to **Inventory management \> Setup \> Quality control \> Quality groups**.</span></span>
1. <span data-ttu-id="4aacc-128">Veljið gæðaflokkinn sem á að bæta vörum við.</span><span class="sxs-lookup"><span data-stu-id="4aacc-128">Select the quality group that you want to add items to.</span></span>
1. <span data-ttu-id="4aacc-129">Á aðgerðasvæðinu skal velja **Vörur**.</span><span class="sxs-lookup"><span data-stu-id="4aacc-129">On the Action Pane, select **Items**.</span></span>
1. <span data-ttu-id="4aacc-130">Á síðunni **Vörur í gæðaflokkum**, á aðgerðasvæðinu, skal velja **Ný** til að bæta nýrri línu við hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="4aacc-130">On the **Items in quality groups** page, on the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="4aacc-131">Í nýju línunni skal síðan stilla reitinn **Vörunúmer** á vörunúmerið sem bæta á við.</span><span class="sxs-lookup"><span data-stu-id="4aacc-131">Then, for the new row, set the **Item number** field to the item number that you want to add.</span></span>
1. <span data-ttu-id="4aacc-132">Endurtakið fyrra skref fyrir hverja viðbótarvöru sem þarf að bæta við.</span><span class="sxs-lookup"><span data-stu-id="4aacc-132">Repeat the previous step for each additional item that must be added.</span></span>
1. <span data-ttu-id="4aacc-133">Lokaðu síðunum.</span><span class="sxs-lookup"><span data-stu-id="4aacc-133">Close the pages.</span></span>

## <a name="add-multiple-items-to-a-quality-group"></a><span data-ttu-id="4aacc-134">Bæta mörgum vörum við gæðaflokk</span><span class="sxs-lookup"><span data-stu-id="4aacc-134">Add multiple items to a quality group</span></span>

<span data-ttu-id="4aacc-135">Fylgið eftirfarandi skrefum til að bæta mörgum atriðum við gæðaflokk.</span><span class="sxs-lookup"><span data-stu-id="4aacc-135">To add multiple items to a quality group, follow these steps.</span></span>

1. <span data-ttu-id="4aacc-136">Fara í **birgðastjórnun \> Uppsetning \> Gæðastjórnun \> Gæðaflokkar**</span><span class="sxs-lookup"><span data-stu-id="4aacc-136">Go to **Inventory management \> Setup \> Quality control \> Quality groups**.</span></span>
1. <span data-ttu-id="4aacc-137">Búa til eða velja gæðahópinn sem bæta á atriðum við.</span><span class="sxs-lookup"><span data-stu-id="4aacc-137">Create or select the quality group that you want to add items to.</span></span>
1. <span data-ttu-id="4aacc-138">Á aðgerðasvæðinu skal velja **Bæta við vörum**.</span><span class="sxs-lookup"><span data-stu-id="4aacc-138">On the Action Pane, select **Add items**.</span></span>
1. <span data-ttu-id="4aacc-139">Færið inn síuviðmiðin fyrir vörurnar sem á að bæta við í glugganum **Fyrirspurn**.</span><span class="sxs-lookup"><span data-stu-id="4aacc-139">In the **Inquiry** dialog box, enter the filter criteria for the items that you want to add.</span></span> <span data-ttu-id="4aacc-140">Til dæmis væri hægt að sía fyrir allar vörur í tilteknum vöruflokki.</span><span class="sxs-lookup"><span data-stu-id="4aacc-140">For example, you might filter for all items in a specific item group.</span></span>
1. <span data-ttu-id="4aacc-141">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="4aacc-141">Select **OK**.</span></span>
1. <span data-ttu-id="4aacc-142">Í glugganum **Bæta við atriðum** sýnir reitur öll atriðin sem samsvara fyrirspurninni.</span><span class="sxs-lookup"><span data-stu-id="4aacc-142">In the **Add items** dialog box, a grid shows all the items that match your query.</span></span> <span data-ttu-id="4aacc-143">Skoða niðurstöður.</span><span class="sxs-lookup"><span data-stu-id="4aacc-143">Review the results.</span></span>

    <span data-ttu-id="4aacc-144">Ef einhverjar breytingar eru nauðsynlegar skal velja **Velja** til að fara aftur í svargluggann **Spyrjast fyrir** og breyta fyrirspurninni.</span><span class="sxs-lookup"><span data-stu-id="4aacc-144">If any changes are required, select **Select** to return to the **Inquiry** dialog box, and adjust your query.</span></span>

1. <span data-ttu-id="4aacc-145">Þegar niðurstöðurnar innihalda allar vörur sem á að bæta við er valið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="4aacc-145">When the results include all the items that you want to add, select **OK**.</span></span>
1. <span data-ttu-id="4aacc-146">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="4aacc-146">Close the page.</span></span>

## <a name="manually-associate-an-item-with-a-quality-group"></a><span data-ttu-id="4aacc-147">Tengja atriði handvirkt við gæðahóp</span><span class="sxs-lookup"><span data-stu-id="4aacc-147">Manually associate an item with a quality group</span></span>

<span data-ttu-id="4aacc-148">Fylgja skal eftirfarandi skrefum til að tengja hlut handvirkt við gæðflokk.</span><span class="sxs-lookup"><span data-stu-id="4aacc-148">To manually associate an item with a quality group, follow these steps.</span></span>

1. <span data-ttu-id="4aacc-149">Farið í **Birgðastjórnun \> Uppsetning \> Gæðastjórnun \> Gæðaflokkar vöru**.</span><span class="sxs-lookup"><span data-stu-id="4aacc-149">Go to **Inventory management \> Setup \> Quality control \> Item quality groups**.</span></span>
1. <span data-ttu-id="4aacc-150">Á aðgerðasvæðinu skal velja **Ný** til að bæta línu við hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="4aacc-150">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="4aacc-151">Stillið svo eftirfarandi reiti fyrir nýju línuna:</span><span class="sxs-lookup"><span data-stu-id="4aacc-151">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="4aacc-152">**Vörunúmer** – Velja vörunúmerið sem á að bæta við.</span><span class="sxs-lookup"><span data-stu-id="4aacc-152">**Item number** – Select the item number to add.</span></span>
    - <span data-ttu-id="4aacc-153">**Gæðaflokkur** – Veljið gæðaflokk sem úthluta á vörunni.</span><span class="sxs-lookup"><span data-stu-id="4aacc-153">**Quality group** – Select the quality group to assign to the item.</span></span>

1. <span data-ttu-id="4aacc-154">Endurtaka skal fyrri skref fyrir hverja viðbótarsamsetningu vöru og gæðaflokks sem verður að bæta við.</span><span class="sxs-lookup"><span data-stu-id="4aacc-154">Repeat the previous step for each additional combination of an item and a quality group that must be added.</span></span>
1. <span data-ttu-id="4aacc-155">Lokaðu síðunum.</span><span class="sxs-lookup"><span data-stu-id="4aacc-155">Close the pages.</span></span>

## <a name="manually-add-a-quality-group-from-the-released-products-page"></a><span data-ttu-id="4aacc-156">Bæta við gæðaflokki handvirkt af síðunni Útgefnar afurðir</span><span class="sxs-lookup"><span data-stu-id="4aacc-156">Manually add a quality group from the Released products page</span></span>

<span data-ttu-id="4aacc-157">Fylgja skal eftirfarandi skrefum til að bæta gæðahópi handvirkt við á síðunni **Losaðar afurðir**.</span><span class="sxs-lookup"><span data-stu-id="4aacc-157">To manually add a quality group from the **Released products** page, follow these steps.</span></span>

1. <span data-ttu-id="4aacc-158">Opna **Afurðaupplýsingastjórnun \> Afurðir \> Útgefnar afurðir**.</span><span class="sxs-lookup"><span data-stu-id="4aacc-158">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="4aacc-159">Veljið afurðina sem úthluta á gæðaflokki á.</span><span class="sxs-lookup"><span data-stu-id="4aacc-159">Select the product that you want to assign a quality group to.</span></span>
1. <span data-ttu-id="4aacc-160">Á aðgerðasvæðinu, í flipanum **Stjórna birgðum**, í flokknum **Gæði**, skal velja **Gæðaflokkar vöru**.</span><span class="sxs-lookup"><span data-stu-id="4aacc-160">On the Action Pane, on the **Manage inventory** tab, in the **Quality** group, select **Item quality groups**.</span></span>
1. <span data-ttu-id="4aacc-161">Á síðunni **Vörur í gæðaflokkum**, á aðgerðasvæðinu, skal velja **Ný** til að bæta nýrri línu við hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="4aacc-161">On the **Items in quality groups** page, on the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="4aacc-162">Í nýju línunni skal síðan stilla reitinn **Gæðaflokkur** á gæðaflokkinn sem þú vilt úthluta afurðinni.</span><span class="sxs-lookup"><span data-stu-id="4aacc-162">Then, for the new row, set the **Quality group** field to the quality group that you want to assign to the product.</span></span>
1. <span data-ttu-id="4aacc-163">Endurtaka á fyrra skref fyrir hvern gæðaflokk sem bætist við sem á að úthluta afurðinni.</span><span class="sxs-lookup"><span data-stu-id="4aacc-163">Repeat the previous step for each additional quality group that you want to assign to the product.</span></span>
1. <span data-ttu-id="4aacc-164">Lokaðu síðunum.</span><span class="sxs-lookup"><span data-stu-id="4aacc-164">Close the pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4aacc-165">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="4aacc-165">Additional resources</span></span>

- [<span data-ttu-id="4aacc-166">Prófunartæki gæðastjórnunar</span><span class="sxs-lookup"><span data-stu-id="4aacc-166">Quality management test instruments</span></span>](quality-test-instruments.md)
- [<span data-ttu-id="4aacc-167">Prófanir gæðastjórnunar</span><span class="sxs-lookup"><span data-stu-id="4aacc-167">Quality management tests</span></span>](quality-tests.md)
- [<span data-ttu-id="4aacc-168">Prófunarflokkar gæðastjórnunar</span><span class="sxs-lookup"><span data-stu-id="4aacc-168">Quality management test groups</span></span>](quality-test-groups.md)
- [<span data-ttu-id="4aacc-169">Prófunarbreytur gæðastjórnunar</span><span class="sxs-lookup"><span data-stu-id="4aacc-169">Quality management test variables</span></span>](quality-test-variables.md)
- [<span data-ttu-id="4aacc-170">Gæðatengingar</span><span class="sxs-lookup"><span data-stu-id="4aacc-170">Quality associations</span></span>](quality-associations.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
