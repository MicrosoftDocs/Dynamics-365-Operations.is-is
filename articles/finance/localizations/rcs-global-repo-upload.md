---
title: Stofna skilgreiningar rafrænnar skýrslugerðar í RCS og hlaða þeim upp í altæka geymslu
description: Þetta efnisatriði útskýrir hvernig á að stofna rafræna skýrslugerð (ER) í Microsoft Regulatory Configuration Services (RCS) og hlaða henni upp í altæku geymsluna.
author: JaneA07
ms.date: 09/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace, RCS
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: a138fd4b525077f12f6575f4b10f682728b71203
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838720"
---
# <a name="create-er-configurations-in-regulatory-configuration-services-rcs-and-upload-them-to-the-global-repository"></a><span data-ttu-id="f78a0-103">Stofna skilgreiningar rafrænnar skýrslugerðar í Regulatory Configuration Services (RCS) og hlaða þeim upp í altæka geymslu</span><span class="sxs-lookup"><span data-stu-id="f78a0-103">Create ER configurations in Regulatory Configuration Services (RCS) and upload them to the Global repository</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f78a0-104">Hægt er að nota Microsoft Regulatory Configuration Services (RCS) til að hanna skilgreiningar rafrænnar skýrslugerðar (ER) og birta þær þannig að hægt sé að nota þær í fyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="f78a0-104">You can use Microsoft Regulatory Configuration Services (RCS) to design Electronic reporting (ER) configurations and publish them so that they can be used in your organization.</span></span>

<span data-ttu-id="f78a0-105">Eftirfarandi ferli útskýra hvernig notandi í hlutverki kerfisstjóra eða þróunaraðila rafrænnar skýrslugerðar getur stofnað afleidda útgáfu af skilgreiningu rafrænnar skýrslugerðar sem hefur verið grunnstillt í RCS-tilviki og hlaðið síðan upp afleiddri skilgreiningu í altæku geymsluna.</span><span class="sxs-lookup"><span data-stu-id="f78a0-105">The following procedures explain how a user in the System Administrator or Electronic Reporting Developer role can create a derived version of an ER configuration that has been configured in an RCS instance, and then upload the derived configuration to the Global repository.</span></span> 

<span data-ttu-id="f78a0-106">Áður en hægt er að ljúka við þessar aðgerðir verður að ljúka við eftirfarandi skilyrði:</span><span class="sxs-lookup"><span data-stu-id="f78a0-106">Before you can complete those procedures, you must complete the following prerequisites:</span></span>

- <span data-ttu-id="f78a0-107">Opna RCS-tilvik.</span><span class="sxs-lookup"><span data-stu-id="f78a0-107">Access an RCS instance.</span></span>
- <span data-ttu-id="f78a0-108">Stofna veitanda virkrar skilgreiningar.</span><span class="sxs-lookup"><span data-stu-id="f78a0-108">Create an active configuration provider.</span></span> <span data-ttu-id="f78a0-109">Nánari upplýsingar er að finna í [Stofna skilgreiningarveitendur og merkja þá sem virka](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="f78a0-109">For more information, see [Create configuration providers and mark them as active](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

<span data-ttu-id="f78a0-110">Einnig þarf að ganga úr skugga um að RCS-umhverfi sé úthlutað fyrir fyrirtækið.</span><span class="sxs-lookup"><span data-stu-id="f78a0-110">You must also make sure that an RCS environment is provisioned for your company.</span></span>

1. <span data-ttu-id="f78a0-111">Í Finance and Operations forriti skal opna **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.</span><span class="sxs-lookup"><span data-stu-id="f78a0-111">In a Finance and Operations app, go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="f78a0-112">Ef engu RCS-umhverfi er úthlutað fyrir fyrirtækið skaltu velja **Regulatory Services – ytri skilgreining** og fylgja svo leiðbeiningunum til að úthluta einu slíku.</span><span class="sxs-lookup"><span data-stu-id="f78a0-112">If no RCS environment is provisioned for your company, select **Regulatory services – Configuration external**, and then follow the instructions to provision one.</span></span>

<span data-ttu-id="f78a0-113">Ef RCS-umhverfi hefur þegar verið útvegað fyrir þitt fyrirtæki, notaðu slóðina á síðunni til að fá aðgang að því með því að velja innskráningarvalkostinn.</span><span class="sxs-lookup"><span data-stu-id="f78a0-113">If an RCS environment has been already provisioned for your company, use the page URL to access it by selecting the sign-in option.</span></span>

## <a name="create-a-derived-version-of-a-configuration-in-rcs"></a><span data-ttu-id="f78a0-114">Búa til afleidda útgáfu af skilgreiningu í RCS</span><span class="sxs-lookup"><span data-stu-id="f78a0-114">Create a derived version of a configuration in RCS</span></span>

1. <span data-ttu-id="f78a0-115">Á vinnusvæðinu **Rafræn skýrslugerð** skal ganga úr skugga um að notandi sé með virka skilgreiningarveitu fyrir fyrirtækið.</span><span class="sxs-lookup"><span data-stu-id="f78a0-115">In the **Electronic reporting** workspace, verify that you have an active configuration provider for your organization.</span></span> 
2. <span data-ttu-id="f78a0-116">Veldu **Skilgreiningar skýrslugerðar**.</span><span class="sxs-lookup"><span data-stu-id="f78a0-116">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="f78a0-117">Veldu skilgreininguna sem ætlunin er að fá nýja útgáfu úr.</span><span class="sxs-lookup"><span data-stu-id="f78a0-117">Select the configuration that you want to derive a new version from.</span></span> <span data-ttu-id="f78a0-118">Hægt er að nota síureitinn fyrir ofan tréð til að þrengja leitina.</span><span class="sxs-lookup"><span data-stu-id="f78a0-118">You can use the filter field above the tree to narrow your search.</span></span>
4. <span data-ttu-id="f78a0-119">Veljið **Stofna skilgreiningu** \> **Leiða af nafni**.</span><span class="sxs-lookup"><span data-stu-id="f78a0-119">Select **Create configuration** \> **Derive from Name**.</span></span>
5. <span data-ttu-id="f78a0-120">Sláið inn heiti og lýsingu og veljið svo **Stofna skilgreiningu** til að búa til nýja afleidda útgáfu.</span><span class="sxs-lookup"><span data-stu-id="f78a0-120">Enter a name and description, and then select **Create configuration** to create a new derived version.</span></span>
6. <span data-ttu-id="f78a0-121">Velja skal nýlega afleidda skilgreiningu, bæta við lýsingu á útgáfunni og velja síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="f78a0-121">Select the newly derived configuration, add a description of the version, and then select **OK**.</span></span> <span data-ttu-id="f78a0-122">Stöðu skilgreiningarinnar er breytt í **Lokið**.</span><span class="sxs-lookup"><span data-stu-id="f78a0-122">The status of the configuration to is changed to **Completed**.</span></span>

![Nýjar skilgreiningarútgáfur í RCS](media/RCS_CompleteConfig.JPG)

> [!NOTE]
> <span data-ttu-id="f78a0-124">Þegar stöðu skilgreiningarinnar er breytt gæti notandi fengið villuboð við villuleit sem tengjast tengdu forritunum.</span><span class="sxs-lookup"><span data-stu-id="f78a0-124">When the configuration status is changed, you might receive a validation error message that is related to the connected applications.</span></span> <span data-ttu-id="f78a0-125">Til að slökkva á villuleit, á aðgerðasvæði á flipanum **Skilgreiningar**, skal velja **Færibreytur notanda** og stilla síðan **Sleppa villuprófun við stöðubreytingu skilgreiningarinnar og endurreikning grunns** valkostinn á **Já**</span><span class="sxs-lookup"><span data-stu-id="f78a0-125">To turn off the validation, on the Action Pane on the **Configurations** tab, select **User parameters**, and then set the **Skip validation at configuration's status change and rebase** option to **Yes**</span></span> 

## <a name="upload-a-configuration-to-the-global-repository"></a><span data-ttu-id="f78a0-126">Hlaða skilgreiningu upp í altæku geymsluna</span><span class="sxs-lookup"><span data-stu-id="f78a0-126">Upload a configuration to the Global repository</span></span>

<span data-ttu-id="f78a0-127">Til að deila nýrri eða afleiddri skilgreiningu með fyrirtækinu er hægt að hlaða henni upp í altæku geymsluna.</span><span class="sxs-lookup"><span data-stu-id="f78a0-127">To share a new or derived configuration with your organization, you can upload it to the Global repository.</span></span>

1. <span data-ttu-id="f78a0-128">Velja skal lokna útgáfu af skilgreiningunni og síðan velja **Hlaða upp í gagnageymslu**.</span><span class="sxs-lookup"><span data-stu-id="f78a0-128">Select the completed version of the configuration, and then select **Upload into repository**.</span></span>
2. <span data-ttu-id="f78a0-129">Veldu **Altækt (Microsoft)** valkostinn og veldu síðan **Hlaða upp**.</span><span class="sxs-lookup"><span data-stu-id="f78a0-129">Select the **Global (Microsoft)** option, and then select **Upload**.</span></span>

    ![Valkostir fyrir upphleðslu í gagnageymslu](media/RCS_Upload_to_GlobalRepo_options.JPG)

3. <span data-ttu-id="f78a0-131">Í staðfestingarglugganum velurðu **Já**.</span><span class="sxs-lookup"><span data-stu-id="f78a0-131">In the confirmation message box, select **Yes**.</span></span> 
4. <span data-ttu-id="f78a0-132">Uppfæra skal lýsinguna á útgáfunni þar sem þess er krafist og velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="f78a0-132">Update the description of the version as required, and then select **OK**.</span></span> 

<span data-ttu-id="f78a0-133">Staða skilgreiningarinnar er uppfærð í **Deila** og grunnstillingunni er hlaðið upp í altæku geymsluna.</span><span class="sxs-lookup"><span data-stu-id="f78a0-133">The status of the configuration is updated to **Share**, and the configuration is uploaded to the Global repository.</span></span> <span data-ttu-id="f78a0-134">Þaðan er hægt að vinna með hana á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="f78a0-134">From there, you can work with it in the following ways:</span></span>

- <span data-ttu-id="f78a0-135">Flytja hana inn í Dynamics 365-tilvik.</span><span class="sxs-lookup"><span data-stu-id="f78a0-135">Import it into your Dynamics 365 instance.</span></span> <span data-ttu-id="f78a0-136">Frekari upplýsingar er að finna í [(Rafræn skýrslugerð) Flytja inn skilgreiningar úr RCS](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md).</span><span class="sxs-lookup"><span data-stu-id="f78a0-136">For more information, see [(ER) Import configurations from RCS](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md).</span></span>
- <span data-ttu-id="f78a0-137">Deilið með þriðja aðila eða ytra fyrirtæki, sjá [Grunnstillingar RCS-samnýttrar rafrænnar skýrslugerðar (ER) með ytri fyrirtækjum](rcs-global-repo-share-configuration.md)</span><span class="sxs-lookup"><span data-stu-id="f78a0-137">Share it with a third party or an external organization, see [RCS Share Electronic reporting (ER) configurations with external organizations](rcs-global-repo-share-configuration.md)</span></span>

    ![Afleidd skilgreiningarútgáfa af Intrastat Contoso í altæku geymslunni](media/RCS_Config_upload_GlobalRepo.JPG)

## <a name="delete-a-configuration-from-the-global-repository"></a><span data-ttu-id="f78a0-139">Eyða skilgreiningu úr altæku geymslunni</span><span class="sxs-lookup"><span data-stu-id="f78a0-139">Delete a configuration from the Global repository</span></span>
<span data-ttu-id="f78a0-140">Ljúkið eftirfarandi skrefum til að eyða skilgreiningu sem fyrirtækið hefur búið til.</span><span class="sxs-lookup"><span data-stu-id="f78a0-140">Complete the following steps to delete a configuration that your organization has created.</span></span>

1. <span data-ttu-id="f78a0-141">Á vinnusvæðinu **Rafræn skýrslugerð** skal ganga úr skugga um að skilgreiningarveitan sé **Virk**.</span><span class="sxs-lookup"><span data-stu-id="f78a0-141">In the **Electronic reporting** workspace, verify that your configuration provider is **Active**.</span></span> <span data-ttu-id="f78a0-142">Nánari upplýsingar er að finna í [Stofna skilgreiningarveitendur og merkja þá sem virka](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="f78a0-142">For more information, see [Create configuration providers and mark them as active](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>
2. <span data-ttu-id="f78a0-143">Á virkri skilgreiningarveitu skal velja **geymslu**.</span><span class="sxs-lookup"><span data-stu-id="f78a0-143">On your active configuration provider, select **repository**.</span></span>
3. <span data-ttu-id="f78a0-144">Velja skal geymslugerðina **Altæk** og velja **Opna**.</span><span class="sxs-lookup"><span data-stu-id="f78a0-144">Select the repository type **Global**, and select **Open**.</span></span>
4. <span data-ttu-id="f78a0-145">Í flýtiflipanum **Sía** skal finna skilgreininguna sem á að eyða með því að nota virknina **Sía**.</span><span class="sxs-lookup"><span data-stu-id="f78a0-145">On the **Filter** FastTab, find the configuration that you want to delete by using the **Filter** functionality.</span></span>
5. <span data-ttu-id="f78a0-146">Í flýtiflipanum **Útgáfa** skal velja útgáfu skilgreiningarinnar sem á að eyða og síðan velja **Eyða**:</span><span class="sxs-lookup"><span data-stu-id="f78a0-146">On the **Version** FastTab, select the version of the configuration that you want to delete, and then select **Delete**:</span></span>

    ![Eyða skilgreiningu úr altækri geymslu](media/RCS_Delete_from_GlobalRepo.JPG)

6. <span data-ttu-id="f78a0-148">Í staðfestingarglugganum velurðu **Já**.</span><span class="sxs-lookup"><span data-stu-id="f78a0-148">In the confirmation message box, select **Yes**.</span></span>

    ![Eyða staðfestingarboðum um útgáfu skilgreiningar](media/RCS_Delete_from_GlobalRepo_Msg.JPG)
 
<span data-ttu-id="f78a0-150">Skilgreiningarútgáfunni er eytt og staðfestingarboð eru sýnd.</span><span class="sxs-lookup"><span data-stu-id="f78a0-150">The configuration version is deleted, and confirmation message is shown.</span></span> 

> [!NOTE]
> <span data-ttu-id="f78a0-151">Aðeins er hægt að eyða skilgreiningum af skilgreiningarveitunni sem stofnaði þær.</span><span class="sxs-lookup"><span data-stu-id="f78a0-151">Configurations can only be deleted by the Configuration provider that created them.</span></span> <span data-ttu-id="f78a0-152">Ef skilgreiningunni hefur verið deilt með öðru fyrirtæki verður að stöðva samnýtingu hennar áður en henni er eytt.</span><span class="sxs-lookup"><span data-stu-id="f78a0-152">If the configuration has been shared with another organization, the configuration will need to be unshared before you delete it.</span></span>
 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]