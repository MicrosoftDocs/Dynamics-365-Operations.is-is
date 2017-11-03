---
title: "Virkni símavers"
description: "Þessi grein veitir yfirlit yfir söluvirkni símavera í Microsoft Dynamics 365 for Retail."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16361
ms.assetid: c8ed2ba4-8d06-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 2c58f71230a0781ee957632b453ced86ca03b15a
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="call-center-functionality"></a><span data-ttu-id="9a5bb-103">Símaversvirkni</span><span class="sxs-lookup"><span data-stu-id="9a5bb-103">Call center functionality</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="9a5bb-104">Þessi grein veitir yfirlit yfir söluvirkni símavera í Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="9a5bb-104">This article provides an overview of the call center sales functionality in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="9a5bb-105">Dynamics 365 for Retail styður einnig símaver sem gerð af smásölurás.</span><span class="sxs-lookup"><span data-stu-id="9a5bb-105">Dynamics 365 for Retail supports call centers as a type of retail channel.</span></span> <span data-ttu-id="9a5bb-106">Í símaveri taka starfskraftar við pöntunum viðskiptavina í gegnum síma og búa til sölupantanir.</span><span class="sxs-lookup"><span data-stu-id="9a5bb-106">In a call center, workers take orders from customers over the phone and create sales orders.</span></span> <span data-ttu-id="9a5bb-107">Virkni símavers inniheldur aðgerðir sem eru hannaðar til að auðvelda símapantanir og afgreiða þjónustu við viðskiptavin í gegnum ferlið uppfyllingu pöntunar.</span><span class="sxs-lookup"><span data-stu-id="9a5bb-107">Call center functionality includes features that are designed to make it easier to take phone orders and handle customer service throughout the order fulfillment process.</span></span> <span data-ttu-id="9a5bb-108">Til dæmis, starfsmenn símavers geta slegið inn greiðsluupplýsingar beint í sölupöntun, og geta skoðað ítarlegt yfirlit yfir gjöld og greiðslur áður en þeir senda pöntunina.</span><span class="sxs-lookup"><span data-stu-id="9a5bb-108">For example, call center workers can enter payment information directly into the sales order, and can view a detailed summary of charges and payments before they submit the order.</span></span> <span data-ttu-id="9a5bb-109">Starfsmenn hafa val á að stýra verðlagningu og geta fengið aðgang að ýmsum gögnum um viðskiptavini, vörur og verð úr síðunni **sölupöntun**.</span><span class="sxs-lookup"><span data-stu-id="9a5bb-109">Workers also have options for controlling pricing, and can access various data about customers, products, and prices from the **Sales order** page.</span></span> <span data-ttu-id="9a5bb-110">Þar að auka hafa Símaver einnig ítarlegri aðgerðir til að rekja sögu og pöntunarstöðu viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="9a5bb-110">Additionally, call centers have enhanced functionality for tracking customer history and order status.</span></span> <span data-ttu-id="9a5bb-111">Hvert símaver getur haft eigin notendur, greiðsluhætti, verðflokkar, fjárhagsvíddir og afhendingarmáta.</span><span class="sxs-lookup"><span data-stu-id="9a5bb-111">Each call center can have its own users, payment methods, price groups, financial dimensions, and modes of delivery.</span></span> <span data-ttu-id="9a5bb-112">Hægt er að skilgreina valkosti þegar símaver er stofnað.</span><span class="sxs-lookup"><span data-stu-id="9a5bb-112">You can configure these options when you create the call center.</span></span> <span data-ttu-id="9a5bb-113">Þar að auki geturðu notað Síðuna **símaver** til að kveikja eða slökkva á eiginleikaflokkum sem eru sértækir fyrir símaver.</span><span class="sxs-lookup"><span data-stu-id="9a5bb-113">Additionally, you can use the **Call center** page to enable or disable the following groups of features that are unique to call centers:</span></span>

-   <span data-ttu-id="9a5bb-114">**Lok pöntunar**– Þessi flokkur inniheldur eiginleika sem tengjast greiðslum og lokum pöntunar í síðunni **sölupöntun**.</span><span class="sxs-lookup"><span data-stu-id="9a5bb-114">**Order completion** – This group includes features that are related to payments and order completion on the **Sales order** page.</span></span>
-   <span data-ttu-id="9a5bb-115">**Beind sala**– Þessi flokkur inniheldur aðgerðir sem tengjast frumkóðum, forskriftum og beiðnum um vörulista.</span><span class="sxs-lookup"><span data-stu-id="9a5bb-115">**Directed selling** – This group includes features that are related to source codes, scripts, and catalog requests.</span></span>

<span data-ttu-id="9a5bb-116">Þegar þessir eiginleikar í stillingum símavers eru virkjaðar, eru þær tiltækar á síðunni **sölupöntun** fyrir notendur sem eru tengdir við símaverið.</span><span class="sxs-lookup"><span data-stu-id="9a5bb-116">After you enable these features in the call center settings, they are available on the **Sales order** page to users who are associated with the call center.</span></span> <span data-ttu-id="9a5bb-117">Flestar þessara aðgerða krefjast frekari uppsetningar áður en hægt er að nota þær.</span><span class="sxs-lookup"><span data-stu-id="9a5bb-117">Most of these features require additional setup before they can be used.</span></span> <span data-ttu-id="9a5bb-118">Áður en notendur geta stofnað pantanir símavers, verður að bæta þessum notendum við símaver sem símaversnotendum.</span><span class="sxs-lookup"><span data-stu-id="9a5bb-118">Before users can create call center orders, you must add those users to the call center as call center users.</span></span> <span data-ttu-id="9a5bb-119">Þetta virkjar skilgreiningu og virkni símavers sem er tengd rásum.</span><span class="sxs-lookup"><span data-stu-id="9a5bb-119">This step enables the call center channel-specific configuration and functionality.</span></span> <span data-ttu-id="9a5bb-120">Hér eru nokkur dæmi um aðgerðir sem verður tiltæk:</span><span class="sxs-lookup"><span data-stu-id="9a5bb-120">Here are some examples of the functionality that becomes available:</span></span>

-   <span data-ttu-id="9a5bb-121">Leiðbeind sala veitir skilgreiningarvalkosti fyrir símasöluhandrit og myndir af vörum til að hjálpa og leiðbeina sölufólki á meðan það tekur pantanir.</span><span class="sxs-lookup"><span data-stu-id="9a5bb-121">Guided selling provides configuration options for telesales scripts and product images to help and guide sales clerks while they take orders.</span></span>
-   <span data-ttu-id="9a5bb-122">Ekki er hægt að ljúka pöntunum þar til sölufólk hefur sótt að minnsta kosti sótt einn greiðslumáta.</span><span class="sxs-lookup"><span data-stu-id="9a5bb-122">Orders can't be completed until sales clerks have captured at least one payment method.</span></span>
-   <span data-ttu-id="9a5bb-123">Viðbótarsölu- eða krosssölureglur er hægt að skilgreina til að biðja sölufólk um að kynna tilteknar vörur fyrir viðskiptavininum.</span><span class="sxs-lookup"><span data-stu-id="9a5bb-123">Upsell and cross-sell rules can be configured to prompt sales clerks to promote specific products to the customer.</span></span>
-   <span data-ttu-id="9a5bb-124">Sölufólk getur sótt upprunakóðana fyrir vörulistana sem viðskiptavinurinn er að panta úr.</span><span class="sxs-lookup"><span data-stu-id="9a5bb-124">Sales clerks can capture the source code for the catalog that a customer is ordering from.</span></span>
-   <span data-ttu-id="9a5bb-125">Sölufólk getur bætt afsláttarmiða smásala við pöntunina.</span><span class="sxs-lookup"><span data-stu-id="9a5bb-125">Sales clerks can add a retailer's coupons to the order.</span></span>
-   <span data-ttu-id="9a5bb-126">Sölufólk getur selja samfelldniáætlanir.</span><span class="sxs-lookup"><span data-stu-id="9a5bb-126">Sales clerks can sell continuity programs.</span></span>
-   <span data-ttu-id="9a5bb-127">Pantanirnar geta verið sett í bið handvirkt eða sjálfvirkt, til að tilgreina að frekari athugunar er krafist áður en hægt er að vinna pöntunina.</span><span class="sxs-lookup"><span data-stu-id="9a5bb-127">Orders can be put on hold manually or automatically, to indicate that additional investigation is required before the order can be processed.</span></span>





