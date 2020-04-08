---
title: Betri meðhöndlun á runuröktum vörum
description: Þetta efnisatriði lýsir endurbótunum sem hafa verið gerðar á meðhöndlun á runum fyrir runuraktar vörur í bókunarferlinu fyrir uppgjör.
author: josaw1
manager: AnnBe
ms.date: 11/04/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-05-28
ms.dyn365.ops.version: 10
ms.openlocfilehash: ecff18f0a34d22ef359f473fa6aaaff16c811bb6
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004206"
---
# <a name="improved-handling-of-batch-tracked-items"></a><span data-ttu-id="0fa6a-103">Betri meðhöndlun á runuröktum vörum</span><span class="sxs-lookup"><span data-stu-id="0fa6a-103">Improved handling of batch-tracked items</span></span>


[!include [banner](includes/banner.md)]


<span data-ttu-id="0fa6a-104">Á sölustaðnum er ekki hægt að sækja rununúmer fyrir runuraktar vörur þegar sala stendur yfir.</span><span class="sxs-lookup"><span data-stu-id="0fa6a-104">In Point of Sale (POS), batch numbers can't be captured for batch-tracked items at the time of sale.</span></span> <span data-ttu-id="0fa6a-105">Hins vegar, fyrir ákveðnar skilgreiningar, þegar sölur eru bókaðar í höfuðstöðvunum í gegnum pantanir viðskiptamanns eða bókun á uppgjöri gerir Microsoft Dynamics-kerfið ráð fyrir því að gild rununúmer fyrir runuraktar vörur séu til staðar og að þau verði notuð í reikningsfærsluferlinu.</span><span class="sxs-lookup"><span data-stu-id="0fa6a-105">However, for specific configurations, when sales are posted in the headquarters through customer orders or statement posting, the Microsoft Dynamics system expects that valid batch numbers for batch-tracked items exist, and that they will be used during the invoicing process.</span></span>

<span data-ttu-id="0fa6a-106">Ef gild rununúmer eru í boði fyrir vörur eru þau notuð í reikningsfærsluferli viðskiptamannapöntunar og reikningsfærsluferli sölupöntunar úr bókun uppgjörs.</span><span class="sxs-lookup"><span data-stu-id="0fa6a-106">If valid batch numbers are available for products, the customer order invoicing process and the sales order invoicing process from statement posting use them.</span></span> <span data-ttu-id="0fa6a-107">Annars nær reikningsfærsluferli viðskiptamannapöntunar ekki að bóka og notandi sölustaðar fær villuboð.</span><span class="sxs-lookup"><span data-stu-id="0fa6a-107">Otherwise, the customer order invoicing process can't post, and the POS user receives an error message.</span></span> <span data-ttu-id="0fa6a-108">Smásöluuppgjör fer þá í villustöðu.</span><span class="sxs-lookup"><span data-stu-id="0fa6a-108">Statement posting then goes into an error state.</span></span> <span data-ttu-id="0fa6a-109">Þessi villustaða kemur upp jafnvel eftir að kveikt hefur verið á neikvæðri birgðastöðu fyrir vörurnar.</span><span class="sxs-lookup"><span data-stu-id="0fa6a-109">This error state occurs even when negative inventory has been turned on for the products.</span></span>

<span data-ttu-id="0fa6a-110">Endurbætur sem gerðar hafa verið á Retail-útgáfu 10.0.4 og nýrri hjálpa til við að tryggja, þegar kveikt er á neikvæðri birgðastöðu fyrir runuraktar vörur, að ekki sé lokað fyrir reikningsfærslu viðskiptamannapöntunar og reikningsfærslu sölupöntunar í gegnum bókun á uppgjöri fyrir þessar vörur ef birgðir eru 0 (núll) eða rununúmer er ekki til staðar.</span><span class="sxs-lookup"><span data-stu-id="0fa6a-110">Improvements that have been made in Retail version 10.0.4 and later help guarantee that, when negative inventory is turned on for batch-tracked items, customer order invoicing and sales order invoicing through statement posting aren't blocked for those items if the inventory is 0 (zero) or a batch number isn't available.</span></span> <span data-ttu-id="0fa6a-111">Nýja virknin notar sjálfgefið runukenni fyrir sölulínur þegar rununúmer eru ekki í boði.</span><span class="sxs-lookup"><span data-stu-id="0fa6a-111">The new functionality uses a default batch ID for the sales lines when batch numbers aren't available.</span></span>

<span data-ttu-id="0fa6a-112">Til að skilgreina sjálfgefið runukenni sem notað er fyrir pantanir viðskiptamanna skal á síðunni **Viðskiptafæribreytur**, í flipanum **Pantanir viðskiptamanna**, í flýtiflipanum **Pöntun**, stilla reitinn **Sjálfgefið auðkenni runu**.</span><span class="sxs-lookup"><span data-stu-id="0fa6a-112">To define the default batch ID that is used for customer orders, on the **Commerce parameters** page, on the **Customer orders** tab, on the **Order** FastTab, set the **Default batch id** field.</span></span>

<span data-ttu-id="0fa6a-113">Til að skilgreina sjálfgefið runukenni sem notað er fyrir reikningsfærslu sölupöntunar í gegnum bókun á uppgjöri skal á síðunni **Viðskiptafæribreytur**, í flipanum **Bókun**, í flýtiflipanum **Birgðauppfærsla**, stilla reitinn **Sjálfgefið auðkenni runu**.</span><span class="sxs-lookup"><span data-stu-id="0fa6a-113">To define the default batch ID that is used for sales order invoicing through statement posting, on the **Commerce parameters** page, on the **Posting** tab, on the **Inventory update** FastTab, set the **Default batch id** field.</span></span>

> [!NOTE]
> <span data-ttu-id="0fa6a-114">Þessi virkni er aðeins í boði þegar kveikt er á ítarlegu vöruhúsakerfi fyrir tiltekna verslun, vöruhús og vörur.</span><span class="sxs-lookup"><span data-stu-id="0fa6a-114">This functionality is available only when advanced warehousing is turned on for the specific store warehouse and items.</span></span> <span data-ttu-id="0fa6a-115">Í seinni útgáfu verður virknin einnig studd fyrir aðstæður þar sem ítarlegt vöruhúsakerfi er ekki notað.</span><span class="sxs-lookup"><span data-stu-id="0fa6a-115">In a later release, the functionality will also be supported for scenarios where advanced warehouse management isn't used.</span></span>

> [!NOTE]
> <span data-ttu-id="0fa6a-116">Stuðningur við bætta meðhöndlun runuraktra vara við uppgjörsbókun fyrir sviðsmyndir vöruhúsakerfis sem ekki er ítarlegt var kynntur í Retail-útgáfu 10.0.5.</span><span class="sxs-lookup"><span data-stu-id="0fa6a-116">Support for improved handling of batch-tracked items during statement posting for non-advanced warehouse management scenarios was introduced in Retail version 10.0.5.</span></span>