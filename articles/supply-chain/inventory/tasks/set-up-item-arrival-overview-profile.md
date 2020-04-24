---
title: Setja upp komuyfirlitsreglu fyrir vöru
description: Þetta efni leggur áherslu á uppsetningu komuyfirlitsregla.
author: ShylaThompson
manager: tfehr
ms.date: 07/30/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSArrivalOverviewProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 885dc6c4fff53b9c1ddbac64e97b2b415bac1c7a
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204057"
---
# <a name="set-up-an-item-arrival-overview-profile"></a><span data-ttu-id="90152-103">Setja upp komuyfirlitsreglu fyrir vöru</span><span class="sxs-lookup"><span data-stu-id="90152-103">Set up an item arrival overview profile</span></span>

<span data-ttu-id="90152-104">[!include [banner](../../includes/banner.md)]]</span><span class="sxs-lookup"><span data-stu-id="90152-104">[!include [banner](../../includes/banner.md)]]</span></span>

<span data-ttu-id="90152-105">Þetta efni leggur áherslu á uppsetningu komuyfirlitsregla.</span><span class="sxs-lookup"><span data-stu-id="90152-105">This topic focuses on the setup of an arrival overview profile.</span></span> <span data-ttu-id="90152-106">Komuyfirlitsreglu er safn reglna sem verður notað þegar síðan Komuyfirlit er opnað af notanda.</span><span class="sxs-lookup"><span data-stu-id="90152-106">The arrival overview profile is a collection of rules that will be applied when the Arrival overview page is opened by a user.</span></span> <span data-ttu-id="90152-107">Þú getur farið í gegnum þetta ferli í sýnigögn fyrirtækisins USMF.</span><span class="sxs-lookup"><span data-stu-id="90152-107">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="90152-108">Þetta verk myndi venjulega vera framkvæmt af starfsmanni í móttöku.</span><span class="sxs-lookup"><span data-stu-id="90152-108">This procedure would typically be carried out by a receiving clerk.</span></span>

1. <span data-ttu-id="90152-109">Í skoðunarrúðunni ferðu í **Kerfiseiningar > Birgðastýring > Uppsetning > Dreifing > Komuyfirlitsreglur**.</span><span class="sxs-lookup"><span data-stu-id="90152-109">In the navigation pane, go to **Modules > Inventory management > Setup > Distribution > Arrival overview profiles**.</span></span>
2. <span data-ttu-id="90152-110">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="90152-110">Select **New**.</span></span> <span data-ttu-id="90152-111">Þar er þú vinnur nánast alltaf í sama vöruhús við hlaða af fullhlöðnum vörubíl , ætti að stofna komuyfirlitsregla til að auðvelda ferlið við að skrá mótteknar vörur.</span><span class="sxs-lookup"><span data-stu-id="90152-111">Because you will almost always work in the same warehouse offloading full truck loads, you should create an arrival overview profile to simplify the process of registering received items.</span></span>  
3. <span data-ttu-id="90152-112">Í reitinn **Heiti komuyfirlitsreglu** skal færa inn gildi.</span><span class="sxs-lookup"><span data-stu-id="90152-112">In the **Arrival overview profile name** field, type a value.</span></span>
4. <span data-ttu-id="90152-113">Í reitnum **Sýna línur** skal velja valkost.</span><span class="sxs-lookup"><span data-stu-id="90152-113">In the **Show lines** field, select an option.</span></span> <span data-ttu-id="90152-114">Veldu hvaða línur á að sýna fyrir innhreyfingarnar:</span><span class="sxs-lookup"><span data-stu-id="90152-114">Select which lines to show for the receipts:</span></span>  

    - <span data-ttu-id="90152-115">**Allt** – Sýna allar línur óháð stöðu.</span><span class="sxs-lookup"><span data-stu-id="90152-115">**All** – Show all lines, regardless of status.</span></span>   
    - <span data-ttu-id="90152-116">**Í vinnslu** – Sýna línur fyrir innhreyfingar þar sem vinnslu er Lokið eða lokið að Hluta.</span><span class="sxs-lookup"><span data-stu-id="90152-116">**In progress** – Show lines for receipts in which the progress is Complete or Partly.</span></span> <span data-ttu-id="90152-117">Það þýðir að fyrir hverja línu hefur annaðhvort fullt magn eða hluti magns verið skráð í komubók.</span><span class="sxs-lookup"><span data-stu-id="90152-117">This means that for each line, either the full quantity or part of the quantity has been registered in an arrival journal.</span></span>   
    - <span data-ttu-id="90152-118">**Ekki lokið** – Sýna línur fyrir innhreyfingar þar sem vinnslustaða er Ekkert eða að Hluta.</span><span class="sxs-lookup"><span data-stu-id="90152-118">**Not complete** – Show lines for receipts in which the progress is None or Partly.</span></span> <span data-ttu-id="90152-119">Þetta þýðir að ekkert magn eða aðeins hluti þess hefur verið skráður í komubók, fyrir hverja línu.</span><span class="sxs-lookup"><span data-stu-id="90152-119">This means that for each line, nothing or only part of the quantity has been registered in an arrival journal.</span></span>  

5. <span data-ttu-id="90152-120">Útvíkkaðu eða dragðu samann hlutann **Komutímavalkostir**.</span><span class="sxs-lookup"><span data-stu-id="90152-120">Expand or collapse the **Arrival options** section.</span></span>
6. <span data-ttu-id="90152-121">Í reitinn **Dagar frá og með** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="90152-121">In the **Days forward** field, type a value.</span></span> <span data-ttu-id="90152-122">Þetta stillir síu til að sýna línur innhreyfingar sem búist við að taka á móti innan nokkra daga (eftir því hvaða númer sett).</span><span class="sxs-lookup"><span data-stu-id="90152-122">This sets a filter to show the receipt lines expected to be received within the next few days (depending on the number you set).</span></span>  
7. <span data-ttu-id="90152-123">Í reitinn **Dagar aftur í tímann** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="90152-123">In the **Days back** field, type a value.</span></span> <span data-ttu-id="90152-124">Þetta stillir síu til að sýna innhreyfingarlínur sem búist við að tekið sé á móti nokkrum dögum fyrir daginn í dag.</span><span class="sxs-lookup"><span data-stu-id="90152-124">This sets a filter to show the receipt lines expected to be received a number of days before today.</span></span>  
8. <span data-ttu-id="90152-125">Í reitinn **Vöruhús** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="90152-125">In the **Warehouses** field, type a value.</span></span> <span data-ttu-id="90152-126">Sía á eina eða fleiri vöruhúsum.</span><span class="sxs-lookup"><span data-stu-id="90152-126">Filter on one or more warehouses.</span></span>  
9. <span data-ttu-id="90152-127">Í reitnum **Afhendingarmáti** skal færa inn gildi.</span><span class="sxs-lookup"><span data-stu-id="90152-127">In the **Mode of delivery** field, select a value.</span></span> <span data-ttu-id="90152-128">Þetta stillir síu til að sýna aðeins innhreyfingarlínur með þennan Afhendingarmáta.</span><span class="sxs-lookup"><span data-stu-id="90152-128">This sets a filter to show only the receipt lines with this Mode of delivery.</span></span>  
10. <span data-ttu-id="90152-129">Í reitinn **Nafn** skal velja WHS.</span><span class="sxs-lookup"><span data-stu-id="90152-129">In the **Name** field, select WHS.</span></span>
11. <span data-ttu-id="90152-130">Í reitnum **Vöruhús** skal velja vöruhús 24.</span><span class="sxs-lookup"><span data-stu-id="90152-130">In the **Warehouse** field, select warehouse 24.</span></span> <span data-ttu-id="90152-131">Þetta er sjálfgefið vöruhús sem verður notað fyrir skráð innhreyfingarlínur sem nota þessa forstillingu.</span><span class="sxs-lookup"><span data-stu-id="90152-131">This is the default warehouse that will be used for registered receipt lines that use this profile.</span></span>  
12. <span data-ttu-id="90152-132">Í reitnum **Staðsetning** skal velja **Afgreiðsluhurð**.</span><span class="sxs-lookup"><span data-stu-id="90152-132">In the **Location** field, select **Baydoor**.</span></span> <span data-ttu-id="90152-133">Þetta er sjálfgefið staðsetning sem verður notað fyrir skráð innhreyfingarlínur sem nota þessa forstillingu.</span><span class="sxs-lookup"><span data-stu-id="90152-133">This is the default location that will be used for registered receipt lines that use this profile.</span></span>  
13. <span data-ttu-id="90152-134">Útvíkkaðu eða felldu saman hlutann **Upplýsingar um komufyrirspurn**.</span><span class="sxs-lookup"><span data-stu-id="90152-134">Expand or collapse the **Arrival query details** section.</span></span>
14. <span data-ttu-id="90152-135">Í reitnum **Takmarka við svæði** velurðu svæði 2.</span><span class="sxs-lookup"><span data-stu-id="90152-135">In the **Restrict to site** field, select site 2.</span></span> <span data-ttu-id="90152-136">Þetta stillir síu til að sýna aðeins innhreyfingarlínur með þennan Stað.</span><span class="sxs-lookup"><span data-stu-id="90152-136">This sets a filter to show only the receipt lines with this site.</span></span>  
15. <span data-ttu-id="90152-137">Stilltu valkostinn **Innkaupapantanir** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="90152-137">Set the **Purchase orders** option to **Yes**.</span></span> <span data-ttu-id="90152-138">Veljið innhreyfingarlínur úr innkaupapöntunum.</span><span class="sxs-lookup"><span data-stu-id="90152-138">Select receipt lines from purchase orders.</span></span>  
16. <span data-ttu-id="90152-139">Stilltu valkostinn **Flytja** pantanir á **Já**.</span><span class="sxs-lookup"><span data-stu-id="90152-139">Set the **Transfer** orders option to **Yes**.</span></span> <span data-ttu-id="90152-140">Veljið innhreyfingarlínur úr flutningspöntun.</span><span class="sxs-lookup"><span data-stu-id="90152-140">Select receipt lines from transfer orders.</span></span>  
17. <span data-ttu-id="90152-141">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="90152-141">Select **Save**.</span></span>
18. <span data-ttu-id="90152-142">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="90152-142">Close the page.</span></span>

