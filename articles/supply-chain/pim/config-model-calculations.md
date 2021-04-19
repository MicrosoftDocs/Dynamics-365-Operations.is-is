---
title: Útreikningar afbrigðalíkans afurðar
description: Þetta efnisatriði lýsir því hvernig á að stofna útreikninga fyrir einingar í afbrigðalíkani afurðar
author: t-benebo
ms.date: 03/18/2021
ms.topic: article
ms.search.form: PCProductConfigurationModelListPage, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-03-18
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: eaf6264f060d33575740ad38e7a65158baba296b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829619"
---
# <a name="product-configuration-model-calculations"></a><span data-ttu-id="67c3d-103">Útreikningar afbrigðalíkans afurðar</span><span class="sxs-lookup"><span data-stu-id="67c3d-103">Product configuration model calculations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="67c3d-104">Þetta efnisatriði lýsir því hvernig á að stofna útreikninga fyrir einingar í afbrigðalíkani afurðar.</span><span class="sxs-lookup"><span data-stu-id="67c3d-104">This topic describes how to create calculations for attributes in a product configuration model.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="67c3d-105">Forkröfur</span><span class="sxs-lookup"><span data-stu-id="67c3d-105">Prerequisites</span></span>

<span data-ttu-id="67c3d-106">Útreikningarnir eru notaðir í afbrigðalíkani afurðar til að reikna út grunnstillingargildi fyrir vöru.</span><span class="sxs-lookup"><span data-stu-id="67c3d-106">Calculations are used in a product configuration model to calculate the configuration values for a product.</span></span> <span data-ttu-id="67c3d-107">Áður en hægt er að setja upp útreikninga verður tengt afbrigðalíkan vörunnar að vera til staðar.</span><span class="sxs-lookup"><span data-stu-id="67c3d-107">Before you can start to set up calculations, the related product configuration model must exist.</span></span> <span data-ttu-id="67c3d-108">Fyrir yfirlit yfir uppsetningarferlið fyrir afbrigðalíkön og tengd verk skal skoða [Setja upp afbrigðalíkan afurðar](set-up-maintain-product-configuration-model.md).</span><span class="sxs-lookup"><span data-stu-id="67c3d-108">For an overview of the setup process for configuration models and the related tasks, see [Set up a product configuration model](set-up-maintain-product-configuration-model.md).</span></span>

## <a name="create-a-calculation"></a><span data-ttu-id="67c3d-109">Stofna útreikning</span><span class="sxs-lookup"><span data-stu-id="67c3d-109">Create a calculation</span></span>

<span data-ttu-id="67c3d-110">Útreikningur samanstendur af segð og markmiðseigind.</span><span class="sxs-lookup"><span data-stu-id="67c3d-110">A calculation consists of an expression and a target attribute.</span></span> <span data-ttu-id="67c3d-111">Frekari upplýsingar eru í [Algengar spurningar um afbrigðalíkan afurðar](calculate-product-configuration-models.md).</span><span class="sxs-lookup"><span data-stu-id="67c3d-111">For more information, see [Calculations for product configuration models FAQ](calculate-product-configuration-models.md).</span></span>

<span data-ttu-id="67c3d-112">Fylgið þessum skrefum til að búa til útreikning fyrir fyrirliggjandi vörulíkan.</span><span class="sxs-lookup"><span data-stu-id="67c3d-112">To create a calculation for an existing product model, follow these steps.</span></span>

1. <span data-ttu-id="67c3d-113">Farið í **Upplýsingastjórnun afurða \> Almennt \> Afbrigðalíkan afurðar**.</span><span class="sxs-lookup"><span data-stu-id="67c3d-113">Go to **Product information management \> Common \> Product configuration models**.</span></span>
1. <span data-ttu-id="67c3d-114">Opnið afbrigðalíkan afurðar og smellið síðan á **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="67c3d-114">Open a product configuration model, and then select **Edit**.</span></span>
1. <span data-ttu-id="67c3d-115">Í flýtiflipanum **Útreikningar** skal velja **Bæta við** til að bæta við útreikningi og stillið síðan eftirfarandi reiti:</span><span class="sxs-lookup"><span data-stu-id="67c3d-115">On the **Calculations** FastTab, select **Add** to add a calculation, and then set the following fields:</span></span>

    - <span data-ttu-id="67c3d-116">**Heiti** – Færið inn heiti fyrir útreikninginn.</span><span class="sxs-lookup"><span data-stu-id="67c3d-116">**Name** – Enter a name for the calculation.</span></span>
    - <span data-ttu-id="67c3d-117">**Lýsing** – Færið inn lýsingu á útreikningnum.</span><span class="sxs-lookup"><span data-stu-id="67c3d-117">**Description** – Enter a description of the calculation.</span></span>
    - <span data-ttu-id="67c3d-118">**Markeigind** – Select the attribute that you're making the calculation for.</span><span class="sxs-lookup"><span data-stu-id="67c3d-118">**Target attribute** – Select the attribute that you're making the calculation for.</span></span>

1. <span data-ttu-id="67c3d-119">Veljið **Breyta segð**.</span><span class="sxs-lookup"><span data-stu-id="67c3d-119">Select **Edit expression**.</span></span>
1. <span data-ttu-id="67c3d-120">Í svarglugganum **Færa inn útreikning** skal bæta nauðsynlegum eiginleikum, virkjum og gildum við segðina.</span><span class="sxs-lookup"><span data-stu-id="67c3d-120">In the **Enter a calculation** dialog box, add the required attributes, operators, and values to the expression.</span></span> <span data-ttu-id="67c3d-121">Frekari upplýsingar um það hvernig vinna á með þessar einingar má finna í [Segðarskorður og töfluskorður í afbrigðalíkönum afurðar](expression-constraints-table-constraints-product-configuration-models.md).</span><span class="sxs-lookup"><span data-stu-id="67c3d-121">For more information about how to work with these elements, see [Expression constraints and table constraints in product configuration models](expression-constraints-table-constraints-product-configuration-models.md).</span></span>
1. <span data-ttu-id="67c3d-122">Þegar segðin er tilbúin skal velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="67c3d-122">When your expression is ready, select **OK**.</span></span>

## <a name="calculation-examples"></a><span data-ttu-id="67c3d-123">Dæmi um útreikning</span><span class="sxs-lookup"><span data-stu-id="67c3d-123">Calculation examples</span></span>

<span data-ttu-id="67c3d-124">Í þessum hluta eru nokkur dæmi sem sýna hvernig útreikningar virka.</span><span class="sxs-lookup"><span data-stu-id="67c3d-124">This section provides a few examples that show how calculations work.</span></span>

### <a name="example-1"></a><span data-ttu-id="67c3d-125">Dæmi 1</span><span class="sxs-lookup"><span data-stu-id="67c3d-125">Example 1</span></span>

<span data-ttu-id="67c3d-126">Markeigindin er Boole-gildi og útreikningurinn notar eftirfarandi skilyrta segð:</span><span class="sxs-lookup"><span data-stu-id="67c3d-126">The target attribute is Boolean, and the calculation uses the following conditional expression:</span></span>

`If[(decimalAttribute1 / decimalAttribute2) < 1, True, False]`

<span data-ttu-id="67c3d-127">Þessi segð skilar gildinu *Rétt* á markmiðseigindina ef `decimalAttribute2` er hærra en eða jafnt og `decimalAttribute1`.</span><span class="sxs-lookup"><span data-stu-id="67c3d-127">This expression returns a value of *True* to the target attribute if `decimalAttribute2` is greater than or equal to `decimalAttribute1`.</span></span> <span data-ttu-id="67c3d-128">Að öðrum kosti skilar hún Boolean *Rangt*.</span><span class="sxs-lookup"><span data-stu-id="67c3d-128">Otherwise, it returns a value of *False*.</span></span>

### <a name="example-2"></a><span data-ttu-id="67c3d-129">Dæmi 2</span><span class="sxs-lookup"><span data-stu-id="67c3d-129">Example 2</span></span>

<span data-ttu-id="67c3d-130">Þetta dæmi notar textaeigindina `textFixedList` sem markeigind.</span><span class="sxs-lookup"><span data-stu-id="67c3d-130">This example uses the text attribute `textFixedList` as the target attribute.</span></span> <span data-ttu-id="67c3d-131">Þessi eigind inniheldur eftirfarandi fastan lista.</span><span class="sxs-lookup"><span data-stu-id="67c3d-131">This attribute contains the following fixed list.</span></span>

| <span data-ttu-id="67c3d-132">Virði</span><span class="sxs-lookup"><span data-stu-id="67c3d-132">Value</span></span> | <span data-ttu-id="67c3d-133">Gildi leysara</span><span class="sxs-lookup"><span data-stu-id="67c3d-133">Solver value</span></span> |
|---|---|
| <span data-ttu-id="67c3d-134">A</span><span class="sxs-lookup"><span data-stu-id="67c3d-134">A</span></span> | <span data-ttu-id="67c3d-135">1a</span><span class="sxs-lookup"><span data-stu-id="67c3d-135">1a</span></span> |
| <span data-ttu-id="67c3d-136">V</span><span class="sxs-lookup"><span data-stu-id="67c3d-136">B</span></span> | <span data-ttu-id="67c3d-137">2b</span><span class="sxs-lookup"><span data-stu-id="67c3d-137">2b</span></span> |
| <span data-ttu-id="67c3d-138">K</span><span class="sxs-lookup"><span data-stu-id="67c3d-138">C</span></span> | <span data-ttu-id="67c3d-139">2c</span><span class="sxs-lookup"><span data-stu-id="67c3d-139">2c</span></span> |

<span data-ttu-id="67c3d-140">Eftirfarandi skjámynd sýnir hvernig stillingar fyrir þessa eigind gætu litið út í kerfinu þínu.</span><span class="sxs-lookup"><span data-stu-id="67c3d-140">The following screenshot shows how the settings for this attribute might look in your system.</span></span>

<span data-ttu-id="67c3d-141">![Stillingar eigindargerðar fyrir dæmi 2](media/model-calculations-example2.png "Stillingar eigindargerðar fyrir dæmi 2")</span><span class="sxs-lookup"><span data-stu-id="67c3d-141">![Attribute type settings for example 2](media/model-calculations-example2.png "Attribute type settings for example 2")</span></span>

<span data-ttu-id="67c3d-142">Eigindin er notuð í eftirfarandi skilyrtu yfirliti:</span><span class="sxs-lookup"><span data-stu-id="67c3d-142">The attribute is used in the following conditional statement:</span></span>

`If[integerAttribute < 150, 0, 2]`

<span data-ttu-id="67c3d-143">Ef `integerAttribute` er minna en 150 skilar þetta yfirlit textagildi fyrstu færslunnar í fasta listanum, *A*. Annars skilar það textagildi þriðju færslunnar í fasta listanum, *C*.</span><span class="sxs-lookup"><span data-stu-id="67c3d-143">If `integerAttribute` is less than 150, this statement returns the text value of the first record in the fixed list, *A*. Otherwise, it returns the text value of the third record in the fixed list, *C*.</span></span>

> [!NOTE]
> <span data-ttu-id="67c3d-144">Fasti listinn jafngildir núllgrunnsupptalningu (fasttexta) og gildi hans eru fengin með viðeigandi heiltölu.</span><span class="sxs-lookup"><span data-stu-id="67c3d-144">The fixed list is equivalent to a zero-based enumeration (enum), and its values are accessed by the appropriate integer value.</span></span> <span data-ttu-id="67c3d-145">Þess vegna er fyrsta gildi fasta listans (*A*) samsvarað við *0*, annað gildið (*B*) er samsvarað við *1* og þriðja gildið (*C*) er samvarað við *2*.</span><span class="sxs-lookup"><span data-stu-id="67c3d-145">Therefore, the first fixed list value (*A*) is matched to *0*, the second value (*B*) is matched to *1*, and the third value (*C*) is matched to *2*.</span></span>

### <a name="example-3"></a><span data-ttu-id="67c3d-146">Dæmi 3</span><span class="sxs-lookup"><span data-stu-id="67c3d-146">Example 3</span></span>

<span data-ttu-id="67c3d-147">Þetta dæmi notar `textFixedList` markeigindina úr fyrra dæminu.</span><span class="sxs-lookup"><span data-stu-id="67c3d-147">This example uses the `textFixedList` target attribute from the previous example.</span></span> <span data-ttu-id="67c3d-148">Það notar einnig aðra textaeigind, `textAttribute`, sem inniheldur eftirfarandi fastan lista.</span><span class="sxs-lookup"><span data-stu-id="67c3d-148">It also uses another text attribute, `textAttribute`, that contains the following fixed list.</span></span>

| <span data-ttu-id="67c3d-149">Virði</span><span class="sxs-lookup"><span data-stu-id="67c3d-149">Value</span></span> | <span data-ttu-id="67c3d-150">Gildi leysara</span><span class="sxs-lookup"><span data-stu-id="67c3d-150">Solver value</span></span> |
|---|---|
| <span data-ttu-id="67c3d-151">AA</span><span class="sxs-lookup"><span data-stu-id="67c3d-151">AA</span></span> | <span data-ttu-id="67c3d-152">1aa</span><span class="sxs-lookup"><span data-stu-id="67c3d-152">1aa</span></span> |
| <span data-ttu-id="67c3d-153">BB</span><span class="sxs-lookup"><span data-stu-id="67c3d-153">BB</span></span> | <span data-ttu-id="67c3d-154">2bb</span><span class="sxs-lookup"><span data-stu-id="67c3d-154">2bb</span></span> |

<span data-ttu-id="67c3d-155">Eftirfarandi skjámynd sýnir hvernig stillingar fyrir þessa eigind gætu litið út í kerfinu þínu.</span><span class="sxs-lookup"><span data-stu-id="67c3d-155">The following screenshot shows how the settings for this attribute might look in your system.</span></span>

<span data-ttu-id="67c3d-156">![Stillingar eigindargerðar fyrir dæmi 3](media/model-calculations-example3.png "Stillingar eigindargerðar fyrir dæmi 3")</span><span class="sxs-lookup"><span data-stu-id="67c3d-156">![Attribute type settings for example 3](media/model-calculations-example3.png "Attribute type settings for example 3")</span></span>

<span data-ttu-id="67c3d-157">Gildið fyrir `textFixedList` eigindina er reiknað með eftirfarandi skilyrtu yfirliti:</span><span class="sxs-lookup"><span data-stu-id="67c3d-157">The value for the `textFixedList` attribute is calculated by using the following conditional statement:</span></span>

`If[textAttribute == "1aa", 0, 2]`

<span data-ttu-id="67c3d-158">Ef `textAttribute` gildið er með leysigildi sem jafngildir *1aa*, skilar þessi segð textagildi fyrstu færslunnar í `textFixedList` fasta listanum, *A*. Annars skilað það textagildi þriðju færslunnar í `textFixedList` fasta listanum, *C*.</span><span class="sxs-lookup"><span data-stu-id="67c3d-158">If the `textAttribute` value has a solver value that equals *1aa*, this expression returns the text value of the first record in the `textFixedList` fixed list, *A*. Otherwise, it returns the text value of the third record in the `textFixedList` fixed list, *C*.</span></span>

> [!NOTE]
> - <span data-ttu-id="67c3d-159">Skilyrta yfirlitið verður að nota leysigildi eigindarinnar.</span><span class="sxs-lookup"><span data-stu-id="67c3d-159">The conditional statement must use the solver value of the attribute.</span></span>
> - <span data-ttu-id="67c3d-160">Aðeins er hægt að nota textaeigindir fasts lista í útreikningum.</span><span class="sxs-lookup"><span data-stu-id="67c3d-160">Only fixed-list text attributes can be used in calculations.</span></span>

## <a name="see-also"></a><span data-ttu-id="67c3d-161">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="67c3d-161">See also</span></span>

- [<span data-ttu-id="67c3d-162">Algengar spurningar um afbrigðalíkan afurðar</span><span class="sxs-lookup"><span data-stu-id="67c3d-162">Calculations for product configuration models FAQ</span></span>](calculate-product-configuration-models.md)
- [<span data-ttu-id="67c3d-163">Bæta skorðu á segð við afbrigðalíkan afurðar</span><span class="sxs-lookup"><span data-stu-id="67c3d-163">Add an expression constraint to a product configuration model</span></span>](tasks/add-expression-constraint-product-configuration-model.md)
- [<span data-ttu-id="67c3d-164">Yfirlit afbrigðalíkön afurðar</span><span class="sxs-lookup"><span data-stu-id="67c3d-164">Product configuration models overview</span></span>](product-configuration-models.md)
