---
title: Stofna nafnakerfi afurðarnúmers fyrir skilgreind afurðarafbrigði
description: Þetta ferli sýnir hvernig á að setja inn nafnakerfi afurðarnúmers fyrir skilgreind afurðarafbrigði og hvernig hægt er að tengja það við skilgreinanlegt afurðarsniðmát.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductListPage, EcoResProductDetails, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7ea30dc107213b1a2c6b2a109188066a6ea82159
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921012"
---
# <a name="create-a-product-number-nomenclature-for-configured-product-variants"></a><span data-ttu-id="1d458-103">Stofna nafnakerfi afurðarnúmers fyrir skilgreind afurðarafbrigði</span><span class="sxs-lookup"><span data-stu-id="1d458-103">Create a product number nomenclature for configured product variants</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1d458-104">Þetta ferli sýnir hvernig á að setja inn nafnakerfi afurðarnúmers fyrir skilgreind afurðarafbrigði og hvernig hægt er að tengja það við skilgreinanlegt afurðarsniðmát.</span><span class="sxs-lookup"><span data-stu-id="1d458-104">This procedure shows you how to set up a product number nomenclature for configured product variants, and how it can be attached to a configurable product master.</span></span> <span data-ttu-id="1d458-105">Þetta ferli sýnir einnig hvernig hægt er að byggja upp skilgreiningu nafnakerfis fyrir íhlut afbrigðalíkans afurðar.</span><span class="sxs-lookup"><span data-stu-id="1d458-105">This procedure also demonstrates how you can build a configuration nomenclature for a product configuration model component.</span></span> <span data-ttu-id="1d458-106">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="1d458-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="1d458-107">Nýju afurðarnúmeri nafnakerfis er úthlutað á afurðarsniðmátið D0004.</span><span class="sxs-lookup"><span data-stu-id="1d458-107">The new product number nomenclature is assigned to the D0004 product master.</span></span> <span data-ttu-id="1d458-108">Þetta verk myndi yfirleitt vera framkvæmt af hálfu vöruhönnuðar.</span><span class="sxs-lookup"><span data-stu-id="1d458-108">This task would typically be done by a product designer.</span></span>

## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="1d458-109">Stofnaðu Nafnakerfi afurðarnúmers</span><span class="sxs-lookup"><span data-stu-id="1d458-109">Create a product number nomenclature</span></span>

1. <span data-ttu-id="1d458-110">Farið í **Afurðaupplýsingastjórnun \> Uppsetning \> Nafnakerfi afurðar**.</span><span class="sxs-lookup"><span data-stu-id="1d458-110">Go to **Product information management \> Setup \> Product nomenclature**.</span></span>
1. <span data-ttu-id="1d458-111">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="1d458-111">Select **New**.</span></span>
1. <span data-ttu-id="1d458-112">Í reitinn **Heiti** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="1d458-112">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="1d458-113">Í reitinn **Lýsing** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="1d458-113">In the **Description** field, type a value.</span></span>
1. <span data-ttu-id="1d458-114">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="1d458-114">Select **Add**.</span></span>
1. <span data-ttu-id="1d458-115">Veljið **Númer afurðarsniðmáts**.</span><span class="sxs-lookup"><span data-stu-id="1d458-115">Select **Product master number**.</span></span>
1. <span data-ttu-id="1d458-116">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="1d458-116">Select **Add**.</span></span>
1. <span data-ttu-id="1d458-117">Veldu **Textafasta**.</span><span class="sxs-lookup"><span data-stu-id="1d458-117">Select **Text constant**.</span></span>
1. <span data-ttu-id="1d458-118">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="1d458-118">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="1d458-119">Í reitnum **Texti** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="1d458-119">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="1d458-120">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="1d458-120">Select **Add**.</span></span>
1. <span data-ttu-id="1d458-121">Veljið **Skilgreining**.</span><span class="sxs-lookup"><span data-stu-id="1d458-121">Select **Configuration**.</span></span>
1. <span data-ttu-id="1d458-122">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="1d458-122">Close the page.</span></span>

## <a name="assign-the-product-number-nomenclature-to-a-product-master"></a><span data-ttu-id="1d458-123">Úthlutaðu nafnakerfi afurðarnúmers á afurðarsniðmát</span><span class="sxs-lookup"><span data-stu-id="1d458-123">Assign the product number nomenclature to a product master</span></span>

1. <span data-ttu-id="1d458-124">Opna **upplýsingar um afurðastjórnun \> Afurðir \> Afurðarsniðmát**.</span><span class="sxs-lookup"><span data-stu-id="1d458-124">Go to **Product information management \> Products \> Product masters**.</span></span>
1. <span data-ttu-id="1d458-125">Nota flýtiafmörkun til að finna færslur</span><span class="sxs-lookup"><span data-stu-id="1d458-125">Use the Quick Filter to find records.</span></span> <span data-ttu-id="1d458-126">Til dæmis, sía reitinn **Vörunúmer** með gildið ‚D'.</span><span class="sxs-lookup"><span data-stu-id="1d458-126">For example, filter on the **Product number** field with a value of 'D'.</span></span>
1. <span data-ttu-id="1d458-127">Í listanum skal velja tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="1d458-127">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="1d458-128">Veljið **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="1d458-128">Select **Edit**.</span></span>
1. <span data-ttu-id="1d458-129">Veldu *Já* í reitnum **Nota nafnakerfi**.</span><span class="sxs-lookup"><span data-stu-id="1d458-129">Select *Yes* in the **Use nomenclature** field.</span></span>
1. <span data-ttu-id="1d458-130">Í reitnum **Nafnakerfi afurðarafbrigðisnúmers** skal færa inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="1d458-130">In the **Product variant number nomenclature** field, enter or select a value.</span></span>
1. <span data-ttu-id="1d458-131">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="1d458-131">Close the page.</span></span>
1. <span data-ttu-id="1d458-132">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="1d458-132">Close the page.</span></span>

## <a name="create-nomenclature-for-a-product-configuration-model-component"></a><span data-ttu-id="1d458-133">Stofnaðu nafnakerfi fyrir íhlut afbrigðalíkans afurðar</span><span class="sxs-lookup"><span data-stu-id="1d458-133">Create nomenclature for a product configuration model component</span></span>

1. <span data-ttu-id="1d458-134">Farið í **Afurðarupplýsingastjórnun \> Afurðir \> Afbrigðalíkön afurða**.</span><span class="sxs-lookup"><span data-stu-id="1d458-134">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="1d458-135">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="1d458-135">In the list, find and select the desired record.</span></span>
1. <span data-ttu-id="1d458-136">Í listanum skal velja tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="1d458-136">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="1d458-137">Veljið **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="1d458-137">Select **Edit**.</span></span>
1. <span data-ttu-id="1d458-138">Velja skal *Já* í reitnum **Nota nafnakerfi skilgreiningar**.</span><span class="sxs-lookup"><span data-stu-id="1d458-138">Select *Yes* in the **Use configuration nomenclature** field.</span></span>
1. <span data-ttu-id="1d458-139">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="1d458-139">Select **Add**.</span></span>
1. <span data-ttu-id="1d458-140">Veljið **Eigindargildi**.</span><span class="sxs-lookup"><span data-stu-id="1d458-140">Select **Attribute value**.</span></span>
1. <span data-ttu-id="1d458-141">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="1d458-141">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="1d458-142">Sláið inn eða veldu gildi í reitnum **Eigind**.</span><span class="sxs-lookup"><span data-stu-id="1d458-142">In the **Attribute** field, enter or select a value.</span></span>
1. <span data-ttu-id="1d458-143">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="1d458-143">Select **Add**.</span></span>
1. <span data-ttu-id="1d458-144">Veldu **Textafasta**.</span><span class="sxs-lookup"><span data-stu-id="1d458-144">Select **Text constant**.</span></span>
1. <span data-ttu-id="1d458-145">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="1d458-145">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="1d458-146">Í reitnum **Texti** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="1d458-146">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="1d458-147">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="1d458-147">Select **Add**.</span></span>
1. <span data-ttu-id="1d458-148">Veljið **Eigindargildi**.</span><span class="sxs-lookup"><span data-stu-id="1d458-148">Select **Attribute value**.</span></span>
1. <span data-ttu-id="1d458-149">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="1d458-149">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="1d458-150">Sláið inn eða veldu gildi í reitnum **Eigind**.</span><span class="sxs-lookup"><span data-stu-id="1d458-150">In the **Attribute** field, enter or select a value.</span></span>
1. <span data-ttu-id="1d458-151">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="1d458-151">Select **Add**.</span></span>
1. <span data-ttu-id="1d458-152">Veldu **Textafasta**.</span><span class="sxs-lookup"><span data-stu-id="1d458-152">Select **Text constant**.</span></span>
1. <span data-ttu-id="1d458-153">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="1d458-153">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="1d458-154">Í reitnum **Texti** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="1d458-154">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="1d458-155">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="1d458-155">Select **Add**.</span></span>
1. <span data-ttu-id="1d458-156">Veljið **Eigindargildi**.</span><span class="sxs-lookup"><span data-stu-id="1d458-156">Select **Attribute value**.</span></span>
1. <span data-ttu-id="1d458-157">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="1d458-157">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="1d458-158">Sláið inn eða veldu gildi í reitnum **Eigind**.</span><span class="sxs-lookup"><span data-stu-id="1d458-158">In the **Attribute** field, enter or select a value.</span></span>
1. <span data-ttu-id="1d458-159">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="1d458-159">Select **Add**.</span></span>
1. <span data-ttu-id="1d458-160">Veldu **Textafasta**.</span><span class="sxs-lookup"><span data-stu-id="1d458-160">Select **Text constant**.</span></span>
1. <span data-ttu-id="1d458-161">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="1d458-161">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="1d458-162">Í reitnum **Texti** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="1d458-162">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="1d458-163">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="1d458-163">Select **Add**.</span></span>
1. <span data-ttu-id="1d458-164">Veljið **Eigindargildi**.</span><span class="sxs-lookup"><span data-stu-id="1d458-164">Select **Attribute value**.</span></span>
1. <span data-ttu-id="1d458-165">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="1d458-165">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="1d458-166">Sláið inn eða veldu gildi í reitnum **Eigind**.</span><span class="sxs-lookup"><span data-stu-id="1d458-166">In the **Attribute** field, enter or select a value.</span></span>
1. <span data-ttu-id="1d458-167">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="1d458-167">Select **Add**.</span></span>
1. <span data-ttu-id="1d458-168">Veldu **Textafasta**.</span><span class="sxs-lookup"><span data-stu-id="1d458-168">Select **Text constant**.</span></span>
1. <span data-ttu-id="1d458-169">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="1d458-169">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="1d458-170">Í reitnum **Texti** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="1d458-170">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="1d458-171">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="1d458-171">Select **Add**.</span></span>
1. <span data-ttu-id="1d458-172">Veljið **Gildi númeraraðar**.</span><span class="sxs-lookup"><span data-stu-id="1d458-172">Select **Number sequence value**.</span></span>
1. <span data-ttu-id="1d458-173">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="1d458-173">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="1d458-174">Sláið inn eða veldu gildi í reitnum **Númeraröð**.</span><span class="sxs-lookup"><span data-stu-id="1d458-174">In the **Number sequence** field, enter or select a value.</span></span>
1. <span data-ttu-id="1d458-175">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="1d458-175">Close the page.</span></span>
1. <span data-ttu-id="1d458-176">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="1d458-176">Close the page.</span></span>
1. <span data-ttu-id="1d458-177">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="1d458-177">Close the page.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]