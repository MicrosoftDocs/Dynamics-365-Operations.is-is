---
title: Valkosturinn Sækja þetta birtist ekki í körfu eða upplýsingasíðu afurðar
description: Þetta efnisatriði býður upp á leiðsögn úrræðaleitar sem getur reynst hjálpleg þegar valkosturinn fyrir sótt í verslun birtist ekki á körfusíðunni eða upplýsingasíðu afurðar.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f692d73bf1755422e9bfc8314c1156e043ccf761
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020808"
---
# <a name="pick-this-up-option-doesnt-appear-on-cart-or-product-details-pages"></a><span data-ttu-id="6334c-103">Valkosturinn „Sækja þetta“ birtist ekki í körfu eða upplýsingasíðu afurðar</span><span class="sxs-lookup"><span data-stu-id="6334c-103">"Pick this up" option doesn't appear on cart or product details pages</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6334c-104">Þetta efnisatriði býður upp á leiðsögn úrræðaleitar sem getur reynst hjálpleg þegar valkosturinn fyrir sótt í verslun birtist ekki á körfusíðunni eða upplýsingasíðu afurðar.</span><span class="sxs-lookup"><span data-stu-id="6334c-104">This topic provides troubleshooting guidance that can help when the option for in-store pickup doesn't appear on the cart page or product details pages.</span></span>

## <a name="description"></a><span data-ttu-id="6334c-105">lýsing</span><span class="sxs-lookup"><span data-stu-id="6334c-105">Description</span></span>

<span data-ttu-id="6334c-106">Hnappurinn **Sækja þetta** birtist ekki á körfusíðu eða upplýsingasíðu afurðar.</span><span class="sxs-lookup"><span data-stu-id="6334c-106">The **Pick this up** button doesn't appear on the cart page or product details pages.</span></span>

<span data-ttu-id="6334c-107">Eftirfarandi skýringarmynd sýnir dæmi um síðu sem inniheldur hnappinn **Sækja þetta**.</span><span class="sxs-lookup"><span data-stu-id="6334c-107">The following illustration shows an example of a page that includes the **Pick this up** button.</span></span>

![Hnappurinn Sækja þetta](media/pickup-button-missing.jpg)

## <a name="resolution"></a><span data-ttu-id="6334c-109">Upplausn</span><span class="sxs-lookup"><span data-stu-id="6334c-109">Resolution</span></span>

### <a name="enable-the-bopis-extension-in-commerce-site-builder"></a><span data-ttu-id="6334c-110">Virkja BOPIS-viðbótina í vefsmið Commerce</span><span class="sxs-lookup"><span data-stu-id="6334c-110">Enable the BOPIS extension in Commerce site builder</span></span>

<span data-ttu-id="6334c-111">Til að virkja (BOPIS)-viðbótina „kaupa á netinu, sækja í verslun“ í vefsmið Commerce skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="6334c-111">To enable the "buy online, pick up in store" (BOPIS) extension in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="6334c-112">Veldu svæðið.</span><span class="sxs-lookup"><span data-stu-id="6334c-112">Select your site.</span></span>
1. <span data-ttu-id="6334c-113">Veljið **Stillingar svæðis** og veljið því næst **Viðbætur**.</span><span class="sxs-lookup"><span data-stu-id="6334c-113">Select **Site settings**, and then select **Extensions**.</span></span>
1. <span data-ttu-id="6334c-114">Gangið úr skugga um að valkosturinn **Slökkva á BOPIS** sé hreinsaður.</span><span class="sxs-lookup"><span data-stu-id="6334c-114">Make sure that the **Disable BOPIS** option is cleared.</span></span>

### <a name="configure-modes-of-delivery-in-commerce-headquarters"></a><span data-ttu-id="6334c-115">Skilgreina afhendingarmáta í Commerce Headquarters</span><span class="sxs-lookup"><span data-stu-id="6334c-115">Configure modes of delivery in Commerce headquarters</span></span>

<span data-ttu-id="6334c-116">Til að skilgreina afhendingarmáta í Commerce Headquarters skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="6334c-116">To configure modes of delivery in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="6334c-117">Farið í **Innkaup og aðföng \> Uppsetning \> Afhendingarmátar**.</span><span class="sxs-lookup"><span data-stu-id="6334c-117">Go to **Procurement and sourcing \> Setup \> Modes of delivery**.</span></span>
1. <span data-ttu-id="6334c-118">Gangið úr skugga um að afhendingarmátinn **Viðskiptavinur sækir** hafi verið búinn til og honum hafi verið úthlutað afurðum og aðsetrum.</span><span class="sxs-lookup"><span data-stu-id="6334c-118">Make sure that a **Customer pickup** mode of delivery has been created, and that products and addresses are assigned to it.</span></span>
1. <span data-ttu-id="6334c-119">Opnið **Smásala og viðskipti \> Uppsetning höfuðstöðva \> Færibreytur**.</span><span class="sxs-lookup"><span data-stu-id="6334c-119">Go to **Retail and Commerce \> Headquarters setup \> Parameters**.</span></span>
1. <span data-ttu-id="6334c-120">Í vinstri flettingunni skal velja **Pantanir viðskiptavinar**.</span><span class="sxs-lookup"><span data-stu-id="6334c-120">In the left navigation, select **Customer orders**.</span></span>
1. <span data-ttu-id="6334c-121">Gangið úr skugga um að **Sóttur afhendingarmáti** sé rétt skilgreindur.</span><span class="sxs-lookup"><span data-stu-id="6334c-121">Make sure that **Pickup mode of delivery** is correctly configured.</span></span>

### <a name="configure-customer-orders-payments"></a><span data-ttu-id="6334c-122">Skilgreina greiðslur vegna pantana viðskiptavina</span><span class="sxs-lookup"><span data-stu-id="6334c-122">Configure customer orders payments</span></span>

<span data-ttu-id="6334c-123">Til að skilgreina greiðslur vegna pantana viðskiptavina í Commerce Headquarters skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="6334c-123">To configure customer orders payments in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="6334c-124">Opnið **Smásala og viðskipti \> Uppsetning höfuðstöðva \> Færibreytur**.</span><span class="sxs-lookup"><span data-stu-id="6334c-124">Go to **Retail and Commerce \> Headquarters setup \> Parameters**.</span></span>
1. <span data-ttu-id="6334c-125">Í vinstri flettingunni skal velja **Pantanir viðskiptavinar**.</span><span class="sxs-lookup"><span data-stu-id="6334c-125">In the left navigation, select **Customer orders**.</span></span>
1. <span data-ttu-id="6334c-126">Í flýtiflipanum **Greiðslur** skal ganga úr skugga um reitirnir **Greiðsluskilmálar** og **Greiðslumáti** séu rétt stilltir.</span><span class="sxs-lookup"><span data-stu-id="6334c-126">On the **Payments** FastTab, make sure that the **Terms of payment** and **Method of payment** fields are correctly set.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6334c-127">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="6334c-127">Additional resources</span></span>

[<span data-ttu-id="6334c-128">Skilgreina BOPIS</span><span class="sxs-lookup"><span data-stu-id="6334c-128">Configure BOPIS</span></span>](../cpe-bopis.md)

[<span data-ttu-id="6334c-129">Virkja marga afhendingamáta fyrir pantanir viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="6334c-129">Enable multiple pickup delivery modes for customer orders</span></span>](../multiple-pickup-modes.md)

[<span data-ttu-id="6334c-130">Greiðslur Commerce-pöntunar í samskiptamiðstöð</span><span class="sxs-lookup"><span data-stu-id="6334c-130">Omni-channel Commerce order payments</span></span>](../dev-itpro/commerce-payments.md)

[<span data-ttu-id="6334c-131">Eining til að velja verslun</span><span class="sxs-lookup"><span data-stu-id="6334c-131">Store selector module</span></span>](../store-selector.md)
