--- 
title: "Úthlutun og hnekking virðisaukaskatts"
description: "Þetta ferli sýnir hvernig á að úthluta VSK-flokkur á smásölurásir."
author: mkirknel
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 8b3dc0beec17d80f7bbbcf234656a537a445789f
ms.contentlocale: is-is
ms.lasthandoff: 04/13/2018

---
# <a name="sales-tax-assignment-and-overrides"></a><span data-ttu-id="2b273-103">Úthlutun og hnekking virðisaukaskatts</span><span class="sxs-lookup"><span data-stu-id="2b273-103">Sales tax assignment and overrides</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2b273-104">Þetta ferli sýnir hvernig á að úthluta VSK-flokkur á smásölurásir.</span><span class="sxs-lookup"><span data-stu-id="2b273-104">This procedure demonstrates how to assign sales tax groups to retail channels.</span></span> <span data-ttu-id="2b273-105">Hún á fer einnig í gegnum ferlið við að stofna nýja hnekking virðisaukaskatts og úthluta henni á fyrirliggjandi hnekkingarflokkur virðisaukaskatts.</span><span class="sxs-lookup"><span data-stu-id="2b273-105">It also walks through the process of creating a new sales tax override and assigning it to an existing sales tax override group.</span></span> <span data-ttu-id="2b273-106">Þetta ferli</span><span class="sxs-lookup"><span data-stu-id="2b273-106">This procedure</span></span>

<span data-ttu-id="2b273-107">notar fyrirtæki USRT sem sýnigögn.</span><span class="sxs-lookup"><span data-stu-id="2b273-107">uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="2b273-108">Fara í Smásölu og viðskipti > rásir > smásöluverslanir > allar smásöluverslanir.</span><span class="sxs-lookup"><span data-stu-id="2b273-108">Go to Retail and commerce > Channels > Retail stores > All retail stores.</span></span>
2. <span data-ttu-id="2b273-109">Á listanum, smella á tengil fyrir kenni smásölurásar fyrir "Houston."</span><span class="sxs-lookup"><span data-stu-id="2b273-109">In the list, click the Retail Channel ID link for "Houston."</span></span>
3. <span data-ttu-id="2b273-110">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="2b273-110">Click Edit.</span></span>
    * <span data-ttu-id="2b273-111">VSK-flokk reiturinn inniheldur lista yfir VSK-flokka fyrir núverandi fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="2b273-111">The "Sales tax group" field contains the list of sales tax groups for the current company.</span></span> <span data-ttu-id="2b273-112">Núverandi úthlutaður flokkur er almennur "Texas VSK-flokkur".</span><span class="sxs-lookup"><span data-stu-id="2b273-112">The currently assigned group is a generic "Texas" sales tax group.</span></span> <span data-ttu-id="2b273-113">Einnig eru til vsk-flokkar fyrir „Washington" og "Washington, King County.“</span><span class="sxs-lookup"><span data-stu-id="2b273-113">There are also sales tax groups for "Washington" and "Washington, King County."</span></span> <span data-ttu-id="2b273-114">Vsk-flokkar geta verið með viðeigandi skatta fyrir mörg sveitarfélög.</span><span class="sxs-lookup"><span data-stu-id="2b273-114">Sales tax groups can include applicable taxes for multiple municipalities.</span></span>  
    * <span data-ttu-id="2b273-115">Reiturinn "hnekking virðisaukaskatts" er þar sem hægt er að varpa hnekkingarflokka söluskatts á rásinni.</span><span class="sxs-lookup"><span data-stu-id="2b273-115">The "Sales tax override" field is where sales tax override groups can be mapped to the channel.</span></span> <span data-ttu-id="2b273-116">Hægt er að nota hnekkingarflokkur virðisaukaskatts til að flokka saman hnekkingar söluskatts sem starfa fyrir margar verslanir.</span><span class="sxs-lookup"><span data-stu-id="2b273-116">Sales tax override groups can be used to group together sales tax overrides that work for multiple stores.</span></span> <span data-ttu-id="2b273-117">Frekar en að úthluta handvirkt hnekkingum virðisaukaskatts einum í einum, er hægt að stofna flokkinn og úthluta beint á rásirnar til að spara tíma.</span><span class="sxs-lookup"><span data-stu-id="2b273-117">Rather than manually assigning sales tax overrides one by one, the group can be created and assigned directly to the channels to save time.</span></span>  
4. <span data-ttu-id="2b273-118">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="2b273-118">Click Save.</span></span>
5. <span data-ttu-id="2b273-119">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="2b273-119">Close the page.</span></span>
6. <span data-ttu-id="2b273-120">Fara í Smásala og viðskipti > Uppsetning rásar > VSK > VSK hnekkja.</span><span class="sxs-lookup"><span data-stu-id="2b273-120">Go to Retail and commerce > Channel setup > Sales taxes > Sales tax overrides.</span></span>
7. <span data-ttu-id="2b273-121">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="2b273-121">Click New.</span></span>
8. <span data-ttu-id="2b273-122">Í reitnum hnekking virðisaukaskatts, gefðu nafn fyrir nýju hnekkinguna þína.</span><span class="sxs-lookup"><span data-stu-id="2b273-122">In the Sales tax override field, provide a name for your new override.</span></span>
9. <span data-ttu-id="2b273-123">Í reitinn Lýsing er færð stutt lýsing á hnekkingunni.</span><span class="sxs-lookup"><span data-stu-id="2b273-123">In the Description field, provide a description of the override.</span></span>
10. <span data-ttu-id="2b273-124">Stilla stöðu á "Virkja".</span><span class="sxs-lookup"><span data-stu-id="2b273-124">Set the status to "Enable."</span></span>
11. <span data-ttu-id="2b273-125">Stækka eða fella saman hlutann Hnekkja.</span><span class="sxs-lookup"><span data-stu-id="2b273-125">Expand or collapse the Override section.</span></span>
12. <span data-ttu-id="2b273-126">Veljið valkost í svæðinu tegund.</span><span class="sxs-lookup"><span data-stu-id="2b273-126">In the Type field, select an option.</span></span>
    * <span data-ttu-id="2b273-127">Vsk-flokka vöru er hægt að nota til að hnekkja skatti fyrir tilteknar vörur sem tilheyrir þeim flokki.</span><span class="sxs-lookup"><span data-stu-id="2b273-127">Item sales tax groups can be used to override taxes for specific items that belong to the group.</span></span> <span data-ttu-id="2b273-128">T.d. er matvara yfirleitt skattlögð öðruvísi en efnislegar vörur og eru líklega með sinn eigin vsk-flokk.</span><span class="sxs-lookup"><span data-stu-id="2b273-128">For example, food items are typically taxed differently from hard goods, and would likely have their own sales tax group.</span></span>     <span data-ttu-id="2b273-129">Vsk-flokkar eru flokkar skatta sem eiga við tiltekinni rás.</span><span class="sxs-lookup"><span data-stu-id="2b273-129">Sales tax groups are groups of taxes that are applicable to a particular channel.</span></span> <span data-ttu-id="2b273-130">Til dæmis ef rás selur bæði í smásölu og milli fyrirtækja, gætu mismunandi vsk-flokka verið notaðir.</span><span class="sxs-lookup"><span data-stu-id="2b273-130">For example, if a channel sells both retail and business-to-business, different items sales tax groups may be used.</span></span> <span data-ttu-id="2b273-131">Allar viðeigandi skatta myndi vera varpað á vsk-flokki.</span><span class="sxs-lookup"><span data-stu-id="2b273-131">All the applicable taxes would be mapped to the sales tax group.</span></span>  
    * <span data-ttu-id="2b273-132">Nú er hægt að velja á "Frá" og "Til" skatta eða "Frá skattflokki" og "Til skattflokks" til að stofna hnekkingu virðisaukaskatts.</span><span class="sxs-lookup"><span data-stu-id="2b273-132">Now you can select the "From" and "To" taxes or "From tax group" and "To tax group" to create your sales tax override.</span></span>    <span data-ttu-id="2b273-133">"Frá" reiturinn tilgreinir skatta eða skattflokk sem á að hnekkja.</span><span class="sxs-lookup"><span data-stu-id="2b273-133">The "From" field indicates the tax or tax group to be overridden.</span></span> <span data-ttu-id="2b273-134">Hnekking samkvæmt VSK-flokkur vöru veitir aðra valkosti en hnekking eftir VSK-flokkur.</span><span class="sxs-lookup"><span data-stu-id="2b273-134">Overriding by Item sales tax group provides different options than overriding by sales tax group.</span></span>    <span data-ttu-id="2b273-135">Hnekkingar virðisaukaskatts má setja upp til að hnekka sköttum á heilum færslum eða á tilteknum línum í færslu.</span><span class="sxs-lookup"><span data-stu-id="2b273-135">Sales tax overrides can be set up to override taxes on entire transactions or on particular lines in the transaction.</span></span>  
13. <span data-ttu-id="2b273-136">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="2b273-136">Click Save.</span></span>
14. <span data-ttu-id="2b273-137">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="2b273-137">Close the page.</span></span>
15. <span data-ttu-id="2b273-138">Fara í Smásala og viðskipti > Uppsetning rásar > VSK > VSK hnekkja flokkar.</span><span class="sxs-lookup"><span data-stu-id="2b273-138">Go to Retail and commerce > Channel setup > Sales taxes > Sales tax override groups.</span></span>
    * <span data-ttu-id="2b273-139">Í þessu skrefi muntu úthluta nýstofnuð hnekkingu vsk á hnekkingarflokkur virðisaukaskatts sem er úthlutað á Houston rásina.</span><span class="sxs-lookup"><span data-stu-id="2b273-139">In this step you will assigned the newly created sales tax override to the sales tax override group assigned to the Houston channel.</span></span>  
16. <span data-ttu-id="2b273-140">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="2b273-140">Click Edit.</span></span>
17. <span data-ttu-id="2b273-141">Útvíkka eða draga saman hlutann Setja upp.</span><span class="sxs-lookup"><span data-stu-id="2b273-141">Expand or collapse the Setup section.</span></span>
18. <span data-ttu-id="2b273-142">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="2b273-142">Click Add.</span></span>
19. <span data-ttu-id="2b273-143">Í reitnum hnekking virðisaukaskatts skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="2b273-143">In the Sales tax override field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="2b273-144">Veldu Hnekking virðisaukaskatts sem þú stofnaðir áður, úr listanum.</span><span class="sxs-lookup"><span data-stu-id="2b273-144">Select the previously created sales tax override from the list.</span></span>
21. <span data-ttu-id="2b273-145">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="2b273-145">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="2b273-146">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="2b273-146">Click Save.</span></span>


