---
title: Eining fyrir afhendingarupplýsingar
description: Þetta efnisatriði fjallar um einingu afhendingarupplýsinga og útskýrir hvernig á að bæta henni við greiðslusíður á vefsvæði Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 11/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-09021
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 063701d5cd5714febeb32907346d9f6e5c2a2ca1
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5804406"
---
# <a name="pickup-information-module"></a><span data-ttu-id="d02d8-103">Eining fyrir afhendingarupplýsingar</span><span class="sxs-lookup"><span data-stu-id="d02d8-103">Pickup information module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d02d8-104">Þetta efnisatriði fjallar um einingu afhendingarupplýsinga og útskýrir hvernig á að bæta henni við greiðslusíður á vefsvæði Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="d02d8-104">This topic covers the pickup information module and describes how to add it to checkout pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="d02d8-105">Hægt er að nota eininguna fyrir afhendingarupplýsingar í greiðsluferliseiningu til að sýna upplýsingar um tiltekt pantana.</span><span class="sxs-lookup"><span data-stu-id="d02d8-105">The pickup information module can be used in a checkout module to show order pickup information.</span></span> <span data-ttu-id="d02d8-106">Viðskiptavinir geta skoðað tiltækar dagsetningar og tímahólf og valið hentugan tíma til að sækja pöntunina.</span><span class="sxs-lookup"><span data-stu-id="d02d8-106">Customers can view available pickup dates and time slots, and then select a suitable time to pick up their order.</span></span> <span data-ttu-id="d02d8-107">Til dæmis getur viðskiptavinur valið að sækja pöntun klukkan 15:00 þann 21. mars frá San Francisco-versluninni.</span><span class="sxs-lookup"><span data-stu-id="d02d8-107">For example, a customer can choose to pick up an order at 3 PM on March 21 from the San Francisco store.</span></span>

<span data-ttu-id="d02d8-108">Skilgreina verður tímahólf sóttra pantana fyrir viðeigandi verslanir í Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="d02d8-108">Pickup time slots for the appropriate stores must be configured in Commerce headquarters.</span></span> <span data-ttu-id="d02d8-109">Frekari upplýsingar er að finna í [Stofna og uppfæra tímabil afhendingar til viðskiptavinar](dev-itpro/pickup-timeslots.md).</span><span class="sxs-lookup"><span data-stu-id="d02d8-109">For more information, see [Create and update time slots for customer pickup](dev-itpro/pickup-timeslots.md).</span></span>

<span data-ttu-id="d02d8-110">Þegar eining fyrir afhendingarupplýsingar er stofnuð á greiðsluferlissíðu en engin tímahólf eru skilgreind fyrir verslunina sem valin er til að sækja, sýnir einingin upplýsingar en notandinn getur ekki valið nein tímahólf.</span><span class="sxs-lookup"><span data-stu-id="d02d8-110">If a pickup information module is created on a checkout page, but no time slots are defined for the store that is selected for pickup, the module will show information, but the user won't be able to select any time slots.</span></span> <span data-ttu-id="d02d8-111">Tímahólf eru valkvæð og eru ekki nauðsynleg til að leggja pöntunina inn.</span><span class="sxs-lookup"><span data-stu-id="d02d8-111">Time slots are optional and aren't required to place an order.</span></span>

<span data-ttu-id="d02d8-112">Þegar margar vörur eru valdar til að sækja í mörgum verslunum leyfir eining fyrir afhendingarupplýsingar notandanum að velja tímahólf fyrir hverja verslun fyrir sig, að því gefnu að tímahólf séu tiltæk fyrir slíkt.</span><span class="sxs-lookup"><span data-stu-id="d02d8-112">If multiple items are selected for pickup across multiple stores, the pickup information module will let the user select a time slot for each store, provided that time slots are available for it.</span></span>

> [!NOTE]
> <span data-ttu-id="d02d8-113">Stuðningur við tímahólf og eining fyrir afhendingarupplýsingar greiðsluferils er tiltækt í Dynamics 365 Commerce útgáfu 10.0.15 og nýrri útgáfum.</span><span class="sxs-lookup"><span data-stu-id="d02d8-113">Support for time slots and the checkout pickup information module is available in Dynamics 365 Commerce version 10.0.15 and later.</span></span>

<span data-ttu-id="d02d8-114">Eftirfarandi skýringarmynd sýnir dæmi um val á tímahólfi á einingu afhendingarupplýsinga á greiðsluferlissíðu.</span><span class="sxs-lookup"><span data-stu-id="d02d8-114">The following illustration shows an example of time slot selection through the pickup information module on a checkout page.</span></span>

![Dæmi um einingu afhendingarvalkosts á greiðsluferlissíðu](./dev-itpro/media/Curbside_timeslot_eCommerce.PNG)

## <a name="module-properties"></a><span data-ttu-id="d02d8-116">Eiginleikar einingar</span><span class="sxs-lookup"><span data-stu-id="d02d8-116">Module properties</span></span>

- <span data-ttu-id="d02d8-117">**Fyrirsögn** – Sláið inn fyrirsögn fyrir eininguna.</span><span class="sxs-lookup"><span data-stu-id="d02d8-117">**Heading** – Enter a heading for the module.</span></span>

## <a name="show-time-slot-information-after-an-order-is-placed"></a><span data-ttu-id="d02d8-118">Sýna upplýsingar um tímahólf eftir að pöntun er gerð</span><span class="sxs-lookup"><span data-stu-id="d02d8-118">Show time slot information after an order is placed</span></span>

<span data-ttu-id="d02d8-119">Eftir að pöntun er gerð er hægt að skoða upplýsingar um valið tímahólf í [Einingu pöntunarstaðfestingar](order-confirmation-module.md) og [Upplýsingaeiningar pöntunar](account-management.md#order-details-page).</span><span class="sxs-lookup"><span data-stu-id="d02d8-119">After an order is placed, information about the selected time slot can be viewed in the [order confirmation module](order-confirmation-module.md) and the [order details module](account-management.md#order-details-page).</span></span> <span data-ttu-id="d02d8-120">Báðar þessar einingar hafa eiginleikann **Sýna upplýsingar um tímahólf**.</span><span class="sxs-lookup"><span data-stu-id="d02d8-120">Both these modules have a **Show timeslot information** property.</span></span> <span data-ttu-id="d02d8-121">Áður en hægt er að sýna valið tímahólf við pöntunarferlið verður að stilla þennan eiginleika á **Satt**.</span><span class="sxs-lookup"><span data-stu-id="d02d8-121">Before they can show the selected time slot during the order process, this property must be set to **True**.</span></span>

## <a name="add-a-checkout-pickup-information-module-to-a-page"></a><span data-ttu-id="d02d8-122">Bæta við einingu afhendingarupplýsinga greiðsluferlis við síðu</span><span class="sxs-lookup"><span data-stu-id="d02d8-122">Add a checkout pickup information module to a page</span></span>

<span data-ttu-id="d02d8-123">Leiðbeiningar um hvernig bæta skuli einingu afhendingarupplýsinga við greiðsluferlissíðu og stilla nauðsynlega eiginleika er að finna í [Greiðsluferliseining](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="d02d8-123">For instructions about how to add a pickup information module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

<span data-ttu-id="d02d8-124">Eftirfarandi mynd sýnir dæmi um útskráningarsíðu e-Commerce sem inniheldur tímahólf fyrir línuvörur afhendingar.</span><span class="sxs-lookup"><span data-stu-id="d02d8-124">The following illustration shows an example of an e-Commerce checkout page that includes time slots for pickup line items.</span></span>

![Dæmi um greiðsluferlissíðu e-Commerce sem inniheldur tímahólf fyrir línuatriði](./dev-itpro/media/Curbside_timeslot_eCommerce_checkoutsummary.PNG)

## <a name="additional-resources"></a><span data-ttu-id="d02d8-126">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="d02d8-126">Additional resources</span></span>

[<span data-ttu-id="d02d8-127">Stofna og uppfæra tímabil afhendingar til viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="d02d8-127">Create and update time slots for customer pickup</span></span>](dev-itpro/pickup-timeslots.md)

[<span data-ttu-id="d02d8-128">Greiðsluferliseining</span><span class="sxs-lookup"><span data-stu-id="d02d8-128">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="d02d8-129">Eining pöntunarstaðfestingar</span><span class="sxs-lookup"><span data-stu-id="d02d8-129">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="d02d8-130">Pöntunarupplýsingaeining</span><span class="sxs-lookup"><span data-stu-id="d02d8-130">Order details module</span></span>](account-management.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]