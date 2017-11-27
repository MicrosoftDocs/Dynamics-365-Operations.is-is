---
title: "Senda pöntun frá annarri verslun"
description: "Þetta efnisatriði lýsir Hleðslusending eiginleikanum."
author: ashishmsft
manager: AnnBe
ms.date: 10/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Core, Retail
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-10-10
ms.dyn365.ops.version: Retail Version
ms.translationtype: HT
ms.sourcegitcommit: 986ec7835dac52c326085c47313205d08b1bafa8
ms.openlocfilehash: d217bc31ad9d93c5440e5329f7b7327d089137f4
ms.contentlocale: is-is
ms.lasthandoff: 10/10/2017

---

# <a name="ship-an-order-from-a-different-store"></a><span data-ttu-id="1641f-103">Senda pöntun frá annarri verslun</span><span class="sxs-lookup"><span data-stu-id="1641f-103">Ship an order from a different store</span></span>

<span data-ttu-id="1641f-104">Með Hleðslusending eiginleikanum í Dynamics 365 for Retail getur viðskiptavinarpantanir verið sett í eina verslun og send frá öðrum verslun.</span><span class="sxs-lookup"><span data-stu-id="1641f-104">With the Charge send feature in Dynamics 365 for Retail, customer orders can be placed in one store and shipped from another store.</span></span> <span data-ttu-id="1641f-105">Viðskiptavinapantanir á sölustað (POS) biðlari styðja margskonar uppfyllingarkosti.</span><span class="sxs-lookup"><span data-stu-id="1641f-105">Customer orders in the point of sale (POS) client support multiple fulfillment options.</span></span> <span data-ttu-id="1641f-106">Nokkur dæmi um valkosti uppfyllingar eru:</span><span class="sxs-lookup"><span data-stu-id="1641f-106">Some examples of fulfillment options include:</span></span>
-   <span data-ttu-id="1641f-107">Sækja frá sömu verslun á annan dag.</span><span class="sxs-lookup"><span data-stu-id="1641f-107">Pick up from the same store on a different date.</span></span>
-   <span data-ttu-id="1641f-108">Sækja frá annarri verslun á sama degi eða öðrum degi.</span><span class="sxs-lookup"><span data-stu-id="1641f-108">Pick up from a different store on the same date or a different date.</span></span>
-   <span data-ttu-id="1641f-109">Senda frá sjálfgefna afhendingarvöruhúsinu sem er úthlutað til verslunarinnar, og afhenda á tilteknum degi.</span><span class="sxs-lookup"><span data-stu-id="1641f-109">Ship from the default shipping warehouse that is assigned to the store, and deliver on a specific date.</span></span>

<span data-ttu-id="1641f-110">Hleðslusending eiginleikinn notar eftirfarandi POS aðgerðir: Senda allar vörur og Senda valdar vörur.</span><span class="sxs-lookup"><span data-stu-id="1641f-110">The Charge send feature uses the following POS operations: Ship all products and Ship selected products.</span></span> <span data-ttu-id="1641f-111">Þetta gerir afgreiðslustarfsmanni kleift að velja „senda frá“ staðsetninguna, þaðan sem hægt er að uppfylla pöntunina eða pöntunarlínuna.</span><span class="sxs-lookup"><span data-stu-id="1641f-111">This allows the store clerk to select the “ship from” location that the order or order line can be fulfilled from.</span></span> <span data-ttu-id="1641f-112">„Senda frá“ staðsetningin er að sjálfgefnu afhendingarvöruhús sem tengist versluninni.</span><span class="sxs-lookup"><span data-stu-id="1641f-112">By default, the “ship from” location is the shipping warehouse that is associated with the store.</span></span> <span data-ttu-id="1641f-113">Hins vegar getur afgreiðslustarfsmaðurinn breytt þessari staðsetningu og valið hvaða verslun sem er skilgreindur í hópnum verslanaleit, sem er úthlutað til verslunarinnar.</span><span class="sxs-lookup"><span data-stu-id="1641f-113">However, the store clerk can change this location and select any store that is defined in the store locator group that is assigned to the store.</span></span> 

<span data-ttu-id="1641f-114">Hæfni til að velja „senda til" heimilisföng er óbreytt.</span><span class="sxs-lookup"><span data-stu-id="1641f-114">The ability to select “ship to” addresses remains unchanged.</span></span> 

<span data-ttu-id="1641f-115">Afhendingaraðferðirnar, sem hægt er að nota til að uppfylla pöntunarlínuna, eru byggðar á grunnstillingum gildra afhendingarmáta fyrir vörur og heimilisföng.</span><span class="sxs-lookup"><span data-stu-id="1641f-115">The shipping methods that can be used to fulfill the order line are based on the configuration of valid modes of delivery for products and addresses.</span></span> <span data-ttu-id="1641f-116">Vegna þess að reglunum um gilda afhendingarmáta eru aðeins viðhaldið í Retail Headquarters (HQ), framkvæmir POS viðskiptavinurinn rauntímasímtal til að sækja gilda afhendingarmáta fyrir sendingarlínu.</span><span class="sxs-lookup"><span data-stu-id="1641f-116">Because the rules about valid of modes of delivery are maintained only in the Retail headquarters (HQ), the POS client makes a real-time call to fetch the valid modes of delivery for a ship line.</span></span> 


