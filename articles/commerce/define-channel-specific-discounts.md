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
ms.custom: 16401
ms.assetid: d807fd51-86aa-47a0-8e00-6c5ddd21ff6b
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 990c0d0b4b89420094dc86552b3e07717e5c7056
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4991391"
---
# <a name="define-channel-specific-discounts"></a><span data-ttu-id="7400f-104">Skilgreining afslátta fyrir tiltekna rás</span><span class="sxs-lookup"><span data-stu-id="7400f-104">Define channel-specific discounts</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7400f-105">Í þessu efnisatriði eru skoðuð hugtök sem nauðsynlegt er að þekkja til að stofna afslátt fyrir tiltekna rás.</span><span class="sxs-lookup"><span data-stu-id="7400f-105">This topic reviews the concepts you need to know to create a discount for a specific channel.</span></span>

## <a name="channel-specific-discounts"></a><span data-ttu-id="7400f-106">Afslættir sem tengjast tilteknum rásum</span><span class="sxs-lookup"><span data-stu-id="7400f-106">Channel-specific discounts</span></span>

<span data-ttu-id="7400f-107">Smásalar bjóða oft mismunandi afslætti á mismunandi rásum.</span><span class="sxs-lookup"><span data-stu-id="7400f-107">Retailers often offer different discounts in different channels.</span></span> <span data-ttu-id="7400f-108">Þetta getur verið gert til að ná til staðbundinna markaðsaðstæðna eða takast á við smásala í samkeppni.</span><span class="sxs-lookup"><span data-stu-id="7400f-108">This may be done to address local market conditions or to deal with competing retailers.</span></span>

<span data-ttu-id="7400f-109">Commerce notar verðflokka til að skilgreina rásarafslætti fyrir smásölu og viðskipti.</span><span class="sxs-lookup"><span data-stu-id="7400f-109">Commerce uses price groups to define channel-specific discounts.</span></span> <span data-ttu-id="7400f-110">Hægt er að úthluta verðflokkum við eitt eða fleiri af eftirfarandi einingar: rásir vörulista, tengsl og vildarkerfi.</span><span class="sxs-lookup"><span data-stu-id="7400f-110">Price groups can be assigned to one or more of the following entities: channels, catalogs, affiliations, and loyalty programs.</span></span> <span data-ttu-id="7400f-111">Þessi skrá fjallað um rásir, en sömu hugtök eiga við vörulistaafslætti, tengslaafslætti og vildarkortaafslætti.</span><span class="sxs-lookup"><span data-stu-id="7400f-111">This article discusses channels, but the same concepts apply to catalog discounts, affiliations discounts, and loyalty discounts.</span></span>

## <a name="price-groups"></a><span data-ttu-id="7400f-112">Verðflokkar</span><span class="sxs-lookup"><span data-stu-id="7400f-112">Price groups</span></span>

<span data-ttu-id="7400f-113">[![Verðflokkar](./media/price-groups-1024x608.png)](./media/price-groups.png)</span><span class="sxs-lookup"><span data-stu-id="7400f-113">[![Price groups](./media/price-groups-1024x608.png)](./media/price-groups.png)</span></span>

<span data-ttu-id="7400f-114">Skýringarmyndin að ofan sýnir tengslin á milli aðila sem geta verið á færslum (rásar, vörulista, sambands, viðskiptavinur, vildarkort) og mismunandi afsláttargerðir sem má stilla.</span><span class="sxs-lookup"><span data-stu-id="7400f-114">The diagram above illustrates the relationship between entities that may be on a transaction (channel, catalog, affiliation, customer, loyalty card) and the various discount types that can be configured.</span></span> <span data-ttu-id="7400f-115">Allar færslur eiga sér stað í rás, svo tryggt er að rás verði til staðar á færslu.</span><span class="sxs-lookup"><span data-stu-id="7400f-115">All transactions occur in a channel, so the channel is guaranteed to be present on a transaction.</span></span> <span data-ttu-id="7400f-116">Eftirstandandi einingar eru valkvæðar.</span><span class="sxs-lookup"><span data-stu-id="7400f-116">The remaining entities are optional.</span></span> <span data-ttu-id="7400f-117">Á öllum síðum aðalgagna er tengill við tengdar verðflokkasíðu þar sem hægt er að skoða og bæta við verðflokkar eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="7400f-117">On each master data pages there is a link to a related price groups page where you can view and add price groups as needed.</span></span> <span data-ttu-id="7400f-118">Verðflokkur er notuð til að tengjast fjórar tegundir eininga við afslætti, verðleiðréttingar og viðskiptasamninga.</span><span class="sxs-lookup"><span data-stu-id="7400f-118">A price group is used to relate four different types of entities to discounts, price adjustments, and trade agreements.</span></span> <span data-ttu-id="7400f-119">Ráðlagt er að undirbúa aðferð um það hvernig þú nefnir verðflokkana þína til að hafa þá skipulagða.</span><span class="sxs-lookup"><span data-stu-id="7400f-119">We recommend that you plan a strategy for how you will name your price groups to keep them organized.</span></span> <span data-ttu-id="7400f-120">Einn valkostur væri að nota bókstaf eða númersforskeyti eða viðskeyti til að greina milli mismunandi gerðum.</span><span class="sxs-lookup"><span data-stu-id="7400f-120">One option would be to use a letter or number prefix or suffix to distinguish between the different types.</span></span> <span data-ttu-id="7400f-121">Til dæmis 1-xxxxx fyrir verðflokka rásar og 2-xxxxx fyrir verðflokka vörulista.</span><span class="sxs-lookup"><span data-stu-id="7400f-121">For example, 1-xxxxx for channel price groups and 2-xxxxx for catalog price groups.</span></span> <span data-ttu-id="7400f-122">Til eru fjórar fyrirspurnarsíður sem áherslu leggja á hverja netverslunareiningu sem geta verið með afslætti tengda við sig.</span><span class="sxs-lookup"><span data-stu-id="7400f-122">There are four inquiry pages that focus on each of the commerce entities that can have discounts associated to them.</span></span>

- <span data-ttu-id="7400f-123">**Verðflokkar rásar** – Þessi síða sýnir lista yfir rásir og afslætti sem eru tengdar saman fyrir hvern verðflokk.</span><span class="sxs-lookup"><span data-stu-id="7400f-123">**Channel channel price groups** – This page shows a list of channels and discounts linked together for each price group.</span></span>
- <span data-ttu-id="7400f-124">**Verðflokkar vörulista** – Þessi síða sýnir lista yfir vörulista og afslætti sem eru tengdar saman fyrir hvern verðflokk.</span><span class="sxs-lookup"><span data-stu-id="7400f-124">**Catalog price groups** – This page shows a list of catalogs and discounts linked together for each price group.</span></span>
- <span data-ttu-id="7400f-125">**Verðflokkar vildarkerfis** – Þessi síða sýnir lista yfir vildarkerfi og afslætti sem eru tengdar saman fyrir hvern verðflokk.</span><span class="sxs-lookup"><span data-stu-id="7400f-125">**Loyalty price groups** – This page shows a list of loyalty programs and discounts linked together for each price group.</span></span>
- <span data-ttu-id="7400f-126">**Verðflokkar tengsla** – Þessi síða sýnir lista yfir tengsl og afslætti sem eru tengdar saman fyrir hvern verðflokk.</span><span class="sxs-lookup"><span data-stu-id="7400f-126">**Affiliation price groups** – This page shows a list of affiliations and discounts linked together for each price group.</span></span>

## <a name="example-channel-discount-set-up"></a><span data-ttu-id="7400f-127">Uppsetning afsláttar fyrir dæmarás</span><span class="sxs-lookup"><span data-stu-id="7400f-127">Example channel discount set up</span></span>

<span data-ttu-id="7400f-128">Eftirfarandi dæmi sýnir verkefnunum sem felast í að setja upp afslátt rásar.</span><span class="sxs-lookup"><span data-stu-id="7400f-128">The following example illustrates the tasks involved in setting up a channel discount.</span></span>

1. <span data-ttu-id="7400f-129">Í þessu dæmi ertu með rás sem kallast **Houston**, og það er verið að stofna nýjan afslátt kallaðan **Aftur í skólann**.</span><span class="sxs-lookup"><span data-stu-id="7400f-129">For this example, you have a channel called **Houston**, and you're going to create a new discount called **Back-to-School**.</span></span>
2. <span data-ttu-id="7400f-130">Þar sem stjórnunarstefna verðs og afsláttar inniheldur möguleika á afslætti fyrir rás, er alltaf stofnaður verðflokk bundnum við rás þegar rás er stofnuð.</span><span class="sxs-lookup"><span data-stu-id="7400f-130">Because the pricing and discount strategy includes the possibility of channel discounts, you always create a channel-specific price group when you create a channel.</span></span>
3. <span data-ttu-id="7400f-131">Verðflokkurinn er **Houston-PG** og er úthlutað á **Houston** rás.</span><span class="sxs-lookup"><span data-stu-id="7400f-131">You have the price group **Houston-PG** and it is assigned to the **Houston** channel.</span></span>
4. <span data-ttu-id="7400f-132">Eftir að Búið er að stofna nýja **aftur í skólann** afsláttur, þarf að smella á **Verðflokkar** efst í **Afsláttur** síðu.</span><span class="sxs-lookup"><span data-stu-id="7400f-132">After you create the new **Back-to-School** discount, you need to click **Price groups** on the top of the **Discount** page.</span></span> <span data-ttu-id="7400f-133">**Afsláttarverðflokka** síðan opnast.</span><span class="sxs-lookup"><span data-stu-id="7400f-133">The **Discount price groups** page will open.</span></span> <span data-ttu-id="7400f-134">Smellið því næst á **Nýtt** og velja **Houston -PG** verðflokk.</span><span class="sxs-lookup"><span data-stu-id="7400f-134">Next, click **New** and select the **Houston-PG** price group.</span></span>
5. <span data-ttu-id="7400f-135">Nú hægt að virkja afsláttinn og færa hann í rás.</span><span class="sxs-lookup"><span data-stu-id="7400f-135">Now you can enable the discount and push it to the channel.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7400f-136">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="7400f-136">Additional resources</span></span>

[<span data-ttu-id="7400f-137">Verðleiðréttingar og afslættir</span><span class="sxs-lookup"><span data-stu-id="7400f-137">Price adjustments and discounts</span></span>](price-adjustments-discounts.md)
