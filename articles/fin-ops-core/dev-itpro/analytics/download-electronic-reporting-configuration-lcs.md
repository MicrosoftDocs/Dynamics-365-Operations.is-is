---
title: Hlaða niður Grunnstillingar fyrir rafræna skýrslugerð úr Lifecycle Services
description: Þetta kennsluefni útskýrir hvernig á að hlaða niður forstillingum Rafrænnar skýrslugerðar (ER) úr Microsoft Dynamics Lifecycle Services (LCS).
author: NickSelin
ms.date: 08/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionImport, ERWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 14f0f2b1a4d63101d432b1361379c61a70ac9345
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271184"
---
# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a><span data-ttu-id="b8d08-103">Niðurhal skilgreininga fyrir rafræna skýrslugerð af Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="b8d08-103">Download Electronic reporting configurations from Lifecycle Services</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b8d08-104">Þetta kennsluefni útskýrir hvernig á að hlaða niður nýjustu útgáfu [Rafrænnar skýrslugerðar (ER)](general-electronic-reporting.md#Configuration) úr [Samnýtt eignasafn](../lifecycle-services/asset-library.md) í Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="b8d08-104">This topic explains how to download the newest version of [Electronic reporting (ER) configurations](general-electronic-reporting.md#Configuration) from the [Shared asset library](../lifecycle-services/asset-library.md) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b8d08-105">Verið er að [úrelda](../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release) notkun LCS sem gagnageymslu fyrir skilgreiningar rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="b8d08-105">The use of LCS as a storage repository for ER configurations is being [deprecated](../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release).</span></span> <span data-ttu-id="b8d08-106">Frekari upplýsingar er að finna í [Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) úrelding á geymslu](../../../finance/localizations/rcs-lcs-repo-dep-faq.md).</span><span class="sxs-lookup"><span data-stu-id="b8d08-106">For more information, see [Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) storage deprecation](../../../finance/localizations/rcs-lcs-repo-dep-faq.md).</span></span>

1. <span data-ttu-id="b8d08-107">Skráðu þig inn í forritið með því að nota eitt af eftirfarandi hlutverkum:</span><span class="sxs-lookup"><span data-stu-id="b8d08-107">Sign in to the application by using one of the following roles:</span></span>

    - <span data-ttu-id="b8d08-108">Þróunaraðili rafrænnar skýrslulausnar</span><span class="sxs-lookup"><span data-stu-id="b8d08-108">Electronic reporting developer</span></span>
    - <span data-ttu-id="b8d08-109">Hagnýtur ráðgjafi vegna rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="b8d08-109">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="b8d08-110">Kerfisstjóri</span><span class="sxs-lookup"><span data-stu-id="b8d08-110">System administrator</span></span>

2. <span data-ttu-id="b8d08-111">Farðu í **Fyrirtækisstjórnun** &gt; **Vinnusvæði** &gt; **Rafræn skýrslugerð**.</span><span class="sxs-lookup"><span data-stu-id="b8d08-111">Go to **Organization administration** &gt; **Workspaces** &gt; **Electronic reporting**.</span></span>
3. <span data-ttu-id="b8d08-112">Í **veitandi skilgreininga** hlutanum, veljið gluggareitinn **Microsoft**</span><span class="sxs-lookup"><span data-stu-id="b8d08-112">In the **Configuration providers** section, select the **Microsoft** tile.</span></span>
4. <span data-ttu-id="b8d08-113">Í reitnum **Microsoft** skal velja **Geymslur**.</span><span class="sxs-lookup"><span data-stu-id="b8d08-113">On the **Microsoft** tile, select **Repositories**.</span></span>

    <span data-ttu-id="b8d08-114">[![Microsoft reitur á Skilgreiningasíðu staðfæringar](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)</span><span class="sxs-lookup"><span data-stu-id="b8d08-114">[![Microsoft tile on the Localization configurations page](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)</span></span>

5. <span data-ttu-id="b8d08-115">Á **gagnasöfn skilgreininga** síðu í hnitanetinu skal velja fyrirliggjandi gagnasafn af gerðinni **LCS** .</span><span class="sxs-lookup"><span data-stu-id="b8d08-115">On the **Configuration repositories** page, in the grid, select the existing repository of the **LCS** type.</span></span> <span data-ttu-id="b8d08-116">Ef þessi gagnasafn birtist ekki í hnitanetinu skal fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="b8d08-116">If this repository doesn't appear in the grid, follow these steps:</span></span>

    1. <span data-ttu-id="b8d08-117">Smellið á **Bæta við** til að bæta við geymslu.</span><span class="sxs-lookup"><span data-stu-id="b8d08-117">Select **Add** to add a repository.</span></span>
    2. <span data-ttu-id="b8d08-118">Veljið **LCS** sem gerð gagnasafns.</span><span class="sxs-lookup"><span data-stu-id="b8d08-118">Select **LCS** as the repository type.</span></span>
    3. <span data-ttu-id="b8d08-119">Veljið **Stofna geymslu**.</span><span class="sxs-lookup"><span data-stu-id="b8d08-119">Select **Create repository**.</span></span>
    4. <span data-ttu-id="b8d08-120">Ef þú ert beðinn um heimild skaltu fylgja leiðbeiningunum á skjánum.</span><span class="sxs-lookup"><span data-stu-id="b8d08-120">If you're prompted about authorization, follow the on-screen instructions.</span></span>
    5. <span data-ttu-id="b8d08-121">Færa skal inn heiti og lýsingu fyrir gagnasafn.</span><span class="sxs-lookup"><span data-stu-id="b8d08-121">Enter a name and description for the repository.</span></span>
    6. <span data-ttu-id="b8d08-122">Veldu **Í lagi** til að staðfesta nýja færslu gagnasafns.</span><span class="sxs-lookup"><span data-stu-id="b8d08-122">Select **OK** to confirm the new repository entry.</span></span>
    7. <span data-ttu-id="b8d08-123">Í hnitanetinu, veljið nýtt gagnasafn af gerðinni **LCS** .</span><span class="sxs-lookup"><span data-stu-id="b8d08-123">In the grid, select the new repository of the **LCS** type.</span></span>

6. <span data-ttu-id="b8d08-124">Smellið á **Opna** til að skoða lista yfir skilgreiningar rafrænnar skýrslugerðar fyrir valda gagnageymslu.</span><span class="sxs-lookup"><span data-stu-id="b8d08-124">Select **Open** to view the list of ER configurations for the selected repository.</span></span>

    <span data-ttu-id="b8d08-125">[![Gagnageymslusíða skilgreininga](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)</span><span class="sxs-lookup"><span data-stu-id="b8d08-125">[![Configuration repositories page](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)</span></span>

    > [!TIP]
    > <span data-ttu-id="b8d08-126">Ef þú í vandræðum með að nota LCS-geymsluna til að sækja skilgreiningar úr samnýttu eignasafni í LCS er hægt að sækja grunnstillingar úr [Altæk geymsla](er-download-configurations-global-repo.md) í staðinn.</span><span class="sxs-lookup"><span data-stu-id="b8d08-126">If you have trouble accessing the LCS repository to download configurations from the Shared asset library in LCS, you can download configurations from the [Global repository](er-download-configurations-global-repo.md) instead.</span></span>

7. <span data-ttu-id="b8d08-127">Í skilgreiningatrénu í vinstri rúðunni er nauðsynleg ER skilgreining valin.</span><span class="sxs-lookup"><span data-stu-id="b8d08-127">In the configurations tree in the left pane, select the required ER configuration.</span></span>
8. <span data-ttu-id="b8d08-128">Á flýtiflipanum **Útgáfur** skal velja nauðsynlega útgáfu skilgreiningar rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="b8d08-128">On the **Versions** FastTab, select the required version of the selected ER configuration.</span></span>
9. <span data-ttu-id="b8d08-129">Veljið **Flytja inn** til að sækja valda útgáfu úr LCS í núverandi tilvik.</span><span class="sxs-lookup"><span data-stu-id="b8d08-129">Select **Import** to download the selected version from LCS to the current instance.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b8d08-130">Hnappurinn **Innflutningur** er ekki tiltækur fyrir útgáfur skilgreininga rafrænnar skýrslugerðar sem þegar eru til staðar í gildandi tilviki.</span><span class="sxs-lookup"><span data-stu-id="b8d08-130">The **Import** button is unavailable for ER configuration versions that are already present in the current instance.</span></span>

    <span data-ttu-id="b8d08-131">[![Síðan Skilgreiningagagnasafn](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)</span><span class="sxs-lookup"><span data-stu-id="b8d08-131">[![Configuration repository page](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)</span></span>

> [!NOTE]
> <span data-ttu-id="b8d08-132">Það fer eftir stillingum rafrænnar skýrslugerðar hvernig skilgreiningar eru villuleitaðar eftir að þær eru fluttar inn.</span><span class="sxs-lookup"><span data-stu-id="b8d08-132">Depending on the ER settings, configurations are validated after they are imported.</span></span> <span data-ttu-id="b8d08-133">Notandi gæti verið látinn vita um vandamál ósamræmi sem fundust.</span><span class="sxs-lookup"><span data-stu-id="b8d08-133">You might be notified about any inconsistency issues that are discovered.</span></span> <span data-ttu-id="b8d08-134">Leysa þarf úr vandamálunum áður en hægt er að nota innflutta útgáfu skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="b8d08-134">You must resolve those issues before you can use the imported configuration version.</span></span> <span data-ttu-id="b8d08-135">Frekari upplýsingar er að finna í lista yfir tengd efnisatriði fyrir þetta efnisatriði.</span><span class="sxs-lookup"><span data-stu-id="b8d08-135">For more information, see the list of related topics for this topic.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b8d08-136">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="b8d08-136">Additional resources</span></span>

[<span data-ttu-id="b8d08-137">Yfirlit yfir rafræna skýrslugerð</span><span class="sxs-lookup"><span data-stu-id="b8d08-137">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="b8d08-138">Sækja skilgreiningar rafrænnar skýrslugerðar úr altækri geymslu skilgreiningarþjónustu</span><span class="sxs-lookup"><span data-stu-id="b8d08-138">Download ER configurations from the Global repository of Configuration service</span></span>](er-download-configurations-global-repo.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
