---
title: Greining á samsvörun áætlunarfínstillingar
description: Þetta efni útskýrir hvernig á að sannreyna núverandi uppsetningu og gögn gagnvart getu virkni fínstillingar skipulagningar.
author: ChristianRytt
manager: tfehr
ms.date: 10/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 17114d4c0ef2c74ab1bb56d41e4a008150c21f36
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208755"
---
# <a name="planning-optimization-fit-analysis"></a><span data-ttu-id="afd5f-103">Greining á samsvörun áætlunarfínstillingar</span><span class="sxs-lookup"><span data-stu-id="afd5f-103">Planning Optimization fit analysis</span></span>

[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

<span data-ttu-id="afd5f-104">Til að sjá hversu samhæf núverandi uppsetning og gögn eru við virkni fínstillingar áætlunarinnar ferðu í **Aðaláætlunargerð** \> **Uppsetning** \> **Greining á samsvörun áætlunarfínstillingar** og veldu síðan **Keyra greiningu**.</span><span class="sxs-lookup"><span data-stu-id="afd5f-104">To see how compatible your current setup and data are with the Planning Optimization functionality, go to **Master planning** \> **Setup** \> **Planning Optimization fit analysis**, and then select **Run analysis**.</span></span> <span data-ttu-id="afd5f-105">Ef greiningin finnur fyrir ósamræmi eru þau skráð á sömu síðu.</span><span class="sxs-lookup"><span data-stu-id="afd5f-105">If the analysis finds any inconsistencies, they are listed on the same page.</span></span> <span data-ttu-id="afd5f-106">(Greiningin getur tekið nokkrar mínútur í keyrslu.)</span><span class="sxs-lookup"><span data-stu-id="afd5f-106">(The analysis can take a few minutes to run.)</span></span>

> [!NOTE]
> <span data-ttu-id="afd5f-107">Ef ósamræmi finnst, getur þú samt notað fínstillingu skipulagsins.</span><span class="sxs-lookup"><span data-stu-id="afd5f-107">If inconsistencies are found, you can still use Planning Optimization.</span></span> <span data-ttu-id="afd5f-108">Niðurstöður samsvörunargreiningar sýna bara staði þar sem skipulagsþjónustan mun ekki heiðra núverandi uppsetningu.</span><span class="sxs-lookup"><span data-stu-id="afd5f-108">The results of the fit analysis just show places where the planning service won't honor your current setup.</span></span> <span data-ttu-id="afd5f-109">Með öðrum orðum sýna þær staði þar sem einhver ferli kunna að vera hunsuð eða ekki studd.</span><span class="sxs-lookup"><span data-stu-id="afd5f-109">In other words, they show places where some processes might be ignored or might not be supported.</span></span>

## <a name="analysis-results-example-1"></a><span data-ttu-id="afd5f-110">Niðurstöður greiningar: Dæmi 1</span><span class="sxs-lookup"><span data-stu-id="afd5f-110">Analysis results: Example 1</span></span>

- <span data-ttu-id="afd5f-111">**Eiginleiki:** Framleiðsla</span><span class="sxs-lookup"><span data-stu-id="afd5f-111">**Feature:** Production</span></span>
- <span data-ttu-id="afd5f-112">**Mál:** Vörur með BOM-stig sem eru hærri en núll: 56</span><span class="sxs-lookup"><span data-stu-id="afd5f-112">**Issue:** Items with BOM level greater than zero: 56</span></span>
- <span data-ttu-id="afd5f-113">**Útskýring:** Í samsvörunargreiningunni fundust 56 vörur sem eru með uppsetningu uppskriftar (BOM) fyrir framleiðslu.</span><span class="sxs-lookup"><span data-stu-id="afd5f-113">**Explanation:** The fit analysis found 56 items that have a bill of materials (BOM) setup for production.</span></span> <span data-ttu-id="afd5f-114">Vegna þess að núverandi útgáfa af fínstillingu áætlunargerðar styður ekki framleiðslu mun fínstilling áætlunarinnar búa til innkaupatillögur í stað framleiðslutillaga.</span><span class="sxs-lookup"><span data-stu-id="afd5f-114">Because the current version of Planning Optimization doesn't support production, Planning Optimization will generate planned purchase orders instead of planned production orders.</span></span> <span data-ttu-id="afd5f-115">Hún mun einnig sýna viðvörun sem sýnir vörurnar sem varða fyrir áhrifum.</span><span class="sxs-lookup"><span data-stu-id="afd5f-115">It will also show a warning that lists the affected items.</span></span>

### <a name="analysis-results-example-2"></a><span data-ttu-id="afd5f-116">Niðurstöður greiningar: Dæmi 2</span><span class="sxs-lookup"><span data-stu-id="afd5f-116">Analysis results: Example 2</span></span>

- <span data-ttu-id="afd5f-117">**Eiginleiki:** Aðgerðir</span><span class="sxs-lookup"><span data-stu-id="afd5f-117">**Feature:** Actions</span></span>
- <span data-ttu-id="afd5f-118">**Mál:** Þekjuhópar með útreikninga á aðgerðum virkjaða: 6</span><span class="sxs-lookup"><span data-stu-id="afd5f-118">**Issue:** Coverage groups with actions calculation enabled: 6</span></span>
- <span data-ttu-id="afd5f-119">**Útskýring:** Samsvörunargreiningin fann sex þekjuhópa þar sem kveikt er á útreikningi á aðgerðum.</span><span class="sxs-lookup"><span data-stu-id="afd5f-119">**Explanation:** The fit analysis found six coverage groups where action calculation is turned on.</span></span> <span data-ttu-id="afd5f-120">Þar sem núverandi útgáfa af fínstillingu áætlunarinnar styður ekki aðgerðir verða engar aðgerðir myndaðar við aðalskipulagningu.</span><span class="sxs-lookup"><span data-stu-id="afd5f-120">Because the current version of Planning Optimization doesn't support actions, no actions will be generated during master planning.</span></span>

## <a name="related-resources"></a><span data-ttu-id="afd5f-121">Tengd tilföng</span><span class="sxs-lookup"><span data-stu-id="afd5f-121">Related resources</span></span>

[<span data-ttu-id="afd5f-122">Yfirlit yfir fínstillingu skipulagningar</span><span class="sxs-lookup"><span data-stu-id="afd5f-122">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="afd5f-123">Byrjaðu með hagræðingu skipulags</span><span class="sxs-lookup"><span data-stu-id="afd5f-123">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="afd5f-124">Skoða áætlunarsögu og skipulagsskrár</span><span class="sxs-lookup"><span data-stu-id="afd5f-124">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="afd5f-125">Nota síur á áætlun</span><span class="sxs-lookup"><span data-stu-id="afd5f-125">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="afd5f-126">Hætta við áætlunarvinnslu</span><span class="sxs-lookup"><span data-stu-id="afd5f-126">Cancel a planning job</span></span>](cancel-planning-job.md)
