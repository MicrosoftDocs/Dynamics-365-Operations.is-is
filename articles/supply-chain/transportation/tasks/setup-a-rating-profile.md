---
title: Taxtaforstillingar
description: Í þessu efnisatriði er lýst hvernig eigi að setja upp gögn fyrir taxtaforstillingar.
author: Henrikan
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TMSRatingProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d359394ee0086edc5c8b9a3a0c48cf5933963ceb
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828443"
---
# <a name="rating-profiles"></a><span data-ttu-id="0293f-103">Taxtaforstillingar</span><span class="sxs-lookup"><span data-stu-id="0293f-103">Rating profiles</span></span>

<span data-ttu-id="0293f-104">Taxtaforstilling líkist vörustjórnunarsamningi (en ekki löglegum þjónustusamningi).</span><span class="sxs-lookup"><span data-stu-id="0293f-104">A rating profile resembles a logistics contract (but not a legal contract).</span></span> <span data-ttu-id="0293f-105">Það er notað til að ákvarða flutningsgjaldskrá fyrir farma.</span><span class="sxs-lookup"><span data-stu-id="0293f-105">It's used to determine transportation tariffs for loads.</span></span> 

<span data-ttu-id="0293f-106">Taxtaforstilling er einkvæm fyrir farmflytjanda.</span><span class="sxs-lookup"><span data-stu-id="0293f-106">Each rating profile is unique to a shipping carrier.</span></span> <span data-ttu-id="0293f-107">Í forstillingunni er hægt að tengja farmflytjanda við aðalsniðmát taxta.</span><span class="sxs-lookup"><span data-stu-id="0293f-107">In the profile, you associate the shipping carrier with a rate master.</span></span> <span data-ttu-id="0293f-108">Aðalsniðmát taxta skilgreinir úthlutun grunntaxta og grunntaxtann.</span><span class="sxs-lookup"><span data-stu-id="0293f-108">The rate master defines the rate base assignment and the rate base.</span></span> <span data-ttu-id="0293f-109">Grunntaxti ákvarðar taxta farmflytjanda.</span><span class="sxs-lookup"><span data-stu-id="0293f-109">The rate base determines the rate of the carrier.</span></span>

<span data-ttu-id="0293f-110">Þú getur sett upp taxtaforstillingar með því að nota almenna uppsetningarskjámynd sem er með yfirlit yfir allar núverandi taxtaforstillingar.</span><span class="sxs-lookup"><span data-stu-id="0293f-110">You can set up a rating profile by using a generic page that shows an overview of all existing rating profiles.</span></span> <span data-ttu-id="0293f-111">Einnig er hægt að setja upp taxtaforstillingar beint úr farmflytjanda.</span><span class="sxs-lookup"><span data-stu-id="0293f-111">Alternatively, you can set up a rating profile directly from the shipping carrier.</span></span> <span data-ttu-id="0293f-112">Í báðum tilvikum er hægt að nota upplýsingarnar sem eru settar upp fyrir fjárhagsforstillinguna.</span><span class="sxs-lookup"><span data-stu-id="0293f-112">In both cases, the information that you set up for the rating profile is the same.</span></span>

## <a name="create-or-edit-a-rating-profile-on-the-rating-profiles-page"></a><span data-ttu-id="0293f-113">Stofna eða breyta einkunnasniðmátið á síðunni Taxtaforstillingar</span><span class="sxs-lookup"><span data-stu-id="0293f-113">Create or edit a rating profile on the Rating profiles page</span></span>

<span data-ttu-id="0293f-114">Á síðunni **Taxtaforstillingar** er hægt að fara yfir allar fyrirliggjandi taxtaforstillingar.</span><span class="sxs-lookup"><span data-stu-id="0293f-114">On the **Rating profiles** page, you can review all available rating profiles.</span></span> <span data-ttu-id="0293f-115">Einnig er hægt að breyta fyrirliggjandi forstillingum og búa til nýjar forstillingar.</span><span class="sxs-lookup"><span data-stu-id="0293f-115">You can also edit existing profiles and create new profiles.</span></span>

1. <span data-ttu-id="0293f-116">Opnið **Flutningsstjórnun \> Uppsetning \> Taxti \> Taxtaforstilling**.</span><span class="sxs-lookup"><span data-stu-id="0293f-116">Go to **Transportation management \> Setup \> Rating \> Rating profile**.</span></span>
1. <span data-ttu-id="0293f-117">Í aðgerðasvæði skal velja **Nýtt** til að bæta nýrri taxtareglu við hnitanetið eða velja **Breyta** til að breyta fyrirliggjandi forstillingu.</span><span class="sxs-lookup"><span data-stu-id="0293f-117">On the Action Pane, select **New** to add a new rating profile to the grid, or select **Edit** to edit an existing profile.</span></span>
1. <span data-ttu-id="0293f-118">Í línunni fyrir nýja eða fyrirliggjandi taxtaforstillingu skal stilla eftirfarandi reiti:</span><span class="sxs-lookup"><span data-stu-id="0293f-118">In the row for the new or existing rating profile, set the following fields:</span></span>

    - <span data-ttu-id="0293f-119">**Taxtaforstilling** – Færðu inn einkvæmt kenni fyrir taxtaforstillinguna.</span><span class="sxs-lookup"><span data-stu-id="0293f-119">**Rating profile** – Enter a unique identifier (ID) for the rating profile.</span></span>
    - <span data-ttu-id="0293f-120">**Heiti** - Færið inn lýsandi heiti á taxtaforstillingunni.</span><span class="sxs-lookup"><span data-stu-id="0293f-120">**Name** – Enter a descriptive name for the rating profile.</span></span>
    - <span data-ttu-id="0293f-121">**Farmflytjandi** – Veljið farmflytjanda.</span><span class="sxs-lookup"><span data-stu-id="0293f-121">**Shipping carrier** – Select a shipping carrier.</span></span> <span data-ttu-id="0293f-122">Taxtaforstillingin sem verið er að setja upp verður einnig sýnd á síðunni **Farmflytjendur** fyrir valinn farmflytjanda.</span><span class="sxs-lookup"><span data-stu-id="0293f-122">The rating profile that you're setting up will also be shown on the **Shipping carriers** page for the selected carrier.</span></span>
    - <span data-ttu-id="0293f-123">**Svæði** og **Vöruhús** – Veljið svæði og vöruhús.</span><span class="sxs-lookup"><span data-stu-id="0293f-123">**Site** and **Warehouse** – Select a site and warehouse.</span></span>
    - <span data-ttu-id="0293f-124">**Taxtavél** – Veljið taxtavél fyrir taxtaforstillinguna.</span><span class="sxs-lookup"><span data-stu-id="0293f-124">**Rate engine** – Select the rate engine for the rating profile.</span></span>
    - <span data-ttu-id="0293f-125">**Aðalsniðmát taxta** – Veljið aðalsniðmát taxta fyrir taxtaforstillinguna.</span><span class="sxs-lookup"><span data-stu-id="0293f-125">**Rate master** – Select the rate master for the rating profile.</span></span> <span data-ttu-id="0293f-126">Hægt er að nota taxtasniðmátinu til að skilgreina með grunngerð og taxtagrunn.</span><span class="sxs-lookup"><span data-stu-id="0293f-126">You can use the rate master to define a rate base type and a rate base.</span></span> <span data-ttu-id="0293f-127">Frekari upplýsingar er að finna í [Setja upp aðalsniðmát taxta](set-up-rate-masters.md).</span><span class="sxs-lookup"><span data-stu-id="0293f-127">For more information, see [Set up rate masters](set-up-rate-masters.md).</span></span>
    - <span data-ttu-id="0293f-128">**Flutningstímavél** -Veljið flutningstímavél fyrir taxtaforstillinguna.</span><span class="sxs-lookup"><span data-stu-id="0293f-128">**Transit time engine** – Select the transit time engine for the rating profile.</span></span>
    - <span data-ttu-id="0293f-129">**Eldsneytisvísir flutningsaðila** – Veljið eldsneytisvísi flutningsaðila fyrir taxtaforstillinguna.</span><span class="sxs-lookup"><span data-stu-id="0293f-129">**Carrier fuel index** – Select the carrier fuel index for the rating profile.</span></span>
    - <span data-ttu-id="0293f-130">**Upphafsdagsetning og-tími** og **Lokadags. og-tími** – Skilgreinið tímabilið þegar taxtaforstillingin á að vera virk.</span><span class="sxs-lookup"><span data-stu-id="0293f-130">**Effect start date and time** and **Effective end date and time** – Define the period when the rating profile should be active.</span></span>

1. <span data-ttu-id="0293f-131">Í aðgerðarúðunni skal velja **Vista**.</span><span class="sxs-lookup"><span data-stu-id="0293f-131">On the Action Pane, select **Save**.</span></span>

## <a name="create-a-rating-profile-directly-on-the-shipping-carriers-page"></a><span data-ttu-id="0293f-132">Búa til taxtaforstillingu beint á síðu farmflytjanda</span><span class="sxs-lookup"><span data-stu-id="0293f-132">Create a rating profile directly on the Shipping carriers page</span></span>

1. <span data-ttu-id="0293f-133">Opnið **Flutningsstjórnun \> Uppsetning \> Flutningsaðilar \> Farmflytjendur**.</span><span class="sxs-lookup"><span data-stu-id="0293f-133">Go to **Transportation management \> Setup \> Carriers \> Shipping carriers**.</span></span>
1. <span data-ttu-id="0293f-134">Veldu farmflytjanda í listanum.</span><span class="sxs-lookup"><span data-stu-id="0293f-134">Select a shipping carrier in the list.</span></span>
1. <span data-ttu-id="0293f-135">Í flýtiflipanum **Taxtaforstilling** velur þú **Nýtt** til að búa til taxtaforstillingu.</span><span class="sxs-lookup"><span data-stu-id="0293f-135">On the **Rating profiles** FastTab, select **New** to create a rating profile.</span></span>
1. <span data-ttu-id="0293f-136">Stillið reitina fyrir nýja taxtaforstilling.</span><span class="sxs-lookup"><span data-stu-id="0293f-136">Set the fields for the new rating profile.</span></span> <span data-ttu-id="0293f-137">Þessir reitir samsvara reitum á síðunni **Taxtasniðmátum**, eins og lýst er í fyrri hluta atriðins.</span><span class="sxs-lookup"><span data-stu-id="0293f-137">These fields correspond to the fields on the **Rating profiles** page, as described in previous section of this topic.</span></span>

> [!NOTE]
> <span data-ttu-id="0293f-138">Forstillingar sem búnar eru til á síðunni **Farmflytjendur** eru einnig sýndar á síðunni **Taxtaforstillingar**.</span><span class="sxs-lookup"><span data-stu-id="0293f-138">Profiles that are created on the **Shipping carriers** page are also shown on the **Rating profiles** page.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]