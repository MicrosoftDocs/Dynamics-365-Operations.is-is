---
title: Úthluta Dynamics 365 Commerce matsumhverfi
description: Þetta efnisatriði útskýrir hvernig á að setja upp að aðgang Microsoft Dynamics 365 Commerce matsumhverfi.
author: psimolin
manager: annbe
ms.date: 11/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: b54216a565c264dfcfe821581fee9df7b5e22323
ms.sourcegitcommit: 715508547f9a71a89a138190e8540686556c753d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/05/2020
ms.locfileid: "4413314"
---
# <a name="provision-a-dynamics-365-commerce-evaluation-environment"></a><span data-ttu-id="385f1-103">Úthluta Dynamics 365 Commerce matsumhverfi</span><span class="sxs-lookup"><span data-stu-id="385f1-103">Provision a Dynamics 365 Commerce evaluation environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="385f1-104">Þetta efnisatriði útskýrir hvernig á að setja upp að aðgang Microsoft Dynamics 365 Commerce matsumhverfi.</span><span class="sxs-lookup"><span data-stu-id="385f1-104">This topic explains how to provision a Microsoft Dynamics 365 Commerce evaluation environment.</span></span>

<span data-ttu-id="385f1-105">Áður en þú byrjar, mælum við með að þú gríptir skjótt í gegnum þetta efni til að fá hugmynd um hvað ferlið krefst.</span><span class="sxs-lookup"><span data-stu-id="385f1-105">Before you begin, we recommend that you take a quick scan through this topic to get an idea of what the process requires.</span></span>

> [!NOTE]
> <span data-ttu-id="385f1-106">Commerce matsumhverfi er almennt ekki í boði og er veitt af samstarfsaðilum og viðskiptavinum á grundvelli beiðna.</span><span class="sxs-lookup"><span data-stu-id="385f1-106">Commerce evaluation environments aren't generally available, and are granted to partners and customers on a per-request basis.</span></span> <span data-ttu-id="385f1-107">Þú ættir að hafa samband við Microsoft samstarfsaðila þinn til að fá aðstoð ef þig vantar frekari upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="385f1-107">For more information, reach out to your Microsoft partner contact.</span></span>

## <a name="overview"></a><span data-ttu-id="385f1-108">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="385f1-108">Overview</span></span>

<span data-ttu-id="385f1-109">Til að hægt sé að úthluta Commerce-matsumhverfi þarf að stofna verk sem er með ákveðið afurðarheiti og gerð.</span><span class="sxs-lookup"><span data-stu-id="385f1-109">To successfully provision a Commerce evaluation environment, you must create a project that has a specific product name and type.</span></span> <span data-ttu-id="385f1-110">Umhverfið og Commerce Scale Unit (CSU) eru einnig með nokkrar ákveðnar færibreytur sem verður að nota þegar áætlun rafræna viðskipta er úthlutað.</span><span class="sxs-lookup"><span data-stu-id="385f1-110">The environment and Commerce Scale Unit (CSU) also have some specific parameters that you must use when you expect to provision e-Commerce later.</span></span> <span data-ttu-id="385f1-111">Leiðbeiningarnar í þessu efnisatriði lýsa öllum skrefunum sem eru nauðsynleg til að ljúka úthlutun og færibreyturnar sem þarf að nota.</span><span class="sxs-lookup"><span data-stu-id="385f1-111">The instructions in this topic describe all the steps that are required to complete provisioning and the parameters that you must use.</span></span>

<span data-ttu-id="385f1-112">Þegar búið er að úthluta Commerce-matsumhverfinu þarf að ljúka nokkrum skrefum eftir úthlutun til að gera það tilbúið fyrir notkun.</span><span class="sxs-lookup"><span data-stu-id="385f1-112">After you successfully provision your Commerce evaluation environment, you must complete a few post-provisioning steps to prepare it for use.</span></span> <span data-ttu-id="385f1-113">Sum skref eru valkvæð, eftir þeim þáttum kerfisins þú vilt meta.</span><span class="sxs-lookup"><span data-stu-id="385f1-113">Some steps are optional, depending on the aspects of the system that you want to evaluate.</span></span> <span data-ttu-id="385f1-114">Þú getur alltaf klárað valfrjálsu skrefin seinna.</span><span class="sxs-lookup"><span data-stu-id="385f1-114">You can always complete the optional steps later.</span></span>

<span data-ttu-id="385f1-115">Frekari upplýsingar um hvernig á að grunnstilla Commerce-matsumhverfið þegar búið er að úthluta því er að finna í [Grunnstilla Commerce-matsumhverfi](cpe-post-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="385f1-115">For information about how to configure your Commerce evaluation environment after you provision it, see [Configure a Commerce evaluation environment](cpe-post-provisioning.md).</span></span> <span data-ttu-id="385f1-116">Frekari upplýsingar um hvernig á að grunnstilla valfrjálsa eiginleika fyrir Commerce-matsumhverfið er að finna í [Grunnstilla valfrjálsa eiginleika fyrir Commerce-matsumhverfið](cpe-optional-features.md).</span><span class="sxs-lookup"><span data-stu-id="385f1-116">For information about how to configure optional features for your Commerce evaluation environment, see [Configure optional features for a Commerce evaluation environment](cpe-optional-features.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="385f1-117">Forkröfur</span><span class="sxs-lookup"><span data-stu-id="385f1-117">Prerequisites</span></span>

<span data-ttu-id="385f1-118">Eftirfarandi skilyrði verða að vera til staðar áður en hægt er að úthluta matsumhverfi í Commerce:</span><span class="sxs-lookup"><span data-stu-id="385f1-118">The following prerequisites must be in place before you can provision your Commerce evaluation environment:</span></span>

- <span data-ttu-id="385f1-119">Þú hefur fengið aðgang að matsforritinu og fengið úthlutað afkastagetu fyrir matsumhverfi.</span><span class="sxs-lookup"><span data-stu-id="385f1-119">You have been onboarded into the evaluation program and granted capacity for an evaluation environment.</span></span>
- <span data-ttu-id="385f1-120">Þú hefur aðgang að Microsoft Dynamics Lifecycle Services (LCS)-gáttinni.</span><span class="sxs-lookup"><span data-stu-id="385f1-120">You have access to the Microsoft Dynamics Lifecycle Services (LCS) portal.</span></span>
- <span data-ttu-id="385f1-121">Þú ert fyrirliggjandi félagi eða viðskiptavinur Microsoft Dynamics 365 og getur stofnað Dynamics 365 Commerce verk.</span><span class="sxs-lookup"><span data-stu-id="385f1-121">You are an existing Microsoft Dynamics 365 partner or customer and are able to create a Dynamics 365 Commerce project.</span></span>
- <span data-ttu-id="385f1-122">Þú ert með stjórnandaaðgang að Microsoft Azure-áskriftinni eða þú ert í samskiptum við umsjónaraðila áskriftar sem getur aðstoðað þig ef þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="385f1-122">You have administrator access to your Microsoft Azure subscription, or you're in contact with a subscription administrator who can assist you if required.</span></span>
- <span data-ttu-id="385f1-123">Þú hefur leigjandakenni þitt fyrir Azure Active Directory (Azure AD) í boði.</span><span class="sxs-lookup"><span data-stu-id="385f1-123">You have your Azure Active Directory (Azure AD) tenant ID available.</span></span>
- <span data-ttu-id="385f1-124">Þú hefur búið til Azure AD-öryggishóp sem hægt er að nota sem kerfisstjórahóp netverslunar og þú ert með kenni hans tiltækt.</span><span class="sxs-lookup"><span data-stu-id="385f1-124">You've created an Azure AD security group that can be used as an e-Commerce system admin group, and you have its ID available.</span></span>
- <span data-ttu-id="385f1-125">Þú hefur búið til Azure AD-öryggishóp sem hægt er að nota sem stjórnandahóp einkunna og umsagna og þú ert með kenni hans tiltækt.</span><span class="sxs-lookup"><span data-stu-id="385f1-125">You've created an Azure AD security group that can be used as a Ratings and Reviews moderator group, and you have its ID available.</span></span> <span data-ttu-id="385f1-126">(Þessi öryggishópur getur verið sá sami og kerfisstjórinn fyrir netkerfi.)</span><span class="sxs-lookup"><span data-stu-id="385f1-126">(This security group can be the same as the e-Commerce system admin group.)</span></span>

<span data-ttu-id="385f1-127">Athugið að þessi listi er ekki tæmandi.</span><span class="sxs-lookup"><span data-stu-id="385f1-127">Note that this list isn't exhaustive.</span></span> <span data-ttu-id="385f1-128">Þú ættir að hafa samband við Microsoft samstarfsaðila þinn til að fá aðstoð ef vandamál koma upp.</span><span class="sxs-lookup"><span data-stu-id="385f1-128">If you experience any issues, reach out to your Microsoft partner contact for assistance.</span></span>

## <a name="provision-your-commerce-evaluation-environment"></a><span data-ttu-id="385f1-129">Skilgreina Commerce matsumhverfi</span><span class="sxs-lookup"><span data-stu-id="385f1-129">Provision your Commerce evaluation environment</span></span>

<span data-ttu-id="385f1-130">Þessar verklagsreglur útskýra hvernig á að úthluta Commerce-matsumhverfi.</span><span class="sxs-lookup"><span data-stu-id="385f1-130">These procedures explain how to provision a Commerce evaluation environment.</span></span> <span data-ttu-id="385f1-131">Þegar búið er að ljúka þeim verður Commerce-matsumhverfið tilbúið fyrir grunnstillingu.</span><span class="sxs-lookup"><span data-stu-id="385f1-131">After you successfully complete them, the Commerce evaluation environment will be ready for configuration.</span></span> <span data-ttu-id="385f1-132">Allar þær aðgerðir sem er lýst hér fara fram í LCS-gáttinni.</span><span class="sxs-lookup"><span data-stu-id="385f1-132">All the activities that are described here occur in the LCS portal.</span></span>

### <a name="create-a-new-project"></a><span data-ttu-id="385f1-133">Stofna nýtt verk</span><span class="sxs-lookup"><span data-stu-id="385f1-133">Create a new project</span></span>

<span data-ttu-id="385f1-134">Til að stofna nýtt verk í LSC skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="385f1-134">To create a new project in LCS, follow these steps.</span></span>

1. <span data-ttu-id="385f1-135">Á heimasíðu LCS velurðu plúsmerkið (**+**) til að búa til verk.</span><span class="sxs-lookup"><span data-stu-id="385f1-135">On the LCS home page, select the plus sign (**+**) to create a project.</span></span>
1. <span data-ttu-id="385f1-136">Fylgdu einu af þessum skrefum á hægri glugganum:</span><span class="sxs-lookup"><span data-stu-id="385f1-136">In the right pane, follow one of these steps:</span></span>

    - <span data-ttu-id="385f1-137">Ef þú ert félagi skaltu velja **Flytja, búa til lausnir og læra**.</span><span class="sxs-lookup"><span data-stu-id="385f1-137">If you're a partner, select **Migrate, create solutions, and learn**.</span></span>
    - <span data-ttu-id="385f1-138">Ef þú ert viðskiptavinur skaltu velja **Væntanleg forsala**.</span><span class="sxs-lookup"><span data-stu-id="385f1-138">If you're a customer, select **Prospective presales**.</span></span>

1. <span data-ttu-id="385f1-139">Færðu inn heiti, lýsingu og iðnað.</span><span class="sxs-lookup"><span data-stu-id="385f1-139">Enter a name, description, and industry.</span></span>
1. <span data-ttu-id="385f1-140">Í reitnum **Heiti afurðar** velurðu **Dynamics 365 Commerce**.</span><span class="sxs-lookup"><span data-stu-id="385f1-140">In the **Product name** field, select **Dynamics 365 Commerce**.</span></span>
1. <span data-ttu-id="385f1-141">Í reitnum **Útgáfa afurðar** velurðu **Dynamics 365 Commerce**.</span><span class="sxs-lookup"><span data-stu-id="385f1-141">In the **Product version** field, select **Dynamics 365 Commerce**.</span></span>
1. <span data-ttu-id="385f1-142">Í reitnum **Aðferð** velurðu **Dynamics Retail útfærsluaðferð**.</span><span class="sxs-lookup"><span data-stu-id="385f1-142">In the **Methodology** field, select **Dynamics Retail implementation methodology**.</span></span>
1. <span data-ttu-id="385f1-143">Valfrjálst: Hægt er að flytja inn hlutverk og notendur úr fyrirliggjandi verki.</span><span class="sxs-lookup"><span data-stu-id="385f1-143">Optional: You can import roles and users from an existing project.</span></span>
1. <span data-ttu-id="385f1-144">Velja **Stofna**.</span><span class="sxs-lookup"><span data-stu-id="385f1-144">Select **Create**.</span></span> <span data-ttu-id="385f1-145">Verksýnin birtist.</span><span class="sxs-lookup"><span data-stu-id="385f1-145">The project view appears.</span></span>

### <a name="add-the-azure-connector"></a><span data-ttu-id="385f1-146">Bættu Azure-tengingunni við</span><span class="sxs-lookup"><span data-stu-id="385f1-146">Add the Azure Connector</span></span>

<span data-ttu-id="385f1-147">Til að bæta Azure-tengingunni við LCS-verk skal fylgja skrefunum í [Ljúka innleiðingarferli Azure Resource Manager](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/arm-onboarding).</span><span class="sxs-lookup"><span data-stu-id="385f1-147">To add the Azure Connector to your LCS project, follow the steps in [Complete the Azure Resource Manager (ARM) onboarding process](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/arm-onboarding).</span></span>

### <a name="deploy-the-environment"></a><span data-ttu-id="385f1-148">Virkjaðu umhverfið</span><span class="sxs-lookup"><span data-stu-id="385f1-148">Deploy the environment</span></span>

<span data-ttu-id="385f1-149">Til að virkja umhverfið skaltu fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="385f1-149">To deploy the environment, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="385f1-150">Þú gætir ekki þurft að klára skref 6, 7 og / eða 8 því að síðum sem hafa einn valkost er sleppt.</span><span class="sxs-lookup"><span data-stu-id="385f1-150">You might not have to complete steps 6, 7, and/or 8, because pages that have a single option are skipped.</span></span> <span data-ttu-id="385f1-151">Þegar þú ert í sýninni **Færibreytur umhverfis** skaltu staðfesta að textinn **Dynamics 365 Commerce - (Forskoðun) - Kynning (10.0.* x* með verkvangsuppfærslu *xx*)\*\* birtist beint fyrir ofan reitinn **Heiti umhverfis**.</span><span class="sxs-lookup"><span data-stu-id="385f1-151">When you're in the **Environment parameters** view, confirm that the text **Dynamics 365 Commerce - Demo (10.0.* x* with Platform update *xx*)\*\* appears directly above the **Environment name** field.</span></span> <span data-ttu-id="385f1-152">Fyrir nánari upplýsingar, sjá myndina sem birtist eftir 8. skref.</span><span class="sxs-lookup"><span data-stu-id="385f1-152">For details, see the illustration that appears after step 8.</span></span>

1. <span data-ttu-id="385f1-153">Í efstu valmyndinni velurðu **Umhverfi í skýi**.</span><span class="sxs-lookup"><span data-stu-id="385f1-153">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="385f1-154">Veldu **Bæta við** til að bæta við umhverfi.</span><span class="sxs-lookup"><span data-stu-id="385f1-154">Select **Add** to add an environment.</span></span>
1. <span data-ttu-id="385f1-155">Í reitnum **Útgáfa forrits**, veldu nýjustu útgáfuna.</span><span class="sxs-lookup"><span data-stu-id="385f1-155">In the **Application version** field, select the most current version.</span></span> <span data-ttu-id="385f1-156">Ef þú hefur sérstaka þörf fyrir að velja aðra forritsútgáfu en nýjustu útgáfuna skaltu ekki velja útgáfu áður **10.0.14**.</span><span class="sxs-lookup"><span data-stu-id="385f1-156">If you have a specific need to select an application version other than the most current version, do not select a version prior to **10.0.14**.</span></span>
1. <span data-ttu-id="385f1-157">Í reitnum **Útgáfa verkvangs**, notarðu verkvangsútgáfuna sem er sjálfkrafa valin fyrir forritsútgáfuna sem þú valdir.</span><span class="sxs-lookup"><span data-stu-id="385f1-157">In the **Platform version** field, use the platform version that is automatically chosen for the application version you selected.</span></span> 

    ![Val á forrita- og verkvangsútgáfum](./media/project1.png)

1. <span data-ttu-id="385f1-159">Veljið **Næst**.</span><span class="sxs-lookup"><span data-stu-id="385f1-159">Select **Next**.</span></span>
1. <span data-ttu-id="385f1-160">Veldu **Kynning** grannfræði umhverfis.</span><span class="sxs-lookup"><span data-stu-id="385f1-160">Select **Demo** as the environment topology.</span></span>

    ![Val á grannfræði umhverfis 1](./media/project2.png)

1. <span data-ttu-id="385f1-162">Á síðunni **Setja upp umhverfi** slærðu inn umhverfisheiti.</span><span class="sxs-lookup"><span data-stu-id="385f1-162">On the **Deploy environment** page, enter an environment name.</span></span> <span data-ttu-id="385f1-163">Hafðu ítarlegar stillingar óbreyttar.</span><span class="sxs-lookup"><span data-stu-id="385f1-163">Leave the advanced settings as they are.</span></span>

    ![Setja upp umhverfissíðu](./media/project4.png)

1. <span data-ttu-id="385f1-165">Stilltu VM stærð eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="385f1-165">Adjust the VM size as required.</span></span> <span data-ttu-id="385f1-166">(Við mælum með VM birgðaeiningunni \[SKU\] **D13 v2**.)</span><span class="sxs-lookup"><span data-stu-id="385f1-166">(We recommend VM stock keeping unit \[SKU\] **D13 v2**.)</span></span>
1. <span data-ttu-id="385f1-167">Skoðaðu verðlagningu og leyfisskilmála og veldu síðan gátreitinn til að gefa til kynna að þú samþykki þá.</span><span class="sxs-lookup"><span data-stu-id="385f1-167">Review the pricing and licensing terms, and then select the check box to indicate that you agree to them.</span></span>
1. <span data-ttu-id="385f1-168">Veljið **Næst**.</span><span class="sxs-lookup"><span data-stu-id="385f1-168">Select **Next**.</span></span>
1. <span data-ttu-id="385f1-169">Á staðfestingarsíðunni staðfestirðu að upplýsingarnar séu réttar og smellir svo á **Setja upp**.</span><span class="sxs-lookup"><span data-stu-id="385f1-169">On the deployment confirmation page, verify that the details are correct, and then select **Deploy**.</span></span> <span data-ttu-id="385f1-170">Þú munt fara aftur í gluggann **Umhverfi í skýi** og umhverfi þitt ætti að birtast á listanum.</span><span class="sxs-lookup"><span data-stu-id="385f1-170">You're returned to the **Cloud-hosted environments** view, and your environment should appear in the list.</span></span>

    <span data-ttu-id="385f1-171">Umbeðið umhverfi þitt birtist í biðröð og síðan er það notað.</span><span class="sxs-lookup"><span data-stu-id="385f1-171">Your requested environment will appear as queued and then deploying.</span></span> <span data-ttu-id="385f1-172">Það tekur nokkurn tíma að klára vinnuflæði umhverfisins.</span><span class="sxs-lookup"><span data-stu-id="385f1-172">The environment workflows will take some time to be completed.</span></span> <span data-ttu-id="385f1-173">Athugaðu því aftur eftir um það bil sex til níu tíma.</span><span class="sxs-lookup"><span data-stu-id="385f1-173">Therefore, check back after approximately six to nine hours.</span></span>

1. <span data-ttu-id="385f1-174">Áður en lengra er haldið skaltu ganga úr skugga um að staða umhverfisins sé **Uppsett**.</span><span class="sxs-lookup"><span data-stu-id="385f1-174">Before you continue, make sure that the status of your environment is **Deployed**.</span></span>

### <a name="initialize-the-commerce-scale-unit-cloud"></a><span data-ttu-id="385f1-175">Frumstilla Commerce Scale Unit (ský)</span><span class="sxs-lookup"><span data-stu-id="385f1-175">Initialize the Commerce Scale Unit (cloud)</span></span>

<span data-ttu-id="385f1-176">Fylgið eftirfarandi skrefum til að hefja CSU.</span><span class="sxs-lookup"><span data-stu-id="385f1-176">To initialize CSU, follow these steps.</span></span>

1. <span data-ttu-id="385f1-177">Í glugganum **Umhverfi í skýi** velurðu umhverfi þitt af listanum.</span><span class="sxs-lookup"><span data-stu-id="385f1-177">In the **Cloud-hosted environments** view, select your environment in the list.</span></span>
1. <span data-ttu-id="385f1-178">Í umhverfissýninni til hægri skaltu velja **Nánari upplýsingar**.</span><span class="sxs-lookup"><span data-stu-id="385f1-178">In the environment view on the right, select **Full details**.</span></span> <span data-ttu-id="385f1-179">Umhverfisupplýsingaskjárinn birtist.</span><span class="sxs-lookup"><span data-stu-id="385f1-179">The environment details view appears.</span></span>
1. <span data-ttu-id="385f1-180">Undir **Eiginleikar umhverfis** velurðu **Stjórna**.</span><span class="sxs-lookup"><span data-stu-id="385f1-180">Under **Environment features**, select **Manage**.</span></span>
1. <span data-ttu-id="385f1-181">Á flipanum **Commerce** velurðu **Frumstilla**.</span><span class="sxs-lookup"><span data-stu-id="385f1-181">On the **Commerce** tab, select **Initialize**.</span></span> <span data-ttu-id="385f1-182">Skjár CSU frumstillingarifæribreyta birtist.</span><span class="sxs-lookup"><span data-stu-id="385f1-182">The CSU initialization parameters view appears.</span></span>
1. <span data-ttu-id="385f1-183">Í reitnum **Svæði** skal velja svæðið sem er það sama eða nálægt því svæði umhverfið er notað í.</span><span class="sxs-lookup"><span data-stu-id="385f1-183">In the **Region** field, select the region that is the same or close to the region that you deployed the environment to.</span></span>
1. <span data-ttu-id="385f1-184">Skildu reitinn **Útgáfa** eftir eins og hann er.</span><span class="sxs-lookup"><span data-stu-id="385f1-184">Leave the **Version** field as it is.</span></span>
1. <span data-ttu-id="385f1-185">Veldu **Frumstilla**.</span><span class="sxs-lookup"><span data-stu-id="385f1-185">Select **Initialize**.</span></span>
1. <span data-ttu-id="385f1-186">Á staðfestingarsíðunni staðfestirðu að upplýsingarnar séu réttar og smellir svo á **Já**.</span><span class="sxs-lookup"><span data-stu-id="385f1-186">On the deployment confirmation page, verify that the details are correct, and then select **Yes**.</span></span> <span data-ttu-id="385f1-187">Skjárinn **Commerce-stjórnun** birtist aftur, þar sem flipinn **Commerce** er valinn.</span><span class="sxs-lookup"><span data-stu-id="385f1-187">The **Commerce management** view displays again, where the **Commerce** tab is selected.</span></span> <span data-ttu-id="385f1-188">CSU þinn hefur verið í biðröð vegna úthlutunar.</span><span class="sxs-lookup"><span data-stu-id="385f1-188">Your CSU has been queued for provisioning.</span></span>
1. <span data-ttu-id="385f1-189">Áður en lengra er haldið skaltu ganga úr skugga um að staða CSU sé **Tókst**.</span><span class="sxs-lookup"><span data-stu-id="385f1-189">Before you continue, make sure that the status of your CSU is **Success**.</span></span> <span data-ttu-id="385f1-190">Frumstilling tekur um það bil tvær til fimm klukkustundir.</span><span class="sxs-lookup"><span data-stu-id="385f1-190">Initialization takes approximately two to five hours.</span></span>

<span data-ttu-id="385f1-191">Ef þú finnur ekki tengilinn **Stjórna** í upplýsingayfirliti umhverfis skal hafa samband við tengiliðann hjá Microsoft til að fá aðstoð.</span><span class="sxs-lookup"><span data-stu-id="385f1-191">If you can't find the **Manage** link in the environment details view, reach out to your Microsoft contact for assistance.</span></span>

### <a name="initialize-e-commerce"></a><span data-ttu-id="385f1-192">Frumstilla rafræn viðskipti</span><span class="sxs-lookup"><span data-stu-id="385f1-192">Initialize e-Commerce</span></span>

<span data-ttu-id="385f1-193">Fylgið eftirfarandi skrefum til að frumstilla e-Commerce.</span><span class="sxs-lookup"><span data-stu-id="385f1-193">To initialize e-Commerce, follow these steps.</span></span>

1. <span data-ttu-id="385f1-194">Í flipanum **e-Commerce** skal fara yfir matssamþykki og velja svo **Uppsetning**.</span><span class="sxs-lookup"><span data-stu-id="385f1-194">On the **e-Commerce** tab, review the evaluation consent, and then select **Setup**.</span></span>
1. <span data-ttu-id="385f1-195">Í reitinn **Heiti e-Commerce-umhverfis** skal færa inn heiti.</span><span class="sxs-lookup"><span data-stu-id="385f1-195">In the **e-Commerce environment name** field, enter a name.</span></span> <span data-ttu-id="385f1-196">Hafa skal í huga að þetta heiti mun birtast á sumum vefslóðum sem benda á tilvik þitt af rafrænum viðskiptum.</span><span class="sxs-lookup"><span data-stu-id="385f1-196">Be aware that this name will appear in some of the URLs that point to your e-Commerce instance.</span></span>
1. <span data-ttu-id="385f1-197">Í reitnum **Heiti Commerce Scale Unit** skal velja CSU í listanum.</span><span class="sxs-lookup"><span data-stu-id="385f1-197">In the **Commerce Scale Unit name** field, select your CSU in the list.</span></span> <span data-ttu-id="385f1-198">(Listinn ætti aðeins að hafa einn valkost.)</span><span class="sxs-lookup"><span data-stu-id="385f1-198">(The list should have only one option.)</span></span>

    <span data-ttu-id="385f1-199">Reiturinn **Svæði rafrænna viðskipta** er stillt sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="385f1-199">The **e-Commerce geography** field is set automatically.</span></span>

1. <span data-ttu-id="385f1-200">Veldu **Næst** til að halda áfram.</span><span class="sxs-lookup"><span data-stu-id="385f1-200">Select **Next** to continue.</span></span>
1. <span data-ttu-id="385f1-201">Í reitnum **Studd hýsilheiti** slærðu inn gilt lén, eins og `www.fabrikam.com`.</span><span class="sxs-lookup"><span data-stu-id="385f1-201">In the **Supported host names** field, enter any valid domain, such as `www.fabrikam.com`.</span></span>
1. <span data-ttu-id="385f1-202">Í reitinn **AAD-öryggisflokkur fyrir kerfisstjóra** skal færa inn fyrstu stafina í heiti öryggisflokksins sem á að nota og síðan velja stækkunarglerið til að skoða leitarniðurstöðurnar.</span><span class="sxs-lookup"><span data-stu-id="385f1-202">In the **AAD security group for system admin** field, enter the first few letters of the name of the security group that you want to use, and then select the magnifying glass symbol to view the search results.</span></span> <span data-ttu-id="385f1-203">Veljið réttan öryggisflokk í listanum.</span><span class="sxs-lookup"><span data-stu-id="385f1-203">Select the correct security group in the list.</span></span>
1.  <span data-ttu-id="385f1-204">Í reitinn **AAD-öryggisflokkur fyrir ritstjóra einkunna og umsagna** skal færa inn fyrstu stafina í heiti öryggisflokksins sem á að nota og síðan velja stækkunarglerið til að skoða leitarniðurstöðurnar.</span><span class="sxs-lookup"><span data-stu-id="385f1-204">In the **AAD security group for ratings and review moderator** field, enter the first few letters of the name of the security group that you want to use, and then select the magnifying glass symbol to view the search results.</span></span> <span data-ttu-id="385f1-205">Veljið réttan öryggisflokk í listanum.</span><span class="sxs-lookup"><span data-stu-id="385f1-205">Select the correct security group in the list.</span></span>
1. <span data-ttu-id="385f1-206">Haldið valkostinum **Virkja þjónustu einkunna og umsagna** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="385f1-206">Leave the **Enable ratings and review service** option set to **Yes**.</span></span>
1. <span data-ttu-id="385f1-207">Veldu **Frumstilla**.</span><span class="sxs-lookup"><span data-stu-id="385f1-207">Select **Initialize**.</span></span> <span data-ttu-id="385f1-208">Skjárinn **Commerce-stjórnun** birtist aftur, þar sem flipinn **e-Commerce** er valinn.</span><span class="sxs-lookup"><span data-stu-id="385f1-208">The **Commerce management** view displays again, where the **e-Commerce** tab is selected.</span></span> <span data-ttu-id="385f1-209">Frumstilling rafrænna viðskipta er hafin.</span><span class="sxs-lookup"><span data-stu-id="385f1-209">E-Commerce initialization has started.</span></span>
1. <span data-ttu-id="385f1-210">Áður en lengra er haldið skaltu bíða þar til staða frumstillingar í netverslun er **Frumstilling tókst**.</span><span class="sxs-lookup"><span data-stu-id="385f1-210">Before you continue, wait until the status of e-Commerce initialization is **Initialization successful**.</span></span>
1. <span data-ttu-id="385f1-211">Undir **Krækjur** neðst til hægri, skrifaðu vefslóðirnar fyrir eftirfarandi tengla:</span><span class="sxs-lookup"><span data-stu-id="385f1-211">Under **Links** in the lower right, make a note of the URLs for the following links:</span></span>

    * <span data-ttu-id="385f1-212">**rafræn viðskipti síða** - Hlekkurinn á rótina á netverslunarsíðunni þinni.</span><span class="sxs-lookup"><span data-stu-id="385f1-212">**e-Commerce site** – The link to the root of your e-Commerce site.</span></span>
    * <span data-ttu-id="385f1-213">**Commerce-vefssmiður** - Tengillinn á verkfæri svæðisstjórnunar.</span><span class="sxs-lookup"><span data-stu-id="385f1-213">**Commerce site builder** – The link to the site management tool.</span></span>

## <a name="next-steps"></a><span data-ttu-id="385f1-214">Næstu skref</span><span class="sxs-lookup"><span data-stu-id="385f1-214">Next steps</span></span>

<span data-ttu-id="385f1-215">Til að halda áfram að úthluta og grunnstilla Commerce-matsumhverfið skal skoða [Grunnstilla Commerce-matsumhverfi](cpe-post-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="385f1-215">To continue the process of provisioning and configuring your Commerce evaluation environment, see [Configure a Commerce evaluation environment](cpe-post-provisioning.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="385f1-216">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="385f1-216">Additional resources</span></span>

[<span data-ttu-id="385f1-217">Dynamics 365 Commerce yfirlit yfir forskoðunarumhverfi</span><span class="sxs-lookup"><span data-stu-id="385f1-217">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="385f1-218">Stilla Dynamics 365 Commerce matsumhverfi</span><span class="sxs-lookup"><span data-stu-id="385f1-218">Configure a Dynamics 365 Commerce evaluation environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="385f1-219">Skilgreina BOPIS í Dynamics 365 Commerce í matsumhverfi</span><span class="sxs-lookup"><span data-stu-id="385f1-219">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="385f1-220">Skilgreina valfrjálsa eiginleika fyrir Dynamics 365 Commerce matsumhverfi</span><span class="sxs-lookup"><span data-stu-id="385f1-220">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="385f1-221">algengar spurningar um Dynamics 365 Commerce matsumhverfi</span><span class="sxs-lookup"><span data-stu-id="385f1-221">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="385f1-222">Microsoft Dynamics Lifecycle Services (LSC)</span><span class="sxs-lookup"><span data-stu-id="385f1-222">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="385f1-223">Commerce Scale Unit (ský)</span><span class="sxs-lookup"><span data-stu-id="385f1-223">Commerce Scale Unit (cloud)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="385f1-224">Microsoft Azure-gátt</span><span class="sxs-lookup"><span data-stu-id="385f1-224">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="385f1-225">Dynamics 365 Commerce vefsvæði</span><span class="sxs-lookup"><span data-stu-id="385f1-225">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)
