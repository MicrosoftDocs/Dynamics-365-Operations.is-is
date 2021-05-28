---
title: Uppsetning sendingarupplýsinga
description: Þetta efnisatriði lýsir því hvernig eigi að setja upp sendingarupplýsingar fyrir Heildarkostnaður eininguna.
author: sherry-zheng
ms.date: 12/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMGoodsDescriptionTable, ITMVesselTable, ITMExporterTable, ITMCommodityCodeTable, ITMCustomsDescription
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-04
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 5093e42b0b5247c24c271ad50c80889516586d58
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020888"
---
# <a name="shipping-information-setup"></a><span data-ttu-id="78338-103">Uppsetning sendingarupplýsinga</span><span class="sxs-lookup"><span data-stu-id="78338-103">Shipping information setup</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="78338-104">Þetta efnisatriði lýsir því hvernig eigi að setja upp sendingarupplýsingar **Heildarkostnaður** eininguna.</span><span class="sxs-lookup"><span data-stu-id="78338-104">This topic describes how to set up shipping information for the **Landed cost** module.</span></span>

## <a name="description-of-goods"></a><a name="description-of-goods"></a><span data-ttu-id="78338-105">Lýsing á vörum</span><span class="sxs-lookup"><span data-stu-id="78338-105">Description of goods</span></span>

<span data-ttu-id="78338-106">Vörulýsing hjálpar til við að auðkenna ferð, gám eða fólíó og vörurnar í þeim.</span><span class="sxs-lookup"><span data-stu-id="78338-106">Descriptions of goods help identify a voyage, shipping container, or folio of goods, and the goods in it.</span></span> <span data-ttu-id="78338-107">Hægt er að velja lýsingu á vörum í haus gámsins eða fólíósins.</span><span class="sxs-lookup"><span data-stu-id="78338-107">You can select a description of goods on the shipping container header or the folio header.</span></span>

<span data-ttu-id="78338-108">Til að vinna með lýsingar á vörum skal fara í **Heildarkostnaður \> Uppsetning sendingarupplýsinga \> Lýsing á vörum**.</span><span class="sxs-lookup"><span data-stu-id="78338-108">To work with descriptions of goods, go to **Landed cost \> Shipping information setup \> Description of goods**.</span></span> <span data-ttu-id="78338-109">Þar er hægt að skoða, opna, stofna og eyða færslum fyrir lýsingar á vörum.</span><span class="sxs-lookup"><span data-stu-id="78338-109">There, you can view, open, create, and delete records for descriptions of goods.</span></span> <span data-ttu-id="78338-110">Eftirfarandi tafla lýsir eritinum sem eru tiltækir fyrir hverja færslu.</span><span class="sxs-lookup"><span data-stu-id="78338-110">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="78338-111">Svæði</span><span class="sxs-lookup"><span data-stu-id="78338-111">Field</span></span> | <span data-ttu-id="78338-112">lýsing</span><span class="sxs-lookup"><span data-stu-id="78338-112">Description</span></span> |
|---|---|
| <span data-ttu-id="78338-113">Lýsing á vörum</span><span class="sxs-lookup"><span data-stu-id="78338-113">Description of goods</span></span> | <span data-ttu-id="78338-114">Færið inn einkvæmt auðkennisheiti/númer fyrir gerð varanna sem notar þessa lýsingu.</span><span class="sxs-lookup"><span data-stu-id="78338-114">Enter a unique identification name/number for the type of goods that will use this description.</span></span> |
| <span data-ttu-id="78338-115">lýsing</span><span class="sxs-lookup"><span data-stu-id="78338-115">Description</span></span> | <span data-ttu-id="78338-116">Færið inn lýsingu á gerð varanna í þessum flokki.</span><span class="sxs-lookup"><span data-stu-id="78338-116">Enter a description of the type of goods in this category.</span></span> |

## <a name="vessels"></a><a name="vessels"></a><span data-ttu-id="78338-117">Skip</span><span class="sxs-lookup"><span data-stu-id="78338-117">Vessels</span></span>

<span data-ttu-id="78338-118">Skip er einkvæmt heiti á skipi sem flutningsfyrirtæki eða umboðsaðili notar.</span><span class="sxs-lookup"><span data-stu-id="78338-118">A vessel is the unique name of a ship or vessel that a shipping company or agency uses.</span></span> <span data-ttu-id="78338-119">Þegar ferð er stofnuð þarf alltaf að annaðhvort velja eða færa inn skip hennar.</span><span class="sxs-lookup"><span data-stu-id="78338-119">When you create a voyage, you must always either select or enter a vessel for it.</span></span> <span data-ttu-id="78338-120">Ef sama skipið er oft notað er hægt að flýta fyrir og auðvelda stofnun nýrrar ferðar með því að stofna færslu skips fyrir hverja þeirra og gera notendum þar með kleift að velja skipið úr lista frekar en að færa inn heiti eða númer handvirkt í hvert skipti.</span><span class="sxs-lookup"><span data-stu-id="78338-120">If you often use the same vessels, then you can make it faster and easier to create a new voyage by creating a vessel record for each of them, thereby allowing users to select the vessel from a list rather then enter the name or number manually each time.</span></span>

<span data-ttu-id="78338-121">Til að vinna með skip skal fara í **Heildarkostnaður \> Uppsetning sendingarupplýsinga \> Skip**.</span><span class="sxs-lookup"><span data-stu-id="78338-121">To work with vessels, go to **Landed cost \> Shipping information setup \> Vessels**.</span></span> <span data-ttu-id="78338-122">Þar er hægt að skoða, opna, stofna og eyða færslum fyrir skip.</span><span class="sxs-lookup"><span data-stu-id="78338-122">There, you can view, open, create, and delete records for vessels.</span></span> <span data-ttu-id="78338-123">Eftirfarandi tafla lýsir eritinum sem eru tiltækir fyrir hverja færslu.</span><span class="sxs-lookup"><span data-stu-id="78338-123">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="78338-124">Svæði</span><span class="sxs-lookup"><span data-stu-id="78338-124">Field</span></span> | <span data-ttu-id="78338-125">lýsing</span><span class="sxs-lookup"><span data-stu-id="78338-125">Description</span></span> |
|---|---|
| <span data-ttu-id="78338-126">Skip</span><span class="sxs-lookup"><span data-stu-id="78338-126">Vessel</span></span> | <span data-ttu-id="78338-127">Færið inn einkvæmt auðkennisheiti/númer fyrir skipið sem verður notað til að flytja vörur í ferð.</span><span class="sxs-lookup"><span data-stu-id="78338-127">Enter a unique identification name/number for the ship that will be used to transport goods on a voyage.</span></span> |
| <span data-ttu-id="78338-128">lýsing</span><span class="sxs-lookup"><span data-stu-id="78338-128">Description</span></span> | <span data-ttu-id="78338-129">Færðu inn lýsingu á skipinu.</span><span class="sxs-lookup"><span data-stu-id="78338-129">Enter a description of the vessel.</span></span> <span data-ttu-id="78338-130">Yfirleitt kemur fram í þessari lýsingu heiti skipsins og flutningsfyrirtækisins/umboðsaðilans.</span><span class="sxs-lookup"><span data-stu-id="78338-130">Typically, this description identifies the name of the ship and the shipping company/agent.</span></span> |
| <span data-ttu-id="78338-131">Afhendingarmáti</span><span class="sxs-lookup"><span data-stu-id="78338-131">Mode of delivery</span></span> | <span data-ttu-id="78338-132">Veljið afhendingarmáta sem skipið notar (t.d. _Flug_, _Haf_ eða _Lest_).</span><span class="sxs-lookup"><span data-stu-id="78338-132">Select the mode of delivery that the vessel uses (such as _Air_, _Ocean_, or _Train_).</span></span> |

## <a name="exporters"></a><span data-ttu-id="78338-133">Útflutningsaðilar</span><span class="sxs-lookup"><span data-stu-id="78338-133">Exporters</span></span>

<span data-ttu-id="78338-134">Hver færsla útflutningsaðila tilgreinir lánardrottin eða útflutningsaðila sem hægt er að skilgreina sem lánardrottin ferðar.</span><span class="sxs-lookup"><span data-stu-id="78338-134">Each exporter record identifies a vendor or exporter that can be defined as the vendor for a voyage.</span></span> <span data-ttu-id="78338-135">Hægt er að tengja útflutningsaðilann við ferð og nota hann í skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="78338-135">The exporter can be associated with a voyage and used for reporting.</span></span>

<span data-ttu-id="78338-136">Til að vinna með útflutningsaðila skal fara í **Heildarkostnaður \> Uppsetning sendingarupplýsinga \> Útflutningsaðilar**.</span><span class="sxs-lookup"><span data-stu-id="78338-136">To work with exporters, go to **Landed cost \> Shipping information setup \> Exporters**.</span></span> <span data-ttu-id="78338-137">Þar er hægt að skoða, opna, stofna og eyða færslum fyrir útflutningsaðila.</span><span class="sxs-lookup"><span data-stu-id="78338-137">There, you can view, open, create, and delete records for exporters.</span></span> <span data-ttu-id="78338-138">Eftirfarandi tafla lýsir eritinum sem eru tiltækir fyrir hverja færslu.</span><span class="sxs-lookup"><span data-stu-id="78338-138">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="78338-139">Svæði</span><span class="sxs-lookup"><span data-stu-id="78338-139">Field</span></span> | <span data-ttu-id="78338-140">lýsing</span><span class="sxs-lookup"><span data-stu-id="78338-140">Description</span></span> |
|---|---|
| <span data-ttu-id="78338-141">Útflutningsaðili</span><span class="sxs-lookup"><span data-stu-id="78338-141">Exporter</span></span> | <span data-ttu-id="78338-142">Færið inn einkvæmt auðkennisheiti/númer fyrir útflutningsaðila á vörum sem eru fluttar í ferð.</span><span class="sxs-lookup"><span data-stu-id="78338-142">Enter a unique identification name/number for the exporter of goods that are transported on a voyage.</span></span> |
| <span data-ttu-id="78338-143">lýsing</span><span class="sxs-lookup"><span data-stu-id="78338-143">Description</span></span> | <span data-ttu-id="78338-144">Færðu inn lýsingu á útflytjanda.</span><span class="sxs-lookup"><span data-stu-id="78338-144">Enter a description of the exporter.</span></span> <span data-ttu-id="78338-145">Yfirleitt auðkennir þessi lýsing fullt heiti flutningsfyrirtækisins/-aðilans.</span><span class="sxs-lookup"><span data-stu-id="78338-145">Typically, this description identifies the full name of the shipping company/agent.</span></span> |

## <a name="commodity-codes"></a><span data-ttu-id="78338-146">Grunnvörukóðar</span><span class="sxs-lookup"><span data-stu-id="78338-146">Commodity codes</span></span>

<span data-ttu-id="78338-147">Vörukóðar eru notaðir til að aðstoða við auðkenningu tolla og útreikning innflutningsgjalda fyrir vörur í ferð.</span><span class="sxs-lookup"><span data-stu-id="78338-147">You use commodity codes to help with customs identification and the calculation of duty rates for goods on a voyage.</span></span> <span data-ttu-id="78338-148">Hægt er að velja vörukóða á Síða **Útgefinna afurða**.</span><span class="sxs-lookup"><span data-stu-id="78338-148">You can select commodity codes on the **Released products** page.</span></span>

<span data-ttu-id="78338-149">Til að vinna með vörukóða skal opna **Heildarkostnaður \> Uppsetning sendingarupplýsinga \> Vörukóðar**.</span><span class="sxs-lookup"><span data-stu-id="78338-149">To work with commodity codes, go to **Landed cost \> Shipping information setup \> Commodity codes**.</span></span> <span data-ttu-id="78338-150">Þar er hægt að skoða, opna, stofna og eyða færslum fyrir vörukóða.</span><span class="sxs-lookup"><span data-stu-id="78338-150">There, you can view, open, create, and delete records for commodity codes.</span></span> <span data-ttu-id="78338-151">Eftirfarandi tafla lýsir eritinum sem eru tiltækir fyrir hverja færslu.</span><span class="sxs-lookup"><span data-stu-id="78338-151">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="78338-152">Svæði</span><span class="sxs-lookup"><span data-stu-id="78338-152">Field</span></span> | <span data-ttu-id="78338-153">lýsing</span><span class="sxs-lookup"><span data-stu-id="78338-153">Description</span></span> |
|---|---|
| <span data-ttu-id="78338-154">Grunnvörukóði</span><span class="sxs-lookup"><span data-stu-id="78338-154">Commodity code</span></span> | <span data-ttu-id="78338-155">Færið inn einkvæman kóða fyrir þessa gerð vöru.</span><span class="sxs-lookup"><span data-stu-id="78338-155">Enter a unique code for this type of commodity.</span></span> |
| <span data-ttu-id="78338-156">lýsing</span><span class="sxs-lookup"><span data-stu-id="78338-156">Description</span></span> | <span data-ttu-id="78338-157">Færið inn lýsingu á vörutegundinni.</span><span class="sxs-lookup"><span data-stu-id="78338-157">Enter a description of the commodity type.</span></span> |

## <a name="customs-description"></a><span data-ttu-id="78338-158">Lýsing tolls</span><span class="sxs-lookup"><span data-stu-id="78338-158">Customs description</span></span>

<span data-ttu-id="78338-159">Lýsing á tolli auðveldar að auðkenna vörur vegna tolla.</span><span class="sxs-lookup"><span data-stu-id="78338-159">Customs descriptions help identify goods for customs purposes.</span></span> <span data-ttu-id="78338-160">Hægt er að velja tollalýsingu á síðunni **útgefnar afurðir** eða í innkaupapöntunarlínum.</span><span class="sxs-lookup"><span data-stu-id="78338-160">You can select a customs description on the **Released products** page or on purchase order lines.</span></span>

<span data-ttu-id="78338-161">Til að vinna með tolllýsingar skal fara í **Heildarkostnaður \> Uppsetning sendingarupplýsinga \> Lýsing tolls**.</span><span class="sxs-lookup"><span data-stu-id="78338-161">To work with customs descriptions, go to **Landed cost \> Shipping information setup \> Customs description**.</span></span> <span data-ttu-id="78338-162">Þar er hægt að skoða, opna, stofna og eyða færslum fyrir sérstakar lýsingar.</span><span class="sxs-lookup"><span data-stu-id="78338-162">There, you can view, open, create, and delete records for custom descriptions.</span></span> <span data-ttu-id="78338-163">Eftirfarandi tafla lýsir eritinum sem eru tiltækir fyrir hverja færslu.</span><span class="sxs-lookup"><span data-stu-id="78338-163">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="78338-164">Svæði</span><span class="sxs-lookup"><span data-stu-id="78338-164">Field</span></span> | <span data-ttu-id="78338-165">lýsing</span><span class="sxs-lookup"><span data-stu-id="78338-165">Description</span></span> |
|---|---|
| <span data-ttu-id="78338-166">Lýsing tolls</span><span class="sxs-lookup"><span data-stu-id="78338-166">Customs description</span></span> | <span data-ttu-id="78338-167">Færið inn einkvæman kóða fyrir þessa gerð tollflokkunar.</span><span class="sxs-lookup"><span data-stu-id="78338-167">Enter a unique code for this type of customs classification.</span></span> <span data-ttu-id="78338-168">Oft verður þessi kóði opinber lýsing sem er gefin út af tollayfirvöldum fyrir lýsingu og eigindleg gildi varanna.</span><span class="sxs-lookup"><span data-stu-id="78338-168">Often, this code will be the official description that is provided by a customs authority for the description and qualitative value of the goods.</span></span> |
| <span data-ttu-id="78338-169">lýsing</span><span class="sxs-lookup"><span data-stu-id="78338-169">Description</span></span> | <span data-ttu-id="78338-170">Færið inn lýsingu á tollaflokkun.</span><span class="sxs-lookup"><span data-stu-id="78338-170">Enter a description of the customs classification.</span></span> |
