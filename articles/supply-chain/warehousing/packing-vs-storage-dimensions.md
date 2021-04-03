---
title: Stilla mismunandi víddir fyrir pakka og geymslu
description: Þetta efnisatriði sýnir hvernig á að tilgreina hvaða vinnslu (pökkun, geymsla eða földuð pökkun) hver tilgreind vídd er notuð fyrir.
author: mirzaab
manager: tfehr
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResPhysicalProductDimensions, WHSPhysDimUOM
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-01-28
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: aa5cbf807e809238489c539d3ad8c0bc34421774
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/04/2021
ms.locfileid: "5501295"
---
# <a name="set-different-dimensions-for-packing-and-storage"></a><span data-ttu-id="ac821-103">Stilla mismunandi víddir fyrir pakka og geymslu</span><span class="sxs-lookup"><span data-stu-id="ac821-103">Set different dimensions for packing and storage</span></span>

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="ac821-104">Sumar vörur eru pakkaðar eða geymdar á þann hátt að nauðsynlegt kann að vera að rekja efnislegar víddir á annan hátt fyrir hvert mismunandi ferli.</span><span class="sxs-lookup"><span data-stu-id="ac821-104">Some items are packed or stored in such a way that you may need to track physical dimensions differently for each of several different processes.</span></span> <span data-ttu-id="ac821-105">Eiginleikinn *Afurðarvíddir pökkunar* gerir kleift að setja upp eina eða fleiri gerðir af víddum fyrir hverja afurð.</span><span class="sxs-lookup"><span data-stu-id="ac821-105">The *Packaging product dimensions* feature lets you set up one or several types of dimensions for each product.</span></span> <span data-ttu-id="ac821-106">Hver gerð víddar býður upp á efnislegar mælingar (þyngd, breidd, dýpt og hæð) og kemur með ferlið þar sem þessi gildi efnislegra mælinga eiga við.</span><span class="sxs-lookup"><span data-stu-id="ac821-106">Each dimension type provides a set of physical measurements (weight, width, depth, and height), and establishes the process where those physical measurement values apply.</span></span> <span data-ttu-id="ac821-107">Þegar þessi eiginleiki er virkur styður kerfið eftirfarandi gerðir af víddum:</span><span class="sxs-lookup"><span data-stu-id="ac821-107">When this feature is enabled, your system will support the following types of dimensions:</span></span>

- <span data-ttu-id="ac821-108">*Geymsla* - Geymsluvíddir eru notaðar ásamt rúmmáli staðsetningar til að ákvarða hversu mikið af hverri vöru er hægt að geyma í hinum ýmsu staðsetningum vöruhúss.</span><span class="sxs-lookup"><span data-stu-id="ac821-108">*Storage* - Storage dimensions are used along with location volumetrics to determine how many of each item can be stored in various warehouse locations.</span></span>
- <span data-ttu-id="ac821-109">*Pökkun* – Pökkunarvíddir eru notaðar við umbúðahönnun og í handvirku pökkunarferli til að ákvarða hversu mikið af hverri vöru passar í hinar ýmsu umbúðagerðir.</span><span class="sxs-lookup"><span data-stu-id="ac821-109">*Packing* - Packing dimensions are used during containerization and the manual packing process to determine how many of each item will fit in various container types.</span></span>
- <span data-ttu-id="ac821-110">*Földuð pökkun* – Víddir faldaðrar pökkunar eru notaðar þegar pökkunarferlið inniheldur mörg stig.</span><span class="sxs-lookup"><span data-stu-id="ac821-110">*Nested packing* - Nested packing dimensions are used when the packing process contains multiple levels.</span></span>

<span data-ttu-id="ac821-111">*Geymsluvíddir* eru studdar hvort sem eiginleikinn *Afurðarvíddir pökkunar* er virkur eða ekki.</span><span class="sxs-lookup"><span data-stu-id="ac821-111">*Storage* dimensions are supported even when the *Packaging product dimensions* feature isn't enabled.</span></span> <span data-ttu-id="ac821-112">Þetta er sett upp með síðunni **Efnisleg vídd** í Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="ac821-112">You set these up using the **Physical dimension** page in Supply Chain Management.</span></span> <span data-ttu-id="ac821-113">Þessar stærðir eru í notaðar af öllum ferlum þar sem víddir pökkunar og faldaðrar pökkunar eru ekki tilgreindar.</span><span class="sxs-lookup"><span data-stu-id="ac821-113">These dimensions are used by all processes where the packing and nested packing dimensions aren't specified.</span></span>

<span data-ttu-id="ac821-114">Víddir *pökkunar* og *faldaðrar pökkunar* eru settar upp á síðunni **Efnislegar afurðarvíddir** sem er bætt við þegar eiginleikinn *Afurðarvíddir pökkunar* er virkjaður.</span><span class="sxs-lookup"><span data-stu-id="ac821-114">*Packing* and *nested packing* dimensions are set up using the **Physical product dimensions** page, which is added when you enable the *Packaging product dimensions* feature.</span></span>
<span data-ttu-id="ac821-115">Í þessu efnisatriði er að finna aðstæður sem lýsa því hvernig á að nota þennan eiginleika.</span><span class="sxs-lookup"><span data-stu-id="ac821-115">This topic provides a scenario that illustrates how to use this feature.</span></span>

## <a name="turn-on-the-packaging-product-dimensions-feature"></a><span data-ttu-id="ac821-116">Kveikja á eiginleika afurðarvíddar pökkunar</span><span class="sxs-lookup"><span data-stu-id="ac821-116">Turn on the packaging product dimensions feature</span></span>

<span data-ttu-id="ac821-117">Áður en hægt er að nota þennan eiginleika þarf að kveikja á honum í kerfinu.</span><span class="sxs-lookup"><span data-stu-id="ac821-117">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="ac821-118">Stjórnendur geta notað vinnusvæði [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og kveikt á honum ef þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="ac821-118">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="ac821-119">Þar er eiginleikinn sýndur á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="ac821-119">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="ac821-120">**Eining:** *Vöruhúsakerfi*</span><span class="sxs-lookup"><span data-stu-id="ac821-120">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="ac821-121">**Heiti eiginleika:** *Afurðarvíddir pökkunar*</span><span class="sxs-lookup"><span data-stu-id="ac821-121">**Feature name:** *Packaging product dimensions*</span></span>

## <a name="example-scenario"></a><span data-ttu-id="ac821-122">Dæmi</span><span class="sxs-lookup"><span data-stu-id="ac821-122">Example scenario</span></span>

### <a name="set-up-the-scenario"></a><span data-ttu-id="ac821-123">Setja upp aðstæður</span><span class="sxs-lookup"><span data-stu-id="ac821-123">Set up the scenario</span></span>

<span data-ttu-id="ac821-124">Áður en hægt er að keyra sýnidæmið þarf að undirbúa kerfið eins og lýst er í þessum hluta.</span><span class="sxs-lookup"><span data-stu-id="ac821-124">Before you can run the example scenario, you must prepare your system as described in this section.</span></span>

#### <a name="enable-demo-data"></a><span data-ttu-id="ac821-125">Kveikja á sýnigögnum</span><span class="sxs-lookup"><span data-stu-id="ac821-125">Enable demo data</span></span>

<span data-ttu-id="ac821-126">Til að vinna í gegnum þessar aðstæður með því að nota sýnigögnin og gildin sem eru tilgreind hér verður þú að vera í kerfi þar sem venjuleg [sýnigögn](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) eru sett upp.</span><span class="sxs-lookup"><span data-stu-id="ac821-126">To work through this scenario using the demo records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="ac821-127">Þar að auki verður þú að velja *USMF*-lögaðila áður en þú byrjar.</span><span class="sxs-lookup"><span data-stu-id="ac821-127">Additionally, you must select the *USMF* legal entity before you begin.</span></span>

#### <a name="add-a-new-physical-dimension-to-a-product"></a><span data-ttu-id="ac821-128">Bæta nýrri efnislegri vídd við afurð</span><span class="sxs-lookup"><span data-stu-id="ac821-128">Add a new physical dimension to a product</span></span>

<span data-ttu-id="ac821-129">Bæta við nýrri efnislegri vídd fyrir afurð með því að gera eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="ac821-129">Add a new physical dimension for a product by doing the following:</span></span>

1. <span data-ttu-id="ac821-130">Opna **Afurðaupplýsingastjórnun \> Afurðir \> Útgefnar afurðir**.</span><span class="sxs-lookup"><span data-stu-id="ac821-130">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="ac821-131">Veljið afurðina með **Vörunúmer** *A0001*.</span><span class="sxs-lookup"><span data-stu-id="ac821-131">Select the product with **Item number** *A0001*.</span></span>
1. <span data-ttu-id="ac821-132">Á aðgerðasvæðinu skal opna flipann **Stjórna birgðum**, úr flokknum **Vöruhús**, og velja **Efnislegar afurðarvíddir**.</span><span class="sxs-lookup"><span data-stu-id="ac821-132">On the Action Pane, open the **Manage inventory** tab and, from the **Warehouse** group, select **Physical product dimensions**.</span></span>
1. <span data-ttu-id="ac821-133">Síðan **Efnislegar afurðavíddir** opnast.</span><span class="sxs-lookup"><span data-stu-id="ac821-133">The **Physical product dimensions** page opens.</span></span> <span data-ttu-id="ac821-134">Á aðgerðasvæðinu skal velja **Ný** til að bæta nýrri vídd við hnitanetið með eftirfarandi stillingum:</span><span class="sxs-lookup"><span data-stu-id="ac821-134">On the Action Pane, select **New** to add a new dimension to the grid with the following settings:</span></span>
    - <span data-ttu-id="ac821-135">**Gerð efnislegrar víddar** - *Pökkun*</span><span class="sxs-lookup"><span data-stu-id="ac821-135">**Physical dimension type** - *Packing*</span></span>
    - <span data-ttu-id="ac821-136">**Efnisleg eining** - *stk*</span><span class="sxs-lookup"><span data-stu-id="ac821-136">**Physical unit** - *pcs*</span></span>
    - <span data-ttu-id="ac821-137">**Þyngd** - *4*</span><span class="sxs-lookup"><span data-stu-id="ac821-137">**Weight** - *4*</span></span>
    - <span data-ttu-id="ac821-138">**Þyngdareining** - *kg*</span><span class="sxs-lookup"><span data-stu-id="ac821-138">**Weight unit** - *kg*</span></span>
    - <span data-ttu-id="ac821-139">**Dýpt** - *3*</span><span class="sxs-lookup"><span data-stu-id="ac821-139">**Depth** - *3*</span></span>
    - <span data-ttu-id="ac821-140">**Hæð** - *4*</span><span class="sxs-lookup"><span data-stu-id="ac821-140">**Height** - *4*</span></span>
    - <span data-ttu-id="ac821-141">**Breidd** - *3*</span><span class="sxs-lookup"><span data-stu-id="ac821-141">**Width** - *3*</span></span>
    - <span data-ttu-id="ac821-142">**Lengd** - *cm*</span><span class="sxs-lookup"><span data-stu-id="ac821-142">**Length** - *cm*</span></span>
    - <span data-ttu-id="ac821-143">**Rúmmálseining** - *cm3*</span><span class="sxs-lookup"><span data-stu-id="ac821-143">**Volume unit** - *cm3*</span></span>

<span data-ttu-id="ac821-144">Reiturinn **Rúmmál** er sjálfkrafa reiknaður samkvæmt stillingunum fyrir **Dýpt**, **Hæð** og **Breidd**.</span><span class="sxs-lookup"><span data-stu-id="ac821-144">The **Volume** field is automatically calculated based on your **Depth**, **Height**, and **Width** settings.</span></span>

#### <a name="create-a-new-container-type"></a><span data-ttu-id="ac821-145">Stofna nýja umbúðagerð</span><span class="sxs-lookup"><span data-stu-id="ac821-145">Create a new container type</span></span>

<span data-ttu-id="ac821-146">Farið í **Vöruhúsakerfi \> Uppsetningu \> Umbúðir \> Umbúðagerðir** og stofnið nýja færslu með eftirfarandi stillingum:</span><span class="sxs-lookup"><span data-stu-id="ac821-146">Go to **Warehouse management \> Setup \> Containers \> Container types** and create a new record with the following settings:</span></span>

- <span data-ttu-id="ac821-147">**Kóði umbúðagerðar** - *Lítill kassi*</span><span class="sxs-lookup"><span data-stu-id="ac821-147">**Container type code** - *Short Box*</span></span>
- <span data-ttu-id="ac821-148">**Lýsing** - *Lítill kassi*</span><span class="sxs-lookup"><span data-stu-id="ac821-148">**Description** - *Short Box*</span></span>
- <span data-ttu-id="ac821-149">**Hámarksnettóþyngd** - *50*</span><span class="sxs-lookup"><span data-stu-id="ac821-149">**Maximum net weight** - *50*</span></span>
- <span data-ttu-id="ac821-150">**Magn** - *144*</span><span class="sxs-lookup"><span data-stu-id="ac821-150">**Volume** - *144*</span></span>
- <span data-ttu-id="ac821-151">**Lengd** - *6*</span><span class="sxs-lookup"><span data-stu-id="ac821-151">**Length** - *6*</span></span>
- <span data-ttu-id="ac821-152">**Breidd** - *6*</span><span class="sxs-lookup"><span data-stu-id="ac821-152">**Width** - *6*</span></span>
- <span data-ttu-id="ac821-153">**Hæð** - *4*</span><span class="sxs-lookup"><span data-stu-id="ac821-153">**Height** - *4*</span></span>

#### <a name="create-a-container-group"></a><span data-ttu-id="ac821-154">Stofna umbúðaflokk</span><span class="sxs-lookup"><span data-stu-id="ac821-154">Create a container group</span></span>

<span data-ttu-id="ac821-155">Farið í **Vöruhúsakerfi \> Uppsetningu \> Umbúðir \> Umbúðaflokkar** og stofnið nýja færslu með eftirfarandi stillingum:</span><span class="sxs-lookup"><span data-stu-id="ac821-155">Go to **Warehouse management \> Setup \> Containers \> Container groups** and create a new record with the following settings:</span></span>

- <span data-ttu-id="ac821-156">**Auðkenni umbúðaflokks** - *Lítill kassi*</span><span class="sxs-lookup"><span data-stu-id="ac821-156">**Container group ID** - *Short Box*</span></span>
- <span data-ttu-id="ac821-157">**Lýsing** - *Lítill kassi*</span><span class="sxs-lookup"><span data-stu-id="ac821-157">**Description** - *Short Box*</span></span>

<span data-ttu-id="ac821-158">Bætið nýrri línu við hlutann **Upplýsingar**.</span><span class="sxs-lookup"><span data-stu-id="ac821-158">Add a new line to the **Details** section.</span></span> <span data-ttu-id="ac821-159">Stillið **Umbúðagerðina** á *Lítill kassi*.</span><span class="sxs-lookup"><span data-stu-id="ac821-159">Set the **Container type** to *Short Box*.</span></span>

#### <a name="set-up-a-container-build-template"></a><span data-ttu-id="ac821-160">Setja upp gámaröðunarsniðmát</span><span class="sxs-lookup"><span data-stu-id="ac821-160">Set up a container build template</span></span>

<span data-ttu-id="ac821-161">Farið í **Vöruhúsakerfi \> Uppsetning \> Umbúðir \> Sniðmát umbúðahönnunar** og veljið **Kassar**.</span><span class="sxs-lookup"><span data-stu-id="ac821-161">Go to **Warehouse management \> Setup \> Containers \> Container build templates** and select **Boxes**.</span></span> <span data-ttu-id="ac821-162">Breytið **Auðkenni umbúðaflokks** í *Lítill kassi*.</span><span class="sxs-lookup"><span data-stu-id="ac821-162">Change the **Container group ID** to *Short Box*.</span></span>

### <a name="run-the-scenario"></a><span data-ttu-id="ac821-163">Keyra aðstæður</span><span class="sxs-lookup"><span data-stu-id="ac821-163">Run the scenario</span></span>

<span data-ttu-id="ac821-164">Þegar kerfið hefur verið undirbúið eins og lýst var í hlutanum hér á undan er hægt að keyra aðstæðurnar eins og lýst er í næsta hluta.</span><span class="sxs-lookup"><span data-stu-id="ac821-164">After you have prepared your system as described in the previous section, you are ready to run the scenario as described in the next section.</span></span>

#### <a name="create-a-sales-order-and-create-a-shipment"></a><span data-ttu-id="ac821-165">Stofna sölupöntun og stofna sendingu</span><span class="sxs-lookup"><span data-stu-id="ac821-165">Create a sales order and create a shipment</span></span>

<span data-ttu-id="ac821-166">Í þessu ferli verður sending stofnuð sem byggir á *pökkunarvíddum* vörunnar þar sem hæðin er minni en 3.</span><span class="sxs-lookup"><span data-stu-id="ac821-166">In this process you will create a shipment based on the item *packing* dimensions, for which the height is less than 3.</span></span>

1. <span data-ttu-id="ac821-167">Farðu í **Sölu og markaðssetningu \> Sölupöntun \> Allar sölupantanir**.</span><span class="sxs-lookup"><span data-stu-id="ac821-167">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="ac821-168">Í aðgerðarúðunni velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="ac821-168">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="ac821-169">Sláið inn eftirfarandi gildi í svarglugganum **Stofna sölupöntun**:</span><span class="sxs-lookup"><span data-stu-id="ac821-169">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="ac821-170">**Viðskiptavinalykill:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="ac821-170">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="ac821-171">**Vöruhús:** *63*</span><span class="sxs-lookup"><span data-stu-id="ac821-171">**Warehouse:** *63*</span></span>

1. <span data-ttu-id="ac821-172">Veljið **Í lagi** til að stofna sölupöntunina og loka svarglugganum.</span><span class="sxs-lookup"><span data-stu-id="ac821-172">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="ac821-173">Ný sölupöntun opnast.</span><span class="sxs-lookup"><span data-stu-id="ac821-173">The new sales order is opened.</span></span> <span data-ttu-id="ac821-174">Hún ætti að innihalda nýja, auða línu í hnitanetinu í flýtiflipanum **Sölupöntunarlínur**.</span><span class="sxs-lookup"><span data-stu-id="ac821-174">It should include a new, empty line in the grid on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="ac821-175">Stilltu eftirfarandi gildi á þessari línu:</span><span class="sxs-lookup"><span data-stu-id="ac821-175">On this line, set the following values:</span></span>

    - <span data-ttu-id="ac821-176">**Vörunúmer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="ac821-176">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="ac821-177">**Magn:** *5*</span><span class="sxs-lookup"><span data-stu-id="ac821-177">**Quantity:** *5*</span></span>

1. <span data-ttu-id="ac821-178">Í flýtiflipanum **Sölupöntunarlínur** skal velja **Birgðir \> Frátekning**.</span><span class="sxs-lookup"><span data-stu-id="ac821-178">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="ac821-179">Á síðunni **Frátekning**, á aðgerðasvæðinu, skal velja **Frátektarlota** til að taka frá birgðir.</span><span class="sxs-lookup"><span data-stu-id="ac821-179">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the inventory.</span></span>
1. <span data-ttu-id="ac821-180">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="ac821-180">Close the page.</span></span>
1. <span data-ttu-id="ac821-181">Á aðgerðasvæðinu skal opna flipann **Vöruhús** og velja **Losa í vöruhús** til að búa til vinnu fyrir vöruhúsið.</span><span class="sxs-lookup"><span data-stu-id="ac821-181">On the Action Pane, open the **Warehouse** tab and select **Release to warehouse** to create work for the warehouse.</span></span>
1. <span data-ttu-id="ac821-182">Í flýtiflipanum **Sölupöntunarlínur** skal velja **Vöruhús \> Upplýsingar sendingar**.</span><span class="sxs-lookup"><span data-stu-id="ac821-182">On the **Sales order lines** FastTab, select **Warehouse \> Shipment details**.</span></span>
1. <span data-ttu-id="ac821-183">Á aðgerðasvæðinu skal opna flipann **Flutningur** og velja **Skoða umbúðir**.</span><span class="sxs-lookup"><span data-stu-id="ac821-183">On the Action Pane, open the **Transportation** tab and select **View containers**.</span></span> <span data-ttu-id="ac821-184">Staðfestið að varan hafi verið komið fyrir í tveimur umbúðum af *Litlum kassa*.</span><span class="sxs-lookup"><span data-stu-id="ac821-184">Confirm that the item was containerized into the two *Short Box* containers.</span></span>

#### <a name="place-an-item-into-storage"></a><span data-ttu-id="ac821-185">Setja vöru í geymslu</span><span class="sxs-lookup"><span data-stu-id="ac821-185">Place an item into storage</span></span>

1. <span data-ttu-id="ac821-186">Opnið fartækið, skráið ykkur inn í vöruhús 63 og farið í **Birgðir \> Breyting á**.</span><span class="sxs-lookup"><span data-stu-id="ac821-186">Open the mobile device, sign in to warehouse 63 and go to **Inventory \> Adjust In**.</span></span>
1. <span data-ttu-id="ac821-187">Sláið inn **Loc** = *SHORT-01*.</span><span class="sxs-lookup"><span data-stu-id="ac821-187">Enter **Loc** = *SHORT-01*.</span></span> <span data-ttu-id="ac821-188">Búið til nýja númeraplötu með **Vöru** = *A0001* og **Magn** = *1 stk*.</span><span class="sxs-lookup"><span data-stu-id="ac821-188">Make a new license plate with **Item** = *A0001* and **Quantity** = *1 pcs*.</span></span>
1. <span data-ttu-id="ac821-189">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="ac821-189">Select **OK**.</span></span> <span data-ttu-id="ac821-190">Upp kemur villan „Staðsetningin SHORT-01 tókst ekki vegna þess að varan A0001 passar ekki í tilgreindar víddir staðsetningar.“</span><span class="sxs-lookup"><span data-stu-id="ac821-190">You will receive the error "Location SHORT-01 failed because item A0001 does not fit in location's specified dimensions."</span></span> <span data-ttu-id="ac821-191">Þetta er vegna þess að víddir *Geymslutegundar* fyrir afurðina eru stærri en víddirnar sem tilgreindar eru í staðsetningarforstillingunni.</span><span class="sxs-lookup"><span data-stu-id="ac821-191">This is because the *Storage* type dimensions of the product are larger than the dimensions specified on the location profile.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]