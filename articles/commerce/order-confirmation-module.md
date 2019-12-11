---
title: Eining pöntunarstaðfestingar
description: Þetta efni fjallar um staðfestingareiningar panntana og lýsir því hvernig á að stofna þær í Microsoft Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: e339ce02bb646d0d9a68c22b24fde9b72071de6f
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698327"
---
# <a name="order-confirmation-module"></a><span data-ttu-id="e0b5c-103">Eining pöntunarstaðfestingar</span><span class="sxs-lookup"><span data-stu-id="e0b5c-103">Order confirmation module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="e0b5c-104">Þetta efni fjallar um staðfestingareiningar panntana og lýsir því hvernig á að stofna þær í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="e0b5c-104">This topic covers order confirmation modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="e0b5c-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="e0b5c-105">Overview</span></span>

<span data-ttu-id="e0b5c-106">Pöntunarstaðfestingareining er notuð til að sýna staðfestingarskilaboð á staðfestingarsíðu þegar pöntun hefur verið gerð.</span><span class="sxs-lookup"><span data-stu-id="e0b5c-106">An order confirmation module is used to show a confirmation message on an order confirmation page after an order is placed.</span></span> <span data-ttu-id="e0b5c-107">Pöntunarstaðfestingareiningin sýnir pöntunarstaðfestingarnúmerið og netfang viðskiptavinarins sem gefið var upp í greiðsluferlinu.</span><span class="sxs-lookup"><span data-stu-id="e0b5c-107">The order confirmation module shows the order confirmation number and the customer email address that was provided during checkout.</span></span>

<span data-ttu-id="e0b5c-108">Þegar pöntun er gerð í greiðsluferli er pöntunarstaðfestingarnúmerið og netfang viðskiptavina sent á staðfestingarsíðu sem fyrirspurnstrengur í vefslóð síðunnar.</span><span class="sxs-lookup"><span data-stu-id="e0b5c-108">When an order is placed during checkout, the order confirmation number and customer email address are passed to the order confirmation page as a query string in the page's URL.</span></span> <span data-ttu-id="e0b5c-109">Pöntunarstaðfestingareiningin fær þessar upplýsingar og birtir pöntunarstöðu á pöntunarstaðfestingarsíðunni.</span><span class="sxs-lookup"><span data-stu-id="e0b5c-109">The order confirmation module receives this information and renders the order status on the order confirmation page.</span></span> <span data-ttu-id="e0b5c-110">Pöntunarstaðfestingin þarf þetta síðusamhengi til að gefa upp stöðu pöntunarinnar.</span><span class="sxs-lookup"><span data-stu-id="e0b5c-110">The order confirmation module requires this page context to provide the status of the order.</span></span>

## <a name="order-confirmation-module-properties"></a><span data-ttu-id="e0b5c-111">Eiginleikar staðfestingareiningar pöntunar</span><span class="sxs-lookup"><span data-stu-id="e0b5c-111">Order confirmation module properties</span></span>

| <span data-ttu-id="e0b5c-112">Nafn eiginleika</span><span class="sxs-lookup"><span data-stu-id="e0b5c-112">Property name</span></span> | <span data-ttu-id="e0b5c-113">Gildi</span><span class="sxs-lookup"><span data-stu-id="e0b5c-113">Values</span></span> | <span data-ttu-id="e0b5c-114">Lýsing</span><span class="sxs-lookup"><span data-stu-id="e0b5c-114">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="e0b5c-115">Fyrirsögn</span><span class="sxs-lookup"><span data-stu-id="e0b5c-115">Heading</span></span>       | <span data-ttu-id="e0b5c-116">Texti og merki fyrirsagnar (**H1**, **H2**, **H3**, **H4**, **H5** eða **H6**)</span><span class="sxs-lookup"><span data-stu-id="e0b5c-116">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="e0b5c-117">Pöntunarstaðfestingareiningin getur haft fyrirsögn.</span><span class="sxs-lookup"><span data-stu-id="e0b5c-117">The order confirmation module can have a heading.</span></span> <span data-ttu-id="e0b5c-118">Sjálfgefið er að fyrirsagnarmerkið **H2** er notað fyrir fyrirsögnina.</span><span class="sxs-lookup"><span data-stu-id="e0b5c-118">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="e0b5c-119">Hins vegar er hægt að breyta merkinu til að uppfylla kröfur um aðgengi.</span><span class="sxs-lookup"><span data-stu-id="e0b5c-119">However, the tag can be changed to meet accessibility requirements.</span></span> |

## <a name="modules-that-can-be-used-in-an-order-confirmation-page-module"></a><span data-ttu-id="e0b5c-120">Einingar sem hægt er að nota í einingu pöntunarstaðfestingarsíðu</span><span class="sxs-lookup"><span data-stu-id="e0b5c-120">Modules that can be used in an order confirmation page module</span></span> 

- <span data-ttu-id="e0b5c-121">**Tillögur** - Hægt er að setja tillögueininguna á staðfestingarsíðu pöntunar til að benda viðskiptavinum á aðrar vörur.</span><span class="sxs-lookup"><span data-stu-id="e0b5c-121">**Recommendations** – The recommendations module can be put on the order confirmation page to suggest other products to the customer.</span></span>
- <span data-ttu-id="e0b5c-122">**Markaðssetning** - Markaðseiningin getur bætt markaðsinnihaldi við staðfestingarsíðu.</span><span class="sxs-lookup"><span data-stu-id="e0b5c-122">**Marketing** – The marketing module can add marketing content to the order confirmation page.</span></span>

## <a name="create-an-order-confirmation-page-module"></a><span data-ttu-id="e0b5c-123">Búa til einingu pöntunarstaðfestingarsíðu</span><span class="sxs-lookup"><span data-stu-id="e0b5c-123">Create an order confirmation page module</span></span>

1. <span data-ttu-id="e0b5c-124">Búðu til síðusniðmát sem heitir **sniðmát pöntunarstaðfestingar**.</span><span class="sxs-lookup"><span data-stu-id="e0b5c-124">Create a page template that is named **order confirmation template**.</span></span>
1. <span data-ttu-id="e0b5c-125">Í hólfinu **Aðal** á sjálfgefnu síðunni bætirðu við pöntunarstaðfestingareiningu.</span><span class="sxs-lookup"><span data-stu-id="e0b5c-125">In the **Main** slot of the default page, add an order confirmation module.</span></span>
1. <span data-ttu-id="e0b5c-126">Bættu við tillagnaeiningu í pöntunarstaðfestingareiningunni.</span><span class="sxs-lookup"><span data-stu-id="e0b5c-126">In the order confirmation module, add a recommendations module.</span></span>
1. <span data-ttu-id="e0b5c-127">Vistaðu og forskoðaðu sniðmátið.</span><span class="sxs-lookup"><span data-stu-id="e0b5c-127">Save and preview the template.</span></span> <span data-ttu-id="e0b5c-128">Ekki ætti að láta pöntunarstaðfestinguna af hendi þar sem hún þarf samhengi við pöntunarstaðfestingarnúmerið.</span><span class="sxs-lookup"><span data-stu-id="e0b5c-128">The order confirmation module should not be rendered, because it requires the context of the order confirmation number.</span></span>
1. <span data-ttu-id="e0b5c-129">Skráðu brotið út í sniðmátinu og birtu það.</span><span class="sxs-lookup"><span data-stu-id="e0b5c-129">Check in the template, and publish it.</span></span>
1. <span data-ttu-id="e0b5c-130">Notaðu pöntunarstaðfestingarsniðmátið sem þú bjóst til til að búa til síðu sem heitir **pöntunarstaðfestingarsíða**.</span><span class="sxs-lookup"><span data-stu-id="e0b5c-130">Use the order confirmation template that you just created to create a page that is named **order confirmation page**.</span></span>
1. <span data-ttu-id="e0b5c-131">Bættu sjálfgefnu síðunni við útlínur síðunnar.</span><span class="sxs-lookup"><span data-stu-id="e0b5c-131">Add the default page to the page outline.</span></span>
1. <span data-ttu-id="e0b5c-132">Í hólfið **Fyrirsögn** bætirðu við fyrirsagnarbroti.</span><span class="sxs-lookup"><span data-stu-id="e0b5c-132">In the **Header** slot, add a header fragment.</span></span>
1. <span data-ttu-id="e0b5c-133">Í hólfið **Síðufótur** bætirðu við síðufótarbroti.</span><span class="sxs-lookup"><span data-stu-id="e0b5c-133">In the **Footer** slot, add a footer fragment.</span></span>
1. <span data-ttu-id="e0b5c-134">Í hólfinu **Aðal** bætirðu við pöntunarstaðfestingareiningu.</span><span class="sxs-lookup"><span data-stu-id="e0b5c-134">In the **Main** slot, add an order confirmation module.</span></span>
1. <span data-ttu-id="e0b5c-135">Í eiginleikaglugganum í einingu pöntunarstaðfestingar bætirðu við fyrirsögninni **Pöntunarstaðfesting**.</span><span class="sxs-lookup"><span data-stu-id="e0b5c-135">In the property pane of the order confirmation module, add the heading **Order confirmation**.</span></span>
1. <span data-ttu-id="e0b5c-136">Fyrir neðan pöntunarstaðfestingareininguna skaltu bæta við tillögueiningunni og stilla hana þannig að hún noti stillingarnar **Nýtt** og **Mest selt**.</span><span class="sxs-lookup"><span data-stu-id="e0b5c-136">Below the order confirmation module, add a recommendations module, and configure it so that it uses the **New** and **Best Selling** settings.</span></span>
1. <span data-ttu-id="e0b5c-137">Vistaðu og forskoðaðu síðuna, skráðu hana inn og gefðu út.</span><span class="sxs-lookup"><span data-stu-id="e0b5c-137">Save and preview the page, check it in, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e0b5c-138">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="e0b5c-138">Additional resources</span></span>

[<span data-ttu-id="e0b5c-139">Yfirlit byrjendaeiningar</span><span class="sxs-lookup"><span data-stu-id="e0b5c-139">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="e0b5c-140">Hólfeining</span><span class="sxs-lookup"><span data-stu-id="e0b5c-140">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="e0b5c-141">Kaupgluggaeining</span><span class="sxs-lookup"><span data-stu-id="e0b5c-141">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="e0b5c-142">Körfueining</span><span class="sxs-lookup"><span data-stu-id="e0b5c-142">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="e0b5c-143">Greiðsluferliseining</span><span class="sxs-lookup"><span data-stu-id="e0b5c-143">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="e0b5c-144">Eining síðuhauss</span><span class="sxs-lookup"><span data-stu-id="e0b5c-144">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="e0b5c-145">Eining síðufótar</span><span class="sxs-lookup"><span data-stu-id="e0b5c-145">Footer module</span></span>](author-footer-module.md)
