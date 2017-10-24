---
title: "Fjarlægja frávik úr sögulegum færslugögn við útreikning á eftirspurnarspá"
description: "Þessi grein lýsir hvernig á að útiloka frávik frá sögulegum gögnum sem eru notuð við útreikning á eftirspurnarspá. Með því útiloka einfara er hægt að auka nákvæmni eftirspurnarspár."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqDemPlanForecastParameters, ReqDemPlanOutlierQuerySetup
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 72621
ms.assetid: 88a964af-14eb-4c5c-945b-388e5908362c
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: ea3f08b20e25af6ebb738c2373b65532d74a0c80
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---

# <a name="remove-outliers-from-historical-transaction-data-when-calculating-a-demand-forecast"></a><span data-ttu-id="16b74-104">Fjarlægja frávik úr sögulegum færslugögn við útreikning á eftirspurnarspá</span><span class="sxs-lookup"><span data-stu-id="16b74-104">Remove outliers from historical transaction data when calculating a demand forecast</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="16b74-105">Þessi grein lýsir hvernig á að útiloka frávik frá sögulegum gögnum sem eru notuð við útreikning á eftirspurnarspá.</span><span class="sxs-lookup"><span data-stu-id="16b74-105">This article describes how to exclude outliers from the historical data that is used to calculate a demand forecast.</span></span> <span data-ttu-id="16b74-106">Með því útiloka einfara er hægt að auka nákvæmni eftirspurnarspár.</span><span class="sxs-lookup"><span data-stu-id="16b74-106">By excluding outliers, you can improve forecast accuracy.</span></span>

<span data-ttu-id="16b74-107">Með því útiloka frávik er hægt að auka nákvæmni spár.</span><span class="sxs-lookup"><span data-stu-id="16b74-107">You can exclude outliers to improve forecast accuracy.</span></span> <span data-ttu-id="16b74-108">Þetta verk er valfrjálst.</span><span class="sxs-lookup"><span data-stu-id="16b74-108">This is an optional task.</span></span> <span data-ttu-id="16b74-109">Hér er yfirlit yfir ferlið:</span><span class="sxs-lookup"><span data-stu-id="16b74-109">Here is an overview of the process:</span></span>

1.  <span data-ttu-id="16b74-110">Smellið á **Aðaláætlanagerð** &gt; **Uppsetning** &gt; **Eftirspurnarspár** &gt; **Frávik fjarlægt** til að opna síðuna **Frávik fjarlægt** þar sem hægt er að nota fyrirspurn til að velja færslur til að útiloka.</span><span class="sxs-lookup"><span data-stu-id="16b74-110">Click **Master planning** &gt; **Setup** &gt; **Demand forecasting** &gt; **Outlier removal** to open the **Outlier removal** page, where you can use a query to select the transactions to exclude.</span></span>
2.  <span data-ttu-id="16b74-111">Veljið fyrirtækið sem fyrirspurnin á við og færið svo inn nafn og lýsingu.</span><span class="sxs-lookup"><span data-stu-id="16b74-111">Select the company that the query applies to, and then enter a name and description.</span></span> <span data-ttu-id="16b74-112">Reiturinn **Dagsetning fyrirspurnar** er sjálfkrafa stilltur á Virkt.</span><span class="sxs-lookup"><span data-stu-id="16b74-112">The **Query date** field is automatically set to the current date.</span></span>
3.  <span data-ttu-id="16b74-113">Velja skal gátreitinn **Virkur** gátreit til að útiloka færslur sem fyrirspurnin finnur í sögulegum gögnum.</span><span class="sxs-lookup"><span data-stu-id="16b74-113">Select the **Active** check box to exclude the transactions that the query finds from the historical data.</span></span> <span data-ttu-id="16b74-114">Þessi stilling tekur gildi þegar grunnlínuspá er stofnuð.</span><span class="sxs-lookup"><span data-stu-id="16b74-114">This setting will take effect when you create a baseline forecast.</span></span>
4.  <span data-ttu-id="16b74-115">Á síðunni **Fjarlægingarfyrirspurn fyrir einfara** er hægt að bæta við, fjarlægja og velja skilyrði sem skilgreina hvaða færslur verða útilokaðar þegar grunnspá er reiknuð.</span><span class="sxs-lookup"><span data-stu-id="16b74-115">On the **Outlier removal query** page, you can add, remove, and select the criteria that define which transactions will be excluded when the baseline forecast is calculated.</span></span> <span data-ttu-id="16b74-116">Til dæmis, veljið tiltekna vöru eða pöntunarfærslu sem á að útiloka.</span><span class="sxs-lookup"><span data-stu-id="16b74-116">For example, select a specific item or order transaction to exclude.</span></span>
5.  <span data-ttu-id="16b74-117">Smellt er á **Birta færslur**.</span><span class="sxs-lookup"><span data-stu-id="16b74-117">Click **Display transactions**.</span></span> <span data-ttu-id="16b74-118">Skjámyndin **Færslur einfara** listar færslur sem uppfylla þau skilyrði sem er skilgreind í fyrirspurninni og mun vera útilokuð frá rannsóknarsöguleg gögn þegar eftirspurnarspá er reiknað.</span><span class="sxs-lookup"><span data-stu-id="16b74-118">The **Outlier transactions** page lists the transactions that meet the criteria that you defined in the query, and that will be excluded from the historical data when the demand forecast is calculated.</span></span>

<span data-ttu-id="16b74-119">**Ábending:** Einnig er hægt að stofna fyrirspurn sem er byggð á fyrirliggjandi fyrirspurn.</span><span class="sxs-lookup"><span data-stu-id="16b74-119">**Note:** You can also create a query that is based on an existing query.</span></span> <span data-ttu-id="16b74-120">Velja skal fyrirspurn sem á að afrita og smella á **Afrita**.</span><span class="sxs-lookup"><span data-stu-id="16b74-120">Select the query to copy, and then click **Duplicate**.</span></span> <span data-ttu-id="16b74-121">Reiturinn **Dagsetning fyrirspurnar** auðkennir útgáfunar.</span><span class="sxs-lookup"><span data-stu-id="16b74-121">The **Query date** field identifies the version.</span></span> <span data-ttu-id="16b74-122">Hægt er að nota fyrirspurnina eins og hún er eða smella á **Breyta fyrirspurn** til að breyta skilyrðum.</span><span class="sxs-lookup"><span data-stu-id="16b74-122">You can use the query as it is, or you can click **Edit query** to modify the criteria.</span></span> <span data-ttu-id="16b74-123">Einnig er hægt að breyta heiti og lýsingu á nýrri fyrirspurn.</span><span class="sxs-lookup"><span data-stu-id="16b74-123">You can optionally modify the name and description of the new query.</span></span>

<a name="see-also"></a><span data-ttu-id="16b74-124">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="16b74-124">See also</span></span>
--------

[<span data-ttu-id="16b74-125">Kynning á eftirspurnarspá</span><span class="sxs-lookup"><span data-stu-id="16b74-125">Introduction to demand forecasting</span></span>](introduction-demand-forecasting.md)

[<span data-ttu-id="16b74-126">Fylgjast með nákvæmni spár</span><span class="sxs-lookup"><span data-stu-id="16b74-126">Monitoring forecast accuracy</span></span>](monitor-forecast-accuracy.md)




