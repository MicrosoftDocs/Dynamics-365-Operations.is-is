---
title: Eftirlit með nákvæmni spár
description: Þetta efni lýsir gerðum nákvæmnispáa sem Dynamics 365 Supply Chain Management reiknar, og útskýrir hvernig hægt er að skoða nákvæmnigildin.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanForecastDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 72863
ms.assetid: 810a0d63-f4c6-4167-b2b3-a178b74ead89
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4cf65826279f0741ce5abc89d8f15bfec98c83ef
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/18/2019
ms.locfileid: "2813685"
---
# <a name="monitor-forecast-accuracy"></a><span data-ttu-id="e94ae-103">Eftirlit með nákvæmni spár</span><span class="sxs-lookup"><span data-stu-id="e94ae-103">Monitor forecast accuracy</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e94ae-104">Þetta efni lýsir gerðum nákvæmnispáa sem Microsoft Dynamics 365 Supply Chain Management reiknar, og útskýrir hvernig hægt er að skoða nákvæmnigildin.</span><span class="sxs-lookup"><span data-stu-id="e94ae-104">This topic describes the types of forecast accuracy that Microsoft Dynamics 365 Supply Chain Management calculates, and explains how you can view the accuracy values.</span></span>

<span data-ttu-id="e94ae-105">Supply Chain Management reiknar eftirfarandi gerðir af nákvæmnispám:</span><span class="sxs-lookup"><span data-stu-id="e94ae-105">Supply Chain Management calculates the following types of forecast accuracy:</span></span>

-   <span data-ttu-id="e94ae-106">Söguleg nákvæmni spár, með því að bera saman sögulega spá sem notar Aðaláætlanagerð með sögulega eftirspurn.</span><span class="sxs-lookup"><span data-stu-id="e94ae-106">Historical forecast accuracy, by comparing the historical forecast that Master Planning uses with the historical demand.</span></span> <span data-ttu-id="e94ae-107">Til að skoða gildi (bæði raungildi og prósentugildi) fyrir sögulega nákvæmni spár er smellt á **Sýna nákvæmni** á **Upplýsingar eftirspurnarspár** síðunni.</span><span class="sxs-lookup"><span data-stu-id="e94ae-107">To view the values (both absolute values and percentage values) for historical forecast accuracy, click **Show accuracy** on the **Demand forecast details** page.</span></span>
-   <span data-ttu-id="e94ae-108">Áætlaðuð nákvæmni spárlíkans sem er notað til að mynda spár.</span><span class="sxs-lookup"><span data-stu-id="e94ae-108">The estimated accuracy of the forecasting model that is used to generate the predictions.</span></span> <span data-ttu-id="e94ae-109">Hægt er að skoða nákvæmnihlutfall undir **Líkan upplýsingar - MAPE** á **Upplýsingar eftirspurnarspár** síðunni.</span><span class="sxs-lookup"><span data-stu-id="e94ae-109">You can view the accuracy percentage under **Model details - MAPE** on the **Demand forecast details** page.</span></span> 

> [!NOTE]
> <span data-ttu-id="e94ae-110">Ef þú notar eftirspurnarspár Microsoft Azure vélnámsþjónustunnar byggist útreikningur á nákvæmni innri líkans á prófunargagnasafni.</span><span class="sxs-lookup"><span data-stu-id="e94ae-110">If you use the Demand forecasting Microsoft Azure Machine Learning service, the calculation of internal model accuracy is based on the test data set.</span></span> <span data-ttu-id="e94ae-111">Til að tilgreina stærð prófunargagnasafns er stillt á **TEST\_SET\_SIZE\_PERCENT** færibreyta á **Færibreytur eftirspurnarspár síðu**.</span><span class="sxs-lookup"><span data-stu-id="e94ae-111">To specify the size of the test data set, set the **TEST\_SET\_SIZE\_PERCENT** parameter on the **Demand forecasting parameters** page.</span></span> <span data-ttu-id="e94ae-112">Til dæmis, ef virðið er stillt á **20**, munu síðustu 20°prósent sögulegra gagna verða notuð til að reikna út nákvæmni innra líkans.</span><span class="sxs-lookup"><span data-stu-id="e94ae-112">For example, if you set the value to **20**, the last 20 percent of the historical data will be used to calculate the internal model accuracy.</span></span>


<a name="additional-resources"></a><span data-ttu-id="e94ae-113">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="e94ae-113">Additional resources</span></span>
--------

[<span data-ttu-id="e94ae-114">Leiðrétt spá heimiluð</span><span class="sxs-lookup"><span data-stu-id="e94ae-114">Authorize an adjusted forecast</span></span>](authorize-adjusted-forecast.md)

[<span data-ttu-id="e94ae-115">Fjarlægja einfara úr sögulegum færslugögnum við útreikning á eftirspurnarspá</span><span class="sxs-lookup"><span data-stu-id="e94ae-115">Remove outliers from historical transaction data when calculating a demand forecast</span></span>](remove-historical-outliers-calculating-demand-forecast.md)



