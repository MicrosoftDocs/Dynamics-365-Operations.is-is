---
title: Breyta vinnuhópi á vinnu
description: Þetta efnisatriði útskýrir hvernig hægt er að nota hnappinn „Breyta vinnuhópi“ fyrir vinnuliði til að breyta vinnuhópi fyrirliggjandi vinnu.
author: mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkPool,WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 66d110c3235e8a87b64bf160bdad8524fad6abe5
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "5001150"
---
# <a name="change-work-pool-on-work"></a><span data-ttu-id="a0d24-103">Breyta vinnuhópi á vinnu</span><span class="sxs-lookup"><span data-stu-id="a0d24-103">Change work pool on work</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a0d24-104">Hægt er að nota vinnuhópa til að skipuleggja vinnu í flokka.</span><span class="sxs-lookup"><span data-stu-id="a0d24-104">You can use work pools to organize work into groups.</span></span> <span data-ttu-id="a0d24-105">Til dæmis er hægt að stofna vinnuhóp til að flokka vinnu sem fer í staðsetningu tiltekins vöruhúss.</span><span class="sxs-lookup"><span data-stu-id="a0d24-105">For example, you can create a work pool to classify work that occurs in a specific warehouse location.</span></span>

<span data-ttu-id="a0d24-106">Eiginleikinn *Breyta vinnuhópi á vinnu* bætir hnappnum **Breyta vinnuhópi** við aðgerðasvæðið fyrir vinnuliði.</span><span class="sxs-lookup"><span data-stu-id="a0d24-106">The *Change work pool on work* feature adds a **Change work pool** button to the Action Pane for work items.</span></span> <span data-ttu-id="a0d24-107">Stjórnendur vöruhúss geta þar af leiðandi auðveldlega breytt vinnuhópi fyrirliggjandi vinnu.</span><span class="sxs-lookup"><span data-stu-id="a0d24-107">Therefore, warehouse managers can easily change the work pool of existing work.</span></span> <span data-ttu-id="a0d24-108">Þessi eiginleiki gerir stjórnendum kleift að bregðast hratt við breytingum í vinnusal vöruhúss og hann eykur getu þeirra til að aðlagast breyttum aðstæðum og þörfinni til að flytja vinnu á annan vinnuhóp.</span><span class="sxs-lookup"><span data-stu-id="a0d24-108">This feature lets managers react quickly to changes on the warehouse shop floor, and it helps improve their ability to adapt to changing situations and the need to transfer work to another work pool.</span></span>

## <a name="turn-on-the-change-work-pool-on-work-feature"></a><span data-ttu-id="a0d24-109">Kveikja á eiginleikanum „Breyta vinnuhópi á vinnu“</span><span class="sxs-lookup"><span data-stu-id="a0d24-109">Turn on the Change work pool on work feature</span></span>

<span data-ttu-id="a0d24-110">Áður en hafist er handa við að setja upp eða nota þennan eiginleika þarf að ganga úr skugga um að hann sé í boði í kerfinu.</span><span class="sxs-lookup"><span data-stu-id="a0d24-110">Before you begin to set up or use this feature, you must make sure that it's available in your system.</span></span> <span data-ttu-id="a0d24-111">Stjórnendur geta notað stillingarnar [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og kveikt á honum ef þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="a0d24-111">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="a0d24-112">Á vinnusvæðinu **Eiginleikastjórnun** er eiginleikinn tilgreindur á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="a0d24-112">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="a0d24-113">**Eining:** *Vöruhúsakerfi*</span><span class="sxs-lookup"><span data-stu-id="a0d24-113">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="a0d24-114">**Heiti eiginleika:** *Breyta vinnuhópi á vinnu*</span><span class="sxs-lookup"><span data-stu-id="a0d24-114">**Feature name:** *Change work pool on work*</span></span>

## <a name="set-up-the-change-work-pool-on-work-feature"></a><span data-ttu-id="a0d24-115">Setja upp eiginleikann „Breyta vinnuhópi á vinnu“</span><span class="sxs-lookup"><span data-stu-id="a0d24-115">Set up the Change work pool on work feature</span></span>

<span data-ttu-id="a0d24-116">Til að nota þennan eiginleika þarf að hafa einhverja vinnuhópa uppsetta.</span><span class="sxs-lookup"><span data-stu-id="a0d24-116">To use this feature, you must have some work pools set up.</span></span> <span data-ttu-id="a0d24-117">Einnig er hægt að setja upp vinnusniðmátin til að þau úthluti hópi sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="a0d24-117">You might also set up your work templates so that they automatically assign a pool.</span></span> <span data-ttu-id="a0d24-118">Ef á að vinna í gegnum sýniaðstæðurnar sem boðið er upp á seinna í þessu efnisatriði, skal setja kerfið eins og lýst er í þessum hluta.</span><span class="sxs-lookup"><span data-stu-id="a0d24-118">If you want to work through the example scenario that is provided later in this topic, set up your system as described in this section.</span></span>

### <a name="set-up-work-pools"></a><span data-ttu-id="a0d24-119">Setja upp vinnuhópa</span><span class="sxs-lookup"><span data-stu-id="a0d24-119">Set up work pools</span></span>

<span data-ttu-id="a0d24-120">Vinnuhópar gera þér kleift að skipuleggja vinnuliði eftir gerð.</span><span class="sxs-lookup"><span data-stu-id="a0d24-120">Work pools let you organize work items by type.</span></span> <span data-ttu-id="a0d24-121">Til að vinna með eiginleikann *Breyta vinnuhópi á vinnu* þarf að hafa a.m.k. tvo vinnuhópa tiltæka.</span><span class="sxs-lookup"><span data-stu-id="a0d24-121">To work with the *Change work pool on work* feature, you must have at least two work pools available.</span></span> <span data-ttu-id="a0d24-122">Til að skoða og bæta við vinnuhópum skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="a0d24-122">To view and add work pools, follow these steps.</span></span>

1. <span data-ttu-id="a0d24-123">Fara í **Vöruhúsakerfi \> Uppsetning \> Vinna \> Vinnuhópar**.</span><span class="sxs-lookup"><span data-stu-id="a0d24-123">Go to **Warehouse management \> Setup \> Work \> Work pools**.</span></span>
1. <span data-ttu-id="a0d24-124">Ef unnið er með sýnigögn úr fyrirtækinu **USMF** og farið verður í gegnum atburðarásina seinna í þessu efnisatriði, skal bæta við tveimur vinnuhópum sem eru með eftirfarandi stillingum:</span><span class="sxs-lookup"><span data-stu-id="a0d24-124">If you're working with demo data from the **USMF** company and will work through the example scenario later in this topic, add two work pools that have the following settings:</span></span>

    - <span data-ttu-id="a0d24-125">Vinnuhópur 1:</span><span class="sxs-lookup"><span data-stu-id="a0d24-125">Work pool 1:</span></span>

        - <span data-ttu-id="a0d24-126">**Auðkenni vinnuhóps:** *Vefverslun*</span><span class="sxs-lookup"><span data-stu-id="a0d24-126">**Work pool ID:** *Webshop*</span></span>
        - <span data-ttu-id="a0d24-127">**Lýsing:** *Vefverslun*</span><span class="sxs-lookup"><span data-stu-id="a0d24-127">**Description:** *Web Shop*</span></span>

    - <span data-ttu-id="a0d24-128">Vinnuhópur 2:</span><span class="sxs-lookup"><span data-stu-id="a0d24-128">Work pool 2:</span></span>

        - <span data-ttu-id="a0d24-129">**Auðkenni vinnuhóps:** *Símaver*</span><span class="sxs-lookup"><span data-stu-id="a0d24-129">**Work pool ID:** *CallCenter*</span></span>
        - <span data-ttu-id="a0d24-130">**Lýsing:** *Símaver*</span><span class="sxs-lookup"><span data-stu-id="a0d24-130">**Description:** *Call Center*</span></span>

1. <span data-ttu-id="a0d24-131">Í aðgerðarúðunni skal velja **Vista**.</span><span class="sxs-lookup"><span data-stu-id="a0d24-131">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-work-templates"></a><span data-ttu-id="a0d24-132">Setja upp vinnusniðmát</span><span class="sxs-lookup"><span data-stu-id="a0d24-132">Set up work templates</span></span>

<span data-ttu-id="a0d24-133">Fyrir hvert vinnusniðmát er hægt að stilla sjálfgefinn vinnuhóp eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="a0d24-133">For each of your work templates, you can set a default work pool, as you require.</span></span> <span data-ttu-id="a0d24-134">Fyrir hvert viðeigandi sniðmát er vinnuhópi úthlutað í dálknum **Auðkenni vinnuhóps**.</span><span class="sxs-lookup"><span data-stu-id="a0d24-134">For each relevant template, you assign a work pool in the **Work pool ID** column.</span></span> <span data-ttu-id="a0d24-135">Í þessu tilviki erfa sjálfkrafa allir vinnuliðir sem búnir eru til með því að nota uppgefið sniðmát úthlutaðan vinnuhóp.</span><span class="sxs-lookup"><span data-stu-id="a0d24-135">In this case, all work items that are generated by using a given template automatically inherit the assigned work pool.</span></span> <span data-ttu-id="a0d24-136">Ef unnið er með sýnigögn úr fyrirtækinu **USMF** og farið verður í gegnum atburðarásina seinna í þessu efnisatriði, skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="a0d24-136">If you're working with the demo data from the **USMF** company and will work through the example scenario later in this topic, follow these steps.</span></span>

1. <span data-ttu-id="a0d24-137">Farðu í **Vöruhúsakerfi \> Uppsetning \> Vinna \> Vinnusniðmát**.</span><span class="sxs-lookup"><span data-stu-id="a0d24-137">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="a0d24-138">Á aðgerðasvæðinu skal velja **Breyta** til að færa síðuna yfir í breytingastillingu.</span><span class="sxs-lookup"><span data-stu-id="a0d24-138">On the Action Pane, select **Edit** to put the page into editing mode.</span></span>
1. <span data-ttu-id="a0d24-139">Breytið sniðmátinu með því að stilla eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="a0d24-139">Edit the template by setting the following values:</span></span>

    - <span data-ttu-id="a0d24-140">**Vinnusniðmát:** *62 Tína til að pakka*</span><span class="sxs-lookup"><span data-stu-id="a0d24-140">**Work template:** *62 Pick to pack*</span></span>
    - <span data-ttu-id="a0d24-141">**Auðkenni vinnuhóps:** *Vefverslun*</span><span class="sxs-lookup"><span data-stu-id="a0d24-141">**Work pool ID:** *Webshop*</span></span>

1. <span data-ttu-id="a0d24-142">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="a0d24-142">Select **Save**.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="a0d24-143">Dæmi</span><span class="sxs-lookup"><span data-stu-id="a0d24-143">Example scenario</span></span>

<span data-ttu-id="a0d24-144">Þessi atburðarás sýnir hvernig á að breyta flæði úrvinnslunnar fyrir fyrirliggjandi vinnulið með því að breyta vinnuhóp hans.</span><span class="sxs-lookup"><span data-stu-id="a0d24-144">This scenario shows how to change the stream of processing for an existing work item by changing its work pool.</span></span> <span data-ttu-id="a0d24-145">Hún notar sýnigögn úr fyrirtækinu **USMF** og stillingarnar sem mælt var með fyrr í þessu efnisatriði.</span><span class="sxs-lookup"><span data-stu-id="a0d24-145">It uses demo data from the **USMF** company and the settings that were suggested earlier in this topic.</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="a0d24-146">Stofna sölupöntun og losa hana í vöruhúsið.</span><span class="sxs-lookup"><span data-stu-id="a0d24-146">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="a0d24-147">Staðfestið að nóg af lagerbirgðum séu til fyrir vörur *A0001* og *A0002* í vöruhúsi *62*.</span><span class="sxs-lookup"><span data-stu-id="a0d24-147">Confirm that there is enough on-hand inventory for items *A0001* and *A0002* in warehouse *62*.</span></span> <span data-ttu-id="a0d24-148">Farið í **Vöruhúsakerfi \> Fyrirspurnir og skýrslur \> Listi á lager** og breytið síunum eins og sýnt er hér:</span><span class="sxs-lookup"><span data-stu-id="a0d24-148">Go to **Inventory management \> Inquiries and reports \> On-hand list**, and edit the filters as shown here:</span></span>

    - <span data-ttu-id="a0d24-149">Gildið **Vöruhús** byrjar á *62*.</span><span class="sxs-lookup"><span data-stu-id="a0d24-149">The **Warehouse** value begins with *62*.</span></span>
    - <span data-ttu-id="a0d24-150">Gildið **Vörunúmer** er annaðhvort *A001* eða *A002*.</span><span class="sxs-lookup"><span data-stu-id="a0d24-150">The **Item number** value is either *A001* or *A002*.</span></span>

    <span data-ttu-id="a0d24-151">Sýnigögn eiga hvort um sig að vera með magn upp á 10.</span><span class="sxs-lookup"><span data-stu-id="a0d24-151">Demo data should have a quantity of 10 each.</span></span>

    <span data-ttu-id="a0d24-152">Næst þarftu að stofna sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="a0d24-152">Next, you must create a sales order.</span></span>

1. <span data-ttu-id="a0d24-153">Farðu í **Sölu og markaðssetningu \> Sölupöntun \> Allar sölupantanir**.</span><span class="sxs-lookup"><span data-stu-id="a0d24-153">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="a0d24-154">Í aðgerðarúðunni velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="a0d24-154">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="a0d24-155">Sláið inn eftirfarandi gildi í svarglugganum **Stofna sölupöntun**:</span><span class="sxs-lookup"><span data-stu-id="a0d24-155">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="a0d24-156">**Viðskiptavinalykill:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="a0d24-156">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="a0d24-157">**Vöruhús:** *62*</span><span class="sxs-lookup"><span data-stu-id="a0d24-157">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="a0d24-158">Veljið **Í lagi** til að stofna sölupöntunina og loka svarglugganum.</span><span class="sxs-lookup"><span data-stu-id="a0d24-158">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="a0d24-159">Ný sölupöntun opnast.</span><span class="sxs-lookup"><span data-stu-id="a0d24-159">The new sales order is opened.</span></span> <span data-ttu-id="a0d24-160">Hún ætti að innihalda nýja, auða línu í hnitanetinu í flýtiflipanum **Sölupöntunarlínur**.</span><span class="sxs-lookup"><span data-stu-id="a0d24-160">It should include a new, empty line in the grid on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="a0d24-161">Stilltu eftirfarandi gildi á þessari línu:</span><span class="sxs-lookup"><span data-stu-id="a0d24-161">On this line, set the following values:</span></span>

    - <span data-ttu-id="a0d24-162">**Vörunúmer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="a0d24-162">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="a0d24-163">**Magn:** *2*</span><span class="sxs-lookup"><span data-stu-id="a0d24-163">**Quantity:** *2*</span></span>

1. <span data-ttu-id="a0d24-164">Á valmyndinni **Birgðir** fyrir ofan hnitanetið smellir þú á **Frátekning**.</span><span class="sxs-lookup"><span data-stu-id="a0d24-164">On the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="a0d24-165">Á síðunni **Frátekning**, á aðgerðasvæðinu, skal velja **Frátektarlota** til að taka frá birgðir.</span><span class="sxs-lookup"><span data-stu-id="a0d24-165">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the inventory.</span></span>
1. <span data-ttu-id="a0d24-166">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="a0d24-166">Close the page.</span></span>
1. <span data-ttu-id="a0d24-167">Í sölupöntuninni sem var nýverið stofnuð, í flýtiflipanum **Sölupöntunarlínur**, skal velja **Bæta við línu** til að bæta annarri línu við sölupöntunina.</span><span class="sxs-lookup"><span data-stu-id="a0d24-167">On the **Sales order lines** FastTab, select **Add line** to add another line to your sales order.</span></span> <span data-ttu-id="a0d24-168">Stilltu eftirfarandi gildi á þessari línu:</span><span class="sxs-lookup"><span data-stu-id="a0d24-168">On this line, set the following values:</span></span>

    - <span data-ttu-id="a0d24-169">**Vörunúmer:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="a0d24-169">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="a0d24-170">**Magn:** *2*</span><span class="sxs-lookup"><span data-stu-id="a0d24-170">**Quantity:** *2*</span></span>

1. <span data-ttu-id="a0d24-171">Á valmyndinni **Birgðir** fyrir ofan hnitanetið smellir þú á **Frátekning**.</span><span class="sxs-lookup"><span data-stu-id="a0d24-171">On the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="a0d24-172">Á síðunni **Frátekning**, á aðgerðasvæðinu, skal velja **Frátektarlota** til að taka frá birgðir.</span><span class="sxs-lookup"><span data-stu-id="a0d24-172">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the inventory.</span></span>
1. <span data-ttu-id="a0d24-173">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="a0d24-173">Close the page.</span></span>
1. <span data-ttu-id="a0d24-174">Á aðgerðasvæðinu, í flipanum **Vöruhús**, skal velja **Losa í vöruhús**.</span><span class="sxs-lookup"><span data-stu-id="a0d24-174">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="a0d24-175">Þú færð skilaboð með upplýsingum um bylgjuauðkenni og sendingarkenni sem voru búin til frá útgáfunni.</span><span class="sxs-lookup"><span data-stu-id="a0d24-175">You receive informational messages that show the wave ID and shipment ID that were created from the release.</span></span> <span data-ttu-id="a0d24-176">Skráðu niður bylgjuauðkennið.</span><span class="sxs-lookup"><span data-stu-id="a0d24-176">Make a note of the wave ID.</span></span>

### <a name="review-the-outbound-wave"></a><span data-ttu-id="a0d24-177">Fara yfir bylgju á útleið</span><span class="sxs-lookup"><span data-stu-id="a0d24-177">Review the outbound wave</span></span>

1. <span data-ttu-id="a0d24-178">Farðu í **Vöruhúsastjórnun \> Bylgjur á útleið \> Sendingarbylgjur \> Allar bylgjur**.</span><span class="sxs-lookup"><span data-stu-id="a0d24-178">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="a0d24-179">Í hnitanetinu skaltu velja bylgjuauðkennið sem var búið til úr losuninni á sölupöntuninni.</span><span class="sxs-lookup"><span data-stu-id="a0d24-179">In the grid, search for the wave ID that was created from the release of the sales order.</span></span>
1. <span data-ttu-id="a0d24-180">Veljið bylgjukennið til að skoða upplýsingarnar.</span><span class="sxs-lookup"><span data-stu-id="a0d24-180">Select the wave ID to view the details.</span></span>
1. <span data-ttu-id="a0d24-181">Í flýtiflipanum **Bylgjulínur** skal ganga úr skugga um að auðkenni sendingar sé sýnt fyrir sölupöntunina.</span><span class="sxs-lookup"><span data-stu-id="a0d24-181">On the **Wave lines** FastTab, make sure that a shipment ID is shown for the sales order.</span></span>

    > [!TIP]
    > <span data-ttu-id="a0d24-182">Ef valkosturinn **Vinna úr bylgju við losun í vörugeymslu** er stilltur á *Nei* í uppsetningunni fyrir bylgjusniðmát sendingar, þarf að vinna handvirkt úr bylgjunni með því að velja **Vinna úr** í flipanum **Bylgja** á aðgerðasvæðinu til að búa til vinnu.</span><span class="sxs-lookup"><span data-stu-id="a0d24-182">If the **Process wave at release to warehouse** option is set to *No* in the setup for the shipping wave template, you must manually process the wave by selecting **Process** from the **Wave** tab on the Action Pane to create work.</span></span>

1. <span data-ttu-id="a0d24-183">Gakktu úr skugga um að bylgjan hafi verið meðhöndluð.</span><span class="sxs-lookup"><span data-stu-id="a0d24-183">Make sure that the wave has been processed.</span></span> <span data-ttu-id="a0d24-184">Þessi meðhöndlun býr til nauðsynlega vinnu.</span><span class="sxs-lookup"><span data-stu-id="a0d24-184">This processing creates the required work.</span></span>

### <a name="view-work-details-and-change-the-work-pool"></a><span data-ttu-id="a0d24-185">Skoða upplýsingar um vinnu og breyta vinnuhópnum</span><span class="sxs-lookup"><span data-stu-id="a0d24-185">View work details and change the work pool</span></span>

<span data-ttu-id="a0d24-186">Hægt er að nota síðuna **Upplýsingar um vinnu** til að skoða vinnuna sem búin var til og til að stjórna vinnuhópnum.</span><span class="sxs-lookup"><span data-stu-id="a0d24-186">You can use the **Work details** page to view the work that was created and to manage the work pool.</span></span>

1. <span data-ttu-id="a0d24-187">Opnaðu **Vöruhúsastjórnun \> Vinna \> Upplýsingar um vinnu**.</span><span class="sxs-lookup"><span data-stu-id="a0d24-187">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="a0d24-188">Veljið línuna fyrir vinnuna sem var verið að búa til.</span><span class="sxs-lookup"><span data-stu-id="a0d24-188">Select the row for the work that was just created.</span></span> <span data-ttu-id="a0d24-189">Dálkurinn **Pöntunarnúmer** sýnir sölupöntunarnúmerið.</span><span class="sxs-lookup"><span data-stu-id="a0d24-189">The **Order number** column will show the sales order number.</span></span>

    <span data-ttu-id="a0d24-190">Reiturinn **Auðkenni vinnuhóps** verður stilltur á auðkenni vinnuhópsins sem settur var upp í vinnusniðmátinu.</span><span class="sxs-lookup"><span data-stu-id="a0d24-190">The **Work pool ID** field will be set to the work pool ID that was set up in the work template.</span></span>

    > [!TIP]
    > <span data-ttu-id="a0d24-191">Ef reiturinn **Auðkenni vinnuhóps** sést ekki, skal bæta dálknum við hnitanetið og síðan endurhlaða síðunni.</span><span class="sxs-lookup"><span data-stu-id="a0d24-191">If you don't see the **Work pool ID** field, add the column to the grid, and then refresh the page.</span></span>

1. <span data-ttu-id="a0d24-192">Til að breyta vinnuhópnum sem tengist vinnukenni, á aðgerðasvæðinu, í flipanum **Vinna**, skal velja **Breyta auðkenni vinnuhóps**.</span><span class="sxs-lookup"><span data-stu-id="a0d24-192">To change the work pool that is associated with the work ID, on the Action Pane, on the **Work** tab, select **Change Work pool ID**.</span></span>
1. <span data-ttu-id="a0d24-193">Í svarglugganum **Breyta vinnuhópi**, í flýtiflipanum **Færibreytur**, í reitnum **Auðkenni vinnuhóps**, skal velja *Símaver*.</span><span class="sxs-lookup"><span data-stu-id="a0d24-193">In the **Change work pool** dialog box, on the **Parameters** FastTab, in the **Work pool ID** field, select *CallCenter*.</span></span>
1. <span data-ttu-id="a0d24-194">Veldu **Í lagi** til að gera breytinguna.</span><span class="sxs-lookup"><span data-stu-id="a0d24-194">Select **OK** to apply your change.</span></span>
1. <span data-ttu-id="a0d24-195">Takið eftir að gildið í reitnum **Auðkenni vinnuhóps** hefur nú verið breytt í *Símaver*.</span><span class="sxs-lookup"><span data-stu-id="a0d24-195">Notice that the value of the **Work pool ID** field has now been changed to *CallCenter*.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a0d24-196">Þegar svarglugginn **Breyta vinnuhópi** birtist, gæti reiturinn **Auðkenni vinnuhóps** verið sjálfgefið auður.</span><span class="sxs-lookup"><span data-stu-id="a0d24-196">When the **Change work pool** dialog box appears, the **Work pool ID** field might be blank by default.</span></span> <span data-ttu-id="a0d24-197">Ef reiturinn er auður þegar valið er **Í lagi** til að koma breytingum á, verður vinnuhópurinn fjarlægður að fullu úr vinnunni.</span><span class="sxs-lookup"><span data-stu-id="a0d24-197">If the field is blank when you select **OK** to apply changes, you will remove the work pool completely from the work.</span></span>
>
> <span data-ttu-id="a0d24-198">Ásamt því að skipta um vinnuhópa, er hægt að nota þetta ferli til að bæta vinnuhópi við hvaða vinnulið sem er sem er ekki með slíkan, eða til að fjarlægja vinnuhóp úr vinnulið sem er með einn slíkan.</span><span class="sxs-lookup"><span data-stu-id="a0d24-198">In addition to switching work pools, you can use this procedure to add a work pool to any work item that doesn't have one, or to remove a work pool from any work item that does have one.</span></span>
