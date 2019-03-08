---
title: Mælieiningarumreikningur á afurðarafbrigði
description: Í þessu efnisatriði er fjallað um hvernig hægt er að setja upp mælieiningarumreikninga fyrir afurðarafbrigði.
author: johanhoffmann
manager: AnnBe
ms.date: 12/18/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
ROBOTS: noindex, nofollow
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-04-01
ms.dyn365.ops.version: 10
ms.openlocfilehash: 9d5d6fd65717cd886f1c6576aabf2bc59ca4fcaf
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "345928"
---
# <a name="unit-of-measure-conversion-per-product-variant"></a><span data-ttu-id="ff6c7-103">Mælieiningarumreikningur á afurðarafbrigði</span><span class="sxs-lookup"><span data-stu-id="ff6c7-103">Unit of measure conversion per product variant</span></span>

[!include [banner](../includes/banner.md)]

[!include [pivate-preview](../includes/pivate-preview-banner.md)]

<span data-ttu-id="ff6c7-104">Í þessu efnisatriði er fjallað um hvernig hægt er að setja upp mælieiningarumreikninga fyrir afurðarafbrigði.</span><span class="sxs-lookup"><span data-stu-id="ff6c7-104">This topic explains how unit of measure conversions can be set up on product variants.</span></span> <span data-ttu-id="ff6c7-105">Dæmi um uppsetninguna fylgir með.</span><span class="sxs-lookup"><span data-stu-id="ff6c7-105">It includes an example of the setup.</span></span>

<span data-ttu-id="ff6c7-106">Þessi eiginleiki gerir fyrirtækjum kleift að skilgreina mismunandi umreikninga eininga milli afbrigða sömu afurðarinnar.</span><span class="sxs-lookup"><span data-stu-id="ff6c7-106">This feature makes it possible for companies to define different unit conversion between the variants of the same product.</span></span> <span data-ttu-id="ff6c7-107">Eftirfarandi dæmi er notað í þessu efnisatriði.</span><span class="sxs-lookup"><span data-stu-id="ff6c7-107">The following example is used in this topic.</span></span> <span data-ttu-id="ff6c7-108">Fyrirtæki selur stuttermaboli í eftirfarandi stærðum: litlir, miðlungs, stórir og mjög stórir.</span><span class="sxs-lookup"><span data-stu-id="ff6c7-108">A company sells T-shirts in sizes Small, Medium, Large, and Extra-Large.</span></span> <span data-ttu-id="ff6c7-109">Stuttermabolur er skilgreindur sem afurð og mismunandi stærðir eru skilgreindar sem afbrigði af vörunni.</span><span class="sxs-lookup"><span data-stu-id="ff6c7-109">The T-shirt is defined as a product, and the different sizes are defined as variants of the product.</span></span> <span data-ttu-id="ff6c7-110">Stuttermabolunum er pakkað í kassa og það geta verið fimm bolir í kassa, fyrir utan þá mjög stóru þar sem aðeins er pláss fyrir fjóra boli.</span><span class="sxs-lookup"><span data-stu-id="ff6c7-110">The T-shirts are packed in boxes and there can be five T-shirts in a box, except for the Extra-Large size where there is only space for four T-shirts.</span></span> <span data-ttu-id="ff6c7-111">Fyrirtækið vill rekja ólík afbrigði af stuttermabolunum í einingunni **Stykki** en selur bolina í einingunni **Kassar**.</span><span class="sxs-lookup"><span data-stu-id="ff6c7-111">The company wants to track the different variants of the T-shirts in the unit **Pieces** but is selling the T-shirts in the unit **Boxes**.</span></span> <span data-ttu-id="ff6c7-112">Umreikningur milli birgðaeiningar og sölueiningar er 1 kassi = 5 stykki, fyrir utan afbrigðið Mjög stór þar sem umreikningurinn er 1 kassi = 4 stykki.</span><span class="sxs-lookup"><span data-stu-id="ff6c7-112">The conversion between the inventory unit and the sales unit is 1 Box = 5 Pieces, except for the variant Extra-Large, where the conversion is 1 Box = 4 Pieces.</span></span>

## <a name="setup"></a><span data-ttu-id="ff6c7-113">Uppsetning</span><span class="sxs-lookup"><span data-stu-id="ff6c7-113">Setup</span></span>

<span data-ttu-id="ff6c7-114">Hægt er að skilgreina færibreyturnar til að nota eiginleikann fyrir afurðir sem **Öll ferli** eða eingöngu fyrir afurð sem er virkjuð fyrir **Vöruhúsaferli** með því að nota valkostinn **Kveikja á mælieiningarumreikningum** á síðunni **Færibreytur afurðarupplýsinga**.</span><span class="sxs-lookup"><span data-stu-id="ff6c7-114">You can configure the parameters for using the feature for products enabled for **All processes** or only for product enabled for the **Warehouse processes** by using the **Enable unit of measure conversations** option on the **Product information parameters** page.</span></span>

### <a name="set-up-a-product-for-unit-conversion-per-variant"></a><span data-ttu-id="ff6c7-115">Setja upp afurð fyrir umreikning einingar fyrir hvert afbrigði</span><span class="sxs-lookup"><span data-stu-id="ff6c7-115">Set up a product for unit conversion per variant</span></span>

<span data-ttu-id="ff6c7-116">Aðeins er hægt að búa til afurðarafbrigði fyrir afurðir af **Undirgerð afurðar**: **Afurðarsniðmát**.</span><span class="sxs-lookup"><span data-stu-id="ff6c7-116">Product variants can only be created for products of **Product subtype**: **Product master**.</span></span> <span data-ttu-id="ff6c7-117">Nánari upplýsingar er að finna í [Stofna afurðarsniðmát](tasks/create-product-master.md).</span><span class="sxs-lookup"><span data-stu-id="ff6c7-117">For more information, see [Create a product master](tasks/create-product-master.md).</span></span>

<span data-ttu-id="ff6c7-118">Eiginleikinn er ekki virkjaður fyrir afurðir sem eru settar upp fyrir ferli framleiðsluþyngdar.</span><span class="sxs-lookup"><span data-stu-id="ff6c7-118">The feature is not enabled for products that are set up for Catch Weight processes.</span></span> 

<span data-ttu-id="ff6c7-119">Við stofnun afurðarsniðmáts skal virkja mælieiningarumreikning með því að nota valkostinn **Virkja umreikninga mælieiningar** á síðunni **Upplýsingar um afurð**.</span><span class="sxs-lookup"><span data-stu-id="ff6c7-119">During the creation of a product master enable unit of measure conversion by using the **Enable unit of measure conversions** option on the **Product details** page.</span></span>

<span data-ttu-id="ff6c7-120">Þegar afurðarsniðmát með útgefnum afurðarafbrigðum er búið til, er hægt að setja upp umreikninga eininga fyrir hvert afbrigði.</span><span class="sxs-lookup"><span data-stu-id="ff6c7-120">When the product master with released products variants is created, unit conversions per variants can be set up.</span></span> <span data-ttu-id="ff6c7-121">Hægt er að finna valmyndaratriðið til að opna síðu fyrir umreikning eininga í samhengi við afurð eða afurðarafbrigði á eftirfarandi síðum.</span><span class="sxs-lookup"><span data-stu-id="ff6c7-121">You can find the menu item for opening the unit conversion page in context of a product or a product variant on the following pages.</span></span>

-   <span data-ttu-id="ff6c7-122">Síðan **Upplýsingar um afurð**</span><span class="sxs-lookup"><span data-stu-id="ff6c7-122">**Product details** page</span></span>
-   <span data-ttu-id="ff6c7-123">Síðan **Upplýsingar um útgefnar afurðar**</span><span class="sxs-lookup"><span data-stu-id="ff6c7-123">**Released products details** page</span></span>
-   <span data-ttu-id="ff6c7-124">Síðan **Útgefin afurðarafbrigði**</span><span class="sxs-lookup"><span data-stu-id="ff6c7-124">**Released product variants** page</span></span>

<span data-ttu-id="ff6c7-125">Þegar þú opnar síðuna **Umreikningur eininga** í samhengi við afurðarsniðmát eða útgefið afurðarafbrigði getur þú valið hvort þú vilt setja upp umreikning eininga fyrir afurðina eða fyrir afurðarafbrigðið.</span><span class="sxs-lookup"><span data-stu-id="ff6c7-125">When you open the **Unit conversion** page in context of a product master or released product variant, you can select if you want to set up the unit conversion for the product or for a product variant.</span></span> <span data-ttu-id="ff6c7-126">Þú gerir það með því að velja annaðhvort **Afurðarafbrigði** eða **Afurð** í reitnum **Búa til umreikning fyrir**.</span><span class="sxs-lookup"><span data-stu-id="ff6c7-126">You do that by selecting either **Product variant** or **Product** in the **Create conversion for** field.</span></span>

### <a name="product-variant"></a><span data-ttu-id="ff6c7-127">Afurðarafbrigði</span><span class="sxs-lookup"><span data-stu-id="ff6c7-127">Product variant</span></span>

<span data-ttu-id="ff6c7-128">Ef þú velur **Afurðarafbrigði** getur þú valið fyrir hvaða afbrigði þú vilt setja upp umreikning eininga í reitnum **Afurðarafbrigði**.</span><span class="sxs-lookup"><span data-stu-id="ff6c7-128">If you select **Product variant,** then you can select for which variant you want to set up the unit conversion in the **Product variant** field.</span></span>

### <a name="product"></a><span data-ttu-id="ff6c7-129">Afurð</span><span class="sxs-lookup"><span data-stu-id="ff6c7-129">Product</span></span>

<span data-ttu-id="ff6c7-130">Ef þú velur **Afurð** getur þú sett upp umreikning eininga fyrir afurðarsniðmát.</span><span class="sxs-lookup"><span data-stu-id="ff6c7-130">If you select **Product**, then you can set up a unit conversion for the product master.</span></span> <span data-ttu-id="ff6c7-131">Þessi umreikningur eininga á við um öll afurðarafbrigði með engan skilgreindan umreikning eininga.</span><span class="sxs-lookup"><span data-stu-id="ff6c7-131">This unit conversion will apply for all product variants with no defined unit conversion.</span></span>

### <a name="example"></a><span data-ttu-id="ff6c7-132">Dæmi</span><span class="sxs-lookup"><span data-stu-id="ff6c7-132">Example</span></span>

<span data-ttu-id="ff6c7-133">Afurðarsniðmát, **Stuttermabolur**, er með fjögur útgefin afurðarafbrigði: Lítill, Miðlungs, Stór og Mjög stór.</span><span class="sxs-lookup"><span data-stu-id="ff6c7-133">A product master, **T-Shirt**, has four released products variants Small, Medium, Large, and X-Large.</span></span> <span data-ttu-id="ff6c7-134">Stuttermabolunum er pakkað í kassa og það geta verið fimm bolir í kassa, fyrir utan þá Mjög stóru þar sem aðeins er pláss fyrir fjóra boli.</span><span class="sxs-lookup"><span data-stu-id="ff6c7-134">The T-shirts are packed in boxes and there can be five T-shirts in a box, except for the Extra-large size where there is only space for four T-shirts.</span></span>

<span data-ttu-id="ff6c7-135">Fyrst skaltu opna síðuna **Umreikningur eininga** á upplýsingasíðu útgefinna afurða fyrir **Stuttermabolir.**</span><span class="sxs-lookup"><span data-stu-id="ff6c7-135">First, open the **Unit conversion** page from the Release product details page for **T-shirt.**</span></span>

<span data-ttu-id="ff6c7-136">Á síðunni **Umreikningur eininga** skal setja upp umreikning eininga fyrir útgefna afurðarafbrigðið Mjög stór.</span><span class="sxs-lookup"><span data-stu-id="ff6c7-136">On the **Unit conversion** page, set up the unit conversion for the release product variant X-Large.</span></span>

| <span data-ttu-id="ff6c7-137">**Svæði**</span><span class="sxs-lookup"><span data-stu-id="ff6c7-137">**Field**</span></span>             | <span data-ttu-id="ff6c7-138">**Stilling**</span><span class="sxs-lookup"><span data-stu-id="ff6c7-138">**Setting**</span></span>             |
|-----------------------|-------------------------|
| <span data-ttu-id="ff6c7-139">Búa til umskráningu fyrir</span><span class="sxs-lookup"><span data-stu-id="ff6c7-139">Create conversion for</span></span> | <span data-ttu-id="ff6c7-140">Afurðarafbrigði</span><span class="sxs-lookup"><span data-stu-id="ff6c7-140">Product variant</span></span>         |
| <span data-ttu-id="ff6c7-141">Afurðarafbrigði</span><span class="sxs-lookup"><span data-stu-id="ff6c7-141">Product variant</span></span>       | <span data-ttu-id="ff6c7-142">Stuttermabolur : : Mjög stór : :</span><span class="sxs-lookup"><span data-stu-id="ff6c7-142">T-Shirt : : X-Large : :</span></span> |
| <span data-ttu-id="ff6c7-143">Frá einingu</span><span class="sxs-lookup"><span data-stu-id="ff6c7-143">From unit</span></span>             | <span data-ttu-id="ff6c7-144">Kassar</span><span class="sxs-lookup"><span data-stu-id="ff6c7-144">Boxes</span></span>                   |
| <span data-ttu-id="ff6c7-145">Stuðull</span><span class="sxs-lookup"><span data-stu-id="ff6c7-145">Factor</span></span>                | <span data-ttu-id="ff6c7-146">4</span><span class="sxs-lookup"><span data-stu-id="ff6c7-146">4</span></span>                       |
| <span data-ttu-id="ff6c7-147">Til einingar</span><span class="sxs-lookup"><span data-stu-id="ff6c7-147">To Unit</span></span>               | <span data-ttu-id="ff6c7-148">Stykki</span><span class="sxs-lookup"><span data-stu-id="ff6c7-148">Pieces</span></span>                  |

<span data-ttu-id="ff6c7-149">Útgefnu afurðarafbrigðin Lítill, Miðlungs og Stór eru með sama umreikning eininga milli eininganna Kassi og Stykki, sem þýðir að hægt er að skilgreina umreikning eininga fyrir þessi afurðarafbrigði í afurðarsniðmátinu.</span><span class="sxs-lookup"><span data-stu-id="ff6c7-149">The Released product variants Small, Medium, and Large have the same unit conversion between the unit Box and Pieces, which means that you can define the unit conversion for these product variants on the product master.</span></span>

| <span data-ttu-id="ff6c7-150">**Svæði**</span><span class="sxs-lookup"><span data-stu-id="ff6c7-150">**Field**</span></span>             | <span data-ttu-id="ff6c7-151">**Stilling**</span><span class="sxs-lookup"><span data-stu-id="ff6c7-151">**Setting**</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="ff6c7-152">Búa til umskráningu fyrir</span><span class="sxs-lookup"><span data-stu-id="ff6c7-152">Create conversion for</span></span> | <span data-ttu-id="ff6c7-153">Afurð</span><span class="sxs-lookup"><span data-stu-id="ff6c7-153">Product</span></span>     |
| <span data-ttu-id="ff6c7-154">Afurð</span><span class="sxs-lookup"><span data-stu-id="ff6c7-154">Product</span></span>               | <span data-ttu-id="ff6c7-155">Stuttermabolur</span><span class="sxs-lookup"><span data-stu-id="ff6c7-155">T-Shirt</span></span>     |
| <span data-ttu-id="ff6c7-156">Frá einingu</span><span class="sxs-lookup"><span data-stu-id="ff6c7-156">From unit</span></span>             | <span data-ttu-id="ff6c7-157">Kassar</span><span class="sxs-lookup"><span data-stu-id="ff6c7-157">Boxes</span></span>       |
| <span data-ttu-id="ff6c7-158">Stuðull</span><span class="sxs-lookup"><span data-stu-id="ff6c7-158">Factor</span></span>                | <span data-ttu-id="ff6c7-159">5</span><span class="sxs-lookup"><span data-stu-id="ff6c7-159">5</span></span>           |
| <span data-ttu-id="ff6c7-160">Til einingar</span><span class="sxs-lookup"><span data-stu-id="ff6c7-160">To Unit</span></span>               | <span data-ttu-id="ff6c7-161">Stykki</span><span class="sxs-lookup"><span data-stu-id="ff6c7-161">Pieces</span></span>      |

### <a name="using-excel-to-update-the-unit-conversions"></a><span data-ttu-id="ff6c7-162">Nota Excel til að uppfæra umreikning eininga</span><span class="sxs-lookup"><span data-stu-id="ff6c7-162">Using Excel to update the unit conversions</span></span>

<span data-ttu-id="ff6c7-163">Ef afurð er með mörg afurðarafbrigði með mismunandi umreikningum eininga, er góð hugmynd að flytja út umreikninga eininga úr síðunni **Umreikningur eininga** í Excel-töflureikni, uppfæra umreikningana, og síðan senda þá til baka til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ff6c7-163">If a product has many product variants with different unit conversions, it's a good idea to export the unit conversions from the **Unit conversion** page to an Excel spreadsheet, update the conversions, and then publish them back to Finance and Operations.</span></span>

<span data-ttu-id="ff6c7-164">Valmöguleikinn að flytja út í Excel og senda breytingarnar aftur til Finance and Operations er virkjuð í valmyndaratriðinu **Opna í Microsoft Office** í aðgerðarúðunni á síðunni **Umreikningur eininga**.</span><span class="sxs-lookup"><span data-stu-id="ff6c7-164">The option to export to Excel and publish the edits back to Finance and Operations is enabled from the **Open in Microsoft office** menu item on the Action Pane on the **Unit conversion** page.</span></span>
