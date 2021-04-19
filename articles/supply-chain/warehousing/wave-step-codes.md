---
title: Kóðar bylgjuskrefs
description: Þetta efni veitir yfirlit yfir bylgjuskrefakóða og hvernig þeir eru notaðir.
author: josaw1
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWaveTableListPage, WHSWaveStepCode, WHSReplenishmentTemplates, WHSWaveTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f44d500d58dffb37b27d230b0633336eb87996a6
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838059"
---
# <a name="wave-step-codes"></a><span data-ttu-id="6035c-103">Kóðar bylgjuskrefs</span><span class="sxs-lookup"><span data-stu-id="6035c-103">Wave step codes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6035c-104">Bylgjuskrefakóðar eru kóðar sem notendur geta sett upp og notað til að tengja sérstök tilvik bylgjuaðferða við samsvarandi sniðmát.</span><span class="sxs-lookup"><span data-stu-id="6035c-104">Wave step codes are codes that users can set up and use to link specific instances of wave methods to a corresponding template.</span></span> <span data-ttu-id="6035c-105">Sniðmátin innihalda sniðmát fyrir áfyllingu, gámagerð, prentun merkimiða, byggingu álags og flokkun.</span><span class="sxs-lookup"><span data-stu-id="6035c-105">The templates include templates for replenishment, containerization, label printing, load building, and sorting.</span></span>

<span data-ttu-id="6035c-106">Þegar bylgjuskrefakóðar eru ekki notaðir, verða notendur að slá inn frjálsan texta til að vísa í ákveðið sniðmát frá bylgjuaðferðartilvikinu.</span><span class="sxs-lookup"><span data-stu-id="6035c-106">When wave step codes aren't used, users must enter free text to reference a specific template from the wave method instance.</span></span> <span data-ttu-id="6035c-107">Frjáls texti er viðkvæmur fyrir villum, vegna þess að notendur verða að ganga úr skugga um að bylgjuskrefatextinn sem þeir bæta við fyrir tiltekna bylgjuþrepaðferð í bylgjusniðmáti samsvari nákvæmlega bylgjuskrefatextanum í marksniðinu.</span><span class="sxs-lookup"><span data-stu-id="6035c-107">Free text is prone to errors because users must make sure that the wave step text that they add for a specific wave step method in a wave template exactly matches the wave step text in the target template.</span></span>

<span data-ttu-id="6035c-108">Bylgjuskrefakóðar fyrir ákveðna gerð bylgjuskrefa eru settir upp á aðskildri síðu.</span><span class="sxs-lookup"><span data-stu-id="6035c-108">Wave step codes for a specific wave step type are set up on a separate page.</span></span> <span data-ttu-id="6035c-109">Fyrir hvert tilvik um bylgjuþrep í bylgjusniðmát sem krefst bylgjuþrepskóða verður að velja bylgjuskrefakóðann í fellilistanum.</span><span class="sxs-lookup"><span data-stu-id="6035c-109">For every wave step method instance in a wave template that requires a wave step code, the wave step code must be selected in a drop-down list.</span></span> <span data-ttu-id="6035c-110">Val í fellivalmynd kemur í staðinn fyrir frjálsan texta og hjálpar til við að draga úr hættu og áhrifum mannlegra mistaka.</span><span class="sxs-lookup"><span data-stu-id="6035c-110">Selection in a drop-down list replaces free text entry and helps reduce the risk and impact of human error.</span></span> <span data-ttu-id="6035c-111">Uppsetningarkóðar eru notaðir til að tengja bylgjuþrep aðferð í bylgjusniðmát við marksnið fyrir aðferðina.</span><span class="sxs-lookup"><span data-stu-id="6035c-111">Setup codes are used to link a wave step method in a wave template to a target template for the method.</span></span>

> [!NOTE]
> <span data-ttu-id="6035c-112">Notkun kóðaeiginleika bylgjuskrefa er valkvæð.</span><span class="sxs-lookup"><span data-stu-id="6035c-112">Use of the wave step codes feature is optional.</span></span> <span data-ttu-id="6035c-113">Hún er virkjum í öllu fyrirtækinu fyrir alla lögaðila.</span><span class="sxs-lookup"><span data-stu-id="6035c-113">It is enabled organization-wide for all legal entities.</span></span>

## <a name="setup-demo"></a><span data-ttu-id="6035c-114">Setja upp kynningu</span><span class="sxs-lookup"><span data-stu-id="6035c-114">Setup demo</span></span> 

<span data-ttu-id="6035c-115">Fyrir þessa kynningu verða kynningargögn að vera sett upp og þú verður að nota kynningarfyrirtækið **USMF**.</span><span class="sxs-lookup"><span data-stu-id="6035c-115">For this demo, demo data must be installed, and you must use the **USMF** demo data company.</span></span>

### <a name="enable-wave-step-codes"></a><span data-ttu-id="6035c-116">Virkja kóða bylgjuskrefs</span><span class="sxs-lookup"><span data-stu-id="6035c-116">Enable wave step codes</span></span>

<span data-ttu-id="6035c-117">Fylgdu þessum skrefum til að kveikja á bylgjuskrefakóða.</span><span class="sxs-lookup"><span data-stu-id="6035c-117">Follow these steps to turn on the wave step codes feature.</span></span>

1. <span data-ttu-id="6035c-118">Farðu í **Stjórnun eiginleika**.</span><span class="sxs-lookup"><span data-stu-id="6035c-118">Go to **Feature Management**.</span></span>
2. <span data-ttu-id="6035c-119">Veldu til að virkja eiginleikann sem heitir **Kóði bylgjuskrefa í öllu fyrirtækinu**.</span><span class="sxs-lookup"><span data-stu-id="6035c-119">Select to enable the feature called **Organization-wide Wave Step Code**.</span></span>

<span data-ttu-id="6035c-120">Allir fyrirliggjandi frjálsir textar bylgjuskrefa í öllum lögaðilum eru uppfærðir í nýja uppbygginguna.</span><span class="sxs-lookup"><span data-stu-id="6035c-120">All existing wave step free texts in all legal entities are upgraded to the new structure.</span></span> <span data-ttu-id="6035c-121">Eftir að þessari uppfærslu er lokið fyrir alla lögaðila er eiginleikinn virkur.</span><span class="sxs-lookup"><span data-stu-id="6035c-121">After this upgrade is completed for all legal entities, then the feature is enabled.</span></span> <span data-ttu-id="6035c-122">Ef ekki er hægt að virkja eiginleikann fyrir einn eða fleiri lögaðila er hann ekki virkur fyrir neina lögaðila.</span><span class="sxs-lookup"><span data-stu-id="6035c-122">If the feature cannot be enabled for one or more legal entities, then the feature is not enabled for any legal entities.</span></span>

<span data-ttu-id="6035c-123">Meðan á virkjuninni stendur er staðfesting gerð við uppfærslu gagna.</span><span class="sxs-lookup"><span data-stu-id="6035c-123">During the enablement, validations are done during the data upgrade.</span></span> <span data-ttu-id="6035c-124">Ef uppfærsla mistekst færðu villuboð.</span><span class="sxs-lookup"><span data-stu-id="6035c-124">If the upgrade fails, you receive an error message.</span></span> <span data-ttu-id="6035c-125">Uppfærsla gæti mistekist vegna eftirfarandi árekstra:</span><span class="sxs-lookup"><span data-stu-id="6035c-125">An upgrade might fail because of the following conflicts:</span></span>

- <span data-ttu-id="6035c-126">Tvíteknir frjálsir textar bylgjuskrefa eru til.</span><span class="sxs-lookup"><span data-stu-id="6035c-126">Duplicate wave step free texts exist.</span></span>
- <span data-ttu-id="6035c-127">Sérsnið er til staðar.</span><span class="sxs-lookup"><span data-stu-id="6035c-127">Customizations exist.</span></span>
- <span data-ttu-id="6035c-128">Frjáls texti bylgjuskrefa sem er tengdur dæmi um aðferð við bylgjuþrep passar ekki við gerð sniðmátsins.</span><span class="sxs-lookup"><span data-stu-id="6035c-128">A wave step free text that is associated with a wave step method instance doesn't match the expected template type.</span></span>

<span data-ttu-id="6035c-129">Eftir að þú hefur leyst alla árekstra sem eru greindir við staðfestingarnar geturðu reynt aftur að virkja eiginleikann.</span><span class="sxs-lookup"><span data-stu-id="6035c-129">After you've resolved any conflicts that are identified during the validations, you can retry to enable the feature.</span></span>

<span data-ttu-id="6035c-130">Þegar eiginleikinn hefur verið virkjaður verður síðan **Bylgjuskrefakóðar** (**Vöruhúsastjórnun \> Uppsetning \> Bylgjur \> Bylgjuskrefakóðar**) í boði.</span><span class="sxs-lookup"><span data-stu-id="6035c-130">When the feature has been enabled, the **Wave step codes** page (**Warehouse management \> Setup \> Waves \> Wave step codes**) becomes available.</span></span> <span data-ttu-id="6035c-131">Þessi síða sýnir bylgjuskrefakóða sem voru uppfærðir þegar eiginleikinn Kóði bylgjuskrefa í öllu fyrirtækinu var virkjaður.</span><span class="sxs-lookup"><span data-stu-id="6035c-131">This page lists the wave step codes that were upgraded when the Organization-wide Wave Step Code feature was enabled.</span></span>

### <a name="create-new-wave-step-codes"></a><span data-ttu-id="6035c-132">Stofna nýja bylgjuskrefakóða</span><span class="sxs-lookup"><span data-stu-id="6035c-132">Create new wave step codes</span></span>

<span data-ttu-id="6035c-133">Þú getur notað síðuna **Bylgjuskrefakóðar** til að búa til og eyða bylgjuskrefakóðum.</span><span class="sxs-lookup"><span data-stu-id="6035c-133">You can use the **Wave step codes** page to create and delete wave step codes.</span></span>

<span data-ttu-id="6035c-134">Sérhver nýr bylgjuskrefakóði og það tilheyrandi auðkenni verður að vera sérstakt fyrir allar tegundir bylgjuskrefa og verður að skilgreina þær fyrir ákveðna gerð bylgjuskrefa.</span><span class="sxs-lookup"><span data-stu-id="6035c-134">Every new wave step code and its associated ID must be unique across all wave step types, and they must be defined for a specific wave step type.</span></span>

### <a name="apply-wave-step-codes"></a><span data-ttu-id="6035c-135">Beita bylgjuskrefakóðum</span><span class="sxs-lookup"><span data-stu-id="6035c-135">Apply wave step codes</span></span>

<span data-ttu-id="6035c-136">Eftir að þú hefur skilgreint viðeigandi bylgjuskrefakóða er hægt að beita þeim á bylgjuferlaaðferðirnar.</span><span class="sxs-lookup"><span data-stu-id="6035c-136">After you've defined the appropriate wave step codes, they can be applied to the wave process methods.</span></span>

<span data-ttu-id="6035c-137">Til að beita bylgjuskrefakóða, farðu í viðeigandi marksniðmát.</span><span class="sxs-lookup"><span data-stu-id="6035c-137">To apply wave step codes, go to the appropriate target template.</span></span> <span data-ttu-id="6035c-138">Hér eru marksniðmát sem bylgjuskrefakóðarnir eru tilnefndir til að benda á:</span><span class="sxs-lookup"><span data-stu-id="6035c-138">Here are the target templates that the wave step codes are designated to point to:</span></span>

- <span data-ttu-id="6035c-139">**Sniðmát áfyllingar:** Vöruhúsakerfi \> Uppsetning \> Áfylling \> Áfyllingarsniðmát</span><span class="sxs-lookup"><span data-stu-id="6035c-139">**Replenishment templates:** Warehouse management \> Setup \> Replenishment \> Replenishment templates</span></span>
- <span data-ttu-id="6035c-140">**Hlaða sniðmát:** Vöruhúsastjórnun \> Uppsetning \> Álag \> Sniðmát hleðslu</span><span class="sxs-lookup"><span data-stu-id="6035c-140">**Load build templates:** Warehouse management \> Setup \> Load \> Load build templates</span></span>
- <span data-ttu-id="6035c-141">**Raða sniðmátum:** Vöruhúsastjórnun \> Uppsetning \> Pökkun \> Sniðmát fyrir útleið</span><span class="sxs-lookup"><span data-stu-id="6035c-141">**Sort templates:** Warehouse management \> Setup \> Packing \> Outbound sorting templates</span></span>
- <span data-ttu-id="6035c-142">**Gámunarsniðmát:** Vöruhúsakerfi \> Uppsetning \> Gámar \> Gámaröðunarsniðmát</span><span class="sxs-lookup"><span data-stu-id="6035c-142">**Containerization templates:** Warehouse management \> Setup \> Containers \> Container build templates</span></span>
- <span data-ttu-id="6035c-143">**Sniðmát fyrir prentunarmerki:** Vöruhúsastjórnun \> Uppsetning \> Beining skjals \> Sniðmát bylgju</span><span class="sxs-lookup"><span data-stu-id="6035c-143">**Label printing templates:** Warehouse management \> Setup \> Document routing \> Wave label templates</span></span>

<span data-ttu-id="6035c-144">Sniðmátin á þessum lista eru notuð þegar þeim er vísað frá bylgjuferlisaðferð sem er valin í bylgjusniðmát.</span><span class="sxs-lookup"><span data-stu-id="6035c-144">The templates in this list are applied when they are referenced from a wave process method that is selected in a wave template.</span></span> <span data-ttu-id="6035c-145">Þegar bylgjuskrefakóðinn á bylgjuferlisaðferð í bylgjusniðmáti passar bylgjuskrefakóðann í einni af sniðmátategundunum er sniðmátinu beitt.</span><span class="sxs-lookup"><span data-stu-id="6035c-145">When the wave step code on a wave process method in a wave template matches the wave step code in one of the templates types, the template is applied.</span></span>

### <a name="sample-scenario"></a><span data-ttu-id="6035c-146">Dæmi</span><span class="sxs-lookup"><span data-stu-id="6035c-146">Sample scenario</span></span>

<span data-ttu-id="6035c-147">Eftirfarandi aðferð hjálpar til við að tryggja að endurnýjunarsniðmátið sem þú bjóst til verður beitt fyrir bylgjusniðmát.</span><span class="sxs-lookup"><span data-stu-id="6035c-147">The following procedure helps guarantee that the replenishment template that you created will be applied for the wave template.</span></span>

1. <span data-ttu-id="6035c-148">Farðu í **Vöruhúsastjórnun \> Uppsetning \> Bylgjur \> Bylgjuskrefakóðar**, og stofnaðu bylgjuskrefakóða fyrir gerðina **Endurnýjun**.</span><span class="sxs-lookup"><span data-stu-id="6035c-148">Go to **Warehouse management \> Setup \> Waves \> Wave step codes**, and create a wave step code for the **Replenishment** type.</span></span>
2. <span data-ttu-id="6035c-149">Farðu í **Vöruhúsakerfi \> Uppsetning \> Áfylling \> Áfyllingarsniðmát** og stofnaðu áfyllingarsniðmát.</span><span class="sxs-lookup"><span data-stu-id="6035c-149">Go to **Warehouse management \> Setup \> Replenishment \> Replenishment templates**, and create a replenishment template.</span></span>
3. <span data-ttu-id="6035c-150">Veldu áfyllingar sniðmátið, veldu bylgjuskrefakóðann sem þú bjóst til fyrir gerðina **Áfylling**.</span><span class="sxs-lookup"><span data-stu-id="6035c-150">In the replenishment template, select the wave step code that you created for the **Replenishment** type.</span></span>
4. <span data-ttu-id="6035c-151">Farðu í **Vöruhúsastjórnun \> Uppsetning \> Bylgjur \> Bylgjusniðmát** og veldu bylgjusniðmátið sem þú ætlar að nota.</span><span class="sxs-lookup"><span data-stu-id="6035c-151">Go to **Warehouse management \> Setup \> Waves \> Wave templates**, and select the wave template that you intend to use.</span></span>
5. <span data-ttu-id="6035c-152">Í sniðmátinu á flýtiflipanum **Aðferðir** velurðu aðferðina **Áfylling**.</span><span class="sxs-lookup"><span data-stu-id="6035c-152">In the template, on the **Methods** FastTab, select the **Replenishment** method.</span></span>
6. <span data-ttu-id="6035c-153">Í reitnum **Bylgjuskrefakóði** velurðu bylgjuskrefakóðann sem þú valdir í áfyllingarsniðinu.</span><span class="sxs-lookup"><span data-stu-id="6035c-153">In the **Wave step code** field, select the wave step code that you selected in the replenishment template.</span></span>

<span data-ttu-id="6035c-154">Þú framkvæmir þessi skref fyrir hvern lögaðila.</span><span class="sxs-lookup"><span data-stu-id="6035c-154">You perform these steps for each legal entity.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]