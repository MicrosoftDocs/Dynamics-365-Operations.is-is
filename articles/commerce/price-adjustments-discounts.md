---
title: Verðleiðréttingar og afslættir
description: Þessi grein gefur upplýsingar um verðleiðréttingar og afslætti í Dynamics 365 Commerce.
author: scott-tucker
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters, RetailPeriodicDiscount
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15891
ms.assetid: bab5adf3-ddf0-4c22-a2eb-b4d25b88de99
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: dfaacfa7681258e3b2273083017c0c398d566651
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022958"
---
# <a name="price-adjustments-and-discounts"></a><span data-ttu-id="97c84-103">Verðleiðréttingar og afslættir</span><span class="sxs-lookup"><span data-stu-id="97c84-103">Price adjustments and discounts</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="97c84-104">Þessi grein gefur upplýsingar um verðleiðréttingar og afslætti í Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="97c84-104">This article provides information about price adjustments and discounts in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="97c84-105">Í Commerce, er hægt að gera verðleiðréttingar afurða og einnig að setja upp afslátt sem er notaður á línu eða færslu á sölustað (POS) í sölupöntun vinnustöðvar símtalalista eða í pöntun á netinu.</span><span class="sxs-lookup"><span data-stu-id="97c84-105">In Commerce, you can make price adjustments to products, and can also set up discounts that are applied to a line item or a transaction at the point of sale (POS), in a call center sales order, or in an online order.</span></span> <span data-ttu-id="97c84-106">Hægt er að tengja verðleiðréttingar og afslátt við sérstaka verðflokka.</span><span class="sxs-lookup"><span data-stu-id="97c84-106">Both price adjustments and discounts can be linked to price groups.</span></span> <span data-ttu-id="97c84-107">Fyrir bæði verðleiðréttingar og afslátt er hægt að tilgreina eina upphafsdagsetningu og lokadag eða endurtekið tímabil, afsláttarkóða og nokkrar aðrar eigindir.</span><span class="sxs-lookup"><span data-stu-id="97c84-107">For both price adjustments and discounts, you can specify a single start date and end date or a reoccurring period, a discount code, and a few additional attributes.</span></span> 

<span data-ttu-id="97c84-108">Hægt er að nota verðleiðréttingar og afslátt á vörur, vöruvíddasamsetningar eða flokka.</span><span class="sxs-lookup"><span data-stu-id="97c84-108">Price adjustments and discounts can be applied to products, variants, or categories.</span></span> <span data-ttu-id="97c84-109">Ef fleiri en einn afslætti er beitt á afurð, gæti viðskiptavinur fengið annaðhvort einn afslátt eða samanlagðan afslátt eftir skilgreiningu á afslættinum.</span><span class="sxs-lookup"><span data-stu-id="97c84-109">If more than one discount applies to a product, a customer might receive either one of the discounts or a combined discount, depending on the configuration of the discount.</span></span> <span data-ttu-id="97c84-110">Commerce beitir afslætti sjálfkrafa eða samsetningu afsláttar sem veitir viðskiptavini besta verð.</span><span class="sxs-lookup"><span data-stu-id="97c84-110">Commerce automatically applies the discount or combination of discounts that gives the best price to the customer.</span></span> <span data-ttu-id="97c84-111">Þegar verðleiðrétting er sett upp eða afsláttur, þarf að tryggja að staðfest sé að verðflokkar séu tengdir við réttar rásir, vörulista, tengsl eða vildarkerfi sem óskað er eftir að afslátturinn gildi á.</span><span class="sxs-lookup"><span data-stu-id="97c84-111">When you set up a price adjustment or a discount, be sure to confirm that price groups are assigned to the correct channels, catalogs, affiliations, or loyalty programs that you want the discount to apply to.</span></span> <span data-ttu-id="97c84-112">Einnig, ef þú vilt mynda afsláttarkenni sjálfkrafa getur þú sett upp númeraraðir á síðunni **Færibreytur Commerce** áður en þú skilgreinir nýjan afslátt eða verðleiðréttingu.</span><span class="sxs-lookup"><span data-stu-id="97c84-112">Additionally, if you want to automatically generate the discount ID, set up number sequences on the **Commerce parameters** page before you define a new price adjustment or discount.</span></span>

> [!NOTE]
> <span data-ttu-id="97c84-113">Ekki er hægt að eyða verðleiðréttingu eða afslætti.</span><span class="sxs-lookup"><span data-stu-id="97c84-113">You can delete a price adjustment or a discount.</span></span> <span data-ttu-id="97c84-114">Hins vegar munu talnagögn glatast.</span><span class="sxs-lookup"><span data-stu-id="97c84-114">However, statistical information will be lost.</span></span>

## <a name="types-of-discounts"></a><span data-ttu-id="97c84-115">Gerðir afsláttar</span><span class="sxs-lookup"><span data-stu-id="97c84-115">Types of discounts</span></span>

<span data-ttu-id="97c84-116">Til eru fjórar gerðir af afslætti:</span><span class="sxs-lookup"><span data-stu-id="97c84-116">There are four types of discounts:</span></span>

- <span data-ttu-id="97c84-117">**Einfaldur afsláttur** - eitt hlutfall eða upphæð.</span><span class="sxs-lookup"><span data-stu-id="97c84-117">**Simple discount** – A single percentage or amount.</span></span>
- <span data-ttu-id="97c84-118">**Magnafsláttur** – Afsláttar sem er notaður þegar tvær eða fleiri vörur eru keyptar.</span><span class="sxs-lookup"><span data-stu-id="97c84-118">**Quantity discount** – A discount that is applied when two or more products are purchased.</span></span>
- <span data-ttu-id="97c84-119">**Afsláttur blandaðs tilboðs** - Afsláttur sem er notaður þegar sérstök samsetning af vörum er keypt.</span><span class="sxs-lookup"><span data-stu-id="97c84-119">**Mix and match discount** – A discount that is applied when a specific combination of products is purchased.</span></span>
- <span data-ttu-id="97c84-120">**Þröskuldur afsláttar** - Afsláttur sem er notaður þegar færslusamtala er hærri en tilgreind upphæð.</span><span class="sxs-lookup"><span data-stu-id="97c84-120">**Threshold discount** – A discount that is applied when the transaction total is more than a specified amount.</span></span>

<span data-ttu-id="97c84-121">Hægt er að tengja bæði verðleiðréttingar og afslátt við sérstaka verðflokka.</span><span class="sxs-lookup"><span data-stu-id="97c84-121">Both price adjustments and discounts can be associated with price groups.</span></span> <span data-ttu-id="97c84-122">Síðan er hægt að tengja verðflokka við rásir, vörulista, tengsl og vildarkerfi.</span><span class="sxs-lookup"><span data-stu-id="97c84-122">Price groups can then be associated with channels, catalogs, affiliations, and loyalty programs.</span></span>
