---
title: Úthlutun og hnekking virðisaukaskatts
description: Þetta ferli sýnir hvernig á að úthluta VSK-flokkur á viðskiptarásir.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTaxOverrideCode, RetailTaxOverrideGroup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e8d7025db9dae57d04ee8b0f827cc13d659ad699
ms.sourcegitcommit: 34e543e807ac8790597f522fe3b4f0266cf4ee56
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/24/2020
ms.locfileid: "3161778"
---
# <a name="sales-tax-assignment-and-overrides"></a><span data-ttu-id="a0662-103">Úthlutun og hnekking virðisaukaskatts</span><span class="sxs-lookup"><span data-stu-id="a0662-103">Sales tax assignment and overrides</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a0662-104">Þetta ferli sýnir hvernig á að úthluta VSK-flokkur á viðskiptarásir.</span><span class="sxs-lookup"><span data-stu-id="a0662-104">This procedure demonstrates how to assign sales tax groups to commerce channels.</span></span> <span data-ttu-id="a0662-105">Hún á fer einnig í gegnum ferlið við að stofna nýja hnekking virðisaukaskatts og úthluta henni á fyrirliggjandi hnekkingarflokkur virðisaukaskatts.</span><span class="sxs-lookup"><span data-stu-id="a0662-105">It also walks through the process of creating a new sales tax override and assigning it to an existing sales tax override group.</span></span> <span data-ttu-id="a0662-106">Þetta ferli notar sýnigögn fyrirtæki USRT.</span><span class="sxs-lookup"><span data-stu-id="a0662-106">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="a0662-107">Fara í Retail og Commerce > Rásir > Verslanir > Allar verslanir.</span><span class="sxs-lookup"><span data-stu-id="a0662-107">Go to Retail and Commerce > Channels > Stores > All stores.</span></span>
2. <span data-ttu-id="a0662-108">Á listanum, smella á tengil fyrir kenni rásar fyrir „Houston”.</span><span class="sxs-lookup"><span data-stu-id="a0662-108">In the list, click the Channel ID link for "Houston."</span></span>
3. <span data-ttu-id="a0662-109">Smella á Breyta.</span><span class="sxs-lookup"><span data-stu-id="a0662-109">Click Edit.</span></span>
    * <span data-ttu-id="a0662-110">VSK-flokk reiturinn inniheldur lista yfir VSK-flokka fyrir núverandi fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="a0662-110">The "Sales tax group" field contains the list of sales tax groups for the current company.</span></span> <span data-ttu-id="a0662-111">Núverandi úthlutaður flokkur er almennur "Texas VSK-flokkur".</span><span class="sxs-lookup"><span data-stu-id="a0662-111">The currently assigned group is a generic "Texas" sales tax group.</span></span> <span data-ttu-id="a0662-112">Einnig eru til vsk-flokkar fyrir „Washington" og "Washington, King County.“</span><span class="sxs-lookup"><span data-stu-id="a0662-112">There are also sales tax groups for "Washington" and "Washington, King County."</span></span> <span data-ttu-id="a0662-113">Vsk-flokkar geta verið með viðeigandi skatta fyrir mörg sveitarfélög.</span><span class="sxs-lookup"><span data-stu-id="a0662-113">Sales tax groups can include applicable taxes for multiple municipalities.</span></span>  
    * <span data-ttu-id="a0662-114">Reiturinn "hnekking virðisaukaskatts" er þar sem hægt er að varpa hnekkingarflokka söluskatts á rásinni.</span><span class="sxs-lookup"><span data-stu-id="a0662-114">The "Sales tax override" field is where sales tax override groups can be mapped to the channel.</span></span> <span data-ttu-id="a0662-115">Hægt er að nota hnekkingarflokkur virðisaukaskatts til að flokka saman hnekkingar söluskatts sem starfa fyrir margar verslanir.</span><span class="sxs-lookup"><span data-stu-id="a0662-115">Sales tax override groups can be used to group together sales tax overrides that work for multiple stores.</span></span> <span data-ttu-id="a0662-116">Frekar en að úthluta handvirkt hnekkingum virðisaukaskatts einum í einum, er hægt að stofna flokkinn og úthluta beint á rásirnar til að spara tíma.</span><span class="sxs-lookup"><span data-stu-id="a0662-116">Rather than manually assigning sales tax overrides one by one, the group can be created and assigned directly to the channels to save time.</span></span>  
4. <span data-ttu-id="a0662-117">Smelltu á Vista.</span><span class="sxs-lookup"><span data-stu-id="a0662-117">Click Save.</span></span>
5. <span data-ttu-id="a0662-118">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="a0662-118">Close the page.</span></span>
6. <span data-ttu-id="a0662-119">Fara í Retail og Commerce > Uppsetning rásar > VSK > VSK hnekkja.</span><span class="sxs-lookup"><span data-stu-id="a0662-119">Go to Retail and Commerce > Channel setup > Sales taxes > Sales tax overrides.</span></span>
7. <span data-ttu-id="a0662-120">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="a0662-120">Click New.</span></span>
8. <span data-ttu-id="a0662-121">Í reitnum hnekking virðisaukaskatts, gefðu nafn fyrir nýju hnekkinguna þína.</span><span class="sxs-lookup"><span data-stu-id="a0662-121">In the Sales tax override field, provide a name for your new override.</span></span>
9. <span data-ttu-id="a0662-122">Í reitinn Lýsing er færð stutt lýsing á hnekkingunni.</span><span class="sxs-lookup"><span data-stu-id="a0662-122">In the Description field, provide a description of the override.</span></span>
10. <span data-ttu-id="a0662-123">Stilla stöðu á "Virkja".</span><span class="sxs-lookup"><span data-stu-id="a0662-123">Set the status to "Enable."</span></span>
11. <span data-ttu-id="a0662-124">Stækka eða fella saman hlutann Hnekkja.</span><span class="sxs-lookup"><span data-stu-id="a0662-124">Expand or collapse the Override section.</span></span>
12. <span data-ttu-id="a0662-125">Veljið valkost í svæðinu tegund.</span><span class="sxs-lookup"><span data-stu-id="a0662-125">In the Type field, select an option.</span></span>
    * <span data-ttu-id="a0662-126">Vsk-flokka vöru er hægt að nota til að hnekkja skatti fyrir tilteknar vörur sem tilheyrir þeim flokki.</span><span class="sxs-lookup"><span data-stu-id="a0662-126">Item sales tax groups can be used to override taxes for specific items that belong to the group.</span></span> <span data-ttu-id="a0662-127">T.d. er matvara yfirleitt skattlögð öðruvísi en efnislegar vörur og eru líklega með sinn eigin vsk-flokk.</span><span class="sxs-lookup"><span data-stu-id="a0662-127">For example, food items are typically taxed differently from hard goods, and would likely have their own sales tax group.</span></span> <span data-ttu-id="a0662-128">Vsk-flokkar eru flokkar skatta sem eiga við tiltekinni rás.</span><span class="sxs-lookup"><span data-stu-id="a0662-128">Sales tax groups are groups of taxes that are applicable to a particular channel.</span></span> <span data-ttu-id="a0662-129">Til dæmis ef rás selur bæði í smásölu og milli fyrirtækja, gætu mismunandi vsk-flokka verið notaðir.</span><span class="sxs-lookup"><span data-stu-id="a0662-129">For example, if a channel sells both retail and business-to-business, different items sales tax groups may be used.</span></span> <span data-ttu-id="a0662-130">Allar viðeigandi skatta myndi vera varpað á vsk-flokki.</span><span class="sxs-lookup"><span data-stu-id="a0662-130">All the applicable taxes would be mapped to the sales tax group.</span></span>  
    * <span data-ttu-id="a0662-131">Nú er hægt að velja á "Frá" og "Til" skatta eða "Frá skattflokki" og "Til skattflokks" til að stofna hnekkingu virðisaukaskatts.</span><span class="sxs-lookup"><span data-stu-id="a0662-131">Now you can select the "From" and "To" taxes or "From tax group" and "To tax group" to create your sales tax override.</span></span> <span data-ttu-id="a0662-132">"Frá" reiturinn tilgreinir skatta eða skattflokk sem á að hnekkja.</span><span class="sxs-lookup"><span data-stu-id="a0662-132">The "From" field indicates the tax or tax group to be overridden.</span></span> <span data-ttu-id="a0662-133">Hnekking samkvæmt VSK-flokkur vöru veitir aðra valkosti en hnekking eftir VSK-flokkur.</span><span class="sxs-lookup"><span data-stu-id="a0662-133">Overriding by Item sales tax group provides different options than overriding by sales tax group.</span></span> <span data-ttu-id="a0662-134">Hnekkingar virðisaukaskatts má setja upp til að hnekka sköttum á heilum færslum eða á tilteknum línum í færslu.</span><span class="sxs-lookup"><span data-stu-id="a0662-134">Sales tax overrides can be set up to override taxes on entire transactions or on particular lines in the transaction.</span></span>  
13. <span data-ttu-id="a0662-135">Smelltu á Vista.</span><span class="sxs-lookup"><span data-stu-id="a0662-135">Click Save.</span></span>
14. <span data-ttu-id="a0662-136">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="a0662-136">Close the page.</span></span>
15. <span data-ttu-id="a0662-137">Fara í Retail og Commerce > Uppsetning rásar > VSK > VSK hnekkja flokkar.</span><span class="sxs-lookup"><span data-stu-id="a0662-137">Go to Retail and Commerce > Channel setup > Sales taxes > Sales tax override groups.</span></span>
    * <span data-ttu-id="a0662-138">Í þessu skrefi muntu úthluta nýstofnuð hnekkingu vsk á hnekkingarflokkur virðisaukaskatts sem er úthlutað á Houston rásina.</span><span class="sxs-lookup"><span data-stu-id="a0662-138">In this step you will assigned the newly created sales tax override to the sales tax override group assigned to the Houston channel.</span></span>  
16. <span data-ttu-id="a0662-139">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="a0662-139">Click Edit.</span></span>
17. <span data-ttu-id="a0662-140">Útvíkka eða draga saman hlutann Setja upp.</span><span class="sxs-lookup"><span data-stu-id="a0662-140">Expand or collapse the Setup section.</span></span>
18. <span data-ttu-id="a0662-141">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="a0662-141">Click Add.</span></span>
19. <span data-ttu-id="a0662-142">Í reitnum hnekking virðisaukaskatts skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="a0662-142">In the Sales tax override field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="a0662-143">Veldu Hnekking virðisaukaskatts sem þú stofnaðir áður, úr listanum.</span><span class="sxs-lookup"><span data-stu-id="a0662-143">Select the previously created sales tax override from the list.</span></span>
21. <span data-ttu-id="a0662-144">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="a0662-144">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="a0662-145">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="a0662-145">Click Save.</span></span>

