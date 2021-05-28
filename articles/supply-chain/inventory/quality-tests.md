---
title: Prófanir gæðastjórnunar
description: Í þessu efnisatriði er lýst hvernig á að búa til prófanir sem hægt er að nota fyrir gæðapantanir í Microsoft Dynamics 365 Supply Chain Management.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 95f759d051a520b577cb1cf3d595ce64e0dc4668
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021685"
---
# <a name="quality-management-tests"></a><span data-ttu-id="b1380-103">Prófanir gæðastjórnunar</span><span class="sxs-lookup"><span data-stu-id="b1380-103">Quality management tests</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b1380-104">Í þessu efnisatriði er lýst hvernig á að búa til prófanir sem hægt er að nota fyrir gæðapantanir í Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="b1380-104">This topic describes how to create tests that can be used for quality orders in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="b1380-105">Notið síðuna **Prófanir** til að skilgreina og skoða einstök próf sem ákvarða hvort framleiðsluvara fyrirtækisins uppfylli gæðakröfur.</span><span class="sxs-lookup"><span data-stu-id="b1380-105">You use the **Tests** page to define and view the individual tests that determine whether your products meet quality specifications.</span></span> <span data-ttu-id="b1380-106">Hægt er að úthluta einu eða fleiri einstökum prófum á prófunarflokk.</span><span class="sxs-lookup"><span data-stu-id="b1380-106">You can assign one or more individual tests to a test group.</span></span> <span data-ttu-id="b1380-107">Í þessu tilviki þarf einnig að tilgreina prófunarsértækar upplýsingar, eins og viðunandi mælingargildi.</span><span class="sxs-lookup"><span data-stu-id="b1380-107">In this case, you also specify test-specific information, such as the acceptable measurement values.</span></span> <span data-ttu-id="b1380-108">Mæligildi eru notuð fyrir magnbundnar prófanir.</span><span class="sxs-lookup"><span data-stu-id="b1380-108">Measurement values are used for quantitative tests.</span></span> <span data-ttu-id="b1380-109">Fyrir gæðapróf eru prófbreytur notaðar.</span><span class="sxs-lookup"><span data-stu-id="b1380-109">For qualitative tests, test variables are used.</span></span>

- <span data-ttu-id="b1380-110">Fyrir magnbundnar prófanir er reiturinn **Gerð** stilltur á *Heiltala* eða *Brot*.</span><span class="sxs-lookup"><span data-stu-id="b1380-110">For quantitative tests, the **Type** field is set to *Integer* or *Fraction*.</span></span> <span data-ttu-id="b1380-111">Mælieining er einnig tilgreind.</span><span class="sxs-lookup"><span data-stu-id="b1380-111">A unit of measure is also specified.</span></span> <span data-ttu-id="b1380-112">Gæðaskilyrði og prófunarniðurstöður sem eru sýnd sem tölur.</span><span class="sxs-lookup"><span data-stu-id="b1380-112">Quality specifications and test results are expressed as numbers.</span></span>
- <span data-ttu-id="b1380-113">Fyrir gæðaprófanir er reiturinn **Gerð** stilltur á *Valkostur*.</span><span class="sxs-lookup"><span data-stu-id="b1380-113">For qualitative tests, the **Type** field is set to *Option*.</span></span> <span data-ttu-id="b1380-114">Eigindlegar prófanir krefjast viðbótarupplýsingar um prófunarbreytuna sem verið er að mæla og tölusetta valkosti hennar.</span><span class="sxs-lookup"><span data-stu-id="b1380-114">Qualitative tests require additional information about the test variable that is being measured and its enumerated options.</span></span> <span data-ttu-id="b1380-115">Gæðaforskriftir og prófunarniðurstöður sem eru sýnd eftir útkomu.</span><span class="sxs-lookup"><span data-stu-id="b1380-115">Quality specifications and test results are expressed according to an outcome.</span></span>

<span data-ttu-id="b1380-116">Einnig má tengja prófunartækið við próf.</span><span class="sxs-lookup"><span data-stu-id="b1380-116">You can optionally assign a test instrument to a test.</span></span> <span data-ttu-id="b1380-117">Hins vegar þarf ekki að búa til og nota próf með gæðapöntunum.</span><span class="sxs-lookup"><span data-stu-id="b1380-117">However, test instruments aren't required to create and use tests with quality orders.</span></span> <span data-ttu-id="b1380-118">Frekari upplýsingar er að finna í [Prófunartæki gæðastjórnunar](quality-test-instruments.md).</span><span class="sxs-lookup"><span data-stu-id="b1380-118">For more information, see [Quality management test instruments](quality-test-instruments.md).</span></span>

<span data-ttu-id="b1380-119">Einnig er hægt að valfrjálst tilgreina einingu fyrir próf, til að gefa upp mælieininguna sem niðurstöður prófunar eru skráðar í.</span><span class="sxs-lookup"><span data-stu-id="b1380-119">You can also optionally specify a unit for a test, to indicate the unit of measure that test results are recorded in.</span></span> <span data-ttu-id="b1380-120">Til dæmis gæti prófun á hitastigi innihaldið einingu sem er annaðhvort gráður Fahrenheit eða gráður Celsíus.</span><span class="sxs-lookup"><span data-stu-id="b1380-120">For example, a test for temperature might include a unit of either degrees Fahrenheit or degrees Celsius.</span></span>

## <a name="example-of-a-test"></a><span data-ttu-id="b1380-121">Dæmi um próf</span><span class="sxs-lookup"><span data-stu-id="b1380-121">Example of a test</span></span>

<span data-ttu-id="b1380-122">Framleiðslufyrirtæki framkvæmir tvær prófanir á innkeyptu efni: magnbundið próf fyrir gæði efnis og gæðapróf fyrir skemmdir á umbúðum.</span><span class="sxs-lookup"><span data-stu-id="b1380-122">A manufacturing company performs two tests on purchased material: a quantitative test for material quality and a qualitative test for packaging damage.</span></span> <span data-ttu-id="b1380-123">Fyrirtækið skilgreinir viðbótarupplýsingar um magnbundna prófið til að skilgreina prófunarbreytuna (til dæmis skemmdir á umbúðum) og útkomu þess.</span><span class="sxs-lookup"><span data-stu-id="b1380-123">The company specifies additional information about the qualitative test to define the test variable (for example, damaged packaging) and its outcomes.</span></span> <span data-ttu-id="b1380-124">Fyrirtæki notar síðuna **Prófunarflokkar** til að úthluta tveimur prófunum á prófunarflokk og tilgreina prófunarsértækar upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="b1380-124">The company uses the **Test groups** page to assign the two tests to a test group and to specify the test-specific information.</span></span> <span data-ttu-id="b1380-125">Prófunarflokkurinn er tengdur við gæðapöntun, þannig að fyrirtækið getur gert skýrslu um niðurstöður þessara tveggja prófa.</span><span class="sxs-lookup"><span data-stu-id="b1380-125">The test group is assigned to a quality order so that the company can report test results for the two tests.</span></span>

## <a name="create-a-test"></a><span data-ttu-id="b1380-126">Stofna próf</span><span class="sxs-lookup"><span data-stu-id="b1380-126">Create a test</span></span>

<span data-ttu-id="b1380-127">Til að stofna próf skal fylgja eftirfarandi skrefum.</span><span class="sxs-lookup"><span data-stu-id="b1380-127">Follow these steps to create a test.</span></span>

1. <span data-ttu-id="b1380-128">Farið í **Birgðastjórnun \> Uppsetning \> Gæðastjórnun \> Prófanir**.</span><span class="sxs-lookup"><span data-stu-id="b1380-128">Go to **Inventory management \> Setup \> Quality control \> Tests**.</span></span>
1. <span data-ttu-id="b1380-129">Á aðgerðasvæðinu skal velja **Ný** til að bæta línu við hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="b1380-129">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="b1380-130">Stillið svo eftirfarandi reiti fyrir nýju línuna:</span><span class="sxs-lookup"><span data-stu-id="b1380-130">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="b1380-131">**Próf** – Færið inn einkvæmt kenni eða heiti fyrir prófið.</span><span class="sxs-lookup"><span data-stu-id="b1380-131">**Test** – Enter a unique ID or name for the test.</span></span>
    - <span data-ttu-id="b1380-132">**Lýsing** – Færið inn nákvæma lýsingu á prófuninni.</span><span class="sxs-lookup"><span data-stu-id="b1380-132">**Description** – Enter a detailed description of the test.</span></span>
    - <span data-ttu-id="b1380-133">**Gerð** – Veljið þá gerð niðurstöðu sem á að koma út úr prófinu.</span><span class="sxs-lookup"><span data-stu-id="b1380-133">**Type** – Select the type of results that the test produces.</span></span> <span data-ttu-id="b1380-134">Fyrir magnbundnar prófanir skal velja *Brot* eða *Heiltala*.</span><span class="sxs-lookup"><span data-stu-id="b1380-134">For quantitative tests, select *Fraction* or *Integer*.</span></span> <span data-ttu-id="b1380-135">Fyrir gæðaprófanir, veljið *Valkostur*.</span><span class="sxs-lookup"><span data-stu-id="b1380-135">For qualitative tests, select *Option*.</span></span>
    - <span data-ttu-id="b1380-136">**Prófunartæki** – Veljið [prófunartæki](quality-test-instruments.md) sem á að nota fyrir prófið.</span><span class="sxs-lookup"><span data-stu-id="b1380-136">**Test instrument** – Select a [test instrument](quality-test-instruments.md) that should be used for the test.</span></span>
    - <span data-ttu-id="b1380-137">**Eining** – Ef þú valdir *Brot* eða *Heiltölu* í reitnum **Gerð** (þ.e. ef prófið er magnbundið próf), skal velja mælieininguna sem niðurstöður prófunar eiga að vera skráðar í.</span><span class="sxs-lookup"><span data-stu-id="b1380-137">**Unit** – If you selected *Fraction* or *Integer* in the **Type** field (that is, if the test is a quantitative test), select the unit of measure that test results should be recorded in.</span></span>

1. <span data-ttu-id="b1380-138">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="b1380-138">Close the page.</span></span>

> [!NOTE]
> <span data-ttu-id="b1380-139">Eftir að próf hefur verið vistað er ekki lengur hægt að breyta reitnum **Tegund** í reitnum hnitanetinu.</span><span class="sxs-lookup"><span data-stu-id="b1380-139">After you save a test, you can no longer edit the **Type** field in the grid.</span></span> <span data-ttu-id="b1380-140">Ef breyta þarf gerð fyrir niðurstöður prófunar sem verður skráð fyrir próf skal velja **Breyta gerð gæðaprófunar** á aðgerðasvæðinu.</span><span class="sxs-lookup"><span data-stu-id="b1380-140">If you must change the type of test results that will be recorded for a test, select **Change quality test type** on the Action Pane.</span></span> <span data-ttu-id="b1380-141">Í svarglugganum **Breyta gerð gæðaprófunar** skal stilla reitinn **Ný gerð** á æskilega gerð og síðan velja **Í lagi** til að loka svarglugganum.</span><span class="sxs-lookup"><span data-stu-id="b1380-141">In the **Change quality test type** dialog box, set the **New type** field to the desired type, and then select **OK** to close the dialog box.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b1380-142">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="b1380-142">Additional resources</span></span>

- [<span data-ttu-id="b1380-143">Prófunartæki gæðastjórnunar</span><span class="sxs-lookup"><span data-stu-id="b1380-143">Quality management test instruments</span></span>](quality-test-instruments.md)
- [<span data-ttu-id="b1380-144">Prófunarflokkar gæðastjórnunar</span><span class="sxs-lookup"><span data-stu-id="b1380-144">Quality management test groups</span></span>](quality-test-groups.md)
- [<span data-ttu-id="b1380-145">Prófunarbreytur gæðastjórnunar</span><span class="sxs-lookup"><span data-stu-id="b1380-145">Quality management test variables</span></span>](quality-test-variables.md)
- [<span data-ttu-id="b1380-146">Gæðatengingar</span><span class="sxs-lookup"><span data-stu-id="b1380-146">Quality associations</span></span>](quality-associations.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
