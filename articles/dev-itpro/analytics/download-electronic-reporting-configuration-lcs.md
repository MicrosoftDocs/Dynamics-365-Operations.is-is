---
title: Hlaða niður Grunnstillingar fyrir rafræna skýrslugerð úr Lifecycle Services
description: Þetta kennsluefni útskýrir hvernig á að hlaða niður forstillingum Rafrænnar skýrslugerðar (ER) úr Microsoft Dynamics Lifecycle Services (LCS).
author: NickSelin
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionImport, ERWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 8686d2639a3ab7f2e79944cc5eed51571d463261
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1550423"
---
# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a><span data-ttu-id="679ce-103">Niðurhal skilgreininga fyrir rafræna skýrslugerð af Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="679ce-103">Download Electronic reporting configurations from Lifecycle Services</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="679ce-104">Þetta kennsluefni útskýrir hvernig á að hlaða niður forstillingum Rafrænnar skýrslugerðar (ER) úr Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="679ce-104">This topic explains how to download Electronic reporting (ER) configurations from Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="679ce-105">Þetta kennsluefni leiðbeinir þér við ferli til að sækja nýjustu útgáfu forstillinga Rafræna skýrslugerð (ER) úr Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="679ce-105">This tutorial guides you through the process of downloading the newest version of Electronic reporting (ER) configurations from Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="679ce-106">Skráðu þig inn á Finance and Operations með því að nota eitt af eftirfarandi hlutverkum:</span><span class="sxs-lookup"><span data-stu-id="679ce-106">Sign in to Finance and Operations by using one of the following roles:</span></span>

    - <span data-ttu-id="679ce-107">Þróunaraðili rafrænnar skýrslulausnar</span><span class="sxs-lookup"><span data-stu-id="679ce-107">Electronic reporting developer</span></span>
    - <span data-ttu-id="679ce-108">Hagnýtur ráðgjafi vegna rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="679ce-108">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="679ce-109">Kerfisstjóri</span><span class="sxs-lookup"><span data-stu-id="679ce-109">System administrator</span></span>

2. <span data-ttu-id="679ce-110">Farðu í **Fyrirtækisstjórnun** &gt; **Rafræn skýrslugerð**.</span><span class="sxs-lookup"><span data-stu-id="679ce-110">Go to **Organization administration** &gt; **Electronic reporting**.</span></span>
3. <span data-ttu-id="679ce-111">Í **veitandi skilgreininga** hlutanum, veljið gluggareitinn **Microsoft**</span><span class="sxs-lookup"><span data-stu-id="679ce-111">In the **Configuration providers** section, select the **Microsoft** tile.</span></span>
4. <span data-ttu-id="679ce-112">Á **Microsoft** gluggareit, er smellt á **gagnasöfn**.</span><span class="sxs-lookup"><span data-stu-id="679ce-112">On the **Microsoft** tile, click **Repositories**.</span></span>

    <span data-ttu-id="679ce-113">[![update-er-from-lcs-for-ms-open-ms-repositories-list](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)</span><span class="sxs-lookup"><span data-stu-id="679ce-113">[![update-er-from-lcs-for-ms-open-ms-repositories-list](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)</span></span>

5. <span data-ttu-id="679ce-114">Á **gagnasöfn skilgreininga** síðu í hnitanetinu skal velja fyrirliggjandi gagnasafn af gerðinni **LCS** .</span><span class="sxs-lookup"><span data-stu-id="679ce-114">On the **Configuration repositories** page, in the grid, select the existing repository of the **LCS** type.</span></span> <span data-ttu-id="679ce-115">Ef þessi gagnasafn birtist ekki í hnitanetinu skal fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="679ce-115">If this repository doesn't appear in the grid, follow these steps:</span></span>

    1. <span data-ttu-id="679ce-116">Smelltu á **Bæta við** til að bæta við nýju gagnasafni.</span><span class="sxs-lookup"><span data-stu-id="679ce-116">Click **Add** to add a new repository.</span></span>
    2. <span data-ttu-id="679ce-117">Veljið **LCS** sem gerð gagnasafns.</span><span class="sxs-lookup"><span data-stu-id="679ce-117">Select **LCS** as the repository type.</span></span>
    3. <span data-ttu-id="679ce-118">Smellið á **Stofna gagnasafn**.</span><span class="sxs-lookup"><span data-stu-id="679ce-118">Click **Create repository**.</span></span>
    4. <span data-ttu-id="679ce-119">Ef beðið er um það skal fylgja heimildarleiðbeiningunum.</span><span class="sxs-lookup"><span data-stu-id="679ce-119">If prompted, follow the authorization instructions.</span></span>
    5. <span data-ttu-id="679ce-120">Færa skal inn heiti og lýsingu fyrir gagnasafn.</span><span class="sxs-lookup"><span data-stu-id="679ce-120">Enter a name and description for the repository.</span></span>
    6. <span data-ttu-id="679ce-121">Smellið á **í lagi** til að staðfesta nýja færslu gagnasafns.</span><span class="sxs-lookup"><span data-stu-id="679ce-121">Click **OK** to confirm the new repository entry.</span></span>
    7. <span data-ttu-id="679ce-122">Í hnitanetinu, veljið nýtt gagnasafn af gerðinni **LCS** .</span><span class="sxs-lookup"><span data-stu-id="679ce-122">In the grid, select the new repository of the **LCS** type.</span></span>

6. <span data-ttu-id="679ce-123">Smellið á **Opna** til að skoða lista yfir skilgreiningar rafrænnar skýrslugerðar (ER) fyrir valda gagnasafn.</span><span class="sxs-lookup"><span data-stu-id="679ce-123">Click **Open** to view the list of ER configurations for the selected repository.</span></span>

    <span data-ttu-id="679ce-124">[![update-er-from-lcs-for-ms-make-lcs-repository](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)</span><span class="sxs-lookup"><span data-stu-id="679ce-124">[![update-er-from-lcs-for-ms-make-lcs-repository](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)</span></span>

7. <span data-ttu-id="679ce-125">Í skilgreiningatrénu í vinstri rúðunni er valið skilgreining ER sem þig vantar.</span><span class="sxs-lookup"><span data-stu-id="679ce-125">In the configurations tree in the left pane, select the ER configuration that you require.</span></span>
8. <span data-ttu-id="679ce-126">Á flýtiflipanum **Útgáfur** skal velja nauðsynlega útgáfu skilgreiningar rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="679ce-126">On the **Versions** FastTab, select the required version of the selected ER configuration.</span></span>
9. <span data-ttu-id="679ce-127">Smellið á **Innflutning** til að sækja valda útgáfu úr LCS í núverandi tilvik Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="679ce-127">Click **Import** to download the selected version from LCS to the current Finance and Operations instance.</span></span>

    > [!NOTE]
    > <span data-ttu-id="679ce-128">Hnappurinn **Innflutningur** er ekki tiltækur fyrir útgáfur skilgreininga rafrænnar skýrslugerðar sem þegar eru til staðar í gildandi tilviki Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="679ce-128">The **Import** button is unavailable for ER configuration versions that are already present in the current Finance and Operations instance.</span></span>

    <span data-ttu-id="679ce-129">[![update-er-from-lcs-for-ms-download-configuration](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)</span><span class="sxs-lookup"><span data-stu-id="679ce-129">[![update-er-from-lcs-for-ms-download-configuration](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)</span></span>

> [!NOTE]
> <span data-ttu-id="679ce-130">Það fer eftir stillingum rafrænnar skýrslugerðar hvernig skilgreiningar eru villuleitaðar eftir að þær eru fluttar inn.</span><span class="sxs-lookup"><span data-stu-id="679ce-130">Depending on the ER settings, configurations are validated after they are imported.</span></span> <span data-ttu-id="679ce-131">Notandi gæti verið látinn vita um vandamál ósamræmi sem fundust.</span><span class="sxs-lookup"><span data-stu-id="679ce-131">You might be notified about any inconsistency issues that are discovered.</span></span> <span data-ttu-id="679ce-132">Leysa þarf úr vandamálunum áður en hægt er að nota innflutta útgáfu skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="679ce-132">You must resolve those issues before you can use the imported configuration version.</span></span> <span data-ttu-id="679ce-133">Nánari upplýsingar, sjá lista yfir tengdar greinum fyrir þetta efni.</span><span class="sxs-lookup"><span data-stu-id="679ce-133">For more information, see the list of related articles for this topic.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="679ce-134">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="679ce-134">Additional resources</span></span>

[<span data-ttu-id="679ce-135">Yfirlit yfir rafræna skýrslugerð</span><span class="sxs-lookup"><span data-stu-id="679ce-135">Electronic reporting overview</span></span>](general-electronic-reporting.md)
