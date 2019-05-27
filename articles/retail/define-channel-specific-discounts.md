---
title: Skilgreina afslætti sem tengjast tilteknum rásum
description: Smásala stilla oft inn mismunandi afslætti á mismunandi rásum. Í þessu efnisatriði eru skoðuð hugtök sem nauðsynlegt er að þekkja til að stofna afslátt fyrir tiltekna rás.
author: scott-tucker
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailAffiliationPriceGroup, RetailCatalogPriceGroup, RetailChannelPriceGroup, RetailDiscountPriceGroup, RetailDiscountPricingWorkspace, RetailPeriodicDiscount, RetailStoreItemPriceList, RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16401
ms.assetid: d807fd51-86aa-47a0-8e00-6c5ddd21ff6b
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: a136e245beaf8dfd8bcf19d49f8a355c8871cde7
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1568069"
---
# <a name="define-channel-specific-discounts"></a><span data-ttu-id="02db3-104">Skilgreina afslætti sem tengjast tilteknum rásum</span><span class="sxs-lookup"><span data-stu-id="02db3-104">Define channel-specific discounts</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="02db3-105">Smásala stilla oft inn mismunandi afslætti á mismunandi rásum.</span><span class="sxs-lookup"><span data-stu-id="02db3-105">Retailers often set different discounts in different channels.</span></span> <span data-ttu-id="02db3-106">Í þessu efnisatriði eru skoðuð hugtök sem nauðsynlegt er að þekkja til að stofna afslátt fyrir tiltekna rás.</span><span class="sxs-lookup"><span data-stu-id="02db3-106">This topic reviews the concepts you need to know to create a discount for a specific channel.</span></span>

## <a name="channel-specific-discounts"></a><span data-ttu-id="02db3-107">Afslættir sem tengjast tilteknum rásum</span><span class="sxs-lookup"><span data-stu-id="02db3-107">Channel-specific discounts</span></span>

<span data-ttu-id="02db3-108">Smásalar bjóða oft mismunandi afslætti á mismunandi rásum.</span><span class="sxs-lookup"><span data-stu-id="02db3-108">Retailers often offer different discounts in different channels.</span></span> <span data-ttu-id="02db3-109">Þetta er getur verið gert til að ná til staðbundinna markaðsaðstæðna eða takast á við smásala í samkeppni.</span><span class="sxs-lookup"><span data-stu-id="02db3-109">This is may be done to address local market conditions or to deal with competing retailers.</span></span>

<span data-ttu-id="02db3-110">Microsoft Dynamics 365 for Retail notar verðflokka til að skilgreina rásarafslætti fyrir smásölu og viðskipti.</span><span class="sxs-lookup"><span data-stu-id="02db3-110">Microsoft Dynamics 365 for Retail uses price groups to define channel-specific discounts.</span></span> <span data-ttu-id="02db3-111">Hægt er að úthluta verðflokkum við eitt eða fleiri af eftirfarandi einingar: rásir vörulista, tengsl og vildarkerfi.</span><span class="sxs-lookup"><span data-stu-id="02db3-111">Price groups can be assigned to one or more of the following entities: channels, catalogs, affiliations, and loyalty programs.</span></span> <span data-ttu-id="02db3-112">Þessi skrá fjallað um rásir, en sömu hugtök eiga við vörulistaafslætti, tengslaafslætti og vildarkortaafslætti.</span><span class="sxs-lookup"><span data-stu-id="02db3-112">This article discusses channels, but the same concepts apply to catalog discounts, affiliations discounts, and loyalty discounts.</span></span>

## <a name="price-groups"></a><span data-ttu-id="02db3-113">Verðflokkar</span><span class="sxs-lookup"><span data-stu-id="02db3-113">Price groups</span></span>

<span data-ttu-id="02db3-114">[![Verðflokkar](./media/price-groups-1024x608.png)](./media/price-groups.png)</span><span class="sxs-lookup"><span data-stu-id="02db3-114">[![Price groups](./media/price-groups-1024x608.png)](./media/price-groups.png)</span></span>

<span data-ttu-id="02db3-115">Skýringarmyndin að ofan sýnir tengslin á milli aðila sem geta verið á færslum (rásar, vörulista, sambands, viðskiptavinur, vildarkort) og mismunandi afsláttargerðir sem má stilla.</span><span class="sxs-lookup"><span data-stu-id="02db3-115">The diagram above illustrates the relationship between entities that may be on a transaction (channel, catalog, affiliation, customer, loyalty card) and the various discount types that can be configured.</span></span> <span data-ttu-id="02db3-116">Allar færslur eiga sér stað í rás, svo tryggt er að rás verði til staðar á færslu.</span><span class="sxs-lookup"><span data-stu-id="02db3-116">All transactions occur in a channel, so the channel is guaranteed to be present on a transaction.</span></span> <span data-ttu-id="02db3-117">Eftirstandandi einingar eru valkvæðar.</span><span class="sxs-lookup"><span data-stu-id="02db3-117">The remaining entities are optional.</span></span> <span data-ttu-id="02db3-118">Á öllum síðum aðalgagna er tengill við tengdar verðflokkasíðu þar sem hægt er að skoða og bæta við verðflokkar eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="02db3-118">On each master data pages there is a link to a related price groups page where you can view and add price groups as needed.</span></span> <span data-ttu-id="02db3-119">Verðflokkur er notuð til að tengjast fjórar tegundir eininga við afslætti, verðleiðréttingar og viðskiptasamninga.</span><span class="sxs-lookup"><span data-stu-id="02db3-119">A price group is used to relate four different types of entities to discounts, price adjustments, and trade agreements.</span></span> <span data-ttu-id="02db3-120">Ráðlagt er að undirbúa aðferð um það hvernig þú nefnir verðflokkana þína til að hafa þá skipulagða.</span><span class="sxs-lookup"><span data-stu-id="02db3-120">We recommend that you plan a strategy for how you will name your price groups to keep them organized.</span></span> <span data-ttu-id="02db3-121">Einn valkostur væri að nota bókstaf eða númersforskeyti eða viðskeyti til að greina milli mismunandi gerðum.</span><span class="sxs-lookup"><span data-stu-id="02db3-121">One option would be to use a letter or number prefix or suffix to distinguish between the different types.</span></span> <span data-ttu-id="02db3-122">Til dæmis 1-xxxxx fyrir verðflokka rásar og 2-xxxxx fyrir verðflokka vörulista.</span><span class="sxs-lookup"><span data-stu-id="02db3-122">For example, 1-xxxxx for channel price groups and 2-xxxxx for catalog price groups.</span></span> <span data-ttu-id="02db3-123">Til eru fjórar fyrirspurnarsíður sem áherslu leggja á hverja smásölueiningu sem geta verið með afslætti tengda við sig.</span><span class="sxs-lookup"><span data-stu-id="02db3-123">There are four inquiry pages that focus on each of the retail entities that can have discounts associated to them.</span></span>

- <span data-ttu-id="02db3-124">**Verðflokkar rásar í smásölu** – Þessi síða sýnir lista yfir rásir og afslætti sem eru tengdar saman fyrir hvern verðflokk.</span><span class="sxs-lookup"><span data-stu-id="02db3-124">**Retail channel price groups** – This page shows a list of channels and discounts linked together for each price group.</span></span>
- <span data-ttu-id="02db3-125">**Verðflokkar vörulista** – Þessi síða sýnir lista yfir vörulista og afslætti sem eru tengdar saman fyrir hvern verðflokk.</span><span class="sxs-lookup"><span data-stu-id="02db3-125">**Catalog price groups** – This page shows a list of catalogs and discounts linked together for each price group.</span></span>
- <span data-ttu-id="02db3-126">**Verðflokkar vildarkerfis** – Þessi síða sýnir lista yfir vildarkerfi og afslætti sem eru tengdar saman fyrir hvern verðflokk.</span><span class="sxs-lookup"><span data-stu-id="02db3-126">**Loyalty price groups** – This page shows a list of loyalty programs and discounts linked together for each price group.</span></span>
- <span data-ttu-id="02db3-127">**Verðflokkar tengsla** – Þessi síða sýnir lista yfir tengsl og afslætti sem eru tengdar saman fyrir hvern verðflokk.</span><span class="sxs-lookup"><span data-stu-id="02db3-127">**Affiliation price groups** – This page shows a list of affiliations and discounts linked together for each price group.</span></span>

## <a name="example-channel-discount-set-up"></a><span data-ttu-id="02db3-128">Uppsetning afsláttar fyrir dæmarás</span><span class="sxs-lookup"><span data-stu-id="02db3-128">Example channel discount set up</span></span>

<span data-ttu-id="02db3-129">Eftirfarandi dæmi sýnir verkefnunum sem felast í að setja upp afslátt rásar.</span><span class="sxs-lookup"><span data-stu-id="02db3-129">The following example illustrates the tasks involved in setting up a channel discount.</span></span>

1. <span data-ttu-id="02db3-130">Í þessu dæmi ertu með rás sem kallast **Houston**, og það er verið að stofna nýjan afslátt kallaðan **Aftur í skólann**.</span><span class="sxs-lookup"><span data-stu-id="02db3-130">For this example, you have a channel called **Houston**, and you're going to create a new discount called **Back-to-School**.</span></span>
2. <span data-ttu-id="02db3-131">Þar sem stjórnunarstefna verðs og afsláttar inniheldur möguleika á afslætti fyrir rás, er alltaf stofnaður verðflokk bundnum við rás þegar rás er stofnuð.</span><span class="sxs-lookup"><span data-stu-id="02db3-131">Because the pricing and discount strategy includes the possibility of channel discounts, you always create a channel-specific price group when you create a channel.</span></span>
3. <span data-ttu-id="02db3-132">Verðflokkurinn er **Houston-PG** og er úthlutað á **Houston** rás.</span><span class="sxs-lookup"><span data-stu-id="02db3-132">You have the price group **Houston-PG** and it is assigned to the **Houston** channel.</span></span>
4. <span data-ttu-id="02db3-133">Eftir að Búið er að stofna nýja **aftur í skólann** afsláttur, þarf að smella á **Verðflokkar** efst í **Afsláttur** síðu.</span><span class="sxs-lookup"><span data-stu-id="02db3-133">After you create the new **Back-to-School** discount, you need to click **Price groups** on the top of the **Discount** page.</span></span> <span data-ttu-id="02db3-134">**Afsláttarverðflokka** síðan opnast.</span><span class="sxs-lookup"><span data-stu-id="02db3-134">The **Discount price groups** page will open.</span></span> <span data-ttu-id="02db3-135">Smellið því næst á **Nýtt** og velja **Houston -PG** verðflokk.</span><span class="sxs-lookup"><span data-stu-id="02db3-135">Next, click **New** and select the **Houston-PG** price group.</span></span>
5. <span data-ttu-id="02db3-136">Nú hægt að virkja afsláttinn og færa hann í rás.</span><span class="sxs-lookup"><span data-stu-id="02db3-136">Now you can enable the discount and push it to the channel.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="02db3-137">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="02db3-137">Additional resources</span></span>

[<span data-ttu-id="02db3-138">Verðleiðréttingar og afslættir</span><span class="sxs-lookup"><span data-stu-id="02db3-138">Price adjustments and discounts</span></span>](price-adjustments-discounts.md)
