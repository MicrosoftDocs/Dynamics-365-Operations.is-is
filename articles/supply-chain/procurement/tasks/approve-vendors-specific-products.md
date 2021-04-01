---
title: Samþykkja lánardrottna fyrir tilteknar afurðir
description: Þessi verklýsing sýnir hvernig á að samþykkja lánardrottna fyrir tilteknar vörur.
author: RichardLuan
manager: tfehr
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, PdsApprovedVendorList, VendTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d08791caba34908903ce330df0f91e44fbdfcaea
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5237276"
---
# <a name="approve-vendors-for-specific-products"></a><span data-ttu-id="54281-103">Samþykkja lánardrottna fyrir tilteknar afurðir</span><span class="sxs-lookup"><span data-stu-id="54281-103">Approve vendors for specific products</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="54281-104">Þessi verklýsing sýnir hvernig á að samþykkja lánardrottna fyrir tilteknar vörur.</span><span class="sxs-lookup"><span data-stu-id="54281-104">This procedure shows you how to approve vendors for specific products.</span></span> <span data-ttu-id="54281-105">Þetta gerir kleift að stýra hvaða lánardrottna er hægt að nota þegar vöru er bætt við innkaupapöntun.</span><span class="sxs-lookup"><span data-stu-id="54281-105">This allows you to control which vendors can be used when the product is added to a purchase order.</span></span> <span data-ttu-id="54281-106">Þú getur farið í gegnum þetta ferli í sýnigögn fyrirtækisins USMF eða með því að nota eigin gögn.</span><span class="sxs-lookup"><span data-stu-id="54281-106">You can use this procedure in demo data company USMF, or on your own data.</span></span> <span data-ttu-id="54281-107">Þetta verk myndi venjulega vera framkvæmt af innkaupaaðila.</span><span class="sxs-lookup"><span data-stu-id="54281-107">This task would typically be carried out by a Purchasing manager.</span></span>

1. <span data-ttu-id="54281-108">Í skoðunarrúðunni ferðu í **Kerfiseiningar > Afurðaupplýsingastjórnun > Afurðir > Útgefnar afurðir**.</span><span class="sxs-lookup"><span data-stu-id="54281-108">In Navigation Pane, go to **Modules > Product information management > Products > Released products**.</span></span>
2. <span data-ttu-id="54281-109">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="54281-109">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="54281-110">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="54281-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="54281-111">Útvíkka **Innkaup** flýtiflipa.</span><span class="sxs-lookup"><span data-stu-id="54281-111">Expand the **Purchase** fastTab.</span></span> <span data-ttu-id="54281-112">Ef aðallánardrottinn er sýnt í svæði **Lánardrottna**, þá þarf að bæta þessi lánardrottinn við sem samþykktan lánardrottinn í eftirfarandi skrefum.</span><span class="sxs-lookup"><span data-stu-id="54281-112">If there is a primary vendor shown in the **Vendor** field, then you need to add this vendor as an approved vendor in the following steps.</span></span> <span data-ttu-id="54281-113">Skráið númer lánardrottins, ef það er sýnt.</span><span class="sxs-lookup"><span data-stu-id="54281-113">Make a note of the vendor number, if one is shown.</span></span>  
5. <span data-ttu-id="54281-114">Í aðgerðasvæðinu skal smella á **Innkaup**.</span><span class="sxs-lookup"><span data-stu-id="54281-114">On the Action Pane, click **Purchase**.</span></span>
6. <span data-ttu-id="54281-115">**Smellt er á Uppsetningu.**</span><span class="sxs-lookup"><span data-stu-id="54281-115">Click **Setup**.</span></span>
7. <span data-ttu-id="54281-116">Smelltu á **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="54281-116">Click **Add**.</span></span>
8. <span data-ttu-id="54281-117">Færa inn eða veljið gildi í svæðinu lánardrottinn.</span><span class="sxs-lookup"><span data-stu-id="54281-117">In the Vendor field, enter or select a value.</span></span> <span data-ttu-id="54281-118">Veljið samþykktan lánardrottin.</span><span class="sxs-lookup"><span data-stu-id="54281-118">Select the approved vendor.</span></span> <span data-ttu-id="54281-119">Minnst ein línanna verður að vera aðallánardrottinn ef það var einn slíkur í afurðarfærslu.</span><span class="sxs-lookup"><span data-stu-id="54281-119">At least one of the lines has to be the primary vendor if there was one in the product record.</span></span> <span data-ttu-id="54281-120">Ef þú tókst niður númer lánardrottins áður, er það valið hér.</span><span class="sxs-lookup"><span data-stu-id="54281-120">If you made a note of the vendor number earlier, select it here.</span></span>  
9. <span data-ttu-id="54281-121">**Í reitinn lokadagsetning, skal færa inn dagsetningu.**</span><span class="sxs-lookup"><span data-stu-id="54281-121">In the **Expiration** field, enter a date.</span></span> <span data-ttu-id="54281-122">Velja dagsetningu sem er nokkra mánuði fram í tímann.</span><span class="sxs-lookup"><span data-stu-id="54281-122">Choose a date a that is a few months ahead.</span></span>  
10. <span data-ttu-id="54281-123">Smelltu á **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="54281-123">Click **Add**.</span></span>
11. <span data-ttu-id="54281-124">**Færa inn eða veljið gildi í svæðinu lánardrottinn.**</span><span class="sxs-lookup"><span data-stu-id="54281-124">In the **Vendor** field, enter or select a value.</span></span>
12. <span data-ttu-id="54281-125">**Í reitinn lokadagsetning, skal færa inn dagsetningu.**</span><span class="sxs-lookup"><span data-stu-id="54281-125">In the **Expiration** field, enter a date.</span></span> <span data-ttu-id="54281-126">Veljið dagsetningu sem er annað en fyrri lokadagsetningu.</span><span class="sxs-lookup"><span data-stu-id="54281-126">Choose a date that is different than the previous expiration date.</span></span>  
13. <span data-ttu-id="54281-127">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="54281-127">Close the page.</span></span>
14. <span data-ttu-id="54281-128">Á aðgerðasvæðinu er smellt á **Samþykktir lánardrottnar**.</span><span class="sxs-lookup"><span data-stu-id="54281-128">On the Action Pane, click **Approved vendors**.</span></span>
15. <span data-ttu-id="54281-129">**Í reitinn lokadagsetning, skal færa inn dagsetningu.**</span><span class="sxs-lookup"><span data-stu-id="54281-129">In the **Expiration** field, enter a date.</span></span> <span data-ttu-id="54281-130">Þessi dagsetning virkar eins og sía þannig að hægt er að hverjir eru samþykkta lánardrottna, fram að tilteknum degi.</span><span class="sxs-lookup"><span data-stu-id="54281-130">This date acts as a filter so you can see who the approved vendors are, up to a certain date.</span></span>  
16. <span data-ttu-id="54281-131">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="54281-131">Close the page.</span></span>
17. <span data-ttu-id="54281-132">Á aðgerðasvæðinu er smellt á **Gildistímabil**.</span><span class="sxs-lookup"><span data-stu-id="54281-132">On the Action Pane, click **Effective period**.</span></span>
18. <span data-ttu-id="54281-133">**Í reitinn sýna lánardrottna sem renna út samkvæmt, skal færa inn dagsetningu.**</span><span class="sxs-lookup"><span data-stu-id="54281-133">In the **Show vendors expired by** field, enter a date.</span></span> <span data-ttu-id="54281-134">Nota þessa síðu til að auðkenna lánardrottnum þar sem staða samþykkis rennur út eftir tiltekna dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="54281-134">You can use this page to identify vendors where the approval status will expire after a certain date.</span></span>  
19. <span data-ttu-id="54281-135">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="54281-135">Close the page.</span></span>
20. <span data-ttu-id="54281-136">Smellið á **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="54281-136">Click **Edit**.</span></span>
21. <span data-ttu-id="54281-137">**Veljið valkost í svæðinu athugunaraðferð samþykkts Lánardrottins.**</span><span class="sxs-lookup"><span data-stu-id="54281-137">In the **Approved vendor check method** field, select an option.</span></span> <span data-ttu-id="54281-138">Þetta svæði leyfir þér að velja reglu fyrir það hvað skuli gerast ef vöru er bætt við innkaupapöntunarlínu þar sem lánardrottinn er ekki samþykktur lánardrottinn.</span><span class="sxs-lookup"><span data-stu-id="54281-138">This field allows you to select the policy for what should happen if the product is added to a purchase order line where the vendor is not an approved vendor.</span></span>  
22. <span data-ttu-id="54281-139">Smellt er á **Vista**.</span><span class="sxs-lookup"><span data-stu-id="54281-139">Click **Save**.</span></span>
23. <span data-ttu-id="54281-140">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="54281-140">Close the page.</span></span>
24. <span data-ttu-id="54281-141">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="54281-141">Close the page.</span></span>
25. <span data-ttu-id="54281-142">Í skoðunarrúðunni ferðu í **Kerfiseiningar > innkaup og aðföng > Lánardrottna > Lánardrottins/vöru tengsl > listi yfir Samþykkta lánardrottna eftir vöru.**</span><span class="sxs-lookup"><span data-stu-id="54281-142">In Navigation Pane, go to **Modules > Procurement and sourcing > Vendors > Vendor/item relations > Approved vendor list by item**.</span></span> <span data-ttu-id="54281-143">Þessi síða gefur yfirlit yfir allar afurðir og samþykkta lánardrottna.</span><span class="sxs-lookup"><span data-stu-id="54281-143">This page gives you an overview of all products and the approved vendors.</span></span>  
26. <span data-ttu-id="54281-144">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="54281-144">Close the page.</span></span>
27. <span data-ttu-id="54281-145">Í skoðunarrúðunni ferðu í **Kerfiseiningar > Innkaup og aðföng > Lánardrottnar > Allir lánardrottnar**.</span><span class="sxs-lookup"><span data-stu-id="54281-145">In Navigation Pane, go to **Modules > Procurement and sourcing > Vendors > All vendors**.</span></span> <span data-ttu-id="54281-146">Einnig er hægt að byrja frá lánardrottni og fara síðan í listann yfir samþykktar afurðir fyrir þann lykil lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="54281-146">You can also start from a vendor and then go to the list of approved products for that vendor account.</span></span>  
28. <span data-ttu-id="54281-147">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="54281-147">In the list, find and select the desired record.</span></span>
29. <span data-ttu-id="54281-148">Á aðgerðasvæðinu er smellt á **Innkaup**.</span><span class="sxs-lookup"><span data-stu-id="54281-148">On the Action Pane, click **Procurement**.</span></span>
30. <span data-ttu-id="54281-149">Smelltu á **Listi yfir Samþykktir lánardrottinn eftir lánardrottni**.</span><span class="sxs-lookup"><span data-stu-id="54281-149">Click **Approved vendor list by vendor**.</span></span>
31. <span data-ttu-id="54281-150">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="54281-150">Close the page.</span></span>
32. <span data-ttu-id="54281-151">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="54281-151">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]