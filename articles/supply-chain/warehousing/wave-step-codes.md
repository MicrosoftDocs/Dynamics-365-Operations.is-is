---
title: Kóðar bylgjuskrefs
description: Þetta efni veitir yfirlit yfir bylgjuskrefakóða og hvernig þeir eru notaðir.
author: josaw1
manager: AnnBe
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 0f89c6098db9e2e3a9aa4ee3666e4b9ae608f054
ms.sourcegitcommit: d8f1135cdbc2deca70bc4b2805a0519253c9a31f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/06/2019
ms.locfileid: "1992358"
---
# <a name="wave-step-codes"></a><span data-ttu-id="748f5-103">Kóðar bylgjuskrefs</span><span class="sxs-lookup"><span data-stu-id="748f5-103">Wave step codes</span></span>

[!include [banner](../includes/preview-banner.md)]
[!include [banner](../includes/banner.md)]

## <a name="about-wave-step-codes"></a><span data-ttu-id="748f5-104">Um bylgjuskrefakóða</span><span class="sxs-lookup"><span data-stu-id="748f5-104">About wave step codes</span></span>

<span data-ttu-id="748f5-105">Bylgjuskrefakóðar eru kóðar sem notendur geta sett upp og notað til að tengja sérstök tilvik bylgjuaðferða við samsvarandi sniðmát.</span><span class="sxs-lookup"><span data-stu-id="748f5-105">Wave step codes are codes that users can set up and use to link specific instances of wave methods to a corresponding template.</span></span> <span data-ttu-id="748f5-106">Sniðmátin innihalda sniðmát fyrir áfyllingu, gámagerð, prentun merkimiða, byggingu álags og flokkun.</span><span class="sxs-lookup"><span data-stu-id="748f5-106">The templates include templates for replenishment, containerization, label printing, load building, and sorting.</span></span>

<span data-ttu-id="748f5-107">Þegar bylgjuskrefakóðar eru ekki notaðir, verða notendur að slá inn frjálsan texta til að vísa í ákveðið sniðmát frá bylgjuaðferðartilvikinu.</span><span class="sxs-lookup"><span data-stu-id="748f5-107">When wave step codes aren't used, users must enter free text to reference a specific template from the wave method instance.</span></span> <span data-ttu-id="748f5-108">Frjáls texti er viðkvæmur fyrir villum, vegna þess að notendur verða að ganga úr skugga um að bylgjuskrefatextinn sem þeir bæta við fyrir tiltekna bylgjuþrepaðferð í bylgjusniðmáti samsvari nákvæmlega bylgjuskrefatextanum í marksniðinu.</span><span class="sxs-lookup"><span data-stu-id="748f5-108">Free text is prone to error, because users must make sure that the wave step text that they add for a specific wave step method in a wave template exactly matches the wave step text in the target template.</span></span>

<span data-ttu-id="748f5-109">Bylgjuskrefakóðar fyrir ákveðna gerð bylgjuskrefa eru settir upp á aðskildri síðu.</span><span class="sxs-lookup"><span data-stu-id="748f5-109">Wave step codes for a specific wave step type are set up on a separate page.</span></span> <span data-ttu-id="748f5-110">Fyrir hvert tilvik um bylgjuþrep í bylgjusniðmát sem krefst bylgjuþrepskóða verður að velja bylgjuskrefakóðann í fellilistanum.</span><span class="sxs-lookup"><span data-stu-id="748f5-110">For every wave step method instance in a wave template that requires a wave step code, the wave step code must be selected in a drop-down list.</span></span> <span data-ttu-id="748f5-111">Val í fellivalmynd kemur í staðinn fyrir frjálsan texta og hjálpar til við að draga úr hættu og áhrifum mannlegra mistaka.</span><span class="sxs-lookup"><span data-stu-id="748f5-111">Selection in a drop-down list replaces free text entry and helps reduce the risk and impact of human error.</span></span> <span data-ttu-id="748f5-112">Uppsetningarkóðar eru notaðir til að tengja bylgjuþrep aðferð í bylgjusniðmát við marksnið fyrir aðferðina.</span><span class="sxs-lookup"><span data-stu-id="748f5-112">Setup codes are used to link a wave step method in a wave template to a target template for the method.</span></span>

> [!NOTE]
> <span data-ttu-id="748f5-113">Notkun eiginleika bylgjuskrefakóða er valkvæð og upptaka er á lögaðila.</span><span class="sxs-lookup"><span data-stu-id="748f5-113">Use of the wave step codes feature is optional, and uptake is per legal entity.</span></span> <span data-ttu-id="748f5-114">Þess vegna, ef sérstakur lögaðili notar eiginleikann, eru allir fyrirliggjandi bylgjuskrefakóðar í lögaðilanum uppfærðir í nýja uppbygginguna.</span><span class="sxs-lookup"><span data-stu-id="748f5-114">Therefore, if a specific legal entity uses the feature, all existing wave step codes in that legal entity are upgraded to the new structure.</span></span>

## <a name="setup-demo"></a><span data-ttu-id="748f5-115">Setja upp kynningu</span><span class="sxs-lookup"><span data-stu-id="748f5-115">Setup demo</span></span> 

<span data-ttu-id="748f5-116">Fyrir þessa kynningu verða kynningargögn að vera sett upp og þú verður að nota kynningarfyrirtækið **USMF**.</span><span class="sxs-lookup"><span data-stu-id="748f5-116">For this demo, demo data must be installed, and you must use the **USMF** demo data company.</span></span>

### <a name="enable-wave-step-codes"></a><span data-ttu-id="748f5-117">Virkja kóða bylgjuskrefs</span><span class="sxs-lookup"><span data-stu-id="748f5-117">Enable wave step codes</span></span>

<span data-ttu-id="748f5-118">Fylgdu þessum skrefum til að kveikja á bylgjuskrefakóða.</span><span class="sxs-lookup"><span data-stu-id="748f5-118">Follow these steps to turn on the wave step codes feature.</span></span>

1. <span data-ttu-id="748f5-119">Farðu í **vöruhúsakerfi \> Uppsetning \> Færibreytur vöruhúsakerfis**.</span><span class="sxs-lookup"><span data-stu-id="748f5-119">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>
2. <span data-ttu-id="748f5-120">Á flipanum **Almennt** á flýtiflipanum **Úrvinnsla bylgna** skal stilla valkostinn **Virkja bylgjuskrefakóða** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="748f5-120">On the **General** tab, on the **Wave processing** FastTab, set the **Enable wave step codes** option to **Yes**.</span></span>

<span data-ttu-id="748f5-121">Allir fyrirliggjandi frjálsir textar bylgjuskrefa eru uppfærðir í nýja uppbygginguna.</span><span class="sxs-lookup"><span data-stu-id="748f5-121">All existing wave step free texts are upgraded to the new structure.</span></span> <span data-ttu-id="748f5-122">Eftir að þessari uppfærslu er lokið fyrir lögaðila er valkosturinn **Virkja bylgjuskrefakóða** er ekki lengur tiltækur á síðunni **Færibreytur vöruhúsastjórnunar**.</span><span class="sxs-lookup"><span data-stu-id="748f5-122">After this upgrade is completed for a legal entity, the **Enable wave step codes** option is no longer available on the **Warehouse management parameters** page.</span></span>

<span data-ttu-id="748f5-123">Staðfestingar eru gerðar við uppfærsluna og ef uppfærslan mistekst færðu villuboð.</span><span class="sxs-lookup"><span data-stu-id="748f5-123">Validations are done during the upgrade, and if the upgrade fails, you receive an error message.</span></span> <span data-ttu-id="748f5-124">Uppfærsla gæti mistekist vegna eftirfarandi árekstra:</span><span class="sxs-lookup"><span data-stu-id="748f5-124">An upgrade might fail because of the following conflicts:</span></span>

- <span data-ttu-id="748f5-125">Tvíteknir frjálsir textar bylgjuskrefa eru til.</span><span class="sxs-lookup"><span data-stu-id="748f5-125">Duplicate wave step free texts exist.</span></span>
- <span data-ttu-id="748f5-126">Sérsnið er til staðar.</span><span class="sxs-lookup"><span data-stu-id="748f5-126">Customizations exist.</span></span>
- <span data-ttu-id="748f5-127">Frjáls texti bylgjuskrefa sem er tengdur dæmi um aðferð við bylgjuþrep passar ekki við gerð sniðmátsins.</span><span class="sxs-lookup"><span data-stu-id="748f5-127">A wave step free text that is associated with a wave step method instance doesn't match the expected template type.</span></span>

<span data-ttu-id="748f5-128">Eftir að þú hefur leyst alla árekstra sem eru greindir við staðfestingarnar geturðu keyrt uppfærsluferlið aftur.</span><span class="sxs-lookup"><span data-stu-id="748f5-128">After you've resolved any conflicts that are identified during the validations, you can rerun the upgrade process.</span></span>

<span data-ttu-id="748f5-129">Þegar uppfærslan tekst verður síðan **Bylgjuskrefakóðar** (**Vöruhúsastjórnun \> Uppsetning \> Bylgjur \> Bylgjuskrefakóðar**) í boði.</span><span class="sxs-lookup"><span data-stu-id="748f5-129">When the upgrade succeeds, the **Wave step codes** page (**Warehouse management \> Setup \> Waves \> Wave step codes**) becomes available.</span></span> <span data-ttu-id="748f5-130">Þessi síða sýnir bylgjuskrefakóða sem voru uppfærðir þegar kveikt var á eiginleikum bylgjuskrefakóða.</span><span class="sxs-lookup"><span data-stu-id="748f5-130">This page lists the wave step codes that were upgraded when the wave step codes feature was turned on.</span></span>

### <a name="create-new-wave-step-codes"></a><span data-ttu-id="748f5-131">Stofna nýja bylgjuskrefakóða</span><span class="sxs-lookup"><span data-stu-id="748f5-131">Create new wave step codes</span></span>

<span data-ttu-id="748f5-132">Þú getur notað síðuna **Bylgjuskrefakóðar** til að búa til og eyða bylgjuskrefakóðum.</span><span class="sxs-lookup"><span data-stu-id="748f5-132">You can use the **Wave step codes** page to create and delete wave step codes.</span></span>

<span data-ttu-id="748f5-133">Sérhver nýr bylgjuskrefakóði og það tilheyrandi auðkenni verður að vera sérstakt fyrir allar tegundir bylgjuskrefa og verður að skilgreina þær fyrir ákveðna gerð bylgjuskrefa.</span><span class="sxs-lookup"><span data-stu-id="748f5-133">Every new wave step code and its associated ID must be unique across all wave step types, and they must be defined for a specific wave step type.</span></span>

### <a name="apply-wave-step-codes"></a><span data-ttu-id="748f5-134">Beita bylgjuskrefakóðum</span><span class="sxs-lookup"><span data-stu-id="748f5-134">Apply wave step codes</span></span>

<span data-ttu-id="748f5-135">Eftir að þú hefur skilgreint viðeigandi bylgjuskrefakóða er hægt að beita þeim á bylgjuferlaaðferðirnar.</span><span class="sxs-lookup"><span data-stu-id="748f5-135">After you've defined the appropriate wave step codes, they can be applied to the wave process methods.</span></span>

<span data-ttu-id="748f5-136">Til að beita bylgjuskrefakóða, farðu í viðeigandi marksniðmát.</span><span class="sxs-lookup"><span data-stu-id="748f5-136">To apply wave step codes, go to the appropriate target template.</span></span> <span data-ttu-id="748f5-137">Hér eru marksniðmát sem bylgjuskrefakóðarnir eru tilnefndir til að benda á:</span><span class="sxs-lookup"><span data-stu-id="748f5-137">Here are the target templates that the wave step codes are designated to point to:</span></span>

- <span data-ttu-id="748f5-138">**Sniðmát áfyllingar:** Vöruhúsakerfi \> Uppsetning \> Áfylling \> Áfyllingarsniðmát</span><span class="sxs-lookup"><span data-stu-id="748f5-138">**Replenishment templates:** Warehouse management \> Setup \> Replenishment \> Replenishment templates</span></span>
- <span data-ttu-id="748f5-139">**Hlaða sniðmát:** Vöruhúsastjórnun \> Uppsetning \> Álag \> Sniðmát hleðslu</span><span class="sxs-lookup"><span data-stu-id="748f5-139">**Load build templates:** Warehouse management \> Setup \> Load \> Load build templates</span></span>
- <span data-ttu-id="748f5-140">**Raða sniðmátum:** Vöruhúsastjórnun \> Uppsetning \> Pökkun \> Sniðmát fyrir útleið</span><span class="sxs-lookup"><span data-stu-id="748f5-140">**Sort templates:** Warehouse management \> Setup \> Packing \> Outbound sorting templates</span></span>
- <span data-ttu-id="748f5-141">**Gámunarsniðmát:** Vöruhúsakerfi \> Uppsetning \> Gámar \> Gámaröðunarsniðmát</span><span class="sxs-lookup"><span data-stu-id="748f5-141">**Containerization templates:** Warehouse management \> Setup \> Containers \> Container build templates</span></span>
- <span data-ttu-id="748f5-142">**Sniðmát fyrir prentunarmerki:** Vöruhúsastjórnun \> Uppsetning \> Beining skjals \> Sniðmát bylgju</span><span class="sxs-lookup"><span data-stu-id="748f5-142">**Label printing templates:** Warehouse management \> Setup \> Document routing \> Wave label templates</span></span>

<span data-ttu-id="748f5-143">Sniðmátin á þessum lista eru notuð þegar þeim er vísað frá bylgjuferlisaðferð sem er valin í bylgjusniðmát.</span><span class="sxs-lookup"><span data-stu-id="748f5-143">The templates in this list are applied when they are referenced from a wave process method that is selected in a wave template.</span></span> <span data-ttu-id="748f5-144">Þegar bylgjuskrefakóðinn á bylgjuferlisaðferð í bylgjusniðmáti passar bylgjuskrefakóðann í einni af sniðmátategundunum er sniðmátinu beitt.</span><span class="sxs-lookup"><span data-stu-id="748f5-144">When the wave step code on a wave process method in a wave template matches the wave step code in one of the templates types, the template is applied.</span></span>

### <a name="sample-scenario"></a><span data-ttu-id="748f5-145">Dæmi</span><span class="sxs-lookup"><span data-stu-id="748f5-145">Sample scenario</span></span>

<span data-ttu-id="748f5-146">Eftirfarandi aðferð hjálpar til við að tryggja að endurnýjunarsniðmátið sem þú bjóst til verður beitt fyrir bylgjusniðmát.</span><span class="sxs-lookup"><span data-stu-id="748f5-146">The following procedure helps guarantee that the replenishment template that you created will be applied for the wave template.</span></span>

1. <span data-ttu-id="748f5-147">Farðu í **Vöruhúsastjórnun \> Uppsetning \> Bylgjur \> Bylgjuskrefakóðar**, og stofnaðu bylgjuskrefakóða fyrir gerðina **Endurnýjun**.</span><span class="sxs-lookup"><span data-stu-id="748f5-147">Go to **Warehouse management \> Setup \> Waves \> Wave step codes**, and create a wave step code for the **Replenishment** type.</span></span>
2. <span data-ttu-id="748f5-148">Farðu í **Vöruhúsakerfi \> Uppsetning \> Áfylling \> Áfyllingarsniðmát** og stofnaðu áfyllingarsniðmát.</span><span class="sxs-lookup"><span data-stu-id="748f5-148">Go to **Warehouse management \> Setup \> Replenishment \> Replenishment templates**, and create a replenishment template.</span></span>
3. <span data-ttu-id="748f5-149">Veldu áfyllingar sniðmátið, veldu bylgjuskrefakóðann sem þú bjóst til fyrir gerðina **Áfylling**.</span><span class="sxs-lookup"><span data-stu-id="748f5-149">In the replenishment template, select the wave step code that you created for the **Replenishment** type.</span></span>
4. <span data-ttu-id="748f5-150">Farðu í **Vöruhúsastjórnun \> Uppsetning \> Bylgjur \> Bylgjusniðmát** og veldu bylgjusniðmátið sem þú ætlar að nota.</span><span class="sxs-lookup"><span data-stu-id="748f5-150">Go to **Warehouse management \> Setup \> Waves \> Wave templates**, and select the wave template that you intend to use.</span></span>
5. <span data-ttu-id="748f5-151">Í sniðmátinu á flýtiflipanum **Aðferðir** velurðu aðferðina **Áfylling**.</span><span class="sxs-lookup"><span data-stu-id="748f5-151">In the template, on the **Methods** FastTab, select the **Replenishment** method.</span></span>
6. <span data-ttu-id="748f5-152">Í reitnum **Bylgjuskrefakóði** velurðu bylgjuskrefakóðann sem þú valdir í áfyllingarsniðinu.</span><span class="sxs-lookup"><span data-stu-id="748f5-152">In the **Wave step code** field, select the wave step code that you selected in the replenishment template.</span></span>
