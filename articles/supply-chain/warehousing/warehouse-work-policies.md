---
title: Vinnureglur
description: Í þessu efnisatriði er útskýrt hvernig á að setja upp vinnureglur.
author: perlynne
manager: tfehr
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 5ea93324547ed81df120db3412ee41fce2a93f4a
ms.sourcegitcommit: 27233e0fda61dac541c5210ca8d94ab4ba74966f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/03/2020
ms.locfileid: "3652006"
---
# <a name="work-policies"></a><span data-ttu-id="e83e0-103">Vinnureglur</span><span class="sxs-lookup"><span data-stu-id="e83e0-103">Work policies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e83e0-104">Þetta efnisatriði útskýrir hvernig á að setja upp kerfið og vöruhúsaforritið þannig að þau styðji vinnureglur.</span><span class="sxs-lookup"><span data-stu-id="e83e0-104">This topic explains how to set up the system and the warehouse app so that they support work policies.</span></span> <span data-ttu-id="e83e0-105">Hægt er að nota þessa virkni til að skrá birgðir á fljótlegan hátt án þess að stofna frágangsvinnu þegar tekið er á móti innkaupa- eða flutningspöntun, eða þegar lokið er við framleiðsluferla.</span><span class="sxs-lookup"><span data-stu-id="e83e0-105">You can use this functionality to quickly register inventory without creating putaway work when you receive purchase or transfer orders, or when you complete manufacturing processes.</span></span> <span data-ttu-id="e83e0-106">Þetta efnisatriði veitir almennar upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="e83e0-106">This topic provides general information.</span></span> <span data-ttu-id="e83e0-107">Ítarlegar upplýsingar sem tengjast móttöku á númeraplötu er að finna í [Móttaka númeraplötu í gegnum vöruhúsaforritið](warehousing-mobile-device-app-license-plate-receiving.md).</span><span class="sxs-lookup"><span data-stu-id="e83e0-107">For detailed information that is related to license plate receiving, see [License plate receiving via the warehouse app](warehousing-mobile-device-app-license-plate-receiving.md).</span></span>

<span data-ttu-id="e83e0-108">Vinnuregla stjórnar því hvort vöruhúsavinna sé stofnuð þegar framleidd vara er tilkynnt sem lokið eða þegar tekið er á móti vörum með því að nota vöruhúsaforritið.</span><span class="sxs-lookup"><span data-stu-id="e83e0-108">A work policy controls whether warehouse work is created when a manufactured item is reported as finished, or when goods are received by using the warehouse app.</span></span> <span data-ttu-id="e83e0-109">Setja skal upp hverja vinnureglu með því að skilgreina skilyrðin þar sem það á við: gerðir verkbeiðna og ferlar, birgðastaðsetningar og (valfrjálst) afurðirnar.</span><span class="sxs-lookup"><span data-stu-id="e83e0-109">You set up each work policy by defining the conditions where it applies: the work order types and processes, the inventory location, and (optionally) the products.</span></span> <span data-ttu-id="e83e0-110">Til dæmis þarf að móttaka innkaupapöntun fyrir afurð *A0001* á staðsetningu *RECV* í vöruhúsi *24*.</span><span class="sxs-lookup"><span data-stu-id="e83e0-110">For example, a purchase order for product *A0001* must be received in location *RECV* in warehouse *24*.</span></span> <span data-ttu-id="e83e0-111">Síðar er afurðin notuð í öðru ferli á staðsetningu *RECV*.</span><span class="sxs-lookup"><span data-stu-id="e83e0-111">Later, the product is consumed in another process at location *RECV*.</span></span> <span data-ttu-id="e83e0-112">Í slíku tilfelli er hægt að setja upp vinnureglu til að koma í veg fyrir að frágangsvinna verði stofnuð þegar starfsmaður tilkynnir afurð *A0001* sem móttekna á staðsetningu *RECV*.</span><span class="sxs-lookup"><span data-stu-id="e83e0-112">In this case, you can set up a work policy to prevent putaway work from being created when a worker reports product *A0001* as received in location *RECV*.</span></span>

> [!NOTE]
> - <span data-ttu-id="e83e0-113">Til að vinnuregla verði virk þarf að skilgreina að minnsta kosti eina staðsetningu fyrir hana í flýtiflipanum **Birgðastaðsetningar** á síðunni **Vinnureglur**.</span><span class="sxs-lookup"><span data-stu-id="e83e0-113">For a work policy to be active, you must define at least one location for it on the **Inventory locations** FastTab of the **Work policies** page.</span></span> 
> - <span data-ttu-id="e83e0-114">Ekki er hægt að tilgreina sömu staðsetninguna fyrir margar vinnureglur.</span><span class="sxs-lookup"><span data-stu-id="e83e0-114">You can't specify the same location for multiple work policies.</span></span>
> - <span data-ttu-id="e83e0-115">Valkosturinn **Prenta merki** fyrir valmyndaratriði fartækis prentar ekki númeraplötumerki nema vinna hafi verið stofnuð.</span><span class="sxs-lookup"><span data-stu-id="e83e0-115">The **Print label** option for mobile device menu items won't print a license plate label unless work was created.</span></span>

## <a name="activate-the-features-in-your-system"></a><span data-ttu-id="e83e0-116">Gera eiginleikana virka í kerfinu</span><span class="sxs-lookup"><span data-stu-id="e83e0-116">Activate the features in your system</span></span>

<span data-ttu-id="e83e0-117">Til að bjóða upp á alla þá virkni sem lýst er í þessu efnisatriði í kerfinu, skal kveikja á eftirfarandi tveimur eiginleikum í [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):</span><span class="sxs-lookup"><span data-stu-id="e83e0-117">To make all the functionality that is described in this topic available in your system, turn on the following two features in [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):</span></span>

- <span data-ttu-id="e83e0-118">Viðbætur við móttöku á númeraplötu</span><span class="sxs-lookup"><span data-stu-id="e83e0-118">License plate receiving enhancements</span></span>
- <span data-ttu-id="e83e0-119">Endurbætur á vinnureglu fyrir vinnu á innleið</span><span class="sxs-lookup"><span data-stu-id="e83e0-119">Work policy enhancements for inbound work</span></span>

## <a name="the-work-policies-page"></a><span data-ttu-id="e83e0-120">Vinnureglusíðan</span><span class="sxs-lookup"><span data-stu-id="e83e0-120">The Work policies page</span></span>

<span data-ttu-id="e83e0-121">Til að setja upp vinnureglur skal fara í **Vöruhúsakerfi \> Uppsetning \> Vinna \> Vinnureglur**.</span><span class="sxs-lookup"><span data-stu-id="e83e0-121">To set up work policies, go to **Warehouse management \> Setup \> Work \> Work policies**.</span></span> <span data-ttu-id="e83e0-122">Því næst, í hverjum flýtiflipa, skal stilla reitina eins og lýst er í eftirfarandi undirhlutum.</span><span class="sxs-lookup"><span data-stu-id="e83e0-122">Then, on each FastTab, set the fields as described in the following subsections.</span></span>

### <a name="the-work-order-types-fasttab"></a><span data-ttu-id="e83e0-123">Flýtiflipi fyrir gerðir verkbeiðna</span><span class="sxs-lookup"><span data-stu-id="e83e0-123">The Work order types FastTab</span></span>

<span data-ttu-id="e83e0-124">Í flýtiflipanum **Gerðir verkbeiðna** skal bæta við öllum gerðum verkbeiðna og tengdum vinnuferlum sem vinnureglan gildir um.</span><span class="sxs-lookup"><span data-stu-id="e83e0-124">On the **Work order types** FastTab, add all the work order types, and the related work processes, that the work policy applies to.</span></span> <span data-ttu-id="e83e0-125">Eftirfarandi gerðir verkbeiðni og tengdir vinnuferlar eru studdir fyrir vinnureglur.</span><span class="sxs-lookup"><span data-stu-id="e83e0-125">The following work order types and related work processes are supported for work policies.</span></span>

| <span data-ttu-id="e83e0-126">Gerð verkpöntunar</span><span class="sxs-lookup"><span data-stu-id="e83e0-126">Work order type</span></span> | <span data-ttu-id="e83e0-127">Vinnuferli</span><span class="sxs-lookup"><span data-stu-id="e83e0-127">Work process</span></span> |
|---|---|
| <span data-ttu-id="e83e0-128">Tiltekt hráefnis</span><span class="sxs-lookup"><span data-stu-id="e83e0-128">Raw material picking</span></span>| <span data-ttu-id="e83e0-129">Öll tengd ferli</span><span class="sxs-lookup"><span data-stu-id="e83e0-129">All related processes</span></span> |
| <span data-ttu-id="e83e0-130">Frágangur aukaafurða og hliðarafurða</span><span class="sxs-lookup"><span data-stu-id="e83e0-130">Co-product and by-product put away</span></span> | <span data-ttu-id="e83e0-131">Öll tengd ferli</span><span class="sxs-lookup"><span data-stu-id="e83e0-131">All related processes</span></span> |
| <span data-ttu-id="e83e0-132">Frágangur fullbúinnar vöru</span><span class="sxs-lookup"><span data-stu-id="e83e0-132">Finished goods putaway</span></span> | <span data-ttu-id="e83e0-133">Öll tengd ferli</span><span class="sxs-lookup"><span data-stu-id="e83e0-133">All related processes</span></span> |
| <span data-ttu-id="e83e0-134">Flutningsinnhreyfing</span><span class="sxs-lookup"><span data-stu-id="e83e0-134">Transfer receipt</span></span> | <span data-ttu-id="e83e0-135">Móttaka (og frágangur) númeraplötu</span><span class="sxs-lookup"><span data-stu-id="e83e0-135">License plate receiving (and putaway)</span></span> |
| <span data-ttu-id="e83e0-136">Innkaupapantanir</span><span class="sxs-lookup"><span data-stu-id="e83e0-136">Purchase orders</span></span> | <ul><li><span data-ttu-id="e83e0-137">Móttaka (og frágangur) númeraplötu</span><span class="sxs-lookup"><span data-stu-id="e83e0-137">License plate receiving (and putaway)</span></span></li><li><span data-ttu-id="e83e0-138">Móttaka (og frágangur) farmvöru</span><span class="sxs-lookup"><span data-stu-id="e83e0-138">Load item receiving (and putaway)</span></span></li><li><span data-ttu-id="e83e0-139">Móttaka (og frágangur) innkaupapöntunarlínu</span><span class="sxs-lookup"><span data-stu-id="e83e0-139">Purchase order line receiving (and putaway)</span></span></li><li><span data-ttu-id="e83e0-140">Móttaka (og frágangur) innkaupapöntunarvöru</span><span class="sxs-lookup"><span data-stu-id="e83e0-140">Purchase order item receiving (and putaway)</span></span></li></ul> |

<span data-ttu-id="e83e0-141">Til að setja upp vinnureglu þannig að hún eigi við um nokkra vinnuferla sömu verkbeiðnigerðar, skal bæta aðskildri línu fyrir hvert vinnuferli við hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="e83e0-141">To set up a work policy so that it applies to several work processes of the same work order type, add a separate line for each work process to the grid.</span></span>

<span data-ttu-id="e83e0-142">Fyrir hverja línu í hnitanetinu skal stilla reitinn **Aðferðir vinnustofnunar** á eitt af eftirfarandi gildum:</span><span class="sxs-lookup"><span data-stu-id="e83e0-142">For each line in the grid, set the **Work creation method** field to one of the following values:</span></span>

- <span data-ttu-id="e83e0-143">**Aldrei** - Vinnureglan kemur í veg fyrir að vöruhúsavinna verði stofnuð fyrir valda verkbeiðnigerð og tengt vinnuferli.</span><span class="sxs-lookup"><span data-stu-id="e83e0-143">**Never** – The work policy will prevent warehouse work from being created for the selected work order type and related work process.</span></span>
- <span data-ttu-id="e83e0-144">**Dreifing frá dreifingarstöð** - Vinnureglan stofnar dreifingarvinnu frá dreifingarstöð með því að nota regluna sem var valin í reitnum **Heiti reglu fyrir dreifingu frá dreifingarstöð**.</span><span class="sxs-lookup"><span data-stu-id="e83e0-144">**Cross docking** – The work policy will create cross-docking work by using the policy that you select in the **Cross docking policy name** field.</span></span>

### <a name="the-inventory-locations-fasttab"></a><span data-ttu-id="e83e0-145">Flýtiflipi birgðastaðsetninga</span><span class="sxs-lookup"><span data-stu-id="e83e0-145">The Inventory locations FastTab</span></span>

<span data-ttu-id="e83e0-146">Í flýtiflipanum **Birgðastaðsetningar** skal bæta við staðsetningunum þar sem þessi vinnuregla á að gilda.</span><span class="sxs-lookup"><span data-stu-id="e83e0-146">On the **Inventory locations** FastTab, add all the locations where this work policy should be applied.</span></span> <span data-ttu-id="e83e0-147">Ef engin staðsetning tengist vinnureglu, verður vinnureglan ekki notuð fyrir neitt ferli.</span><span class="sxs-lookup"><span data-stu-id="e83e0-147">If no location is associated with a work policy, the work policy won't be applied to any process.</span></span>

<span data-ttu-id="e83e0-148">Ekki er hægt að tilgreina sömu staðsetninguna fyrir margar vinnureglur.</span><span class="sxs-lookup"><span data-stu-id="e83e0-148">You can't specify the same location for multiple work policies.</span></span>

<span data-ttu-id="e83e0-149">Hægt er að nota vöruhúsastaðsetningu sem er úthlutað á staðsetningarforstillingu þar sem slökkt er á valkostinum **Nota rakningu númeraplötu**.</span><span class="sxs-lookup"><span data-stu-id="e83e0-149">You can use a warehouse location that is assigned to a location profile where the **Use license plate tracking** option is turned off.</span></span> <span data-ttu-id="e83e0-150">Í slíku tilfelli skrá starfsmenn lagerbirgðirnir beint.</span><span class="sxs-lookup"><span data-stu-id="e83e0-150">In this case, workers will directly register the on-hand inventory.</span></span>

### <a name="the-products-fasttab"></a><span data-ttu-id="e83e0-151">Flýtiflipi afurða</span><span class="sxs-lookup"><span data-stu-id="e83e0-151">The Products FastTab</span></span>

<span data-ttu-id="e83e0-152">Í flipanum **Afurðir** skal stilla reitinn **Afurðaval** til að stjórna því hvaða afurðir reglan á að gilda fyrir:</span><span class="sxs-lookup"><span data-stu-id="e83e0-152">On the **Products** tab, set the **Product selection** field to control which products the policy should apply to:</span></span>

- <span data-ttu-id="e83e0-153">**Allar** – Reglan á að gilda um allar afurðir.</span><span class="sxs-lookup"><span data-stu-id="e83e0-153">**All** – The policy should apply to all products.</span></span>
- <span data-ttu-id="e83e0-154">**Valið** – Reglan á aðeins að gilda um afurðir sem koma fram í hnitanetinu.</span><span class="sxs-lookup"><span data-stu-id="e83e0-154">**Selected** – The policy should apply only to products that are listed in the grid.</span></span> <span data-ttu-id="e83e0-155">Notið tækjastikuna í flýtiflipanum **Afurðir** til að bæta afurðum við hnitanetið eða fjarlægja þær úr hnitanetinu.</span><span class="sxs-lookup"><span data-stu-id="e83e0-155">Use the toolbar on the **Products** FastTab to add products to the grid or remove them from the grid.</span></span>

## <a name="default-and-custom-to-locations"></a><span data-ttu-id="e83e0-156">Sjálfgefnar og sérsniðnar „til“ staðsetningar</span><span class="sxs-lookup"><span data-stu-id="e83e0-156">Default and custom "to" locations</span></span>

> [!NOTE]
> <span data-ttu-id="e83e0-157">Til að gera virknina sem lýst er í þessum hluta tiltæka í kerfinu þarf að kveikja á eiginleikunum *Viðbætur við móttöku á númeraplötu* og *Viðbætur við vinnureglu fyrir vinnu á innleið* í [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="e83e0-157">To make the functionality that is described in this section available in your system, you must turn on the *License plate receiving enhancements* and *Work policy enhancements for inbound work* features in [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>

<span data-ttu-id="e83e0-158">Áður studdi kerfið að taka aðeins á móti á sjálfgefinni staðsetningu sem er skilgreind fyrir hvert vöruhús.</span><span class="sxs-lookup"><span data-stu-id="e83e0-158">Previously, the system supported receiving only at the default location that is defined for each warehouse.</span></span> <span data-ttu-id="e83e0-159">Valmyndaratriði fartækis sem nota eftirfarandi ferla við stofnun vinnu bjóða aftur á móti upp á valkostinn **Nota sjálfgefin gögn**.</span><span class="sxs-lookup"><span data-stu-id="e83e0-159">However, mobile device menu items that use the following work creation processes now provide the **Use default data** option.</span></span> <span data-ttu-id="e83e0-160">Þessi valkostur gerir kleift að úthluta sérstilltri "til" staðsetningu á eitt eða fleiri valmyndaratriði.</span><span class="sxs-lookup"><span data-stu-id="e83e0-160">This option lets you assign a custom "to" location to one or more menu items.</span></span> <span data-ttu-id="e83e0-161">(Þessi valkostur var þegar tiltækur fyrir nokkrar aðrar gerðir valmyndaratriða.)</span><span class="sxs-lookup"><span data-stu-id="e83e0-161">(This option was already available for some other types of menu items.)</span></span>

- <span data-ttu-id="e83e0-162">Móttaka (og frágangur) númeraplötu</span><span class="sxs-lookup"><span data-stu-id="e83e0-162">License plate receiving (and putaway)</span></span>
- <span data-ttu-id="e83e0-163">Móttaka (og frágangur) farmvöru</span><span class="sxs-lookup"><span data-stu-id="e83e0-163">Load item receiving (and putaway)</span></span>
- <span data-ttu-id="e83e0-164">Móttaka (og frágangur) innkaupapöntunarlínu</span><span class="sxs-lookup"><span data-stu-id="e83e0-164">Purchase order line receiving (and putaway)</span></span>
- <span data-ttu-id="e83e0-165">Móttaka (og frágangur) innkaupapöntunarvöru</span><span class="sxs-lookup"><span data-stu-id="e83e0-165">Purchase order item receiving (and putaway)</span></span>

<span data-ttu-id="e83e0-166">Stillingin **Til staðsetningar** fyrir valmyndaratriði hnekkir sjálfgefinni móttökustaðsetningu fyrir vöruhúsið, fyrir allar pantanir sem unnið er úr með því að nota þetta valmyndaratriði.</span><span class="sxs-lookup"><span data-stu-id="e83e0-166">The **To location** setting for a menu item overrides the default receiving location for the warehouse, for all orders that are processed by using that menu item.</span></span>

<span data-ttu-id="e83e0-167">Til að setja upp valmyndaratriði fartækis til að styðja móttöku á sérstilltri staðsetningu skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="e83e0-167">To set up a mobile device menu item to support receiving at a custom location, follow these steps.</span></span>

1. <span data-ttu-id="e83e0-168">Farðu í **Vöruhúsakerfi \> Uppsetning \> Fartæki \> Valmyndaratriði fartækis**.</span><span class="sxs-lookup"><span data-stu-id="e83e0-168">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="e83e0-169">Veljið eða búið til valmyndaratriði sem notar einn ferlanna við stofnun vinnu sem gefnir eru upp í þessum hluta.</span><span class="sxs-lookup"><span data-stu-id="e83e0-169">Select or create a menu item that uses one of the work creation processes that are listed earlier in this section.</span></span>
1. <span data-ttu-id="e83e0-170">Í flipanum **Almennt** skal stilla valkostinn **Nota sjálfgefin gögn** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="e83e0-170">On the **General** FastTab, set the **Use default data** option to **Yes**.</span></span>
1. <span data-ttu-id="e83e0-171">Á aðgerðasvæðinu skal velja **Sjálfgefin gögn**.</span><span class="sxs-lookup"><span data-stu-id="e83e0-171">On the Action Pane, select **Default data**.</span></span>
1. <span data-ttu-id="e83e0-172">Á síðunni **Sjálfgefin gögn** skal stilla eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="e83e0-172">On the **Default data** page, set the following values:</span></span>

    - <span data-ttu-id="e83e0-173">**Reitur sjálfgefinna gagna:** Stilið þennan reit á *Til staðsetningar*.</span><span class="sxs-lookup"><span data-stu-id="e83e0-173">**Default data field:** Set this field to *To location*.</span></span>
    - <span data-ttu-id="e83e0-174">**Vöruhús:** Veljið vöruhús áfangastaðar til að nota með þessu valmyndaratriði.</span><span class="sxs-lookup"><span data-stu-id="e83e0-174">**Warehouse:** Select the destination warehouse to use with this menu item.</span></span>
    - <span data-ttu-id="e83e0-175">**Staðsetning:** Þessi reitur birtir öll staðsetningarauðkennin sem eru í boði fyrir valið vöruhús.</span><span class="sxs-lookup"><span data-stu-id="e83e0-175">**Location:** This field lists all the location IDs that are available for the selected warehouse.</span></span> <span data-ttu-id="e83e0-176">Stillingin á þessum reit hefur hins vegar engin áhrif í raun og veru.</span><span class="sxs-lookup"><span data-stu-id="e83e0-176">However, the setting of this field doesn't actually have any effect.</span></span> <span data-ttu-id="e83e0-177">Þess vegna er hægt að skilja hann eftir auðan.</span><span class="sxs-lookup"><span data-stu-id="e83e0-177">Therefore, you can leave it blank.</span></span> <span data-ttu-id="e83e0-178">Engu að síður er hægt að nota listann til að staðfesta auðkennið sem færa verður inn í reitinn **Harðkóðað gildi**.</span><span class="sxs-lookup"><span data-stu-id="e83e0-178">Nevertheless, you can use the list to confirm the ID that you must enter in the **Hardcoded value** field.</span></span>
    - <span data-ttu-id="e83e0-179">**Harðkóðað gildi:** Færið inn staðsetningarauðkennið fyrir móttökustaðsetninguna sem gildir um þetta valmyndaratriði.</span><span class="sxs-lookup"><span data-stu-id="e83e0-179">**Hardcoded value:** Enter the location ID for the receiving location that applies to this menu item.</span></span>

> [!TIP]
> <span data-ttu-id="e83e0-180">Vinnureglu er aðeins hægt að nota ef allar móttökustaðsetningarnar eru gefnar upp í uppsetningu viðeigandi vinnureglu.</span><span class="sxs-lookup"><span data-stu-id="e83e0-180">A work policy can be applied only if all the receiving locations are listed in the relevant work policy setup.</span></span> <span data-ttu-id="e83e0-181">Þessi krafa gildir óháð því hvort verið sé að nota sjálfgefna móttökustaðsetningu vöruhúss eða sérstillta „til“ staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="e83e0-181">This requirement applies regardless of whether you're using the default warehouse receiving location or a custom "to" location.</span></span>

## <a name="example-scenario-warehouse-receiving"></a><span data-ttu-id="e83e0-182">Sýnidæmi: Vöruhúsamóttaka</span><span class="sxs-lookup"><span data-stu-id="e83e0-182">Example scenario: Warehouse receiving</span></span>

<span data-ttu-id="e83e0-183">Allar afurðir sem tekið er á móti með ferlinu *Móttaka (og frágangur) innkaupapöntunarvöru* verða að vera skráðar í staðsetningu *FL-001* og þær verða að vera tiltækar í vöruhúsi *24*.</span><span class="sxs-lookup"><span data-stu-id="e83e0-183">All products that are received by the *Purchase order item receiving (and putaway)* process must be registered in location *FL-001*, and they must be available in warehouse *24*.</span></span> <span data-ttu-id="e83e0-184">Hins vegar ætti ekki að stofna vinnu.</span><span class="sxs-lookup"><span data-stu-id="e83e0-184">However, work should not be created.</span></span> <span data-ttu-id="e83e0-185">Afurðir sem tekið er á móti með einhverju öðru ferli (þ.e. með því að nota önnur valmyndaratriði fartækis) á að skrá á sjálfgefna móttökustaðsetningu vöruhúss (*RECV*) og vinnu á að stofna eins og venjulega.</span><span class="sxs-lookup"><span data-stu-id="e83e0-185">Products that are received by any other process (that is, by using other mobile device menu items) should be registered at the default warehouse receiving location (*RECV*), and work should be created as usual.</span></span> <span data-ttu-id="e83e0-186">(Þetta dæmi sýnir ekki uppsetningu sjálfgefinnar móttöku.)</span><span class="sxs-lookup"><span data-stu-id="e83e0-186">(This scenario doesn't show the default receiving setup.)</span></span>

<span data-ttu-id="e83e0-187">Þetta dæmi krefst eftirfarandi þátta:</span><span class="sxs-lookup"><span data-stu-id="e83e0-187">This scenario requires the following elements:</span></span>

- <span data-ttu-id="e83e0-188">Vinnureglu fyrir ferlið *Móttaka (og frágangur) innkaupapöntunarvöru* á staðsetningu *FL-001* fyrir allar afurðir</span><span class="sxs-lookup"><span data-stu-id="e83e0-188">A work policy for the *Purchase order item receiving (and putaway)* process in location *FL-001*, for all products</span></span>
- <span data-ttu-id="e83e0-189">Valmyndaratriði fartækis sem inniheldur sjálfgefin gögn og sem stillir reitinn **Til staðsetningar** á *FL-001*</span><span class="sxs-lookup"><span data-stu-id="e83e0-189">A mobile device menu item that has default data, and that sets the **To location** field to *FL-001*</span></span>

### <a name="prerequisites"></a><span data-ttu-id="e83e0-190">Forkröfur</span><span class="sxs-lookup"><span data-stu-id="e83e0-190">Prerequisites</span></span>

<span data-ttu-id="e83e0-191">Til að gera virknina sem lýst er í þessu dæmi tiltæka í kerfinu þarf að kveikja á eiginleikunum *Viðbætur við móttöku á númeraplötu* og *Viðbætur við vinnureglu fyrir vinnu á innleið* í [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="e83e0-191">To make the functionality that is described in this scenario available in your system, you must turn on the *License plate receiving enhancements* and *Work policy enhancements for inbound work* features in [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>

<span data-ttu-id="e83e0-192">Þetta dæmi notar stöðluð sýnigögn.</span><span class="sxs-lookup"><span data-stu-id="e83e0-192">This scenario uses the standard demo data.</span></span> <span data-ttu-id="e83e0-193">Til að fara í gegnum það með því að nota gildin sem hér koma fram, þarf að nota kerfi þar sem sýnigögn eru uppsett.</span><span class="sxs-lookup"><span data-stu-id="e83e0-193">Therefore, if you want to work through it by using the values that are provided here, you must work on a system where demo data is installed.</span></span> <span data-ttu-id="e83e0-194">Þar að auki verður þú að velja **USMF**-lögaðila.</span><span class="sxs-lookup"><span data-stu-id="e83e0-194">Additionally, you must select the **USMF** legal entity.</span></span>

### <a name="set-up-a-work-policy"></a><span data-ttu-id="e83e0-195">Setja upp vinnureglu</span><span class="sxs-lookup"><span data-stu-id="e83e0-195">Set up a work policy</span></span>

1. <span data-ttu-id="e83e0-196">Fara í **Vöruhúsakerfi \> Uppsetning \> Vinna \> Vinnureglur**.</span><span class="sxs-lookup"><span data-stu-id="e83e0-196">Go to **Warehouse management \> Setup \> Work \> Work policies**.</span></span>
1. <span data-ttu-id="e83e0-197">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="e83e0-197">Select **New**.</span></span>
1. <span data-ttu-id="e83e0-198">Í reitinn **Heiti vinnureglu** skal færa inn *Engin frágangsvinna innkaupavöru*.</span><span class="sxs-lookup"><span data-stu-id="e83e0-198">In the **Work policy name** field, enter *No purchase item putaway work*.</span></span>
1. <span data-ttu-id="e83e0-199">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="e83e0-199">Select **Save**.</span></span>
1. <span data-ttu-id="e83e0-200">Í flýtiflipanum **Gerðir verkbeiðni** skal velja **Bæta við** til að bæta línu við hnitanetið og síðan stilla eftirfarandi gildi fyrir nýju línuna:</span><span class="sxs-lookup"><span data-stu-id="e83e0-200">On the **Work order types** FastTab, select **Add** to add a row to the grid, and then set the following values for the new row:</span></span>

    - <span data-ttu-id="e83e0-201">**Gerð verkbeiðni:** *Innkaupapantanir*</span><span class="sxs-lookup"><span data-stu-id="e83e0-201">**Work order type:** *Purchase orders*</span></span>
    - <span data-ttu-id="e83e0-202">**Vinnuferli:** *Móttaka (og frágangur) innkaupapöntunarvöru*</span><span class="sxs-lookup"><span data-stu-id="e83e0-202">**Work process:** *Purchase order item receiving (and putaway)*</span></span>
    - <span data-ttu-id="e83e0-203">**Aðferð við stofnun vinnu:** *Aldrei*</span><span class="sxs-lookup"><span data-stu-id="e83e0-203">**Work creation method:** *Never*</span></span>
    - <span data-ttu-id="e83e0-204">**Heiti reglu fyrir dreifingu frá dreifingarstöð:** Skiljið reitinn eftir auðan.</span><span class="sxs-lookup"><span data-stu-id="e83e0-204">**Cross docking policy name:** Leave this field blank.</span></span>

1. <span data-ttu-id="e83e0-205">Í flýtiflipanum **Birgðastaðsetningar** skal velja **Bæta við** til að bæta línu við hnitanetið og síðan stilla eftirfarandi gildi fyrir nýju línuna:</span><span class="sxs-lookup"><span data-stu-id="e83e0-205">On the **Inventory locations** FastTab, select **Add** to add a row to the grid, and then set the following values for the new row:</span></span>

    - <span data-ttu-id="e83e0-206">**Vöruhús:** *24*</span><span class="sxs-lookup"><span data-stu-id="e83e0-206">**Warehouse:** *24*</span></span>
    - <span data-ttu-id="e83e0-207">**Staðsetning:** *FL-001*</span><span class="sxs-lookup"><span data-stu-id="e83e0-207">**Location:** *FL-001*</span></span>

1. <span data-ttu-id="e83e0-208">Í flýtiflipanum **Afurðir** skal stilla reitinn **Afurðaval** á *Allt*.</span><span class="sxs-lookup"><span data-stu-id="e83e0-208">On the **Products** FastTab, set the **Product selection** field to *All*.</span></span>
1. <span data-ttu-id="e83e0-209">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="e83e0-209">Select **Save**.</span></span>

### <a name="set-up-a-mobile-device-menu-item-to-change-the-receiving-location"></a><span data-ttu-id="e83e0-210">Setja upp valmyndaratriði fartækis til að breyta móttökustaðsetningunni</span><span class="sxs-lookup"><span data-stu-id="e83e0-210">Set up a mobile device menu item to change the receiving location</span></span>

1. <span data-ttu-id="e83e0-211">Farðu í **Vöruhúsakerfi \> Uppsetning \> Fartæki \> Valmyndaratriði fartækis**.</span><span class="sxs-lookup"><span data-stu-id="e83e0-211">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="e83e0-212">Á svæðinu vinstra megin skal velja fyrirliggjandi valmyndaratriði fyrir **Móttaka innkaupa**.</span><span class="sxs-lookup"><span data-stu-id="e83e0-212">In the left pane, select the existing **Purchase receive** menu item.</span></span>
1. <span data-ttu-id="e83e0-213">Í flipanum **Almennt** skal stilla valkostinn **Nota sjálfgefin gögn** á *Já*.</span><span class="sxs-lookup"><span data-stu-id="e83e0-213">On the **General** FastTab, set the **Use default data** option to *Yes*.</span></span>
1. <span data-ttu-id="e83e0-214">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="e83e0-214">Select **Save**.</span></span>
1. <span data-ttu-id="e83e0-215">Á aðgerðasvæðinu skal velja **Sjálfgefin gögn**.</span><span class="sxs-lookup"><span data-stu-id="e83e0-215">On the Action Pane, select **Default data**.</span></span>
1. <span data-ttu-id="e83e0-216">Í flýtiflipanum **Sjálfgefin gögn**, á aðgerðasvæðinu, skal velja **Ný** til að bæta línu við hnitanetið og síðan stilla eftirfarandi gildi fyrir nýju línuna:</span><span class="sxs-lookup"><span data-stu-id="e83e0-216">On the **Default data** page, on the Action Pane, select **New** to add a row to the grid, and then set the following values for the new row:</span></span>

    - <span data-ttu-id="e83e0-217">**Reitur sjálfgefinna gagna:** *Til staðsetningar*</span><span class="sxs-lookup"><span data-stu-id="e83e0-217">**Default data field:** *To location*</span></span>
    - <span data-ttu-id="e83e0-218">**Vöruhús:** *24*</span><span class="sxs-lookup"><span data-stu-id="e83e0-218">**Warehouse:** *24*</span></span>
    - <span data-ttu-id="e83e0-219">**Staðsetning:** Skiljið þennan reit eftir auðan.</span><span class="sxs-lookup"><span data-stu-id="e83e0-219">**Location:** Leave this field blank.</span></span>
    - <span data-ttu-id="e83e0-220">**Harðkóðað gildi:** *FL-001*</span><span class="sxs-lookup"><span data-stu-id="e83e0-220">**Hardcoded value:** *FL-001*</span></span>

1. <span data-ttu-id="e83e0-221">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="e83e0-221">Select **Save**.</span></span>

### <a name="receive-a-purchase-order-without-creating-work"></a><span data-ttu-id="e83e0-222">Móttaka innkaupapöntun án stofnunar vinnu</span><span class="sxs-lookup"><span data-stu-id="e83e0-222">Receive a purchase order without creating work</span></span>

<span data-ttu-id="e83e0-223">Dæmið í þessum hluta sýnir hvernig á að taka á móti vöru innkaupapöntunar, en án þess að stofna vinnu, á staðsetningu sem er ólík sjálfgefinni móttökustaðsetningu sem er uppsett fyrir vöruhúsið.</span><span class="sxs-lookup"><span data-stu-id="e83e0-223">The example in this section shows how to receive a purchase order item, but without creating work, at a location that differs from the default receiving location that is set up for the warehouse.</span></span> <span data-ttu-id="e83e0-224">Þetta dæmi notar vinnuregluna og atriði fartækis sem búið var til fyrr í þessu sýnidæmi.</span><span class="sxs-lookup"><span data-stu-id="e83e0-224">This example uses the work policy and mobile device item that you created earlier in this scenario.</span></span>

#### <a name="create-a-purchase-order"></a><span data-ttu-id="e83e0-225">Stofna innkaupapöntun</span><span class="sxs-lookup"><span data-stu-id="e83e0-225">Create a purchase order</span></span>

1. <span data-ttu-id="e83e0-226">Farðu í **Innkaup og aðföng \> Innkaupapantanir \> Allar innkaupapantanir**.</span><span class="sxs-lookup"><span data-stu-id="e83e0-226">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="e83e0-227">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="e83e0-227">Select **New**.</span></span>
1. <span data-ttu-id="e83e0-228">Sláðu inn eftirfarandi gildi í svarglugganum **Búa til innkaupapöntun**:</span><span class="sxs-lookup"><span data-stu-id="e83e0-228">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="e83e0-229">**Lánardrottnalykill:** *US-101*</span><span class="sxs-lookup"><span data-stu-id="e83e0-229">**Vendor account:** *US-101*</span></span>
    - <span data-ttu-id="e83e0-230">**Svæði:** *2*</span><span class="sxs-lookup"><span data-stu-id="e83e0-230">**Site:** *2*</span></span>
    - <span data-ttu-id="e83e0-231">**Vöruhús:** *24*</span><span class="sxs-lookup"><span data-stu-id="e83e0-231">**Warehouse:** *24*</span></span>

1. <span data-ttu-id="e83e0-232">Veljið **Í lagi** til að loka svarglugganum og opnið nýju innkaupapöntunina.</span><span class="sxs-lookup"><span data-stu-id="e83e0-232">Select **OK** to close the dialog box and open the new purchase order.</span></span>
1. <span data-ttu-id="e83e0-233">Í flýtiflipanum **Innkaupapöntunarlínur** skal stilla eftirfarandi gildi fyrir auðu línuna:</span><span class="sxs-lookup"><span data-stu-id="e83e0-233">On the **Purchase order lines** FastTab, set the following values for the empty row:</span></span>

    - <span data-ttu-id="e83e0-234">**Vörunúmer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="e83e0-234">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="e83e0-235">**Magn:** *1*</span><span class="sxs-lookup"><span data-stu-id="e83e0-235">**Quantity:** *1*</span></span>

1. <span data-ttu-id="e83e0-236">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="e83e0-236">Select **Save**.</span></span>
1. <span data-ttu-id="e83e0-237">Skráið niður innkaupapöntunarnúmerið.</span><span class="sxs-lookup"><span data-stu-id="e83e0-237">Make a note of the purchase order number.</span></span>

#### <a name="receive-a-purchase-order"></a><span data-ttu-id="e83e0-238">Móttaka innkaupapöntunar</span><span class="sxs-lookup"><span data-stu-id="e83e0-238">Receive a purchase order</span></span>

1. <span data-ttu-id="e83e0-239">Í fartækinu skal skrá sig inn í vöruhús *24* með því að nota *24* fyrir notandakenni og *1* fyrir aðgangsorð.</span><span class="sxs-lookup"><span data-stu-id="e83e0-239">On the mobile device, sign in to warehouse *24* by using *24* as the user ID and *1* as the password.</span></span>
1. <span data-ttu-id="e83e0-240">Veljið **Á innleið**.</span><span class="sxs-lookup"><span data-stu-id="e83e0-240">Select **Inbound**.</span></span>
1. <span data-ttu-id="e83e0-241">Veljið **Innkaup móttekin**.</span><span class="sxs-lookup"><span data-stu-id="e83e0-241">Select **Purchase receive**.</span></span> <span data-ttu-id="e83e0-242">Reiturinn **Staðsetning** ætti að stilla á *FL-001*.</span><span class="sxs-lookup"><span data-stu-id="e83e0-242">The **Location** field should be set to *FL-001*.</span></span>
1. <span data-ttu-id="e83e0-243">Sláið inn innkaupapöntunarnúmerið fyrir innkaupapöntunina sem var stofnuð í fyrra ferlinu.</span><span class="sxs-lookup"><span data-stu-id="e83e0-243">Enter the purchase order number for the purchase order that you created in the previous procedure.</span></span>
1. <span data-ttu-id="e83e0-244">Í **vörunúmerasvæðið** skal slá inn *A0001*.</span><span class="sxs-lookup"><span data-stu-id="e83e0-244">In the **Item number** field, enter *A0001*.</span></span>
1. <span data-ttu-id="e83e0-245">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="e83e0-245">Select **OK**.</span></span>
1. <span data-ttu-id="e83e0-246">Í **Magn** reitinn er fært inn *1*.</span><span class="sxs-lookup"><span data-stu-id="e83e0-246">In the **Quantity** field, enter *1*.</span></span>
1. <span data-ttu-id="e83e0-247">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="e83e0-247">Select **OK**.</span></span>

<span data-ttu-id="e83e0-248">Innkaupapöntunin er nú móttekin en engin vinna er tengd henni.</span><span class="sxs-lookup"><span data-stu-id="e83e0-248">The purchase order is now received, but no work is associated with it.</span></span> <span data-ttu-id="e83e0-249">Lagerbirgðir hafa verið uppfærðar og magn *1* af vöru *A0001* er nú tiltækt á staðsetningu *FL-001*.</span><span class="sxs-lookup"><span data-stu-id="e83e0-249">The on-hand inventory has been updated, and a quantity of *1* of item *A0001* is now available at location *FL-001*.</span></span>

## <a name="example-scenario-manufacturing"></a><span data-ttu-id="e83e0-250">Sýnidæmi: Framleiðsla</span><span class="sxs-lookup"><span data-stu-id="e83e0-250">Example scenario: Manufacturing</span></span>

<span data-ttu-id="e83e0-251">Í eftirfarandi dæmi eru tvær framleiðslupantanir, *PRD 001* og *PRD 002*.</span><span class="sxs-lookup"><span data-stu-id="e83e0-251">In the following example, there are two production orders, *PRD-001* and *PRD-002*.</span></span> <span data-ttu-id="e83e0-252">Framleiðslupöntunin *PRD-001* hefur aðgerðar sem nefnist *Samsetningu*, þar sem afurð *SC1* verið skráð sem lokið á staðsetningu *001*.</span><span class="sxs-lookup"><span data-stu-id="e83e0-252">Production order *PRD-001* has an operation that is named *Assembly*, where product *SC1* is being reported as finished to location *001*.</span></span> <span data-ttu-id="e83e0-253">Framleiðslupöntunin *PRD 002* hefur aðgerðar sem nefnist *Málun* og notar afurð *SC1* frá staðsetningu *001*.</span><span class="sxs-lookup"><span data-stu-id="e83e0-253">Production order *PRD-002* has an operation that is named *Painting* and consumes product *SC1* from location *001*.</span></span> <span data-ttu-id="e83e0-254">Framleiðslupöntunin *PRD-002* notar einnig *RM1* hráefni úr staðsetningunni *001*.</span><span class="sxs-lookup"><span data-stu-id="e83e0-254">Production order *PRD-002* also consumes raw material *RM1* from location *001*.</span></span> <span data-ttu-id="e83e0-255">Hráefni *RM1* er geymt á staðsetningu vöruhúss *BULK-001* og verður tínt yfir á staðsetningu *001* af vöruhúsavinnu fyrir tiltekt hráefnis.</span><span class="sxs-lookup"><span data-stu-id="e83e0-255">Raw material *RM1* is stored in warehouse location *BULK-001* and will be picked to location *001* by warehouse work for raw material picking.</span></span> <span data-ttu-id="e83e0-256">Vinna tiltektar er myndað þegar *PRD 002 framleiðsla* er losuð.</span><span class="sxs-lookup"><span data-stu-id="e83e0-256">The picking work is generated when production *PRD-002* is released.</span></span>

<span data-ttu-id="e83e0-257">[![Reglur vöruhúsavinnu](./media/warehouse-work-policies.png)](./media/warehouse-work-policies.png)</span><span class="sxs-lookup"><span data-stu-id="e83e0-257">[![Warehouse work policies](./media/warehouse-work-policies.png)](./media/warehouse-work-policies.png)</span></span>

<span data-ttu-id="e83e0-258">Þegar ætlunin er að skilgreina vinnureglu vöruhúss fyrir þetta sýnidæmi ætti að hafa eftirfarandi punkta í huga:</span><span class="sxs-lookup"><span data-stu-id="e83e0-258">When you're planning to configure a warehouse work policy for this scenario, you should consider the following points:</span></span>

- <span data-ttu-id="e83e0-259">Vöruhúsavinna fyrir frágang á fullbúnum vörum er ekki áskilin þegar afurð *SC1* er tilkynnt sem lokið frá framleiðslupöntun *PRD-001* til staðsetningar *001*.</span><span class="sxs-lookup"><span data-stu-id="e83e0-259">Warehouse work for putaway of finished goods isn't required when you report product *SC1* as finished from production order *PRD-001* to location *001*.</span></span> <span data-ttu-id="e83e0-260">Ástæðan er vegna þess að aðgerðin *Málun* fyrir framleiðslupöntun *PRD 002* notar afurð *SC1* á sömu staðsetningunni.</span><span class="sxs-lookup"><span data-stu-id="e83e0-260">The reason is that the *Painting* operation for production order *PRD-002* consumes product *SC1* at the same location.</span></span>
- <span data-ttu-id="e83e0-261">Vinna vöruhús fyrir tiltekt hráefnis er krafist til að flytja *RM1* hráefni frá staðsetningu vöruhúss *BULK-001* á staðsetningu *001*.</span><span class="sxs-lookup"><span data-stu-id="e83e0-261">Warehouse work for raw material picking is required to move raw material *RM1* from warehouse location *BULK-001* to location *001*.</span></span>

<span data-ttu-id="e83e0-262">Hér er dæmi um vinnureglu sem hægt er að setja upp, byggt á þessum atriðum:</span><span class="sxs-lookup"><span data-stu-id="e83e0-262">Here is an example of a work policy that you can set up, based on these considerations:</span></span>

- <span data-ttu-id="e83e0-263">**Heiti vinnureglu:** *Engin frágangsvinna*</span><span class="sxs-lookup"><span data-stu-id="e83e0-263">**Work policy name:** *No putaway work*</span></span>
- <span data-ttu-id="e83e0-264">**Gerðir verkbeiðna:** *Frágangur fullbúinna vara* og *Frágangur aukaafurða og hliðarafurða*</span><span class="sxs-lookup"><span data-stu-id="e83e0-264">**Work order types:** *Finished goods put away* and *Co-product and by-product put away*</span></span>
- <span data-ttu-id="e83e0-265">**Birgðastaðsetningar:** Vöruhús *51* og staðsetning *001*</span><span class="sxs-lookup"><span data-stu-id="e83e0-265">**Inventory locations:** Warehouse *51* and location *001*</span></span>
- <span data-ttu-id="e83e0-266">**Afurðir:** *SC1*</span><span class="sxs-lookup"><span data-stu-id="e83e0-266">**Products:** *SC1*</span></span>

<span data-ttu-id="e83e0-267">Eftirfarandi sýnidæmi býður upp á ítarlegar leiðbeiningar um uppsetningu á vinnureglu vöruhúss fyrir þetta dæmi.</span><span class="sxs-lookup"><span data-stu-id="e83e0-267">The following example scenario provides step-by-step instructions for setting up the warehouse work policy for this scenario.</span></span>

## <a name="example-scenario-report-as-finished-to-a-location-that-isnt-license-platecontrolled"></a><span data-ttu-id="e83e0-268">Sýnidæmi: Tilkynna sem lokið á staðsetningu sem er ekki númeraplötustýrð</span><span class="sxs-lookup"><span data-stu-id="e83e0-268">Example scenario: Report as finished to a location that isn't license plate–controlled</span></span>

<span data-ttu-id="e83e0-269">Þetta sýnidæmi kemur með dæmi þar sem framleiðslupöntun er tilkynnt sem lokið á staðsetningu sem er ekki númeraplötustýrð.</span><span class="sxs-lookup"><span data-stu-id="e83e0-269">This scenario shows an example where a production order is reported as finished to a location that isn't license plate–controlled.</span></span>

<span data-ttu-id="e83e0-270">Þetta dæmi notar stöðluð sýnigögn.</span><span class="sxs-lookup"><span data-stu-id="e83e0-270">This scenario uses the standard demo data.</span></span> <span data-ttu-id="e83e0-271">Til að fara í gegnum það með því að nota gildin sem hér koma fram, þarf að nota kerfi þar sem sýnigögn eru uppsett.</span><span class="sxs-lookup"><span data-stu-id="e83e0-271">Therefore, if you want to work through it by using the values that are provided here, you must work on a system where demo data is installed.</span></span> <span data-ttu-id="e83e0-272">Þar að auki verður þú að velja **USMF**-lögaðila.</span><span class="sxs-lookup"><span data-stu-id="e83e0-272">Additionally, you must select the **USMF** legal entity.</span></span>

### <a name="set-up-a-warehouse-work-policy"></a><span data-ttu-id="e83e0-273">Setja upp reglur vöruhúsavinnu</span><span class="sxs-lookup"><span data-stu-id="e83e0-273">Set up a warehouse work policy</span></span>

<span data-ttu-id="e83e0-274">Ferli vöruhúsa innihalda ekki alltaf vöruhúsavinnu.</span><span class="sxs-lookup"><span data-stu-id="e83e0-274">Warehouse processes don't always include warehouse work.</span></span> <span data-ttu-id="e83e0-275">Með því að skilgreina vinnustefnu, sem getur komið í veg fyrir stofnun vinnu fyrir tiltekt hráefnis og frágangur fullbúinna vara fyrir safn af afurðum á tiltekna staði.</span><span class="sxs-lookup"><span data-stu-id="e83e0-275">By defining a work policy, you can prevent the creation of work for raw material picking and putaway of finished goods for a set of products at specific locations.</span></span>

1. <span data-ttu-id="e83e0-276">Fara í **Vöruhúsakerfi \> Uppsetning \> Vinna \> Vinnureglur**.</span><span class="sxs-lookup"><span data-stu-id="e83e0-276">Go to **Warehouse management \> Setup \> Work \> Work policies**.</span></span>
1. <span data-ttu-id="e83e0-277">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="e83e0-277">Select **New**.</span></span>
1. <span data-ttu-id="e83e0-278">Í reitinn **Heiti vinnureglu** skal færa inn *Engin frágangsvinna*.</span><span class="sxs-lookup"><span data-stu-id="e83e0-278">In the **Work policy name** field, enter *No putaway work*.</span></span>
1. <span data-ttu-id="e83e0-279">Í aðgerðarúðunni skal velja **Vista**.</span><span class="sxs-lookup"><span data-stu-id="e83e0-279">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="e83e0-280">Í flýtiflipanum **Gerðir verkbeiðni** skal velja **Bæta við** til að bæta línu við hnitanetið og síðan stilla eftirfarandi gildi fyrir nýju línuna:</span><span class="sxs-lookup"><span data-stu-id="e83e0-280">On the **Work order types** FastTab, select **Add** to add a row to the grid, and then set the following values for the new row:</span></span>

    - <span data-ttu-id="e83e0-281">**Gerð verkbeiðni:** *Frágangur á fullunnum vörum*</span><span class="sxs-lookup"><span data-stu-id="e83e0-281">**Work order type:** *Finished goods put away*</span></span>
    - <span data-ttu-id="e83e0-282">**Vinnuferli:** *Öll tengd vinnuferli*</span><span class="sxs-lookup"><span data-stu-id="e83e0-282">**Work process:** *All related work processes*</span></span>
    - <span data-ttu-id="e83e0-283">**Aðferð við stofnun vinnu:** *Aldrei*</span><span class="sxs-lookup"><span data-stu-id="e83e0-283">**Work creation method:** *Never*</span></span>
    - <span data-ttu-id="e83e0-284">**Heiti reglu fyrir dreifingu frá dreifingarstöð:** Skiljið reitinn eftir auðan.</span><span class="sxs-lookup"><span data-stu-id="e83e0-284">**Cross docking policy name:** Leave this field blank.</span></span>

1. <span data-ttu-id="e83e0-285">Veljið **Bæta við** aftur til að bæta annarri línu við hnitanetið og því næst stilla eftirfarandi gildi fyrir nýju línuna:</span><span class="sxs-lookup"><span data-stu-id="e83e0-285">Select **Add** again to add a second row to the grid, and then set the following values for the new row:</span></span>

    - <span data-ttu-id="e83e0-286">**Gerð verkbeiðni:** *Frágangur aukaafurða og hliðarafurða*</span><span class="sxs-lookup"><span data-stu-id="e83e0-286">**Work order type:** *Co-product and by-product put away*</span></span>
    - <span data-ttu-id="e83e0-287">**Vinnuferli:** *Öll tengd vinnuferli*</span><span class="sxs-lookup"><span data-stu-id="e83e0-287">**Work process:** *All related work processes*</span></span>
    - <span data-ttu-id="e83e0-288">**Aðferð við stofnun vinnu:** *Aldrei*</span><span class="sxs-lookup"><span data-stu-id="e83e0-288">**Work creation method:** *Never*</span></span>
    - <span data-ttu-id="e83e0-289">**Heiti reglu fyrir dreifingu frá dreifingarstöð:** Skiljið reitinn eftir auðan.</span><span class="sxs-lookup"><span data-stu-id="e83e0-289">**Cross docking policy name:** Leave this field blank.</span></span>

1. <span data-ttu-id="e83e0-290">Í flýtiflipanum **Birgðastaðsetningar** skal velja **Bæta við** til að bæta línu við hnitanetið og síðan stilla eftirfarandi gildi fyrir nýju línuna:</span><span class="sxs-lookup"><span data-stu-id="e83e0-290">On the **Inventory locations** FastTab, select **Add** to add a row to the grid, and then set the following values for the new row:</span></span>

    - <span data-ttu-id="e83e0-291">**Vöruhús:** *51*</span><span class="sxs-lookup"><span data-stu-id="e83e0-291">**Warehouse:** *51*</span></span>
    - <span data-ttu-id="e83e0-292">**Staðsetning:** *001*</span><span class="sxs-lookup"><span data-stu-id="e83e0-292">**Location:** *001*</span></span>

1. <span data-ttu-id="e83e0-293">Í flýtiflipanum **Afurðir** skal stilla reitinn **Afurðaval** á *Valið*.</span><span class="sxs-lookup"><span data-stu-id="e83e0-293">On the **Products** FastTab, set the **Product selection** field to *Selected*.</span></span>
1. <span data-ttu-id="e83e0-294">Í flýtiflipanum **Afurðir** skal velja **Bæta við** til að bæta línu við hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="e83e0-294">On the **Products** FastTab, select **Add** to add a row to the grid.</span></span>
1. <span data-ttu-id="e83e0-295">Í nýju línunni skal stilla reitinn **Vörunúmer** á *L0101*.</span><span class="sxs-lookup"><span data-stu-id="e83e0-295">In the new row, set the **Item number** field to *L0101*.</span></span>
1. <span data-ttu-id="e83e0-296">Í aðgerðarúðunni skal velja **Vista**.</span><span class="sxs-lookup"><span data-stu-id="e83e0-296">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-an-output-location"></a><span data-ttu-id="e83e0-297">Setja upp staðsetningu úttaks</span><span class="sxs-lookup"><span data-stu-id="e83e0-297">Set up an output location</span></span>

1. <span data-ttu-id="e83e0-298">Fara á **Fyrirtækisstjórnun \> Tilföng \> Tilfangaflokkar**.</span><span class="sxs-lookup"><span data-stu-id="e83e0-298">Go to **Organization administration \> Resources \> Resource groups**.</span></span>
1. <span data-ttu-id="e83e0-299">Á svæðinu vinstra megin skal velja tilfangaflokkinn **5102**.</span><span class="sxs-lookup"><span data-stu-id="e83e0-299">In the left pane, select resource group **5102**.</span></span>
1. <span data-ttu-id="e83e0-300">Stilltu eftirfarandi gildi á flýtiflipanum **Almennt**:</span><span class="sxs-lookup"><span data-stu-id="e83e0-300">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="e83e0-301">**Vöruhús úttaks:** *51*</span><span class="sxs-lookup"><span data-stu-id="e83e0-301">**Output warehouse:** *51*</span></span>
    - <span data-ttu-id="e83e0-302">**Staðsetning úttaks:** *001*</span><span class="sxs-lookup"><span data-stu-id="e83e0-302">**Output location:** *001*</span></span>

1. <span data-ttu-id="e83e0-303">Í aðgerðarúðunni skal velja **Vista**.</span><span class="sxs-lookup"><span data-stu-id="e83e0-303">On the Action Pane, select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="e83e0-304">Staðsetning *001* er ekki númeraplötustýrð staðsetning.</span><span class="sxs-lookup"><span data-stu-id="e83e0-304">Location *001* isn't a license plate–controlled location.</span></span> <span data-ttu-id="e83e0-305">Hægt er að setja upp staðsetningu úttaks sem er ekki númeraplötustýrð eingöngu ef gildandi vinnuregla er til fyrir staðsetninguna.</span><span class="sxs-lookup"><span data-stu-id="e83e0-305">You can set up an output location that isn't license plate–controlled only if an applicable work policy exists for the location.</span></span>

### <a name="create-a-production-order-and-report-it-as-finished"></a><span data-ttu-id="e83e0-306">Stofna framleiðslupöntun og skrá sem lokið.</span><span class="sxs-lookup"><span data-stu-id="e83e0-306">Create a production order and report it as finished</span></span>

1. <span data-ttu-id="e83e0-307">Fara í **Framleiðslustýringar \> Framleiðslupantanir \> Allar framleiðslupantanir**.</span><span class="sxs-lookup"><span data-stu-id="e83e0-307">Go to **Production control \> Production orders \> All production orders**.</span></span>
1. <span data-ttu-id="e83e0-308">Á aðgerðasvæðinu skal velja **Ný framleiðslupöntun**.</span><span class="sxs-lookup"><span data-stu-id="e83e0-308">On the Action Pane, select **New production order**.</span></span>
1. <span data-ttu-id="e83e0-309">Í svarglugganum **Stofna framleiðslupöntun** skal stilla reitinn **Vörunúmer** á *L0101*.</span><span class="sxs-lookup"><span data-stu-id="e83e0-309">In the **Create production order** dialog box, set the **Item number** field to *L0101*.</span></span>
1. <span data-ttu-id="e83e0-310">Veljið **Stofna** til að stofna pöntunina og loka svarglugganum.</span><span class="sxs-lookup"><span data-stu-id="e83e0-310">Select **Create** to create the order and close the dialog box.</span></span>

    <span data-ttu-id="e83e0-311">Ný framleiðslupöntun er bætt við hnitanetið á síðunni **Allar framleiðslupantanir**.</span><span class="sxs-lookup"><span data-stu-id="e83e0-311">A new production order is added to the grid on the **All production orders** page.</span></span>

    <span data-ttu-id="e83e0-312">Halda nýju framleiðslupöntuninni valdri.</span><span class="sxs-lookup"><span data-stu-id="e83e0-312">Keep the new production order selected.</span></span>

1. <span data-ttu-id="e83e0-313">Á aðgerðasvæðinu, í flipanum **Framleiðslupöntun**, í flokknum **Uppsetning**, skal velja **Áætla**.</span><span class="sxs-lookup"><span data-stu-id="e83e0-313">On the Action Pane, on the **Production order** tab, in the **Process** group, select **Estimate**.</span></span>
1. <span data-ttu-id="e83e0-314">Í svarglugganum **Áætla** skal lesa áætlunina og síðan velja **Í lagi** til að loka svarglugganum.</span><span class="sxs-lookup"><span data-stu-id="e83e0-314">In the **Estimate** dialog box, read the estimate, and then select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="e83e0-315">Á aðgerðasvæðinu, í flipanum **Framleiðslupöntun**, í flokknum **Uppsetning**, skal velja **Hefja**.</span><span class="sxs-lookup"><span data-stu-id="e83e0-315">On the Action Pane, on the **Production order** tab, in the **Process** group, select **Start**.</span></span>
1. <span data-ttu-id="e83e0-316">Í svarglugganum **Hefja**, í flipanum **Almennt**, skal stilla reitinn **Sjálfvirk uppskriftanotkun** á *Aldrei*.</span><span class="sxs-lookup"><span data-stu-id="e83e0-316">In the **Start** dialog box, on the **General** tab, set the **Automatic BOM consumption** field to *Never*.</span></span>
1. <span data-ttu-id="e83e0-317">Veldu **Í lagi** til að vista stillingarnar þínar og loka glugganum.</span><span class="sxs-lookup"><span data-stu-id="e83e0-317">Select **OK** to save your setting and close the dialog box.</span></span>
1. <span data-ttu-id="e83e0-318">Á aðgerðasvæðinu, í flipanum **Framleiðslupöntun**, í flokknum **Uppsetning**, skal velja **Tilkynna sem lokið**.</span><span class="sxs-lookup"><span data-stu-id="e83e0-318">On the Action Pane, on the **Production order** tab, in the **Process** group, select **Report as finished**.</span></span>
1. <span data-ttu-id="e83e0-319">Í svarglugganum **Tilkynna sem lokið**, í flipanum **Almennt**, skal stilla valkostinn **Leyfa villu** á *Já*.</span><span class="sxs-lookup"><span data-stu-id="e83e0-319">In the **Report as finished** dialog box, on the **General** tab, set the **Accept error** option to *Yes*.</span></span>
1. <span data-ttu-id="e83e0-320">Veldu **Í lagi** til að vista stillingarnar þínar og loka glugganum.</span><span class="sxs-lookup"><span data-stu-id="e83e0-320">Select **OK** to save your setting and close the dialog box.</span></span>
1. <span data-ttu-id="e83e0-321">Á aðgerðarrúðunni, á flipanum **Vöruhús**, í hópnum **Almennt** skaltu velja **Upplýsingar um vinnu**.</span><span class="sxs-lookup"><span data-stu-id="e83e0-321">On the Action Pane, on the **Warehouse** tab, in the **General** group, select **Work details**.</span></span>

<span data-ttu-id="e83e0-322">Þegar framleiðslupöntunin er tilkynnt sem lokið, er engin vinna búin til fyrir frágang.</span><span class="sxs-lookup"><span data-stu-id="e83e0-322">When the production order is reported as finished, no work is generated for putaway.</span></span> <span data-ttu-id="e83e0-323">Þetta gerist vegna þess að vinna regla er skilgreind sem kemur í veg fyrir vinnu búnar til þegar afurð *L0101* er skráð sem lokið á staðsetningu *001*.</span><span class="sxs-lookup"><span data-stu-id="e83e0-323">This behavior occurs because a work policy is defined that prevents work from being generated when product *L0101* is reported as finished to location *001*.</span></span>

## <a name="more-information"></a><span data-ttu-id="e83e0-324">Meiri upplýsingar</span><span class="sxs-lookup"><span data-stu-id="e83e0-324">More information</span></span>

<span data-ttu-id="e83e0-325">Nánari upplýsingar um valmyndaratriði fartækja, sjá [Uppsetning fartækja fyrir vöruhúsavinnu](configure-mobile-devices-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="e83e0-325">For more information about mobile device menu items, see [Set up mobile devices for warehouse work](configure-mobile-devices-warehouse.md).</span></span>

<span data-ttu-id="e83e0-326">Frekari upplýsingar um móttöku á númeraplötu og vinnureglur er að finna í [Móttaka númeraplötu í gegnum vöruhúsaforritið](warehousing-mobile-device-app-license-plate-receiving.md).</span><span class="sxs-lookup"><span data-stu-id="e83e0-326">For more information about license plate receiving and work policies, see [License plate receiving via the warehouse app](warehousing-mobile-device-app-license-plate-receiving.md).</span></span>

<span data-ttu-id="e83e0-327">Frekari upplýsingar um stjórnun á farmi á innleið er að finna í [Meðhöndlun vöruhúss á farmi á innleið fyrir innkaupapantanir](inbound-load-handling.md).</span><span class="sxs-lookup"><span data-stu-id="e83e0-327">For more information about inbound load management, see [Warehouse handling of inbound loads for purchase orders](inbound-load-handling.md).</span></span>
