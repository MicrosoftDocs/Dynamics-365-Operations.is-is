---
title: Úrræðaleit fínstillingar áætlanagerðar
description: Þetta efnisatriði lýsir því hvernig á að leysa vandamál sem kunna að koma upp á meðan unnið er með fínstillingu áætlanagerðar.
author: ChristianRytt
manager: tfehr
ms.date: 05/07/2020
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
ms.search.validFrom: 2020-5-7
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: c3dd0bf262f65aac2359c05ff954bdfbd294353f
ms.sourcegitcommit: 89022f39502b19c24c0997ae3a01a64b93280f42
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/12/2020
ms.locfileid: "3367002"
---
# <a name="troubleshoot-planning-optimization"></a><span data-ttu-id="614c3-103">Úrræðaleit fínstillingar áætlanagerðar</span><span class="sxs-lookup"><span data-stu-id="614c3-103">Troubleshoot Planning Optimization</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="614c3-104">Þetta efnisatriði lýsir því hvernig á að laga almenn vandamál sem kunna að koma upp þegar unnið er með fínstillingu áætlanagerðar.</span><span class="sxs-lookup"><span data-stu-id="614c3-104">This topic describes how to fix common issues that you might encounter while working with Planning Optimization.</span></span>

## <a name="installation-of-the-planning-optimization-add-in-doesnt-complete"></a><span data-ttu-id="614c3-105">Uppsetningu á innbót fínstilling áætlanagerðar er ekki lokið</span><span class="sxs-lookup"><span data-stu-id="614c3-105">Installation of the Planning Optimization add-in doesn't complete</span></span>

<span data-ttu-id="614c3-106">Fínstilling áætlanagerðar krefst þess að kveikt sé á Lifecycle Services (LCS), virkt umhverfi, á stigi 2 eða hærra (ekki OneBox-umhverfi), með Dynamics 365 Supply Chain Management-útgáfu 10.0.7 eða nýrri.</span><span class="sxs-lookup"><span data-stu-id="614c3-106">Planning Optimization requires a Lifecycle Services (LCS) enabled, high-availability environment, tier 2 or higher (not a OneBox environment), with Dynamics 365 Supply Chain Management version 10.0.7 or later.</span></span> <span data-ttu-id="614c3-107">Ef reynt er að setja upp innbótina í OneBox-umhverfi verður uppsetningunni ekki lokið.</span><span class="sxs-lookup"><span data-stu-id="614c3-107">If you try to install the add-in on a OneBox environment, the installation won't complete.</span></span>

<span data-ttu-id="614c3-108">**Lagfæra**: hætta við uppsetninguna og nota umhverfi með miklum tiltækileika, lag 2 eða hærra (ekki OneBox-umhverfi).</span><span class="sxs-lookup"><span data-stu-id="614c3-108">**Fix**: Cancel the installation and use a high-availability environment, tier 2 or higher (not a OneBox environment).</span></span>

## <a name="planning-of-batch-jobs-fails-when-planning-optimization-is-enabled"></a><span data-ttu-id="614c3-109">Áætlun um runuvinnslur mistekst þegar fínstilling áætlanagerðar er virk</span><span class="sxs-lookup"><span data-stu-id="614c3-109">Planning of batch jobs fails when Planning Optimization is enabled</span></span>

<span data-ttu-id="614c3-110">Þegar fínstilling áætlanagerðar er gerð virk er innbyggð aðaláætlunargerðarkerfi sjálfkrafa gerð óvirk.</span><span class="sxs-lookup"><span data-stu-id="614c3-110">When you enable Planning Optimization, the built-in master planning engine is automatically disabled.</span></span> <span data-ttu-id="614c3-111">Runuvinnslur aðaláætlanagerðar sem voru búnar til fyrir innbyggt áætlunarkerfi Supply Chain Management mistekst ef þær eru ræstar þegar fínstilling áætlanagerðar er virk.</span><span class="sxs-lookup"><span data-stu-id="614c3-111">Master planning batch jobs that were created for the built-in Supply Chain Management planning engine will fail if they are triggered while Planning Optimization is enabled.</span></span> <span data-ttu-id="614c3-112">Hugsanlega birtast villuboð á borð við *Þessi aðgerð ræsti aðaláætlanagerð sem er ekki studd þegar fínstilling áætlunar er virk*.</span><span class="sxs-lookup"><span data-stu-id="614c3-112">You may receive an error message such as *This operation triggered master planning that isn't supported when Planning Optimization is enabled*.</span></span>

<span data-ttu-id="614c3-113">**Lagfæra**: hætta við allar runuvinnslur Supply Chain Management sem voru stofnaðar fyrir innbyggt áætlunarkerfi aðfangakeðjustjórnunar.</span><span class="sxs-lookup"><span data-stu-id="614c3-113">**Fix**: Cancel all master planning batch jobs that were created for the built-in Supply Chain Management planning engine.</span></span>

## <a name="planning-optimization-results-are-different-from-earlier-results"></a><span data-ttu-id="614c3-114">Niðurstöður fínstillingar áætlunargerðar eru frábrugðnar fyrri niðurstöðum</span><span class="sxs-lookup"><span data-stu-id="614c3-114">Planning Optimization results are different from earlier results</span></span>

<span data-ttu-id="614c3-115">Fínstilling áætlanagerðar er frábrugðin hönnun innbyggðar aðaláætlanagerðar á sumum svæðum.</span><span class="sxs-lookup"><span data-stu-id="614c3-115">Planning Optimization differs from the built-in master planning design in some areas.</span></span> <span data-ttu-id="614c3-116">Þetta getur einnig stafað af eiginleikum í bið.</span><span class="sxs-lookup"><span data-stu-id="614c3-116">This can also be caused by pending features.</span></span>

<span data-ttu-id="614c3-117">**Lagfæra**: keyra samræmisgreiningu á fínstillingu áætlanagerðar og greina síðan niðurstöðurnar þegar vísað er í tengd fylgiskjöl til að skilja áhrifin.</span><span class="sxs-lookup"><span data-stu-id="614c3-117">**Fix**: Run Planning Optimization fit analysis and then analyze the results while referring to the related documentation to understand the impact.</span></span> <span data-ttu-id="614c3-118">Frekari upplýsingar er að finna í [Greining á samsvörun áætlunarfínstillingar](planning-optimization-fit-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="614c3-118">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

## <a name="master-planning-doesnt-respect-the-coverage-time-fence"></a><span data-ttu-id="614c3-119">Aðaláætlanagerð virðir ekki tímamörk fyrir umfang</span><span class="sxs-lookup"><span data-stu-id="614c3-119">Master planning doesn't respect the coverage time fence</span></span>

<span data-ttu-id="614c3-120">Þetta stafar af því að eiginleiki er í bið vegna fínstillingar áætlanagerðar.</span><span class="sxs-lookup"><span data-stu-id="614c3-120">This is caused by a pending feature for Planning Optimization.</span></span>

<span data-ttu-id="614c3-121">**Lagfæra**: þar til eiginleiki í bið er tiltækur skal sía eða eyða áætluðum pöntunum til að fjarlægja framboðstillögur utan tímamörk fyrir umfang.</span><span class="sxs-lookup"><span data-stu-id="614c3-121">**Fix**: Until the pending feature is available, filter or delete planned orders to remove supply suggestions outside of the coverage time fence.</span></span>

## <a name="cant-enable-planning-optimization"></a><span data-ttu-id="614c3-122">Ekki hægt að virkja fínstillingu áætlanagerðar</span><span class="sxs-lookup"><span data-stu-id="614c3-122">Can't enable Planning Optimization</span></span>

<span data-ttu-id="614c3-123">**Tengingarstaðan** verður að vera **Tengdur** áður en hægt er að stilla **Nota fínstillingu áætlanagerðar** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="614c3-123">The **Connection status** must be **Connected** before you can set **Use Planning Optimization** to **Yes**.</span></span> <span data-ttu-id="614c3-124">Frekari upplýsingar er að finna í [Hafist handa með fínstillingu skipulags](get-started.md).</span><span class="sxs-lookup"><span data-stu-id="614c3-124">For more information, see [Get started with Planning Optimization](get-started.md).</span></span>

<span data-ttu-id="614c3-125">**Lagfæra**: Gangið úr skugga um að innbót fínstillingar áætlanagerðar hafi verið uppsett.</span><span class="sxs-lookup"><span data-stu-id="614c3-125">**Fix**: Make sure that the Planning Optimization add-in was installed successfully.</span></span>

## <a name="error-message-is-shown-during-ctp"></a><span data-ttu-id="614c3-126">Villuboð eru sýnd í CTP</span><span class="sxs-lookup"><span data-stu-id="614c3-126">Error message is shown during CTP</span></span>

<span data-ttu-id="614c3-127">Ef reynt er að keyra afhendingargetu (CTP) frá sölupöntun þegar fínstilling áætlanagerðar er virk birtast eftirfarandi villuboð: *Þessi aðgerð ræsti aðaláætlanagerð sem er ekki studd þegar fínstilling áætlanagerðar er virk*.</span><span class="sxs-lookup"><span data-stu-id="614c3-127">If you try to run capable to promise (CTP) from a sales order when Planning Optimization is enabled, you will receive the following error message: *This operation triggered master planning that isn't supported when the Planning Optimization is enabled*.</span></span>

<span data-ttu-id="614c3-128">Þetta tengist eiginleika í bið sem er áætlaður sem hluti af stuðningi við framleiðslupantanir.</span><span class="sxs-lookup"><span data-stu-id="614c3-128">This is related to a pending feature that is planned as part of the support for production orders.</span></span>

<span data-ttu-id="614c3-129">**Lagfæra:** forðast CTP-útreikninga þegar fínstilling áætlanagerðar er virk þar til stuðningur við CTP er tiltækur.</span><span class="sxs-lookup"><span data-stu-id="614c3-129">**Fix:** Avoid CTP calculations when Planning Optimization is enabled until CTP support is available.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="614c3-130">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="614c3-130">Additional resources</span></span>

[<span data-ttu-id="614c3-131">Hafist handa með fínstillingu áætlanagerðar</span><span class="sxs-lookup"><span data-stu-id="614c3-131">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="614c3-132">Samræmisgreining á fínstillingu áætlanagerðar</span><span class="sxs-lookup"><span data-stu-id="614c3-132">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)
