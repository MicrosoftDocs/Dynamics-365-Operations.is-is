---
title: Mælieiningarumreikningur á afurðarafbrigði
description: Í þessu efnisatriði er fjallað um hvernig hægt er að setja upp mælieiningarumreikninga fyrir afurðarafbrigði.
author: johanhoffmann
manager: tfehr
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: UnitOfMeasureConversion
ROBOTS: noindex, nofollow
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-04-01
ms.dyn365.ops.version: 10
ms.openlocfilehash: e50be7fa6fa686a90b2dd5c5200c881e4629f019
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204494"
---
# <a name="unit-of-measure-conversion-per-product-variant"></a><span data-ttu-id="b1cbd-103">Mælieiningarumreikningur á afurðarafbrigði</span><span class="sxs-lookup"><span data-stu-id="b1cbd-103">Unit of measure conversion per product variant</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b1cbd-104">Í þessu efnisatriði er fjallað um hvernig hægt er að setja upp mælieiningarumreikninga fyrir afurðarafbrigði.</span><span class="sxs-lookup"><span data-stu-id="b1cbd-104">This topic explains how unit of measure conversions can be set up on product variants.</span></span> <span data-ttu-id="b1cbd-105">Dæmi um uppsetninguna fylgir með.</span><span class="sxs-lookup"><span data-stu-id="b1cbd-105">It includes an example of the setup.</span></span>

<span data-ttu-id="b1cbd-106">Þessi eiginleiki gerir fyrirtækjum kleift að skilgreina mismunandi umreikninga eininga milli afbrigða sömu afurðarinnar.</span><span class="sxs-lookup"><span data-stu-id="b1cbd-106">This feature makes it possible for companies to define different unit conversion between the variants of the same product.</span></span> <span data-ttu-id="b1cbd-107">Eftirfarandi dæmi er notað í þessu efnisatriði.</span><span class="sxs-lookup"><span data-stu-id="b1cbd-107">The following example is used in this topic.</span></span> <span data-ttu-id="b1cbd-108">Fyrirtæki selur stuttermaboli í eftirfarandi stærðum: litlir, miðlungs, stórir og mjög stórir.</span><span class="sxs-lookup"><span data-stu-id="b1cbd-108">A company sells T-shirts in sizes Small, Medium, Large, and Extra-Large.</span></span> <span data-ttu-id="b1cbd-109">Stuttermabolur er skilgreindur sem afurð og mismunandi stærðir eru skilgreindar sem afbrigði af vörunni.</span><span class="sxs-lookup"><span data-stu-id="b1cbd-109">The T-shirt is defined as a product, and the different sizes are defined as variants of the product.</span></span> <span data-ttu-id="b1cbd-110">Stuttermabolunum er pakkað í kassa og það geta verið fimm bolir í kassa, fyrir utan þá mjög stóru þar sem aðeins er pláss fyrir fjóra boli.</span><span class="sxs-lookup"><span data-stu-id="b1cbd-110">The T-shirts are packed in boxes and there can be five T-shirts in a box, except for the Extra-Large size where there is only space for four T-shirts.</span></span> <span data-ttu-id="b1cbd-111">Fyrirtækið vill rekja ólík afbrigði af stuttermabolunum í einingunni **Stykki** en selur bolina í einingunni **Kassar**.</span><span class="sxs-lookup"><span data-stu-id="b1cbd-111">The company wants to track the different variants of the T-shirts in the unit **Pieces** but is selling the T-shirts in the unit **Boxes**.</span></span> <span data-ttu-id="b1cbd-112">Umreikningur milli birgðaeiningar og sölueiningar er 1 kassi = 5 stykki, fyrir utan afbrigðið Mjög stór þar sem umreikningurinn er 1 kassi = 4 stykki.</span><span class="sxs-lookup"><span data-stu-id="b1cbd-112">The conversion between the inventory unit and the sales unit is 1 Box = 5 Pieces, except for the variant Extra-Large, where the conversion is 1 Box = 4 Pieces.</span></span>

### <a name="set-up-a-product-for-unit-conversion-per-variant"></a><span data-ttu-id="b1cbd-113">Setja upp afurð fyrir umreikning einingar fyrir hvert afbrigði</span><span class="sxs-lookup"><span data-stu-id="b1cbd-113">Set up a product for unit conversion per variant</span></span>

<span data-ttu-id="b1cbd-114">Aðeins er hægt að búa til afurðarafbrigði fyrir afurðir af **Undirgerð afurðar**: **Afurðarsniðmát**.</span><span class="sxs-lookup"><span data-stu-id="b1cbd-114">Product variants can only be created for products of **Product subtype**: **Product master**.</span></span> <span data-ttu-id="b1cbd-115">Nánari upplýsingar er að finna í [Stofna afurðarsniðmát](tasks/create-product-master.md).</span><span class="sxs-lookup"><span data-stu-id="b1cbd-115">For more information, see [Create a product master](tasks/create-product-master.md).</span></span>

<span data-ttu-id="b1cbd-116">Eiginleikinn er ekki virkjaður fyrir afurðir sem eru settar upp fyrir ferli framleiðsluþyngdar.</span><span class="sxs-lookup"><span data-stu-id="b1cbd-116">The feature is not enabled for products that are set up for Catch Weight processes.</span></span> 

<span data-ttu-id="b1cbd-117">Þegar afurðarsniðmát með útgefnum afurðarafbrigðum er búið til, er hægt að setja upp umreikninga eininga fyrir hvert afbrigði.</span><span class="sxs-lookup"><span data-stu-id="b1cbd-117">When the product master with released products variants is created, unit conversions per variants can be set up.</span></span> <span data-ttu-id="b1cbd-118">Hægt er að finna valmyndaratriðið til að opna síðu fyrir umreikning eininga í samhengi við afurð eða afurðarafbrigði á eftirfarandi síðum.</span><span class="sxs-lookup"><span data-stu-id="b1cbd-118">You can find the menu item for opening the unit conversion page in context of a product or a product variant on the following pages.</span></span>

-   <span data-ttu-id="b1cbd-119">Síðan **Upplýsingar um afurð**</span><span class="sxs-lookup"><span data-stu-id="b1cbd-119">**Product details** page</span></span>
-   <span data-ttu-id="b1cbd-120">Síðan **Upplýsingar um útgefnar afurðar**</span><span class="sxs-lookup"><span data-stu-id="b1cbd-120">**Released products details** page</span></span>
-   <span data-ttu-id="b1cbd-121">Síðan **Útgefin afurðarafbrigði**</span><span class="sxs-lookup"><span data-stu-id="b1cbd-121">**Released product variants** page</span></span>

<span data-ttu-id="b1cbd-122">Þegar þú opnar síðuna **Umreikningur eininga** í samhengi við afurðarsniðmát eða útgefið afurðarafbrigði getur þú valið hvort þú vilt setja upp umreikning eininga fyrir afurðina eða fyrir afurðarafbrigðið.</span><span class="sxs-lookup"><span data-stu-id="b1cbd-122">When you open the **Unit conversion** page in context of a product master or released product variant, you can select if you want to set up the unit conversion for the product or for a product variant.</span></span> <span data-ttu-id="b1cbd-123">Þú gerir það með því að velja annaðhvort **Afurðarafbrigði** eða **Afurð** í reitnum **Búa til umreikning fyrir**.</span><span class="sxs-lookup"><span data-stu-id="b1cbd-123">You do that by selecting either **Product variant** or **Product** in the **Create conversion for** field.</span></span>

### <a name="product-variant"></a><span data-ttu-id="b1cbd-124">Afurðarafbrigði</span><span class="sxs-lookup"><span data-stu-id="b1cbd-124">Product variant</span></span>

<span data-ttu-id="b1cbd-125">Ef þú velur **Afurðarafbrigði** getur þú valið fyrir hvaða afbrigði þú vilt setja upp umreikning eininga í reitnum **Afurðarafbrigði**.</span><span class="sxs-lookup"><span data-stu-id="b1cbd-125">If you select **Product variant,** then you can select for which variant you want to set up the unit conversion in the **Product variant** field.</span></span>

### <a name="product"></a><span data-ttu-id="b1cbd-126">Afurð</span><span class="sxs-lookup"><span data-stu-id="b1cbd-126">Product</span></span>

<span data-ttu-id="b1cbd-127">Ef þú velur **Afurð** getur þú sett upp umreikning eininga fyrir afurðarsniðmát.</span><span class="sxs-lookup"><span data-stu-id="b1cbd-127">If you select **Product**, then you can set up a unit conversion for the product master.</span></span> <span data-ttu-id="b1cbd-128">Þessi umreikningur eininga á við um öll afurðarafbrigði með engan skilgreindan umreikning eininga.</span><span class="sxs-lookup"><span data-stu-id="b1cbd-128">This unit conversion will apply for all product variants with no defined unit conversion.</span></span>

### <a name="example"></a><span data-ttu-id="b1cbd-129">Dæmi</span><span class="sxs-lookup"><span data-stu-id="b1cbd-129">Example</span></span>

<span data-ttu-id="b1cbd-130">Afurðarsniðmát, **Stuttermabolur**, er með fjögur útgefin afurðarafbrigði: Lítill, Miðlungs, Stór og Mjög stór.</span><span class="sxs-lookup"><span data-stu-id="b1cbd-130">A product master, **T-Shirt**, has four released products variants Small, Medium, Large, and X-Large.</span></span> <span data-ttu-id="b1cbd-131">Stuttermabolunum er pakkað í kassa og það geta verið fimm bolir í kassa, fyrir utan þá Mjög stóru þar sem aðeins er pláss fyrir fjóra boli.</span><span class="sxs-lookup"><span data-stu-id="b1cbd-131">The T-shirts are packed in boxes and there can be five T-shirts in a box, except for the Extra-large size where there is only space for four T-shirts.</span></span>

<span data-ttu-id="b1cbd-132">Fyrst skaltu opna síðuna **Umreikningur eininga** á upplýsingasíðu útgefinna afurða fyrir **Stuttermabolir.**</span><span class="sxs-lookup"><span data-stu-id="b1cbd-132">First, open the **Unit conversion** page from the Release product details page for **T-shirt.**</span></span>

<span data-ttu-id="b1cbd-133">Á síðunni **Umreikningur eininga** skal setja upp umreikning eininga fyrir útgefna afurðarafbrigðið Mjög stór.</span><span class="sxs-lookup"><span data-stu-id="b1cbd-133">On the **Unit conversion** page, set up the unit conversion for the release product variant X-Large.</span></span>

| <span data-ttu-id="b1cbd-134">**Svæði**</span><span class="sxs-lookup"><span data-stu-id="b1cbd-134">**Field**</span></span>             | <span data-ttu-id="b1cbd-135">**Stilling**</span><span class="sxs-lookup"><span data-stu-id="b1cbd-135">**Setting**</span></span>             |
|-----------------------|-------------------------|
| <span data-ttu-id="b1cbd-136">Búa til umskráningu fyrir</span><span class="sxs-lookup"><span data-stu-id="b1cbd-136">Create conversion for</span></span> | <span data-ttu-id="b1cbd-137">Afurðarafbrigði</span><span class="sxs-lookup"><span data-stu-id="b1cbd-137">Product variant</span></span>         |
| <span data-ttu-id="b1cbd-138">Afurðarafbrigði</span><span class="sxs-lookup"><span data-stu-id="b1cbd-138">Product variant</span></span>       | <span data-ttu-id="b1cbd-139">Stuttermabolur : : Mjög stór : :</span><span class="sxs-lookup"><span data-stu-id="b1cbd-139">T-Shirt : : X-Large : :</span></span> |
| <span data-ttu-id="b1cbd-140">Frá einingu</span><span class="sxs-lookup"><span data-stu-id="b1cbd-140">From unit</span></span>             | <span data-ttu-id="b1cbd-141">Kassar</span><span class="sxs-lookup"><span data-stu-id="b1cbd-141">Boxes</span></span>                   |
| <span data-ttu-id="b1cbd-142">Stuðull</span><span class="sxs-lookup"><span data-stu-id="b1cbd-142">Factor</span></span>                | <span data-ttu-id="b1cbd-143">4</span><span class="sxs-lookup"><span data-stu-id="b1cbd-143">4</span></span>                       |
| <span data-ttu-id="b1cbd-144">Til einingar</span><span class="sxs-lookup"><span data-stu-id="b1cbd-144">To Unit</span></span>               | <span data-ttu-id="b1cbd-145">Stykki</span><span class="sxs-lookup"><span data-stu-id="b1cbd-145">Pieces</span></span>                  |

<span data-ttu-id="b1cbd-146">Útgefnu afurðarafbrigðin Lítill, Miðlungs og Stór eru með sama umreikning eininga milli eininganna Kassi og Stykki, sem þýðir að hægt er að skilgreina umreikning eininga fyrir þessi afurðarafbrigði í afurðarsniðmátinu.</span><span class="sxs-lookup"><span data-stu-id="b1cbd-146">The Released product variants Small, Medium, and Large have the same unit conversion between the unit Box and Pieces, which means that you can define the unit conversion for these product variants on the product master.</span></span>

| <span data-ttu-id="b1cbd-147">**Svæði**</span><span class="sxs-lookup"><span data-stu-id="b1cbd-147">**Field**</span></span>             | <span data-ttu-id="b1cbd-148">**Stilling**</span><span class="sxs-lookup"><span data-stu-id="b1cbd-148">**Setting**</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="b1cbd-149">Búa til umskráningu fyrir</span><span class="sxs-lookup"><span data-stu-id="b1cbd-149">Create conversion for</span></span> | <span data-ttu-id="b1cbd-150">Afurð</span><span class="sxs-lookup"><span data-stu-id="b1cbd-150">Product</span></span>     |
| <span data-ttu-id="b1cbd-151">Afurð</span><span class="sxs-lookup"><span data-stu-id="b1cbd-151">Product</span></span>               | <span data-ttu-id="b1cbd-152">Stuttermabolur</span><span class="sxs-lookup"><span data-stu-id="b1cbd-152">T-Shirt</span></span>     |
| <span data-ttu-id="b1cbd-153">Frá einingu</span><span class="sxs-lookup"><span data-stu-id="b1cbd-153">From unit</span></span>             | <span data-ttu-id="b1cbd-154">Kassar</span><span class="sxs-lookup"><span data-stu-id="b1cbd-154">Boxes</span></span>       |
| <span data-ttu-id="b1cbd-155">Stuðull</span><span class="sxs-lookup"><span data-stu-id="b1cbd-155">Factor</span></span>                | <span data-ttu-id="b1cbd-156">5</span><span class="sxs-lookup"><span data-stu-id="b1cbd-156">5</span></span>           |
| <span data-ttu-id="b1cbd-157">Til einingar</span><span class="sxs-lookup"><span data-stu-id="b1cbd-157">To Unit</span></span>               | <span data-ttu-id="b1cbd-158">Stykki</span><span class="sxs-lookup"><span data-stu-id="b1cbd-158">Pieces</span></span>      |

### <a name="using-excel-to-update-the-unit-conversions"></a><span data-ttu-id="b1cbd-159">Nota Excel til að uppfæra umreikning eininga</span><span class="sxs-lookup"><span data-stu-id="b1cbd-159">Using Excel to update the unit conversions</span></span>

<span data-ttu-id="b1cbd-160">Ef afurð er með mörg afurðarafbrigði með mismunandi umreikningum eininga, er góð hugmynd að flytja út umreikninga eininga úr síðunni **Umreikningur eininga** í Excel-töflureikni, uppfæra umreikningana, og síðan senda þá til baka til Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="b1cbd-160">If a product has many product variants with different unit conversions, it's a good idea to export the unit conversions from the **Unit conversion** page to an Excel spreadsheet, update the conversions, and then publish them back to Supply Chain Mangement.</span></span>

<span data-ttu-id="b1cbd-161">Valmöguleikinn að flytja út í Excel og senda breytingarnar aftur til Supply Chain Management er virkjuð í valmyndaratriðinu **Opna í Microsoft Office** í aðgerðarúðunni á síðunni **Umreikningur eininga**.</span><span class="sxs-lookup"><span data-stu-id="b1cbd-161">The option to export to Excel and publish the edits back to Supply Chain Mangement is enabled from the **Open in Microsoft office** menu item on the Action Pane on the **Unit conversion** page.</span></span>
