---
title: Verðlagsreglur fyrir flokka til að búa til verðsamninga
description: Þetta ferli sýnir hvernig á að stofna verðsamninga söluverðs með verðlagningarreglu flokka.
author: scott-tucker
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, RetailDiscountPricingWorkspace, RetailPricingDiscountCategoryPriceRule, RetailCategoryPriceRule, EcoResCategorySingleLookup, RetailCategoryPriceWizard, PriceDiscAdm, PriceDiscAdmTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 35c85e6e3bbdc913e9cd7aefdf6b143f3f03496f
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022918"
---
# <a name="category-pricing-rules-to-create-trade-agreements"></a><span data-ttu-id="dcaed-103">Verðlagsreglur fyrir flokka til að búa til verðsamninga</span><span class="sxs-lookup"><span data-stu-id="dcaed-103">Category pricing rules to create trade agreements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="dcaed-104">Þetta ferli sýnir hvernig á að stofna verðsamninga söluverðs með verðlagningarreglu flokka.</span><span class="sxs-lookup"><span data-stu-id="dcaed-104">This procedure demonstrates how to create sales price trade agreements using a category pricing rule.</span></span> <span data-ttu-id="dcaed-105">Sýnigögn fyrirtækisins til að stofna verkið er USRT.</span><span class="sxs-lookup"><span data-stu-id="dcaed-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="dcaed-106">Þetta verk er ætluð fyrir hlutverk stjórnanda Commerce.</span><span class="sxs-lookup"><span data-stu-id="dcaed-106">This task is intended for the Commerce merchandising manager role.</span></span>

1. <span data-ttu-id="dcaed-107">Smella á Stjórnun verðlagningar og afslátta.</span><span class="sxs-lookup"><span data-stu-id="dcaed-107">Click Pricing and discount management.</span></span>
2. <span data-ttu-id="dcaed-108">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="dcaed-108">Click New.</span></span>
3. <span data-ttu-id="dcaed-109">Smelltu á Verðregla tegundar</span><span class="sxs-lookup"><span data-stu-id="dcaed-109">Click Category price rule.</span></span>
4. <span data-ttu-id="dcaed-110">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="dcaed-110">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="dcaed-111">Veljið valkost í svæðinu kóði lykils.</span><span class="sxs-lookup"><span data-stu-id="dcaed-111">In the Account code field, select an option.</span></span>
    * <span data-ttu-id="dcaed-112">Lykilkóði "Flokkur" er notuð til að setja upp viðskiptasamninga um söluverð sem eru sértækir fyrir Rásir, vildarkerfi, áætlanir, Vörulista og Tengsl.</span><span class="sxs-lookup"><span data-stu-id="dcaed-112">A "Group" type account code is used to set up sales price trade agreements that are specific for Channels, Loyalty programs, Catalogs, and Affiliations.</span></span>  
6. <span data-ttu-id="dcaed-113">Sláðu inn eða veldu gildi í valreitnum lykill.</span><span class="sxs-lookup"><span data-stu-id="dcaed-113">In the Account selection field, enter or select a value.</span></span>
7. <span data-ttu-id="dcaed-114">Sláið inn eða veldu gildi í reitnum flokkur.</span><span class="sxs-lookup"><span data-stu-id="dcaed-114">In the Category field, enter or select a value.</span></span>
8. <span data-ttu-id="dcaed-115">Í reitinn upphæð/prósenta skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="dcaed-115">In the Amount/Percent field, enter a number.</span></span>
9. <span data-ttu-id="dcaed-116">Sláið inn eða veldu gildi í reitnum sléttunarútgáfa.</span><span class="sxs-lookup"><span data-stu-id="dcaed-116">In the Rounding version field, enter or select a value.</span></span>
10. <span data-ttu-id="dcaed-117">Smellt er á Mynda viðskiptasamninga</span><span class="sxs-lookup"><span data-stu-id="dcaed-117">Click Generate trade agreements.</span></span>
11. <span data-ttu-id="dcaed-118">Smelltu á Næsta.</span><span class="sxs-lookup"><span data-stu-id="dcaed-118">Click Next.</span></span>
12. <span data-ttu-id="dcaed-119">Dagsetning er rituð í reitinn Frá dags.</span><span class="sxs-lookup"><span data-stu-id="dcaed-119">In the From date field, enter a date.</span></span>
13. <span data-ttu-id="dcaed-120">Í reitinn Til dagsetningar skal slá inn dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="dcaed-120">In the To date field, enter a date.</span></span>
14. <span data-ttu-id="dcaed-121">Velja skal Já í Finna næsta svæði.</span><span class="sxs-lookup"><span data-stu-id="dcaed-121">Select Yes in the Find next field.</span></span>
15. <span data-ttu-id="dcaed-122">Smelltu á Næsta.</span><span class="sxs-lookup"><span data-stu-id="dcaed-122">Click Next.</span></span>
16. <span data-ttu-id="dcaed-123">Smellt er á Ljúka.</span><span class="sxs-lookup"><span data-stu-id="dcaed-123">Click Finish.</span></span>
    * <span data-ttu-id="dcaed-124">Þetta býr til verðsamningabók og opnar hana fyrir þig að fara yfir.</span><span class="sxs-lookup"><span data-stu-id="dcaed-124">This creates a Trade agreement journal and opens it for your review.</span></span>  
17. <span data-ttu-id="dcaed-125">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="dcaed-125">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="dcaed-126">Verðsamningabækur stofnuð úr reglur um verðlagningu flokks eru ekki bókuð.</span><span class="sxs-lookup"><span data-stu-id="dcaed-126">The trade agreement journals created from the Category pricing rules aren't posted.</span></span> <span data-ttu-id="dcaed-127">Hægt er að fara yfir og breyta mynduð verði áður en þær eru bókaðar.</span><span class="sxs-lookup"><span data-stu-id="dcaed-127">You can  review and edit the prices generated before posting them.</span></span>  
18. <span data-ttu-id="dcaed-128">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="dcaed-128">Click Edit.</span></span>
19. <span data-ttu-id="dcaed-129">Í Upphæð í gjaldmiðli svæðinu, færið inn tölu.</span><span class="sxs-lookup"><span data-stu-id="dcaed-129">In the Amount in currency field, enter a number.</span></span>
20. <span data-ttu-id="dcaed-130">Smellið á „Bóka“.</span><span class="sxs-lookup"><span data-stu-id="dcaed-130">Click Post.</span></span>
21. <span data-ttu-id="dcaed-131">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="dcaed-131">Click OK.</span></span>
22. <span data-ttu-id="dcaed-132">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="dcaed-132">Close the page.</span></span>
23. <span data-ttu-id="dcaed-133">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="dcaed-133">Close the page.</span></span>
24. <span data-ttu-id="dcaed-134">Smellið á flipann verðlagningarreglur flokks.</span><span class="sxs-lookup"><span data-stu-id="dcaed-134">Click the Category price rules tab.</span></span>
    * <span data-ttu-id="dcaed-135">verðlagningarreglur flokka fyrir tiltekna rás mun sýna á þessum lista.</span><span class="sxs-lookup"><span data-stu-id="dcaed-135">Channel specific Category pricing rules will show in this list.</span></span>  
