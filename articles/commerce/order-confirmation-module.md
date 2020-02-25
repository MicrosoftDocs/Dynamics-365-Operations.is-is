---
title: Upplýsingaeining pöntunar
description: Þetta efni fjallar um upplýsingaeiningar pantana og lýsir því hvernig á að nota þær í Microsoft Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar-ms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: cb09a0b6ce1e48707f96021e9fad0006d9c1c55c
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/05/2020
ms.locfileid: "3026018"
---
# <a name="order-details-module"></a><span data-ttu-id="03748-103">Upplýsingaeining pöntunar</span><span class="sxs-lookup"><span data-stu-id="03748-103">Order details module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="03748-104">Þetta efni fjallar um upplýsingaeiningar pantana og lýsir því hvernig á að nota þær í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="03748-104">This topic covers order details modules and describes how to use them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="03748-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="03748-105">Overview</span></span>

<span data-ttu-id="03748-106">Eftir að pöntun hefur verið gerð er hægt að nota staðfestingarhlutann til að sýna staðfestingarupplýsingar.</span><span class="sxs-lookup"><span data-stu-id="03748-106">The order details module is used to show order confirmation details after an order has been placed.</span></span> <span data-ttu-id="03748-107">Hún sýnir auðkenni pöntunarstaðfestingar, upplýsingar um pöntunarupplýsingar og aðrar pöntunarupplýsingar, svo sem hlutina sem voru keyptir, greiðsluupplýsingar og sendingaraðferð.</span><span class="sxs-lookup"><span data-stu-id="03748-107">It shows the order confirmation ID, order contact information, and other order details, such as the items that were purchased, payment information, and the shipping method.</span></span>

## <a name="order-confirmation-module-properties"></a><span data-ttu-id="03748-108">Eiginleikar staðfestingareiningar pöntunar</span><span class="sxs-lookup"><span data-stu-id="03748-108">Order confirmation module properties</span></span>

| <span data-ttu-id="03748-109">Nafn eiginleika</span><span class="sxs-lookup"><span data-stu-id="03748-109">Property name</span></span>  | <span data-ttu-id="03748-110">Gildi</span><span class="sxs-lookup"><span data-stu-id="03748-110">Values</span></span> | <span data-ttu-id="03748-111">Lýsing</span><span class="sxs-lookup"><span data-stu-id="03748-111">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="03748-112">Fyrirsögn</span><span class="sxs-lookup"><span data-stu-id="03748-112">Heading</span></span>        | <span data-ttu-id="03748-113">Texti og merki fyrirsagnar (**H1**, **H2**, **H3**, **H4**, **H5** eða **H6**)</span><span class="sxs-lookup"><span data-stu-id="03748-113">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="03748-114">Pöntunarstaðfestingareiningin getur haft fyrirsögn.</span><span class="sxs-lookup"><span data-stu-id="03748-114">The order confirmation module can have a heading.</span></span> <span data-ttu-id="03748-115">Sjálfgefið er að fyrirsagnarmerkið **H2** er notað fyrir fyrirsögnina.</span><span class="sxs-lookup"><span data-stu-id="03748-115">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="03748-116">Hins vegar er hægt að breyta merkinu til að uppfylla kröfur um aðgengi.</span><span class="sxs-lookup"><span data-stu-id="03748-116">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="03748-117">Númer tengiliðar</span><span class="sxs-lookup"><span data-stu-id="03748-117">Contact number</span></span> | <span data-ttu-id="03748-118">Text</span><span class="sxs-lookup"><span data-stu-id="03748-118">Text</span></span> | <span data-ttu-id="03748-119">Hægt er að gefa upp tengiliðanúmer fyrir pöntunarskyldar spurningar.</span><span class="sxs-lookup"><span data-stu-id="03748-119">A contact number can be provided for order-related questions.</span></span> |

## <a name="modules-that-can-be-used-on-an-order-details-page"></a><span data-ttu-id="03748-120">Einingar sem hægt er að nota á pöntunarupplýsingasíðu</span><span class="sxs-lookup"><span data-stu-id="03748-120">Modules that can be used on an order details page</span></span>

<span data-ttu-id="03748-121">Þegar þú býrð til síðu fyrir pöntunarupplýsingar geturðu bætt við öðrum viðeigandi einingum til viðbótar pöntunarupplýsingareiningunni.</span><span class="sxs-lookup"><span data-stu-id="03748-121">When you create an order details page, you can add other relevant modules in addition to the order details module.</span></span> <span data-ttu-id="03748-122">Hér eru nokkur dæmi:</span><span class="sxs-lookup"><span data-stu-id="03748-122">Here are some examples:</span></span>

- <span data-ttu-id="03748-123">**Tillögueining** - Hægt er að bæta tillögueiningunni við á upplýsingasíðu pöntunar til að benda viðskiptavinum á aðrar vörur.</span><span class="sxs-lookup"><span data-stu-id="03748-123">**Recommendations module** – The recommendations module can be added to the order details page to suggest other products to the customer.</span></span>
- <span data-ttu-id="03748-124">**Markaðseiningar** - Hægt er að bæta hvaða markaðsseining sem er við pöntunarsíðuna til að sýna markaðsefni.</span><span class="sxs-lookup"><span data-stu-id="03748-124">**Marketing modules** – Any marketing module can be added to the order details page to show marketing content.</span></span>

## <a name="create-an-order-details-page-module"></a><span data-ttu-id="03748-125">Búa til einingu pöntunarupplýsingasíðu</span><span class="sxs-lookup"><span data-stu-id="03748-125">Create an order details page module</span></span>

1. <span data-ttu-id="03748-126">Búðu til síðusniðmát sem heitir **Sniðmát pöntunarstaðfestingar**.</span><span class="sxs-lookup"><span data-stu-id="03748-126">Create a page template that is named **Order details template**.</span></span>
1. <span data-ttu-id="03748-127">Í hólfinu **Aðal** á sjálfgefnu síðunni bætirðu við pöntunarupplýsingaeiningu.</span><span class="sxs-lookup"><span data-stu-id="03748-127">In the **Main** slot of the default page, add an order details module.</span></span>
1. <span data-ttu-id="03748-128">Bættu við tillögueiningu í pöntunarupplýsingaeiningunni.</span><span class="sxs-lookup"><span data-stu-id="03748-128">In the order details module, add a recommendations module.</span></span>
1. <span data-ttu-id="03748-129">Vistaðu og forskoðaðu sniðmátið.</span><span class="sxs-lookup"><span data-stu-id="03748-129">Save and preview the template.</span></span> <span data-ttu-id="03748-130">Pöntunarupplýsingaeiningin verður ekki látin af hendi sem hún þarf samhengi við pöntunarstaðfestingarnúmerið.</span><span class="sxs-lookup"><span data-stu-id="03748-130">The order details module won't be rendered, because it requires the context of the order confirmation number.</span></span>
1. <span data-ttu-id="03748-131">Ljúktu við að breyta sniðmátinu, vistaðu það og birtu.</span><span class="sxs-lookup"><span data-stu-id="03748-131">Finish editing the template, and publish it.</span></span>
1. <span data-ttu-id="03748-132">Notaðu pöntunarupplýsingasniðmátið sem þú bjóst til til að búa til síðu sem heitir **pöntunarupplýsingasíða**.</span><span class="sxs-lookup"><span data-stu-id="03748-132">Use the order details template that you just created to create a page that is named **order details page**.</span></span>
1. <span data-ttu-id="03748-133">Bættu sjálfgefnu síðunni við útlínur síðunnar.</span><span class="sxs-lookup"><span data-stu-id="03748-133">Add the default page to the page outline.</span></span>
1. <span data-ttu-id="03748-134">Í hólfið **Fyrirsögn** bætirðu við fyrirsagnarbroti.</span><span class="sxs-lookup"><span data-stu-id="03748-134">In the **Header** slot, add a header fragment.</span></span>
1. <span data-ttu-id="03748-135">Í hólfið **Síðufótur** bætirðu við síðufótarbroti.</span><span class="sxs-lookup"><span data-stu-id="03748-135">In the **Footer** slot, add a footer fragment.</span></span>
1. <span data-ttu-id="03748-136">Í hólfinu **Aðal** bætirðu við pöntunarupplýsingaeiningu.</span><span class="sxs-lookup"><span data-stu-id="03748-136">In the **Main** slot, add an order details module.</span></span>
1. <span data-ttu-id="03748-137">Í eiginleikaglugganum í einingu pöntunarupplýsinga bætirðu við fyrirsögninni **Pöntunarupplýsingar**.</span><span class="sxs-lookup"><span data-stu-id="03748-137">In the property pane for the order details module, add the heading **Order details**.</span></span>
1. <span data-ttu-id="03748-138">Fyrir neðan pöntunarupplýsingaeininguna skaltu bæta við tillögueiningunni og stilla hana þannig að hún noti stillingarnar **Nýtt** og **Mest selt**.</span><span class="sxs-lookup"><span data-stu-id="03748-138">Below the order details module, add a recommendations module, and configure it so that it uses the **New** and **Best Selling** settings.</span></span>
1. <span data-ttu-id="03748-139">Vistaðu og forskoðaðu síðuna.</span><span class="sxs-lookup"><span data-stu-id="03748-139">Save and preview the page.</span></span>
1. <span data-ttu-id="03748-140">Ljúktu við að breyta síðunni, vistaðu hana og birtu.</span><span class="sxs-lookup"><span data-stu-id="03748-140">Finish editing the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="03748-141">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="03748-141">Additional resources</span></span>

[<span data-ttu-id="03748-142">Yfirlit byrjendaeiningar</span><span class="sxs-lookup"><span data-stu-id="03748-142">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="03748-143">Hólfeining</span><span class="sxs-lookup"><span data-stu-id="03748-143">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="03748-144">Kaupgluggaeining</span><span class="sxs-lookup"><span data-stu-id="03748-144">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="03748-145">Körfueining</span><span class="sxs-lookup"><span data-stu-id="03748-145">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="03748-146">Greiðsluferliseining</span><span class="sxs-lookup"><span data-stu-id="03748-146">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="03748-147">Eining síðuhauss</span><span class="sxs-lookup"><span data-stu-id="03748-147">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="03748-148">Eining síðufótar</span><span class="sxs-lookup"><span data-stu-id="03748-148">Footer module</span></span>](author-footer-module.md)
