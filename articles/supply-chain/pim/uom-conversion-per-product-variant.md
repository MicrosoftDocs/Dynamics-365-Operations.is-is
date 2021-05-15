---
title: Umreikningur mælieiningar eftir afurðarafbrigði
description: Þetta efnisatriði útskýrir hvernig á að setja upp umreikning mælieiningar fyrir afurðarafbrigði. Dæmi um uppsetninguna fylgir með.
author: johanhoffmann
ms.date: 05/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: UnitOfMeasureConversion
ROBOTS: noindex, nofollow
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-04-01
ms.dyn365.ops.version: 10
ms.openlocfilehash: ed28928b0f07833d5906a68f780e3bb5bbe0bfe9
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921218"
---
# <a name="unit-of-measure-conversion-per-product-variant"></a><span data-ttu-id="169be-104">Umreikningur mælieiningar eftir afurðarafbrigði</span><span class="sxs-lookup"><span data-stu-id="169be-104">Unit of measure conversion per product variant</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="169be-105">Þetta efnisatriði útskýrir hvernig á að setja upp umreikning mælieiningar fyrir ýmis afurðarafbrigði.</span><span class="sxs-lookup"><span data-stu-id="169be-105">This topic explains how to set up unit of measure conversions for various product variants.</span></span>

<span data-ttu-id="169be-106">Í stað þess að búa til margar stakar afurðir sem þarf að vinna með er hægt að nota afurðarafbrigði til að búa til afbrigði af einni afurð.</span><span class="sxs-lookup"><span data-stu-id="169be-106">Instead of creating multiple individual products that must be maintained, you can use product variants to create variations of a single product.</span></span> <span data-ttu-id="169be-107">Til dæmis gæti afurðarafbrigðið verið stuttermabolur af tiltekinni stærð og lit.</span><span class="sxs-lookup"><span data-stu-id="169be-107">For example, a product variant might be a T-shirt of a given size and color.</span></span>

<span data-ttu-id="169be-108">Áður var aðeins hægt að setja umreikning eininga upp á afurðarsniðmáti.</span><span class="sxs-lookup"><span data-stu-id="169be-108">Previously, unit conversions could be set up only on the product master.</span></span> <span data-ttu-id="169be-109">Þess vegna voru öll afurðarafbrigði með sömu umreikningsreglur einingar.</span><span class="sxs-lookup"><span data-stu-id="169be-109">Therefore, all product variants had the same unit conversion rules.</span></span> <span data-ttu-id="169be-110">Hins vegar þegar kveikt er á *Umreikningur mælieiningar fyrir afurðarafbrigði*, ef stuttermabolirnir eru seldir í kössum, og fjöldi stuttermabola sem hægt er að pakka í kassa fer eftir stærð stuttermabolanna, er hægt að setja upp umreikning eininga á milli mismunandi bolastærða og kassa sem notaðir eru sem umbúðir.</span><span class="sxs-lookup"><span data-stu-id="169be-110">However, when the *Unit of measure conversions for product variants* feature is turned on, if your T-shirts are sold in boxes, and the number of T-shirts that can be packed in a box depends on the size of the T-shirts, you can now set up unit conversions between the different shirt sizes and the boxes that are used for packaging.</span></span>

## <a name="turn-on-the-feature-in-your-system"></a><span data-ttu-id="169be-111">Kveikja á eiginleikanum í kerfinu</span><span class="sxs-lookup"><span data-stu-id="169be-111">Turn on the feature in your system</span></span>

<span data-ttu-id="169be-112">Ef þessi eiginleiki er ekki þegar til staðar í kerfinu skal fara á [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), og kveikja á *Umreikningur mælieiningar fyrir afurðarafbrigði*.</span><span class="sxs-lookup"><span data-stu-id="169be-112">If you don't already see this feature in your system, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), and turn on the *Unit of measure conversions for product variants* feature.</span></span>

## <a name="set-up-a-product-for-unit-conversion-per-variant"></a><span data-ttu-id="169be-113">Setja upp afurð fyrir umreikning einingar fyrir hvert afbrigði</span><span class="sxs-lookup"><span data-stu-id="169be-113">Set up a product for unit conversion per variant</span></span>

<span data-ttu-id="169be-114">Aðeins er hægt að stofna afurðarafbrigði fyrir afurðir sem eru afurðarsniðmát.</span><span class="sxs-lookup"><span data-stu-id="169be-114">Product variants can be created only for products that are product masters.</span></span> <span data-ttu-id="169be-115">Nánari upplýsingar er að finna í [Stofna afurðarsniðmát](tasks/create-product-master.md).</span><span class="sxs-lookup"><span data-stu-id="169be-115">For more information, see [Create a product master](tasks/create-product-master.md).</span></span> <span data-ttu-id="169be-116">*Umreikningur mælieiningar fyrir afurðarafbrigði* er ekki tiltækur fyrir afurðir sem eru settar upp fyrir ferli fyrir þyngd afurðar.</span><span class="sxs-lookup"><span data-stu-id="169be-116">The *Unit of measure conversions for product variants* feature isn't available for products that are set up for catch-weight processes.</span></span>

<span data-ttu-id="169be-117">Til að skilgreina afurðarsniðmát til að styðja umbreytingu eininga á hvert afbrigði skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="169be-117">To configure a product master to support unit conversion per variant, follow these steps.</span></span>

1. <span data-ttu-id="169be-118">Opna **upplýsingar um afurðastjórnun \> Afurðir \> Afurðarsniðmát**.</span><span class="sxs-lookup"><span data-stu-id="169be-118">Go to **Product information management \> Products \> Product masters**.</span></span>
1. <span data-ttu-id="169be-119">Stofna eða opna afurðarsniðmát til að fara á **Upplýsingar um afurð**-síðuna.</span><span class="sxs-lookup"><span data-stu-id="169be-119">Create or open a product master to go to its **Product details** page.</span></span>
1. <span data-ttu-id="169be-120">Stilltu **Virkja umreikning mælieiningar** á *Já*.</span><span class="sxs-lookup"><span data-stu-id="169be-120">Set the **Enable unit of measure conversions** option to *Yes*.</span></span>
1. <span data-ttu-id="169be-121">Á aðgerðarúðunni á flipanum **Afurð** í flokknum **Uppsetning** skal velja **Umreikningur eininga**.</span><span class="sxs-lookup"><span data-stu-id="169be-121">On the Action Pane, on the **Product** tab, in the **Set up** group, select **Unit conversions**.</span></span>
1. <span data-ttu-id="169be-122">**Umreikningur eininga** síðan opnast.</span><span class="sxs-lookup"><span data-stu-id="169be-122">The **Unit conversions** page opens.</span></span> <span data-ttu-id="169be-123">Velja einn af eftirfarandi flipum:</span><span class="sxs-lookup"><span data-stu-id="169be-123">Select one of the following tabs:</span></span>

    - <span data-ttu-id="169be-124">**Umreikningur innan flokks** – Veljið þennan flipa til að umbreyta á milli eininga sem tilheyra sama mælieiningaflokki.</span><span class="sxs-lookup"><span data-stu-id="169be-124">**Intra-class conversions** – Select this tab to convert between units that belong to the same unit class.</span></span>
    - <span data-ttu-id="169be-125">**Umreikningur milli flokka** – Veljið þennan flipa til að umbreyta á milli eininga sem tilheyra mismunandi mælieiningaflokkum.</span><span class="sxs-lookup"><span data-stu-id="169be-125">**Inter-class conversions** – Select this tab to convert between units that belong to different unit classes.</span></span>

1. <span data-ttu-id="169be-126">Ef bæta á nýrri einingu við er smellt á **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="169be-126">Select **New** to add a new unit conversion.</span></span>
1. <span data-ttu-id="169be-127">Stillið **Búa til umreikning fyrir** reitinn á eitt af eftirfarandi gildum:</span><span class="sxs-lookup"><span data-stu-id="169be-127">Set the **Create conversion for** field to one of the following values:</span></span>

    - <span data-ttu-id="169be-128">**Afurð** – Ef þú velur þetta gildi getur þú sett upp umreikning eininga fyrir afurðarsniðmát.</span><span class="sxs-lookup"><span data-stu-id="169be-128">**Product** – If you select this value, you can set up a unit conversion for the product master.</span></span> <span data-ttu-id="169be-129">Þessi umreikningur eininga verður notaður til vara fyrir öll afurðarafbrigði sem enginn umreikningur eininga er skilgreindur fyrir.</span><span class="sxs-lookup"><span data-stu-id="169be-129">That unit conversion will be used as a fallback for all product variants that no unit conversion is defined for.</span></span>
    - <span data-ttu-id="169be-130">**Afurðarafbrigði** – ef þetta gildi er valið er hægt að setja upp umreikning eininga fyrir tilgreint afurðarafbrigði.</span><span class="sxs-lookup"><span data-stu-id="169be-130">**Product variant** – If you select this value, you can set up a unit conversion for a specific product variant.</span></span> <span data-ttu-id="169be-131">Notaðu reitinn **Afurðarafbrigði** til að velja afbrigðið.</span><span class="sxs-lookup"><span data-stu-id="169be-131">Use the **Product variant** field to select the variant.</span></span>

    <span data-ttu-id="169be-132">![Nýjum umreikningi eininga bætt við](media/uom-new-conversion.png "Nýjum umreikningi eininga bætt við")</span><span class="sxs-lookup"><span data-stu-id="169be-132">![Adding a new unit conversion](media/uom-new-conversion.png "Adding a new unit conversion")</span></span>

1. <span data-ttu-id="169be-133">Notaðu önnur svæði sem eru gefin upp til að setja upp umreikning eininga.</span><span class="sxs-lookup"><span data-stu-id="169be-133">Use the other fields that are provided to set up your unit conversion.</span></span>
1. <span data-ttu-id="169be-134">Veljið **Í lagi** til að vista nýja umreikning eininga.</span><span class="sxs-lookup"><span data-stu-id="169be-134">Select **OK** to save the new unit conversion.</span></span>

> [!TIP]
> <span data-ttu-id="169be-135">Hægt er að opna **Umreikningur eininga** síðu afurðar eða afurðarafbrigðis af einhverri eftirfarandi síðna:</span><span class="sxs-lookup"><span data-stu-id="169be-135">You can open the **Unit conversions** page for a product or a product variant from any of the following pages:</span></span>
> 
> - <span data-ttu-id="169be-136">Upplýsingar um afurð</span><span class="sxs-lookup"><span data-stu-id="169be-136">Product details</span></span>
> - <span data-ttu-id="169be-137">Upplýsingar um losaðar afurðir</span><span class="sxs-lookup"><span data-stu-id="169be-137">Released products details</span></span>
> - <span data-ttu-id="169be-138">Útgefin afurðarafbrigði</span><span class="sxs-lookup"><span data-stu-id="169be-138">Released product variants</span></span>

## <a name="example-scenario"></a><span data-ttu-id="169be-139">Dæmi</span><span class="sxs-lookup"><span data-stu-id="169be-139">Example scenario</span></span>

<span data-ttu-id="169be-140">Í þessu tilviki selur fyrirtæki stuttermaboli í eftirfarandi stærðum: litlir, miðlungs, stórir og mjög stórir.</span><span class="sxs-lookup"><span data-stu-id="169be-140">In this scenario, a company sells T-shirts in sizes small, medium, large, and extra-large.</span></span> <span data-ttu-id="169be-141">Stuttermabolur er skilgreindur sem afurð og mismunandi stærðir eru skilgreindar sem afbrigði af afurðinni.</span><span class="sxs-lookup"><span data-stu-id="169be-141">The T-shirt is defined as a product, and the different sizes are defined as variants of that product.</span></span> <span data-ttu-id="169be-142">Bolirnir eru pakkaðir í kössum.</span><span class="sxs-lookup"><span data-stu-id="169be-142">The shirts are packed in boxes.</span></span> <span data-ttu-id="169be-143">Fyrir stærðir lítill, meðalstór og stór geta verið fimm bolir í hverjum kassa.</span><span class="sxs-lookup"><span data-stu-id="169be-143">For sizes small, medium, and large, there can be five shirts in each box.</span></span> <span data-ttu-id="169be-144">Hins vegar, fyrir mjög stóra, er ekki til pláss nema fyrir fjóra boli í hverjum kassa.</span><span class="sxs-lookup"><span data-stu-id="169be-144">However, for size extra-large, there is space for only four shirts in each box.</span></span>

<span data-ttu-id="169be-145">Fyrirtækið vill rekja mismunandi afbrigði í einingunni *Stykki*, en það selur þær í einingunni *Kassar*.</span><span class="sxs-lookup"><span data-stu-id="169be-145">The company wants to track the different variants in the *Pieces* unit, but it's selling them in the *Boxes* unit.</span></span> <span data-ttu-id="169be-146">Fyrir stærðir lítill, miðlungs og stór er umreikningur milli birgðaeiningar og sölueiningar 1 kassi = 5 stykki.</span><span class="sxs-lookup"><span data-stu-id="169be-146">For sizes small, medium, and large, the conversion between the inventory unit and the sales unit is 1 Box = 5 Pieces.</span></span> <span data-ttu-id="169be-147">Fyrir stærð mjög stór er umreikningurinn 1 kassi = 4 stykki.</span><span class="sxs-lookup"><span data-stu-id="169be-147">For size extra-large, the conversion is 1 Box = 4 Pieces.</span></span>

1. <span data-ttu-id="169be-148">Á síðunni **Upplýsingar um losaðar afurðir** fyrir vöruna **Stuttermabolir** opnaðu síðuna **Umreikningur eininga**.</span><span class="sxs-lookup"><span data-stu-id="169be-148">From the **Released product details** page for the **T-Shirt** product, open the **Unit conversions** page.</span></span>
1. <span data-ttu-id="169be-149">Á síðunni **Umreikningur eininga** skal setja upp eftirfarandi umreikning eininga fyrir útgefna afurðarafbrigðið **Mjög stór**.</span><span class="sxs-lookup"><span data-stu-id="169be-149">On the **Unit conversions** page, set up the following unit conversion for the **X-Large** released product variant.</span></span>

    | <span data-ttu-id="169be-150">Svæði</span><span class="sxs-lookup"><span data-stu-id="169be-150">Field</span></span>                 | <span data-ttu-id="169be-151">Stilling</span><span class="sxs-lookup"><span data-stu-id="169be-151">Setting</span></span>                 |
    |-----------------------|-------------------------|
    | <span data-ttu-id="169be-152">Búa til umskráningu fyrir</span><span class="sxs-lookup"><span data-stu-id="169be-152">Create conversion for</span></span> | <span data-ttu-id="169be-153">Afurðarafbrigði</span><span class="sxs-lookup"><span data-stu-id="169be-153">Product variant</span></span>         |
    | <span data-ttu-id="169be-154">Afurðarafbrigði</span><span class="sxs-lookup"><span data-stu-id="169be-154">Product variant</span></span>       | <span data-ttu-id="169be-155">Stuttermabolur : : Mjög stór : :</span><span class="sxs-lookup"><span data-stu-id="169be-155">T-Shirt : : X-Large : :</span></span> |
    | <span data-ttu-id="169be-156">Frá einingu</span><span class="sxs-lookup"><span data-stu-id="169be-156">From unit</span></span>             | <span data-ttu-id="169be-157">Kassar</span><span class="sxs-lookup"><span data-stu-id="169be-157">Boxes</span></span>                   |
    | <span data-ttu-id="169be-158">Stuðull</span><span class="sxs-lookup"><span data-stu-id="169be-158">Factor</span></span>                | <span data-ttu-id="169be-159">4</span><span class="sxs-lookup"><span data-stu-id="169be-159">4</span></span>                       |
    | <span data-ttu-id="169be-160">Til einingar</span><span class="sxs-lookup"><span data-stu-id="169be-160">To Unit</span></span>               | <span data-ttu-id="169be-161">Stykki</span><span class="sxs-lookup"><span data-stu-id="169be-161">Pieces</span></span>                  |

1. <span data-ttu-id="169be-162">Útgefnu afurðarafbrigðin **Lítill**, **Miðlungs** og **Stór** eru með sama umreikning eininga milli eininganna *Kassi* og *Stykki*, sem þýðir að hægt er að skilgreina umreikning eininga fyrir þessi afurðarafbrigði í afurðarsniðmátinu.</span><span class="sxs-lookup"><span data-stu-id="169be-162">Because the **Small**, **Medium**, and **Large** product variants all have the same unit conversion between the *Box* and *Pieces* units, you can define the following unit conversion for them on the product master.</span></span>

    | <span data-ttu-id="169be-163">Svæði</span><span class="sxs-lookup"><span data-stu-id="169be-163">Field</span></span>                 | <span data-ttu-id="169be-164">Stilling</span><span class="sxs-lookup"><span data-stu-id="169be-164">Setting</span></span> |
    |-----------------------|---------|
    | <span data-ttu-id="169be-165">Búa til umskráningu fyrir</span><span class="sxs-lookup"><span data-stu-id="169be-165">Create conversion for</span></span> | <span data-ttu-id="169be-166">Afurð</span><span class="sxs-lookup"><span data-stu-id="169be-166">Product</span></span> |
    | <span data-ttu-id="169be-167">Afurð</span><span class="sxs-lookup"><span data-stu-id="169be-167">Product</span></span>               | <span data-ttu-id="169be-168">Stuttermabolur</span><span class="sxs-lookup"><span data-stu-id="169be-168">T-Shirt</span></span> |
    | <span data-ttu-id="169be-169">Frá einingu</span><span class="sxs-lookup"><span data-stu-id="169be-169">From unit</span></span>             | <span data-ttu-id="169be-170">Kassar</span><span class="sxs-lookup"><span data-stu-id="169be-170">Boxes</span></span>   |
    | <span data-ttu-id="169be-171">Stuðull</span><span class="sxs-lookup"><span data-stu-id="169be-171">Factor</span></span>                | <span data-ttu-id="169be-172">5</span><span class="sxs-lookup"><span data-stu-id="169be-172">5</span></span>       |
    | <span data-ttu-id="169be-173">Til einingar</span><span class="sxs-lookup"><span data-stu-id="169be-173">To Unit</span></span>               | <span data-ttu-id="169be-174">Stykki</span><span class="sxs-lookup"><span data-stu-id="169be-174">Pieces</span></span>  |

## <a name="using-excel-to-update-the-unit-conversions"></a><span data-ttu-id="169be-175">Nota Excel til að uppfæra umreikning eininga</span><span class="sxs-lookup"><span data-stu-id="169be-175">Using Excel to update the unit conversions</span></span>

<span data-ttu-id="169be-176">Ef afurð er með mörg afurðarafbrigði með mismunandi umreikningum eininga, er góð hugmynd að flytja út umreikninga eininga í Microsoft Excel vinnubók, uppfæra umreikningana, og síðan senda þá til baka til Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="169be-176">If a product has many product variants that have different unit conversions, it's a good idea to export the unit conversions to a Microsoft Excel workbook, update them, and then publish them back to Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="169be-177">Til að flytja út umreikninga eininga í Excel, á síðunni **Umreikningur eininga**, í aðgerðasvæði, skal velja **Opna í Microsoft Office**.</span><span class="sxs-lookup"><span data-stu-id="169be-177">To export unit conversions to Excel, on the **Unit conversions** page, on the Action Pane, select **Open in Microsoft Office**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="169be-178">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="169be-178">Additional resources</span></span>

[<span data-ttu-id="169be-179">Stjórna mælieiningum</span><span class="sxs-lookup"><span data-stu-id="169be-179">Manage units of measure</span></span>](tasks/manage-unit-measure.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]