---
title: Bæta spálíkanið (forskoðun)
description: Þetta efnisatriði lýsir eiginleikum sem hægt er að nota til að bæta afköst spálíkana.
author: ShivamPandey-msft
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 184a1cb5d3851e26b41340b711c51ef38e06eb53
ms.sourcegitcommit: ebcd9019cbb88a7f2afd9e701812e222566fd43d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/04/2021
ms.locfileid: "6186643"
---
# <a name="improve-the-prediction-model-preview"></a><span data-ttu-id="4bb83-103">Bæta spálíkanið (forskoðun)</span><span class="sxs-lookup"><span data-stu-id="4bb83-103">Improve the prediction model (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="4bb83-104">Þetta efnisatriði lýsir eiginleikum sem hægt er að nota til að bæta afköst spálíkana.</span><span class="sxs-lookup"><span data-stu-id="4bb83-104">This topic describes features that you can use to improve the performance of prediction models.</span></span> <span data-ttu-id="4bb83-105">Þú byrjar á því að bæta líkanið á vinnusvæðinu **Greiðsluspár viðskiptavinar** í Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="4bb83-105">You start to improve your model in the **Customer payment predictions** workspace in Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="4bb83-106">Umbótaskrefunum er svo lokið í AI Builder.</span><span class="sxs-lookup"><span data-stu-id="4bb83-106">The improvement steps are then completed in AI Builder.</span></span>

## <a name="select-historical-outcomes"></a><span data-ttu-id="4bb83-107">Velja sögulegar niðurstöður</span><span class="sxs-lookup"><span data-stu-id="4bb83-107">Select historical outcomes</span></span>

<span data-ttu-id="4bb83-108">Þú velur fyrst eina eða fleiri af þremur mögulegum niðurstöðum fyrir reikninga: **Á réttum tíma**, **Seint** og **mjög seint**.</span><span class="sxs-lookup"><span data-stu-id="4bb83-108">You first select one or more of the three possible outcomes for invoices: **On time**, **Late**, and **Very late**.</span></span> <span data-ttu-id="4bb83-109">Velja ætti allar þrjár niðurstöður.</span><span class="sxs-lookup"><span data-stu-id="4bb83-109">All three outcomes should be selected.</span></span> <span data-ttu-id="4bb83-110">Þegar val niðurstaðnanna er hreinsað verða reikningar síaðir út úr þjálfunarferlinu og nákvæmni spárinnar minnkar.</span><span class="sxs-lookup"><span data-stu-id="4bb83-110">If you clear the selection of any of the outcomes, invoices will be filtered out of the training process and the accuracy of the prediction will be reduced.</span></span>

<span data-ttu-id="4bb83-111">[![Staðfestir niðurstöður](./media/confirm-3-outcomes.png)](./media/confirm-3-outcomes.png)</span><span class="sxs-lookup"><span data-stu-id="4bb83-111">[![Confirming outcomes](./media/confirm-3-outcomes.png)](./media/confirm-3-outcomes.png)</span></span>

<span data-ttu-id="4bb83-112">Ef fyrirtækið krefst aðeins tveggja niðurstaðna skal breyta **Seint** og **Mjög seint** viðmiðunarmörkunum í 0 (núll) daga.</span><span class="sxs-lookup"><span data-stu-id="4bb83-112">If your organization requires only two outcomes, change the **Late** and **Very late** thresholds to 0 (zero) days.</span></span> <span data-ttu-id="4bb83-113">Á þennan hátt er hægt að draga spána saman í tvíundarstöðuna **Á réttum tíma** eða **Seint**.</span><span class="sxs-lookup"><span data-stu-id="4bb83-113">In this way, you effectively collapse the prediction to a binary state of **On time** or **Late**.</span></span>

## <a name="select-fields"></a><span data-ttu-id="4bb83-114">Velja svæði</span><span class="sxs-lookup"><span data-stu-id="4bb83-114">Select fields</span></span>

<span data-ttu-id="4bb83-115">Þegar þú velur svæði til að taka með í líkaninu skaltu hafa í huga að listinn inniheldur öll tiltæk svæði í Microsoft Dataverse -töflunni sem er varpað í gögnin í Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="4bb83-115">When you're selecting fields to include in the model, be aware that the list includes all available fields in the Microsoft Dataverse table that is mapped to the data in the Azure data lake.</span></span> <span data-ttu-id="4bb83-116">Suma þessa reiti ætti **ekki** að velja.</span><span class="sxs-lookup"><span data-stu-id="4bb83-116">Some of these fields should **not** be selected.</span></span> <span data-ttu-id="4bb83-117">Reitirnir sem ættu ekki að vera valdir falla undir einn af þremur flokkum:</span><span class="sxs-lookup"><span data-stu-id="4bb83-117">The fields that should not be selected fall into one of three categories:</span></span>

- <span data-ttu-id="4bb83-118">Reiturinn er áskilinn fyrir Dataverse töfluna en engin gögn eru til staðar fyrir það í Data Lake.</span><span class="sxs-lookup"><span data-stu-id="4bb83-118">The field is required for the Dataverse table, but there is no backing data for it in the data lake.</span></span>
- <span data-ttu-id="4bb83-119">Svæðið er auðkenni og er því óskiljanlegt fyrir vélnámseiginleika.</span><span class="sxs-lookup"><span data-stu-id="4bb83-119">The field is an ID and therefore doesn't make sense for a machine learning feature.</span></span>
- <span data-ttu-id="4bb83-120">Reiturinn sýnir upplýsingar sem verða ekki í boði við spá.</span><span class="sxs-lookup"><span data-stu-id="4bb83-120">The field represents information that won't be available during prediction.</span></span>

<span data-ttu-id="4bb83-121">Eftirfarandi kaflar sýna svæðin sem eru tiltæk fyrir einingar reikninga og viðskiptavina og listi yfir svæðin sem ætti **ekki** að velja til þjálfunar.</span><span class="sxs-lookup"><span data-stu-id="4bb83-121">The following sections show the fields that are available for the invoice and customer entities, and list the fields that should **not** be selected for training.</span></span> <span data-ttu-id="4bb83-122">Flokkurinn sem er tilgreindur fyrir hvert þessara svæða vísar í flokkana í listanum þar á undan.</span><span class="sxs-lookup"><span data-stu-id="4bb83-122">The category that is specified for each of those fields refers to the categories in the preceding list.</span></span>
 
### <a name="invoice-dataverse-table"></a><span data-ttu-id="4bb83-123">Reikningur Dataverse tafla</span><span class="sxs-lookup"><span data-stu-id="4bb83-123">Invoice Dataverse table</span></span>

<span data-ttu-id="4bb83-124">Eftirfarandi mynd sýnir reitina sem eru í boði fyrir reikningstöfluna.</span><span class="sxs-lookup"><span data-stu-id="4bb83-124">The following illustration shows the fields that are available for the invoice table.</span></span>

<span data-ttu-id="4bb83-125">[![Tiltæk svæði fyrir reikningstöfluna](./media/available-fields.png)](./media/available-fields.png)</span><span class="sxs-lookup"><span data-stu-id="4bb83-125">[![Available fields for the invoice table](./media/available-fields.png)](./media/available-fields.png)</span></span>

<span data-ttu-id="4bb83-126">Eftirfarandi reitir ættu ekki að vera valdir fyrir þjálfun:</span><span class="sxs-lookup"><span data-stu-id="4bb83-126">The following fields should not be selected for training:</span></span>

- <span data-ttu-id="4bb83-127">**Reikningslykill** (flokkur 2)</span><span class="sxs-lookup"><span data-stu-id="4bb83-127">**Invoice Account** (category 2)</span></span>
- <span data-ttu-id="4bb83-128">**Er lokað** (flokkur 3) – Þetta svæði er notað til að sía reikninga fyrir þjálfun (lokað) og spá (ekki lokað).</span><span class="sxs-lookup"><span data-stu-id="4bb83-128">**Is closed** (category 3) – This field is used to filter invoices for training (closed) and prediction (not closed).</span></span>
- <span data-ttu-id="4bb83-129">**Heiti** (flokkur 1)</span><span class="sxs-lookup"><span data-stu-id="4bb83-129">**Name** (category 1)</span></span>
- <span data-ttu-id="4bb83-130">**Upprunakenni** (flokkur 2)</span><span class="sxs-lookup"><span data-stu-id="4bb83-130">**Source Id** (category 2)</span></span>
- <span data-ttu-id="4bb83-131">**Upprunafærsla** (flokkur 2)</span><span class="sxs-lookup"><span data-stu-id="4bb83-131">**Source record** (category 2)</span></span>
- <span data-ttu-id="4bb83-132">**Upprunatafla** (flokkur 2)</span><span class="sxs-lookup"><span data-stu-id="4bb83-132">**Source table** (category 2)</span></span>

### <a name="customer-dataverse-table"></a><span data-ttu-id="4bb83-133">Viðskiptavinur Dataverse tafla</span><span class="sxs-lookup"><span data-stu-id="4bb83-133">Customer Dataverse table</span></span>

<span data-ttu-id="4bb83-134">Eftirfarandi mynd sýnir reitina sem eru í boði fyrir viðskiptavinatöfluna.</span><span class="sxs-lookup"><span data-stu-id="4bb83-134">The following illustration shows the fields that are available for the customer table.</span></span>

<span data-ttu-id="4bb83-135">[![Tiltæk svæði fyrir viðskiptavinatöfluna](./media/related-entities.png)](./media/related-entities.png)</span><span class="sxs-lookup"><span data-stu-id="4bb83-135">[![Available fields for the customer table](./media/related-entities.png)](./media/related-entities.png)</span></span>

<span data-ttu-id="4bb83-136">Ekki ætti að velja eftirfarandi reit fyrir þjálfun:</span><span class="sxs-lookup"><span data-stu-id="4bb83-136">The following field should not be selected for training:</span></span>

- <span data-ttu-id="4bb83-137">**Einkvæm lykillína** (flokkur 2)</span><span class="sxs-lookup"><span data-stu-id="4bb83-137">**Row Unique Key** (category 2)</span></span>

## <a name="filters"></a><span data-ttu-id="4bb83-138">Síur</span><span class="sxs-lookup"><span data-stu-id="4bb83-138">Filters</span></span>

<span data-ttu-id="4bb83-139">Eins og er styðja síurnar ekki sviðsmynd fyrir spá um greiðslu viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="4bb83-139">The filters don't currently support the Customer payment predictor scenario.</span></span> <span data-ttu-id="4bb83-140">Þess vegna skal velja **Sleppa þessu skrefi** og halda áfram á samantektarsíðuna.</span><span class="sxs-lookup"><span data-stu-id="4bb83-140">Therefore, select **Skip this step**, and continue to the summary page.</span></span>

<span data-ttu-id="4bb83-141">[![Fókusstilling með síum](./media/focus-model-with-filters.png)](./media/focus-model-with-filters.png)</span><span class="sxs-lookup"><span data-stu-id="4bb83-141">[![Focus model with filters](./media/focus-model-with-filters.png)](./media/focus-model-with-filters.png)</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
