---
title: "Fylgjast með nákvæmni spár"
description: "Þessi grein lýsir gerðum nákvæmnispáa sem Microsoft Microsoft Dynamics 365 for Finance and Operations reiknar, og útskýrir hvernig hægt er að skoða nákvæmnigildin."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 72863
ms.assetid: 810a0d63-f4c6-4167-b2b3-a178b74ead89
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: c2f9482a9906ad6c607d275769ac06b29b22c25d
ms.contentlocale: is-is
ms.lasthandoff: 08/29/2017

---

# <a name="monitor-forecast-accuracy"></a><span data-ttu-id="cf848-103">Fylgjast með nákvæmni spár</span><span class="sxs-lookup"><span data-stu-id="cf848-103">Monitor forecast accuracy</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="cf848-104">Þessi grein lýsir gerðum nákvæmnispáa sem Microsoft Microsoft Dynamics 365 for Finance and Operations reiknar, og útskýrir hvernig hægt er að skoða nákvæmnigildin.</span><span class="sxs-lookup"><span data-stu-id="cf848-104">This article describes the types of forecast accuracy that Microsoft Dynamics 365 for Finance and Operations calculates, and explains how you can view the accuracy values.</span></span>

<span data-ttu-id="cf848-105">Finance and Operations reiknar eftirfarandi gerðir af nákvæmnispám:</span><span class="sxs-lookup"><span data-stu-id="cf848-105">Finance and Operations calculates the following types of forecast accuracy:</span></span>

-   <span data-ttu-id="cf848-106">Söguleg nákvæmni spár, með því að bera saman sögulega spá sem notar Aðaláætlanagerð með sögulega eftirspurn.</span><span class="sxs-lookup"><span data-stu-id="cf848-106">Historical forecast accuracy, by comparing the historical forecast that Master Planning uses with the historical demand.</span></span> <span data-ttu-id="cf848-107">Til að skoða gildi (bæði raungildi og prósentugildi) fyrir sögulega nákvæmni spár er smellt á **Sýna nákvæmni** á **Upplýsingar eftirspurnarspár** síðunni.</span><span class="sxs-lookup"><span data-stu-id="cf848-107">To view the values (both absolute values and percentage values) for historical forecast accuracy, click **Show accuracy** on the **Demand forecast details** page.</span></span>
-   <span data-ttu-id="cf848-108">Áætlaðuð nákvæmni spárlíkans sem er notað til að mynda spár.</span><span class="sxs-lookup"><span data-stu-id="cf848-108">The estimated accuracy of the forecasting model that is used to generate the predictions.</span></span> <span data-ttu-id="cf848-109">Hægt er að skoða nákvæmnihlutfall undir **Líkan upplýsingar - MAPE** á **Upplýsingar eftirspurnarspár** síðunni.</span><span class="sxs-lookup"><span data-stu-id="cf848-109">You can view the accuracy percentage under **Model details - MAPE** on the **Demand forecast details** page.</span></span> 

<span data-ttu-id="cf848-110">**Athugaðu:** Ef þú notar eftirspurnarspár í Finance and Operations Microsoft Azure Machine Learning þjónustu, byggist útreikningur á nákvæmni innra líkans á prófunargagnsafni.</span><span class="sxs-lookup"><span data-stu-id="cf848-110">**Note:** If you use the Finance and Operations Demand forecasting Microsoft Azure Machine Learning service, the calculation of internal model accuracy is based on the test data set.</span></span> <span data-ttu-id="cf848-111">Til að tilgreina stærð prófunargagnasafns er stillt á **TEST\_SET\_ SIZE\_ PERCENT** færibreyta á **Færibreytur eftirspurnarspár síðu**.</span><span class="sxs-lookup"><span data-stu-id="cf848-111">To specify the size of the test data set, set the **TEST\_SET\_SIZE\_PERCENT** parameter on the **Demand forecasting parameters** page.</span></span> <span data-ttu-id="cf848-112">Til dæmis, ef virðið er stillt á **20**, munu síðustu 20°prósent sögulegra gagna verða notuð til að reikna út nákvæmni innra líkans.</span><span class="sxs-lookup"><span data-stu-id="cf848-112">For example, if you set the value to **20**, the last 20 percent of the historical data will be used to calculate the internal model accuracy.</span></span>


<a name="see-also"></a><span data-ttu-id="cf848-113">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="cf848-113">See also</span></span>
--------

[<span data-ttu-id="cf848-114">Heimila leiðrétta spá</span><span class="sxs-lookup"><span data-stu-id="cf848-114">Authorizing the adjusted forecast</span></span>](authorize-adjusted-forecast.md)

[<span data-ttu-id="cf848-115">Fjarlægja frávik úr sögulegum færslugögn við útreikning á eftirspurnarspá</span><span class="sxs-lookup"><span data-stu-id="cf848-115">Remove outliers from historical transaction data when calculating a demand forecast</span></span>](remove-historical-outliers-calculating-demand-forecast.md)




