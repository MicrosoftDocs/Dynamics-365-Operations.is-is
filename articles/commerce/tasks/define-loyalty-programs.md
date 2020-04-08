---
title: Skilgreina vildarkerfi
description: Þessi verklýsing sýnir hvernig á að setja upp vildarkerfi með tveimur vildarlög.
author: jashanno
manager: AnnBe
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b178f1c6a71b34b70db4dbcd1765117215a4d2a1
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022901"
---
# <a name="define-loyalty-programs"></a><span data-ttu-id="4624c-103">Skilgreina vildarkerfi</span><span class="sxs-lookup"><span data-stu-id="4624c-103">Define loyalty programs</span></span>

[!include [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="4624c-104">Þessi verklýsing sýnir hvernig á að setja upp vildarkerfi með tveimur vildarlög.</span><span class="sxs-lookup"><span data-stu-id="4624c-104">This procedure shows how to set up a loyalty program with two loyalty tiers.</span></span> <span data-ttu-id="4624c-105">Þessi aðferð notar USRT sýnigögn fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="4624c-105">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="4624c-106">Fara í Retail og Commerce > ..</span><span class="sxs-lookup"><span data-stu-id="4624c-106">Go to Retail and Commerce > ..</span></span> <span data-ttu-id="4624c-107">> Vildarkerfi.</span><span class="sxs-lookup"><span data-stu-id="4624c-107">> Loyalty programs.</span></span>
2. <span data-ttu-id="4624c-108">Smellið á Nýtt.</span><span class="sxs-lookup"><span data-stu-id="4624c-108">Click New.</span></span>
3. <span data-ttu-id="4624c-109">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="4624c-109">In the Name field, type a value.</span></span>
4. <span data-ttu-id="4624c-110">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="4624c-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="4624c-111">Smella á bæta Við línu.</span><span class="sxs-lookup"><span data-stu-id="4624c-111">Click Add line.</span></span>
6. <span data-ttu-id="4624c-112">Í reitinn Stig skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="4624c-112">In the Level field, enter a number.</span></span>
7. <span data-ttu-id="4624c-113">Færið inn heiti fyrir í vildarlag í svæðinu Lag.</span><span class="sxs-lookup"><span data-stu-id="4624c-113">In the Tier field, enter a name for the loyalty tier.</span></span>
8. <span data-ttu-id="4624c-114">Í reitinn Lýsing skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="4624c-114">In the Description field, type a value.</span></span>
9. <span data-ttu-id="4624c-115">Í reitnum dagsetningabil skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="4624c-115">In the Date interval field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="4624c-116">dagsetningabili ætti að ná inn í framtíðina.</span><span class="sxs-lookup"><span data-stu-id="4624c-116">This date interval should extend into the future.</span></span> <span data-ttu-id="4624c-117">Til dæmis, ef dagsetningabil sem er valið fyrir fulllag er eins árs tímabil, getur hvaða viðskiptavinur sem uppfyllir skilyrði fyrir gulllag getur fengið umbun sem eru úthluta í the gulllag fyrir eitt ár.</span><span class="sxs-lookup"><span data-stu-id="4624c-117">For example, if the date interval that is selected for gold tier is a one-year period, any customer who qualifies for the gold tier can receive the rewards that are assigned to the gold tier for one year.</span></span> <span data-ttu-id="4624c-118">Ef viðskiptavinurinn verður aftur hæfur fyrir gull stig lags meðan þær eru í því lagi, verður dagsetningin þegar lagið þeirra rennur út framlengt um annað ár, frá þeim degi þegar þeir verða aftur hæfir.</span><span class="sxs-lookup"><span data-stu-id="4624c-118">If the customer re-qualifies for the gold tier while they are in the tier, the date that the tier expires is extended by another year from the date when they re-qualify.</span></span>  
10. <span data-ttu-id="4624c-119">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="4624c-119">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="4624c-120">Smellið á „Bæta við línu“.</span><span class="sxs-lookup"><span data-stu-id="4624c-120">Click Add line.</span></span>
12. <span data-ttu-id="4624c-121">Í reitinn Stig skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="4624c-121">In the Level field, enter a number.</span></span>
13. <span data-ttu-id="4624c-122">Færið inn heiti fyrir í vildarlag í svæðinu Lag.</span><span class="sxs-lookup"><span data-stu-id="4624c-122">In the Tier field, enter a name for the loyalty tier.</span></span>
14. <span data-ttu-id="4624c-123">Í reitinn Lýsing skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="4624c-123">In the Description field, type a value.</span></span>
15. <span data-ttu-id="4624c-124">Í reitnum dagsetningabil skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="4624c-124">In the Date interval field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="4624c-125">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="4624c-125">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="4624c-126">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="4624c-126">Click Save.</span></span>
18. <span data-ttu-id="4624c-127">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="4624c-127">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="4624c-128">Reglur vildarlags skilgreina lágmarksfjöldi sem þarf að vera unnið inn á tímabili til að geta fengið vildarpunktur lags.</span><span class="sxs-lookup"><span data-stu-id="4624c-128">Tier rules define the minimum number of a reward point needed to be earned during a time period to qualify for the tier.</span></span>  
19. <span data-ttu-id="4624c-129">Víxla útvíkkun á liðnum reglur lags.</span><span class="sxs-lookup"><span data-stu-id="4624c-129">Toggle the expansion of the Tier rules section.</span></span>
20. <span data-ttu-id="4624c-130">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="4624c-130">Click New.</span></span>
    * <span data-ttu-id="4624c-131">Hægt er að hafa fleiri en eitt lag reglu hvert lag.</span><span class="sxs-lookup"><span data-stu-id="4624c-131">You can have more than one tier rule per tier.</span></span> <span data-ttu-id="4624c-132">Til dæmis gæti verið þrjár skilyrði til að laga; aukakort eftir eyðsluþök $500 í einn mánuð með eyðsluþök einu ári á 1000 usd og hafi 20 færslur í einu ári á eftir.</span><span class="sxs-lookup"><span data-stu-id="4624c-132">For example, you could have three different criteria to earn a tier; by spending $500 in one month, by spending $1000 over one year, and by having 20 transactions in one year.</span></span> <span data-ttu-id="4624c-133">Ef Þetta er gert yrði þarf að stofna þrjá vildarlags.</span><span class="sxs-lookup"><span data-stu-id="4624c-133">To do this, you would need to create three tier rules.</span></span>  
21. <span data-ttu-id="4624c-134">Í reitnum vildarpunktar skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="4624c-134">In the Reward point field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="4624c-135">Þetta ætti að vera ekki innleysanlegur vildarpunktur.</span><span class="sxs-lookup"><span data-stu-id="4624c-135">This should be a non-redeemable loyalty reward point.</span></span>  
22. <span data-ttu-id="4624c-136">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="4624c-136">In the list, click the link in the selected row.</span></span>
23. <span data-ttu-id="4624c-137">Færið inn tölu í svæðinu Lágmarksfjöldi útgefinna punkta.</span><span class="sxs-lookup"><span data-stu-id="4624c-137">In the Minimum issued points field, enter a number.</span></span>
    * <span data-ttu-id="4624c-138">Fyrir lægsta stig lags ef allir viðskiptavinir eru gildir einfaldlega með því að taka þátt í áætluninni, færa inn '0'.</span><span class="sxs-lookup"><span data-stu-id="4624c-138">For the lowest level tier, if all customers qualify simply by participating in the program, enter '0'.</span></span>  
24. <span data-ttu-id="4624c-139">Í reitnum Dagsetningabil endurmats skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="4624c-139">In the Evaluation date interval field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="4624c-140">Þessu dagsetningabili ætti að ná inn í fortíðina.</span><span class="sxs-lookup"><span data-stu-id="4624c-140">This date interval should extend into the past.</span></span> <span data-ttu-id="4624c-141">Aðeins stig sem fengin á þessu dagsetningabili einungis verða talin upp gildið fyrir lágmarks útgefnir punktar .</span><span class="sxs-lookup"><span data-stu-id="4624c-141">Only points earned during this date interval will be counted towards reaching the minimum issued points value.</span></span>  
25. <span data-ttu-id="4624c-142">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="4624c-142">In the list, click the link in the selected row.</span></span>
26. <span data-ttu-id="4624c-143">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="4624c-143">Click Save.</span></span>
27. <span data-ttu-id="4624c-144">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="4624c-144">In the list, find and select the desired record.</span></span>
28. <span data-ttu-id="4624c-145">Smellt er á Nýtt.</span><span class="sxs-lookup"><span data-stu-id="4624c-145">Click New.</span></span>
29. <span data-ttu-id="4624c-146">Í reitnum vildarpunktar skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="4624c-146">In the Reward point field, click the drop-down button to open the lookup.</span></span>
30. <span data-ttu-id="4624c-147">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="4624c-147">In the list, click the link in the selected row.</span></span>
31. <span data-ttu-id="4624c-148">Færið inn tölu í svæðinu Lágmarksfjöldi útgefinna punkta.</span><span class="sxs-lookup"><span data-stu-id="4624c-148">In the Minimum issued points field, enter a number.</span></span>
32. <span data-ttu-id="4624c-149">Í reitnum Dagsetningabil endurmats skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="4624c-149">In the Evaluation date interval field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="4624c-150">Þessu dagsetningabili ætti að ná inn í fortíðina.</span><span class="sxs-lookup"><span data-stu-id="4624c-150">This date interval should extend into the past.</span></span>  
33. <span data-ttu-id="4624c-151">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="4624c-151">In the list, click the link in the selected row.</span></span>
34. <span data-ttu-id="4624c-152">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="4624c-152">Click Save.</span></span>
35. <span data-ttu-id="4624c-153">Smellt er á verðflokkur.</span><span class="sxs-lookup"><span data-stu-id="4624c-153">Click Price groups.</span></span>
    * <span data-ttu-id="4624c-154">Ef óskað er að veita vildarviðskiptavini afslætti .</span><span class="sxs-lookup"><span data-stu-id="4624c-154">If you want to give loyalty customers discounts.</span></span> <span data-ttu-id="4624c-155">Þú þarft að úthluta eina eða fleiri verðflokkum fyrir vildarkerfi og úthluta verðflokkum á afslætti.</span><span class="sxs-lookup"><span data-stu-id="4624c-155">you'll need to assign one or more price groups to the loyalty program and assign the price groups to discounts.</span></span> <span data-ttu-id="4624c-156">Góðir starfshættir eru að blanda ekki verðflokkum yfir mismunandi gerðir af afsláttareiningum.</span><span class="sxs-lookup"><span data-stu-id="4624c-156">It is a best practice to not mix price groups across different types of discounting entities.</span></span>  <span data-ttu-id="4624c-157">Til dæmis ekki nota sömu verðflokk fyrir afslátt vildarkorts og afslátt rásar.</span><span class="sxs-lookup"><span data-stu-id="4624c-157">For example, don't use the same price group for a loyalty discount and a channel discount.</span></span>  
36. <span data-ttu-id="4624c-158">Í reitnum verðflokkur skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="4624c-158">In the Price group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="4624c-159">Verðflokkatengill flokka efst á síðunni er fyrir vildarkerfi.</span><span class="sxs-lookup"><span data-stu-id="4624c-159">The Price groups link at the top of the page is for the loyalty program.</span></span> <span data-ttu-id="4624c-160">Verðflokkatengillinn í lögum forrits hjá flýtiflipanum er fyrir í tilteknu vildarlag aðeins.</span><span class="sxs-lookup"><span data-stu-id="4624c-160">The Price groups link in the Program tiers fasttab is for a specific loyalty tier only.</span></span>  
37. <span data-ttu-id="4624c-161">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="4624c-161">In the list, click the link in the selected row.</span></span>
38. <span data-ttu-id="4624c-162">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="4624c-162">Click Save.</span></span>
39. <span data-ttu-id="4624c-163">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="4624c-163">Close the page.</span></span>
40. <span data-ttu-id="4624c-164">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="4624c-164">Click Save.</span></span>
