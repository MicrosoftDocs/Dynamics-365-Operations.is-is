---
title: Setja upp greiningu nýleika-, tíðni- og peningastigs (RFM)
description: Í þessu efnisatriði er útskýrt hvernig til að setja upp Nýleikastig, Tíðnistig og Peningastig (RFM) greiningar viðskiptavinum.
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: MCRRFMDefinition
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 78943
ms.assetid: 8ff9aac3-5ada-4150-85fd-18901c926d53
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: c7cb79fa82b579bee01e51cb635597cc5f711a98
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022925"
---
# <a name="set-up-recency-frequency-and-monetary-rfm-analysis"></a><span data-ttu-id="5356b-103">Setja upp greiningu nýleika-, tíðni- og peningastigs (RFM)</span><span class="sxs-lookup"><span data-stu-id="5356b-103">Set up Recency, Frequency, and Monetary (RFM) analysis</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5356b-104">Í þessu efnisatriði er útskýrt hvernig til að setja upp Nýleikastig, Tíðnistig og Peningastig (RFM) greiningar viðskiptavinum.</span><span class="sxs-lookup"><span data-stu-id="5356b-104">This topic explains how to set up a Recency, Frequency, and Monetary (RFM) analysis of your customers.</span></span>

<span data-ttu-id="5356b-105">Greiningin Nýleikastig, Tíðnistig og Peningastig (RFM) er markaðssetningarverkfæri sem fyrirtæki þitt getur notað til að meta gögn sem myndast við innkaup viðskiptavina.</span><span class="sxs-lookup"><span data-stu-id="5356b-105">Recency, frequency, and monetary (RFM) analysis is a marketing tool that your organization can use to evaluate the data that is generated by customer purchases.</span></span> <span data-ttu-id="5356b-106">Eftir að þú sett upp RFM-greiningu, eru viðskiptavinir úthlutað reiknað RFM-stigum þegar þeir gera innkaup.</span><span class="sxs-lookup"><span data-stu-id="5356b-106">After you set up RFM analysis, customers are assigned a calculated RFM score as they make purchases.</span></span> <span data-ttu-id="5356b-107">Rfm-stig getur þriggja stafa einkunn eða steypa saman núver, eftir því hvernig fyrirtæki þitt hefur skilgreint rfm-greining.</span><span class="sxs-lookup"><span data-stu-id="5356b-107">The RFM score can be a three-digit rating or an aggregate number, depending on how your organization has configured RFM analysis.</span></span> <span data-ttu-id="5356b-108">Svona virkar einkunnargjöfin ef fyrirtækið notar þriggja stafa einkunn fyrir stigaskor:</span><span class="sxs-lookup"><span data-stu-id="5356b-108">Here's how the rating works if your organization uses a three-digit rating for the score:</span></span>

- <span data-ttu-id="5356b-109">Fyrsti stafurinn er einkunn viðskiptavinar fyrir nýleika, sem er hve nýlega viðskiptavinur gerði innkaup frá fyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="5356b-109">The first digit is the customer's recency rating, which is how recently the customer made a purchase from your organization.</span></span>
- <span data-ttu-id="5356b-110">Annar stafurinn er einkunn viðskiptavinarins fyrir tíðni, sem er hversu oft viðskiptavinurinn gerir innkaup frá fyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="5356b-110">The second digit is the customer's frequency rating, which is how often the customer makes purchases from your organization.</span></span>
- <span data-ttu-id="5356b-111">Þriðji stafurinn er peningalegt einkunn viðskiptavinarins, sem er hversu miklu viðskiptavinurinn eyðir þegar hann gerir innkaup frá fyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="5356b-111">The third digit is the customer's monetary rating, which is how much the customer spends when he makes purchases from your organization.</span></span>

<span data-ttu-id="5356b-112">Til dæmis hefur fyrirtækið stillt einkunnir á skalanum 1 til 5, þar sem 5 er hæsta einkunn.</span><span class="sxs-lookup"><span data-stu-id="5356b-112">For example, your organization has set the ratings on a scale of 1 through 5, where 5 is the highest rating.</span></span> <span data-ttu-id="5356b-113">Í þessu tilviki gefur mat viðskiptavinar upp á 535 eftirfarandi upplýsingar um viðskiptavininn:</span><span class="sxs-lookup"><span data-stu-id="5356b-113">In this case, a customer rating of 535 tells you the following information about the customer:</span></span>

- <span data-ttu-id="5356b-114">**Nýleikastig upp á 5** – Viðskiptavinurinn gerði innkaup nýlega.</span><span class="sxs-lookup"><span data-stu-id="5356b-114">**Recency rating of 5** – The customer recently made a purchase.</span></span>
- <span data-ttu-id="5356b-115">**Tíðnistig upp á 3** – Viðskiptavinurinn kaupir vörur frá fyrirtækinu í meðallagi oft.</span><span class="sxs-lookup"><span data-stu-id="5356b-115">**Frequency rating of 3** – The customer purchases products from your organization moderately often.</span></span>
- <span data-ttu-id="5356b-116">**Peningaeinkunn upp á 5** - Þegar viðskiptavinurinn gerir innkaup eyðir hann umtalsverðu magni af peningum.</span><span class="sxs-lookup"><span data-stu-id="5356b-116">**Monetary rating of 5** – When the customer makes a purchase, he spends a significant amount of money.</span></span>

<span data-ttu-id="5356b-117">Ef fyrirtækið notar uppsöfnuð númer, eru stigin lögð saman.</span><span class="sxs-lookup"><span data-stu-id="5356b-117">If your organization uses an aggregate number for the score, the individual ratings are added together.</span></span> <span data-ttu-id="5356b-118">Í sama dæmi er einkunn viðskiptavinarins 13 (5 + 3 + 5).</span><span class="sxs-lookup"><span data-stu-id="5356b-118">For the same example, the customer has a rating of 13 (5 + 3 + 5).</span></span>

## <a name="set-up-rfm-analysis-for-the-customers-in-your-organization"></a><span data-ttu-id="5356b-119">Setja upp RFM-greiningu fyrir viðskiptavini fyrirtækisins</span><span class="sxs-lookup"><span data-stu-id="5356b-119">Set up RFM analysis for the customers in your organization</span></span>

1. <span data-ttu-id="5356b-120">Farðu í **Símaver** \> **Reglubundið** \> **RFM-greining**.</span><span class="sxs-lookup"><span data-stu-id="5356b-120">Go to **Call center** \> **Periodic** \> **RFM analysis**.</span></span>
2. <span data-ttu-id="5356b-121">Á **RFM greining** síðu skaltu velja **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="5356b-121">On **RFM analysis** page, select **New**.</span></span> <span data-ttu-id="5356b-122">Í reitnum **RFM skilgreining** er fært inn heiti fyrir RFM skilgreininguna.</span><span class="sxs-lookup"><span data-stu-id="5356b-122">In the **RFM definition** field, enter a name for the RFM definition.</span></span> <span data-ttu-id="5356b-123">Til dæmis, hægt væri að kalla á skilgreiningu RFM-A.</span><span class="sxs-lookup"><span data-stu-id="5356b-123">For example, you could call the definition RFM-A.</span></span>
3. <span data-ttu-id="5356b-124">Færið inn upphafsdagsetningu og lokadagsetningu fyrir RFM skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="5356b-124">Enter a start date and end date for this RFM definition.</span></span>
4. <span data-ttu-id="5356b-125">Á flýtiflipanum **Almennt** er eftirfarandi gert:</span><span class="sxs-lookup"><span data-stu-id="5356b-125">On the **General** FastTab, do the following:</span></span>

    - <span data-ttu-id="5356b-126">Ef hver hluti RFM stigaskors verður að innihalda jafnan fjöldi viðskiptavinum, veljið þá **Jöfn dreifing** gátreitinn.</span><span class="sxs-lookup"><span data-stu-id="5356b-126">If each section of the RFM score must contain an equal count of customers, select the **Even distribution** check box.</span></span>
    - <span data-ttu-id="5356b-127">Velja skal **Bæta við stigaskori** gátreit til að steypa saman öllum þremur stigaskorum.</span><span class="sxs-lookup"><span data-stu-id="5356b-127">Select the **Add scores** check box to aggregate the three scores.</span></span> <span data-ttu-id="5356b-128">Þetta, til dæmis, myndi veita viðskiptavini RFM skor upp á 13 í stað 535.</span><span class="sxs-lookup"><span data-stu-id="5356b-128">For example, this would give a customer an RFM score of 13 instead of 535.</span></span>
    - <span data-ttu-id="5356b-129">Velja skal **Vista feril** gátreit til að krefja kerfið til að vista tölfræðileg gögn fyrir viðskiptavini þannig að gögnin sé hægt er að nota til að reikna út RFM skorið.</span><span class="sxs-lookup"><span data-stu-id="5356b-129">Select the **Save history** check box to require the system to save the statistical data for customers so that the data can be used to calculate the RFM score.</span></span>

5. <span data-ttu-id="5356b-130">Á flýtiflipanum **Nýleiki** er eftirfarandi gert:</span><span class="sxs-lookup"><span data-stu-id="5356b-130">On the **Recency** FastTab, do the following:</span></span>

    - <span data-ttu-id="5356b-131">Í því **Deildir** svæðinu, færið inn fjölda deilda eða flokka sem verður notað til að reikna út á nýleikaskor fyrir viðskiptavini.</span><span class="sxs-lookup"><span data-stu-id="5356b-131">In the **Divisions** field, enter the number of divisions, or groups, which will be used to calculate the recency score for customers.</span></span> <span data-ttu-id="5356b-132">Til dæmis, ef þú átt 100 viðskiptavinir þýðir skipting upp á 5 að það eru 20 viðskiptavina fyrir hvert stig.</span><span class="sxs-lookup"><span data-stu-id="5356b-132">For example, if you have 100 customers, a division of 5 means that there are 20 customers for each score.</span></span> <span data-ttu-id="5356b-133">Þeir 20 viðskiptavinir sem hafa gert innkaup nýlega hafa nýleikaskor 5.</span><span class="sxs-lookup"><span data-stu-id="5356b-133">The 20 customers who have made purchases most recently have a recency score of 5.</span></span> <span data-ttu-id="5356b-134">Næstu 20 viðskiptavinir hafa nýleikaskor 4, og svo framvegis.</span><span class="sxs-lookup"><span data-stu-id="5356b-134">The next 20 customers have a recency score of 4, and so on.</span></span> <span data-ttu-id="5356b-135">Ef 50 viðskiptavini, 10 viðskiptavinir hafa stig recency upp á 5, 10 hafa recency stig 4 og svo framvegis.</span><span class="sxs-lookup"><span data-stu-id="5356b-135">If you have 50 customers, 10 customers have a recency score of 5, 10 have a recency score of 4, and so on.</span></span>
    - <span data-ttu-id="5356b-136">Í **Forgangur** svæðinu skal velja hversu mikið vægi á að gefa nýleikafæribreytu miðað við aðrar færibreytur þegar RFM skorið er reiknuð út fyrir viðskiptavini.</span><span class="sxs-lookup"><span data-stu-id="5356b-136">In the **Priority** field, select how much weight to give the recency parameter in relation to the other parameters when the RFM score is calculated for a customer.</span></span> <span data-ttu-id="5356b-137">Til dæmis gætirðu lagt hærra gildi á nýleikastig en á peningastig.</span><span class="sxs-lookup"><span data-stu-id="5356b-137">For example, you might place more value on the recency score than the monetary score.</span></span>
    - <span data-ttu-id="5356b-138">Í **Margfaldari** svæðinu, færið inn gildi sem á að margfalda nýleikaskor með.</span><span class="sxs-lookup"><span data-stu-id="5356b-138">In the **Multiplier** field, enter the value by which to multiply the recency score.</span></span> <span data-ttu-id="5356b-139">Ef gildi er ekki færður þeirri einkunn sem er ekki margfaldað.</span><span class="sxs-lookup"><span data-stu-id="5356b-139">If you do not enter a value, the score will not be multiplied.</span></span>
    - <span data-ttu-id="5356b-140">Í því **Tímabil** svæðinu, veljið það tímabil þar sem nýleikaskor er reiknuð.</span><span class="sxs-lookup"><span data-stu-id="5356b-140">In the **Period** field, select the time period by which the recency score is calculated.</span></span> <span data-ttu-id="5356b-141">Til dæmis eftir viku eða mánuð.</span><span class="sxs-lookup"><span data-stu-id="5356b-141">For example, by week or by month.</span></span>

6. <span data-ttu-id="5356b-142">Á flýtiflipanum **Tíðni** er eftirfarandi gert:</span><span class="sxs-lookup"><span data-stu-id="5356b-142">On the **Frequency** FastTab, do the following:</span></span>

    - <span data-ttu-id="5356b-143">Í **Deildir** svæðinu, færið inn fjölda deilda eða flokka sem verður notað til að reikna út tíðniskor fyrir viðskiptavini.</span><span class="sxs-lookup"><span data-stu-id="5356b-143">In the **Divisions** field, enter the number of divisions, or groups, which will be used to calculate the frequency score for customers.</span></span>
    - <span data-ttu-id="5356b-144">Í **Forgangur** svæðinu skal velja hversu mikið vægi á að gefa tíðnifæribreytu miðað við aðrar þegar RFM skorið er reiknuð út fyrir viðskiptavini.</span><span class="sxs-lookup"><span data-stu-id="5356b-144">In the **Priority** field, select how much weight to give the frequency parameter in relation to the others when the RFM score is calculated for a customer.</span></span>
    - <span data-ttu-id="5356b-145">Í **Margfaldari** svæðinu, færið inn gildi sem margfalda á tíðniskor með.</span><span class="sxs-lookup"><span data-stu-id="5356b-145">In the **Multiplier** field, enter the value by which to multiply the frequency score.</span></span> <span data-ttu-id="5356b-146">Ef gildi er ekki færður þeirri einkunn sem er ekki margfaldað.</span><span class="sxs-lookup"><span data-stu-id="5356b-146">If you do not enter a value, the score will not be multiplied.</span></span>

7. <span data-ttu-id="5356b-147">Á flýtiflipanum **Peningalegt** er eftirfarandi gert:</span><span class="sxs-lookup"><span data-stu-id="5356b-147">On the **Monetary** FastTab, do the following:</span></span>

    - <span data-ttu-id="5356b-148">Í **Deildir** svæðinu, færið inn fjölda deilda eða flokka sem verður notað til að reikna út á peningalegt skor fyrir viðskiptavini.</span><span class="sxs-lookup"><span data-stu-id="5356b-148">In the **Divisions** field, enter the number of divisions, or groups, which will be used to calculate the monetary score for customers.</span></span>
    - <span data-ttu-id="5356b-149">Í **Forgangur** svæðinu skal velja hversu mikið vægi á að gefa peningafæribreytu miðað við aðrar þegar RFM skorið er reiknuð út fyrir viðskiptavini.</span><span class="sxs-lookup"><span data-stu-id="5356b-149">In the **Priority** field, select how much weight to give the monetary parameter in relation to the others when the RFM score is calculated for a customer.</span></span>
    - <span data-ttu-id="5356b-150">Í **Margfaldari** svæðinu, færið inn gildi sem margfalda á peningaskorið með.</span><span class="sxs-lookup"><span data-stu-id="5356b-150">In the **Multiplier** field, enter the value by which to multiply the monetary score.</span></span> <span data-ttu-id="5356b-151">Ef gildi er ekki færður þeirri einkunn sem er ekki margfaldað.</span><span class="sxs-lookup"><span data-stu-id="5356b-151">If you do not enter a value, the score will not be multiplied.</span></span>
    - <span data-ttu-id="5356b-152">Í **Brúttó/nettó** svæðinu skal velja hvort eigi að reikna peningaskor viðskiptavinar með því að nota brúttó eða nettó reikningsupphæð.</span><span class="sxs-lookup"><span data-stu-id="5356b-152">In the **Gross/net** field, select whether the customer's monetary score should be calculated by using the gross or net invoice amount.</span></span>
    - <span data-ttu-id="5356b-153">Ef ætti að draga skilaupphæðir viðskiptavinar frá heildarútreikningi reiknings viðskiptavinar skal velja gátreitinn **Draga frá skil**.</span><span class="sxs-lookup"><span data-stu-id="5356b-153">If a customer's return amounts should be subtracted from the customer's total invoice calculation, select the **Subtract returns** check box.</span></span>

## <a name="view-a-customers-rfm-score"></a><span data-ttu-id="5356b-154">Skoða RFM-skor viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="5356b-154">View a customer's RFM score</span></span>

<span data-ttu-id="5356b-155">Notið þessa aðferð til að skoða RFM-skor viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="5356b-155">Use this procedure to view a customer's RFM score.</span></span>

1. <span data-ttu-id="5356b-156">Fara í **Símaver** \> **Færslubækur** \> **Þjónustuver**.</span><span class="sxs-lookup"><span data-stu-id="5356b-156">Go to **Call center** \> **Journals** \> **Customer service**.</span></span>
2. <span data-ttu-id="5356b-157">Á **Þjónustuver** síðunni, á **Þjónustuver** rúðunni, í leitarsvæðunum, velja gerð lykilorðs til að leita í og færið inn leitartextann.</span><span class="sxs-lookup"><span data-stu-id="5356b-157">On the **Customer service** page, in the **Customer service** pane, in the search fields, select the keyword type to search on and enter the search text.</span></span>
3. <span data-ttu-id="5356b-158">Velja **Leita**.</span><span class="sxs-lookup"><span data-stu-id="5356b-158">Select **Search**.</span></span>
4. <span data-ttu-id="5356b-159">Á síðunni **Leit viðskiptavinur** skal velja viðskiptavinaskrá sem þú vilt og smellið síðan á **Velja viðskiptavinur**.</span><span class="sxs-lookup"><span data-stu-id="5356b-159">On the **Customer search** page, select the customer record that you want, and then click **Select customer**.</span></span>

<span data-ttu-id="5356b-160">RFM skorið birtist í **Pöntunarferill** hópnum hægra megin á **Þjónustuver** síðunni.</span><span class="sxs-lookup"><span data-stu-id="5356b-160">The RFM score is displayed in the **Order history** group on the right side of the **Customer service** page.</span></span>

## <a name="view-or-clear-the-history-of-an-rfm-analysis-record"></a><span data-ttu-id="5356b-161">Skoða eða hreinsa sögu til RFM-greiningarfærslu</span><span class="sxs-lookup"><span data-stu-id="5356b-161">View or clear the history of an RFM analysis record</span></span>

<span data-ttu-id="5356b-162">Notið þetta ferli til að skoða eða hreinsa sögu RFM analysis færslu.</span><span class="sxs-lookup"><span data-stu-id="5356b-162">Use this procedure to view or clear the history of an RFM analysis record.</span></span>

1. <span data-ttu-id="5356b-163">Farðu í **Símaver** \> **Reglubundið** \> **RFM-greining**.</span><span class="sxs-lookup"><span data-stu-id="5356b-163">Go to **Call center** \> **Periodic** \> **RFM analysis**.</span></span>
2. <span data-ttu-id="5356b-164">Á **RFM greining** síðunni skal velja skrána sem á að skoða.</span><span class="sxs-lookup"><span data-stu-id="5356b-164">On the **RFM analysis** page, select the record that you want to view.</span></span>
3. <span data-ttu-id="5356b-165">Til að skoða skráarferil, smellið á flýtiflipann **Ferill**.</span><span class="sxs-lookup"><span data-stu-id="5356b-165">To view the record history, select the **History** FastTab.</span></span>
4. <span data-ttu-id="5356b-166">Til að hreinsa feril skráar, smellið á **Hreinsa feril**.</span><span class="sxs-lookup"><span data-stu-id="5356b-166">To clear the history of the record, select **Clear history**.</span></span>