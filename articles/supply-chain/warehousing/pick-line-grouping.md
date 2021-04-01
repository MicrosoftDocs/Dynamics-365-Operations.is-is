---
title: Flokkun tiltektarlínu
description: Þetta efnisatriði veitir yfirlit yfir flokkun tiltektarlínu.
author: Mirzaab
manager: tfehr
ms.date: 12/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem,WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-12-31
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 7ab8cdd7cad5420aca0de53e59220da9e230d411
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5234634"
---
# <a name="pick-line-grouping"></a><span data-ttu-id="6ad9b-103">Flokkun tiltektarlínu</span><span class="sxs-lookup"><span data-stu-id="6ad9b-103">Pick line grouping</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6ad9b-104">Flokkun tiltektarlínu gerir kleift að sameina margar vinnulínur sem eru með sömu vöru og staðsetningu í eina tiltekt sem birtist notanda í fartæki.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-104">Pick line grouping enables multiple work lines that have the same item and location to be combined into a single pick that is presented to the user on the mobile device.</span></span> <span data-ttu-id="6ad9b-105">Starfsmenn í vöruhúsi geta þar af leiðandi fengið gagnlegustu leiðbeiningarnar, en nauðsynlegur aðskilnaður vinnulínu (fyrir mismunandi umbúðir, pantanir og svo framvegis) er enn hægt að vinna með í kerfinu.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-105">Therefore, warehouse workers can receive the most efficient instructions, but required work line separation (for different containers, orders, and so on) can still be maintained in the system.</span></span>

## <a name="turn-on-the-pick-line-grouping-feature"></a><span data-ttu-id="6ad9b-106">Kveikja á eiginleika fyrir flokkun tiltektarlínu</span><span class="sxs-lookup"><span data-stu-id="6ad9b-106">Turn on the pick line grouping feature</span></span>

<span data-ttu-id="6ad9b-107">Áður en hægt er að nota þennan eiginleika þarf að kveikja á honum í kerfinu.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-107">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="6ad9b-108">Stjórnendur geta notað vinnusvæðið [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og kveikja á honum ef þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-108">Administrators can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="6ad9b-109">Þar er eiginleikinn sýndur á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="6ad9b-109">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="6ad9b-110">**Eining:** *Vöruhúsakerfi*</span><span class="sxs-lookup"><span data-stu-id="6ad9b-110">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="6ad9b-111">**Heiti eiginleika:** *Flokkun tiltektarlínu*</span><span class="sxs-lookup"><span data-stu-id="6ad9b-111">**Feature name:** *Pick line grouping*</span></span>

## <a name="set-up-pick-line-grouping"></a><span data-ttu-id="6ad9b-112">Setja upp flokkun tiltektarlínu</span><span class="sxs-lookup"><span data-stu-id="6ad9b-112">Set up pick line grouping</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="6ad9b-113">Stofna valmyndaratriði fartækis</span><span class="sxs-lookup"><span data-stu-id="6ad9b-113">Create a mobile device menu item</span></span>

1. <span data-ttu-id="6ad9b-114">Farðu í **Vöruhúsakerfi \> Uppsetning \> Fartæki \> Valmyndaratriði fartækis**.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-114">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="6ad9b-115">Í aðgerðarúðunni velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-115">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="6ad9b-116">Í reitinn **Heiti valmyndaratriðis** skal færa inn *Tiltekt söluflokkslínu*.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-116">In the **Menu item name** field, enter *Sales group line picking*.</span></span>
1. <span data-ttu-id="6ad9b-117">Í reitinn **Titill** skal slá inn *Tiltekt söluflokkslínu*.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-117">In the **Title** field, enter *Sales group line picking*.</span></span> <span data-ttu-id="6ad9b-118">Þessi titill birtist í valmynd fartækis.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-118">This title will be shown on the mobile device menu.</span></span>
1. <span data-ttu-id="6ad9b-119">Í reitnum **Stilling** velurðu *Vinna*.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-119">In the **Mode** field, select *Work*.</span></span>
1. <span data-ttu-id="6ad9b-120">Stilltu valkostinn **Nota fyrirliggjandi vinnu** á *Já*.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-120">Set the **Use existing work** option to *Yes*.</span></span>
1. <span data-ttu-id="6ad9b-121">Stilltu eftirfarandi gildi á flýtiflipanum **Almennt**:</span><span class="sxs-lookup"><span data-stu-id="6ad9b-121">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="6ad9b-122">Í reitnum **Stýrt af** velurðu *Stýrt af notanda*.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-122">In the **Directed by** field, select *User directed*.</span></span>
    - <span data-ttu-id="6ad9b-123">Stilltu valkostinn **Mynda númeraplötu** á *Já*.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-123">Set the **Generate license plate** option to *Yes*.</span></span>
    - <span data-ttu-id="6ad9b-124">Stilltu valkostinn **Flokkatiltekt** á *Já*.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-124">Set the **Group pick** option to *Yes*.</span></span>
    - <span data-ttu-id="6ad9b-125">Samþykkið sjálfgefin gildi fyrir valkostina sem eftir eru.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-125">Accept the default values for the remaining options.</span></span>

1. <span data-ttu-id="6ad9b-126">Fylgið þessum skrefum til að skilgreina gilda vinnuklasa fyrir valmyndaratriði fartækis:</span><span class="sxs-lookup"><span data-stu-id="6ad9b-126">Follow these steps to configure the valid work classes for the mobile device menu item:</span></span>

    1. <span data-ttu-id="6ad9b-127">Í flýtiflipanum **Vinnuklasar** skal velja **Nýr**.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-127">On the **Work classes** FastTab, elect **New**.</span></span>
    2. <span data-ttu-id="6ad9b-128">Í reitnum **Auðkenni vinnuklasa** er hægt að velja annaðhvort *Sala* eða *Tiltekt sölupöntunar*, en það fer eftir vöruhúsinu sem verður notað.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-128">In the **Work class ID** field, you can select either *Sales* or *SO Pick*, depending on the warehouse that you will use.</span></span> <span data-ttu-id="6ad9b-129">Fyrir þessar aðstæður skal velja *Tiltekt sölupöntunar*.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-129">For this scenario, select *SO Pick*.</span></span>

        <span data-ttu-id="6ad9b-130">Reiturinn **Gerð verkbeiðni** er sjálfkrafa stilltur á *Sölupantanir*.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-130">The **Work order type** field is automatically set to *Sales orders*.</span></span>

### <a name="set-up-a-mobile-device-menu"></a><span data-ttu-id="6ad9b-131">Setja upp valmynd fartækja</span><span class="sxs-lookup"><span data-stu-id="6ad9b-131">Set up a mobile device menu</span></span>

<span data-ttu-id="6ad9b-132">Fylgið þessum skrefum til að bæta við valmyndaratriðinu sem var stofnað í valmyndinni **Á útleið**.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-132">Follow these steps to add the menu item that you just created to the **Outbound** menu.</span></span>

1. <span data-ttu-id="6ad9b-133">Farðu í **Vöruhúsakerfi \> Uppsetning \> Fartæki \> Valmynd fartækis**.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-133">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="6ad9b-134">Á aðgerðarúðunni skal velja **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-134">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="6ad9b-135">Listasvæðið sýnir allar fyrirliggjandi valmyndir fartækis.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-135">The list pane shows all existing mobile device menus.</span></span> <span data-ttu-id="6ad9b-136">Veljið *Á útleið* í listanum.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-136">Select *Outbound* in the list.</span></span>
1. <span data-ttu-id="6ad9b-137">Í listanum **Tiltækar valmyndir og valmyndaratriði** skal finna og velja valmyndaratriðið *Tiltekt söluflokkslínu* sem var stofnað.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-137">In the **Available menus and menu items** list, find and select the *Sales group line picking* menu item that you created.</span></span>
1. <span data-ttu-id="6ad9b-138">Veljið hægri örvarhnappinn til að flytja valmyndaratriðið *Tiltekt söluflokkslínu* yfir í listann **Valmyndaskipan**.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-138">Select the right arrow button to move the *Sales group line picking* menu item to the **Menu structure** list.</span></span>
1. <span data-ttu-id="6ad9b-139">Notið örvarhnappana upp og niður til að færa valmyndaratriðið á æskilegan stað í valmyndaskipanina.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-139">Use the up arrow and down arrow buttons to move the menu item into the desired position in the menu structure.</span></span>
1. <span data-ttu-id="6ad9b-140">Í aðgerðarúðunni skal velja **Vista**.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-140">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-a-work-template"></a><span data-ttu-id="6ad9b-141">Setja upp vinnusniðmát</span><span class="sxs-lookup"><span data-stu-id="6ad9b-141">Set up a work template</span></span>

1. <span data-ttu-id="6ad9b-142">Farðu í **Vöruhúsakerfi \> Uppsetning \> Vinna \> Vinnusniðmát**.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-142">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="6ad9b-143">Í reitnum **Gerð verkbeiðni** velurðu *Sölupantanir*.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-143">In the **Work order type** field, select *Sales orders*.</span></span>
1. <span data-ttu-id="6ad9b-144">Í hnitanetinu **Yfirlit** skal finna og velja vinnusniðmátið sem á að nota með þessari aðgerð.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-144">In the **Overview** grid, find and select the work template that should be used with this function.</span></span> <span data-ttu-id="6ad9b-145">Fyrir þessar aðstæður skal velja sniðmátið *51 Tína fyrir geymslustað*.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-145">For this scenario, select the *51 Pick to stage* template.</span></span>
1. <span data-ttu-id="6ad9b-146">Á aðgerðasvæðinu skal velja **Breyta fyrirspurn**.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-146">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="6ad9b-147">Í svarglugga fyrirspurnarritils, í flipanum **Röðun**, skal velja **Bæta við** og síðan stilla eftirfarandi gildi fyrir nýju línuna:</span><span class="sxs-lookup"><span data-stu-id="6ad9b-147">In the query editor dialog box, on the **Sorting** tab, select **Add**, and then set the following values for the new row:</span></span>

    - <span data-ttu-id="6ad9b-148">Í dálkinum **Tafla** skal velja *Tímabundnar vinnufærslur*.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-148">In the **Table** column, select *Temporary work transactions*.</span></span>
    - <span data-ttu-id="6ad9b-149">Í dálkinum **Afleidd tafla** skal velja *Tímabundnar vinnufærslur*.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-149">In the **Derived table** column, select *Temporary work transactions*.</span></span>
    - <span data-ttu-id="6ad9b-150">Í dálkinum **Reitur** skal velja *Vörunúmer*.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-150">In the **Field** column, select *Item number*.</span></span>
    - <span data-ttu-id="6ad9b-151">Í dálkinum **Leitarstefna** skal velja *Hækkandi*.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-151">In the **Search direction** column, select *Ascending*.</span></span>

1. <span data-ttu-id="6ad9b-152">Veljið **Í lagi** til að loka svarglugganum og vista breytingarnar.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-152">Select **OK** to close the dialog box and save your selection.</span></span>
1. <span data-ttu-id="6ad9b-153">Eftirfarandi skilaboð birtast: „Flokkun verður endurstillt, á að halda áfram?"</span><span class="sxs-lookup"><span data-stu-id="6ad9b-153">You receive the following message: "Grouping will be reset, continue?"</span></span> <span data-ttu-id="6ad9b-154">Veldu **Já** til að halda áfram.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-154">Select **Yes** to continue.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6ad9b-155">Til að flokkunarvirkni tiltektarlínu virki verður að flokka vinnulínurnar eftir auðkenni hlutar.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-155">For the pick line grouping functionality to work, the work lines must be sorted by item ID.</span></span> <span data-ttu-id="6ad9b-156">Ef línum sem eru með sömu hlutina er ekki skipt í röð hver á eftir annarri verða þær ekki flokkaðar.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-156">If lines that have the same items aren't sequenced one after another, they won't be grouped.</span></span>

## <a name="example"></a><span data-ttu-id="6ad9b-157">Dæmi</span><span class="sxs-lookup"><span data-stu-id="6ad9b-157">Example</span></span>

### <a name="create-picking-work"></a><span data-ttu-id="6ad9b-158">Stofna tiltektarvinnu</span><span class="sxs-lookup"><span data-stu-id="6ad9b-158">Create picking work</span></span>

<span data-ttu-id="6ad9b-159">Áður en þú getur sett upp flokkun tiltektarlína verður þú að búa til einhverja hæfa vinnu á útleið.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-159">Before you can set up pick line grouping, you must create some eligible outbound work.</span></span>

1. <span data-ttu-id="6ad9b-160">Farðu í **Sölu og markaðssetningu \> Sölupöntun \> Allar sölupantanir**.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-160">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="6ad9b-161">Smellið á **Nýtt** til að stofna nýja sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-161">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="6ad9b-162">Í reitnum **Viðskiptavinalykill** skal velja *US-004*.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-162">In the **Customer account** field, select *US-004*.</span></span>
1. <span data-ttu-id="6ad9b-163">Á flýtiflipanum **Almennt**, í reitnum **Vöruhús**, er valið *51*.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-163">On the **General** FastTab, in the **Warehouse** field, select *51*.</span></span>
1. <span data-ttu-id="6ad9b-164">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-164">Select **OK**.</span></span>
1. <span data-ttu-id="6ad9b-165">Í flýtiflipanum **Sölupöntunarlínur** skal bæta við eftirfarandi sex línum:</span><span class="sxs-lookup"><span data-stu-id="6ad9b-165">On the **Sales order lines** FastTab, add the following six lines:</span></span>

    - <span data-ttu-id="6ad9b-166">**Lína 1:** Í reitnum **Vörunúmer** velurðu *M9200*.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-166">**Line 1:** In the **Item number** field, select *M9200*.</span></span> <span data-ttu-id="6ad9b-167">Í **Magn** reitinn er fært inn *3*.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-167">In the **Quantity** field, enter *3*.</span></span>
    - <span data-ttu-id="6ad9b-168">**Lína 2:** Í reitnum **Vörunúmer** velurðu *M9201*.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-168">**Line 2:** In the **Item number** field, select *M9201*.</span></span> <span data-ttu-id="6ad9b-169">Í **Magn** reitinn er fært inn *3*.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-169">In the **Quantity** field, enter *3*.</span></span>
    - <span data-ttu-id="6ad9b-170">**Lína 3:** Í reitnum **Vörunúmer** velurðu *M9202*.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-170">**Line 3:** In the **Item number** field, select *M9202*.</span></span> <span data-ttu-id="6ad9b-171">Í **Magn** reitinn er fært inn *2*.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-171">In the **Quantity** field, enter *2*.</span></span>
    - <span data-ttu-id="6ad9b-172">**Lína 4:** Í reitnum **Vörunúmer** velurðu *M9200*.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-172">**Line 4:** In the **Item number** field, select *M9200*.</span></span> <span data-ttu-id="6ad9b-173">Í **Magn** reitinn er fært inn *1*.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-173">In the **Quantity** field, enter *1*.</span></span>
    - <span data-ttu-id="6ad9b-174">**Lína 5:** Í reitnum **Vörunúmer** velurðu *M9200*.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-174">**Line 5:** In the **Item number** field, select *M9200*.</span></span> <span data-ttu-id="6ad9b-175">Í **Magn** reitinn er fært inn *3*.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-175">In the **Quantity** field, enter *3*.</span></span>
    - <span data-ttu-id="6ad9b-176">**Lína 6:** Í reitnum **Vörunúmer** velurðu *M9202*.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-176">**Line 6:** In the **Item number** field, select *M9202*.</span></span> <span data-ttu-id="6ad9b-177">Í **Magn** reitinn er fært inn *7*.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-177">In the **Quantity** field, enter *7*.</span></span>

    <span data-ttu-id="6ad9b-178">Hér er yfirlit yfir heildarmagn fyrir hverja vöru:</span><span class="sxs-lookup"><span data-stu-id="6ad9b-178">Here is a summary of the total quantities for each item:</span></span>

    - <span data-ttu-id="6ad9b-179">**Vara M9200:** *7* hver</span><span class="sxs-lookup"><span data-stu-id="6ad9b-179">**Item M9200:** *7* each</span></span>
    - <span data-ttu-id="6ad9b-180">**Vara M9201:** *3* hver</span><span class="sxs-lookup"><span data-stu-id="6ad9b-180">**Item M9201:** *3* each</span></span>
    - <span data-ttu-id="6ad9b-181">**Vara M9202:** *9* hver</span><span class="sxs-lookup"><span data-stu-id="6ad9b-181">**Item M9202:** *9* each</span></span>

1. <span data-ttu-id="6ad9b-182">Áður en þú losar pantanir í vöruhúsið verður þú að ganga úr skugga um að tiltektarstaðirnir séu með nægar birgðir fyrir allar vörur í öllum pöntunum.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-182">Before you release the orders to the warehouse, you must make sure that the pick locations have enough inventory for all the items on all the orders.</span></span> <span data-ttu-id="6ad9b-183">Farðu yfir stillinguna **Staðsetningartilskipun** til að ákvarða hvaða tínslustaðir eru notaðir við tínslu sölupöntunum.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-183">Review the **Location directive** setting to determine which picking locations are used for sales order picking.</span></span> <span data-ttu-id="6ad9b-184">Ef verið er að nota umhverfi contoso-sýnigagna fyrir vöruhús *51* skal staðfesta að til séu lausar birgðir.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-184">If you're using the Contoso demo data environment for warehouse *51*, confirm that there is available inventory.</span></span>

    <span data-ttu-id="6ad9b-185">Nú þarf að taka frá birgðirnar fyrir hverja línu.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-185">You must now reserve the inventory for each line.</span></span>

1. <span data-ttu-id="6ad9b-186">Í flýtiflipanum **Sölupöntunarlínur** skal velja eina af línunum sem þarf að taka frá.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-186">On the **Sales order lines** FastTab, select one of the lines that must be reserved.</span></span>
1. <span data-ttu-id="6ad9b-187">Á valmyndinni **Birgðir** fyrir ofan hnitanetið smellir þú á **Frátekning**.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-187">On the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="6ad9b-188">Á síðunni **Frátekning**, á aðgerðasvæðinu, skal velja **Frátektarlota** til að nota frátekninguna.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-188">On the **Reservation** page, on the Action Pane, select **Reserve lot** to apply the reservation.</span></span> <span data-ttu-id="6ad9b-189">Því næst skal loka síðunni.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-189">Then close the page.</span></span>
1. <span data-ttu-id="6ad9b-190">Endurtakið skref 8 til 10 fyrir eftirstandandi línur sem þarf að taka frá.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-190">Repeat steps 8 through 10 for the remaining lines that must be reserved.</span></span>

    <span data-ttu-id="6ad9b-191">Nú þarf að losa sölupöntunina í vöruhúsið.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-191">You must now release the sales order to the warehouse.</span></span>

1. <span data-ttu-id="6ad9b-192">Á aðgerðasvæðinu, í flipanum **Vöruhús**, skal velja **Losa í vöruhús**.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-192">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="6ad9b-193">Skilaboð birtast sem segja að sending og bylgja hafi verið stofnuð og að bylgjan hafi verið send inn til að keyra í runu.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-193">You receive a message that states that a shipment and a wave have been created, and that the wave has been submitted to run in a batch.</span></span>

    <span data-ttu-id="6ad9b-194">Þegar bylgjunni og öllum seinni verkum er lokið er vinnunkenni stofnað fyrir vinnuna sem er með sex línur.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-194">When the wave and all downstream jobs have been completed, a work ID is created for work that has six lines.</span></span> <span data-ttu-id="6ad9b-195">Línunum er raðað eftir vörunúmeri.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-195">The lines are sorted by item number.</span></span>

1. <span data-ttu-id="6ad9b-196">Farið í **Vöruhúsakerfi \> Vinna \> Öll vinna** til að skoða vinnuna sem var stofnuð.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-196">Go to **Warehouse management \> Work \> All work** to view the work that was created.</span></span> <span data-ttu-id="6ad9b-197">Skráið hjá ykkur gildið fyrir **Vinnukennið** því það þarf að nota það í næsta skrefi.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-197">Make a note of the **Work ID** value, because you will need it in the next procedure.</span></span>

### <a name="initiate-picking-from-the-mobile-device"></a><span data-ttu-id="6ad9b-198">Tiltekt hafin í fartæki</span><span class="sxs-lookup"><span data-stu-id="6ad9b-198">Initiate picking from the mobile device</span></span>

1. <span data-ttu-id="6ad9b-199">Skráðu þig inn í fartækið sem notandi sem er settur upp fyrir í vöruhús *51*.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-199">Sign in to the mobile device as a user who is set up for warehouse *51*.</span></span>
1. <span data-ttu-id="6ad9b-200">Í fartækinu velurðu valmynd sem inniheldur nýtt valmyndaratriði fartækis.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-200">On the mobile device, select the menu that includes the new mobile device menu item.</span></span> <span data-ttu-id="6ad9b-201">Fyrir þessar aðstæður skal velja **Á útleið**.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-201">For this scenario, select **Outbound**.</span></span>
1. <span data-ttu-id="6ad9b-202">Veljið valmyndaratriðið **Tiltekt söluflokkslínu** til að hefja tiltektina.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-202">Select the **Sales group line picking** menu item to initiate the pick.</span></span>
1. <span data-ttu-id="6ad9b-203">Færið inn gildið fyrir **Vinnukenni** sem skráð var niður í skrefinu hér á undan.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-203">Enter the **Work ID** value that you made a note of in the previous procedure.</span></span>

    <span data-ttu-id="6ad9b-204">Tiltektarskref ætti að sjást þar sem öllum tiltektarlínum fyrir vöru *M9200* er safnað saman og skipun um að tína *7* af vöru *M9200*.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-204">You should see a pick step where all pick lines for item *M9200* are grouped, and you should receive an instruction to pick *7* each of item *M9200*.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="6ad9b-205">Í fartækinu hefur tiltektarvinnunni fyrir þessar þrjár tiltektarlínur verið safnað saman í eitt tiltektarskref fyrir notandann.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-205">On the mobile device, the pick work for the three pick work lines has been aggregated into one picking step for the user.</span></span>

1. <span data-ttu-id="6ad9b-206">Staðfestu tiltektarskrefið.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-206">Confirm the pick step.</span></span>
1. <span data-ttu-id="6ad9b-207">Farið á vinnusíðu fyrir vinnunkennið og takið eftir að öllum þremur tiltektarlínunum fyrir vöru *M9200* var lokað samtímis.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-207">Go to the work page for the work ID, and notice that all three pick lines for item *M9200* were closed simultaneously.</span></span>
1. <span data-ttu-id="6ad9b-208">Farið aftur í fartækið og haldið áfram með tiltektina.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-208">Go back to the mobile device, and continue to pick.</span></span> <span data-ttu-id="6ad9b-209">Vinnulína 4 fyrir vöru *M9201* ætti að koma upp.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-209">Work line 4 for item *M9201* should be presented.</span></span> <span data-ttu-id="6ad9b-210">Þar sem aðeins ein vinnulína var í pöntuninni er ekkert til að safna saman.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-210">Because there was only one work line on the order, there is nothing to aggregate.</span></span>
1. <span data-ttu-id="6ad9b-211">Staðfestu tiltektarskrefið.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-211">Confirm the pick step.</span></span>
1. <span data-ttu-id="6ad9b-212">Síðasta tiltektarstigið í fartækinu safnar saman síðustu tveimur tiltektarlínunum úr vinnupöntuninni.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-212">The last pick step on the mobile device aggregates the last two pick lines from the work order.</span></span>
1. <span data-ttu-id="6ad9b-213">Ljúkið við tiltektarskrefið fyrir *9* af vöru *M9202*.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-213">Complete the pick step for *9* each of item *M9202*.</span></span>
1. <span data-ttu-id="6ad9b-214">Staðfestu frágangsskrefið og öll viðbótartiltektar-/frágangspör til að klára vinnuna.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-214">Confirm the put step and any additional pick/put pairs to complete the work.</span></span>

> [!IMPORTANT]
>
> - <span data-ttu-id="6ad9b-215">Aðeins er hægt að flokka vinnu línur ef þær eru í röð.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-215">Work lines can be grouped only if they are in sequence.</span></span>
> - <span data-ttu-id="6ad9b-216">Eftirfarandi aðgerðir eru ekki studdar:</span><span class="sxs-lookup"><span data-stu-id="6ad9b-216">The following functionality isn't supported:</span></span>
>
>   - <span data-ttu-id="6ad9b-217">Vörur með framleiðsluþyngd</span><span class="sxs-lookup"><span data-stu-id="6ad9b-217">Catch-weight items</span></span>
>
>    <span data-ttu-id="6ad9b-218">Ef það eru einhverjar framleiðsluþyngdir í vvinnunni færðu villuboð áður en þú byrjar tiltekt.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-218">If there are any catch-weight items on the work, you receive an error message before you start to pick.</span></span>
>
>   - <span data-ttu-id="6ad9b-219">Stykkjatínsla</span><span class="sxs-lookup"><span data-stu-id="6ad9b-219">Piece picking</span></span>
>   - <span data-ttu-id="6ad9b-220">Vinnulínur sem eru með óuppgerða áfyllingarvinnu</span><span class="sxs-lookup"><span data-stu-id="6ad9b-220">Work lines that have unfinished replenishment work</span></span>
>   - <span data-ttu-id="6ad9b-221">Umframtiltekt</span><span class="sxs-lookup"><span data-stu-id="6ad9b-221">Over-picking</span></span>
>   - <span data-ttu-id="6ad9b-222">Endurúthlutun með fyrir vöru</span><span class="sxs-lookup"><span data-stu-id="6ad9b-222">Short picking with item reallocation</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]