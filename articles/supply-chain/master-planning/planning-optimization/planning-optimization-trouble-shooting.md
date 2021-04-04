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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-5-7
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 39583c244f09f54551d560e8b1dd9f1a5a1590cc
ms.sourcegitcommit: 72f70c81176e86cda714a4712525f73514c895b7
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/16/2021
ms.locfileid: "5457330"
---
# <a name="troubleshoot-planning-optimization"></a><span data-ttu-id="7bced-103">Úrræðaleit fínstillingar áætlanagerðar</span><span class="sxs-lookup"><span data-stu-id="7bced-103">Troubleshoot Planning Optimization</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7bced-104">Þetta efnisatriði lýsir því hvernig á að laga almenn vandamál sem kunna að koma upp þegar unnið er með fínstillingu áætlanagerðar.</span><span class="sxs-lookup"><span data-stu-id="7bced-104">This topic describes how to fix common issues that you might encounter while working with Planning Optimization.</span></span>

## <a name="installation-of-the-planning-optimization-add-in-doesnt-complete"></a><span data-ttu-id="7bced-105">Uppsetningu á innbót fínstilling áætlanagerðar er ekki lokið</span><span class="sxs-lookup"><span data-stu-id="7bced-105">Installation of the Planning Optimization add-in doesn't complete</span></span>

<span data-ttu-id="7bced-106">Fínstilling áætlanagerðar krefst þess að kveikt sé á Lifecycle Services (LCS), virkt umhverfi, á stigi 2 eða hærra (ekki OneBox-umhverfi), með Dynamics 365 Supply Chain Management-útgáfu 10.0.7 eða nýrri.</span><span class="sxs-lookup"><span data-stu-id="7bced-106">Planning Optimization requires a Lifecycle Services (LCS) enabled, high-availability environment, tier 2 or higher (not a OneBox environment), with Dynamics 365 Supply Chain Management version 10.0.7 or later.</span></span> <span data-ttu-id="7bced-107">Ef reynt er að setja upp innbótina í OneBox-umhverfi verður uppsetningunni ekki lokið.</span><span class="sxs-lookup"><span data-stu-id="7bced-107">If you try to install the add-in on a OneBox environment, the installation won't complete.</span></span>

<span data-ttu-id="7bced-108">**Lagfæra**: hætta við uppsetninguna og nota umhverfi með miklum tiltækileika, lag 2 eða hærra (ekki OneBox-umhverfi).</span><span class="sxs-lookup"><span data-stu-id="7bced-108">**Fix**: Cancel the installation and use a high-availability environment, tier 2 or higher (not a OneBox environment).</span></span>

## <a name="planning-of-batch-jobs-fails-when-planning-optimization-is-enabled"></a><span data-ttu-id="7bced-109">Áætlun um runuvinnslur mistekst þegar fínstilling áætlanagerðar er virk</span><span class="sxs-lookup"><span data-stu-id="7bced-109">Planning of batch jobs fails when Planning Optimization is enabled</span></span>

<span data-ttu-id="7bced-110">Þegar fínstilling áætlanagerðar er gerð virk er innbyggð aðaláætlunargerðarkerfi sjálfkrafa gerð óvirk.</span><span class="sxs-lookup"><span data-stu-id="7bced-110">When you enable Planning Optimization, the built-in master planning engine is automatically disabled.</span></span> <span data-ttu-id="7bced-111">Runuvinnslur aðaláætlanagerðar sem voru búnar til fyrir innbyggt áætlunarkerfi Supply Chain Management mistekst ef þær eru ræstar þegar fínstilling áætlanagerðar er virk.</span><span class="sxs-lookup"><span data-stu-id="7bced-111">Master planning batch jobs that were created for the built-in Supply Chain Management planning engine will fail if they are triggered while Planning Optimization is enabled.</span></span> <span data-ttu-id="7bced-112">Hugsanlega birtast villuboð á borð við *Þessi aðgerð ræsti aðaláætlanagerð sem er ekki studd þegar fínstilling áætlunar er virk*.</span><span class="sxs-lookup"><span data-stu-id="7bced-112">You may receive an error message such as *This operation triggered master planning that isn't supported when Planning Optimization is enabled*.</span></span>

<span data-ttu-id="7bced-113">**Lagfæra**: hætta við allar runuvinnslur Supply Chain Management sem voru stofnaðar fyrir innbyggt áætlunarkerfi aðfangakeðjustjórnunar.</span><span class="sxs-lookup"><span data-stu-id="7bced-113">**Fix**: Cancel all master planning batch jobs that were created for the built-in Supply Chain Management planning engine.</span></span>

## <a name="planning-optimization-results-are-different-from-earlier-results"></a><span data-ttu-id="7bced-114">Niðurstöður fínstillingar áætlunargerðar eru frábrugðnar fyrri niðurstöðum</span><span class="sxs-lookup"><span data-stu-id="7bced-114">Planning Optimization results are different from earlier results</span></span>

<span data-ttu-id="7bced-115">Fínstilling áætlanagerðar er frábrugðin hönnun innbyggðar aðaláætlanagerðar á sumum svæðum.</span><span class="sxs-lookup"><span data-stu-id="7bced-115">Planning Optimization differs from the built-in master planning design in some areas.</span></span> <span data-ttu-id="7bced-116">Þetta getur einnig stafað af eiginleikum í bið.</span><span class="sxs-lookup"><span data-stu-id="7bced-116">This can also be caused by pending features.</span></span>

<span data-ttu-id="7bced-117">**Lagfæra**: keyra samræmisgreiningu á fínstillingu áætlanagerðar og greina síðan niðurstöðurnar þegar vísað er í tengd fylgiskjöl til að skilja áhrifin.</span><span class="sxs-lookup"><span data-stu-id="7bced-117">**Fix**: Run Planning Optimization fit analysis and then analyze the results while referring to the related documentation to understand the impact.</span></span> <span data-ttu-id="7bced-118">Frekari upplýsingar er að finna í [Greining á samsvörun áætlunarfínstillingar](planning-optimization-fit-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="7bced-118">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

## <a name="cant-enable-planning-optimization"></a><span data-ttu-id="7bced-119">Ekki hægt að virkja fínstillingu áætlanagerðar</span><span class="sxs-lookup"><span data-stu-id="7bced-119">Can't enable Planning Optimization</span></span>

<span data-ttu-id="7bced-120">**Tengingarstaðan** verður að vera **Tengdur** áður en hægt er að stilla **Nota fínstillingu áætlanagerðar** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="7bced-120">The **Connection status** must be **Connected** before you can set **Use Planning Optimization** to **Yes**.</span></span> <span data-ttu-id="7bced-121">Frekari upplýsingar er að finna í [Hafist handa með fínstillingu skipulags](get-started.md).</span><span class="sxs-lookup"><span data-stu-id="7bced-121">For more information, see [Get started with Planning Optimization](get-started.md).</span></span>

<span data-ttu-id="7bced-122">**Lagfæra**: Gangið úr skugga um að innbót fínstillingar áætlanagerðar hafi verið uppsett.</span><span class="sxs-lookup"><span data-stu-id="7bced-122">**Fix**: Make sure that the Planning Optimization add-in was installed successfully.</span></span>

## <a name="error-message-is-shown-during-ctp"></a><span data-ttu-id="7bced-123">Villuboð eru sýnd í CTP</span><span class="sxs-lookup"><span data-stu-id="7bced-123">Error message is shown during CTP</span></span>

<span data-ttu-id="7bced-124">Ef reynt er að keyra afhendingargetu (CTP) frá sölupöntun þegar fínstilling áætlanagerðar er virk birtast eftirfarandi villuboð: *Þessi aðgerð ræsti aðaláætlanagerð sem er ekki studd þegar fínstilling áætlanagerðar er virk*.</span><span class="sxs-lookup"><span data-stu-id="7bced-124">If you try to run capable to promise (CTP) from a sales order when Planning Optimization is enabled, you will receive the following error message: *This operation triggered master planning that isn't supported when the Planning Optimization is enabled*.</span></span>

<span data-ttu-id="7bced-125">Þetta tengist eiginleika í bið sem er áætlaður sem hluti af stuðningi við framleiðslupantanir.</span><span class="sxs-lookup"><span data-stu-id="7bced-125">This is related to a pending feature that is planned as part of the support for production orders.</span></span>

<span data-ttu-id="7bced-126">**Lagfæra:** forðast CTP-útreikninga þegar fínstilling áætlanagerðar er virk þar til stuðningur við CTP er tiltækur.</span><span class="sxs-lookup"><span data-stu-id="7bced-126">**Fix:** Avoid CTP calculations when Planning Optimization is enabled until CTP support is available.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7bced-127">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="7bced-127">Additional resources</span></span>

[<span data-ttu-id="7bced-128">Hafist handa með fínstillingu áætlanagerðar</span><span class="sxs-lookup"><span data-stu-id="7bced-128">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="7bced-129">Samræmisgreining á fínstillingu áætlanagerðar</span><span class="sxs-lookup"><span data-stu-id="7bced-129">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]