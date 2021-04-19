---
title: Afgreiða pantanir frá annarri verslun með því að nota eiginleikann Hleðslusending
description: Þetta efnisatriði lýsir Hleðslusending eiginleikanum.
author: ashishmsft
ms.date: 10/10/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-10-10
ms.dyn365.ops.version: Retail July 2017 update
ms.openlocfilehash: b9e0c4f55fd823bf7471edfe6ce1d424b0179d21
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800472"
---
# <a name="ship-orders-from-another-store-by-using-the-charge-send-feature"></a><span data-ttu-id="600c6-103">Afgreiða pantanir frá annarri verslun með því að nota eiginleikann Hleðslusending</span><span class="sxs-lookup"><span data-stu-id="600c6-103">Ship orders from another store by using the Charge send feature</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="600c6-104">Með Hleðslusending eiginleikanum í Commerce getur viðskiptavinarpantanir verið sett í eina verslun og send frá öðrum verslun.</span><span class="sxs-lookup"><span data-stu-id="600c6-104">With the Charge send feature in Commerce, customer orders can be placed in one store and shipped from another store.</span></span>

<span data-ttu-id="600c6-105">Viðskiptavinapantanir á sölustað (POS) biðlari styðja margskonar uppfyllingarkosti.</span><span class="sxs-lookup"><span data-stu-id="600c6-105">Customer orders in the point of sale (POS) client support multiple fulfillment options.</span></span> <span data-ttu-id="600c6-106">Nokkur dæmi um valkosti uppfyllingar eru:</span><span class="sxs-lookup"><span data-stu-id="600c6-106">Some examples of fulfillment options include:</span></span>

- <span data-ttu-id="600c6-107">Sækja frá sömu verslun á annan dag.</span><span class="sxs-lookup"><span data-stu-id="600c6-107">Pick up from the same store on a different date.</span></span>
- <span data-ttu-id="600c6-108">Sækja frá annarri verslun á sama degi eða öðrum degi.</span><span class="sxs-lookup"><span data-stu-id="600c6-108">Pick up from a different store on the same date or a different date.</span></span>
- <span data-ttu-id="600c6-109">Senda frá sjálfgefna afhendingarvöruhúsinu sem er úthlutað til verslunarinnar, og afhenda á tilteknum degi.</span><span class="sxs-lookup"><span data-stu-id="600c6-109">Ship from the default shipping warehouse that is assigned to the store, and deliver on a specific date.</span></span>

<span data-ttu-id="600c6-110">Hleðslusending eiginleikinn notar eftirfarandi POS aðgerðir: Senda allar vörur og Senda valdar vörur.</span><span class="sxs-lookup"><span data-stu-id="600c6-110">The Charge send feature uses the following POS operations: Ship all products and Ship selected products.</span></span> <span data-ttu-id="600c6-111">Þetta gerir afgreiðslustarfsmanni kleift að velja „senda frá“ staðsetninguna, þaðan sem hægt er að uppfylla pöntunina eða pöntunarlínuna.</span><span class="sxs-lookup"><span data-stu-id="600c6-111">This allows the store clerk to select the "ship from" location that the order or order line can be fulfilled from.</span></span> <span data-ttu-id="600c6-112">„Senda frá“ staðsetningin er að sjálfgefnu afhendingarvöruhús sem tengist versluninni.</span><span class="sxs-lookup"><span data-stu-id="600c6-112">By default, the "ship from" location is the shipping warehouse that is associated with the store.</span></span> <span data-ttu-id="600c6-113">Hins vegar getur afgreiðslustarfsmaðurinn breytt þessari staðsetningu og valið hvaða verslun sem er skilgreindur í hópnum verslanaleit, sem er úthlutað til verslunarinnar.</span><span class="sxs-lookup"><span data-stu-id="600c6-113">However, the store clerk can change this location and select any store that is defined in the store locator group that is assigned to the store.</span></span>

<span data-ttu-id="600c6-114">Hæfni til að velja „senda til" heimilisföng er óbreytt.</span><span class="sxs-lookup"><span data-stu-id="600c6-114">The ability to select "ship to" addresses remains unchanged.</span></span>

<span data-ttu-id="600c6-115">Afhendingaraðferðirnar, sem hægt er að nota til að uppfylla pöntunarlínuna, eru byggðar á grunnstillingum gildra afhendingarmáta fyrir vörur og heimilisföng.</span><span class="sxs-lookup"><span data-stu-id="600c6-115">The shipping methods that can be used to fulfill the order line are based on the configuration of valid modes of delivery for products and addresses.</span></span> <span data-ttu-id="600c6-116">Vegna þess að reglunum um gilda afhendingarmáta eru aðeins viðhaldið í bakvinnslu (HQ), framkvæmir POS viðskiptavinurinn rauntímasímtal til að sækja gilda afhendingarmáta fyrir sendingarlínu.</span><span class="sxs-lookup"><span data-stu-id="600c6-116">Because the rules about valid of modes of delivery are maintained only in the Headquarters (HQ), the POS client makes a real-time call to fetch the valid modes of delivery for a ship line.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]