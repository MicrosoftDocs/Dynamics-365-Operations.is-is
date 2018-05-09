---
title: "Afurðarafbrigði byggt á vídd"
description: "Afurðarafbrigði sem byggist á víddum stendur fyrir einfalda lausn til að búa til mörg afbrigði vöru frá einum afurðarsniðmáti og uppskrift þess."
author: cvocph
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMConfigRule, BOMTable, ConfigChooseFromRoute, ConfigGroup, ConfigHierarchy, EcoResDimensionBasedConfiguration
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19821
ms.assetid: 4db9890b-306b-4be7-ba98-3be2094d561f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 18e53494b5cdb49c0bf7e8c311f17bfdbff78b0d
ms.contentlocale: is-is
ms.lasthandoff: 05/08/2018

---

# <a name="dimension-based-product-configuration"></a><span data-ttu-id="38bd1-103">Afurðarafbrigði byggt á vídd</span><span class="sxs-lookup"><span data-stu-id="38bd1-103">Dimension-based product configuration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="38bd1-104">Afurðarafbrigði sem byggist á víddum stendur fyrir einfalda lausn til að búa til mörg afbrigði vöru frá einum afurðarsniðmáti og uppskrift þess.</span><span class="sxs-lookup"><span data-stu-id="38bd1-104">Dimension-based product configuration represents a simple solution for creating many product variants from a single product master and its bill of materials.</span></span>

<span data-ttu-id="38bd1-105">Skilgreiningu afurðarafbrigðis sem byggja á víddum er einn af þremur innbyggðu afbrigðistækni afurðar.</span><span class="sxs-lookup"><span data-stu-id="38bd1-105">Dimension-based product configuration is one of the three built-in product configuration technologies.</span></span> <span data-ttu-id="38bd1-106">Hinar tvær tækninálganirnar eru forskilgreind afbrigði og skorðuskilgreining.</span><span class="sxs-lookup"><span data-stu-id="38bd1-106">The two other technologies are predefined variants and constraint-based configuration.</span></span> <span data-ttu-id="38bd1-107">Allar þrjár tækninálganirnar nota afurðarsniðmát sem upphafspunkt og leyfa notanda að stofna margar afurðarafbrigða fyrir eitt afurðarsniðmát .</span><span class="sxs-lookup"><span data-stu-id="38bd1-107">All three technologies use a product master as the starting point and allow the user to create many product variants for one product master.</span></span>

## <a name="key-concepts"></a><span data-ttu-id="38bd1-108">Lykilhugtök</span><span class="sxs-lookup"><span data-stu-id="38bd1-108">Key concepts</span></span>
<span data-ttu-id="38bd1-109">Skilgreiningu afurðarafbrigðis sem byggja á víddum byggist á eftirfarandi grundvallarhugtök:</span><span class="sxs-lookup"><span data-stu-id="38bd1-109">Dimension-based product configuration is based on the following key concepts:</span></span>

-   <span data-ttu-id="38bd1-110">Afurðarsniðmát</span><span class="sxs-lookup"><span data-stu-id="38bd1-110">Product masters</span></span>
-   <span data-ttu-id="38bd1-111">Skilgreind Afurðarvídd</span><span class="sxs-lookup"><span data-stu-id="38bd1-111">Configuration product dimension</span></span>
-   <span data-ttu-id="38bd1-112">Afbrigðaflokkar</span><span class="sxs-lookup"><span data-stu-id="38bd1-112">Configuration groups</span></span>
-   <span data-ttu-id="38bd1-113">Uppskrift</span><span class="sxs-lookup"><span data-stu-id="38bd1-113">Bill of materials (BOM)</span></span>
-   <span data-ttu-id="38bd1-114">Afbrigðaleið</span><span class="sxs-lookup"><span data-stu-id="38bd1-114">Configuration route</span></span>
-   <span data-ttu-id="38bd1-115">Afbrigðareglur</span><span class="sxs-lookup"><span data-stu-id="38bd1-115">Configuration rules</span></span>

### <a name="product-masters"></a><span data-ttu-id="38bd1-116">Afurðarsniðmát</span><span class="sxs-lookup"><span data-stu-id="38bd1-116">Product masters</span></span>

<span data-ttu-id="38bd1-117">Afurðarsniðmát er upphafspunkt fyrir öll afurðarafbrigðisferli.</span><span class="sxs-lookup"><span data-stu-id="38bd1-117">A product master is the starting point for any product configuration process.</span></span> <span data-ttu-id="38bd1-118">Fyrir afurðarafbrigði sem byggja á víddum þarf afurðarsniðmát með þessu tiltekna afbrigðistækni og afurðavíddaflokk sem inniheldur víddaskilgreiningu afurðar.</span><span class="sxs-lookup"><span data-stu-id="38bd1-118">For the dimension-based product configuration, you need a product master with this particular configuration technology and a product dimension group that includes the configuration product dimension.</span></span>

### <a name="configuration-product-dimension"></a><span data-ttu-id="38bd1-119">Skilgreind Afurðarvídd</span><span class="sxs-lookup"><span data-stu-id="38bd1-119">Configuration product dimension</span></span>

<span data-ttu-id="38bd1-120">Víddaskilgreining afurðar er notuð til að auðkenna afurðarafbrigði fyrir afurðarsniðmát með skilgreiningartækninni sem byggist á víddum.</span><span class="sxs-lookup"><span data-stu-id="38bd1-120">The configuration product dimension is used to identify the product variants for a product master with the dimension-based configuration technology.</span></span> <span data-ttu-id="38bd1-121">víddargildi Skilgreiningar er færð inn af notandanum ætti að hjálpa við að auðkenna einstaka afurðarafbrigði.</span><span class="sxs-lookup"><span data-stu-id="38bd1-121">The configuration dimension value is entered by the user and should help to identify the individual product variants.</span></span>

### <a name="configuration-groups"></a><span data-ttu-id="38bd1-122">Afbrigðaflokkar</span><span class="sxs-lookup"><span data-stu-id="38bd1-122">Configuration groups</span></span>

<span data-ttu-id="38bd1-123">Afbrigðaflokkar eru skilgreindar í miðlægri geymslu og er hægt að nota fyrir allar afbrigðalíkönum afurða sem byggja á víddum.</span><span class="sxs-lookup"><span data-stu-id="38bd1-123">Configuration groups are defined in a central repository and can be used for all dimension-based product configuration models.</span></span> <span data-ttu-id="38bd1-124">Afbrigðaflokkar eru tengdir einstaka uppskriftalínur og halda saman flokki af línum sem gagnkvæmt útiloka hverja aðra.</span><span class="sxs-lookup"><span data-stu-id="38bd1-124">Configuration groups are associated to the individual BOM lines and hold together a group of lines that are mutually exclusive.</span></span> <span data-ttu-id="38bd1-125">Þetta þýðir að hægt er að velja aðeins eina lína í flokki fyrir eitt afurðarafbrigði.</span><span class="sxs-lookup"><span data-stu-id="38bd1-125">This means that only one line in a group can be selected for a single product variant.</span></span>

### <a name="bill-of-materials-bom"></a><span data-ttu-id="38bd1-126">Uppskrift</span><span class="sxs-lookup"><span data-stu-id="38bd1-126">Bill of materials (BOM)</span></span>

<span data-ttu-id="38bd1-127">Uppskriftin standa fyrir einingar fyrir afurðarafbrigði sem byggja á víddum.</span><span class="sxs-lookup"><span data-stu-id="38bd1-127">The BOM represent the building blocks for a dimension-based product configuration.</span></span> <span data-ttu-id="38bd1-128">Það verður að innihalda allar mismunandi afurðir sem hægt er að nota í hvaða afurðarafbrigði sem er.</span><span class="sxs-lookup"><span data-stu-id="38bd1-128">It must include all the different products that can be used in any product variant.</span></span> <span data-ttu-id="38bd1-129">Hverja línu í Uppskriftinni getur vísað til afbrigðaflokkur.</span><span class="sxs-lookup"><span data-stu-id="38bd1-129">Each line in the BOM can reference a configuration group.</span></span> <span data-ttu-id="38bd1-130">Ef línu ekki vísa afbrigðaflokkur er hún höfð með í öll afurðarafbrigði.</span><span class="sxs-lookup"><span data-stu-id="38bd1-130">If a line doesn’t reference a configuration group, it will be included in all product variants.</span></span>

### <a name="configuration-route"></a><span data-ttu-id="38bd1-131">Afbrigðaleið</span><span class="sxs-lookup"><span data-stu-id="38bd1-131">Configuration route</span></span>

<span data-ttu-id="38bd1-132">Skilgreiningarleiðinni ákvarðar röð skilgreiningarflokka, eins og þær birtast notandanum við ferli afurðarafbrigðis.</span><span class="sxs-lookup"><span data-stu-id="38bd1-132">The configuration route determines the sequence of the configuration groups, as they will be displayed to the user during the product configuration process.</span></span>

### <a name="configuration-rules"></a><span data-ttu-id="38bd1-133">Afbrigðareglur</span><span class="sxs-lookup"><span data-stu-id="38bd1-133">Configuration rules</span></span>

<span data-ttu-id="38bd1-134">Skilgreiningarreglur tákna mekanisma til að tryggja að afurð sem er í einumafbrigðisflokk í Uppskrift framkalli annað hvort meðtalningu eða útilokun fyrir vöru í mismunandi afbrigðisflokkum í sömu uppskrift.</span><span class="sxs-lookup"><span data-stu-id="38bd1-134">The configuration rules represent a mechanism for ensuring that a product included in one configuration group in a BOM enforces either an inclusion or an exclusion of a product in a different configuration group in the same BOM.</span></span>

## <a name="product-modeling-process"></a><span data-ttu-id="38bd1-135">Ferli vörulíkanagerðar</span><span class="sxs-lookup"><span data-stu-id="38bd1-135">Product modeling process</span></span>
<span data-ttu-id="38bd1-136">Eðlileg röðun til að byggja vörulíkan fyrir afurð sem byggist á víddum byrjar á skilgreiningu viðeigandi afbrigðisflokka.</span><span class="sxs-lookup"><span data-stu-id="38bd1-136">The natural sequence for building a product model for a dimension-based product starts with defining the relevant configuration groups.</span></span> <span data-ttu-id="38bd1-137">Það er mikilvægt að tryggja að allar afurðir sem verður notaður í Uppskriftinni hafa verið losaðar í fyrirtækið sem vörulíkan er búið til fyrir.</span><span class="sxs-lookup"><span data-stu-id="38bd1-137">It is important to ensure that all products which will be used in the BOM have been released to the company that the product model is built for.</span></span> <span data-ttu-id="38bd1-138">Með þessum einingum á sínum stað, getur notandi stofna Uppskrift og úthluta afbrigðisflokka á allar viðeigandi uppskriftalínur.</span><span class="sxs-lookup"><span data-stu-id="38bd1-138">With these building blocks in place, the user can create the BOM and assign configuration groups to all relevant BOM lines.</span></span> <span data-ttu-id="38bd1-139">Þegar Uppskrift er lokið er hægt að skilgreina afbrigðisleið skilgreinda fyrir röðun á afbrigðisflokkum í viðeigandi númeraröð.</span><span class="sxs-lookup"><span data-stu-id="38bd1-139">When the BOM is complete, a configuration route can be defined for ordering the configuration groups in the proper sequence.</span></span> <span data-ttu-id="38bd1-140">[![Víddarmiðað vörulíkanaferli](./media/dimension-based-product-modeling-process-v1.png)](./media/dimension-based-product-modeling-process-v1.png) Ef það er vitað um afurðir úr mismunandi afbrigðisflokkum sem annað hvort verður eða má ekki nota saman, er hægt að stofna afbrigðareglur sem munu framfylgja þessum afurðavenslum.</span><span class="sxs-lookup"><span data-stu-id="38bd1-140">[![Dimension-based product modeling process](./media/dimension-based-product-modeling-process-v1.png)](./media/dimension-based-product-modeling-process-v1.png) If there are certain products from different configuration groups that either must or must not be used together, you can create configuration rules that will enforce these product relationships.</span></span> <span data-ttu-id="38bd1-141">Eftir að uppskrift hefur verið tengd við afurðarsniðmát sem byggist á víddum í gegnum uppskriftarútgáfu og bæði hafa verið samþykktar og virkjaðar, er hægt að stofna afurðarafbrigði og færa inn heiti fyrir hvert afbrigði.</span><span class="sxs-lookup"><span data-stu-id="38bd1-141">After the BOM has been tied together with a dimension-based product master through a BOM version and both have been approved and activated, you can create product configurations and enter a name for each configuration.</span></span> <span data-ttu-id="38bd1-142">Hægt er að skilgreina afbrigði áður en neinar færslur eru mynduðar eða það er gert þegar þörf fyrir ákveðið afbrigði á sér stað.</span><span class="sxs-lookup"><span data-stu-id="38bd1-142">The configurations can be defined before any transactions are generated or it can be done when the need for a certain configuration occurs.</span></span>

### <a name="suggested-use"></a><span data-ttu-id="38bd1-143">Notkun sem mælt er með</span><span class="sxs-lookup"><span data-stu-id="38bd1-143">Suggested use</span></span>

<span data-ttu-id="38bd1-144">Afbrigðistækni sem byggist á víddum hentar best fyrir vörur með takmörkuðum breytileika og samsetningu staðlaðra stærða afurðarvídda, lit, stíl, og afbrigði hentar ekki til að auðkenna tiltekinn afurðarafbrigði.</span><span class="sxs-lookup"><span data-stu-id="38bd1-144">The dimension-based configuration technology is best used for products with limited variability and the combination of the standard product dimensions size, color, style, and configuration is unsuitable for identifying a specific product variant.</span></span> <span data-ttu-id="38bd1-145">Dæmi gæti verið reiðhjól með stellhæð, hjólastærð, og mismunandi gíra.</span><span class="sxs-lookup"><span data-stu-id="38bd1-145">An example could be bicycle with frame height, wheel size, brake types, and different gears.</span></span>

### <a name="next-step"></a><span data-ttu-id="38bd1-146">Næsta skref</span><span class="sxs-lookup"><span data-stu-id="38bd1-146">Next step</span></span> 

<span data-ttu-id="38bd1-147">Eftirfarandi átta verkefnaleiðbeiningar eru taldar upp í þeirri röð sem ætti að ljúka þeim.</span><span class="sxs-lookup"><span data-stu-id="38bd1-147">The following eight task guides are listed in the order in which you should complete them.</span></span> 

1.  [<span data-ttu-id="38bd1-148">Búa til afurðarsniðmát sem byggir á víddum (verkleiðbeiningar)</span><span class="sxs-lookup"><span data-stu-id="38bd1-148">Create a dimension-based product master (Task guide)</span></span>](tasks/create-dimension-based-product-master.md)
2.  [<span data-ttu-id="38bd1-149">Losa afurðarsniðmát sem byggir á víddum (verkleiðbeiningar)</span><span class="sxs-lookup"><span data-stu-id="38bd1-149">Release a dimension-based product master (Task guide)</span></span>](tasks/release-dimension-based-product-master.md)
3.  [<span data-ttu-id="38bd1-150">Ljúka grunnuppsetningu útgefins afurðarsniðmáts (verkleiðbeiningar)</span><span class="sxs-lookup"><span data-stu-id="38bd1-150">Complete basic setup of a released product master (Task guide)</span></span>](tasks/complete-basic-setup-released-product-master.md)
4.  [<span data-ttu-id="38bd1-151">Skilgreina skilgreiningarflokka (verkleiðbeiningar)</span><span class="sxs-lookup"><span data-stu-id="38bd1-151">Define configuration groups (Task guide)</span></span>](tasks/define-configuration-groups.md)
5.  [<span data-ttu-id="38bd1-152">Stofnun farmbréf fyrir afurðarsniðmát byggt á víddum (verkleiðbeiningar)</span><span class="sxs-lookup"><span data-stu-id="38bd1-152">Create a bill of materials for a dimension-based product master (Task guide)</span></span>](tasks/create-bill-materials-dimension-based-product-master.md)
6.  [<span data-ttu-id="38bd1-153">Skilgreina skilgreiningarleiðir (verkleiðbeiningar)</span><span class="sxs-lookup"><span data-stu-id="38bd1-153">Define configuration routes (Task guide)</span></span>](tasks/define-configuration-route.md)
7.  [<span data-ttu-id="38bd1-154">Stofna skilgreiningarreglur (verkleiðbeiningar)</span><span class="sxs-lookup"><span data-stu-id="38bd1-154">Create configuration rules (Task guide)</span></span>](tasks/create-configuration-rules.md)
8.  [<span data-ttu-id="38bd1-155">Stofna skilgreiningar sem byggja á víddum (verkleiðbeiningar)</span><span class="sxs-lookup"><span data-stu-id="38bd1-155">Create dimension-based configurations (Task guide)</span></span>](tasks/create-dimension-based-configurations.md)


