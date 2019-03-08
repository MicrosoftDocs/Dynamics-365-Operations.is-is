---
title: Hlutastaðsetning reglulegrar talningar
description: Áætlanir um reglulega talningu stýra raunverulegum talningaraðgerðum. Hægt er að biðja um að aðeins tilteknar afurðir og afurðaafbrigði séu talin í stað þess að allar efnislegar lagerbirgðir í staðsetningu séu taldar.
author: perlynne
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSCycleCountPlan, WHSWorkLineCycleCount, WHSWorkTemplateLineGroup, WHSWorkTemplateTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cd7cb8b35023ed63af191545d01c60c2c7cc8ef5
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "320651"
---
# <a name="partial-location-cycle-counting"></a><span data-ttu-id="0a3bb-104">Hlutastaðsetning reglulegrar talningar</span><span class="sxs-lookup"><span data-stu-id="0a3bb-104">Partial location cycle counting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0a3bb-105">Áætlanir um reglulega talningu stýra raunverulegum talningaraðgerðum.</span><span class="sxs-lookup"><span data-stu-id="0a3bb-105">Cycle count plans guide the actual counting operations.</span></span> <span data-ttu-id="0a3bb-106">Hægt er að biðja um að aðeins tilteknar afurðir og afurðaafbrigði séu talin í stað þess að allar efnislegar lagerbirgðir í staðsetningu séu taldar.</span><span class="sxs-lookup"><span data-stu-id="0a3bb-106">You can request that only specific products and product variants be counted instead of all on-hand inventory in a location.</span></span>

<span data-ttu-id="0a3bb-107">Með því að nota áætlanir fyrir reglulega talningu, er hægt að stýra raunverulegum talningaraðgerðum.</span><span class="sxs-lookup"><span data-stu-id="0a3bb-107">By using cycle count plans to create counting work, you can guide the actual counting operations.</span></span> <span data-ttu-id="0a3bb-108">Hægt er að biðja um að aðeins tilteknar afurðir og afurðaafbrigði séu talin í stað þess að allar efnislegar lagerbirgðir í staðsetningu séu taldar.</span><span class="sxs-lookup"><span data-stu-id="0a3bb-108">You can request that only specific products and product variants be counted instead of all on-hand inventory in a location.</span></span> <span data-ttu-id="0a3bb-109">Með því að sía tilteknar vörur getur vöruhúsastjóri dregið úr kostnaði við endurskoðun, forðast samstæðumistök og sparað tíma.</span><span class="sxs-lookup"><span data-stu-id="0a3bb-109">By filtering on specific products, the warehouse manager can reduce review overhead, avoid consolidation mistakes, and save time.</span></span>

## <a name="how-to-configure-partial-location-cycle-counting"></a><span data-ttu-id="0a3bb-110">Skilgreining hlutastaðsetningar reglulegrar talningar</span><span class="sxs-lookup"><span data-stu-id="0a3bb-110">How to configure partial location cycle counting</span></span>
<span data-ttu-id="0a3bb-111">Þegar þú notast við vinnuferla vöruhúss í talningaraðgerðum er vinnuhaus stofnaður fyrir hverja staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="0a3bb-111">When you use the warehouse work process for counting operations, a work header is created for each location.</span></span> <span data-ttu-id="0a3bb-112">Þegar þú skilgreinir áætlun fyrir reglulega talningu, getur þú notað fyrirspurnina **Velja staðsetningar** til að takmarka þá talningarvinnu sem stofnað er til.</span><span class="sxs-lookup"><span data-stu-id="0a3bb-112">When you define the cycle count plan, you can use the **Select locations** query to limit the cycle counting work that is created.</span></span> <span data-ttu-id="0a3bb-113">Þegar afurðir fyrir áætlun reglulegrar talningar eru valdar er bæði hægt að velja fyrirspurnir um afurð og afurðarafbirgði til að fínstilla hvað er talið.</span><span class="sxs-lookup"><span data-stu-id="0a3bb-113">When you select products for the cycle count plan, you can select both product and product variant queries to refine what is counted.</span></span> 

<span data-ttu-id="0a3bb-114">Þú getur tengt **vinnusniðmát** við áætlun fyrir reglulega talningu til að skilgreina hvernig regluleg talningarvinna skal stofnuð.</span><span class="sxs-lookup"><span data-stu-id="0a3bb-114">You can associate a **work template** with a cycle count plan to define how the cycle count work should be created.</span></span> <span data-ttu-id="0a3bb-115">Vísað er beint í vinnusniðmát fyrir talningaraðgerðir úr áætlun fyrir reglulega talningu.</span><span class="sxs-lookup"><span data-stu-id="0a3bb-115">The work template for counting operations is directly referenced from the cycle count plan.</span></span> 

<span data-ttu-id="0a3bb-116">Þegar upplýsingar um vinnusniðmát eru skilgreindar getur þú notað valmöguleikann **Vinnulínuskil** til að tilgreina hvort talningarvinnulínurnar eigi að flokkast eftir vörunúmeri eða afurðarafbrigðisnúmeri.</span><span class="sxs-lookup"><span data-stu-id="0a3bb-116">When you define the work template details, you can use the **Work line breaks** option to specify whether the counting work lines must be grouped by item number or product variant number.</span></span> <span data-ttu-id="0a3bb-117">Þessi uppsetning er nauðsynleg viljir þú aðeins telja efnislegar lagerbirgðir fyrir tilteknar afurðir í staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="0a3bb-117">This setup is required if you want to count on-hand inventory only for specific products in a location.</span></span> <span data-ttu-id="0a3bb-118">Vinnulínur fyrir talningarvinnu sem eru stofnaðar munu hafa að geyma þær upplýsingar sem þú skilgreinir hér og stýrðri talningarvinnu er stjórnað á grundvelli þessa stigs.</span><span class="sxs-lookup"><span data-stu-id="0a3bb-118">The cycle counting work lines that are created will have the level of information that you define here, and the guided counting operation will be handled based on this level.</span></span> 

<span data-ttu-id="0a3bb-119">Ef þú tengir áætlanir fyrir reglulega talningu við vinnusniðmát með því að nota valmöguleikann **Vinnulínuskil** er reiturinn **Regluleg talning að hluta** valinn fyrir reglulega talningarvinnu sem stofnuð er og margar vinnulínur fyrir reglulega talningu eru stofnaðar á grundvelli skilgreiningarinnar á vinnusniðmátinu.</span><span class="sxs-lookup"><span data-stu-id="0a3bb-119">If you associate cycle count plans with work templates by using the **Work lines breaks** option, the **Partial cycle count** field is selected for the cycle counting work that is created, and multiple cycle counting work lines will be created based on the definition of the work template.</span></span> 

<span data-ttu-id="0a3bb-120">Áður en vinna við reglulega talningu að hluta getur farið í ferli verður þú að minnsta kosti að velja **Birta vörunúmer** fyrir valmyndaratriði fartækja sem hluta af uppsetningu reglulegrar talningar.</span><span class="sxs-lookup"><span data-stu-id="0a3bb-120">Before partial cycle count work can be processed, you must, at a minimum, select **Display item number** for the mobile device menu item as part of the cycle counting setup.</span></span> <span data-ttu-id="0a3bb-121">Starfsmaður í vöruhúsi verður beðinn að skrá aðeins talningarupplýsingar sem tengjast talningarlínum (vörunúmer og afurðarvíddir).</span><span class="sxs-lookup"><span data-stu-id="0a3bb-121">The warehouse operator will be asked to record only counting information that is related to the counting lines (item numbers and product dimensions).</span></span> <span data-ttu-id="0a3bb-122">Allar aðrar efnislegar lagerbirgðir verða hunsaðar fyrir þetta talningarferli.</span><span class="sxs-lookup"><span data-stu-id="0a3bb-122">All other on-hand inventory will be ignored for this counting process.</span></span> 

<span data-ttu-id="0a3bb-123">Á meðan regluleg talning að hluta fer fram uppfærist dagsetning/tími í **Síðasta reglulega talning** ekki fyrir staðsetninguna.</span><span class="sxs-lookup"><span data-stu-id="0a3bb-123">For the partial cycle count process, the **Last cycle count** date/time won’t be updated for the location.</span></span>

## <a name="example"></a><span data-ttu-id="0a3bb-124">Dæmi</span><span class="sxs-lookup"><span data-stu-id="0a3bb-124">Example</span></span>
<span data-ttu-id="0a3bb-125">Í þessu dæmi þarf aðeins að telja vörunúmer A0001 í vöruhúsi 61.</span><span class="sxs-lookup"><span data-stu-id="0a3bb-125">For this example, only item number A0001 must be counted in warehouse 61.</span></span>

1.  <span data-ttu-id="0a3bb-126">Nýtt vinnusniðmát fyrir reglulega talningu er stofnað.</span><span class="sxs-lookup"><span data-stu-id="0a3bb-126">A new work template for cycle counting is created.</span></span> <span data-ttu-id="0a3bb-127">Valmöguleikinn **Vinnulínuskil** er notaður til að flokka talningarlínur eftir vörunúmerum.</span><span class="sxs-lookup"><span data-stu-id="0a3bb-127">The **Work line breaks** option is used to group counting work lines by item number.</span></span> <span data-ttu-id="0a3bb-128">Þar af leiðandi mun sú reglulega talningarvinna sem stofnuð er hafa línur á hvert vörunúmer.</span><span class="sxs-lookup"><span data-stu-id="0a3bb-128">Therefore, the cycle counting work that is created will have lines per item number.</span></span> <span data-ttu-id="0a3bb-129">Einnig er hægt að flokka línurnar eftir afurðarafbrigðisnúmeri.</span><span class="sxs-lookup"><span data-stu-id="0a3bb-129">You can also group the lines by product variant number.</span></span>
2.  <span data-ttu-id="0a3bb-130">Ný áætlun fyrir reglulega talningu er stofnuð sem vísar í vinnusniðmátið sem var verið að stofna.</span><span class="sxs-lookup"><span data-stu-id="0a3bb-130">A new cycle counting plan is created that references the newly created work template.</span></span> <span data-ttu-id="0a3bb-131">Áætlun fyrir reglulega talningu inniheldur allar staðsetningar í vöruhúsi 61 (fyrirspurnin **Velja staðsetningar**) sem geyma birgðir fyrir vörunúmer A0001.</span><span class="sxs-lookup"><span data-stu-id="0a3bb-131">The cycle counting plan includes all locations in warehouse 61 (**Select locations** query) that hold inventory for item number A0001.</span></span> <span data-ttu-id="0a3bb-132">Val á tilteknum vörum er skilgreint í hlutanum **Afurðarval fyrir reglulega talningu**.</span><span class="sxs-lookup"><span data-stu-id="0a3bb-132">The selection of specific products is defined in the **Cycle count product selections** section.</span></span>
3.  <span data-ttu-id="0a3bb-133">Hægt er að velja vörur fyrir reglulega talningu með því að stilla **Tómar staðsetningar** reitinn á **Taka ekki með tómar**.</span><span class="sxs-lookup"><span data-stu-id="0a3bb-133">You can select products for cycle counting plans by setting the **Empty locations** field to **Exclude empty**.</span></span> <span data-ttu-id="0a3bb-134">Þegar regluleg talning er framkvæmt er hlutatalning fyrir vörunúmer A0001 stofnuð.</span><span class="sxs-lookup"><span data-stu-id="0a3bb-134">When the cycle counting plan is processed, partial cycle count work for item number A0001 is created.</span></span> <span data-ttu-id="0a3bb-135">Hægt er að framkvæma raunverulegt talningarferli með því að nota valmyndaratriði í fartæki fyrir stýrða reglulega talningu.</span><span class="sxs-lookup"><span data-stu-id="0a3bb-135">The actual counting process can be performed by using a mobile device menu item for guided cycle counting.</span></span>



<a name="additional-resources"></a><span data-ttu-id="0a3bb-136">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="0a3bb-136">Additional resources</span></span>
--------

[<span data-ttu-id="0a3bb-137">Regluleg talning</span><span class="sxs-lookup"><span data-stu-id="0a3bb-137">Cycle counting</span></span>](cycle-counting.md)

