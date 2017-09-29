---
title: "Setja upp samfelldniáætlanirnar fyrir símaver"
description: "Þessi grein lýsir hvernig setja á upp samfelldniáætlanirnar fyrir símaver."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 16081
ms.assetid: 426a9be7-a931-4780-b372-e06f6083dd60
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 00504b62237ac4f121d603d5144ffa4e71956cc3
ms.contentlocale: is-is
ms.lasthandoff: 08/29/2017

---

# <a name="set-up-a-continuity-program-for-a-call-center"></a><span data-ttu-id="2b1cf-103">Setja upp samfelldniáætlanirnar fyrir símaver</span><span class="sxs-lookup"><span data-stu-id="2b1cf-103">Set up a continuity program for a call center</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="2b1cf-104">Þessi grein lýsir hvernig setja á upp samfelldniáætlanirnar fyrir símaver.</span><span class="sxs-lookup"><span data-stu-id="2b1cf-104">This article describes how to set up a continuity program for a call center.</span></span>

<span data-ttu-id="2b1cf-105">Í samfelldniáætlun, sem er einnig þekkt sem forrit fyrir endurtekna pöntun, viðskiptavinir fá reglulegar vörusendingar samkvæmt fyrirfram ákveðinni áætlun.</span><span class="sxs-lookup"><span data-stu-id="2b1cf-105">In a continuity program, which is also known as a recurring order program, customers receive regular product shipments according to a predefined schedule.</span></span> <span data-ttu-id="2b1cf-106">Hver sending getur innihaldið aðra afurð og mál yfir bók-á-í-mánuður klúbbkort, eða hægt er að senda á sömu afurð margsinnis.</span><span class="sxs-lookup"><span data-stu-id="2b1cf-106">Each shipment can contain a different product, as in the case of a book-of-the-month club, or the same product can be sent repeatedly.</span></span> <span data-ttu-id="2b1cf-107">Til að skilgreina samfelldniáætlun þarf að ljúka eftirfarandi verkefnum:</span><span class="sxs-lookup"><span data-stu-id="2b1cf-107">To set up a continuity program, you must complete the following tasks.</span></span>

1.  <span data-ttu-id="2b1cf-108">Setja upp færibreytur samfelldni á síðunni **Færibreytur símavers**.</span><span class="sxs-lookup"><span data-stu-id="2b1cf-108">Set the continuity parameters on the **Call center parameters** page.</span></span>
2.  <span data-ttu-id="2b1cf-109">Stofnaðu samfelluforrit sem skilgreinir upplýsingar, svo sem greiðsluáætlun, tímasetningu sendingar, og hvort greitt er upp að framan.</span><span class="sxs-lookup"><span data-stu-id="2b1cf-109">Create a continuity program that specifies details such as the payment schedule, the timing of the shipments, and whether billing is up front.</span></span> <span data-ttu-id="2b1cf-110">Einnig verður að bæta við lista yfir afurðir sem eru innifaldar í samfelldniáætlanirnar.</span><span class="sxs-lookup"><span data-stu-id="2b1cf-110">You must also add a list of products that are included in the continuity program.</span></span> <span data-ttu-id="2b1cf-111">Hver afurð fær kennisnúmer tilviks sem er úthlutað í röð og byrjar á 1.</span><span class="sxs-lookup"><span data-stu-id="2b1cf-111">Each product receives an event ID number that is assigned sequentially, beginning with 1.</span></span> <span data-ttu-id="2b1cf-112">Kenni tilviks ákvarðar röðina sem afurðir eru sendar í.</span><span class="sxs-lookup"><span data-stu-id="2b1cf-112">The event IDs determine the order that products are sent in.</span></span>
    -   <span data-ttu-id="2b1cf-113">Þegar viðskiptavinir fá mismunandi afurð í hverri sendingu eru afurðirnar sendar raðbundið, samkvæmt tilvikskennum þeirra og ni tilviks frá og hefjast á núgildandi tilviki.</span><span class="sxs-lookup"><span data-stu-id="2b1cf-113">If customers receive a different product in each shipment, the products are sent in sequential order, based on their event IDs and beginning with the current event.</span></span>
    -   <span data-ttu-id="2b1cf-114">Ef viðskiptavinir fá sömu afurð í hverri sendingu inniheldur listinn einungis eina afurð sem hefur eitt tilvikskenni.</span><span class="sxs-lookup"><span data-stu-id="2b1cf-114">If customers receive the same product in each shipment, the list contains only one product that has one event ID.</span></span> <span data-ttu-id="2b1cf-115">Sama atvikið kemur endurtekið upp.</span><span class="sxs-lookup"><span data-stu-id="2b1cf-115">The same event occurs repeatedly.</span></span> <span data-ttu-id="2b1cf-116">Hægt er að tilgreina hversu oft á að endurtaka öll tilvik.</span><span class="sxs-lookup"><span data-stu-id="2b1cf-116">You can specify how many times each event is repeated.</span></span>

3.  <span data-ttu-id="2b1cf-117">Stofnaðu yfirafurð sem endurspeglar samfelluforritið sem þú bjóst til í verki 2.</span><span class="sxs-lookup"><span data-stu-id="2b1cf-117">Create a parent product that represents the continuity program that you created in task 2.</span></span> <span data-ttu-id="2b1cf-118">Ef þessar afurð er bætt við sölupöntun opnast síðan **Samfelldni**.</span><span class="sxs-lookup"><span data-stu-id="2b1cf-118">If you add this product to a sales order, the **Continuity** page opens.</span></span> <span data-ttu-id="2b1cf-119">Síðan er hægt að nota þá síðu til að stofna samfelldnipöntunina sjálfa.</span><span class="sxs-lookup"><span data-stu-id="2b1cf-119">You can then use that page to create the actual continuity order.</span></span> <span data-ttu-id="2b1cf-120">Yfirstig afurða tilgreinir ekki stakar afurðir sem viðskiptavinur fær í hverri sendingu.</span><span class="sxs-lookup"><span data-stu-id="2b1cf-120">The parent product doesn't specify the individual products that the customer receives in each shipment.</span></span>

<span data-ttu-id="2b1cf-121">Eftir að þú hefur sett upp samfelluforrit eins og lýst er hér að ofan, getur þú stofnað samfellupöntun fyrir viðskiptavin.</span><span class="sxs-lookup"><span data-stu-id="2b1cf-121">After you've set up a continuity program as described above, you can create a continuity order for a customer.</span></span> <span data-ttu-id="2b1cf-122">Einnig gæti þurft að framkvæma eftirfarandi verk viðbótar viðhalds:</span><span class="sxs-lookup"><span data-stu-id="2b1cf-122">You might also have to perform the following additional maintenance tasks.</span></span>

-   <span data-ttu-id="2b1cf-123">**Uppfæra núverandi tilvikstímabil samfelldni** – Setja upp runuvinnslu sem segir kerfinu hvert núverandi tilvikstímabilið er.</span><span class="sxs-lookup"><span data-stu-id="2b1cf-123">**Update the current continuity event period** – Set up a batch job that tells the system what the current event period is.</span></span>
-   <span data-ttu-id="2b1cf-124">**Stofna samfelldniundirpantanir** - Stofna undirpantanir úr yfirstigi samfelldnipöntunar.</span><span class="sxs-lookup"><span data-stu-id="2b1cf-124">**Create continuity child orders** – Create child orders from the parent continuity order.</span></span>
-   <span data-ttu-id="2b1cf-125">**Vinna samfelldnigreiðslur** – Vinna reikningsfærslu og tilkynningar fyrir greiðslur sem eru tengdar samfelldnisölupöntunum.</span><span class="sxs-lookup"><span data-stu-id="2b1cf-125">**Process continuity payments** – Process billing and notifications for payments that are associated with continuity sales orders.</span></span>
-   <span data-ttu-id="2b1cf-126">**Útvíkka samfelldnilínur (Ef þarf)** - Lengja fjölda skipta sem hægt er að endurtaka samfelldnitilvik.</span><span class="sxs-lookup"><span data-stu-id="2b1cf-126">**Extend continuity lines** (if required) – Extend the number of times that a continuity event can be repeated.</span></span> <span data-ttu-id="2b1cf-127">Endurtekning sendinga er síðan hægt að útvíkka umfram mörk sem voru sett í reitinn **Viðmiðunarmörk á endurtekinni samfelldni** í færibreytum símavers.</span><span class="sxs-lookup"><span data-stu-id="2b1cf-127">The repetition of shipments can then extend beyond the limit that was set in the **Continuity repeat threshold** field in the call center parameters.</span></span>
-   <span data-ttu-id="2b1cf-128">**Framkvæma samfelldniuppfærslu** (ef þarf) - Samstilltu breytingar milli samfelldniáætlunarinnar og samfelldni yfirsölupöntunar.</span><span class="sxs-lookup"><span data-stu-id="2b1cf-128">**Perform a continuity update** (if required) – Synchronize changes between the continuity program and the continuity parent sales orders.</span></span>
-   <span data-ttu-id="2b1cf-129">**Loka samfelldnisyfirlínum og -pöntunum** - Loka pöntunum.</span><span class="sxs-lookup"><span data-stu-id="2b1cf-129">**Close continuity parent lines and orders** – Close continuity orders.</span></span>





