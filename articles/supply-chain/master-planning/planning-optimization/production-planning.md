---
title: Framleiðsluáætlun
description: Þetta efnisatriði lýsir áætlanagerð fyrir framleiðslu og útskýrir hvernig á að breyta áætluðum framleiðslupöntunum með því að nota fínstillingu skipulagningar.
author: ChristianRytt
manager: tfehr
ms.date: 12/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-12-15
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: eda22aa6f1e8d665d8ef390f24b247a76d4c2956
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992396"
---
# <a name="production-planning"></a><span data-ttu-id="f0099-103">Framleiðsluáætlun</span><span class="sxs-lookup"><span data-stu-id="f0099-103">Production planning</span></span>

<span data-ttu-id="f0099-104">Fínstilling skipulagningar styður nokkrar framleiðsluaðstæður.</span><span class="sxs-lookup"><span data-stu-id="f0099-104">Planning Optimizations supports several production scenarios.</span></span> <span data-ttu-id="f0099-105">Ef verið er að flytja sig úr fyrirliggjandi innbyggðri aðaláætlunarvél er mikilvægt að gera sér grein fyrir breyttri hegðun.</span><span class="sxs-lookup"><span data-stu-id="f0099-105">If you're migrating from the existing, built-in master planning engine, it's important that you be aware of some changed behavior.</span></span>

<!-- The following video gives a short introduction to some of the current capabilities. 
KFM: Link to video for production functionality, coming soon... -->

## <a name="planned-production-orders"></a><span data-ttu-id="f0099-106">Framleiðslutillögur</span><span class="sxs-lookup"><span data-stu-id="f0099-106">Planned production orders</span></span>

<span data-ttu-id="f0099-107">Þegar aðaláætlanagerð stofnar áætlaðar pantanir til að uppfylla kröfur er pöntunargerðin ákvörðuð af gildinu í reitnum **Gerð áætlaðrar pöntunar**.</span><span class="sxs-lookup"><span data-stu-id="f0099-107">When master planning creates planned orders to fulfill requirements, the order type is determined by the value of the **Planned order type** field.</span></span> <span data-ttu-id="f0099-108">Ef reiturinn **Gerð áætlaðrar pöntunar** er stilltur á *Framleiðsla*, eru áætlaðar framleiðslupantanir stofnaðar.</span><span class="sxs-lookup"><span data-stu-id="f0099-108">If the **Planned order type** field is set to *Production*, planned production orders are created.</span></span> <span data-ttu-id="f0099-109">Í þessum áætluðu framleiðslupöntununum eru upplýsingar um virku uppskriftirnar og kenni leiðar úr tengdri uppsetningu framleiðslu.</span><span class="sxs-lookup"><span data-stu-id="f0099-109">These planned production orders include information about the active bill of materials (BOM) and the route ID from the related production setup.</span></span>

## <a name="requirements-from-boms"></a><span data-ttu-id="f0099-110">Kröfur úr uppskriftum</span><span class="sxs-lookup"><span data-stu-id="f0099-110">Requirements from BOMs</span></span>

<span data-ttu-id="f0099-111">Upplýsingar um uppskrift eru teknar inn í myndina í aðaláætlanagerð.</span><span class="sxs-lookup"><span data-stu-id="f0099-111">BOM information is honored during master planning.</span></span> <span data-ttu-id="f0099-112">Útkoma áætlunarinnar felur í sér framboð á efni til að ná yfir tengda eftirspurn eftir efni fyrir framleiðslu.</span><span class="sxs-lookup"><span data-stu-id="f0099-112">The plan output includes material supply to cover related material demand for production.</span></span>

<span data-ttu-id="f0099-113">Við aðaláætlanagerð er núgildandi virk uppskrift notuð til að ákveða efnin sem þarf fyrir framleiðslu.</span><span class="sxs-lookup"><span data-stu-id="f0099-113">During master planning, the current, active BOM is used to determine the materials that are required for production.</span></span> <span data-ttu-id="f0099-114">Þetta skref er gert í gegnum öll skipulagsstig uppskriftar sem tengist nauðsynlegri framleiðslupöntun.</span><span class="sxs-lookup"><span data-stu-id="f0099-114">This step is done through all levels of the BOM structure that is related to the required production order.</span></span> <span data-ttu-id="f0099-115">Efnisþörf er uppfyllt með því að nota tiltækar birgðir á lager, fyrirliggjandi framboð í pöntun og samþykktar áætlaðar pantanir.</span><span class="sxs-lookup"><span data-stu-id="f0099-115">Material requirement is fulfilled by using available on-hand inventory, existing on-order supply, and approved planned orders.</span></span> <span data-ttu-id="f0099-116">Ef meira efni þarf einhvers staðar verður áætluð pöntun stofnuð til að mæta eftirspurninni.</span><span class="sxs-lookup"><span data-stu-id="f0099-116">If additional material is required anywhere, a planned order is created to cover the demand.</span></span>

## <a name="scheduling-during-firming"></a><span data-ttu-id="f0099-117">Áætlanagerð við staðfestingu</span><span class="sxs-lookup"><span data-stu-id="f0099-117">Scheduling during firming</span></span>

<span data-ttu-id="f0099-118">Áætlaðar framleiðslupantanir innihalda leiðakennið sem er nauðsynlegt fyrir framleiðsluröðun.</span><span class="sxs-lookup"><span data-stu-id="f0099-118">Planned production orders include the route ID that is required for production scheduling.</span></span> <span data-ttu-id="f0099-119">Hins vegar er stuðningur áætlanagerðar í bið á meðan á keyrslu áætlunar stendur fyrir áætlaðar pantanir.</span><span class="sxs-lookup"><span data-stu-id="f0099-119">However, scheduling support during the planning run for planned orders is pending.</span></span> <span data-ttu-id="f0099-120">Leiðarkennið er notað til að tímasetja áætlaðar framleiðslupantanir við staðfestingu.</span><span class="sxs-lookup"><span data-stu-id="f0099-120">The route ID is used to schedule planned production orders during firming.</span></span> <span data-ttu-id="f0099-121">Þess vegna getur afhendingartími á áætluðum framleiðslupöntunum verið frábrugðinn afhendingartíma á tengdri áætlun, staðfestum framleiðslupöntunum sem eru myndaðar úr þeim, eins og lýst er hér:</span><span class="sxs-lookup"><span data-stu-id="f0099-121">Therefore, the lead time on planned production orders can differ from the lead time on related scheduled, firmed production orders that are generated from them, as described here:</span></span>

- <span data-ttu-id="f0099-122">**Áætluð framleiðslupöntun** – Afhendingartími er byggður á föstum afhendingartíma úr útgefinni afurð.</span><span class="sxs-lookup"><span data-stu-id="f0099-122">**Planned production order** – The lead time is based on the static lead time from the released product.</span></span>
- <span data-ttu-id="f0099-123">**Staðfest framleiðslupöntun** – Afhendingartími er byggður á áætlanagerð sem notar upplýsingar um leið og tengdar takmarkanir tilfanga.</span><span class="sxs-lookup"><span data-stu-id="f0099-123">**Firmed production order** – The lead time is based on scheduling that uses route information and related resource constraints.</span></span>

<span data-ttu-id="f0099-124">Frekari upplýsingar um væntanlegt framboð eiginleikans er að finna í [Greining á samsvörun áætlunarfínstillingar](planning-optimization-fit-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="f0099-124">For more information about expected feature availability, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

<span data-ttu-id="f0099-125">Ef treyst er á virkni framleiðslu sem er ekki í boði sem stendur fyrir fínstillingu skipulagningar er hægt að halda áfram að nota innbyggðu aðaláætlunarvélina.</span><span class="sxs-lookup"><span data-stu-id="f0099-125">If you depend on production functionality that isn't yet available for Planning Optimization, you can continue to use the built-in master planning engine.</span></span> <span data-ttu-id="f0099-126">Engar undantekningar eru nauðsynlegar.</span><span class="sxs-lookup"><span data-stu-id="f0099-126">No exception is required.</span></span>

## <a name="delays"></a><span data-ttu-id="f0099-127">Seinkanir</span><span class="sxs-lookup"><span data-stu-id="f0099-127">Delays</span></span>

<span data-ttu-id="f0099-128">Ef afhendingartími fyrir nauðsynlegt efni er lengri en tímabilið frá deginum í dag og til dagsetningar efnisþarfa, verður áætlaðri pöntun fyrir nauðsynlegt efni og tengda framleiðslupöntun frestað.</span><span class="sxs-lookup"><span data-stu-id="f0099-128">If the lead time for required material is longer than the period between today's date and the material requirement date, the planned order for the required material and the related production order will be delayed.</span></span> <span data-ttu-id="f0099-129">Fyrir áætlaðar pantanir er seinkunin (í dögum) reiknuð út frá afhendingartíma útgefinnar afurðar.</span><span class="sxs-lookup"><span data-stu-id="f0099-129">For planned orders, the delay (in days) is calculated based on the lead time from the released product.</span></span> <span data-ttu-id="f0099-130">Upplýsingum um seinkun er síðan komið áleiðis í gegnum öll skipulagsstig uppskriftar.</span><span class="sxs-lookup"><span data-stu-id="f0099-130">The delay information is then propagated through all levels of the BOM structure.</span></span> <span data-ttu-id="f0099-131">Þess vegna er hægt að fylgjast með áhrifum seinkaðra hráefna alla leið að sölupöntun viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="f0099-131">Therefore, you can follow the impact of delayed raw material all the way to the customer sales order.</span></span>

## <a name="modifying-planned-orders"></a><span data-ttu-id="f0099-132">Breyta áætluðum pöntunum</span><span class="sxs-lookup"><span data-stu-id="f0099-132">Modifying planned orders</span></span>

<span data-ttu-id="f0099-133">Þegar upplýsingum er breytt á áætlaðri pöntun birtast eftirfarandi skilaboð: „Hafið í huga að áhrif handvirkra breytinga á tillögur munu ekki koma fram í afganginum af áætluninni fyrr en við næstu keyrslu áætlunargerðar.“</span><span class="sxs-lookup"><span data-stu-id="f0099-133">When you change information on a planned order, you receive the following message: "Note that the impact of manual changes on planned orders won't be reflected in the rest of the plan until the next master planning run."</span></span>

<span data-ttu-id="f0099-134">Ef á að breyta upplýsingum um áætlaða pöntun og sjá áhrifin á tengda efnisþörf skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="f0099-134">If you want to change information on a planned order and see the impact on the related material requirements, follow these steps.</span></span>

1. <span data-ttu-id="f0099-135">Uppfærið áætluðu pöntunina.</span><span class="sxs-lookup"><span data-stu-id="f0099-135">Update the planned order.</span></span>
2. <span data-ttu-id="f0099-136">Samþykkja áætlaða pöntun.</span><span class="sxs-lookup"><span data-stu-id="f0099-136">Approve the planned order.</span></span>
3. <span data-ttu-id="f0099-137">Keyra áætlanagerð.</span><span class="sxs-lookup"><span data-stu-id="f0099-137">Run master planning.</span></span>

<span data-ttu-id="f0099-138">Þegar aðaláætlanagerð er keyrð ætti ekki að nota síur ef áætlaðar framleiðslupantanir eru teknar með.</span><span class="sxs-lookup"><span data-stu-id="f0099-138">When you run master planning, you should not use filters if planned production orders are included.</span></span> <span data-ttu-id="f0099-139">Nánari upplýsingar er að finna í hlutanum [Síur](#filters) síðar í þessu efnisatriði.</span><span class="sxs-lookup"><span data-stu-id="f0099-139">For more information, see the [Filters](#filters) section later in this topic.</span></span>

> [!NOTE]
> <span data-ttu-id="f0099-140">Ef afhendingardagsetningu áætlaðrar pöntunar er breytt í síðari dagsetningu gæti eftirspurnin verið fest við nýja áætlaða pöntun.</span><span class="sxs-lookup"><span data-stu-id="f0099-140">If the delivery date of the planned order is changed to a later date, the demand might be pegged against a new planned order.</span></span> <span data-ttu-id="f0099-141">Þessi hegðun á sér stað þegar nýja birgðadagsetningin veldur töfum á festri eftirspurn en, samkvæmt stillingum afhendingartíma, er hægt að komast hjá seinkuninni.</span><span class="sxs-lookup"><span data-stu-id="f0099-141">This behavior occurs when the new supply date causes a delay for the pegged demand but, according to the lead time settings, the delay can be avoided.</span></span>

## <a name="explosion-page"></a><span data-ttu-id="f0099-142">Niðurbrotssíða</span><span class="sxs-lookup"><span data-stu-id="f0099-142">Explosion page</span></span>

<span data-ttu-id="f0099-143">Hægt er að nota síðuna **Niðurbrot** til að greina eftirspurnina sem þarf fyrir tiltekna framleiðslupöntun eða áætlaða framleiðslupöntun, tengt umfang og upplýsingar um þarfarakningu.</span><span class="sxs-lookup"><span data-stu-id="f0099-143">You can use the **Explosion** page to analyze the demand that is required for a specific production order or planned production order, the related coverage, and pegging information.</span></span> <span data-ttu-id="f0099-144">Upplýsingar á síðunni **Niðurbrot** eru uppfærðar við aðaláætlanagerð.</span><span class="sxs-lookup"><span data-stu-id="f0099-144">Information on the **Explosion** page is updated during master planning.</span></span> <span data-ttu-id="f0099-145">Ekki er hægt að uppfæra upplýsingarnar beint af síðunni **Niðurbrot**.</span><span class="sxs-lookup"><span data-stu-id="f0099-145">You can't update the information directly from the **Explosion** page.</span></span>

## <a name="filters"></a><a name="filters"></a><span data-ttu-id="f0099-146">Síur</span><span class="sxs-lookup"><span data-stu-id="f0099-146">Filters</span></span>

<span data-ttu-id="f0099-147">Fyrir aðstæður áætlanagerðar sem fela í sér framleiðslu er mælt með að forðast síaðar keyrslur aðaláætlanagerðar.</span><span class="sxs-lookup"><span data-stu-id="f0099-147">For planning scenarios that include production, we recommend that you avoid filtered master planning runs.</span></span> <span data-ttu-id="f0099-148">Til að tryggja að fínstilling skipulagningar sé með upplýsingarnar sem þarf til að fá út rétta útkomu við útreikning þarf að hafa með allar afurðir sem á einhvern hátt tengjast afurðunum í öllu skipulagi uppskriftar fyrir áætluðu pöntunina.</span><span class="sxs-lookup"><span data-stu-id="f0099-148">To ensure that Planning Optimization has the information that is required to calculate the correct result, you must include all products that have any relation to products in the whole BOM structure of the planned order.</span></span>

<span data-ttu-id="f0099-149">Þó að háðar undireiningar séu sjálfkrafa greindar og hafðar með í keyrslum aðaláætlanagerðar þegar innbyggð aðaláætlunarvél er notuð, þá framkvæmir fínstilling skipulagningar ekki þessi aðgerð.</span><span class="sxs-lookup"><span data-stu-id="f0099-149">Although dependent child items are automatically detected and included in master planning runs when the built-in master planning engine is used, Planning Optimization doesn't perform this action.</span></span>

<span data-ttu-id="f0099-150">Til dæmis ef einn bolti úr skipulagi uppskriftar fyrir afurð A er einnig notaður til að framleiða afurð B, þá verður að hafa með allar afurðir í skipulagi uppskriftar fyrir afurðir A og B í síuninni.</span><span class="sxs-lookup"><span data-stu-id="f0099-150">For example, if a single bolt from the BOM structure of product A is also used to produce product B, all products in the BOM structure of products A and B must be included in the filter.</span></span> <span data-ttu-id="f0099-151">Það getur verið mjög flókið að ganga úr skugga um að allar afurðir séu hluti af síunni og þar af leiðandi er mælt með að forðast keyrslur á síaðri aðaláætlanagerð þegar framleiðslupantanir eru hafðar með.</span><span class="sxs-lookup"><span data-stu-id="f0099-151">Because it can be very complex to ensure that all products are part of the filter, we recommend that you avoid filtered master planning runs when production orders are involved.</span></span>