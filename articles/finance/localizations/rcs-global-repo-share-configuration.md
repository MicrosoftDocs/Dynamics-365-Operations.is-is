---
title: Deila skilgreiningum rafrænnar skýrslugerðar í RCS/altækri geymslu með utanaðkomandi fyrirtækjum
description: Þetta efnisatriði útskýrir hvernig á að deila skilgreiningum rafrænnar skýrslugerðar í Microsoft Regulatory Configuration Services (RCS)/altækri geymslu beint með ytri fyrirtækjum.
author: JaneA07
manager: AnnBe
ms.date: 05/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace, RCS
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 04c46824123906eccbfff18a03974c8043729e0a
ms.sourcegitcommit: 204cec8ca2a6c4474d21dbcd408e369131a47856
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/13/2020
ms.locfileid: "3371250"
---
# <a name="share-electronic-reporting-er-configurations-in-regulatory-configuration-services-rcs-global-repository-with-external-organizations"></a><span data-ttu-id="44ce7-103">Deila skilgreiningum rafrænnar skýrslugerðar í altækri geymslu Regulatory Configuration Services (RCS) með ytri fyrirtækjum</span><span class="sxs-lookup"><span data-stu-id="44ce7-103">Share Electronic reporting (ER) configurations in Regulatory Configuration Services (RCS) Global repository with external organizations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="44ce7-104">Hægt er að nota Microsoft Regulatory Configuration Services (RCS) til að deila skilgreiningum rafrænnar skýrslugerðar og gefa þær út til ytri fyrirtækja.</span><span class="sxs-lookup"><span data-stu-id="44ce7-104">You can use Microsoft Regulatory Configuration Services (RCS) to share Electronic reporting (ER) configurations and then publish them to external organizations.</span></span>

<span data-ttu-id="44ce7-105">Eftirfarandi ferli útskýra hvernig RCS-notandi getur deilt útgáfu af skilgreiningu rafrænnar skýrslugerðar sem hefur verið grunnstillt í RCS-tilviki með ytra fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="44ce7-105">The following procedures explain how an RCS user can share a version of an ER configuration that has been configured in an RCS instance with an external organization.</span></span> <span data-ttu-id="44ce7-106">Áður en hægt er að ljúka við þessar aðgerðir verður að ljúka við eftirfarandi skilyrði:</span><span class="sxs-lookup"><span data-stu-id="44ce7-106">Before you can complete those procedures, you must complete the following prerequisites:</span></span>

- <span data-ttu-id="44ce7-107">Opna RCS-tilvik.</span><span class="sxs-lookup"><span data-stu-id="44ce7-107">Access an RCS instance.</span></span>
- <span data-ttu-id="44ce7-108">Stofna veitanda virkrar skilgreiningar.</span><span class="sxs-lookup"><span data-stu-id="44ce7-108">Create an active configuration provider.</span></span> <span data-ttu-id="44ce7-109">Nánari upplýsingar er að finna í [Stofna skilgreiningarveitendur og merkja þá sem virka](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="44ce7-109">For more information, see [Create configuration providers and mark them as active](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>
- <span data-ttu-id="44ce7-110">Stofna og hlaða upp nýrri útgáfu af skilgreiningu rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="44ce7-110">Create and upload a new version of an ER configuration.</span></span> <span data-ttu-id="44ce7-111">Frekari upplýsingar er að finna í [Stofna og hlaða upp nýrri útgáfu af skilgreiningu rafrænnar skýrslugerðar](rcs-global-repo-upload.md).</span><span class="sxs-lookup"><span data-stu-id="44ce7-111">For more information, see [Create and upload a new version of an Electronic reporting (ER) configuration](rcs-global-repo-upload.md).</span></span>

<span data-ttu-id="44ce7-112">Einnig þarf að ganga úr skugga um að RCS-umhverfi sé úthlutað fyrir fyrirtækið.</span><span class="sxs-lookup"><span data-stu-id="44ce7-112">You must also make sure that an RCS environment is provisioned for your company.</span></span>

1. <span data-ttu-id="44ce7-113">Í Finance and Operations forriti skal opna **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.</span><span class="sxs-lookup"><span data-stu-id="44ce7-113">In a Finance and Operations app, go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="44ce7-114">Ef engu RCS-umhverfi er úthlutað fyrir fyrirtækið skaltu velja **Regulatory Services – ytri skilgreining** og fylgja svo leiðbeiningunum til að úthluta einu slíku.</span><span class="sxs-lookup"><span data-stu-id="44ce7-114">If no RCS environment is provisioned for your company, select **Regulatory services – Configuration external**, and then follow the instructions to provision one.</span></span>

<span data-ttu-id="44ce7-115">Ef RCS-umhverfi hefur þegar verið útvegað fyrir þitt fyrirtæki, notaðu slóðina á síðunni til að fá aðgang að því með því að velja innskráningarvalkostinn.</span><span class="sxs-lookup"><span data-stu-id="44ce7-115">If an RCS environment has been already provisioned for your company, use the page URL to access it by selecting the sign-in option.</span></span>

## <a name="verify-the-configuration-that-you-want-to-share"></a><span data-ttu-id="44ce7-116">Staðfestu skilgreininguna sem á að deila</span><span class="sxs-lookup"><span data-stu-id="44ce7-116">Verify the configuration that you want to share</span></span>

<span data-ttu-id="44ce7-117">Fylgið eftirfarandi skrefum til að staðfesta að skilgreiningunni sem á að nota hafi þegar verið hlaðið upp í altæku geymsluna.</span><span class="sxs-lookup"><span data-stu-id="44ce7-117">Follow these steps to verify that the configuration that you want to share has already been uploaded to the Global repository.</span></span>

1. <span data-ttu-id="44ce7-118">Á vinnusvæðinu **Rafræn skýrslugerð** skal velja **Gagnaeymslur** fyrir skilgreiningarveitu.</span><span class="sxs-lookup"><span data-stu-id="44ce7-118">In the **Electronic reporting** workspace, select **Repositories** for your configuration provider.</span></span>

    ![Veitendur skilgreiningar](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/1_RCS_Repo_for_config_provider.JPG)

2. <span data-ttu-id="44ce7-120">Veldu **Altæk geymsla** \> **Opna**.</span><span class="sxs-lookup"><span data-stu-id="44ce7-120">Select **Global repository** \> **Open**.</span></span>
3. <span data-ttu-id="44ce7-121">Leita að skilgreiningunni sem á að deila.</span><span class="sxs-lookup"><span data-stu-id="44ce7-121">Search for the configuration that you want to share.</span></span> <span data-ttu-id="44ce7-122">Hægt er að nota síureitinn til að þrengja leitina.</span><span class="sxs-lookup"><span data-stu-id="44ce7-122">You can use the filter field to narrow your search.</span></span> <span data-ttu-id="44ce7-123">Ef ekki er hægt að finna skilgreininguna í altæku geymslunni skal fylgja skrefunum í [Stofna og hlaða upp nýrri útgáfu af skilgreiningu rafrænnar skýrslugerðar](rcs-global-repo-upload.md).</span><span class="sxs-lookup"><span data-stu-id="44ce7-123">If you can't find the configuration in the Global repository, follow the steps in [Create and upload a new version of an Electronic reporting (ER) configuration](rcs-global-repo-upload.md).</span></span>

## <a name="share-er-configurations-with-external-organizations"></a><span data-ttu-id="44ce7-124">Deila skilgreiningum rafrænnar skýrslugerðar með utanaðkomandi fyrirtækjum</span><span class="sxs-lookup"><span data-stu-id="44ce7-124">Share ER configurations with external organizations</span></span>

<span data-ttu-id="44ce7-125">Eftir að skilgreining hefur verið stofnuð í skilgreiningarveitu er hægt að samnýta hana beint með ytri fyrirtækjum með því að nota flýtiflipann **Samnýtt með** á síðunni **Altæk skilgreiningargeymsla**.</span><span class="sxs-lookup"><span data-stu-id="44ce7-125">After a configuration has been created under your configuration provider, you can share it directly with external organizations by using the **Shared with** FastTab on the **Global configuration repository** page.</span></span>

1. <span data-ttu-id="44ce7-126">Á vinnusvæðinu **Rafræn skýrslugerð** skal velja **Gagnaeymslur** fyrir skilgreiningarveitu.</span><span class="sxs-lookup"><span data-stu-id="44ce7-126">In the **Electronic reporting** workspace, select **Repositories** for your configuration provider.</span></span>
2. <span data-ttu-id="44ce7-127">Veldu **Altæk geymsla** \> **Opna**.</span><span class="sxs-lookup"><span data-stu-id="44ce7-127">Select **Global repository** \> **Open**.</span></span> 
3. <span data-ttu-id="44ce7-128">Veldu skilgreininguna sem á að deila.</span><span class="sxs-lookup"><span data-stu-id="44ce7-128">Select the configuration that you want to share.</span></span>
4. <span data-ttu-id="44ce7-129">Í **Samnýtt með** flýtiflipanum, veldu **Fyrirtæki**.</span><span class="sxs-lookup"><span data-stu-id="44ce7-129">On the **Shared with** FastTab, select **Organization**.</span></span>

    ![Flýtiflipinn Samnýtt með](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/1_RCS_Repo_for_Share_with_org.JPG)

5. <span data-ttu-id="44ce7-131">Í svarglugganum er fært inn lénsheiti ytra fyrirtækis og síðan valið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="44ce7-131">In the dialog box, enter the domain name for the external organization, and then select **OK**.</span></span>

    ![Samnýta skilgreiningarútgáfu með svarglugga ytra fyrirtækis](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/1_RCS_Repo_for_Share_with_form.JPG)

<span data-ttu-id="44ce7-133">Skilgreiningunni er deilt með ytra fyrirtækinu og er aðgengileg fyrir það fyrirtæki í altæku geymslunni.</span><span class="sxs-lookup"><span data-stu-id="44ce7-133">The configuration is shared with the external organization and is available to that organization in the Global repository.</span></span> <span data-ttu-id="44ce7-134">Þaðan er hægt að flytja hana inn í tilvik fyrirtækisins í RCS eða í tilvik Finance and Operations-forrita.</span><span class="sxs-lookup"><span data-stu-id="44ce7-134">From there, it can be imported into the organization's instance of RCS or into its instances of Finance and Operations apps.</span></span>

![Skilgreiningu deilt með ytra fyrirtæki](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/1_RCS_Repo_for_Share_with_test.com)

6. <span data-ttu-id="44ce7-136">Til að stöðva samnýtingu skilgreiningar sem áður hefur verið deilt með ytra fyrirtæki skal velja skilgreininguna og smella á **Stöðva samnýtingu** og velja síðan **Í lagi**</span><span class="sxs-lookup"><span data-stu-id="44ce7-136">To unshare a configuration that has been previously shared with an external organization, select the configuration and click **Unshare**, and then select **OK**</span></span>
