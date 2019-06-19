---
title: Betri meðhöndlun á runuröktum vörum
description: Þetta efnisatriði lýsir endurbótum sem hafa verið gerðar á meðhöndlun á runum fyrir runuraktar vörur í bókunarferli smásöluuppgjörs.
author: josaw1
manager: AnnBe
ms.date: 05/28/2019
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
ms.openlocfilehash: 4456fc3d5bc4547fa8211642b11ca6df455fa187
ms.sourcegitcommit: aec1dcd44274e9b8d0770836598fde5533b7b569
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2019
ms.locfileid: "1617390"
---
# <a name="improved-handling-of-batch-tracked-items"></a><span data-ttu-id="f7a19-103">Betri meðhöndlun á runuröktum vörum</span><span class="sxs-lookup"><span data-stu-id="f7a19-103">Improved handling of batch-tracked items</span></span>

<span data-ttu-id="f7a19-104">Á sölustaðnum Microsoft Dynamics 365 for Retail er ekki hægt að sækja rununúmer fyrir runuraktar vörur þegar sala stendur yfir.</span><span class="sxs-lookup"><span data-stu-id="f7a19-104">In Microsoft Dynamics 365 for Retail Point of Sale (POS), batch numbers can't be captured for batch-tracked items at the time of sale.</span></span> <span data-ttu-id="f7a19-105">Hins vegar, fyrir ákveðnar skilgreiningar, þegar sölur eru bókaðar í höfuðstöðvunum í gegnum pantanir viðskiptamanns eða bókun á uppgjöri gerir Microsoft Dynamics-kerfið ráð fyrir því að gild rununúmer fyrir runuraktar vörur séu til staðar og að þau verði notuð í reikningsfærsluferlinu.</span><span class="sxs-lookup"><span data-stu-id="f7a19-105">However, for specific configurations, when sales are posted in the headquarters through customer orders or statement posting, the Microsoft Dynamics system expects that valid batch numbers for batch-tracked items exist, and that they will be used during the invoicing process.</span></span>

<span data-ttu-id="f7a19-106">Ef gild rununúmer eru í boði fyrir vörur eru þau notuð í reikningsfærsluferli viðskiptamannapöntunar og reikningsfærsluferli sölupöntunar úr bókun uppgjörs.</span><span class="sxs-lookup"><span data-stu-id="f7a19-106">If valid batch numbers are available for products, the customer order invoicing process and the sales order invoicing process from statement posting use them.</span></span> <span data-ttu-id="f7a19-107">Annars nær reikningsfærsluferli viðskiptamannapöntunar ekki að bóka og notandi sölustaðar fær villuboð.</span><span class="sxs-lookup"><span data-stu-id="f7a19-107">Otherwise, the customer order invoicing process can't post, and the POS user receives an error message.</span></span> <span data-ttu-id="f7a19-108">Smásöluuppgjör fer þá í villustöðu.</span><span class="sxs-lookup"><span data-stu-id="f7a19-108">Statement posting then goes into an error state.</span></span> <span data-ttu-id="f7a19-109">Þessi villustaða kemur upp jafnvel eftir að kveikt hefur verið á neikvæðri birgðastöðu fyrir vörurnar.</span><span class="sxs-lookup"><span data-stu-id="f7a19-109">This error state occurs even when negative inventory has been turned on for the products.</span></span>

<span data-ttu-id="f7a19-110">Endurbætur sem gerðar hafa verið á Microsoft Dynamics for Retail útgáfu 10.0.4 og nýrri hjálpa til við að tryggja, þegar kveikt er á neikvæðri birgðastöðu fyrir runuraktar vörur, að ekki sé lokað fyrir reikningsfærslu viðskiptamannapöntunar og reikningsfærslu sölupöntunar í gegnum bókun á uppgjöri fyrir þessar vörur ef birgðir eru 0 (núll) eða rununúmer er ekki til staðar.</span><span class="sxs-lookup"><span data-stu-id="f7a19-110">Improvements that have been made in Microsoft Dynamics for Retail version 10.0.4 and later help guarantee that, when negative inventory is turned on for batch-tracked items, customer order invoicing and sales order invoicing through statement posting aren't blocked for those items if the inventory is 0 (zero) or a batch number isn't available.</span></span> <span data-ttu-id="f7a19-111">Nýja virknin notar sjálfgefið runukenni fyrir sölulínur þegar rununúmer eru ekki í boði.</span><span class="sxs-lookup"><span data-stu-id="f7a19-111">The new functionality uses a default batch ID for the sales lines when batch numbers aren't available.</span></span>

<span data-ttu-id="f7a19-112">Til að skilgreina sjálfgefið runukenni sem notað er fyrir pantanir viðskiptamanna skal á síðunni **Smásölufæribreytur**, í flipanum **Pantanir viðskiptamanna**, í flýtiflipanum **Pöntun**, stilla reitinn **Sjálfgefið auðkenni runu**.</span><span class="sxs-lookup"><span data-stu-id="f7a19-112">To define the default batch ID that is used for customer orders, on the **Retail parameters** page, on the **Customer orders** tab, on the **Order** FastTab, set the **Default batch id** field.</span></span>

<span data-ttu-id="f7a19-113">Til að skilgreina sjálfgefið runukenni sem notað er fyrir reikningsfærslu sölupöntunar í gegnum bókun á uppgjöri skal á síðunni **Smásölufæribreytur**, í flipanum **Bókun**, í flýtiflipanum **Birgðauppfærsla**, stilla reitinn **Sjálfgefið auðkenni runu**.</span><span class="sxs-lookup"><span data-stu-id="f7a19-113">To define the default batch ID that is used for sales order invoicing through statement posting, on the **Retail parameters** page, on the **Posting** tab, on the **Inventory update** FastTab, set the **Default batch id** field.</span></span>

> [!NOTE]
> <span data-ttu-id="f7a19-114">Þessi virkni er aðeins í boði þegar kveikt er á ítarlegu vöruhúsakerfi fyrir tiltekna verslun, vöruhús og vörur.</span><span class="sxs-lookup"><span data-stu-id="f7a19-114">This functionality is available only when advanced warehousing is turned on for the specific store warehouse and items.</span></span> <span data-ttu-id="f7a19-115">Í seinni útgáfu verður virknin einnig studd fyrir aðstæður þar sem ítarlegt vöruhúsakerfi er ekki notað.</span><span class="sxs-lookup"><span data-stu-id="f7a19-115">In a later release, the functionality will also be supported for scenarios where advanced warehouse management isn't used.</span></span>
